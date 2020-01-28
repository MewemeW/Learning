
> 多线程多进程比较
```python
import multiprocessing as mp
import threading as td
import time


def timer(fun):
    def calculateTime():
        start = time.clock()
        fun()
        end = time.clock()
        print(f'函数运行时间：{str(end - start)}')

    return calculateTime


def job(q):
    res = 0
    for i in range(1000000):
        res += i + i ** 2 + i ** 3
    q.put(res)  # queue


@timer
def multicore():
    q = mp.Queue()
    p1 = mp.Process(target=job, args=(q,))
    p2 = mp.Process(target=job, args=(q,))
    p1.start()
    p2.start()
    p1.join()
    p2.join()
    res1 = q.get()
    res2 = q.get()
    print('multicore:', res1 + res2)


@timer
def normal():
    res = 0
    for _ in range(2):
        for i in range(1000000):
            res += i + i ** 2 + i ** 3
    print('normal:', res)


@timer
def multithread():
    q = mp.Queue()
    t1 = td.Thread(target=job, args=(q,))
    t2 = td.Thread(target=job, args=(q,))
    t1.start()
    t2.start()
    t1.join()
    t2.join()
    res1 = q.get()
    res2 = q.get()
    print('multithread:', res1 + res2)


if __name__ == '__main__':
    normal()
    multithread()
    multicore()
```

> 进程池
```python
import multiprocessing as mp


def job(x):
    return x * x


def multicore():
    pool = mp.Pool()
    res = pool.map(job, range(10))
    print(res)
    res = pool.apply_async(job, (2,))
    print(res.get())
    multi_res = [pool.apply_async(job, (i,)) for i in range(10)]
    print([res.get() for res in multi_res])


if __name__ == '__main__':
    multicore()
```


> 进程锁 & 共享内存

```python
import multiprocessing as mp
import time

def job(v, num, l):
    l.acquire()
    for _ in range(10):
        time.sleep(0.1)
        v.value += num
        print(v.value)
    l.release()

def multicore():
    l = mp.Lock()
    v = mp.Value('i', 0)
    p1 = mp.Process(target=job, args=(v, 1, l))
    p2 = mp.Process(target=job, args=(v, 3, l))
    p1.start()
    p2.start()
    p1.join()
    p2.join()

if __name__ == '__main__':
    multicore()
```
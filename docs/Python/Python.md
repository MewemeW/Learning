# Python Basic

> 变量

### 快速交换

```python
a, b = 1, 2
a, b = b, a
print(a, b)
```


> 函数

### 自定义函数

```python
def fun():
    print('hello word!')

fun()
```

### 函数参数
```python
def fun(arg, *args, **kwargs):
    print(arg)
    print(args)
    print(kwargs)


fun(1, 2, 3, 2, 3, name='cao', email='chensy@qq.com')
```

> 高级函数

### `filter`
```python
ls = [1, 2, 3, 4, 5, 6]
print(list(filter(lambda x: x % 2 == 0, ls)))
```


> 类

### `__var__` 前后双下划线 魔法方法


### `__call__` 可调用对象

```python
class C():

    def __init__(self):
        pass

    def __call__(self, *args, **kwargs):
        print('This is class C')


print(callable(C))
c = C()
print(callable(c), c())
```

### 类装饰器



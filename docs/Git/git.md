### Git

#### 版本
- git —version

#### 配置
- git config —global user.name 'Chensy'
- git config —global user.email 'chensy.cao@foxmail.com'

#### 查看配置
- Git config -l

#### 初始化
- git init folder

#### 添加文件&commit
- git add . && git commit -m '1'

#### 查看日志
- git log —oneline

#### 远程仓
- Git remote
- Git remote -v

#### 推送到远程
- git push -u GitHub mster

#### 克隆远程仓
- git clone https://...

> `.gitignore` 忽略 `Pycharm` `.idea` 文件夹

- 如果`.gitignore`文件是后续添加的
- 需要先清除`.idea`的`git`缓存

```git
git rm -r --cached .idea
```


```bash
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/CaoChensy/MyLearning.git
git push -u origin master
```

- 更改远程 remote

```bash
git remote set-url origin URL
```

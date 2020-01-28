> `.gitignore` 忽略 `Pycharm` `.idea` 文件夹

- 如果`.gitignore`文件是后续添加的
- 需要先清除`.idea`的`git`缓存

```git
git rm -r --cached .idea
```
<h3><center>Git</center></h3>
- git —version
- git config —global user.name 'Chensy'
- git config —global user.email 'chensy.cao@foxmail.com'
- Git config -l
- git init folder
- git add . && git commit -m '1'
- git log —oneline
- Git remote
- Git remote -v
- git push -u GitHub mster
- git clone https://...

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
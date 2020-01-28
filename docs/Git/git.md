> `.gitignore` 忽略 `Pycharm` `.idea` 文件夹

- 如果`.gitignore`文件是后续添加的
- 需要先清除`.idea`的`git`缓存

```git
git rm -r --cached .idea
```

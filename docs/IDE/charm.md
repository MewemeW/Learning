### 文件头信息

找到该路径并添加以下信息
> `File->settings->Editor->File and Code Templates->Python Script` 

```bash
# -*- coding: utf-8 -*-
# @Time    : ${DATE} ${TIME}
# @Author  : Your name
# @Site    : ${SITE}
# @File    : ${NAME}.py
# @Software: ${PRODUCT_NAME}
```

### Autopep8

```bash
pip install autopep8
```

> `Settings -> Tools -> External Tools ->界面框点击“+”`

```bash
Name: AutoPep8
Description: autopep8 your code
Program: autopep8
Arguments: --in-place --aggressive --aggressive $FilePath$
Working directory: $ProjectFileDir$
Output filters: $FILE_PATH$\:$LINE$\:$COLUMN$\:.*
```

### Git

> Clone

**Step 1 复制远程仓链接**

<img src='../img/copy_git.png' width='720px'>

**Step 2 Clone 远程仓到本地**

<img src='../img/clone.png' width='720px'>

**URL 为远程仓地址**
**Directory 为本地地址**

<img src='../img/clone_site.png' width='720px'>

**Step 3 Checkout 切换到自己的分支**

<img src='../img/checkout.png' width='720px'>

**比较自己的分支与 origin/master 分支的异同**
*下图展示了 origin/master 相对于自己的分支多出来的 commit*

<img src='../img/compare_with_origin_master.png' width='720px'>

**选择 merge into current 后再查看与 origin/master 分支的异同，发现自己的分支与 origin/master 分支完全相同**
<img src='../img/compare_agin.png' width='720px'>

> Add  new line

**在自己的分支上增加相应内容**
<img src='../img/add_line.png' width='720px'>



**commit 自己的修改内容**
- Auther: Your Name
- Commit Message: 本次 Commit 的备注信息
- 选择 Commit and Push 将自己的分支推送到GitHub

<img src='../img/commit.png' width='720px'>

**Push Info**

<img src='../img/push.png' width='720px'>

**推送成功信息**
<img src='../img/push_success.png' width='720px'>

**管理员去GitHub页面，已经发现新的分支修改可以提起PR**
<img src='../img/back_to_git.png' width='720px'>

**详细代码修改信息**
<img src='../img/pr.png' width='720px'>











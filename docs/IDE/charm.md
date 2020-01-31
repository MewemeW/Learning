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

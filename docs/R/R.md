# R语言也是能发财的语言
> 这是一个终身学习管理的文档。

> 这是另外一个章节。
### 在Jupyter Notebook 中配置 IRkernel

```bash
install.packages('IRkernel',repos='http://cran.us.r-project.org')
IRkernel::installspec()
IRkernel::installspec(user  =  FALSE)
```


### R语言镜像配置
```R
# 设置输出图的大小
# options(repr.plot.width=6, repr.plot.height=4)
# 设置国内清华镜像
options(repos=structure(c(CRAN="https://mirrors.tuna.tsinghua.edu.cn/CRAN/"))) 
```



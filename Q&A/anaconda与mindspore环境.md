
## 安装mindspore时python 版本过高（3.10+）

如果使用了anaconda, 它base环境默认的版本是小于3.9的。在命令行中打印`python version`时显示高版本，有两个原因：

1. 你打印的是系统的python版本，而不是anaconda的python版本

2. 你无意间在anaconda的base环境中将python更新到了更高版本


对于[1], 你可以在anaconda的base环境中打印python版本，看看是否是3.9以下的版本。具体的，打开anaconda prompt，确保命令行头部是 `(base)`. 输入`python --version`，查看python版本。

对于[2], 如果是高版本，可以尝试降级到3.9以下的版本。或者，新建一个conda环境专门用于Mindspore运行，指定python版本为3.9以下的版本。


## 为什么安装成功后，运行代码仍显示No module named 'mindspore'？

首先，你应该先 `重启内核`，然后再次运行代码。

如果还是不行，可能是因为你的jupyter notebook使用的环境不是mindspore安装的环境。

检查安装的包是否是在本机的anaconda base环境下。

    具体的，打开anaconda prompt，确保命令行头部是 `(base)`. 输入`conda list`，查看mindspore是否在base环境下。

如果是，在vscode中jupyter notebook右上角选择kernel，选择base环境，重启kernel后再次运行代码即可。

如果不在，需要在base环境下安装mindspore（或新建一个conda环境）

## anaconda solve environment failed with initial frozen solve

1. 尝试使用pip安装mindspore。Pip命令指定了国内源，可以避免网络问题。注意，需要关闭代理。
2. 尝试将conda镜像源更换为清华源, 参考[清华源](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/)；注意换源后下载不必开代理；换源后需要`conda clean -i`清除缓存




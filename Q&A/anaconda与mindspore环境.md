

## 为什么安装成功后，运行代码仍显示No module named 'mindspore'？

检查安装的包是否是在本机的anaconda base环境下。

    具体的，打开anaconda prompt，确保命令行头部是 `(base)`. 输入`conda list`，查看mindspore是否在base环境下。

如果是，在vscode中jupyter notebook右上角选择kernel，选择base环境，重启kernel后再次运行代码即可。

如果不在，需要在base环境下安装mindspore（或新建一个conda环境）

## anaconda solve environment failed with initial frozen solve

1. 尝试使用pip安装mindspore
2. 尝试将conda镜像源更换为清华源, 参考[清华源](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/)；注意换源后可以不用开tizi；换源后需要`conda clean -i`清除缓存




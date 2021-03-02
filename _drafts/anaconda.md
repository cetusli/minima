anaconda

Anaconda基础操作命令汇总    电子自修室

$conda env list

$conda update anaconda-navigator

卸载：$rm -rf anaconda；清理下.bashrc中的Anaconda路径

删除环境：$conda remove -n xxxx --all

anaconda安装TensorFlow版本:$conda install --channel https://conda.anaconda.org/anaconda tensorflow=1.8.0

清理（conda瘦身）:
conda clean就可以轻松搞定！第一步：通过conda clean -p来删除一些没用的包，这个命令会检查哪些包没有在包缓存中被硬依赖到其他地方，并删除它们。第二步：通过conda clean -t可以将conda保存下来的tar包。:$conda clean -p      //删除没有用的包;$conda clean -t      //tar打包

anaconda + tensorflow 安装 : https://zhuanlan.zhihu.com/p/110023452

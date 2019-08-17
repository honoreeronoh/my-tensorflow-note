安装
=====

'''
设置清华镜像站Pypi：
C:\Users\honore>pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple


通过Pypi安装tensorflow CPU版本：
C:\Users\honore>pip install --upgrade tensorflow
'''

tensorflowGPU版本安装（window）
------
打开官方网站https://tensorflow.google.cn/install/pip?lang=python2
首先选择GPU支持，查看必要的软件

下载各软件，注意版本

CUDA安装是需要重新开机的，使用以下命令来确认
  C:\Users\honore>nvcc -V
CUPTI就附带安装了（自定义安装，全选）

cuDNN的安装：
首先打开CUDA安装目录，解压cnDNN压缩包到该目录
（打开控制面板，系统与安全，系统或）我的电脑右键属性，高级系统设置，下方环境变量，确定有


再到系统变量PATH变量中确定有
  C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0\bin
添加
  C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0\include
  C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0\lib\x64

之后设置清华镜像站Pypi：
  C:\Users\honore>pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple


通过Pypi安装tensorflow GPU版本：
  C:\Users\honore>pip install --upgrade tensorflow-gpu

暂未发现使用VS2019有错误，理论上是可以的

出现的错误代码情况：

确定安装的numpy版本，可能会太新，利用
  pip uninstall numpy   # 卸载
  pip install "numpy < 1.17"  # 低版本安装

确定显卡驱动够新，不能用我的电脑属性里的硬件管理器来验证，
上官网，利用任务管理器查看显卡名字，直接在官网下载安装

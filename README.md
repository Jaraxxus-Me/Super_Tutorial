# Super_Tutorial
## Tutorial on environment setting in Ubuntu20.04 for ROS2 and DL developers in China
### 一
1. 镜像文件烧录，见百度网盘
2. 安好ubuntu先装驱动，直接软件与更新选择附加驱动，tested，apply，然后重启，nvidia-smi测试
3. 可选择先ros2，follow官网http://wiki.ros.org/
    其中的rosdep是最容易出问题的，参考
https://blog.csdn.net/weixin_39730025/article/details/113348458?utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-1.control&dist_request_id=1331645.10688.16183893261330005&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-1.control
    建议直接用最后一种解决rosdep update的问题
4. 安装anaconda：官网下载即可
    需要注意 ~/.bashrc里面，只有需要用conda的时候再去掉conda init的注释，否册与ros有冲突
5. 安装cuda11.2，cudnn11.2，run文件、tar包见百度网盘，安装参考：
https://blog.csdn.net/weixin_45225975/article/details/109179077
6. 安装pytorch，官网选择pip，11.1版本，命令行安装即可 (conda环境)
https://pytorch.org/get-started/locally/#linux-installation

### 二
1. 退出conda环境 conda deactivate (使用ros2时建议不激活conda环境，否则找不到pytorch)
2. 安装pytorch，官网选择pip，11.1版本，命令行安装即可 (非conda环境)
https://pytorch.org/get-started/locally/#linux-installation
pip3 install xxxxx
3. 在非conda环境下测试ros2以及torch的调用

### 三
1. 按照教程采用源码编译再次安装ros2 （建议可以一开始就装源码版本ros2）
https://www.ncnynl.com/archives/201801/2274.html
**注意：**每开一个终端都要改代理：
export https_proxy=http://180.124.207.129:118
export http_proxy=http://180.124.207.129:118
2. 国内镜像换源
将source.list改为网站中内容
http://ftp.xzcas.com:8000/apt.txt
3. ros1_bridge
https://www.ncnynl.com/archives/202007/3794.html

# AliyunAsPan

阿里云盘变本地硬盘-MAC版

# 准备工作

0、参考文章
https://mp.weixin.qq.com/s/PoxNiUqQhB7k6pg8ut7Chg

1、token值
bffdee6c752f4a8ab3453ed844982971

2、命令行
https://gitee.com/mirrors/webdav-aliyundriver

docker run -d --name=webdav-aliyundriver --restart=always -p 8080:8080  -v /etc/localtime:/etc/localtime -v /etc/aliyun-driver/:/etc/aliyun-driver/ -e TZ="Asia/Shanghai" -e ALIYUNDRIVE_REFRESH_TOKEN="bffdee6c752f4a8ab3453ed844982971" -e ALIYUNDRIVE_AUTH_PASSWORD="admin" -e JAVA_OPTS="-Xmx1g" zx5253/webdav-aliyundriver

# 操作步骤

1》安装brew下载工具
> * 打开终端，在终端中输入如下命令：
> * /usr/bin/ruby -e "$(curl -fsSL https://cdn.jsdelivr.net/gh/ineo6/homebrew-install/install)"
> * 然后回车，等待安装成功的提示。效果如下：
![Image text](https://user-images.githubusercontent.com/9125526/132012657-554293e6-de9d-4834-8d66-e715d4223b6d.jpg)
> * 需要将brew配置到系统环境环境中，操作如图所示：
> * ![Image text](https://user-images.githubusercontent.com/9125526/132014542-d2adae26-b80c-4cde-86e9-ed103dfa4531.png)
> * ![Image text](https://user-images.githubusercontent.com/9125526/132014605-2d1c1c03-aa61-4c19-901e-7417f04ce9fe.png)


2》利用brew安装docker
> * 打开终端，在终端中输入如下命令：
> * brew install --cask --appdir=/Applications docker
> * 你也可以通过网页下载安装包进行安装，地址为：https://docs.docker.com/desktop/mac/install/
> 

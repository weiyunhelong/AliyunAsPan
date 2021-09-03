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


2》利用brew安装docker
> * 打开终端，在终端中输入如下命令：
> * brew install --cask --appdir=/Applications docker
> * 你也可以通过网页下载安装包进行安装，地址为：https://docs.docker.com/desktop/mac/install/
> * 漫长的⌛️，搓搓小手，看个动漫再回来
> * 成功后的效果如下图所示：
> * ![Image text](https://user-images.githubusercontent.com/9125526/132014980-dd269057-d757-43aa-bd19-156be46b1ee8.jpg)

3》docker初始化，下载最新的版本
> * 打开终端，在终端中输入如下命令：
> * docker run -d -p 80:80 docker/getting-started
> * 然后回车，等待安装成功的提示。效果如下：
> * ![Image text](https://user-images.githubusercontent.com/9125526/132015235-f3703b9f-8bfd-4fee-9152-de17251a512a.jpg)

4》docker 运行上面的命令行
> * 打开终端，在终端中输入如下命令：【记得替换为自己的TOKEN值】
> * docker run -d --name=webdav-aliyundriver --restart=always -p 8080:8080  -v /etc/localtime:/etc/localtime -v /etc/aliyun-driver/:/etc/aliyun-driver/ -e TZ="Asia/Shanghai" -e ALIYUNDRIVE_REFRESH_TOKEN="【记得替换为自己的TOKEN值】" -e ALIYUNDRIVE_AUTH_PASSWORD="admin" -e JAVA_OPTS="-Xmx1g" zx5253/webdav-aliyundriver
> * 运行成功后的效果如下：
> * ![Image text](https://user-images.githubusercontent.com/9125526/132015721-102a700a-806a-4bf7-a9f7-a5298df203ca.jpg)

5》打开谷歌浏览器，在地址栏输入http://127.0.0.1:8080,然后回车,会出现登录浮窗，如下图所示
> * ![Image text](https://user-images.githubusercontent.com/9125526/132015720-6884fc7c-b886-4526-9170-1fce43126701.jpg)
> * 账号密码都为admin

6》登录成功后，会进入到阿里云盘中，展示你自己的云盘内容
> * 这是我自己的阿里云盘内容
> * ![Image text](https://user-images.githubusercontent.com/9125526/132016248-325cc58a-38b3-4ab6-a711-3f8dfb81c6a0.jpg)
> * 此时已看到万里长城，兄弟们再努把子力气，胜利的曙光就要到来啦。

7》接下来是系统端操作啦
> * 回到桌面，使用快捷键Command+K键，浮窗如下图所示
> * ![Image text](https://user-images.githubusercontent.com/9125526/132016645-f7bfb309-6b90-4da9-9158-99ae146d5126.jpg)
> * 输入网址为：http://127.0.0.1:8080,然后在点击连接按钮或者回车键，之后会出现确认连接提示浮窗，如下:
> * ![Image text](https://user-images.githubusercontent.com/9125526/132016765-ebc6f0ee-6b6e-4678-ae82-4a4dc50af56c.jpg)
> * 点击连接按钮，再次输入账户密码都为admin

8》链接成功之后，找到位置，下面出现127.0.0.1，点击即出现阿里云盘。
> * ![Image text](https://user-images.githubusercontent.com/9125526/132016935-3d729b59-41e5-463c-9b1f-3297e5a5ac4a.jpg)

9》大功告成！！！回家吃饭饭～～～


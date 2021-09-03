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
![Image text](https://user-images.githubusercontent.com/9125526/132012657-554293e6-de9d-4834-8d66-e715d4223b6d.jpg)

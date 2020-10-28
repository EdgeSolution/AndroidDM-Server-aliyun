#Introduction In Englishi(英文说明)
## AndroidDM-VM-Cloud
AndroidDM Server for cloud VM, such as aliyun VM, azure VM

## git clone https://github.com/EdgeSolution/AndroidDM-VM-Cloud.git

## run application
  - The virtual machine needs to expose ports: 8080, 30001, 30002, 1883, 5432, 5500, 5901, 9191, 9000
  - Run start.sh

## Run the Debian slim docker image for AndroidDM

#中文说明（Introduction In Chinese）

部署到云端虚拟机步骤
##1．	首先需要在平台上上申请一个基于Ubuntu 18.04 x64系统的虚拟机
我们已经有验证过阿里云和微软Azure云
##2．	开放如下的端口：
8080, 30001, 30002, 1883, 5432, 5500, 5901, 9191, 9000
##3．	远程登录该VM，安装一些必须的工具：git, docker, docker-compose
$ sudo apt update && apt install git 
$ curl  -sSL  https://get.daocloud.io/docker | sh                 
$ sudo apt  install  docker-compose                               
安装完成后，使用下面的命令检查版本，确认安装正确。
a)	$ docker version                     
b)	$ docker-compose  version  


##4．	使用git命令下载AndroidDM的安装文件
$ git clone https://github.com/EdgeSolution/AndroidDM-VM-Cloud.git


##5．	安装和启动AndroidDM
当你通过git下载到安装文件后，ECS会生成“AndroidDM-VM-Cloud” 目录，进入该目前，执行 start.sh 脚本。
$ cd AndroidDM-VM-Cloud /              
$ chmod +x  start.sh                 
$./start.sh                                          
start.sh会完成AndroidDM服务器的安装和启动，因为安装过程是在线安装，需要从网络上下载AndrodDM docker镜像，根据网络速度不同，大约需要10~20分钟的时间完成安装，请耐心等待。
当安装完成后，就会自动启动，你就可以通过浏览器访问AndroidDM的服务了
http://ServerIP:8080
SeverIP就是VM对外的公网IP地址。

理论上，上述方法同样适用在各种云平台上安装AndroidDM，目前我们已经验证适用Azure和阿里云VM。



#Change Log
# v1.0.0 version
 - New features
 - docker images version
  - localhost/harbor/androiddm-javaenv-admin:v1.0.0
  - localhost/harbor/androiddm-astore-slim-admin:v1.0.0
  - localhost/harbor/androiddm-mosquitto-admin:v1.0
  - localhost/harbor/androiddm-novnc-admin:v1.0
  - postgres:9.4
  - portainer/portainer

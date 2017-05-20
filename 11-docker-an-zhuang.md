

#ubunt下安装docker

###1.安装默认版本
#####sudo apt-get update
#####sudo apt-get install docker.io
####安装完成之后查看版本:
#####docker --version
#####![](/assets/1.png)

###2.安装最新版本
#####sudo apt-get update
#####//让apt支持https：
#####sudo apt-get install apt-transport-https
#####//将docker库的公钥加入本地apt中：
#####sudo apt-key adv --keyserver hkp://keysrver.ubuntu.com:80 --recv-keys 36A1D7869245C8950F966E92D8576A8BA88D21E9
#####//将安装源添加到apt源中，更新、安装
##容器
###1.创建容器 (docker create , docker run)
####1.1: docker create 与 docker run 区别
#####&emsp; 用docker create 创建的容器处于停止状态，docker run 创建容器并启动。
####1.2：docker create实例
#####&emsp; sudo docker create ubuntu:14.04
![](/assets/4.png)![](/assets/6.png)
#####&emsp; 创建完容器之后，会返回容器的ID，例如图中的589....,每一个容器ID都是唯一的。
#####&emsp; docker ps 查看当前正在运行的容器
![](/assets/5.png)
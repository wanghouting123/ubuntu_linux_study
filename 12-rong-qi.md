##容器
###1.创建容器 (docker create , docker run)
####1.1: docker create 与 docker run 区别
#####&emsp; 用docker create 创建的容器处于停止状态，docker run 创建容器并启动。
####1.2：docker create实例
#####&emsp; sudo docker create ubuntu:14.04 </code>

![](/assets/4.png)
#####&emsp; 创建完容器之后，会返回容器的ID，例如图中的589....,每一个容器ID都是唯一的。
#####&emsp; docker ps 查看当前正在运行的容器(此时，没用任何运行的容器)
![](/assets/5.png)
#####&emsp; docker ps -a 查看所有的容器，包括未运行的容器
![](/assets/6.png)
#####&emsp; 使用docker start 启动容器

####1.3：docker run实例
#####&emsp; 想要让创建的容器立马进入运行状态，可以使用docker run命令，该命令等同于docker create创建容器之后再使用docker start启动容器。使用docker run命令，可以创建两种类型的容器：后台型容器和交互型容器。
######&emsp; * 交互型容器：运行在前台，通常会指定有交互的控制台，可以给容器输入，也可以得到容器的输出。创建该容器的终端被关闭，在容器内部使用exit命令或者调用了docker stop、docker kill命令后，容器会变成停止状态。
######&emsp; * 后台型容器：运行在后台，创建启动之后就与终端无关。即便终端关闭了，该后台容器也依然存在，只有调用了docker stop或docker kill命令时才能够使容器变成停止状态。
#####&emsp; 创建一个交互型容器：


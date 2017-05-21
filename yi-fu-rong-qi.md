#依附容器

#####&emsp; 依附操作attach通常用在由docker start或者docker restart启动的交互型容器中。由于docker start启动的交互型容器并没有具体终端可以依附，而容器本身是可以接收用户交互的，这时就需要通过attach命令将终端依附到容器中。

#####&emsp; docker run -i -t ubuntu:14.04 /bin/bash
![](/assets/15.png)

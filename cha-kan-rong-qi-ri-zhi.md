#查看容器日志

#####&emsp; 对于交互型容器，由于本身就存在交互终端或者可以通过attach依附终端，所以查看容器的配置信息或者调试程序比较方便。但对于后台型容器，它不存在交互终端，要获取其信息，势必需要其他的方法。docker给我们提供了logs、inspect等方法。docker logs命令用于查看容器的日志，它将输出到标准输出的数据作为日志输出到运行docker logs命令的终端上。

#####&emsp; 首先，创建一个不断输出一些内容的后台型容器：
#####&emsp; sudo docker run -d --name deamon_logs ubuntu /bin/bash -c 'for((i=0;1;i++));do echo $i;sleep 1;done;' 



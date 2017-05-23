<h1>查看容器日志</h1>

</p>&emsp; 对于交互型容器，由于本身就存在交互终端或者可以通过attach依附终端，所以查看容器的配置信息或者调试程序比较方便。但对于后台型容器，它不存在交互终端，要获取其信息，势必需要其他的方法。docker给我们提供了logs、inspect等方法。docker logs命令用于查看容器的日志，它将输出到标准输出的数据作为日志输出到运行docker logs命令的终端上。</p>

#####&emsp; 首先，创建一个不断输出一些内容的后台型容器：
#####&emsp; sudo docker run -d --name deamon_logs ubuntu /bin/bash -c 'for((i=0;1;i++));do echo $i;sleep 1;done;' 
![](/assets/16.png)
#####&emsp;  我们可以使用logs来查看其输出：
#####&emsp;  sudo docker logs -f deamon_logs
#####&emsp;  默认情况下，logs输出的是从容器启动到调用执行logs命令时的所有输出，之后的日志不再输出，并立即返回主机的控制台。如果要实时差看日志，可以使用-f标志。ctrl+c快捷键退出监视日志。
#####&emsp; 使用--tail标记可以精确控制logs输出的日志行数。例如，查看最后5行日志：
#####&emsp; sudo docker logs -f --tail=5 daemon_logs

 





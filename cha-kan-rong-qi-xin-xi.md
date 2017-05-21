#查看容器信息

#####&emsp; docker inspect用于查看容器的配置信息，包含容器名、环境变量、运行命令、主机配置、网络配置和数据卷配置等：
![](/assets/18.png)

#####&emsp; 使用-f或者--format格式化标志，可以查看指定部分的信息。
#####&emsp; sudo docker inspect --format='{{ .State.Runing }}' deamon_logs

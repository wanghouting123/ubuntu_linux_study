</h1>删除容器</h1>

####&emsp; 当一个容器停止时，容器并没有消失，只是进入了停止状态，必要的话还可以重新运行。如果不再需要这个容器时，可以使用docker rm 命令删除它：

 ####&emsp; sudo docker rm deamon_while2 
 ####&emsp; 要注意一点，不可以删除一个运行中的容器，此时必须先用docker stop或docker kill 命令停止它才能删除。
 ![](/assets/13.png)
 ####&emsp; 当然，也可以使用-f选项强制删除它：
 ![](/assets/14.png)
 
 ####&emsp; Docker并没有提供一次性删除所有容器命令，但是可以用下面的命令来实现这个目的：
 ####&emsp; docker rm \`docker ps -a -q`
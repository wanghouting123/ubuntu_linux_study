#终止容器
#####&emsp; 退出容器的方式有很多种。当容器发生严重错误时，容器会因为异常而退出并带有错误码，这时可以通过错误码来判断容器内部发生的错误。而在正常情况下，交互型容器可以在shell中输入exit，或者是使用ctrl+d组合键来使其退出。另外，交互型容器和后台型容器都可以采用docker stop命令来停止：

#####&emsp; sudo docker stop daemon_while

#####&emsp; 还可以通过容器ID来停止容器：
#####&emsp; sudo docker stop 


<h1>终止容器</h1>
<p>&emsp; 退出容器的方式有很多种。当容器发生严重错误时，容器会因为异常而退出并带有错误码，这时可以通过错误码来判断容器内部发生的错误。而在正常情况下，交互型容器可以在shell中输入exit，或者是使用ctrl+d组合键来使其退出。另外，交互型容器和后台型容器都可以采用docker stop命令来停止：</p>



<p>&emsp; sudo docker stop daemon_while</p>



<p>&emsp; 还可以通过容器ID来停止容器：</p>



<p>&emsp; sudo docker stop 1234969414b8</p>

<p>&emsp; docker stop命令给容器中的进程发送SIGTERM信号，默认行为是会导致容器退出。当然，容器内程序可以捕捉该信号并自行处理，例如可以选择忽略。如果要强行停止一个容器，则需要使用docker kill命令，它会给容器的进程发送SIGKILL信号，该信号将会使容器必然退出。</p>



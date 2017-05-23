<h1>启动容器</h1>
#####&emsp; 通过docker run命令创建的容器会直接进入到运行状态，而通过docker create 命令创建的容器会进入到停止状态，想要运行该容器，则可以通过docker start命令来启动它。当容器运行完自己的任务后，容器会退出，进入到停止状态，如果需要再次启动该容器，可以再使用docker start命令来启动。

#####&emsp; 例如： sudo docker start inspect_shell
#####&emsp; 也可以使用该容器的ID来启动 ：
#####&emsp; sudo docker start 45aaedbdbf1b

#####&emsp; 容器在运行过程中，总是不可避免的出现各种问题，严重的会导致容器因为异常而退出。而有时我们需要根据错误码来判断容器是否需要重启。默认情况下，容器时不重启的，为了让容器在退出后能够自动重启，需要用到--restart参数。--restart标志会检查容器的退出码，并根据此来决定是否需要重启容器。

#####&emsp; sudo docker run --restart=always --name docker_restart -d ubuntu /bin/bash -c "while true;do echo hello world ;sleep 1;done;

#####&emsp;  在这个例子中，--restart标志被设置为always。不管容器的返回码是什么，docker都会尝试重启容器。另外，我们也可以将其设置为on-failure,这样的话，当容器的返回值是非0时，docker才会重启容器。on-failure标志还接受一个可选的重启次数：
#####&emsp; --restart=on-failure:5
#####&emsp; 表示收到一个非0的返回码，最多尝试重启容器5次。

#容器的导入和导出

#####&emsp; Docker的流行与它对容器的易分享和易移植密不可分。用户不仅可以把容器提交到公共服务器上，还可以将容器导出到本地文件系统中。同样，我们也可以将导出的容器重新导入到docker运行环境中。docker的导入和导出分别由import命令和export命令完成。

####&emsp; 容器的导出 
#####&emsp; 创建一个容器：
#####&emsp; sudo docker run -d --name ubuntu ubuntu /bin/bash 
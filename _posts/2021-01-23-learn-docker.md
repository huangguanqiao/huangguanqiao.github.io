---
layout:     post
title:      Docker Introduction
subtitle:   BY Guanqiao Huang
date:       2021-01-23
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - Docker
---

- `docker ps` 查看正在运行的容器
- `docker ps -a` 查看所有容器
- `docker run -i -t ubuntu` 建立一个Ubuntu，-i代表与这个容器互动（比如像ssh进去，可以向他输入指令），-t代表类型让他创建个terminal给我们, 一起写就是-it
- `docker start [id]` 输入容器id，不会进入容器里面，只是以detached模式运行起来
- `docker attach [id]` 进去容器里面
- `docker stop [id]` 停止容器，Stop a running container through SIGTERM
- `docker kill [name]` 停止容器, Stop a running container through SIGKILL
- `docker rm [id]` 移除容器
- `docker image ls` 可以查看下载到本地的image
- `docker image` 查看image
- `docker rmi [imageid]` 可以移除本地镜像
- `docker image rm [myimage:1.0]` Delete an image from the local image store
- `docker run --name web-server -d -p 8000:80 nginx` 运行nginx服务器, 容器名字叫web-server，-d意思是以detached模式运行。-p设置端口port，8000是本机8000端口映射到容器的80 port
- `localhost:8000` 在本机浏览器输入localhost，查看server是否正常运行（比如nginx例子）
- `docker run --name [web-name] -d -p 8000:80 -v $(pwd):/usr/share/nginx/html nginx` 这里-v是将电脑的文件映射到容器，pwd当前目录，冒号后面是容器的路径。新建并运行在nginx
- 退出ubuntu container，可以输入exit，container也会被关闭
- 想保持运行但退出container，可以使用ctrl+p或者ctrl+q
- docker hub是docker的镜像仓库
- ubuntu里查看运行情况，命令top。退出top可以按q或者ctrl+c
- ubuntu里安装nodejs， `apt update && apt install nodejs -y`
- ubuntu里查看node版本，`node -v`
- `docker exec -it [webapp's name] /bin/bash` 用bash连接docker container
- `docker logs --tail 100 [webapp_1] ` 显示100条container 记录
- `docker container rm -f $(docker ps -aq)` Delete all running and stopped containers
- `ENTRYPOINT` 不可以被overwrite，但CMD可以，两者都是run的时候运行命令
- 登到container, ps aux
- `docker build -t myimage:1.0 .` 根据当前目录（.）的dockerfile来build image
- `docker run --rm jr/console-helloworld` 帮助清空当前的container，避免conflict，简单来说时用完即删
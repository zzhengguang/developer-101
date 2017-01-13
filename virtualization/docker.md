#  Docker 新手入门

### 介绍

[Docker](https://www.docker.com/)

### 安装

**Mac**

	brew cask install docker
	
**Linux**

	sudo apt-key adv \
           --keyserver hkp://ha.pool.sks-keyservers.net:80 \
           --recv-keys 58118E89F3A912897C070ADBF76221572C52609D

	echo "deb https://apt.dockerproject.org/repo ubuntu-xenial main" \
	    | sudo tee /etc/apt/sources.list.d/docker.list
	
	sudo apt-get update
	
	sudo apt-get install apt-transport-https ca-certificates \
		linux-image-extra-$(uname -r) linux-image-extra-virtual \
    	docker-engine

	sudo usermod -aG docker $USER
	sudo reboot
	
	

#### Docker 镜像相关

解决下载`docker pull` 镜像速度慢的问题。

**Mac**

`Preferences` -> `Advanced` -> `Registry mirrors`

`https://ep1dz7wh.mirror.aliyuncs.com`


**Ubuntu**

	sudo tee /etc/docker/daemon.json << EOD
	{
			"registry-mirrors": ["https://ep1dz7wh.mirror.aliyuncs.com"]
	}
	EOD

* [Docker Hub](https://hub.docker.com/)
* [Docker加速器 - USTC LUG](https://lug.ustc.edu.cn/wiki/mirrors/help/docker)
* [Docker加速器 - aliyun](dev.aliyun.com)(需要注册) [现在注册](https://cr.console.aliyun.com/)
* [Docker私有镜像库 - aliyun](https://help.aliyun.com/knowledge_detail/40557.html)


### 常用命令

* `docker info`: 检查 Docker 安装

#### 镜像(Images)

* 获取: `docker pull`
* 列出本地: `docker images`
* 删除: `docker rmi`
* 保存: `docker save`
* 加载: `docker load`
* 上传: `docker push`
* 标签: `docker tag`
* 通过Dockerfile生成镜像: `docker build`
* 查看镜像历史: `docker history`

#### 容器(Containers)

**选项**

* `-t` : 分配一个伪终端
* `-i` : 让容器的标准输入保持打开
* `-d` : 在后台运行
* `--name`:  定义容器名字
* `--link`: 容器互联
* `-P` : 随机映射 49000~49900 的端口到内部容器开放的网络端口
* `-p` : 映射指定端口
* `-v` : 数据卷
* `-m`: 指定内存

**命令**

* 新建并启动: `docker run`
* 启动: `docker start`
* 终止: `docker stop`
* ---: `docker restart`
* 通过容器创建镜像: `docker commit`
* 列出: `docker ps`
* 获取容器的日志信息: `docker logs`
* 进入: `docker attach`
* 导出: `docker export`
* 导入: `docker import`
* 删除: `docker rm`
* 查看端口: `docker port`
* 查看容器修改: `docker diff`
* `docker kill`
* `docker events`
* `docker wait`


#### Dockerfile

* `#` 注释
* `FROM` : 指定镜像
* `MAINTAINER`: 作者
* `RUN` 运行命令
* `ADD`: 复制本地文件到镜像
* `EXPOSE`: 向外部开放端口
* `CMD`: 容器启动后于行的程序
* `ENTRYPOINT`: 配置给容器一个可执行的命令
* `WORKDIR`: 指定 `cmd`、`run`、 `entrypoint` 工作目录
* `ENV`: 设置环境变量
* `USER`: 镜像正在运行时设置一个UID
* `VOLUME`: 授权访问从容器内到主机上的目录



### 替换安装源

	# debian
	RUN sed -i 's/httpredir.debian.org/mirrors.aliyun.com/g' /etc/apt/sources.list
	
	# ubuntu
	RUN sed -i 's/archive.ubuntu.com/mirrors.aliyun.com/g' /etc/apt/sources.list
	
	RUN apt-get update && apt-get install -y --no-install-recommends \
	
				&& rm -rf /var/lib/apt/lists/*
	
	



#### 推荐资料

* [Docker — 从入门到实践](https://www.gitbook.com/book/yeasy/docker_practice/details)
* [Docker Compose and Rails](https://docs.docker.com/compose/rails/)

#### 安装

**Mac**

	brew cask install docker
	
**Linux**


### 替换安装源

	# debian
	RUN sed -i 's/httpredir.debian.org/mirrors.aliyun.com/g' /etc/apt/sources.list
	
	# ubuntu
	RUN sed -i 's/archive.ubuntu.com/mirrors.aliyun.com/g' /etc/apt/sources.list


#### 推荐资料

* [Docker — 从入门到实践](https://www.gitbook.com/book/yeasy/docker_practice/details)
* [Docker Compose and Rails](https://docs.docker.com/compose/rails/)


#### Docker 镜像相关
解决下载`docker pull` 镜像速度慢的问题。

`https://ep1dz7wh.mirror.aliyuncs.com`

* [Docker Hub](https://hub.docker.com/)
* [Docker加速器 - USTC LUG](https://lug.ustc.edu.cn/wiki/mirrors/help/docker)
* [Docker加速器 - aliyun](dev.aliyun.com)(需要注册) [现在注册](https://cr.console.aliyun.com/)
* [Docker私有镜像库 - aliyun](https://help.aliyun.com/knowledge_detail/40557.html)


### 常用命令

#### 镜像

* 获取: `docker pull`
* 列出本地: `docker images`
* 删除: `docker rmi`
* 保存: `docker save`
* 加载: `docker load`
* 上传: `docker push`
* 标签: `docker tag`
* 通过容器创建镜像: `docker commit`
* 通过Dockerfile生成镜像: `docker build`

#### 容器

**选项**

* `-t` : 分配一个伪终端
* `-i` : 让容器的标准输入保持打开
* `-d` : 在后台运行
* `--name`:  定义容器名字
* `--link`: 容器互联
* `-P` : 随机映射 49000~49900 的端口到内部容器开放的网络端口
* `-p` : 映射指定端口
* `-v` : 数据卷

**命令**

* 新建并启动: `docker run`
* 启动: `docker start`
* 终止: `docker stop`
* 列出: `docker ps`
* 获取容器的日志信息: `docker logs`
* 进入: `docker attach`
* 导出: `docker export`
* 导入: `docker import`
* 删除: `docker rm`
* 查看端口: `docker port`

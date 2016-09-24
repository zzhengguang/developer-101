# vagrant
#### vagrant 相关文章
* [使用Vagrant打造跨平台开发环境](https://segmentfault.com/a/1190000000264347)
* [开启 NFS 文件系统提升 Vagrant 共享目录的性能](https://segmentfault.com/a/1190000000270453)

#### 安装Vagrant
	sudo apt-get install vagrant

#### 检查是否安装成功
	vagrant -v 
#### 列出vagrant的box文件
> [vagrant box文件下载地址](www.baidu.com)

	vagrant box list
#### 加载vagrant的box
	vagrant box add box_name
#### 移除加载的box
	vagrant box remove box_name
#### 初始化虚拟机，并产生Vagrantfile文件
	vagrant init
#### 启动虚拟机
	vagrant up
#### 进入虚拟机
	vagrant ssh
#### 关闭虚拟机
	vagrant halt
#### 重启虚拟机
	vagrant reload
#### 查看虚拟机的运行状态
	vagrant status
#### 销毁虚拟机
	vagrant destroy
#### 打包虚拟机
	vagrant package

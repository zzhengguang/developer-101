# MySQL 新手入门

#### 介绍

* [MySQL 官方网站](http://www.mysql.com/)
* 默认端口: 3306


#### 安装

**Ubuntu**
	
	sudo apt-get install mysql-server mysql-client libmysqlclient-dev
	
	# 解决 Ubuntu 16.04 上不能直接用 root 用户登录
	sudo mysql -u root -e "update mysql.user set plugin='mysql_native_password' WHERE User='root';
	
**Mac**

	brew install mysql
	
	
#### 登录

	mysql -u root
	
	
#### 控制台命令

* <code>show databases;</code>: 列出所有数据库
* <code>use [database_name]</code>: 连接其他数据库
* <code>show tables;</code>: 列出当前数据库的所有表
* <code>describe tables;</code>: 列出某一张表格的结构
* <code>exit</code>: 退出控制台

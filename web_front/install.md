# 基础安装


## Node.js


**Mac**

	brew install nodejs
	
**Linux**

* [Installing Node.js via package manager](https://nodejs.org/en/download/package-manager/)
* [Nodesource 镜像使用帮助](https://mirrors.tuna.tsinghua.edu.cn/help/nodesource/)

	curl -sL https://deb.nodesource.com/setup_9.x | sudo -E bash -
	sudo apt-get install -y nodejs


## Yarn
[Yarn install](https://yarnpkg.com/lang/en/docs/install/)

**Mac**

	brew install yarn
	
**Linux**

	curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
	echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
	
	sudo apt-get update && sudo apt-get install yarn


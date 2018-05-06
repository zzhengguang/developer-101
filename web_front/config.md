## npm & yarn 配置


[在中国，安装 & 升级 npm 依赖的正确方法](https://sebastianblade.com/the-truly-way-to-install-upgrade-npm-dependency-in-china/)

	# yarn
	yarn config set registry 'https://registry.npm.taobao.org'
	
	# npm
	npm config set registry https://registry.npm.taobao.org
	
	
**node-sass**

	yarn config set sass_binary_site "http://cdn.npm.taobao.org/dist/node-sass"

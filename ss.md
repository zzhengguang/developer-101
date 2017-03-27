## 翻墙入门


### 快速入门

SwitchyOmega: 您可以在[谷歌应用商店][SwitchyOmega_Chrome]安装，或者在[发布页面][SwitchyOmega_Release]下载一份离线   
GFWList: `https://raw.githubusercontent.com/gfwlist/gfwlist/master/gfwlist.txt`



### 服务器配置


安装 shadowsocks

	sed -i 's/deb.debian.org/mirrors.aliyun.com/g' /etc/apt/sources.list
	curl --show-error --retry 5 https://bootstrap.pypa.io/get-pip.py | python
	pip install shadowsocks
	
启动服务器

	ssserver --fast-open  -k <password> -d start
	
启动客户端

	sslocal -s <ip> -k <password> --fast-open -b 0.0.0.0 -d start
	
	
### 参考资料

* [wiki](https://github.com/shadowsocks/shadowsocks/wiki)
* [SwitchyOmega][SwitchyOmega_Home]
* [GFWList][gfwlist]
* [shadowsocks][shadowsocks]


[SwitchyOmega_Home]: https://github.com/FelisCatus/SwitchyOmega
[SwitchyOmega_Chrome]: https://chrome.google.com/webstore/detail/padekgcemlokbadohgkifijomclgjgif
[SwitchyOmega_Release]: https://github.com/FelisCatus/SwitchyOmega/releases
[gfwlist]: https://github.com/gfwlist/gfwlist
[shadowsocks]: https://shadowsocks.org/en/index.html



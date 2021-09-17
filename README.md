# ServerStatusForOnlyIPV6
## 文章缘由
     关于你的VPS主机上面只有纯IPV6确无法连接服务端的问题
     首先呢 我在这边讲述一下为什么会有这个教程
     是因为我最近在 EUServ.com 获取了FREE的主机
     在经过很长的时间内的寻找
     我先是看见了使用tunnelbroker进行搭建服务端支持IPV6
     但是我未知原因无法连接
     在后面的话我就看见了 WARP
     所以就有了今天这个教程
     如果有侵权或者文章有错误所在 麻烦各位指出
     这是我第一次写GitHub
## 设置NAT64实现访问IPV4网络
### 原帖 (https://haoduck.com/681.html）
>输入一键脚本：mv /etc/resolv.conf /etc/resolv.conf.bak && echo -e "nameserver 2001:67c:2b0::4\nnameserver 2001:67c:2b0::6" > /etc/resolv.conf
>>在你的服务器控制台输入     curl https://www.baidu.com
>>>正常就能显示百度页面的内容了
## 设置WARP
### [WARP](https://github.com/fscarmen/warp）
>运行脚本 wget -N https://raw.githubusercontent.com/fscarmen/warp/main/menu.sh && chmod +x menu.sh && ./menu.sh
### 会出现以下内容
---
本项目专为 VPS 添加 wgcf 网络接口，详细说明：https://github.com/fscarmen/warp
***
脚本特点:
***
	* 根据不同系统综合情况显示不同的菜单，避免出错
	* 结合 Linux 版本和虚拟化方式，自动优选三个 WireGuard 方案。网络性能方面：内核集成 WireGuard＞安装内核模块＞wireguard-go
	* 智能判断 WGCF 作者 github库的最新版本 （Latest release
	* 智能判断vps操作系统：Ubuntu 18.04、Ubuntu 20.04、Debian 10、Debian 11、CentOS 7、CentOS 8，请务必选择 LTS 系统
	* 智能判断硬件结构类型：Architecture 为 AMD 或者 ARM
	* 智能分析内网和公网IP生成 WGCF 配置文件
	* 输出结果，提示是否使用 WARP IP ，并自动清理安装时的临时文件

====================================================================================

    系统信息：
	当前操作系统： Debian GNU/Linux 10 (buster)
	内核：5.4.123-1.el7.elrepo.x86_64
	处理器架构：amd64
	虚拟化：lxc 
	IPv4： 
	IPv6：xxxxx
	WARP 已开启

=====================================================================================
***
***这时候只需要输入指令 1 为仅IPv6服务器添加IPv4***
**安装ServerStatus配置好对接服务器即可**

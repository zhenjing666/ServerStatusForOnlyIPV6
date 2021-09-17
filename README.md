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

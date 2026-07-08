# QuickTunnel
众所周知现在ssh是最广泛使用的远程连接协议

但这个东西有个最大的缺点 基于TCP 导致他只要遇到丢包就卡死

所以我突发奇想啊 用魔改的Hysteria2来做类似的远程连接隧道可不可以呢

于是我发现你只要在服务端写一个
```toml
[quicktunnel]
listen="0.0.0.0"
port=59
```
就这么简单就可以跑起来了

客户端连接只需要用
```bash
qt 用户名@目标主机IP 密码或 -p 密钥路径
```

什么你说Hysteria2默认用Brutal怎么办

quicktunnel把Brutal给蒯了变成了BBR 也就是一个开了ignoreclientbandwidth并且客户端不设置上下的Hysteria2节点

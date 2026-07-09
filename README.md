# QCSH 全称QUIC Shell
## 🖊 项目简介
众所周知现在ssh是最广泛使用的远程连接协议

但这个东西有个最大的缺点 基于TCP 导致他只要遇到丢包就卡死

所以我突发奇想啊 用魔改的Hysteria2来做类似的远程连接隧道可不可以呢
## ？ 如何使用
于是我发现你只要在服务端写一个
```toml
[qcsh]
listen="0.0.0.0"
port=59
```
就这么简单就可以跑起来了

客户端连接只需要用
```bash
qt 用户名@目标主机IP 密码
```
## ⛰ 实现方法
什么你说Hysteria2默认用Brutal怎么办

QCSH默认是一个用BBR流控的Hysteria2协议 Brutal需要额外指定上下行 但不排除在未来的版本中加回来的可能
## ⚖️ 条款和授权
QCSH使用MoPL授权 <https://867678.xyz/doc/MoPL>

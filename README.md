# QCSH (QUICShell)
## 🖊 Intro
SSH is the most widely used remote connection protocol today.

But he was founded 30 years ago.

From today's perspective, he should have been eliminated long ago.

So QCSH is a protocol that can eliminate SSH and is based on [Hysteria2](https://github.com/apernet/hysteria).
## 🚀 Features
- **So Fast**: No three-way handshake, no four-way wave.
- **Easy to use**: You only need to download its binary file and supplement it with a configuration file to start.
- **Open Source**: Under the MoPL, it is free software.
- **Every Free**: No charge, always free.
- **Support Most platforms**: Linux, macOS, Windows, Plan9, ... Every Golang supports platforms theoretically all support QCSH.
## ？ How to use
Just need some `toml` config file

Default port `59`
```toml
[qcsh]
listen="0.0.0.0"
port=59
```
Yes, it is. Very simple!

And if you need connect server?
```bash
qcsh username@IP "password"
```
Options
```bash
qcsh username@IP "password" -k "/path/to/private.key" -c "/path/to/configfile.toml" 
```
## ⚖️ LICENSE
QCSH under the [MoPL](https://867678.xyz/doc/MoPL)

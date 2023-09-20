## 触发器集合
用于解决 Debian 上常用包没有统一的处理脚本托管平台，导致的需要各显神通的问题。原理是使用自定义触发器
并结合aur上针对性的处理，将一些 archlinux 上很常见很好用的操作和 patch 带到 Debian 上减少 archlinux 用户
因为各种原因切换到 DEB 系的不适感

### 如何使用
克隆仓库：

```bash
git clone https://github.com/weearc/debian-custom-trigger.git
```

切换到目录：

```bash
cd debian-custom-trigger
```

手动构建包：

```bash
dpkg-deb -b <包名>.deb <包名目录>
```

使用 `dpkg` 安装触发器:

```bash
sudo dpkg -i <pkgname>.deb
```

触发触发器的方法为重新安装对应包，即可触发对应触发器，获得 patch 效果

### 包含的包
|pkgname|trigger-name|desc|
|:-:|:-:|:-:|
|google-chrome-stable|google-chrome-stable-trigger|-|
|linuxqq|linuxqq-trigger|-|

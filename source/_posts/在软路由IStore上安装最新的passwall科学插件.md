---
title: 在软路由IStore上安装最新的passwall科学插件
date: 2024-01-14 00:35:54
tags: 软路由
---

1、passwall开源项目地址：【[点击进入](https://github.com/xiaorouji/openwrt-passwall/releases)】

- 需要下载的资料如下（

  OpenWrt SDK Version: 23.05-rc3

  ）：

  - luci-app-passwall_4.71-2_all.ipk
  - luci-i18n-passwall-zh-cn_git-23.289.45328-a953315_all.ipk
  - passwall_packages_ipk_aarch64_generic.zip（这个需要根据自己的软路由CPU架构下载）
  - 老版本需要下载此资料包：【[点击下载](https://www.mediafire.com/file/r054ykbeiwcmj5f/luci-lua-runtime_all_fake.zip/file)】

- 下载SSH连接工具Finalshell：【[点击进入](https://www.hostbuf.com/t/988.html)】

- 查看CPU架构

```
cat /etc/os-release |grep ARCHCopy
```

2、上传下载好的资料包

- 系统——文件传输——选择文件——点击上传（把三个文件都上传）

3、安装

```lisp
# 进入安装包所在目录 
cd /tmp/upload 
# 查看目录下所有文件 
ls 
# 解压安装包 
unzip passwall_packages_ipk_aarch64_generic.zip 
# 安装所有软件包 
opkg install *.ipk --force-reinstall
```

4、组件更新

打开服务=》passwall=>组件更新=>手动更新所有组件

![image-20240114004029979](https://image.wanc.eu.org/file/496bdfd9992c8cf08d4f1.png)

## 安装完成！享受自由上网吧！


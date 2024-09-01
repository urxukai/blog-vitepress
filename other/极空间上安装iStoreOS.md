---
title: 极空间上安装iStoreOS
---

# {{ $frontmatter.title }}

## 1. 模式切换

设置 :arrow_right: 网络相关设置 :arrow_right: 模式切换 :arrow_right: 选择「网桥模式」 :arrow_right: 确定

![模式切换](/images/极空间/模式切换.png)

## 2. 网桥设置

虚拟机 :arrow_right: 网桥设置 :arrow_right: 选择「双网口加入同一网桥」

![网桥设置](/images/极空间/网桥设置.png)

## 3. 下载 iStoreOS 镜像

官网：https://www.istoreos.com/

下载地址：https://fw.koolcenter.com/iStoreOS/x86_64_efi/

下载后需要解压 :arrow_right: 解压好的文件上传到极空间

![iStoreOS](/images/极空间/istoreDownload.png)

## 安装 iStoreOS

① 打开极空间上的「虚拟机」App

② 点击「新建虚拟机」
![iStoreOS](/images/极空间/istore1.png)

③ 设置虚拟机参数信息
![iStoreOS](/images/极空间/istore2.png)

④ 设置硬盘信息
![iStoreOS](/images/极空间/istore3.png)

⑤ 设置网络
![iStoreOS](/images/极空间/istore4.png)

## iStoreOS 常用命令

```sh
# 查看ip地址
ip addr

# 修改地址、查看地址
quickstart
```

## 上网设备配置走旁路由

- 修改 ipv4 为手动，ip 地址填入和旁路由同一网段的 ip，子网掩码填 255.255.255.0
- 修改路由器为旁路由 IP
- 添加 DNS 为旁路由 IP

> 安装 iStoreOS 参考地址：https://zhuanlan.zhihu.com/p/703547359

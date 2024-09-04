---
title: 随时随地远程启动家里设备，极空间部署一键网络唤醒工具『UpSnap』
---

# {{ $frontmatter.title }}

## 关于UpSnap

![iStoreOS](/images/极空间/upSnap/1.png)

🔺UpSnap是一个使用 SvelteKit、Go 和 PocketBase 编写的简单局域网唤醒 Web 应用程序。

它的功能特性如下：

- 🚀 一键启动设备控制面板
- ⏰ 通过定时任务自动安排事件
- 🔌 检查您指定的任何网络端口是否可用
- 🔍 使用网络扫描工具找到连接的设备（需要安装 nmap）
- 👤 安全的用户管理系统
- 🌐 支持多种语言
- 🎨 提供29种不同的主题样式
- 🐳 提供适用于各种架构（如 amd64、arm64、arm/v7、arm/v6）的 Docker 镜像
- 🏠 可以自行搭建和管理

## UpSnap部署

🔺先打开极空间的文件管理器（个人空间），在Docker目录下新建“upsnap”文件夹用于数据文件的持久化。
![iStoreOS](/images/极空间/upSnap/2.png)

🔺然后和之前一样，打开极空间的Docker镜像仓库。因为这个项目的镜像发布在 ghcr.io，所以我们这里需要自定义拉取镜像“ghcr.io/seriousm4x/upsnap:latest”。
![iStoreOS](/images/极空间/upSnap/3.png)

🔺如果拉取镜像有问题，那么就就要考虑搞定你那边的网络问题。最新版本的极空间Docker管理器现在已经支持添加代理设置来解决这个问题了，至于怎么开启代理这里就不详说
![iStoreOS](/images/极空间/upSnap/4.png)

🔺完成后直接双击镜像开始部署容器。
![iStoreOS](/images/极空间/upSnap/5.png)

🔺【基本设置】这里，容器名称自己可以随意修改，可以取消勾选“启用性能限制”。
![iStoreOS](/images/极空间/upSnap/6.png)

🔺【文件夹路径】这里，咱们需要手动添加以下映射关系：
.Docker/upsnap:/app/pb_data    # 冒号前面映射新建的“upsnap”子文件夹
![iStoreOS](/images/极空间/upSnap/7.png)

🔺【文件夹路径】这里手动选取host。
![iStoreOS](/images/极空间/upSnap/8.png)

🔺因为这个项目默认的端口号是8090，而这个端口貌似被极空间某个程序占用了，所以我们可以在【命令】这里更改。在EntryPoint下面选择“自定义”，添加命令【'./upsnap' 'serve' '--http=0.0.0.0:XXXX' 】，XXXX就是我们更改的本地不冲突的其它端口，比如说我上图演示的端口为“8191”。
其它就没什么可修改的了，点“应用”即可完成配置。
![iStoreOS](/images/极空间/upSnap/9.png)

🔺回到Docker管理器的容器列表，可以看到项目“启动中”。
![iStoreOS](/images/极空间/upSnap/10.png)

🔺打开日志，看到显示“Admin UI”就说明可以使用了。
![iStoreOS](/images/极空间/upSnap/11.png)

🔺返回Docker管理器这里显示“非正常”，其实它是“正常”的（这话怎么看着有些毛病啊···)。
![iStoreOS](/images/极空间/upSnap/12.png)

## UpSnap体验

🔺打开方式浏览器【极空间IP:端口号】即可，UpSnap目前已经加入中文显示，之前还是没有的。首次打开先根据向导初始化设置。
![iStoreOS](/images/极空间/upSnap/13.png)

🔺其实就是创建一个管理员账号而已~。
![iStoreOS](/images/极空间/upSnap/14.png)

🔺完成后就可以开始使用了。
![iStoreOS](/images/极空间/upSnap/15.png)

🔺进来之后可以看到这里目前还没有任何设备，所以先添加设备吧。
![iStoreOS](/images/极空间/upSnap/16.png)

🔺添加设备分为手动配置和网络扫描，这里建议小伙伴们直接选择网络扫描可以快速添加。
![iStoreOS](/images/极空间/upSnap/17.png)

🔺需要说明的是，网络扫描一定要设置好IP范围，其实就是咱们使用的主路由器的IP网关，然后直接扫描即可，扫描速度还是比较快的，咱们想要唤醒那个设备，直接点击“添加”按钮即可。
![iStoreOS](/images/极空间/upSnap/18.png)

🔺比如说我目前添加了3个设备网络唤醒，它是以卡片的形式呈现在首页。可以看到第一个是我的华硕NAS，它显示的是黄色按钮，说明它目前是关机状态。
![iStoreOS](/images/极空间/upSnap/19.png)

🔺我只需要点击一下按钮，它就会变成一个黄色的倒计时状态。
![iStoreOS](/images/极空间/upSnap/20.png)

🔺稍等一会它就能唤醒成功了，就这么简单。
![iStoreOS](/images/极空间/upSnap/21.png)

🔺我们还能对设备上的端口号进行检测，还是以我唤醒的这台华硕NAS为例，我想要检测它的SSH 22端口，直接添加即可。
![iStoreOS](/images/极空间/upSnap/22.png)

🔺在首页位置可以看到检测的SSH 22端口是连通的。
![iStoreOS](/images/极空间/upSnap/23.png)

🔺同时它还能对局域网的一些主机远程关机，比如我在它的设置界面设置好关机命令之后，就能对其一键关机，非常方便。
![iStoreOS](/images/极空间/upSnap/24.png)

🔺还有非常多的个性化设置与主题可以选择。
![iStoreOS](/images/极空间/upSnap/25.png)

🔺想要远程控制？直接在极空间的远程访问添加UpSnap即可，记得需要勾选“代理模式”哦~
![iStoreOS](/images/极空间/upSnap/26.png)

🔺OK，就这么简单。
![iStoreOS](/images/极空间/upSnap/27.png)
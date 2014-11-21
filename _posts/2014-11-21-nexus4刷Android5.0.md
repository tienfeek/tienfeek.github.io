
Nexus 4 刷Android5.0
====================

##准备工作 

1. 解锁你的 Nexus 设备 
解锁教程：http://www.inexus.co/thread-3741-1-1.html 
温馨提示 1：解锁过程中会清空设备，切记要备份数据。 
温馨提示 2：如果你并不知道自己的设备有没有解锁，可以重启手机，观察开机动画前屏幕下方出现的「白色小锁」是否闭合，若然你的设备和下图一样呈「开锁」状，证明你的爱机早已解锁。 
![Alt text](http://cdn.sspai.com/attachment/thumbnail/2014/11/04/79140e866356e47e33a983393edd5c79_mw_800_wm_1_wmp_3.jpg)

2. 在 Windows 电脑上配置好 adb fastboot 环境： 
下载并解压 adb 工具包（下载地址） 
将名称中含有 adb 和 fastboot.exe 的文件复制到 c:/windows/system32 目录下 
再将名称中含有 adb 的所有文件复制到 c:/windows/system 文件夹里
考虑到用 MacBook 的大多数同学用的都是高贵冷艳的 iPhone，这边就不多阐述 OS X 配置 adb 环境教程了，感兴趣的同学可移步到：http://www.inexus.co/article-1636-1.html
下载工厂镜像 （[官方地址](https://developers.google.com/android/nexus/images)）

准备完毕后，教程正式开始。首先在《Android 5.0 Lollipop 正式版工厂镜像下载》中找到自己机型对应的镜像（需科学上网），然后在压缩工具打开工厂镜像，将其解压到任意目录下。


## 正式开刷 

将设备连接上电脑，进入工厂镜像解压后的目录；
找到 flash-all.bat，双击运行（OS X 需在终端输入sh flash-all.sh ）；
看到命令行窗口显示 waiting for drive 时，手动关闭设备，并同时按住电源键和音量下键；
这时候 Nexus 设备将进入 bootloader 模式开始刷机。
整个过程会持续两三分钟，完成后手机会自动重启进入 Android 5.0 Lollipop，这次开机需要等待较长时间，请耐心等待。

温馨提示

1. 刷入镜像时，系统默认会清除设备所有数据（含内置 SD 卡数据），请做好相关备份工作。

2. 若然要保留手机数据直接升级，可以在运行 flash-all.bat 前用「记事本」打开，将「fastboot -w update image- xxx-xxx.zip」中的「-w」 去掉，保存即可，OS X 下需修改 flash-all.sh。

3. 保留数据升级后，新系统可能会出现各种不可预知的问题。

4. 刷入镜像时出现 missing system.img 错误？戳这里查看解决方案。


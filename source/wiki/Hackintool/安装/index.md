---
layout: wiki
wiki: Hackintool
order: 102
title: BigSur安装教程
---



——本文章改编与[《黑果小兵部落阁》](https://blog.daliansky.net)   [天逸510s Mini兼macOS BigSur](https://blog.daliansky.net/Lenovo-Tianyi-510s-Mini-and-macOS-BigSur-Installation-Tutorial.html)安装教程

### 软件准备

#### 操作系统：

一个可以制作安装U盘的操作系统，包括但不限于**macOS** / **Windows** / ****Linux**** 等

比如：

- 运行  **macOS**  的苹果电脑；
- 运行  **Windows**  或者  **PE**  的电脑；
- 基于  **Live CD**  模式运行的  ****Linux****  系统等等；

#### 软件或者用到的工具：

##### md5检查器：**Windows**

- **Windows**:
  - [WinMD5](https://www.winmd5.com/)
- **macOS**或者**Linux**自带：
  -   md5   for macOS
  -   md5sum   for Linux

##### 磁盘分区工具

- **Windows**:
  - [Disk Genuis](https://www.diskgenius.cn/)
- **macOS**或者**Linux**：
  - 略

##### U盘制作工具

- [etcher](https://pan.bilnn.com/s/OxYmTz)
- [transmac](https://www.acutesystems.com/scrtm.htm)

#### 创建USB安装盘

##### 下载安装镜像

- 本站下载：[请点击前往](https://blog.daliansky.net/categories/下载/镜像/)
- 本站镜像盘：[世纪互联](https://download.shaoxingshare.com/t/6GpM2WdLWR) [迅雷](https://mirrors.dtops.cc/iso/MacOS/daliansky_macos/)

##### 校验  md5  值

-   **Windows**  环境：

  利用刚才下载的[WinMD5](https://www.winmd5.com/)检查md5值是否正确，如果md5值不相同**必须重新下载安装镜像，不要心存侥幸**

  ![WinMD5](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/WinMD5.png)

-   **macOS**  环境：

    ```
  # md5 macOS\ Big\ Sur\ 11.1\ 20C69\ Installer\ for\ CLOVER\ 5127\ and\ WEPE.dmg
  MD5 (macOS Big Sur 11.1 20C69 Installer for CLOVER 5127 and WEPE.dmg) = e39ea551e8dc099ea3bdff82d315f847
    ```

##### 将安装镜像写到  USB  上（制作安装镜像）

- 镜像制作：
  - 下载[etcher](https://pan.bilnn.com/s/OxYmTz)，选择安装镜像，选择需要制作的U盘，点击   Flash   即可。***Windows10需要以管理员权限运行***![etcher](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/etcher.png)

#### 查找适合自己的  EFI  

- 本站：[Hackintosh黑苹果长期维护机型整理清单](https://blog.daliansky.net/Hackintosh-long-term-maintenance-model-checklist.html)
- 通用EFI合集整理：
  - [世纪互联](https://download.shaoxingshare.com/t/65rvzjrvo4)：https://download.shaoxingshare.com/t/65rvzjrvo4
  - [比邻网盘](https://pan.bilnn.com/s/2k5NIM)：https://pan.bilnn.com/s/2k5NIM
- 其它：
  - 远景：[http://bbs.pcbeta.com](http://bbs.pcbeta.com/)
  - tonymacx86: [https://www.tonymacx86.com](https://www.tonymacx86.com/)
  - insanelymac: [insanelymac.com](https://www.insanelymac.com/)
  - 谷歌: [https://www.google.com](https://www.google.com/)

#### 替换USB安装盘里的  EFI  

如果USB安装盘自带的EFI无法完成安装或者安装后不完美，那么就需要执行替换EFI的操作

- 操作过程：（略）

## 安装  Big Sur  

### 设置  BIOS  

以联想  天逸510s Mini  为例：

- 安全菜单：
  - 安全启动 ->   关闭   (*Disable Secure Boot*)
- 高级菜单：
  -   CFG Lock   ->   关闭   (*Disabling CFG Lock*)
- 设备：
  - 显示设备
    - 预指派内存大小：  64MB   (*DVMT* pre-allocated memory)
  - ATA设备菜单：
    -   配置SATA为   ->   AHCI  
- 其它参数默认即可

### 安装  **macOS** Big Sur  

开机，按  F12  选择U盘引导，光标移动到  EFI USB Device  选择  OpenCore  分区启动：

进入  OpenCore  主引导界面，选择  Install macOS Big Sur  ，直接回车进入  OpenCore  引导，这期间会显示引导日志，也就是常见的  -v  (  啰嗦模式  )，如果不幸卡住了，请拍照发到  QQ群  里寻求帮助，也可以移步：[macOS BigSur 11.0安装中常见的问题及解决方法](https://blog.daliansky.net/Common-problems-and-solutions-in-macOS-BigSur-11.0-installation.html)；不会操作  OpenCore  的请事先补课：[精解OpenCore](https://blog.daliansky.net/OpenCore-BootLoader.html)

![OpenCore_Installer](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/OpenCore_Installer.png)

![OpenCore_Installer](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_01.png)

![BigSur_Installer_02](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_02.png)

很多的机友都是会在这个地方翻车。出现问题请进群反馈，请提供翻车照片及机器配置图。**不提供任何信息直接发问就是耍流氓**

![BigSur_Installer_03](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_03.png)

这个过程需要1-2分钟,耐心等待，进入安装程序,出现语言选择界面

![BigSur_Installer_04](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_04.png)

选择  简体中文  ，点击  →   继续

![BigSur_Installer_05](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_05.png)

出现安装界面，选择  磁盘工具  ，点击  继续  

![BigSur_Installer_06](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_06.png)

进入  磁盘工具  ，点击下图所示，选择  显示所有设备  

![BigSur_Installer_07](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_07.png)

***在  磁盘工具  里面所做的操作涉及到你的数据安全，请认真仔细确认后再操作，否则由此造成的一切后果本站概不负责。***

选择  APPLE SSD macOS Big Sur-0 SSD Media  ***本例中为虚拟机中的磁盘名称，请根据你的设备选择相应的磁盘***

![BigSur_Installer_08](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/vrnvXq.png)

点击  抹掉  ，在弹出的窗口中输入：名称：  Macintosh HD  ；格式：  APFS  ；方案：  GUID分区图  ，

***假设您的磁盘是空的或者数据是已经备份过的,别怪我没提醒你!!!***

点击  抹除  ，然后等待操作结束，点击  完成  ，通过菜单选择  退出磁盘工具  或者按窗口左上角红色按钮离开磁盘工具

![BigSur_Installer_09](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_09.png)

返回到安装界面，选择  安装macOS  ，点击  继续  

![BigSur_Installer_010](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_010.png)

点击  同意  ，继续

![BigSur_Installer_011](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_011.png)

阅读许可协议的条款，点击   同意  

![BigSur_Installer_012](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_012.png)

选择将要安装的磁盘卷标  Macintosh HD  ，点击  继续  

![BigSur_Installer_013](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_013.png)

它会把USB安装盘上的安装文件预复制到要安装的系统分区里，这个过程通常会持续1-2分钟，之后系统会自动重启，进入第二阶段的安装

![BigSur_Installer_014](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_014.png)

重启后继续安装，在安装期间，通常会自动重启2-3遍

![BigSur_Installer_016](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_016.png)

![BigSur_Installer_017](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_017.png)

![BigSur_Installer_018](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_018.png)
安装  Big Sur  的时间通常是安装  Catalina  的2倍，请务必耐心等待；安装完成后，会进入  设置向导  

![BigSur_Installer_020](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_020.png)

选择  国家和地区  ：  China mainland  ，点击  Continue  继续

![BigSur_Installer_021](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_021.png)

设置键盘，使用默认值，点击  Continue  继续
![BigSur_Installer_022](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_022.png)

进入辅助功能设置，默认不设置，选择  Not Now  继续

![BigSur_Installer_023](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_023.png)

进入网络连接设置，选择  My computer does not connect to the Internet  ，点击  Continue  继续

![BigSur_Installer_024](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_024.png)

弹出提示信息：  Your Mac isn t connected to the Internet.  ，点击  Continue  继续

![BigSur_Installer_025](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_025.png)

出现数据与隐私，阅读后点击  Continue  继续

![BigSur_Installer_026](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_026.png)

出现数据迁移助手，如果全新安装而不使用  Time Machine  恢复数据，请点击  Not Now  继续

![BigSur_Installer_027](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_027.png)

出现条款与条件，请阅读后，点击  Agree  继续

![BigSur_Installer_028](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_028.png)

在弹窗提示上再次点击  Agree  ，继续

![BigSur_Installer_029](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_029.png)

出现创建用户账号窗口，输入用户名和密码，点击  Continue  继续

![BigSur_Installer_030](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_030.png)

出现快速设置窗口，点击  Continue  继续

![BigSur_Installer_031](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_031.png)

出现分析窗口，点击  Continue  继续

![BigSur_Installer_032](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_032.png)

出现屏幕使用时间窗口，点击  Set Up Later  继续

![BigSur_Installer_033](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_033.png)

出现  Siri  设置界面，点击  Continue  继续

![BigSur_Installer_034](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_034.png)

选择  Siri  语言，点击  Continue  继续

![BigSur_Installer_035](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_035.png)

进入  Siri  改善和听写界面，选择  Not Now  ，点击  Continue  继续

![BigSur_Installer_036](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_036.png)

弹出界面，让你选择外观

![BigSur_Installer_037](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_037.png)

您可以根据个人的喜好选择浅色主题或者深色主题，点击  Continue  继续

![BigSur_Installer_038](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_038.png)

出现  正在设置您的Mac  ,请稍候完成设置向导

![BigSur_Installer_039](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_039.png)

设置向导完成，根据选择主题的不同，分别进入不同的界面

![BigSur_Installer_040](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_040.png)

出现桌面后,整个的安装向导就完成了。

![BigSur_Installer_041](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/BigSur_Installer_041.png)

## 安装后的系统设置

系统安装后,你可以先喝杯咖啡兴奋会儿,马上还有更艰巨的任务在等着你呢

先打开终端，输入几行命令：

  ```
sudo spctl --master-disable		# 启用macOS安装应用允许任何来源
sudo kextcache -i /						# 重建缓存
  ```

如果出于某些原因，在  /System/Library/Extensions/  或者  /Library/Extensions/  修改了某些驱动，请使用以下命令重建缓存：

  ```
sudo chown -R root:wheel /System/Library/Extensions/
sudo chmod -R 755 /System/Library/Extensions/
sudo kmutil install --update-all
sudo kcditto
  ```

### 将U盘中的EFI复制进硬盘

#### 工具篇

目的是脱离U盘引导使用**macOS**，所以它是最优先需要执行的动作

最简单的方法：使用工具  Hackintool  ,如图所示：

1. 打开  Hackintool  工具，点击  磁盘  图标![Hackintool_Disk](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/Hackintool_Disk.png)
2. 点击挂载图标，输入用户密码![Hackintool_Disk_Mount](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/Hackintool_Disk_Mount.png)
3. 分别点击挂载固态硬盘和安装U盘的EFI分区，并打开文件夹![Hackintool_Disk_Mount2](https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/Hackintool_Disk_Mount2.png)
4. 将U盘的  EFI  分区中的  EFI  目录复制到固态硬盘的  EFI  分区里即可

#### 命令行篇

##### 查看磁盘分区表

  ```
diskutil list
  ```

> */dev/disk0(internal, physical):*

| #:   |                  TYPE | NAME            | SIZE     | IDENTIFIER |
| :--- | --------------------: | :-------------- | :------- | :--------- |
| 0:   | GUID_partition_scheme |                 | 256 GB   | disk0      |
| 1:   |                   EFI | EFI             | 200 MB   | disk0s1    |
| 2:   |            Apple_APFS | Container disk1 | 128 GB   | disk0s2    |
| 3:   |  Microsoft Basic Data | WIN10           | 127.7 GB | disk0s3    |

> */dev/disk2(external, physical):*

| #:   |                  TYPE | NAME                  | SIZE    | IDENTIFIER |
| :--- | --------------------: | :-------------------- | :------ | :--------- |
| 0:   | GUID_partition_scheme |                       | 16 GB   | Disk2      |
| 1:   |                   EFI | EFI                   | 200 MB  | disk2s1    |
| 2:   |  Microsoft Basic Data | PE                    | 716.8MB | Disk2s2    |
| 3:   |             Apple_HFS | Install macOS Big Sur | 15.8 GB | Disk2s3    |

##### 挂载固态硬盘EFI分区

  ```
sudo diskutil mount disk0s1
  ```

##### 挂载U盘EFI分区

  ```
sudo diskutil mount disk2s1
  ```

打开Finder，注意后面有个  .  

  ```
open .
  ```

左侧会显示挂载了两个EFI分区，将U盘EFI目录全部复制到磁盘的EFI分区即可。

### 完善驱动

刚安装完的系统，只能算是万里长征走完的第一步，对于驱动部分的完善才是重中之重。除非你有相同机型的  EFI  可供借鉴，否则请耐心阅读下面的内容。

#### 显卡：

在所有的驱动里，显卡驱动是应该最优先解决的。

参考的文章：

- 黑苹果必备：[Intel核显platform ID整理](https://blog.daliansky.net/Intel-core-display-platformID-finishing.html)
- [利用Hackintool工具驱动核显](https://blog.daliansky.net/Intel-FB-Patcher-tutorial-and-insertion-pose.html#核心功能给缓冲帧打补丁)
- [利用Hackintool打开第8代核显HDMI/DVI输出的正确姿势](https://blog.daliansky.net/Tutorial-Using-Hackintool-to-open-the-correct-pose-of-the-8th-generation-core-display-HDMI-or-DVI-output.html)
- 醉渔小站：[使用 WhateverGreen 驱动 Intel 核显](https://blog.zuiyu1818.cn/posts/Hac_Intel_Graphics.html)
- WhateverGreen: [英特尔® 核芯显卡 常见问答](https://github.com/acidanthera/WhateverGreen/blob/master/Manual/FAQ.IntelHD.cn.md)

#### 网卡

如果幸运的话，安装好的黑苹果系统默认已经支持有线网线的连接了，这是因为它内置的通常都是  RTL8111  或者  INTEL  等的驱动，而无线网卡的驱动就需要单独添加

##### 博通：

绝大多数的博通(Boardcom)可以得到免驱或者通过添加驱动得到支持；

- [DW1820A/BCM94350ZAE/BCM94356ZEPA50DX插入的正确姿势](https://blog.daliansky.net/DW1820A_BCM94350ZAE-driver-inserts-the-correct-posture.html)

##### INTEL：

感谢 [OpenIntelWireless](https://github.com/OpenIntelWireless) 提供 [AirportItlwm](https://github.com/OpenIntelWireless/itlwm)，[HeliPort](https://github.com/OpenIntelWireless/HeliPort) 和 [itlwm](https://github.com/OpenIntelWireless/itlwm)

感谢[stevezhengshiqi](https://github.com/stevezhengshiqi)更新维护的 [驱动内置英特尔无线网卡](https://github.com/daliansky/XiaoMi-Pro-Hackintosh/wiki/驱动内置英特尔无线网卡)

###### 准备

在这个教程里，我们将介绍两种方式来驱动我们的英特尔无线网卡。

- **[使用 itlwm 和 HeliPort](https://blog.daliansky.net/Lenovo-Tianyi-510s-Mini-and-macOS-BigSur-Installation-Tutorial.html#使用-itlwm-和-heliport)**
- **[使用 AirportItlwm](https://blog.daliansky.net/Lenovo-Tianyi-510s-Mini-and-macOS-BigSur-Installation-Tutorial.html#使用-airportitlwm)**

**如果想使用   AirportItlwm   和   itlwm  ，** 您可以从以下链接来下载最新 releases：

- https://github.com/OpenIntelWireless/itlwm/releases

**如果想使用   HeliPort  ，** 您可以从以下链接来下载最新 releases：

- https://github.com/OpenIntelWireless/HeliPort/releases

###### 如何使用

###### 使用 itlwm 和 HeliPort

- 首先，进入  系统偏好设置 - 网络 - Wi-Fi  ，关闭  在菜单栏中显示 Wi-Fi 状态  。
- 然后，解压所有下载的包并拷贝   itlwm.kext   到   /EFI/CLOVER/kexts/Other/   或者   /EFI/OC/Kexts/  。
- 如果您是 OC 用户，您需要添加以下代码到   config.plist  ：

  ```
<dict>
	<key>Arch</key>
	<string>x86_64</string>
	<key>BundlePath</key>
	<string>itlwm.kext</string>
	<key>Comment</key>
	<string>Intel Wi-Fi driver</string>
	<key>Enabled</key>
	<true/>
	<key>ExecutablePath</key>
	<string>Contents/MacOS/itlwm</string>
	<key>MaxKernel</key>
	<string></string>
	<key>MinKernel</key>
	<string>16.0.0</string>
	<key>PlistPath</key>
	<string>Contents/Info.plist</string>
</dict>
  ```

- 重启，然后移动   HeliPort.app   到您的   应用程序   文件夹。

- 打开

   

    ```
  HeliPort.app
    ```

  ，完成。

  - 您需要先允许任意来源。
  - 打开   终端.app   并运行   sudo spctl --master-disable  。

###### 使用 AirportItlwm

- 首先，确保你的 **macOS** 版本 >= 10.15，此教程只涵盖 OpenCore 引导。
- 移除   itlwm   和   HeliPort   并进入  系统偏好设置 - 网络 - Wi-Fi   打开   在菜单栏中显示 Wi-Fi 状态  。
- 然后，解压下载的包并拷贝   AirportItlwm.kext   到   /EFI/CLOVER/kexts/Other   或者   /EFI/OC/Kexts/  。

###### 如果是 Clover 用户

- 打开   /EFI/CLOVER/config.plist   并在   KernelAndKextPatches - ForceKextsToLoad   里添加以下代码：

  ```
<key>ForceKextsToLoad</key>
<array>
	<string>\System\Library\Extensions\IO80211Family.kext</string>
</array>
  ```

###### 如果是 OpenCore 用户

- 打开   /EFI/OC/config.plist   并更改以下代码：

  ```
<dict>
	<key>Arch</key>
	<string>x86_64</string>
	<key>BundlePath</key>
	<string>AirportItlwm.kext</string>
	<key>Comment</key>
	<string>Intel Wi-Fi driver</string>
	<key>Enabled</key>
-	<false/>
+	<true/>
	<key>ExecutablePath</key>
	<string>Contents/MacOS/AirportItlwm</string>
	<key>MaxKernel</key>
	<string></string>
	<key>MinKernel</key>
	<string>19.0.0</string>
	<key>PlistPath</key>
	<string>Contents/Info.plist</string>
</dict>
  ```

- 同时，修改   SecureBootModel   来允许加载 immutablekernel。如果您的 **macOS** 版本 >= **macOS**11 (KernelCollection)，就不需要做以下步骤：

  ```
	<key>DmgLoading</key>
-	<string>Any</string>
+	<string>Signed</string>
	<key>SecureBootModel</key>
-	<string>Disabled</string>
+	<string>Default</string>
  ```

- 如果上述方法不管用，还原对   DmgLoading   和   SecureBootModel   的修改，然后强制加载   IO80211Family  。打开   /EFI/OC/config.plist   并更改以下代码：

  ```
<key>Force</key>
<array>
	<dict>
		<key>Arch</key>
		<string>Any</string>
		<key>BundlePath</key>
		<string>System/Library/Extensions/IO80211Family.kext</string>
		<key>Comment</key>
		<string></string>
		<key>Enabled</key>
-		<false/>
+		<true/>
		<key>Identifier</key>
		<string>com.apple.iokit.IO80211Family</string>
		<key>ExecutablePath</key>
		<string>Contents/MacOS/IO80211Family</string>
		<key>MaxKernel</key>
		<string>19.99.99</string>
		<key>MinKernel</key>
		<string></string>
		<key>PlistPath</key>
		<string>Contents/Info.plist</string>
	</dict>
</array>
  ```

- 如果你是 **macOS**10.13 用户，你还需要强制加载   corecapture.kext  。在   IO80211Family.kext   条目前添加以下代码：

  ```
<dict>
	<key>Arch</key>
	<string>Any</string>
	<key>BundlePath</key>
	<string>System/Library/Extensions/corecapture.kext</string>
	<key>Comment</key>
	<string></string>
	<key>Enabled</key>
	<true/>
	<key>Identifier</key>
	<string>com.apple.driver.corecapture</string>
	<key>ExecutablePath</key>
	<string>Contents/MacOS/corecapture</string>
	<key>MaxKernel</key>
	<string>17.99.99</string>
	<key>MinKernel</key>
	<string>17.0.0</string>
	<key>PlistPath</key>
	<string>Contents/Info.plist</string>
</dict>
  ```

###### 讨论

- 如果您对驱动有任何疑问，请进入 https://gitter.im/OpenIntelWireless/itlwm 来参与讨论。
- 如果您想反馈问题，请使用 https://github.com/OpenIntelWireless/itlwm/issues

#### 声卡

- [AppleALC声卡仿冒ID查询](https://github.com/acidanthera/AppleALC/wiki/Supported-codecs)
- [利用hackintool工具驱动你的声卡](https://blog.daliansky.net/Intel-FB-Patcher-tutorial-and-insertion-pose.html#声卡修补)
- 声卡仿冒教程：[使用AppleALC声卡仿冒驱动AppleHDA的正确姿势](https://blog.daliansky.net/Use-AppleALC-sound-card-to-drive-the-correct-posture-of-AppleHDA.html)

通常台式机的声卡可以尝试注入ID：layout   1, 2, 3, 5, 7, 11  

笔记本的声卡ID需要注入正确的ID：[AppleALC声卡仿冒ID查询](https://github.com/acidanthera/AppleALC/wiki/Supported-codecs)

#### 其它驱动

@  宪武   提供的hotpatch的全套方法：

- 适用于  CLOVER   的 [P-little](https://github.com/daliansky/P-little) ；
- 适用于   OpenCore   的 [OC-little](https://github.com/daliansky/OC-little)

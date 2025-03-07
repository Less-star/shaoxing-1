---
layout: wiki
wiki: Hackintool
order: 1
seo_title: 黑果小六
title: 黑苹果 （操作系统）
cover: true
logo:
  src: https://cdn.jsdelivr.net/gh/muzishaoxing/Picture@main/uPic/avatar.png
small: 
  large: 
description: 此文档由本站在黑苹果安装过程中收集，测试，改编而成。所属资料版权归属原作者。

---




> **版权©️声明 : 此页出自 百度百科 [黑苹果 （操作系统）](https://baike.baidu.com/item/黑苹果/5220943?fr=aladdin)**

------------




&emsp;     自从苹果采用[Intel](https://baike.baidu.com/item/Intel)的[处理器](https://baike.baidu.com/item/处理器/914419)，[OS X](https://baike.baidu.com/item/OSX/426765)被黑客破解后可以安装在Intel [CPU](https://baike.baidu.com/item/CPU/120556)与部分[AMD](https://baike.baidu.com/item/AMD/5905) CPU的机器上。从而出现了一大批非苹果设备而使用苹果操作系统的机器，被称为黑苹果(Hackintosh)；在Mac苹果机上面安装原版Mac系统的被称为白苹果（[Macintosh](https://baike.baidu.com/item/Macintosh)），与黑苹果相对。

| 中文名 |     黑苹果 |  类型  | [操作系统](https://baike.baidu.com/item/操作系统/192)（OS） |
| :----: | ---------: | :----: | ----------------------------------------------------------: |
| 外文名 | Hackintosh | 反  义 |                                                      白苹果 |



## MAC系统

&emsp;     OS X 是全球领先的操作系统。基于坚如磐石的 UNIX ，设计简单直观，让处处充满创新的Mac 安全易用，高度兼容，出类拔萃。UNIX 之威力，iMac 之简单让Mac OS X 既简单易用且功能强大。所有的一切 - 从启动 Mac 后所看到的桌面，到你日常使用的应用程序，都设计得简约精致。无论是浏览网页、查看邮件和与外地朋友视频聊天，所有事情都简单高效、趣味盎然。当然，简化复杂任务要求尖端科技，而 Mac OS X 正拥有这些尖端科技。它不仅使用基础坚实、久经考验的 UNIX 系统提供空前的稳定性，还提供超强性能、超炫图形并支持互联网标准。 [1] 。


## 发展背景

&emsp;     它以 Mach 核心为基础和 UNIX的 BSD 实作，整合到由 Steve Jobs 于 1985年被迫离开苹果后的 NeXT 公司所发展 面向对象操作系统 之 NeXTSTEP 中。同时，苹果电脑企图创造一个自己拥有的（参考 en:Taligent 和 en:Copland） "下个时代" 操作系统，但只有小部份成功。最后 NeXT 的操作系统—在那时候称为 OPENSTEP—被选为苹果下个操作系统的基础形式，然后苹果电脑完全地买下了 NeXT。Jobs 也就重新被聘雇，后来回到公司的领导阶层，带领大家把程序设计师亲善的 OPENSTEP，转换到苹果主要家庭使用者市场和创新的专家都很欢迎的一个系统上，就是大家都知道的 Rhapsody。在某些威胁独立开发者对于 Mac OS 忠心的失策，以及对于从 Mac OS 9 到新系统减轻转变的策略改变后，Rhapsody 演化为 OS X。　OS X 是与先前麦金塔操作系统彻底地分离开来，它的底层程序码完全地与先前版本不同。尽管最重要的架构改变是在表面之下，但是 Aqua GUI 是最突出和引人注目的特色。柔软边缘的使用，半透明颜色和细条纹（与第一台 iMac 的硬件相似）把更多的颜色和材质带入到桌面上的视窗和控件，比 OS9 所提供的 "白金" 外观更多，引发了使用者间大量的争论。很多旧的麦金塔使用者把这个接口描述得像是玩具一般，和缺乏专业的优美，而其他的人则为苹果革命的新 GUI 欢呼。这种外观非常立即地可以辨认出来，即使在第一个 OS X 版本推出之前，第三方的开发者开始针对可以换外表的程序像是 Winamp 制作类似 Aqua 接口的外表。苹果电脑以法律行动，威胁那些声称是由他们有版权的设计下，所制造或散布且提供这种接口软件的人。　纯粹由系统销售的数字来看，这种 GUI 和核心的组合最近变成最畅销的类 Unix 环境。

&emsp;     尽管苹果官方声称，OS X只能在使用G3或更高阶的微处理器的电脑上运行。但实际上，通过修改，OS X 亦能成功安装并运行在较早期的Power PC 604e上；甚至有人透过PearPC模拟器Linux版，在更早期的Centris 650 (25MHz) 上安装OS X 10.3，只是以此方式安装的OS X，没有多大的实用价值可言。(仅系统自我检测便得花上数天时间)　OS X 透过提供一种称为 Classic 的模拟环境，保留了与较旧的 Mac OS 应用程序的兼容像，允许使用者在 OS X 中把 Mac OS 9 当做一个程序行程来执行，使大部分旧的应用程序就像在旧的操作系统下执行一样。另外，给 Mac OS 9 和 OS X 的 Carbon API 可以创造出允许在两种系统执行的程序码。OpenStep 的 API 也依然可以使用，但是苹果把它称为 Cocoa 技术。(这个遗留下来的传统可以在 Cocoa API 中看到，大部分的类别名称都是以 NeXTSTEP 的缩写 "NS" 开头。) 给开发者的第四个选项是可以在 OS X 当做 "第一等公民" 一样的 Java 平台上写应用程序 — 事实上这就是说 Java 应用程序尽可能的与操作系统合适地搭配而仍然能够"跨平台(cross-platform)"，以及他的 GUI，是以 Swing 撰写的，看起来几乎完全地与天生的 Cocoa 接口类似。　只要他们能够在这个平台上被编译，OS X 可以执行很多 BSD 或 Linux 软件套件。编译过的程序码通常是以 OS X 封装的方式来散布，但有些可能需要命令列的组态设定或是编译。像是 Fink 和 DarwinPorts 这样的专案，提供很多标准套件之预先编译或是预先格式好的封装。

&emsp;     在 10.3 版开始，OS X 已经包含 Apple X11，这是给 Unix应用程序的 X11 图形接口的公司版本，当做是在安装阶段的选择性元件。苹果是以 XFree86 4.3 和 X11R6.6 为基础实作的，搭配一个模仿 OS X 外观的视窗管理员，与 OS X 有更密切的整合，延展扩充到使用天生的 Quartz 显像系统和加速 OpenGL。

&emsp;     早期的 OS X 版本可使用 XDarwin 来执行 X11 应用程序。

&emsp;     对于早期的 OS X 版本，有支援的标准硬件平台是以 PowerPC G3、G4、G5 处理器的麦金塔电脑产品线（膝上型、装上型、或是服务器）。后期的 OS X 版本不再支援某些老旧的硬件、举例来说，Panther 不支援 "米黄色" G3，以及 Tiger 不支援苹果在推出 FireWire 之前的系统。然而，免费的工具像是 XPostFacto 可以使得苹果官方宣称不支援的某些旧系统可以安装 OS X，包含某些 G3 之前的系统。操作系统针对所有支援的硬件提供相同的功能，除了基本硬件的限制之外（例如，CD-ROM 不能烧录 CD）以及在更多先进配备上尽量增快效能（例如图形加速）。

&emsp;     于2005年6月6日，Steve Jobs 在苹果每年的全球开发者大会中发表演说，表示接下来的两年间苹果将会从 PowerPC 转换到 Intel 的微处理器[1]，而且在这个转变的期间，OS X 都会支援两种平台。对于 PowerPC 平台的支援会一直持续到 10.5 版，但是同时支援两种平台多久的时间并不清楚（Mac OS 对于 Motorola 68k 架构的支援一直持续到 PowerPC 系统推出后的约四年）。

&emsp;     新版的 Xcode 支援建造 通用二元程序码(Universal Binaries)，可以在两种架构执行。PowerPC 程序码在 Intel 为基础的 Mac 会使用称为 Rosetta 的模拟器来提供支援。Jobs 也证实先前的谣言，就是苹果之前每一版的 OS X 开发周期都有 Intel 微处理器的版本。像是跨平台的能力已经早就存在 OS X 的血统中 - 就是 OS X 的前身，OPENSTEP，已经被移植到很多个架构下，包含 Intel 的 x86，以及 OS X 的核心操作系统 Apple Darwin 也移植到 x86，早在 OS X 第一次推出就可以免费下载。然而，苹果声明 x86 平台的 OS X 将不会支援 Classic 环境。 [2] 



## 讨论社区

- [远景论坛或远景在线](https://bbs.pcbeta.com/)

  [黑苹果板块](https://bbs.pcbeta.com/forum.php?gid=86)，国内的主要讨论社区，大部分资料来源于此处，高手云集。

- [威锋论坛或威锋网](https://www.feng.com/forum)
  [黑苹果板块](https://www.feng.com/forum/13)，国内主要讨论苹果的一线社区，iOS为主要讨论对象






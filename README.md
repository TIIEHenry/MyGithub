# 公开项目

## [AgenticLoopDev](https://github.com/TIIEHenry/AgenticLoopDev)

任务写在仓库里。每个任务占一个工作区，合回去的时候，两边还没提交的修改都留着。

## [TerminatorX](https://github.com/TIIEHenry/TerminatorX)

一个窗口里放多个终端。标签和窗格在左侧，拖动可以重排、嵌到别的标签下面，或把窗格拉成自己的标签。一个窗格可以盖住其余窗格，再收回来。终端用的是 GNOME Terminal 那套 VTE。窗口是白色标题栏；窗格之间一条 1px 的线，只有分开之后才有窗格标题栏。

命令是 `terminator`。

<img src="shots/terminatorx/main.png" alt="TerminatorX 主窗口，左侧是标签列表，右侧是两个窗格" width="720">

## Android

### [AppSnapshoter](https://github.com/TIIEHenry/AppSnapshoter)

在 Root 下把一个应用的安装包和数据打成快照，用来备份和恢复。每个应用可以留多份，也可以沿时间线查看。

<img src="shots/appsnapshoter/home.png" alt="AppSnapshoter 主页" width="180">
<img src="shots/appsnapshoter/snapshotting.png" alt="正在做快照" width="180">
<img src="shots/appsnapshoter/archives.png" alt="存档列表" width="180">
<img src="shots/appsnapshoter/timeline.png" alt="时间线" width="180">

### [ClashMetaForAndroid](https://github.com/TIIEHenry/ClashMetaForAndroid)

Clash Meta 的 Android 客户端。哪些应用走代理，存成几份策略，用的时候换一份。

### [CrashCenter](https://github.com/TIIEHenry/CrashCenter)

接住应用里没人处理的 Java 异常，应用不会因此直接闪退，崩溃日志留着。

### [HyperOSRuntime](https://github.com/TIIEHenry/HyperOSRuntime)

在别的手机系统上运行 HyperOS 的天气、相册这些系统应用。系统版本和芯片平台要和原来的机型一致。

### [Android-Interface-IPC](https://github.com/TIIEHenry/Android-Interface-IPC)

跨进程调用写成普通的 Java 接口，不用写 AIDL。

## GNOME 扩展

这四项在同一条面板上一起用。

### [Gnome-AppIndicatorChip](https://github.com/TIIEHenry/Gnome-AppIndicatorChip)

托盘收成一块读数。面板上是 `14 U 33 M`，钉住的图标留在旁边，其余在点开的格子里，底下是「管理托盘图标...」。读数宽度是固定的，数字变了，旁边的图标不动。

<img src="shots/appindicator/chip.png" alt="面板上的 14 U 33 M，以及打开的托盘收纳" width="480">

### [Gnome-TopBarOrganizer](https://github.com/TIIEHenry/Gnome-TopBarOrganizer)

托盘图标按应用记住位置。应用重启之后还是原来那一条。

### [Gnome-NetSpeed](https://github.com/TIIEHenry/Gnome-NetSpeed)

网速占一块固定的宽度。位数和单位变了，旁边的图标不动。

### [gnome-nvidia-extension](https://github.com/TIIEHenry/gnome-nvidia-extension)

面板上显示 NVIDIA 的读数。显示哪些项，在菜单里选。

<img src="shots/nvidia/panel.png" alt="面板上的 NVIDIA 读数" width="480">

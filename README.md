# 公开项目

## 桌面

这四项挂在同一条面板上，一起开。

### [Gnome-AppIndicatorChip](https://github.com/TIIEHenry/Gnome-AppIndicatorChip)

托盘入口是一块固定宽度的 CPU / 内存读数，例如 `14 U 33 M`，数字变了旁边的图标也不跟着挪。点开是收纳面板：图标按网格排，底下是「管理托盘图标...」。钉住的图标留在读数旁边，其余收进这个面板。管理页里可以改每个图标是留在面板上还是收进去，并调整顺序。

<img src="shots/appindicator/chip.png" alt="面板上的 14 U 33 M，以及打开的托盘收纳" width="480">

### [Gnome-TopBarOrganizer](https://github.com/TIIEHenry/Gnome-TopBarOrganizer)

上游用托盘的 id 记住图标属于哪个应用。有的库用进程号当 id，应用每启动一次就多一条，设置页会堆到上千条。这里在 id 里带长数字时改用标题来认应用，保存顺序时清掉已经不在面板上的旧记录，并把同一次启动里的 XEmbed 和 SNI 记成同一个应用。面板上的左右顺序和芯片的收纳一起用。

### [Gnome-NetSpeed](https://github.com/TIIEHenry/Gnome-NetSpeed)

网速文字一变长，整条面板就会左右挪。这里把文字放进固定宽度的槽，槽外的图标不再被推开。宽度、对齐、单位后缀和刷新间隔都可以改，改完立刻生效。它和芯片、托盘图标排在同一条面板上。

### [gnome-nvidia-extension](https://github.com/TIIEHenry/gnome-nvidia-extension)

面板上显示 NVIDIA GPU 的读数，数据来自 `nvidia-smi`，也可以用 `nvidia-settings`。要显示哪些项从下拉菜单里勾选。这条 `legacy` 分支给旧版 GNOME Shell 用，并修了多卡时的解析错误。和上面几项一起挂在面板上。

<img src="shots/nvidia/panel.png" alt="面板上的 NVIDIA 读数" width="480">

## 终端

### [TerminatorX](https://github.com/TIIEHenry/TerminatorX)

在一个窗口里放多个终端。标签和窗格排在左侧，拖动可以重排、把一个标签嵌到另一个下面，或把窗格拉成自己的标签。一个窗格可以盖住其余窗格，再退回来。底下的终端是 VTE，和 GNOME Terminal 用的是同一个组件。窗口本身很薄：白色标题栏、窗格之间一条 1px 的线，只有分割之后才出现窗格标题栏。

基于 Terminator 2.1.6。命令名仍是 `terminator`。

<img src="shots/terminatorx/main.png" alt="TerminatorX 主窗口，左侧是标签列表，右侧是两个窗格" width="720">

## Android

### [AppSnapshoter](https://github.com/TIIEHenry/AppSnapshoter)

在 Root 下把一个应用的 APK、数据、OBB 打成压缩快照，用来备份和恢复，也可以交给 Syncthing 同步。打包在原生层做 TAR 和 ZSTD。同一个 APK 不重复压。每个应用可以留多份存档，也可以按时间线跨分组看。

<img src="shots/appsnapshoter/home.png" alt="AppSnapshoter 主页" width="180">
<img src="shots/appsnapshoter/snapshotting.png" alt="正在做快照" width="180">
<img src="shots/appsnapshoter/archives.png" alt="存档列表" width="180">
<img src="shots/appsnapshoter/timeline.png" alt="时间线" width="180">

### [CrashCenter](https://github.com/TIIEHenry/CrashCenter)

Xposed 模块。在目标进程里接住没有人处理的 Java 异常，让应用不要直接闪退，并把崩溃日志留下来。应用名是稳定性中心，包名 `nota.android.crash.xp.app`。

### [ClashMetaForAndroid](https://github.com/TIIEHenry/ClashMetaForAndroid)

Clash Meta 的 Android 客户端。在上游之上加了应用策略：访问控制可以存成多份，每份有名字、模式（允许全部、只允许选中、拒绝选中）和包名列表，用的时候切换当前这一份。

### [HyperOSRuntime](https://github.com/TIIEHenry/HyperOSRuntime)

让 HyperOS 的系统应用跑在别的手机系统上。用 Magisk 模块加 Xposed 模块，再装天气、相册这类系统应用。Android 版本和芯片平台（高通 QC、联发科 MTK）最好和原来的机型一致。

### [Android-Interface-IPC](https://github.com/TIIEHenry/Android-Interface-IPC)

用普通 Java 接口做跨进程调用，不写 AIDL 文件。这样 Gradle 模块之间不用互相引用 AIDL，同名方法可以重载，也可以把调用注进已有的 Binder。没有 oneway，数据类型也不做静态检查，速度比 AIDL 稍差。

## 编码代理

### [AgenticLoopDev](https://github.com/TIIEHenry/AgenticLoopDev)

给编码代理用的一套循环。任务写在仓库里的文本契约上，不靠对话记忆。人和代理、代理和代理分开占用 git worktree，合回去时走三路合并，不覆盖另一边没提交的修改。做完的人不能自己宣布做完，要过独立核对和本地测试。

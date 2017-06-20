# CCR Plus 测评器
CCR Plus 是一款适用于 NOI(National Olympiad in Informatics) 系列比赛的开源的跨平台测评环境，使用 Qt 编写，是对原版 CCR 测评器的重大改进。CCR Plus 目前支持 Windows 和 Linux 两大操作系统，可以方便地配置与评测传统题、提交答案题等题型。


## 下载与安装
### 下载地址
<https://github.com/zhzh2001/CCR-Plus/releases>

### 安装及使用说明：
#### Windows
解压下载文件到安装目录，无需安装，直接双击 `CCR-Plus.exe` 运行程序。可自行创建桌面快捷方式。

#### Linux

解压下载文件到安装目录，双击运行 `install.sh`，把生成的图标复制到任意位置，再双击图标运行程序。


## 从源代码构建
你可以直接下载源代码，并从源代码构建 CCR Plus：

* [Windows 构建方法](https://github.com/sxyzccr/CCR-Plus/wiki/Windows-Build)
* [Linux 构建方法](https://github.com/sxyzccr/CCR-Plus/wiki/Linux-Build)


## 新增功能

下面列出了 CCR Plus 相对于原版 CCR 的重大改进：

1. 支持 Linux 操作系统。
2. 支持直接移动表头来更改题目顺序。
3. 更方便地选择测评某几项。
4. 鼠标移到测评信息的测试点编号上时，会显示该测试点的信息。
5. 通过 .prb 文件可以设置编译时限与校验器时限。
6. 支持配置提交答案型试题。
7. 配置试题时，可以只更改某一试题的某几项信息，而不全部重新配置，当然也可以选择重新配置某一题。
8. 强大的高级配置功能，支持修改编译器、修改测试点、打包测试点等功能。


by zhzh2001:

1. 删除令人困惑的“进程被阻塞”，简化超时判定，允许多线程的解答。
2. 默认识别代码并自动链接[GMP](https://gmplib.org/),[MPFR](http://www.mpfr.org/),GCC libquadmath等数学库，可以手动禁止。

## TO-DO-LIST

- [ ] 手动指定超时判定方式
- [ ] 加入帮助文件

## 注意事项

### Windows
1. 如果界面字体显示不正常(很难看)，请安装字体“微软雅黑”。
2. 如果使用选手名单后中文显示乱码，请转换名单的文件编码为 ANSI，行尾格式为 Windows。
3. 请注意在环境变量中添加编译器路径。

### Linux
1. 请注意设置某些文件的可执行权限。
2. 竞赛目录不要放在 Windows 文件系统(NTFS, FAT)中，要放在 Linux 文件系统(Ext3, Ext4)中。
3. 如果使用选手名单后中文显示乱码，请转换名单的文件编码为 UTF-8，行尾格式为 Unix。


## BUG
下面列出了一些已知且暂时无法修复的 BUG：

### Windows
1. 如果选手的程序编译超时，测评器可能无法结束一个叫 cc1plus 的进程。必要时需手动结束该进程，以免占用系统资源。

### Linux
1. 即使终止测评，选手的程序进程也会等到它运行结束或超过时间限制后才被结束。必要时需手动结束该进程，以免占用系统资源。
2. 某些按钮未完全汉化。


## LICENSE
基于 [GPLv3](LICENSE.txt)。请在获取源代码后遵循此许可证。

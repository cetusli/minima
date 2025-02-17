---
layout: post
title: "Use Ubuntu in Win10"
author: Cetus Li
date: 2021-01-14
---
#### <b>Windows 用户使用 Linux 的 3 种方法 </b>
1. 在电脑上安装双系统
2. 在 Windows 中使用 VMware
3. 在 Windows 中使用 WSL（Windows Subsystem for Linux）

#### <b>这三种方法各自的特点 </b>
##### 1、在电脑上安装双系统 
如果电脑是近几年大品牌产的笔记本电脑，不建议改装操作系统。因为出厂自带的 Windows 系统集成了厂家自带的很多设置，在稳定性和安全性上都有加强，能最大程度发挥性能。在不考虑加新的（内置或外置）存储盘的情况下，安装双系统首先需要 破坏原有 Windows 系统:one: ，这会削弱电脑的使用体验。

优点是用户真的拥有两台电脑，缺点是一次只能使用其中一台，而且用户切换操作系统需要电脑关机重启，在预启动页面选择另一个操作系统，该过程费时。另外，两个系统中的文件不能及时互动，一般使用U盘或云盘在两者之间转移文件。

>:one:<small> 安装双系统需要删除已有分区；格式化硬盘；权衡两个操作系统使用磁盘情况，分配好各自的磁盘空间大小；分别建立分区，分区时所使用文件系统格式：Windows/NTFS 和 Linux/ext3；然后分别安装对应的电脑操作系统。</small>

##### 2、在 Windows 中使用 VMware 
在以前，VMware Workstation 只能免费试用一个月，当然，也有人使用破解版。现在有官方免费版本 <b>VMware Workstation Player</b>，用于非商业、个人和家用目的。免费的 VMware Workstation Player 只能运行单一虚拟机，对于大部分人一个虚拟机够用了。使用虚拟机是一个很不错的选择，尤其对于没有虚拟机使用经验的人，可借此机会认识虚拟机。另外，虚拟机备份简单，对整个目录复制即可实现备份。

##### 3、在 Windows 中使用 WSL（Windows Subsystem for Linux）
WSL 是由微软 Windows 内核团队创建, 在 Windows 10 上开始发布，近几年才出现的，使用 Linux 的新选择。 WSL 通过在 Windows NT 内核上虚拟化一个 Linux 内核接口来执行 Linux ELF64 二进制文件。在 WSL 中是完全仿真的 Linux 文件系统；在 WSL 中可直接通过 /mnt/c、/mnt/d 等访问 Windows 的 C、D 等盘的文件内容。因为是内核支持，没有使用虚拟机技术，WSL 启动快速（启动时间不到一秒，第一次例外），执行程序时反应快捷，使用体验远远高于虚拟机和双系统。本人曾经使用过很长时间的双系统和虚拟机，对比之下，WSL 最值得推荐。

------
如果读者有在自己 Windows PC 上使用 Linux 的需求，选择 WSL（Windows Subsystem for Linux）可以少走很多不必要的弯路。

#### <b>WSL 使用方法 </b>
##### 成功安装 WSL 的前提 
1. 启用固件虚拟化功能: 可在 `cmd` 中运行命令`>Systeminfo.exe` ，查看结果中的 Hyper-v 项，如果含有“固件中已启用虚拟化: 是”则无需操作，否则在 BIOS 中启用固件虚拟化功能。
2. 启用 Windows 的子系统功能: 控制面板->程序和功能->启用或关闭Windows功能->勾选 适用于Linux的Windows子系统。
3. 重启电脑：如果前两项已是默认设置，此项省略。
 
##### 安装并使用 WSL 
1. 打开微软应用市场 Microsoft Store，搜索“WSL”，在搜索结果中选择感兴趣的 Linux 版本并安装。本人选择的 Ubuntu；使用命令行窗口安装 Linux 时:two:，Ubuntu 是默认系统。 
2. 安装完成后，在开始菜单里找到对应图标，点击图标启动你的 Linux 系统，首次启动需要等待文件解压并存储到电脑上，未来的所有启动时间应不到一秒。
3. 日常使用与常见的 Windows 程序无异。

>:two:<small> 管理员权限打开 `cmd` 执行 `>wsl --install` 命令。此操作非必须，建议去微软应用市场 Microsoft Store 安装 wsl。<small/>

###### <b>如果遇到报错，请见官方指导 <i>[WSL docs][wsl-docs]。</i></b>

###### <b>更多使用方法，请见官方指导 <i>[WSL command][wsl-command]。</i></b>

###### <b>Linux 用法可参考 <i>[B站][bilibili]</i> “Linux 入门” 课程。</b>



[wsl-docs]: https://docs.microsoft.com/zh-cn/windows/wsl/
[wsl-command]: https://docs.microsoft.com/zh-cn/windows/wsl/wsl-config
[bilibili]: https://www.bilibili.com

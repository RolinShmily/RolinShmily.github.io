---
title: 略知OBS | 开源视频录制与直播 (未完成)
categories:
  - - Software
    - OBS Studio
tags:
  - OBS Studio
  - FFmpeg
  - nvidia
  - H.264
  - 编码器
  - 视频封装格式
  - 推流
  - 比特率
  - 码率
  - 虚拟摄像机
cover: 'https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/20250721newstart/001.jpg'
abbrlink: bc4f008a
date: 2025-07-25 00:00:00
updated: 2025-07-25 00:00:00
---
# 前言与摘要
首先，OBS的功能是非常强大的，可以用于**直播推流**、**视频录制**、**即时回放**、**多机位画面切换**。另外其自带的**虚拟摄像机**可以将准备好的画面，作为伪装好的摄像头画面在通讯软件中输出。其次，OBS作为开源软件，具有庞大的插件社区和脚本数量，使用OBS丰富的插件可以实现非常多的功能，而编写脚本可以实现自定义功能。
本篇主要介绍OBS的下载、录制与直播设置、虚拟摄像头的使用案例、及时回放的设置、好用的插件教程。其中会涉及到诸如，什么是视频/音频编码器、码率是什么、什么是视频封装格式等基础问题的简要回答。
# 下载与手册
官网下载地址: https://obsproject.com/download ，选择对应系统和方式下载。
![obs-download](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/20250721newstart/PixPin_2025-07-25_11-57-38.jpg)
如果打不开，这里提供下载链接：
- Windows：[OBS-Studio-31.1.1-Windows-x64-Installer.exe](https://cdn-fastly.obsproject.com/downloads/OBS-Studio-31.1.1-Windows-x64-Installer.exe)
- MacOS：[obs-studio-31.1.1-macos-intel.dmg](https://cdn-fastly.obsproject.com/downloads/obs-studio-31.1.1-macos-intel.dmg)
- Linux：
	下载：`flatpak install flathub com.obsproject.Studio`
	运行：`flatpak run com.obsproject.Studio`
- 官方的帮助页面(全英)：[Knowledge Base](https://obsproject.com/kb/)
# 快速开始
这一部分主要是视频录制的快速实现。
![默认页面](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/20250721newstart/PixPin_2025-07-25_13-06-16.jpg)
1. 进入设置，点击左侧**视频**，设置**基础(画布)分辨率**为你想要录制的分辨率，默认推荐`1920×1080`；选择帧率，推荐为`30帧`或`60帧`。
![视频设置](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/20250721newstart/PixPin_2025-07-25_21-00-30.png)
2. 点击输出，选择输出模式为**高级**，点击录制选项：设置你的录像路径、选择录像格式为`MPEG-4(.mp4)`；选择音频编码器为`FFmpeg AAC`。
3. 选择视频编码器为`x264`或`QuickSync H.264`或`NVIDIA NVENC H.264`或`AMD HW H.264(AVC)`，如果存在多个，后两个更优，其次为第二个。
4. 将上述编码器的设置中，**比特率控制**分别对应设置为`CRF`、`CQP`、`恒定QP`、`恒定QP`，并将**值**设置为`20`。
![输出设置](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/20250721newstart/PixPin_2025-07-25_21-06-12.jpg)
5. 返回主页面，添加源，请选择**显示器采集**，随后自定义名称；然后选择你的显示器，确保画布中出现了显示器的画面；如果画布中显示不完全，请选择对应源右击，进行变换。
![添加显示器源](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/20250721newstart/PixPin_2025-07-25_20-49-02.jpg)
![拉伸到全屏](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/20250721newstart/Timeline%201_01_00_00_00.jpg)
至此，可以进行正常的录制屏幕了。
后面的详解配置将以此作为基础，进行优化和不同用法的介绍。
# 客户端的基础设置
# 有关录像的高级设置
# 插件分享

缓存清理测试
新的缓存测试
#嵌入式系统导论实验报告
##Lab5:安装ROS
###1. 介绍ROS
&emsp;&nbsp;ROS(Robot operation system) 是一套系统框架，底层提供硬件驱动，软件层面支持通用的文件格式。ROS提供一系列程序库和工具以帮助软件开发者创建机器人应用软件，提供了硬件抽象、设备驱动、函数库、可视化工具、消息传递和软件包管理等诸多功能。ROS遵循BSD开源许可协议。
###2.安装ROS过程  
 
&emsp;2.1 配置Ubuntu软件库，确保软件仓库允许"restricted", "universer"和"multiverse"这三种安装模式。  

&emsp;2.2 添加sourses.list,确保电脑能够按照来自packages.ros.org的软件包。

&emsp;2.3 添加keys密钥文件。  

&emsp;2.4 访问软件包源列表里的每一个网址，并读取软件列表，更新软件列表，以确保debian软件包索引是最新的。  

&emsp;2.5 ROS中有很多函数库和工具，安装桌面完整版，其中包含ROS、rqt、rviz、通用机器人函数库、2D/3D仿真器、导航以及2D/3D感知功能。  

&emsp;2.6 初始化rosdep,rosdep能在编译某些源码时为系统安装依赖库，同时也是某些ROS核心功能组件所必需用到的工具。  

&emsp;2.7 配置一个bashrc脚本以确保每次打开一个新的终端时ROS环境变量都能够自动配置好，以添加到bash会话中，使用source ~/.bashrc能够使个性化配置立即生效。  

&emsp;2.8 安装rosinstall,rosinstall是ROS中一个独立分开的常用命令行工具，方便用户通过一条命令给某个ROS软件包下载源码树。
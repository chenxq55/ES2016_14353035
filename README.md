#嵌入式实验报告
##
###DOL框架描述：
  DOL是一种实现并行化操作的软件发展框架。DOL以Kahn计算处理网络模型和SystemC语言为基础，使用XML格式来描述多核处理器并行化运算的实现。
###DOL安装笔记：
   1. 使用命令行下载所需要的安装包，包括ant, jdk, g++, unzip等
      - sudo apt-get update
      - sudo apt-get install ant (安装ant)
      - sudo apt-get install openjdk-7-jdk (安装jdk)
      - sudo apt-get install unzip (安装解压软件)
      - sudo apt-get install build-essential (安装必要的东西，包括g++)
   2. 解压DOL和SystemC
      - mkdir dol(生成目录)
      - unzip dol_ethz.zip -d dol (解压dol)
      - tar -zxvfsystemc-2.3.1.tgz (解压systemc)
   3. 编译SystemC
      - cd systemc-2.3.1 (进入目录)
      - mkdir objdir (生成目录)
      - cd objdir 
      - ../configure CXX=g++--disable-async-updates(能根据系统的环境设置参数，用于编译）[在执行这个步骤的时候遇到了无法编译C代码的问题，因此执行命令(sudo apt-get install build-essential)去获取所需要的包，编译成功后截图如下：![systemc](http://i.imgur.com/URLlMiI.png) 
      - sudo make install (编译)
      - pwd (记录当前的工作路径)![path](http://i.imgur.com/eg3xuCi.png)
   4. 编译DOL
      -  cd ../dol (进入dol文件夹，修改build_zip.xml文件，修改systemc的路径（上一张图所示）
      -  ant -f build_zip.xml all [用ant编译dol,编译成功后截图如下：![dol](http://i.imgur.com/xJFnu6d.png)
      -  cd build/bin/main
      -  ant -f runexample.xml -Dnumber=1[用ant编译样例runexample.xml，编译成后截图如下：![example](http://i.imgur.com/WmCvlFc.png)
      -  样例生成框架图如下：![frame](http://i.imgur.com/7SCbVsT.png)
###Experimental experience:
1. SystemC是一种软/硬件协同设计语言，一种系统级的建模语言，主要用于并行化的进程，特别是在SoC系统中。DOL是基于SystemC语言的一种系统框架，主要用于处理并行化系统，应用于多核系统。
2. make工具主要用于C语言的编译，ant工具主要用于java语言的编译，两者的性能相似，但ant工具应用范围更广，因为java语言是一种基于虚拟机的语言，可以跨平台、跨系统运行。
3. git是一款分布式版本控制系统，可以敏捷高效地处理任何大小项目，尤其是大型团队的开发项目，通过git可以同步更新团队成员的成果并对其进行整合，还可以进行版本控制，记录成员修改记录。
 

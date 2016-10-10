#嵌入式系统导论实验报告
##
###任务一：修改example2,让3个square模块变为2个
    解决方法：

1. 将example1.xml中的variable N 改为2
 ![changeN](http://i.imgur.com/RErERaG.png)
2. 在迭代器中减少次数
 - 减少平方模块迭代次数,如图：		
   ![square](http://i.imgur.com/CuJWTld.png)
 - 减少连线迭代次数，如图：
   ![sw_channel](http://i.imgur.com/GEQIPNw.png)
 - 减少连线连到平方模块和从平方模块连出到连线的迭代次数，如图：
   ![from_to_square](http://i.imgur.com/jedo8nD.png)
 - 将最后一条连线连到消费者模块，将其编号变小，如图：
   ![last](http://i.imgur.com/VAd8MGn.png)
3. 实验结果截图如下：
![two_result](http://i.imgur.com/3n1h5q1.png)
4. dol截图如下：
![two_dol](http://i.imgur.com/NSC83AR.png)

###任务二：修改example1,使其输出3次方数
    解决方法：
1. 将平方模块中输入和输出之间的 i x i 换成 i x i x i ,如图：
![change_i](http://i.imgur.com/2bDMTCd.png)
2. 实验结果截图如下：
![one_result](http://i.imgur.com/WItGOSw.png)
3. dol截图如下：
![one_dol](http://i.imgur.com/Qii2gjR.png)


###实验感想：
1. 这次的两个dol例子中，都有生产者模块，消费者模块，中间的处理模块（平方模块）和连线。
2. 在每个模块函数中都有一个初始化函数和一个运行函数，初始化函数只运行一次，而运行函数会重复运行，直到达到上限，一旦达到上限，则回收这个模块。
3. 每一个模块都有输入端口或输出端口，每个模块的端口编号不能重复，不同模块之间的端口编号可以重复。
4. 可以使用迭代的方法写会重复的代码，其模块命名可以相同，用append来对相同模块进行编号。
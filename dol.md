#Lab2 : DOL 实例分析 &编程
##
###实验内容：
1. 修改example2，让3个square模块变成2个, tips:修改xml的iterator
2. 修改example1，使其输出3次方数，tips:修改square.c
##
###实验结果
1.
![](http://p1.bpimg.com/567571/99d5c0beaf9845fc.png)
![](http://p1.bpimg.com/567571/dccfb554ab013080.png)
2.
![](http://p1.bpimg.com/567571/5c6b139cd04de565.png)
![](http://i1.piimg.com/567571/f4dde85ed8526e57.png)
##
###实验感想
比较轻松能完成实验，对于example2，先是定义了2个process，分别为generator和consumer，然后利用迭代去定义square和通道channel，再下面又利用迭代将square连接起来，最后将已经连接的square与generator和consumer连接在一起。对于任务要求只需不要迭代，手动传两个square，其余不变。example1只需将i*i修改为i*i*i即可。
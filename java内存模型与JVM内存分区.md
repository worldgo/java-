## java内存模型与JVM内存分区都是一种逻辑概念，物理上并不实际存在  
> java内存模型是一种逻辑规范，在此逻辑中分工作内存和主内存。这个规范最主要是为了解决可见性、有序性(通过禁止指令重排序)-volatile关键字的两个作用   
> 要解决共享对象可见性这个问题，我们可以使用java volatile关键字或者是加锁--**怎么加**  
> 对应Java程序员来说，理解happens-before是理解JMM的关键?

>https://www.jianshu.com/p/8a58d8335270     --文章来源 https://zhuanlan.zhihu.com/p/29881777、https://www.zhihu.com/column/EnjoyMoving  
>https://blog.csdn.net/alinshen/article/details/80521484    
>http://www.ifcoding.com/archives/289.html  
> https://blog.csdn.net/qq_41297896/article/details/89949632  
> https://mp.weixin.qq.com/s?__biz=MzU4NzA3MTc5Mg==&mid=2247484606&idx=1&sn=42212c0ac1c123ebee1903d07f88b6db&chksm=fdf0ece1ca8765f7e623d2a3d19ff637d8f2449db0dea2bb63d87e11f63b482cf16c0a007faf&token=2087444891&lang=zh_CN&scene=21#wechat_redirect  

> 内存模型的主内存 = JVM分区的堆内存、内存模型的工作区域 = JVM分区的私有线程栈  
> JMM是一种抽象的概念，并不实际存在，在逻辑上分工作内存和主内存，但在物理上二者都可能在主存中也可能在Cache或者寄存器中。Java内存分区也是这个道理。   

**深入学习java虚拟机**





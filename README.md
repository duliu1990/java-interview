# java-interview
Java Basic Interview Summary

## 堆栈信息
堆 存放对象的内容信息
栈 存放对象的地址信息



## JAVA  JDK 基础

### JVM

JVM java虚拟机，是java程序在不同的平台运行的基础。





堆：



线程私有：

1. 程序计数器
2. 虚拟机栈
3. 本地方法栈

线程共有：

1. 堆
2. 方法区
3. 直接内存



#### 类加载机制

1. 类加载器

   启动类加载器

   扩展类加载器

   应用程序类加载器



### Java 源码相关

1. StringBuffer 与 StringBuilder

   StringBuffer @Since JDk1.0 

   StringBuilder @Since JDK 1.5 在多线程中是不安全的，出现的原因在于StringBuffer是线程安全的，在单一线程中使用StringBuilder是更加快的。

   二者操作的方法几乎相似

2. Throwable, Error, Exception

   Throwable @Since JDK 1.0

   Exception @Since JDK 1.0 继承 Throwable 程序本身异常，因为一些不确定因素导致程序在运行时会出现的异常。

   Error @Since JDK 1.0 继承 Throwable JVM 无法处理的错误，

3. BIO, NIO, AIO

   Blocking I/O (BIO) 传统I/O模式， 同步阻塞I/O模式

   New I/O (NIO) @JDK1.4 引入的新的I/O， 同步非阻塞的I/O模型

    Asynchronous I/O (AIO) 异步I/O

4. List

   ArrayList: @Since JDK 1.2 非线程安全 基于数组实现

   LinkedList：@Since JDK 1.2  非线程安全 基于双端链表实现

5. Map

   HashMap: @Since JDK 1.2 非线程安全 基于数组和链表 也就是链表散列 ConcurrentHashMap线程安全的，支持key值为 null, 在JDK 1.8 以后 当阀值大于8时改用红黑树，减少搜索时间。

   HashTable 线程安全 不支持key值为null

6. Set

   HashSet 基于HashMap

   TreeSet 基于 红黑叔结构

7. 





### 多线程





## 锁

1. 乐观锁和悲观锁

   乐观锁： 总是假设好的情况，在每次拿取数据的时候认为不会修改。适合与读操作较高的情况。

   ​	compare and swap (CAS) 算法，通过以比较的形式，来验证是否修改，例如在数据库中用到的version字段。

   悲观锁： 总是假设悲观的情况，在每次拿取数据的时候认为会修改。适合与写操作较高的情况。

   ​	在传统数据库中的表的行锁，读锁，写锁等，在java中synchronized。

   乐观锁存在的问题：

   	1. ABA现象，当字段的值与更新值一样，但是在过程中发生了 A-> B -> A 的过程，容易造成忽略的情况。
    	2. 对比循环开销的时间大
    	3. 只能保证共享变量的原子操作

   悲观锁饿问题：

   1. 比较的笨重
   2. 容易造成死锁

2. 



## 数据库

事务：一组操作。

事务的特性：原子性，一致性，隔离性，持久性
















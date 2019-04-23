# Java高并发编程

#### 1.同一个资源，同步和非同步的方法可以同时调用  
#### 2.对业务写代码进行加锁，对读代码不进行加锁，会产生脏读  
#### 3.同线程内一个同步方法可以去调用另一个同步方法（重入锁 还有一种重入锁就是子类调用父类的同步方法）  
#### 4.模拟一个简单的死锁  
#### 5.如果执行同步方法中出现异常，那么就会自动释放锁，如果不想释放锁，加上try/catch  
#### 6.volatile关键字（无锁同步）  
#### 7.voliatile 不能保证原子性 不能替换synchronized  
#### 8.多个原子类的方法之间不具备原子性  
#### 9.原子类的不具备可见性  
#### 10.锁是锁在堆内存的那个对象上，而不是引用  
#### 11.不要锁字符串常量  
#### 12.wait 让线程暂停，释放锁， notify 唤醒线程，不释放锁  
#### 13.ReentrantLock的简单使用  
Reentrant n.再进入  
ReentrantLock 一个可重入互斥Lock具有与使用synchronized方法和语句访问的隐式监视锁相同的基本行为和语义，但具有扩展功能   
可以完成synchronized相同的作用，但必须手动释放锁   
#### 14.ReentrantLock对synchronized的扩展之tryLock()   
#### 15.ReentranLock对synchronized的扩展：可以被另外的线程打断    
#### 16.ReentrantLock对synchronized的扩展：可以指定公平锁    
#### 17.使用wait和notifyAll实现消费者生产者模式    
#### 18.使用Condition 完成生产者消费者模式
#### 19.同步容器类

1：Vector Hashtable ：早期使用synchronized实现   
2：ArrayList HashSet ：未考虑多线程安全（未实现同步）  
3：HashSet vs Hashtable StringBuilder vs StringBuffer  
4：Collections.synchronized***工厂方法使用的也是synchronized  

使用早期的同步容器以及Collections.synchronized***方法的不足之处，请阅读：
http://blog.csdn.net/itm_hadf/article/details/7506529

使用新的并发容器
http://xuganggogo.iteye.com/blog/321630
#### 20.集合映射总结
1：对于map/set的选择使用   
HashMap  
TreeMap  
LinkedHashMap  

Hashtable  
Collections.sychronizedXXX  

ConcurrentHashMap  
ConcurrentSkipListMap   

2：队列  
ArrayList  
LinkedList  
Collections.synchronizedXXX  
CopyOnWriteList  
Queue  
 &ensp; CocurrentLinkedQueue //concurrentArrayQueue   
 &ensp; BlockingQueue  
	&emsp;	LinkedBQ  
	&emsp;	ArrayBQ  
	&emsp;	TransferQueue  
	&emsp;	SynchronusQueue  
 &ensp;	DelayQueue执行定时任务  
#### 21.线程池
Executor  
ExecutorService submit  
Callable = Runnable  
Executors   
ThreadPool  
Future  
  
fixed cached single scheduled workstealing forkjoin  
  
ThreadpoolExecutor  
  
PStreamAPI  

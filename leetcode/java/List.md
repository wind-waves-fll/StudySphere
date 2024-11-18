ArrayList:

1) 可以存储null
2) 是由数组来实现数据存储
3) 基本等同于Vector,线程不安全的，在多线程情况下，不建议使用

ArrayList底层源码分析：

1. 底层维护了一个Object类型的数组elementData
2. 当创建ArrayList对象时，如果使用的是无参构造器，初始化elementData的容量为0，第一次添加，则扩容elementData为10，如需要再次扩容，则扩容elementData为1.5倍
3. 如果使用指定大小的构造器，则初始化elementData容量为指定大小，如需要再次扩容，则扩容elementData为1.5倍

```
transient Object[] elementData; // non-private to simplify nested class access
transient 表示瞬间，短暂的，表示该属性不会被序列化 

elementData = Arrays.copyOf(elementData, newCapacity);
```

Vector:

1) public class Vector<E> implements List<E>,java.io.Serializable
2) Vector底层也是一个对象数组，protected Object[] elementData;

3. Vector是线程同步的，即线程安全，Vector类的操作方法带有synchronized
4. 在开发中，需要线程安全时，考虑使用Vector

LinkedList:

1. 底层实现了双向链表和双端队列特点
2. 可以添加任意元素，包括null
3. 线程不安全，没有实现线程同步

LinkedList底层机制：

1. 底层维护了一个双向链表
2. 维护了两个属性first和last分别指向首节点和尾节点
3. 每个节点(Node对象)，里面又维护了prev,next,item三个属性
4. 添加删除效率较高

<img src="D:\fanlulin\Desktop\StudySphere\leetcode\java\assert\List\image-20241112143350642.png" alt="image-20241112143350642" style="zoom: 67%;" />


















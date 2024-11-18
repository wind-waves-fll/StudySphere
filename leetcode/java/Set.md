Set:

1. 无序
2. 不允许有重复的元素，所以最多包含一个null
3. JDK中Set接口的实现类有：

![image-20241112143944427](D:\fanlulin\Desktop\StudySphere\leetcode\java\assert\Set\image-20241112143944427.png)



HashSet:

1. HashSet实现了Set接口
2. HashSet实际上是HashMap

```
public HashSet() {
    map = new HashMap<>();
}
```

1. 可以存放null
2. HashSet不保证元素是有序的，取决于hash后，在确定索引的位置
3. 不能有重复的元素

LinkedHashSet:

1. LinkedHashSet 是HashSet的子类
2. LinkedHashSet底层是一个LinkedHashMap,底层维护了一个数组+双向链表
3. LinkedHashSet根据元素的hashCode值来决定元素的存储位置，同时使用链表维护元素的次序，这使得元素看起来是以插入顺序保存的
4. LinkedHashSet不允许添重复元素
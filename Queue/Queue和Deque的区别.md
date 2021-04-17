## [Queue和Deque的区别](https://my.oschina.net/u/4168855/blog/4916288)

Queue是队列，Deque是双端队列

<br/>

![队列与双端队列.png](https://i.loli.net/2021/04/17/eOmAzx5Y8kbhSWH.png)

add会抛出NullPointException异常，而offer会返回null。

### 队列
> 队列(queue)是一种常用的数据结构，可以将队列看做是一种特殊的线性表，该结构遵循的先进先出原则。Java中，LinkedList实现了Queue接口,因为LinkedList进行插入、删除操作效率较高

相关常用方法：
```java
// 向队尾添加，成功返回true, 如果超出容量限制，抛出异常
boolean add(E e);
// 向队尾添加，成功返回true, 如果超出容量限制，返回false
boolean offer(E e);
// 删除并获取队首元素，成功返回true，如果队列为空，抛出异常
E remove();
// 删除并获取队首元素，成功返回true，如果队列为空，返回false
E poll();
// 获取队首元素，成功返回true，如果队列为空，抛出异常
E element();
// 获取队首元素，成功返回true，如果队列为空，返回false
E peek();
```

### 双向队列
> (Deque),是Queue的一个子接口，双向队列是指该队列两端的元素既能入队(offer)也能出队(poll),如果将Deque限制为只能从一端入队和出队，则可实现栈的数据结构。对于栈而言，有入栈(push)和出栈(pop)，遵循先进后出原则

**Deque继承了Queue，除了继承了Queue的接口，又对每种方法额外添加了first与last方法用以实现操作双端队列。**

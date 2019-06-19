# Data-structure-and-algorithm
记录数据结构和算法的学习

**数据结构**
* 计算机中存储和组织数据的方式叫做数据结构
* 常见的数据结构：数组、图、树、堆、栈、链表，每一种数据结构都有不同的应用场景
* 二分查找的效率比线性查找高很多
* 图书馆摆放图书demo
    * 新书怎么摆
    * 如何快速的把某一本书取出来

**算法的概念**
* 有限指令集，不依赖于语言
* 做某一件事情的方法、步骤、逻辑
* demo
    * 找电缆问题
    * 快递员送快速

**数组**
* 数组的插入、扩容和删除效率非常低
* 数组查找和修改元素效率非常高，因为采用的是通过下标进行操作
* 链表的查找和修改元素效率非常低，因为采用的是线性查找
* 链表不需要扩容，会自动扩容，插入和删除效率也非常高

**栈**
* 栈结构-基于数组实现，数组是一个(线性结构)
* 栈、队列都是一种受限的线性结构(受限：仅仅只有一端可供操作)
* 特点：LIFO(后进先出)
* demo
    * 餐厅托盘
    * 邮箱
    * 函数调用栈-函数之间相互依赖和嵌套导致的
    * 递归-有时候会导致栈溢出，因为递归是自己调用自己，如果始终不释放，最终导致栈溢出

**队列**
* 先进先出
* FIFO
* 有两端
* 常见的队列操作有
	* 出队，dequeue，删除队列的第一个元素，并返回改元素
	* 入队，enqueue
	* 获取队列的第一个元素，front，不删除改元素
	* 判断队列是否为空，isEmpty
	* 获取队列的大小，size

**优先级队列**
* 在插入一个元素的时候会考虑该数据的优先级
* demo
    * 登机顺序
    * 急诊科
    * 线程处理任务的重要性

**链表**
* 链表和数组的实现机制完全不同
* 链表中的元素在内存中可以不连续
* 当当前数组不能满足需求时，需要申请扩容，而扩容是非常消耗性能的
* 链表中的每一个节点由一个存储元素本身的节点和指向下一个元素的引用组成
* 默认有一个head属性，值为null
* 优点
    * 可以充分利用计算机的内存，实现内存的动态管理
    * 不必再创建时指定大小，并且可以无限的延伸下去
    * 在插入和删除时，时间复杂度可以达到O(1)，相对数组效率很高
* 缺点
    * 链表访问任何一个位置的元素都需要从头开始访问，无法跳过第一个元素访问其他任何元素
    * 不能通过下标进行访问
* demo
    * 链表类似于火车：有一个火车头，火车头会连接一个节点，节点上有乘客(类似于数据)，并且这个节点会连接到下一个节点，以此类推
*链表分类*
* 一种是单向链表一种是双向链表
* 链表本身就是一种可以替代数组的结构

**单向链表常见方法**
* append，在链表的末尾追加一个节点
* toString
* insert(position,data)
* get(position) //获取指定位置的节点
* indexOf(element) //返回元素在链表中的索引，找不到就返回-1
* update(position, element) //修改某一个位置的元素
* removeAt(position) // 移除指定位置的元素
* remove(data) //删除指定项
* isEmpty() // 判断链表是否为空
* size() //获取链表的长度

**单向链表的特点**
* 只能从头遍历到尾或者从尾遍历到头(一般是前者)
* 链表相连的过程是单向的
* 实现的原理是上一个链表中有指向下一个的引用

**单向链表的缺点**
* 到达下一个节点很容易，但是回到上一个节点很难
* demo
    * 文本编辑器，比如每一行数据用一个String对象存储在链表的一个节点中，随着光标的上下移动，需要不断进行上下节点之间的切换

**双向链表**
* 既可以从头遍历到尾又可以从尾遍历到头
* 链表的相连过程是双向的
* 一个节点既有一个向前连接的引用，也有一个向后连接的引用

**双向链表的缺点**
* 每次在处理插入和删除操作时，需要同时操作四个引用，比较麻烦
* 相对于单向链表，双向链表占用的内存空间更大一些

**双向链表的特点**
* 用一个head和一个tail分别指向头部和尾部的节点
* 每一个节点由三部分组成：前一个节点的指针prev、保存的数据、后一个节点的指针next
* 双向链表的第一个节点的prev是null
* 双向链表的最后一个节点的next是null

**双向链表的常见操作**
* append // 在末尾插入一项
* insert(position, element) // 在指定位置插入一项
* toString()
    * forwardString()
    * backwardString()
* insert(position, data)
* get(position) // 根据位置获取元素
* indexOf(data) // 找出指定数据的索引
* update(position, element) // 修改某个位置的元素为element
* removeAt(position) // 删除指定位置元素
* remove(data)
* isEmpty()
* size()
* getHead() // 获取链表的第一个元素
* getTail() // 获取链表的最后一个元素

**集合**
* 无序、不重复
* 实现方式是哈希表
* 常见操作
    * add(value) // 向集合添加一个新的项
    * remove(value)
    * has(value)
    * clear()
    * values() // 获取所有的属性
    * size

**集合间操作**
* 并集
    * 对于给定的两个集合，返回一个新集合，这个新的集合包含了两个集合的所有元素
* 交集
    * 对于给定的两个集合，返回一个新集合，这个新的集合包含了两个集合的共有元素
* 子集
    * 验证一个集合是否是另一个集合的子集
* 差集
    * 对于给定的两个集合，返回一个新的集合，这个新的集合中的元素只存在于一个集合中而不存在于另一个集合中

**字典**
* 实现方式-哈希表
* 存的是键值对
* 特点
    * 键值一一对应
    * 键不可以重复
    * 值可以重复
    * 有些语言中把字典也称为映射(比如Java)
    * 键是无序的
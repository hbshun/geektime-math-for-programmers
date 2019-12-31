### 算法复杂度
- 时间
- 空间
### 复杂度的计算
- 平行的两个使用加法
- 嵌套使用乘法
- 只需要计算最高量级代码的复杂度
- 排列组合
- 画图-----图论
-  在给定的计算量下，通常时间复杂度和空间复杂度呈现数学中的反比关系。这就说明，如果我们没法降低整体的计算量，那么也许可以通过增加空间复杂度来达到降低时间复杂度的目的，或者反之，通过增加时间复杂度来降低空间复杂度。

### 双向广度优先搜索的时间和空间复杂度

在没有缓存系统的时候，每次请求都要服务器来处理，因此时间复杂度比较高。如果使用了缓存系统，那么我们会消耗更多的内存空间，但是降低了请求相应的时间

### 复习部分常用算法的 与其时间复杂度计算
- 二分法搜索 O(log n) 对数阶 
- 求最大值  O（n）
- 快速排序算法  O(nlog n);   --------实现快速排序算法
- 选择排序 冒泡排序 o(n^2)   ----------- 
- 立方阶
- 指数阶
- 阶乘阶
------------
### chapter17
##### 案例分析（效率）
> 广度优先搜索
  ##### 单向
  - 判断边界条件
  - 生成空的队列，常量级内存操作
  - 把搜索的起始点放入队列  和 已访问的hash点集合
  - while 和for两个循环，分析while和for的复杂度    m*m + m*mM ......m*l
  ##### 双向
  - 走n条      复杂度     O(m^1/2)
  - 判断一个点是否是 两侧的交集  复杂度 O(n);

  ### 双向搜索两侧的节点数量的差距会影响，复杂度的大小
> 全文搜索
  - 全文有n个字符串   关键词m， 搜索的读咋读  o(n*m)
  - 全文作为一个字符串氛围 n 个有意义的字符， o(n*m)
  - 倒排索引 为每篇文章贴上标签，占用一定的空间，牺牲空间来提高搜索的时间复杂度




  ### 18 数据结构、编程语句和基础算法体现了哪些数学思想
  
  ##### 数组
  - 常常和循环语句相结合，来实现迭代法，例如二分查找、斐波那契数列等等。不过，数组只对稠密的数列更有效。如果数列非常稀疏，那么很多数组的元素就是无效值，浪费了存储空间。此外，数组中元素的插入和删除也比较麻烦，需要进行数据的批量移动。

  ##### 链表
  - 链表中的结点存储了数据，而链表结点之间的相连关系，在 C 和 C++ 语言中是通过指针来实现的，而在 Java 语言中是通过对象引用来实现的。
  - 链地址哈希表 数组中的每一个元素都是一个链表的头部。随后，我们就可以根据哈希函数算出的哈希值（也叫哈希的 key），找到数组的某个元素及对应的链表，然后把数据添加到这个链表中。
  - 链地址哈希表 解决了 哈希冲突每个元素对应了一个链表，那么当发生冲突的时候，我们就可以把多个数据添加到同一个链表中
  ##### 栈
  - 先进后出 可以实现基于递归的编程， 由于栈可以避免过多的中间变量，它可以节省内存空间的使用。

  ##### 队列
  - 先进先出，队列模拟了日常生活中人们排队的现象


  ##### SQL 语言中的 Join 操作
  - 内连接（inner join）：假设被连接的两张数据表分别是左表和右表，那么内连接查询能将左表和右表中能关联起来的数据连接后返回，返回的结果就是两个表中所有相匹配的数据。如果认为左表是集合 A，右表是集合 B，那么从集合的角度来说，内连接产生的结果是 A、B 两个集合的交集。
  - 外连接（outer join）：外连接可以保留左表，右表或全部表。根据这些行为的不同，可分为左外连接、右外连接和全连接。无论哪一种，都是对应于不同的集合操作。

  ##### 算法
  - 介绍分治思想的时候，我谈及了 MapReduce 的数据切分
  - 轮询或者源地址哈希算法
  - 字符串匹配的算
  - 迭代法
  - RK 算法可以根据两个字符串哈希后的值。来判断它们是不是相同
  - 动态规划
  - 回溯


  ##### 需要抽空对比总结下。。。。。

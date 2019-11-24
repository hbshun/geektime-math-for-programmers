# 14 | 树的广度优先搜索（下）：为什么双向广度优先搜索的效率更高？

## 如何更高效地求两个用户间的最短路径？

双向广度优先搜索可能是一种方案。

如何判断给定的两个用户之间关系多紧密？最直接的就是这俩人是几度好友来衡量。

计算他们是几度好友可以用广度优先算法，先把 a 的好友遍历，然后看 b 在不在，但是数据量很大，因为要把 a 的好友的好友的好友的...遍历出来。

可以使用一种双向广度优先搜索的方法来进行优化。就是两个人都找自己的好友，然后进行交集运算查找是否有共同好友，没有继续进行一层，然后在匹配直到匹配结束。

### 其他应用：嵌套型聚合

聚合是数据分析中一个很常见的操作，它会根据一定的条件把记录聚集成不同的分组，以便我们统计每个分组里的信息。目前，SQL 语言中的 GROUP BY 语句，Python 和 Spark 语言中 data frame 的 groupby 函数，Solr 的 facet 查询和 Elasticsearch 的 aggregation 查询，都可以实现聚合的功能。

在这个过程中有很多优化的思路。对于只需要返回前若干结果的应用场景，我们可以对图中树状结构进行剪枝，比如只需要返回前 100 个参与项目最多的用户，就先找出来高度为 1 的结点然后根据项目数量排序取出前 100。

重点是控制结点数量，只取比较相关的结点，避免无用的内存和运算消耗。

## 思考题

Q：在什么情况下，单向广度优先更高效？如何优化双向广度优先？
A：在两边好友数量差距很大的时候，单向广度优先更高效，比如一边有 100 个好友，另一边有 2 个好友，单向用两个好友的人进行遍历然后对比前面那个人是否在里面来确定关联。

这种情况下，可以先判断数量，然后优先用数量少的人来做遍历。其次就是要控制层级，不然计算量会很大，看了下 LinkedIn 发现都是有条件的搜索，然后一般是 2nd 最多 3rd 了，然后还带分页。要么就是依靠公司的前置条件来运算，要么就是关联推荐。里面估计有很多优化算法和方案。

> 来自评论：还有一个前提条件是确定两个被搜索结点必须是连通的，不然两边都搜到底了，发现没有，不如就搜一边搜到底。
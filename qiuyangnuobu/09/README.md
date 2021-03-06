## 动态规划（上）：如何实现基于编辑距离的查询推荐？

### 动态规划（Dynamic Programming）
查询推荐（Query Suggestion）的实现过程所应用的数学思想是 动态规划

动态规划需要通过子问题的最优解，推导出最终问题的最优解，因此这种方法特别注重子问题之间的转移关系。我们通常把这些子问题之间的转移称为状态转移，并把用于刻画这些状态转移的表达式称为状态转移方程。很显然，找到合适的状态转移方程，是动态规划的关键。

### 编辑距离（Edit Distance）
查询推荐的核心思想其实就是，对于用户的输入，查找相似的关键词并进行返回。而测量拉丁文的文本相似度，最常用的指标是编辑距离
由一个字符串转成另一个字符串所需的最少编辑操作次数，我们就叫作编辑距离 也称为 莱文斯坦距离（Levenshtein distance）
很显然，编辑距离越小，说明这两个字符串越相似，可以互相作为查询推荐。编辑操作有这三种：把一个字符替换成另一个字符；插入一个字符；删除一个字符。

### 状态转移
给定任意两个非常复杂的字符串，如何高效地计算出它们之间的编辑距离

三种操作： 插入、删除、编辑

取上述三种情况中编辑距离的最小值作为当前的编辑距离，这里我们只需要保留这个最小的值，而舍弃其他更大的值

编辑距离是具有对称性的，也就是说从字符串 A 到 B 的编辑距离，和从字符串 B 到 A 的编辑距离，两者一定是相等的

从字符串 A 演变到 B 的每一种操作，都可以转换为从字符串 B 演变到 A 的某一种操作
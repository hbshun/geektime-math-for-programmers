# 向量空间模型
### 向量空间
- 用于描述一个点在空间中的位置信息比如 x=[x1, x2, x3 ...... xn]
####  向量的长度
- 是向量所对应的点到空间原点的距离。通常我们使用欧氏距离来表示向量的长度。
- 范数”的概念。范数满足非负性、齐次性、和三角不等式。你可以不用深究这三点的含义，不过你需要知道范数常常被用来衡量某个向量空间中向量的大小或者长度。
#### 向量之间的距离
- 可以把一个向量想象为 n 维空间中的一个点。而向量空间中两个向量的距离，就是这两个向量所对应的点之间的距离
- 曼哈顿距离指的是你在曼哈顿从一个地方到达另一个地方的距离，当然不是直线距离，期间会绕着各种恶扬的障碍物、建筑。按平面来计算从A(x1, x2)到B(y1, y2)的距离就是md(A,B) = |x1 - y1| + |x2 - y2|
- 欧氏距离 点与点间的直线距离，可以用向量间的平房和的平方根表示
#### 向量之间的夹脚
- 夹角余弦的取值范围在[-1,1]，当两个向量的方向重合时夹角余弦取最大值 1，当两个向量的方向完全相反夹角余弦取最小值 -1。值越大，说明夹角越小，两点相距就越近；值越小，说明夹角越大，两点相距就越远。而且越大表示越相似，所以可以直接作为相似度的取值。

- cosθ=向量a×向量b/|向量a|×|向量b| 涉及到向量的乘法  向量的模
### 总结
-  为了让计算机理解现实世界中的事物，我们会把事物的特点转换成为数据，并使用多维度的特征来表示某个具体的对象。多个维度的特征很容易构成向量，因此我们就可以充分利用向量和向量空间，来刻画事物以及它们之间的关系。我们可以在向量空间中定义多种类型的向量长度和向量间距离，用于衡量向量之间的差异或者说相似程度。此外，夹角余弦也是常用的相似度衡量指标。和距离相比，夹角余弦的取值已经控制在[-1, 1]的范围内，不会因为异常点所产生的过大距离而受到干扰。向量空间模型充分利用了空间中向量的距离和夹角特性，来描述文档和查询之间的相似程度，或者说相关性。虽然向量空间模型来自信息检索领域，但是也被用广泛运用在机器学习领域中。在接下来的文章里，我会结合具体的案例，分别来说说如何在这些领域使用向量空间模型。思考题

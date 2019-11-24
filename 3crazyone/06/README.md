# 06 | 递归（下）：分而治之，从归并排序到 MapReduce

### notes

_归并排序_ 「归并」，也就是把两个有序的数列合并起来，形成一个更大的有序数列

_分尔治之_ 将一个复杂问题，分解成两个甚至多个规模相同或者类似的子问题，
然后对这些子问题再进一步细分，到最后子问题变得很简单，容易求解，这样这个复杂问题就求解出来了

### 应用

大数据集的多机器分配处理，处理完后进行合并
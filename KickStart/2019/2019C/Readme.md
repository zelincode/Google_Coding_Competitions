# 2019 Round C

-   Score : 100
-   Rank : 35

---

## A

- 每个点维护上下左右第一个没走过的点
- map+并查集维护这个东西
- 分行列考虑并查集的合并与上下左右第一个未达点的维护

## B

- 不知道$O(RC^2)$能不能过, 所以写了$O(RC\log C)$的算法
- 对于矩阵内的每个点, 利用ST+二分处理出向右最远能到哪里
- 枚举每一列, 转化为一维问题, 本质上是直方图最大面积
- 单调栈做这个事情即可
- 后来发现这题本质上是$O(RC)$的，原因在于ST+二分可以用双指针+端点单调RMQ优化到线性

## C

- 考虑一种颜色的衣服只会出门一次
- 我们把每种颜色的狗离散化成一个前缀, 看成一个物品
- 相当于每一类物品最多取一个的背包
- 额外考虑一维$0/1$表示是否返回原地即可

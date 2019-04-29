# 计算上的考虑

| 原文   | [The Elements of Statistical Learning](../book/The Elements of Statistical Learning.pdf#page=474) |
| ---- | ---------------------------------------- |
| 翻译   | szcf-weiya                               |
| 时间   | 2018-08-09                   |
|状态 |Done|


当有 $N$ 个训练情形，$p$ 个预测变量，以及 $m$ 个支持向量时，并假设 $m\approx N$，支持向量机需要 $m^3+mN+mpN$ 次操作。尽管存在计算上的捷径 (Platt, 1999)，但他们不能很好地随着 $N$ 缩放。因为他们更新很快，读者应该在网上搜索最新的技巧。

LDA 需要 $Np^2+p^3$ 次操作，PDA 也一样。FDA 的复杂度取决于使用的回归方法。许多技巧关于 $N$ 是线性的，比如可加模型和 MARS。一般的样条和基于核的回归方法一般需要 $N^3$ 次操作。

R 中的包 `mda` 可以用来拟合 FDA，PDA 和 MDA 模型，S-PLUS 中也有软件包。


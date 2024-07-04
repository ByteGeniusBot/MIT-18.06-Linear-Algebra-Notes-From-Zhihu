# 第15讲 子空间投影

Projections onto subspaces

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AJLJU)

- **投影（射影）Projections**

![](https://pic1.zhimg.com/v2-ceccf98f3c8151a48bfc32d133345ae4_b.jpg)

投影问题的几何解释就是：如何在向量**a**的方向上寻找与向量**b**距离最近的一点。从图中可以看出，这个距离最近的点**p**就位于穿过**b**点并与向量**a**正交的直线与向量**a**所在直线的交点上。这就是**b**在**a**上的投影。如果我们将向量**p**视为**b**的一种近似，则长度**e**=**b**-**p**就是这一近似的误差。

因为 **p** 在向量 **a** 的方向上，因此可以令 **p** = x **a**，而因为它和 **e** 正交，我们可以得到方程：

$$
\boldsymbol{a}^T (\boldsymbol{b} - x \boldsymbol{a}) = 0
$$

解得：x = $\frac{{\boldsymbol{a}^T \boldsymbol{b}}}{{\boldsymbol{a}^T \boldsymbol{a}}}$ ，**p** = $x \boldsymbol{a} = \boldsymbol{a} \frac{{\boldsymbol{a}^T \boldsymbol{b}}}{{\boldsymbol{a}^T \boldsymbol{a}}}$ 。


如果**b**变为原来的2倍，则**p**也变为原来的2倍。而如果**a**变为原来的2倍，**p**不发生变化。从几何上和计算中都会得到验证。

> 本单元前半部分的核心内容就是射影。上一单元我们最核心的内容是认识消元法对于线性方程组的意义，并用矩阵的数学语言实现了消元过程，在那里最核心的策略就是利用矩阵乘法中的行操作来实现这一过程。这里面临类似的情况，我们有一个明确的几何目标，要将向量投影到已知子空间，而这里的策略就是误差向量和已知子空间正交，即两者求点积为0。

- **投影矩阵 Projections matrix**

我们将投影问题用投影矩阵的方式进行描述，即为 **p** = **P** **b**，其中 **P** 为投影矩阵。

**p** = $x \boldsymbol{a} = \boldsymbol{a} \frac{{\boldsymbol{a}^T \boldsymbol{b}}}{{\boldsymbol{a}^T \boldsymbol{a}}}$。则有 **P** = $\frac{{\boldsymbol{a} \boldsymbol{a}^T}}{{\boldsymbol{a}^T \boldsymbol{a}}}$，其分子 $\boldsymbol{a} \boldsymbol{a}^T$ 是一个矩阵，而分母 $\boldsymbol{a}^T \boldsymbol{a}$ 是一个数。

观察这个矩阵可知，矩阵 **P** 的列空间就是向量 **a** 所在的直线，矩阵的秩是 1。投影矩阵 **P** 是一个对称矩阵。另一方面，如果做两次投影则有 $\boldsymbol{P}^2 \boldsymbol{b} = \boldsymbol{P} \boldsymbol{b}$，这是因为第二次投影还在原来的位置。因此矩阵 **P** 有如下性质： $\boldsymbol{P}^2 = \boldsymbol{P}$， $\boldsymbol{P}^T = \boldsymbol{P}$。

- **为什么要投影 Why Project**

如前所述，方程 **A** **x** = **b** 有可能无解，我们需要得到方程的“最优解”。这里的问题在于向量 **A** **x** 一定在矩阵 **A** 的列空间之内，但是 **b** 不一定，因此我们希望将 **b** 投影到 **A** 的列空间得到 **p**，将问题转化为求解 $\boldsymbol{A} \hat{\boldsymbol{x}} = \boldsymbol{p}$。

- **在高维投影 Projection in higher dimensions**
-
在**R**³空间内，如何将向量**b**投影到它距离平面最近的一点**p**？

![Projection](https://pic2.zhimg.com/v2-e1498d1411c5a8df5088d24dad5e8b4d_b.jpg)

如果**a**₁和**a**₂构成了平面的一组基，则平面就是矩阵**A** = [**a**₁ **a**₂] 的列空间。

已知向量**p**在平面内，则有**p** = ${\hat x_1}{\boldsymbol{a}_1} + {\hat x_2}{\boldsymbol{a}_2} = \boldsymbol{A}\boldsymbol{\hat x}$ 。而 $\boldsymbol{e} =\boldsymbol{b}- \boldsymbol{p} = \boldsymbol{b} - \boldsymbol{A}\boldsymbol{\hat x}$ 与投影平面正交（*重点*），因此**e**与**a**₁和**a**₂均正交，因此可以得到： $\boldsymbol{a}_1^T(\boldsymbol{b} - \boldsymbol{A}\boldsymbol{\hat x})=0$并且 $\boldsymbol{a}_2^T(\boldsymbol{b} - \boldsymbol{A}\boldsymbol{\hat x})=0$ 。因为**a**₁和**a**₂分别为矩阵**A**的列向量，即$\boldsymbol{a}_1^T$和$\boldsymbol{a}_2^T$为矩阵$\boldsymbol{A}^T$的行向量，所以将两个方程式写成矩阵形式即为$\boldsymbol{A}^T(\boldsymbol{b} - \boldsymbol{A}\boldsymbol{\hat x})=0$。这与一维投影的方程形式相同。

向量$\boldsymbol{e}= \boldsymbol{b} - \boldsymbol{A}\boldsymbol{\hat x}$ 存在于矩阵$\boldsymbol{A}^T$的零空间N($\boldsymbol{A}^T$)里，从上一讲讨论子空间的正交性可知，向量**e**与矩阵**A**的列空间正交，这也正是方程的意义。

将方程$\boldsymbol{A}^T(\boldsymbol{b} - \boldsymbol{A}\boldsymbol{\hat x})=0$改写，可得$\boldsymbol{A}^T\boldsymbol{A}\boldsymbol{\hat x}=\boldsymbol{A}^T\boldsymbol{b}$。两侧左乘$(\boldsymbol{A}^T\boldsymbol{A})^{-1}$，得到：

$$
\boldsymbol{\hat x}=(\boldsymbol{A}^T\boldsymbol{A})^{-1}\boldsymbol{A}^T\boldsymbol{b}
$$

$$
\boldsymbol{p}=\boldsymbol{A}\boldsymbol{\hat x}=\boldsymbol{A}(\boldsymbol{A}^T\boldsymbol{A})^{-1}\boldsymbol{A}^T\boldsymbol{b}
$$

$$
\boldsymbol{P}=\boldsymbol{A}(\boldsymbol{A}^T\boldsymbol{A})^{-1}\boldsymbol{A}^T
$$

因为矩阵**A**不是方阵，无法简单的用$(\boldsymbol{A}^T\boldsymbol{A})^{-1}=\boldsymbol{A}^{-1}(\boldsymbol{A}^T)^{-1}$ 对投影矩阵公式进行化简。若**A**是可逆方阵，则化简得到**P** = **I**。此时**A**的列空间就是整个**R**ⁿ空间，**b**到这个空间的投影就是其本身，投影矩阵等于单位阵。

对 $\boldsymbol{P}=\boldsymbol{A}(\boldsymbol{A}^T\boldsymbol{A})^{-1}\boldsymbol{A}^T$ 用矩阵乘法的结合律和矩阵乘积的转置公式，可以证明投影矩阵的性质： $\boldsymbol{P}^2=\boldsymbol{P}$ ， $\boldsymbol{P}^T=\boldsymbol{P}$。
- **最小二乘法 Least Squares**

![](https://pic3.zhimg.com/v2-082e342a358ad8014cf6bb6453e40692_b.jpg)

应用投影矩阵求方程组最优解的方法，最常用于“最小二乘法”拟合曲线。

有三个数据点{(1,1), (2,2), (3,2)}，求直线方程b=C+Dt，要求直线尽量接近于三个点。把三个点的数据代入方程则有：

C+ D=1

C+2D=2

C+3D=2

矩阵形式为 $\left[ {\begin{array}{*{20}{r}} 1&1\\ 1&2\\ 1&3 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} C\\ D \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 1\\ 2\\ 2 \end{array}} \right]$ 

这个的方程***A*x**=**b**是无解的，解决办法就是求其最优解，即方程$\boldsymbol{A}^T\boldsymbol{A}\boldsymbol{\hat x}=\boldsymbol{A}^T\boldsymbol{b}$的解。

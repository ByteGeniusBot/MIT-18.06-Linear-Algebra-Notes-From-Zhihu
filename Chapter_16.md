# 第16讲 投影矩阵和最小二乘法

Projection matrices and least squares

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AOJPU)

- **投影 Projections**

上一讲介绍了投影矩阵 $\boldsymbol{P}=\boldsymbol{A}(\boldsymbol{A}^T\boldsymbol{A})^{-1}\boldsymbol{A}^T$ ，当它作用于向量**b**，相当于把**b**投影到矩阵***A***的列空间。

如果向量**b**本身就在***A***列空间之内，即存在**x**使得***A*x**=**b**，则有：

$\begin{array}{*{20}{l}} {\boldsymbol{P}\boldsymbol{b}}&{ =\boldsymbol{A}{{({\boldsymbol{A}^T}\boldsymbol{A})}^{ - 1}}{\boldsymbol{A}^T}\boldsymbol{b}}\\ {}&{ = \boldsymbol{A}{{({\boldsymbol{A}^T}\boldsymbol{A})}^{ - 1}}{\boldsymbol{A}^T}\boldsymbol{A}\boldsymbol{x}}\\ {}&{ = \boldsymbol{A}({{({\boldsymbol{A}^T}\boldsymbol{A})}^{ - 1}}{\boldsymbol{A}^T}\boldsymbol{A})\boldsymbol{x}}\\ {}&{ = \boldsymbol{A}\boldsymbol{x}= \boldsymbol{b}} \end{array}$ 

如果向量**b**与***A***的列空间正交，即向量**b**在矩阵***A***的左零空间N(***A***)中，则有

$\begin{array}{*{20}{l}} {\boldsymbol{P}\boldsymbol{b}}&{ =\boldsymbol{A}{{({\boldsymbol{A}^T}\boldsymbol{A})}^{ - 1}}{\boldsymbol{A}^T}\boldsymbol{b}}\\ {}&{ = \boldsymbol{A}{{({\boldsymbol{A}^T}\boldsymbol{A})}^{ - 1}}({\boldsymbol{A}^T}\boldsymbol{b})}\\ {}&{ = \boldsymbol{A}({{{\boldsymbol{A}^T}\boldsymbol{A})}^{ - 1}}\boldsymbol{0}}\\ {}&{ = \boldsymbol{0}} \end{array}$ 

![](https://pic1.zhimg.com/v2-02c981400cf48ff449aff79a3a041c60_b.jpg)

- **最小二乘法 Least Squares**

应用投影矩阵求方程组最优解的方法，最常用于“最小二乘法”拟合曲线。

![](https://pic3.zhimg.com/v2-75d86d5dc676ebd773e5de8c8ca345ca_b.jpg)

三个点{(1,1), (2,2), (3,2)}，求直线方程b=C+Dt，要求直线尽量接近于三个点。

C+ D=1

C+2D=2

C+3D=2


矩阵形式为 $\left[ {\begin{array}{*{20}{r}} 1&1\\ 1&2\\ 1&3 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} C\\ D \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 1\\ 2\\ 2 \end{array}} \right]$ 

这个的方程***A*x**=**b**是无解的，解决办法就是求其最优解，最优解的含义即为误差最小，这里误差就是每个方程误差值的平方和 ${\left\| \boldsymbol{e} \right\|^2} = {\left\| {\boldsymbol{A}\boldsymbol{x} - \boldsymbol{b}} \right\|^2}$ ，因此就是寻找具有最小误差平方和的解**x**，这就是所谓的“最小二乘”问题。

![](https://pic3.zhimg.com/v2-a8e05740edefdd861cc100d45c6fe1aa_b.jpg)

从几何上讨论求解过程，就是试图寻找数据点到直线距离的平方和 $\boldsymbol{e}_1^2 + \boldsymbol{e}_2^2 +\boldsymbol{e}_3^2$ 最小的情况，此时得到的C+Dt分别为p1，p2和p3，它们是满足方程并最接近于**b**的结果。另一种看法是，对于**R**3空间上的向量**b**，它投影到矩阵***A***的列空间中会得到向量**p**=[p1 p2 p3]，投影到矩阵***A***的零空间中则为**e**。

现在求解 $\boldsymbol{\hat x} = \left[ {\begin{array}{*{20}{c}} {\hat C}\\ {\hat D} \end{array}} \right]$ 和**p**。

方程$\boldsymbol{A}^T\boldsymbol{A}\boldsymbol{\hat x}=\boldsymbol{A}^T\boldsymbol{b}$

![](https://pic2.zhimg.com/v2-a474eb90887cf07b72a4051b9728bc59_b.jpg)

还可以从误差最小的角度出发求解：

$\boldsymbol{e}_1^2 + \boldsymbol{e}_2^2 +\boldsymbol{e}_3^2=(C+D-1)^2+(C+2D-2)^2+(C+3D-2)^2$ 

对等号右边的表达式求偏导数，极值出现在偏导数为0的位置。求偏导最终会得到相同的线性方程组和相同的解。

得到直线表达式y=2/3+t/2。将t=1, 2, 3分别代入可得：

![](https://pic2.zhimg.com/v2-85a884ee6152dd99ed51c9ae68a0d161_b.jpg)

可以验证，向量**p**与**e**正交，并且**e**与矩阵***A***的列空间正交。

- **矩阵** $\boldsymbol{A}^T\boldsymbol{A}$ 

证明：若***A***的列向量线性无关时，矩阵 $\boldsymbol{A}^T\boldsymbol{A}$ 为可逆矩阵。

假设存在**x**使得 $\boldsymbol{A}^T\boldsymbol{A}\boldsymbol{x}=\boldsymbol{0}$ 。则有$\boldsymbol{x}^T\boldsymbol{A}^T\boldsymbol{A}\boldsymbol{x}=0=(\boldsymbol{A}{\boldsymbol{x}})^T(\boldsymbol{A}\boldsymbol{x})$，因此***A*x**=**0**。因为***A***的列向量线性无关，所以只有当**x**=**0**时有***A*x**=**0**。因此只有当**x**=**0**时有$\boldsymbol{A}^T\boldsymbol{A}\boldsymbol{x}=\boldsymbol{0}$ 。即矩阵$\boldsymbol{A}^T\boldsymbol{A}$为可逆矩阵。

如果矩阵的列向量是互相垂直的单位向量，则它们一定是线性无关的。我们将这种向量称之为标准正交（orthonormal）。

例如： $\left[ {\begin{array}{*{20}{c}} 1\\ 0\\ 0 \end{array}} \right]$ ，$\left[ {\begin{array}{*{20}{c}} 0\\ 1\\ 0 \end{array}} \right]$  和$\left[ {\begin{array}{*{20}{c}} 0\\ 0\\ 1 \end{array}} \right]$ 。还有 $\left[ {\begin{array}{*{20}{c}} {\cos \theta }\\ {\sin \theta } \end{array}} \right]$ 和$\left[ {\begin{array}{*{20}{c}} {-\sin \theta }\\ {\cos \theta } \end{array}} \right]$ 。

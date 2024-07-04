# 第22讲 对角化和矩阵的幂

Diagonalization and powers of ***A***

[22 对角化和A的权力](https://v.youku.com/v_show/id_XNDA0Mzc3NzA4.html?spm=a2h0j.11185381.listitem_page1.5!22~A&&s=46136e60aecd11e19013)

本讲中我们学习如何对角化含有n个线性无关特征向量的矩阵，以及对角化是怎样简化计算的。

- **对角化矩阵 Diagonalizing a matrix ** $\boldsymbol{S}^{-1}\boldsymbol{AS}=\boldsymbol{\varLambda}$ 

如果矩阵***A***具有n个线性无关的特征向量，将它们作为列向量可以组成一个可逆方阵***S***，并且有：

$\begin{array}{*{20}{l}} {\boldsymbol{AS}}&{ = \boldsymbol{A}\left[ {\begin{array}{*{20}{c}} {{\boldsymbol{x}_1}}&{{\boldsymbol{x}_2}}& \cdots &{{\boldsymbol{x}_{\rm{n}}}} \end{array}} \right]}\\ {}&{ = \left[ {\begin{array}{*{20}{c}} {{\lambda _1}{\boldsymbol{x}_1}}&{{\lambda _2}{\boldsymbol{x}_2}}& \cdots &{{\lambda _{\rm{n}}}{\boldsymbol{x}_{\rm{n}}}} \end{array}} \right]}\\ {}&{ = \boldsymbol{S}\left[ {\begin{array}{*{20}{c}} {{\lambda _1}}&0& \cdots &0\\ 0&{{\lambda _2}}&{}&0\\  \vdots &{}& \ddots & \vdots \\ 0& \cdots &0&{{\lambda _{\rm{n}}}} \end{array}} \right]}\\ {}&{ = \boldsymbol{S\varLambda} } \end{array}$ 

这里的矩阵***Λ***为对角阵，它的非零元素就是矩阵***A***的特征值。因为矩阵***S***中的列向量线性无关，因此逆矩阵 $\boldsymbol{S}^{-1}$ 存在。在等式两侧左乘逆矩阵，得到$\boldsymbol{S}^{-1}\boldsymbol{AS}=\boldsymbol{\varLambda}$***。***同样地，$\boldsymbol{A}=\boldsymbol{S}\boldsymbol{\varLambda}\boldsymbol{S}^{-1}$***。***

对于消元法而言，矩阵有***LU***分解，对于施密特正交法，矩阵有***QR***分解，而上面的推导是一种新的矩阵分解。

> 之前曾经提到过消元进行行操作和列操作最后会得到“相抵标准型”。现在我们得到的是矩阵的“相似标准形”,它还保有矩阵操作的基本性质——特征值，而相抵标准型只剩下最内核的秩信息还保留着。

- **矩阵的幂 Powers of *A***

特征值给矩阵的幂计算提供了方法。

如果 $\boldsymbol{A}\boldsymbol{x}=\lambda \boldsymbol{x}$ ，则有 $\boldsymbol{A}^2\boldsymbol{x}=\lambda \boldsymbol{A}\boldsymbol{x}=\lambda^2\boldsymbol{x}$ 。说明矩阵 $\boldsymbol{A}^2$ 有着和***A***一样的特征向量，而特征值为 $\lambda^2$ 。写成对角化形式则有：$\boldsymbol{A}^2=\boldsymbol{S}\boldsymbol{\varLambda}\boldsymbol{S}^{-1}\boldsymbol{S}\boldsymbol{\varLambda}\boldsymbol{S}^{-1}=\boldsymbol{S}\boldsymbol{\varLambda}^{2}\boldsymbol{S}^{-1}$ 。做相同的处理还可以得到： $\boldsymbol{A}^k=\boldsymbol{S}\boldsymbol{\varLambda}^{k}\boldsymbol{S}^{-1}$ 。这说明 $\boldsymbol{A}^k$ 有着和***A***一样的特征向量，而特征值为 $\lambda^k$ 。

如果矩阵***A***具有n个线性无关的特征向量，如果所有的特征值均满足 $\left| {{\lambda _i}} \right|$ <1。则k→∞时， $\boldsymbol{A}^k$ →0。

- **重特征值 Repeated eigenvalues**

如果矩阵***A***没有重特征值，则其一定具有n个线性无关的特征向量。

如果矩阵***A***有重特征值，它有可能具有n个线性无关的特征向量，也可能没有。比如单位阵的特征值为重特征值1，但是其具有n个线性无关的特征向量。

对于如***A***= $\left[ {\begin{array}{*{20}{c}} 2&1\\ 0&2 \end{array}} \right]$ 的三角矩阵，特征值就是矩阵对角线上的元素2。其特征向量在 $\boldsymbol{A}-\lambda\boldsymbol{I}$ 的零空间中，满足 $(\boldsymbol{A}-\lambda\boldsymbol{I})\boldsymbol{x}=\left[ {\begin{array}{*{20}{c}} 0&1\\ 0&0 \end{array}} \right]\boldsymbol{x}=\boldsymbol{0}$ 。求解可得**x**= $\left[ {\begin{array}{*{20}{c}} 1\\ 0 \end{array}} \right]$ ，而没有第二个特征向量。

- **差分方程 Difference equations **$\boldsymbol{u}_{k+1}=\boldsymbol{A}\boldsymbol{u}_{k}$ 

从给定的一个向量**u**0出发，我们可以通过对前一项乘以矩阵***A***得到下一项的方式，得到一个向量序列：$\boldsymbol{u}_{k+1}=\boldsymbol{A}\boldsymbol{u}_{k}$。

$\boldsymbol{u}_{k+1}=\boldsymbol{A}\boldsymbol{u}_{k}$为一个一阶差分方程，$\boldsymbol{u}_{k}=\boldsymbol{A}^k\boldsymbol{u}_{0}$是方程的解。但这种简洁形式并没有给出足够的信息，我们需要通过特征向量和矩阵的幂运算给出真实解的结构。

将**u**0写成特征向量的线性组合：

$\boldsymbol{u}_0=c_1\boldsymbol{x}_1+c_2\boldsymbol{x}_2+…+c_n\boldsymbol{x}_n=\boldsymbol{S}\boldsymbol{c}$ 

$$
\boldsymbol{A}\boldsymbol{u}_0=c_1\lambda_1\boldsymbol{x}_1+c_2\lambda_2\boldsymbol{x}_2+…+c_n\lambda_n\boldsymbol{x}_n
$$

$\boldsymbol{u}_k=\boldsymbol{A}^k\boldsymbol{u}_0=c_1\lambda_1^k\boldsymbol{x}_1+c_2\lambda_2^k\boldsymbol{x}_2+…+c_n\lambda_n^k\boldsymbol{x}_n=\boldsymbol{\varLambda}^k\boldsymbol{S}\boldsymbol{c}$ 

下面用斐波那契数列进行举例。

- **斐波那契数列 Fibonacci sequence**

斐波那契数列为0,1,1,2,3,4,8,13……其通项公式为 $F_{k+2}=F_{k+1}+F_{k}$。求 $F_{100}$ ？

如果我们以矩阵的方式来理解数列，则矩阵的特征值可以告诉我们数列中数值的增长速度。

为了凑成矩阵形式，需要用一个比较巧妙的技巧。令 ${\boldsymbol{u}_k} = \left[ {\begin{array}{*{20}{c}} {{F_{k + 2}}}\\ {{F_{k + 1}}} \end{array}} \right]$ ，则有：

$\begin{array}{*{20}{c}} {{F_{k + 2}} = {F_{k + 1}} + {F_k}}\\ {{F_{k + 1}} = {F_{k + 1}}} \end{array}$ 写成矩阵形式为 $\boldsymbol{u}_{k+1}=\left[ {\begin{array}{*{20}{c}} 1&1\\ 1&0 \end{array}} \right]\boldsymbol{u}_{k}$ 

观察矩阵***A***= $\left[ {\begin{array}{*{20}{c}} 1&1\\ 1&0 \end{array}} \right]$ 的特征值和特征向量，因为其为对称矩阵，特征值为实数，且特征向量正交。

$\det (\boldsymbol{A} - \lambda \boldsymbol{I}) = \left| {\begin{array}{*{20}{c}} {1{\rm{ - }}\lambda }&1\\ 1&{{\rm{ - }}\lambda } \end{array}} \right| = \lambda ^2 - \lambda- 1 =0$ 

解得 ${\lambda _1}{\rm{ = }}\frac{{1 + \sqrt 5 }}{2}$ , ${\lambda _2}{\rm{ = }}\frac{{1 - \sqrt 5 }}{2}$ ，绝对值大于1的 $\lambda_1$ 控制着在斐波那契数列的增长。$\boldsymbol{u}_k=\boldsymbol{A}^k\boldsymbol{u}_0=c_1\lambda_1^k\boldsymbol{x}_1+c_2\lambda_2^k\boldsymbol{x}_2$，因为 $\left| {{\lambda _2}} \right|$ <1，所以当乘方次数较高时有k→∞， $\lambda_2^k$ →0。

从特征值可以求得对应的特征向量**x**1= $\left[ {\begin{array}{*{20}{c}} {{\lambda _1}}\\ 1 \end{array}} \right]$ 和**x**2= $\left[ {\begin{array}{*{20}{c}} {{\lambda _2}}\\ 1 \end{array}} \right]$ 。

> 在这里G. Strang 用了个小技巧，因为是二阶方程，而且矩阵$\boldsymbol{A} - \lambda \boldsymbol{I}$ 是奇异矩阵，所以只要符合$(\boldsymbol{A}-\lambda\boldsymbol{I})\boldsymbol{x}=\boldsymbol{0}$ 两个方程其中的一个即可，选取下面的方程，则立刻可以看出方程的解。

从${\boldsymbol{u}_0} = \left[ {\begin{array}{*{20}{c}} {{F_{1}}}\\ {{F_{0}}} \end{array}} \right]= \left[ {\begin{array}{*{20}{c}} {{1}}\\ {{0}} \end{array}} \right]=c_1\boldsymbol{x}_1+c_2\boldsymbol{x}_2$ ，可以求得 ${c_1} = \frac{1}{{\sqrt 5 }}， {c_2} = -\frac{1}{{\sqrt 5 }}$ 。

$\left[ {\begin{array}{*{20}{c}} {{F_{100}}}\\ {{F_{99}}} \end{array}} \right] = {\boldsymbol{A}^{99}}\left[ {\begin{array}{*{20}{c}} {{F_1}}\\ {{F_0}} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {{\lambda _1}}&{{\lambda _2}}\\ 1&1 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{\lambda _1}^{99}}&{}\\ {}&{{\lambda _2}^{99}} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{c_1}}\\ {{c_2}} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {{c_1}{\lambda _1}^{100} + {c_2}{\lambda _2}^{100}}\\ {} \end{array}} \right]$ 

可知 $F_{100}\approx c_1\lambda_1^{100}$ 。

> 很多人会问矩阵的特征值特征向量为什么这么神奇，可以把矩阵的操作变成一个简单的参数。还有人会问道为什么特征值在物理中出现非常频繁。对此我只能简单解释一下，物理中常见的被研究物体都有一个自身的内禀结构，这个内在结构的方向往往和观察者也就是外场的坐标有区别。当我们给物体施加一个外场刺激的时候，比如说外力或者电场极化等等，物体沿着其内在结构的取向来响应外场，但是观察者从外场坐标下采集反馈。实际上矩阵在不同坐标之间实现变换，特征向量显示了物体内结构的方向，特征值则是在这个主方向上物体对外场的响应参数。在有的领域直接将特征值称为伸缩系数，实际上它反应了在其所对应的特征向量方向上，内结构与外场之间的相互关系。
> 特征值还有一个应用是作为降维的判据，比如在图像压缩过程中，极小的特征值会被赋值为0，以此节省存储空间，也便于其它操作。反应在图像上，降维后的图像基本轮廓依旧清晰，图像细节有所牺牲。

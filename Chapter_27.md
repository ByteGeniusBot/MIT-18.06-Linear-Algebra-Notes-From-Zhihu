# 第27讲 正定矩阵和最小值

Positive definite matrices and minima

[28 正定矩阵和最小值](https://v.youku.com/v_show/id_XNDA0MzkxNzky.html?&s=46136e60aecd11e19013)

本讲学习正定矩阵，这部分内容将本课程之前的知识点：主元、行列式、特征值以及方程的稳定性融为一体。本讲介绍如何判定一个矩阵是否正定矩阵，以及当一个矩阵是正定矩阵时，其内涵和矩阵操作的效果有何特别之处。此外还有正定矩阵与几何的关系：椭圆和正定有关，双曲线与正定无关。

- **正定矩阵 Positive definite matrices**

给定一个2x2矩阵 $\boldsymbol{A}{\rm{ = }}\left[ {\begin{array}{*{20}{c}} a&b\\ b&c \end{array}} \right]$ ，有四个途径判定矩阵是否正定矩阵：

1. 特征值： $\lambda_1>0,\lambda_2>0$ 
2. 行列式（所有子行列式）： $a>0，ac-b^2>0$ 
3. 主元： $a>0，(ac-b^2)/a>0$ 
4. 表达式 $\boldsymbol{x}^T\boldsymbol{A}\boldsymbol{x}>0$ （**x**=0除外）。通常这就是正定的定义，而前三条是用来验证正定性的条件。

给定矩阵 $A{\rm{ = }}\left[ {\begin{array}{*{20}{c}} 2&6\\ 6&y \end{array}} \right]$ ，从判据可知矩阵为正定阵的条件是2y-36>0，即y>18。

矩阵 $\left[ {\begin{array}{*{20}{c}} 2&6\\ 6&{18} \end{array}} \right]$ 正好处在判定为正定矩阵的临界点上，称之为半正定（positive semidefinite）矩阵，它具有一个特征值0，是奇异矩阵，只有一个主元，而行列式为0。半正定矩阵特征值大于等于0。

再观察 $\boldsymbol{x}^T\boldsymbol{A}\boldsymbol{x}$ 判据：

$ \begin{array}{*{20}{l}} {\boldsymbol{x}^T\boldsymbol{A}\boldsymbol{x}}&{{\rm{ = }}\left[ {\begin{array}{*{20}{c}} {{x_1}}&{{x_2}} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 2&6\\ 6&{18} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{x_1}}\\ {{x_2}} \end{array}} \right]}\\ {}&{{\rm{ = }}2{x_1}^2 + 12{x_1}{x_2} + 18{x_2}^2} \end{array}$ 

之前讨论得都是线性方程***A*x**，现在引入 $\boldsymbol{x}^T$ ，变成二次，如果对于任意x，y，这种二次型（quadratic form） $a{x^2} + 2bxy + c{y^2}$ 均大于零，则矩阵为正定矩阵。

在本例的半正定矩阵中，当x1=3，x2=-1时 $2{x_1}^2 + 12{x_1}{x_2} + 18{x_2}^2 = 2{x_1} + 3{x_2}{^2} = 0$ 。

如果将矩阵变为 $\left[ {\begin{array}{*{20}{c}} 2&6\\ 6&7 \end{array}} \right]$ ，二次型为 $f(x,y) = 2{x^2} + 12xy + 7{y^2}$ ，从几何图像上看没有最小值点，在原点处有一鞍点。鞍点在某个方向上看是极大值点，在另一方向上是极小值点，实际上最佳观测角度是特征向量的方向。

如果将矩阵变为 $\left[ {\begin{array}{*{20}{c}} 2&6\\ 6&{20} \end{array}} \right]$ ，主元为正；特征值之积为行列式的值4，特征值和为矩阵的迹22，因此特征值为正；子行列式均为正。矩阵为正定矩阵。

二次型 $f(x,y) = 2{x^2} + 12xy + 20{y^2}$ ，其图像最小值点为原点，一阶偏导数为0，二阶偏导数为正。

![](https://pic3.zhimg.com/v2-3fc386ccee5eaab764c775f22bb10caa_b.jpg)

> 当年上课时候老师讲双曲面的鞍点，画的图不好，有个篮球队的哥们理解不了，于是下了课跑去问老师，老师指着他的热身篮球裤说，就你这种裤腿两侧能撕开的篮球裤，全部打开，拎起来，裤裆地方就是鞍点……算了，反正GS画图真心不行，看看Lay的吧：

![](https://pic4.zhimg.com/v2-2d59b896b28863326870c5168e6b5797_b.jpg)

微积分中判定最小值点的判据：一阶导数等于零 $\frac{{du}}{{dx}} = 0$ ，二阶导数为正 $\frac{{{d^2}u}}{{d{x^2}}} > 0$ 。线性代数中判据为二阶导数矩阵正定。

对于二次型我们可以用配方的办法来验证其是否具有最小值：

$f(x,y) = 2{x^2} + 12xy + 20{y^2}{\rm{ = }}2{(x + 3y)^2} + 2{y^2}$ 

配方使得 $x^2$ 的系数和交叉项 $xy$ 的系数配合形成完全平方的形式，这个时候用到的 $y^2$ 的系数正好是18，即判定正定的临界点。如果实际的系数d大于18，则还剩余 $(d-18)y^2$ ，二次型在原点之外一定大于零，若小于18则二次型可以小于等于0。

对于 $f(x,y) = 2{x^2} + 12xy + 20{y^2}{\rm{ = }}2{(x + 3y)^2} + 2{y^2}$ ，其几何图像为碗型的曲面，如果我们用f=1的截面横截曲面，得到的就是 $2{(x + 3y)^2} + 2{y^2}{\rm{ = }}1$ 的椭圆曲线。而对于双曲面进行切割就得到双曲线。

配方法其实就是消元：

![](https://pic2.zhimg.com/v2-e599da4fb492ddf8c3b8fd92dff6dc41_b.jpg)

主元就是平方项系数，***L***矩阵中的行操作数 $l_{21}$ 就是配方项内y的系数。因此这就是为什么主元为正则矩阵为正定矩阵，因为主元是每一个完全平方项的系数。本例中二次型表达式的配方说明了二维的情形，而线代的理论可以将之推广到n维。

二阶导数的矩阵记为 $\left[ {\begin{array}{*{20}{c}} {{f_{xx}}}&{{f_{xy}}}\\ {{f_{yx}}}&{{f_{yy}}} \end{array}} \right]$ ，矩阵对称代表交叉二阶偏导数与求导顺序无关 $f_{xy}=f_{yx}$ 。在微积分中我们学到的判据 $f_{xx}f_{yy}>f_{xy}^2$ ，和二阶矩阵判定正定是等价的，并且线代可以推广到n维。

3阶矩阵***A***= $\left[ {\begin{array}{*{20}{r}} 2&{{\rm{ - }}1}&0\\ {{\rm{ - }}1}&2&{{\rm{ - }}1}\\ 0&{{\rm{ - }}1}&2 \end{array}} \right]$ ，它是正定矩阵。计算子行列式得到 $\left| 2 \right|{\rm{ = }}2$ 

， $\left| {\begin{array}{*{20}{r}} 2&{{\rm{ - }}1}\\ {{\rm{ - }}1}&2 \end{array}} \right|{\rm{ = }}3$ ， $\left| {\begin{array}{*{20}{r}} 2&{{\rm{ - }}1}&0\\ {{\rm{ - }}1}&2&{{\rm{ - }}1}\\ 0&{{\rm{ - }}1}&2 \end{array}} \right|{\rm{ = }}4$ 。主元是2，3/2，4/3。特征值是 $2 - \sqrt 2 ,2,2 + \sqrt 2 $ 。

> 这是G. Strang最爱的矩阵之一，可以用来把二阶微分方程变成离散问题，因为它每一行都是差分方程 ${f_{n + 1}} - 2{f_n} + {f_{n - 1}}$ 。

其二次型为 ${{\boldsymbol{x}}^T}{\boldsymbol{A}\boldsymbol{x} = }2{x_1}^2 + 2{x_2}^2 + 2{x_3}^2 - 2{x_1}{x_2} - 2{x_2}{x_3}$ 。

这是一个四维的图像，三个维度x1，x2，x3，还有函数f，如果用f=1切割图像，则得到 $2{x_1}^2 + 2{x_2}^2 + 2{x_3}^2 - 2{x_1}{x_2} - 2{x_2}{x_3}{\rm{ = }}1$ 。这是一个椭球体，三个特征值不同，因此椭球的三个长轴长度不同。三个轴的方向就是特征向量的方向，轴长度就是特征值，矩阵的分解$\boldsymbol{A}=\boldsymbol{Q}\boldsymbol{\varLambda}\boldsymbol{Q}^T$ 很好的说明了这件事，这就是所谓的“主轴定理”。


---


> 对于三条判据可以判定正定： $\boldsymbol{x}^T\boldsymbol{A}\boldsymbol{x}>0$ （**x**=0除外）。已经分析了主元要大于零的原因，因为它是配方后的参数，只有都大于零才能保证正定。以下对于判据1和2做简要说明。
> 
> 对称矩阵**A**，其正交的特征向量可以张成整个空间，因此任意向量**x**均可表示成特征向量的线性组合 $\boldsymbol{x}=c_1\boldsymbol{x}_1+c_2\boldsymbol{x}_2+…c_n\boldsymbol{x}_n$ ，代入得$\boldsymbol{x}^T\boldsymbol{A}\boldsymbol{x}=c_1^2\lambda_1+c_2^2\lambda_2+…c_n^2\lambda_n$ ，当特征值都大于零且**x**≠0时，才能保证$\boldsymbol{x}^T\boldsymbol{A}\boldsymbol{x}>0$。因此条件1与正定性等价。
> 
> 记 $\boldsymbol{A}_k$ 为矩阵**A**左上角k阶方块，取特殊向量**x**= $\left[ {\begin{array}{*{20}{c}} {{\boldsymbol{x}_k}}\\ \boldsymbol{0} \end{array}} \right]$ ，即后n-k个元素为0，则有 $\boldsymbol{x}^T\boldsymbol{A}\boldsymbol{x}=\left[ {\begin{array}{*{20}{c}} {{x_k}}&0 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{A_k}}&*\\ *&* \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{x_k}}\\ 0 \end{array}} \right]\ =\boldsymbol{x}_k^T\boldsymbol{A}_k\boldsymbol{x}_k$ 。若矩阵**A**满足正定性，则所有$\boldsymbol{A}_k$均满足正定性。已证明正定性等价于特征值均为正，而矩阵行列式等于特征值之积，因此可知子行列式均大于零。反之亦成立，两命题等价。

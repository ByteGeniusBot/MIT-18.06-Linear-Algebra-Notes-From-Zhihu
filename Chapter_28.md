# 第28讲 相似矩阵和若尔当标准型

Similar matrices and Jordan form

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2B5OKE)

本讲介绍相似矩阵，这些内容以及奇异值分解是线性代数最核心的概念。

- **正定矩阵 **$\boldsymbol{A}^T\boldsymbol{A}$ 

若矩阵***A***满足对任意向量**x**0均有$\boldsymbol{x}^T\boldsymbol{A}\boldsymbol{x}>0$，则称矩阵为正定矩阵，可以通过特征值、主元和行列式的办法来判断矩阵的正定性。

正定矩阵来自于最小二乘问题。有大量的实际问题用到了长方形矩阵，而最小二乘问题中用到了长方形矩阵的积$\boldsymbol{A}^T\boldsymbol{A}$，它是正定矩阵。

正定矩阵***A***是对称矩阵，它的逆矩阵 $\boldsymbol{A}^{-1}$也是正定矩阵，逆矩阵的特征值是原矩阵的倒数，因此也都是正数。若矩阵***A***和***B***都是正定矩阵，则***A***+***B***也是正定矩阵：$\boldsymbol{x}^T\boldsymbol{A}\boldsymbol{x}>0$，$\boldsymbol{x}^T\boldsymbol{B}\boldsymbol{x}>0$，则有 $\boldsymbol{x}^T\boldsymbol{(A+B)}\boldsymbol{x}>0$ 。

如果***A***是一个mxn长方形矩阵，则 $\boldsymbol{A}^T\boldsymbol{A}$ 是对称方阵。通过讨论$\boldsymbol{x}^T(\boldsymbol{A}^T\boldsymbol{A})\boldsymbol{x}$的正负可以确认它是正定矩阵：$\boldsymbol{x}^T(\boldsymbol{A}^T\boldsymbol{A})\boldsymbol{x}=(\boldsymbol{A}\boldsymbol{x})^T(\boldsymbol{A}\boldsymbol{x})={\left| {Ax} \right|^2}\geq0$。当且仅当***A*x**=0时，表达式为0。当矩阵***A***的各列线性无关时，即矩阵为列满秩r=n，***A***的零空间只有零向量，即此条件下仅有零向量，满足$\boldsymbol{x}^T(\boldsymbol{A}^T\boldsymbol{A})\boldsymbol{x}=0$。因此矩阵列满秩时，$\boldsymbol{A}^T\boldsymbol{A}$是正定矩阵。正定矩阵将之前的知识点串联起来。

- **相似矩阵 Similar matrices**

***A***和***B***均是nxn方阵，若存在可逆矩阵***M***，使得 $\boldsymbol{B}=\boldsymbol{M}^{-1}\boldsymbol{A}\boldsymbol{M}$ ，则***A***和***B***为相似矩阵。

- **特征值互不相同 Distinct eigenvalues**

若矩阵***A***具有n个线性无关的特征向量，可以对角化得到$\boldsymbol{S}^{-1}\boldsymbol{A}\boldsymbol{S}=\boldsymbol{\varLambda}$，则***A***相似于***Λ***，这里的***M***是特征向量矩阵***S***。如果将***M***取其它可逆矩阵，可以得到和***A***相似的另一矩阵***B***，实际上这样可以定义一类矩阵，***Λ***是其中最简洁的一个。

例：***A***= $\left[ {\begin{array}{*{20}{c}} 2&1\\ 1&2 \end{array}} \right]$ ，则***Λ***= $\left[ {\begin{array}{*{20}{c}} 3&0\\ 0&1 \end{array}} \right]$ ，而取另一M，则有***B***= $\left[ {\begin{array}{*{20}{c}} 1&{ - 4}\\ 0&1 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 2&1\\ 1&2 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1&4\\ 0&1 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} { - 2}&{ - 15}\\ 1&6 \end{array}} \right]$ 。

相似矩阵最重要的特性是：**相似矩阵具有相同的特征值。**事实上，所有特征值为3和1的二阶矩阵都是***A***的相似矩阵。

证明矩阵***A***的相似矩阵$\boldsymbol{B}=\boldsymbol{M}^{-1}\boldsymbol{A}\boldsymbol{M}$，具有和矩阵***A***相同的特征值：

矩阵***A***具有的特征值 $\lambda$ ，即存在特征向量**x**满足 $\boldsymbol{A}\boldsymbol{x}=\lambda\boldsymbol{x}$ 。则有：

$\begin{array}{*{20}{l}} {\boldsymbol{A}\boldsymbol{M}{\boldsymbol{M}^{ - 1}}\boldsymbol{x}}&{ = \lambda \boldsymbol{x}}\\ {{\boldsymbol{M}^{ - 1}}\boldsymbol{A}\boldsymbol{M}{\boldsymbol{M}^{ - 1}}\boldsymbol{x}}&{ = \lambda {\boldsymbol{M}^{ - 1}}\boldsymbol{x}}\\ {\boldsymbol{B}{\boldsymbol{M}^{ - 1}}\boldsymbol{x}}&{ = \lambda {\boldsymbol{M}^{ - 1}}\boldsymbol{x}} \end{array}$ 

即矩阵具有特征值 $\lambda$ ，且特征向量为 $\boldsymbol{M}^{ - 1}\boldsymbol{x}$ 。

因此，相似矩阵具有相同的特征值，并且线性无关的特征向量的个数相同，但是特征向量往往不同。如果矩阵***A***的特征值互不相等 $\lambda_1\ne\lambda_2\ne…\ne\lambda_n$ ，而与另一个矩阵***B***的特征值完全相同 $\lambda_1=\lambda_1',\lambda_2=\lambda_2',…\lambda_n=\lambda_n'$ ，则它们与相同的对角矩阵***Λ***相似。

- **重特征值 Repeated eigenvalues**

如果矩阵有重特征值，则可能无法进行对角化。

例：二阶矩阵有重特征值 $\lambda_1=\lambda_2=4$ 。

第一类： $\left[ {\begin{array}{*{20}{c}} 4&0\\ 0&4 \end{array}} \right]$ 只与自己相似， ${\boldsymbol{M}^{ - 1}}\left[ {\begin{array}{*{20}{c}} 4&0\\ 0&4 \end{array}} \right]\boldsymbol{M} = 4{\boldsymbol{M}^{ - 1}}\boldsymbol{I}\boldsymbol{M} = \left[ {\begin{array}{*{20}{c}} 4&0\\ 0&4 \end{array}} \right]$ 。这个系列的相似矩阵仅包含其自身。

第二类包含其它所有的重特征值为4的矩阵：其中最简洁的是 $\left[ {\begin{array}{*{20}{c}} 4&1\\ 0&4 \end{array}} \right]$ ，元素1的位置换上其它数值仍然是相似矩阵。这个最优形式称为若尔当（Jordan form）标准型。有了这个理论，就可以处理不可对角化的矩阵，完成近似的“对角化”转化为若尔当标准型进行处理。

与 $\left[ {\begin{array}{*{20}{c}} 4&1\\ 0&4 \end{array}} \right]$ 相似的矩阵，迹为8，行列式为16，因此我们可以构造出很多相似矩阵： $\left[ {\begin{array}{*{20}{c}} 5&1\\ { - 1}&3 \end{array}} \right]$ ， $\left[ {\begin{array}{*{20}{c}} 4&0\\ {17}&4 \end{array}} \right]$ ， $\left[ {\begin{array}{*{20}{c}} a&*\\ *&{8 - a} \end{array}} \right]$ ……它们都不能对角化（因为若可以对角化则按照特征值可知结果为4***I***，而4***I***只与自己相似）。

- **若尔当标准型 Jordan form**

更复杂的情况，一个四阶矩阵具有重特征值0， $\lambda_1=\lambda_2=\lambda_3=\lambda_4=0$ 。

***A***= $\left[ {\begin{array}{*{20}{c}} 0&1&0&0\\ 0&0&1&0\\ 0&0&0&0\\ 0&0&0&0 \end{array}} \right]$ ,它的秩为2，因此其零空间的维数为4-2=2，而零空间的向量就是矩阵的特征向量，满足***A*x**=0**x**，所以矩阵***A***只有两个特征向量。若尔当指出上对角线每增加一个1，矩阵就减掉一个特征向量，本例中特征向量数为4-2=2。

矩阵***B***= $\left[ {\begin{array}{*{20}{c}} 0&1&7&0\\ 0&0&1&0\\ 0&0&0&0\\ 0&0&0&0 \end{array}} \right]$ 与矩阵***A***=$\left[ {\begin{array}{*{20}{c}} 0&1&0&0\\ 0&0&1&0\\ 0&0&0&0\\ 0&0&0&0 \end{array}} \right]$ 为相似矩阵。

但矩阵***C***= $\left[ {\begin{array}{*{20}{c}} 0&1&0&0\\ 0&0&0&0\\ 0&0&0&1\\ 0&0&0&0 \end{array}} \right]$ 与***A***=$\left[ {\begin{array}{*{20}{c}} 0&1&0&0\\ 0&0&1&0\\ 0&0&0&0\\ 0&0&0&0 \end{array}} \right]$并不是相似矩阵，两者具有不同的若尔当块。若尔当块形如***J*** i= $\left[ {\begin{array}{*{20}{c}} {{\lambda _i}}&1&0& \cdots &0\\ 0&{{\lambda _i}}&1& \ddots & \vdots \\ 0&0& \ddots & \ddots &0\\  \vdots &{}& \ddots & \ddots &1\\ 0&0& \cdots &0&{{\lambda _i}} \end{array}} \right]$ ，对角线上为重特征值 $\lambda_i$ ，上对角线为1，其它位置的元素均为0，每个若尔当块只有1个特征向量。若干个若尔当块可以拼成一个若尔当矩阵。

若尔当矩阵：***J***= $\left[ {\begin{array}{*{20}{c}} {{\boldsymbol{J}_1}}&0& \cdots &0\\ 0&{{\boldsymbol{J}_2}}& \cdots &0\\  \vdots &{}& \ddots & \vdots \\ 0&0& \cdots &{{\boldsymbol{J}_d}} \end{array}} \right]$ 

两个矩阵具有相同的特征值和特征向量个数，但是其若尔当块的尺寸不同，两者也并不是相似矩阵。如前述矩阵***A***与***C***并不相似。

若尔当理论：任意n阶矩阵***A***都与一个若尔当矩阵***J***相似。若尔当矩阵中的每一个若尔当块对应一个特征向量。若矩阵具有n个不同的特征向量，则可以对角化，此时其若尔当标准型***J***就是对角矩阵***Λ***。若出现重特征值，则特征向量个数变少。


---


> 说到了$\boldsymbol{A}^T\boldsymbol{A}$和最小二乘问题就要解释一下，G.Strang举得曲线拟合的例子，都是线性公式y=ax+b，但实际上最小二乘法也处理非线性方程，因为这里所谓的非线性是对x而言，而只要对于所求的参数是线性方程就可以。比如下面的例子中x的方幂组成的矩阵**X**只是一个系数矩阵，对于所求的参数β这仍是个线性方程组。

![](https://pic3.zhimg.com/v2-7a8693a6d2e67520f38d5b753a42cc6a_b.jpg)

![](https://pic4.zhimg.com/v2-d15c57885faabf198b29b78dcef0c7bf_b.jpg)

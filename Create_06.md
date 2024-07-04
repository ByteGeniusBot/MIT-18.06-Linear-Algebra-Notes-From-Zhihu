 第06讲 列空间和零空间 Column space & Nullspace 

[网易公开课](http://open.163.com/movie/2010/11/B/5/M6V0BQC4M_M6V2AB1B5.html)

本节继续研究子空间，特别是矩阵的列空间（column space）和零空间（nullspace）。

- **子空间综述**

所谓的“向量空间”是对于线性运算封闭的向量集合。即对于空间中的任意向量**v**和**w**，其和**v**+**w**和数乘c**v**必属于该空间；换而言之对于任何实数c和d，线性组合c**v**+d**w**必属于该空间。

${\boldsymbol{R}^1}$ ， ${\boldsymbol{R}^2}$ ，${\boldsymbol{R}^3}$ ，……都是重要的向量空间，${\boldsymbol{R}^n}$ 代表的空间包含所有具有n个分量的向量。其中字母R表明分量均为实数（real）。

“子空间”为包含于向量空间内的一个向量空间。它是原向量空间的一个子集，而且本身也满足向量空间的要求。

> 但是“子空间”和“子集”的概念有区别，所有元素都在原空间之内就可称之为子集，但是要满足对线性运算封闭的子集才能成为子空间。

例如

![](https://pic2.zhimg.com/v2-3b13ead6721a9545de84f7bb62db8de1_b.jpg)

通过原点的平面P是${\boldsymbol{R}^3}$的一个子空间。

通过原点的直线L也是${\boldsymbol{R}^3}$的子空间。

P并L（union）通常并不是${\boldsymbol{R}^3}$的子空间。

P交L（intersection）是${\boldsymbol{R}^3}$子空间的特例——0空间，只有零向量。

任意子空间S和T的交集都是子空间，可以通过S和T本身对线性组合封闭来证明。

- **列空间 Column space**

矩阵***A***的列空间C(***A***)是其列向量的所有线性组合所构成的空间。

求解***A*x**=**b**的问题，对于给定的矩阵***A***，对于任意的**b**都能得到解么？

如果 $\boldsymbol{A} = \left[ {\begin{array}{*{20}{r}} 1&1&2\\ 2&1&3\\ 3&1&4\\ 4&1&5 \end{array}} \right]$ 

显然并不是所有的**b**都能保证***A*x**=**b**有解，因为它有4个线性方程而只有3个未知数，矩阵***A***列向量的线性组合无法充满**R**4，因此如果**b**不能被表示为***A***列向量的线性组合时，方程是无解的。只有当**b**在矩阵***A***列空间C(***A***)里时，**x**才有解。

对于我们所给定的矩阵***A***，由于列向量不是线性无关的，第三个列向量为前两个列向量之和，所以尽管有3个列向量，但是只有2个对张成向量空间有贡献。矩阵***A***的列空间为${\boldsymbol{R}^4}$内的一个二维子空间。

- **零空间（或化零空间）Nullspace**

矩阵***A***的零空间N(***A***)是指满足***A*x**=**0**的所有解的集合。对于所给定这个矩阵***A***，其列向量含有4个分量，因此列空间是空间${\boldsymbol{R}^4}$的子空间，**x**为含有3个分量的向量，故矩阵***A***的零空间是${\boldsymbol{R}^3}$的子空间。对于mxn矩阵，列空间为${\boldsymbol{R}^m}$的子空间，零空间为${\boldsymbol{R}^n}$空间的子空间。

本例中矩阵***A***的零空间N(***A***)为包含 $\left[ {\begin{array}{*{20}{r}} 1\\ 1\\ { - 1} \end{array}} \right]$ 的任何倍数的集合，因为很容易看到第一列向量（1）和第二列向量（1）相加减去第三列向量（-1）为零。此零空间为${\boldsymbol{R}^3}$中的一条直线。

为了验证***A*x**=**0**的解集是一个向量空间，我们可以检验它是否对线性运算封闭。

若**v**和**w**为解集中的元素，则有：

***A***(**v**+**w**)=***A*v**+***A*w**=**0**+**0**=**0**，

***A***(c**v**)=c***A*v**=**0**，

因此得证N(***A***)确实为${\boldsymbol{R}^n}$空间的一个子空间。

- **b值的影响 Other values of b**

若方程变为 $\left[ {\begin{array}{*{20}{r}} 1&1&2\\ 2&1&3\\ 3&1&4\\ 4&1&5 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{x_1}}\\ {{x_2}}\\ {{x_3}} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 1\\ 2\\ 3\\ 4 \end{array}} \right]$ ，则其解集不能构成一个子空间。零向量并不在这个集合内。解集是空间${\boldsymbol{R}^3}$内过 $\left[ {\begin{array}{*{20}{r}} 1\\ 0\\ 0 \end{array}} \right]$和 $\left[ {\begin{array}{*{20}{r}} 0\\ -1\\ 1 \end{array}} \right]$的一个直线，但是并不穿过原点 $\left[ {\begin{array}{*{20}{r}} 0\\ 0\\ 0 \end{array}} \right]$。




本讲给出了关于矩阵的两种子空间，同时给出了两种构造子空间的方法。对于列空间，它是由列向量进行线性组合张成的空间；而零空间是从方程组出发，通过让**x**满足特定条件而得到的子空间。
# 第17讲 正交矩阵和施密特正交化

Orthogonal matrices & Gram-Schmidt

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AORLS)

本讲我们完成对“正交”的介绍。Gram-Schmidt过程可以将原空间的一组基转变为标准正交基。

- **正交向量 Orthonormal vectors**

满足如下条件的向量**q**1，**q**2……**q**n为标准正交：

${\boldsymbol{q}_i}^T{\boldsymbol{q}_j} = \left\{ {\begin{array}{*{20}{l}} 0&{i \ne j}\\ {}&{}\\ 1&{i = j} \end{array}} \right.$ 

换而言之，它们都具有单位长度1，并且彼此正交。标准正交向量是线性无关的。很多线性代数的计算都建立在标准正交基础上，它让一切变得简单可控。

- **标准正交矩阵 Orthonormal matrix**

如果矩阵***Q***的列向量为标准正交向量，则 $\boldsymbol{Q}^T\boldsymbol{Q}=\boldsymbol{I}$ 为单位阵。

![](https://pic1.zhimg.com/v2-7de84b3b906095fced9c1e352f32de48_b.jpg)

注意这里的矩阵***Q***可以不是方阵。我们已经学过了一系列矩阵，包括三角阵、对角阵、置换矩阵、对称矩阵、行最简梯形矩阵、投影矩阵等等，现在有了“标准正交”矩阵。

一个标准正交的方阵我们称之为“正交矩阵”（orthogonal matrix）。如果***Q***为方阵，因为$\boldsymbol{Q}^T\boldsymbol{Q}=\boldsymbol{I}$ ，所以$\boldsymbol{Q}^T=\boldsymbol{Q}^{-1}$ 。

> 注意必须是方阵，必须是标准正交，而不只是正交*。*

例如，置换矩阵 $\boldsymbol{Q} = \left[ {\begin{array}{*{20}{c}} 0&0&1\\ 1&0&0\\ 0&1&0 \end{array}} \right]$ ，则有 ${\boldsymbol{Q}^T} = \left[ {\begin{array}{*{20}{c}} 0&1&0\\ 0&0&1\\ 1&0&0 \end{array}} \right]$ ，两者皆为正交矩阵，并且两者乘积为单位阵。

再例如， $\boldsymbol{Q} = \left[ {\begin{array}{*{20}{r}} {cos\theta }&{{\rm{ - }}sin\theta }\\ {sin\theta }&{cos\theta } \end{array}} \right]$ 为正交矩阵。而矩阵 $\left[ {\begin{array}{*{20}{r}} 1&1\\ 1&{{\rm{ - }}1} \end{array}} \right]$ 并不是正交矩阵，而通过调整得到的矩阵 $\boldsymbol{Q} = \frac{1}{{\sqrt 2 }}\left[ {\begin{array}{*{20}{r}} 1&1\\ 1&{{\rm{ - }}1} \end{array}} \right]$ 为正交矩阵，在矩阵外面要除以向量的长度。

再比如 $\boldsymbol{Q} = \frac{1}{2}\left[ {\begin{array}{*{20}{r}} 1&1&1&1\\ 1&{{\rm{ - }}1}&1&{{\rm{ - }}1}\\ 1&1&{{\rm{ - }}1}&{{\rm{ - }}1}\\ 1&{{\rm{ - }}1}&{{\rm{ - }}1}&1 \end{array}} \right]$ 也是由-1和+1组成的正交矩阵，这种类型的矩阵称之为阿达玛Hadamard矩阵，不同阶数矩阵性质不同并且没有规律，无从判断几阶的阿达玛矩阵为正交阵。

再给一个长方形矩阵的例子，其列向量为标准正交：

$\boldsymbol{Q} = \frac{1}{3}\left[ {\begin{array}{*{20}{r}} 1&{{\rm{ - }}2}\\ 2&{{\rm{ - }}1}\\ 2&2 \end{array}} \right]$ ，我们可以拓展其成为正交矩阵 $\frac{1}{3}\left[ {\begin{array}{*{20}{r}} 1&{{\rm{ - }}2}&2\\ 2&{{\rm{ - }}1}&{{\rm{ - }}2}\\ 2&2&1 \end{array}} \right]$ 。

- **标准正交列向量的优势 Orthonormal columns are good**

若***Q***的列向量为标准正交向量，则投影到***Q***的列空间的投影矩阵为：

$\boldsymbol{P}=\boldsymbol{Q}(\boldsymbol{Q}^T\boldsymbol{Q})^{-1}\boldsymbol{Q}^T$ 

因为 $\boldsymbol{Q}^T\boldsymbol{Q}=\boldsymbol{I}$ ，所以$\boldsymbol{P}=\boldsymbol{Q}\boldsymbol{Q}^T$。这种情况会降低很多运算量。如果***Q***为方阵，则***P***=***I***，因为***Q***的列向量张成了整个空间，投影过程不会对向量有任何改变。

很多复杂问题使用标准正交向量之后都变得简单。如果基为标准正交，则方程$\boldsymbol{A}^T\boldsymbol{A}\boldsymbol{\hat x}=\boldsymbol{A}^T\boldsymbol{b}$ 的解变为$\boldsymbol{\hat x}=\boldsymbol{Q}^T\boldsymbol{b}$ ，$\boldsymbol{\hat x}$ 的分量$\hat x_i$就等于$\boldsymbol{q}_i^T\boldsymbol{b}$。

- **施密特正交化Gram-Schmidt**

从两个线性无关的向量**a**和**b**开始，它们张成了一个空间，我们的目标是希望找到两个标准正交的向量**q**1，**q**2能张成同样的空间。Schmidt给出的结论是如果我们有一组正交基**A**和**B**（*注意这个小节***A**，**B**，**C***均为向量*），那么我们令它们除以自己的长度就得到标准正交基：

${{\boldsymbol{q}}_1}{\rm{ = }}\frac{\boldsymbol{A}}{{\left\| \boldsymbol{A} \right\|}}$ ,${{\boldsymbol{q}}_2}{\rm{ = }}\frac{\boldsymbol{B}}{{\left\| \boldsymbol{B} \right\|}}$ 。

Gram做了重要的工作，令**A**=**a**，我们在**a**和**b**张成的空间中，取与**A**正交的向量做成标准正交基，方法就是将**b**投影到**a**的方向，然后取**B**=**b**-**p**（**B**就是之前谈论过的误差**e**的方向）。

![](https://pic3.zhimg.com/v2-b7417f61a8b405107811ede251ece9c2_b.jpg)

则有 ${\boldsymbol{B}}=\boldsymbol{b} - \frac{{{\boldsymbol{A}^T}\boldsymbol{b}}}{{{\boldsymbol{A}^T}\boldsymbol{A}}}\boldsymbol{A}$ 

如果从等式两端左乘 $\boldsymbol{A}^T$ ，可以得到$\boldsymbol{A}^T\boldsymbol{B}=0$ 。

如果从三个线性无关的向量**a**、**b**和**c**出发，则可以通过从**c**中减去其在**A**和**B**两个方向的投影来得到**C**。 $\boldsymbol{C} =\boldsymbol{c} - \frac{{{\boldsymbol{A}^T}\boldsymbol{c}}}{{{\boldsymbol{A}^T}\boldsymbol{A}}}\boldsymbol{A} - \frac{{{\boldsymbol{B}^T}\boldsymbol{c}}}{{{\boldsymbol{B}^T}\boldsymbol{B}}}\boldsymbol{B}$ 

例如：**a**= $\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 1 \end{array}} \right]$ ，**b**=$\left[ {\begin{array}{*{20}{c}} 1\\ 0\\ 2 \end{array}} \right]$ ，则有**A**=**a**，**B**= $\left[ {\begin{array}{*{20}{c}} 1\\ 0\\ 2 \end{array}} \right] - \frac{3}{3}\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 1 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 0\\ 1\\ { - 1} \end{array}} \right]$ ，验证计算得$\boldsymbol{A}^T\boldsymbol{B}=0$ 。

写出**q**1，**q**2所组成的矩阵为：

***Q***= $\left[ {\begin{array}{*{20}{r}} {}&{}\\ {{\boldsymbol{q}_1}}&{{\boldsymbol{q}_2}}\\ {}&{} \end{array}} \right] = \left[ {\begin{array}{*{20}{r}} {1/\sqrt 3 }&0\\ {1/\sqrt 3 }&{ - 1/\sqrt 2 }\\ {1/\sqrt 3 }&{1/\sqrt 2 } \end{array}} \right]$ 

***Q***列向量的空间就是**a**和**b**张成的空间。因此矩阵***Q***和矩阵***A***= $\left[ {\begin{array}{*{20}{r}} 1&1\\ 1&0\\ 1&2 \end{array}} \right]$ 有相同的列空间。

在消元过程中，我们可以对矩阵进行分解得到***A***=***LU***，而在对***A***做施密特正交化的过程也可以用矩阵运算的方式表示为***A***=***QR***。此处***R***为上三角阵。

![](https://pic1.zhimg.com/v2-95de193943ccc9cfd5ee6272050f9068_b.jpg)

***R***为上三角阵，则 $\boldsymbol{a}_1^T\boldsymbol{q}_2=0$ 。这是因为**a**1就是**q**1的方向，而**q**1和**q**2为标准正交向量，因此**q**2的方向与**a**1垂直，因此内积为0。***R**在**Q**右侧相当于对**Q**做列操作，即**A**的列向量是**Q**列向量的线性组合，而**Q**为**A**列空间的一组标准正交基，则**R**的元素实际上是**A**的列向量基于**Q**这组标准正交基的权。*

> 采用矩阵的***QR***分解来帮助求解***A*x**=**b**的问题，最大的优势是提高了数值的稳定性。

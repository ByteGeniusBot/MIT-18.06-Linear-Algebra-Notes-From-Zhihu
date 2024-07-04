# 第14讲 正交向量与正交子空间

Orthogonal vectors & subspaces

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AJEMH)

本讲我们讨论正交（orthogonal）概念对于向量、基和子空间的意义。

![](https://pic3.zhimg.com/v2-20c81709c3bdca46f82258331afaa43e_b.jpg)

图中绘制空间成90度角，这是表示这两个空间正交。

> 这张图是G.Strang最得意的作品之一，它反映了四个子空间的关系，在后面的课程中可以看到其两两形成正交补，在**R**n空间中的向量会向两个子空间射影，并向**R**m空间形成映射，反之亦然。

- **正交向量 Orthogonal vectors**

![](https://pic2.zhimg.com/v2-d0917ff44f56bc641bf35501be4fbf65_b.jpg)

正交就是垂直（perpendicular）的另一种说法。两向量正交的判据之一是其点积$x^{T}y=y^{T}x=0$ 。当两个向量的夹角为90度时，按照勾股定理（毕达哥拉斯定理 Pythagorean theorem）**x**，**y**满足：

${\left\| {x} \right\|^2} + {\left\| {y} \right\|^2} = {\left\| {{x} + {y}} \right\|^2}$ 

 其中 ${\left\|{x} \right\|^2}{\rm{ = }}{{x}^T}{x}$ 

例如 **x**= $\left[ \begin{array}{*{20}{r}} 1\\ 2\\ 3 \end{array} \right]$ ，**y**= $\left[ \begin{array}{*{20}{r}} 2\\ -1\\ 0 \end{array} \right]$ ，则 **x** + **y**= $\left[ \begin{array}{*{20}{r}} 3\\ 1\\ 3 \end{array} \right]$ ， ${\left\| x \right\|^2} = 14$ ， ${\left\| \boldsymbol{y} \right\|^2} = 5$ ， ${\left\| \boldsymbol{x} + \boldsymbol{y} \right\|^2} = 19$ 。

将勾股定理展开进行计算，则有：

$$
{\boldsymbol{x}^T \boldsymbol{x} + \boldsymbol{y}^T \boldsymbol{y} = (\boldsymbol{x} + \boldsymbol{y})^T (\boldsymbol{x} + \boldsymbol{y}) = \boldsymbol{x}^T \boldsymbol{x} + \boldsymbol{y}^T \boldsymbol{y} + \boldsymbol{x}^T \boldsymbol{y} + \boldsymbol{y}^T \boldsymbol{x}}
$$

得到 $2 \boldsymbol{x}^T \boldsymbol{y} = 0$ 。


零向量与所有向量都正交。

- **正交子空间 Orthogonal subspaces**

子空间**S**与子空间**T**正交，则**S**中的任意一个向量都和**T**中的任意向量正交。黑板所在的平面和地板所在平面不是正交关系，沿两者的交线方向的向量同时属于两个平面，但并不与自己正交。

我们在平面内讨论正交子空间，平面的子空间包括只包含零向量的**0**空间、过原点的直线以及整个平面。经过原点的直线不会和整个空间正交；**0**空间和过原点的直线正交；经过原点的两条直线若夹角为直角则互相正交。

- **零空间与行空间正交 Null space is perpendicular to row space**

矩阵的行空间和它的零空间相交。若**x**在零空间内，则有***A*x**=**0**，将***A***表示为行向量的格式：

$\left[ {\begin{array}{*{20}{c}} {ro{w_1}}\\ {ro{w_2}}\\  \vdots \\ {ro{w_m}} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {}\\ x\\ {} \end{array}} \right]{\rm{ = }}\left[ {\begin{array}{*{20}{c}} {ro{w_1} \cdot x}\\ {ro{w_2} \cdot x}\\  \vdots \\ {ro{w_m} \cdot x} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 0\\ 0\\  \vdots \\ 0 \end{array}} \right]$ 

**x**与矩阵***A***的行向量点积都等于0，则它和矩阵***A***行向量的线性组合进行点积也为0，所以**x**与***A***的行空间正交。**x**为零空间内的任意向量，所以零空间与行空间正交。同理可以证明列空间与左零空间正交。

行空间和零空间实际上把**R**n空间分割成了两个正交的子空间。例如对于矩阵：

***A***= $\left[ {\begin{array}{*{20}{r}} 1&2&5\\ 2&4&{10} \end{array}} \right]$ ,其行空间是1维的，向量 $\left[ {\begin{array}{*{20}{c}} 1\\ 2\\ 5 \end{array}} \right]$ 是它的基向量，而其零空间是垂直于 $\left[ {\begin{array}{*{20}{c}} 1\\ 2\\ 5 \end{array}} \right]$ 并穿过原点的2维平面。

行空间和零空间不仅仅是正交，并且其维数之和等于n，我们称行空间和零空间为**R**n空间内的正交补（orthogonal complements）。这表示零空间包含所有和行空间正交的向量，反之亦然。

> 想想我们之前提到的黑板和地板平面不是正交子空间的例子，二者都在3维空间中，分别为2维空间，因此不可能正交。一个空间中正交子空间的维数之和不可能超过原空间的维数。

我们可以称目前讨论的这部分内容是线性代数基本定理的第二部分。第一部分是给出四个子空间和它们的维数，第二部分说明它们是两两互为正交补，第三部分讨论子空间的正交基。

> 这些内容都反映在了本讲座开始的那幅图上。

- **矩阵** $\boldsymbol{A}^T\boldsymbol{A}$ 

下面讨论如何求解一个无解方程组***A*x**=**b**的解。如果***A***是长方形矩阵，m大于n。当左侧方程数特别多的时候，容易混入“坏”数据，方程变得无解。但是对于数据的可信度我们无从判断，线性代数要做的就是在这种条件下求一个方程的“最优解”。矩阵$\boldsymbol{A}^T\boldsymbol{A}$会发挥重要作用，它是一个nxn方阵，并且是对称阵，$(\boldsymbol{A}^T\boldsymbol{A})^{T}=\boldsymbol{A}^T\boldsymbol{A}$。

本章的核心内容就是当***A*x**=**b**无解的时候，求解 $\boldsymbol{A}^T\boldsymbol{A}x=\boldsymbol{A}^Tb$ 得到最优解。

**例：*A***= $\left[ {\begin{array}{*{20}{r}} 1&1\\ 1&2\\ 1&5 \end{array}} \right]$ ，则$\boldsymbol{A}^T\boldsymbol{A}$= $\left[ {\begin{array}{*{20}{r}} 1&1&1\\ 1&2&5 \end{array}} \right]\left[ {\begin{array}{*{20}{r}} 1&1\\ 1&2\\ 1&5 \end{array}} \right]{\rm{ = }}\left[ {\begin{array}{*{20}{c}} 3&8\\ 8&{30} \end{array}} \right]$ 是可逆矩阵。

但是矩阵$\boldsymbol{A}^T\boldsymbol{A}$并不总是可逆。

**例：*A***= $\left[ {\begin{array}{*{20}{r}} 1&3\\ 1&3\\ 1&3 \end{array}} \right]$ ，则$\boldsymbol{A}^T\boldsymbol{A}$= $\left[ {\begin{array}{*{20}{r}} 1&1&1\\ 3&3&3 \end{array}} \right]\left[ {\begin{array}{*{20}{r}} 1&3\\ 1&3\\ 1&3 \end{array}} \right]{\rm{ = }}\left[ {\begin{array}{*{20}{c}} 3&9\\ 9&{27} \end{array}} \right]$ 是不可逆矩阵。

实际上 N($\boldsymbol{A}^T\boldsymbol{A}$)=N(***A***)，并且矩阵$\boldsymbol{A}^T\boldsymbol{A}$的秩等于***A***的秩。因此矩阵$\boldsymbol{A}^T\boldsymbol{A}$可逆，则要求***A***的零空间只有零向量，即***A***的列向量线性无关。

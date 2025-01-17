# 第07讲 求解Ax=0：主变量，特解 

Solving ***A*x**=**0**: pivot variables, special solutions

[网易公开课](http://open.163.com/movie/2010/11/H/H/M6V0BQC4M_M6V2ABAHH.html)

我们定义了矩阵的列空间和零空间，那么如何求得这些子空间呢？本节课的内容即从定义转到算法。

- **计算零空间 Nullspace**

矩阵***A***的零空间即满足***A*x**=**0**的所有**x**构成的向量空间。

取 $\boldsymbol{A} = \left[ {\begin{array}{*{20}{r}} 1&2&2&2\\ 2&4&6&8\\ 3&6&8&{10} \end{array}} \right]$ 

（***A***的列空间并不是线性无关的。）无论矩阵A是否可逆，我们都采用消元法作为计算零空间的算法。

对于矩阵***A***进行“行操作”并不会改变***A*x**=**b**的解，因此也不会改变零空间。（但是会改变列空间。）此处不需要应用增广矩阵，因为等号右侧的向量**b**=**0**。

第一步消元得到：

![](https://pic1.zhimg.com/v2-f94cbb6d0d6f7f5a904253673563bf94_b.jpg)

第二列没有主元，因此主元二是第二行第三列的2。

![](https://pic3.zhimg.com/v2-a8cc3da743f9bba6d3e8760b07414eb2_b.jpg)

矩阵***U***为梯形矩阵。其第三行变为零，是因为原矩阵***A***第三行的行向量本身就是第一行和第二行行向量的线性组合。

矩阵的秩（rank）就是矩阵的主元的个数。本例中矩阵***A***和***U***的秩均为2。矩阵中包含主元的列为主元列（pivot column），不包含主元的列称为自由列（free column）。

- **特解 Special solutions**

当我们将系数矩阵变换为上三角阵***U***时，就可以用回代求得方程***U*x**=**0**的解。本例中，包含主元的矩阵第1列和第3列为主元列，而不包含主元的第2列和第4列为自由列。对自由变量（free variable）x2和x4我们可以进行赋值。例如令x2=1而x4=0。则有

$2{x_3} + 4{x_4} = 0 \Rightarrow {x_3} = 0$ 

${x_1} + 2{x_2} + 2{x_3} + 2{x_4} = 0 \Rightarrow {x_1} =  - 2$ 

因此可得一解**x**= $\left[ {\begin{array}{*{20}{r}} { - 2}\\ 1\\ 0\\ 0 \end{array}} \right]$ ，其任意倍数均在矩阵的零空间之内。

取自由变量中x2=0而x4=1，则可得到另一解**x**= $\left[ {\begin{array}{*{20}{r}} 2\\ 0\\ { - 2}\\ 1 \end{array}} \right]$ 。

矩阵***A***的零空间就是这些“特解”向量的线性组合所构成的向量空间。

矩阵的秩r 等于其主元列的数目，因此自由列的数目就等于n-r，即列的数目减去主元列的数目。这个数值等于特解的数目和零空间的维数。

> 主元列和自由列的一个重要区别就是，自由列可以表示为其左侧所有主元列的线性组合，而主元列则不可以。

![](https://pic2.zhimg.com/v2-a5f7c098bb04ae317a2de6cac8302035_b.jpg)

> 例如，我们得到一个消元完成后的梯形矩阵***U***，其包含四个主元列。观察它的第五列，这是自由列，其左侧有两个主元列，这两个主元列显然线性无关，第五列也显然可以写成前两个主元列的线性组合。这里求的是***U*x**=**0**的解，如果令对应第二列，第四列，第七列这三个自由列以及第五列右侧的两个主元列的x分量都为0，而对应第五列的自由变量x5=1，则方程变为：

![](https://pic1.zhimg.com/v2-23ad2b254fb33f7c7abc13300d7a5148_b.jpg)

> 相当于求第五列如何用前两个主元列进行线性组合，所得解[x1,0,x3,0,1,0,0,0]即为原方程的特解之一。对所有的自由列都进行此操作，就是上文求解过程中对自由变量的赋值过程。在本例中，四个自由变量分别取1会得到零空间的四个特解。如果把自由变量都赋值为0会怎么样？答案是求得的解为**0**向量。

- **行最简阶梯矩阵 Reduced row echelon form （rref）**

通过继续消元我们可以将矩阵***U***转变为行最简阶梯矩阵形式***R***，其中主元为1，而主元列除主元外皆为0。在Matlab中用命令rref(***A***)实现这一过程。

![](https://pic4.zhimg.com/v2-3d48d9dc5347585998167f9dbdf2a2cb_b.jpg)

在矩阵中主元行和主元列的交汇处存在一个单位阵。通过“列交换”，可以将矩阵***R***中的主元列集中在左侧，从而在左上角形成这个单位阵，而将自由列集中在矩阵的右侧。如果矩阵***A***中的某些行是线性相关的，则在矩阵***R***的下半部分就会出现一些完全为**0**的行向量。

![](https://pic4.zhimg.com/v2-3a94133bc6345ee18153b65bd9899783_b.jpg)

这里的***I ***是一个rxr的方阵。***F ***即自由列消元后组成的部分。

原方程***A*x**=**0**变为求解***R***的主元行乘以**x**， $\left[ {\begin{array}{*{20}{c}} I&F \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{x_{pivot}}}\\ {{x_{free}}} \end{array}} \right] = 0$ 。我们将***A*x**=**0**的特解作为列向量写成一个矩阵***N***，即零空间矩阵。则其形式为***N***= $\left[ {\begin{array}{*{20}{r}} {}\\ \boldsymbol{I} \end{array}} \right]$ 。这里的***I ***为一个(n-r)x(n-r)的矩阵，就是对n-r个自由变量分别赋值为1所构造出来的，零空间矩阵满足***RN***=***0***，***0***矩阵是一个mx(n-r)的矩阵。则从矩阵分块乘法运算可知零空间矩阵上半部分为-***F***，即***N***最终形式为

![](https://pic2.zhimg.com/v2-a5b61cf2c07dfe3dc14c7a7afba7605d_b.jpg)

> 对于矩阵***R ***而言，求零空间特解就变得非常简单，只需要将消元的到的***F ***部分拼接上单位阵就可以得到所有的通解。注意如果在变换出***R ***左上角的单位阵的过程中采用了列交换，则最后的解要完成逆变换。

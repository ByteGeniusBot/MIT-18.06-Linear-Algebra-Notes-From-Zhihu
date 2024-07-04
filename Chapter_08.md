# 第08讲 求解Ax=b：可解性与结构   

Complete Solution of ***A*x**=**b**

[网易公开课](http://open.163.com/movie/2010/11/V/8/M6V0BQC4M_M6V2ABHV8.html)

- **可解的条件 Solvability conditions on b**

仍取***A***= $\left[ {\begin{array}{*{20}{r}} 1&2&2&2\\ 2&4&6&8\\ 3&6&8&{10} \end{array}} \right]$ 为例，则方程为 $\left[ {\begin{array}{*{20}{r}} 1&2&2&2\\ 2&4&6&8\\ 3&6&8&{10} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{x_1}}\\ {{x_2}}\\ {{x_3}}\\ {{x_4}} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {{b_1}}\\ {{b_2}}\\ {{b_3}} \end{array}} \right]$ 。

矩阵***A***的第三行为第一行和第二行的加和，因此***A*x**=**b**中**b**的第3个分量也要等于其第1和第2个分量的和。若**b**不满足b3=b1+b2则方程组无解。

检验***A*x**=**b**是否可解的方法是对增广矩阵进行行消元。如果矩阵***A***的行被完全消去的话，则对应的**b**的分量也要得0。在本例中，矩阵***A***的第三行被消去：

$\left[ {\begin{array}{*{20}{r}} 1&2&2&2&{{b_1}}\\ 2&4&6&8&{{b_2}}\\ 3&6&8&{10}&{{b_3}} \end{array}} \right] \to ... \to \left[ {\begin{array}{*{20}{l}} 1&2&2&2&{{b_1}}\\ 0&0&2&4&{{b_2} - 2{b_1}}\\ 0&0&0&0&{{b_3} - {b_2} - {b_1}} \end{array}} \right]$ 

如果***A*x**=**b**有解，则b3-b1-b2=0。在本例中我们令**b**= $\left[ {\begin{array}{*{20}{c}} 1\\ 5\\ 6 \end{array}} \right]$ 

前几讲讨论过，只有当**b**处于矩阵的列空间C(***A***)之中时，方程才有解。本讲推导出矩阵***A***的行向量若经过线性组合成为了零向量，则对应的**b**经同样的线性组合后也要等于0。因此看起来我们有了两条关于**b**的限制条件，但实际上这两点是等价的。

- **通解 Complete solution**

为求得***A*x**=**b**的所有解，我们首先检验方程是否可解，然后找到一个特解。将特解和矩阵零空间的向量相加即为方程的通解。

- **特解 A particular solution**

求***A*x**=**b**特解的方法是将自由变量均赋值为0，求解其主变量。

本例中，令x2=x4=0得到方程组：

$\begin{array}{*{20}{r}} {{x_1} + 2{x_3} = 1}\\ {2{x_3} = 3} \end{array}$ 

可解得x3=3/2，x1=-2，因此特解为**x**p= $\left[ {\begin{array}{*{20}{c}} { - 2}\\ 0\\ {3/2}\\ 0 \end{array}} \right]$ 。

> 上一讲说了主元列和自由列的一个重要区别就是，自由列可以表示为其左侧所有主元列的线性组合，而主元列则不可以，主元列是线性无关的。

![](https://pic4.zhimg.com/v2-a06711690ca62d8f4407965b9106affb_b.jpg)

> 我们仍以这个消元完成后的梯形矩阵***U***为例，其包含四个主元列。对于***A*x**=**b**的求解转变为***U*x**=**c**，其中**c**是向量**b**经过与左侧矩阵相同的行操作得到的向量。明显可以看到，此时四个主元列的线性组合可以组成任何 ${\boldsymbol{R}^4}$ 中的向量，我们将**x**中的自由变量赋值为0就可以去掉自由列列向量的干扰，求得方程的特解 ${\boldsymbol{x}_p}$ 。如果消 元得到***U***最后i行为0，就要求**c**的最后i个分量为0，这时主元列才可以通过线性组合得到**c**，否则无解。

- **与零空间进行线性组合 Combined with nullspace**

***A*x**=**b**的通解为${\boldsymbol{x}_{complete}} = {\boldsymbol{x}_p} + {\boldsymbol{x}_{n}}$ ，其中 ${\boldsymbol{x}_n}$ 为矩阵零空间中的一般向量。将 $\boldsymbol{A}{\boldsymbol{x}_p} = \boldsymbol{b}$ 和 $\boldsymbol{A}{\boldsymbol{x}_n} = \boldsymbol{0}$ 相加可得 $\boldsymbol{A}({\boldsymbol{x}_p}+{\boldsymbol{x}_n}) = \boldsymbol{b}$ 。

上一讲我们得到了矩阵的零空间N(***A***)就是其特解 $\left[ {\begin{array}{*{20}{r}} { - 2}\\ 1\\ 0\\ 0 \end{array}} \right]$ 和 $\left[ {\begin{array}{*{20}{r}} 2\\ 0\\ { - 2}\\ 1 \end{array}} \right]$ 的线性组合的集合。因此方程***A*x**= $\left[ {\begin{array}{*{20}{c}} 1\\ 5\\ 6 \end{array}} \right]$ 的通解即为： ${\boldsymbol{x}_{complete}} = \left[ {\begin{array}{*{20}{c}} { - 2}\\ 0\\ {3/2}\\ 0 \end{array}} \right] + {c_1}\left[ {\begin{array}{*{20}{r}} { - 2}\\ 1\\ 0\\ 0 \end{array}} \right] + {c_2}\left[ {\begin{array}{*{20}{r}} 2\\ 0\\ { - 2}\\ 1 \end{array}} \right]$ ,式中c1和c2为任意实数。

矩阵的零空间N(***A***)是**R**4空间中的二维子空间，方程的解***A*x**=**b**构成了穿过**x**p点并和矩阵零空间平行的“平面“。但该”平面“并不是**R**4空间的子空间。

> 前面求取**Ax**=**b**的特解过程中，我们令所有自由变量赋值为0。如果不赋值为0，则等于带着自由列进行计算，但自由列其实也就是主元列的线性组合，这样求的特解**x**p’只不过是**x**p与零空间特解的一个加和。如此例中若令x2=1,x4=0，则求特解的方程变为： $\begin{array}{*{20}{r}} {{x_1} + 2 + 2{x_3} = 1}\\ {2{x_3} = 3} \end{array}$ ，求得x1=-4，x3=3/2。因此特解为 ${\boldsymbol{x}_p}^\prime  =\left[ {\begin{array}{*{20}{c}} { - 4}\\ 1\\ {3/2}\\ 0 \end{array}} \right]$ 。而实际上 ${\boldsymbol{x}_p}^\prime  = {\boldsymbol{x}_p} + {\boldsymbol{x}_{n1}} = \left[ {\begin{array}{*{20}{c}} { - 2}\\ 0\\ {3/2}\\ 0 \end{array}} \right] + \left[ {\begin{array}{*{20}{r}} { - 2}\\ 1\\ 0\\ 0 \end{array}} \right]$ 。

- **秩 Rank**

矩阵的秩等于矩阵的主元数。如果mxn矩阵的秩为r，则必有r<=m且r<=n。

讨论满秩（full rank）的情形：

- 列满秩：r=n。每列都有主元，**x**的每一个分量都是主变量，没有自由变量。零空间N(***A***)之内只有零向量。方程无解或者有唯一解**x**p。

    例如***A***= $\left[ {\begin{array}{*{20}{r}} 1&3\\ 2&1\\ 6&1\\ 5&1 \end{array}} \right] \to \left[ {\begin{array}{*{20}{r}} 1&0\\ 0&1\\ 0&0\\ 0&0 \end{array}} \right]$ =***R***

- 行满秩：r=m。每行都有主元，无论**b**取何值，方程***A*x**=**b**都有解。主变量r个，自由变量n-r个。

    例如***A***= $\left[ {\begin{array}{*{20}{r}} 1&2&6&5\\ 3&1&1&1 \end{array}} \right] \to \left[ {\begin{array}{*{20}{r}} 1&0&{\rm{*}}&{\rm{*}}\\ 0&1&*&* \end{array}} \right]$ =***R***

- 满秩r=m=n，矩阵可逆。零空间只有零向量，无论**b**取何值，方程***A*x**=**b**都有唯一解。

    例如***A***= $\left[ {\begin{array}{*{20}{c}} 1&2\\ 3&1 \end{array}} \right] \to \left[ {\begin{array}{*{20}{c}} 1&0\\ 0&1 \end{array}} \right]$ =***R***为单位阵。

总结：

![](https://pic2.zhimg.com/v2-42ee38f151cc96f8f2df713dd3e08f41_b.jpg)

秩决定了方程组解的数量。

> mxn给出了矩阵的尺寸，但是秩r给出的是矩阵的实际“大小”。关于这个随后会有讨论。

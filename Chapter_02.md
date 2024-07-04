# 第02讲 矩阵消元 Elimination with matrices**

[优酷视频](https://v.youku.com/v_show/id_XNDA0MjQzMjY0.html?spm=a2h0k.11417342.soresults.dselectbutton&s=46136e60aecd11e19013)

- **消元法Method of Elimination**

消元法是计算机软件求解线形方程组所用的最常见的方法。任何情况下，只要是矩阵***A***可逆，均可以通过消元法求得***A*x**=**b**的解。

此处给出的线性方程组为

***A***= $\left[ {\begin{array}{*{20}{c}} 1&2&1\\ 3&8&1\\ 0&4&1 \end{array}} \right]$ **b**=  $\left[ {\begin{array}{*{20}{c}} 2\\ {12}\\ 2 \end{array}} \right]$ 

高斯消元法（Gauss elimination）就是通过对方程组中的某两个方程进行适当的数乘和加（jian）和（fa），以达到将某一未知数系数变为零，从而削减未知数个数的目的。

我们将矩阵左上角的1称之为“主元一”（the first pivot），第一步要通过消元将第一列中除了主元之外的数字均变化为0。操作方法就是用之后的每一行减去第一行的适当倍数，此例中第二行应减去第一行的3倍。之后应对第三行做类似操作，本例中三行第一列数字已经为0，故不用进行操作。

![](https://pic4.zhimg.com/v2-61339d2c149cd27fa1534f14955b59cb_b.jpg)

处在第二行第二列的主元二为2，因此用第三行减去第二行的两倍进行消元，得到第三个主元为5。

矩阵***A***为可逆矩阵，消元结束后得到上三角阵***U***（Uppertriangular matrix），其左侧下半部分的元素均为0，而主元1,2,5分列在***U***的对角线上。主元之积即行列式的值。

需要说明的是，主元不能为0，如果恰好消元至某行，0出现在了主元的位置上，应当通过与下方一行进行“行交换”使得非零数字出现在主元位置上。如果0出现在了主元位置上，并且下方没有对等位置为非0数字的行，则消元终止，并证明矩阵A为不可逆矩阵，且线性方程组没有唯一解。

例如消成这样  $\left[ {\begin{array}{*{20}{c}} {\rm{*}}&{\rm{*}}&{\rm{*}}\\ 0&{\rm{*}}&{\rm{*}}\\ 0&0&0 \end{array}} \right] $ 

- **回代 Back-Substitution**

做方程的高斯消元时，需要对等式右侧的**b**做同样的乘法和加减法。手工计算时比较有效率的方法是应用“增广矩阵”（augmented matrix），将**b**插入矩阵***A***之后形成最后一列，在消元过程中带着**b**一起操作。（Matlab是算完系数矩阵再处理**b**的。）

$\left[ {\begin{array}{*{20}{c}} 1&2&1&2\\ 3&8&1&{12}\\ 0&4&1&2 \end{array}} \right] \to \left[ {\begin{array}{*{20}{c}} 1&2&1&2\\ 0&2&{{\rm{ - }}2}&6\\ 0&4&1&2 \end{array}} \right] \to \left[ {\begin{array}{*{20}{c}} 1&2&1&2\\ 0&2&{{\rm{ - }}2}&6\\ 0&0&5&{{\rm{ - }}10} \end{array}} \right]$ 

此时我们将原方程***A*x**=**b**转化为了新的方程***U*x**=**c**，其中**c**=此时我们将原方程***A*x**=**b**转化为了新的方程***U*x**=**c**，其中**c**= $\left[ {\begin{array}{*{20}{c}} 2\\ 6\\ {{\rm{ - }}10} \end{array}} \right]$ 。

从最后一行得到z=-2，依次回代可以得到y=1,和x=2。

> 以上高斯消元法的内容基本是回忆求解线性方程的步骤，是我们很熟悉的东西。在线性代数中比较重要的就是将之前所说的“第二行减去第一行的3倍”这种操作条例变为矩阵化的数学语言。

- **消元矩阵 Elimination Matrices**

矩阵运算的核心内容就是对“行”或者“列”进行独立操作。

如前一节课“列图像”部分所言，系数矩阵乘以未知数向量，相当于对系数矩阵的列向量进行线性组合。

例如

![](https://pic2.zhimg.com/v2-c52123cd6c73a47aac1dee794ec13b1d_b.jpg)

与之相对称，矩阵左乘行向量则是对矩阵的行向量进行线性组合。

例如

![](https://pic1.zhimg.com/v2-89967b7b08509860ad3c77e1df55d138_b.jpg)

> 我学这部分的时候，列向量的线性组合非常容易就接受了，左乘行向量这个总觉得很别扭，偏偏行向量在下面介绍消元矩阵时比较重要。后来想想觉得“列”操作就像是把向量开进矩阵，而“行操作”这个就像把向量倒车进入矩阵（如图中箭头所示）。-_-! 虽然挺扯淡的，但是我反正突然就觉得习惯了。

矩阵消元的第一步是通过左乘矩阵***E21***来实现原矩阵***A***的第二行减去第一行的3倍这一过程。***E21***的第二行使矩阵***A***的行向量进行前述的线性组合，而其它两行为了保持与原矩阵相同，采用同阶单位阵***I ***的行向量。左乘的这个矩阵为“初等矩阵”（Elementary Matrix），因此记做***E***。*我以为是消元矩阵，所以记做**E**呢。*因为所乘行向量的倍数-3出现在***E***矩阵的第二行第一列，因此将之标注为21。完成操作后矩阵变为***E21A***。

第一行： $\left[ {\begin{array}{*{20}{c}} 1&0&0 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1&2&1\\ 3&8&1\\ 0&4&1 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 1&2&1 \end{array}} \right]$ 

第三行： $\left[ {\begin{array}{*{20}{c}} 0&0&1 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1&2&1\\ 3&8&1\\ 0&4&1 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 0&4&1 \end{array}} \right]$ 

关键第二行： $\left[ {\begin{array}{*{20}{c}} {{\rm{ - }}3}&1&0 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1&2&1\\ 3&8&1\\ 0&4&1 \end{array}} \right] = \begin{array}{*{20}{r}} {{\rm{ - }}3}&{[1}&2&{1]}\\ {\begin{array}{*{20}{c}}  + &1 \end{array}}&{[3}&8&{1]}\\ {\begin{array}{*{20}{c}}  + &0 \end{array}}&{[0}&4&{1]} \end{array} = \left[ {\begin{array}{*{20}{r}} 0&2&{ - 2} \end{array}} \right]$ 

$\begin{array}{l} \left[ {\begin{array}{*{20}{c}} 1&0&0\\ {{\rm{ - }}3}&1&0\\ 0&0&1 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1&2&1\\ 3&8&1\\ 0&4&1 \end{array}} \right] = \left[ {\begin{array}{*{20}{r}} 1&2&1\\ 0&2&{{\rm{ - }}2}\\ 0&4&1 \end{array}} \right]\\ \begin{array}{*{20}{l}} &{}{{\boldsymbol{E}_{21}}}&{}&{}&{}&{}&\boldsymbol{A}&{}&{}&{}&{}&{}&{{\boldsymbol{E}_{21}}\boldsymbol{A}}&{}&{} \end{array} \end{array}$ 

矩阵消元的第二步是完成矩阵***E21A***的第三行减去第二行的2倍，通过左乘矩阵***E32***来实现这一过程。

$\begin{array}{l} \left[ {\begin{array}{*{20}{c}} 1&0&0\\ 0&1&0\\ 0&{{\rm{ - }}2}&1 \end{array}} \right]\left[ {\begin{array}{*{20}{r}} 1&2&1\\ 0&2&{{\rm{ - }}2}\\ 0&4&1 \end{array}} \right] = \left[ {\begin{array}{*{20}{r}} 1&2&1\\ 0&2&{{\rm{ - }}2}\\ 0&0&5 \end{array}} \right]\\ \begin{array}{*{20}{l}} {}&{{\boldsymbol{E}_{32}}}&{}&{}&&{}{{\boldsymbol{E}_{21}}\boldsymbol{A}}&{}&{}&{}&{{\boldsymbol{E}_{32}}({\boldsymbol{E}_{21}}\boldsymbol{A})}&{}&{}&{}&{}&{}&{}&{}&{} \end{array} \end{array}$ 

3x3矩阵的消元本来应该分三步完成，最终得到***E32***(***E31***(***E21A***))。本例中***E31***=***I***，所以结果变为***E32***(***E21 A***）=***U***，因为矩阵运算符合结合律，也可写作(***E32 E21***)***A***=***U***。可以记作***EA***=**U**。

方程***A*x**=**b**的解也满足方程***U*x**=***EA*x**=***E*b**=**c**，因此我们将问题转化为***U*x**=**c**。

- **置换矩阵 Permutation**

左乘置换矩阵可以完成原矩阵的行变换，右乘置换矩阵则为列变换。例如

$\left[ {\begin{array}{*{20}{c}} 0&1\\ 1&0 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} a&b\\ c&d \end{array}} \right]\begin{array}{*{20}{c}} {}&{\begin{array}{*{20}{c}} {}&{_{}} \end{array}}\\ {}&{} \end{array} = \left[ {\begin{array}{*{20}{c}} c&d\\ a&b \end{array}} \right] $ 

$\begin{array}{*{20}{c}} {}&{\begin{array}{*{20}{c}} {}&{_{}} \end{array}}\\ {}&{} \end{array}\left[ {\begin{array}{*{20}{c}} a&b\\ c&d \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 0&1\\ 1&0 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} b&a\\ d&c \end{array}} \right]$ 

对于三阶矩阵， $\left[ {\begin{array}{*{20}{c}} 0&0&1\\ 0&1&0\\ 1&0&0 \end{array}} \right]\left[ {\begin{array}{*{20}{r}} a&b&c\\ d&e&f\\ g&h&i \end{array}} \right] = \left[ {\begin{array}{*{20}{r}} g&h&i\\ d&e&f\\ a&b&c \end{array}} \right]$ 

构造***P ***矩阵是通过对***I ***矩阵进行“行交换”来实现的。

 左右乘效果不同也展示了矩阵运算不符合交换律的性质。

- **逆矩阵 Inverse**

这里主要讨论消元矩阵的逆矩阵。消元矩阵之逆矩阵的实施效果就是抵消原矩阵的消元操作。消元矩阵实现了对原矩阵***A***的操作，使第二行行向量[3,8,1]减掉了第一行[1,2,1]的3倍变为[0,2,-2]，则逆向操作就应该是把现在的第二行行向量[0,2,-2]加上第一行[1,2,1]的3倍，从而变回原来的第二行[3,8,1]。

所以对于 ${\boldsymbol{E}_{21}} = \left[ {\begin{array}{*{20}{r}} 1&0&0\\ {{\rm{ - }}3}&1&0\\ 0&0&1 \end{array}} \right]$  ，有 $\boldsymbol{E}_{21}^{ - 1} = \left[ {\begin{array}{*{20}{r}} 1&0&0\\ 3&1&0\\ 0&0&1 \end{array}} \right]$   。

满足 $\boldsymbol{E}_{21}^{ - 1}{\boldsymbol{E}_{21}} =\boldsymbol{I}$ ，即 $\left[ {\begin{array}{*{20}{r}} 1&0&0\\ 3&1&0\\ 0&0&1 \end{array}} \right]\left[ {\begin{array}{*{20}{r}} 1&0&0\\ {{\rm{ - }}3}&1&0\\ 0&0&1 \end{array}} \right] = \left[ {\begin{array}{*{20}{r}} 1&0&0\\ 0&1&0\\ 0&0&1 \end{array}} \right]$ 。

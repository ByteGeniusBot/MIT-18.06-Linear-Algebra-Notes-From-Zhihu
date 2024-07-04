# 第01讲 行图像和列图像 Row picture & Column picture

[01 方程组的几何解释](https://v.youku.com/v_show/id_XNDA0MjQxMDgw.html?spm=a2h0k.11417342.soresults.dselectbutton&s=46136e60aecd11e19013)

- **线性方程的几何图像 The geometry of linear equations**

线性代数的基本问题就是解n元一次方程组。例如：二元一次方程组

$\begin{array}{*{20}{r}} {2x - y = 0}\\ { - x + 2y = 3} \end{array}$ 

写成矩阵形式就是

$\left[ {\begin{array}{*{20}{r}} 2&{ - 1}\\ { - 1}&2 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} x\\ y \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 0\\ 3 \end{array}} \right]$ 

其中***A***= $\left[ {\begin{array}{*{20}{r}} 2&{{\rm{ - }}1}\\ {{\rm{ - }}1}&2 \end{array}} \right]$ 被称为系数矩阵（coefficient matrix）。

未知数向量通常记为**x**= $\left[ {\begin{array}{*{20}{c}} x\\ y \end{array}} \right]$ 

而等号右侧的向量记为**b**。线性方程组简记为***A*x**=**b**。

- **行图像 Row Picture**

![](https://pic1.zhimg.com/v2-5409108b2547739d61638a5f27da7b5c_b.jpg)

行图像遵从解析几何的描述，每个方程在平面上的图像为一条直线。找到符合方程的两个数组，就可以确定出x-y平面上的两个点，连接两点可以画出该方程所代表的直线。两直线交点即为方程组的解x=1,y=2。    

- **列图像Column Picture**

 在列图像中，我们将系数矩阵写成列向量的形式，则求解原方程变为寻找列向量的线性组合（linear combination）来构成向量**b**。

$x\left[ {\begin{array}{*{20}{r}} 2\\ { - 1} \end{array}} \right] + y\left[ {\begin{array}{*{20}{r}} { - 1}\\ 2 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 0\\ 3 \end{array}} \right]$ 

 向量线性组合是贯穿本课程的重要概念。对于给定的向量**c**和**d**以及标量*x*和*y*，我们将*x***c**+*y***d**称之为**c**和**d**的一个线性组合。

从几何上讲，我们是寻找满足如下要求的x和y，使得两者分别数乘对应的列向量之后相加得到向量 $\left[ {\begin{array}{*{20}{c}} 0\\ 3 \end{array}} \right]$。其几何图像如下图。

![](https://pic3.zhimg.com/v2-84c168e85e4e541b26f007937a676366_b.jpg)

蓝色为向量 $\left[ {\begin{array}{*{20}{r}} 2\\ {{\rm{ - }}1} \end{array}} \right]$ ；

红色为向量  $\left[ {\begin{array}{*{20}{r}} {{\rm{ - }}1}\\ 2 \end{array}} \right]$ ；

可以看到当蓝色的向量乘以1与红色的向量乘以2后做加法（首尾相接）就可以得到绿色的向量**b**=$\left[ {\begin{array}{*{20}{c}} 0\\ 3 \end{array}} \right]$，由此可得到方程的解x=1,y=2。    

想象一下如果任意取x,y，则得到的线性组合又是什么？其结果就是以上两个列向量的所有线性组合将会布满整个坐标平面。

![](https://pic4.zhimg.com/v2-f05fd33a67d91da8d3449b2d6bc10533_b.jpg)

*D.C.Lay 的《线性代数及其应用》中，绘制向量${v_1} = \left[ {\begin{array}{*{20}{c}} { - 1}\\ 1 \end{array}} \right]$和${v_2} = \left[ {\begin{array}{*{20}{c}} 1\\ 2 \end{array}} \right]$的线性组合充满整个平面的图像，节点处为向量的整数倍线性组合。（老规矩，斜体部分是我自己乱喷的）*

*这本书也是难得的好书，作者喜欢利用几何图像来帮助读者理解线性代数中的概念，英文版出到第5版了，华章出过中译本。（是不是觉得上面那个图片有点斜，是斜线造成的错觉呦！）*

 将以上讨论扩展到三元。*图不好弄，所以用了G. Strang课本里的另一个方程，没有用视频中的那个！！！这样方程和配图是吻合的。*

$\begin{array}{*{20}{r}} x&{ + 2y}&{ + 3{\rm{z}}}& = &6\\ {2x}&{ + 5y}&{ + 2z}& = &4\\ {6{\rm{x}}}&{ - 3y}&{ + z}& = &2 \end{array}$ 矩阵形式为 $\left[ {\begin{array}{*{20}{r}} 1&2&3\\ 2&5&2\\ 6&{{\rm{ - }}3}&1 \end{array}} \right]\left[ {\begin{array}{*{20}{r}} x\\ y\\ z \end{array}} \right] = \left[ {\begin{array}{*{20}{r}} 6\\ 4\\ 2 \end{array}} \right]$ 

![](https://pic2.zhimg.com/v2-6e55df9df4f8e7dfadd653311aa5dfa1_b.jpg)

*画图真不是G.Strang的长项，在视频里画的就比较shi，他自己也承认了。在课本里他用两个面相交于一条直线画了一个图，然后让这条直线和第三个平面相交画了第二个图。同样的事，D.C.Lay一张图分分钟搞定。*

方程组列图像为 $x\left[ {\begin{array}{*{20}{r}} 1\\ 2\\ 6 \end{array}} \right] + y\left[ {\begin{array}{*{20}{r}} 2\\ 5\\ { - 3} \end{array}} \right] + z\left[ {\begin{array}{*{20}{r}} 3\\ 2\\ 1 \end{array}} \right] = \left[ {\begin{array}{*{20}{r}} 6\\ 4\\ 2 \end{array}} \right]$ 

![](https://pic1.zhimg.com/v2-62ba415a4e07eb146beee58380e95bd0_b.jpg)

如果改变等号右侧的**b**的数值，那么对于行图像而言三个平面都改变了，而对于列图像而言，三个向量并没有发生变化，只是需要寻找一个新的组合。

那么问题来了，是否对于所有的**b**，方程***A*x**=**b**都有解？

从列图像上看，问题转化为“列向量的线性组合是否覆盖整个三维空间？”

反例：若三个向量在同一平面内——比如“列3”恰好等于“列1”加“列2”，而若**b**不在该平面内，则三个列向量无论怎么组合也得不到平面外的向量**b**。此时矩阵***A***为奇异阵或称不可逆矩阵。在矩阵***A***不可逆条件下，不是所有的**b**都能令方程***A*x**=**b**有解。

对n维情形则是，n个列向量如果相互独立——“线性无关”，则方程组有解。否则这n个列向量起不到n个的作用，其线性组合无法充满n维空间，方程组未必有解。

*从行图像的角度来看，三元方程组是否有解意味着什么？当方程所代表的三个平面相交于一点时方程有唯一解；三个平面中至少两个平行则方程无解；平面的两两交线互相平行方程也无解；三个平面交于一条直线则方程有无穷多解。*

* 都是示意图，来看看GS和Lay的作图差异有多大吧……*

![](https://pic2.zhimg.com/v2-0a7b3add1122aa47c7345a16831ba761_b.jpg)

- **矩阵与向量的乘法**

列图像：***A*x**是矩阵***A***列向量的线性组合 ： $\left[ {\begin{array}{*{20}{c}} 2&5\\ 1&3 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1\\ 2 \end{array}} \right] = 1\left[ {\begin{array}{*{20}{c}} 2\\ 1 \end{array}} \right] + 2\left[ {\begin{array}{*{20}{c}} 5\\ 3 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {12}\\ 7 \end{array}} \right] $ 

也可以通过将矩阵***A***的行向量和**x**向量进行点积来计算：

$\left[ {\begin{array}{*{20}{c}} 2&5\\ 1&3 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1\\ 2 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {1 \times 2 + 2 \times 5}\\ {1 \times 1 + 2 \times 3} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {12}\\ 7 \end{array}} \right]$ 

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

# 第03讲 矩阵的乘法和逆矩阵** Multiplication & inverse matrices 

[优酷视频](https://v.youku.com/v_show/id_XNDA0MjQ1MTcy.html?spm=a2h0k.11417342.soresults.dselectbutton&s=46136e60aecd11e19013)

- **矩阵乘法 Matrix multiplication**

我们通过四种方法讨论如何使矩阵***A***与***B***相乘得到矩阵***C***。其中***A***为mxn（m行n列）矩阵，而***B***为nxp矩阵，则***C***为mxp矩阵，记cij为矩阵***C***中第i行第j列的元素。

**1)标准方法（行乘以列）**

矩阵乘法的标准计算方法是通过矩阵***A***第i行的行向量和矩阵***B ***第j列的列向量点积得到cij。

${c_{ij}} = \sum\limits_{k = 1}^n {{a_{ik}}{b_{kj}}}  = {a_{i1}}{b_{1j}} + {a_{i2}}{b_{2j}} + {a_{i3}}{b_{3j}} +  \ldots  \ldots $ 

举例

![](https://pic4.zhimg.com/v2-5b54ac3095ee9df2574d35d0b239c51f_b.jpg)

${c_{34}} = row3*col4 = \sum\limits_{k = 1}^n {{a_{3k}}{b_{k4}}}  = {a_{31}}{b_{14}} + {a_{32}}{b_{24}} + {a_{33}}{b_{34}} +  \ldots  \ldots $ 

> 所谓标准方法就是矩阵乘法的运算规则，下面扯几句矩阵代数运算的淡。念书的时候，学到矩阵代数，同桌问我：“矩阵运算怎么这么奇怪，只有同样型号的矩阵（指同为mxn）可以做加法，但是不同型号的矩阵却可以做乘法，话说这不同型号的矩阵为啥要做这种复杂的乘法？数乘一个矩阵为啥其中每一个元素都要乘以这个数，而行列式则不是？”我后来在A.D.亚历山大洛夫编著的《数学：它的内容，方法和意义》第三卷中找到了答案。
> 先补一下矩阵的加法和数乘规则：

![](https://pic2.zhimg.com/v2-7280c38ea402861970808e633a0ffbf9_b.jpg)

> 本质上矩阵的代数运算就是线性方程组的运算：

![](https://pic1.zhimg.com/v2-effbeb09bd84814cef315618ecdb513c_b.jpg)

> 而矩阵乘法可以视为给线性方程组做变量替换

![](https://pic1.zhimg.com/v2-64bf4f7a2a50badeea9f6fd6b2b7aa84_b.jpg)

> 矩阵乘法符合结合律、分配率，但是不遵守交换律，这些通常通过定义加以证明，即将等号两侧矩阵的元素乘开，比较对应元素，从而得出相等或者不等的结论。我们也可以从变量替换的角度思考一下矩阵乘法运算定律。比如结合律，若方程组有如下关系**u**=***E*w**，**w**=***D*y**，**y**=***A*x**，则做变量替换可有**u**=***E*w**=***ED*y**=***EDA*x**。结合律为(***ED***)***A***=***E***(***DA***)，它表达的意思就是替换环节无论是先把**u**表示成***ED*y**，再表示成**x**的表达式，又或者先把**w**表示成***DA*x**，再把公式带入**u**=***E*w**都是等效的。分配率也一样，先做加法再进行变量替换，或者先做变量替换再相加也是等效的。但是交换律就不行了，别说矩阵的尺寸可能导致交换顺序后不能进行乘法运算，即使能进行乘法，变量替换的关系也完全不对了。

**2)列操作**

列操作是指矩阵***C***的第j列是通过矩阵***A***乘以矩阵***B***第j列的列向量得到的。这表明矩阵***C***的列向量是矩阵***A***列向量的线性组合，组合的“权”就是矩阵***B***第j列的各个分量。

$\boldsymbol{AB} = \boldsymbol{A}\left[ {\begin{array}{*{20}{c}} {{b_1}}&{{b_2}}&{...}&{{b_p}} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {\boldsymbol{A}{b_1}}&{\boldsymbol{A}{b_2}}&{...}&{\boldsymbol{A}{b_p}} \end{array}} \right]$ 

上式中**b**i，***A*b**i均为列向量，其中

![](https://pic4.zhimg.com/v2-bb3f57a3c1b2104ab5ba90dc97261e53_b.jpg)

为矩阵***A***中列向量的线性组合

**3)行操作**

行操作是指矩阵***C***的第i行是通过矩阵***A***的第i行乘以矩阵***B***得到的。这表明矩阵***C***的行向量是矩阵***B***行向量的线性组合。

$\boldsymbol{AB} = \left[ {\begin{array}{*{20}{c}} {{a_1}}\\ {{a_2}}\\  \vdots \\  \vdots \\ {{a_m}} \end{array}} \right]\boldsymbol{B} = \left[ {\begin{array}{*{20}{c}} {{a_1}\boldsymbol{B} }\\ {{a_2}\boldsymbol{B} }\\  \vdots \\  \vdots \\ {{a_m}\boldsymbol{B} } \end{array}} \right]$ 

此处**a**i和**a**i***B***为行向量

![](https://pic1.zhimg.com/v2-3abfb6d65e47b16cf3cc798d4d9687ac_b.jpg)

**4)列乘以行**

矩阵***A***的第k列是一个m1的向量，而矩阵***B***第k行是一个1p的向量，两向量相乘会得到一个矩阵***Ck***，将所有的n个矩阵相加记得到***C***。

$\boldsymbol{AB} = \sum\limits_{k = 1}^n {\left[ {\begin{array}{*{20}{c}} {{a_{1k}}}\\  \vdots \\ {{a_{mk}}} \end{array}} \right]} \left[ {\begin{array}{*{20}{c}} {{b_{k1}}}& \cdots &{{b_{kp}}} \end{array}} \right]$ 

> 可以从矩阵乘法对加法的分配率推导出来。

- **分块乘法block multiplication**

如果将矩阵***A***和矩阵***B***划分为严格匹配的区块，则矩阵乘法可以通过分块的乘法加以实现。

![](https://pic2.zhimg.com/v2-2cbfa5fbc9499e554866bcae08c29659_b.jpg)

其中***C***1=***A***1***B***1+***A***2***B***3，计算方法与标准算法中矩阵里元素的操作方式相同。

> 之前没有提到一点，就是因为矩阵乘法规则有点小复杂，在手算计算过程中有可能会串行，我们不可能每一次都如下图这样认真标注。

![](https://pic2.zhimg.com/v2-07b2df7a3abc39272bb8a1244fc8851d_b.jpg)

> 一个比较好的小技巧就是把***B***矩阵的位置改变一下，这样矩阵***C***中每一个元素所对应***A***和***B***中的行与列就变得非常清楚了。我在wiki百科中看到了这张图，MIT多元微积分课程上老师也提到了这种方法。

![](https://pic2.zhimg.com/v2-37f677bcfb6ec22250541abfcf7be1ed_b.jpg)

> 这里我们可以利用这种小技巧来帮助理解矩阵的分块乘法：

![](https://pic3.zhimg.com/v2-f41118cd00bf33445b7f9c2734c4275e_b.jpg)

> 可以看到***C***1就是经过***C***1=***A***1***B***1+***A***2***B***3的运算计算出来的，***A***1中的元素只和***B***1的元素进行运算，***A***2只和***B***3进行运算，***C***1为两者加和。

- **逆矩阵 Inverse**

如果矩阵***A***是方阵，若存在逆矩阵 ${\boldsymbol{A}^{ - 1}}$ ，使得 ${\boldsymbol{A}^{ - 1}}\boldsymbol{A} = \boldsymbol{I} =\boldsymbol{A}{\boldsymbol{A}^{ - 1}}$ （左逆矩阵等于右逆矩阵）。我们称矩阵***A***可逆（invertible）或者矩阵***A***非奇异（nonsingular）。

反之，如果***A***为奇异（singular），则其没有逆矩阵。它的行列式为**0**。另一个等价的说法是，***A***为奇异阵，则方程***A*x**=**0**存在非零解**x**。例如：

$\left[ {\begin{array}{*{20}{c}} 1&3\\ 2&6 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{\rm{ - }}3}\\ 1 \end{array}} \right]{\rm{ = }}\left[ {\begin{array}{*{20}{c}} 0\\ 0 \end{array}} \right]$ 

在这个二阶矩阵的例子中，两个列向量排列在同一方向上。不可逆矩阵中总有列向量对生成线性组合没有贡献，等价的说法还有：不可逆矩阵的列向量可以通过线性组合得到**0**。

换而言之，若矩阵***A***存在逆矩阵，则方程***A*x**=**0**只有零解。证明：反设其存在非零解**x**，则有 $\boldsymbol{x}= ({\boldsymbol{A}^{ - 1}}\boldsymbol{A})\boldsymbol{x} = {\boldsymbol{A}^{ - 1}}\boldsymbol{A}\boldsymbol{x} = {\boldsymbol{A}^{ - 1}}\boldsymbol{0} = \boldsymbol{0}$ ，矛盾。

对于可逆矩阵，求它的逆矩阵是一个重要的问题。

$\begin{array}{l} \left[ {\begin{array}{*{20}{c}} 1&3\\ 2&7 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} a&c\\ b&d \end{array}} \right]{\rm{ = }}\left[ {\begin{array}{*{20}{c}} 1&0\\ 0&1 \end{array}} \right]\\ \begin{array}{*{20}{r}} {}&\boldsymbol{A}&{}&{}&{{\boldsymbol{A}^{ - 1}}}&{}&{}&\boldsymbol{I}&{}&{}&{}&{} \end{array} \end{array}$ 

从“列操作”的角度来看，求逆矩阵过程其实和求***A*x**=**b**相同，只是这里**x**为矩阵${\boldsymbol{A}^{ - 1}}$ 的第j列，而**b**为单位阵***I ***的第j列。

**高斯-若尔当消元法 Gauss-Jordan Elimination**

对于前面的二阶矩阵，求逆相当于两组方程：

$\left[ {\begin{array}{*{20}{c}} 1&3\\ 2&7 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} a\\ b \end{array}} \right]{\rm{ = }}\left[ {\begin{array}{*{20}{c}} 1\\ 0 \end{array}} \right]$ 和 $\left[ {\begin{array}{*{20}{c}} 1&3\\ 2&7 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} c\\ d \end{array}} \right]{\rm{ = }}\left[ {\begin{array}{*{20}{c}} 0\\ 1 \end{array}} \right]$ 

Gauss-Jordan消元法可以同时处理两个方程：

![](https://pic1.zhimg.com/v2-6a4e74f23d7e17bb2bdcb33baee6745c_b.jpg)

在用高斯消元法的到上三角矩阵之后，按照若尔当的做法继续消元，用第一行减去第二行的若干倍，最后原矩阵变为单位阵，这时右侧的矩阵即为逆矩阵。

对***A***进行一系列消元操作，相当于左乘消元矩阵***E***，此时消元的结果为***EA***=***I***，因为右侧矩阵也进行了同样消元操作，也等于左乘矩阵***E***，则右侧矩阵为***EI***=***E***。由***EA***=***I ***可知这里的***E***就是***A***的逆矩阵，因此右侧矩阵给出的就是逆矩阵${\boldsymbol{E}=\boldsymbol{A}^{ - 1}}$ 。

![](https://pic4.zhimg.com/v2-826083064defbfed5a57867715a62c43_b.jpg)

# 第四讲 矩阵的LU分解 Factorization into ***A***=***LU***

[04 A的LU分解](https://v.youku.com/v_show/id_XNDA0Mjk2NDEy.html?spm=a2h0k.11417342.soresults.dselectbutton&s=46136e60aecd11e19013)

本节的主要目的是从矩阵的角度理解高斯消元法，最后找到所谓的***L***矩阵，使得矩阵***A***可以转变为上三角阵***U***。即完成***LU***分解得到***A***=***LU***。

首先继续了解一些矩阵乘法和逆矩阵的相关内容。

- **矩阵乘积的逆矩阵 Inverse of a product**

${(\boldsymbol{AB})^{ - 1}} = {\boldsymbol{B}^{ - 1}}{\boldsymbol{A}^{ - 1}}$ 

$\boldsymbol{AB}{\boldsymbol{B}^{ - 1}}{\boldsymbol{A}^{ - 1}} = \boldsymbol{A}(\boldsymbol{B}{\boldsymbol{B}^{ - 1}}){\boldsymbol{A}^{ - 1}} = \boldsymbol{I}$ 比较等式两端可得${(\boldsymbol{AB})^{ - 1}} = {\boldsymbol{B}^{ - 1}}{\boldsymbol{A}^{ - 1}}$ 。

> **矩阵乘积的转置 Transpose of a product**
> （本讲要用到的只是转置矩阵求逆的公式，把相关内容放在这里做个简介，方便大家理解。GS在下一讲还会讲到转置。）
> 矩阵***A***的转置矩阵记为即 ${\boldsymbol{A}^T} $ ，对矩阵进行转置就是将**A**矩阵的行变为 ${\boldsymbol{A}^T} $的列，则完成后***A***的列也就成为了 ${\boldsymbol{A}^T} $的行，看起来矩阵如同沿着对角线进行了翻转。

$\boldsymbol{A} = \left[ {\begin{array}{*{20}{c}} 2&1&4\\ 0&0&3 \end{array}} \right]$ 则 ${\boldsymbol{A}^T} = \left[ {\begin{array}{*{20}{c}} 2&0\\ 1&0\\ 4&3 \end{array}} \right]$ 

> 其数学表达式为$\boldsymbol{A}_{ij}^T = {\boldsymbol{A}_{ji}}$ ，即 ${\boldsymbol{A}^T} $ 的第i行j列的元素为原矩阵***A***中第j行i列的元素。
> ${(\boldsymbol{AB})^{ T}} = {\boldsymbol{B}^{T}}{\boldsymbol{A}^{ T}}$ 可以用定义证明。把上次课介绍的那个乘法小技巧的图片按照乘积矩阵的对角线翻转也看得一清二楚。

![](https://pic2.zhimg.com/v2-25fc9e56f2c5e35d829b9727347a3fb9_b.jpg)

- **转置矩阵的逆矩阵 Inverse of a transpose**

${({\boldsymbol{A}^T})^{ - 1}} = {({\boldsymbol{A}^{ - 1}})^T}$ 

$\boldsymbol{A}{\boldsymbol{A}^{ - 1}}  = \boldsymbol{I}$ 两边取转置，并应用积的转置公式，得到${({\boldsymbol{A}^{-1}})^{T}} {({\boldsymbol{A}^{T}})}= {\boldsymbol{I}}$。根据逆矩阵定义得到${({\boldsymbol{A}^T})^{ - 1}} = {({\boldsymbol{A}^{ - 1}})^T}$

- **矩阵的LU分解**

我们已经看到了如何应用消元法将矩阵***A***转变为上三角阵***U***，这就引出了矩阵的***LU***分解，它是理解矩阵***A***性质的重要方法。

> 可以将矩阵的分解类比为多项式的因式分解，分解后的结果可以让我们更容易看清“解”的状态。

在没有行交换的情况下，矩阵A通过左乘一系列消元矩阵***E***ij可以转化为***U***。在二阶矩阵中，进行一次消元操作即可达到这一效果。

$\begin{array}{l} \left[ {\begin{array}{*{20}{c}} 1&0\\ {{\rm{ - }}4}&1 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 2&1\\ 8&7 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 2&1\\ 0&3 \end{array}} \right]\\ \begin{array}{*{20}{r}} {}&{{\boldsymbol{E}_{21}}}&&{}&{}\boldsymbol{A}&{}&{}&\boldsymbol{U}&{}&{} \end{array} \end{array}$ 

在等式两侧左乘 $\boldsymbol{E}_{21}^{ - 1}$ ，得到 $\boldsymbol{E}_{21}^{ - 1}\boldsymbol{E}_{21}\boldsymbol{A}= \boldsymbol{E}_{21}^{ - 1}\boldsymbol{U}$即$\boldsymbol{A}= \boldsymbol{E}_{21}^{ - 1}\boldsymbol{U}$。就得到了矩阵***A***的***LU***分解结果。

> $\boldsymbol{E}_{21}^{ - 1}$ 是$\boldsymbol{E}_{21}$ 的逆向操作，即左乘$\boldsymbol{E}_{21}$ 使得矩阵**A**第二行[8,7]减去第一行的4倍得到“新第二行”[0,3]，那么再左乘$\boldsymbol{E}_{21}^{ - 1}$可以使得”新第二行”[0,3]加上“第一行”的4倍又变回原第二行的数值[8,7]。

$\begin{array}{l} \left[ {\begin{array}{*{20}{c}} 2&1\\ 8&7 \end{array}} \right] = \left[ {\begin{array}{*{20}{r}} 1&0\\ 4&1 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 2&1\\ 0&3 \end{array}} \right]\\ \begin{array}{*{20}{r}} {}&{}\boldsymbol{A}&{}&{}&{}&\boldsymbol{L}&{}&{}&\boldsymbol{U}&{} \end{array} \end{array}$ 

其中***U***为上三角阵（Upper triangular matrix），主元依次排列于它的对角线上，$\boldsymbol{E}_{21}^{ - 1}$即***L***为下三角阵（Lower triangular matrix）。有时我们也通过分解得到对角阵***D***（diagonal matrix）,例如

$\begin{array}{l} \left[ {\begin{array}{*{20}{c}} 2&1\\ 8&7 \end{array}} \right] = \left[ {\begin{array}{*{20}{r}} 1&0\\ 4&1 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 2&0\\ 0&3 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1&{1/2}\\ 0&1 \end{array}} \right]\\ \begin{array}{*{20}{r}} {}&\boldsymbol{A}&{}&{}&{}&\boldsymbol{L}&{}&{}&\boldsymbol{D}&{}&{}&\boldsymbol{U}&{}&{} \end{array} \end{array}$ 

对于三阶矩阵不需要换行进行消元的情况则有：

${\boldsymbol{E}_{32}}({\boldsymbol{E}_{31}}({\boldsymbol{E}_{21}}\boldsymbol{A})) = \boldsymbol{U}$ ，左乘逆矩阵可得$\boldsymbol{A} = \boldsymbol{E}_{21}^{ - 1}\boldsymbol{E}_{31}^{ - 1}\boldsymbol{E}_{32}^{ - 1}\boldsymbol{U} = \boldsymbol{LU}$ 

设定一组消元矩阵，其中***E31***为单位阵***I***，其它两个消元矩阵如下：

$\begin{array}{l} \left[ {\begin{array}{*{20}{r}} 1&0&0\\ 0&1&0\\ 0&{{\rm{ - }}5}&1 \end{array}} \right]\left[ {\begin{array}{*{20}{r}} 1&0&0\\ {{\rm{ - }}2}&1&0\\ 0&0&1 \end{array}} \right] = \left[ {\begin{array}{*{20}{r}} 1&0&0\\ {{\rm{ - }}2}&1&0\\ {10}&{{\rm{ - }}5}&1 \end{array}} \right]\\ \begin{array}{*{20}{r}} {}&{}&{{\boldsymbol{E}_{32}}}&{}&{}&{}&{{\boldsymbol{E}_{21}}}&{}&{}&{}&{}&{}&\boldsymbol{E}&{}&{}&{} \end{array} \end{array}$ 

可以看到在消元矩阵E的左下角出现了数10。它的出现是由于第一步操作***E21***中“第二行”减去了2倍的“第一行”得到了“新第二行”。**row2**-2**row1**=**newrow2**,而在第二步操作***E32***中第三行减去了5倍的“新第二行”，这相当于减去5倍的“原第二行”并减去5倍的“（-2）倍原第一行”，**10**就出现在这里。

**row3**-5**newrow2**=**row3**-5(**row2**-2**row1**)=**row3**-5**row2**+***10 *row1**

在右侧操作则不会有这种情况发生，运算顺序会发生变化， $\boldsymbol{L} = {\boldsymbol{E}^{ - 1}} = \boldsymbol{E}_{21}^{ - 1}\boldsymbol{E}_{32}^{ - 1}$ 。

$\begin{array}{l} \left[ {\begin{array}{*{20}{r}} 1&0&0\\ 2&1&0\\ 0&0&1 \end{array}} \right]\left[ {\begin{array}{*{20}{r}} 1&0&0\\ 0&1&0\\ 0&5&1 \end{array}} \right] = \left[ {\begin{array}{*{20}{r}} 1&0&0\\ 2&1&0\\ 0&5&1 \end{array}} \right]\\ \begin{array}{*{20}{r}} {}&{\boldsymbol{E}_{21}^{ - 1}}&{}&{}&{}&{\boldsymbol{E}_{32}^{ - 1}}&{}&{}&{}&{}&\boldsymbol{L}&{}&{} \end{array} \end{array}$ 

如果没有行交换操作，则消元矩阵的因子可以直接写入矩阵***L***。没有多余的交叉项出现是***LU***分解要优于***EA***=***U***这种形式的原因之一。

- **消元法所需运算量**

在一些应用中我们需要处理超大型矩阵，即使用计算机来处理这一问题，也需要评估所需的计算量。

如果我们把“先乘后减”大致记为一次运算，那么对于一个nxn矩阵，对于一行进行消元要进行n次运算，由于有n行所以进行了nxn次运算，结果得到了第一列除第一主元外都消成0的矩阵。随后开始对除第一行第一列之外的剩余部分进行消元，这相当于一个(n-1)x(n-1)的矩阵，那么就要进行(n-1)x(n-1)次运算，以此类推。

最后需要的运算次数为1x1+2x2+……+nxn，利用积分公式可以估算其数值。

${1^2} + {2^2} + ... + {n^2} = \sum\limits_{i = 1}^n {{i^2} \approx \int\limits_0^n {{x^2}dx = \frac{1}{3}} } {n^3}$ 

> 这里算是个灵活使用数学工具的例子，我看到完全平方的求和，就一直在回忆公式，但其实作为估算采用积分公式就很方便了。有时候应用数学工具就像开车，保证你正常行驶主要靠驾驶技能，而不是你手边的一本《交规》，熟练驾驶但是不遵守交规很容易出错，交规倒背如流却没有驾驶技能则往往寸步难行。
> 再扯几句淡。在统计学中经常用到斯特林公式（Stirling's approximation），它用来评估和近似阶乘的大小 $n! \sim \sqrt {2\pi n} {\left( {\frac{n}{e}} \right)^n}$ 。如果你去阅读Stirling公式的发展历程和证明过程，就会意识到级数、极限和微积分中间的紧密联系，感兴趣可以看一看。

等号右侧向量**b**的行变换大致需要nxn次运算。

- **行转换 Row exchanges**

如果主元的位置出现了0，就需要进行“行交换”。我们可以通过左乘一个置换矩阵（Permutation Matrix）实现“行交换”的操作。例如

${\boldsymbol{P}_{21}} = \left[ {\begin{array}{*{20}{r}} 0&1&0\\ 1&0&0\\ 0&0&1 \end{array}} \right]$ 

可以实现33矩阵的第一行与第二行的交换。所有的33的置换矩阵包括：

$\left[ {\begin{array}{*{20}{c}} 1&0&0\\ 0&1&0\\ 0&0&1 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1&0&0\\ 0&0&1\\ 0&1&0 \end{array}} \right]\left[ {\begin{array}{*{20}{r}} 0&1&0\\ 1&0&0\\ 0&0&1 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 0&1&0\\ 0&0&1\\ 1&0&0 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 0&0&1\\ 1&0&0\\ 0&1&0 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 0&0&1\\ 0&1&0\\ 1&0&0 \end{array}} \right]$ 

对于nxn矩阵存在着n！个置换矩阵。

> 置换矩阵每一行或者每一列只有一个元素是1，其它都是0，从第一行选一个位置设定为1有n个选择，第二行则只剩下n-1个选择，以此类推，最终有n！种可能。

对于某阶的置换矩阵集合而言，置换矩阵的两两乘积仍在这个集合中，置换矩阵的逆矩阵也在此集合中。置换矩阵的逆矩阵即为它的转置 ${\boldsymbol{P}^{ - 1}} = {\boldsymbol{P}^T}$ 。

> 可以用前面介绍过的乘法运算小技巧来理解这件事情

![](https://pic4.zhimg.com/v2-cefa530328760f6b9816e54458f1ccef_b.jpg)

> ***P***的第i行和$ \boldsymbol{P}^{-1}$ 的第i列相乘会得到1，与其他列相乘都得到0，所以$ \boldsymbol{P}^{-1}$ 的第i列只能是***P***的第i行行向量的转置（让分量1出现在向量里的相同位置），其他各列以此类推，则***P***的每一个行向量转置就得到$ \boldsymbol{P}^{-1}$ 的列向量，这也就是矩阵转置 $ \boldsymbol{P}^T$ 的定义。因此可得 ${\boldsymbol{P}^{ - 1}} = {\boldsymbol{P}^T}$ 。

# 第05讲 转置、置换和空间** Transposes, permutations, spaces 

[网易公开课](http://open.163.com/movie/2010/11/J/K/M6V0BQC4M_M6V29FRJK.html)

本节的将引入向量空间（vector spaces）和子空间（subspaces）。

- **置换 Permutations**

当应用消元法求解方程组的时候我们需要通过行交换将0从主元位置移走。左乘一个置换阵可以实现行交换的操作。（为了满足数值计算的要求，Matlab甚至会对接近于0的非零主元做行交换）因此我们的***LU***分解由***A***=***LU***变为***PA***=***LU***。其中的***P***就是对***A***的行向量进行重新排序的置换矩阵。

> 我之前看到这里的时候有个疑惑，如果在消元的过程中进行“行交换”，那么不是意味着**P**矩阵存在于一堆*** E ***矩阵之间么***EEEPEPEA***=***U***，矩阵乘法不符合交换律，你怎么保证能把**P**提出来变成***PA***=***LU***呢。同桌说可以假想在消元过程中你已经完全知道需要怎么进行“行交换”之后，我们重新开始做矩阵分解，这一次先对***A***进行“行交换”得到***A****，这时候对***A****消元，就不用再进行“行交换”了，于是有***PA***=***A****=***LU***。

置换矩阵***P***是通过对单位阵进行“行交换”得到的。对于nxn矩阵存在着n!个置换矩阵。置换矩阵具有特殊性质${\boldsymbol{P}^{-1}}={\boldsymbol{P}^T}$ 即${\boldsymbol{P}^T}{\boldsymbol{P}}={\boldsymbol{I}}$。

- **转置 Transposes**

矩阵***A***的转置矩阵记为 ${\boldsymbol{A}^T}$ ，对矩阵进行转置就是将***A***矩阵的行变为${\boldsymbol{A}^T}$ 的列，则完成后***A***的列也就成为了${\boldsymbol{A}^T}$ 的行，看起来矩阵如同沿着对角线进行了翻转。

其数学表达式为 ${({\boldsymbol{A}^T})_{ij}} = {\boldsymbol{A}_{ji}}$ ，即${\boldsymbol{A}^T}$ 的第i行j列的元素为原矩阵***A***中第j行i列的元素。

${\left[ {\begin{array}{*{20}{c}} 1&3\\ 2&3\\ 4&1 \end{array}} \right]^T}{\rm{ = }}\left[ {\begin{array}{*{20}{c}} 1&2&4\\ 3&3&1 \end{array}} \right]$ 

若***A***是对称矩阵则有${{\boldsymbol{A}^T}} = {\boldsymbol{A}}$ 。

矩阵乘积的转置${{\boldsymbol{(AB)}^T}} = {\boldsymbol{B}^T\boldsymbol{A}^T}$ ，

给定一个矩阵***R***，***R***可以不是方阵，则乘积${\boldsymbol{R}^T\boldsymbol{R}}$ 一定是对称阵。

${({\boldsymbol{R}^T}\boldsymbol{R})^T} = {\boldsymbol{R}^T}{({\boldsymbol{R}^T})^T} = {\boldsymbol{R}^T}\boldsymbol{R}$ 

- **向量空间 Vector spaces**

我们可以对向量进行所谓“线性运算”，即通过加和（**v**+**w**）与数乘运算（3**v**）得到向量的线性组合。向量空间对线性运算封闭，即空间内向量进行线性运算得到的向量仍在空间之内。

**R**2即为向量空间，它是具有两个实数分量的所有向量（二维实向量）的集合。

例如 $\left[ {\begin{array}{*{20}{c}} 3\\ 2 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0\\ 0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} \pi \\ e \end{array}} \right]$ ……

向量 $\left[ {\begin{array}{*{20}{c}} a\\ b \end{array}} \right]$ 的图像是从原点出发到点(a,b)的箭头，其中第一分量a为横轴坐标，第二分量b为纵轴坐标。空间**R**2的图像为整个x-y平面。

所有向量空间必然包含零向量，因为任何向量数乘0或者加上反向量都会得到零向量，而因为向量空间对线性运算封闭，所以零向量必属于向量空间。

**R**3是向量空间，它是具有三个实数分量的所有向量的集合。

**R**n是向量空间，它是具有n个实数分量的所有向量的集合。

反例：**R**2中的第一象限则不是一个向量空间。

- **子空间 Subspaces**

包含于向量空间之内的一个向量空间称为原向量空间的一个子空间。例如用实数c数乘**R**2空间中向量**v**所得到的向量集合就是**R**2空间的一个子空间，其图像为二维平面上穿过原点的一条直线，它对于线性运算封闭。

反例：**R**2中不穿过原点的直线就不是向量空间。子空间必须包含零向量，原因就是数乘0的到的零向量必须处于子空间中。

**R**2的子空间包括：

- **R**2空间本身
- 过原点的一条直线（这是**R**2空间中的一条直线，与**R**1空间有区别）
- 原点 仅包含0向量 Z

**R**3的子空间包括：

- **R**3空间本身 3维
- 过原点的一个平面 2维
- 过原点的一条直线 1维
- 原点 仅包含0向量 Z

![](https://pic2.zhimg.com/v2-9292ea5104e8b1a191bad6a895c2b325_b.jpg)

**列空间 Column spaces**

给定矩阵***A***，其列向量属于**R**3空间，这些列向量和它们的线性组合张成了**R**3空间中的一个子空间，即矩阵***A***的列空间C(***A***)。

如果 $\boldsymbol{A} = \left[ {\begin{array}{*{20}{c}} 1&3\\ 2&3\\ 4&1 \end{array}} \right]$ ，则***A***的列空间是**R**3空间中包含向量 $\left[ {\begin{array}{*{20}{c}} 1\\ 2\\ 4 \end{array}} \right]$ 和 $\left[ {\begin{array}{*{20}{c}} 3\\ 3\\ 1 \end{array}} \right]$ 并穿过原点的平面，空间内包含两向量的所有线性组合。

下面课程的任务就是在列空间和子空间的基础上理解***A*x**=**b**。

# 第06讲 列空间和零空间 Column space & Nullspace 

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

# 第09讲 线性无关，基和维数 

Independence, basis, and dimension

[网易公开课](http://open.163.com/movie/2010/11/C/T/M6V0BQC4M_M6V2ACDCT.html)

向量的线性无关意味着什么？如何用线性无关的概念来帮助我们描述包括零空间在内的子空间。

- **线性无关 Independence**

矩阵***A***为mxn矩阵，其中m<n（因此***A*x**=**b**中未知数个数多于方程数）。则***A***中具有至少一个自由变量，那么***A*x**=**0**一定具有非零解。***A***的列向量可以线性组合得到零向量，所以***A***的列向量是线性相关的。

若 ${c_1}{\boldsymbol{x}_1} + {c_2}{\boldsymbol{x}_2} +  \cdots  + {c_n}{\boldsymbol{x}_n} = \boldsymbol{0}$ 仅在${c_1}= {c_2}=  \cdots  ={c_n}= \boldsymbol{0}$ 时才成立，则称向量**x**1，**x**2……**x**n是线性无关的。若这些向量作为列向量构成矩阵***A***，则方程***A*x**=**0**只有零解**x**=**0**，或称矩阵***A***的零空间只有零向量。换而言之，若存在非零向量**c**，使得***A*c**=**0**，则这个矩阵***A***的列向量线性相关。

在**R**2空间中，两个向量只要不在一条直线上就是线性无关的。（在**R**3中，三个向量线性无关的条件是它们不在一个平面上。）若选定空间**R**2中的三个向量，则他们必然是线性相关的。例如，如下的三个向量**v**1，**v**2和**v**3是线性相关的。

$\begin{array}{l} \boldsymbol{A} = \left[ {\begin{array}{*{20}{r}} 2&1&{2.5}\\ 1&2&{ - 1} \end{array}} \right]\\ \begin{array}{*{20}{r}} {}&{}&{{\boldsymbol{v}_1}}&{{\boldsymbol{v}_2}}&{{\boldsymbol{v}_3}}&{}&{}&{}&{} \end{array} \end{array}$ 

由我们研究方程组得到的结论，此矩阵构成的方程***A*x**=**0**必有非零解，即三个向量线性相关。

如果矩阵***A***的列向量为线性无关，则***A***所有的列均为主元列，没有自由列，矩阵的秩为n。若***A***的列向量为线性相关，则矩阵的秩小于n，并且存在自由列。

- **张成空间 Spanning a space**

当一个空间是由向量**v**1，**v**2……**v**k的所有线性组合组成时，我们称这些向量张成了这个空间。例如矩阵的列向量张成了该矩阵的列空间。

如果向量**v**1，**v**2……**v**k张成空间**S**，则**S**是包含这些向量的最小空间。

- **基与维数Basis &Dimension**

向量空间的基是具有如下两个性质的一组向量**v**1，**v**2……**v**d：

- **v**1，**v**2……**v**d 线性无关
- **v**1，**v**2……**v**d张成该向量空间

空间的基告诉我们了空间的一切信息。

例：**R**3空间

**R**3空间有一组基 $\left[ {\begin{array}{*{20}{c}} 1\\ 0\\ 0 \end{array}} \right]$ ， $\left[ {\begin{array}{*{20}{c}} 0\\ 1\\ 0 \end{array}} \right]$ ， $\left[ {\begin{array}{*{20}{c}} 0\\ 0\\ 1 \end{array}} \right]$ ，

因为它们满足 ${c_1}\left[ {\begin{array}{*{20}{c}} 1\\ 0\\ 0 \end{array}} \right] + {c_2}\left[ {\begin{array}{*{20}{c}} 0\\ 1\\ 0 \end{array}} \right] + {c_3}\left[ {\begin{array}{*{20}{c}} 0\\ 0\\ 1 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 0\\ 0\\ 0 \end{array}} \right]$ 只有零解。并且这三个向量可以张成**R**3空间。

而$\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 2 \end{array}} \right]$ ， $\left[ {\begin{array}{*{20}{c}} 2\\ 2\\ 5 \end{array}} \right]$ ， $\left[ {\begin{array}{*{20}{c}} 3\\ 3\\ 8 \end{array}} \right]$ 则不能构成一组基，因为以它们为列向量组成的矩阵，有两个相同的行，消元肯定有自由列存在，因此这三个向量并非线性无关。

> G.Strang在这里犯了个错误，他以为这三个是线性无关的，最后在第10讲中才进行了更正。当判定线性相关性时，可以随时在矩阵、空间和方程组的概念之间切换，哪个判据更容易判定就用哪个，这里显然矩阵不可逆更容易看出来，因为存在行向量重复的情况。从这里也可以看到行向量线性相关则列向量不可能线性无关，矩阵行空间的维数等于列空间的维数。

若以**R**n空间中的n个向量为列向量构成的矩阵为可逆矩阵，则这些向量可以构成**R**n空间中的一组基。

- **子空间的基 Basis for a subspace**

向量$\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 2 \end{array}} \right]$ ， $\left[ {\begin{array}{*{20}{c}} 2\\ 2\\ 5 \end{array}} \right]$ 可以张成**R**3中的一个平面，但是它们无法成为**R**3空间的一组基。

空间的每一组基都具有相同的向量数，这个数值就是空间的维数（dimension）。所以**R**n空间的每组基都包含n个向量。

- **列空间和零空间的基 Basis of a column space and nullspace**

取***A***= $\left[ {\begin{array}{*{20}{r}} 1&2&3&1\\ 1&1&2&1\\ 1&2&3&1 \end{array}} \right]$ 

**讨论列空间：**矩阵***A***的四个列向量张成了矩阵***A***的列空间，其中第3列和第4列与前两列线性相关，而前两个列向量线性无关。因此前两列为主元列。他们组成了列空间C(***A***)的一组基。矩阵的秩为2。

实际上对于任何矩阵***A***均有：矩阵的秩r=矩阵主元列的数目=列空间的维数

注意：矩阵具有秩rank而不是维数dimension，而空间有维数而不是秩。

当知道了列空间的维数，可以从矩阵列向量中随意选取足够数量的线性无关的向量，它们每一组都可以构成列空间的一组基。

**讨论零空间：**本例中矩阵的列向量不是线性无关的，因此其零空间N(***A***)不止包含零向量。因为可以看出第3列是第1列和第2列的加和。所以向量 $\left[ {\begin{array}{*{20}{c}} { - 1}\\ { - 1}\\ 1\\ 0 \end{array}} \right]$ 必然在零空间N(***A***)之内。同样还可以对x4赋值为1，从而得到 $\left[ {\begin{array}{*{20}{c}} 1\\ 0\\ 0\\ 1 \end{array}} \right]$ 也在零空间之内。它们就是***A*x**=**0**的两个特解。

零空间的维数=自由列的数目=n-r，因此本例中N(***A***)的维数为4-2=2。这两个特解就构成了零空间的一组基。



# 第10讲 四个基本子空间 

The four fundamental subspaces

[网易公开课](http://open.163.com/movie/2010/11/D/T/M6V0BQC4M_M6V2ADFDT.html)

本讲讨论矩阵的四个基本子空间以及他们之间的关系。

- **四个子空间 Four subspaces**

任意的mxn矩阵***A***都定义了四个子空间。

**列空间** Column space C(***A***)

	矩阵***A***的列空间是***A***的列向量的线性组合在 ${\boldsymbol{R}^m}$空间中构成的子空间。

**零空间**Nullspace N(***A***)

	矩阵***A***的零空间是***A*x=0**的所有解**x**在${\boldsymbol{R}^n}$空间中构成的子空间。

**行空间**Row space C( ${\boldsymbol{A}^T}$ )

	矩阵***A***的行空间是***A***的行向量的线性组合在${\boldsymbol{R}^n}$空间中构成的子空间，也就是矩阵 ${\boldsymbol{A}^T}$的列空间。

**左零空间**Left nullspace N( ${\boldsymbol{A}^T}$)

	我们称矩阵 ${\boldsymbol{A}^T}$的零空间为矩阵***A***的左零空间，它是${\boldsymbol{R}^m}$空间中的子空间。

![](https://pic2.zhimg.com/v2-6fa633bb92c68d718c59770efb506e95_b.jpg)

- **基和维数 Basis& Dimension**

**列空间**

矩阵***A***的r个主元列构成了列空间C(***A***)的一组基。dim C(***A***)=r

**零空间**

***A*x**=**0**的一组特解对应于矩阵***A***的n-r个自由列，并构成了零空间的一组基。dim N(***A***)=n-r

**行空间**

我们用矩阵***A***的化简的行阶梯矩阵***R***。

$\boldsymbol{A} = \left[ {\begin{array}{*{20}{r}} 1&2&3&1\\ 1&1&2&1\\ 1&2&3&1 \end{array}} \right] \to ... \to \left[ {\begin{array}{*{20}{r}} 1&0&1&1\\ 0&1&1&0\\ 0&0&0&0 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} I&F\\ 0&0 \end{array}} \right] = \boldsymbol{R}$ 

尽管矩阵***A***和矩阵***R***的列空间不同，但两者行空间相同。***R***的行向量来自于***A***的行向量的线性组合，因为消元操作是可逆的，所以***A***的向量也可以表示为***R***行向量的线性组合。

***R***的前r行阶梯型“行向量”就是矩阵***A***行空间C( ${\boldsymbol{A}^T}$ )的一组基。dim C( ${\boldsymbol{A}^T}$ )=r

**左零空间**

矩阵 ${\boldsymbol{A}^T}$ 有m列，而其秩为r，因此其自由列数目为m-r。所以dim N( ${\boldsymbol{A}^T}$ )=m-r。

左零矩阵是满足 ${\boldsymbol{A}^T}\boldsymbol{y} = \boldsymbol{0}$ 的所有向量**y**的集合。称之为左零矩阵是因为该式可写作${\boldsymbol{y}^T}\boldsymbol{A}= \boldsymbol{0}$，而**y**出现在矩阵***A***左侧。

为找到左零空间的基，我们应用增广矩阵： $\left[ {\begin{array}{*{20}{c}} {{A_{m \times n}}}&{{I_{m \times n}}} \end{array}} \right] \to \left[ {\begin{array}{*{20}{c}} {{R_{m \times n}}}&{{E_{m \times n}}} \end{array}} \right]$ 

我们将***A***通过消元得到矩阵***R***，其消元矩阵记为***E***，即***EA***=***R***。若***A***为方阵，且***R***=***I***，则有 $\boldsymbol{E} = {\boldsymbol{A}^{ - 1}}$ 。在本例中

![](https://pic1.zhimg.com/v2-bb570dd82dd0c6b42611fbbaf9988230_b.jpg)

以“行操作”的观点来看矩阵***E***和***A***的乘法，则矩阵***E***最下面的m-r个行向量使得矩阵***A***的行向量线性组合成为**0**，也就是矩阵***R***最下面的m-r个零向量。本例中，m-r=1。

矩阵***E***的这m-r个行向量满足${\boldsymbol{y}^T}\boldsymbol{A}= \boldsymbol{0}$，它组成了矩阵A左零空间的一组基。

- **新向量空间 New vector space**

所有3x3矩阵构成的集合是一个向量空间，符合对于线性运算封闭，称之为**M**。

**M**的子空间包括：

- 所有的上三角阵
- 所有的对称阵
- 所有的对角阵

对角阵是前两个子空间的交集，其维数为3，具有以下一组基：

$\left[ {\begin{array}{*{20}{r}} 1&0&0\\ 0&0&0\\ 0&0&0 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 0&0&0\\ 0&1&0\\ 0&0&0 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 0&0&0\\ 0&0&0\\ 0&0&1 \end{array}} \right]$ 




> 讨论：当最初告诉我说，矩阵的列秩等于主元数，并且主元列构成了列空间的一组基时，其实我是拒绝的。主元这个东西不是行变换消元得来的么，消元过程列空间不是已经改变了么，为什么所得出**U**的主元数和主元列的位置还能够反映出矩阵***A***列空间的状态呢？
> 这里需要说明的是两点，其一是关于秩的定义有很多在数学上等价但是描述差异很大的说法，在这里我们把“秩”理解为行（列）向量中最大的线性无关向量组的向量数即可，在矩阵***A***行变换消元成梯形阵后，很容易看到行空间内极大无关组之一就是主元所在的那前r行，这r个行向量可以张成行空间，因此行空间的维数与主元数相等都是r，并且前r行构成了行空间的一组基。
> 但是为什么列空间的维数也是r，并且主元列可以构成列空间的一组基呢？这就是要说明的第二点，初等行变换不会改变列向量的线性相关性。为了叙述方便起见，我们假定矩阵***A***列向量的极大无关组就是***A***前r’列的向量（若否可以通过列交换而达成，列交换不会改变线性关系）。则矩阵***A***经过行消元得到梯形矩阵**U**的过程，可以用左乘可逆矩阵**E**来实现，即***EA***=***U***。对等式左侧的矩阵乘法采用列操作的形式进行理解，***E***[**a**1,**a**2,……**a**n]=***U***，其中**a**i为矩阵***A***的第i列。则***U***的前r’列分别为***E*a**1……***E*a**r’。第一步，证明之前线性无关的列向量，行变换之后还无关：反设这些列向量线形相关，即存在非零c1，c2……cr’使方程c1***E*a**1+c2***E*a**2……+cr’***E*a**r’=**0**，等式等价于***E***(c1**a**1+……+ cr’**a**r’)=**0**，等式两端同时乘以**E** 的逆矩阵，则有c1**a**1+c2**a**2……+cr’**a**r’=**0**，但已知前r’列的向量是线性无关的，所以**c**=0，矛盾，因此经过左乘可逆矩阵***E***，即“行变换”，不会改变线性无关的状态。第二步证明类似，就是证明之前线性相关的还相关，没有生成新的线性无关项，此处略去。综上可知，经过行变换列向量极大无关组的向量数仍为r’，即***U***的列空间维度为r’。而从***U***的矩阵形态可知，它的r个主元列线性无关，其列空间的维度为r，因此有r’=r，并且主元列经过逆变换回去得到***A***的主元列也不会改变线性无关的关系，因此***A***的主元列就是***A***列空间的基。
> 我们大致说明了一件事情，就是矩阵的行秩等于其列秩。如果将矩阵***A***消元得到rref，***PA***=***R***，其中***R***= $\left[ {\begin{array}{*{20}{c}} I&F\\ 0&0 \end{array}} \right]$ ，对***R***再进行列变换，可得***PAQ***=***RQ***= $\left[ {\begin{array}{*{20}{c}} I&0\\ 0&0 \end{array}} \right]$ ，最后凹出的这个造型被称为矩阵***A***的相抵标准型，它和***A***具有相同的秩，具有同构的行空间和列空间。你可以视这个标准型为“初代”，在对它进行了可逆的行变换或者列变换之后得到了一系列矩阵，其中就包括老***A***，这个初代的行列空间维数同为r，所以它“繁衍”出来的一系列矩阵的行列空间维数就同为r，所有的矩阵都有它的相抵标准型，所有的矩阵行秩都等于列秩。所以之前我们说过m和n给出了矩阵的尺寸，但是r给出了矩阵的“大小”，它告诉了你矩阵行向量和列向量中真正“管用的”有几个，它告诉了你方程组里管用的方程有几个，解集里面不能随便取的变量是几个，能随便赋值的又是哪几个。
> 再扯几句淡，如果去网上搜索“矩阵的行秩等于列秩究竟意味着什么”，那么你会发现很多看上去完完全全不同的说法，甚至完全不像是在讨论一个问题。之所以有这种感受，其中一个原因是对于秩的定义出发点不同，比如从行列式开始讲起的线代是用行列式来定义“秩”的；而另一个原因是，大家是在线代的不同层面在讨论这件事情。总体而言，G.Strang所讲的这套线代，是偏重于应用数学这个方向，希望通过深入理解矩阵运算，在工程应用的方面能走得更远，后面他引入马尔科夫链、傅里叶、微分方程的内容都是朝着这个方向努力，还有他开设的“计算科学与工程”的课程也是秉持这个理念；与之不同，还有一种讲解线性代数的思路是强调线性算子的核心作用，实际上它是在一个更加抽象的层面来进行讨论和推演，Sheldon Axler 的《Linear algebra done right》（中译本：线性代数应该这样学）就是以这个出发点来写作的书，引领我们走向线代更深入的部分，方便与其他数学分支建立联系。
> 其实数学的学习过程中，我们一直在做着“抽象”这件工作，我们从10个苹果、2头牛这种实际事物中，抽象出数字的概念放下了实物的概念，随后我们抽象出未知数x，y而放下了具体数字的概念，再后来到函数,连x，y的系数都已经被字母替代，到了微积分直接讨论函数之间的联系已经可以暂时放下函数的解析式，再到泛函……每前进一步我们都用一个更加抽象的概念替代一族具象的概念，使得一切操作变得更加简洁（但不一定就好懂），而结果更富普遍意义，但是对于理解能力就有更高的要求。
> 把话说回来，G.Strang讲的线性代数更low么（有人说GS的所讲的不是线性代数的核心而是matlab的核心-_-!）？显然不是的，他将线代的触角已经延伸出去很广的范围，在应用的领域做了非常细致有效的工作，开启了科学家和工程师对线代的正确理解方式。

# 第11讲 矩阵空间、秩1矩阵和小世界图

Matrix Spaces；Rank 1；Small World Graphs

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AJS2T)

扩展一下向量空间的含义。

- **新的向量空间 New vector spaces**

**3x3矩阵空间 3 by 3 matrices**

空间**M**是所有3x3矩阵所构成的空间，**M**的部分子空间包括：

- 所有的上三角阵，记为**U**。
- 所有的对称阵，记为**S**。
- 所有的对角阵，记为**D，**它是前两个子空间的交集。

空间**M**的维数为9，与**R**9空间很类似。我们可以选定它的一组基：

$\left[ {\begin{array}{*{20}{r}} 1&0&0\\ 0&0&0\\ 0&0&0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0&1&0\\ 0&0&0\\ 0&0&0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0&0&1\\ 0&0&0\\ 0&0&0 \end{array}} \right],......\left[ {\begin{array}{*{20}{c}} 0&0&0\\ 0&0&0\\ 0&1&0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0&0&0\\ 0&0&0\\ 0&0&1 \end{array}} \right]$ 

对称阵构成的子空间**S**维数为6，它的一组基为：

$\left[ {\begin{array}{*{20}{r}} 1&0&0\\ 0&0&0\\ 0&0&0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0&1&0\\ 1&0&0\\ 0&0&0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0&0&1\\ 0&0&0\\ 1&0&0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0&0&0\\ 0&1&0\\ 0&0&0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0&0&0\\ 0&0&1\\ 0&1&0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0&0&0\\ 0&0&0\\ 0&0&1 \end{array}} \right]$ 

上三角阵构成的子空间**U**维数也为6，它的一组基为：

$\left[ {\begin{array}{*{20}{r}} 1&0&0\\ 0&0&0\\ 0&0&0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0&1&0\\ 0&0&0\\ 0&0&0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0&0&1\\ 0&0&0\\ 0&0&0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0&0&0\\ 0&1&0\\ 0&0&0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0&0&0\\ 0&0&1\\ 0&0&0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0&0&0\\ 0&0&0\\ 0&0&1 \end{array}} \right]$ 

对角阵构成的子空间**D**维数为3，可以选定**S**和**U**的基的交集为**D**的基。

**S**和**U**的并集，即3x3矩阵中或为上三角阵或为对称阵的矩阵，构成**M**的子空间么？答案是否定的，这就如同在**R**2空间中找出两条直线，询问它们的并集是否构成一个子空间。如果我们将**S**和**U**中所有元素可能构成的加和作为一个集合，可以称为和集**S**+**U**，它是**M**的一个子空间。实际上**S**+**U**就是**M**本身，其维数为9。

$\dim \boldsymbol{S} + \dim \boldsymbol{U} = \dim  \boldsymbol{S} \cap\boldsymbol{U} + \dim ( \boldsymbol{S} + \boldsymbol{U})$ 等式右侧应是和集的维数与交集的维数相加。

- **微分方程 Differential equations**

对于给定的微分方程 $\frac{{{d^2}y}}{{d{x^2}}} + y = 0$ ，求解该方程可以视为求它的零空间。我们可以得到的解为： $y = \cos x$ ， $y = \sin x$ ， $y = {e^{ix}}$ 。

事实上，通解为 $y = {c_1}\cos x + {c_2}\sin x$ ，其中c可以取任意复数。也将解的线性组合构成的空间称为解空间，其维数为2。cosx和sinx可以成为解空间的一组基。这些并不像是向量，它们是函数，但是可以对其进行线性运算，在线性代数的范畴内讨论之。

- **秩1矩阵 Rank one matrices**

矩阵 $\boldsymbol{A} = \left[ {\begin{array}{*{20}{r}} 1&4&5\\ 2&8&{10} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 1\\ 2 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1&4&5 \end{array}} \right]$ ，矩阵的秩为1。 $\dim C(\boldsymbol{A}) = r = \dim C({\boldsymbol{A}^T})$ 

所有的秩1矩阵都可分解 $\boldsymbol{A} = \boldsymbol{U}{\boldsymbol{V}^T}$ ，其中**U**和**V**都是列向量。秩1矩阵的行列式和特征值都很简单，它可以被当作是构建其他矩阵的“积木”。*其实我们在矩阵乘法的第四种形式里面见过它的作用。*例如若存在一个5x17的矩阵***M***，而其秩为4，那么它可以由4个秩1矩阵组合而成。

若矩阵空间**M**为所有的5x17矩阵，那么**M**中所有的秩4矩阵所构成的集合是一个子空间么？答案是否定的，即使加入零矩阵也无法构成子空间，对于两个矩阵的加和，秩4矩阵集合并不封闭。

两个矩阵之和的秩小于等于两个矩阵的秩之和。

在**R**4空间中，所有满足分量之和 ${v_1} + {v_2} + {v_3} + {v_4} = 0$ 的向量**v**= $\left[ {\begin{array}{*{20}{c}} {{v_1}}\\ {{v_2}}\\ {{v_3}}\\ {{v_4}} \end{array}} \right]$ 构成了一个子空间**S**，包含零向量并对线性运算封闭。它是矩阵***A***= $\left[ {\begin{array}{*{20}{c}} 1&1&1&1 \end{array}} \right]$ 的零空间，因为矩阵***A***的秩为1，因此其零空间的秩为n-r=3。零空间的基就是***A*x**=**0**特解： $\left[ {\begin{array}{*{20}{c}} { - 1}\\ 1\\ 0\\ 0 \end{array}} \right]$ ， $\left[ {\begin{array}{*{20}{c}} { - 1}\\ 0\\1\\ 0 \end{array}} \right]$ ， $\left[ {\begin{array}{*{20}{c}} { - 1}\\ 0\\ 0\\ 1 \end{array}} \right]$ 。

> 本例的一个意义就是寻找子空间维数的逆向思路，可以考虑它是不是某个方程的解空间，在这里它是矩阵***A***=$\left[ {\begin{array}{*{20}{c}} 1&1&1&1 \end{array}} \right]$ 的零空间，我们可以从矩阵推出这个空间的维数。

矩阵***A***的列空间为**R**1。左零空间仅包含零向量，维数为0。

- **小世界图 Small world graphs**

介绍小世界图主要是引出图论和线性代数的联系。

在这里，“图”G是结点和边的集合：G=｛结点（nodes），边（edges）｝

![](https://pic1.zhimg.com/v2-4cf27db345b511e1f753df549ef35530_b.jpg)

此图包含5个结点和6条边，我们可以利用一个5x6矩阵完全描述它。

我们可以用图来描述一个实际问题，如果每个人是一个结点，两个人互相认识为一个边，那么整个美国可以以此构成一张大图。我们可以通过这张图来确认两个人之间的最短距离是多少，即两个人需要通过最少几个朋友才能建立联系。G.Strang本人和克林顿之间的距离为2，他的一个朋友是参议员，他认识这个参议员朋友，那个人认识克林顿。班里的学生跟克林顿的距离因此不会大于3。还可以继续算希拉里和莱温斯基……

所谓“六度分割理论”（six degrees of separation）猜想一个人和陌生人之间间隔的点不会超过六个。因此当陌生的两人聊起这种联系都会感叹：“世界真小啊！”这也是“小世界图”这个名字的由来。

> 尽管都在***A*x**=**b**这个单元之下，但是第11和第12两讲的内容与其他几节课程明显有所差异。之前的课程偏重于介绍线性代数的基础知识，主要是将矩阵运算和消元法解线性方程联系起来，告诉我们矩阵不是你常规理解的用于存储的数组，它可以是一种变换操作或者是空间的缩影。而这两节课程告诉我们线性方程组也不是你常规理解的，从一个非常明显的线性关系抽象出来的方程，它可以是从微分方程或者从图论的角度建立起来的关系式，而应用我们在线性代数里面学到的理论，可以处理这些问题，甚至得到一些更加精深的理解。
> 在应用数学工具来解决实际问题的过程中有两个基本步骤：建模和解方程。可以说前面的课程主要在解方程这边，而这后两节课稍稍向建模那个方面靠近了一点。

# 第12讲 图、网络、关联矩阵

Graphs，networks，incidence matrices

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AIUTE)

本讲讨论线性代数在物理系统中的应用。

- **图和网络 Graphs & Networks**

“图”就是“结点”和“边”的一个集合。

![](https://pic4.zhimg.com/v2-d61c945325aaacc121fbc766a369af27_b.jpg)

边线上的箭头代表从结点流出的正方向。

- **关联矩阵（Incidence matrices）**

构造一个矩阵来表示图的内在含义，此矩阵称为关联矩阵，图中每个结点代表一列，每边代表一行。则上图为54矩阵。反过来从这个矩阵出发我们也能画出图。

![](https://pic3.zhimg.com/v2-8632c3dccd23401edc54daa037f72b0a_b.jpg)

源于现实问题的关联矩阵，通常描述了问题的结构。如果我们研究一个很大的图，则会构建一个很大的矩阵，但这个矩阵会是稀疏矩阵。

**考察矩阵的零空间**，即求***A*x**=**0**的解。零空间告诉我们列向量线性组合的状态。

***A*x**= $\left[ {\begin{array}{*{20}{r}} {{x_2} - {x_1}}\\ {{x_3} - {x_2}}\\ {{x_3} - {x_1}}\\ {{x_4} - {x_1}}\\ {{x_4} - {x_3}} \end{array}} \right]{\rm{ = }}\left[ {\begin{array}{*{20}{r}} 0\\ 0\\ 0\\ 0\\ 0 \end{array}} \right]$ 。如果x为结点上的电势，则***A*x**给出了每个边上的电势差。

求解可以得到零空间为一维dim N(***A***)=1，它的基就是 $\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 1\\ 1 \end{array}} \right]$ ，解集则是**x**= $c\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 1\\ 1 \end{array}} \right]$ ，代表等电势，说明等电势条件下不会有电流产生。常数c的确定需要边界条件，比如我们将结点4接地，则x4=0。

> 若求***A*x**=**b**的解，则相当于在给定了电压**b**的情况下，求各点的电势，但实际上我们得不到电势的准确值，因为零空间有常数解**c**，各点得到的电势需要加上常数c，这很类似于求积分要加上常函数，常数值需要边界条件来确定。

矩阵的列数为4，而其零空间的维数为1，则矩阵的秩为3，矩阵第1列，第2列，第4列的列向量线性无关。

> **考察矩阵列空间**，一个重要的问题就是对于什么样的**b**，***A*x**=**b**有解。边①,边②和边③构成了环，这三个行向量线性相关，同样的情况还有边④,边⑤和边③构成的环。于是**b**的分量需要满足b1+b2-b3=0以及b3-b4+b5=0。如果把边①,边②，边④,边⑤构成的大环也表示出来则还可以得到一个等式，但实际上这个等式就是之前这两个等式的组合。这两个等式就是基尔霍夫电压定律（Kirchhoff’s Voltage law）,即环路电势差之和为零。

**矩阵的左零空间**是满足 ${\boldsymbol{A}^T}\boldsymbol{y} = \boldsymbol{0}$ 的向量**y**的集合。因为矩阵 ${\boldsymbol{A}^T}$ 有5列，且矩阵的秩为3，因此矩阵的左零空间维数为2。这反应了行向量的线性关系，整个“图”中，环数为2。

${\boldsymbol{A}^T}\boldsymbol{y} = \left[ {\begin{array}{*{20}{r}} { - 1}&0&{ - 1}&{ - 1}&0\\ 1&{ - 1}&0&0&0\\ 0&1&1&0&{ - 1}\\ 0&0&0&1&1 \end{array}} \right]\left[ {\begin{array}{*{20}{r}} {{y_1}}\\ {{y_2}}\\ {{y_3}}\\ {{y_4}}\\ {{y_5}} \end{array}} \right]{\rm{ = }}\left[ {\begin{array}{*{20}{c}} 0\\ 0\\ 0\\ 0 \end{array}} \right]$ 。**y**的分量的值为“边”上的电流。

在电势差和电流之间建立联系就是欧姆定律（Ohm’s Law）

![](https://pic3.zhimg.com/v2-d2b6cc9a2251daaf39f297a12b94be86_b.jpg)

我们求解 ${\boldsymbol{A}^T}\boldsymbol{y} = \boldsymbol{0}$ 就是在求5个满足基尔霍夫电流定律（Kirchhoff’s Law）的电流值。

![](https://pic1.zhimg.com/v2-2a5caefacd2d9ed476805a4de9974aa8_b.jpg)

${\boldsymbol{A}^T}\boldsymbol{y} = \boldsymbol{0}$ 的方程形式 $\begin{array}{*{20}{r}} { - {y_1} - {y_3} - {y_4}}& = &0\\ {{y_1} - {y_2}}& = &0\\ {{y_2} + {y_3} - {y_5}}& = &0\\ {{y_4} + {y_5}}& = &0 \end{array}$ ，每一个方程关于一个结点，方程表示结点电流值为0，即流入等于流出。

从图上解方程，而不是采用消元法解方程。如果我们设定y1=1，并且让y1，y2和y3组成的回路的“环流“为0，则有y2=1，y3=-1。可解得**y**= $\left[ {\begin{array}{*{20}{r}} 1\\ 1\\ { - 1}\\ 0\\ 0 \end{array}} \right]$ 。取另一个回路的环流为0，则有y3=1，y4=-1，y5=1。**y**= $\left[ {\begin{array}{*{20}{r}} 0\\ 0\\ 1\\ { - 1}\\ 1 \end{array}} \right]$ 。

如果设定y1，y2，y4和y5组成的大回路环流为0，则可以得到另一个向量**y**，而该向量在零空间内，是前两个向量的线性组合。

**考察矩阵的行空间**，因为矩阵r=3，所以存在3个线性无关的向量。第1行，第2行和第4行为线性无关，在“图”中，边①,边②和边④构成了一张小图，这三个边没有形成回路。线性相关问题等价于形成回路。没有回路的小图包含4个结点和3条边，再添加一条边就会产生回路，在矩阵里表现为在第1行，第2行和第4行之上再添加一个行向量就会变为线性相关。没有回路的图称为“树”。

**思考一下维数公式的在“图”中的意义：**

左零空间维数dim N(***A***T)=m-r；

等价于“环”数量=“边”数量-（“结点”数量-1）；

即Eular公式：“结点”-“边”+“环”=1。对所有的“图”都成立。

> 矩阵的秩r=“结点”-1，因为r表示了线性无关的边的数目，也就是“树”中“边”的数目。

![](https://pic1.zhimg.com/v2-9e9e4c1f8f5fb2b3a8d923c46c9a26b8_b.jpg)

之前的讨论都是针对于一个无源的电场，如果加入电源则情况又不同，例如加入电流源相当于将基尔霍夫定律的方程变为 ${\boldsymbol{A}^T}\boldsymbol{y} = \boldsymbol{f}$ ，**f**就是外部流入的电流。

将$\boldsymbol{e} = \boldsymbol{A}\boldsymbol{x}\$， $\boldsymbol{y} = \boldsymbol{C}\boldsymbol{e}\$ ， ${\boldsymbol{A}^T}\boldsymbol{y} = \boldsymbol{f}$ ，三个等式结合得到应用数学中的基本方程${\boldsymbol{A}^T}\boldsymbol{CA}\boldsymbol{x} = \boldsymbol{f}$**。**

> 关于方程${\boldsymbol{A}^T}\boldsymbol{CA}\boldsymbol{x} = \boldsymbol{f}$的更多内容可以阅读G.Strang的书《Computational science and engineering》的第二章。



# 第13讲 复习一  

Exam 1 review

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AJ69K)

本讲为考前复习课，考试范围就是***A*x**=**b**这个单元，重点是长方形矩阵，与此相关的概念包括零空间、左零空间、秩、向量空间、子空间，特别是四个基本子空间。当矩阵为可逆的方阵时，很多性质是一目了然的，但是对于长方形矩阵则需要多加注意。

**问题一：**向量**u**，**v**和**w**是**R**7空间中的非零向量。它们张成了**R**7空间中的一个子空间，那么这个子空间的维数可能是多少？

解答：1，2或者3。空间的基的个数不超过3个，所以其维数也不会超过3。因为是非零向量，所以不能是0。

**问题二：**给定矩阵***U***为5x3阶梯型矩阵，其秩r=3。

*G.Strang 老师这里设定的矩阵**U**就是行最简阶梯型矩阵**R**，他在视频中说这是多年前卷子上的题目，那时候他都写**U**而不是**R**。而挂在OCW网上的11年课堂笔记中已经改为**R**了。此处我们与视频保持相同。*

1.求***U***的零空间N(***U***)

解答：因为列数为3且秩为3，其列向量线性无关，则***U*x**=**0**只有零解，所以其零空间N(***U***)={**0**}={ $\left[ {\begin{array}{*{20}{c}} 0\\ 0\\ 0 \end{array}} \right]$ }

2.令***B***= $\left[ {\begin{array}{*{20}{c}} U\\ {2U} \end{array}} \right]$ ，求***B***的行最简阶梯矩阵？

解答： $\left[ {\begin{array}{*{20}{c}} U\\ 0 \end{array}} \right]$ 

3.***B***的秩？

解答：3。

4.令***C***= $\left[ {\begin{array}{*{20}{c}} U&U\\ U&0 \end{array}} \right]$ ，求它的行最简阶梯矩阵？

解答：进行行消元， $\left[ {\begin{array}{*{20}{c}} U&U\\ U&0 \end{array}} \right] \to \left[ {\begin{array}{*{20}{r}} U&U\\ 0&{ - U} \end{array}} \right] \to \left[ {\begin{array}{*{20}{r}} U&0\\ 0&{ - U} \end{array}} \right] \to \left[ {\begin{array}{*{20}{c}} U&0\\ 0&U \end{array}} \right]$ 

最后还要做的就是将***R***中最后两行的零行向量下移到矩阵最下面。

5.***C***的秩？

解答：6，***B***的秩为3。

6.求***C***左零空间的维数dim N( $\boldsymbol{C}^T$ )?

解答：m=10而r=6，所以dim N( $\boldsymbol{C}^T$ )=4。

**问题三:*A*x**= $\left[ {\begin{array}{*{20}{c}} 2\\ 4\\ 2 \end{array}} \right]$ ，其中**x**= $\left[ {\begin{array}{*{20}{c}} 2\\ 0\\ 0 \end{array}} \right] + c\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 0 \end{array}} \right] + d\left[ {\begin{array}{*{20}{c}} 0\\ 0\\ 1 \end{array}} \right]$ 为通解。

1.矩阵***A***的形状？

解答：矩阵***A***为3x3矩阵，因为**x**的分量数即为***A***的列数，而**b**的分量数为***A***的行数。

2.矩阵***A***的行空间的维数？

解答：从通解的形式可以看出***A***零空间的维数为2，则其行空间的维数为3-2=1。

3.求矩阵***A***？

解答：代入特解***A*** $\left[ {\begin{array}{*{20}{c}} 2\\ 0\\ 0 \end{array}} \right]$ =2x（矩阵***A***列1）= $\left[ {\begin{array}{*{20}{c}} 2\\ 4\\ 2 \end{array}} \right]$ ，可知***A***的第一列（列1）= $\left[ {\begin{array}{*{20}{c}} 1\\ 2\\ 1 \end{array}} \right]$ ，代入零空间的特解***A*** $\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 0 \end{array}} \right]$ =（列1）+（列2）=0，可知（列2）= $\left[ {\begin{array}{*{20}{c}} -1\\ -2\\ -1 \end{array}} \right]$ ，代入另一特解***A*** $\left[ {\begin{array}{*{20}{c}} 0\\ 0\\ 1 \end{array}} \right]$ =（列3）=**0**，可知***A***=$\left[ {\begin{array}{*{20}{r}} 1&{ - 1}&0\\ 2&{ - 2}&0\\ 1&{ - 1}&0 \end{array}} \right]$ 。

4.什么样的向量**b**使得方程***A*x**=**b**有解**x**？

解答：当**b**在矩阵***A***的列空间内的时候，方程有解。本题中**b**需为 $\left[ {\begin{array}{*{20}{c}} 1\\ 2\\ 1 \end{array}} \right]$ 的倍数。本题中矩阵的秩为1，因此零空间很大。请注意系数矩阵满秩的情况，我们曾经花了不少时间进行讨论。

**小问题**

1.***A***是方阵，零空间只有零向量**0**， $\boldsymbol{A}^T$ 的零空间？

解答：***A***转置的零空间也只有零向量。

2.所有的5x5可逆矩阵，是否构成5x5矩阵空间的子空间？

解答：不行，不包含零矩阵***0***，不是子空间。顺便说一下奇异阵也不是一个子空间。

3.判断：如果 $\boldsymbol{B}^2$ =***0***，是否必有矩阵***B***=***0***？

解答：否，反例***B***= $\left[ {\begin{array}{*{20}{c}} 0&1\\ 0&0 \end{array}} \right]$ 。

4.判断：方程组***A*x**=**b**具有n个方程n个未知数，若矩阵***A***的列向量线性无关，则**b**取任意向量，方程均有解。

解答：是，***A***为可逆矩阵，所以 $\boldsymbol{x}=\boldsymbol{A}^{-1}\boldsymbol{b}$ 是唯一解。

**问题四**

矩阵***B***=***CD***= $\left[ {\begin{array}{*{20}{c}} 1&1&0\\ 0&1&0\\ 1&0&1 \end{array}} \right]\left[ {\begin{array}{*{20}{r}} 1&0&{ - 1}&2\\ 0&1&1&{ - 1}\\ 0&0&0&0 \end{array}} \right]$ 

1.给出矩阵***B***零空间的一组基？

解答：因为矩阵***C***为可逆矩阵，因此矩阵***B***零空间与矩阵***D***的零空间相同。矩阵***D***已经是行最简阶梯矩阵了，可解得其零空间的一组基为 $\left[ {\begin{array}{*{20}{r}} 1\\ { - 1}\\ 1\\ 0 \end{array}} \right]$ 和 $\left[ {\begin{array}{*{20}{r}} {-2}\\ { 1}\\ 0\\ 1 \end{array}} \right]$。

*左乘可逆矩阵，相当于对行向量进行可逆的线性组合。既不改变行空间，也不改变零空间。*

*若***x***满足****B*x**=**0***，则有 $\boldsymbol{C}^{-1}\boldsymbol{B}\boldsymbol{x}=\boldsymbol{D}\boldsymbol{x}=\boldsymbol{0}$ ，**B**零空间中的向量均在**D**的零空间中；若***y***满足****D*y**=**0***，则有****CD*y**=**0**=***B*y***，则**D**零空间中的向量均在**B**的零空间中，因此**B**零空间与矩阵**D**的零空间相同。*

2.求***B*x**= $\left[ {\begin{array}{*{20}{c}} 1\\ 0\\ 1 \end{array}} \right]$ 的通解？

解答：向量**b**= $\left[ {\begin{array}{*{20}{c}} 1\\ 0\\ 1 \end{array}} \right]$ 与矩阵***C***第一列列向量完全相同，则问题变为***D*x**= $\left[ {\begin{array}{*{20}{c}} 1\\ 0\\ 0 \end{array}} \right]$ ，求解方程得到一个特解为 $\left[ {\begin{array}{*{20}{c}} 1\\ 0\\ 0\\ 0 \end{array}} \right]$，则其通解就是**x**= $\left[ {\begin{array}{*{20}{c}} 1\\ 0\\ 0\\ 0 \end{array}} \right] + c\left[ {\begin{array}{*{20}{r}} 1\\ { - 1}\\ 1\\ 0 \end{array}} \right] + d\left[ {\begin{array}{*{20}{r}} { - 2}\\ 1\\ 0\\ 1 \end{array}} \right]$ 

**小问题**

1.判断：***A***为方阵，则它的行空间和列空间相同？

解答：否，只是空间的维数相等，但空间不一定相同。反例***B***= $\left[ {\begin{array}{*{20}{c}} 0&1\\ 0&0 \end{array}} \right]$ 。*都是**R**n空间中的r维子空间，但是彼此不一定相同。*对称矩阵的行空间和列空间相同。

2.判断：矩阵***A***和***-A***的四个子空间相同？

解答：是，相同。

3.判断：如果***A***和***B***的四个子空间相同，则***A***一定是***B***的倍数？

解答：错误，***A***和***B***的可以为同阶可逆方阵。

4.如果我们对矩阵***A***中的两行做行交换，四个子空间中不变的是哪些？

解答：是行空间和零空间。

5.为什么向量**v**= $\left[ {\begin{array}{*{20}{c}} 1\\ 2\\ 3 \end{array}} \right]$ 不可能既在矩阵***A***的零空间中，又成为***A***的一个行向量？

解答：反设命题成立。**v**在零空间中，则有***A*v**=**0**，而它**v**也是***A***的行向量，则**v**和这个行向量**v**做乘法得到数值为14而不是0，与***A*v**=**0**矛盾。实际上**v**若在零空间中，则根本不会再零空间中，在下一章中我们将看到矩阵的零空间和其行空间是正交的。


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






# 第15讲 子空间投影

Projections onto subspaces

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AJLJU)

- **投影（射影）Projections**

![](https://pic1.zhimg.com/v2-ceccf98f3c8151a48bfc32d133345ae4_b.jpg)

投影问题的几何解释就是：如何在向量**a**的方向上寻找与向量**b**距离最近的一点。从图中可以看出，这个距离最近的点**p**就位于穿过**b**点并与向量**a**正交的直线与向量**a**所在直线的交点上。这就是**b**在**a**上的投影。如果我们将向量**p**视为**b**的一种近似，则长度**e**=**b**-**p**就是这一近似的误差。

因为 **p** 在向量 **a** 的方向上，因此可以令 **p** = x **a**，而因为它和 **e** 正交，我们可以得到方程：

$$
\boldsymbol{a}^T (\boldsymbol{b} - x \boldsymbol{a}) = 0
$$

解得：x = $\frac{{\boldsymbol{a}^T \boldsymbol{b}}}{{\boldsymbol{a}^T \boldsymbol{a}}}$ ，**p** = $x \boldsymbol{a} = \boldsymbol{a} \frac{{\boldsymbol{a}^T \boldsymbol{b}}}{{\boldsymbol{a}^T \boldsymbol{a}}}$ 。


如果**b**变为原来的2倍，则**p**也变为原来的2倍。而如果**a**变为原来的2倍，**p**不发生变化。从几何上和计算中都会得到验证。

> 本单元前半部分的核心内容就是射影。上一单元我们最核心的内容是认识消元法对于线性方程组的意义，并用矩阵的数学语言实现了消元过程，在那里最核心的策略就是利用矩阵乘法中的行操作来实现这一过程。这里面临类似的情况，我们有一个明确的几何目标，要将向量投影到已知子空间，而这里的策略就是误差向量和已知子空间正交，即两者求点积为0。

- **投影矩阵 Projections matrix**

我们将投影问题用投影矩阵的方式进行描述，即为 **p** = **P** **b**，其中 **P** 为投影矩阵。

**p** = $x \boldsymbol{a} = \boldsymbol{a} \frac{{\boldsymbol{a}^T \boldsymbol{b}}}{{\boldsymbol{a}^T \boldsymbol{a}}}$。则有 **P** = $\frac{{\boldsymbol{a} \boldsymbol{a}^T}}{{\boldsymbol{a}^T \boldsymbol{a}}}$，其分子 $\boldsymbol{a} \boldsymbol{a}^T$ 是一个矩阵，而分母 $\boldsymbol{a}^T \boldsymbol{a}$ 是一个数。

观察这个矩阵可知，矩阵 **P** 的列空间就是向量 **a** 所在的直线，矩阵的秩是 1。投影矩阵 **P** 是一个对称矩阵。另一方面，如果做两次投影则有 $\boldsymbol{P}^2 \boldsymbol{b} = \boldsymbol{P} \boldsymbol{b}$，这是因为第二次投影还在原来的位置。因此矩阵 **P** 有如下性质： $\boldsymbol{P}^2 = \boldsymbol{P}$， $\boldsymbol{P}^T = \boldsymbol{P}$。

- **为什么要投影 Why Project**

如前所述，方程 **A** **x** = **b** 有可能无解，我们需要得到方程的“最优解”。这里的问题在于向量 **A** **x** 一定在矩阵 **A** 的列空间之内，但是 **b** 不一定，因此我们希望将 **b** 投影到 **A** 的列空间得到 **p**，将问题转化为求解 $\boldsymbol{A} \hat{\boldsymbol{x}} = \boldsymbol{p}$。

- **在高维投影 Projection in higher dimensions**
-
在**R**³空间内，如何将向量**b**投影到它距离平面最近的一点**p**？

![Projection](https://pic2.zhimg.com/v2-e1498d1411c5a8df5088d24dad5e8b4d_b.jpg)

如果**a**₁和**a**₂构成了平面的一组基，则平面就是矩阵**A** = [**a**₁ **a**₂] 的列空间。

已知向量**p**在平面内，则有**p** = ${\hat x_1}{\boldsymbol{a}_1} + {\hat x_2}{\boldsymbol{a}_2} = \boldsymbol{A}\boldsymbol{\hat x}$ 。而 $\boldsymbol{e} =\boldsymbol{b}- \boldsymbol{p} = \boldsymbol{b} - \boldsymbol{A}\boldsymbol{\hat x}$ 与投影平面正交（*重点*），因此**e**与**a**₁和**a**₂均正交，因此可以得到： $\boldsymbol{a}_1^T(\boldsymbol{b} - \boldsymbol{A}\boldsymbol{\hat x})=0$并且 $\boldsymbol{a}_2^T(\boldsymbol{b} - \boldsymbol{A}\boldsymbol{\hat x})=0$ 。因为**a**₁和**a**₂分别为矩阵**A**的列向量，即$\boldsymbol{a}_1^T$和$\boldsymbol{a}_2^T$为矩阵$\boldsymbol{A}^T$的行向量，所以将两个方程式写成矩阵形式即为$\boldsymbol{A}^T(\boldsymbol{b} - \boldsymbol{A}\boldsymbol{\hat x})=0$。这与一维投影的方程形式相同。

向量$\boldsymbol{e}= \boldsymbol{b} - \boldsymbol{A}\boldsymbol{\hat x}$ 存在于矩阵$\boldsymbol{A}^T$的零空间N($\boldsymbol{A}^T$)里，从上一讲讨论子空间的正交性可知，向量**e**与矩阵**A**的列空间正交，这也正是方程的意义。

将方程$\boldsymbol{A}^T(\boldsymbol{b} - \boldsymbol{A}\boldsymbol{\hat x})=0$改写，可得$\boldsymbol{A}^T\boldsymbol{A}\boldsymbol{\hat x}=\boldsymbol{A}^T\boldsymbol{b}$。两侧左乘$(\boldsymbol{A}^T\boldsymbol{A})^{-1}$，得到：

$$
\boldsymbol{\hat x}=(\boldsymbol{A}^T\boldsymbol{A})^{-1}\boldsymbol{A}^T\boldsymbol{b}
$$

$$
\boldsymbol{p}=\boldsymbol{A}\boldsymbol{\hat x}=\boldsymbol{A}(\boldsymbol{A}^T\boldsymbol{A})^{-1}\boldsymbol{A}^T\boldsymbol{b}
$$

$$
\boldsymbol{P}=\boldsymbol{A}(\boldsymbol{A}^T\boldsymbol{A})^{-1}\boldsymbol{A}^T
$$

因为矩阵**A**不是方阵，无法简单的用$(\boldsymbol{A}^T\boldsymbol{A})^{-1}=\boldsymbol{A}^{-1}(\boldsymbol{A}^T)^{-1}$ 对投影矩阵公式进行化简。若**A**是可逆方阵，则化简得到**P** = **I**。此时**A**的列空间就是整个**R**ⁿ空间，**b**到这个空间的投影就是其本身，投影矩阵等于单位阵。

对 $\boldsymbol{P}=\boldsymbol{A}(\boldsymbol{A}^T\boldsymbol{A})^{-1}\boldsymbol{A}^T$ 用矩阵乘法的结合律和矩阵乘积的转置公式，可以证明投影矩阵的性质： $\boldsymbol{P}^2=\boldsymbol{P}$ ， $\boldsymbol{P}^T=\boldsymbol{P}$。
- **最小二乘法 Least Squares**

![](https://pic3.zhimg.com/v2-082e342a358ad8014cf6bb6453e40692_b.jpg)

应用投影矩阵求方程组最优解的方法，最常用于“最小二乘法”拟合曲线。

有三个数据点{(1,1), (2,2), (3,2)}，求直线方程b=C+Dt，要求直线尽量接近于三个点。把三个点的数据代入方程则有：

C+ D=1

C+2D=2

C+3D=2

矩阵形式为 $\left[ {\begin{array}{*{20}{r}} 1&1\\ 1&2\\ 1&3 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} C\\ D \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 1\\ 2\\ 2 \end{array}} \right]$ 

这个的方程***A*x**=**b**是无解的，解决办法就是求其最优解，即方程$\boldsymbol{A}^T\boldsymbol{A}\boldsymbol{\hat x}=\boldsymbol{A}^T\boldsymbol{b}$的解。



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



# 第18讲 行列式及其性质

Properties of determinants

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AP150)

课程进入第二大部分，之前学习了大量长方形矩阵的性质，现在我们集中讨论方阵的性质，行列式和特征值将我们的又一个重点，求行列式则与特征值息息相关。

- **行列式 Determinants**

行列式是一个每个方阵都具有的数值，我们将矩阵***A***的行列式记作 $\det (\boldsymbol{A}) = \left| \boldsymbol{A} \right|$ 。它将尽可能多的矩阵信息压缩在这一个数里。例如，矩阵不可逆或称奇异与矩阵的行列式等于0等价，因此可以用行列式来判定矩阵是否可逆。

- **性质 Properties**

直接给出n阶行列式的公式，则一下子代入了大量信息，并不利于接受这个概念，我们从行列式的三个性质开始讲起，这三个性质定义了行列式。

这里可以给出二阶行列式的表达式 $\left| {\begin{array}{*{20}{c}} a&b\\ c&d \end{array}} \right| = ad - bc$ 。我们可以用它来验证行列式的性质，也可以看到它本身是可以从行列式的性质推导出来的。

**1.**det(***I***)=1。 $\left| {\begin{array}{*{20}{c}} 1&0\\ 0&1 \end{array}} \right| =  + 1$ 

**2.**如果交换行列式的两行，则行列式的数值会反号。从前两条可以推知置换矩阵的行列式是+1或者-1。 $\left| {\begin{array}{*{20}{c}} 0&1\\ 1&0 \end{array}} \right|{\rm{ =  - }}1$ 

**3.**(a)如果在矩阵的一行乘上t，则行列式的值就要乘上t。 $\left| {\begin{array}{*{20}{c}} {ta}&{tb}\\ c&d \end{array}} \right|{\rm{ = }}t\left| {\begin{array}{*{20}{c}} a&b\\ c&d \end{array}} \right|$ 

**3.**(b)行列式是“矩阵的行”的线性函数。 $\left| {\begin{array}{*{20}{c}} {a + a'}&{b + b'}\\ c&d \end{array}} \right| = \left| {\begin{array}{*{20}{c}} a&b\\ c&d \end{array}} \right| + \left| {\begin{array}{*{20}{c}} {a'}&{b'}\\ c&d \end{array}} \right|$ 

> 行列式本身是有显式的，但是直接给出显式真的无益于理解行列式，我觉得G.Strang这里做了一个类似公理化的办法来给出行列式，是一个比较高明的办法。如他所言，很少有人用公式进行行列式计算，计算机也是用消元的办法来求解的。窃以为把大量时间花在“逆序”这一概念上对学习线代帮助并不大。

**更多的性质可以从以上的三条性质中推导出来。**

**4.**如果矩阵的两行是完全相同的，则它的行列式为0。这可以从第二条性质推导出来，因为交换这个相同的两行，行列式应该变号；但是新生成的矩阵跟原矩阵没有区别，因此行列式应该不变，所以有det=-det，所以det等于0。

**5.**从矩阵的某行k减去另一行i的倍数，并不改变行列式的数值，我们以二阶为例：

![](https://pic4.zhimg.com/v2-158a15a28b62fbd429ca3cf472e8bb8f_b.jpg)

**6.**如矩阵A的某一行都是0，则其行列式为0。可以应用性质3(a)，取t=0证明。

**7.**三角阵的行列式的值等于其对角线上数值（主元）的乘积。

$\left| {\begin{array}{*{20}{c}} {{d_1}}&*&*& \cdots &*\\ 0&{{d_2}}&*& \cdots &*\\ 0&0& \ddots & \ddots & \vdots \\  \vdots & \vdots & \ddots & \ddots & \vdots \\ 0&0& \cdots & \cdots &{{d_n}} \end{array}} \right| = \left| {\begin{array}{*{20}{c}} {{d_1}}&0&0& \cdots &0\\ 0&{{d_2}}&0& \cdots &0\\ 0&0& \ddots & \ddots & \vdots \\  \vdots & \vdots & \ddots & \ddots & \vdots \\ 0&0& \cdots & \cdots &{{d_n}} \end{array}} \right| = {d_1}{d_2} \cdots {d_n}\left| {\begin{array}{*{20}{c}} 1&0&0& \cdots &0\\ 0&1&0& \cdots &0\\ 0&0& \ddots & \ddots & \vdots \\  \vdots & \vdots & \ddots & \ddots & \vdots \\ 0&0& \cdots & \cdots &1 \end{array}} \right| = {d_1}{d_2} \cdots {d_n}$ 

性质5告诉我们三角阵通过行消元法得到对角阵的过程中，行列式的数值没有发生变化。性质3(a)告诉我们对角阵的行列式等于其主元的乘积再乘以单位阵的行列式。而性质1表明单位阵行列式为1。

**8.**当且仅当矩阵***A***为奇异矩阵时，其行列式为0。

如果矩阵***A***为奇异阵，则必可通过消元法使得矩阵的某行全等于零，则按照性质6，***A***的行列式为0。

如果其不是奇异阵，则通过消元可以得到一个上三角矩阵，且其主元均不为0，则按照性质7，行列式的数值等于主元的乘积也不等于0。

计算非奇异矩阵的行列式有确切的公式，但通常计算机是靠消元的方法来转化为三角阵，然后将主元相乘来进行计算的。

例如：二阶矩阵 $\left[ {\begin{array}{*{20}{c}} a&b\\ c&d \end{array}} \right] \to \left[ {\begin{array}{*{20}{c}} a&b\\ 0&{d - \frac{c}{a}b} \end{array}} \right]$ 

若a≠0则有 $\left| {\begin{array}{*{20}{c}} a&b\\ c&d \end{array}} \right|{\rm{ = }}a(d - \frac{c}{a}b){\rm{ = }}ad - bc$ 

**9. **det(***AB***)=det(***A***)det(***B***)

尽管矩阵的和的行列式不等于行列式的和，但矩阵乘积的行列式等于矩阵行列式的乘积。

> 在课本中，G.Strang给了一个挺赞的证明，其主要思想就是证明det(***AB***)/det(***B***)与矩阵***A***的关系完全符合行列式的前三个性质，而因为前三个性质定义了行列式，因此det(***AB***)/det(***B***)这就等于矩阵的行列式值，即det(***AB***)/det(***B***)= det(***A***)。

如果***A***为可逆矩阵，则 $\boldsymbol{A}^{-1}\boldsymbol{A}=\boldsymbol{I}$ ，所以有 $\det ({\boldsymbol{A}^{ - 1}}) = \frac{1}{{det(\boldsymbol{A})}}$ 

此外，$\det ({\boldsymbol{A}^{ 2}}) = {{det(\boldsymbol{A})}}^2$并且有$\det ({\boldsymbol{2A}}) = 2^n{{det(\boldsymbol{A})}}$。后一个公式让我们容易联想到体积，当长宽高都倍增之后，体积变成了原来的2^3=8倍。

**10.** $\det ({\boldsymbol{A}^{T}}) = {{det(\boldsymbol{A})}}$ 

对于二阶矩阵这显然成立: $\left| {\begin{array}{*{20}{c}} a&b\\ c&d \end{array}} \right| = \left| {\begin{array}{*{20}{c}} a&c\\ b&d \end{array}} \right| = ad - bc$ 

证明： 矩阵消元可得***A***=***LU***，则 $\boldsymbol{A}^T=\boldsymbol{U}^T\boldsymbol{L}^T$ ，由性质9可知$\det ({\boldsymbol{A}}) = {{det(\boldsymbol{L})}}{{det(\boldsymbol{U})}}$，$\det ({\boldsymbol{A}^{T}}) = {{det(\boldsymbol{L}^T)}}{{det(\boldsymbol{U}^T)}}$，根据性质7可知$\det ({\boldsymbol{L}^{T}}) = {{det(\boldsymbol{L})}}$，$\det ({\boldsymbol{U}^{T}}) = {{det(\boldsymbol{U})}}$，则二者乘积相等。

因为性质10成立，所以性质2,3,4,5,6可以用在行列式的列性质上。

行列式的性质2中隐藏着一个内容，这就是置换隐藏着奇偶性，一个矩阵不可能经过奇数次置换得到和偶数次置换相同的方阵。



# 第19讲 行列式公式和代数余子式

Determinant formulas and cofactors

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2APP34)

我们已经认识到了行列式的性质，应该推导出其公式了。[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2APP34)我们已经认识到了行列式的性质，应该推导出其公式了。

- **行列式公式 Formula for the determinant**

行列式有如下三个性质：

1.	det（***I***)=1。

2.	如果交换行列式的两行，则行列式的数值会反号。

3.	行列式是“矩阵的行”的线性函数。

从这三条性质可以推导出后续的七条性质，从这十个性质出发可以得到二阶方阵的行列式公式：

$\begin{array}{*{20}{l}} {\left| {\begin{array}{*{20}{c}} a&b\\ c&d \end{array}} \right|}&{{=}\left| {\begin{array}{*{20}{c}} a&0\\ c&d \end{array}} \right|{+}\left| {\begin{array}{*{20}{c}} 0&b\\ c&d \end{array}} \right|}\\ {}&{{\rm{ = }}\left| {\begin{array}{*{20}{c}} a&0\\ c&0 \end{array}} \right|{\rm{ + }}\left| {\begin{array}{*{20}{c}} a&0\\ 0&d \end{array}} \right|{\rm{ + }}\left| {\begin{array}{*{20}{c}} 0&b\\ c&0 \end{array}} \right|{\rm{ + }}\left| {\begin{array}{*{20}{c}} 0&b\\ 0&d \end{array}} \right|}\\ {}&{=0 + ad - bc + 0}\\ {}&{ = ad - bc} \end{array}$ 

通过性质3对n阶矩阵的行列式进行拆分，我们可以得到所有只包含n个非零元素的行列式，对于二阶行列式我们从1个拆分为2个，然后拆分成4个。而对于三阶矩阵我们从1个拆分成3个，然后拆分成9个，最后要拆分成27个。但最终这些行列式中有很大一部分等于0。

$\begin{array}{*{20}{l}} {\left| {\begin{array}{*{20}{c}} {{a_{11}}}&{{a_{12}}}&{{a_{13}}}\\ {{a_{21}}}&{{a_{22}}}&{{a_{23}}}\\ {{a_{31}}}&{{a_{32}}}&{{a_{33}}} \end{array}} \right|}&{{\rm{ = }}\left| {\begin{array}{*{20}{c}} {{a_{11}}}&0&0\\ 0&{{a_{22}}}&0\\ 0&0&{{a_{33}}} \end{array}} \right|{\rm{ + }}\left| {\begin{array}{*{20}{c}} {{a_{11}}}&0&0\\ 0&0&{{a_{23}}}\\ 0&{{a_{32}}}&0 \end{array}} \right|{\rm{ + }}\left| {\begin{array}{*{20}{c}} 0&{{a_{12}}}&0\\ {{a_{21}}}&0&0\\ 0&0&{{a_{33}}} \end{array}} \right|}\\ {}&{{\rm{ + }}\left| {\begin{array}{*{20}{c}} 0&{{a_{12}}}&0\\ 0&0&{{a_{23}}}\\ {{a_{31}}}&0&0 \end{array}} \right|{\rm{ + }}\left| {\begin{array}{*{20}{c}} 0&0&{{a_{13}}}\\ {{a_{21}}}&0&0\\ 0&{{a_{32}}}&0 \end{array}} \right|{\rm{ + }}\left| {\begin{array}{*{20}{c}} 0&0&{{a_{13}}}\\ 0&{{a_{22}}}&0\\ {{a_{31}}}&0&0 \end{array}} \right|}\\ {}&{{\rm{ = }}{a_{11}}{a_{22}}{a_{33}} - {a_{11}}{a_{23}}{a_{33}} - {a_{12}}{a_{21}}{a_{33}}}\\ {}&{ + {a_{12}}{a_{23}}{a_{31}} + {a_{13}}{a_{21}}{a_{32}} - {a_{13}}{a_{22}}{a_{31}}} \end{array}$ 

每一个拆分出来的非0行列式都是在每行每列都有且只有一个元素，就如同置换矩阵的元素分布。应用性质3可以将元素从行列式中提出来，而置换矩阵的行列式值为+1或者-1，因此可以给出行列式的公式。n阶拆分矩阵非0行列式的个数的计算方法就如同计算置换矩阵的个数一样，第一行放置一个非0元素的位置有n个选择，第二行为n-1个……。最后得到共n!个矩阵。

对于拆分得到的三阶矩阵，元素从上至下朝向右侧方向的，其行列式的数值为正，朝向左侧方向的则为负。但是这个规律只适用于三阶矩阵，不适用于高阶矩阵。

![](https://pic2.zhimg.com/v2-92d312157533283dee2825f7962e51c9_b.jpg)

行列式的公式： $\det (\boldsymbol{A}) = \sum\limits_{n!} { \pm {a_{1\alpha }}} {a_{2\beta }}{a_{3\gamma }} \cdots {a_{n\omega }}$ 

其中列标号（ $\alpha$ , $\beta$ , $\gamma$ ……）是列标号（1, 2, 3……n）的某个排列。比如说对于单位阵而言，只有$\alpha$ =1, $\beta$ =2…… $\omega$ =n所得到的行列式为+1，其它都为零，所以单位阵的行列式为1。

例如： $\left| {\begin{array}{*{20}{c}} 0&0&1&1\\ 0&1&1&0\\ 1&1&0&0\\ 1&0&0&1 \end{array}} \right| = \left| {\begin{array}{*{20}{c}} 0&0&0&1\\ 0&0&1&0\\ 0&1&0&0\\ 1&0&0&0 \end{array}} \right| + \left| {\begin{array}{*{20}{c}} 0&0&1&0\\ 0&1&0&0\\ 1&0&0&0\\ 0&0&0&1 \end{array}} \right|$ 

列标号取（4,3,2,1）得到第一个拆分行列式，符号为正，因为只要经过两次交换就能变为（1,2,3,4）。第二个为（3,2,1,4），因为只需交换一次就可变为正序，所以符号为负。因此本行列式为0。

- **代数余子式 Cofactor formula**

代数余子式是用较小的矩阵的行列式来写出n阶行列式的公式。

det（***A***）= ${a_{11}}({a_{22}}{a_{33}} - {a_{23}}{a_{32}}) + {a_{12}}( - {a_{21}}{a_{33}} + {a_{23}}{a_{31}} + {a_{13}}{a_{21}}{a_{32}} - {a_{22}}{a_{31})}$ 

= $\left| {\begin{array}{*{20}{c}} {{a_{11}}}&0&0\\ 0&{{a_{22}}}&{{a_{23}}}\\ 0&{{a_{32}}}&{{a_{33}}} \end{array}} \right| + \left| {\begin{array}{*{20}{c}} 0&{{a_{12}}}&0\\ {{a_{21}}}&0&{{a_{23}}}\\ {{a_{31}}}&0&{{a_{33}}} \end{array}} \right| + \left| {\begin{array}{*{20}{c}} 0&0&{{a_{13}}}\\ {{a_{21}}}&{{a_{22}}}&0\\ {{a_{31}}}&{{a_{32}}}&0 \end{array}} \right|$ 

将原公式中属于矩阵第一行的a1j提出来，其系数即为代数余子式，是一个低阶行列式的值。这个低阶行列式是由原矩阵去掉a1j所在的行和列组成的。

对矩阵中任意元素aij而言，其代数余子式Cij就是矩阵的行列式的公式中aij的系数。Cij等于原矩阵移除第i行和第j列后剩余元素组成的n-1阶矩阵的行列式数值乘以 $(-1)^{i+j}$ 。（Cij在i+j为偶数时为正，奇数时为负数。）

对于n阶方阵，其行列式的代数余子式公式为：

det（***A***）= ${a_{11}}{{\rm{C}}_{11}}{\rm{ + }}{a_{12}}{{\rm{C}}_{12}}{\rm{ + }} \cdots {\rm{ + }}{a_{1{\rm{n}}}}{{\rm{C}}_{1{\rm{n}}}}$ 

对于二阶矩阵，按照代数余子式公式则有 $\left| {\begin{array}{*{20}{c}} a&b\\ c&d \end{array}} \right| = ad + b( - c)$ 

对于矩阵行列式的计算，消元的得到主元是一个很好的方法，与之相比行列式的展开公式较为复杂，而代数余子式的方法介于两者之间，它的核心想法是通过降阶来将原来的行列式展开成更简单的行列式。

举"三对角阵"（tridiagonal matrix）为例，它除了对角线和对角线两侧相邻的元素之外，其它元素均为0。例如由1组成的4阶三对角阵为 ${\boldsymbol{A}_4} = \left[ {\begin{array}{*{20}{c}} 1&1&0&0\\ 1&1&1&0\\ 0&1&1&1\\ 0&0&1&1 \end{array}} \right]$

由1组成的n阶三对角阵的行列式等于多少？

我们可以从1阶开始算起： $\left| {{\boldsymbol{A}_1}} \right| = 1$ , $\left| {{\boldsymbol{A}_2}} \right| = \left| {\begin{array}{*{20}{c}} 1&1\\ 1&1 \end{array}} \right| = 0$ ， $\left| {{\boldsymbol{A}_3}} \right| = \left| {\begin{array}{*{20}{c}} 1&1&0\\ 1&1&1\\ 0&1&1 \end{array}} \right| =- 1$ ，则有 $\left| {{\boldsymbol{A}_4}} \right| = 1\left| {\begin{array}{*{20}{c}} 1&1&0\\ 1&1&1\\ 0&1&1 \end{array}} \right|{\rm{ - }}1\left| {\begin{array}{*{20}{c}} 1&1&0\\ 0&1&1\\ 0&1&1 \end{array}} \right| = \left| {{\boldsymbol{A}_3}} \right| - 1\left| {{\boldsymbol{A}_2}} \right| =  - 1$ 

从矩阵的特殊结构我们可以得到： $\left| {{\boldsymbol{A}_{\rm{n}}}} \right| = \left| {{\boldsymbol{A}_{{\rm{n - }}1}}} \right| - 1\left| {{\boldsymbol{A}_{{\rm{n - 2}}}}} \right|$ 

由1组成的n阶三对角阵的行列式从1阶开始按照1,0，-1，-1,0,1进行循环。



# 第20讲 克莱姆法则、逆矩阵、体积

Cramer’s rule, inverse matrix, and volume

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AQ40C)

我们已经了解了行列式的公式和性质，下面讨论它的应用。

- **逆矩阵的公式 Formula for ** $\boldsymbol{A}^{-1}$ 

我们已经知道二阶矩阵的逆矩阵公式：

$\left[ {\begin{array}{*{20}{c}} a&b\\ c&d \end{array}} \right] = \frac{1}{{ad - bc}}\left[ {\begin{array}{*{20}{c}} d&{ - b}\\ { - c}&a \end{array}} \right]$ 

那么我们能写出三阶甚至高阶的公式么？通过观察二阶矩阵逆矩阵的公式，我们可以用同样的策略来构造高阶矩阵的求逆公式，为：

${\boldsymbol{A}^{ - 1}} = \frac{1}{{\det (\boldsymbol{A})}}{\boldsymbol{C}^T}$ 

等式右侧矩阵外的因子，其分母是矩阵的行列式的值，而矩阵是“代数余子式矩阵”（cofactor matrix）***C***的转置矩阵。即伴随矩阵（adjoint matrix）。

矩阵***A***的行列式的计算中包含的都是n个元素的乘积：

$det\boldsymbol{A}=\sum\limits_{n} { \pm {a_{1\alpha }}{a_{2\beta }}{a_{3\gamma }} \cdots {a_{{\rm{n}}\omega }}} $ 

而伴随矩阵中的元素都是n-1阶行列式，它的运算中出现的是n-1个矩阵***A***中元素的乘积。所以矩阵***A***与两者相乘才能完全消去，而得到单位矩阵。下面我们就用矩阵***A***与矩阵 $\boldsymbol{C}^T$ 相乘来验证 $\boldsymbol{A}\boldsymbol{C}^T=det(\boldsymbol{A})\boldsymbol{I}$ ，并且理解逆矩阵的构造策略。

$\boldsymbol{A}{\boldsymbol{C}^T} = \left[ {\begin{array}{*{20}{c}} {{a_{11}}}& \ldots &{{a_{1n}}}\\  \vdots & \ddots & \vdots \\ {{a_{n1}}}& \cdots &{{a_{nn}}} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{C_{11}}}& \ldots &{{C_{n1}}}\\  \vdots & \ddots & \vdots \\ {{C_{1n}}}& \cdots &{{C_{nn}}} \end{array}} \right]$ 

矩阵 $\boldsymbol{A}{\boldsymbol{C}^T}$ 第一行第一列的元素等于矩阵***A***第一行和矩阵 ${\boldsymbol{C}^T}$ 第一列进行点积，计算可得：

$\sum\limits_{j = 1}^n {{a_{1j}}{C_{1j}} = \det (\boldsymbol{A})} $ 

点积的算式本身就是矩阵***A***的计算公式，因此结果为***A***行列式的值。而矩阵$\boldsymbol{A}{\boldsymbol{C}^T}$ 对角线上所有的元素都是如此，因此其对角戏上的元素都等于det***A***。

而对于非对角线元素，我们以第二行第一列的元素为例，其计算公式为：

$\sum\limits_{j = 1}^n {{a_{2j}}{C_{1j}} = \det ({\boldsymbol{A}_{s}})} $ 

这可以视为矩阵***A**s*的行列式数值，各个代数余子式的形式不变，但是与代数余子式相乘的变为了矩阵***A***第二行第j列元素。因此***A**s*的形式相当于用矩阵***A***第二行的元素替代第一行的元素得到的矩阵。因为该矩阵中前两行完全相同，因此按照行列式性质4，det(***A**s*)=0（G.Strang在课堂上是用二阶矩阵为例）：

$\sum\limits_{j = 1}^n {{a_{2j}}{C_{1j}} = } \left| {\begin{array}{*{20}{r}} {{a_{21}}}&{{a_{22}}}& \cdots & \cdots &{{a_{2n}}}\\ {{a_{21}}}&{{a_{22}}}& \cdots & \cdots &{{a_{2n}}}\\ {{a_{31}}}&{{a_{32}}}& \ddots &{}&{{a_{3n}}}\\  \vdots &{}&{}& \ddots & \vdots \\ {{a_{n1}}}&{{a_{n2}}}& \cdots & \cdots &{{a_{nn}}} \end{array}} \right|{\rm{ = }}0$ 

而$\boldsymbol{A}{\boldsymbol{C}^T}$乘积矩阵中非对角线元素的计算均服从此规律，因此均为0。则：

$\boldsymbol{A}{\boldsymbol{C}^T}$= $\left[ {\begin{array}{*{20}{r}} {\det \boldsymbol{A}}&0&0& \cdots &0\\ 0&{\det \boldsymbol{A}}&0& \cdots &0\\ 0&0& \ddots &{}&0\\  \vdots &{}&{}& \ddots & \vdots \\ 0&0&0& \cdots &{\det \boldsymbol{A}} \end{array}} \right]{\rm{ = }}\det (\boldsymbol{A})\boldsymbol{I}$ 

即 $\boldsymbol{A}\frac{1}{{\det (\boldsymbol{A})}}{\boldsymbol{C}^T} =\boldsymbol{I}$ ，因此有${\boldsymbol{A}^{ - 1}} = \frac{1}{{\det (\boldsymbol{A})}}{\boldsymbol{C}^T}$。

逆矩阵公式的一个好处就是，我们从中可以看到，当改变原矩阵中的一个元素时，给逆矩阵带来了怎样的变化。

- **克莱姆法则 Cramer’s Rule for **$\boldsymbol{x}=\boldsymbol{A}^{-1}\boldsymbol{b}$ 

对于可逆矩阵***A***，方程***A*x**=**b**必然有解$\boldsymbol{x}=\boldsymbol{A}^{-1}\boldsymbol{b}$，将逆矩阵的公式带入其中，则有：

$$
\boldsymbol{x}=\boldsymbol{A}^{-1}\boldsymbol{b}=\frac{1}{{\det (\boldsymbol{A})}}{\boldsymbol{C}^T}\boldsymbol{b}
$$

克莱姆法则是从另一个角度来看待这个公式。实际上**x**的分量 ${x_j} = \frac{{\det ({\boldsymbol{B}_j})}}{{\det (\boldsymbol{A})}}$ 

其中，矩阵***B*** j为用向量**b**替换矩阵***A***的第j列所得到的新矩阵。例如：

${\boldsymbol{B}_1} = \left[ {\begin{array}{*{20}{r}} {{b_1}}&{{a_{12}}}& \cdots & \cdots &{{a_{1n}}}\\ {{b_2}}&{{a_{22}}}& \cdots & \cdots &{{a_{2n}}}\\ {{b_3}}&{{a_{32}}}& \ddots &{}&{{a_{3n}}}\\  \vdots &{}&{}& \ddots & \vdots \\ {{b_n}}&{{a_{n2}}}& \cdots & \cdots &{{a_{nn}}} \end{array}} \right]$ ， ${\boldsymbol{B}_n} = \left[ {\begin{array}{*{20}{r}} {{a_{11}}}& \cdots & \cdots &{{a_{1n - 1}}}&{{b_1}}\\ {{a_{21}}}& \cdots & \cdots &{{a_{2n - 1}}}&{{b_2}}\\  \vdots &{}& \ddots & \vdots & \vdots \\  \vdots &{}&{}&{{a_{n - 1n - 1}}}&{{b_{n - 1}}}\\ {{a_{n1}}}&{{a_{n2}}}& \cdots &{{a_{nn - 1}}}&{{b_n}} \end{array}} \right]$ 

矩阵***B*** j的行列式的数值从第j列用代数余子式进行展开计算，正好是伴随矩阵${\boldsymbol{C}^T}$的第j行与向量**b**点积的结果。此处我们用到了行列式的性质10。

相比于消元法，采用克莱姆法则计算方程的解，效率较低。

- **体积 volume of box**

矩阵***A***行列式的绝对值等于以矩阵***A***行（列）向量为边所构成的平行六面体的体积。行列式的正负对应左手系和右手系。

如果矩阵***A***是单位矩阵，则其构成的是三个边长均为1且互相垂直的立方体，其体积为1，这与上面的结论相符。这也是行列式的性质1。

而如果矩阵***A***为正交矩阵***Q***，则其构成的也是三个边边长为1且三边互相垂直的立方体，其体积也为1只是取向与单位阵不同。这也与上面的结论相符，因为 $\boldsymbol{Q}^T\boldsymbol{Q}=\boldsymbol{I}$ ，且 $det(\boldsymbol{Q})=det(\boldsymbol{Q}^T)$ ，所以det***Q***=1。

交换矩阵***A***中的行并不会改变其行列式的绝对值，显然也不会改变向量围成的体积，因此这也和体积理论相符。这是行列式的性质2。

![](https://pic4.zhimg.com/v2-48c39ecd0c2f47ecac79285402296273_b.jpg)

对于长方体，也非常直观，当你将其中一条边的边长增加2倍时，平行六面体的体积也会增加2倍，这相当于性质3a。

对于性质3b，实际上是要求体积理论摆脱角度的限制（之前几条完全都是在直角的背景下讨论得），我们可以在二维条件下简单证明。

> **证明二阶行列式是平行四边形的面积**

![](https://pic3.zhimg.com/v2-621f2263c0da7eae72eea0e1a0705d06_b.jpg)

> 如图所示，**a**和**b**围成的平行四边形的面积，就等于**a**和**h**的长度之积，就等于两个互相垂直的向量**a**和**h**所围成的长方形的面积，按照前面所述即为 $\left| {\begin{array}{*{20}{c}} {{a_1}}&{{a_2}}\\ {{h_1}}&{{h_2}} \end{array}} \right|$ 。
> 根据行列式运算法则有 $\left| {\begin{array}{*{20}{c}} {{a_1}}&{{a_2}}\\ {{h_1}}&{{h_2}} \end{array}} \right| = \left| {\begin{array}{*{20}{c}} {{a_1}}&{{a_2}}\\ {{b_1}}&{{b_2}} \end{array}} \right| - \left| {\begin{array}{*{20}{c}} {{a_1}}&{{a_2}}\\ {{p_1}}&{{p_2}} \end{array}} \right|$ ，而**p**与**a**同方向因此第二项为0，因此平行四边形的面积等于 $\left| {\begin{array}{*{20}{c}} {{a_1}}&{{a_2}}\\ {{b_1}}&{{b_2}} \end{array}} \right|$ 。结果可以推广到高维。




![](https://pic4.zhimg.com/v2-d15c1caf9a267aac6f38ed786751be07_b.jpg)

$\left| {\begin{array}{*{20}{c}} {a + a'}&{b + b'}\\ c&d \end{array}} \right| = \left| {\begin{array}{*{20}{c}} a&b\\ c&d \end{array}} \right| + \left| {\begin{array}{*{20}{c}} {a'}&{b'}\\ c&d \end{array}} \right|$ 

二阶行列式的值等于平行四边形的面积，同时其一半也是{(a,b),(c,d),(0,0)}围成的三角形的面积。

若三角形不过原点，为{(x1,y1),( x2,y2),( x3,y3)}围成，则其面积等于 $\frac{1}{2}\left| {\begin{array}{*{20}{c}} {{x_1}}&{{y_1}}&1\\ {{x_2}}&{{y_2}}&1\\ {{x_3}}&{{y_3}}&1 \end{array}} \right|$ 。

> 这个公式可以从第三列用代数余子式展开，所得结果可以看做是从一个过原点的大三角形中减去两个过原点的小三角形。

![](https://pic4.zhimg.com/v2-fb04fecc798546a02fcff96b86baf547_b.jpg)

> 除以上各条之外，性质4也比较直观，当有两条边重合时，平行六面体或者平行四边形被压扁，体积或者面积为0。





# 第21讲 特征值和特征向量

Eigenvalues and eigenvectors

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AV2R8)

本单元后面的课程主要围绕特征值和特征向量。在这个议题下讨论得都是方阵。

- **特征向量和特征值 Eigenvectors and eigenvalues**

将矩阵***A***与向量**x**相乘当做是对向量的一种操作或者函数，输入**x**而输出***A*x**。特征向量即在特定的向量**x**方向上输出的***A*x**平行于**x**，即为：$\boldsymbol{A}\boldsymbol{x}=\lambda\boldsymbol{x}$ 。

其中**x**为矩阵***A***的特征向量，而 $\lambda$ 为***A***的特征值。

如果0是矩阵的特征值，则有***A*x**=0**x=0**。特征值0所对应的向量生成了矩阵的零空间。如果矩阵***A***为不可逆矩阵，则0是其特征值之一。

**例1：**矩阵***P***是朝向一个平面的投影矩阵。对于这个平面之内的**x**，均有***P*x**=**x**，因此**x**是特征向量而1为特征值。垂直于该平面的向量**x**经投影得到***P*x**=0，这个x也是矩阵的特征向量而0为特征值。矩阵***P***的所有特征向量张成了整个空间。

**例2：**矩阵***A***= $\left[ {\begin{array}{*{20}{c}} 0&1\\ 1&0 \end{array}} \right]$ ，具有特征向量**x**= $\left[ {\begin{array}{*{20}{c}} 1\\ 1 \end{array}} \right]$ ，对应的特征向量为1；另一个特征向量为**x**= $\left[ {\begin{array}{*{20}{c}} 1\\ {{\rm{ - }}1} \end{array}} \right]$ ，对应的特征向量为-1。这些特征向量张成了整个空间。因为是对称矩阵，其特征向量互相垂直。

- $det(\boldsymbol{A}-\lambda\boldsymbol{I})=0$ 

任意nxn矩阵***A***具有n个特征值，并且它们的和等于矩阵对角线上的元素之和，这个数值为矩阵的迹（trace）。对于二阶矩阵，在已知一个特征值的条件下，可以据此得到另一个特征值。

方程$\boldsymbol{A}\boldsymbol{x}=\lambda\boldsymbol{x}$ 中特征值和特征向量均未知，没法直接求解。因此我们做如下数学处理：$\boldsymbol{A}\boldsymbol{x}=\lambda\boldsymbol{x}$ ，因此有 $(\boldsymbol{A}-\lambda\boldsymbol{I})\boldsymbol{x}=\boldsymbol{0}$ ，则$\boldsymbol{A}-\lambda\boldsymbol{I}$ 为奇异阵，因此$det(\boldsymbol{A}-\lambda\boldsymbol{I})=0$。在这个没有**x**的方程中，可以解得n个特征值，但是有可能方程有重根，则会得到重复的特征值。

得到特征值之后，可以用消元法解$\boldsymbol{A}-\lambda\boldsymbol{I}$ ，这一矩阵零空间中的向量为矩阵***A***的特征向量。

例如：矩阵***A***= $\left[ {\begin{array}{*{20}{c}} 3&1\\ 1&3 \end{array}} \right]$ ，则 $\det (\boldsymbol{A} - \lambda \boldsymbol{I}) = \left| {\begin{array}{*{20}{c}} {3{\rm{ - }}\lambda }&1\\ 1&{3{\rm{ - }}\lambda } \end{array}} \right| = {(3 - \lambda )^2} - 1 = {\lambda ^2} - 6\lambda  + 8$ 。可以看到其中的参数6是矩阵***A***的迹，而8是行列式的值。通常一个2阶矩阵的特征值是如下方程的解： $\lambda^2-trace(\boldsymbol{A})\lambda+det\boldsymbol{A}=0$。

对于上述矩阵***A***，可以求得特征值 $\lambda_1=4$ 和 $\lambda_2=2$ 。

$\boldsymbol{A} - 4\boldsymbol{I}  = \left[ {\begin{array}{*{20}{c}} {{\rm{ - }}1}&1\\ 1&{{\rm{ - }}1} \end{array}} \right]$ ***，*** $(\boldsymbol{A} - 4\boldsymbol{I})\boldsymbol{x}_1=\boldsymbol{0}$ ***,*** ${\boldsymbol{x}_1} = \left[ {\begin{array}{*{20}{c}} 1\\ 1 \end{array}} \right]$ ；

$\boldsymbol{A} - 2\boldsymbol{I}  = \left[ {\begin{array}{*{20}{c}} {{\rm{  }}1}&1\\ 1&{{\rm{}}1} \end{array}} \right]$***，***$(\boldsymbol{A} - 2\boldsymbol{I})\boldsymbol{x}_2=\boldsymbol{0}$***,***${\boldsymbol{x}_2} = \left[ {\begin{array}{*{20}{c}} -1\\ 1 \end{array}} \right]$ ；

与前例中矩阵***A***= $\left[ {\begin{array}{*{20}{c}} 0&1\\ 1&0 \end{array}} \right]$ 的特征值和特征向量相对比，可知两者为一组平移矩阵。在对角元素上分别加3，改变了特征值但是没有改变特征向量。

$\boldsymbol{A}\boldsymbol{x}=\lambda\boldsymbol{x}$ ，则有$(\boldsymbol{A}+3\boldsymbol{I})\boldsymbol{x}=\lambda\boldsymbol{x}+3\boldsymbol{x}=(\lambda+3)\boldsymbol{x}$ 。

需要注意的是，两个矩阵的和的特征值不是两特征值直接相加之和，因为特征向量并不相同。

> **矩阵的迹等于特征值之和：**如上所述，将$det(\boldsymbol{A}-\lambda\boldsymbol{I})=0$展开会得到 $\lambda$ 的n阶多项式，多项式的解就是矩阵**A** 的特征值，根据多项式根与系数的关系，解之和即特征值之和等于 $\lambda^{n-1}$ 的系数。而行列式展开式中只有对角线的积这一项包含$\lambda^{n-1}$（其它项最高是n-2 次方），而其系数为矩阵**A** 对角线元素之和，即矩阵**A **的迹，因此特征值之和与矩阵的迹相等。
> **对称矩阵的特征向量正交：**$\lambda_1$ 和 $\lambda_2$ 是对称矩阵的两个不同的特征值，对应的特征向量分别为**x**1 和**x**2。则有$\boldsymbol{A}\boldsymbol{x}_1=\lambda_1\boldsymbol{x}_1$ ，左乘**x**2得$\boldsymbol{x}_2^T\boldsymbol{A}\boldsymbol{x}_1=\lambda_1\boldsymbol{x}_2^T\boldsymbol{x}_1$ 。而又有 $\boldsymbol{x}_2^T\boldsymbol{A}\boldsymbol{x}_1=(\boldsymbol{A}^T\boldsymbol{x}_2)^T\boldsymbol{x}_1=\lambda_2\boldsymbol{x}_2^T\boldsymbol{x}_1$ 。因此有$(\lambda_1-\lambda_2)\boldsymbol{x}_2^T\boldsymbol{x}_1=0$，而两特征值不等，所以可得两特征向量正交。

- **复数特征值 Complex eigenvalues**

矩阵 $\boldsymbol{Q} = \left[ {\begin{array}{*{20}{c}} 0&{{\rm{ - }}1}\\ 1&0 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {\cos {{90}^{\rm{o}}}}&{{\rm{ - }}\sin {{90}^{\rm{o}}}}\\ {\sin {{90}^{\rm{o}}}}&{\cos {{90}^{\rm{o}}}} \end{array}} \right]$ 是一个90度旋转矩阵。从矩阵的迹和行列式的值可以得到$\lambda_1+\lambda_2=0$， $\lambda_1\lambda_2=1$ 。从矩阵的性质可知它的实数特征向量只有零向量，因为其他任何向量乘以旋转矩阵，向量的方向都会发生改变。计算可得：

$\det (\boldsymbol{Q} - \lambda \boldsymbol{I}) = \left| {\begin{array}{*{20}{c}} {{\rm{ - }}\lambda }&{{\rm{ - }}1}\\ 1&{{\rm{ - }}\lambda } \end{array}} \right| = {\lambda ^2} + 1 = 0$ 

可以解得$\lambda_1=i$ 和 $\lambda_2=-i$ 。如果一个矩阵具有复数特征值a+bi则，它的共轭复数a-bi也是矩阵的特征值。*实数特征值让特征向量伸缩而虚数让其旋转。*

对称矩阵永远具有实数的特征值，而反对称矩阵（antisymmetric matrices），即满足 $\boldsymbol{A}^T=-\boldsymbol{A}$ 的矩阵，具有纯虚数的特征值。

- **三角阵和重特征值 Triangular matrices and repeated eigenvalues**

对于如***A***= $\left[ {\begin{array}{*{20}{c}} 3&1\\ 0&3 \end{array}} \right]$ 的三角矩阵，特征值就是矩阵对角线上的元素。

$\det (\boldsymbol{A} - \lambda \boldsymbol{I}) = \left| {\begin{array}{*{20}{c}} {3{\rm{ - }}\lambda }&1\\ 0&{3{\rm{ - }}\lambda } \end{array}} \right| = {(3 - \lambda )^2} =0$ 。

可以解得 $\lambda_1=\lambda_2=3$ 。

$(\boldsymbol{A} - \lambda \boldsymbol{I})\boldsymbol{x} = \left[ {\begin{array}{*{20}{c}} 0&1\\ 0&0 \end{array}} \right]\boldsymbol{x} = 0$ 。得到**x**1= $\left[ {\begin{array}{*{20}{c}} 1\\ 0 \end{array}} \right]$ ，而没有**x**2。说明***A***是一个退化矩阵，对应相同的特征值而特征向量短缺。



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

# 第23讲 微分方程和 e^{\boldsymbol{A}t}e^{\boldsymbol{A}t} 

Differential equations and $e^{\boldsymbol{A}t}$

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AVIBM)

$\frac{{d\boldsymbol{u}}}{{dt}} = \boldsymbol{A}\boldsymbol{u}$ 

本讲中我们将面对微分方程，将一阶常系数微分方程转化为线性代数问题进行处理。主要思路基于常系数线性方程的解是指数形式，而寻找其指数和系数就是线代主要研究的问题。这里会涉及到矩阵型指数的运算$e^{\boldsymbol{A}t}$。

- **微分方程 Differential equations **

例： $\begin{array}{l} \frac{{d{u_1}}}{{dt}} =  - {u_1} + 2{u_2}\\ \frac{{d{u_2}}}{{dt}} = {u_1} - 2{u_2} \end{array}$ ,初值条件u1=1，u2=0。

则有$\frac{{d\boldsymbol{u}}}{{dt}} = \boldsymbol{A}\boldsymbol{u}$， $\boldsymbol{A}=\left[ {\begin{array}{*{20}{c}} {{\rm{ - }}1}&2\\ 1&{{\rm{ - }}2} \end{array}} \right]$ ， $\boldsymbol{u}(0)=\left[ {\begin{array}{*{20}{c}} 1\\ 0 \end{array}} \right]$ 。

分析矩阵***A***的目的是要追踪**u**随时间的变化，而首先要做的是找到矩阵的特征值和特征向量。矩阵***A***为奇异矩阵，因此存在一个特征值 $\lambda_1=0$ ，而矩阵的迹为-3，因此还有一个特征值为$\lambda_2=-3$。

一阶线性微分方程的解的形式是 $e^{\lambda t}$ 。两个特征值中，0会使结果达到稳态，而-3所对应的$e^{-3t}$ 会随时间增大而变小。

方程的通解为 $\boldsymbol{u}({\rm{t}}) = {{c}_1}{{e}^{{\lambda _1}t}}{\boldsymbol{x}_1} + {{c}_2}{{e}^{{\lambda _2}t}}{\boldsymbol{x}_2}$ 。

> 尽管直接代入可以验证 ${{e}^{{\lambda _1}t}}{\boldsymbol{x}_1} $ 是方程的解，但类似我这种比较笨的，对微分方程的解$e^{\lambda t}$ 是如何跟矩阵的特征值联系起来的根本理解不了，只好用差商方程帮助理解。方程所求的是t时刻**u**的状态**u**(t)，设需要N步从**u**(0)达到**u**(t)，且每一步都满足$\frac{{d\boldsymbol{u}}}{{dt}} = \boldsymbol{A}\boldsymbol{u}$，即 $\frac{{{\boldsymbol{u}_{step(n{\rm{ + }}1)}} - {\boldsymbol{u}_{step(n)}}}}{{\Delta t}} = \frac{{{\boldsymbol{u}_{step(n{\rm{ + }}1)}} - {\boldsymbol{u}_{step(n)}}}}{{t/N}} = \boldsymbol{A}{\boldsymbol{u}_{step(n)}}$ ，从**u**(0)=**u**step(0)开始进行计算： $\frac{{{\boldsymbol{u}_{step(1)}} - {\boldsymbol{u}_{step(0)}}}}{{t/N}} = \boldsymbol{A}{\boldsymbol{u}_{step(0)}}$ ，则有 ${\boldsymbol{u}_{step(1)}} = (\frac{t}{N}\boldsymbol{A} + 1){\boldsymbol{u}_{step(0)}}{\rm{ = }}(\frac{t}{N}\boldsymbol{A}  + 1)\boldsymbol{u}(0)$ 
> ,将**u**(0)表示成为矩阵特征向量的线性组合，则有 $\boldsymbol{u}(0)=c_1\boldsymbol{x}_1+c_2\boldsymbol{x}_2$ ， $\boldsymbol{A}\boldsymbol{u}(0)=c_1\lambda_1\boldsymbol{x}_1+c_2\lambda_2\boldsymbol{x}_2$ ，代入前式得到 ${\boldsymbol{u}_{step(1)}} = {{c}_1}(\frac{t}{N}{\lambda _1} + 1){\boldsymbol{x}_1} + {{c}_2}(\frac{t}{N}{\lambda _2} + 1){\boldsymbol{x}_2}$ ,
> ${\boldsymbol{u}_{step(2)}} = (\frac{t}{N}\boldsymbol{A} + 1){\boldsymbol{u}_{step(1)}} = {{c}_1}{(\frac{t}{N}{\lambda _1} + 1)^2}{\boldsymbol{x}_1} + {{c}_2}{(\frac{t}{N}{\lambda _2} + 1)^2}{\boldsymbol{x}_2}$ ，重复代入过程最后得到： $\boldsymbol{u}(t)={\boldsymbol{u}_{step(N)}}  = {{c}_1}{(\frac{t}{N}{\lambda _1} + 1)^N}{\boldsymbol{x}_1} + {{c}_2}{(\frac{t}{N}{\lambda _2} + 1)^N}{\boldsymbol{x}_2}$，因为 $\mathop {\lim }\limits_{k \to \infty } {(\frac{1}{{{k_{}}}} + 1)^k} \to e$ ，所以可求得$\boldsymbol{u}({\rm{t}}) = {{c}_1}{{e}^{{\lambda _1}t}}{\boldsymbol{x}_1} + {{c}_2}{{e}^{{\lambda _2}t}}{\boldsymbol{x}_2}$ 。

将$\lambda_1=0$ ，$\lambda_2=-3$代入$(\boldsymbol{A}-\lambda \boldsymbol{I})\boldsymbol{x}=\boldsymbol{0}$ ，分别求得对应的特征向量**x**1= $\left[ {\begin{array}{*{20}{c}} 2\\ 1 \end{array}} \right]$ ，**x**2=$\left[ {\begin{array}{*{20}{c}} 1\\ -1 \end{array}} \right]$ ，$\boldsymbol{u}({\rm{t}}) = {{c}_1}{{e}^{{\lambda _1}t}}{\boldsymbol{x}_1} + {{c}_2}{{e}^{{\lambda _2}t}}{\boldsymbol{x}_2}={{c}_1}{{e}^0}\left[ {\begin{array}{*{20}{c}} 2\\ 1 \end{array}} \right] + {{c}_2}{{e}^{ - 3t}}\left[ {\begin{array}{*{20}{c}} 1\\ { - 1} \end{array}} \right]$ 。

由初始条件得 $\boldsymbol{u}(0) = {c_1}\left[ {\begin{array}{*{20}{c}} 2\\ 1 \end{array}} \right] + {c_2}\left[ {\begin{array}{*{20}{c}} 1\\ { - 1} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 1\\ 0 \end{array}} \right]$ ,可解得c1=c2=1/3。

因此 $\boldsymbol{u}({\rm{t}}) = \frac{1}{3}\left[ {\begin{array}{*{20}{c}} 2\\ 1 \end{array}} \right] + \frac{1}{3}{e^{ - 3t}}\left[ {\begin{array}{*{20}{c}} 1\\ { - 1} \end{array}} \right]$ ，前一项为稳态状态，后一项随着时间衰减。


---


稳定性：并不是所有的系统都会达到稳态，矩阵的特征值会告诉我们**u**(t)的发展趋势。

1. Re( $\lambda$ )<0，则有**u**(t)→0。（支配稳定性的是实部，虚部的作用是在单位圆上转圈。）
2. 稳态：有一个特征值为0，并且其它所有的特征值实部为负数。
3. 至少有一个特征值满足Re( $\lambda$ )>0，则发散。

如果二阶矩阵***A***= $\left[ {\begin{array}{*{20}{c}} a&b\\ c&d \end{array}} \right]$ 的两个特征值实部为负数，则矩阵的迹a+d也是负数。反之并不一定成立，例如矩阵$\left[ {\begin{array}{*{20}{c}} -2&0\\ 0&1 \end{array}} \right]$ 的迹为-1，但是一个特征值为1。如果二阶矩阵的行列式为正而迹为负，则解为收敛的。


---


在方程$\frac{{d\boldsymbol{u}}}{{dt}} = \boldsymbol{A}\boldsymbol{u}$中，是矩阵***A***使得不同分量之间相互耦合。令**u**=***S*v**，其中***S***是由矩阵***A***的特征向量组成。则有：

$\boldsymbol{S}\frac{{d\boldsymbol{v}}}{{dt}} = \boldsymbol{AS}\boldsymbol{v}$ $ \Rightarrow \frac{{d\boldsymbol{v}}}{{dt}} = {\boldsymbol{S}^{ - 1}}\boldsymbol{AS}\boldsymbol{v} = \boldsymbol{\varLambda} \boldsymbol{v}$

新的方程不再耦合，则方程组的对角线为： $\frac{{d{v_i}}}{{dt}} = {\lambda _i}{v_i}$ ，方程组的通解为：

$\boldsymbol{v}(t) = {e^{\boldsymbol{\varLambda}  t}}\boldsymbol{v}(0)$ ， $\boldsymbol{u}(t) =\boldsymbol{S}{e^{\boldsymbol\varLambda  t}}{\boldsymbol{S}^{ - 1}}\boldsymbol{u}(0) = {e^{\boldsymbol{A}t}}\boldsymbol{u}(0)$ 

- **矩阵指数函数 Matrix exponential ** $e^{\boldsymbol{A}t}$ 

我们可以用幂级数的公式：

${e^x} = \sum\limits_{n = 0}^\infty  {\frac{{{x^n}}}{{n!}}}  = 1 + x + \frac{{{x^2}}}{2} + \frac{{{x^3}}}{6} +  \cdots $ 

来定义矩阵型指数运算$e^{\boldsymbol{A}t}$：

${e^{\boldsymbol{A} t}} = I + \boldsymbol{A}t + \frac{{{{(\boldsymbol{A}t)}^2}}}{2} + \frac{{{{(\boldsymbol{A}t)}^3}}}{6} +  \cdots $ 

如果***A***t的特征值很小，满足收敛条件 $\left| {\lambda (\boldsymbol{A}t)} \right|$ <1，则可以用几何级数来定义矩阵型指数：

$\frac{1}{{1 - x}} = \sum\limits_{n = 0}^\infty  {{x^n}}  \to {(I - \boldsymbol{A}t)^{ - 1}} = I + \boldsymbol{A}t + {(\boldsymbol{A}t)^2} + {\left( {\boldsymbol{A}t} \right)^3} +  \cdots $ 

前文中我们已经写出了矩阵指数函数的公式 ${e^{\boldsymbol{A} t}} = \boldsymbol{S}{e^{\boldsymbol\varLambda  t}}{\boldsymbol{S}^{ - 1}}$ 。如果矩阵***A***具有n个线性无关的特征向量，我们可以从幂级数定义的矩阵指数公式来再次验证：

$\begin{array}{*{20}{l}} {{e^{\boldsymbol{A} t}}}&{ = I + \boldsymbol{A}t + \frac{{{{(\boldsymbol{A}t)}^2}}}{2} + \frac{{{{(\boldsymbol{A}t)}^3}}}{6} +  \cdots }\\ {}&{ = \boldsymbol{S}{ \boldsymbol{S}^{ - 1}} +  \boldsymbol{S}\boldsymbol\varLambda { \boldsymbol{S}^{ - 1}}t + \frac{{ \boldsymbol{S}{\boldsymbol\varLambda ^2}{ \boldsymbol{S}^{ - 1}}}}{2}{t^2} + \frac{{ \boldsymbol{S}{\boldsymbol\varLambda ^3}{ \boldsymbol{S}^{ - 1}}}}{6}{t^3} +  \cdots }\\ {}&{ =  \boldsymbol{S}(I + \boldsymbol\varLambda t + \frac{{{\boldsymbol\varLambda ^2}}}{2}{t^2} + \frac{{{\boldsymbol\varLambda ^3}}}{6}{t^3} +  \cdots ){ \boldsymbol{S}^{ - 1}}}\\ {}&{ =  \boldsymbol{S}{e^{\boldsymbol\varLambda  t}}{ \boldsymbol{S}^{ - 1}}} \end{array}$ 

能够对角化的矩阵都可以表示为上式。

${e^{\boldsymbol\varLambda  t}} = \left[ {\begin{array}{*{20}{c}} {{e^{{\lambda _1}}}^t}&0& \cdots &0\\ 0&{{e^{{\lambda _2}}}^t}&{}&0\\  \vdots &{}& \ddots & \vdots \\ 0& \cdots &0&{{e^{{\lambda _n}}}^t} \end{array}} \right]$ 

- **二阶微分方程 Second order differential equations**

我们可以将二阶微分方程 $y'' + by' + ky = 0$ 转化为2x2的一阶问题进行处理，构造方法类似于我们对斐波那契数列的处理方法。

令**u**= $\left[ {\begin{array}{*{20}{c}} {y'}\\ y \end{array}} \right]$ ，则有**u'**= $\left[ {\begin{array}{*{20}{c}} {y''}\\ {y'} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} { - b}&{ - k}\\ 1&0 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {y'}\\ y \end{array}} \right]$ 

如果是k阶微分方程，那么需要一个kxk矩阵，除了第一行和对角线下面一排斜线上的元素之外，这个系数矩阵其它元素均为0。

# 第24讲 马尔可夫矩阵；傅里叶级数

Markov matrices; Fourier series

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AVOAV)

本讲学习马尔可夫矩阵和傅里叶级数，两者是关于特征值和投影矩阵的应用。

- **马尔可夫矩阵 Markov matrices**

***A***= $\left[ {\begin{array}{*{20}{c}} {0.1}&{0.01}&{0.3}\\ {0.2}&{0.99}&{0.3}\\ {0.7}&0&{0.4} \end{array}} \right]$ 

形如矩阵***A***，任何元素非负，且每列的元素加和为1的矩阵被称为马尔可夫矩阵。马尔可夫矩阵主要应用在概率领域。将一个马尔可夫矩阵进行方幂运算得到的矩阵仍旧是马尔可夫矩阵。

当处理一个微分方程问题时，特征值0意味着得到一个稳态。当进行矩阵的方幂运算时，特征值给出稳态的条件包括：

1. $\lambda_1$ =1是特征值之一。
2. 其它特征值的绝对值都比1小，$\left| {{\lambda _i}} \right|$ <1。

如我们所知，如果矩阵具有n个线性无关的特征向量，则有：

$\boldsymbol{u}_k=\boldsymbol{A}^k\boldsymbol{u}_0 = {{c}_1}{{{\lambda _1}^k}}{\boldsymbol{x}_1} + {{c}_2}{{{\lambda _2}^k}}{\boldsymbol{x}_2}+…+{{c}_n}{{{\lambda _n}^k}}{\boldsymbol{x}_n}$ 。

如果$\lambda_1$ =1并且其他的特征值都小于1，则系统在k增大过程中趋近于**u**0的分量 $c_1\boldsymbol{x}_1$ ，即给出了一个稳态状况。这里特征向量**x**1的每一分量都是正的，因此若初始值为正，则最终的稳态也是正的。

Markov矩阵每一列的元素加和为1这个条件，保证了矩阵具有1这个特征值。

***A***-***I***= $\left[ {\begin{array}{*{20}{r}} { - .9}&{.01}&{.3}\\ {.2}&{ - .01}&{.3}\\ {.7}&0&{ - .6} \end{array}} \right]$ 

从每一列减去1，则每列的加和都从1变为0。这时候行向量相加的结构就是**0**向量，因此行向量线性相关，矩阵为奇异矩阵。矩阵***A***有特征向量在***A***-***I***的零空间中，其对应的特征值为1。回代计算可得**x**1= $\left[ {\begin{array}{*{20}{c}} {0.6}\\ {33}\\ {0.7} \end{array}} \right]$ 。


---


**转置矩阵的特征值：**转置矩阵 $\boldsymbol{A}^T$ 具有和原矩阵***A***相同的特征值。

$(\boldsymbol{A}-\lambda\boldsymbol{I})^T=\boldsymbol{A}^T-\lambda\boldsymbol{I}$ 

则由行列式的性质10可知 $\det(\boldsymbol{A}-\lambda \boldsymbol{I})=\det(\boldsymbol{A}^T-\lambda \boldsymbol{I})$ 。如果 $\lambda$ 是矩阵***A***的特征值，则其满足$\det(\boldsymbol{A}^T-\lambda \boldsymbol{I})=0$ 。0，因此它也是转置矩阵 $ \boldsymbol{A}^T$ 的特征值。

但是两者特征向量有所区别，零空间不等同于左零空间。


---


我们用马尔可夫矩阵来研究人口流动问题。

${\left[ {\begin{array}{*{20}{c}} {{u_{Cal}}}\\ {{u_{Mass}}} \end{array}} \right]_{t = k + 1}} = \left[ {\begin{array}{*{20}{c}} {.9}&{.2}\\ {.1}&{.8} \end{array}} \right]{\left[ {\begin{array}{*{20}{c}} {{u_{Cal}}}\\ {{u_{Mass}}} \end{array}} \right]_{t = k}}$ 

方程中**u**的分量分别代表加利福尼亚州和马萨诸塞州的人口，矩阵中的每一列中元素代表着人口去留比例，比如第一列0.9表示留在加州的人口占加州人口的90%，而10%进入麻省，第二列中由麻省进入加州的人口占麻省的20%，而80%选择留在麻省。如果取初值 ${\left[ {\begin{array}{*{20}{c}} {{u_{Cal}}}\\ {{u_{Mass}}} \end{array}} \right]_0} = \left[ {\begin{array}{*{20}{c}} 0\\ {1000} \end{array}} \right]$ ，则经过一次迁徙 ${\left[ {\begin{array}{*{20}{c}} {{u_{Cal}}}\\ {{u_{Mass}}} \end{array}} \right]_1} = \left[ {\begin{array}{*{20}{c}} {.9}&{.2}\\ {.1}&{.8} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 0\\ {1000} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {200}\\ {800} \end{array}} \right]$ 。

为了获取长时间后的人口分布，我们需要了解矩阵的特征值和特征向量。因为这是马尔可夫矩阵，所以有一个特征值1，则另一个特征值为0.9+0.8-1=0.7。可以求得**x**1= $\left[ {\begin{array}{*{20}{c}} 2\\ 1 \end{array}} \right]$ ，**x**2= $\left[ {\begin{array}{*{20}{c}} 1\\ { - 1} \end{array}} \right]$ 。从$\left[ {\begin{array}{*{20}{c}} 2\\ 1 \end{array}} \right]$可知最后的稳态为加州人口2/3，麻省人口1/3。

通解为： $\boldsymbol{u}_k={c_1}\left[ {\begin{array}{*{20}{c}} 2\\ 1 \end{array}} \right] + {c_2}{(0.7)^k}\left[ {\begin{array}{*{20}{c}} { - 1}\\ 1 \end{array}} \right]$ ，可以从**u**0解得c1=1000/3,c2=2000/3。

- **傅里叶级数和投影矩阵 Fourier series & Projections**

如果有一组标准正交基**q**1，**q**2……**q**n为则任意向量**v**可以写成：

$\boldsymbol{v}=x_1\boldsymbol{q}_1+x_2\boldsymbol{q}_2+…+x_n\boldsymbol{q}_n$ ,

因为当i，j不相等时有 $\boldsymbol{q}_i^T\boldsymbol{q}_j=0$ 。因此有$\boldsymbol{q}_i^T\boldsymbol{v}=x_1\boldsymbol{q}_i^T\boldsymbol{q}_1+x_2\boldsymbol{q}_i^T\boldsymbol{q}_2+…+x_n\boldsymbol{q}_i^T\boldsymbol{q}_n=x_i$ 。

我们得到了分量xi的公式： $x_i=\boldsymbol{q}_i^T\boldsymbol{v}$ 。

因为 $\boldsymbol{v}=\left[ {\begin{array}{*{20}{c}} {{\boldsymbol{q}_1}}& \cdots &{{\boldsymbol{q}_n}} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{x_1}}\\  \vdots \\ {{x_n}} \end{array}} \right]$，即**v**=***Q*x**，所以 $\boldsymbol{x}=\boldsymbol{Q}^{-1}\boldsymbol{v}$ 。因为***Q***为正交矩阵，所以有 $\boldsymbol{Q}^{-1}=\boldsymbol{Q}^T$ ,可得 $\boldsymbol{x}=\boldsymbol{Q}^{T}\boldsymbol{v}$ 。这与我们之前得到的$x_i=\boldsymbol{q}_i^T\boldsymbol{v}$ 完全相同。这里给出了求分量的思路就是用空间的一组标准正交基去点乘目标向量，利用其标准正交的性质得到所求。

标准正交是此处的核心概念。而傅里叶级数也是在这个概念上构建的。我们可以对任意函数做傅里叶展开，得到表达式： $f(x) = {a_0} + {a_1}\cos x + {b_1}\sin x + {a_2}\cos 2x + {b_2}\sin 2x +  \cdots $ 

与之前的有限个标准正交向量组成的正交矩阵不同，这个空间是无限维，它的一组基是1，cosx，sinx，cos2x，sin2x……

此处的正交概念与**R**n空间不同，点积的概念也不同。

向量$\boldsymbol{v}^T\boldsymbol{w}=v_1w_1+v_2w_2+…+v_nw_n$ ,

函数 ${f^T}g = \int_0^{2\pi } {f(x)g(x)dx} $ 

计算基sinx和cosx的点积可以验证其正交性。

$\int_0^{2\pi } {\sin x\cos xdx}  = \frac{1}{2}{(\sin 2x)^2}\left| {_0^{2\pi }} \right. = 0$ 

采用和标准正交基相同的策略可以得到傅里叶变换的参数。

$\begin{array}{*{20}{l}} {\int_0^{2\pi } {f(x)\cos xdx} }&{ = \int_0^{2\pi } {({a_0} + {a_1}\cos x + {b_1}\sin x + {a_2}\cos 2x +  \cdots )\cos xdx} }\\ {}&{ = 0 + \int_0^{2\pi } {{a_1}{{\cos }^2}xdx}  + 0 + 0 \cdots }\\ {}&{ = {a_1}\pi } \end{array}$ 

可以得到 ${a_1} = \frac{1}{\pi }\int_0^{2\pi } {f(x)\cos xdx} $ ，同理可以求得其它参数。


---


> 之前我们已经提到了G. Strang 所讲的线代和其他人的差别，学习越深入则越能体会到这一点。网上有一篇《理解矩阵》的博客介绍了很多大家对线代的认识误区，在开篇处作者就点出了初学者面对线代为什么觉得困难，因为我们目前学习的线代是通过公理化来表述的第二代数学模型，而此前大家都是在以实用为导向的第一代数学模型中，困难来自于全面提升的抽象性。G. Strang 做的事情大体上可以理解为在第一代数学模型中讨论线性计算的核心内容，因此在学习中可以保留直觉性，非常大程度地降低了抽象性带来的困难。这种讲授思路的优劣，只有在有明确的目标情况下才好判定。换句话说，看你学线代的目的是什么，如果是数值计算或者是在一些实验科学中使用矩阵工具，那么G. Strang 讲授的内容非常恰如其分。至于更具抽象性的部分，我推荐《线性代数应该这样学》这本书，以线性算子作为核心，可以从另一种框架下领略线代的魅力，并且深入地理解线性代数的内涵。

# 复习二 

Exam 2 Review

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M7E4C9V6P)

> 不知道为什么视频课程中这次复习课没有排入课号。

- **第二单元主要内容**

1)正交矩阵***Q***，用矩阵形式描述正交性质。

![](https://pic3.zhimg.com/v2-8584acd857dca173361d22ad5161885e_b.jpg)

投影矩阵***P***，最小二乘法，在方程无解时求“最优解”。

Gram-Schmidt正交化——从任意一组基得到标准正交基，策略是从向量中减去投影到其它向量方向的分量。

2)行列式det(***A***)

三个性质定义了行列式，可以推导出之后的性质4~10。

行列式展开公式包含n!个非零项，一半取+，一半取-。

代数余子式公式，以及推导出逆矩阵公式：${\boldsymbol{A}^{ - 1}} = \frac{1}{{\det (\boldsymbol{A})}}{\boldsymbol{C}^T}$ 。

3)特征值$\boldsymbol{A}\boldsymbol{x}=\lambda\boldsymbol{x}$

$$
det(\boldsymbol{A}-\lambda\boldsymbol{I})=0
$$

对角化：如果矩阵***A***包含n个线性无关的特征向量，可以对角化得到$\boldsymbol{S}^{-1}\boldsymbol{AS}=\boldsymbol{\varLambda}$***。***

矩阵***A***的幂： $\boldsymbol{A}^k=(\boldsymbol{S}\boldsymbol{\varLambda}\boldsymbol{S}^{-1})^k=\boldsymbol{S}\boldsymbol{\varLambda}^{k}\boldsymbol{S}^{-1}$


---


**例题**

**例1**.	**a**= $\left[ {\begin{array}{*{20}{c}} 2\\ 1\\ 2 \end{array}} \right]$ 

a）求投影到向量**a**方向的投影矩阵***P***。

解： $\boldsymbol{P}=\boldsymbol{A}(\boldsymbol{A}^T\boldsymbol{A})^{-1}\boldsymbol{A}^T$ ，这里**a**是向量，因此有 $\boldsymbol{P}=\frac{{\boldsymbol{a}{\boldsymbol{a}^T}}}{{{\boldsymbol{a}^T}\boldsymbol{a}}}=\frac{1}{9}\left[ {\begin{array}{*{20}{c}} 4&2&4\\ 2&1&2\\ 4&2&4 \end{array}} \right]$ 

b）求矩阵***P***的秩

解：矩阵的秩为1，因为所有的列都是第二列的倍数。或者从投影矩阵投影的空间是1维可以判断出来。

c）矩阵***P***的列空间？

解：向量**a**所在的直线。

d）矩阵***P***的特征值？

解：矩阵的秩为1，因此存在重特征值0，再从矩阵的迹可以得到另一个特征值为1。即特征值为1,0,0。

e）求矩阵***P***对应特征值1的特征向量？

解：因为矩阵***P***为投影矩阵，在投影空间中的向量就是对应特征值1的特征向量，因此**a**就是对应的特征向量。

f）若有 $\boldsymbol{u}_{k+1}=\boldsymbol{P}\boldsymbol{u}_k$ ，且有初值**u**0= $\left[ {\begin{array}{*{20}{c}} 9\\ 9\\ 0 \end{array}} \right]$ 。求**u**k？

解：重复将一个向量投影到一条直线，从第二次开始投影结果即不发生变化。

$\boldsymbol{u}_{k+1}=\boldsymbol{P}^k\boldsymbol{u}_0=\boldsymbol{P}\boldsymbol{u}_0=\boldsymbol{a}\frac{{{\boldsymbol{a}^T}{\boldsymbol{u}_0}}}{{{\boldsymbol{a}^T}\boldsymbol{a}}}=3\boldsymbol{a}=\left[ {\begin{array}{*{20}{c}} 6\\ 3\\ 6 \end{array}} \right]$ 

g）测验中可能出现$\boldsymbol{u}_{k+1}=\boldsymbol{A}\boldsymbol{u}_k$ ，其中的矩阵***A***不是投影矩阵，没有投影矩阵的性质 $\boldsymbol{P}^k\boldsymbol{u}_0=\boldsymbol{P}\boldsymbol{u}_0$ ，此时需要求矩阵的特征值和特征向量。

$\boldsymbol{u}_0=c_1\boldsymbol{x}_1+c_2\boldsymbol{x}_2+c_3\boldsymbol{x}_3$ ，则$\boldsymbol{u}_k= {{c}_1}{{{\lambda _1}^k}}{\boldsymbol{x}_1} + {{c}_2}{{{\lambda _2}^k}}{\boldsymbol{x}_2}+{{c}_3}{{{\lambda _3}^k}}{\boldsymbol{x}_3}$ 。

对于投影矩阵而言， $\lambda_1=1$ ， $\lambda_2=\lambda_3=0$ 。因此有**u**1=**u**2=**u**3=……




**例2**.	已知以下数据点

![](https://pic4.zhimg.com/v2-485ca983e1bb1d0ca1cf484c50ed635f_b.jpg)

a）求利用三个数据点拟合过原点的一条直线y=Dt？

解： $\left[ {\begin{array}{*{20}{c}} 1\\ 2\\ 3 \end{array}} \right]D = \left[ {\begin{array}{*{20}{c}} 4\\ 5\\ 8 \end{array}} \right]$ ，我们求解的问题就是求方程的最优解 $\hat D$ 。 $\boldsymbol{A}^T\boldsymbol{A}\hat D=\boldsymbol{A}^T\boldsymbol{b}$ 。

解得$\hat D$ =19/7。因此直线解析式为y=(19/7)t。

b）怎样从投影来理解这个问题？

解：对于最小二乘问题有两种理解方法。其一是找到平面内最优的一条直线。另一种是将**b**= $\left[ {\begin{array}{*{20}{c}} 4\\ 5\\ 8 \end{array}} \right]$ 投影到***A***的列空间，来得到最接近于***A*x**=**b**的解。




**例3**.	向量**a**1= $\left[ {\begin{array}{*{20}{c}} 1\\ 2\\ 3 \end{array}} \right]$ 和**a**2= $\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 1 \end{array}} \right]$ 确定了一个平面，找到该平面的一组正交基。

解：应用Gram-Shmidt正交化方法。取**a**1为第一个方向，找出垂直于该方向的向量**B**。策略就是在**a**2中减掉它在**a**1方向上的分量，得到完全垂直于**a**1的部分：

$\boldsymbol{B} = {\boldsymbol{a}_2} - \frac{{{\boldsymbol{a}_1}^T{\boldsymbol{a}_2}}}{{{\boldsymbol{a}_1}^T{\boldsymbol{a}_1}}}{\boldsymbol{a}_1} = \left[ {\begin{array}{*{20}{c}} {4/7}\\ {1/7}\\ { - 2/7} \end{array}} \right]$ 




**例4**.	已知一个4阶方阵***A***具有特征值 $\lambda_1,\lambda_2,\lambda_3,\lambda_4$ 。

a）特征值需要满足什么条件才能保证***A***为可逆矩阵。

解：当且仅当矩阵的特征值均不为0的时候，***A***为可逆矩阵。若有特征值0存在，则矩阵零空间有非零向量，矩阵不可逆。

b）求逆矩阵行列式的值？

解： $\boldsymbol{A}^{-1}$ 的特征值为 $\boldsymbol{A}$ 特征值的倒数。因此，$\det(\boldsymbol{A}^{-1}) = \left(\frac{1}{{\lambda_1}}\right) \left(\frac{1}{{\lambda_2}}\right) \left(\frac{1}{{\lambda_3}}\right) \left(\frac{1}{{\lambda_4}}\right)$

c）求(***A***+***I***)的迹？

解：矩阵的迹等于其特征值的和，(***A***+***I***)的特征值为$\lambda_1+1,\lambda_2+1,\lambda_3+1,\lambda_4+1$ ，则该矩阵的迹为 $\lambda_1+\lambda_2+\lambda_3+\lambda_4+4$ 。




**例5**.	已知三对角矩阵： ${\boldsymbol{A}_4} = \left[ {\begin{array}{*{20}{c}} 1&1&0&0\\ 1&1&1&0\\ 0&1&1&1\\ 0&0&1&1 \end{array}} \right]$ 

令 $D_n=\det(\boldsymbol{A}_n)$ 

a）用代数余子式的方法求出 $D_n=aD_{n-1}+bD_{n-2}$ 中的a,b?

解：用代数余子式可得D4=(1)D3+(-1)D2。

b）利用找到的递归方程 $D_n=aD_{n-1}+bD_{n-2}$ ，求Dn？

解：把它当作方程组来求解，我们首先解得初值D1=1，D2=0。

按照递归方程构造2 阶线性方程： $\left[ {\begin{array}{*{20}{c}} {{D_n}}\\ {{D_{n - 1}}} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 1&{ - 1}\\ 1&0 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{D_{n - 1}}}\\ {{D_{n - 2}}} \end{array}} \right]$ 。求解矩阵的特征值可得： $\lambda  = \frac{{1 \pm \sqrt 3 i}}{2} = e \pm i\pi /3$ ，均是模为1 的复数，在单位圆上旋转。可以看到 $\lambda_1^6=\lambda_2^6=1$ ，矩阵经六次变换变为单位阵。该序列既不发散也不收敛，数列以6 次为重复周期不停循环，1,0,-1,0,1,1。




**例6**.	有一组对称矩阵：

${\boldsymbol{A}_2} = \left[ {\begin{array}{*{20}{r}} 0&1\\ 1&0 \end{array}} \right]$ , ${\boldsymbol{A}_3} = \left[ {\begin{array}{*{20}{r}} 0&1&0\\ 1&0&2\\ 0&2&0 \end{array}} \right]$ , ${\boldsymbol{A}_4} = \left[ {\begin{array}{*{20}{r}} 0&1&0&0\\ 1&0&2&0\\ 0&2&0&3\\ 0&0&3&0 \end{array}} \right]$ 

a）找到投影到矩阵$\boldsymbol{A}_3$列空间的投影矩阵***P***。

解：矩阵$\boldsymbol{A}_3$为奇异阵，其第3列列向量为第1列的3倍，而第1,2列线性无关，因此其列空间为一个平面，取其前两列列向量组成矩阵***A***，则有 $\boldsymbol{P}=\boldsymbol{A}(\boldsymbol{A}^T\boldsymbol{A})^{-1}\boldsymbol{A}^T=\left[ {\begin{array}{*{20}{r}} {1/5}&0&{2/5}\\ 0&1&0\\ {2/5}&0&{4/5} \end{array}} \right]$ 

可以通过将矩阵$\boldsymbol{A}_3$的列向量乘以投影矩阵来验证这一结果，在平面内的向量投影后应该不发生变化。

b）求$\boldsymbol{A}_3$的特征值和特征向量?

解： $\det ({\boldsymbol{A}_3} - \lambda \boldsymbol{I}) = \left| {\begin{array}{*{20}{c}} { - \lambda }&1&0\\ 1&{ - \lambda }&2\\ 0&2&{ - \lambda } \end{array}} \right| =  - {\lambda ^3} + 5\lambda  = 0$ 

解得三个特征值，$\lambda_1=0,\lambda_2=\sqrt{5},\lambda_3=-\sqrt{5}$ 。可用矩阵的迹做检查。

求解 $ ({\boldsymbol{A}_3} - \lambda \boldsymbol{I}) \boldsymbol{x}=\boldsymbol{0}$ ，可得特征向量 $\boldsymbol{x}_1=\left[ {\begin{array}{*{20}{c}} -2\\ 0\\ 1 \end{array}} \right]$ ， $\boldsymbol{x}_2=\left[ {\begin{array}{*{20}{c}} 1\\ -\sqrt{5}\\ 2 \end{array}} \right]$ ，$\boldsymbol{x}_3=\left[ {\begin{array}{*{20}{c}} 1\\ \sqrt{5}\\ 2 \end{array}} \right]$。

c）找到投影到矩阵$\boldsymbol{A}_4$列空间的投影矩阵***P***？

解：因为 $\boldsymbol{A}_4$ 为可逆矩阵，所以它的列空间就是整个**R**4空间，所以***P***=***I***。而可逆矩阵的证明可以采用求行列式的办法，用代数余子式展开可得det($\boldsymbol{A}_4$)=9。









# 第25讲 对称矩阵和正定性

Symmetric matrices and positive definiteness

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AVUL4)

进入第三单元学习，主题是正定矩阵及其应用。对称矩阵是最重要的矩阵之一，特征值为实数并且拥有一套正交特征向量。正定矩阵的性质则更好。

- **对称矩阵 Symmetric matrices**

对称矩阵 $\boldsymbol{A}=\boldsymbol{A}^T$ 。包含特殊性质的矩阵，例如Markov矩阵，其特征值和特征向量往往拥有一定特性。对称矩阵的特征值为实数，具有完全正交的特征向量。这里的“有”，是指可以选出一套完全正交的特征向量（例如在重特征值条件下，可能存在一个平面内向量都可以作为特征向量）。

如果***A***具有n个线性无关的特征向量，可以对角化得到 $\boldsymbol{A}=\boldsymbol{S}\boldsymbol{\varLambda}\boldsymbol{S}^{-1}$ 。而对于对称矩阵， $\boldsymbol{A}=\boldsymbol{Q}\boldsymbol{\varLambda}\boldsymbol{Q}^{-1}=\boldsymbol{Q}\boldsymbol{\varLambda}\boldsymbol{Q}^{T}$ ，其中***Q***为正交矩阵，列向量为标准正交基，这个公式本身还显示了矩阵的对称性。矩阵能够进行这种分解，在数学上称为“谱定理”（spectral theorem），将特征值视为“谱”，而在物理上称之为“主轴定理”。

- **实特征值 Real eigenvalues**

矩阵***A***具有特征值 $\lambda$ 和特征向量**x**，则有 $\boldsymbol{A}\boldsymbol{x}=\lambda\boldsymbol{x}$ 。若为复数，则其共轭复数满足

$\boldsymbol{A} \boldsymbol{\bar{x}} = \bar \lambda\boldsymbol{\bar x}$ 。两侧取转置，则有：$\boldsymbol{\bar{x}}^T\boldsymbol{A}^T=\boldsymbol{\bar{x}}^T\bar \lambda$ ，

两侧同乘**x**，则： $\boldsymbol{\bar{x}}^T\boldsymbol{A}^T\boldsymbol{x}=\boldsymbol{\bar{x}}^T\bar \lambda\boldsymbol{x}$ ，

因为矩阵为对称矩阵，则有： $\boldsymbol{\bar{x}}^T\lambda\boldsymbol{x}=\boldsymbol{\bar{x}}^T\bar \lambda\boldsymbol{x}$ ,若$\boldsymbol{\bar{x}}^T\boldsymbol{x}\ne0$ 则有 $\bar \lambda=\lambda$ ,即 $\lambda$ 为实数。

因为 $\bar {\boldsymbol{x}}$ 为**x**的共轭，因此两者点积得到的是**x**中的每一分量与其共轭复数的乘积之和，即复向量**x**之模，当且仅当**x**=**0**时，其模为0。

${\boldsymbol {\bar x}^T}\boldsymbol{x} = \left[ {\begin{array}{*{20}{c}} {{{\bar x}_1}}&{{{\bar x}_2}}&{{{\bar x}_3}}&{{{\bar x}_4}} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{x_1}}\\ {{x_2}}\\ {{x_3}}\\ {{x_4}} \end{array}} \right] = {\left| {{x_1}} \right|^2} + {\left| {{x_2}} \right|^2} + {\left| {{x_3}} \right|^2} + {\left| {{x_4}} \right|^2}$ 

因此得证$\lambda$ 为实数。

对于复矩阵***A***，若有$\boldsymbol{A}=\boldsymbol{\bar A}^T$ 则上面的推导全部成立，因此共轭对称复矩阵***A***的特征值为实数。

对于对称矩阵， $\boldsymbol{A}=\boldsymbol{Q}\boldsymbol{\varLambda}\boldsymbol{Q}^{-1}=\boldsymbol{Q}\boldsymbol{\varLambda}\boldsymbol{Q}^{T}$ ，可以写作：

$\begin{array}{*{20}{l}} \boldsymbol{A}=\boldsymbol{Q}\boldsymbol{\varLambda}\boldsymbol{Q}^{-1}&{{\rm{ = }}\left[ {\begin{array}{*{20}{c}} {{\boldsymbol{q}_1}}&{{\boldsymbol{q}_2}}& \cdots &{{\boldsymbol{q}_{\rm{n}}}} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{\lambda _1}}&{}&{}&{}\\ {}&{{\lambda _2}}&{}&{}\\ {}&{}& \ddots &{}\\ {}&{}&{}&{{\lambda _{\rm{n}}}} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{\boldsymbol{q}_1}^T}\\ {{\boldsymbol{q}_2}^T}\\  \vdots \\ {{\boldsymbol{q}_{\rm{n}}}^T} \end{array}} \right]}\\ {}&{{\rm{ = }}{\lambda _1}{\boldsymbol{q}_1}{\boldsymbol{q}_1}^T{\rm{ + }}{\lambda _2}{\boldsymbol{q}_2}{\boldsymbol{q}_2}^T{\rm{ + }} \cdots {\rm{ + }}{\lambda _{\rm{n}}}{\boldsymbol{q}_{\rm{n}}}{\boldsymbol{q}_{\rm{n}}}^T} \end{array}$ 

矩阵 $\boldsymbol{q}_k\boldsymbol{q}_k^T$ 是朝向向量**q**k的投影矩阵，所以每一个对称矩阵都是正交投影矩阵的线性组合。这是理解谱定理的另一种方法。

当确认矩阵特征值为实数后，下一个要考虑的问题就是它是正还是负数，因为这影响着微分方程中体系的稳定与否。但是对于大型矩阵通过计算 $\left| {\boldsymbol{A}{\rm{ - }}\lambda \boldsymbol{I}} \right|{\rm{ = }}0$ 得到特征值进行判定难以实现，即使用MATLAB求解结果也不一定可靠，但MATLAB可以得到矩阵的主元，而对称阵的主元中正负数的个数与特征值相同，即正主元的数目等于正特征值的数目。


---


> 对于对称阵主元与特征值符号相匹配这件事情，通常是用合同矩阵的惯性定理加以证明。若存在可逆矩阵**C **满足$\boldsymbol{A}=\boldsymbol{CBC}^T$ ，就称***A* **与***B* **为合同矩阵，惯性定理是指矩阵的特征值符号经过合同变换后不发生变化。对称阵***A ***经过消元操作可得$\boldsymbol{A}=\boldsymbol{L}\boldsymbol{D}\boldsymbol{L}^{T}$ ，而经过对角化处理得到$\boldsymbol{A}=\boldsymbol{Q}\boldsymbol{\varLambda}\boldsymbol{Q}^{T}$ ，两者比较可知$\boldsymbol{D}=(\boldsymbol{L}^{-1}\boldsymbol{Q})\boldsymbol{\varLambda}(\boldsymbol{L}^{-1}\boldsymbol{Q})^{T}$ ，因此两个对角阵为合同矩阵，主元和特征值的符号匹配。
> G.Strang 在书里给了一个接近同伦理论的证明：对于对称矩阵 可做分解，如$\left[ {\begin{array}{*{20}{c}} 1&3\\ 3&1 \end{array}} \right]{\rm{ = }}\left[ {\begin{array}{*{20}{c}} 1&{}\\ 3&1 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1&{}\\ {}&{{\rm{ - }}8} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1&3\\ {}&1 \end{array}} \right]$ ，在下三角阵转变 $\left[ {\begin{array}{*{20}{c}} 1&0\\ 3&1 \end{array}} \right] \to \left[ {\begin{array}{*{20}{c}} 1&0\\ 0&1 \end{array}} \right]$的过程中，矩阵的变化为 $\left[ {\begin{array}{*{20}{c}} 1&3\\ 3&1 \end{array}} \right] \to \left[ {\begin{array}{*{20}{c}} 1&0\\ 0&{{\rm{ - }}8} \end{array}} \right]$ ，矩阵的特征值也从4，-2 变为1，-8（即原矩阵的主元）。这个过程中如果特征值发生符号变化，则总有一个瞬间特征值穿过0点，那个瞬间矩阵应该是奇异阵，但是相乘的三个矩阵一直是非奇异阵，因此不可能有这样一个时刻存在，所以特征值不会发生符号变化，即和主元符号保持一致。


---


矩阵***A***+b***I***的特征值比矩阵***A***的特征值大b，可以通过***A***+b***I***的主元来了解矩阵***A***的特征值与b的大小关系，因此利用这个性质可以估计特征值的状态。

- **正定矩阵 Positive definite matrices**

正定矩阵***A***是特征值都为正数的对称矩阵。它的主元也均为正数。

例如矩阵***A***= $\left[ {\begin{array}{*{20}{c}} 5&2\\ 2&3 \end{array}} \right]$ 。主元为5和det***A***/5=11/5。对称矩阵主元都为正数，则是正定矩阵。计算其特征值为： $\left| {\boldsymbol{A}-\lambda \boldsymbol{I}} \right|{\rm{ = }}{\lambda ^2}{\rm{ - 8}}\lambda {\rm{ + 11 = }}0$ ， $\lambda {\rm{ = 4}} \pm \sqrt 5 $ 。

因为主元和特征值都是正的，可以知道正定矩阵的特征值也是正的。但是反之并不成立。矩阵 $\left[ {\begin{array}{*{20}{c}} {{\rm{ - }}1}&0\\ 0&{{\rm{ - }}3} \end{array}} \right]$ 的行列式也是正的，但不是正定矩阵。

若将行列式作为正定的判据，则要求n阶矩阵左上角的所有kxk（1<=k<=n）子行列式（subdeterminant）数值均为正，矩阵确定为正定矩阵。

本讲的内容将之前教授的主元、行列式和特征值的概念结合在了一起，对于正定矩阵这些都是正的，当完全掌握了它们的性质后会推广到非对称矩阵，甚至非方阵。





# 第26讲 复矩阵；快速傅里叶变换

Complex matrices; fast Fourier transform

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2B4U77)

实矩阵也可能有复特征值，因此无法避免在矩阵运算中碰到复数，本讲学习处理复数矩阵和复向量。

最重要的复矩阵是傅里叶矩阵，它用于傅里叶变换。而对于大数据处理快速傅里叶变换（FFT）显得更为重要，它将矩阵乘法的运算次数从 $n^2$ 次降至 $nlog_2n$次。

- **复向量 Complex vectors**

对于给定的复向量**z**= $\left[ {\begin{array}{*{20}{c}} {{z_1}}\\ {{z_2}}\\  \vdots \\ {{z_{\rm{n}}}} \end{array}} \right] \in {\boldsymbol{C}^n}$ ，其元素中有复数，因此 $\boldsymbol{z}^T\boldsymbol{z}$ 无法给出向量的长度。例如： $\left[ {\begin{array}{*{20}{c}} 1&i \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1\\ i \end{array}} \right] = 0$ 。则定义 ${\left| \boldsymbol{z} \right|^2}={\bar {\boldsymbol z}^T}\boldsymbol z={\left| {{z_1}} \right|^2} + {\left| {{z_1}} \right|^2} +  \cdots  + {\left| {{z_1}} \right|^2}$ 为向量长度。因此向量 $\left[ {\begin{array}{*{20}{c}} 1\\ i \end{array}} \right]$ 的长度就是 $\left[ {\begin{array}{*{20}{c}} 1&{{\rm{ - }}i} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1\\ i \end{array}} \right] = 2$ 。记 $\left| \boldsymbol{z} \right|^2=\boldsymbol{\bar z}^T\boldsymbol{z}={\boldsymbol{z}^H}\boldsymbol{z}$ 。H来自于“Hermite”。

与之相似，内积的定义也变为 ${\boldsymbol{y}^H}\boldsymbol{x}={\boldsymbol{\bar y}^T}\boldsymbol{x}={\bar y_1}{x_1} + {\bar y_2}{x_2} +  \cdots  + {\bar y_n}{x_n}$ 。

- **复矩阵 Complex matrices**

上一讲中讲到了对于复矩阵***A***，若有 $\boldsymbol{\bar A}^T=\boldsymbol{A}$ 则复矩阵***A***的特征值为实数。这种复矩阵被称为埃尔米特矩阵（Hermitian matrixes）。又译作“厄米特矩阵”或者“厄米矩阵”。转置共轭记作$\boldsymbol{A}^H=\boldsymbol{\bar A}^T$。

例如矩阵 $\left[ {\begin{array}{*{20}{c}} 2&{3{\rm{ + }}i}\\ {3 - i}&5 \end{array}} \right]$ 为埃尔米特矩阵。它具有实数特征值和正交的特征向量。由性质可知埃尔米特矩阵对角线均为实数。

此处向量标准正交的意思是 ${\boldsymbol{\bar q}_{j}}^T{\boldsymbol{q}_{k}}=\left\{ {\begin{array}{*{20}{c}} 0&{j \ne k}\\ 1&{j = k} \end{array}} \right.$ 。用n个标准正交的复向量作为列向量可以构造一个矩阵***Q***，则有 ${\boldsymbol{Q}^T}\boldsymbol{Q} =\boldsymbol{I} = {\boldsymbol{Q}^H}\boldsymbol{Q}$ 。这个复空间的正交矩阵称为酉矩阵（unitary matrix）。

- **傅里叶变换Fourier transform**

傅里叶级数是将周期函数或者信号变换为不同频率的三角函数的和函数。

$f(x) = {a_0} + {a_1}\cos x + {b_1}\sin x + {a_2}\cos 2x + {b_2}\sin 2x +  \cdots $ 

在电子工程或者计算机科学中，矩阵的行和列从第0行和第0列开始计数，最后到第n-1行和第n-1列。我们在讨论傅里叶矩阵的时候遵从这种习惯。

${\boldsymbol{F}_n} = \left[ {\begin{array}{*{20}{r}} 1&1&1& \cdots &1\\ 1&\omega &{{\omega ^2}}&{}&{{\omega ^{(n - 1)}}}\\ 1&{{\omega ^2}}&{{\omega ^2}}&{}&{{\omega ^{2(n - 1)}}}\\  \vdots &{}&{}& \ddots &{}\\ 1&{{\omega ^{n - 1}}}&{{\omega ^{2(n - 1)}}}&{}&{{\omega ^{{{(n - 1)}^2}}}} \end{array}} \right]$ 

$(\boldsymbol{F}_n)_{jk}=\omega^{jk}$ ，傅里叶矩阵为对称矩阵 $\boldsymbol{F}_n=\boldsymbol{F}_n^T$ 。矩阵中的 $\omega^n=1,\omega=e^{i2\pi/n}$ 。矩阵的列向量正交。的方次分布在复平面的单位元上，只是幅角不同。当n=4时，$\omega^4=1,\omega=e^{i2\pi/4}=i$。

${\boldsymbol{F}_4} = \left[ {\begin{array}{*{20}{c}} 1&1&1&1\\ 1&i&{{i^2}}&{{i^3}}\\ 1&{{i^2}}&{{i^4}}&{{i^6}}\\ 1&{{i^3}}&{{i^6}}&{{i^9}} \end{array}} \right] = \left[ {\begin{array}{*{20}{r}} 1&1&1&1\\ 1&i&{ - 1}&{ - i}\\ 1&{ - 1}&1&{ - 1}\\ 1&{ - i}&{ - 1}&i \end{array}} \right]$ 

从矩阵可以得到一个四点（离散的）傅里叶变换，它的逆矩阵就是反傅里叶变换。逆矩阵很容易计算，因为傅里叶矩阵列向量正交。实际上这个矩阵可以分解成一系列稀疏矩阵，并且它们的逆矩阵都很容易得到。

计算可知列向量的模不是1，矩阵除以2之后，向量标准正交： $\frac{1}{4}{\boldsymbol{F}_4}^H{\boldsymbol{F}_4}{\rm{ = }}\boldsymbol{I}$ 。它的逆矩阵就是共轭转置。

- **快速傅里叶变换 Fast Fourier transform**

对于64阶傅里叶矩阵$\boldsymbol{F}_{64}$ 中的 $\omega_{64}$ 与32阶傅里叶矩阵 $\boldsymbol{F}_{32}$ 的元素 $\omega_{32}$ 相比，幅角是其一半， $(\omega_{64})^2=\omega_{32}$ 。可以从分块矩阵运算找到两者的联系：

$\left[ {{\boldsymbol{F}_{64}}} \right]{\rm{ = }}\left[ {\begin{array}{*{20}{r}} \boldsymbol{I}&\boldsymbol{D}\\ \boldsymbol{I}&{ -\boldsymbol{D}} \end{array}} \right]\left[ {\begin{array}{*{20}{r}} {{\boldsymbol{F}_{32}}}&0\\ 0&{{\boldsymbol{F}_{32}}} \end{array}} \right]\left[ \boldsymbol{P} \right]$ 

其中***P***是置换矩阵，而***D***为对角矩阵：

$\boldsymbol{P}{\rm{ = }}\left[ {\begin{array}{*{20}{r}} 1&0&0&0& \cdots & \cdots &0&0\\ 0&0&1&0&{}&{}&0&0\\ {}&{}&{}& \vdots &{}&{}&{}&{}\\ 0&0&0&0& \cdots & \cdots &1&0\\ 0&1&0&0& \cdots & \cdots &0&0\\ 0&0&0&1& \cdots & \cdots &0&0\\ {}&{}&{}& \vdots &{}&{}&{}&{}\\ 0&0&0&0& \cdots & \cdots &0&1 \end{array}} \right]$ 

， $\boldsymbol{D} = \left[ {\begin{array}{*{20}{r}} 1&{}&{}&{}&{}\\ {}&\omega &{}&{}&{}\\ {}&{}&{{\omega ^2}}&{}&{}\\ {}&{}&{}& \ddots &{}\\ {}&{}&{}&{}&{{\omega ^{31}}} \end{array}} \right]$ 

***P***的效果是使得所乘的向量**x**序数为奇数的分量如x1，x3，x5等提到前面，而偶数分量x2，x4等放到后面。

计算64阶傅里叶变换（傅里叶矩阵乘以向量）的计算量是64x64，而等式右侧的计算量是2x32x32（两个32阶）再加上一些修正项，修正项主要来自于与对角矩阵***D***的乘法，大约为32次。继续对***F***32进行分解，计算的运算量再一次下降变为2 (2x16x16+16)+32。分解到最后，仅剩修正项的运算， $32\times log_264$ 次。对于n阶矩阵，即将$n^2$ 次计算降至 $(n/2)log_2n$次。例如对于1024阶矩阵，运算量从1024x1024降至5x1024。





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



# 第29讲 奇异值分解

Singular value decomposition

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2B5R1G)

本讲介绍奇异值分解（Singular value decomposition），简称SVD。这是矩阵最终也是最好的分解，任意矩阵可分解为 $\boldsymbol{A}=\boldsymbol{U}\boldsymbol{\varSigma} \boldsymbol{V}^T$ ，分解结果为正交矩阵***U***，对角阵$\boldsymbol{\varSigma}$和正交矩阵***V***。

如果矩阵***A***是正定矩阵，它的奇异值分解就是$\boldsymbol{A}=\boldsymbol{Q}\boldsymbol{\varLambda}\boldsymbol{Q}^{T}$，一个正交矩阵***Q***就可以满足分解，而不需要两个。而对于可对角化的矩阵有$\boldsymbol{A}=\boldsymbol{S}\boldsymbol{\varLambda}\boldsymbol{S}^{-1}$，但特征向量矩阵***S***并不是正交矩阵，而SVD中的***U***和***V***都是正交矩阵。

- **如何实现**

可以将矩阵***A***视为一种线性变换操作，将其行空间中的一个向量**v**1,变为其列空间中的向量 $\boldsymbol{u}_1=\boldsymbol{A}\boldsymbol{v}_1$ 。奇异值分解就是要在行空间中寻找一组正交基，将其通过矩阵***A***线性变换生成列空间中的一组正交基 $\boldsymbol{A}\boldsymbol{v}_i=\sigma_i\boldsymbol{u}_i$ 。

![](https://pic1.zhimg.com/v2-2661c185a567047804e7831766cd79f0_b.jpg)

找出矩阵***A***行空间中的正交基很容易，Gram-Schmidt正交化过程就可以做到，但是随便的一组正交基经过矩阵矩阵***A***变换得到的向量并不一定正交，因此满足此要求的行空间的正交基非常特殊。而矩阵***A***零空间的向量所对应的是矩阵$\boldsymbol{\varSigma}$对角线上的0元素，因此很容易处理。

- **用矩阵数学语言描述这一过程**

问题的核心就是找到行空间中一组特殊的正交基：

$\begin{array}{*{20}{l}} {\boldsymbol{A}\left[ {\begin{array}{*{20}{c}} {{\boldsymbol{v}_1}}&{{\boldsymbol{v}_2}}& \cdots &{{\boldsymbol{v}_r}} \end{array}} \right]}&{ = \left[ {\begin{array}{*{20}{c}} {{\sigma _1}{\boldsymbol{u}_1}}&{{\sigma _2}{\boldsymbol{u}_2}}& \cdots &{{\sigma _r}{\boldsymbol{u}_r}} \end{array}} \right]}\\ {}&{ = \left[ {\begin{array}{*{20}{c}} {{\boldsymbol{u}_1}}&{{\boldsymbol{u}_2}}& \cdots &{{\boldsymbol{u}_r}} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{\sigma _1}}&{}&{}&{}\\ {}&{{\sigma _2}}&{}&{}\\ {}&{}& \ddots &{}\\ {}&{}&{}&{{\sigma _r}} \end{array}} \right]} \end{array}$ 

如果加入零空间的部分，等式就变为$\boldsymbol{A}\boldsymbol{V}=\boldsymbol{U}\boldsymbol{\varSigma} $。其中零空间对应的正交基 $\boldsymbol{v}_{r+1}…\boldsymbol{v}_{n}$ ，经过线性变换得到***A*v**=0，对应矩阵$\boldsymbol{\varSigma}$中对角线最后的特征值 $\sigma_{r+1}=\sigma_{r+2}=…=0$ 。在等式$\boldsymbol{A}\boldsymbol{V}=\boldsymbol{U}\boldsymbol{\varSigma} $两侧右乘 $\boldsymbol{V}^{-1}$ 得到$\boldsymbol{A}=\boldsymbol{U}\boldsymbol{\varSigma} \boldsymbol{V}^{-1}=\boldsymbol{U}\boldsymbol{\varSigma} \boldsymbol{V}^T$。

现在的问题就是怎么找到符合要求的向量**v**i和**u**i。

为了得到这两个正交矩阵，考虑首先解决其中的一个，在等式$\boldsymbol{A}=\boldsymbol{U}\boldsymbol{\varSigma} \boldsymbol{V}^T$ 两侧分别乘上等式$\boldsymbol{A}^T=\boldsymbol{V}\boldsymbol{\varSigma} ^T\boldsymbol{U}^T$ 两侧的项：

$\begin{array}{*{20}{l}} \boldsymbol{A}^T\boldsymbol{A}&=\boldsymbol{V}{\boldsymbol\varSigma^T}{\boldsymbol{U}^T}\boldsymbol{U}\boldsymbol\varSigma { \boldsymbol{V}^T}\\ {}&{ =  \boldsymbol{V}\boldsymbol\varSigma^T \boldsymbol\varSigma \boldsymbol{V}^T}\\ {}&{ =  \boldsymbol{V}\left[ {\begin{array}{*{20}{c}} {{\sigma _1}^2}&{}&{}&{}\\ {}&{{\sigma _2}^2}&{}&{}\\ {}&{}& \ddots &{}\\ {}&{}&{}&{{\sigma _r}^2} \end{array}} \right]{ \boldsymbol{V}^T}} \end{array}$ 

上式其实是正定矩阵 $\boldsymbol{A}^T\boldsymbol{A}$ 的正交分解，**v**i就是矩阵$\boldsymbol{A}^T\boldsymbol{A}$ 的特征向量， $\sigma_i^2$ 就是矩阵$\boldsymbol{A}^T\boldsymbol{A}$ 的特征值，奇异值 $\sigma_i$ 要取正平方根。用同样的办法也可以求得***U***，它的列向量就是矩阵$\boldsymbol{A}\boldsymbol{A}^T$ 的的特征向量。

**例1：**矩阵***A***= $\left[ {\begin{array}{*{20}{c}} 4&4\\ { - 3}&3 \end{array}} \right]$ ，求其SVD分解。

矩阵为可逆矩阵，秩为2，则需要在行空间中求得**v**1，**v**2，列空间中求得**u**1，**u**2，以及伸缩因子 $\sigma_1,\sigma_2$ 。

计算得 ${\boldsymbol{A}^T}\boldsymbol{A} = \left[ {\begin{array}{*{20}{c}} 4&{ - 3}\\ 4&3 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 4&4\\ { - 3}&3 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {25}&7\\ 7&{25} \end{array}} \right]$ ，它的特征向量为$\left[ {\begin{array}{*{20}{r}} 1\\ 1 \end{array}} \right]$ 和 $\left[ {\begin{array}{*{20}{r}} 1\\ -1 \end{array}} \right]$ 。标准化得到**v**1= $\left[ {\begin{array}{*{20}{r}} {1/\sqrt 2 }\\ {1/\sqrt 2 } \end{array}} \right]$ ，**v**2= $\left[ {\begin{array}{*{20}{r}} {1/\sqrt 2 }\\ {-1/\sqrt 2 } \end{array}} \right]$ ，求得$\sigma_1^2$=32，$\sigma_2^2$=18。

求***U***的过程可以利用矩阵$\boldsymbol{A}\boldsymbol{A}^T$。

$\boldsymbol{A}\boldsymbol{A}^T=\left[ {\begin{array}{*{20}{c}} 4&4\\ { - 3}&3 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 4&{ - 3}\\ 4&3 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {32}&0\\ 0&{18} \end{array}} \right]\$ ，求得$\sigma_1^2$=32，$\sigma_2^2$=18，它的特征向量为 $\left[ {\begin{array}{*{20}{c}} 1\\ 0 \end{array}} \right]$ 和 $\left[ {\begin{array}{*{20}{c}} 0\\ 1 \end{array}} \right]$ 。

但是我们直接将 $\left[ {\begin{array}{*{20}{c}} 1&0\\ 0&1 \end{array}} \right]$ 作为矩阵U代入，会产生错误 $\boldsymbol{U}\boldsymbol{\varSigma}\boldsymbol{V}^T$ = $\left[ {\begin{array}{*{20}{c}} 4&4\\ 3&{ - 3} \end{array}} \right]$ 。

> 这是因为确定特征向量的过程中，特征向量反向仍然符合要求，通过现在的方法无法确认向量的符号，但是一旦我们确认**v**的方向之后，**u**的方向也就随之确定，将**v**代入$\boldsymbol{A}\boldsymbol{V}=\boldsymbol{U}\boldsymbol{\varSigma} $计算**u**可以避免这种问题。**u**和**v**之间的符号联系在进行$\boldsymbol{A}\boldsymbol{A}^T$的计算时被切断了，而用$\boldsymbol{A}\boldsymbol{V}=\boldsymbol{U}\boldsymbol{\varSigma} $可以避免此问题。

**例2：**奇异阵***A***= $\left[ {\begin{array}{*{20}{c}} 4&3\\ 8&6 \end{array}} \right]$ ，求其SVD分解。

矩阵的秩为1，行空间和列空间都是1维的。行空间和零空间可以找到一组正交基转换得到列空间和左零空间的一组正交基。

很容易确定**v**1= $\left[ {\begin{array}{*{20}{r}} {0.8}\\ {0.6} \end{array}} \right]$ ，**v**2= $\left[ {\begin{array}{*{20}{r}} {0.6}\\ { - 0.8} \end{array}} \right]$ ，**u**1= $\frac{1}{{\sqrt 5 }}\left[ {\begin{array}{*{20}{r}} 1\\ 2 \end{array}} \right]$ ，**u**2= $\frac{1}{{\sqrt 5 }}\left[ {\begin{array}{*{20}{r}} 2\\ -1 \end{array}} \right]$ 。

$\boldsymbol{A}^T\boldsymbol{A}$ = $\left[ {\begin{array}{*{20}{c}} 4&8\\ 3&6 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 4&3\\ 8&6 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {80}&{60}\\ {60}&{45} \end{array}} \right]$ ，秩1矩阵，很容易求得$\sigma_1^2$=125，$\sigma_2^2$=0。

矩阵的SVD分解为：***A***= $\frac{1}{{\sqrt 5 }}\left[ {\begin{array}{*{20}{c}} 1&2\\ 2&{ - 1} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {\sqrt {125} }&0\\ 0&0 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {0.8}&{0.6}\\ {0.6}&{ - 0.8} \end{array}} \right]$ 

做奇异值分解就是在矩阵的四个子空间中寻找到合适的基：

$\boldsymbol{v}_1,\boldsymbol{v}_2…,\boldsymbol{v}_r$ 为行空间的标准正交基。

$\boldsymbol{u}_1,\boldsymbol{u}_2…,\boldsymbol{u}_r$ 为列空间的标准正交基。

$\boldsymbol{v}_{r+1},\boldsymbol{v}_{r+2}…,\boldsymbol{v}_n$ 为零空间的标准正交基。

$\boldsymbol{u}_{r+1},\boldsymbol{u}_{r+2}…,\boldsymbol{u}_m$为左零空间的标准正交基。

> 奇异值分解在最小二乘法问题中有重要应用，因为在实际问题中常碰到矩阵***A***不是列满秩的状态，因此$\boldsymbol{A}^T\boldsymbol{A}$ 不可逆，无法用之前的方法求最优解。即使是列满秩的情况当矩阵是超大型矩阵时，$\boldsymbol{A}^T\boldsymbol{A}$ 的计算量太大，用奇异值分解的办法会降低计算量。




![](https://pic2.zhimg.com/v2-4573616cb17eead5dd6df7601ff65fcd_b.jpg)

> 图为G.Strang给出的二阶方阵SVD的几何意义。# 第30讲 线性变换及对应矩阵

Linear transformations and their matrices

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2B60PJ)

- **线性变换 Linear transformations**

本讲介绍线性变换。在传统的线代课程中，线性变换会出现在的比矩阵还要早的位置，实际上可以在脱离坐标和具体数值的情况下讨论线性变换。但是面对科学计算的课题，还是要回到坐标上来。每个线性变换都对应于一个矩阵，矩阵概念的背后就是线性变换的概念。


---


> 无论是“线性变换”还是“矩阵”，对于初学者来说都是陌生而且突兀的概念。矩阵看起来直观，但是其运算规则总让人摸不着头脑；线性变换的概念显得抽象一些，但其实也可以描述得很朴素。G.Strang是从矩阵的概念出发，往求解线性方程组的方向引导大家，他最成功的地方是引入了列图像以及矩阵乘法的行操作、列操作,将矩阵运算变得不那么“没头没脑”。而之前推荐过的《线性代数应该这样学》是从线性变换的角度出发，用朴素的描述在更高的抽象层面讨论，很多原理与法则就变得比较简洁。个人认为两者都优于从行列式出发进入线性代数的路线。在《理解矩阵》中，作者写到矩阵的背后就是线性变换，相似矩阵描述的实际上是同一种线性变换。G.Strang说理解线性变换的本质就是找到它背后的矩阵。这实际上是一个意思，只是出发点和看问题的角度不同。当具体的矩阵和抽象的线性变换在大脑中合二为一的时候，才是对线代最本质的理解。
> 线性变换和矩阵的关系还可以参考以下课程，在2D空间中这个关系更容易描述：

[三少爷的贱男春：线性代数的本质03 矩阵与线性变换](https://zhuanlan.zhihu.com/p/110299551)


---


**例：投影 Projection**

抛开矩阵，从线性变换的概念来讨论“投影”。通过线性变换使得平面内的一个向量变为平面内的另一个向量，这种变换关系通常称之为“映射”（mapping）。

***T***：**R**2→**R**2

***T***(**v**)就像一个函数，给一个"输入"，进行线性变换后得到一个"输出"。比如将二维平面的向量投影到一条直线上。

线性代数只讨论线性变换，而线性变换符合如下规则：对于任意向量**v**，**w**和标量c，

***T***(**v**+**w**)=***T***(**v**)+***T***(**w**)；***T***(c**v**)=c***T***(**v**)

将两者结合就得到：***T***(c**v**+d**w**)=c***T***(**v**)+d***T***(**w**)。

**反例：平面平移 Shift whole plane**

沿着某方向**v**0平移一个平面。这就不是一个线性变换。两条法则都违反。更简单的验证方法是线性运算规则的特例***T***(**0**)=**0**，“平移”不符合这个规则特例。

**反例：求长度*T***(**v**)= $\left\| \boldsymbol{v} \right\|$ 

这个变换，输入一个三维向量，得到一个数值，或者说一维向量***T***：**R**3→**R**1。这个变换可以满足***T***(**0**)=**0**，但是数乘负数就不符合规则。

**例：旋转45度 Rotation by 45**

这个变换***T***：**R**2→**R**2，是一个线性变换，数乘和加法均符合。

![](https://pic3.zhimg.com/v2-d53df625321ccf3dfb9407034d45b5b2_b.jpg)

对二维平面的图像做线性变换的操作示意图。




![](https://pic4.zhimg.com/v2-850677b48cf0b490b4e763abf91dfe6f_b.jpg)




**例：矩阵 *T***(**v**)=***A*v**，矩阵乘法是一个线性变换。***A***(**v**+**w**)=***A***(**v**)+***A***(**w**)；***A***(c**v**)=c***A***(**v**)。整个平面可以通过矩阵的乘法完成变换。

例如，对上图的房子图像施加矩阵***A***= $\left[ {\begin{array}{*{20}{c}} 1&0\\ 0&{ - 1} \end{array}} \right]$ ，则输出的是上下颠倒的房子。

理解线性变换的本质就是确定它背后的矩阵。

**例：**对某一线性变换***T***：**R**3→**R**2，输入一个三维向量而输出是一个二维向量。变成矩阵的形式***T***(**v**)=***A*v**，则矩阵***A***是一个2x3矩阵。

- **描述线性变换 Describing *T***(**v**)

在平面内，如果我们已经了解两个线性无关的向量**v**1和**v**2经过线性变换的结果***T***(**v**1)和***T***(**v**2)，我们实际上可以通过其线性组合，了解平面内所有的向量线性变换的结果。因此如果我们想了解线性变换对整个输入空间的影响，只需要确定它的一组基**v**1，**v**2……**v**n线性变换的结果。

$\boldsymbol{v}=c_1\boldsymbol{v}_1+c_2\boldsymbol{v}_2+…+c_n\boldsymbol{v}_n$ 

$$
\boldsymbol{T}(\boldsymbol{v})=c_1\boldsymbol{T}(\boldsymbol{v}_1)+c_2\boldsymbol{T}(\boldsymbol{v}_2)+…+c_n\boldsymbol{T}(\boldsymbol{v}_n)
$$

线性变换与坐标无关，而矩阵是与坐标有关的。选定一组基，则对于一个向量而言c1，c2等等就是一组坐标值，给定了将向量表示为基向量线性组合的唯一的表达式。因此可以说坐标源自于一组基，c1，c2……cn就是向量的一组坐标值。通常给出空间的坐标是标准坐标，即一组标准基。例如，

**v**= $\left[ {\begin{array}{*{20}{c}} 3\\ 2\\ 4 \end{array}} \right] = 3\left[ {\begin{array}{*{20}{c}} 1\\ 0\\ 0 \end{array}} \right] + 2\left[ {\begin{array}{*{20}{c}} 0\\ 1\\ 0 \end{array}} \right] + 4\left[ {\begin{array}{*{20}{c}} 0\\ 0\\ 1 \end{array}} \right]$ 

如果用矩阵***A***来表示线性变换***T***：**R**n→**R**m。则需要两组基，即输入空间的一组基和输出空间的一组基，来分别确认输入向量与输出向量的坐标。设**v**1，**v**2……**v**n为输入空间的基，而**w**1，**w**2……**w**m为输出空间的基，用矩阵来表示线性变换就是将向量的坐标乘以矩阵得到它在输出空间的坐标。

**例：投影 **

将二维平面内的向量投影到一条直线，选择输入空间的基向量为**v**1，**v**2，其中**v**1是沿着投影方向的向量，**v**2是垂直于投影方向的向量，而输出空间的基选择为**w**1=**v**1，**w**2=**v**2。对于输入空间中任意向量**v**有**v**=c1**v**1+c2**v**2，输出为***T***(**v**)=c1**v**1。

因此这个线性变换的矩阵就是***A***= $\left[ {\begin{array}{*{20}{c}} 1&0\\ 0&0 \end{array}} \right]$ ，输入 $\left[ {\begin{array}{*{20}{c}} {{c_1}}\\ {{c_2}} \end{array}} \right]$ 得到 $\left[ {\begin{array}{*{20}{c}} 1&0\\ 0&0 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{c_1}}\\ {{c_2}} \end{array}} \right]{\rm{ = }}\left[ {\begin{array}{*{20}{c}} {{c_1}}\\ 0 \end{array}} \right]$。这组例子中实际上我们以投影矩阵的特征向量为基，因此得到的矩阵***A***是对角阵。对角线上就是投影矩阵的特征值1和0。

而如果我们以标准坐标为基，即**w**1=**v**1= $\left[ {\begin{array}{*{20}{c}} 1\\ 0 \end{array}} \right]$ ，**w**2=**v**2= $\left[ {\begin{array}{*{20}{c}} 0\\ 1 \end{array}} \right]$ 。对应的投影矩阵就是之前学到的投影矩阵***P***= $\frac{{\boldsymbol{a}{\boldsymbol{a}^T}}}{{{\boldsymbol{a}^T}\boldsymbol{a}}}$ 对于投影到斜率45度的直线，***P***= $\left[ {\begin{array}{*{20}{c}} {\frac{1}{2}}&{\frac{1}{2}}\\ {\frac{1}{2}}&{\frac{1}{2}} \end{array}} \right]$ 。

- **如何确定矩阵*A * Rule to find *A***

矩阵***A***的列实际上是描述输入原空间的基向量得到的列空间线性组合的系数：

$\boldsymbol{T}(\boldsymbol{v}_1)=a_{11}\boldsymbol{w}_1+a_{21}\boldsymbol{w}_2+…+a_{m1}\boldsymbol{w}_m$，

$\boldsymbol{T}(\boldsymbol{v}_2)=a_{12}\boldsymbol{w}_1+a_{22}\boldsymbol{w}_2+…+a_{m2}\boldsymbol{w}_m$ ，

……

这样矩阵***A***就满足“***A***[输入向量的坐标]=[输出空间的坐标]”。

例如 $\boldsymbol{A}\left[ {\begin{array}{*{20}{c}} 1\\ 0\\  \vdots \\ 0 \end{array}} \right]{\rm{ = }}\left[ {\begin{array}{*{20}{c}} {{a_{11}}}\\ {{a_{21}}}\\  \vdots \\ {{a_{m1}}} \end{array}} \right]$ ，所得结果就是输出空间的坐标，也就是输出空间的基进行线性组合所需要的系数。

介绍一个特别的线性变换——求导，***T***= $\frac{d}{{dx}}$ 。

输入： $c_1+c_2x+c_3x^2$ ，基： $1，x，x^2$ 

输出： $c_2+2c_3x$ ，基： $1，x$ 

这是一个***T***：**R**3→**R**2的线性变换。

矩阵***A***满足 $\boldsymbol{A}\left[ {\begin{array}{*{20}{c}} {{c_1}}\\ {{c_2}}\\ {{c_3}} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {{c_2}}\\ {2{c_3}} \end{array}} \right]$ ，可求得矩阵***A***= $\left[ {\begin{array}{*{20}{r}} 0&1&0\\ 0&0&2 \end{array}} \right]$ 。

更普遍的来讲，矩阵的逆矩阵就是线性变换的逆变换，矩阵的乘积就是线性变换的乘积，矩阵乘法源自于线性变换。

# 第31讲 基变换和图像压缩

Change of basis; image compression

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2BA04Q)

本讲介绍基变换。选择合适的基向量会给计算制造便利。基变换的一个重要应用就是压缩，图像、影像、音频和其它一些数据都会因为基变换而得到更高效的压缩储存。本讲的主题仍旧是线性变换和矩阵的关联。

- **图像压缩 Compression of images**

本讲涉及的压缩过程是有损压缩。例如一幅像素是512x512的静态黑白图像，图像用一个向量来表示，向量的分量xi表示像素的灰度，变化范围0<=xi<=255，占8bits。该向量属于**R**n空间，n=(512)x(512)。彩色图像描述每个点的像素需要三个数据，向量长度是黑白图像的3倍。

图像的标准压缩方式为JPEG（联合图像专家组 Joint Photographic Experts Group）。图像压缩的本质就是基变换。

压缩前图像采用的基向量是标准基。但是在图像中离得很近的区域，颜色是非常接近的，比如教学视频中黑板的一个区域，这些区域像素的灰度值很接近，但是用标准基来存储并没有利用上这一特点，这就给了我们压缩的空间。

标准基就是 $\left[ {\begin{array}{*{20}{c}} 1\\ 0\\ 0\\  \vdots \\ 0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0\\ 1\\ 0\\  \vdots \\ 0 \end{array}} \right], \cdots \left[ {\begin{array}{*{20}{c}} 0\\ 0\\ 0\\  \vdots \\ 1 \end{array}} \right]$ ，而显然对于灰度很接近的情况， $\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 1\\  \vdots \\ 1 \end{array}} \right]$ 是一个很好的基（代表低频信号，频率为0，平滑。在图像压缩后经常会存在，因为其系数通常很大），在一组基中有一个这样的向量能解决很大的问题，可以处理像素灰度接近一致的情况。但图像不是灰度完全一致的，因此接下来的问题是跟它相配合的基要选择哪些。极端的情况包括选择 $\left[ {\begin{array}{*{20}{c}} { + 1}\\ { - 1}\\ { + 1}\\ { - 1}\\  \vdots  \end{array}} \right]$ ，它可以给出类似国际象棋盘那种黑白相间的状态（最高频信号，噪音、扰动……在图像压缩后很少存在），还有图像一半图像暗一半图像亮，可以选择 $\left[ {\begin{array}{*{20}{c}}  \vdots \\ { + 1}\\ { - 1}\\  \vdots \\ { - 1} \end{array}} \right]$ 。

- **傅里叶基 Fourier basis**

在JPEG中，将512x512的区域划分为8x8的区块进行处理，所用到的基是傅里叶基向量。

以**R**8中的基举例 $\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 1\\ 1\\ 1\\ 1\\ 1\\ 1 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 1\\ \omega \\ {{\omega ^2}}\\ {{\omega ^3}}\\ {{\omega ^4}}\\ {{\omega ^5}}\\ {{\omega ^6}}\\ {{\omega ^7}} \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 1\\ {{\omega ^2}}\\ {{\omega ^4}}\\ {{\omega ^6}}\\ {{\omega ^8}}\\ {{\omega ^{10}}}\\ {{\omega ^{12}}}\\ {{\omega ^{14}}} \end{array}} \right], \cdots \left[ {\begin{array}{*{20}{c}} 1\\ {{\omega ^7}}\\ {{\omega ^{14}}}\\ {{\omega ^{21}}}\\ {{\omega ^{28}}}\\ {{\omega ^{35}}}\\ {{\omega ^{42}}}\\ {{\omega ^{49}}} \end{array}} \right]$ 

![](https://pic4.zhimg.com/v2-47aac1128e8302217ee9334888d44963_b.jpg)

傅里叶基（Fourier basis）就是之前讲过的傅里叶矩阵的列向量，每个元素为复数的幂。在8x8区块中有64个系数，64个基向量，在这个64维空间中做基变换。

![](https://pic1.zhimg.com/v2-7338ecd7b4f9ebd936109c8fa36a7574_b.jpg)

首先对输入的信号**x**，从标准基变换为傅里叶基，得到系数c，这一步是无损的过程。之后设置阀值进行压缩，超过阀值的认定为肉眼无法分辨的信号。在数学上表现为某些基向量的系数很小，这部分可以丢弃，随之得到新的系数 $\hat c$ 。将新的系数赋值在傅里叶基上求和得到 $\boldsymbol{\hat x} = \sum {{{\hat c}_i}{\boldsymbol{v}_i}} $ 。此时求和项已经不是64项，可能只剩下两三项，这就是压缩。

视频文件可以视为图像的序列，一幅一幅进行图像压缩即可。但这样做没有利用好视频的性质，因为视频是连续的，一幅图像和下一幅图像非常接近，因此可以存储一幅基础图像，随后只存储下一幅图像对它的修正部分。

- **小波 Wavelets**

下面介绍另一组和傅里叶竞争的基向量——小波。

以**R**8中的基举例 $\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 1\\ 1\\ 1\\ 1\\ 1\\ 1 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 1\\ 1\\ { - 1}\\ { - 1}\\ { - 1}\\ { - 1} \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ { - 1}\\ { - 1}\\ 0\\ 0\\ 0\\ 0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0\\ 0\\ 0\\ 0\\ 1\\ 1\\ { - 1}\\ { - 1} \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 1\\ { - 1}\\ 0\\ 0\\ 0\\ 0\\ 0\\ 0 \end{array}} \right], \cdots \left[ {\begin{array}{*{20}{c}} 0\\ 0\\ 0\\ 0\\ 0\\ 0\\ 1\\ { - 1} \end{array}} \right]$ 。

这个只是一个小波选择，还有很多种更多精细的选择，这一组基中有太多从+1跳转到-1的变化。线性代数要做的基变换，就是将标准基下的向量**p**=[p1,p2,p3……p8]表示为小波基的线性组合，求出线性组合的参数**c**满足**p**=c1**w**1+c2**w**2+……+c8**w**8，即**p**=***W*** **c**。***W***即以小波基向量为列向量的小波矩阵。因此有 $\boldsymbol{c}=\boldsymbol{W}^{-1}\boldsymbol{p}$ 。

好的基向量组要求：第一，可以快速求逆矩阵，例如快速傅里叶变换，这里也存在快速小波变换，因为小波矩阵列向量正交，因此可以转置得到逆矩阵；第二，要少量基向量就可以近似信号，可压缩的比例就比较高。

- **基变换 Change of basis**

***W***的列向量是一组新的基向量。在旧基向量体系下的向量**x**和新基向量下的**c**的关系是：**x**=***W*** **c**。

- **变换矩阵**

已知一个线性变换***T***：**R**8→**R**8。当使用空间的一组基**v**1，**v**2……**v**8时，线性变换对应的矩阵为***A***；当使用一组新的基**u**1，**u**2……**u**8时，线性变换对应的矩阵为矩阵***B***。两个矩阵对应的是同一个线性变换，只是使用了不同的基向量。那么***A***和***B***为相似矩阵 $\boldsymbol{B}=\boldsymbol{M}^{-1}\boldsymbol{A}\boldsymbol{M}$ ，***M***是基变换矩阵。

复习一下线性变换的内容：

$\boldsymbol{x}=c_1\boldsymbol{v}_1+c_2\boldsymbol{v}_2+…+c_8\boldsymbol{v}_8$ 

$$
\boldsymbol{T}(\boldsymbol{x})=c_1\boldsymbol{T}(\boldsymbol{v}_1)+c_2\boldsymbol{T}(\boldsymbol{v}_2)+…+c_8\boldsymbol{T}(\boldsymbol{v}_8)
$$

$\boldsymbol{T}(\boldsymbol{v}_1)=a_{11}\boldsymbol{v}_1+a_{21}\boldsymbol{v}_2+…+a_{81}\boldsymbol{v}_8$，

$\boldsymbol{T}(\boldsymbol{v}_2)=a_{12}\boldsymbol{v}_1+a_{22}\boldsymbol{v}_2+…+a_{82}\boldsymbol{v}_8$ ，

……

矩阵***A***就是aij组成的矩阵。

如果我们使用的基向量就是特征向量 $\boldsymbol{T}(\boldsymbol{v}_i)=\lambda_i\boldsymbol{v}_i$ ，矩阵***A***就变成对角阵***Λ***。找出特征向量是压缩最理想的结果，但是找出图像的特征向量代价太大，因此我们找到代价小但是接近理想状态的基向量（例如小波基）进行基变换，完成压缩过程。

> 之前我在线性变换和基变换这两讲后面留了很多具体文字，希望帮助大家理解和区分这些概念，但是有的小伙伴貌似反而被误导，所以我把另一门课程的几何描述放在这里，希望大家看了之后可以完全明白，基变换是在同一个空间中，改变对一个东西的描述方式而已。

[三少爷的贱男春：线性代数的本质09 基变换](https://zhuanlan.zhihu.com/p/110975625)


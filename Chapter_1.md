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

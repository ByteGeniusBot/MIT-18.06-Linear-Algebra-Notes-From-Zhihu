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

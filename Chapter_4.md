# 第04讲 矩阵的LU分解 Factorization into ***A***=***LU***

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

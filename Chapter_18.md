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

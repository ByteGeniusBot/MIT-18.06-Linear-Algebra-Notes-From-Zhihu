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

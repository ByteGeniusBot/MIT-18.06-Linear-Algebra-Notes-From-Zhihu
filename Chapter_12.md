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

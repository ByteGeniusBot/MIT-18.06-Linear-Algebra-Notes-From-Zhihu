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

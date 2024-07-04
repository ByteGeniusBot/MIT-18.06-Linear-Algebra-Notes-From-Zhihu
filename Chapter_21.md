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

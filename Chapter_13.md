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

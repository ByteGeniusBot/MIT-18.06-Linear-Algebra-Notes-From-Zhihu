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

# 第23讲 微分方程和 e^{\boldsymbol{A}t}e^{\boldsymbol{A}t} 

Differential equations and $e^{\boldsymbol{A}t}$

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AVIBM)

$\frac{{d\boldsymbol{u}}}{{dt}} = \boldsymbol{A}\boldsymbol{u}$ 

本讲中我们将面对微分方程，将一阶常系数微分方程转化为线性代数问题进行处理。主要思路基于常系数线性方程的解是指数形式，而寻找其指数和系数就是线代主要研究的问题。这里会涉及到矩阵型指数的运算$e^{\boldsymbol{A}t}$。

- **微分方程 Differential equations **

例： $\begin{array}{l} \frac{{d{u_1}}}{{dt}} =  - {u_1} + 2{u_2}\\ \frac{{d{u_2}}}{{dt}} = {u_1} - 2{u_2} \end{array}$ ,初值条件u1=1，u2=0。

则有$\frac{{d\boldsymbol{u}}}{{dt}} = \boldsymbol{A}\boldsymbol{u}$， $\boldsymbol{A}=\left[ {\begin{array}{*{20}{c}} {{\rm{ - }}1}&2\\ 1&{{\rm{ - }}2} \end{array}} \right]$ ， $\boldsymbol{u}(0)=\left[ {\begin{array}{*{20}{c}} 1\\ 0 \end{array}} \right]$ 。

分析矩阵***A***的目的是要追踪**u**随时间的变化，而首先要做的是找到矩阵的特征值和特征向量。矩阵***A***为奇异矩阵，因此存在一个特征值 $\lambda_1=0$ ，而矩阵的迹为-3，因此还有一个特征值为$\lambda_2=-3$。

一阶线性微分方程的解的形式是 $e^{\lambda t}$ 。两个特征值中，0会使结果达到稳态，而-3所对应的$e^{-3t}$ 会随时间增大而变小。

方程的通解为 $\boldsymbol{u}({\rm{t}}) = {{c}_1}{{e}^{{\lambda _1}t}}{\boldsymbol{x}_1} + {{c}_2}{{e}^{{\lambda _2}t}}{\boldsymbol{x}_2}$ 。

> 尽管直接代入可以验证 ${{e}^{{\lambda _1}t}}{\boldsymbol{x}_1} $ 是方程的解，但类似我这种比较笨的，对微分方程的解$e^{\lambda t}$ 是如何跟矩阵的特征值联系起来的根本理解不了，只好用差商方程帮助理解。方程所求的是t时刻**u**的状态**u**(t)，设需要N步从**u**(0)达到**u**(t)，且每一步都满足$\frac{{d\boldsymbol{u}}}{{dt}} = \boldsymbol{A}\boldsymbol{u}$，即 $\frac{{{\boldsymbol{u}_{step(n{\rm{ + }}1)}} - {\boldsymbol{u}_{step(n)}}}}{{\Delta t}} = \frac{{{\boldsymbol{u}_{step(n{\rm{ + }}1)}} - {\boldsymbol{u}_{step(n)}}}}{{t/N}} = \boldsymbol{A}{\boldsymbol{u}_{step(n)}}$ ，从**u**(0)=**u**step(0)开始进行计算： $\frac{{{\boldsymbol{u}_{step(1)}} - {\boldsymbol{u}_{step(0)}}}}{{t/N}} = \boldsymbol{A}{\boldsymbol{u}_{step(0)}}$ ，则有 ${\boldsymbol{u}_{step(1)}} = (\frac{t}{N}\boldsymbol{A} + 1){\boldsymbol{u}_{step(0)}}{\rm{ = }}(\frac{t}{N}\boldsymbol{A}  + 1)\boldsymbol{u}(0)$ 
> ,将**u**(0)表示成为矩阵特征向量的线性组合，则有 $\boldsymbol{u}(0)=c_1\boldsymbol{x}_1+c_2\boldsymbol{x}_2$ ， $\boldsymbol{A}\boldsymbol{u}(0)=c_1\lambda_1\boldsymbol{x}_1+c_2\lambda_2\boldsymbol{x}_2$ ，代入前式得到 ${\boldsymbol{u}_{step(1)}} = {{c}_1}(\frac{t}{N}{\lambda _1} + 1){\boldsymbol{x}_1} + {{c}_2}(\frac{t}{N}{\lambda _2} + 1){\boldsymbol{x}_2}$ ,
> ${\boldsymbol{u}_{step(2)}} = (\frac{t}{N}\boldsymbol{A} + 1){\boldsymbol{u}_{step(1)}} = {{c}_1}{(\frac{t}{N}{\lambda _1} + 1)^2}{\boldsymbol{x}_1} + {{c}_2}{(\frac{t}{N}{\lambda _2} + 1)^2}{\boldsymbol{x}_2}$ ，重复代入过程最后得到： $\boldsymbol{u}(t)={\boldsymbol{u}_{step(N)}}  = {{c}_1}{(\frac{t}{N}{\lambda _1} + 1)^N}{\boldsymbol{x}_1} + {{c}_2}{(\frac{t}{N}{\lambda _2} + 1)^N}{\boldsymbol{x}_2}$，因为 $\mathop {\lim }\limits_{k \to \infty } {(\frac{1}{{{k_{}}}} + 1)^k} \to e$ ，所以可求得$\boldsymbol{u}({\rm{t}}) = {{c}_1}{{e}^{{\lambda _1}t}}{\boldsymbol{x}_1} + {{c}_2}{{e}^{{\lambda _2}t}}{\boldsymbol{x}_2}$ 。

将$\lambda_1=0$ ，$\lambda_2=-3$代入$(\boldsymbol{A}-\lambda \boldsymbol{I})\boldsymbol{x}=\boldsymbol{0}$ ，分别求得对应的特征向量**x**1= $\left[ {\begin{array}{*{20}{c}} 2\\ 1 \end{array}} \right]$ ，**x**2=$\left[ {\begin{array}{*{20}{c}} 1\\ -1 \end{array}} \right]$ ，$\boldsymbol{u}({\rm{t}}) = {{c}_1}{{e}^{{\lambda _1}t}}{\boldsymbol{x}_1} + {{c}_2}{{e}^{{\lambda _2}t}}{\boldsymbol{x}_2}={{c}_1}{{e}^0}\left[ {\begin{array}{*{20}{c}} 2\\ 1 \end{array}} \right] + {{c}_2}{{e}^{ - 3t}}\left[ {\begin{array}{*{20}{c}} 1\\ { - 1} \end{array}} \right]$ 。

由初始条件得 $\boldsymbol{u}(0) = {c_1}\left[ {\begin{array}{*{20}{c}} 2\\ 1 \end{array}} \right] + {c_2}\left[ {\begin{array}{*{20}{c}} 1\\ { - 1} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} 1\\ 0 \end{array}} \right]$ ,可解得c1=c2=1/3。

因此 $\boldsymbol{u}({\rm{t}}) = \frac{1}{3}\left[ {\begin{array}{*{20}{c}} 2\\ 1 \end{array}} \right] + \frac{1}{3}{e^{ - 3t}}\left[ {\begin{array}{*{20}{c}} 1\\ { - 1} \end{array}} \right]$ ，前一项为稳态状态，后一项随着时间衰减。


---


稳定性：并不是所有的系统都会达到稳态，矩阵的特征值会告诉我们**u**(t)的发展趋势。

1. Re( $\lambda$ )<0，则有**u**(t)→0。（支配稳定性的是实部，虚部的作用是在单位圆上转圈。）
2. 稳态：有一个特征值为0，并且其它所有的特征值实部为负数。
3. 至少有一个特征值满足Re( $\lambda$ )>0，则发散。

如果二阶矩阵***A***= $\left[ {\begin{array}{*{20}{c}} a&b\\ c&d \end{array}} \right]$ 的两个特征值实部为负数，则矩阵的迹a+d也是负数。反之并不一定成立，例如矩阵$\left[ {\begin{array}{*{20}{c}} -2&0\\ 0&1 \end{array}} \right]$ 的迹为-1，但是一个特征值为1。如果二阶矩阵的行列式为正而迹为负，则解为收敛的。


---


在方程$\frac{{d\boldsymbol{u}}}{{dt}} = \boldsymbol{A}\boldsymbol{u}$中，是矩阵***A***使得不同分量之间相互耦合。令**u**=***S*v**，其中***S***是由矩阵***A***的特征向量组成。则有：

$\boldsymbol{S}\frac{{d\boldsymbol{v}}}{{dt}} = \boldsymbol{AS}\boldsymbol{v}$ $ \Rightarrow \frac{{d\boldsymbol{v}}}{{dt}} = {\boldsymbol{S}^{ - 1}}\boldsymbol{AS}\boldsymbol{v} = \boldsymbol{\varLambda} \boldsymbol{v}$

新的方程不再耦合，则方程组的对角线为： $\frac{{d{v_i}}}{{dt}} = {\lambda _i}{v_i}$ ，方程组的通解为：

$\boldsymbol{v}(t) = {e^{\boldsymbol{\varLambda}  t}}\boldsymbol{v}(0)$ ， $\boldsymbol{u}(t) =\boldsymbol{S}{e^{\boldsymbol\varLambda  t}}{\boldsymbol{S}^{ - 1}}\boldsymbol{u}(0) = {e^{\boldsymbol{A}t}}\boldsymbol{u}(0)$ 

- **矩阵指数函数 Matrix exponential ** $e^{\boldsymbol{A}t}$ 

我们可以用幂级数的公式：

${e^x} = \sum\limits_{n = 0}^\infty  {\frac{{{x^n}}}{{n!}}}  = 1 + x + \frac{{{x^2}}}{2} + \frac{{{x^3}}}{6} +  \cdots $ 

来定义矩阵型指数运算$e^{\boldsymbol{A}t}$：

${e^{\boldsymbol{A} t}} = I + \boldsymbol{A}t + \frac{{{{(\boldsymbol{A}t)}^2}}}{2} + \frac{{{{(\boldsymbol{A}t)}^3}}}{6} +  \cdots $ 

如果***A***t的特征值很小，满足收敛条件 $\left| {\lambda (\boldsymbol{A}t)} \right|$ <1，则可以用几何级数来定义矩阵型指数：

$\frac{1}{{1 - x}} = \sum\limits_{n = 0}^\infty  {{x^n}}  \to {(I - \boldsymbol{A}t)^{ - 1}} = I + \boldsymbol{A}t + {(\boldsymbol{A}t)^2} + {\left( {\boldsymbol{A}t} \right)^3} +  \cdots $ 

前文中我们已经写出了矩阵指数函数的公式 ${e^{\boldsymbol{A} t}} = \boldsymbol{S}{e^{\boldsymbol\varLambda  t}}{\boldsymbol{S}^{ - 1}}$ 。如果矩阵***A***具有n个线性无关的特征向量，我们可以从幂级数定义的矩阵指数公式来再次验证：

$\begin{array}{*{20}{l}} {{e^{\boldsymbol{A} t}}}&{ = I + \boldsymbol{A}t + \frac{{{{(\boldsymbol{A}t)}^2}}}{2} + \frac{{{{(\boldsymbol{A}t)}^3}}}{6} +  \cdots }\\ {}&{ = \boldsymbol{S}{ \boldsymbol{S}^{ - 1}} +  \boldsymbol{S}\boldsymbol\varLambda { \boldsymbol{S}^{ - 1}}t + \frac{{ \boldsymbol{S}{\boldsymbol\varLambda ^2}{ \boldsymbol{S}^{ - 1}}}}{2}{t^2} + \frac{{ \boldsymbol{S}{\boldsymbol\varLambda ^3}{ \boldsymbol{S}^{ - 1}}}}{6}{t^3} +  \cdots }\\ {}&{ =  \boldsymbol{S}(I + \boldsymbol\varLambda t + \frac{{{\boldsymbol\varLambda ^2}}}{2}{t^2} + \frac{{{\boldsymbol\varLambda ^3}}}{6}{t^3} +  \cdots ){ \boldsymbol{S}^{ - 1}}}\\ {}&{ =  \boldsymbol{S}{e^{\boldsymbol\varLambda  t}}{ \boldsymbol{S}^{ - 1}}} \end{array}$ 

能够对角化的矩阵都可以表示为上式。

${e^{\boldsymbol\varLambda  t}} = \left[ {\begin{array}{*{20}{c}} {{e^{{\lambda _1}}}^t}&0& \cdots &0\\ 0&{{e^{{\lambda _2}}}^t}&{}&0\\  \vdots &{}& \ddots & \vdots \\ 0& \cdots &0&{{e^{{\lambda _n}}}^t} \end{array}} \right]$ 

- **二阶微分方程 Second order differential equations**

我们可以将二阶微分方程 $y'' + by' + ky = 0$ 转化为2x2的一阶问题进行处理，构造方法类似于我们对斐波那契数列的处理方法。

令**u**= $\left[ {\begin{array}{*{20}{c}} {y'}\\ y \end{array}} \right]$ ，则有**u'**= $\left[ {\begin{array}{*{20}{c}} {y''}\\ {y'} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} { - b}&{ - k}\\ 1&0 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {y'}\\ y \end{array}} \right]$ 

如果是k阶微分方程，那么需要一个kxk矩阵，除了第一行和对角线下面一排斜线上的元素之外，这个系数矩阵其它元素均为0。

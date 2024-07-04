# 第24讲 马尔可夫矩阵；傅里叶级数

Markov matrices; Fourier series

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AVOAV)

本讲学习马尔可夫矩阵和傅里叶级数，两者是关于特征值和投影矩阵的应用。

- **马尔可夫矩阵 Markov matrices**

***A***= $\left[ {\begin{array}{*{20}{c}} {0.1}&{0.01}&{0.3}\\ {0.2}&{0.99}&{0.3}\\ {0.7}&0&{0.4} \end{array}} \right]$ 

形如矩阵***A***，任何元素非负，且每列的元素加和为1的矩阵被称为马尔可夫矩阵。马尔可夫矩阵主要应用在概率领域。将一个马尔可夫矩阵进行方幂运算得到的矩阵仍旧是马尔可夫矩阵。

当处理一个微分方程问题时，特征值0意味着得到一个稳态。当进行矩阵的方幂运算时，特征值给出稳态的条件包括：

1. $\lambda_1$ =1是特征值之一。
2. 其它特征值的绝对值都比1小，$\left| {{\lambda _i}} \right|$ <1。

如我们所知，如果矩阵具有n个线性无关的特征向量，则有：

$\boldsymbol{u}_k=\boldsymbol{A}^k\boldsymbol{u}_0 = {{c}_1}{{{\lambda _1}^k}}{\boldsymbol{x}_1} + {{c}_2}{{{\lambda _2}^k}}{\boldsymbol{x}_2}+…+{{c}_n}{{{\lambda _n}^k}}{\boldsymbol{x}_n}$ 。

如果$\lambda_1$ =1并且其他的特征值都小于1，则系统在k增大过程中趋近于**u**0的分量 $c_1\boldsymbol{x}_1$ ，即给出了一个稳态状况。这里特征向量**x**1的每一分量都是正的，因此若初始值为正，则最终的稳态也是正的。

Markov矩阵每一列的元素加和为1这个条件，保证了矩阵具有1这个特征值。

***A***-***I***= $\left[ {\begin{array}{*{20}{r}} { - .9}&{.01}&{.3}\\ {.2}&{ - .01}&{.3}\\ {.7}&0&{ - .6} \end{array}} \right]$ 

从每一列减去1，则每列的加和都从1变为0。这时候行向量相加的结构就是**0**向量，因此行向量线性相关，矩阵为奇异矩阵。矩阵***A***有特征向量在***A***-***I***的零空间中，其对应的特征值为1。回代计算可得**x**1= $\left[ {\begin{array}{*{20}{c}} {0.6}\\ {33}\\ {0.7} \end{array}} \right]$ 。


---


**转置矩阵的特征值：**转置矩阵 $\boldsymbol{A}^T$ 具有和原矩阵***A***相同的特征值。

$(\boldsymbol{A}-\lambda\boldsymbol{I})^T=\boldsymbol{A}^T-\lambda\boldsymbol{I}$ 

则由行列式的性质10可知 $\det(\boldsymbol{A}-\lambda \boldsymbol{I})=\det(\boldsymbol{A}^T-\lambda \boldsymbol{I})$ 。如果 $\lambda$ 是矩阵***A***的特征值，则其满足$\det(\boldsymbol{A}^T-\lambda \boldsymbol{I})=0$ 。0，因此它也是转置矩阵 $ \boldsymbol{A}^T$ 的特征值。

但是两者特征向量有所区别，零空间不等同于左零空间。


---


我们用马尔可夫矩阵来研究人口流动问题。

${\left[ {\begin{array}{*{20}{c}} {{u_{Cal}}}\\ {{u_{Mass}}} \end{array}} \right]_{t = k + 1}} = \left[ {\begin{array}{*{20}{c}} {.9}&{.2}\\ {.1}&{.8} \end{array}} \right]{\left[ {\begin{array}{*{20}{c}} {{u_{Cal}}}\\ {{u_{Mass}}} \end{array}} \right]_{t = k}}$ 

方程中**u**的分量分别代表加利福尼亚州和马萨诸塞州的人口，矩阵中的每一列中元素代表着人口去留比例，比如第一列0.9表示留在加州的人口占加州人口的90%，而10%进入麻省，第二列中由麻省进入加州的人口占麻省的20%，而80%选择留在麻省。如果取初值 ${\left[ {\begin{array}{*{20}{c}} {{u_{Cal}}}\\ {{u_{Mass}}} \end{array}} \right]_0} = \left[ {\begin{array}{*{20}{c}} 0\\ {1000} \end{array}} \right]$ ，则经过一次迁徙 ${\left[ {\begin{array}{*{20}{c}} {{u_{Cal}}}\\ {{u_{Mass}}} \end{array}} \right]_1} = \left[ {\begin{array}{*{20}{c}} {.9}&{.2}\\ {.1}&{.8} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 0\\ {1000} \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {200}\\ {800} \end{array}} \right]$ 。

为了获取长时间后的人口分布，我们需要了解矩阵的特征值和特征向量。因为这是马尔可夫矩阵，所以有一个特征值1，则另一个特征值为0.9+0.8-1=0.7。可以求得**x**1= $\left[ {\begin{array}{*{20}{c}} 2\\ 1 \end{array}} \right]$ ，**x**2= $\left[ {\begin{array}{*{20}{c}} 1\\ { - 1} \end{array}} \right]$ 。从$\left[ {\begin{array}{*{20}{c}} 2\\ 1 \end{array}} \right]$可知最后的稳态为加州人口2/3，麻省人口1/3。

通解为： $\boldsymbol{u}_k={c_1}\left[ {\begin{array}{*{20}{c}} 2\\ 1 \end{array}} \right] + {c_2}{(0.7)^k}\left[ {\begin{array}{*{20}{c}} { - 1}\\ 1 \end{array}} \right]$ ，可以从**u**0解得c1=1000/3,c2=2000/3。

- **傅里叶级数和投影矩阵 Fourier series & Projections**

如果有一组标准正交基**q**1，**q**2……**q**n为则任意向量**v**可以写成：

$\boldsymbol{v}=x_1\boldsymbol{q}_1+x_2\boldsymbol{q}_2+…+x_n\boldsymbol{q}_n$ ,

因为当i，j不相等时有 $\boldsymbol{q}_i^T\boldsymbol{q}_j=0$ 。因此有$\boldsymbol{q}_i^T\boldsymbol{v}=x_1\boldsymbol{q}_i^T\boldsymbol{q}_1+x_2\boldsymbol{q}_i^T\boldsymbol{q}_2+…+x_n\boldsymbol{q}_i^T\boldsymbol{q}_n=x_i$ 。

我们得到了分量xi的公式： $x_i=\boldsymbol{q}_i^T\boldsymbol{v}$ 。

因为 $\boldsymbol{v}=\left[ {\begin{array}{*{20}{c}} {{\boldsymbol{q}_1}}& \cdots &{{\boldsymbol{q}_n}} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{x_1}}\\  \vdots \\ {{x_n}} \end{array}} \right]$，即**v**=***Q*x**，所以 $\boldsymbol{x}=\boldsymbol{Q}^{-1}\boldsymbol{v}$ 。因为***Q***为正交矩阵，所以有 $\boldsymbol{Q}^{-1}=\boldsymbol{Q}^T$ ,可得 $\boldsymbol{x}=\boldsymbol{Q}^{T}\boldsymbol{v}$ 。这与我们之前得到的$x_i=\boldsymbol{q}_i^T\boldsymbol{v}$ 完全相同。这里给出了求分量的思路就是用空间的一组标准正交基去点乘目标向量，利用其标准正交的性质得到所求。

标准正交是此处的核心概念。而傅里叶级数也是在这个概念上构建的。我们可以对任意函数做傅里叶展开，得到表达式： $f(x) = {a_0} + {a_1}\cos x + {b_1}\sin x + {a_2}\cos 2x + {b_2}\sin 2x +  \cdots $ 

与之前的有限个标准正交向量组成的正交矩阵不同，这个空间是无限维，它的一组基是1，cosx，sinx，cos2x，sin2x……

此处的正交概念与**R**n空间不同，点积的概念也不同。

向量$\boldsymbol{v}^T\boldsymbol{w}=v_1w_1+v_2w_2+…+v_nw_n$ ,

函数 ${f^T}g = \int_0^{2\pi } {f(x)g(x)dx} $ 

计算基sinx和cosx的点积可以验证其正交性。

$\int_0^{2\pi } {\sin x\cos xdx}  = \frac{1}{2}{(\sin 2x)^2}\left| {_0^{2\pi }} \right. = 0$ 

采用和标准正交基相同的策略可以得到傅里叶变换的参数。

$\begin{array}{*{20}{l}} {\int_0^{2\pi } {f(x)\cos xdx} }&{ = \int_0^{2\pi } {({a_0} + {a_1}\cos x + {b_1}\sin x + {a_2}\cos 2x +  \cdots )\cos xdx} }\\ {}&{ = 0 + \int_0^{2\pi } {{a_1}{{\cos }^2}xdx}  + 0 + 0 \cdots }\\ {}&{ = {a_1}\pi } \end{array}$ 

可以得到 ${a_1} = \frac{1}{\pi }\int_0^{2\pi } {f(x)\cos xdx} $ ，同理可以求得其它参数。


---


> 之前我们已经提到了G. Strang 所讲的线代和其他人的差别，学习越深入则越能体会到这一点。网上有一篇《理解矩阵》的博客介绍了很多大家对线代的认识误区，在开篇处作者就点出了初学者面对线代为什么觉得困难，因为我们目前学习的线代是通过公理化来表述的第二代数学模型，而此前大家都是在以实用为导向的第一代数学模型中，困难来自于全面提升的抽象性。G. Strang 做的事情大体上可以理解为在第一代数学模型中讨论线性计算的核心内容，因此在学习中可以保留直觉性，非常大程度地降低了抽象性带来的困难。这种讲授思路的优劣，只有在有明确的目标情况下才好判定。换句话说，看你学线代的目的是什么，如果是数值计算或者是在一些实验科学中使用矩阵工具，那么G. Strang 讲授的内容非常恰如其分。至于更具抽象性的部分，我推荐《线性代数应该这样学》这本书，以线性算子作为核心，可以从另一种框架下领略线代的魅力，并且深入地理解线性代数的内涵。

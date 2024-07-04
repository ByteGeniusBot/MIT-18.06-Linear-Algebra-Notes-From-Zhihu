# 第29讲 奇异值分解

Singular value decomposition

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2B5R1G)

本讲介绍奇异值分解（Singular value decomposition），简称SVD。这是矩阵最终也是最好的分解，任意矩阵可分解为 $\boldsymbol{A}=\boldsymbol{U}\boldsymbol{\varSigma} \boldsymbol{V}^T$ ，分解结果为正交矩阵***U***，对角阵$\boldsymbol{\varSigma}$和正交矩阵***V***。

如果矩阵***A***是正定矩阵，它的奇异值分解就是$\boldsymbol{A}=\boldsymbol{Q}\boldsymbol{\varLambda}\boldsymbol{Q}^{T}$，一个正交矩阵***Q***就可以满足分解，而不需要两个。而对于可对角化的矩阵有$\boldsymbol{A}=\boldsymbol{S}\boldsymbol{\varLambda}\boldsymbol{S}^{-1}$，但特征向量矩阵***S***并不是正交矩阵，而SVD中的***U***和***V***都是正交矩阵。

- **如何实现**

可以将矩阵***A***视为一种线性变换操作，将其行空间中的一个向量**v**1,变为其列空间中的向量 $\boldsymbol{u}_1=\boldsymbol{A}\boldsymbol{v}_1$ 。奇异值分解就是要在行空间中寻找一组正交基，将其通过矩阵***A***线性变换生成列空间中的一组正交基 $\boldsymbol{A}\boldsymbol{v}_i=\sigma_i\boldsymbol{u}_i$ 。

![](https://pic1.zhimg.com/v2-2661c185a567047804e7831766cd79f0_b.jpg)

找出矩阵***A***行空间中的正交基很容易，Gram-Schmidt正交化过程就可以做到，但是随便的一组正交基经过矩阵矩阵***A***变换得到的向量并不一定正交，因此满足此要求的行空间的正交基非常特殊。而矩阵***A***零空间的向量所对应的是矩阵$\boldsymbol{\varSigma}$对角线上的0元素，因此很容易处理。

- **用矩阵数学语言描述这一过程**

问题的核心就是找到行空间中一组特殊的正交基：

$\begin{array}{*{20}{l}} {\boldsymbol{A}\left[ {\begin{array}{*{20}{c}} {{\boldsymbol{v}_1}}&{{\boldsymbol{v}_2}}& \cdots &{{\boldsymbol{v}_r}} \end{array}} \right]}&{ = \left[ {\begin{array}{*{20}{c}} {{\sigma _1}{\boldsymbol{u}_1}}&{{\sigma _2}{\boldsymbol{u}_2}}& \cdots &{{\sigma _r}{\boldsymbol{u}_r}} \end{array}} \right]}\\ {}&{ = \left[ {\begin{array}{*{20}{c}} {{\boldsymbol{u}_1}}&{{\boldsymbol{u}_2}}& \cdots &{{\boldsymbol{u}_r}} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{\sigma _1}}&{}&{}&{}\\ {}&{{\sigma _2}}&{}&{}\\ {}&{}& \ddots &{}\\ {}&{}&{}&{{\sigma _r}} \end{array}} \right]} \end{array}$ 

如果加入零空间的部分，等式就变为$\boldsymbol{A}\boldsymbol{V}=\boldsymbol{U}\boldsymbol{\varSigma} $。其中零空间对应的正交基 $\boldsymbol{v}_{r+1}…\boldsymbol{v}_{n}$ ，经过线性变换得到***A*v**=0，对应矩阵$\boldsymbol{\varSigma}$中对角线最后的特征值 $\sigma_{r+1}=\sigma_{r+2}=…=0$ 。在等式$\boldsymbol{A}\boldsymbol{V}=\boldsymbol{U}\boldsymbol{\varSigma} $两侧右乘 $\boldsymbol{V}^{-1}$ 得到$\boldsymbol{A}=\boldsymbol{U}\boldsymbol{\varSigma} \boldsymbol{V}^{-1}=\boldsymbol{U}\boldsymbol{\varSigma} \boldsymbol{V}^T$。

现在的问题就是怎么找到符合要求的向量**v**i和**u**i。

为了得到这两个正交矩阵，考虑首先解决其中的一个，在等式$\boldsymbol{A}=\boldsymbol{U}\boldsymbol{\varSigma} \boldsymbol{V}^T$ 两侧分别乘上等式$\boldsymbol{A}^T=\boldsymbol{V}\boldsymbol{\varSigma} ^T\boldsymbol{U}^T$ 两侧的项：

$\begin{array}{*{20}{l}} \boldsymbol{A}^T\boldsymbol{A}&=\boldsymbol{V}{\boldsymbol\varSigma^T}{\boldsymbol{U}^T}\boldsymbol{U}\boldsymbol\varSigma { \boldsymbol{V}^T}\\ {}&{ =  \boldsymbol{V}\boldsymbol\varSigma^T \boldsymbol\varSigma \boldsymbol{V}^T}\\ {}&{ =  \boldsymbol{V}\left[ {\begin{array}{*{20}{c}} {{\sigma _1}^2}&{}&{}&{}\\ {}&{{\sigma _2}^2}&{}&{}\\ {}&{}& \ddots &{}\\ {}&{}&{}&{{\sigma _r}^2} \end{array}} \right]{ \boldsymbol{V}^T}} \end{array}$ 

上式其实是正定矩阵 $\boldsymbol{A}^T\boldsymbol{A}$ 的正交分解，**v**i就是矩阵$\boldsymbol{A}^T\boldsymbol{A}$ 的特征向量， $\sigma_i^2$ 就是矩阵$\boldsymbol{A}^T\boldsymbol{A}$ 的特征值，奇异值 $\sigma_i$ 要取正平方根。用同样的办法也可以求得***U***，它的列向量就是矩阵$\boldsymbol{A}\boldsymbol{A}^T$ 的的特征向量。

**例1：**矩阵***A***= $\left[ {\begin{array}{*{20}{c}} 4&4\\ { - 3}&3 \end{array}} \right]$ ，求其SVD分解。

矩阵为可逆矩阵，秩为2，则需要在行空间中求得**v**1，**v**2，列空间中求得**u**1，**u**2，以及伸缩因子 $\sigma_1,\sigma_2$ 。

计算得 ${\boldsymbol{A}^T}\boldsymbol{A} = \left[ {\begin{array}{*{20}{c}} 4&{ - 3}\\ 4&3 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 4&4\\ { - 3}&3 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {25}&7\\ 7&{25} \end{array}} \right]$ ，它的特征向量为$\left[ {\begin{array}{*{20}{r}} 1\\ 1 \end{array}} \right]$ 和 $\left[ {\begin{array}{*{20}{r}} 1\\ -1 \end{array}} \right]$ 。标准化得到**v**1= $\left[ {\begin{array}{*{20}{r}} {1/\sqrt 2 }\\ {1/\sqrt 2 } \end{array}} \right]$ ，**v**2= $\left[ {\begin{array}{*{20}{r}} {1/\sqrt 2 }\\ {-1/\sqrt 2 } \end{array}} \right]$ ，求得$\sigma_1^2$=32，$\sigma_2^2$=18。

求***U***的过程可以利用矩阵$\boldsymbol{A}\boldsymbol{A}^T$。

$\boldsymbol{A}\boldsymbol{A}^T=\left[ {\begin{array}{*{20}{c}} 4&4\\ { - 3}&3 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 4&{ - 3}\\ 4&3 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {32}&0\\ 0&{18} \end{array}} \right]\$ ，求得$\sigma_1^2$=32，$\sigma_2^2$=18，它的特征向量为 $\left[ {\begin{array}{*{20}{c}} 1\\ 0 \end{array}} \right]$ 和 $\left[ {\begin{array}{*{20}{c}} 0\\ 1 \end{array}} \right]$ 。

但是我们直接将 $\left[ {\begin{array}{*{20}{c}} 1&0\\ 0&1 \end{array}} \right]$ 作为矩阵U代入，会产生错误 $\boldsymbol{U}\boldsymbol{\varSigma}\boldsymbol{V}^T$ = $\left[ {\begin{array}{*{20}{c}} 4&4\\ 3&{ - 3} \end{array}} \right]$ 。

> 这是因为确定特征向量的过程中，特征向量反向仍然符合要求，通过现在的方法无法确认向量的符号，但是一旦我们确认**v**的方向之后，**u**的方向也就随之确定，将**v**代入$\boldsymbol{A}\boldsymbol{V}=\boldsymbol{U}\boldsymbol{\varSigma} $计算**u**可以避免这种问题。**u**和**v**之间的符号联系在进行$\boldsymbol{A}\boldsymbol{A}^T$的计算时被切断了，而用$\boldsymbol{A}\boldsymbol{V}=\boldsymbol{U}\boldsymbol{\varSigma} $可以避免此问题。

**例2：**奇异阵***A***= $\left[ {\begin{array}{*{20}{c}} 4&3\\ 8&6 \end{array}} \right]$ ，求其SVD分解。

矩阵的秩为1，行空间和列空间都是1维的。行空间和零空间可以找到一组正交基转换得到列空间和左零空间的一组正交基。

很容易确定**v**1= $\left[ {\begin{array}{*{20}{r}} {0.8}\\ {0.6} \end{array}} \right]$ ，**v**2= $\left[ {\begin{array}{*{20}{r}} {0.6}\\ { - 0.8} \end{array}} \right]$ ，**u**1= $\frac{1}{{\sqrt 5 }}\left[ {\begin{array}{*{20}{r}} 1\\ 2 \end{array}} \right]$ ，**u**2= $\frac{1}{{\sqrt 5 }}\left[ {\begin{array}{*{20}{r}} 2\\ -1 \end{array}} \right]$ 。

$\boldsymbol{A}^T\boldsymbol{A}$ = $\left[ {\begin{array}{*{20}{c}} 4&8\\ 3&6 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 4&3\\ 8&6 \end{array}} \right] = \left[ {\begin{array}{*{20}{c}} {80}&{60}\\ {60}&{45} \end{array}} \right]$ ，秩1矩阵，很容易求得$\sigma_1^2$=125，$\sigma_2^2$=0。

矩阵的SVD分解为：***A***= $\frac{1}{{\sqrt 5 }}\left[ {\begin{array}{*{20}{c}} 1&2\\ 2&{ - 1} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {\sqrt {125} }&0\\ 0&0 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {0.8}&{0.6}\\ {0.6}&{ - 0.8} \end{array}} \right]$ 

做奇异值分解就是在矩阵的四个子空间中寻找到合适的基：

$\boldsymbol{v}_1,\boldsymbol{v}_2…,\boldsymbol{v}_r$ 为行空间的标准正交基。

$\boldsymbol{u}_1,\boldsymbol{u}_2…,\boldsymbol{u}_r$ 为列空间的标准正交基。

$\boldsymbol{v}_{r+1},\boldsymbol{v}_{r+2}…,\boldsymbol{v}_n$ 为零空间的标准正交基。

$\boldsymbol{u}_{r+1},\boldsymbol{u}_{r+2}…,\boldsymbol{u}_m$为左零空间的标准正交基。

> 奇异值分解在最小二乘法问题中有重要应用，因为在实际问题中常碰到矩阵***A***不是列满秩的状态，因此$\boldsymbol{A}^T\boldsymbol{A}$ 不可逆，无法用之前的方法求最优解。即使是列满秩的情况当矩阵是超大型矩阵时，$\boldsymbol{A}^T\boldsymbol{A}$ 的计算量太大，用奇异值分解的办法会降低计算量。




![](https://pic2.zhimg.com/v2-4573616cb17eead5dd6df7601ff65fcd_b.jpg)

> 图为G.Strang给出的二阶方阵SVD的几何意义。

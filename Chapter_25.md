# 第25讲 对称矩阵和正定性

Symmetric matrices and positive definiteness

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2AVUL4)

进入第三单元学习，主题是正定矩阵及其应用。对称矩阵是最重要的矩阵之一，特征值为实数并且拥有一套正交特征向量。正定矩阵的性质则更好。

- **对称矩阵 Symmetric matrices**

对称矩阵 $\boldsymbol{A}=\boldsymbol{A}^T$ 。包含特殊性质的矩阵，例如Markov矩阵，其特征值和特征向量往往拥有一定特性。对称矩阵的特征值为实数，具有完全正交的特征向量。这里的“有”，是指可以选出一套完全正交的特征向量（例如在重特征值条件下，可能存在一个平面内向量都可以作为特征向量）。

如果***A***具有n个线性无关的特征向量，可以对角化得到 $\boldsymbol{A}=\boldsymbol{S}\boldsymbol{\varLambda}\boldsymbol{S}^{-1}$ 。而对于对称矩阵， $\boldsymbol{A}=\boldsymbol{Q}\boldsymbol{\varLambda}\boldsymbol{Q}^{-1}=\boldsymbol{Q}\boldsymbol{\varLambda}\boldsymbol{Q}^{T}$ ，其中***Q***为正交矩阵，列向量为标准正交基，这个公式本身还显示了矩阵的对称性。矩阵能够进行这种分解，在数学上称为“谱定理”（spectral theorem），将特征值视为“谱”，而在物理上称之为“主轴定理”。

- **实特征值 Real eigenvalues**

矩阵***A***具有特征值 $\lambda$ 和特征向量**x**，则有 $\boldsymbol{A}\boldsymbol{x}=\lambda\boldsymbol{x}$ 。若为复数，则其共轭复数满足

$\boldsymbol{A} \boldsymbol{\bar{x}} = \bar \lambda\boldsymbol{\bar x}$ 。两侧取转置，则有：$\boldsymbol{\bar{x}}^T\boldsymbol{A}^T=\boldsymbol{\bar{x}}^T\bar \lambda$ ，

两侧同乘**x**，则： $\boldsymbol{\bar{x}}^T\boldsymbol{A}^T\boldsymbol{x}=\boldsymbol{\bar{x}}^T\bar \lambda\boldsymbol{x}$ ，

因为矩阵为对称矩阵，则有： $\boldsymbol{\bar{x}}^T\lambda\boldsymbol{x}=\boldsymbol{\bar{x}}^T\bar \lambda\boldsymbol{x}$ ,若$\boldsymbol{\bar{x}}^T\boldsymbol{x}\ne0$ 则有 $\bar \lambda=\lambda$ ,即 $\lambda$ 为实数。

因为 $\bar {\boldsymbol{x}}$ 为**x**的共轭，因此两者点积得到的是**x**中的每一分量与其共轭复数的乘积之和，即复向量**x**之模，当且仅当**x**=**0**时，其模为0。

${\boldsymbol {\bar x}^T}\boldsymbol{x} = \left[ {\begin{array}{*{20}{c}} {{{\bar x}_1}}&{{{\bar x}_2}}&{{{\bar x}_3}}&{{{\bar x}_4}} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{x_1}}\\ {{x_2}}\\ {{x_3}}\\ {{x_4}} \end{array}} \right] = {\left| {{x_1}} \right|^2} + {\left| {{x_2}} \right|^2} + {\left| {{x_3}} \right|^2} + {\left| {{x_4}} \right|^2}$ 

因此得证$\lambda$ 为实数。

对于复矩阵***A***，若有$\boldsymbol{A}=\boldsymbol{\bar A}^T$ 则上面的推导全部成立，因此共轭对称复矩阵***A***的特征值为实数。

对于对称矩阵， $\boldsymbol{A}=\boldsymbol{Q}\boldsymbol{\varLambda}\boldsymbol{Q}^{-1}=\boldsymbol{Q}\boldsymbol{\varLambda}\boldsymbol{Q}^{T}$ ，可以写作：

$\begin{array}{*{20}{l}} \boldsymbol{A}=\boldsymbol{Q}\boldsymbol{\varLambda}\boldsymbol{Q}^{-1}&{{\rm{ = }}\left[ {\begin{array}{*{20}{c}} {{\boldsymbol{q}_1}}&{{\boldsymbol{q}_2}}& \cdots &{{\boldsymbol{q}_{\rm{n}}}} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{\lambda _1}}&{}&{}&{}\\ {}&{{\lambda _2}}&{}&{}\\ {}&{}& \ddots &{}\\ {}&{}&{}&{{\lambda _{\rm{n}}}} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} {{\boldsymbol{q}_1}^T}\\ {{\boldsymbol{q}_2}^T}\\  \vdots \\ {{\boldsymbol{q}_{\rm{n}}}^T} \end{array}} \right]}\\ {}&{{\rm{ = }}{\lambda _1}{\boldsymbol{q}_1}{\boldsymbol{q}_1}^T{\rm{ + }}{\lambda _2}{\boldsymbol{q}_2}{\boldsymbol{q}_2}^T{\rm{ + }} \cdots {\rm{ + }}{\lambda _{\rm{n}}}{\boldsymbol{q}_{\rm{n}}}{\boldsymbol{q}_{\rm{n}}}^T} \end{array}$ 

矩阵 $\boldsymbol{q}_k\boldsymbol{q}_k^T$ 是朝向向量**q**k的投影矩阵，所以每一个对称矩阵都是正交投影矩阵的线性组合。这是理解谱定理的另一种方法。

当确认矩阵特征值为实数后，下一个要考虑的问题就是它是正还是负数，因为这影响着微分方程中体系的稳定与否。但是对于大型矩阵通过计算 $\left| {\boldsymbol{A}{\rm{ - }}\lambda \boldsymbol{I}} \right|{\rm{ = }}0$ 得到特征值进行判定难以实现，即使用MATLAB求解结果也不一定可靠，但MATLAB可以得到矩阵的主元，而对称阵的主元中正负数的个数与特征值相同，即正主元的数目等于正特征值的数目。


---


> 对于对称阵主元与特征值符号相匹配这件事情，通常是用合同矩阵的惯性定理加以证明。若存在可逆矩阵**C **满足$\boldsymbol{A}=\boldsymbol{CBC}^T$ ，就称***A* **与***B* **为合同矩阵，惯性定理是指矩阵的特征值符号经过合同变换后不发生变化。对称阵***A ***经过消元操作可得$\boldsymbol{A}=\boldsymbol{L}\boldsymbol{D}\boldsymbol{L}^{T}$ ，而经过对角化处理得到$\boldsymbol{A}=\boldsymbol{Q}\boldsymbol{\varLambda}\boldsymbol{Q}^{T}$ ，两者比较可知$\boldsymbol{D}=(\boldsymbol{L}^{-1}\boldsymbol{Q})\boldsymbol{\varLambda}(\boldsymbol{L}^{-1}\boldsymbol{Q})^{T}$ ，因此两个对角阵为合同矩阵，主元和特征值的符号匹配。
> G.Strang 在书里给了一个接近同伦理论的证明：对于对称矩阵 可做分解，如$\left[ {\begin{array}{*{20}{c}} 1&3\\ 3&1 \end{array}} \right]{\rm{ = }}\left[ {\begin{array}{*{20}{c}} 1&{}\\ 3&1 \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1&{}\\ {}&{{\rm{ - }}8} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1&3\\ {}&1 \end{array}} \right]$ ，在下三角阵转变 $\left[ {\begin{array}{*{20}{c}} 1&0\\ 3&1 \end{array}} \right] \to \left[ {\begin{array}{*{20}{c}} 1&0\\ 0&1 \end{array}} \right]$的过程中，矩阵的变化为 $\left[ {\begin{array}{*{20}{c}} 1&3\\ 3&1 \end{array}} \right] \to \left[ {\begin{array}{*{20}{c}} 1&0\\ 0&{{\rm{ - }}8} \end{array}} \right]$ ，矩阵的特征值也从4，-2 变为1，-8（即原矩阵的主元）。这个过程中如果特征值发生符号变化，则总有一个瞬间特征值穿过0点，那个瞬间矩阵应该是奇异阵，但是相乘的三个矩阵一直是非奇异阵，因此不可能有这样一个时刻存在，所以特征值不会发生符号变化，即和主元符号保持一致。


---


矩阵***A***+b***I***的特征值比矩阵***A***的特征值大b，可以通过***A***+b***I***的主元来了解矩阵***A***的特征值与b的大小关系，因此利用这个性质可以估计特征值的状态。

- **正定矩阵 Positive definite matrices**

正定矩阵***A***是特征值都为正数的对称矩阵。它的主元也均为正数。

例如矩阵***A***= $\left[ {\begin{array}{*{20}{c}} 5&2\\ 2&3 \end{array}} \right]$ 。主元为5和det***A***/5=11/5。对称矩阵主元都为正数，则是正定矩阵。计算其特征值为： $\left| {\boldsymbol{A}-\lambda \boldsymbol{I}} \right|{\rm{ = }}{\lambda ^2}{\rm{ - 8}}\lambda {\rm{ + 11 = }}0$ ， $\lambda {\rm{ = 4}} \pm \sqrt 5 $ 。

因为主元和特征值都是正的，可以知道正定矩阵的特征值也是正的。但是反之并不成立。矩阵 $\left[ {\begin{array}{*{20}{c}} {{\rm{ - }}1}&0\\ 0&{{\rm{ - }}3} \end{array}} \right]$ 的行列式也是正的，但不是正定矩阵。

若将行列式作为正定的判据，则要求n阶矩阵左上角的所有kxk（1<=k<=n）子行列式（subdeterminant）数值均为正，矩阵确定为正定矩阵。

本讲的内容将之前教授的主元、行列式和特征值的概念结合在了一起，对于正定矩阵这些都是正的，当完全掌握了它们的性质后会推广到非对称矩阵，甚至非方阵。

# 第26讲 复矩阵；快速傅里叶变换

Complex matrices; fast Fourier transform

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2B4U77)

实矩阵也可能有复特征值，因此无法避免在矩阵运算中碰到复数，本讲学习处理复数矩阵和复向量。

最重要的复矩阵是傅里叶矩阵，它用于傅里叶变换。而对于大数据处理快速傅里叶变换（FFT）显得更为重要，它将矩阵乘法的运算次数从 $n^2$ 次降至 $nlog_2n$次。

- **复向量 Complex vectors**

对于给定的复向量**z**= $\left[ {\begin{array}{*{20}{c}} {{z_1}}\\ {{z_2}}\\  \vdots \\ {{z_{\rm{n}}}} \end{array}} \right] \in {\boldsymbol{C}^n}$ ，其元素中有复数，因此 $\boldsymbol{z}^T\boldsymbol{z}$ 无法给出向量的长度。例如： $\left[ {\begin{array}{*{20}{c}} 1&i \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1\\ i \end{array}} \right] = 0$ 。则定义 ${\left| \boldsymbol{z} \right|^2}={\bar {\boldsymbol z}^T}\boldsymbol z={\left| {{z_1}} \right|^2} + {\left| {{z_1}} \right|^2} +  \cdots  + {\left| {{z_1}} \right|^2}$ 为向量长度。因此向量 $\left[ {\begin{array}{*{20}{c}} 1\\ i \end{array}} \right]$ 的长度就是 $\left[ {\begin{array}{*{20}{c}} 1&{{\rm{ - }}i} \end{array}} \right]\left[ {\begin{array}{*{20}{c}} 1\\ i \end{array}} \right] = 2$ 。记 $\left| \boldsymbol{z} \right|^2=\boldsymbol{\bar z}^T\boldsymbol{z}={\boldsymbol{z}^H}\boldsymbol{z}$ 。H来自于“Hermite”。

与之相似，内积的定义也变为 ${\boldsymbol{y}^H}\boldsymbol{x}={\boldsymbol{\bar y}^T}\boldsymbol{x}={\bar y_1}{x_1} + {\bar y_2}{x_2} +  \cdots  + {\bar y_n}{x_n}$ 。

- **复矩阵 Complex matrices**

上一讲中讲到了对于复矩阵***A***，若有 $\boldsymbol{\bar A}^T=\boldsymbol{A}$ 则复矩阵***A***的特征值为实数。这种复矩阵被称为埃尔米特矩阵（Hermitian matrixes）。又译作“厄米特矩阵”或者“厄米矩阵”。转置共轭记作$\boldsymbol{A}^H=\boldsymbol{\bar A}^T$。

例如矩阵 $\left[ {\begin{array}{*{20}{c}} 2&{3{\rm{ + }}i}\\ {3 - i}&5 \end{array}} \right]$ 为埃尔米特矩阵。它具有实数特征值和正交的特征向量。由性质可知埃尔米特矩阵对角线均为实数。

此处向量标准正交的意思是 ${\boldsymbol{\bar q}_{j}}^T{\boldsymbol{q}_{k}}=\left\{ {\begin{array}{*{20}{c}} 0&{j \ne k}\\ 1&{j = k} \end{array}} \right.$ 。用n个标准正交的复向量作为列向量可以构造一个矩阵***Q***，则有 ${\boldsymbol{Q}^T}\boldsymbol{Q} =\boldsymbol{I} = {\boldsymbol{Q}^H}\boldsymbol{Q}$ 。这个复空间的正交矩阵称为酉矩阵（unitary matrix）。

- **傅里叶变换Fourier transform**

傅里叶级数是将周期函数或者信号变换为不同频率的三角函数的和函数。

$f(x) = {a_0} + {a_1}\cos x + {b_1}\sin x + {a_2}\cos 2x + {b_2}\sin 2x +  \cdots $ 

在电子工程或者计算机科学中，矩阵的行和列从第0行和第0列开始计数，最后到第n-1行和第n-1列。我们在讨论傅里叶矩阵的时候遵从这种习惯。

${\boldsymbol{F}_n} = \left[ {\begin{array}{*{20}{r}} 1&1&1& \cdots &1\\ 1&\omega &{{\omega ^2}}&{}&{{\omega ^{(n - 1)}}}\\ 1&{{\omega ^2}}&{{\omega ^2}}&{}&{{\omega ^{2(n - 1)}}}\\  \vdots &{}&{}& \ddots &{}\\ 1&{{\omega ^{n - 1}}}&{{\omega ^{2(n - 1)}}}&{}&{{\omega ^{{{(n - 1)}^2}}}} \end{array}} \right]$ 

$(\boldsymbol{F}_n)_{jk}=\omega^{jk}$ ，傅里叶矩阵为对称矩阵 $\boldsymbol{F}_n=\boldsymbol{F}_n^T$ 。矩阵中的 $\omega^n=1,\omega=e^{i2\pi/n}$ 。矩阵的列向量正交。的方次分布在复平面的单位元上，只是幅角不同。当n=4时，$\omega^4=1,\omega=e^{i2\pi/4}=i$。

${\boldsymbol{F}_4} = \left[ {\begin{array}{*{20}{c}} 1&1&1&1\\ 1&i&{{i^2}}&{{i^3}}\\ 1&{{i^2}}&{{i^4}}&{{i^6}}\\ 1&{{i^3}}&{{i^6}}&{{i^9}} \end{array}} \right] = \left[ {\begin{array}{*{20}{r}} 1&1&1&1\\ 1&i&{ - 1}&{ - i}\\ 1&{ - 1}&1&{ - 1}\\ 1&{ - i}&{ - 1}&i \end{array}} \right]$ 

从矩阵可以得到一个四点（离散的）傅里叶变换，它的逆矩阵就是反傅里叶变换。逆矩阵很容易计算，因为傅里叶矩阵列向量正交。实际上这个矩阵可以分解成一系列稀疏矩阵，并且它们的逆矩阵都很容易得到。

计算可知列向量的模不是1，矩阵除以2之后，向量标准正交： $\frac{1}{4}{\boldsymbol{F}_4}^H{\boldsymbol{F}_4}{\rm{ = }}\boldsymbol{I}$ 。它的逆矩阵就是共轭转置。

- **快速傅里叶变换 Fast Fourier transform**

对于64阶傅里叶矩阵$\boldsymbol{F}_{64}$ 中的 $\omega_{64}$ 与32阶傅里叶矩阵 $\boldsymbol{F}_{32}$ 的元素 $\omega_{32}$ 相比，幅角是其一半， $(\omega_{64})^2=\omega_{32}$ 。可以从分块矩阵运算找到两者的联系：

$\left[ {{\boldsymbol{F}_{64}}} \right]{\rm{ = }}\left[ {\begin{array}{*{20}{r}} \boldsymbol{I}&\boldsymbol{D}\\ \boldsymbol{I}&{ -\boldsymbol{D}} \end{array}} \right]\left[ {\begin{array}{*{20}{r}} {{\boldsymbol{F}_{32}}}&0\\ 0&{{\boldsymbol{F}_{32}}} \end{array}} \right]\left[ \boldsymbol{P} \right]$ 

其中***P***是置换矩阵，而***D***为对角矩阵：

$\boldsymbol{P}{\rm{ = }}\left[ {\begin{array}{*{20}{r}} 1&0&0&0& \cdots & \cdots &0&0\\ 0&0&1&0&{}&{}&0&0\\ {}&{}&{}& \vdots &{}&{}&{}&{}\\ 0&0&0&0& \cdots & \cdots &1&0\\ 0&1&0&0& \cdots & \cdots &0&0\\ 0&0&0&1& \cdots & \cdots &0&0\\ {}&{}&{}& \vdots &{}&{}&{}&{}\\ 0&0&0&0& \cdots & \cdots &0&1 \end{array}} \right]$ 

， $\boldsymbol{D} = \left[ {\begin{array}{*{20}{r}} 1&{}&{}&{}&{}\\ {}&\omega &{}&{}&{}\\ {}&{}&{{\omega ^2}}&{}&{}\\ {}&{}&{}& \ddots &{}\\ {}&{}&{}&{}&{{\omega ^{31}}} \end{array}} \right]$ 

***P***的效果是使得所乘的向量**x**序数为奇数的分量如x1，x3，x5等提到前面，而偶数分量x2，x4等放到后面。

计算64阶傅里叶变换（傅里叶矩阵乘以向量）的计算量是64x64，而等式右侧的计算量是2x32x32（两个32阶）再加上一些修正项，修正项主要来自于与对角矩阵***D***的乘法，大约为32次。继续对***F***32进行分解，计算的运算量再一次下降变为2 (2x16x16+16)+32。分解到最后，仅剩修正项的运算， $32\times log_264$ 次。对于n阶矩阵，即将$n^2$ 次计算降至 $(n/2)log_2n$次。例如对于1024阶矩阵，运算量从1024x1024降至5x1024。



# 第31讲 基变换和图像压缩

Change of basis; image compression

[网易公开课](http://open.163.com/newview/movie/free?pid=M6V0BQC4M&mid=M6V2BA04Q)

本讲介绍基变换。选择合适的基向量会给计算制造便利。基变换的一个重要应用就是压缩，图像、影像、音频和其它一些数据都会因为基变换而得到更高效的压缩储存。本讲的主题仍旧是线性变换和矩阵的关联。

- **图像压缩 Compression of images**

本讲涉及的压缩过程是有损压缩。例如一幅像素是512x512的静态黑白图像，图像用一个向量来表示，向量的分量xi表示像素的灰度，变化范围0<=xi<=255，占8bits。该向量属于**R**n空间，n=(512)x(512)。彩色图像描述每个点的像素需要三个数据，向量长度是黑白图像的3倍。

图像的标准压缩方式为JPEG（联合图像专家组 Joint Photographic Experts Group）。图像压缩的本质就是基变换。

压缩前图像采用的基向量是标准基。但是在图像中离得很近的区域，颜色是非常接近的，比如教学视频中黑板的一个区域，这些区域像素的灰度值很接近，但是用标准基来存储并没有利用上这一特点，这就给了我们压缩的空间。

标准基就是 $\left[ {\begin{array}{*{20}{c}} 1\\ 0\\ 0\\  \vdots \\ 0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0\\ 1\\ 0\\  \vdots \\ 0 \end{array}} \right], \cdots \left[ {\begin{array}{*{20}{c}} 0\\ 0\\ 0\\  \vdots \\ 1 \end{array}} \right]$ ，而显然对于灰度很接近的情况， $\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 1\\  \vdots \\ 1 \end{array}} \right]$ 是一个很好的基（代表低频信号，频率为0，平滑。在图像压缩后经常会存在，因为其系数通常很大），在一组基中有一个这样的向量能解决很大的问题，可以处理像素灰度接近一致的情况。但图像不是灰度完全一致的，因此接下来的问题是跟它相配合的基要选择哪些。极端的情况包括选择 $\left[ {\begin{array}{*{20}{c}} { + 1}\\ { - 1}\\ { + 1}\\ { - 1}\\  \vdots  \end{array}} \right]$ ，它可以给出类似国际象棋盘那种黑白相间的状态（最高频信号，噪音、扰动……在图像压缩后很少存在），还有图像一半图像暗一半图像亮，可以选择 $\left[ {\begin{array}{*{20}{c}}  \vdots \\ { + 1}\\ { - 1}\\  \vdots \\ { - 1} \end{array}} \right]$ 。

- **傅里叶基 Fourier basis**

在JPEG中，将512x512的区域划分为8x8的区块进行处理，所用到的基是傅里叶基向量。

以**R**8中的基举例 $\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 1\\ 1\\ 1\\ 1\\ 1\\ 1 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 1\\ \omega \\ {{\omega ^2}}\\ {{\omega ^3}}\\ {{\omega ^4}}\\ {{\omega ^5}}\\ {{\omega ^6}}\\ {{\omega ^7}} \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 1\\ {{\omega ^2}}\\ {{\omega ^4}}\\ {{\omega ^6}}\\ {{\omega ^8}}\\ {{\omega ^{10}}}\\ {{\omega ^{12}}}\\ {{\omega ^{14}}} \end{array}} \right], \cdots \left[ {\begin{array}{*{20}{c}} 1\\ {{\omega ^7}}\\ {{\omega ^{14}}}\\ {{\omega ^{21}}}\\ {{\omega ^{28}}}\\ {{\omega ^{35}}}\\ {{\omega ^{42}}}\\ {{\omega ^{49}}} \end{array}} \right]$ 

![](https://pic4.zhimg.com/v2-47aac1128e8302217ee9334888d44963_b.jpg)

傅里叶基（Fourier basis）就是之前讲过的傅里叶矩阵的列向量，每个元素为复数的幂。在8x8区块中有64个系数，64个基向量，在这个64维空间中做基变换。

![](https://pic1.zhimg.com/v2-7338ecd7b4f9ebd936109c8fa36a7574_b.jpg)

首先对输入的信号**x**，从标准基变换为傅里叶基，得到系数c，这一步是无损的过程。之后设置阀值进行压缩，超过阀值的认定为肉眼无法分辨的信号。在数学上表现为某些基向量的系数很小，这部分可以丢弃，随之得到新的系数 $\hat c$ 。将新的系数赋值在傅里叶基上求和得到 $\boldsymbol{\hat x} = \sum {{{\hat c}_i}{\boldsymbol{v}_i}} $ 。此时求和项已经不是64项，可能只剩下两三项，这就是压缩。

视频文件可以视为图像的序列，一幅一幅进行图像压缩即可。但这样做没有利用好视频的性质，因为视频是连续的，一幅图像和下一幅图像非常接近，因此可以存储一幅基础图像，随后只存储下一幅图像对它的修正部分。

- **小波 Wavelets**

下面介绍另一组和傅里叶竞争的基向量——小波。

以**R**8中的基举例 $\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 1\\ 1\\ 1\\ 1\\ 1\\ 1 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ 1\\ 1\\ { - 1}\\ { - 1}\\ { - 1}\\ { - 1} \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 1\\ 1\\ { - 1}\\ { - 1}\\ 0\\ 0\\ 0\\ 0 \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 0\\ 0\\ 0\\ 0\\ 1\\ 1\\ { - 1}\\ { - 1} \end{array}} \right],\left[ {\begin{array}{*{20}{c}} 1\\ { - 1}\\ 0\\ 0\\ 0\\ 0\\ 0\\ 0 \end{array}} \right], \cdots \left[ {\begin{array}{*{20}{c}} 0\\ 0\\ 0\\ 0\\ 0\\ 0\\ 1\\ { - 1} \end{array}} \right]$ 。

这个只是一个小波选择，还有很多种更多精细的选择，这一组基中有太多从+1跳转到-1的变化。线性代数要做的基变换，就是将标准基下的向量**p**=[p1,p2,p3……p8]表示为小波基的线性组合，求出线性组合的参数**c**满足**p**=c1**w**1+c2**w**2+……+c8**w**8，即**p**=***W*** **c**。***W***即以小波基向量为列向量的小波矩阵。因此有 $\boldsymbol{c}=\boldsymbol{W}^{-1}\boldsymbol{p}$ 。

好的基向量组要求：第一，可以快速求逆矩阵，例如快速傅里叶变换，这里也存在快速小波变换，因为小波矩阵列向量正交，因此可以转置得到逆矩阵；第二，要少量基向量就可以近似信号，可压缩的比例就比较高。

- **基变换 Change of basis**

***W***的列向量是一组新的基向量。在旧基向量体系下的向量**x**和新基向量下的**c**的关系是：**x**=***W*** **c**。

- **变换矩阵**

已知一个线性变换***T***：**R**8→**R**8。当使用空间的一组基**v**1，**v**2……**v**8时，线性变换对应的矩阵为***A***；当使用一组新的基**u**1，**u**2……**u**8时，线性变换对应的矩阵为矩阵***B***。两个矩阵对应的是同一个线性变换，只是使用了不同的基向量。那么***A***和***B***为相似矩阵 $\boldsymbol{B}=\boldsymbol{M}^{-1}\boldsymbol{A}\boldsymbol{M}$ ，***M***是基变换矩阵。

复习一下线性变换的内容：

$\boldsymbol{x}=c_1\boldsymbol{v}_1+c_2\boldsymbol{v}_2+…+c_8\boldsymbol{v}_8$ 

$$
\boldsymbol{T}(\boldsymbol{x})=c_1\boldsymbol{T}(\boldsymbol{v}_1)+c_2\boldsymbol{T}(\boldsymbol{v}_2)+…+c_8\boldsymbol{T}(\boldsymbol{v}_8)
$$

$\boldsymbol{T}(\boldsymbol{v}_1)=a_{11}\boldsymbol{v}_1+a_{21}\boldsymbol{v}_2+…+a_{81}\boldsymbol{v}_8$，

$\boldsymbol{T}(\boldsymbol{v}_2)=a_{12}\boldsymbol{v}_1+a_{22}\boldsymbol{v}_2+…+a_{82}\boldsymbol{v}_8$ ，

……

矩阵***A***就是aij组成的矩阵。

如果我们使用的基向量就是特征向量 $\boldsymbol{T}(\boldsymbol{v}_i)=\lambda_i\boldsymbol{v}_i$ ，矩阵***A***就变成对角阵***Λ***。找出特征向量是压缩最理想的结果，但是找出图像的特征向量代价太大，因此我们找到代价小但是接近理想状态的基向量（例如小波基）进行基变换，完成压缩过程。

> 之前我在线性变换和基变换这两讲后面留了很多具体文字，希望帮助大家理解和区分这些概念，但是有的小伙伴貌似反而被误导，所以我把另一门课程的几何描述放在这里，希望大家看了之后可以完全明白，基变换是在同一个空间中，改变对一个东西的描述方式而已。

[三少爷的贱男春：线性代数的本质09 基变换](https://zhuanlan.zhihu.com/p/110975625)

# Chapter 3 输运和热扩散


## 气体的输运性质

气体一般考虑三种输运性质：
+ 黏性，动量的量运
+ 热传导，热量的量运
+ 扩散，粒子的输运

### 黏性

黏性：流体对由剪应力产生的形变抵抗程度的量度。

对于平直、平行、均匀的流动，层与层之间的剪应力正比于垂直于层方向的速度梯度，我们称之为黏性系数$\eta$

我们可以定义动量通量：

$$
\Pi_{z}=-\eta\frac{\partial \langle u_x \rangle}{\partial z}=\int_{0}^{\infty}\int_{0}^{\pi}v\cos\theta nf\mathrm{d}v\frac{1}{2}\sin\theta\mathrm{d}\theta m(-\frac{\partial\left\langle v_{x}\right\rangle}{\partial z})\lambda\cos\theta
$$

得

$$
\eta = \frac13nm\lambda\langle v \rangle
$$

有以下推论：

带入各个表达式，有

$$
\eta = \frac{2}{3\pi d^2}\sqrt{\frac{mk_BT}{\pi}}
$$

### 热传导

热流可以用热通量矢量$\vec{J}$描述，在$z$方向，有：

$$
J_z=-\kappa \frac{\partial T}{\partial z}
$$

在三维情况下:

$$
\vec{J}=-\kappa \nabla T
$$

$$
\begin{aligned}
J_{z}& =\int_{0}^{\infty}\int_{0}^{\pi}v\cos\theta nf\mathrm{d}v\frac{1}{2}\sin\theta\mathrm{d}\theta C_{\text{分子}}(\frac{\partial T}{\partial z})\lambda\cos\theta  \\
&=-\frac{1}{3}nC_{\text{分子}}\lambda\left\langle v\right\rangle\frac{\partial T}{\partial z}
\end{aligned}
$$

得

$$
\kappa=\frac{1}{3}C_{V}\lambda \langle v\rangle
$$

同理可得：

$$
\kappa = \frac{2}{3\pi d^2}C_{\text{分子}}\sqrt{\frac{k_BT}{\pi m}}
$$

### 扩散

对于$z$方向分子通量，有：

$$
\Phi_z=-D\frac{\partial n}{\partial z}
$$

考虑厚度为d$z$，面积为$A$的一薄块气体，进入薄块的通量为$A\Phi_z$，流出薄块的通量为$A(\Phi_z+\frac{\partial \Phi_z}{\partial z}\mathrm{d}z)$

这两个通量之差必须被该区域内随时间而变的带标记的粒子数所平衡，因此有：

$$
\frac{\partial}{\partial t}(nA\mathrm{d}z)=-A\frac{\partial Phi_z}{\partial z}\mathrm{d}z
$$

得

$$
\frac{\partial n}{\partial t}=D\frac{\partial^2n}{\partial z^2}
$$

$$
D=\frac13\langle v \rangle
$$

同时与前面类似，有：

$$
D=\frac{2}{3\pi n d^2}\sqrt{\frac{k_BT}{\pi m}}
$$

## 热扩散方程

### 热扩散方程的推导

我们知道

$$
\vec{J}=-\kappa\nabla T\quad \&\quad \vec{\Phi}=-D\nabla n
$$

我们知道不能破坏能量和粒子以及电荷的守恒，对于一个封闭曲面$S$，流出的总热量为

$$
\int_s \vec{J}\mathrm{d}S
$$

这是一个有功率量纲的量，因此它应该为曲面内无职损失能量的速率，即$S$包裹体积$V$中总动能的变化率。热能可以写为体积分$\int_VCT\mathrm{d}V$，其中$C$为单位体积的热容，等于$\rho c$，则

$$
\int_S\vec{J}\cdot \mathrm{d}S=-\frac{\partial}{\partial t}\int_V CT\mathrm{d}V
$$

因此

$$
\nabla \cdot \vec{J}=-C\frac{\partial T}{\partial t}
$$

得到

$$
\frac{\partial T}{\partial t} = D\nabla^2T
$$

### 稳恒态

如果系统到达一个稳恒态，此时

$$
\nabla^2 T = 0
$$

这为一个拉普拉斯方程

### 球扩散方程

在三维球坐标下：

$$
\frac{\partial T}{\partial t} = \frac{\kappa}{Cr^2}\frac{\partial}{\partial r}(r^2\frac{\partial T}{\partial r})
$$

### 牛顿冷却定律

牛顿冷却定律：正在冷却的物体的温度指数下降而趋近于周围环境的温度，下降的速率正比于物体与环境之间的接触面积，即

$$
\vec{J}=\vec{h}\Delta{T}
$$

其中$\vec{h}$为一个垂直于物体表面的矢量，其大小为传热系数

### 普朗特数

定义普朗特数：

$$
\sigma_p=\frac{\nu}{D}=\frac{\eta c_p}{\kappa}
$$

普朗特数（Prandtl number）是一个无量纲数，用于描述流体中的传热现象。它定义为动量扩散率（黏性扩散率）与热扩散率之比，它表征了流体中动量和热量传递的相对重要性。

### 热源

如果热量以每单位体积的速率$H$产生，则对于热扩散方程

$$
\frac{\partial T}{\partial t}=D\nabla^2T+\frac{H}{C}
$$



# Chapter 2 气体动理学理论


## 麦克斯韦-玻尔兹曼分布

### 速度分布

我们定义速度分布函数：

$$g(v_x)\propto\exp\frac{-mv_x^2}{2k_BT}$$

对这个函数归一化，有：

$$g(v_x)=\sqrt{\frac{m}{2\pi k_{B}T}}\exp\frac{-mv_x^2}{2k_BT}$$

$$
\begin{aligned}
&\langle v_{x}\rangle=\int_{-\infty}^{\infty}v_{x}g(v_{x})dv_{x}=0 \\
&\langle|v_{x}|\rangle=\sqrt{\frac{2k_{B}T}{\pi m}} \\
&\langle v_{x}^{2}\rangle=\frac{k_{B}T}{m}
\end{aligned}
$$

### 速率分布

在热力学中，我们更关注系统的速率分布，定义速率分布函数：

$$f(v)=\frac{4}{\sqrt{\pi}}\biggl(\frac{m}{2k_{B}T}\biggr)^{3/2}v^{2}\exp(-\frac{1}{2}mv^{2}\beta)$$

我们称这个分布为麦克斯韦-玻尔兹曼速率分布，我们能求得其速率的期望和均方：

$$
\begin{aligned}
&\langle v\rangle=\int_{0}^{\infty}vf(v)dv=\sqrt{\frac{8k_{B}T}{\pi m}} \\
&\langle v^{2}\rangle=\frac{3k_{B}T}{m}\\
&\langle E_{KE} \rangle = \frac12 \langle v^{2}\rangle =\frac32k_BT
\end{aligned}
$$

同时我们也能求出$f(v)$的极大值

$$v_{max}=\sqrt{\frac{2k_BT}m}$$

## 压强

压强：压力与接触面积之比

我们定义状态方程：

$$p=f(T,V,N)$$

它的一个典型离子是理想气体状态方程：

$$pV=Nk_BT$$

### 理想气体定律

接下来我们导出理想气体状态方程，$f(v)$为麦克斯韦-玻尔兹曼速度分布，面积为$A$的器壁与垂直方向夹角为$\theta$,在时间 d$t$时间内速度为
$v$的分子恰好撞到器壁上为：

$$\mathrm{d}N=Av\mathrm{d}t\cos\theta\frac{1}{2}\sin\theta\mathrm{d}\theta nf(v)\mathrm{d}v$$

则可得到：

$$
p=\int_0^\infty\int_0^{\pi/2}2mv\cos\theta v\cos\theta\frac{1}{2}\sin\theta\mathrm{d}\theta nf(v)\mathrm{d}v\\
p=\frac13nm\langle v^2\rangle
$$

则：

$$
pV=Nk_BT
$$

式中$N$为气体分子总数，若令$R=N_Ak_B$，由$N=N_An$，则得到我们常见的形式：

$$pV=nRT$$

### 道尔顿分压定律

如果处于热平衡的集中气体的混合物，则总压强为混合物各组分的压强的和：

$$p=\sum_ip_i$$

## 分子泻流

泻流：液体或气体从一个非常小的口流出或泄漏的现象，由**格拉姆泻流定律**：分子的泻流速率反比于泻流分子的质量的平方根。

### 通量

定义通量：

$$\text{通量}=\frac{\text{某种属性}}{\text{面积}\cdot\text{时间}}$$

对于分子通量：

$$\Phi=\frac{n}{St}$$

$$\Phi=\int_0^\infty\int_0^{\pi/2}v\cos\theta\frac{1}{2}\sin\theta\mathrm{d}\theta nf(v)\mathrm{d}v$$

带入理想气体状态方程，有:

$$\Phi=\frac{p}{\sqrt{2\pi mk_BT}}$$

### 泻流速率

若定义面积为$S$，则泻流速率为$S\Phi$

泻流优先选择速率较快的分子，因此从小孔泻流的分子速率不符合麦克斯韦分布。

由于速率更高的分子有更大的概率到达小孔，即速率分布：

$$f \propto v^3\exp(-\frac{mv^2}{2k_BT})$$

## 平均自由程和碰撞

### 平均碰撞时间

我们假设所考虑的分子正以速率$v$运动，而气体中的气体分子是静止的，在d$t$内，一个分子将扫过$\sigma v\mathrm{d}t$，则d$t$碰撞的概率为$n\sigma v\mathrm{d}t$，定义$P(t)$为一个分子直到$t$才发生碰撞的概率，则

$$P(t+\mathrm{d})=P(t)(1-n\sigma v\mathrm{d}t)$$

整理得

$$P(t)=\exp(-n\sigma vt)$$

则我们可以计算两次碰撞之间平均经历时间

$$
\begin{aligned}
\tau&=\int_0^\infty tP(t)n\sigma v\mathrm{d}t\\
&=frac{1}{n\sigma v}
\end{aligned}
$$

这就是平均碰撞时间。

### 碰撞截面

考虑两个半径为$a_1$、$a_2$的球形分子，定义碰撞截面

$$
\sigma=\pi(a_1+a_2)^2
$$

### 平均自由程

平均自由程：在一定的条件下, 一个气体分子在连续两次碰撞之间可能通过的各段自由程的平均值

由平均碰撞时间，我们可以得到：

$$
\lambda = \langle v \rangle \tau \approx \frac{1}{\sqrt{2}n\sigma}
$$

带入状态方程

$$
\lambda = \frac{k_BT}{\sqrt{2}p\sigma}
$$







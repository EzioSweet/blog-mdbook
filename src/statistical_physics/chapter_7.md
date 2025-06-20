# Chapter 7 统计力学

## 能量均分

### 能量均分定理

定义：如果一个经典系统的能量是$n$个平方模之和，且该系统与一个温度为$T$的恒温热源进行接触，则系统的平均能量为:$n\times \frac{1}{2}k_BT$

### 单原子气体的平动

单原子气体中每个原子的能量为：

$$
E=\frac{1}{2}mv_x^2+\frac{1}{2}mv_y^2+\frac{1}{2}mv_z^2
$$

则其由三个独立的平方模之和，则其能量为$\langle E\rangle=\frac32k_BT$

### 双原子气体的转动

$$
E=\frac{1}{2}mv_x^2+\frac{1}{2}mv_y^2+\frac{1}{2}mv_z^2+\frac{L_1^2}{2I_1}+\frac{L_2^2}{2I_2}
$$

则能量为$$\frac52k_BT$$

能量均分定理通常仅在高温下有效，高温使得热能远大于量子化能级之间的能量间隔

## 配分函数

定义配分函数为所有态的玻尔兹曼因子的和：

$$Z=\sum_\alpha\exp(-\beta E_\alpha)$$

解统计力学问题的步骤：
1. 写出配分函数
2. 按照标准程序得到态函数

### 写出配分函数

我们以几个例子来说明：

对于一个二能级系统，其能量为$\pm\frac{\Delta}{2}$，则

$$Z=\sum_i\exp{-\beta E_i}=\exp(\beta\frac{\Delta}{2})+\exp(-\beta\frac{\Delta}{2})=2\cosh(\frac{\beta\Delta}{2})$$

对于一个转动能级系统，其能量为$E_J=\frac{\hbar^2}{2I}J(J+1)$

$$Z=\sum_i\exp{-\beta E_i}=\sum_{J=0}^\infty(2J+1)\exp(-\beta\hbar^2\frac{J(J+1)}{2I})$$

### 得到态函数

$$
U=-\frac{\mathrm d \ln Z}{\mathrm \beta}\\
S=\frac{U}{T}+k_B\ln Z\\
F=-k_BT\ln Z\\
p=k_BT\left(\frac{\partial Z}{\partial V} \right)_T\\
H=U+pV\\
G=F+pV=H-TS
$$

### 组合配分函数

假定能量$E$依赖于各种独立的共线，比如是$a$和$b$两个系统的和，则

$$E=E_a+E_b$$

则

$$Z=Z_aZ_b$$

## 理想气体的统计力学

### 态密度

这里的态密度我们可以使用在固体物理中的定义，但不考虑电子自旋。

$$g(k)=\cdot\frac{L^3}{8\pi^3}\cdot 4\pi k^2\mathrm dk$$

### 量子密度

$$Z_1=\int_0^\infty exp(-\beta E(k))g(k)$$

对于单分子，有：

$$E=\frac{\hbar^2k^2}{2m}$$

则

$$Z_1=\frac{V}{\hbar^3}\biggl(\frac{mk_BT}{2\pi}\biggr)^{3/2}=Vn_Q$$

我们称$n_Q$为量子密度，则可定义热波长：

$$
\lambda_{th}=n_Q^{-1/3}=\frac h{\sqrt{2\pi mk_BT}}
$$

则

$$
Z_1=\frac{V}{\lambda_{th}^3}
$$

### 可分辨性

如果所有粒子均可分辨，则

$$
Z_N=(Z_1)^N
$$

如果所有粒子均不可分辨，则

$$
Z_N=\frac{Z_1^N}{N!}
$$

但是对于理想气体来说，往往是不可分辨的，则有：


$$
Z_N=\frac{1}{N!}\left(Z_1=\frac{V}{\lambda_{th}^3}\right)^N
$$

## 化学势

定义：如果向系统加入一个粒子而不改变系统的体积或熵，则系统的内能将改变一个量，我们就称这个改变量为化学势

则在粒子数变化的情况下，系统的内能必须包含另外一项，即：

$$
\mathrm dU=T\mathrm dS-p\mathrm dV+\mu\mathrm dN
$$

则有

$$
\mathrm{d}S=\left(\frac{\partial S}{\partial U}\right)_{N,V}\mathrm{d}U+\left(\frac{\partial S}{\partial V}\right)_{N,U}\mathrm{d}V+\left(\frac{\partial S}{\partial N}\right)_{U,V}\mathrm{d}N\\\mathrm{d}S=\frac{\mathrm{d}U}T+\frac{p\mathrm{d}V}T-\frac{\mu\mathrm{d}N}T
$$

由此我们可以得到

$$
\mu=\left(\frac{\partial U}{\partial N}\right)_{S,V}
$$

我们同理根据$F,G$的定义，有：

$$
\mu=\left(\frac{\partial F}{\partial N}\right)_{V,T}\\
\mu=\left(\frac{\partial G}{\partial N}\right)_{p,T}
$$

### 化学势的内涵

考虑两个可以交换热量的系统，如果系统1失去内能，则系统2必然得到同样的内能：

$$
\begin{aligned}
\text{dS}& =\left(\frac{\partial S_{1}}{\partial U_{1}}\right)_{N,V}\mathrm{d}U_{1}+\left(\frac{\partial S_{2}}{\partial U_{2}}\right)_{N,V}\mathrm{d}U_{2} \\
&=\left(-\frac1{T_1}+\frac1{T_2}\right)\mathrm{d}U\geqslant0
\end{aligned}
$$

考虑两个可以交换粒子的系统：

$$
\begin{aligned}
\text{ds}& =\left(\frac{\partial S_{1}}{\partial N_{1}}\right)_{U,V}\mathrm{d}N_{1}+\left(\frac{\partial S_{2}}{\partial N_{2}}\right)_{U,V}\mathrm{d}N_{2} \\
&=\left(\frac{\mu_1}{T_1}-\frac{\mu_2}{T_2}\right)\mathrm{d}N\geqslant0
\end{aligned}
$$

可以看到，当两个系统的化学势相同时，两个系统达到平衡。

### 巨配分函数

我们推广系统到能够和环境交换能量和粒子的情况，即巨正则系综。

我们考虑这样一个系统：固定体积$V$，具有能量$\epsilon$，包含$N$个粒子数的系统，能够和一个能量为$U-\epsilon$，粒子数为$\mathscr{N}-N$的源相连，可以用泰勒级数表示源的熵

$$
S(U-\epsilon,\mathscr{N}-N)=S(U,\mathscr{N})-\epsilon\left(\frac{\partial S}{\partial U}\right)_{\mathscr{N},V}-N\left(\frac{\partial S}{\partial \mathscr{N}}\right)_{U,V}
$$

则有:

$$
S(U-\epsilon,\mathscr{N}-N)=S(U,\mathscr{N})-\frac{1}{T}(\epsilon-\mu N)
$$

则我们可以写出概率：

$$
P(\epsilon,N)\propto \exp(\frac{S(U-\epsilon,\mathscr{N}-N)}{k_B})\propto \exp(\beta(\mu N-\epsilon))
$$

定义巨配分函数

$$
\mathscr{Z}=\sum_i \exp(\beta(\mu N_i-E_i))
$$

则$P=\frac{1}{\mathscr{Z}}\exp(\beta(\mu N_i-E_i))$

我们定义巨势：

$$
\Phi_G=-k_BT\ln\mathscr{Z}=F-\mu N
$$

则

$$
\mathscr{Z}=exp(-\beta\Phi_G)
$$

### 单粒子的化学势

对于单粒子，易得：

$$
\mu=\frac{G}{N}
$$

即化学势可以看作单粒子的吉布斯函数

同时巨势可以写成

$$
\Phi_G=-pV
$$

### 多粒子系统

多粒子系统有：

$$
\mathrm dG=\sum_i \mu_i\mathrm dN_i
$$

### 平衡常数

对于一个简单的化学反应：

$$
A\rightleftharpoons B
$$

我们定义平衡常数为平衡时反应物和生成物的分压比值：

$$
K=\frac{p_B}{p_A}
$$

研究其吉布斯函数：

$$
\mathrm dG=\mu_A\mathrm dN_A+\mu_B\mathrm dN_B \quad \& \quad \mathrm dN_B=-\mathrm dN_A
$$

则：

$$
\mathrm dG=(\mu_B-\mu_A)\mathrm dN_B
$$

则：

$$
\begin{aligned}\Delta_rG=\Delta_rG^\ominus+RT\ln\frac{p_B}{p_A}\end{aligned}
$$

其中$\Delta_rG^\ominus$为两种物质的摩尔化学势之差

可得：

$$
\ln K=-\frac{\Delta_rG^\ominus}{RT}
$$

则对于复杂反应，有：

$$
\sum_i\nu_i\mathrm{d}N_i=0\\\Rightarrow\sum_i\nu_i\mu_i=0
$$

方程一边为正，另一边为负

$$
K=\prod\left(\frac{p_j}{p^\ominus}\right)^{\nu_\mathbf{i}}\\
\frac{\mathrm{d}\ln K}{\mathrm{d}T}=\frac{\Delta_rH^\ominus}{RT^2}
$$

可得范托斯方程：

$$
\begin{aligned}\frac{\mathrm{d}\ln K}{\mathrm{d}1/T}=-\frac{\Delta_rH^\ominus}{R}\end{aligned}
$$

### 渗透

化学势之差可以驱动粒子从一个源流动到另一个源，这是熵驱动的，这种情况最典型的就是渗透现象

考虑一种溶液被半透膜隔开，允许较小的溶剂分子透过而不允许溶质分子透过，比如我们将糖水经过半透膜扣在纯水上，纯水会在渗透作用下进入糖水，使糖水液面升高，直到压强差和渗透压相同，才达到平衡

## 光子

我们可以用真空介电常数和磁导率来描述光速：

$$
c=(\varepsilon_0\mu_0)^{-\frac{1}{2}}
$$

同时光不仅有波动的性质，也有粒子的性质，我们用光子来描述光的粒子性，每个光子的有能量$\hbar\omega$，其中$\omega=2\pi\nu$为角频率，光子的动量为$\hbar k$，这里$k$为波矢。

$$\frac{\omega}{k}=c$$

在非零温度下，任何物质都会放出热辐射，以光子的形式辐射能量。

### 电磁辐射的经典热力学

我们将环境视为体积为$V$的容器，温度为$T$，光子气体单位体积内的光子数为$n$，则能量密度可以写为：

$$
u=\frac{U}{V}=n\hbar\omega
$$

辐射压强为：

$$
p=frac13nm\langle v^2 \rangle=\frac13 nmc^2=\frac13 n \hbar\omega
$$

光子通量为：

$$
\Phi=\frac14nc
$$

单位面积的入射功率为：

$$
F=\hbar\omega\Phi=\frac14uc
$$

则可以得到斯特藩-玻尔兹曼定律:

$$
u=\frac13T\biggl(\frac{\partial u}{\partial T}\biggr)_V-\frac13u
$$

得

$$u=AT^4$$

$$F=\frac14uc=\frac14AcT^4=\sigma T^4$$

其中$\sigma=\frac14Ac$为斯特藩-玻尔兹曼常量，上式称为斯特藩-玻尔兹曼定律。

定义谱能量密度：$u_\lambda$为$\lambda-\lambda+\mathrm d\lambda$内的光子的能量密度

$$
u=\int u_{\lambda} \mathrm{d}\lambda
$$

### 基尔霍夫定律

我们定义：
+ 谱吸收率$\alpha_\lambda$表示物体对波长为$\lambda$
+ 表面的谱辐射功率$e_\lambda$是一个函数，它使得$e_\lambda d\lambda$表示波长位于d$\lambda$内的电磁辐射每单位面积的辐射功率

则吸收功率可以为：

$$
(\frac14u_\lambda\mathrm d\lambda c)\alpha_lambda
$$

在平衡下，有：

$$
\frac{e_\lambda}{\alpha_\lambda}=\frac{c}{4}u_\lambda
$$

这就是基尔霍夫定律

### 辐射压强

光会对照射的物体施加一个压强

$$
p=u=\frac{\sigma T^4}{c}
$$

### 光子的统计力学

同样与固体物理类似，

$$
g(k)\mathrm dk=2\frac{L^3}{8\pi^3}\cdot 4\pi k^2\mathrm dk
$$

写成频率的函数：

$$
g(\omega)=\frac{g(k)}{c}
$$

则有：

$$
U=\int_0^\infty \epsilon f(\omega)g(\omega)\mathrm d\omega=\frac{V\pi^2k_BT^4}{15c^3\hbar^3}T^4
$$

同理，对于黑体辐射 ：

$$
\sigma=\frac{\pi^2k_B^4}{60c^2\hbar^3}\\u=\int u_\omega\mathrm{d}\omega\\u_\omega=\frac\hbar{\pi^2c^3}\frac{\omega^3}{e^{\beta\hbar\omega}-1}
$$

### AB理论

对于自发辐射$A_{21}$、受激吸收$B_{12}$、受激辐射$B_{21}$，有：

$$
N_2B_{21}+N_2A_{21}=N_1B_{12}u_\omega
$$

则有：

$$
\begin{aligned}
u_{\omega} &=\frac{A_{21}/B_{21}}{(g_{1}B_{12}/g_{2}B_{21})e^{-\beta\hbar\omega}-1} \\
\frac{B_{21}}{B_{12}}&=\frac{g_{1}}{g_{2}} \\
A_{21}&=\frac{\hbar\omega^{3}}{\pi^{2}c^{3}}B_{21}
\end{aligned}
$$

## 声子

本部分可以参考固体物理部分的爱因斯坦模型和德拜模型，色散关系可以参考电子气部分

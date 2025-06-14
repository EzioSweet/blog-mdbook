# Chapter 8 超越理想气体

## 相对论性气体

### 有质量粒子的相对论性色散关系

在导出气体的配分函数时，我们认为$\frac{p}{m}\ll c$，所以才能成立，而一般的，对于相对论气体，有：

$$
E^2=p^2c^2+m^2c^4
$$

其中$m$为静质量，当位于非相对论极限时

$$
E=\frac{p^2}{2m}+mc^2
$$

这和我们经典近似式完全相同，除了多了一个额外的常数。在$p\gg mc$时，即极端相对论极限，

$$
E=pc
$$

### 极端相对论气体

在极端相对论情形下，有：

$$
Z_1=\int_0^\infty\exp(-\beta \hbar kc)g(k)\mathrm dk=\frac{V}{\pi^2}(\frac{k_BT}{\hbar c})^3
$$

我们能看出来，对于极端相对论气体，有

$$
VT^3=\text{const}\\
pV^{\frac43}=\text{const}
$$

说明对于极端相对论气体，其绝热指数为$\gamma=\frac43$

## 实际气体

### 范德瓦尔斯模型

我们一般使用范德瓦尔斯模型来描述实际气体，其满足下列状态方程：

$$(p+\frac{a}{V_m^2})(V_m-b)=RT$$

$V_m$是摩尔体积，写出配分函数

$$Z_N=\frac1{N!}\left(\frac{V-n_\text{摩尔}}{\lambda_{th}^3}\right)^Ne^{\beta an_\text{摩尔}^2/V}$$

得到其等温压缩率

$$
\kappa_T=-\frac{1}{V}\left(\frac{\partial V}{\partial p}\right)_T=\frac{V^2-bV}{3V^2p-2Vpb-2VRT+a}
$$

我们能发现当温度低于一个临界温度时，等温压缩率变成负数。

临界体积：

$$
V_c=3b
$$

临界温度：

$$
T_c=\frac{8a}{27Rb}
$$

### 迪特利奇方程

范德瓦尔斯方程也可以表现为：

$$
p=p_{排斥}+p_{吸引}
$$

其中

$$
p_{排斥}=\frac{RT}{V_m-b}
$$

$$
p_{吸引}=\frac{-a}{TV_m^2}
$$

迪特利奇提出

$$
p=p_{排斥}\exp(-\frac{a}{RTV_m})
$$

即

$$
p(V_m-b)=RT\exp(-\frac{a}{RTV_m})
$$

这就是迪特利奇方程

### 位力展开

我们也可以用位力展开来描述实际气体

$$
\frac{pV_m}{RT}=1+\frac{B}{V_m}+\frac{C}{V_m^2}+...
$$

参数$B,C$等称为位力系数，而且可以是温度的函数。$B(T)$趋于0的温度称为波义耳温度，这是波义耳定律近似成立的温度


## 冷却实际气体

### 焦耳膨胀

前面已经对焦耳膨胀进行了简单的定义，我们定义焦耳系数：

$$
\mu_j=\left(\frac{\partial T}{\partial V}\right)_U=-\frac{1}{C_V}\left(\frac{\partial U}{\partial V}\right)_T
$$

由热力学第一定律，得

$$
\mu_J=-\frac{1}{C_V}\left[T\left(\frac{\partial p}{\partial T}\right)_V-p\right]
$$

### 等温膨胀

在等温膨胀中，由

$$
\left(\frac{\partial U}{\partial V}\right)_T=T\left(\frac{\partial p}{\partial T}\right)_V-p
$$

可得

$$
\Delta U =\int_{V_1}^{V_2}\left[T\left(\frac{\partial p}{\partial T}\right)_V-p\right]\mathrm dV
$$

### 焦耳-开尔文膨胀

考虑一个定常流动的过程，其中具有高压$p_1$的气体被迫通过节流阀进入$p_2$的低压区，考虑高压区一个体积为$V_1$，内能为$U_1$，通过节流阀时，高压气体对其做$p_1V_1$的功，在右侧变成$V_2$的体积，对右侧气体做$p_2V_2$的功，即：

$$
U_1+p_1V_1=U_2+p_2V_2
$$

因此焦耳-开尔文膨胀又称为等焓膨胀，或者称为节流过程。

定义焦耳-开尔文系数：

$$
\begin{aligned}
\mu_{JK}& =\left(\frac{\partial T}{\partial p}\right)_{H} \\
&=-\biggl(\frac{\partial T}{\partial H}\biggr)_{p}\biggl(\frac{\partial H}{\partial p}\biggr)_{T} \\
&=-\frac{1}{C_{p}}\bigg[T\bigg(\frac{\partial S}{\partial p}\bigg)_{T}+V\bigg] \\
&=\frac{1}{C_p}\Bigg[T\Bigg(\frac{\partial V}{\partial T}\Bigg)_p-V\Bigg]
\end{aligned}
$$

则

$$
\Delta T=\int_{p_1}^{p_2}\frac{1}{C_p}\bigg[T\bigg(\frac{\partial V}{\partial T}\bigg)_p-V\bigg]\mathrm dp
$$

这说明节流过程是可以加热也可以制冷

当

$$
\left(\frac{\partial V}{\partial T}\right)_p=\frac{V}{T}
$$

时，会变号

### 气体的液化

气体液化是一个节流过程，当$\mu_{JK}=0$时，有最大的液化效率

## 相变

### 潜热

为了提高物质的温度，需要提供热量，当物质发生相变的时候，需要提供一个热量来促使其进行物态变化，我们称这个热量为潜热。

$$
L=\Delta Q_{rev}=T_c(S_2-S_1)
$$

其中$S_1,S_2$是相变前后的熵，这说明在温度曲线上，存在一个阶跃点

一般来说气体的密度是液体的$10^{-3}$倍。

则：

$$
\Delta S=k_{B}(\ln\Omega_{g}-\ln\Omega_{l})=k_{B}\ln\left(\frac{\rho_{l}}{\rho_{g}}\right)^{N_{A}}=R\ln10^{3}=7R\\L=7RT_{b}
$$

这被称为特鲁顿规则

但是潜热一般比简单论证大一些，约为

$$
L\approx 10RT_b
$$

### 化学势和相变

$$\mathrm dG=V\mathrm dp-S\mathrm dT+\mu_1\mathrm dN_1+\mu_2\mathrm dN_2$$

由于处于平衡，则必有：

$$\mu_1=\mu_2$$

这说明，在相平衡时，每个共存相都有相同的化学势，其最低的相为稳定相，沿着共存曲线，有$\mu_1=\mu_2$

### 克劳修斯-克拉珀龙方程

我们在$p-T$界面上，其共存线

$$
\mu_1(p,T)=\mu_2(p,T)
$$

则必有：

$$
\mathrm d\mu_1=\mathrm d\mu_2
$$

我们定义单粒子相变潜热为$l=T\Delta S$,$v$指代体积

$$
\frac{\mathrm dp}{\mathrm dT}=\frac{l}{T(v_2-v_1)}
$$

单粒子显然可以推广到宏观，则我们得到克拉修斯-克拉珀龙方程：

$$
\frac{\mathrm dp}{\mathrm dT}=\frac{L}{T(V_2-V_1)}
$$

### 稳定性和亚稳性

在前面我们能够看到，化学势$\mu$最低的相是稳定相，因为由前面的知识我们可以知道，化学势$\mu$是单粒子的吉布斯函数，则有：

$$
\left(\frac{\partial \mu}{\partial p} \right)_T=v
$$

由于体积总是正的，则化学势随压强的变化总是正的，在最大压强下稳定的相因此必定有最小的体积，也就是说在压强越大的情况下，我们预期占据空间体积最小的相是最稳定的相。

我们也可以考虑$\mu$是温度的函数，则有：

$$
\left(\frac{\partial \mu}{\partial T} \right)_p=-s
$$

单粒子的熵$s>0$，则作为温度函数的化学势必然是递减的，则说明在高温度下稳定的相必有最大的熵

这也说明当加热一个物质到达沸点时，他有可能继续沿着$\mu_{liquid}$的曲线并形成过热液体，这是一个亚稳态，同理也有可能生成过冷蒸汽。

我们考虑如下情况：一个过冷蒸汽环境，$p_{liquid}$的液体和$p_{air}$的气体相平衡，则二者具有相同的化学势，若液体的压强增大$\mathrm dp_{liquid}$，则气体必增加$\mathrm dp_{air}$来平衡，则有：

$$
\left(\frac{\partial \mu_{liquid}}{\partial p_{liquid}}\right)_T\mathrm dp_{liquid}=\left(\frac{\partial \mu_{air}}{\partial p_{air}}\right)_T\mathrm dp_{air}
$$

则有：

$$
v_{liquid}\mathrm dp_{liquid} = v_{air}\mathrm dp_{air}
$$

利用理想气体的状态方程，我们可以得到：

$$
p_{air}=p_0\exp(\frac{V_{liquid} \Delta p_{liquid}}{RT})
$$

由表面张力公式，我们可以得到：

$$
\Delta p_{liquid}=\frac{2\gamma}{r}
$$

则：

$$
p_{air}=p_0\exp{\frac{2\gamma V_{liquid}}{rRT}}
$$

我们称这个公式为开尔文公式。

对于过热液体，则有：

$$
p_{air}=p_0\exp{\frac{2\gamma V_{liquid}}{rRT}}
$$

### 吉布斯相律

我们引入摩尔分数$x_i=\frac{n_i}{n}$

考虑一个包含$C$个组元的多元系统，每个组元都处于$P$个不同相中之一，则：

$$
F=C-P+2
$$

$F$为系统自由度，我们称这个为吉布斯相律

### 依数性

当一种特定物质的液体$A$溶解了另外一种物质$B$，$A$的化学势降低，导致对比纯液体，液体$A$的沸点升高且凝固点降低，这个效应称为依数性，则有：

$$
T-T^*\approx\frac{RT^{*2}}{\Delta H_{air}}x_B=K_bx_B
$$

同理对于冰点降低量

$$
T-T^*=K_{f}x_B
$$


## 玻色-爱因斯坦统计和费米-狄拉克统计

### 全同粒子的统计

对于全同粒子，有：

$$
\mathscr Z=\sum_n\exp(n\beta(\mu-E))
$$

对于费米子：

$$
f(E)=\frac{1}{\exp(\beta(E-\mu))+1}
$$


对于玻色子：

$$
f(E)=\frac{1}{\exp(\beta(E-\mu))-1}
$$

## 量子气体和凝聚

### 无相互作用的量子流体

考虑自旋为$S$的粒子，巨配分函数就是单粒子配分函数的积

$$
\mathscr{Z}=\prod_k\mathscr{Z}_k^{2S+1}
$$

则可得

$$
n_k=k_BT\frac{\partial}{\partial \mu}\mathscr{Z}_k=\frac{1}{\exp(\beta(E_k-\mu)\pm 1)}
$$

定义逸度$z=\exp(\beta \mu)$

则有：

$$
N=\frac{(2S+1)V}{(2\pi)^2}\left(\frac{2m}{\hbar^2}\right)^{3/2}\int\frac{E^{1/2\mathrm{d}E}}{z^{-1}e^{\beta E}\pm1}\\U==\frac{(2S+1)V}{(2\pi)^2}\left(\frac{2m}{\hbar^2}\right)^{3/2}\int\frac{E^{3/2\mathrm{d}E}}{z^{-1}e^{\beta E}\pm1}
$$

得：

$$
\begin{cases}N=\frac{(2S+1)V}{\lambda_{th}^3}[\mp Li_{3/2}(\mp z)]\\U=\frac32Nk_BT\frac{Li_{5/2}(\mp z)}{Li_{3/2}(\mp z)}\end{cases}
$$

### 费米气体

我们讨论费米子的气体，我们定义费米能：$E_F=\mu(T=0)$

则：

$$
n_k=\frac{1}{\exp(\beta(E_k-\mu))=\theta(E_F-E_k)}
$$

则:

$$
N=\int_0^{k_F} g(\vec{k})\mathrm d^3\vec{k}
$$

参考固体物理

### 玻色气体

$$
N=\frac{(2S+1)V}{\lambda_{th}^{3}}Li_{3/2}(z)\\U=\frac32Nk_BT\frac{Li_{5/2}(z)}{Li_{3/2}(z)}
$$

则有:

$$
\frac{n\lambda_{th}^3}{2S+1}=Li_{3/2}(z)
$$

$$
\frac{n_0}n=\frac{N-N_0}N=\frac{\frac{(2S+1)V}{\lambda_th^3(T_c)}Li_{3/2}(1)-\frac{(2S+1)V}{\lambda_th^3(T)}Li_{3/2}(1)}{\frac{(2S+1)V}{\lambda_th^3(T)}Li_{3/2}(1)}=1-\left(\frac{T}{T_c}\right)^{3/2}
$$



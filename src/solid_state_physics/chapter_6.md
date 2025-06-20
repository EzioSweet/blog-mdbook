# Chapter 6 金属自由电子论


以下是固体物理金属自由电子论部分的复习笔记

## 金属自由电子气

### 特鲁特模型

1900年，特鲁特提出金属之所以有这些共同的物理性质，是因为其中存在大量的“自由”电子。

特鲁特模型：将金属模型为由大量“自由”电子构成的气体，如同理想气体，构成这一理想气体的粒子是彼此没有相互作用的电子。

特鲁特模型是最早被用来解释金属性质的模型，但模型中有两个基本问题并没有给以清楚的交代:
+  对每个金属原子而言，其核外有多个电子，由于当时对原子结构的了解并不清晰，模型中未明确指出哪些电子参与了自由电子气的形成
+ 金属中的大量电子处在正电荷背景中，按理说正、负电荷之间以及电子与电子之间均应当存在库仑相互作用，但模型却认为金属中大量电子是处在自由运动状态

### 索末菲模型

索末菲模型：金属被看成是大量在均匀分布的正电荷背景上“自由”运动的价电子构成的自由电子气。

电子“自由”运动的范围仅因存在表面势垒而限制在金属内部

在金属内部，周期性分布的带正电荷的离子实起着保持体系电中性的均匀正电荷背景的作用

均匀分布的正电荷背景，成为价电子可在其中“自由”移动的“凝胶”，由于这一原因，自由电子气模型有时也称为凝胶模型

**两种模型共同点**：均是将金属视为由大量自由电子构成的理想气体

## 自由电子气量子理论

物理基础：
+ 金属自由电子气模型
+ 电子具有波粒二象性，其状态应由薛定谔方程给出
+ 电子作为费米子，应服从费米-狄拉克统计

### 单电子本征态及其本征能量

假设金属是一个边长为$L$的立方体，立方体内含有$N$个“自由”电子，如果金属表面势垒非常高，以至于金属内部的电子无法脱离金属，相当于将这些电子囚禁在很深的势阱中

电子气系统状态由波函数$\psi(\vec{r})$描述，遵从定态薛定谔方程：

$$\left[-\frac{\hbar^2}{2m}\nabla^2+V(\vec r)\right]\psi(\vec r)=\varepsilon\psi(\vec r)$$

按照金属自由电子气模型，金属中的电子是自由的，因此，电子的势场为常数，不凡选取为0

$$-\frac{\hbar^2}{2m}\nabla^2\psi(\vec{r})=\varepsilon\psi(\vec{r})$$

由于$N$个电子彼此间没有相互作用，多电子问题转化为单电子问题，因此，只要第$i$个电子的本征态和本征能量求得，则整个电子气系统的本征态和本征能量就可以得到

$$-\frac{\hbar^2}{2m}\nabla^2\psi_i(\vec{r})=\varepsilon_i\psi_i(\vec{r})$$

$$\psi_{\vec{k}}(\vec{r})=\frac{1}{L^{3/2}}e^{i\vec{k}\cdot\vec{r}}$$

描述的是波矢为$\vec{k}$的平面波

$$
\varepsilon(\vec{k})=\frac{\hbar^2k^2}{2m}\\
-i\hbar\nabla\psi_{\vec{k}}(\vec{r})=\hbar\vec{k}\psi_{\vec{k}}(\vec{r})
$$

### 波恩-卡门边界条件

$$
\begin{cases}\psi_{\vec{k}}(x+L,y,z)=\psi_{\vec{k}}(x,y,z)\\\psi_{\vec{k}}(x,y+L,z)=\psi_{\vec{k}}(x,y,z)\\\psi_{\vec{k}}(x,y,z+L)=\psi_{\vec{k}}(x,y,z)\end{cases}
$$

$$
\begin{gathered}
\psi_{\vec{k}}(x+L,y,z)=\psi_{\vec{k}}(x,y,z)\Rightarrow e^{ik_{x}L}=1 \Rightarrow k_{x}=\frac{2\pi}{L}n_{x} \\
\psi_{\vec{k}}(x,y+L,z)=\psi_{\vec{k}}(x,y,z)\Rightarrow e^{ik_{y}L}=1 \Rightarrow k_{y}=\frac{2\pi}{L}n_{y} \\
\psi_{\hat{k}}(x,y,z+L)=\psi_{\hat{k}}(x,y,z)\Longrightarrow e^{ik_{z}L}=1 \Rightarrow k_z=\frac{2\pi}Ln_z
\end{gathered}
$$

电子能量：

$$\varepsilon(\vec{k})=\frac{\hbar^2k^2}{2m}=\frac{\hbar^2}{2m}\times(\frac{2\pi}{L})^2\times(n_x^2+n_y^2+n_z^2)$$

### 状态密度和能态密度

因此在波矢空间可以用一个点来代表一个可能的电子状态，这个代表电子状态的点简称为状态点，沿每一个轴方向响铃的两个状态点的间隔为$\frac{2\pi}{L}$，则在波矢空间每个状态点所占的体积为：

$$\Delta\vec{k}=\frac{2\pi}L\times\frac{2\pi}L\times\frac{2\pi}L=\frac{(2\pi)^3}V$$

其倒数$\frac{V}{8\pi^3}$称为$k$空间状态密度

由：

$$\frac V{(2\pi)^3}\int\mathrm{d}k^3=\frac V{(2\pi)^3}\int_0^{2\pi}\mathrm{d}\phi\int_0^{\pi}\sin\theta\mathrm{d}\theta\int k^2\mathrm{d}k=\int\frac{Vk^2}{2\pi^2}\mathrm{d}k=\int g(k)\mathrm{d}k$$

可得$g(k)=\frac{Vk^2}{2\pi^2}$，则有能态密度：

$$g(\varepsilon)=\frac{dN}{d\varepsilon}=4\pi V(\frac{2m}{h^2})^{3/2}\varepsilon^{\frac12}$$

### 自由电子气基态及费米面

自由电子气的基态是指，$T＝0$时$N$个电子通过在状态点上“适当” 占据使得自由电子气系统具有最低能量的状态。显然能量最低的状态点对应的$k=0$

但电子是费米子，受泡利不相容原理的限制，每一个状态点上最多只能占据自旋向上和自旋向下的两个电子，意味着$N$个电子不可能都占据在$k=0$最低能量的状态点位置。

这样一来，$N$个电子只能从能量最低的$k=0$态开始，按能量从低到高，每个状态点上占据两个电子，依次占据。由于电子能量正比于波矢的平方，$N$的数目又很大，在$k$空间中占据区最后成为一个球,称作费米球，其表面称为费米面

费米面指的是，$T=0$时将$k$空间中电子占据态和没有电子占据态分开的界面。

$$ N=2\cdot\frac{V}{(2\pi)^3}\cdot\frac{4}{3}\pi(k_F^0)^3=\frac{V}{3\pi^2}(k_F^0)^3$$

费米波矢：$k_F^0=(3\pi^2n)^{1/3}$

自由电子气基态能量指费米球内所有单电子能量相加后得到的能量，即：

$$E_0=2\sum_{k<k_F^0}\frac{\hbar^2k^2}{2m}=\frac35N\varepsilon_F^0$$

其中$\varepsilon_F^0$为费米能

$$
\varepsilon_F^0=\frac{\hbar^2(k_F^0)^2}{2m}
$$

由此得到费米动量和费米速度:

$$\vec{p}_F^0=\hbar\vec{k}_F^0$$

$$\vec{v}_F^0=\frac{\hbar\vec{k}_F^0}m$$

同时还能得到费米温度：

$$T_F^0=\frac{\varepsilon_F^0}{k_B}=\frac{\hbar^2(3\pi^2n)^{\frac23}}{2mk_B}$$

由此得到自由电子气基态能量：

$$
E_0=\int_0^{\varepsilon_F^0}Eg(E)\mathrm{d}E=\frac V{2\pi^2}\left(\frac{2m}{\hbar^2}\right)^{\frac32}\int_0^{\varepsilon_F^0}E^{\frac32}\mathrm{d}E=\frac35N\varepsilon_F^0
$$

其平均能量为：

$$\bar{\boldsymbol{\varepsilon}}_0=\frac{E_0}{N}=\frac{3}{5}\boldsymbol{\varepsilon}_F^0$$

## 自由电子气激发态的量子理论

费米根据泡利不相容原理，提出电子不应当服从经典的玻尔兹曼统计，而应当服从如下的统计规律：

$$f(\varepsilon)=\frac1{e^{(\varepsilon-\mu)/k_BT}+1}$$

由于$T=0$时的化学势$\mu$实际上就是前面的基态费米能,则可将化学势理解为费米能

$$f(\varepsilon)=\frac1{e^{(\varepsilon-\varepsilon_F)/k_BT}+1}$$

由于热激发使得一些电子从费米能以下的量子态跃迁到费米能以上的量子态上，在这种情况下如何确定电子在各个量子态上的占据？
+ 满足泡利不相容原理
+ 电子在各个量子态上的占据几率

由能态密度和费米-狄拉克统计，可得：

$$
N=\int_0^\infty g(\varepsilon)f(\varepsilon)d\varepsilon
$$

由此可知费米-狄喇克分布函数实际上表示的是能量为$\varepsilon$的能级上平均电子占据数。

对自由电子气，$g(\varepsilon)=C\sqrt{\varepsilon}$，$C=4\pi V(\frac{2m}{h^2})^{3/2}$。

则分部积分后，有：

$$
\begin{aligned}\text{N}&=\frac23Cf(\varepsilon)\varepsilon^{3/2}\left|_0^\infty-\frac23C\int_0^\infty\varepsilon^{3/2}\frac{\partial f(\varepsilon)}{\partial\varepsilon}d\varepsilon\right.\\&=\int_0^\infty\frac23C\varepsilon^{3/2}(-\frac{\partial f}{\partial\varepsilon})d\varepsilon\end{aligned}
$$

令$G(\varepsilon)=\frac{2}{3}C\varepsilon^{3/2}\quad$

则:

$$
N=\int_{0}^{\infty}G(\varepsilon)(-\frac{\partial f}{\partial\varepsilon})d\varepsilon
$$

将$G$在$\varepsilon_F$附近作泰勒展开:

$$G(\varepsilon)=G(\varepsilon_{F})+(\varepsilon-\varepsilon_{F})G^{\prime}(\varepsilon)\Big|_{\varepsilon_{F}}+\frac{1}{2!}(\varepsilon-\varepsilon_{F})^{2}G^{\prime\prime}(\varepsilon)\Big|_{\varepsilon_{F}}+...$$

$$
\begin{aligned}
&N=\int_0^\infty G(\varepsilon)(-\frac{\partial f}{\partial\varepsilon})d\varepsilon=G(\varepsilon_F)\int_0^\infty(-\frac{\partial f}{\partial\varepsilon})d\varepsilon \\
&+G'(\varepsilon_{F})\int_{0}^{\infty}(\varepsilon-\varepsilon_{F})(-\frac{\partial f}{\partial\varepsilon})d\varepsilon +\frac{1}{2!}G''(\varepsilon_{F})\int_{0}^{\infty}(\varepsilon-\varepsilon_{F})^{2}(-\frac{\partial f}{\partial\varepsilon})d\varepsilon+... \\
&=I_0G(\varepsilon_F)+I_1G^{^{\prime}}(\varepsilon_F)+I_2G^{^{\prime\prime}}(\varepsilon_F)+...
\end{aligned}
$$

$$
\begin{aligned}\boldsymbol{\varepsilon}_{F}&=\frac{\boldsymbol{\varepsilon}_F^0}{\left[1+\frac{\pi^2}8\left(k_BT/\varepsilon_F\right)^2\right]^{2/3}}\approx\frac{\boldsymbol{\varepsilon}_F^0}{\left[1+\frac{\pi^2}8\left(k_BT/\varepsilon_F^0\right)^2\right]^{2/3}}\\&\approx\varepsilon_F^0[1-\frac{\pi^2}{12}(k_BT/\varepsilon_F^0)^2]\end{aligned}
$$

对于自由电子气，费米面是球面。温度升高，费米球收缩，这是由于费 米面以内能量离 $\varepsilon_F$ 约 $k_B T$ 范围的能级上的电子被热激发到 $\varepsilon_F$ 之上约 $k_B T$ 范围的较高能级上。

## 电子比热

+ 经典理论:得到的电子比热是温度无关的量，电子比热在数值上和晶格比热是同一量级
+ 特鲁特模型：金属内部的自由电子是经典粒子， 且服从玻尔兹曼分布
+ 索末菲模型：金属内部的自由电子具有波动性，其状态由薛 定谔方程给出，不同能级上电子占据几率由费米分布函数确定

按照索末菲量子理论，对$N$个电子构成的自由电子气系统，激发态的总能量：

$$
E=\frac{3}{5}N\varepsilon_{F}^{0}\left[1+\frac{5\pi^{2}}{12}\Big(k_{B}T / \varepsilon_{F}^{0}\Big)^{2}\right]\\=\frac35N\boldsymbol{\varepsilon}_F^0+\frac{\pi^2}4Nk_BT\Bigg(\frac{k_BT}{\boldsymbol{\varepsilon}_F^0}\Bigg)
$$

第一项是基态电子的平均能量，第二项的电子受热激发而对系统能量的贡献。热激发电子占总电子数的比例近似为$\frac{k_BT}{\varepsilon_F^0}$

则可得自由电子气系统的电子比热：

$$
C_V^e=\frac{\partial E}{\partial T}=\frac{\pi^2}2Nk_B\left(\frac{k_BT}{\varepsilon_F^0}\right)
$$

只有费米面附近约 $k_B T$能量范围内的电子因热激发跃迁到较高能级的那部分电子才参与了对比热的贡献。
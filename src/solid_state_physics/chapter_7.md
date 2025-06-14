# Chapter 7 固体能带论


以下是固体能带论相关知识

## 固体能带论的理论基础

固体由大量周期性排列的原子构成，固体能带理论的主要任务就是用量子力学研究在大量带正电、周期性排列的离子实背景中价电子的运动状态，包括电子的本征能量和本征函数等。

这原本是一个复杂的多体问题，但在经过适当的近似处理后，可以将如此复杂的多体问题转化为一个在周期势场中运动的单电子问题。

### 哈密顿算符

如果要用量子力学理论来处理电子的状态（包括电子能量和描述状态的波函数），首先要知道电子所在系统的哈米顿算符。

设体积$V=L^3$的固体内含有$N$个原子，每个原子有$Z$个价电子，则整个系统共有$NZ$个电子。

失去价电子后的原子在固体中称为离子实，每个离子实具有$Ze$的正电荷，整个系统共有$N$个带正电荷的离子实

整个系统由$N$个周期性分布的带正电荷的离子实和运动于其中的$NZ$个带负电荷的电子构成

则系统的哈密顿量包括：

+ $NZ$个价电子的动能
+ $NZ$个价电子的库仑作用能
+ $N$个离子实的动能
+ $N$个离子实的库仑作用能
+ 离子实和电子之间的库仑作用能

即：

$$
H=-\sum_{i=1}^{NZ}\frac{\hbar^{2}}{2m}\nabla_{i}^{2}+\frac{1}{2}\sum_{i\neq j}\frac{1}{4\pi\varepsilon_{0}}\frac{e^{2}}{|\vec{r}_{i}-\vec{r}_{j}|}-\sum_{n=1}^{N}\frac{\hbar^{2}}{2M}\nabla_{n}^{2}+\frac{1}{2}\sum_{n\neq m}\frac{1}{4\pi\varepsilon_{0}}\frac{Z^{2}e^{2}}{|\vec{R}_{n}-\vec{R}_{m}|}-\sum_{i=1}^{NZ}\sum_{n=1}^{N}\frac{1}{4\pi\varepsilon_{0}}\frac{Ze^{2}}{|\vec{r}_{i}-\vec{R}_{n}|}
$$

但是这个方程在现实生活中几乎不可求解，因此我们做了一些假设，来使这个方程可解：

### 绝热近似

如果把大量电子构成的系统看作为一个热力学系统，当这样的热力学系统与周期性分布的离子实之间的热交换可忽略时，则可近似认为电子能绝热于离子实的运动，这便是所谓的玻恩-奥本海姆近似 ，简称绝热近似

玻恩-奥本海姆近似基于两个事实：
+ 固体中电子质量远小于离子实的质量
+ 电子运动速率远快于离子实的运动速率

这意味着电子可近似认为是绝热于离子实的运动，以至于可将电子与离子实的运动分开处理，因此，当我们只关注电子体系的运动时，可以认为$N$个离子实固定在各自的瞬时位置

在绝热近似下，有：

$$
H_e=-\sum_{i=1}^{NZ}\frac{\hbar^2}{2m}\nabla_i^2+\frac12\sum_{i\neq j}\frac1{4\pi\varepsilon_0}\frac{e^2}{|\vec{r}_i-\vec{r}_j|}-\sum_{i=1}^{NZ}\sum_{n=1}^N\frac1{4\pi\varepsilon_0}\frac{Ze^2}{|\vec{r}_i-\vec{R}_n|}
$$

通过绝热近似，将$(N+NZ)$体问题变成了$NZ$体问题

### 平均场近似

在经过绝热近似之后，问题得到了一定的简化，但是由于涉及到不同电子的坐标，因此，每个电子的运动都要受到其它电子运动的牵连，或者说，由于库仑关联项的存在，电子的运动彼此是相互关联的。 

库仑关联量可以用一个场来描述：

$$
V_e(r_i,r_j)=\frac12\sum_{j\neq i}^{\prime}\frac1{4\pi\varepsilon_0}\frac{e^2}{\left|r_i-r_j\right|}
$$

但是我们能否引入一个平均场$\upsilon_{e}(r_{i})$来代替库仑关联场？

经过平均场近似，对于一个电子，有：

$$
H_{ei}=-\frac{\hbar^2}{2m}\nabla_i^2+v_e(\vec{r}_i)-\sum_{n=1}^N\frac1{4\pi\varepsilon_0}\frac{Ze^2}{|\vec{r}_i-\vec{R}_n|}
$$

则NZ个电子的薛定谔方程可写作：

$$
\sum_{i=1}^{NZ}\hat{H}_{ei}\psi(\vec{r}_{1,}\vec{r}_{2,}...\vec{r}_{NZ})=\varepsilon\psi(\vec{r}_{1,}\vec{r}_{2,}...\vec{r}_{NZ})
$$

$$
\varepsilon=\varepsilon_1+\varepsilon_2+...\varepsilon_{NZ}=\sum_{i=1}^{NZ}\varepsilon_i
$$

这样便简化为了单电子问题，因此平均场近似有称为单电子近似。

### 周期性势场

在经过绝热近似和平均场近似，将原先的问题转换为单电子问题，则求解

$$
[-\frac{\hbar^2}{2m}\nabla_i^2+\nu_e(\vec{r}_i)-\sum_{n=1}^N\frac1{4\pi\varepsilon_0}\frac{Ze^2}{\left|\vec{r}_i-\vec{R}_n\right|}]\psi_i(\vec{r}_i)=\varepsilon_i\psi_i(\vec{r}_i)
$$

便可得到整个体系的本征能量和本征态。

对于单电子:

$$
H_e=-\frac{\hbar^2}{2m}\nabla^2+v_e(\vec r)-\sum_{n=1}^N\frac1{4\pi\varepsilon_0}\frac{Ze^2}{|\vec r-\vec R_n|}=-\frac{\hbar^2}{2m}\nabla^2+V(\vec r)
$$

单电子势应当具有和晶格相同的周期性：

$$
V(\vec{r}+\vec{R}_l)=V(\vec{r})
$$

## 布洛赫定理

布洛赫从理论上证明，对于周期性势场中运动的电子，其薛定谔方程的本征函数必然是按照晶格周期函数调幅的平面波的形式，并使单电子能谱呈能带结构。

$$
\begin{aligned}
&\psi_k(\vec{r})=e^{i\vec{k}\bullet\vec{r}}u_k(\vec{r}) \\
&u_k(\vec{r}+\vec{R}_m)=u_k(\vec{r})
\end{aligned}
$$

### 平移操作算符

对任意函数$f(\vec{r})$,经平移对称操作 $\hat{T}_{\bar{R}}$ 后，得到的结果 和该函数在$\vec{r}+\vec{R}$处的结果相同，即：

$$
\hat{T_R}f(\vec{r})=f(\vec{r}+\vec{R})
$$

平移操作前、后平移操作算符的本征函数只差一个常数，这个常数正好是平移操作算符的本征值。即

$$f(\vec{r}+\vec{R})=\lambda_{\vec{R}}f(\vec{r})$$

则根据前面的定义，有

$$\hat{T}_{\vec{R}_i}V(\vec{r})=V(\vec{r})$$

$$\hat{T}_{\bar{R}_{j}}\psi(\vec{r})=\hat{T}_{l_{3}\bar{a}_{3}}\hat{T}_{l_{2}\bar{a}_{2}}\hat{T}_{l_{1}\bar{a}_{1}}\psi(\vec{r})=e^{i2\pi(l_{1}\frac{t_{1}}{N_{1}}+l_{2}\frac{t_{2}}{N_{2}}+l_{3}\frac{t_{3}}{N_{3}})}\psi(\vec{r})$$

根据正、倒格子基矢的关系，在倒格子空间中可描述为：

$$\hat{T}_{\vec{R}_l}\psi(\vec{r})=e^{i\vec{k}\bullet\vec{R}_l}\psi(\vec{r})$$

### 布洛赫定理

如上面的表述:

$$
\psi_{\vec{k}}(\vec{r})=e^{i\vec{k}\bullet\vec{r}}u_{\vec{k}}(\vec{r})
$$

对周期性势场，则单电子$S$方程$\left[-\frac{\hbar^2}{2m}\nabla^2+V(\vec{r})\right]\psi=\varepsilon\psi $的本征函数取布洛赫波函数的形式

**推论**:$\psi_k(\vec{r}+\vec{R}_l)=e^{i\vec{k}\cdot\vec{R}_l}\psi_k(\vec{r})$

对于用平面波表述的自由电子$\hbar\vec{k}$是电子的动量，即$\vec{k}$为电子的波矢，是标志电子在具有平移对称性的周期场中不同状态的量子数。

### 波矢$\vec{k}$的取值

以$(\vec{a}_1,\vec{a}_2,\vec{a}_3)$ 为基矢的正格子空间的格矢 $\vec{R}_l$可表示为

$$
\vec{R}_l=l_1\vec{a}_1+l_2\vec{a}_2+l_3\vec{a}_3\quad(l_i=0,\pm1,\pm2....)
$$

倒格矢可表示为：

$$
\vec{K}_h=h_1\vec{b}_1+h_2\vec{b}_2+h_3\vec{b}_3\quad(h_i=0,\pm1,\pm2....)
$$

由：

$$-\frac{b_j}2<k_j\leq\frac{b_j}2$$

$$\vec{k}=\frac{l_1}{N_1}\vec{b}_1+\frac{l_2}{N_2}\vec{b}_2+\frac{l_3}{N_3}\vec{b}_3$$

则

$$
-\frac{N_j}2<l_j\leq\frac{N_j}2
$$

则在每个方向上，均有$N_j$个取值，$N=N_1N_2N_3$

## 近自由电子近似

对于处在和晶格相同周期性的势场中运动的电子，其波函数具有布洛赫波函数的形式并使电子能谱呈能带结构，近自由电子情况，这是能带理论中一个最简单的模型，模型的基本出发点是假设电子所感受到的势场V随空间位置的变化不大以至于其空间起伏$\Delta V=V-V_0$可看作是对自由电子（势场为常数）情形的微扰。

$$
V=V_0+\sum_{n\neq0}V_ne^{iK_nx}
$$

零级近似的波函数和能量：

$$
\psi_{k}^{(0)}=\frac{1}{\sqrt{L}}e^{ikx}\quad \varepsilon_{k}^{(0)}=\frac{\hbar^2k^2}{2m}
$$

能量的一、二级修正：

$$
\varepsilon_k^{(1)}=0\\
\varepsilon_k^{(2)}=\sum_{k\neq k^{\prime}}\frac{\left|H_{kk^{\prime}}^{\prime}\right|^2}{\varepsilon_k^{(0)}-\varepsilon_{k^{\prime}}^{(0)}}=\sum_{n\neq0}\frac{\left|V_n\right|^2}{\frac{\hbar^2}{2m}[k^2-(k-\frac{2\pi n}a)^2]}
$$

波函数一级修正：

$$
\psi_{k}\approx\frac{1}{\sqrt{L}}e^{jk}+\sum_{n=0}\frac{V_{n}}{\frac{\hbar^{2}}{2m}[k^{2}-(k-\frac{2\pi n}{a})^{2}]}\frac{1}{\sqrt{L}}e^{i(k-\frac{2\pi n}{a})i}=\frac{1}{\sqrt{L}}e^{jk}\left\{1+\sum_{n=0}\frac{V_{n}}{\frac{\hbar^{2}}{2m}[k^{2}-(k-\frac{2\pi n}{a})^{2}]}e^{-i\frac{2\pi n}{a}i}\right\}
$$

$$
\psi_k(x)=\frac{1}{\sqrt{L}}e^{ikx}+\frac{1}{\sqrt{L}}\sum_{n\neq0}\frac{V_n}{\frac{\hbar^2}{2m}\left[k^2-\left(k-\frac{2\pi n}{a}\right)^2\right]}e^{i\left(k-\frac{2\pi n}{a}\right)x}
$$

近似波函数由两种波函数迭加而成:
1. 波矢为$k$的行进平面波
2. 行进平面波因受周期场作用而产生的各散射分波之和 

## 布洛赫电子的运动速度和有效质量

固体的物理性质涉及到布洛赫电子的运动，因此需要知道布洛赫电子的运动速度和质量与能带函数之间的关系。

由于处于$\psi_{k}$态中的电子没有确定的速度，故只能计算平均速度

$$
\begin{aligned}
\vec{\nu}(\vec{k})& =\frac{-i\hbar}{m}\int\psi_{k}^{*}\nabla\psi_{k}d\tau  \\
&=\frac{-i\hbar}m\int e^{-i\vec{k}\bullet\vec{r}}u_{\vec{k}}^*e^{i\vec{k}\cdot\vec{r}}(i\vec{k}u_{\vec{k}}+\nabla u_{\vec{k}})d\tau \\
&=\frac{\hbar}{m}\int u_{\vec{k}}^{*}(-i\nabla+\vec{k})u_{\vec{k}}d\tau
\end{aligned}
$$

本部分下面的速度均为平均速度

$$\vec{\nu}_n(\vec{k})=\frac1\hbar\nabla_k\varepsilon_n(\vec{k})$$

布洛赫电子的有效质量是一个二阶张量：

$$(\frac1{m^*})_{\alpha\beta}=\frac1{\hbar^2}\frac{\partial^2\varepsilon(\vec{k})}{\partial k_\alpha\partial k_\beta}$$

$$
\begin{gathered}\frac{1}{m^{*}}=\frac{1}{\hbar^{2}}\begin{bmatrix}\frac{\partial^{2}\varepsilon}{\partial k_{x}^{2}}&\frac{\partial^{2}\varepsilon}{\partial k_{x}\partial k_{y}}&\frac{\partial^{2}\varepsilon}{\partial k_{x}\partial k_{z}}\\\frac{\partial^{2}\varepsilon}{\partial k_{y}\partial k_{x}}&\frac{\partial^{2}\varepsilon}{\partial k_{y}^{2}}&\frac{\partial^{2}\varepsilon}{\partial k_{y}\partial k_{z}}\\\frac{\partial^{2}\varepsilon}{\partial k_{z}\partial k_{x}}&\frac{\partial^{2}\varepsilon}{\partial k_{z}\partial k_{y}}&\frac{\partial^{2}\varepsilon}{\partial k_{z}^{2}}\end{bmatrix}\end{gathered}
$$

## 金属、半金属、半导体、绝缘体的能带论解释

不同的能带结构导致不同的导电性质。

电子是携带电荷的粒子，因此，只要电子运动就会产生电流，第$n$能带中处在 $\vec{k}$ 态的电子，当以速度 $\vec{\nu}_n(\vec{k})$ 运动时，对电流密度的贡献为$-e\vec{\nu}_n(\vec{k})$。

$$\vec J_n=(-e)\int\vec\nu_n(\vec k)dN$$

满带情况下，不管是否外加电场均没有电流产生，即满带不导电。

未满带情况下，如果没有外加电场则没有电流产生，当外加电场时则有电流产生，即未满能带外加电场会导电。

**判断原则**:
+ 能带间无重叠：如一价碱金属 (Na)，价带半满，属于良导体
+ 能带间重叠：二价碱土金属 (Mg)，因能带交叠，使得上下两能带均为电子部分占据的能带，故也是良导体。
+ 能带与能级非一一对应：元素半导体 (Si, Ge)，s 能带和 p 能带的显著重叠导致晶体能带发生强烈变化，以至于分裂成满带和空带的两个子能带，使得 Si、Ge 等晶体呈现半导体型能带结构。

## 紧束缚法

简单来说:

$$\varepsilon_s(\vec{k})=\varepsilon_s^{\mathrm{at}}-J(0)-\sum_m^\text{最近邻}J(\vec{R}_m)e^{i\vec{k}\cdot\vec{R}_m}$$

### 简单立方晶体的紧束缚法：

$$
\begin{aligned}
\varepsilon_{s}(\vec{k})&=\varepsilon_s^{\mathrm{at}}-J(0)-J\left(e^{ik_xa}+e^{-ik_xa}+e^{ik_ya}+e^{-ik_ya}+e^{ik_za}+e^{-ik_za}\right) \\
&=\varepsilon_s^{\mathrm{at}}-J(0)-2J\left(\cos k_xa+\cos k_ya+\cos k_za\right)
\end{aligned}
$$

$\vec{k}=(0,0,0)\to$能量最低，$\vec{k}=(\frac\pi a,\frac\pi a,\frac\pi a)$能量最高

$$
\varepsilon_{s,\min}=\varepsilon_s^{\mathrm{at}}-J(0)-6J\\
\varepsilon_{s,\max}=\varepsilon_s^{\mathrm{at}}-J(0)+6J
$$

$$\frac{\partial^2\varepsilon}{\partial k_x^2}=2Ja^2\cos k_xa\quad\frac{\partial^2\varepsilon}{\partial k_y^2}=2Ja^2\cos k_ya\quad\frac{\partial^2\varepsilon}{\partial k_z^2}=2Ja^2\cos k_za$$
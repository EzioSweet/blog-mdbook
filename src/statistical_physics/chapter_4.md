# Chapter 4 热力学第一定律

## 能量

### 一些定义

+ 热平衡系统：处于热平衡的一个系统，如果有一组特定的宏观观测量，则称该系统处于一个特定的平衡态
+ 态函数：如果一个系统的一些宏观可观测性质具有固定且明确的值，而与它们如何到达这些值的过程无关，我们称这些性质为态函数

### 热力学第一定律

热力学第一定律：能量是守恒的，热量和功均是能量形式

内能：系统具有的所有内部自由度相关的能量之和

$$
\mathrm{d}U=\mathrm{d}Q+\mathrm{d}W
$$

则做功为：

$$
\mathrm dW=-p\mathrm dV
$$

### 热容

$U=U(T,V)$，则:

$$
\mathrm{d}U=\left(\frac{\partial U}{\partial T}\right)_V\mathrm{d}T+\left(\frac{\partial U}{\partial V}\right)_T\mathrm{d}V
$$

则：

$$
\mathrm{d}Q=\left(\frac{\partial U}{\partial T}\right)_{V}\mathrm{d}T+\left[\left(\frac{\partial U}{\partial V}\right)_{T}+p\right]\mathrm{d}V\\\frac{\mathrm{d}Q}{\mathrm{d}T}=\left(\frac{\partial U}{\partial T}\right)_{V}+\left[\left(\frac{\partial U}{\partial V}\right)_{T}+p\right]\frac{\mathrm{d}V}{\mathrm{d}T}
$$

上式对于$T$或$V$的任何变化都成立，但是我们往往考虑等容或等压过程，在等容条件下：

$$
C_V=\left(\frac{\partial Q}{\partial T}\right)_V=\left(\frac{\partial U}{\partial T}\right)_V
$$

在等压条件下：

$$
C_p=\left(\frac{\partial Q}{\partial T}\right)_p=\left(\frac{\partial U}{\partial T}\right)_V+\left[\left(\frac{\partial U}{\partial V}\right)_T+p\right]\left(\frac{\partial V}{\partial T}\right)_p
$$

定义绝热指数：

$$\gamma=\frac{C_p}{C_V}$$

在单原子理想气体的情况下：

$$
C_V=\frac32R\\
C_p=\frac52R\\
\gamma = \frac53
$$

## 等温和绝热过程

可逆过程：在热力学中，可逆过程是指一种理想化的过程，其中系统和环境在整个过程中都能够保持平衡，并且在任何阶段都可以通过微小的变化逆转，使系统和环境返回到初始状态。换句话说，在可逆过程中，系统在每个步骤上都无限接近于平衡状态，因此过程中没有不可逆的损失或熵的增加。

准静态过程：准静态过程是系统以无限慢的速度经历的一系列平衡状态的过程。在这个过程中，系统在任何时刻都可以被认为处于热力学平衡状态。

### 等温膨胀

在等温过程中，名副其实，$\Delta T=0$

由$\mathrm{d}U=C_V\mathrm{d}T$，得

$$\Delta U = 0$$

因此

$$
\Delta Q = -\int \mathrm{d}W=RT\ln\frac{V_2}{V_1}
$$

### 绝热膨胀

我们认为绝热过程$\mathrm{d}Q=0$，则$\mathrm{d}U=\mathrm{d}W$

则

$$
C_V\mathrm dT=-\frac{RT}{V}\mathrm dV\\
\ln\frac{T_2}{T_1}=\frac{R}{C_V}\ln\frac{V_2}{V_1}
$$

由$C_p=C_V+R$，得

$$
p^{1-\gamma}T^{\gamma}=\text{const}\\
TV^{\gamma-1}=\text{const}\\
pV^{\gamma}=\text{const}
$$

### 绝热大气

厚度为d$z$，密度为$\rho$的大气，有：

$$\mathrm{d}p=-\rho g \mathrm{d}z$$

则

$$
T\frac{\mathrm{d}p}{p}=-\frac{mg}{k_B}\mathrm{d}z
$$

$$
\frac{\mathrm{d}T}{\mathrm{d}z}=-\biggl(\frac{\gamma-1}{\gamma}\biggr)\frac{mg}{k_B}
$$


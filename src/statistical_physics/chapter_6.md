# Chapter 6 热力学的应用

## 热力学势

### 内能

在前面，我们把热力学第一定律写作：

$$\mathrm{d}U=T\mathrm{d}S-p\mathrm{d}V$$

我们定义$U$为系统的内能，我们由上式能得到，$U=U(S,V)$，则：

$$
T=\left(\frac{\partial U}{\partial S}\right)_V\\
p=-\left(\frac{\partial U}{\partial V}  \right)_S
$$

### 焓

焓是系统的内能加上系统在外界压强下做功所需的能量。这个定义使得在恒压过程中，焓的变化可以直接对应于系统的热量交换。

我们定义系统的焓：

$$
H=U+pV
$$

则有：

$$
\begin{aligned}\mathrm{d}H&=T\mathrm{d}S-p\mathrm{d}V+p\mathrm{d}V+V\mathrm{d}p\\&=T\mathrm{d}S+V\mathrm{d}p\end{aligned}
$$

能够得到：

$$
T=\left(\frac{\partial H}{\partial S}\right)_p\\V=\left(\frac{\partial H}{\partial p}\right)_S
$$

我们常在等压环境中研究

### 亥姆霍兹函数

亥姆霍兹自由能的物理意义在于，它表示了在恒定体积和温度条件下，系统能对外界做的最大功。也就是说，当一个系统从一个状态变化到另一个状态时，亥姆霍兹自由能的变化量等于系统在恒定体积和温度条件下可以对外界做的最大功。

我们定义系统的亥姆霍兹函数：

$$
F=U-TS
$$

则有：

$$
\begin{gathered}
\mathrm{d}F =-S\mathrm{d}T-p\mathrm{d}V \\
S=-\left(\frac{\partial F}{\partial T}\right)_{V} \\
p=-\left(\frac{\partial F}{\partial V}\right)_{T} 
\end{gathered}
$$

我们常在研究等温过程中重点研究

### 吉布斯函数

吉布斯函数（Gibbs function），又称吉布斯自由能（Gibbs free energy），是热力学中的一个重要状态函数，用来描述系统在恒定温度和恒定压力下的自发过程和相平衡。

我们定义吉布斯函数：

$$G=H-TS$$

则有：

$$
\begin{gathered}
\text{dG} =-S\mathrm{d}T+V\mathrm{d}p \\
S=-\left(\frac{\partial G}{\partial T}\right)_{p} \\
V=\left(\frac{\partial G}{\partial p}\right)_{T} 
\end{gathered}
$$

### 麦克斯韦关系

我们知道对于：

$$\mathrm{d}z=f\mathrm{d}x+g\mathrm{d}y$$

有：

$$
\frac{\partial f}{\partial y}=\frac{\partial g}{\partial x}
$$

则根据上面几个的表达式，得到麦克斯韦关系：

$$
\begin{gathered}
\left(\frac{\partial T}{\partial V}\right)_{s} =-\left(\frac{\partial p}{\partial S}\right)_V \\
\left(\frac{\partial T}{\partial p}\right)_{S} =\left(\frac{\partial V}{\partial S}\right)_p \\
\left(\frac{\partial S}{\partial V}\right)_{T}=\left(\frac{\partial p}{\partial T}\right)_{V} \\
\left(\frac{\partial S}{\partial p}\right)_{T}=-\left(\frac{\partial V}{\partial T}\right)_{p} 
\end{gathered}
$$

我们还有如下恒等式：

互反定理：

$$
\left(\frac{\partial x}{\partial y}\right)_z = -\left( \frac{\partial x}{\partial z} \right)_y\left(\frac{\partial z}{\partial y}\right)_x
$$

由此我们能够得到热容：

$$
\frac{C_V}{T}=\left(\frac{\partial S}{\partial T}\right)_V \quad \& \quad  \frac{C_p}{T}=\left(\frac{\partial S}{\partial T}\right)_p
$$


## 细杆、气泡、磁体

以下是我们将热力学应用于宏观系统

### 弹性杆

考虑一根长度为$L$，横截面积为$A$的杆，维持温度为$T$，这个杆由弹性材料构成，我们定义用协变$\epsilon=$d$L/L$和协强$\sigma=$d$f/A$之比等温杨氏模量

$$E_T=\frac{L}{A}\left( \frac{\partial f}{\partial L} \right)_T$$

定义等张力线胀率：$\alpha_f=\frac1L\left(\frac{\partial L}{\partial T}\right)_f$

利用热力学第一定律，

$$\left(\frac{\partial S}{\partial L}\right)_T=-\left(\frac{\partial f}{\partial T}\right)_L=\left(\frac{\partial f}{\partial L}\right)_T\left(\frac{\partial L}{\partial T}\right)_f=AE_T\alpha_f$$

### 气泡的表面张力

对于一个气泡，其表面面积改变所需的功为:

$$
\mathrm dW=\gamma\mathrm dA
$$

其中$\gamma$即为表面张力

$$\mathrm dF=-S\mathrm dT+\gamma\mathrm dA$$

则：

$$p=\frac{2\gamma}{r}$$

$p$为内外大气压差值，$r$为气泡半径

### 磁体

$$\mathrm dU = T\mathrm dS -m \mathrm dB$$

其中$m$为磁矩，$B$为磁场，

## 热力学第三定律

### 热力学第三定律的不同表述

+ 能斯特表述：接近绝对零度时，处于内平衡的一个系统中的所有反应发生时熵不变
+ 普朗克表述：处于内平衡的所有系统的熵在绝对零度时是相同的，可以取为0
+ 西蒙表述：处于热力学内平衡的系统的每个方面对系统熵的共线随着$T\to 0$K而趋于0
+ 不可达性：不可能经过有限的步骤到达绝对零度

### 推论

+ 随着$T\to 0$，热容趋于0
+ 绝对零度热膨胀停止
+ 绝对零度附近没有理想气体
+ 绝对零度时居里定律失效


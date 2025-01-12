### Quench晶格后关联函数的振荡

实验中晶格阱深先$40\mathrm{ms}$升至$6.25E_r$，相互作用$U/t=2\sim20$，再将晶格瞬间（近似约$30\mu\mathrm{s}$）内升至$20E_r$，测量在$20E_r$下保持晶格不同时间后的动量分布，观察到了干涉对比度随保持时间的振荡行为。下面先介绍实验的观测量关联函数与准动量分布间的关系，再推导出关联函数在$quench$后的演化。

#### 关联函数与准动量分布

三维准动量分布$S(\boldsymbol{k})=\langle a^\dagger_{\boldsymbol{k}}a_{\boldsymbol{k}}\rangle$表示在准动量$\boldsymbol{k}$上的占据数。准动量算符$a^\dagger_{\boldsymbol{k}}$可以展开到晶格格点的产生与湮灭算符上（这里为了书写方便忽略算符的自旋指标）：
$$
a^{\dagger}_{\boldsymbol{k}}=\frac{1}{\sqrt{L^3}}\sum_l e^{-i\boldsymbol{k}\cdot\boldsymbol{R}_l}a^{\dagger}_l
$$
其中$L^3$为三维晶格的格点数，对$l$的求和遍历所有格点。则三维准动量可以表示为
$$
S(\boldsymbol{k})=\langle a^\dagger_{\boldsymbol{k}}a_{\boldsymbol{k}}\rangle=\frac{1}{L^3}\sum_{l,m}e^{-i\boldsymbol{k}(\boldsymbol{R}_l-\boldsymbol{R}_m)}\langle \hat a^{\dagger}_l\hat a_m\rangle
$$
我们定义一维准动量分布为
$$
S_{1\mathrm{d}}(k_x) = \int_{-k_\mathrm{lat}}^{k_\mathrm{lat}}\int_{-k_\mathrm{lat}}^{k_\mathrm{lat}}S(k_x,k_y,k_z)\mathrm{d}k_y\mathrm{d}k_z
$$
其中$k_\mathrm{lat}=\frac{2\pi}{\lambda}=\frac{\pi}{a}$，$\lambda$为晶格光波长，$a$为晶格常数，即对$k_y$与$k_z$方向的积分限制在第一布里渊区。我们将准动量算符在格点产生与湮灭算符上展开，得
$$
\begin{aligned}
S_{\mathrm{1d}}(k_x)&=\int^{k_\mathrm{lat}}_{-k_\mathrm{lat}}\int^{k_\mathrm{lat}}_{-k_\mathrm{lat}}S(k_x,k_y,k_z)\mathrm{d}k_y\mathrm{d}k_z\\
&=\frac{1}{L^3}\int^{k_\mathrm{lat}}_{-k_\mathrm{lat}}\int^{k_\mathrm{lat}}_{-k_\mathrm{lat}}\sum_{lm}e^{-ik_x(x_l-x_m)-ik_y(y_l-y_m)-ik_z(z_l-z_m)}\langle \hat{a}^\dagger_l\hat{a}_m\rangle\mathrm{d}k_y\mathrm{d}k_z\\
&=\frac{1}{L^3}\sum_{lm}\int^{k_\mathrm{lat}}_{-k_\mathrm{lat}}e^{-ik_x(x_l-x_m)-ik_y(y_l-y_m)}\langle \hat{a}^\dagger_l\hat{a}_m\rangle\mathrm{d}k_y\int^{k_\mathrm{lat}}_{-k_\mathrm{lat}}e^{-ik_z(z_l-z_m)}\mathrm{d}k_z
\end{aligned}
$$
交换对$k_y,k_z$积分与对格点$l,m$求和的顺序，我们得到先对$k_z$积分的表达式$\int^{k_\mathrm{lat}}_{-k_\mathrm{lat}}e^{-ik_z(z_l-z_m)}\mathrm{d}k_z$。格点$l,m$沿$z$方向的坐标之差$z_l-z_m=0,a,2a,\cdots$为晶格常数的整倍数。因此对$k_z$在$[-\pi/a,\pi/a]$范围内积分，只有当$z_l-z_m=0$时积分等于不为零的常数$2\pi/a$，即$\int^{k_\mathrm{lat}}_{-k_\mathrm{lat}}e^{-ik_z(z_l-z_m)}\mathrm{d}k_z=\frac{2\pi}{a}\delta_{z_lz_m}$。同理对$k_y$的积分给出$\int^{k_\mathrm{lat}}_{-k_\mathrm{lat}}e^{-ik_y(y_l-y_m)}\mathrm{d}k_y=\frac{2\pi}{a}\delta_{y_ly_m}$。考虑晶格的平移对称性与周期性边界条件，最终对格点$l,m$的求和可以简化为
$$
\begin{aligned}
S_{\mathrm{1d}}(k_x) &= \frac{1}{L^3}\sum_{lm}e^{-ik_x(x_l-x_m)}\langle\hat{a}^\dagger_l\hat{a}_m\rangle(2\pi/a)^2\delta_{y_ly_m}\delta_{z_lz_m}\\
&=(2\pi/a)^2\sum_{n=0}^{L}\cos(nk_xa)\langle\hat{a}^\dagger_i\hat{a}_{i+n}\rangle
\end{aligned}
$$
其中，所有的$i+n$格点构成一条一维链。我们定义一维准动量分布的中心峰值$S_\mathrm{peak}$为
$$
\begin{aligned}
S_\mathrm{peak} &= S_{1\mathrm{d}}(k_x=0)=(2\pi/a)^2\sum_{n=0}^{L}\langle\hat{a}^\dagger_i\hat{a}_{i+n}\rangle \\
&=(2\pi/a)^2\left(\langle\hat{a}^\dagger_i\hat{a}_{i}\rangle+\langle\hat{a}^\dagger_i\hat{a}_{i+1}\rangle+\langle\hat{a}^\dagger_i\hat{a}_{i+2}\rangle+\cdots\right)
\end{aligned}
$$
即实验的观测量，一维准动量分布的中心峰值$S_\mathrm{peak}$，对应了体系的关联函数。

#### 关联函数的含时演化

实验观测到了在$quench$后在准动量分布上的振荡。公式(6)的第一项为$\langle\hat{a}^\dagger_{i\sigma}\hat{a}_{i\sigma}\rangle=n_\sigma$为自旋$\sigma$原子在晶格中的填充数，其在$quench$后保持不变，因此中心峰值$S_\mathrm{peak}$的振荡由非局域的关联函数振荡产生。我们考虑初态$\psi_0$在末态哈密顿量$H=\sum_lUn_{l\sigma}n_{l\bar{\sigma}}$下的演化（忽略$20E_r$下的隧穿项），则演化时间$t$后，关联函数$\langle a_{i\sigma}^\dagger a_{j\sigma}\rangle_{i\ne j}$的取值可以表示为（$\hbar=1$）：
$$
\langle \psi(t)| a^\dagger_{i\sigma}a_{j\sigma}|\psi(t)\rangle = \langle \psi_0|e^{iHt}a^\dagger_{i\sigma}a_{j\sigma}e^{-iHt}|\psi_0\rangle
$$
末态哈密顿量$H=\sum_lUn_{l\sigma}n_{l\bar{\sigma}}$可以分成两项$H = H_{i,j}+H_{l\ne i,j}$：一项$H_{i,j}=U n_{i\sigma}n_{i\bar{\sigma}}+n_{j\sigma}n_{j\bar{\sigma}}$与算符$a^\dagger_{i\sigma}a_{j\sigma}$不对易，另一项$$H_{l\ne i,j}=\sum_{l\ne i,j}Un_{l\sigma}n_{l\bar{\sigma}}$$与之对易。对易的部分可以通过与$a^\dagger_{i\sigma}a_{j\sigma}$交换顺序而约去。$i$格点的相互作用哈密顿量与$j$格点算符对易，因此我们可以将演化算符进一步拆开，从而关联函数$\langle a_{i\sigma}^\dagger a_{j\sigma}\rangle_{i\ne j}$的取值可以表示成：
$$
\begin{aligned}
\langle \psi(t)| a^\dagger_{i\sigma}a_{j\sigma}|\psi(t)\rangle &= \langle \psi_0|e^{i(U n_{i\sigma}n_{i\bar{\sigma}}+n_{j\sigma}n_{j\bar{\sigma}})t}a^\dagger_{i\sigma}a_{j\sigma}e^{-i(U n_{i\sigma}n_{i\bar{\sigma}}+n_{j\sigma}n_{j\bar{\sigma}})t}|\psi_0\rangle \\
&=\langle \psi_0|e^{iUn_{i\sigma}n_{i\bar{\sigma}}t}a^\dagger_{i\sigma}e^{-iU n_{i\sigma}n_{i\bar{\sigma}}t} e^{iUn_{j\sigma}n_{j\bar{\sigma}}t}a_{j\sigma}e^{-iU n_{j\sigma}n_{j\bar{\sigma}}t}|\psi_0\rangle
\end{aligned}
$$
我们将算符分为了两部分：$i$格点的$e^{iUn_{i\sigma}n_{i\bar{\sigma}}t}a^\dagger_{i\sigma}e^{-iU n_{i\sigma}n_{i\bar{\sigma}}t}$和$j$格点的$e^{iUn_{j\sigma}n_{j\bar{\sigma}}t}a_{j\sigma}e^{-iU n_{j\sigma}n_{j\bar{\sigma}}t}$。对于任意两个算符A和B，我们有
$$
e^{A}Be^{-A} = B + [A,B]+\frac{1}{2!}[A,[A,B]] +\cdots
$$
将$A = iU n_{i\sigma}n_{i\bar{\sigma}}t$与$B = a^\dagger_{i\sigma}$带入得
$$
\begin{aligned}
e^{iUn_{i\sigma}n_{i\bar{\sigma}}t}a^\dagger_{i\sigma}e^{-iU n_{i\sigma}n_{i\bar{\sigma}}t}=a^\dagger_{i\sigma} + [iU n_{i\sigma}n_{i\bar{\sigma}}t,a^\dagger_{i\sigma}]+ \\
\frac{1}{2!}[iU n_{i\sigma}n_{i\bar{\sigma}}t,a^\dagger_{i\sigma},[iU n_{i\sigma}n_{i\bar{\sigma}}t,a^\dagger_{i\sigma}]] + \cdots
\end{aligned}
$$
对于费米子算符，我们有
$$
\begin{align}
[n_{i\sigma},a_{i\sigma}] &= -a_{i\sigma}\\
[n_{i\sigma},a^\dagger_{i\sigma}] &= a^\dagger_{i\sigma}
\end{align}
$$
因此展开式(10)中的各项对易子可以化简为：
$$
\begin{aligned}[]
[iU n_{i\sigma}n_{i\bar{\sigma}}t,a^\dagger_{i\sigma}]&=iUta^\dagger_{i\sigma}n_{i\bar{\sigma}}\\
[iU n_{i\sigma}n_{i\bar{\sigma}}t,a^\dagger_{i\sigma},[iU n_{i\sigma}n_{i\bar{\sigma}}t,a^\dagger_{i\sigma}]]&=(iUt)^2a^\dagger_{i\sigma}n_{i\bar{\sigma}}\\
&\cdots
\end{aligned}
$$
将上式带回到公式(10)中可得
$$
\begin{aligned}
e^{iUn_{i\sigma}n_{i\bar{\sigma}}t}a^\dagger_{i\sigma}e^{-iU n_{i\sigma}n_{i\bar{\sigma}}t}&=a^\dagger_{i\sigma}+iUta^\dagger_{i\sigma}n_{i\bar{\sigma}}+\frac{(iUt)^2}{2!}a^\dagger_{i\sigma}n_{i\bar{\sigma}}+\cdots\\
&=a^\dagger_{i\sigma}-a^\dagger_{i\sigma}n_{i\bar{\sigma}}+\left(1+iUt+\frac{(iUt)^2}{2!}+\cdots\right)a^\dagger_{i\sigma}n_{i\bar{\sigma}}\\
&=a^\dagger_{i\sigma}(1-n_{i\bar{\sigma}})+e^{iUt}a^\dagger_{i\sigma}n_{i\bar{\sigma}}
\end{aligned}
$$
同理对于$j$格点的$e^{iUn_{j\sigma}n_{j\bar{\sigma}}t}a_{j\sigma}e^{-iU n_{j\sigma}n_{j\bar{\sigma}}t}$，我们有
$$
e^{iUn_{j\sigma}n_{j\bar{\sigma}}t}a_{j\sigma}e^{-iU n_{j\sigma}n_{j\bar{\sigma}}t}=a_{j\sigma}(1-n_{j\bar{\sigma}})+e^{-iUt}a_{j\sigma}n_{j\bar{\sigma}}
$$
则$i,j$格点两部分算符的乘积为
$$
\begin{aligned}
& e^{iUn_{i\sigma}n_{i\bar{\sigma}}t}a^\dagger_{i\sigma}e^{-iU n_{i\sigma}n_{i\bar{\sigma}}t} e^{iUn_{j\sigma}n_{j\bar{\sigma}}t}a_{j\sigma}e^{-iU n_{j\sigma}n_{j\bar{\sigma}}t}\\
&=\left(a^\dagger_{i\sigma}(1-n_{i\bar{\sigma}})+e^{iUt}a^\dagger_{i\sigma}n_{i\bar{\sigma}}\right)\left(a_{j\sigma}(1-n_{j\bar{\sigma}})+e^{-iUt}a_{j\sigma}n_{j\bar{\sigma}}\right)\\
&=a^\dagger_{i\sigma}(1-n_{i\bar{\sigma}})a_{j\sigma}(1-n_{j\bar{\sigma}})+a^\dagger_{i\sigma}n_{i\bar{\sigma}}a_{j\sigma}n_{j\bar{\sigma}}\\
&+e^{iUt}a^\dagger_{i\sigma}n_{i\bar{\sigma}}a_{j\sigma}(1-n_{j\bar{\sigma}})+e^{-iUt}a^\dagger_{i\sigma}(1-n_{i\bar{\sigma}})a_{j\sigma}n_{j\bar{\sigma}}
\end{aligned}
$$

#### 含时演化中的offset

公式(16)中前两项为时间无关项，贡献了关联函数$\langle a_{i\sigma}^\dagger a_{j\sigma}\rangle_{i\ne j}$随时间演化的offset。我们可以分别指出其对应的物理过程：

第一项为$a^\dagger_{i\sigma}(1-n_{i\bar{\sigma}})a_{j\sigma}(1-n_{j\bar{\sigma}})$，对应在第$j$个格点上湮灭自旋$\sigma$，同时在第$i$个格点上产生自旋$\sigma$。并且$(1-n_{i\bar{\sigma}})(1-n_{j\bar{\sigma}})$要求在$i,j$格点上均没有相反的自旋$\bar{\sigma}$。因此第一项实际对应将$|0,\uparrow\rangle$ 变换为 $|\uparrow,0\rangle$。

第二项为$a^\dagger_{i\sigma}n_{i\bar{\sigma}}a_{j\sigma}n_{j\bar{\sigma}}$，对应在第$j$个格点上湮灭自旋$\sigma$，同时在第$i$个格点上产生自旋$\sigma$。并且$n_{i\bar{\sigma}}n_{j\bar{\sigma}}$要求在$i,j$格点上均存在相反的自旋$\bar{\sigma}$。因此第二项实际对应将$|\downarrow,\uparrow\downarrow\rangle$ 变换为 $|\uparrow\downarrow,\downarrow\rangle$。

我们可以定义双占据与空穴的产生与湮灭算符：
$$
\begin{align}
d^\dagger_{i\sigma}&=a^\dagger_{i\sigma}n_{i\bar\sigma}\\
d_{i\sigma}&=a_{i\sigma}n_{i\bar\sigma}\\
h^\dagger_{i\sigma}&=a_{i\sigma}(1-n_{i\bar{\sigma}})\\
h_{i\sigma}&=a^\dagger_{i\sigma}(1-n_{i\bar{\sigma}})
\end{align}
$$
其中$d^\dagger_{i\sigma}$表示在第$i$个格点上通过产生自旋$\sigma$来形成双占据（意味着$i$格点原来存在自旋$\bar\sigma$），$d_{i\sigma}$表示在第$i$个格点上通过湮灭自旋$\sigma$来形成单占据（$i$格点原来存在自旋$\bar\sigma$）；$h^\dagger_{i\sigma}$表示在第$i$个格点上通过湮灭自旋$\sigma$来形成空穴（意味着$i$格点原来不存在自旋$\bar\sigma$），$h_{i\sigma}$表示在第$i$个格点上通过产生自旋$\sigma$来形成单占据（$i$格点原来不存在自旋$\bar\sigma$）。利用双占据与空穴的产生湮灭算符，我们可以将两项不随时间变化的offset项表示为：
$$
\begin{align}
a^\dagger_{i\sigma}(1-n_{i\bar{\sigma}})a_{j\sigma}(1-n_{j\bar{\sigma}})&=h_{i\sigma}^\dagger h_{j\sigma}\\
a^\dagger_{i\sigma}n_{i\bar{\sigma}}a_{j\sigma}n_{j\bar{\sigma}}&=d^\dagger_{i\sigma}d_{j\sigma}
\end{align}
$$

#### 含时演化中的振荡

进一步我们分析关联函数$\langle a_{i\sigma}^\dagger a_{j\sigma}\rangle_{i\ne j}$中的含时项$e^{iUt}a^\dagger_{i\sigma}n_{i\bar{\sigma}}a_{j\sigma}(1-n_{j\bar{\sigma}})+e^{-iUt}a^\dagger_{i\sigma}(1-n_{i\bar{\sigma}})a_{j\sigma}n_{j\bar{\sigma}}$。我们将$e^{iHt}$展开为实部$\cos(Ut)$与虚部$i\sin(Ut)$，则含时项可以表示为：
$$
\cos(Ut)\left(a^\dagger_{i\sigma}n_{i\bar{\sigma}}a_{j\sigma}(1-n_{j\bar{\sigma}})+a^\dagger_{i\sigma}(1-n_{i\bar{\sigma}})a_{j\sigma}n_{j\bar{\sigma}}\right)+\\
i\sin(Ut)\left(a^\dagger_{i\sigma}n_{i\bar{\sigma}}a_{j\sigma}(1-n_{j\bar{\sigma}})-a^\dagger_{i\sigma}(1-n_{i\bar{\sigma}})a_{j\sigma}n_{j\bar{\sigma}}\right)
$$
对于虚部，我们有
$$
\begin{aligned}
&a^\dagger_{i\sigma}n_{i\bar{\sigma}}a_{j\sigma}(1-n_{j\bar{\sigma}})-a^\dagger_{i\sigma}(1-n_{i\bar{\sigma}})a_{j\sigma}n_{j\bar{\sigma}}\\
=&a^\dagger_{i\sigma}n_{i\bar{\sigma}}a_{j\sigma}-a^\dagger_{i\sigma}n_{i\bar{\sigma}}a_{j\sigma}n_{j\bar{\sigma}}-a^\dagger_{j\sigma} a_{j\sigma}n_{j\bar{\sigma}}+a^\dagger_{i\sigma}n_{i\bar{\sigma}}a_{j\sigma}n_{j\bar{\sigma}}\\
=&a^\dagger_{i\sigma}n_{i\bar{\sigma}}a_{j\sigma}-a^\dagger_{i\sigma} a_{j\sigma}n_{j\bar{\sigma}}=a^\dagger_{i\sigma} a_{i\sigma}(n_{i\bar{\sigma}}-n_{j\bar{\sigma}})
\end{aligned}
$$
虚部这一项在对态求期望值时，由于$i,j$格点自旋$\bar\sigma$占据数的期望值相同，因此$n_{i\bar{\sigma}}-n_{j\bar{\sigma}}$期望值恒为零，从而含时项中不含虚部。

对于含时的实部项：$\cos(Ut)\left(a^\dagger_{i\sigma}n_{i\bar{\sigma}}a_{j\sigma}(1-n_{j\bar{\sigma}})+a^\dagger_{i\sigma}(1-n_{i\bar{\sigma}})a_{j\sigma}n_{j\bar{\sigma}}\right)$，利用双占据与空穴的产生湮灭算符，我们可以将含时项写成：
$$
\cos(Ut)\left(d^\dagger_{i\sigma}h^\dagger_{j\sigma}+h_{i\sigma}d_{j\sigma}\right)
$$
这一项对应了从$i,j$格点均为单占据态变成双占据与空穴对，和从双占据与空穴对变成$i,j$格点的单占据态，即将$|\downarrow,\uparrow\rangle$变换为$|\uparrow\downarrow,0\rangle$和从$|0,\uparrow\downarrow\rangle$变换成$|\downarrow,\uparrow\rangle$。由前面含时演化虚部的期望值为零可知，这两项的期望值相同，即$\langle d^\dagger_{i\sigma}h^\dagger_{j\sigma}\rangle = \langle h_{i\sigma}d_{j\sigma}\rangle$

#### 总结

综上，我们写出关联函数$\langle a_{i\sigma}^\dagger a_{j\sigma}\rangle_{i\ne j}$在末态哈密顿量下随时间的演化为：
$$
\langle \psi(t)| a^\dagger_{i\sigma}a_{j\sigma}|\psi(t)\rangle_{i\ne j}=\langle h_{i\sigma}^\dagger h_{j\sigma}\rangle+\langle d^\dagger_{i\sigma}d_{j\sigma}\rangle+\cos(Ut)\left(\langle d^\dagger_{i\sigma}h^\dagger_{j\sigma}\rangle + \langle h_{i\sigma}d_{j\sigma}\rangle\right)
$$
前两项贡献了振荡的offset，后两项贡献了振荡的振幅，其中双占据与空穴的产生与湮灭算符的表达式为：
$$
\begin{align}
d^\dagger_{i\sigma}&=a^\dagger_{i\sigma}n_{i\bar\sigma}\\
d_{i\sigma}&=a_{i\sigma}n_{i\bar\sigma}\\
h^\dagger_{i\sigma}&=a_{i\sigma}(1-n_{i\bar{\sigma}})\\
h_{i\sigma}&=a^\dagger_{i\sigma}(1-n_{i\bar{\sigma}})
\end{align}
$$
第一项实际对应将$|0,\uparrow\rangle$ 变换为 $|\uparrow,0\rangle$；

第二项实际对应将$|\downarrow,\uparrow\downarrow\rangle$ 变换为 $|\uparrow\downarrow,\downarrow\rangle$；

振荡项实际对应将$|\downarrow,\uparrow\rangle$变换为$|\uparrow\downarrow,0\rangle$和从$|0,\uparrow\downarrow\rangle$变换成$|\downarrow,\uparrow\rangle$。


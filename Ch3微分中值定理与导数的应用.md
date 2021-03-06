目录

[TOC]

##微分中值定理与导数的应用
用导数来研究函数以及曲线的某些性态

微分学中的几个中值定理是导数应用的理论基础

###1.微分中值定理
####中值定理的条件
几个概念**左(右)极限,左(右)连续,左(右)导数**

+ 极限存在的充要条件是:左右极限存在且相等(P34)
	- $\lim\limits_{x \to x_0}f(x) 存在\iff f(x_0^-)=f(x_0^+)$
	- 单侧极限
+ 连续的充要条件是:$在x_0处的极限等于函数值$
	- $f(x_0) =  \lim\limits_{x \to x_0}f(x)$
		- ($f(x_0)=\lim\limits_{x \to x_0}f(x) = f(x_0^-)=f(x_0^+)$)
	- 左连续/右连续
		- 左连续:函数值等于左极限$f(x_0)=f(x_0^-)$
		- 右连续:函数值等于右极限$f(x_0)=f(x_0^+)$
+ 可导/导数存在的充要条件是:左右导数存在且相等
(**导数是一个极限**,导数存在即极限存在)
(左右导数分别是一个左右极限)
	- $f_-^\prime(x_0) = f_+^\prime(x_0)=f^\prime(x_0)$
	- 单侧导数
		- 左导数
		- 右导数

**连续是左右极限相等且等于函数值,可导是左右导数(极限)相等**
但是

+ 连续里的极限是$\lim\limits_{x \to x_0}f(x_0)$
+ 可导里的极限是$\lim\limits_{\Delta x \to 0}\frac{\Delta y}{\Delta x}$


**闭区间上的连续与可导**

+ 闭区间$[a,b]$连续:$a处左连续,b处右连续$
+ 闭区间$[a,b]$可导:$a处存在左导数,b处存在右导数$

**关于中值定理的适用条件**

+ 在$闭区间[a,b]上连续,在开区间(a,b)内可导$
在端点处只要满足"单侧连续即可"
	- $a处连续但不可导:a处左连续$
	- $b处连续但不可导:b处右连续$


####罗尔定理
几何描述:满足一定条件的曲线弧在最高点或最低点处有水平切线


费马引理
$设函数f(x)在点x_0的某邻域U(x_0)内有定义,且在x_0处可导$
$如果对任意的x\in U(x_0)有$
$$f(x) \leqslant f(x_0)(或f(x) \geqslant f(x_0))$$
那么$f^\prime(x_0)=0$

(证明用到了可导的条件,和极限的保号性,既$\leqslant 0$又$\geqslant 0$,那么只能$=0$)


罗尔定理
$如果函数f(x)满足$

+ $在开区间[a,b]上连续$
+ $在开区间(a,b)内可导$
+ $在区间端点处函数值相等,即f(a)=f(b)$
那么在$(a,b)$内至少有一点$\xi(a<\xi<b),使得$
$$f^\prime(\xi)=0$$

####拉格朗日中值定理
取消罗尔定理中的一个较特殊的限制
几何描述:满足一定条件的曲线弧,弧上必有一点的切线平行于两端点所连成的弦

$如果函数f(x)满足$

+ $在开区间[a,b]上连续$
+ $在开区间(a,b)内可导$
+ $在区间端点处函数值相等,即f(a)=f(b)$
那么在$(a,b)$内至少有一点$\xi(a<\xi<b),使得等式$
$$f(b)-f(a)=f^\prime(\xi)(b-a)$$
成立

给出了自变量去有限增量时**函数增量的准确表达式**
$$\Delta y = f(x+\Delta x) - f(x) = f^\prime(\xi)(x+\Delta x - x) =f^\prime(x+\theta \Delta x)\bullet \Delta x$$
**有限增量定理**
**微分中值定理**

由拉格朗日中值定理导出的一个在积分学中很有用的定理:
**定理**:导数恒为0函数时常数

####柯西中值定理

$如果函数f(x),F(x)满足$

+ $在开区间[a,b]上连续$
+ $在开区间(a,b)内可导$
+ 对任一$x \in (a,b),F^\prime(x) \not = 0$
那么,在$(a,b)内至少有一点\xi 使得下列等式成立$
$$\frac{f(b)-f(a)}{F(b) - F(a)}=\frac{f^\prime(\xi)}{F^\prime(\xi)}$$

证明,.....????>......

###2.洛必达法则

无穷小及无穷大之间的商的极限

+ $\frac{0}{\infty}:0\bullet \frac{1}{\infty} 是0$
+ $\frac{\infty}{0}:\frac{1}{\frac{0}{\infty}}是\infty$
极限的结果是定的
其他形式

+ $\frac{0}{0}$
+ $\frac{\infty}{\infty}$
极限可能存在,可能不存在,极限的结果是不确定的,
称之为未定式
其他的一些未定式.....


"商的极限等于极限的商"要满足两个条件

+ 极限存在,:分子分母不能是无穷大
+ 分母的极限不但要存在还不能为0:分母不能是无穷小
(分子可以是无穷小,分母既不能是无穷大也不能是无穷小)
所以未定式的极限无法用此法则

洛必达法则,用柯西中值定理推出的一种求未定式极限的方法
分子分母分别求导再求极限
**定理1**:$x \to a时,未定式\frac{0}{0}的情形$
要满足的条件

+ $x \to a时,f(x),F(x)都趋于零$
+ $在点a的某去心邻域内,f^\prime(x),F\^prime(x)都存在,且F\^prime(x)\not= 0$
+ $\lim\limits_{x \to a}\frac{f(x)}{F(x)}=\frac{f^\prime(x)}{F^\prime(x)}(或为无穷大)$

$x \to \infty 时,未定式\frac{0}{0}$
$x \to a ,x \to \infty 时,未定式\frac{\infty}{\infty}$
都有相应的洛必达法则


**函数增大的速度**
$x \to +\infty时,$
$$e^{\lambda x} \gg x^n \gg lnx$$

其他的一些未定式.....
$0\bullet \infty,\infty - \infty,0^0,1^\infty,\infty ^ 0$


**如何求未定式**
转化

+ $0\bullet \infty,\frac{0}{\frac{1}{\infty}}$
+ $\infty - \infty,化为分式$
+ $0^0,取对数求导$

洛必达法则是向高阶导数的方向努力
化简
等价无穷小
洛必达法则

+ 洛必达法则和其他方法结合
+ 极限存在,未必能用洛必达法则求出......
用洛必达法则求极限,如果求的极限不存在(等于无穷大的情况除外),要求的极限却未必不存在.....

###3.泰勒公式
###4.函数的单调性与曲线的凹凸性
###5.函数的极值与最大值最小值
###6.函数图形的描绘
###7.曲率
###8.方程的近似解


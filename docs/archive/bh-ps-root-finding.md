
_玻海同人本《无解》习题集_

***求根算法***

三题分别是二分法[<sup>1</sup>](#refer-1)、割线法[<sup>2</sup>](#refer-2)和牛顿法[<sup>3</sup>](#refer-3)。
二分法那题凑得实在是太生硬了。

---

68. 用二分法求已知连续函数$f(x)=0$的一个解。首先，找到一个区间$[a,b]$，使得$f(a)f(b)<0$。根据介值定理，存在$x^* \in [a,b]$使得$f(x^*)=0$。利用二分法求解步骤如下：
	1. 求该区间的中点$m=(a+b)/2$，计算$f(m)$。
	2. 若$f(m)f(a)>0$，取$[m,b]$为新区间，否则取$[a,m]$为新区间。
	3. 重复上述两步，直至达到理想精度。
已知函数$F(x)$在区间$[0,2]$上连续，且$F(0)<0$，$F(2)>0$。请问：用二分法求解$F(x)=0$，最多需要多少步就能找到一个$\hat{x}$，使得$\hat{x}$到$F(x)=0$的某个解的距离小于$10^{-65}$？<!--217--><!--n=ceil((ln(b-a)-ln(d))/ln(2))-->

69. 令$x_0=0$，$x_1 = 100$，$f(x) = x^2 -1941$，作如下迭代：
$$x_{n+1} = x_n - \dfrac{x_n-x_{n-1}}{f(x_n)-f(x_{n-1})} f(x_n), \quad n = 1,2,\cdots$$
对$x_{19}$到$x_{41}$这23个数取整后求和，请问等于多少？<!--1012-->

70. 令$x_0=1$，作如下迭代：
$$x_{n+1} = \dfrac{x_n}{2} + \dfrac{1941}{2x_n}, \quad n = 1,2,\cdots$$
对$x_{1901}$到$x_{1921}$这些数取整后求和，请问等于多少？<!--924-->

---

###### References

<div id="refer-1"></div>

- [1] [Bisection method](https://en.wikipedia.org/wiki/Bisection_method)

<div id="refer-2"></div>

- [2] [Secant method](https://en.wikipedia.org/wiki/Secant_method)

<div id="refer-3"></div>

- [3] [Newton's method](https://en.wikipedia.org/wiki/Newton%27s_method)

---

[题目合集](archive/bh-ps)
[上一页](archive/bh-ps-computational-mathematics)
[下一页](archive/bh-ps-game-theory)
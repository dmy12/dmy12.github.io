
_玻海同人本《无解》习题集_

***计数***

第1、2题是根据离散数学教材[<sup>1</sup>](#refer-1)编的。主要是在题面里塞了玻海两人的生日。

第12题可能是这几道计数题里最难的一题，来源于一个视频[<sup>2</sup>](#refer-2)，强烈推荐这个up主：[3Blue1Brown - YouTube](https://www.youtube.com/watch?v=K8P8uFahAgc)，[3Blue1Brown - B站](https://www.bilibili.com/video/av19849697/)。11题算是12题的中间过程吧。

第17题灵感来源于疯子坐飞机问题。4年前也出过的一道装信的题，当时那题是说，如果每一封信都装对了信封就会把信寄出，求把信寄出的概率（的倒数）。然而二维码改了之后需要重新凑数，那题就不能用了。没有寄出的信永远是玻海最令我内伤的一个点。

第65题是因为我出题那会儿沉迷turtle画图，然后知道了[Frieze Group](https://en.wikipedia.org/wiki/Frieze_group)，画了一些相关的图。题目本身只是简单计数。

---

1. $m$是$1007$到$9999$之间个十百千位数各不相同的整数的个数，$n$是$1205$（含$1205$）到$9999$之间个十百千位数各不相同的奇数的个数。试求$m-n$。<!--2325-->

2. 求方程
$$\frac{1}{x}+\frac{2}{y}-\frac{3}{z}=1$$
满足$x\leq 1007$且$y<1205$的正整数解的个数。<!--1610 Hint: (1,2k,3k),(k,2,3k),(2,1,2),(2,3,18) -->



11. 将圆上的$13$个点两两连线，请问连成的线段在圆内最多有多少个交点？<!--715 Hint: n choose 4 -->

12. 平面上有一个圆，圆上$17$个点两两连线，假设不存在三条或三条以上线段交与同一点，请问这些线段和圆把平面分成了多少块区域？<!--2518 Hint: f=e-v+2, v=C_n^4+n, n on Circle, C_n^4 in Circle, e=C_n^2 + 2*C_n^4-->



17. B给H写了$11$封信，但他犹豫是否要将这些信寄出。为帮助自己做决定，他取出$11$个信封，依次编号为$1,\cdots,11$，并把信按照写信的时间先后顺序编号，最近写的一封编号为$1$，最早写的一封编号为$11$。现在他按照如下规则分装信件：首先，他随机地将$1$号信装进$11$个信封中的一个，接下来，装$2$号信，如果$2$号信封是空的，则把$2$号信装入$2$号信封，否则随机把$2$号信装进剩下的信封。之后的信都依照这样的规则分装，即在装$i$号信时，如果$i$号信封是空的，则将$i$号信装入$i$号信封，否则，随机将$i$号信装进剩下的信封。依照这样的规则装完全部$11$封信。他会把放对信封的信全都寄出。请问：有多少种情况，B会寄出至少两封信。<!--1013 Hint: All possible case: \sum_{i=0}^{10}C_{10}^i = 1024; every letter is wrong: 1; 10 letters are wrong: 10. -->



65. 用如下方法生成一条无穷长的带状花纹: 首先选取下图方格1、2、3、4中的任意图案填充这4个方格，或者保持空白，假设方格的长度为$L$，将方格水平移动$2L*k$, $k=\cdots, -3,-2,-1,0,1,2,3,\cdots$。下面两图均是示例。请问：一共能产生多少种不同的无穷长的带状花纹？
<!--325-->
<center>
<img src="archive/imgs/FG p2mm.jpeg" width="80%" height="80%">
<img src="archive/imgs/FG p11g.jpeg" width="80%" height="80%">
</center>

---

###### References:

<div id="refer-1"></div>

[1] Rosen, K., Discrete Mathematics and Its Applications

<div id="refer-2"></div>

[2] [Circle Division Solution - 3Blue1Brown](https://www.youtube.com/watch?v=K8P8uFahAgc)

---

[题目合集](archive/bh-ps)
[下一页](archive/bh-ps-number-theory-and-cryptography)


_玻海同人本《无解》习题集_

***数论与密码***

题目都是根据离散数学教材[<sup>1</sup>](#refer-1)编的。

涉及到了[ISBN](https://en.wikipedia.org/wiki/International_Standard_Book_Number), [hamming code](https://en.wikipedia.org/wiki/Hamming_code), [RSA](https://en.wikipedia.org/wiki/RSA_(cryptosystem)).

第4题和第8题有彩蛋。

---

4. 已知某本图书的国际标准书号(ISBN)是10位，但最后一位被磨损了看不清，只能看到前9位是004925020。试补全该书的书号并搜索出书名。写下该书书名中第 一个单词的第一个字母，并按字母表顺序(abcdefg...a对应01,b对应02,...,z对应26)把这个字母转化成数字写出来作为答案的千位和百位，而补全书号的最后两位作为答案的十位和个位。<!--1605 Physics and Beyond-->

5. $(7,4)$汉明码是一种线性纠错码，它把$4$比特的数据$(d_1,d_2,d_3,d_4)$增加$3$个校验码$(p_1,p_2,p_3)$，编码成$7$位。规则是下图每个圆内的数的和为偶数。
<center>
<img src="https://upload.wikimedia.org/wikipedia/commons/b/b0/Hamming%287%2C4%29.svg" width="50%" height="50%">
</center>
例如，$(1001)$会被编码成$(1001001)$。(7,4)汉明码可以检测并纠正单个比特的差错，也能检测双比特差错。现有一个十进制的四位数，转化成二进制后它有$12$位，我们把它按顺序分成$3$个四位01字符串，并把它们用$(7,4)$汉明码编码并进行传输。假设传输过程中这$3$个$7$位的字符串每串至多出现一位错误，接收到的最高四位到最低四位编码依次为$(1011011)$，$(1101011)$，$(1111010)$。试写出这个数的十进制表示。<!--3019-->

6. 在数论中，对正整数$n$，欧拉函数$\varphi(n)$是小于等于$n$的正整数中与$n$互质的数的个数。试求$\varphi(2685)$。<!--1424-->

7. RSA加密算法是一种非对称加密算法，在公开密钥加密和电子商业中被广泛使用。应用RSA加密算法时，首先需要产生一个公钥和一个私钥，这可以通过以下方式可以产生：

    1. 随意选择两个大素数$p$和$q$，$p \neq q$，$N=pq$。
    2. 根据欧拉函数，求得$r=\varphi(N)=(p-1)(q-1)$。
    3. 选择一个小于$r$的正整数$e$，使得$e$与$r$互质。并求得正整数$d$使得：$ed \equiv 1 \text{ (mod r)}$。

  现在A和B想要用RSA加密算法传递信息。A选取$p=31$，$q=37$，由此可得$N=1147$，并选取$e=17$。试求出$d$，写下$2d$。<!--1906,d=953-->

8. A把上题中的公钥$(N,e)$与B共享，这样B就能用这个公钥加密消息。首先B把想要传送的消息（按约定规则）转化成一个或一列小于$N$的非负整数，对于一个数$n$，B会用如下公式将$n$加密为$c$:
$$c\equiv n^e \text{ (mod N)}$$
现在B想向A传递的信息为如下一列数：
$$(67, 79, 80, 69, 78, 72, 65, 71, 69, 78)$$
请问其中的$80$会被加密成多少？<!--820 COPENHAGEN-->

9. B用上面的公钥和规则将$x$加密得到$430$，并把加密后的数传给了A，请问A利用密钥$d$解码得到的数是多少？<!--711-->


---

###### References:

<div id="refer-1"></div>

- [1] Rosen, K., Discrete Mathematics and Its Applications

---

[题目合集](archive/bh-ps)
[上一页](archive/bh-ps-counting)
[下一页](archive/bh-ps-graph-theory)
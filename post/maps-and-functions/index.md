# 映射
$X$,$Y$为非空集合.$f(x)$中$X$为法则.

每个元素$x$都有唯一的$y$与之对应.
 
$f$为映射.

$$f:X\rightarrow Y$$

$X$为定义域，用$D_f$（Domain）表示.
值域用$R_f$（Range）表示.

## 注意
- 函数三要素$X,f,Rf$.
- $x \in X$,对应的是唯一的.一个$x$不能对应多个$y$,但一个$y$可以对应多个$x$.$R_f \subset Y$,$R_f \ne Y$.

# 满射与单射
满射：$R_f = Y$,单射$x_1 \ne x_2$.同时满足则为一一映射(或双射).

# 逆函数
设$f:X \rightarrow Y$单射,每个$y \in R_f$,有唯一$x \in X$,满足$f(x)=y$,则$g:R_f \rightarrow X$为逆映射,记作$f^{-1}$.

# 复合映射
$g:X \rightarrow Y_1 ,f:Y_2 \rightarrow Z,Y_1 \subset Y,x \in X.f[g(x)] \in Z.$可表示为$f \circ g:X \rightarrow Z$.
$R_g \subset D_f$.

# 函数

$D \subset R$,$f:D\rightarrow R$,$y=f(x)$,$x\in D$.x自变量,y因变量,值域$R_f = f(D)$.

## 两要素
$D_f,f$.

## 表示方法 
- 表格法
- 图形法
- 解析式(公式法)

例8 $f(x)=[x]$ (不超过x的最大整数)

## 特性

### 有界性 

(1)上界不唯一:$\exists k_1$,$f(x) \leq k_1$  $f(x)=-\frac{1}{x} (x >  0)$ $f(x)\leq 0$

(2)下界不唯一:$\exists k_2,f(x)\geq k_2$

(3)有界性:$\exists 正数M,使得\lvert f(x) \rvert\leq M$.无界性:$\forall 正数M \exists x_1 \in x,\lvert f(x_1) \rvert> M$.

### 单调性 

$x_1 <  x_2$ $f(x_1)<  f(x_2)$  单增
$x_1<  x_2$ $f(x_1)> f(x_2)$ 单减 

### 奇偶性 

(1)奇函数：$D$ 关于原点对称。$f(-x)=-f(x)$

(2)偶函数：$D$ 关于$y$ 轴对称。$f(-x)=f(x)$ 

### 周期性 

$\exists 正数 l,f(x+l)=f(x)$

最小周期:$y=sin x$,周期 $2\pi$ .

并非每个周期函数都有最小周期:例10:狄利克雷函数
$$
f(x)=\begin{cases}
1, &x \in Q\\\
0, &x \in Q^{C}
\end{cases}
$$
这是一个周期函数,任何正有理数r都是它的周期.不存在最小的正有理数,所以没有最小正周期.

$x$ (有理数)+$r$ = 有理数

$x$ (无理数)+$r$ = 无理数

## 反函数与复合函数

### 反函数 

设$f:D\rightarrow f(D)$ 单射,$f^{-1}:f(D)\rightarrow D$.

$f$ 单调,单射,则$f^{-1}$ 必存在,且单调,单调性与$f$ 相同.二者函数图像关于$y=x$ 对称.

原函数与反函数关于$y=x$ 对称.
#### 反三角函数
##### 正弦函数

$y=sin x$的反函数是$x=arcsin y$,即$y=arcsin x$.

$y=sin x$ 的定义域是$(-\infty ,+\infty )$,值域是$[-1,1]$.

$y=arcsin x$ 的定义域是$[-1,1]$,值域是$[-\frac{\pi }{2},\frac{\pi }{2}]$,单调增.

| x         | $-1$              | $\cdots$ | $-\frac{1}{2}$    | $0$ | $\frac{1}{2}$    | $\frac{\sqrt{2}}{2}$ | $1$              |
| --------- | ----------------- | -------- | ----------------- | --- | ---------------- | -------------------- | ---------------- |
| $arcsinx$ | $-\frac{\pi }{2}$ | $\cdots$ | $-\frac{\pi }{6}$ | $0$ | $\frac{\pi }{6}$ | $\frac{\pi }{4}$     | $\frac{\pi }{2}$ |
##### 余弦函数
定义域$[0,\pi ]$,值域$[0,\pi ]$,单调减.
##### 正切函数
定义域$R$,值域$(-\frac{\pi }{2},\frac{\pi }{2})$,单调增.
##### 余切函数
定义域$R$,值域$(0,\pi )$,单调减.
### 复合函数及其运算 

$y=f(t),t=g(x),y = f(g(x))$. $t= g(x)$ 为中间变量.

#### 运算

$f(x),g(x)$,其定义域分别为$D_f,D_g$.$D=D_f \cap D_g \ne \varnothing$.
1. $(f \pm g)(x)=f(x)\pm g(x)$
2. $(f \cdot g)(x)=f(x)\cdot g(x)$
3. $\frac{f}{g}(x)=\frac{f(x)}{g(x)},g(x) \ne 0$


例11: $f(x)$ 定义域$(-l,l)$.$f(x)=g(x)+h(x)$,$f(x)为任给,g(x)为偶函数,h(x)为奇函数.$
$$
\begin{cases}
f(x) & = &g(x)+h(x)\\\
f(-x) & = &g(x)-h(x)
\end{cases}
$$

可得$g(x)=\frac{1}{2}[f(x)+f(-x)]$,$h(x)=\frac{1}{2}[f(x)-f(-x)]$.

### 初等函数

幂函数$y=x^{\mu }$ 指数函数$y=a^{x}$ 对数函数$y=\log_{a}{x}$,三角,反三角函数.

有限次运算.($f_1(x)+f_2(x)+ \cdots$ 不是初等函数,$但f_1(x)+f_2(x)+ \cdots +f_n(x)是初等函数$.) 

# 极限

## 数列

一列数.

$x_n$ 为一般项(通项).

## 极限

数列:$\frac{1}{2},\frac{1}{4},\frac{1}{8} \cdots \rightarrow 0$

定义:设$f(x)$是一个数列,$\forall \varepsilon  > 0 ,\exists N,使得当n > N时,\lvert x_n-a \rvert <  \varepsilon , a 是极限.$ 其中$\varepsilon 为任意小距离,N为某项,n为这项后所有项.\lvert x_n-a   \rvert <  \varepsilon 都落在小区间里.$

例1. 证明$2,\frac{1}{2},\frac{4}{3},\frac{3}{4},\cdots,\frac{n+(-1)^{n-1}}{n}$ 的极限是1.

证: $\lvert x_n -1 \rvert=\lvert \frac{n+(-1)^{n-1}}{n}-1\rvert=\lvert \frac{(-1)^{n-1}}{n} \rvert=\frac{1}{n}<  \varepsilon$,$n > \frac{1}{\varepsilon }$.

$\forall \varepsilon > 0,N=[\frac{1}{\varepsilon }].n > N时在,\lvert x_n-1 \rvert =\cdots=\frac{1}{n}<  \varepsilon$

例3. $\lvert x_{n}<  1 \rvert ,1,q,q_2,q_3,\cdots,q^{n-1}<  \varepsilon,(n-1)\ln\lvert q \rvert <  \ln \varepsilon ,(n-1)> \frac{\ln\varepsilon }{\ln\lvert q \rvert },n> \frac{\ln\varepsilon }{\ln\lvert q \rvert }+1$.

## 收敛函数的性质

### 收敛函数的极限唯一
证: 反证. $x_{n}\rightarrow a,x_{b}\rightarrow b.(a \ne b)a<  b$取$\varepsilon =\frac{b-a}{2}$

$\because {\lim\limits_{n \to +\infty}} \exists N_1, n> N_1$ 时,$\lvert x_{n}-a \rvert <  \frac{b-a}{2}\implies-\frac{b-a}{2}<  x_{n}-a<  \frac{b-a}{2}\implies\frac{3a-b}{2}<  x_{n}<  \frac{a+b}{2}$

$\because {\lim\limits_{n \to +\infty } x_{n}}=b$,$\exists N_2$时,$\lvert x_{n}-b \rvert <  \frac{b-a}{2}\implies-\frac{b-a}{2}\leq x_{n}-b<  \frac{b-a}{2}\implies\frac{a+b}{2}<  x_{n}<  \frac{3b-a}{2}$

$\therefore 矛盾$ 

例4. 证明数列$x_{n}=(-1)^{n+1}(n=1,2,\cdots)$是发散的.

设收敛${\lim\limits_{n \to +\infty } x_{n}}=a$.对$\varepsilon =\frac{1}{2},\exists N,n> N$时,$\lvert x_{n}-a \rvert <  \frac{1}{2}$.

$-\frac{1}{2}<  x_{n}-a<  \frac{1}{2},a-\frac{1}{2}<  x_{b}<  a+\frac{1}{2}$.

### 收敛函数一定有界,有界数列不一定收敛.

证:设$\lim\limits_{n \to +\infty } =a$,对$\varepsilon =1,\exists N,n> N$ 时,$\lvert x_{n}-a \rvert <  1$ 

证:$\lvert x_{n} \rvert =\lvert x_{n}-a+a \rvert \leq \lvert x_{n}-a \rvert +\lvert a \rvert <  \lvert a \rvert +1$.$n> N$ 时,$N$ 后$\lvert x_{n} \rvert <  \lvert a \rvert +1$有界.

$M=max\{\lvert x_1 \rvert ,\lvert x_2 \rvert ,\cdots,\lvert x_{n} \rvert ,\lvert a \rvert +1\}$ 

一切$x_{n},\lvert x_{n} \rvert \leq M$

### 收敛函数具有保号性.

$\lim\limits_{n \to +\infty } x_{n}=a,$ 且$a<   0.\exists N> 0,n> N$ 时,$x_{n}<   0$$(a> 0$ 时$x_{n}> 0)$ 

![保号性](https://pic.imgdb.cn/item/62b4fca60947543129d41f99.png "保号性")

证:$a> 0$ 时,$\varepsilon =\frac{a}{2}> 0,\exists N> 0,n> N$时,$x_{n}-a<  \frac{a}{2}$

$\lvert x_{n}-a \rvert <  \frac{a}{2}$,$-\frac{a}{2}<  x_{n}<  \frac{a}{2},0<  \frac{a}{2}<  x_{n}<  \frac{3}{2}a$,$x_{n}> 0$ 

推论:若数列从某项起$x_{n}\geq 0$,且$\lim\limits_{n \to +\infty } x_{n}=a$,则$a \geq 0$.($\leq 0$ 同样成立)

### 收敛数列的任一子数列收敛于同一象限.

子数列:$1,\frac{1}{2},\frac{1}{4},\frac{1}{8},\cdots$ 的子数列是$1,\frac{1}{4},\frac{1}{16},\frac{1}{64},\cdots$ 

证:$\{x_{n_{k}}\}$ 是$\{x_{n}\}$的子数列.
$\because \lim\limits_{n \to +\infty } x_{n}=a$,故$\forall \varepsilon > 0,\exists N> 0.n> N$时,$\lvert x_{n}-a \rvert <  \varepsilon$.

取$K=N,k > K$ 时,$n_{k}> n_{k}=n_{N}\geq N,\lvert s_{n_{k}} \rvert <  \varepsilon$

说明:

由此性质可知,若数列有两个子数列收敛于不同的极限,则原数列一定发散.

例如,
$$
x_{n}=(-1)^{n+1}(n=1,2,\cdots)发散
$$

$$
 \lim\limits_{k \to \infty } x_{2k-1}=1;\lim\limits_{k \to \infty } x_{2k}=-1 
$$

## 函数的极限
$x \rightarrow a$有限数.$x \rightarrow a,f(x)\rightarrow b$

定义:$f(x)$在$x_0$ 的去心邻域内有定义.(在$x_0$ 处可以没有定义.)(区别于连续:$\lim\limits_{x \to x_0} f(x)=f(x_0)$)
$\exists A ,\forall \varepsilon > 0,\exists \delta> 0,0<  \lvert x-x_0 \rvert <  \delta$时$\lvert f(x)-A \rvert <  \varepsilon$ .

补充:设$x_0\in R,\delta > 0,$ 开区间$(x_0-\delta,x_0+\delta)$称为点$x_0$ 的$\delta$ 邻域,记作$U(x_0,\delta )$,点$x_0$ 的去心$\delta$ 邻域记作$\mathring{U}(x_0,\delta )$,$\delta$称为邻域半径.

$\lim\limits_{x \to x_0} f(x)=A,f(x)\rightarrow A(x \rightarrow x_0)$

1. $\lim\limits_{x \to x_0} C=C$ 

解:$\forall \varepsilon > 0,\exists \delta > 0$使得$0<  \lvert x-x_0 \rvert <  \delta$ 时,$\lvert f(x)-A \rvert =\lvert C-C \rvert =0<  \varepsilon$

2. $\lim\limits_{x \to x_0} x=x_0$ 

解:$\forall \varepsilon > 0,$ 取$\delta =\varepsilon$,$0<  \lvert x-x_0 \rvert <  \delta$ 时,$\lvert f(x)-A \rvert =\lvert x-x_0 \rvert <  \varepsilon$

3. $\lim\limits_{x \to 1} (2x-1)=1$ 

证:$\forall x> 0$ 取$\delta =\frac{\varepsilon }{2}$ $0<  \lvert x-1 \rvert <  \delta$

$\lvert f(x)-A \rvert =\lvert 2x-1-1 \rvert =2\lvert x-1 \rvert <  \varepsilon$ ,$\lvert x-1 \rvert <  \delta =\frac{\varepsilon }{2}$ 

$\lvert f(x)-A \rvert =\lvert 2x-1-1 \rvert=2\lvert x-1 \rvert <  \varepsilon$

4. $\lim\limits_{x \to 1} \frac{x^2-1}{x-1}=2$ 

证:$\forall \varepsilon > 0,\exists \delta =\varepsilon 0<  \lvert x-1 \rvert <  \delta =\varepsilon \lvert x+1-2 \rvert =\lvert x-1 \rvert <  \varepsilon$

左极限$\lim\limits_{x \to x_0^{-}} f(x)=A$.右极限$\lim\limits_{x \to x_0^{+}}f(x)=A$

$x \rightarrow x_0 f(x)$ 极限存在$\Leftrightarrow$ 左右极限均存在且相等。

6. $f(x)=
\begin{cases}
x-1 &x<  0\\\
0&x=0\\\
2x-1&x> 0	
\end{cases}
$

$\lim\limits_{x \to 0^{-}} f(x)=-1 \lim\limits_{x \to 0^{+}} f(x)=-1$ 

$x \rightarrow \infty \forall \varepsilon > 0\exists$正数$X$(找一个)$\lvert x \rvert > X$时$\lvert f(x)-A \rvert <  \varepsilon \lim\limits_{x \to \infty } f(x)=A$

7. $\lim\limits_{x \to \infty } \frac{1}{x}=0$ 

证:$\forall \varepsilon > 0\exists x=\frac{1}{\varepsilon }$

$\lvert x \rvert > X=\frac{1}{\varepsilon }\lvert \frac{1}{x}-0 \rvert <  \varepsilon$ 

$\lvert x \rvert > \frac{2}{\varepsilon }\frac{1}{\lvert x \rvert }<  \frac{\varepsilon }{2}<  \varepsilon$

 性质(1)函数极限唯一性

 (2)$\lim\limits_{x \to x_0} f(x)=A \exists M> 0\delta > 0,0<  \lvert x-x_0 \rvert <  \delta$ 时$f(x)\leq M(界)$ 

 (3)局部保号性:$\lim\limits_{x \to x_0} f(x)=A,A> 0\exists \delta > 0 局部:0<  \lvert x-x_0 \rvert <  \delta 保号:f(x)> 0$

$\lim\limits_{x \to x_0} f(x)=A\{x_{n}\}\rightarrow x_0.\lim\limits_{n \to \infty } f(x_{n})=\lim\limits_{x \to x_0} f(x)$

其中$\lim\limits_{x \to x_0} f(x)=A$ 为函数极限, $x_{n}\rightarrow x$ 为数列,$\lim\limits_{n \to \infty } f(x_{n})$ 为数列极限.

$$
f(x)=
\begin{cases}
x-1 &x<  0\\\\
0 &x=0\\\\
x+1 &x> 0
\end{cases}$$



取数列$x_{n}=\frac{1}{n}\lim\limits_{n \to \infty } f(x_{n})=1$

# 无穷小与无穷大
## 无穷小
错误:$-1000000000000000\cdots$

正确:趋于零

1. 正方向趋于零
2. 负方向趋于零
3. 等于$0$ 

以上三种情况均属于趋于无穷小.

定义:$x \rightarrow x_0 (x \rightarrow \infty )f(x)$ 的极限是$0$ 叫$f(x)$ 是$x \rightarrow x_0 (x \rightarrow \infty )$ 时的无穷小.

无穷小 + 无穷小 无穷小 - 无穷小 无穷小$\times$无穷小 常数$\times$无穷小 都为零

## 无穷大 
$+\infty ,-\infty$ 统称$\infty$ $\lim\limits_{x \to x_0} f(x)=\infty (\lim\limits_{x \to \infty } f(x)=\infty )$ 

定理1:$\infty +\infty$、 $\infty -\infty$ 、 $\frac{\infty }{\infty }、 常数\times\infty$未知.$\infty \times\infty=\infty$

无穷小$\times$无穷大=未知

定理2:$f(x)$无穷大,$\frac{1}{f(x)}$ 无穷小

$f(x)$无穷小,$\frac{1}{f(x)}$无穷大.

## 极限运算法则
定理1:两个无穷小的和是无穷小,**有限个**无穷小的和是无穷小.

定理2(※):有界与无穷小的乘积是无穷小.

有界: $sin,cos$ 及反三角函数.

$\lim\limits_{x \to 0} sin\frac{1}{x}\cdot x=0$ 

推论:
1. 常数$\times$ 无穷小是无穷小.
2. **有限个**无穷小的积是无穷小.

定理3: $\lim f(x)=A ,\lim g(x)=B$ (条件:两者极限存在)

1. $\lim [f(x)\pm g(x)]=\lim f(x)\pm \lim g(x)=A+B$
2. $\lim [f(x)\cdot g(x)]=\lim f(x)\cdot \lim g(x)$ 
3. $\lim \frac{f(x)}{g(x)}=\frac{\lim f(x)}{\lim g(x)}(B\ne 0)$ 

1,2需满足有限个,无限个不成立.(选择题)

$\lim f(x)$ 存在

$\lim [c\cdot  f(x)]=c \cdot \lim f(x)$ 

$\lim [f(x)]^{n}=[\lim f(x)]^{n}$

定理4:数列极限(略)

定理5:$\lim \varphi (x) \geq \psi (x) \lim \varphi (x)\geq \psi (x)$ 注:即使函数1大于函数2,极限也是大于等于.

例1:$\lim\limits_{x \to 1} (2x-1)=\lim\limits_{x \to 1} (2x)-\lim\limits_{x \to 1} 1=2\lim\limits_{x \to 1} x-1=2-1=1$ 

例2:$\lim\limits_{x \to 2} \frac{x^3-1}{x^2-5x+3}=-\frac{7}{3}$(分母不为0时直接代入)

$\lim\limits_{x \to z_0} f(x)=\lim\limits_{x \to x_0} (a_0x^{n}+a_1x^{n-1}+\cdots+a_{n})$ (直接代)

例3:$\lim\limits_{x \to 3} \frac{x-3}{x^2-9}=\lim\limits_{x \to 3} \frac{x-3}{(x+3)(x-3)}=\lim\limits_{x \to 3}\frac{1}{x+3}=\frac{1}{6}$

例4:$\lim\limits_{x \to 1} \frac{2x-3}{x^2-5x+4}=\infty$ 

分子是常数，分母趋于0，则整体趋于无穷。反之趋于0。

例5:$\lim\limits_{z \to \infty } \frac{3x^3+4x^2+2}{7x^3+5x^2-3}=\lim\limits_{x \to \infty } \frac{x+4\frac{1}{x}+\frac{2}{x^3}}{7+5\frac{1}{x}-\frac{3}{x^3}}=\frac{3}{7}$(同除$x^3$)

例6:$\lim\limits_{x \to \infty } \frac{3x^2-2x-1}{2x^3-x+5}=\lim\limits_{x \to \infty } \frac{\frac{3}{x}-\frac{2}{x^2}-\frac{1}{x^3}}{2-\frac{1}{x}+\frac{5}{x^3}}=\frac{0}{2}=0$

例7:$\lim\limits_{x \to \infty } \frac{2x^3-x^2+5}{3x^3-2x-1}=\lim\limits_{x \to \infty } \frac{3-\frac{1}{x}+\frac{3}{x^3}}{3-\frac{2}{x^2}-\frac{1}{x^3}}=\infty$

总结：$x$ 趋于$\infty$ 时，若最高次项次数相等，则结果为最高次项系数相比。若分子次数高于分母，则趋于0，反之则趋于$\infty$ ，低次项可忽略。

$\lim\limits_{x \to x_0}f[g(x)]=\lim\limits_{u \to u_0} f(u)=A$

### 极限存在准则 两个重要极限 夹逼准则
1. 数列$\{x_{n}\}\{y_{n}\}$(1)$\exists n_0\in N使得n> n_0时，y_{n}\leq x_{n}\leq z_{n}则\lim\limits_{n \to \infty } x_{n}=a$(2)$\lim\limits_{v \to \infty } y_{n}=a \lim\limits_{n \to \infty } z_{n}=a$ 

(1)$g(x)\leq f(x)\leq h(x)$ (2)$\lim g(x)=A \lim h(x)=A 则\lim f(x)=A$

(1)$\lim\limits_{x \to 0} \frac{sinx}{x}=1$ 同理$\lim\limits_{x \to 0} \frac{x}{sinx}=1$

i.  $x \rightarrow 0$ ii.$\lim\limits_{() \to 0 }\frac{sin()}{()}$ iii.无$sin$，有$tan,cos,arcsin,arctan$。
无$x$,$\lim\limits_{x \to 0} \frac{sinx}{sin2x}=\lim\limits_{x \to 0} \frac{\frac{sinx}{x}}{\frac{sin2x}{2}}\times\frac{1}{2}=\frac{1}{2} 
\lim\limits_{x \to 0} \frac{tan 2x}{tan 3x}=\lim\limits_{x \to 0} \frac{\frac{sin 2x}{2x}\cdot \frac{1}{cos 2x}}{\frac{sin 3x}{3x}\cdot \frac{1}{cos3x}}\times\frac{2}{3}=\frac{2}{3}$

例1$\lim\limits_{x \to 0} \frac{tanx}{x}=\lim\limits_{x \to 0} \frac{sinx}{x}\cdot \frac{cosx}{1}=\lim\limits_{x \to 0} \frac{sinx}{x}\cdot \lim\limits_{x \to 0} \frac{1}{cosx}=1$

例2$\lim\limits_{x \to 0} \frac{(1-cosx)(1+cosx)}{x^2(1+cosx)}=\lim\limits_{x \to 0} \frac{sin^2x}{x^2}\left(\frac{1}{1+cosx}\right)=\frac{1}{2}$

(3)$\lim\limits_{x \to 0} \frac{arcsinx}{x}=\lim\limits_{t \to 0} \frac{t}{sint}=1$ $(x=sint)$

$\lim\limits_{x \to 0} \frac{tanx÷x}{arcsinx÷x}$

2. **单调有界**数列必有极限。收敛必有界，有界不一定收敛。

$\lim\limits_{x \to \infty } \left(1+\frac{1}{x}\right)^{x}=e=\lim\limits_{x \to 0} (1+x)^{\frac{1}{x}}$


必须是加号。$\lim\limits_{x \to \infty } \left(1-\frac{1}{x}\right)^{x}=\lim\limits_{x \to \infty } [(1+\frac{1}{-x})^{-x}]^{-1}$
$\lim\limits_{x \to \infty } [(1+\frac{1}{3x})^{3x}]^{\frac{2}{3}}$

必须是1。$\lim\limits_{x \to \infty } [(1+\frac{1}{\frac{x}{5}})^{\frac{x}{5}}]^{5}$
$\lim\limits_{x \to \infty } (2+\frac{1}{x})^{x}=\lim\limits_{x \to \infty } 2^{x}[(1+\frac{1}{2x})^{2x}]^{\frac{1}{2}}$不一定（$+\infty$和$-\infty$ )。

例4:$\lim\limits_{x \to \infty } [(1+\frac{1}{-x})^{-x}]^{-1}=e^{-1}$

$\lim\limits_{x \to \infty } [(1+\frac{1}{x})^{-x}]^2=e^2$

$\{x_{n}\}$收敛$\Leftrightarrow \forall \varepsilon \exists N m> N n> N$时，$\lvert x_{n}-x_{m} \rvert <  \varepsilon$

### 无穷小的比较 
$\lim\limits_{x \to 0} x^3 \lim\limits_{x \to 0} x \lim\limits_{x \to 0} \lim\limits_{x \to 0} \sqrt{x} \frac{x^2}{3x} =0 \lim\limits_{x \to 0} \frac{3x}{x^2}=\infty \lim\limits_{x \to 0} \frac{sinx}{3x}=\frac{1}{3}$

$\lim \frac{\beta }{\alpha }=0$ 其中$\alpha \beta$ 是两个函数。高阶无穷小。$\beta =o(\alpha )$

$\lim \frac{\beta }{\alpha }=\infty$ 低阶无穷小。

$\lim \frac{\beta }{\alpha } =C\ne 0$同阶无穷小。

$\lim \frac{\beta }{\alpha ^{k}}=C\ne 0$k阶无穷小，$\beta$趋近于0速度更快。

$\lim \frac{\beta }{\alpha }=1$等价无穷小。记作$\alpha \sim \beta$。

$\lim\limits_{x \to 0} \frac{sinx}{x}=1 sinx \sim x (x \rightarrow 0)$

1. $x \rightarrow 0$时$\sqrt[n]{1+x}-1 \sim \frac{1}{n}x$ 

$(a-1)(a^{n-1}+a^{n-2}+\cdots +a+1)=a^{n}-1$

$a=\sqrt[n]{1+x}$ $\sqrt[n]{1+x}-1=\frac{x}{\sqrt[n]{(1+x)^{n-1}}+\sqrt[n]{(1+x)^{n-2}}+ \cdots +1}$

$\lim\limits_{x \to 0} \frac{\sqrt[n]{1+x}-1}{\frac{1}{n}x}=\lim\limits_{x \to 0} \frac{x}{\sqrt[n]{(1+x)^{n-1}}+\cdots+1}=1$

定理1：$\beta$与$\alpha$等价$\Leftrightarrow \beta = \alpha + o(\alpha)$

定理2：$\alpha \sim \widetilde{\alpha},\beta \sim \widetilde{\beta}$且$\lim \frac{\widetilde{\beta}}{\widetilde{\alpha}}$存在。$\lim \frac{\beta}{\alpha}=\lim \frac{\widetilde{\beta}}{\widetilde{\alpha}}$

$\lim \frac{\beta}{\alpha}=\lim \frac{\beta}{\widetilde{\beta}}\times \frac{\widetilde{\beta}}{\widetilde{\alpha}}\times \frac{\widetilde{\alpha}}{\alpha}=\lim \frac{\widetilde{\beta}}{\widetilde{\alpha}}$

(3)$\lim\limits_{x \to 0} \frac{tan 2x}{sin 5x}=\lim\limits_{x \to 0} \frac{2x}{5x}=\frac{2}{5}$

$tanx \sim x sinx \sim x$

$tan ()\sim () ()\rightarrow 0 sin()\sim () ()\rightarrow 0$

(4)$\lim\limits_{x \to 0} \frac{sinx}{x ^3 +3x}\lim\limits_{x \to 0} \frac{x}{x ^3 +3x}=\lim\limits_{x \to 0} \frac{1}{x^2 +3}=\frac{1}{3}$

(5)$\lim\limits_{x \to 0} \frac{(1 +x^2)^{\frac{1}{3}}-1}{cosx-1}=\lim\limits_{x \to 0} \frac{\frac{1}{3}x^2}{-\frac{1}{2}x^2}=-\frac{2}{3}$

1)两个无穷小比的极限时，分子和分母用等价无穷小替换。
2)分子或分母是若干因子的**乘积**，可对其中一个或几个因子做等价无穷小替换(相加不行)。

连续性

增量(改变量)$\Delta y =f(x_0 +\Delta x)-f(x_0)$

$\lim\limits_{\Delta x \to 0} \Delta y=\lim\limits_{\Delta x \to 0} (f(x_0 +\Delta x)-f(x_0))=0$

$\lim\limits_{\Delta x \to 0} f(x_0 +\Delta x)=f(x_0)$

$\Delta x=x-x_0$

$\lim\limits_{x \to x_0}f(x)=f(x_0)$

连续：
1. 在$x_0$处有极限
2. 在$x_0$处有定义
3. 极限=函数值

左连续：$\lim\limits_{x \to x_0^{-}} f(x)=f(x_0)$

右连续：$\lim\limits_{x \to x_0^{+}} f(x)=f(x_0)$

连续$\Leftrightarrow$左、右连续

几何含义：一笔能画出函数图像。

$y=sinx (-\infty,+\infty)$

证：$x \rightarrow x + \Delta x,\Delta y=sin(x + \Delta x)-sinx=2sin\frac{\Delta x}{2}cos(x + \frac{\Delta x}{2})$

$cos(\alpha \pm \beta)=cos \alpha cos \beta \mp sin \alpha sin \beta$

$sin(\alpha \pm \beta)=sin \alpha cos \beta \pm cos \alpha sin \beta$

$sin \alpha cos \beta=\frac{1}{2}[sin(\alpha +\beta)+sin(\alpha-\beta)]$

$cos \alpha cos \beta =\frac{1}{2}[cos(\alpha +\beta )+cos(\alpha -\beta )]$

$sin \alpha sin \beta =-\frac{1}{2}[cos(\alpha +\beta )-cos(\alpha -\beta )]$

$sin \alpha +sin \beta =2sin\frac{\alpha +\beta }{2}cos\frac{\alpha -\beta }{2}$

$cos \alpha  + cos \beta =2cos\frac{\alpha +\beta }{2}cos\frac{\alpha -\beta }{2}$

$cos \alpha -cos \beta =-2sin\frac{\alpha +\beta }{2}sin\frac{\alpha -\beta }{2}$

$\lim\limits_{\Delta x \to 0} \Delta y=\lim\limits_{\Delta x \to 0} \frac{sin(\frac{\Delta x}{2})}{\frac{\Delta x}{2}}\cdot \Delta x=0$ 其中那一大坨分式$=1,\Delta x=0,cos(x+\frac{\Delta x}{2})=0,$有界。

间断点
1. 在$x_0$处无定义
2. $\lim\limits_{x \to x_0} f(x)$不存在
3. $\lim\limits_{x \to x_0} f(x)\ne f(x_0)$

第1种：$y=tanx ,x=\frac{\pi }{2}无意义，是无穷间断点$。

第2种：$y=sin\frac{1}{x} ,x=0时(震荡)是震荡间断点。$

第3种：$y=\frac{x^2-1}{x-1}在x=1时无意义，是可去间断点。$

第3种(2)：$y=
\begin{cases}
x&&x \ne 1\\\
\frac{1}{2}&&x=1
\end{cases}
$

第4种：$f(x)=
\begin{cases}
x-1&&x <  0\\\
0 &&x=0\\\
x+1&&x > 0
\end{cases}
是跳跃间断点。$

第一类间断点：左右极限都存在：第3、4种间断点。

不符合第一类间断点定义的间断点为第二类间断点：第1、2种间断点。

*闭区间*上连续的性质

(有界性)$[a,b]$连续，有界

(最值性)……必有最大、最小值

(介值性)……值域$[m,M]且m <  c <  M$则必有一点$\xi$满足$f(\xi )=c$

零点存在定理 $[a,b]$连，$f(a)f(b)<  0$(a,b异号)

在$(a,b)$存在一点$\xi$使得$f(\xi)=0$

证：$\varphi (x)=f(x)-C$

$\varphi (a)=f(a)-C=A-C$

$\varphi (b)=f(b)-C=B-C$

$f(\xi)=0, \varphi (\xi)=f(\xi)-C=0$

推论：$[a,b]$连续，值域$[m,M]$则m,M为最值。

(1)$x^3-4x^2+1=0$在$(0,1)$上有一个根。

证：$f(x)=x^3-4x^2+1$在$[0,1]$上连续(闭区间)

$f(0)=1,f(1)=-2$异号

$\exists \xi \in (0,1),s.t.f(\xi)=0$



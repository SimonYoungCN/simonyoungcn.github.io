今天我们再简单了解一下不定积分的第一换元积分法。

由于讲解时间有限，如有部分讲解不清楚之处，敬请见谅！

在我讲解之前，大家应该把最基本的15个积分公式都牢记于心了，如果没有的话，可以再看一下。

(1)$\displaystyle\int k \mathrm{d}x=kx+C$

(2)$\displaystyle\int x^{\mu } \mathrm{d}x=\frac{1}{\mu +1}x^{\mu +1}+C (\mu \ne -1)$

(3)$\displaystyle\int \frac{1}{x} \mathrm{d}x=\ln \lvert x \rvert +C$

(4)$\displaystyle\int \frac{1}{1+x^2} \mathrm{d}x=\arctan x+C$

(5)$\displaystyle\int \frac{1}{\sqrt{1-x^2}} \mathrm{d}x=\arcsin x+C$

(6)$\displaystyle\int \cos x \mathrm{d}x=\sin x+C$

(7)$\displaystyle\int \sin x \mathrm{d}x=-\cos x+C$

(8)$\displaystyle\int \frac{1}{\cos^2x} \mathrm{d}x=\displaystyle\int \sec^2x \mathrm{d}x=\tan x+C$

(9)$\displaystyle\int \frac{1}{\sin^2x} \mathrm{d}x=\displaystyle\int \csc^2x \mathrm{d}x=-\cot x+C$

(10)$\displaystyle\int \sec x\tan x \mathrm{d}x=\sec x+C$

(11)$\displaystyle\int \csc x\cot x \mathrm{d}x=-\csc x+C$

(12)$\displaystyle\int e^{x} \mathrm{d}x=e^{x}+C$

(13)$\displaystyle\int a^{x} \mathrm{d}x=\frac{a^{x}}{\ln a}+C(a > 0,a \ne 1)$

(14)$\displaystyle\int \sinh x \mathrm{d}x=\cosh x+C$

(15)$\displaystyle\int \cosh x \mathrm{d}x=\sinh x+C$

今天我讲的第一换元法的核心其实还是训练整体意识。这一方法也在老师讲微分的时候提到过。

定理如下：

设函数$f(u)$在区间$I$内的函数存在，$u=\varphi (x)$有连续的导数，且$\varphi$的值域包含在$I$中，则有换元公式

$$
\displaystyle\int f[\varphi (x)]\varphi ^{\prime}(x) \mathrm{d}x=\left[\displaystyle\int f(u) \mathrm{d}u \right]_{u=\varphi (x)}
$$

简单来说，就是先把某一函数的导数积分放到$\mathrm{d}$后，然后再以这一函数为整体，将剩下部分积分。

例1 计算不定积分$\displaystyle\int \sin 3x \mathrm{d}x$

原式$=\displaystyle\int \sin 3x \cdot \frac{1}{3} \mathrm{d}(3x)=\frac{1}{3}\cos 3x+C$

例2 计算不定积分$\displaystyle\int x \sqrt{1-x^2} \mathrm{d}x$

原式$= \displaystyle\int -\frac{1}{2}\sqrt{1-x^2} \mathrm{d}(1-x^2)=-\frac{1}{3}(1-x^2)^{\frac{3}{2}}+C$

小结：形如$\displaystyle\int f(ax+b) \mathrm{d}x$的积分，总可以将被积表达式中的$\mathrm{d}x$凑成$\frac{1}{a}(ax+b)$,从而
$$
\displaystyle\int f(ax+b) \mathrm{d}x=\displaystyle\int f(ax+b)\cdot \frac{1}{a} \mathrm{d}(ax+b)=\frac{1}{a}\left [\displaystyle\int f(u) \mathrm{d}u \right ]_{u=ax+b}
$$
例3 计算不定积分$\displaystyle\int \tan x \mathrm{d}x$

原式$=\displaystyle\int \frac{\sin x}{\cos x} \mathrm{d}x=-\displaystyle\int \frac{\mathrm{d}\cos x}{\cos x} \mathrm{d}x=-\ln \lvert \cos x \rvert +C$

例4 计算不定积分$\displaystyle\int \frac{1}{a^2+x^2} \mathrm{d}x$

原式$=\displaystyle\int \frac{1}{a^2}\frac{\mathrm{d}x}{1+(\frac{x}{a})^2}=\frac{1}{a}\displaystyle\int \frac{\mathrm{d}(\frac{x}{a})}{1+(\frac{x}{a})^2}=\frac{1}{a}\arctan \frac{x}{a}+C$

其他类型的微分形式还有很多，比如：
$\frac{1}{x}\mathrm{d}x=\mathrm{d}\ln x,\frac{1}{\sqrt{x}}\mathrm{d}x=2\mathrm{d}\sqrt{x}=\frac{2}{a}\mathrm{d}(a \sqrt{x}+b),$

$e^{x}\mathrm{d}x=\mathrm{d}e^{x},\cos x\mathrm{d}x=\mathrm{d}\sin x,\sin x\mathrm{d}x=-\mathrm{d}\cos x,$

$\sec^2x\mathrm{d}x=\mathrm{d}\tan x, \csc^2x\mathrm{d}x=-\mathrm{d}\cot x,$

$\sec x \tan x\mathrm{d}x=\mathrm{d}\sec x,\frac{1}{1+x^2}\mathrm{d}x=\mathrm{d}\arctan x,$

$\frac{1}{\sqrt{1-x^2}}\mathrm{d}x=\mathrm{d}\arcsin x,\frac{x}{\sqrt{1+x^2}}\mathrm{d}x=\mathrm{d}\sqrt{1+x^2},$

积分时应根据被积函数的特点加以选择使用。

### 第1章 函数、极限、连续

#### 知识结构

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//ff4e52ec-feb5-4c55-aa44-862f9180bb1e/markdown_3/imgs/img_in_image_box_266_403_1171_884.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A26Z%2F-1%2F%2F4bdfe4e6ca580cece144464e898f1231b83882f77f7a4987cd8d8fb628fb12f5" alt="Image" width="62%" /></div>


## 1.1 函数

微积分的主要任务是研究函数的性态及变化规律. 确定函数表达式是研究函数最基本的工作，它可涉及各种初等运算，也可涉及极限、导数、积分、级数等多种非初等运算；函数的单调性与有界性常借助于导数来进行研究；确定函数表达式一般性的方法属于微分方程的范畴. 这些内容我们将在以后的不同章节中讨论，这里以初等方法为主介绍一些有关函数表达式及简单性质的问题. 这些问题虽然较为初等、简单，但它是构成复杂或综合问题的基础.

例1 设  $ f(x)=\begin{cases}e^{x}, & x<1 \\ x, & x\geq1\end{cases} $， $ \varphi(x)=\begin{cases}x+2, & x<0 \\ x^{2}-1, & x\geq0\end{cases} $，求  $ f[\varphi(x)] $。

分析 引入中间变量  $ u = \varphi(x) $，由外层函数定义域的各区间段，通过中间变量得到自变量 x 的对应范围，进而确定中间变量的具体表达式，以得到复合函数.

解 记  $ u = \varphi(x) $，则  $ f[\varphi(x)] = f(u) = \begin{cases} e^u, & u < 1, \\ u, & u \geq 1 \end{cases} $

当u<1时：

当x<0时， $ u=x+2<1\Rightarrow x<-1 $， $ f[\varphi(x)]=e^{x+2} $；

当 $ x\geq0 $时， $ u=x^{2}-1<1\Rightarrow0\leq x<\sqrt{2} $， $ f[\varphi(x)]=e^{x^{2}-1} $

当 $ u \geqslant 1 $时：

当x<0时， $ u=x+2\geq1\Rightarrow-1\leq x<0,\ f[\varphi(x)]=x+2; $

当 $ x\geq0 $时， $ u=x^{2}-1\geq1\Rightarrow x\geq\sqrt{2} $， $ f[\varphi(x)]=x^{2}-1 $。

综上所述，得

 $$ f[\varphi(x)]=\left\{\begin{aligned}{}&{{}\mathsf{e}^{x+2},}&{}&{{}x<-1,}\\ {}&{{}x+2,}&{}&{{}-1\leqslant x<0,}\\ {}&{{}\mathsf{e}^{x^{2}-1},}&{}&{{}0\leqslant x<\sqrt{2},}\\ {}&{{}x^{2}-1,}&{}&{{}x\geqslant\sqrt{2}.}\\ \end{aligned}\right. $$ 

评注 求分段函数的复合函数，其关键是要确定外层函数的自变量在不同段的代入标的，引入中间变量进行讨论是比较清晰的方法。

例2 设  $ f(x)=\lim_{n\to\infty}\sqrt[n]{1+x^n+\left(\frac{x^2}{2}\right)^n} $ (x>0)，求  $ f(x) $ 的显式表达式.

分析 只需算出极限即可. 由于  $ \lim_{n\to\infty}\sqrt[n]{c}=1(c>0) $，所以容易想到极限的夹逼原理.

解 首先证明对于任意有限个正数  $ a_{i}(i=1,2,\cdots,m) $，有

 $$ \lim_{n\to\infty}\sqrt[n]{a_{1}^{n}+a_{2}^{n}+\cdots+a_{m}^{n}}=\max_{1\leq i\leq m}\left\{a_{i}\right\}. $$ 

记 $ \max_{1\leq i\leq m}\left\{a_{i}\right\}=a $，则

 $$ a=\sqrt[n]{a^{n}}\leqslant\sqrt[n]{a_{1}^{n}+a_{2}^{n}+\cdots+a_{m}^{n}}\leqslant\sqrt[n]{ma^{n}}=a\sqrt[n]{m}. $$ 

由于  $ \lim_{n\to\infty}\sqrt[n]{m}=1 $，利用极限的夹逼原理便可得到①式。利用①式，有

 $$ f(x)=\max_{x\in(0,+\infty)}\left\{1,x,\frac{x^{2}}{2}\right\}=\left\{\begin{aligned}&1,&0<x\leq1,\\ &x,&1<x\leq2,\\ &\frac{x^{2}}{2},&x>2.\end{aligned}\right. $$ 

评注 （1）分段函数是微积分中较常见的一类函数，这类函数除有明显的分段表示外，还有一些经常以非分段的形式呈现出来，例如，绝对值函数、取整函数、符号函数、最大（小）值函数，以及由极限形式给出的函数等。在研究这些函数的极限及连续性、可导性、积分性质时，要特别注意其分段点的特殊性。对非分段形式的分段函数要善于识别，并能正确找出其分段点。

(2) 通常情况下，绝对值函数  $ |f(x)| $ 的分段点是方程  $ f(x)=0 $ 的根；最值函数  $ \max\{f(x), g(x)\} $ 与  $ \min\{f(x), g(x)\} $ 的分段点是方程  $ f(x)=g(x) $ 的根；取整函数  $ [f(x)] $ 的分段点是方程  $ f(x)=n (n \in \mathbb{Z}) $ 的根.

例3 设  $ F(x) $ 除 x=0 与1两点外，对全体实数都有定义并且满足等式  $ F(x)+F\left(\frac{x-1}{x}\right)=1+x $ （①式），求函数  $ F(x) $.

分析 将所给等式视为未知函数  $ F(x) $ 的一个方程，如果能通过变量代换得到新的方程，且新方程中没有增加未知函数的不同形式，那么就可通过解方程组来求得  $ F(x) $ 的表达式.

解 设已知等式为①式，将①式中的x换为 $ \frac{x-1}{x} $，得

 $$ F\left(\frac{x-1}{x}\right)+F\left(-\frac{1}{x-1}\right)=\frac{2x-1}{x}, $$ 

将②式中 $ -\frac{1}{x-1} $换成x，得

 $$ F\left(-\frac{1}{x-1}\right)+F(x)=\frac{x-2}{x-1}, $$ 

①+③-②式得

 $$ 2F(x)=1+x+\frac{x-2}{x-1}-\frac{2x-1}{x} $$ 

所以

 $$ F(x)=\frac{x^{3}-x^{2}-1}{2x(x-1)}. $$ 

评注 （1）题解中所作的变量代换 “x 换为  $ \frac{x-1}{x} $”，即为作变量代换  $ x=\frac{t-1}{t} $，再将代换后等式中的 t 写成 x （因为函数与变量的字母选取无关）.

（2）若未知函数及其复合函数满足某个简单的代数方程，作适当的变量代换能得到一个（或多个）新的方程，而新方程中不出现新的函数形式，就可通过解方程组来求得未知函数.

例4 设连续函数  $ f(x) $ 满足方程  $ f(x)-\frac{1}{2}f\left(\frac{x}{2}\right)=x^{2} $，求  $ f(x) $ 的表达式.

分析 已知方程给出了函数的递推关系式，逐次代入，最后求极限就可得到  $ f(x) $ 的表达式.

解 由已知条件，有

 $$ f(x)=\frac{1}{2}f\left(\frac{x}{2}\right)+x^{2}, $$ 

 $$ f\left(\frac{x}{2}\right)=\frac{1}{2}f\left(\frac{x}{2^2}\right)+\left(\frac{x}{2}\right)^2 $$ 

 $$ f\left(\frac{x}{2^{n}}\right)=\frac{1}{2}f\left(\frac{x}{2^{n+1}}\right)+\left(\frac{x}{2^{n}}\right)^{2} $$ 

将上面等式从后往前依次代入，得

 $$ \begin{aligned}f(x)=&\frac{1}{2^{n+1}}f\bigg(\frac{x}{2^{n+1}}\bigg)+\frac{1}{2^{n}}\bigg(\frac{x}{2^{n}}\bigg)^{2}+\frac{1}{2^{n-1}}\bigg(\frac{x}{2^{n-1}}\bigg)^{2}+\cdots+\frac{1}{2}\bigg(\frac{x}{2}\bigg)^{2}+x^{2}\\ =&\frac{1}{2^{n+1}}f\bigg(\frac{x}{2^{n+1}}\bigg)+x^{2}\sum_{k=0}^{n}\frac{1}{2^{3k}}.\end{aligned} $$ 

取  $ n \to \infty $，由 f 的连续性及  $ f(0) = 0 $，可得

 $$ f(x)=x^{2}\frac{1}{1-\frac{1}{8}}=\frac{8}{7}x^{2}\;. $$ 

评注 该题也可视为与例3同类型的问题，只是作变量代换后出现了新的函数，但新函数的变化规律却保持不变，以此下去可得到无穷多个方程（递推关系式），求解时（依次代入）就需用到处理无穷的方法——极限。

例  $ 5^{*} $ 求函数  $ y = f(x) = \sqrt{x^{2} - x + 1} - \sqrt{x^{2} + x + 1} $ 的反函数  $ y = f^{-1}(x) $ 及其定义域.

分析 只需由  $ y = f(x) $ 解关于 x 的方程，得到  $ x = f^{-1}(y) $，再交换变量 x, y 即可.

解 由  $ y=\sqrt{x^{2}-x+1}-\sqrt{x^{2}+x+1} $，易见，当 x>0 时，y<0；当 x<0 时，y>0.

为了解出x，两边平方，得

 $$ y^{2}=x^{2}-x+1+x^{2}+x+1-2\sqrt{(x^{2}+1)^{2}-x^{2}}=2(x^{2}+1)-2\sqrt{x^{4}+x^{2}+1}, $$ 

移项

 $$ 2\sqrt{x^{4}+x^{2}+1}=2(x^{2}+1)-y^{2}. $$ 

两边再平方，化简得

 $$ x^{2}=\frac{y^{2}}{4}\left(\frac{4-y^{2}}{1-y^{2}}\right), $$ 

注意到x与y反号，开方得

 $$ x=-\frac{y}{2}\sqrt{\frac{4-y^{2}}{1-y^{2}}}. $$ 

该函数的定义域为| y |<1 或 | y |≥2．由于 y = f(x) 连续，且 f(0) = 0，故其定义域为{y||y|<1}．改写记号，得所求反函数为

 $$ y=-\frac{x}{2}\sqrt{\frac{4-x^{2}}{1-x^{2}}}, 定义域为 \left\{x\parallel x\mid<1\right\}. $$ 

评注（1）求函数  $ y = f(x) $ 的反函数  $ x = f^{-1}(y) $ 的过程，就是解方程的过程。只有当 f 是其定义域到值域的一一映射时，函数  $ y = f(x) $ 才存在反函数。

(2) 通常情况下  $ f $ 是否为一一映射较难判断，而判断  $ f $ 是否单调（ $ f'(x) $ 不变号）会容易些。单调函数一定有反函数。

例6 设  $ f(x)=(x^{6}+2x^{5}-10x^{4}-12x^{3}+18x^{2}+30x-210)^{2023} $，求  $ f\left(\frac{\sqrt{45}-1}{2}\right) $

分析 直接计算函数值很困难，若令  $ t=\frac{\sqrt{45}-1}{2} $，则有  $ t^{2}+t=11 $，只需将  $ f(t) $ 的表达式拼凑成以  $ t^{2}+t $ 为变量的形式即可.

解 记  $ t=\frac{\sqrt{45}-1}{2} $，则  $ (2t+1)^{2}=45 $，从而知  $ t^{2}+t=11 $，于是

 $$ \begin{aligned}&t^{6}+2t^{5}-10t^{4}-12t^{3}+18t^{2}+30t-210\\ &=(t^{6}+t^{5})+(t^{5}+t^{4})-(11t^{4}+11t^{3})-(t^{3}+t^{2})+(19t^{2}+19t)+11t-210\\ &=(t^{2}+t)(t^{4}+t^{3}-11t^{2}-t+19)+11t-210\\ &=11\Big[(t^{2}+t)t^{2}-11t^{2}-t+19\Big]+11t-210\\ &=11(19-t)+11t-210=11\times19-210\\ &=-1.\\ \end{aligned} $$ 

从而

 $$ f\left(\frac{\sqrt{45-1}}{2}\right)=f(t)=(t^{6}+2t^{5}-10t^{4}-12t^{3}+18t^{2}+30t-210)^{2023}=(-1)^{2023}=-1. $$ 

评注 该题也可用多项式除法，得到  $ f(x)=\left[(x^{2}+x)(x^{4}+x^{3}-11x^{2}-x+19)+11x-210\right]^{2023} $，再代入  $ x^{2}+x=11 $ 来计算.

例  $ 7^{*} $ 已知定义在  $ [0,4] $ 上的函数  $ f(x)=3^{x} $，试先延拓至  $ [-4,0] $，使之成为偶函数，然后再把已延拓至  $ [-4,4] $ 上的函数，延拓至整个实数轴上，使函数成为以 8 为周期的函数.

分析 由偶函数的定义  $ f(-x)=f(x) $，容易得到  $ f(x) $ 在  $ [-4,0] $ 上的表达式；若  $ f(x) $ 以 8 为周期，由于对任一实数 x，都存在整数 k，使  $ 8k-4 \leq x \leq 8k+4 $，则有  $ -4 \leq x-8k \leq 4 $，利用周期性，就容易得到  $ f(x) $ 的表达式了.

解 当  $ x \in [-4,0] $ 时， $ -x \in [0,4] $，若  $ f(x) $ 在  $ [-4,0] $ 上进行延拓后成为偶函数，则

 $$ f(-x)=f(x),\ x\in[-4,4]. $$ 

故当 $ x\in[-4,0] $时，有

 $$ f(x)=f(-x)=3^{-x}. $$ 

因此有

 $$ f(x)=\begin{cases}3^{x},&x\in[0,4],\\3^{-x},&x\in[-4,0].\end{cases} $$ 

如果再将  $ f(x) $ 延拓至整个实数轴上，使之成为以 8 为周期的函数，那么，对于任何实数 x，都唯一地存在整数 k，使

 $$ 8k-4\leq x\leq8k+4. $$ 

当8k-4\leq x\leq 8k时，有-4\leq x-8k\leq 0，此时

 $$ f(x)=f(x-8k)=3^{-(x-8k)}=3^{8k-x}. $$ 

当 $ 8k \leq x \leq 8k+4 $时，有 $ 0 \leq x-8k \leq 4 $，此时

 $$ f(x)=f(x-8k)=3^{x-8k}. $$ 

因此得

 $$ f(x)=\left\{\begin{aligned}{}&{{}3^{-x+8k},}&{8k-4\leqslant x\leqslant8k,}\\ {}&{{}3^{x-8k},}&{8k\leqslant x\leqslant8k+4.}\\ \end{aligned}\right.{~}k\in\mathbb{Z}. $$ 

例8设函数  $ y = f(x) (-\infty < x < +\infty) $ 的图形关于点  $ A(a, y_{1}) $ 和点  $ B(b, y_{2})(a < b) $ 对称，试讨论函数  $ f(x) $ 的周期性.

分析 由函数图形的对称性可知  $ f(a+x)+f(a-x)=2y_1 $， $ f(b+x)+f(b-x)=2y_2 $，只需讨论是否存在常数  $ T \neq 0 $，使得  $ \forall x \in \mathbb{R} $，有  $ f(x)=f(x+T) $。

解 由于函数  $ y = f(x) $ 的图形关于点  $ A(a, y_{1}) $ 和点  $ B(b, y_{2}) $ 对称，则

 $$ f(a+x)+f(a-x)=2y_{1},\quad f(b+x)+f(b-x)=2y_{2}, $$ 

于是

 $$ \begin{aligned}f(x)&=f\big[a+(x-a)\big]=2y_{1}-f\big[a-(x-a)\big]\\&=2y_{1}-f(2a-x)=2y_{1}-f\big[b+(2a-x-b)\big]\\&=2y_{1}-2y_{2}+f\big[b-(2a-x-b)\big]\\&=2(y_{1}-y_{2})+f\big[x+2(b-a)\big].\\ \end{aligned} $$ 

由此可知，当  $ y_{1}=y_{2} $ 时， $ f(x) $ 是周期函数，其周期为 2(b-a).

当 $ y_{1}\neq y_{2} $时，记 $ f(x)=px+q+\varphi(x) $，p和q为常数，由①式得

 $$ \begin{aligned}2(y_{2}-y_{1})&=f\big[x+2(b-a)\big]-f(x)\\&=p\big[x+2(b-a)\big]+q+\varphi\big[x+2(b-a)\big]-\big[px+q+\varphi(x)\big]\\&=2(b-a)p+\varphi\big[x+2(b-a)\big]-\varphi(x).\\ \end{aligned} $$ 

取  $ p=\frac{y_{2}-y_{1}}{b-a} $，则有

 $$ \varphi\big[x+2(b-a)\big]-\varphi(x)=0. $$ 

即  $ \varphi(x) $ 是以 2(b-a) 为周期的函数. 此时  $ f(x) $ 是一线性函数与周期函数之和.

评注 不难看出，若函数  $ y = f(x) (-\infty < x < +\infty) $ 关于 x = a 与  $ x = b (a < b) $ 均对称，则  $ f(x) $ 是以 T = 2(b - a) 为周期的函数.

例 $ 9^* $ 设 $ f $ 是 $ \mathbb{R} $上的下凸函数，即对任意 $ x,y\in\mathbb{R} $及 $ t\in(0,1) $都有

 $$ f(t x+(1-t)y)\leq t f(x)+(1-t)f(y)\;. $$ 

求证： $ g(x)=f(x)+f(-x) $ 在 $ [0,+\infty) $ 上单调递增.

分析 对任意  $ 0 < x_{1} < x_{2} $，需要证明  $ g(x_{1}) \leq g(x_{2}) $ 。根据已知条件，我们容易得到  $ g(x_{1}) \leq \frac{x_{1}}{x_{2}} g(x_{2}) + \left(1 - \frac{x_{1}}{x_{2}}\right) g(0) $，所以只要  $ g(0) \leq g(x_{2}) $，问题就解决了。

证明 首先， $ \forall x \in (0, +\infty) $，有

 $$ g(0)=2f(0)\leqslant2\cdot\frac{1}{2}\big[f(x)+f(-x)\big]=g(x). $$ 

0 < x_{1} < x_{2}，由于  $ \pm x_{1} = \frac{x_{1}}{x_{2}} \cdot (\pm x_{2}) + \left(1 - \frac{x_{1}}{x_{2}}\right) \cdot 0 $，则

 $$ f(x_{1})\leqslant\frac{x_{1}}{x_{2}}f(x_{2})+\left(1-\frac{x_{1}}{x_{2}}\right)f(0),\quad f(-x_{1})\leqslant\frac{x_{1}}{x_{2}}f(-x_{2})+\left(1-\frac{x_{1}}{x_{2}}\right)f(0). $$ 

两式相加得

 $$ f(x_{1})+f(-x_{1})\leqslant\frac{x_{1}}{x_{2}}\big[f(x_{2})+f(-x_{2})\big]+\left(1-\frac{x_{1}}{x_{2}}\right)2f(0), $$ 

即

 $$ g(x_{1})\leqslant\frac{x_{1}}{x_{2}}g(x_{2})+\left(1-\frac{x_{1}}{x_{2}}\right)g(0). $$ 

利用 $ ^{①} $式，有

 $$ g(x_{1})\leqslant\frac{x_{1}}{x_{2}}g(x_{2})+\left(1-\frac{x_{1}}{x_{2}}\right)g(x_{2})=g(x_{2}). $$ 

例  $ 10^{*} $ 设有一实值连续函数，对于所有的实数 x 和 y 满足函数方程  $ f(x+y)=f(x)f(y) $，以及  $ f(1)=2 $。证明： $ f(x)=2^x $。

分析 由于  $ 1 = \underbrace{\frac{1}{n} + \frac{1}{n} + \cdots + \frac{1}{n}}_{n \text{ 个}} $，根据题设条件易得  $ f^n\left(\frac{1}{n}\right) = 2 $，结论对  $ x = \frac{1}{n} $ 是正确的；同样的道理，对  $ x = \frac{m}{n} $ 也是正确的；任一实数均是有理数的极限，所以问题就解决了.

证明 对任何实数 x 都有

 $$ f(x+1)=f(x)f(1)=2f(x)\Rightarrow f(0)=1. $$ 

由于

 $$ f(1)=f\left(\begin{array}{c}\frac{1}{n}+\frac{1}{n}+\cdots+\frac{1}{n}\\ \underbrace{n}_{n 个 }\end{array}\right)=f^{n}\left(\frac{1}{n}\right)=2\ , $$ 

于是  $ f\left(\frac{1}{n}\right)=2^{\frac{1}{n}} $. 对正有理数  $ \frac{m}{n}(n,m\in\mathbb{N}_{+}) $，有

 $$ f\left(\frac{m}{n}\right)=f\left(\begin{array}{c}\frac{1}{n}+\frac{1}{n}+\cdots+\frac{1}{n}\\ \underbrace{n\quad n\quad n}_{m 个 }\end{array}\right)=f^{m}\left(\frac{1}{n}\right)=2^{\frac{m}{n}}. $$ 

则结论对于任何正有理数成立.

当x为负有理数时，有

 $$ 1=f(x-x)=f(x)f(-x)=f(x)2^{-x}\Rightarrow f(x)=2^{x}, $$ 

结论也成立.

对于任何无理数 x，可取有理数列  $ x_{n} \to x $。再由函数的连续性可得

 $$ f(x)=\lim_{n\to\infty}f(x_{n})=\lim_{n\to\infty}2^{x_{n}}=2^{x}. $$ 

所以对任意实数 x 都有  $ f(x)=2^{x} $

评注 由于函数仅满足连续的条件，所以导数、微分等工具都用不上。这种从有理数到实数取极限的方法是较常见的方法。

例  $ 11^{*} $ 是否存在区间  $ [0,1] $ 上的连续函数  $ f(x) $，使得  $ f(x^{2}) = x - f(x) $.

分析 若能由所给条件得到  $ f(x) $ 的表达式，问题就解决了.

解 若存在，显然  $ f(0)=0,\ f(1)=1/2 $ ，且有

 $$ \begin{aligned}f(x)&=x-f(x^{2})=x-x^{2}+f(x^{4})=\cdots\\&=x-x^{2}+x^{4}-x^{8}+\cdots+(-1)^{n}x^{2^{n}}+(-1)^{n+1}f(x^{2^{n+1}}).\end{aligned} $$ 

 $ \forall x \in (0,1) $，由于  $ \lim_{x \to \infty} f(x^{2^{n+1}}) = f(0) = 0 $，得到

 $$ f(x)=x-x^{2}+x^{4}-x^{8}+\cdots+(-1)^{n}x^{2^{n}}+\cdots,0\leqslant x<1. $$ 

即有

 $$ f(x)=\left\{\begin{aligned}&\sum_{n=0}^{\infty}(-1)^{n}x^{2^{n}},&0\leq x<1,\\ &1/2,&x=1.\end{aligned}\right. $$ 

显然该函数在 x=1 不连续，因为  $ \lim_{x\to1^-}f(x) $ 不存在（如取  $ x_n=1-\frac{1}{2^n}\to1^- $）。所以满足题设条件的函数不存在.

评注 像这类存在性问题，通常情况下是很难找出函数表达式的，常用的方法是假设命题成立，在推理中看是否会出现矛盾。

<div style="text-align: center;"><div style="text-align: center;">习题1.1</div> </div>


1. 设  $ g(x)=\begin{cases}2-x, & x \leq 0 \\ x+2, & x > 0\end{cases} $,  $ f(x)=\begin{cases}x^2, & x < 0 \\ -x, & x \geq 0\end{cases} $，求  $ g(f(x)) $.

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//d8c55d04-6122-43ff-8213-6e3c414d47bd/markdown_1/imgs/img_in_image_box_1234_901_1369_1031.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A26Z%2F-1%2F%2F68c9f179c2cfdefd45e64071c97f2694dc426564798fadd112b1efd1f15dc65c" alt="Image" width="9%" /></div>


习题1.1答案

2. 已知  $ f(x) $ 满足等式  $ 2f(x)+x^{2}f\left(\frac{1}{x}\right)=\frac{x^{2}+2x}{x+1} $，求  $ f(x) $ 的表达式.

3. 设  $ f(x)=\lim_{n\to\infty}n\left[\left(1+\frac{x}{n}\right)^n-\mathrm{e}^x\right] $，求  $ f(x) $ 的显式表达式.

4. 设函数  $ f(x) $ 满足方程  $ \sin f(x) - \frac{1}{3}\sin f\left(\frac{x}{3}\right) = x $，求  $ f(x) $ 的表达式.

5. 设函数  $ F(x) $ 是奇函数， $ f(x)=F(x)\left(\frac{1}{a^{x}-1}+\frac{1}{2}\right) $，其中  $ a>0, a\neq1 $．证明： $ f(x) $ 是偶函数.

6*. 设对一切实数 x，有  $ f\left(\frac{1}{2}+x\right)=\frac{1}{2}+\sqrt{f(x)-f^{2}(x)} $，证明  $ f(x) $ 是周期函数.

7. 函数  $ f(x) $ 在  $ (-\infty,+\infty) $ 上满足等式  $ f(3-x)=f(3+x) $， $ f(8-x)=f(8+x) $，且  $ f(0)=0 $，试问：方程  $ f(x)=0 $ 在区间  $ [0,2023] $ 上至少有多少个根？

8. 设  $ y = f(x) $ 在  $ (-\infty, +\infty) $ 上满足  $ f(x + T) = kf(x) $ （其中 T 和 k 是正常数），证明  $ f(x) $ 可表示为  $ f(x) = a^x \varphi(x) $，式中  $ a > 0 $， $ \varphi(x) $ 是以 T 为周期的周期函数.

9. 若对任意x,y，有 $ f(x)-f(y)\leq(x-y)^{2} $，求证对任意正整数n，任意a,b，有

 $$ |f(b)-f(a)|\leqslant\frac{1}{n}(b-a)^{2}. $$ 

10. 求实系数二次多项式  $ p(x) $，使得  $ \forall x \in [-1,1] $，都有  $ \left|p(x)-\frac{1}{x-3}\right|<0.02 $。

 $ 11^* $. 设  $ L $ 是定义在  $ \mathbb{R} $ 上的某些连续函数所构成的集合，满足  $ f(x) \in L $，当且仅当存在常数  $ k $ 使得  $ f(f(x)) = kx^9 $。求  $ k $ 的取值范围。

## 1.2 极限

微积分是建立在极限理论的基础上的。极限反映了变量的局部性态与变化趋势，是实现无穷运算的唯一方法。极限主要包括极限的定义、存在性、相关性质与极限的计算等方面的内容。工科数学尤以极限的计算为主，下面将求极限的常用方法归类介绍。

# 1. 利用初等变形法做计算

用初等运算、变量代换、恒等变形等方法将极限式化简，再由极限的四则运算、复合运算法则求出极限，是极限运算最基本的方法。由于极限四则运算法则的条件是：为有限项，各项极限均存在，分母的极限不为零。所以化简的过程就是使极限式满足运算条件的过程。

例1 计算 $ \lim_{x\to0}\frac{\sqrt{\cos x}-\sqrt[3]{\cos x}}{\sin^{2}x} $.

分析 这是 $ \frac{0}{0} $型极限. 应将分子有理化，进而约去分母中的零因子再求极限. 由于分子的有理化因式较复杂，所以作变量代换更为简便.

解 令 $ \sqrt[6]{\cos x}=u $，则 $ \sin^{2}x=1-u^{12} $

 $$ \begin{aligned} 原式 &=\lim_{u\to1}\frac{u^{3}-u^{2}}{1-u^{12}}=-\lim_{u\to1}\frac{(u-1)u^{2}}{u^{12}-1}=-\lim_{u\to1}\frac{(u-1)u^{2}}{(u-1)(u^{11}+u^{10}+\cdots+u+1)}\\&=-\lim_{u\to1}\frac{u^{2}}{u^{11}+u^{10}+\cdots+u+1}=-\frac{1}{12}\end{aligned} $$ 

评注 对 $ \frac{0}{0} $型的无理分式，分子、分母有理化是消去分母中零因子的有效方法. 当有理化因式较复杂时，作变量代换是比较好的有理化方法.

例2 计算 $ \lim_{x\to1}\frac{(1-x^{\frac{1}{2}})(1-x^{\frac{1}{3}})\cdots(1-x^{\frac{1}{n}})}{(1-x)^{n-1}} $

分析 极限式变形为 $ \lim_{x\to1}\left(\frac{1-x^{\frac{1}{2}}}{1-x}\cdot\frac{1-x^{\frac{1}{3}}}{1-x}\cdots\cdot\frac{1-x^{\frac{1}{n}}}{1-x}\right) $，只需算出各因子 $ \frac{1-x^{\frac{1}{i}}}{1-x}(i=2,3,\cdots,n) $的极限.

解 令 $ x^{\frac{1}{i}}=t $，则

 $$ \lim_{x\to1}\frac{1-x^{\frac{1}{i}}}{1-x}=\lim_{t\to1}\frac{1-t}{1-t^{i}}=\lim_{t\to1}\frac{1}{1+t+\cdots+t^{i-1}}=\frac{1}{i}\;. $$ 

所以

 $$ \lim_{x\to1}\frac{(1-x^{\frac{1}{2}})(1-x^{\frac{1}{3}})\cdots(1-x^{\frac{1}{n}})}{(1-x)^{n-1}}=\lim_{x\to1}\left(\frac{1-x^{\frac{1}{2}}}{1-x}\cdot\frac{1-x^{\frac{1}{3}}}{1-x}\cdot\cdots\cdot\frac{1-x^{\frac{1}{n}}}{1-x}\right)=\frac{1}{2}\cdot\frac{1}{3}\cdot\cdots\cdot\frac{1}{n}=\frac{1}{n!}. $$ 

例3 设数列  $ a_n = \begin{cases} 1, & n \leq k \\ \dfrac{(n+1)^k - n^k}{C_n^{k-1}}, & n > k \end{cases} $ ( $ k \in \mathbb{N}_+ $). 若  $ b_n = 1 + \sum_{k=1}^n (k \lim_{n \to \infty} a_n) $，求  $ \lim_{n \to \infty} \left( \dfrac{b_n^2}{b_{n-1} b_{n+1}} \right)^n $

分析 计算  $ \lim_{n\to\infty}a_n $ 时显然要先将  $ a_n=\frac{(n+1)^k-n^k}{C_n^{k-1}} $ 进行初等运算化简；然后要将  $ b_n $ 的表达式化简才便于计算所求极限.

解 由于

 $$ \lim_{n\to\infty}a_{n}=\lim_{n\to\infty}\frac{(n+1)^{k}-n^{k}}{C_{n}^{k-1}}=\lim_{n\to\infty}\frac{(k-1)!\left[kn^{k-1}+\frac{(k-1)k}{2!}n^{k-2}+\cdots+1\right]}{n(n-1)\cdots(n-k+1)}=k!. $$ 

故

 $$ b_{n}=1+\sum_{k=1}^{n}(k\cdot k!)=(n+1)!\mid( 归纳法易证 )\mid. $$ 

所以

 $$ \lim_{n\to\infty}\left(\frac{b_{n}^{2}}{b_{n-1}b_{n+1}}\right)^{n}=\lim_{n\to\infty}\left(\frac{n}{n+1}\right)^{n}=\mathrm{e}^{-1}. $$ 

评注 ①式最后一个极限式中，方括号[]内仅有第1项 $ kn^{k-1} $除以分母的极限为k，其余各项除以分母的极限均为0；②式对求和的化简至关重要.

例4 计算  $ \lim_{x\to0}\left(\frac{\ln(1+e^{\frac{2}{x}})}{\ln(1+e^{\frac{1}{x}})}-2[x]\right) $，[x] 表示不超过 x 的最大整数.

分析  $ [x] $ 是分段函数，x=0 是分段点，需计算左、右极限.

解

 $$ \operatorname*{l i m}_{x\to0^{-}}\left(\frac{\ln(1+\mathbf{e}^{\frac{2}{x}})}{\ln(1+\mathbf{e}^{\frac{1}{x}})}-2[x]\right)=\operatorname*{l i m}_{x\to0^{-}}\left(\frac{\ln(1+\mathbf{e}^{\frac{2}{x}})}{\ln(1+\mathbf{e}^{\frac{1}{x}})}+2\right)=\operatorname*{l i m}_{x\to0^{-}}\frac{\mathbf{e}^{\frac{2}{x}}}{\mathbf{e}^{\frac{1}{x}}}+2=\operatorname*{l i m}_{x\to0^{-}}\mathbf{e}^{\frac{1}{x}}+2=2\;; $$ 

 $$ \begin{aligned}\lim_{x\to0^{+}}\left(\frac{\ln(1+\mathbf{e}^{\frac{2}{x}})}{\ln(1+\mathbf{e}^{\frac{1}{x}})}-2[x]\right)&=\lim_{x\to0^{+}}\left(\frac{\ln(1+\mathbf{e}^{\frac{2}{x}})}{\ln(1+\mathbf{e}^{\frac{1}{x}})}+0\right)=\lim_{x\to0^{+}}\frac{\ln\left[\mathbf{e}^{\frac{2}{x}}(\mathbf{e}^{\frac{2}{x}}+1)\right]}{\ln\left[\mathbf{e}^{\frac{1}{x}}(\mathbf{e}^{\frac{1}{x}}+1)\right]}\\&=\lim_{x\to0^{+}}\frac{\frac{2}{x}+\ln(1+\mathbf{e}^{\frac{2}{x}})}{\frac{1}{x}+\ln(1+\mathbf{e}^{\frac{1}{x}})}=\lim_{x\to0^{+}}\frac{2+x\ln(1+\mathbf{e}^{\frac{2}{x}})}{1+x\ln(1+\mathbf{e}^{\frac{1}{x}})}=2.\end{aligned} $$ 

故所求极限为2.

评注 求分段函数在分段点的极限，要计算左、右极限；函数  $ a^{\frac{1}{x-x_0}}(a>0, a\neq1) $、 $ \arctan\frac{1}{x-x_0} $、 $ \operatorname{arccot}\frac{1}{x-x_0} $ 中的  $ x_0 $ 类似于分段点.

例5 试确定 a, b, c 的值，使极限等式  $ \lim_{x \to 1} \frac{a(x-1)^2 + b(x-1) + c - \sqrt{x^2 + 3}}{(x-1)^2} = 0 $ 成立.

分析 利用分子是分母的高阶无穷小，可得到几个不同的极限式，从而解出所求的常数.

解 因为

 $$ \lim_{x\to1}\frac{a(x-1)^{2}+b(x-1)+c-\sqrt{x^{2}+3}}{(x-1)^{2}}=0, $$ 

所以

 $$ a(x-1)^{2}+b(x-1)+c-\sqrt{x^{2}+3}=o((x-1)^{2}). $$ 

则有

 $$ \left\{\begin{aligned}&\lim_{x\to1}\left(a(x-1)^{2}+b(x-1)+c-\sqrt{x^{2}+3}\right)=0,\\ &\lim_{x\to1}\frac{a(x-1)^{2}+b(x-1)+c-\sqrt{x^{2}+3}}{x-1}=0.\end{aligned}\right. $$ 

由③式得c=2，代入④式得

 $$ b=\lim_{x\to1}\frac{\sqrt{x^{2}+3}-2}{x-1}=\lim_{x\to1}\frac{x^{2}-1}{(x-1)(\sqrt{x^{2}+3}+2)}=\frac{1}{2}. $$ 

将c=2,  $ b=\frac{1}{2} $代入①式得

 $$ \begin{aligned}a&=-\lim_{x\to1}\frac{\frac{1}{2}(x-1)+2-\sqrt{x^{2}+3}}{(x-1)^{2}}=-\frac{1}{2}\lim_{x\to1}\frac{x+3-2\sqrt{x^{2}+3}}{(x-1)^{2}}\\&=\frac{3}{2}\lim_{x\to1}\frac{(x-1)^{2}}{(x-1)^{2}(x+3+2\sqrt{x^{2}+3})}=\frac{3}{16}.\end{aligned} $$ 

评注 若一个 $ \frac{0}{0} $型极限式中有几个待定常数，可利用分子、分母无穷小的比较及原极限式建立与待定系数个数相同的等式（方程组），再解方程组求得所需的常数. 为得到不同的等式，常使用洛必达法则（见本节例42）. 本题未使用洛必达法则的原因是题设极限式的分子中有无理式，求导后形式更复杂，不利于问题求解.

例6 设  $ x_{1}, x_{2}, \cdots $ 为方程  $ \tan x = x $ 的全体正根按增序排成的数列，求  $ \lim_{n \to \infty} (x_{n} - x_{n-1}) $.

分析 由函数  $ \tan x $ 的周期性，容易得到  $ x_n $ 所在的范围；再考虑到  $ \tan x_n = x_n \to +\infty (n \to \infty) $ 时，只有  $ (x_n - n\pi) \to \frac{\pi}{2} $，问题就解决了。

解 令  $ f(x)=\tan x - x $，由于

 $$ \operatorname*{l i m}_{x\to\left(n\pi-\pi/2\right)^{+}}f(x)=-\infty~,\quad\operatorname*{l i m}_{x\to\left(n\pi+\pi/2\right)^{-}}f(x)=+\infty, $$ 

故在区间 $ \left(n\pi-\frac{\pi}{2},n\pi+\frac{\pi}{2}\right) $内方程 $ f(x)=0 $有根.

又  $ f'(x)=\frac{1}{\cos^{2}x}-1>0 $， $ f(x) $ 在每个子区间  $ \left(n\pi-\frac{\pi}{2},n\pi+\frac{\pi}{2}\right) $ 内均严格单调递增，故根  $ x_{n} $ 唯一。因为  $ \lim \tan x_{-}=\lim x_{+}=+\infty $，所以

 $$ \lim_{n\to\infty}(x_n-n\pi)=\frac{\pi}{2}. $$ 

因此

 $$ \operatorname*{l i m}_{n\to\infty}(x_{n}-x_{n-1})=\operatorname*{l i m}_{n\to\infty}(x_{n}-n\pi)-\operatorname*{l i m}_{n\to\infty}(x_{n-1}-(n-1)\pi)+\pi=\frac{\pi}{2}-\frac{\pi}{2}+\pi=\pi. $$ 

也可用以下方法求得极限：

因为

 $$ \operatorname*{l i m}_{n\to\infty}\operatorname{t a n}(x_{n}-x_{n-1})=\operatorname*{l i m}_{n\to\infty}\frac{\operatorname{t a n}x_{n}-\operatorname{t a n}x_{n-1}}{1+\operatorname{t a n}x_{n}\operatorname{t a n}x_{n-1}}=\operatorname*{l i m}_{n\to\infty}\frac{x_{n}-x_{n-1}}{1+x_{n}x_{n-1}}=\operatorname*{l i m}_{n\to\infty}\frac{1/x_{n-1}-1/x_{n}}{1/x_{n}x_{n-1}+1}=0\;. $$ 

再根据  $ x_{n} $ 所在的范围知  $ \lim_{n\to\infty}(x_{n}-x_{n-1})=\pi $.

例7 设  $ x_{n}=\sum_{k=1}^{n}\frac{k^{3}+6k^{2}+11k+5}{(k+3)!} $，求  $ \lim_{n\to\infty}x_{n} $

分析 随着 n 的增加， $ x_{n} $ 为无穷项的和. 为求极限，需将  $ x_{n} $ 进行初等运算或恒等变形化为有限项和的形式，再用极限的运算法则计算极限.

解 由于  $ k^{3}+6k^{2}+11k+5=(k+1)(k+2)(k+3)-1 $，所以

 $$ \begin{aligned}x_{n}=&\sum_{k=1}^{n}\left(\frac{1}{k!}-\frac{1}{(k+3)!}\right)\\=&\left(\frac{1}{1!}-\frac{1}{4!}\right)+\left(\frac{1}{2!}-\frac{1}{5!}\right)+\left(\frac{1}{3!}-\frac{1}{6!}\right)+\cdots\\&+\left(\frac{1}{(n-2)!}-\frac{1}{(n+1)!}\right)+\left(\frac{1}{(n-1)!}-\frac{1}{(n+2)!}\right)+\left(\frac{1}{n!}-\frac{1}{(n+3)!}\right)\\=&\frac{1}{1!}+\frac{1}{2!}+\frac{1}{3!}-\frac{1}{(n+1)!}-\frac{1}{(n+2)!}-\frac{1}{(n+3)!}\rightarrow&1+\frac{1}{2}+\frac{1}{6}=\frac{5}{3}\quad(n\rightarrow\infty).\end{aligned} $$ 

即 $ \lim_{n\to\infty}x_n=\frac{5}{3} $

评注 求无穷和极限有很多方法，其基本方法之一就是通过初等运算、数列求和公式或恒等变形等方法化为有限运算形式（又称“缩项”），再计算极限。

例8 求  $ \lim_{n\to\infty}\frac{1}{n}\left[\cos\frac{\pi}{4n}+\cos\frac{3\pi}{4n}+\cdots+\cos\frac{(2n-1)\pi}{4n}\right] $

分析 利用三角函数的积化和差公式先 “分拆”，再 “缩项”。

解 由于

 $$ \begin{aligned}x_{n}=&\frac{1}{n}\sum_{k=1}^{n}\cos\frac{(2k-1)\pi}{4n}=\frac{1}{n\cdot2\sin\frac{\pi}{4n}}\sum_{k=1}^{n}2\sin\frac{\pi}{4n}\cos\frac{(2k-1)\pi}{4n}\\=&\frac{1}{n\cdot2\sin\frac{\pi}{4n}}\sum_{k=1}^{n}\left[\sin\frac{k\pi}{2n}-\sin\frac{(k-1)\pi}{2n}\right]\\=&\frac{1}{n\cdot2\sin\frac{\pi}{4n}}\left(\sin\frac{\pi}{2}-\sin0\right),\end{aligned} $$ 

所以  $ \lim_{n\to\infty}x_n=\frac{2}{\pi} $.

评注 这里应用了三角公式： $ 2\cos\alpha\sin\beta=\sin(\alpha+\beta)-\sin(\alpha-\beta) $。其目的是将乘积转化为两项之差（分拆），从而在求和中达到缩项的效果。常用的分拆公式还有：

 $$ \begin{aligned}\frac{1}{(n+a)(n+b)}=&\frac{1}{b-a}\left(\frac{1}{n+a}-\frac{1}{n+b}\right),\\\frac{1}{n(n+1)\cdots(n+l)}=&\frac{1}{l}\left[\frac{1}{n(n+1)\cdots(n+l-1)}-\frac{1}{(n+1)(n+2)\cdots(n+l)}\right].\end{aligned} $$ 

例9 $ ^{*} $ 求  $ \lim_{n\to\infty}\frac{2^{-n}}{n(n+1)}\sum_{k=1}^{n}C_{n}^{k}\cdot k^{2} $

分析 这是无穷和问题，需转化为有限运算形式的极限. 涉及组合数，可考虑用二项公式来处理.

解 对二项公式 $ (1+x)^{n}=\sum_{k=0}^{n}C_{n}^{k}x^{k} $两边求导，得

 $$ n(1+x)^{n-1}=\sum_{k=1}^{n}C_{n}^{k}k x^{k-1}. $$ 

两边乘x，得

 $$ nx(1+x)^{n-1}=\sum_{k=1}^{n}C_{n}^{k}kx^{k}. $$ 

两边再求导，得

 $$ n(1+x)^{n-1}+n(n-1)x(1+x)^{n-2}=\sum_{k=1}^{n}C_{n}^{k}k^{2}x^{k-1}. $$ 

令x=1，得

 $$ \sum_{k=1}^{n}C_{n}^{k}k^{2}=n(n+1)2^{n-2}. $$ 

 $$ \lim_{n\to\infty}\frac{2^{-n}}{n(n+1)}\sum_{k=1}^{n}C_{n}^{k}\cdot k^{2}=\lim_{n\to\infty}\frac{2^{-n}}{n(n+1)}n(n+1)2^{n-2}=\frac{1}{4}. $$ 

2. 利用两个重要极限及等价无穷小做计算

（1）两个重要极限的等价形式：

 $$ \operatorname*{l i m}_{f(x)\to0}\frac{\operatorname{s i n}f(x)}{f(x)}=1\quad,\qquad\operatorname*{l i m}_{f(x)\to\infty}\left(1+\frac{1}{f(x)}\right)^{f(x)}=\mathbf{e}\quad. $$ 

（2）等价无穷小替换定理：设  $ \alpha \sim \alpha' $， $ \beta \sim \beta' $，则  $ \lim \frac{\beta}{\alpha} = \lim \frac{\beta'}{\alpha'} $。

（3）几个常用的等价无穷小：当 $ x\to0 $时，有

 $$ x\sim\sin x\sim\arcsin x\sim\tan x\sim\arctan x\sim\ln(1+x)\sim\mathrm{e}^{x}-1,\ (1+x)^{\alpha}-1\sim\alpha x, $$ 

 $$ 1-\cos x{\sim}\frac{1}{2}x^{2},\quad\tan x-\sin x{\sim}\frac{1}{2}x^{3},\quad\tan x-x{\sim}\frac{1}{3}x^{3},\quad x-\sin x{\sim}\frac{1}{6}x^{3}. $$ 

例10 求极限 $ \lim_{x\to0}\frac{1}{x^{3}}\left[\left(\frac{2+\cos x}{3}\right)^{x}-1\right] $

分析 将分子中的幂指函数转化为指数函数，再用等价无穷小替换.

解 原式= $ \lim_{x\to0}\frac{e^{x\ln\left(\frac{2+\cos x}{3}\right)}-1}{x^{3}}=\lim_{x\to0}\frac{\ln\left(1+\frac{\cos x-1}{3}\right)}{x^{2}}=\lim_{x\to0}\frac{\cos x-1}{3x^{2}}=-\frac{1}{6} $

评注 若极限式中有幂指函数  $ f(x)^{g(x)} $，常用换底公式  $ f(x)^{g(x)} = \mathrm{e}^{g(x)\ln f(x)} $ 将其化为指数函数来处理

例11 求  $ \lim_{x\to1}\frac{1-\sqrt[n]{\cos2n\pi x}}{(x-1)(x^x-1)} $

分析 作变量代换 t = x - 1，化为  $ t \to 0 $ 的情况，再用等价无穷小替换.

解 令 t=x-1，则

 $$ \begin{aligned} 原式 =&\lim_{\substack{t\to0\\ t[(t+1)^{t+1}-1]}}-\lim_{t\to0}\frac{[1+(\cos2n\pi t-1)]^{\frac{1}{n}}-1}{t[\mathrm{e}^{(t+1)\ln(t+1)}-1]}\\=&-\lim_{t\to0}\frac{\frac{1}{n}(\cos2n\pi t-1)}{\frac{n}{t(t+1)\ln(t+1)}}=\lim_{t\to0}\frac{\frac{1}{n}\cdot\frac{1}{2}(2n\pi t)^{2}}{\frac{n}{t^{2}(t+1)}}=2n\pi^{2}.\end{aligned} $$ 

评注 注意等价无穷小：若  $ f(x) \to 1 $，则  $ \sqrt[n]{f(x)} - 1 = \sqrt[n]{1 + [f(x) - 1]} - 1 \sim \frac{1}{n} [f(x) - 1] $.

例 12 计算  $ \lim_{x\to0}\frac{1}{x^2}\left(1-\cos x\cdot\sqrt{\cos2x}\cdot\sqrt[3]{\cos3x}\right) $.

分析 这是 $ \frac{0}{0} $型，将括号中的乘积因子进行分拆，再求各项的极限.为此可在括号中插入 $ (-\cos x+\cos x-\cdots) $来达到分拆的目的.也可做恒等变形 $ \cos x\cdot\sqrt{\cos 2x}\cdot\sqrt[3]{\cos 3x}=e^{\sum_{k=1}^{3}\frac{1}{k}\ln\cos kx} $，用等价无穷小来计算.

 $$ \begin{aligned} 原式 &=\lim_{x\to0}\frac{1}{x^{2}}\Big[(1-\cos x)+\cos x\cdot(1-\sqrt{\cos2x})+\cos x\cdot\sqrt{\cos2x}\cdot(1-\sqrt[3]{\cos3x})\Big]\\&=\lim_{x\to0}\frac{1}{x^{2}}(1-\cos x)+\lim_{x\to0}\frac{1}{x^{2}}(1-\sqrt{\cos2x})+\lim_{x\to0}\frac{1}{x^{2}}(1-\sqrt[3]{\cos3x})\\&=\frac{1}{2}+\frac{1}{2}\lim_{x\to0}\frac{1}{x^{2}}(1-\cos2x)+\frac{1}{3}\lim_{x\to0}\frac{1}{x^{2}}(1-\cos3x)\quad( 见上题评注 )\\&=\frac{1}{2}+1+\frac{3}{2}=3.\end{aligned} $$ 

方法2 原式  $ = \lim_{x \to 0} \frac{1 - e^{\sum_{k=1}^{3} \frac{1}{k} \ln \cos kx}}{x^2} = -\lim_{x \to 0} \frac{\sum_{k=1}^{3} \frac{1}{k} \ln \cos kx}{x^2} = -\sum_{k=1}^{3} \frac{1}{k} \lim_{x \to 0} \frac{\ln \cos kx}{x^2} $

 $ = \sum_{k=1}^{3} \lim_{x \to 0} \frac{\tan kx}{2x} = \frac{1}{2} \sum_{k=1}^{3} k = 3. $

评注从“方法2”可看出，该题的极限形式可推广。一般情形为：

 $$ I_{n}=\lim_{x\to0}\frac{1}{x^{2}}\Big(1-\cos x\cdot\sqrt{\cos2x}\cdot\cdots\cdot\sqrt[n]{\cos nx}\Big)=\frac{1}{2}\sum_{k=1}^{n}k=\frac{1}{4}n(n+1). $$ 

按“方法1”可写为：

 $$ \begin{aligned}I_{k}-I_{k-1}=&\lim_{x\to0}\frac{1}{x^{2}}\Big[\cos x\cdot\sqrt{\cos2x}\cdot\cdots\cdot\sqrt[k-1]{\cos kx}\left(1-\sqrt[k]{\cos kx}\right)\Big]\\ =&\lim_{x\to0}\frac{1}{x^{2}}\Big(1-\sqrt[k]{\cos kx}\Big)=\frac{1}{k}\lim_{x\to0}\frac{1-\cos kx}{x^{2}}=\frac{k}{2}.\end{aligned} $$ 

则

 $$ I_{n}=\sum_{k=2}^{n}(I_{k}-I_{k-1})+I_{1}=\frac{1}{2}\sum_{k=2}^{n}k+I_{1}=\frac{1}{2}\left[\frac{1}{2}n(n+1)-1\right]+I_{1}, $$ 

由于 $ I_{1}=\lim_{x\to0}\frac{1-\cos x}{x^{2}}=\frac{1}{2} $，所以 $ I_{n}=\frac{1}{4}n(n+1) $.

例13 求  $ \lim_{x\to+\infty}\left[\sqrt[k]{(x+a_1)(x+a_2)\cdots(x+a_k)}-x\right] $.

分析 这是  $ \infty - \infty $ 型，令  $ x = \frac{1}{t} $，通分化为  $ \frac{0}{0} $ 型，再用等价无穷小替换.

解 令  $ x = \frac{1}{t} $，则

 $$  原式 =\lim_{t\to0^{+}}\frac{\sqrt[k]{(1+a_{1}t)(1+a_{2}t)\cdots(1+a_{k}t)}-1}{t}. $$ 

因为

 $$ (1+a_{1}t)(1+a_{2}t)\cdots(1+a_{k}t)\;=\;1+\left(\sum_{i=1}^{k}a_{i}\right)t+\left(\sum_{1\leq i<j\leq k}a_{i}a_{j}\right)t^{2}+\cdots+(a_{1}a_{2}\cdots a_{k})t^{k}\;, $$ 

故

 $$ \sqrt[k]{(1+a_{1}t)(1+a_{2}t)\cdots(1+a_{k}t)}-1=\sqrt[k]{1+\left(\sum_{i=1}^{k}a_{i}\right)t+o(t)}-1\sim\frac{1}{k}\left(\sum_{i=1}^{k}a_{i}\right)t+o(t). $$ 

于是

 $$  原式 =\lim_{t\to0^{+}}\frac{\frac{1}{k}\left(\sum_{i=1}^{k}a_{i}\right)t+o(t)}{t}=\frac{a_{1}+a_{2}+\cdots+a_{k}}{k}． $$ 

例14 $ ^{*} $ 记 $ I_{n}=\frac{\overbrace{n\uparrow}^{\pi}\tan\cdots\tan x-\overbrace{\sin\sin\cdots\sin x}^{\pi\uparrow}}{\tan x-\sin x} $，求 $ \lim_{x\to0}I_{n} $

分析 如果  $ I_{n} $ 的分子换为同类函数的差，极限就好计算了. 为此可利用  $ I_{k}-I_{k-1} $ 来实现转换，最后再由  $ I_{n}=\sum_{k=2}^{n}(I_{k}-I_{k-1})+I_{1} $ 求极限.

解 因为  $ I_{k} - I_{k-1} = \frac{\overbrace{\tan \tan \cdots \tan x}^{k \text{个}} - \overbrace{\tan \tan \cdots \tan x}^{(k-1) \text{个}}}{\tan x - \sin x} - \frac{\overbrace{\sin \sin \cdots \sin x}^{k \text{个}} - \overbrace{\sin \sin \cdots \sin x}^{(k-1) \text{个}}}{\tan x - \sin x} $,

由  $ \tan x - x \sim \frac{1}{3} x^{3} $， $ x - \sin x \sim \frac{1}{6} x^{3} (x \to 0) $，知

 $$ \overbrace{\tan\tan\cdots\tan x}^{k 个 }-\overbrace{\tan\tan\cdots\tan x}^{(k-1) 个 }\sim\frac{1}{3}\left(\overbrace{\tan\tan\cdots\tan x}^{(k-1) 个 }\right)^{3}\sim\frac{1}{3}x^{3}, $$ 

 $$ \overbrace{\sin\sin\cdots\sin x}^{k 个 }-\overbrace{\sin\sin\cdots\sin x}^{(k-1) 个 }\sim-\frac{1}{6}(\overbrace{\sin\sin\cdots\sin x}^{(k-1) 个 })^{3}\sim-\frac{1}{6}x^{3}. $$ 

再由  $ \tan x - \sin x \sim \frac{1}{2} x^{3} (x \to 0) $，得

 $$ \lim_{x\to0}(I_{k}-I_{k-1})=\lim_{x\to0}\frac{\frac{1}{3}x^{3}}{\frac{1}{2}x^{3}}-\lim_{x\to0}\frac{-\frac{1}{6}x^{3}}{\frac{1}{2}x^{3}}=\frac{2}{3}+\frac{1}{3}=1\ . $$ 

所以

 $$ \lim_{x\to0}I_{n}=\sum_{k=2}^{n}\lim_{x\to0}(I_{k}-I_{k-1})+\lim_{x\to0}I_{1}=(n-1)+1=n. $$ 

评注 当  $ \lim_{n}I_{n} $ 难算，而  $ \lim(I_{k}-I_{k-1}) $ 容易计算时，常借助公式  $ I_{n}=\sum_{k=2}^{n}(I_{k}-I_{k-1})+I_{1} $ 来计算  $ \lim I_{n} $.

3. 利用无穷小的性质做计算

(1)  $ \lim f(x) = a \Leftrightarrow f(x) = a + o(1) $.

（2）无穷小与局部有界函数的乘积是无穷小

(3)  $ f(x) $ 是无穷小  $ (f(x) \neq 0) \Leftrightarrow \frac{1}{f(x)} $ 是无穷大.

例15 求  $ \lim_{x\to\infty}\frac{x\ln(1+x^{2})+e^{x}\sin x}{x^{2}(1+e^{x})} $

分析 将极限拆分为两项，易得两项的极限均存在.

解

 $$ \frac{x\ln(1+x^{2})+\mathrm{e}^{x}\sin x}{x^{2}(1+\mathrm{e}^{x})}=\frac{\ln(1+x^{2})}{x}\cdot\frac{1}{1+\mathrm{e}^{x}}+\frac{1}{x^{2}}\cdot\frac{\mathrm{e}^{x}\sin x}{1+\mathrm{e}^{x}}. $$ 

由于  $ \lim_{x\to\infty}\frac{\ln(1+x^2)}{x}=\lim_{x\to\infty}\frac{2x}{1+x^2}=0,\quad\lim_{x\to\infty}\frac{1}{x^2}=0 $ ，而  $ \left|\frac{1}{1+e^x}\right|\leq1,\quad\left|\frac{e^x\sin x}{1+e^x}\right|\leq1 $ ，所以

 $$  原式 =\lim_{x\to\infty}\frac{\ln(1+x^{2})}{x}\cdot\frac{1}{1+\mathrm{e}^{x}}+\lim_{x\to\infty}\frac{1}{x^{2}}\cdot\frac{\mathrm{e}^{x}\sin x}{1+\dot{\mathrm{e}}^{x}}=0. $$ 

评注 因为极限式中有函数  $ e^x $，若直接计算极限，需分别讨论  $ x \to -\infty $ 与  $ x \to +\infty $ 的情形.

例16 设  $ \lim_{x\to0}\frac{\sin2x+xf(x)}{\tan x-\sin x}=0 $ 求 a,b，使  $ x\to0 $ 时， $ f(x)+2 $ 与  $ ax^{b} $ 为等价无穷小.

分析 由所给极限式可得到  $ f(x) $ 在 x=0 附近的局部表达式，再做相关运算.

解 因为当  $ x \to 0 $ 时， $ \tan x - \sin x = \tan x (1 - \cos x) \sim \frac{1}{2} x^{3} $，则

 $$ \lim_{x\to0}\frac{\sin2x+xf(x)}{\tan x-\sin x}=0\Rightarrow\lim_{x\to0}\frac{\sin2x+xf(x)}{x^{3}}=0 $$ 

所以

 $$ \sin2x+x f(x)=o(x^{3})\Longrightarrow f(x)=\frac{-\sin2x+o(x^{3})}{x}. $$ 

利用泰勒公式  $ \sin 2x = 2x - \frac{(2x)^3}{3!} + o(x^3) $，代入上式得

 $$ f(x)=-2+\frac{4}{3}x^{2}+o(x^{2})\Rightarrow f(x)+2\sim\frac{4}{3}x^{2}(x\to0). $$ 

因此， $ a=\frac{4}{3} $，b=2.

评注 利用已知极限式得到其中抽象函数的局部表达式，再做相关运算，这是处理局部问题（如极限、极值等）较常用的方法。

例17 设命题：若函数  $ f(x) $ 在 x=0 处连续，且

 $$ \lim_{x\to0}\frac{f(2x)-f(x)}{x}=a\ (a 为常数 ), $$ 

则  $ f(x) $ 在 x=0 处可导，且  $ f'(0)=a $

判断该命题是否成立. 若成立，则给出证明；若不成立，则举出反例.

分析 由所给极限式可得到  $ f(x) $ 在 x=0 附近的局部表达式，再讨论是否有  $ \lim_{x\to0}\frac{f(x)-f(0)}{x}=a $

解 由于  $ \lim_{x\to0}\frac{f(2x)-f(x)}{x}=a $ ，所以

 $$ f(2x)=f(x)+ax+o(x)\quad( 在 x=0 附近 ). $$ 

此式等价于

 $$ f(x)=f\left(\frac{x}{2}\right)+\frac{1}{2}\big(ax+o(x)\big). $$ 

递推可得

 $$ \begin{aligned}f(x)=&\Biggl(f\Biggl(\frac{x}{2^{2}}\Biggr)+\frac{1}{2^{2}}\bigl(ax+o(x)\bigr)\Biggr)+\frac{1}{2}\bigl(ax+o(x)\bigr)=f\Biggl(\frac{x}{2^{2}}\Biggr)+\Biggl(\frac{1}{2}+\frac{1}{2^{2}}\Biggr)\bigl(ax+o(x)\bigr)\\ =&\cdots=f\Biggl(\frac{x}{2^{n}}\Biggr)+\Biggl(\frac{1}{2}+\frac{1}{2^{2}}+\frac{1}{2^{3}}+\cdots+\frac{1}{2^{n}}\Biggr)\bigl(ax+o(x)\bigr).\end{aligned} $$ 

由于 $ \lim_{n\to\infty}\left(\frac{1}{2}+\frac{1}{2^2}+\cdots+\frac{1}{2^n}\right)=1 $， $ \lim_{n\to\infty}\frac{x}{2^n}=0 $，且 $ f(x) $在x=0处连续。在上式中令 $ n\to\infty $，可得

 $$ f(x)=f(0)+ax+o(x). $$ 

所以  $ f'(0) = \lim_{x \to 0} \frac{f(x) - f(0)}{x} = a $．原命题是正确的.

评注 注意，若去掉题设中的条件 “ $ f(x) $ 在 x=0 连续”，则命题就不一定正确。读者可考察函数  $ f(x)=\begin{cases}x+1, & x \leq 0 \\ x, & x > 0\end{cases} $。显然  $ \lim_{x \to 0} \frac{f(2x)-f(x)}{x} = \lim_{x \to 0} \frac{x}{x} = 1 $，但  $ f(x) $ 在 x=0 处不可导。

例18 $ ^{*} $ 设 $ \lim_{n\to\infty}a_n=A $， $ \lim_{n\to\infty}b_n=B $，记 $ c_n=\frac{a_1b_n+a_2b_{n-1}+\cdots+a_nb_1}{n} $，求证： $ \lim_{n\to\infty}c_n=AB $

分析 只需证明  $ c_{n}=AB+\gamma_{n} $， $ \gamma_{n}\to0(n\to\infty) $. 为此，可将已知条件写成  $ a_{n}=A+\alpha_{n} $， $ b_{n}=B+\beta_{n} $，其中  $ \alpha_{n}\to0 $， $ \beta_{n}\to0(n\to\infty) $，再做运算.

证明 因为  $ \lim_{n\to\infty}a_n=A $， $ \lim_{n\to\infty}b_n=B $，则有  $ a_n=A+\alpha_n $， $ b_n=B+\beta_n $，其中  $ \alpha_n\to0 $， $ \beta_n\to0(n\to\infty) $。

于是

 $$ \begin{aligned}{c_{n}=}&{{}\frac{1}{n}[(A+\alpha_{1})(B+\beta_{n})+(A+\alpha_{2})(B+\beta_{n-1})+\cdots+(A+\alpha_{n})(B+\beta_{1})]}\\ {=}&{{}A B+\frac{B}{n}(\alpha_{1}+\alpha_{2}+\cdots+\alpha_{n})+\frac{A}{n}(\beta_{1}+\beta_{2}+\cdots+\beta_{n})+\frac{1}{n}(\alpha_{1}\beta_{n}+\alpha_{2}\beta_{n-1}+\cdots+\alpha_{n}\beta_{1})\;.}\\ \end{aligned} $$ 

由数列极限的施笃兹定理（见本节8），有

 $$ \operatorname*{l i m}_{n\to\infty}\frac{1}{n}(\alpha_{1}+\alpha_{2}+\cdots+\alpha_{n})=\operatorname*{l i m}_{n\to\infty}\alpha_{n}=0~{,}\quad\operatorname*{l i m}_{n\to\infty}\frac{1}{n}(\beta_{1}+\beta_{2}+\cdots+\beta_{n})=\operatorname*{l i m}_{n\to\infty}\beta_{n}=0{.} $$ 

再由  $ \{\alpha_n\} $ 有界， $ \exists M > 0 $，使得  $ \forall n \in \mathbb{N} $，有  $ |\alpha_n| \leq M $，于是

 $$ 0\leqslant\frac{1}{n}\mid\alpha_{1}\beta_{n}+\alpha_{2}\beta_{n-1}+\cdots+\alpha_{n}\beta_{1}\mid\leqslant\frac{M}{n}\mid\beta_{1}+\beta_{2}+\cdots+\beta_{n}\mid\rightarrow0\left(n\rightarrow\infty\right), $$ 

所以

 $$ \operatorname*{l i m}_{n\to\infty}\frac{1}{n}(\alpha_{1}\beta_{n}+\alpha_{2}\beta_{n-1}+\cdots+\alpha_{n}\beta_{1})=0~. $$ 

综上，在①式中令  $ n \to \infty $，即得  $ \lim_{n \to \infty} c_n = AB $。

评注 关系式 $ \lim f(x)=a\Leftrightarrow f(x)=a+o(1) $将极限问题转换成了函数或无穷小的运算问题，这为解决某些局部问题带来许多方便.

# 4. 利用极限存在的原理做计算

（1）归并原理： $ \lim_{n \to \infty} a_n = a $ 的充要条件是对于  $ \{a_n\} $ 的任意一个子列  $ \{a_{n_k}\} $ 都有  $ \lim_{k \to \infty} a_{n_k} = a $。特别地，设  $ m \in \mathbb{N} $，则  $ \lim_{n \to \infty} a_n = a $ 的充要条件是  $ \lim_{k \to \infty} a_{km+i} = a $ ( $ i = 0, 1, \cdots, m-1 $)。

（2）夹逼原理：设  $ \lim_{n\to\infty}a_n=\lim_{n\to\infty}b_n=a $，若  $ \exists M\in\mathbb{N} $，当  $ n>M $ 时，恒有  $ a_n\leq c_n\leq b_n $，则  $ \lim_{n\to\infty}c_n=a $

（3）单调有界原理：单调递增（减）有上（下）界的数列必定收敛.

例 19 设  $ x_{n}=\frac{1}{n}\cdot\left|1-2+3-\cdots+(-1)^{n+1}n\right| $，求  $ \lim_{n\to\infty}x_{n} $.

分析 这是无穷和形式的极限，需要缩项。缩项就需要讨论 n 的奇、偶，故需要求子列  $ \{x_{2n}\} $ 与  $ \{x_{2n+1}\} $ 的极限。

解

 $$ \begin{aligned}x_{2n}=&\frac{1}{2n}\cdot\left|1-2+3-\cdots+(2n-1)-2n\right|\\=&\frac{1}{2n}\cdot\left|(1+3+\cdots+(2n-1))-(2+4+\cdots+2n)\right|=\frac{1}{2n}\cdot\left|n^{2}-(n^{2}+n)\right|=\frac{1}{2},\end{aligned} $$ 

 $$ \begin{aligned}x_{2n+1}=&\frac{1}{2n+1}\cdot\left|1-2+3-\cdots-2n+(2n+1)\right|\\=&\frac{1}{2n+1}\cdot\left|(1+3+\cdots+(2n+1))-(2+4+\cdots+2n)\right|\\=&\frac{1}{2n+1}\cdot\left|(n^{2}+2n+1)-(n^{2}+n)\right|=\frac{n+1}{2n+1}.\end{aligned} $$ 

由于 $ \lim_{n\to\infty}x_{2n}=\frac{1}{2} $， $ \lim_{n\to\infty}x_{2n+1}=\frac{1}{2} $，故 $ \lim_{n\to\infty}x_n=\frac{1}{2} $.

评注 当  $ x_{n} $ 不能用一个式子表示，或  $ x_{n} $ 的性态随不同的子列而相异时，常用“归并原理”来研判其极限.

例  $ 20^{*} $ 对数列  $ \{a_{n}\} $，若存在正整数 p 使得  $ \lim_{n\to\infty}(a_{n+p}-a_{n})=\lambda $，证明  $ \lim_{n\to\infty}\frac{a_{n}}{n}=\frac{\lambda}{p} $.

分析 记  $ n=kp+i,\ i\in\{0,1,\cdots,p-1\} $，则  $ \lim_{n\to\infty}(a_{n+p}-a_n)=\lambda\Leftrightarrow\lim_{k\to\infty}(a_{(k+1)p+i}-a_{kp+i})=\lambda $，从而只需证明  $ \lim_{k\to\infty}\frac{a_{(k+1)p+i}}{(k+1)p+i}=\frac{\lambda}{p} $.

证明 因为对任意自然数  $ n \geq p $，有  $ n = kp + i $，其中  $ k \in \mathbb{N} $， $ i \in \{0,1,\cdots,p-1\} $。因此由题设条件可得

 $$ \operatorname*{l i m}_{k\to\infty}(a_{(k+1)p+i}-a_{k p+i})=\lambda\;(i=0,1,\cdots,p-1). $$ 

方法1 记  $ A_{k}^{(i)}=a_{(k+1)p+i}-a_{kp+i} $ (i=0,1, $ \cdots $,p-1)，由于  $ \lim_{k\to\infty}A_{k}^{(i)}=\lambda $，则

 $$ \lim_{k\to\infty}\frac{A_{1}^{(i)}+A_{2}^{(i)}+\cdots+A_{k}^{(i)}}{k}=\lambda. $$ 

而  $ A_{1}^{(i)} + A_{2}^{(i)} + \cdots + A_{k}^{(i)} = a_{(k+1)p+i} - a_{p+i} $， $ \lim_{k \to \infty} \frac{a_{p+i}}{k} = 0 $，所以

 $$ \lambda=\operatorname*{l i m}_{k\to\infty}\frac{a_{(k+1)p+i}}{k}=\operatorname*{l i m}_{k\to\infty}\left[\frac{a_{(k+1)p+i}}{(k+1)p+i}\cdot\frac{(k+1)p+i}{k}\right]=p\operatorname*{l i m}_{k\to\infty}\frac{a_{(k+1)p+i}}{(k+1)p+i}\;, $$ 

即

 $$ \lim_{k\to\infty}\frac{a_{(k+1)p+i}}{(k+1)p+i}=\frac{\lambda}{p}(i=0,1,\cdots,p-1). 故 \lim_{n\to\infty}\frac{a_{n}}{n}=\frac{\lambda}{p}. $$ 

方法2 使用施笃兹定理（见本节后面介绍）：

 $$ \lim_{k\to\infty}\frac{a_{(k+1)p+i}}{(k+1)p+i}=\lim_{k\to\infty}\frac{a_{(k+1)p+i}-a_{kp+i}}{(k+1)p+i-(kp+i)}=\frac{\lambda}{p}. $$ 

例21 求  $ \lim_{n\to\infty}\left(\frac{1}{n^{2}+n+1}+\frac{2}{n^{2}+n+2}+\cdots+\frac{n}{n^{2}+n+n}\right) $.

分析　这是无穷和形式的极限. 为化简数列，可将各分式的分母做适当的放大与缩小（形成公分母）达到通分化简的效果，再用夹逼原理求极限.

解 记  $ x_{n}=\frac{1}{n^{2}+n+1}+\frac{2}{n^{2}+n+2}+\cdots+\frac{n}{n^{2}+n+n} $，则

 $$ \frac{1+2+\cdots+n}{n^{2}+n+n}<x_{n}<\frac{1+2+\cdots+n}{n^{2}+n+1}. $$ 

因为

 $$ \lim_{n\to\infty}\frac{1+2+\cdots+n}{n^{2}+n+n}=\lim_{n\to\infty}\frac{1}{2}\cdot\frac{n(n+1)}{n^{2}+2n}=\frac{1}{2} $$ 

 $$ \lim_{n\to\infty}\frac{1+2+\cdots+n}{n^{2}+n+1}=\lim_{n\to\infty}\frac{1}{2}\cdot\frac{n(n+1)}{n^{2}+n+1}=\frac{1}{2}. $$ 

根据夹逼原理得  $ \lim_{n\to\infty}x_n=\frac{1}{2} $

评注 （1）用夹逼原理求极限  $ \lim_{n\to\infty}c_n $ 的关键是将数列  $ c_n $ 做适当的缩小与放大来得到  $ a_n $ 与  $ b_n $ ，即  $ a_n\leq c_n\leq b_n $ ，且  $ a_n $ 与  $ b_n $ 有相同的极限. 对函数极限的情形也是类似的道理.

（2）夹逼原理常用于求（数列极限中）无穷和的极限问题。若和的各项为分式，且各分母不同（但为等价无穷大），则可通过各项分母的放缩（保持等价性）以形成公分母，达到通分化简的效果，再用夹逼原理求极限。

例 22 求极限  $ \lim_{n\to\infty}\sum_{k=1}^{n}(n+1-k)[nC_{n}^{k}]^{-1} $.

分析　这是无穷和形式的极限，将通项写成分式后做适当的放大与缩小，再用夹逼原理.

解  $ C_{n}^{k}=\frac{n(n-1)\cdots(n-k+1)}{k!} $. 当 k<n 时，有

 $$ (n+1-k)\left(nC_{n}^{k}\right)^{-1}=n^{-2}\frac{k!}{(n-1)\cdots(n-k+2)}\leqslant2n^{-2}, $$ 

因此

 $$ 0<\sum_{k=1}^{n}(n+1-k)\Big(nC_{n}^{k}\Big)^{-1}\leqslant2\sum_{k=1}^{n-1}n^{-2}+\frac{1}{n}<\frac{2}{n}+\frac{1}{n}=\frac{3}{n}\to0(n\to\infty). $$ 

所以  $ \lim_{n \to \infty} \sum_{k=1}^{n} (n+1-k) [nC_n^k]^{-1} = 0 $.

例 23 求极限  $ \lim_{n \to \infty} \frac{1}{\ln n} \sum_{k=1}^{n} \frac{1}{k} $.

分析 分母是  $ \ln n $，分子最好能用对应的函数形式来估计。由于  $ (\ln x)'|_{x=k}=\frac{1}{k} $，所以想到用定积分的不等式性质来对分子做放大与缩小。

解 由于  $ y=\frac{1}{x} $ 在 x>0 时单调递减，则

 $$ \int_{k}^{k+1}\frac{1}{x}\mathrm{d}x\leqslant\frac{1}{k}\leqslant\int_{k-1}^{k}\frac{1}{x}\mathrm{d}x, $$ 

 $$ \int_{1}^{n+1}\frac{1}{x}\mathrm{d}x=\sum_{k=1}^{n}\int_{k}^{k+1}\frac{1}{x}\mathrm{d}x\leqslant\sum_{k=1}^{n}\frac{1}{k}\leqslant\sum_{k=2}^{n}\int_{k-1}^{k}\frac{1}{x}\mathrm{d}x+1=\int_{1}^{n}\frac{1}{x}\mathrm{d}x+1. $$ 

即

 $$ \ln(n+1)\leqslant\sum_{k=1}^{n}\frac{1}{k}\leqslant\ln n+1\Rightarrow\frac{\ln(n+1)}{\ln n}\leqslant\frac{1}{\ln n}\sum_{k=1}^{n}\frac{1}{k}\leqslant\frac{\ln n+1}{\ln n}. $$ 

由于 $ \lim_{n\to\infty}\frac{\ln(n+1)}{\ln n}=1=\lim_{n\to\infty}\frac{\ln n+1}{\ln n} $，所以 $ \lim_{n\to\infty}\frac{1}{\ln n}\sum_{k=1}^{n}\frac{1}{k}=1 $

评注（1）该题还有一些更简单的解法，如用后面将要讲到的施笃兹定理；还可以用例30的结论，将分子表示为 $ \sum_{k=1}^{n}\frac{1}{k}=\ln n+C+\alpha_{n}(\alpha_{n}\rightarrow0) $等.

（2）该题求解中用函数的积分来放大或缩小离散和的方法值得借鉴. 离散和不易计算，而积分具

有区间可加性，容易计算. 读者不妨用该方法计算  $ \sum_{n=1}^{100}\frac{1}{\sqrt{n}} $ 的整数部分是多少.

例24 证明  $ \lim_{x \to 0} \cos \cos \cdots \cos x $ 存在，且其极限是方程  $ \cos x - x = 0 $ 的根.

分析 数列的递推关系式为  $ x_{n+1} = \cos x_n $ 。若  $ a $ 是方程  $ \cos x - x = 0 $ 的根，只需证明  $ |x_{n+1} - a| $ 是  $ n $ 充分大时的无穷小量。

证明 令  $ f(x)=\cos x - x $，则  $ f(0)=1>0 $， $ f(1)=\cos 1 - 1 < 0 \Rightarrow \cos x - x = 0 $ 在  $ (0,1) $ 内有根，设根为  $ a $，即  $ a = \cos a $。

以下证明  $ \lim_{n \to \infty} \underbrace{\cos \cos \cdots \cos x}_{n 个} = a $.

记  $ x_{1}=\cos x $， $ x_{n+1}=\cos x_{n} $ （ $ n=2,3,\cdots $），则

 $$ \begin{aligned}\left|x_{n+1}-a\right|&\models\cos x_{n}-\cos a\mid=\left|\sin\xi_{n}\cdot(x_{n}-a)\right|\quad(\xi_{n} 介于 a 与 x_{n} 之间 )\\&\leq\sin1\cdot\left|x_{n}-a\right|\quad\left(\because\left|\xi_{n}\right|\leq1\right)\\&\leq\left(\sin1\right)^{2}\mid x_{n-1}-a\mid\leq\cdots\leq\left(\sin1\right)^{n}\mid x_{1}-a\mid\rightarrow0\left(n\rightarrow\infty\right).\end{aligned} $$ 

所以  $ \lim_{n\to\infty}x_n=a $，即  $ \lim_{n\to\infty}\underbrace{\cos\cos\cdots\cos x}_{n个}=a $。

评注 在用夹逼原理证明由递推公式给出的数列的极限时，拉格朗日中值公式常常是有效的工具.

例25 已知  $ a_{n}=\int_{0}^{n}\frac{\arctan\frac{x}{n}}{(1+x)(1+x^{2})}dx,\quad n=1,2,\cdots $ ，求  $ \lim_{n\to\infty}na_{n} $

分析 显然  $ a_{n} $ 的积分没法计算出来，困难在于被积函数中的分子  $ \arctan\frac{x}{n} $，若能将分子用 x 的多项式来做双向估计，并保持放大与缩小后的极限不变，问题就解决了.

解 根据不等式：t>0 时， $ t>\arctan t>t-\frac{1}{3}t^{3} $（用函数的单调性容易证明），可得

 $$ n\int_{0}^{n}\frac{\frac{x}{n}-\frac{1}{3}\left(\frac{x}{n}\right)^{3}}{(1+x)(1+x^{2})}\mathrm{d}x<n a_{n}<\int_{0}^{n}\frac{x}{(1+x)(1+x^{2})}\mathrm{d}x\;. $$ 

注意到

 $$ \begin{aligned}n\int_{0}^{n}&\frac{\frac{x}{n}-\frac{1}{3}\left(\frac{x}{n}\right)^{3}}{(1+x)(1+x^{2})}\mathrm{d}x=\int_{0}^{n}\frac{x}{(1+x)(1+x^{2})}\mathrm{d}x-\frac{1}{3n^{2}}\int_{0}^{n}\frac{x^{3}}{(1+x)(1+x^{2})}\mathrm{d}x\\&\lim_{n\rightarrow\infty}\int_{0}^{n}\frac{x}{(1+x)(1+x^{2})}\mathrm{d}x=\lim_{n\rightarrow\infty}\frac{1}{2}\int_{0}^{n}\left(\frac{1+x}{1+x^{2}}-\frac{1}{1+x}\right)\mathrm{d}x\\&=\lim_{n\rightarrow\infty}\left[\frac{1}{2}\arctan x+\frac{1}{4}\ln\frac{1+x^{2}}{(1+x)^{2}}\right]_{0}^{n}=\frac{\pi}{4}.\\&\lim_{n\rightarrow\infty}\frac{1}{3n^{2}}\int_{0}^{n}\frac{x^{3}}{(1+x)(1+x^{2})}\mathrm{d}x=\lim_{t\rightarrow+\infty}\frac{\int_{0}^{t}\frac{x^{3}}{(1+x)(1+x^{2})}\mathrm{d}x}{t^{2}}\\&=\lim_{t\rightarrow+\infty}\frac{\frac{t^{3}}{(1+t)(1+t^{2})}}{2t}=\frac{1}{2}\lim_{t\rightarrow+\infty}\frac{t^{2}}{(1+t)(1+t^{2})}=0.\end{aligned} $$ 

且

对①式应用夹逼原理，得  $ \lim_{n\to\infty}na_n=\frac{\pi}{4} $.

评注  $ t > \arctan t > t - \frac{1}{3}t^{3} (t > 0) $ 是较为常见的基本不等式，了解它对某些问题的解决会有帮助.

例26 设数列 $ \{a_{n}\} $满足条件 $ (2-a_{n})a_{n+1}=1,n\geq1 $。证明 $ \lim_{n\to\infty}a_{n} $存在且等于1。

分析 数列由递推关系式给出，常用单调有界原理证明极限存在，再设法求出极限. 若能由递推公式求出数列的通项表达式，再求极限就更为方便了.

解 方法1 考察数列的单调性与有界性.

 $$ a_{n+1}-a_{n}=\frac{1}{2-a_{n}}-a_{n}=\frac{(1-a_{n})^{2}}{2-a_{n}}. $$ 

若 $ a_{n}<2 $，则有 $ a_{n+1}-a_{n}>0 $， $ \{a_{n}\} $单调递增有上界，所以 $ \{a_{n}\} $收敛.

若有某个 $ a_n > 2 $，由 $ a_{n+1} = \frac{1}{2 - a_n} $知，存在 $ p > n $，使 $ a_p \leq a_{p+1} \leq a_{p+2} \leq \cdots \leq 1 $， $ \{a_n\} $也收敛。设 $ \lim_{n \to \infty} a_n = A $，在 $ (2 - a_n)a_{n+1} = 1 $的两边取极限，得

 $$ (2-A)A=1. $$ 

解这个方程得 A = 1. 即  $ \lim_{n \to \infty} a_n = 1 $.

方法2 若 $ \exists m \in \mathbb{N} $，使 $ a_m = 1 $，则 $ \forall n > m $，有 $ a_n = 1 $，所以 $ \lim_{n \to \infty} a_n = 1 $。

若  $ \forall a_{n}\neq1 $ ，令  $ b_{n}=a_{n}-1 $ ，由题设条件有

 $$ (1-b_{n})(1+b_{n+1})=1\Rightarrow\frac{1}{b_{n+1}}-\frac{1}{b_{n}}=-1\Rightarrow b_{n}=\frac{1}{\frac{1}{b_{1}}+1-n}\rightarrow0, $$ 

所以 $ \lim_{n\to\infty}a_n=1 $

例 27 设  $ F(x,y)=\frac{f(y-x)}{2x} $， $ F(1,y)=\frac{y^{2}}{2}-y+5 $， $ x_{0}>0 $， $ x_{1}=F(x_{0},2x_{0}) $， $ \cdots $， $ x_{n+1}=F(x_{n},2x_{n}) $， $ (n=1,2,\cdots) $。证明  $ \lim_{x\to\infty}x_n $ 存在，并求该极限。

分析 求出  $ F(x,y) $ 的表达式就知道了数列  $ x_{n} $ 的递推关系式，再用单调有界原理求极限.

解 令x=1， $ \frac{f(y-1)}{2}=F(1,y)=\frac{y^{2}}{2}-y+5 $，即有

 $$ f(y-1)=y^{2}-2y+10=(y-1)^{2}+9. $$ 

从而

 $$ f(y-x)=(y-x)^{2}+9,\quad F(x,y)=\frac{(y-x)^{2}+9}{2x}. $$ 

则

 $$ x_{1}=\frac{(2x_{0}-x_{0})^{2}+9}{2x_{0}}=\frac{x_{0}^{2}+9}{2x_{0}}, $$ 

 $$ x_{n+1}=\frac{x_{n}^{2}+9}{2x_{n}}=\frac{1}{2}\left(x_{n}+\frac{9}{x_{n}}\right)\geqslant\sqrt{x_{n}\cdot\frac{9}{x_{n}}}=3\left( 有下界 \right). $$ 

又

 $$ \frac{x_{n+1}}{x_{n}}=\frac{1}{2}\left(1+\frac{9}{x_{n}^{2}}\right)\leqslant\frac{1}{2}\left(1+\frac{9}{3^{2}}\right)=1. $$ 

所以 $ \left\{x_{n}\right\} $单调递减并有下界，故 $ \lim_{n\to\infty}x_n $存在. 令 $ \lim_{n\to\infty}x_n=A $，在 $ x_{n+1}=\frac{x_n^2+9}{2x_n} $的两边取极限得

 $$ A=\frac{A^{2}+9}{2A}\Rightarrow A=3\ (A=-3 舍去 ). $$ 

所以 $ \lim_{n\to\infty}x_n=3 $.

评注 单调有界原理多用于求递推关系式给出的数列极限。在证明单调性和有界性时，有时先证明有界性，再利用有界性来证明单调性；有时先证明单调性，再利用单调性来证明有界性；有时互不利用，而各自独立证明。

证明有界性常用的方法有：从数列的递推关系式观察；用已知不等式推出；用归纳法证明；利用单调性证明；由递推式 $ x_{n+1}=f(x_n) $中函数 $ f(x) $的有界性（或最大值、最小值）得到.

证明单调性的常用方法有：比值法——讨论 $ x_{n+1}/x_n $与1的大小（条件为 $ x_n>0 $）；差值法——讨论 $ x_{n+1}-x_n $与0的大小；由递推式 $ x_{n+1}=f(x_n) $中函数 $ f(x) $的单调性得到（如果 $ f'(x)>0 $，则当 $ x_0<x_1 $时， $ \{x_n\} $单调递增；当 $ x_0>x_1 $时，单调递减）；用数学归纳法或其他方法比较 $ x_{n+1} $与 $ x_n $的大小。

例如，设 $ x_{1}>0 $， $ x_{n+1}=\frac{1}{4}\left(3x_{n}+\frac{a}{x_{n}^{3}}\right)(a>0,n=1,2,\cdots) $，则

 $$ x_{n+1}=\frac{1}{4}\left(x_{n}+x_{n}+x_{n}+\frac{a}{x_{n}^{3}}\right)\geqslant\sqrt[4]{x_{n}\cdot x_{n}\cdot x_{n}\cdot\frac{a}{x_{n}^{3}}}=\sqrt[4]{a}\quad( 有下界 ). $$ 

单调性可由 $ \frac{x_{n+1}}{x_n}=\frac{1}{4}\left(3+\frac{a}{x_n^4}\right)<\frac{1}{4}\left(3+\frac{a}{a}\right)=1 $得到，这里用到了 $ \left\{x_{n}\right\} $有下界.

又如，设  $ x_{n}=\sqrt{3+\sqrt{3+\sqrt{\cdots+\sqrt{3}}}} $，易见  $ \left\{x_{n}\right\} $ 是单调递增的，且有  $ x_{n}^{2}=3+x_{n-1} $，所以

 $$ x_{n}=\frac{3}{x_{n}}+\frac{x_{n-1}}{x_{n}}<\frac{3}{x_{1}}+1=\sqrt{3}+1. $$ 

即 $ \left\{x_{n}\right\} $有上界，这里用到了 $ \left\{x_{n}\right\} $单调递增.

例28 设  $ x_{1}=1 $,  $ x_{n}=1+\frac{1}{1+x_{n-1}}(n=2,3,\cdots) $. 证明  $ \lim_{n\to\infty}x_n $ 存在，并求该极限.

分析 观察前几项，易发现数列不具有单调性，但其奇、偶子列有单调性。若能证明数列的奇、偶子列都有极限且极限相等，则数列的极限也就存在了。

解 方法1  $ x_{1}=1 $,  $ x_{2}=\frac{3}{2} $,  $ x_{3}=\frac{7}{5} $,  $ x_{4}=\frac{17}{12} $,  $ \cdots $, 数列不具有单调性.

考虑 $ \left\{x_{n}\right\} $的奇、偶子列 $ \left\{x_{2n-1}\right\},\left\{x_{2n}\right\} $.

易见  $ x_{1}<x_{3}, x_{2}>x_{4} $，假设  $ x_{2k-1}<x_{2k+1}, x_{2k}>x_{2k+2} $，则

 $$ x_{2k+3}=1+\frac{1}{1+x_{2k+2}}>1+\frac{1}{1+x_{2k}}=x_{2k+1}, $$ 

 $$ x_{2k+4}=1+\frac{1}{x_{2k+3}+1}<1+\frac{1}{x_{2k+1}+1}=x_{2k+2}. $$ 

即 $ \left\{x_{2n-1}\right\} $单调递增， $ \left\{x_{2n}\right\} $单调递减.

显然 $ 0<x_{n}<2 $，故 $ \left\{x_{2n-1}\right\},\left\{x_{2n}\right\} $都收敛。设 $ \lim_{n\to\infty}x_{2n}=a $， $ \lim_{n\to\infty}x_{2n-1}=b $。在等式 $ x_{n+1}=1+\frac{1}{1+x_n} $的两边分别取 $ n=2k-1 $与 $ n=2k $且 $ k\to\infty $，得

 $$ a=1+\frac{1}{1+b},~b=1+\frac{1}{1+a}. $$ 

解得  $ b = a = \pm\sqrt{2} $，所以  $ \left\{x_{n}\right\} $ 收敛，由  $ x_{n} > 0 $ 知， $ \lim_{n \to \infty} x_{n} = \sqrt{2} $.

方法2 解方程  $ x=1+\frac{1}{1+x} $，得  $ x=\pm\sqrt{2} $。因为

 $$ \begin{aligned}\left|x_{n}-\sqrt{2}\right|=&\left|1+\frac{1}{1+x_{n-1}}-\sqrt{2}\right|=\left|\frac{(1-\sqrt{2})(x_{n-1}-\sqrt{2})}{1+x_{n-1}}\right|\\<&\frac{\sqrt{2}-1}{2}\left|x_{n-1}-\sqrt{2}\right|\quad\left(\because x_{n-1}>1\right)\\<&\left(\frac{\sqrt{2}-1}{2}\right)^{2}\left|x_{n-2}-\sqrt{2}\right|\\<&\cdots<\left(\frac{\sqrt{2}-1}{2}\right)^{n-1}\left|x_{1}-\sqrt{2}\right|\rightarrow0(n\rightarrow\infty).\end{aligned} $$ 

所以  $ \lim_{n\to\infty}x_n=\sqrt{2} $.

评注（1）若数列由递推公式  $ x_{n}=f(x_{n-1}) $ 给出，而方程  $ x=f(x) $ 有根 x=a，用上面的方法 2（夹逼原理）证明  $ \lim_{n\to\infty}x_n=a $ 更为简便.

（2）数列  $ x_{n}=f(x_{n-1}) $ 的单调性与有界性都取决于函数  $ f(x) $ 的性态。在所规定的范围内，如果  $ x>f(x) $，则数列单调递减；如果  $ x<f(x) $，则数列单调递增。有时也用函数的导数为工具进行研判。

(3) 由方法2不难进一步得到加边极限 $ \lim 4^{n}(x_{n}-\sqrt{2})=0 $（加边极限的概念见例49评注）.

例 29 设  $ x_{1}=\ln a $， $ x_{n}=\sum_{i=1}^{n-1}\ln(a-x_{i}) $，n>1。证明  $ \lim_{n\to\infty}x_n=a-1 $。

分析　所给数列满足递推公式： $ x_{n+1}=x_n+\ln(a-x_n) $，为判断数列的有界性与单调性，可考虑函数 $ f(x)=x+\ln(a-x)(x<a) $的最值，以及 $ f(x) $与x的大小关系。也可利用不等式 $ \ln x\leq x-1 $直接得到 $ \{x_n\} $的有界性与单调性。

解 方法1 因为  $ x_{n}=\sum_{i=1}^{n-1}\ln(a-x_{i}),\quad n>1 $ ，则有  $ x_{n+1}=x_{n}+\ln(a-x_{n}) $

令  $ f(x)=x+\ln(a-x) $ (x<a)，则  $ f'(x)=1-\frac{1}{a-x} $，x=a-1 是函数的唯一驻点

当x<a-1时， $ f'(x) $为正，当x>a-1时， $ f'(x) $为负，所以 $ f(a-1)=a-1 $是f的最大值，即有 $ f(x)\leq a-1 $。故 $ \{x_n\} $有上界。

又若  $ x \leq a-1 $，则  $ \ln(a-x) \geq 0 $，故  $ f(x) \geq x $。即  $ \{x_n\} $ 单调递增，故数列  $ \{x_n\} $ 有极限，记为 A。在  $ x_{n+1} = x_n + \ln(a - x_n) $ 的两边取极限得

 $$ A=A+\ln(a-A)\Rightarrow\ln(a-A)=0. $$ 

所以

 $$ \lim_{n\to\infty}x_{n}=A=a-1. $$ 

方法2 利用不等式 $ \ln x \leq x-1 $，有

 $$ x_{n+1}=x_{n}+\ln(a-x_{n})\leq x_{n}+(a-x_{n}-1)=a-1,x_{n+1}-x_{n}=\ln(a-x_{n})\geq\ln[a-(a-1)]=\ln1=0. $$ 

所以 $ \{x_{n}\} $单调递增有上界，极限存在（后同方法1）.

评注 从几何上看，数列 $ \{x_{n}\} $的极限即为直线y=x与曲线 $ y=f(x) $交点的横（纵）坐标。本题中的 $ f(x)=x+\ln(a-x) $（如图1.1所示），其

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//dadcd5b8-126f-463f-bc51-10649f08b384/markdown_0/imgs/img_in_image_box_1076_1694_1390_1974.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A26Z%2F-1%2F%2Fe15f1151af69ecea53e645112e6cde1982cb3b3a986d4172f46d743d6cc25284" alt="Image" width="21%" /></div>


<div style="text-align: center;"><div style="text-align: center;">图1.1</div> </div>


有向折线表示了 $ x_{n} $的递推过程.

例 30 证明数列  $ x_{n}=1+\frac{1}{2}+\frac{1}{3}+\cdots+\frac{1}{n}-\ln n $ 的极限存在.

分析 由不等式 $ \frac{1}{n+1}<\ln\left(1+\frac{1}{n}\right)<\frac{1}{n} $，容易判断 $ \{x_{n}\} $的单调性与有界性.

证明 由于

 $$ x_{n+1}-x_{n}=\frac{1}{n+1}-\ln(n+1)+\ln n=\frac{1}{n+1}-\ln\left(1+\frac{1}{n}\right)<0, $$ 

所以 $ \{x_{n}\} $单调递减.又

 $$ \begin{aligned}x_{n}&>\ln(1+1)+\ln\left(1+\frac{1}{2}\right)+\cdots+\ln\left(1+\frac{1}{n}\right)-\ln n\left(\because\frac{1}{k}>\ln\left(1+\frac{1}{k}\right)\right)\\&=\ln2+\ln\frac{3}{2}+\cdots+\ln\frac{n+1}{n}-\ln n=\ln\left(2\cdot\frac{3}{2}\cdot\frac{4}{3}\cdot\cdots\cdot\frac{n}{n-1}\cdot\frac{n+1}{n}\right)-\ln n\\&=\ln(n+1)-\ln n>0．\end{aligned} $$ 

所以 $ \{x_{n}\} $有下界0，故 $ x_{n} $的极限存在.

评注（1）单调有界原理只是极限存在的一个充分条件，该原理并未给出求极限的方法，要计算极限还需要借助其他方法.

（2）记 $ \lim_{n\to\infty}\left(\sum_{k=1}^{n}\frac{1}{k}-\ln n\right)=C $，C称为欧拉常数，它是一个无理数，其值为0.5772156649 $ \cdots $。于是 $ \sum_{k=1}^{n}\frac{1}{k}=\ln n+C+\alpha_n $，其中 $ \lim_{n\to\infty}\alpha_n=0 $。

例 31 设  $ x_{1}, x_{2}, \cdots $ 是非负数列，满足  $ x_{n+1} \leqslant x_{n} + \frac{1}{n^{2}} (n = 1, 2, \cdots) $. 证明  $ \lim_{n \to \infty} x_{n} $ 存在.

分析 从题设条件容易得到  $ \{x_{n}\} $ 的有界性，但很难判定其单调性。如果改写  $ \frac{1}{n^{2}} = \sum_{k=1}^{n} \frac{1}{k^{2}} - \sum_{k=1}^{n-1} \frac{1}{k^{2}} \triangleq y_{n+1} - y_{n} $，则条件变为  $ x_{n+1} - y_{n+1} \leq x_{n} - y_{n} $，数列  $ \{x_{n} - y_{n}\} $ 的单调性与有界性都容易判定了。

证明 记  $ y_{n}=\sum_{k=1}^{n-1}\frac{1}{k^{2}}(n=2,3,\cdots) $，由于  $ \lim_{n\to\infty}y_{n}=\sum_{k=1}^{\infty}\frac{1}{k^{2}} $ 收敛，所以  $ \{y_{n}\} $ 有界，即存在 M>0 使

 $$ 0<y_{n}\leq M(n=2,3,\cdots) $$ 

由 $ 0 \leqslant x_{n+1} \leqslant x_n + \frac{1}{n^2} $及 $ \frac{1}{n^2} = y_{n+1} - y_n $，可得

 $$ -M\leqslant x_{n+1}-y_{n+1}\leqslant x_{n}-y_{n}. $$ 

这说明数列 $ \left\{x_{n}-y_{n}\right\} $单调递减有下界，从而收敛.进而得到

 $$ \operatorname*{l i m}_{n\to\infty}x_{n}=\operatorname*{l i m}_{n\to\infty}(x_{n}-y_{n})+\operatorname*{l i m}_{n\to\infty}y_{n}, $$ 

所以 $ \lim_{n\to\infty}x_n $存在.

评注 从证明过程可看出，将题设条件改为  $ x_{n+1} \leqslant x_n + a_n $，只要级数  $ \sum_{n=1}^{\infty} a_n $ 收敛，则  $ \{x_n\} $ 就收敛.

5. 利用导数的定义做计算

导数的概念： $  f'(x_0) = \lim_{x \to x_0} \frac{f(x) - f(x_0)}{x - x_0} = \lim_{\Delta x \to 0} \frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x}  $.

例  $ 32^{*} $ 求极限  $ \lim_{x\to0}\frac{\sqrt{\frac{1+x}{1-x}}\sqrt[4]{\frac{1+2x}{1-2x}}\sqrt[6]{\frac{1+3x}{1-3x}}\cdots\sqrt[2n]{\frac{1+nx}{1-nx}}-1}{3\pi\arcsin x-(x^2+1)\arctan^3x} $，其中 n 为正整数.

分析 记  $ f(x)=\sqrt{\frac{1+x}{1-x}}\sqrt[4]{\frac{1+2x}{1-2x}}\sqrt[6]{\frac{1+3x}{1-3x}}\cdots\sqrt[2n]{\frac{1+nx}{1-nx}} $，显然  $ f(0)=1 $，而极限式的分母是 x 的一阶无穷小，故可用  $ f'(0) $ 的定义来求极限.

解 令  $ f(x)=\sqrt{\frac{1+x}{1-x}}\sqrt[4]{\frac{1+2x}{1-2x}}\sqrt[6]{\frac{1+3x}{1-3x}}\cdots\sqrt[2n]{\frac{1+nx}{1-nx}} $ ，则  $ f(0)=1 $ ，且

 $$ \ln f(x)=\frac{1}{2}\ln\frac{1+x}{1-x}+\frac{1}{4}\ln\frac{1+2x}{1-2x}+\frac{1}{6}\ln\frac{1+3x}{1-3x}+\cdots+\frac{1}{2n}\ln\frac{1+nx}{1-nx}, $$ 

 $$ \frac{f^{\prime}(x)}{f(x)}=\frac{1}{2}\left(\frac{1}{1+x}+\frac{1}{1-x}\right)+\frac{1}{4}\left(\frac{2}{1+2x}+\frac{2}{1-2x}\right)+\cdots+\frac{1}{2n}\left(\frac{n}{1+nx}+\frac{n}{1-nx}\right) $$ 

得  $ f'(0)=n $．注意到  $ \lim_{x\to0}\frac{\arcsin x}{x}=1=\lim_{x\to0}\frac{\arctan x}{x} $，因此

 $$  原式 =\lim_{x\to0}\frac{x}{3\pi\arcsin x-(x^{2}+1)\arctan^{3}x}\cdot\frac{f(x)-f(0)}{x-0}=\frac{n}{3\pi}. $$ 

评注 当极限式为 $ \frac{U}{0} $型，且分母是分子函数自变量的一阶无穷小时，可考虑用导数的定义来计算极限.

例 33 若  $ f(0)=0 $，且  $ f'(0) $ 存在，求极限  $ \lim_{x \to 0} \frac{f(1 - \cos x)}{1 - \cos x \cdot \sqrt{\cos 2x} \cdot \sqrt[3]{\cos 3x}} $.

分析 这属于 $ \frac{0}{0} $型，但仅知道 $ f'(0) $存在，不能用洛必达法则. 由于分母是分子函数自变量 $ 1-\cos x $的同阶无穷小（见本节例12），所以可考虑用导数的定义来求极限.

 $$ \operatorname*{l i m}_{x\to0}\frac{f(1-\cos x)}{1-\cos x\cdot\sqrt{\cos2x}\cdot\sqrt[3]{\cos3x}}=\operatorname*{l i m}_{x\to0}\frac{f(1-\cos x)}{1-\cos x}\cdot\frac{1-\cos x}{1-\cos x\cdot\sqrt{\cos2x}\cdot\sqrt[3]{\cos3x}}\;. $$ 

因为  $ f(0)=0 $ ，则

 $$ \lim_{x\to0}\frac{f(1-\cos x)}{1-\cos x}\xlongequal{h=1-\cos x}\lim_{h\to0}\frac{f(h)-f(0)}{h}=f^{\prime}(0) $$ 

又

 $$ \lim_{x\to0}\frac{1-\cos x}{1-\cos x\cdot\sqrt{\cos2x}\cdot\sqrt[3]{\cos3x}}=\frac{1}{2}\lim_{x\to0}\frac{x^{2}}{1-\cos x\cdot\sqrt{\cos2x}\cdot\sqrt[3]{\cos3x}}=\frac{1}{6}( 见本节例 12), $$ 

所以

 $$ \operatorname*{l i m}_{x\to0}\frac{f(1-\cos x)}{1-\cos x\cdot\sqrt{\cos2x}\cdot\sqrt[3]{\cos3x}}=\frac{1}{6}f^{\prime}(0). $$ 

评注 由导数的定义易知：若  $ f(x) $ 在 x=a 可导，且  $ f(a)=0 $，则对任意  $ \alpha(t)\to a(t\to t_{0}) $，都有  $ \lim_{t\to t_{0}}\frac{f(\alpha(t))}{\alpha(t)-a}=f'(a) $；特别地，若 a=0，且有  $ \alpha(t)\sim\beta(t)(t\to t_{0}) $，则等价无穷小替换  $ f(\alpha(t))\sim f(\beta(t)) $ 也是正确的.

例 34 已知  $ f(0)=0 $,  $ f'(0)=1 $, 求  $ \lim_{n\to\infty}\left[f\left(\frac{1}{n^2}\right)+f\left(\frac{2}{n^2}\right)+\cdots+f\left(\frac{n}{n^2}\right)\right] $.

分析 可利用  $ f'(0) $ 的定义得到  $ f(x) $ 在 x=0 附近的局部表达式，再代入所求极限式做计算.

解 由于  $ f'(0)=\lim_{x\to0}\frac{f(x)-f(0)}{x} $，则  $ f(x)=f(0)+f'(0)x+o(x) $，从而

 $$ \begin{aligned}f\Biggl(\frac{1}{n^{2}}\Biggr)+f\Biggl(\frac{2}{n^{2}}\Biggr)+\cdots+f\Biggl(\frac{n}{n^{2}}\Biggr)=&\frac{1}{n^{2}}+\frac{2}{n^{2}}+\cdots+\frac{n}{\cdot n^{2}}+n\cdot o\Biggl(\frac{1}{n}\Biggr)\\=&\frac{n(n+1)}{2n^{2}}+o(1)\to\frac{1}{2}\end{aligned} $$ 

即

 $$ \lim_{n\to\infty}\left[f\left(\frac{1}{n^{2}}\right)+f\left(\frac{2}{n^{2}}\right)+\cdots+f\left(\frac{n}{n^{2}}\right)\right]=\frac{1}{2}. $$ 

评注 上面计算中用到了无穷小运算  $ O\left(\frac{1}{n^{2}}\right) + O\left(\frac{2}{n^{2}}\right) + \cdots + O\left(\frac{n}{n^{2}}\right) = n \cdot O\left(\frac{1}{n}\right) $，其原因是  $ O\left(\frac{i}{n^{2}}\right) $  $ (i=1,2,\cdots,n) $ 都是  $ \frac{1}{n} $ 的高阶无穷小，从而都可记为  $ O\left(\frac{1}{n}\right) $。所以运算是正确的。

6. 利用微分或积分中值公式做计算

1）拉格朗日中值定理

若  $ f(x) \in C[a,b] \cap D(a,b) $，则  $ \exists \xi \in (a,b) $，使得  $ f(b) - f(a) = f'(\xi)(b - a) $。

2）积分中值定理

若  $ f(x) \in C[a,b] $，则  $ \exists \xi \in (a,b) $，使得  $ \int_{a}^{b} f(x) \, \mathrm{d}x = f(\xi)(b-a) $.

例 35 设  $ a $ 是非零常数，求  $ \lim_{n \to \infty} n^3 \left[ \ln \left( n + \arctan \frac{a}{n} \right) - \ln \left( n + \arctan \frac{a}{n+1} \right) \right] $.

分析 不妨设 $a>0$，极限中的因式 $\left[\ln\left(n+\arctan\frac{a}{n}\right)-\ln\left(n+\arctan\frac{a}{n+1}\right)\right]$ 是函数 $\ln x$ 在区间 $\left[n+\arctan\frac{a}{n+1}, n+\arctan\frac{a}{n}\right]$ 上的增量，可考虑用拉格朗日中值公式；进一步，$\arctan\frac{a}{n}-\arctan\frac{a}{n+1}$ 又是函数 $\arctan x$ 在区间 $\left[\frac{a}{n+1}, \frac{a}{n}\right]$ 上的增量，可用相同方法处理。

解 不妨设 $a>0$，对 $\ln x$ 在区间 $\left[n+\arctan\frac{a}{n+1}, n+\arctan\frac{a}{n}\right]$ 上用拉格朗日中值定理，则存在 $\xi_n\in\left(n+\arctan\frac{a}{n+1}, n+\arctan\frac{a}{n}\right)$，使得

 $$ \ln\left(n+\arctan\frac{a}{n}\right)-\ln\left(n+\arctan\frac{a}{n+1}\right)=\frac{1}{\xi_{n}}\left(\arctan\frac{a}{n}-\arctan\frac{a}{n+1}\right). $$ 

再对  $ \arctan x $ 在  $ \left[\frac{a}{n+1}, \frac{a}{n}\right] $ 上用拉格朗日中值定理， $ \exists \eta_n \in \left(\frac{a}{n+1}, \frac{a}{n}\right) $，使得

 $$ \arctan\frac{a}{n}-\arctan\frac{a}{n+1}=\frac{1}{1+\eta_{n}^{2}}\left(\frac{a}{n}-\frac{a}{n+1}\right). $$ 

所以

 $$ n^{3}\left[\ln\left(n+\arctan\frac{a}{n}\right)-\ln\left(n+\arctan\frac{a}{n+1}\right)\right]=\frac{n^{3}}{\xi_{n}}\cdot\frac{1}{1+\eta_{n}^{2}}\left(\frac{a}{n}-\frac{a}{n+1}\right). $$ 

注意到  $ \lim_{n\to\infty}\frac{\xi_n}{n}=1 $， $ \lim_{n\to\infty}\eta_n=0 $。所以

 $$ \begin{aligned}&\lim_{n\to\infty}n^{3}\left[\ln\left(n+\arctan\frac{a}{n}\right)-\ln\left(n+\arctan\frac{a}{n+1}\right)\right]=\lim_{n\to\infty}\frac{n^{3}}{\xi_{n}}\cdot\frac{1}{1+\eta_{n}^{2}}\left(\frac{a}{n}-\frac{a}{n+1}\right)\\ &=\lim_{n\to\infty}\frac{n}{\xi_{n}}\cdot\lim_{n\to\infty}\frac{n^{2}}{1+\eta_{n}^{2}}\cdot\frac{a}{n(n+1)}=a\ .\\ \end{aligned} $$ 

评注 当极限式中有某一函数的增量时，可考虑用微分中值定理.

例 36 设  $ f(x) $ 在  $ (-\infty, +\infty) $ 内可导，且  $ \lim_{x \to \infty} f'(x) = e $， $ \lim_{x \to \infty} \left( \frac{x + c}{x - c} \right)^x = \lim_{x \to \infty} [f(x) - f(x-1)] $，求 c.

分析 右边极限式中是  $ f(x) $ 在区间  $ [x-1,x] $ 上的增量，且函数可导，可考虑用拉格朗日中值定理.

解 由条件易知 $ c\neq0 $，而

 $$ \lim_{x\to\infty}\left(\frac{x+c}{x-c}\right)^{x}=\lim_{x\to\infty}\frac{\left(1+\frac{c}{x}\right)^{x}}{\left(1-\frac{c}{x}\right)^{x}}=\mathrm{e}^{2c}, $$ 

又  $ f(x) $ 在  $ (-\infty,+\infty) $ 内可导，由拉格朗日中值定理， $ \exists\xi\in(x-1,x) $，使得

 $$ f(x)-f(x-1)=f^{\prime}(\xi)\;. $$ 

取极限得

 $$ \operatorname*{l i m}_{x\to\infty}[f(x)-f(x-1)]=\operatorname*{l i m}_{\xi\to\infty}f^{\prime}(\xi)=\mathsf{e}. $$ 

由①，②式得  $ e^{2c} = e $， $ c = \frac{1}{2} $.

例37 求  $ \lim_{x\to+\infty}\sqrt{x}\int_{x}^{x+1}\frac{dt}{\sqrt{t+\sin t+x}} $

分析 因积分不易求出，所以用积分中值定理去掉积分符号再求极限.

解 由积分中值定理得

 $$ \begin{aligned}\lim_{x\to+\infty}\sqrt{x}\int_{x}^{x+1}\frac{\mathrm{d}t}{\sqrt{t+\sin t+x}}&=\lim_{x\to+\infty}\frac{\sqrt{x}}{\sqrt{(x+\theta)+\sin(x+\theta)+x}}\quad(0<\theta<1)\\&=\lim_{x\to+\infty}\frac{1}{\sqrt{2+\frac{\theta+\sin(x+\theta)}{x}}}=\frac{1}{\sqrt{2}}.\end{aligned} $$ 

评注 当极限式中有定积分，而定积分又难以计算时，常用两种方法处理：一是利用积分中值定理去掉积分符号，再求极限；另一种是适当地放大与缩小被积函数，使得放大与缩小后的积分容易计算，再用夹逼原理求极限。读者可考虑用夹逼原理求该题的极限。

例 38 $ ^{*} $ 求  $ \lim_{n \to \infty} \int_{0}^{\frac{\pi}{2}} \sin^{n} x \, dx $.

分析 因为在积分区间中有  $ 0 \leq \sin x \leq 1 $，所以直接用积分中值定理确定不了极限值。可将积分区间分成两个子区间  $ \left[0, \frac{\pi}{2} - \varepsilon\right] $ 和  $ \left[\frac{\pi}{2} - \varepsilon, \frac{\pi}{2}\right] $，在前一个区间里被积函数的极限是 0，而后一个区间的长度可任意小，其积分值也就任意小，由极限的定义可知所求极限为 0。该题也可先算出积分再求极限，但要困难些。

解  $ \forall\varepsilon>0 $，有

 $$ \int_{0}^{\frac{\pi}{2}}\sin{}^{n}x\mathrm{d}x=\int_{0}^{\frac{\pi}{2}-\varepsilon}\sin{}^{n}x\mathrm{d}x+\int_{\frac{\pi}{2}-\varepsilon}^{\frac{\pi}{2}}\sin{}^{n}x\mathrm{d}x. $$ 

由积分中值定理  $ \int_{0}^{\frac{\pi}{2}-\varepsilon}\sin^{n}x\,\mathrm{d}x=\left(\frac{\pi}{2}-\varepsilon\right)\sin^{n}\xi $，其中  $ 0<\xi\leq\frac{\pi}{2}-\varepsilon $．则

 $$ \lim_{n\to\infty}\int_{0}^{\frac{\pi}{2}-\varepsilon}\sin^{n}x\mathrm{d}x=\lim_{n\to\infty}\left(\frac{\pi}{2}-\varepsilon\right)\sin^{n}\xi=0. $$ 

所以 $ \exists N>0 $，当 $ n>N $时，有

 $$ \left|\int_{0}^{\frac{\pi}{2}}\sin^{n}x dx\right|<\varepsilon; $$ 

又

 $$ \left|\int_{\frac{\pi}{2}-\varepsilon}^{\frac{\pi}{2}}\sin^{n}x\mathrm{d}x\right|<\int_{\frac{\pi}{2}-\varepsilon}^{\frac{\pi}{2}}1\mathrm{d}x=\varepsilon. $$ 

由 $ ^{①} $， $ ^{②} $式可得

 $$ \left|\int_{0}^{\frac{\pi}{2}}\sin^{n}x\mathrm{d}x\right|<2\varepsilon. $$ 

根据极限的定义知  $ \lim_{n\to\infty}\int_{0}^{\frac{\pi}{2}}\sin^{n}x dx=0 $.

评注 注意直接利用积分中值定理的以下做法是错误的：

 $$ \lim_{n\to\infty}\int_{0}^{\frac{\pi}{2}}\sin^{n}x\mathrm{d}x=\frac{\pi}{2}\lim_{n\to\infty}\sin^{n}\xi=0\left(0<\xi<\frac{\pi}{2}\right). $$ 

原因是这里的  $ \xi $ 与 n 有关，记为  $ \xi_n $，由  $ 0 < \sin \xi_n < 1 $，不能得出  $ \lim_{n \to \infty} \sin^n \xi_n = 0 $。比如  $ 0 < 1 - \frac{1}{n} < 1 $，但  $ \lim_{n \to \infty} \left(1 - \frac{1}{n}\right)^n = e^{-1} \neq 0 $。

# 7. 利用洛必达（L'Hospital）法则做计算

洛必达法则是求函数不定式极限最常用、最基本的方法。它主要解决 $ \frac{0}{0} $与 $ \frac{\infty}{\infty} $型的极限问题，即有 $ \lim\frac{f(x)}{g(x)}=\lim\frac{f'(x)}{g'(x)} $。其他类型的不定式则是通过初等运算转化为这两种形式来解决的，即有 $ 0\cdot\infty,\infty-\infty,1^{\infty},\infty^{0},0^{0}\xrightarrow[\text{变量代换}]{\text{恒等变形}}\frac{0}{0} $或 $ \frac{\infty}{\infty} $。学习中要注意各种不同形式的有效转化。

例 39 计算  $ \lim_{x\to\infty}\left(\sin\frac{2}{x^{2}}+\cos\frac{1}{x}\right)^{\frac{1}{\sin^{2}\left(\frac{1}{x}\right)}} $

分析 这属于 $ 1^{\circ} $型，取对数转化为 $ \frac{0}{0} $型. 为便于求导运算，可先作倒代换.

解 方法1 记  $ y=\left(\sin\frac{2}{x^{2}}+\cos\frac{1}{x}\right)^{\frac{1}{\sin^{2}\left(\frac{1}{x}\right)}} $，令  $ t=\frac{1}{x} $，则  $ \ln y=\frac{1}{\sin^{2}t}\ln\left(\sin2t^{2}+\cos t\right) $.

 $$ \begin{aligned}\lim_{x\to\infty}(\ln y)&=\lim_{t\to0}\frac{\ln(\sin2t^{2}+\cos t)}{\sin^{2}t}=\lim_{t\to0}\frac{\ln(\sin2t^{2}+\cos t)}{t^{2}}\\&=\lim_{t\to0}\frac{4t\cos2t^{2}-\sin t}{2t(\sin2t^{2}+\cos t)}=\lim_{t\to0}\frac{4t\cos2t^{2}-\sin t}{2t}\quad(\because\sin2t^{2}+\cos t\to1)\end{aligned} $$ 

 $$ =\operatorname*{l i m}_{t\to0}\left(2\cos2t^{2}-\frac{\sin t}{2t}\quad\right)=\frac{3}{2}\;. $$ 

所以  $ \lim_{x \to \infty} y = e^{\frac{3}{2}} $.

方法2 原式 $ \lim_{x\to0}\left[1+(\sin2t^{2}+\cos t-1)\right]^{\frac{1}{\sin^{2}t}}=\mathrm{e}^{\lim\limits_{t\to0}\frac{\sin2t^{2}+\cos t-1}{\sin^{2}t}} $

其中

 $$ \operatorname*{l i m}_{t\to0}\frac{\operatorname{s i n}2t^{2}+\operatorname{c o s}t-1}{\operatorname{s i n}^{2}t}=\operatorname*{l i m}_{t\to0}\frac{\operatorname{s i n}2t^{2}}{\operatorname{s i n}^{2}t}-\operatorname*{l i m}_{t\to0}\frac{1-\operatorname{c o s}t}{\operatorname{s i n}^{2}t}=2-\frac{1}{2}=\frac{3}{2}\;. $$ 

评注 洛必达法则是求不定式极限的一种有效方法，但未必一定简单，计算中要注意与求极限的其他方法综合使用，以达到简化计算的效果。

例40 计算 $ \lim_{n\to\infty}\left[\left(n^{3}-n^{2}+\frac{n}{2}\right)\mathrm{e}^{\frac{1}{n}}-\sqrt{1+n^{6}}\right] $

分析 这属于 $ \infty-\infty $型，通分化为 $ \frac{0}{0} $或 $ \frac{\infty}{\infty} $型，为便于通分可先作倒代换.

解 考虑函数极限  $ \lim_{x\to+\infty}\left[\left(x^{3}-x^{2}+\frac{x}{2}\right)\mathrm{e}^{\frac{1}{x}}-\sqrt{1+x^{6}}\right] $.

设 $ t=\frac{1}{x} $，当 $ x\to+\infty $时， $ t\to0^{+} $，有

 $$ \begin{aligned}&\lim_{x\rightarrow+\infty}\left[\left(x^{3}-x^{2}+\frac{x}{2}\right)\mathrm{e}^{\frac{1}{x}}-\sqrt{1+x^{6}}\right]=\lim_{t\rightarrow0^{+}}\frac{(1-t+\frac{1}{2}t^{2})\mathrm{e}^{t}-\sqrt{1+t^{6}}}{t^{3}}\\ &=\lim_{t\rightarrow0^{+}}\frac{(-1+t)\mathrm{e}^{t}+\left(1-t+\frac{t^{2}}{2}\right)\mathrm{e}^{t}-\frac{6t^{5}}{2\sqrt{1+t^{6}}}}{3t^{2}}=\lim_{t\rightarrow0^{+}}\frac{\frac{1}{2}\mathrm{e}^{t}-\frac{3t^{3}}{\sqrt{1+t^{6}}}}{3}=\frac{1}{6}.\\ \end{aligned} $$ 

由海涅（Heine）定理知，原极限为 $ \frac{1}{6} $.

评注（1）数列极限不能直接使用洛必达法则，但可考虑对应的函数极限，从而使用洛必达法则。这样做的理论依据是如下的Heine定理。

Heine 定理： $ \lim_{x\to a}f(x)=c\Leftrightarrow\forall x_n\to a(n\to\infty) $，都有 $ \lim_{n\to\infty}f(x_n)=c $

（2）如果数列极限无法转化为函数极限，则常用后面将要介绍的施笃兹定理.

例41 设  $ f(x) $ 在 x=0 处存在 n 阶导数，又  $ f(0)=f'(0)=\cdots=f^{(n-1)}(0)=0,\ f^{(n)}(0)\neq0 $ ，求

 $$ \lim_{x\to0}\frac{\int_{0}^{x}(x-t)f(t)dt}{x\int_{0}^{x}f(x-t)dt}. $$ 

分析 这属于 $ \frac{0}{0} $型，函数可导又有变限积分，因此用洛必达法则较为方便.

解 由于  $ f(x) $ 在 x=0 处存在 n 阶导数，则在 x=0 的某邻域内存在 n-1 阶导数，由洛必达法则

 $$ I=\lim_{x\to0}\frac{\int_{0}^{x}(x-t)f(t)\mathrm{d}t}{x\int_{0}^{x}f(x-t)\mathrm{d}t}=\lim_{x\to0}\frac{x\int_{0}^{x}f(t)\mathrm{d}t-\int_{0}^{x}t f(t)\mathrm{d}t}{x\int_{0}^{x}f(u)\mathrm{d}u}\quad(u=x-t) $$ 

 $$ \begin{aligned}&=\lim_{x\to0}\frac{\int_{0}^{x}f(t)\mathrm{d}t}{xf(x)+\int_{0}^{x}f(u)\mathrm{d}u}=\lim_{x\to0}\frac{f(x)}{xf^{\prime}(x)+2f(x)}\\&=\lim_{x\to0}\frac{f^{\prime}(x)}{xf^{\prime \prime}(x)+3f^{\prime}(x)}=\cdots=\lim_{x\to0}\frac{f^{(n-2)}(\dot{x})}{xf^{(n-1)}(x)+nf^{(n-2)}(x)}.\end{aligned} $$ 

上式仍属于 $ \frac{0}{0} $型，但不能再用洛必达法则了，因为未设 $ f(x) $在x=0邻域存在n阶导数.将分子分母同时除以 $ x^{2} $，考察分母的第1项

 $$ \lim_{x\to0}\frac{f^{(n-1)}(x)}{x}=\lim_{x\to0}\frac{f^{(n-1)}(x)-f^{(n-1)}(0)}{x-0}=f^{(n)}(0), $$ 

①式的分子除以 $ x^{2} $后

 $$ \operatorname*{l i m}_{x\to0}\frac{f^{(n-2)}(x)}{x^{2}}=\operatorname*{l i m}_{x\to0}\frac{f^{(n-1)}(x)}{2x}=\frac{1}{2}f^{(n)}(0)~, $$ 

于是

 $$ I=\frac{\frac{1}{2}f^{(n)}(0)}{f^{(n)}(0)+\frac{n}{2}f^{(n)}(0)}=\frac{1}{n+2}. $$ 

评注 由已知条件也容易想到将  $ f(x) $ 在 x=0 处展开至 n 阶带皮亚诺余项形式的泰勒公式来计算，读者不妨自己做做.

例 42 设函数  $ f(x) $ 在 x=0 的某邻域内有二阶连续导数，且  $ f(0) $,  $ f'(0) $,  $ f''(0) $ 均不为零. 证明存在唯一一组实数  $ k_{1} $,  $ k_{2} $,  $ k_{3} $，使得

 $$ \operatorname*{l i m}_{h\to0}\frac{k_{1}f(h)+k_{2}f(2h)+k_{3}f(3h)-f(0)}{h^{2}}=0~. $$ 

分析 这属于 $ \frac{0}{0} $型，分母为 $ h^{2} $，可用两次洛必达法则，由分子极限为零可得 $ k_{1}, k_{2}, k_{3} $的线性方程组，解方程组可求得 $ k_{1}, k_{2}, k_{3} $的值.

证明 如果结论成立，则

 $$ \operatorname*{l i m}_{h\to0}\bigl(k_{1}f(h)+k_{2}f(2h)+k_{3}f(3h)-f(0)\bigr)=(k_{1}+k_{2}+k_{3}-1)f(0)=0, $$ 

由于  $ f(0) \neq 0 $，所以

 $$ k_{1}+k_{2}+k_{3}-1=0. $$ 

由洛必达法则得

 $$ \begin{aligned}{0=}&{{}\varliminf_{h\to0}\frac{k_{1}f(h)+k_{2}f(2h)+k_{3}f(3h)-f(0)}{h^{2}}}\\ {=}&{{}\varliminf_{h\to0}\frac{k_{1}f^{\prime}(h)+2k_{2}f^{\prime}(2h)+3k_{3}f^{\prime}(3h)}{2h}.}\\ \end{aligned} $$ 

由 $ ^{②} $式知

 $$ 0=\operatorname*{l i m}_{h\to0}\bigl(k_{1}f^{\prime}(h)+2k_{2}f^{\prime}(2h)+3k_{3}f^{\prime}(3h)\bigr)=(k_{1}+2k_{2}+3k_{3})f^{\prime}(0)\;, $$ 

由于  $ f'(0) \neq 0 $，所以

 $$ k_{1}+2k_{2}+3k_{3}=0\;. $$ 

对②式再用一次洛必达法则，有

 $$ 0=\operatorname*{l i m}_{h\to0}\frac{k_{1}f^{\prime\prime}(h)+4k_{2}f^{\prime\prime}(2h)+9k_{3}f^{\prime\prime}(3h)}{2}=(k_{1}+4k_{2}+9k_{3})f^{\prime\prime}(0), $$ 

由于 $ f''(0)\neq0 $，所以

 $$ k_{1}+4k_{2}+9k_{3}=0. $$ 

将表达式①，③，④联立得关于 $ k_{1}, k_{2}, k_{3} $的非齐次线性方程组，由于该方程组的系数行列式不为零，由克莱姆法则知，方程组有唯一解（事实上 $ k_{1}=3, k_{2}=-3, k_{3}=1 $）.

##### 评注（1）用洛必达法则确定不定式中的常数是十分常用的方法.

##### (2) 读者不难证明该题的一般性结论：

设函数  $ f(x) $ 在 x=0 的某邻域内有 n 阶连续导数，且  $ f^{(k)}(0) \neq 0 (k=0,1,\cdots,n) $. 则对任意一组互异的实数  $ l_{1}, l_{2}, \cdots, l_{n+1} $，必存在唯一一组实数  $ k_{1}, k_{2}, \cdots, k_{n+1} $，使得当  $ h \to 0 $ 时， $ \sum_{i=1}^{n+1} k_{i} f(l_{i} h) - f(0) $ 是比  $ h^{n} $ 高阶的无穷小.

# 8 $ ^{*} $. 利用施笃兹（Stolz）定理做计算

施笃兹定理又称数列极限的洛必达法则，对求某些不定型的数列极限十分有效. 与函数极限的洛必达法则类似，施笃兹定理也有 $ \frac{0}{0} $与 $ \frac{\infty}{\infty} $两种情形.

施笃兹定理：（1）设  $ \lim_{n\to\infty}x_n=0 $， $ \{y_n\} $ 单调递减，且  $ \lim_{n\to\infty}y_n=0 $，如果  $ \lim_{n\to\infty}\frac{x_n-x_{n-1}}{y_n-y_{n-1}} $ 存在或为  $ \infty $，则  $ \lim_{n\to\infty}\frac{x_n}{y_n}=\lim_{n\to\infty}\frac{x_n-x_{n-1}}{y_n-y_{n-1}} $.

（2）设数列 $ \left\{y_{n}\right\} $单调递增，且 $ \lim_{n\to\infty}y_n=+\infty $，如果 $ \lim_{n\to\infty}\frac{x_{n+1}-x_n}{y_{n+1}-y_n} $存在或为 $ \infty $，则 $ \lim_{n\to\infty}\frac{x_n}{y_n}=\lim_{n\to\infty}\frac{x_n-x_{n-1}}{y_n-y_{n-1}} $.

这里我们仅介绍定理的应用，对定理证明感兴趣的读者可查阅《数学分析》教材。根据施笃兹定理，我们很容易得到以下两个常用的极限公式：

① 若  $ \lim_{n\to\infty}x_n $ 存在或为 $ \infty $，则  $ \lim_{n\to\infty}\frac{1}{n}\sum_{k=1}^{n}x_k=\lim_{n\to\infty}x_n $

② 若 $\{x_n\}$ 为正项数列，且 $\lim_{n \to \infty} x_n$ 存在或为 $\infty$，则 $\lim_{n \to \infty} \sqrt[n]{x_1 x_2} \cdots x_n = \lim_{n \to \infty} x_n$。例 $43^*$ 设 $x_1 \in (0,1)$，$x_{n+1} = x_n (1 - x_n)$，$n=1,2,\cdots$。证明 $\lim_{n \to \infty} nx_n = 1$。

分析 只需证明  $ \lim_{n\to\infty}\frac{n}{1/x_n}=1 $，要利用施笃兹定理还得验证  $ x_n $ 单调递减并趋于 0.

证明 由  $ x_1 \in (0,1) $， $ x_2 = x_1(1 - x_1) $，知  $ x_2 \in (0,1) $。由归纳法，易证： $ x_n \in (0,1) $。于是

 $$ 0<\frac{x_{n+1}}{x_{n}}=(1-x_{n})<1\;(n=1,2,\cdots). $$ 

所以 $ \{x_{n}\} $单调递减有下界，从而 $ \lim_{n\to\infty}x_n=A $存在.在 $ x_{n+1}=x_n(1-x_n) $中取 $ n\to\infty $，有

 $$ A=A(1-A)\Rightarrow A=0\ , 即 \lim_{n\to\infty}x_{n}=0. $$ 

设  $ y_{n}=\frac{1}{x_{n}} $，则  $ \lim_{n\to\infty}y_{n}=\infty $，且  $ y_{n}<y_{n+1} $，利用施笃兹定理，有

 $$ \operatorname*{l i m}_{n\to\infty}n x_{n}=\operatorname*{l i m}_{n\to\infty}\frac{n}{y_{n}}=\operatorname*{l i m}_{n\to\infty}\frac{(n+1)-n}{y_{n+1}-y_{n}}=\operatorname*{l i m}_{n\to\infty}\frac{1}{y_{n+1}-y_{n}}. $$ 

由于

 $$ \lim_{n\to\infty}(y_{n+1}-y_n)=\lim_{n\to\infty}\left(\frac{1}{x_{n+1}}-\frac{1}{x_n}\right)=\lim_{n\to\infty}\left(\frac{1}{x_n(1-x_n)}-\frac{1}{x_n}\right)=\lim_{n\to\infty}\frac{1}{1-x_n}=1 $$ 

所以 $ \lim_{n\to\infty}nx_n=1 $

评注 一般情况下，若  $ x_{n+1} = f(x_n) $ 且方程  $ x = f(x) $ 只有零解，则极限  $ \lim_{n \to \infty} nx_n = \lim_{n \to \infty} \frac{n}{1/x_n} $ 宜用施笃兹定理来计算.

例 44 $ ^{*} $ 设函数列  $ \sin_{1}x = \sin x $， $ \sin_{n}x = \sin(\sin_{n-1}x) $， $ n = 2, 3, \cdots $。证明  $ \lim_{n \to \infty} \sqrt{\frac{n}{3}} \sin_{n}x = 1 $。

分析 只需证明  $ \lim_{n\to\infty}n\sin_{n}^{2}x=3 $ 。显然  $ \sin_{n}^{2}x $ 单调递减并趋于 0，故可考虑对  $ \lim_{n\to\infty}\frac{n}{1/\sin_{n}^{2}x} $ 用施笃兹定理.

证明 对取定的 x，显然  $ \sin_{n}^{2}x $ 单调递减并趋于 0，利用施笃兹定理，有

 $$ \begin{aligned}\lim_{n\to\infty}n\sin_{n}^{2}x&=\lim_{n\to\infty}\frac{n}{\frac{1}{\sin_{n}^{2}x}}=\lim_{n\to\infty}\frac{(n+1)-n}{\frac{1}{\sin_{n+1}^{2}x}-\frac{1}{\sin_{n}^{2}x}}\\&=\lim_{t\to0}\frac{1}{\frac{1}{\sin^{2}t}-\frac{1}{t^{2}}}=\lim_{t\to0}\frac{t^{2}\sin^{2}t}{t^{2}-\sin^{2}t}=\lim_{t\to0}\frac{t^{4}}{t^{2}-\sin^{2}t}\\&=\lim_{t\to0}\frac{4t^{3}}{2t-\sin2t}=\lim_{t\to0}\frac{12t^{2}}{2-2\cos2t}=3.\end{aligned} $$ 

所以 $ \lim_{n\to\infty}\sqrt{\frac{n}{3}}\sin_nx=1 $

评注 该题的极限运算中用到了将数列极限转换为函数极限来计算，目的是便于用洛必达法则.

例 45 $ ^{*} $ 设  $ a_{n}=\frac{1}{n^{2}}\sum_{k=0}^{n}\ln C_{n}^{k} $，计算  $ \lim_{n\to\infty}a_{n} $.

分析 该题属于 $ \frac{\infty}{\infty} $型，且满足施笃兹定理的条件.

解

 $$ \begin{aligned}\lim_{n\rightarrow\infty}a_{n}&=\lim_{n\rightarrow\infty}\frac{\sum_{k=0}^{n}\ln C_{n}^{k}-\sum_{k=0}^{n-1}\ln C_{n-1}^{k}}{n^{2}-\left(n-1\right)^{2}}=\lim_{n\rightarrow\infty}\frac{\sum_{k=0}^{n-1}\ln\left(C_{n}^{k}\ /\ C_{n-1}^{k}\right)}{2n-1}\\&=\lim_{n\rightarrow\infty}\frac{\sum_{k=0}^{n-1}\ln\frac{n}{n-k}}{2n-1}=\lim_{n\rightarrow\infty}\frac{n\ln n-\sum_{k=1}^{n}\ln k}{2n-1}\\&=\lim_{n\rightarrow\infty}\frac{\left(n\ln n-\sum_{k=1}^{n}\ln k\right)-\left((n-1)\ln(n-1)-\sum_{k=1}^{n-1}\ln k\right)}{(2n-1)-(2n-3)}\\&=\frac{1}{2}\lim_{n\rightarrow\infty}(n-1)\ln\left(1+\frac{1}{n-1}\right)=\frac{1}{2}.\end{aligned} $$ 

评注 若 $ \frac{\infty}{\infty} $型极限中的分子或分母含有无穷和的形式，用施笃兹定理来计算是比较方便的.

例46 $ ^{*} $ 求下列极限：

(1)  $ \lim_{n \to \infty} \frac{\sqrt[n]{n!}}{n} $; (2)  $ \lim_{n \to \infty} \left( \sqrt[n]{(n+1)!} - \sqrt[n]{n!} \right) $.

分析（1）属于 $ \frac{\infty}{\infty} $型，但用施笃兹定理计算时分子难以化简，若取对数，则问题就解决了.

（2）对（1）直接用施笃兹定理就可看出（2）的结果.

解 （1）方法1 记 $ a_{n}=\frac{\sqrt[n]{n!}}{n} $，则

 $$ \ln a_{n}=\frac{1}{n}\ln n!-\ln n=\frac{\ln n!-n\ln n}{n}. $$ 

取极限并用施笃兹定理，得

 $$ \begin{aligned}\lim_{n\to\infty}\ln a_{n}&=\lim_{n\to\infty}\frac{(\ln n!-n\ln n)-\left[\ln(n-1)!-(n-1)\ln(n-1)\right]}{n-(n-1)}\\&=\lim_{n\to\infty}(1-n)\ln\left(1+\frac{1}{n-1}\right)=-1.\end{aligned} $$ 

所以  $ \lim_{n \to \infty} \frac{\sqrt[n]{n!}}{n} = e^{-1} $.

方法2 记  $ x_{n}=\left(1+\frac{1}{n}\right)^{-n} $，则  $ \lim_{n\to\infty}x_{n}=\lim_{n\to\infty}\left(1+\frac{1}{n}\right)^{-n}=e^{-1} $。又

 $$ x_{1}x_{2}\cdots x_{n}=\left(1+\frac{1}{1}\right)^{-1}\left(1+\frac{1}{2}\right)^{-2}\cdots\left(1+\frac{1}{n}\right)^{-n}=\left(\frac{1}{2}\right)^{1}\left(\frac{2}{3}\right)^{2}\left(\frac{3}{4}\right)^{3}\cdots\left(\frac{n}{n+1}\right)^{n}=\frac{n!}{\left(n+1\right)^{n}}, $$ 

由此得到

 $$ \operatorname*{l i m}_{n\to\infty}\frac{\sqrt[n]{n!}}{n+1}=\operatorname*{l i m}_{n\to\infty}\sqrt[n]{x_{1}x_{2}\cdots x_{n}}=\operatorname*{l i m}_{n\to\infty}x_{n}=\mathrm{e}^{-1}\Rightarrow\operatorname*{l i m}_{n\to\infty}\frac{\sqrt[n]{n!}}{n}=\operatorname*{l i m}_{n\to\infty}\frac{n+1}{n}\cdot\frac{\sqrt[n]{n!}}{n+1}=\mathrm{e}^{-1}. $$ 

方法3 化为定积分来做计算

 $$ \operatorname*{l i m}_{n\to\infty}\frac{\sqrt[n]{n!}}{n}=\operatorname*{l i m}_{n\to\infty}\sqrt[n]{\frac{n!}{n^{n}}}=\mathsf{e}^{\operatorname*{l i m}_{n\to\infty}\frac{1}{n}\operatorname{l n}\frac{n!}{n^{n}}}=\mathsf{e}^{\operatorname*{l i m}_{n\to\infty}\frac{1}{n}\sum_{k=1}^{n}\operatorname{l n}\frac{k}{n}}=\mathsf{e}^{\int_{0}^{1}\operatorname{l n}x\mathrm{d}x}=\mathsf{e}^{[x\operatorname{l n}x-x]_{0}^{1}}=\mathsf{e}^{-1}. $$ 

(2) 对  $ \lim_{n\to\infty}\frac{\sqrt[n]{n!}}{n} $ 用施笃兹定理，并由（1）的结果，有

 $$ \mathrm{e}^{-1}=\lim_{n\to\infty}\frac{\sqrt[n]{n!}}{n}=\lim_{n\to\infty}\frac{\sqrt[n+1]{(n+1)!}-\sqrt[n]{n!}}{(n+1)-n}=\lim_{n\to\infty}\left(\sqrt[n+1]{(n+1)!}-\sqrt[n]{n!}\right). $$ 

需要注意的是，上面等式成立的条件是右端的极限存在，但却不易判断。下面我们用其他方法来求右端的极限。

 $$ \begin{aligned}{{}^{n+1}\sqrt{(n+1)!}-\sqrt[n]{n!}}&{{}=\sqrt[n]{n!}\left(\frac{\overset{n+1}{\sqrt[n]{n+1}}!}{\sqrt[n]{n!}}-1\right)=\sqrt[n]{n!}\left[\left(\frac{(n+1)!}{(n!)^{(n+1)/n}}\right)^{\frac{1}{n+1}}-1\right]}\\ {}&{{}=\sqrt[n]{n!}\left[\left(\frac{n+1}{\sqrt[n]{n!}}\right)^{\frac{1}{n+1}}-1\right]=\sqrt[n]{n!}\left(\mathsf{e}^{\frac{1}{n+1}\operatorname{l n}\frac{n+1}{\sqrt[n]{n!}}}-1\right).}\\ \end{aligned} $$ 

由（1）知  $ \lim_{n\to\infty}\frac{\sqrt[n]{n!}}{n+1}=e^{-1} $，所以  $ \lim_{n\to\infty}\frac{1}{n+1}\ln\frac{n+1}{\sqrt[n]{n!}}=0 $， $ e^{\frac{1}{n+1}\ln\frac{n+1}{\sqrt[n]{n!}}}-1\sim\frac{1}{n+1}\ln\frac{n+1}{\sqrt[n]{n!}} $。从而

 $$ \sqrt[n+1]{(n+1)!}-\sqrt[n]{n!}\sim\frac{\sqrt[n]{n!}}{n+1}\ln\frac{n+1}{\sqrt[n]{n!}}\to\mathrm{e}^{-1}\ln\mathrm{e}=\mathrm{e}^{-1}(n\to\infty)\;. $$ 

即  $ \lim_{n\to\infty}\left(\sqrt[n+1]{(n+1)!}-\sqrt[n]{n!}\right)=\mathrm{e}^{-1} $.

评注 注意结论： $ \lim_{n\to\infty}\frac{\sqrt[n]{n!}}{n}=e^{-1} $。这对某些相关极限问题的解决会有帮助。

# 9. 利用泰勒公式做计算

带皮亚诺（Peano）余项形式的泰勒（Taylor）公式  $ f(x)=\sum_{k=0}^{n}\frac{f^{(k)}(x_0)}{k!}(x-x_0)^k+O((x-x_0)^n) $ 给出了函数在  $ x_0 $ 点的局部表达式. 当  $ f(x) $ 是  $ x\to x_0 $ 的无穷小量，但其阶数不显见时，用泰勒公式展开是较好的方法. 读者要熟悉以下几个常见函数的展开式：

 $$ \mathrm{e}^{x}=1+x+\frac{x^{2}}{2!}+\cdots+\frac{x^{n}}{n!}+o(x^{n}); $$ 

 $$ \sin x=x-\frac{x^{3}}{3!}+\frac{x^{5}}{5!}-\cdots+(-1)^{n-1}\frac{x^{2n-1}}{(2n-1)!}+o(x^{2n}); $$ 

 $$ \cos x=1-\frac{1}{2!}x^{2}+\frac{1}{4!}x^{4}-\cdots+(-1)^{n}\frac{x^{2n}}{(2n)!}+o(x^{2n+1}); $$ 

 $$ \ln(1+x)=x-\frac{x^{2}}{2}+\frac{x^{3}}{3}-\cdots+(-1)^{n-1}\frac{x^{n}}{n}+o(x^{n}); $$ 

 $$ (1+x)^{\alpha}=1+\alpha x+\frac{\alpha(\alpha-1)}{2!}x^{2}+\cdots+\frac{\alpha(\alpha-1)\cdots(\alpha-n+1)}{n!}x^{n}+o(x^{n}). $$ 

例47 求  $ \lim_{x\to0}\frac{\frac{x^{2}}{2}+1-\sqrt{1+x^{2}}}{(\cos x-\mathrm{e}^{x^{2}})\sin x^{2}} $

分析 该题属于 $ \frac{0}{0} $型，用洛必达法则计算的工作量太大，这里用泰勒公式展开，再求极限.

解 由于  $ \sqrt{1+x^{2}}=1+\frac{1}{2}x^{2}+\frac{1}{2!}\cdot\frac{1}{2}\left(\frac{1}{2}-1\right)x^{4}+o(x^{4})=1+\frac{1}{2}x^{2}-\frac{1}{8}x^{4}+o(x^{4}) $

 $$ \mathrm{e}^{x^{2}}=1+x^{2}+o(x^{2}),\quad\cos x=1-\frac{x^{2}}{2!}+o(x^{2})\,. $$ 

 $$  原式 =\lim_{x\to0}\frac{\frac{x^{2}}{2}+1-\left[1+\frac{1}{2}x^{2}-\frac{1}{8}x^{4}+o(x^{4})\right]}{\left[\left(1-\frac{x^{2}}{2!}+o(x^{2})\right)-\left(1+x^{2}+o(x^{2})\right)\right]x^{2}}=\lim_{x\to0}\frac{\frac{1}{8}x^{4}+o(x^{4})}{-\frac{3}{2}x^{4}+o(x^{4})}=-\frac{1}{12}. $$ 

评注（1）用泰勒公式求极限时，函数展开的阶数应由极限式中分子（或分母）无穷小的阶数来确定。例如，想要看出本题分子无穷小的阶， $ \sqrt{1+x^{2}} $ 展开的阶数就要大于2，题中取的4阶（大于2的最小阶数）。分子的阶确定了，分母就应展开到相应的阶数。

(2) 在运算中，凡高于4次的项都并入了 $ o(x^{4}) $中．一般有： $ o(x^{n})+o(x^{m})=o(x^{n})(m\geqslant n) $．

（3）等价无穷小替换是泰勒公式中取n=0或1时的情形（舍去了高阶无穷小的余项）.

例48 求下列极限.

(1)  $ \lim_{n \to \infty} \sum_{k=1}^{n} \left(1 - \frac{k}{n}\right) \ln \left(1 + \frac{k}{n^2}\right) $; (2)  $ \lim_{n \to \infty} \sin \left( \frac{\pi}{e^{1/(2n)} - 1} \right) $.

分析（1）这是无穷和，只需将 $ \ln\left(1+\frac{k}{n^{2}}\right) $做一阶泰勒展开，利用数列求和公式来缩项，再求极限.

（2）显然  $ \lim_{n\to\infty}\left(\frac{\pi}{\mathrm{e}^{1/(2n)}-1}\right) $ 不存在，但  $ \lim_{n\to\infty}\left(\frac{\pi}{\mathrm{e}^{1/(2n)}-1}-2n\pi\right) $ 却是存在的.

解（1）

 $$ \begin{aligned}&\sum_{k=1}^{n}\left(1-\frac{k}{n}\right)\ln\left(1+\frac{k}{n^{2}}\right)=\sum_{k=1}^{n}\left(1-\frac{k}{n}\right)\left(\frac{k}{n^{2}}+o\left(\frac{1}{n^{2}}\right)\right)\\ &=\frac{1}{n^{2}}\sum_{k=1}^{n}k-\frac{1}{n^{3}}\sum_{k=1}^{n}k^{2}+o\left(\frac{1}{n}\right)\\ &=\frac{1}{n^{2}}\cdot\frac{1}{2}n(n+1)-\frac{1}{n^{3}}\cdot\frac{1}{6}n(n+1)(2n+1)+o\left(\frac{1}{n}\right)\rightarrow\frac{1}{2}-\frac{1}{3}=\frac{1}{6}.\\ \end{aligned} $$ 

即

 $$ \lim_{n\to\infty}\sum_{k=1}^{n}\left(1+\frac{k}{n}\right)\ln\left(1+\frac{k}{n^{2}}\right)=\frac{1}{6}. $$ 

（2）由于 $ \sin\left(\frac{\pi}{\mathrm{e}^{1/(2n)}-1}\right)=\sin\pi\left(\frac{1}{\mathrm{e}^{1/(2n)}-1}-2n\right) $，而

 $$ \begin{aligned}&\sin\pi\left(\frac{1}{\mathbf{e}^{1/(2n)}-1}-2n\right)=\sin\pi\left[\frac{1-2n\left(\mathbf{e}^{1/(2n)}-1\right)}{\mathbf{e}^{1/(2n)}-1}\right]\\ &=\sin\pi\left[\frac{1-2n\left(\frac{1}{2n}+\frac{1}{2(2n)^{2}}+o\left(\frac{1}{n^{2}}\right)\right)}{\frac{1}{2n}+o\left(\frac{1}{n}\right)}\right]=\sin\pi\left[\frac{-\frac{1}{2}+o(1)}{1+o(1)}\right].\\ \end{aligned} $$ 

所以  $ \lim_{n\to\infty}\sin\left(\frac{\pi}{\mathrm{e}^{1/(2n)}-1}\right)=-\sin\frac{\pi}{2}=-1 $

评注 容易看出，若（1）中作等价无穷小代换 $ \ln\left(1+\frac{k}{n^{2}}\right)\sim\frac{k}{n^{2}} $，其计算结果仍然不变。原因是题解中用的是一阶泰勒公式，它等同于等价无穷小替换。但计算中还是用泰勒公式为好，以避免误解。（2）的求解中若用等价无穷小替换 $ \lim_{n\to\infty}\sin\left(\frac{\pi}{e^{1/(2n)}-1}\right)=\lim_{n\to\infty}\sin\left(\frac{\pi}{1/(2n)}\right)=0 $就错了。请读者想想错误的原因。

例  $ 49^{*} $ 设  $ a_{n}=n\sin(2\pi en!) $，求  $ I=\lim_{n\to\infty}a_{n} $ 与  $ J=\lim_{n\to\infty}n(a_{n}-I) $.

分析 由于  $ \sin(2k\pi + \alpha) = \sin \alpha (k \in \mathbb{Z}) $，所以化简  $ \sin(2\pi n!) $ 的关键是要将  $ e^n $ 表示为整数加真分数的形式，为此可将  $ e $ 做泰勒展开。

解 由于  $ e=1+1+\frac{1}{2!}+\frac{1}{3!}+\cdots+\frac{1}{n!}+\frac{1}{(n+1)!}+\frac{1}{(n+2)!}+o\left(\frac{1}{(n+2)!}\right) $

所以

 $$ I=\lim_{n\to\infty}a_{n}=\lim_{n\to\infty}n\sin\left(\frac{2\pi}{n+1}+o\left(\frac{1}{n}\right)\right)=\lim_{n\to\infty}n\cdot\left(\frac{2\pi}{n+1}+o\left(\frac{1}{n}\right)\right)=2\pi. $$ 

 $$ \begin{aligned}J&=\lim_{n\to\infty}n(a_{n}-I)=\lim_{n\to\infty}n\left[n\sin\left(\frac{2\pi}{n+1}+\frac{2\pi}{(n+1)(n+2)}+o\left(\frac{1}{n^{2}}\right)\right)-2\pi\right]\\&=\lim_{n\to\infty}n\cdot\left[n\left(\frac{2\pi}{n+1}+\frac{2\pi}{(n+1)(n+2)}+o\left(\frac{1}{n^{2}}\right)\right)-2\pi\right](\because\sin x=x+o(x))\\&=\lim_{n\to\infty}n\cdot\left(-\frac{2\pi}{n+1}+\frac{2\pi n}{(n+1)(n+2)}+o\left(\frac{1}{n}\right)\right)=0.\\ \end{aligned} $$ 

评注 若  $ \lim_{n\to\infty}a_n=I $ ，则称  $ \lim_{n\to\infty}g(n)(a_n-I)(g(n)\to\infty) $ 为  $ \lim_{n\to\infty}a_n $ 的加边极限， $ g(n) $ 常为幂函数、指数函数或对数函数. 若  $ \lim_{n\to\infty}a_n $ 可用泰勒公式计算，其加边极限只需将泰勒公式多展开一阶. 如本题在计算 I 时，只用了①式中的 n 阶展开式，计算 J 时则用了  $ n+1 $ 阶展开式. 数列极限的施笃兹定理也是解决某些加边极限的有效方法（见本节例 43、例 44）. 加边极限问题还可能有多次加边的情形.

例 50 设  $ a_{i} > 0 (i = 1, 2, \cdots, n) $，记  $ f(x) = \left( \frac{1}{n} \sum_{i=1}^{n} a_{i}^{x} \right)^{\frac{1}{x}} $。求极限  $ I = \lim_{x \to 0} f(x) $ 与  $ J = \lim_{x \to 0} \frac{1}{x} \left[ f(x) - I \right] $。

分析 极限 I 属于  $ 1^{\infty} $ 型，极限中有幂指函数，需要将幂指函数转化为指数函数来计算，可用洛必达法则或泰勒公式. 考虑到 J 是 I 的加边极限，所以都用泰勒公式计算为好.

解  $ f(x)=\mathrm{e}^{\ln f(x)}=\mathrm{e}^{\frac{1}{x}\ln\left(\frac{1}{n}\sum_{i=1}^{n}a_{i}^{x}\right)} $．利用泰勒公式

 $$ a_{i}^{x}=\mathrm{e}^{x\ln a_{i}}=1+x\ln a_{i}+\frac{1}{2}(x\ln a_{i})^{2}+o(x^{2})\triangleq1+u_{i}, $$ 

其中  $ u_{i}=x\ln a_{i}+\frac{1}{2}(x\ln a_{i})^{2}+o(x^{2}) $，则

 $$ \ln\left(\frac{1}{n}\sum_{i=1}^{n}a_{i}^{x}\right)=\ln\left(\frac{1}{n}\sum_{i=1}^{n}(1+u_{i})\right)=\ln\left(1+\frac{1}{n}\sum_{i=1}^{n}u_{i}\right). $$ 

再利用  $ \ln(1+x) $ 的泰勒公式，将上式化为

 $$ \begin{align*}\ln\Biggl(\frac{1}{n}\sum_{i=1}^{n}a_{i}^{x}\Biggr)=&\frac{1}{n}\sum_{i=1}^{n}u_{i}-\frac{1}{2}\Biggl(\frac{1}{n}\sum_{i=1}^{n}u_{i}\Biggr)^{2}+o(u_{i}^{2})\\=&\frac{1}{n}\sum_{i=1}^{n}x\ln a_{i}+\frac{1}{2n}\sum_{i=1}^{n}(x\ln a_{i})^{2}-\frac{1}{2}\Biggl(\frac{1}{n}\sum_{i=1}^{n}x\ln a_{i}\Biggr)^{2}+o(x^{2})\\=&\frac{x}{n}\ln(a_{1}a_{2}\cdots a_{n})+\frac{x^{2}}{2n}\Biggl[\sum_{i=1}^{n}(\ln a_{i})^{2}-\frac{1}{n}\ln^{2}(a_{1}a_{2}\cdots a_{n})\Biggr]+o(x^{2})\;.\end{align*} $$ 

利用 $ ^{②} $式可得

 $$ I=\mathrm{e}^{\lim\limits_{x\to0}\frac{1}{x}\ln\left(\frac{1}{n}\sum_{i=1}^{n}a_{i}^{x}\right)}=\mathrm{e}^{\frac{1}{n}\ln\left(a_{1}a_{2}\cdots a_{n}\right)}=\sqrt[n]{a_{1}a_{2}\cdots a_{n}}. $$ 

 $$ \begin{aligned}J=&\lim_{x\to0}\frac{1}{x}\Big[f(x)-\sqrt[n]{a_{1}a_{2}\cdots a_{n}}\Big]\\=&\sqrt[n]{a_{1}a_{2}\cdots a_{n}}\lim_{x\to0}\frac{1}{x}\Bigg[\exp\left[\frac{1}{x}\ln\left(\frac{1}{n}\sum_{i=1}^{n}a_{i}^{x}\right)-\frac{1}{n}\ln(a_{1}a_{2}\cdots a_{n})\right]-1\Bigg]\\=&\sqrt[n]{a_{1}a_{2}\cdots a_{n}}\lim_{x\to0}\frac{1}{x}\left[\frac{1}{x}\ln\left(\frac{1}{n}\sum_{i=1}^{n}a_{i}^{x}\right)-\frac{1}{n}\ln(a_{1}a_{2}\cdots a_{n})\right](t\to0 时 ,\mathbf{e}^{t}-1\sim t).\end{aligned} $$ 

 $$ \begin{aligned}&=\sqrt[n]{a_{1}a_{2}\cdots a_{n}}\lim_{x\to0}\frac{1}{x}\Biggl[\frac{x}{2n}\Biggl(\sum_{i=1}^{n}(\ln a_{i})^{2}-\frac{1}{n}\ln^{2}(a_{1}a_{2}\cdots a_{n})\Biggr)+o(x)\Biggr]\quad( 代入\textcircled{2}式 )\\&=\frac{1}{2n}\sqrt[n]{a_{1}a_{2}\cdots a_{n}}\Biggl(\sum_{i=1}^{n}(\ln a_{i})^{2}-\frac{1}{n}\ln^{2}(a_{1}a_{2}\cdots a_{n})\Biggr).\end{aligned} $$ 

评注 该题与上题类似，都是加边极限问题，上题是数列极限，该题是函数极限。为了计算J，①式与②式都用了二阶泰勒公式，如果只计算I，用一阶泰勒公式即可，或用洛必达法则更简单

例 51 设 C 为实数，函数  $ f(x) $ 满足  $ \lim_{x\to\infty}f(x)=C $， $ \lim_{x\to\infty}f^m(x)=0 $。求证  $ \lim_{x\to\infty}f'(x)=0 $， $ \lim_{x\to\infty}f''(x)=0 $。

分析 泰勒公式建立了函数与各阶导数的联系，由题设条件容易想到利用函数的二阶泰勒公式.

证明 用拉格朗日型余项的泰勒公式，有

 $$ f(x+1)=f(x)+f^{\prime}(x)+\frac{1}{2}f^{n}(x)+\frac{1}{6}f^{m}\big(x+\xi(x)\big),\ (0<\xi<1); $$ 

 $$ f(x-1)=f(x)-f^{\prime}(x)+\frac{1}{2}f^{\prime \prime}(x)-\frac{1}{6}f^{\prime \prime \prime}(x-\eta(x)),(0<\eta<1). $$ 

①±②式，并整理得③，④式：

 $$ f^{\prime \prime}(x)=f(x+1)-2f(x)+f(x-1)-\frac{1}{6}f^{m}\big(x+\xi(x)\big)+\frac{1}{6}f^{m}\big(x-\eta(x)\big), $$ 

 $$ 2f^{\prime}(x)=f(x+1)-f(x-1)-\frac{1}{6}f^{m}\big(x+\xi(x)\big)-\frac{1}{6}f^{m}\big(x-\eta(x)\big). $$ 

当  $ x \to \infty $ 时， $ x + \xi(x) \to \infty $， $ x - \eta(x) \to \infty $，因此

 $$ \lim_{x\to\infty}f^{\prime \prime}(x)=C-2C+C-\frac{1}{6}\cdot0+\frac{1}{6}\cdot0=0,\quad\lim_{x\to\infty}f^{\prime}(x)=\frac{1}{2}(C-C-\frac{1}{6}\cdot0-\frac{1}{6}\cdot0)=0. $$ 

注意，以下做法是不对的：

方法1

 $$ \begin{aligned}\lim_{x\to\infty}f(x)&=\lim_{x\to\infty}\frac{f(x)\mathrm{e}^{x}}{\mathrm{e}^{x}}=\lim_{x\to\infty}\frac{[f(x)+f^{\prime}(x)]\mathrm{e}^{x}}{\mathrm{e}^{x}}\left( 洛必达法则 \right)\\&=\lim_{x\to\infty}[f(x)+f^{\prime}(x)]=\lim_{x\to\infty}f(x)+\lim_{x\to\infty}f^{\prime}(x).\end{aligned} $$ 

所以 $ \lim_{x\to\infty}f'(x)=0 $.

方法2 在区间 $ [x,x+1] $上用拉格朗日中值定理，得

 $$ f(x+1)-f(x)=f^{\prime}(\xi),\ x<\xi<x+1. $$ 

当  $ x \to \infty $ 时，有  $ \xi \to \infty $，所以  $ \lim_{\xi \to \infty} f'(\xi) = \lim_{x \to \infty} [f(x+1) - f(x)] = C - C = 0 $，得  $ \lim_{x \to \infty} f'(x) = 0 $。

“方法1”中的错误有二：一是 $ \lim_{x\to\infty}\frac{f(x)e^x}{e^x} $不一定是

例如， $ f(x)=\frac{\sin x^{2}}{x} $，显然 $ \lim_{x\to\infty}f(x)=0 $， $ f'(x)=2\cos x^{2}-\frac{\sin x^{2}}{x^{2}} $，但 $ \lim_{x\to\infty}f'(x) $不存在.

“方法2”中的错误在于：由 $ \lim_{\xi \to \infty} f'(\xi) = 0 $得不到 $ \lim_{x \to \infty} f'(x) = 0 $。因为这里的 $ \xi $不一定是连续变量。评注对可微函数 $ f(x) $，仅由 $ \lim_{x \to \infty} f(x) = C $，得不到 $ \lim_{x \to \infty} f'(x) = 0 $的结论。

10. 利用定积分的定义做计算

由定积分的定义知 $ \int_{0}^{1}f(x)\mathrm{d}x=\lim_{n\to\infty}\sum_{k=1}^{n}f\left(\frac{k}{n}\right)\cdot\frac{1}{n} $，我们通常将等式的右端称为积分和式的极限。当数列可化为（或等价于）一个积分和式时，用定积分来计算极限是较方便的。

例52 求  $ \lim_{n\to\infty}\sin\frac{\pi}{n}\sum_{k=1}^{n}\frac{1}{2+\cos\frac{k\pi}{n}}. $

分析 利用等价无穷小  $ \sin\frac{\pi}{n}\sim\frac{\pi}{n} $，极限可表示为定积分.

解

 $$ \begin{aligned} 原式 &=\lim_{n\to\infty}\frac{\pi}{n}\sum_{k=1}^{n}\frac{1}{2+\cos\frac{k\pi}{n}}=\pi\int_{0}^{1}\frac{\mathrm{d}x}{2+\cos\pi x}\\&=\pi\int_{0}^{1}\frac{\mathrm{d}x}{1+2\cos^{2}\frac{\pi x}{2}}=2\int_{0}^{1}\frac{\mathrm{d}\tan\frac{\pi x}{2}}{3+\tan^{2}\frac{\pi x}{2}}=\frac{2}{\sqrt{3}}\cdot\arctan\frac{\tan\frac{\pi x}{2}}{\sqrt{3}}\Bigg|_{0}^{1}=\frac{\pi}{\sqrt{3}}.\end{aligned} $$ 

例 53 求极限  $ \lim_{n\to\infty}\frac{1}{n}\sqrt[n]{n(n+1)(n+2)\cdots(2n-1)} $.

分析这是无穷乘积问题，取对数化为无穷和，容易看出用定积分定义计算很方便.

解 令  $ a_{n}=\frac{1}{n}\sqrt[n]{n(n+1)(n+2)\cdots(2n-1)}=\sqrt[n]{\left(\frac{1}{n}+1\right)\left(\frac{2}{n}+1\right)\cdots\left(\frac{n-1}{n}+1\right)} $．则

 $$ \ln a_{n}=\frac{1}{n}\sum_{k=1}^{n-1}\ln\left(1+\frac{k}{n}\right), $$ 

 $$ \operatorname*{l i m}_{n\to\infty}\ln a_{n}=\operatorname*{l i m}_{n\to\infty}\frac{1}{n}\sum_{k=1}^{n-1}\ln\left(1+\frac{k}{n}\right)=\int_{0}^{1}\ln(1+x)\,\mathrm{d}x=2\ln2-1\,. $$ 

故

 $$ \operatorname*{l i m}_{n\to\infty}\frac{1}{n}\sqrt[n]{n(n+1)(n+2)\cdots(2n-1)}=\mathrm{e}^{2\ln2-1}=\frac{4}{\mathrm{e}}. $$ 

例 54 求极限  $ \lim_{n\to\infty}\sqrt{n}\left(1-\sum_{k=1}^{n}\frac{1}{n+\sqrt{k}}\right) $.

分析 各项分母均介于 n 到  $ n+\sqrt{n} $ 之间，为统一分母，将它们做适当的放缩（取为 n 或  $ n+\sqrt{n} $），极限式就可表示为定积分，利用夹逼原理就可求得极限.

解 记  $ a_{n}=\sqrt{n}\left(1-\sum_{k=1}^{n}\frac{1}{n+\sqrt{k}}\right) $，则

 $$ a_{n}=\sqrt{n}\sum_{k=1}^{n}\left(\frac{1}{n}-\frac{1}{n+\sqrt{k}}\right)=\frac{1}{\sqrt{n}}\sum_{k=1}^{n}\frac{\sqrt{k}}{n+\sqrt{k}}. $$ 

显然

 $$ \frac{1}{n+\sqrt{n}}\sum_{k=1}^{n}\sqrt{\frac{k}{n}}<\frac{1}{\sqrt{n}}\sum_{k=1}^{n}\frac{\sqrt{k}}{n+\sqrt{k}}<\frac{1}{n}\sum_{k=1}^{n}\sqrt{\frac{k}{n}}. $$ 

而

 $$ \lim_{n\to\infty}\frac{1}{n}\sum_{k=1}^{n}\sqrt{\frac{k}{n}}=\int_{0}^{1}\sqrt{x}\mathrm{d}x=\frac{2}{3}，\quad\lim_{n\to\infty}\frac{1}{n+\sqrt{n}}\sum_{k=1}^{n}\sqrt{\frac{k}{n}}=\lim_{n\to\infty}\frac{n}{n+\sqrt{n}}\cdot\lim_{n\to\infty}\frac{1}{n}\sum_{k=1}^{n}\sqrt{\frac{k}{n}}=\frac{2}{3}． $$ 

由夹逼原理知  $ \lim_{n\to\infty}a_n=\frac{2}{3} $.

评注（1）如果一个和式的各项均为分式，且分母中极限变量 n 的最高次幂项均相同，则任意取

舍各分母中的其余项（最高次幂项不变）不会改变和的极限。该结论对我们运用夹逼原理很有帮助。

（2）该题也可不用定积分，仅用来逼原理来求极限，但要困难些，可参见第十一届全国大学生数学竞赛（非数学类）决赛试题解答.

例55 $ ^{*} $ 设  $ A_{n}=\sum_{k=1}^{n}\frac{n}{n^{2}+k^{2}} $ 求  $ \lim_{n\to\infty}n\left(\frac{\pi}{4}-A_{n}\right) $.

分析 易知  $ \lim_{n\to\infty}A_n=\lim_{n\to\infty}\sum_{k=1}^{\infty}\frac{1}{1+(k/n)^2}\frac{1}{n}=\int_{0}^{1}\frac{dx}{1+x^2}=\frac{\pi}{4} $，所以会想到将所求极限转化为定积分来计算。要将极限化为一个和式，就需要将  $ \int_{0}^{1}\frac{dx}{1+x^2} $ 也写成 n 项和，将点  $ x_k=\frac{k}{n} $ 插入积分区间即可实现。

解 方法1  $ \lim_{n\to\infty}A_n=\lim_{n\to\infty}\sum_{k=1}^{n}\frac{1}{1+\left(\frac{k}{n}\right)^2}\cdot\frac{1}{n}=\int_{0}^{1}\frac{dx}{1+x^2}=\arctan x\Big|_{0}^{1}=\frac{\pi}{4} $

记  $ f(x)=\frac{1}{1+x^{2}} $， $ x_{k}=\frac{k}{n} $ ( $ k=0,1,\cdots,n $)，则

 $$ A_{n}=\sum_{k=1}^{n}f(x_{k})(x_{k}-x_{k-1})=\sum_{k=1}^{n}\int_{x_{k-1}}^{x_{k}}f(x_{k})\mathrm{d}x. $$ 

 $$ \begin{aligned} 且 \frac{\pi}{4}=\int_{0}^{1}f(x)\mathrm{d}x&=\sum_{k=1}^{n}\int_{x_{k-1}}^{x_{k}}f(x)\mathrm{d}x\ , 得 \\\lim_{n\to\infty}n\Bigg(\frac{\pi}{4}-A_{n}\Bigg)&=\lim_{n\to\infty}n\sum_{k=1}^{n}\int_{x_{k-1}}^{x_{k}}[f(x)-f(x_{k})]\mathrm{d}x\\=\lim_{n\to\infty}n\sum_{k=1}^{n}\int_{x_{k-1}}^{x_{k}}f^{\prime}(\xi_{k})(x-x_{k})\mathrm{d}x\quad&( 微分中值定理 ,\ \xi_{k}\in(x_{k-1},x_{k})).\end{aligned} $$ 

显然  $ f'(x) $ 在区间  $ [0,1] $ 上连续，记  $ m_k, M_k $ 分别是  $ f'(x) $ 在区间  $ [x_{k-1}, x_k] $ 上的最小值与最大值，则  $ \int_{x_{k-1}}^{x_k} f'(\xi_k)(x - x_k) \, \mathrm{d}x $ 介于  $ m_k \int_{x_{k-1}}^{x_k} (x - x_k) \, \mathrm{d}x $ 与  $ M_k \int_{x_{k-1}}^{x_k} (x - x_k) \, \mathrm{d}x $ 之间，所以  $ \exists \eta_k \in (x_{k-1}, x_k) $，使

 $$ \int_{x_{k-1}}^{x_{k}}f^{\prime}(\xi_{k})(x-x_{k})\mathrm{d}x=f^{\prime}(\eta_{k})\int_{x_{k-1}}^{x_{k}}(x-x_{k})\mathrm{d}x=-f^{\prime}(\eta_{k})\frac{1}{2}(x_{k}-x_{k-1})^{2}. $$ 

所以

 $$ \begin{align*}\lim_{n\to\infty}n\Biggl(\frac{\pi}{4}-A_{n}\Biggr)=&-\lim_{n\to\infty}n\sum_{k=1}^{n}f^{\prime}(\eta_{k})\frac{1}{2}(x_{k}-x_{k-1})^{2}=-\frac{1}{2}\lim_{n\to\infty}\sum_{k=1}^{n}f^{\prime}(\eta_{k})\frac{1}{n}\\=&-\frac{1}{2}\int_{0}^{1}f^{\prime}(x)\mathrm{d}x=-\frac{1}{2}f(x)\big|_{0}^{1}=\frac{1}{4}.\end{align*} $$ 

方法2 记  $ f(x)=\arctan x $， $ x_{k}=\frac{\kappa}{n}(k=0,1,\cdots,n) $，则  $ f(x_{n})=\arctan1=\frac{\pi}{4} $， $ f(x_{0})=\arctan0=0 $，由泰勒公式

 $$ f(x)=f(x_{k})+f^{\prime}(x_{k})(x-x_{k})+\frac{1}{2!}f^{\prime \prime}(\xi_{k})(x-x_{k})^{2}, $$ 

取  $ x = x_{k-1} $，移项得

 $$ f(x_{k})-f(x_{k-1})=f^{\prime}(x_{k})(x_{k}-x_{k-1})-\frac{1}{2!}f^{n}(\xi_{k})(x_{k}-x_{k-1})^{2} $$ 

 $$ \begin{align*}=&\frac{1}{1+\left(\frac{k}{n}\right)^{2}}\cdot\frac{1}{n}-\frac{1}{2}f^{\prime \prime}(\xi_{k})\frac{1}{n^{2}}\\=&\frac{n}{n^{2}+k^{2}}-\frac{1}{2}f^{\prime \prime}(\xi_{k})\frac{1}{n^{2}}\quad(x_{k-1}<\xi_{k}<\dot{x}_{k},\quad k=1,2,\cdots,n).\end{align*} $$ 

上面n个等式相加得

 $$ \frac{\pi}{4}=\sum_{k=1}^{n}[f(x_{k})-f(x_{k-1})]=\sum_{k=1}^{n}\left[\frac{n}{n^{2}+k^{2}}-\frac{1}{2}f^{\prime \prime}(\xi_{k})\frac{1}{n^{2}}\right]=\dot{A}_{n}-\frac{1}{2}\sum_{k=1}^{n}f^{\prime \prime}(\xi_{k})\frac{1}{n^{2}}. $$ 

所以

 $$ \begin{align*}\lim_{n\to\infty}n\Biggl(\frac{\pi}{4}-A_{n}\Biggr)=-\frac{1}{2}\lim_{n\to\infty}\sum_{k=1}^{n}f^{\prime \prime}(\xi_{k})\frac{1}{n}=-\frac{1}{2}\int_{0}^{1}f^{\prime \prime}(x)\mathrm{d}x\\=-\frac{1}{2}f^{\prime}(x)\Big|_{0}^{1}=-\frac{1}{2}\frac{1}{1+x^{2}}\bigg|_{0}^{1}=\frac{1}{4}.\end{align*} $$ 

评注 （1）该题仍属于极限  $ \lim_{n\to\infty}A_n=\frac{\pi}{4} $ 的加边问题，“方法2” 是将其中的函数  $ f(x)=\arctan x $ 在点  $ x_k $ 的泰勒公式较“方法1”多展开了一阶（拉格朗日中值定理是0阶泰勒公式），则更为简洁.

(2) 将该题中的  $ f(x) $ 换为其他函数，可构造出更多形式的加边极限问题.

# 11. 利用级数做计算

级数的敛散性就是其部分和数列的敛散性，所以数列与级数的敛散性无法分割。对某些形式（特别是无穷和形式）的数列极限借助于级数的相关知识来解决会更为方便。

例 56 求极限  $ \lim_{n\to\infty}\frac{n^{3}\ln(n!)}{a^n} $ (a>1).

分析 由于该分式分母增加的速度远比分子快，极限应该是 0，所以可利用收敛级数的通项必趋于 0 来判断.

解 考察级数  $ \sum_{n=1}^{\infty}\frac{n^{3}\ln(n!)}{a^{n}} $ 的收敛性. 记  $ u_{n}=\frac{n^{3}\ln(n!)}{a^{n}} $，因为

 $$ \begin{aligned}\lim_{n\rightarrow\infty}\frac{u_{n+1}}{u_{n}}&=\lim_{n\rightarrow\infty}\frac{(n+1)^{3}\ln\left[(n+1)!\right]}{a^{n+1}}\cdot\frac{a^{n}}{n^{3}\ln(n!)}\\&=\frac{1}{a}\lim_{n\rightarrow\infty}\left(\frac{n+1}{n}\right)^{3}\frac{\ln(n!)+\ln(n+1)}{\ln(n!)}=\frac{1}{a}<1,\end{aligned} $$ 

级数 $ \sum_{n=1}^{\infty}\frac{n^{3}\ln(n!)}{a^{n}} $收敛，所以 $ \lim_{n\to\infty}\frac{n^{3}\ln(n!)}{a^{n}}=0 $

评注 该方法只适用于极限为0的数列，而且是收敛速度较快的情况（即级数要收敛）。求该题的极限还有很多其他方法，如夹逼原理、单调有界原理等，读者可自行练习。

例 57 求  $ \lim_{n\to\infty}\left(\frac{1}{a}+\frac{2}{a^{2}}+\cdots+\frac{n}{a^n}\right)(a>1) $

分析 因为所求极限为级数  $ \sum_{n=1}^{\infty}\frac{n}{a^{n}} $ 的和，所以可借助幂级数的和函数来计算.

解 令  $ S(x)=\sum_{n=1}^{\infty}nx^{n} $ ( $ |x|<1 $)，则

 $$ S(x)=x\left(\sum_{n=1}^{\infty}x^{n}\right)^{\prime}=x\left(\frac{1}{1-x}\right)^{\prime}=\frac{x}{\left(1-x\right)^{2}}, $$ 

 $$ \lim_{n\to\infty}\left(\frac{1}{a}+\frac{2}{a^{2}}+\cdots+\frac{n}{a^{n}}\right)=S\left(\frac{1}{a}\right)=\frac{a}{(1-a)^{2}}. $$ 

评注 数列极限中，求无穷和形式的极限通常较为困难，解决这类问题没有普遍适用的方法，现将我们前面已涉及的方法罗列如下（读者要善于总结不同方法所适用的对象）：

（1）做初等运算，将和式化为有限运算形式，再求极限；

(2) 对和式做放缩，用夹逼原理求极限：

(3) 用施笃兹定理求极限：

(4) 化为定积分计算：

(5) 利用幂级数的和函数计算.

例 58 设  $ x_{1}=1 $,  $ x_{2}=4 $,  $ x_{n}=\frac{x_{n-1}+x_{n-2}}{2}(n\geqslant3) $，求  $ \lim_{n\to\infty}x_n $.

分析 该题采用递推公式两边同时取极限的方法无法算得极限. 从几何上看，点  $ x_{n} $ 是  $ x_{n-1} $ 与  $ x_{n-2} $ 的中点，所以  $ x_{n} $ 与  $ x_{n-1} $ 的距离是  $ x_{n-1} $ 与  $ x_{n-2} $ 距离的一半，这样就可得到数列  $ \{x_{n}-x_{n-1}\} $ 的一阶递推式，从而解出  $ x_{n} $.

 $$  解 \quad x_{k}-x_{k-1}=-\frac{1}{2}(x_{k-1}-x_{k-2})=\left(-\frac{1}{2}\right)^{2}(x_{k-2}-x_{k-3})=\cdots=\left(-\frac{1}{2}\right)^{k-2}(x_{2}-x_{1})=3\left(-\frac{1}{2}\right)^{k-2}. $$ 

k从2到n各式相加得

 $$ x_{n}-x_{1}=\sum_{k=2}^{n}(x_{k}-x_{k-1})=3\left[1-\frac{1}{2}+\frac{1}{2^{2}}+\cdots+\left(-\frac{1}{2}\right)^{n-2}\right], $$ 

所以

 $$ \lim_{n\to\infty}x_{n}=\sum_{n=2}^{\infty}3\left(-\frac{1}{2}\right)^{n-2}+x_{1}=\frac{3}{1+\frac{1}{2}}+1=3. $$ 

评注 该题的关键是得到了数列 $ \left\{x_{n}-x_{n-1}\right\} $的一阶递推式.

例  $ 59^{*} $ 设数列  $ \left\{a_{n}\right\} $ 满足： $ a_{1}=1,\quad a_{n+1}=\frac{a_{n}}{(n+1)(a_{n}+1)}\quad(n\geqslant1) $. 求极限  $ \lim_{n\to\infty}n!a_{n} $

分析 考察 $ \frac{1}{a_{n+1}} $，容易得到其一阶递推式，从而得到 $ a_{n} $的表达式，极限也就容易计算了.

解 利用归纳法易知  $ a_{n}>0(n\geqslant1) $. 由于

 $$ \begin{align*}\frac{1}{a_{n+1}}=&(n+1)\left(1+\frac{1}{a_{n}}\right)=(n+1)+(n+1)\frac{1}{a_{n}}\\=&(n+1)+(n+1)\left(n+n\frac{1}{a_{n-1}}\right)=(n+1)+(n+1)n+(n+1)n\frac{1}{a_{n-1}}\\=&(n+1)+(n+1)n+(n+1)n(n-1)+(n+1)n(n-1)\frac{1}{a_{n-2}}\\=&\cdots=(\dot{n}+1)!\left(\sum_{k=1}^{n}\frac{1}{k!}+\frac{1}{a_{1}}\right)=(n+1)!\sum_{k=0}^{n}\frac{1}{k!}.\end{align*} $$ 

因此

 $$ \lim_{n\to\infty}n!a_{n}=\lim_{n\to\infty}\left(\sum_{k=0}^{n-1}\frac{1}{k!}\right)^{-1}=\mathrm{e}^{-1}. $$ 

例 60 已知  $ x_{0}=1 $， $ x_{1}=\frac{1}{x_{0}^{3}+4} $， $ \cdots $， $ x_{n+1}=\frac{1}{x_{n}^{3}+4} $。求证：

（1）数列 $ \{x_{n}\} $收敛；

（2） $ \{x_{n}\} $ 的极限值 a 是方程  $ x^{4}+4x-1=0 $ 的唯一正根.

分析 易看出数列 $ \{x_{n}\} $不单调，所以不使用单调有界原理. 但容易证明级数 $ \sum_{n=0}^{\infty}(x_{n+1}-x_{n}) $绝对收敛，从而得到数列 $ \{x_{n}\} $收敛.

证明（1）易知0<x_{n}<1，且有

 $$ \begin{aligned}\left|x_{n+1}-x_{n}\right|=&\left|\frac{1}{x_{n}^{3}+4}-\frac{1}{x_{n-1}^{3}+4}\right|=\frac{\left|x_{n}^{3}-x_{n-1}^{3}\right|}{(x_{n}^{3}+4)(x_{n-1}^{3}+4)}\\<&\frac{\left|x_{n}-x_{n-1}\right|\left|x_{n}^{2}+x_{n}x_{n-1}+x_{n-1}^{2}\right|}{4^{2}}<\frac{3\left|x_{n}-x_{n-1}\right|}{16}\\<&\left(\frac{3}{16}\right)^{2}\left|x_{n-1}-x_{n-2}\right|<\cdots<\left(\frac{3}{16}\right)^{n}\left|x_{1}-x_{0}\right|=\frac{4}{5}\left(\frac{3}{16}\right)^{n}.\end{aligned} $$ 

因为 $ \sum_{n=0}^{\infty}\left(\frac{3}{16}\right)^{n} $收敛，所以 $ \sum_{n=0}^{\infty}(x_{n+1}-x_{n}) $收敛（绝对收敛），其部分和为 $ S_{n}=x_{n+1}-x_{0} $。故 $ \{x_{n}\} $收敛。

 $$ \lim_{n\to\infty}x_{n}=a $$ 

 $$ 0<x_{n}<1 $$ 

 $$ 0\leq a\leq1 $$ 

由  $ x_{n+1}=\frac{1}{x_{n}^{3}+4} $ 取极限得  $ a=\frac{1}{a^{3}+4} $. 显然  $ a\neq0 $，所以 a 是方程  $ x^{4}+4x-1=0 $ 的正根.

再由 $ (x^{4}+4x-1)^{\prime}=4x^{3}+4>0 $， $ x\in[0,1] $，知 $ f(x)=x^{4}+4x-1 $在 $ [0,1] $上严格单调递增，故根唯一.

评注 （1）数列  $ \{x_{n}\} $ 与级数  $ \sum_{n=1}^{\infty}(x_{n+1}-x_{n}) $ 有相同的敛散性. 要善于利用两者间的相互转化.

(2) 该题还可用以下两种方法证明有极限：

① 数列的偶数项单调递减，奇数项单调递增。用单调有界原理判定其奇、偶数项均有极限，再说明两极限相同；

② 利用介值定理及函数的单调性说明方程  $ x^{4}+4x-1=0 $ 在区间  $ (0,1) $ 内有唯一根，设为 a. 则有  $ \left|x_{n}-a\right|=\left|\frac{1}{x_{n-1}^{3}+4}-\frac{1}{a^{3}+4}\right|=\frac{(a-x_{n-1})(a^{2}+ax_{n-1}+x_{n-1}^{2})}{(x_{n-1}^{3}+4)(a^{3}+4)}<\frac{3}{16}\left|x_{n-1}-a\right|<\cdots<\left(\frac{3}{16}\right)^{n-1}\left|x_{1}-a\right|\rightarrow0(n\rightarrow\infty) $.

<div style="text-align: center;"><div style="text-align: center;">习题1.2</div> </div>


1. 求下列极限.

(1)

 $$ \lim_{n\to\infty}\left[\frac{3}{1^2\times2^2}+\frac{5}{2^2\times3^2}+\cdots+\frac{2n+1}{n^2\times(n+1)^2}\right]; $$ 

(2)  $ \lim_{n \to \infty} \frac{(1+x)}{x} \cdot \frac{(1+x^2)}{x^2} \cdot \frac{(1+x^4)}{x^4} \cdots \cdot \frac{(1+x^2^n)}{x^2^n} (x \neq 0,1) $;

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//795e591d-babc-48df-9bdf-0d84956b46a7/markdown_3/imgs/img_in_image_box_1182_1547_1317_1678.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A30Z%2F-1%2F%2Fc291c89ed2b00abdb91a1a4c875898d8dfd752e28a7627d0a3ff6acb72ce2ef2" alt="Image" width="9%" /></div>


习题1.2答案

(3)

 $$ \lim_{n\to\infty}\left(\frac{2^3-1}{2^3+1}\cdot\frac{3^3-1}{3^3+1}\cdot\frac{4^3-1}{4^3+1}\cdot\cdots\cdot\frac{n^3-1}{n^3+1}\right). $$ 

2. 求下列极限.

(1)  $ \lim_{x \to \infty} \frac{e^x - x \arctan x}{e^x + x} $; (2)  $ \lim_{x \to 0} \left( \frac{2 + e^{1/x}}{1 + e^{4/x}} + \frac{\sin x}{|x|} \right) $.

3. 计算极限  $ \lim_{x \to \infty} \sum_{k=0}^{n} (-1)^k C_n^k \sqrt{x^2 + k} $.

4. 设数列  $ \{x_{n}\} $ 满足  $ x_{1}=\sqrt{5} $， $ x_{n+1}=x_{n}^{2}-2(n=1,2,\cdots) $，求  $ \lim_{n\to\infty}\frac{x_1x_2\cdots x_n}{x_{n+1}} $.

5*. 设  $ f, g: \mathbb{R} \to \mathbb{R} $ 是周期函数，周期分别为  $ a, b $，且满足  $ \lim_{x \to 0} \frac{f(x)}{x} = u $， $ \lim_{x \to 0} \frac{g(x)}{x} = v \ne 0 $。证明  $ \lim_{n \to \infty} \frac{f\left((3 + \sqrt{7})^n a\right)}{g\left((2 + \sqrt{2})^n b\right)} $ 存在，并求该极限。

6*. 设[x]为不超过x的最大整数，记{x}=x-[x]。求极限 $ \lim_{n\to\infty}\left\{(2+\sqrt{3})^n\right\} $.

7. 求下列极限.

(1)  $ \lim_{x \to +\infty} [\cos \ln (1 + x) - \cos \ln x] $; (2)  $ \lim_{x \to 0^+} x \ln x \ln \left[ (1 + \sin x + \cos^2 x) / (1 - \sin x) \right] $.

8. 已知 $ \lim_{x\to0}\left(1-x+\frac{f(x)}{x^2}\right)^{\frac{1}{x}}=\mathrm{e} $，求 $ \lim_{x\to0}\frac{f(x)}{x^3} $.

9. 求下列极限.

(1)  $ \lim_{x \to 0} \frac{\ln \left( e^{\sin x} + \sqrt[3]{1 - \cos x} \right) - \sin x}{\arctan \left( 4\sqrt[3]{1 - \cos x} \right)} $;

(2)  $ \lim_{x \to \frac{\pi}{2}} \frac{(1 - \sqrt{\sin x})(1 - \sqrt[3]{\sin x}) \cdots (1 - \sqrt[n]{\sin x})}{(1 - \sin x)^{n-1}} $;

(3)  $ \lim_{x \to 0} \frac{(4 + \sin x)^x - 4^x}{\sqrt{\cos x} - 1} $;

(4)  $ \lim_{x \to +\infty} \frac{\left[ (x+1)^{1/x} - x^{1/x} \right] x^2 \ln^2 x}{x^{x^{1/x}} - x} $;

(5)  $ \lim_{n \to \infty} \left( \cos \pi \sqrt{1 + 4n^2} \right)^{n^2} $.

10. 设  $ f(x) $ 和  $ g(x) $ 在 x=0 的某一邻域 U 内有定义，对任意  $ x \in U $,  $ f(x) \neq g(x) $，且  $ \lim_{x \to 0} f(x) = \lim_{x \to 0} g(x) = a > 0 $，求  $ \lim_{x \to 0} \frac{\left[f(x)\right]^g(x) - \left[g(x)\right]^g(x)}{f(x) - g(x)} $.

11. 设  $ F(x)=\left(\frac{a_{1}^{x}+a_{2}^{x}+\cdots+a_{n}^{x}}{n}\right)^{\frac{1}{x}} $， $ a_{1},a_{2},\cdots,a_{n} $ 都是正数，求下列极限.

(1)  $ \lim_{x \to +\infty} F(x) $; (2)  $ \lim_{x \to -\infty} F(x) $; (3)  $ \lim_{x \to 0} F(x) $.

(1)  $ \lim_{n \to \infty} \sqrt[n]{1 + \sqrt{2 + \sqrt[3]{3 + \cdots + \sqrt[n]{n}}}} $; (2)  $ \lim_{n \to \infty} (n!)^{\frac{1}{n^2}} $; (3)  $ \lim_{n \to \infty} \sum_{k=1}^{n} \frac{n + k}{n^2 + k} $;

(4)  $ \lim_{n \to \infty} \sqrt[n]{\sum_{k=1}^{n} \frac{1}{\sqrt[k]{k}}}  $; (5)  $ \lim_{n \to \infty} \frac{(2n-1)!!}{(2n)!!}  $; (6)  $ \lim_{n \to \infty} (n! e - [n! e]) $. 其中  $ [\cdot] $ 为取整函数.

13*. 设  $ f_{1}(x)=x $,  $ f_{2}(x)=x^{x} $,  $ f_{3}(x)=x^{x^{x}} $,  $ \cdots $,  $ f_{n}(x)=x^{x^{x-x}} $ 共 n 个. 求极限  $ \lim_{x\to0^{+}}f_{n}(x) $.

14. 设  $ x_{1}=2 $,  $ x_{2}=2+\frac{1}{x_{1}} $,  $ \cdots $,  $ x_{n+1}=2+\frac{1}{x_{n}} $,  $ \cdots $, 证明  $ \lim_{n\to\infty}x_n $ 存在；记  $ \lim_{n\to\infty}x_n=A $, 求

 $$ \lim_{n\to\infty}4^{n}(x_{n}-A) $$ 

15*. 设  $ x_{1}=2023 $， $ x_{n}^{2}-2(x_{n}+1)x_{n+1}+2023=0 $ ( $ n=1,2,\cdots $)，证明  $ \lim_{n\to\infty}x_n $ 存在，并求其值.

16. 已知  $ x_1 = \frac{\pi}{2023} $,  $ y_1 = \frac{\pi}{2022} $，且  $ x_{n+1} = \sin x_n $,  $ y_{n+1} = \sin y_n $ ( $ n=1,2,\cdots $)，求  $ \lim_{n \to \infty} \frac{x_n}{y_n} $.

 $ 17^* $. 设函数  $ f: [0, +\infty) \to \mathbb{R} $，且满足  $ x = f(x) e^{f(x)} $，证明  $ \lim_{x \to +\infty} \frac{f(x)}{\ln x} $ 存在，并求极限.

18. 设  $ x_{1}>0 $， $ x_{n+1}=1-e^{-x_{n}}(n=1,2,\cdots) $，证明  $ \lim_{n\to\infty}x_n $ 存在，并求其值.

19. 设  $ x_{1} = -1 $， $ 4x_{n}x_{n+1} + 3x_{n} + x_{n+1} + 1 = 0 (n = 1, 2, \cdots) $，证明数列  $ \left\{x_{n}\right\} $ 收敛，并求极限  $ \lim_{n \to \infty} x_{n} $

20. 设数列  $ \{x_{n}\} $ 满足  $ 0 < x_{1} < \pi $， $ x_{n+1} = \sin x_{n} (n=1,2,\cdots) $，求  $ \lim_{n \to \infty} \left( \frac{x_{n+1}}{\tan x_n} \right)^{\frac{1}{x_n^2}} $。

21 $ ^{*} $. 设  $ x_{1} = \frac{1}{1} $， $ x_{2} = \frac{1}{1 + \frac{1}{1}} $， $ x_{3} = \frac{1}{1 + \frac{1}{1 + \frac{1}{1}}} $， $ \cdots $。求  $ \lim_{n \to \infty} x_{n} $。

22. 设  $ x_{n+1} = x_n (2 - Ax_n) (n = 0, 1, 2, \cdots) $，其中 A > 0。确定初始值  $ x_0 $，使得  $ \{x_n\} $ 收敛。

23. 设曲线  $ y = f(x) $ 在原点与  $ y = \sin x $ 相切，试求极限  $ \lim_{n \to \infty} n^{\frac{1}{2}} \sqrt{f\left(\frac{2}{n}\right)} $.

24. 设函数  $ f(x) > 0 $，在 x = a 处可导，试求  $ \lim_{n \to \infty} \left[ \frac{f(a+1/n)}{f(a-1/n)} \right]^n $.

25. 设  $ y = y(x) $ 是由方程  $ \arctan xy + e^{2y} (\cos x + \sin x) = 1 $ 确定的隐函数，求  $ \lim_{x \to 0} \left( \frac{1 - y(x)}{1 + y(x)} \right)^{1/x} $

26. 求下列极限.

(1)  $ \lim_{x \to +\infty} x^2 \ln \frac{\arctan(x+1)}{\arctan x} $; (2)  $ \lim_{x \to 0} \frac{\tan(\tan x) - \tan(\sin x)}{\sqrt{1 + x - \frac{1}{2} x^2} - \sqrt{1 + \ln(1+x)}} $.

27. 如图1.2所示，弦PQ所对的圆心角为 $ \theta $，设 $ A(\theta) $是弦PQ与弧PQ之间的面积， $ B(\theta) $是切线长PR、QR与弧之间的面积，求极限 $ \lim_{\theta\to0^{+}}\frac{A(\theta)}{B(\theta)} $.

28. 求下列极限.

(1)  $ \lim_{x \to 0} \left( \frac{1}{x^2} - \cot^2 x \right) $; (2)  $ \lim_{x \to \frac{\pi}{2}} \frac{1 - \sin^{\alpha + \beta} x}{\sqrt{(1 - \sin^{\alpha} x)(1 - \sin^{\beta} x)}} $;

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//eba342cc-0683-419f-b5dc-5c0c7a4c258d/markdown_1/imgs/img_in_image_box_951_1472_1316_1737.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A29Z%2F-1%2F%2F7c84c2f4c16fcc18d3220584945184cc457b43689750d1aad254a94ee07b375f" alt="Image" width="25%" /></div>


(3)  $ \lim_{x \to +\infty} \left[ \left( x^3 + \frac{x}{2} - \tan \frac{1}{x} \right) e^{1/x} - \sqrt{1 + x^6} \right] $.

<div style="text-align: center;"><div style="text-align: center;">图1.2</div> </div>


29. 确定 a, b 的值，使当  $ x \to 0 $ 时， $ f(x) = e^x - \frac{1 + ax}{1 + bx} $ 为 x 的三阶无穷小.

 $ 30^* $. 设数列  $ \{a_n\} $ 满足  $ \lim_{n \to \infty}(2a_n + a_{n-1}) = 0 $，证明： $ \lim_{n \to \infty} a_n = 0 $.

31*. 设  $ f(x) $ 在区间  $ [0,a] $ 上有二阶连续导数， $ f'(0)=1 $， $ f''(0)\neq0 $，且  $ 0<f(x)<x $， $ x\in(0,a) $。令  $ x_{n+1}=f(x_n) $， $ x_1\in(0,a) $。

（1）证明 $ \left\{x_{n}\right\} $收敛并求极限；

(2) 试问  $ \{nx_n\} $ 是否收敛？若不收敛，说明理由；若收敛，求其极限。

 $ 32^* $. 设  $ x_1 > 0 $， $ x_{n+1} = \arctan x_n $ ( $ n=1,2,\cdots $)，证明  $ \lim_{n \to \infty} \sqrt{\frac{2n}{3}} x_n = 1 $。

 $ 33^* $. 设  $ 0 < \lambda < 1 $， $ x_n > 0 $，且  $ \lim_{n \to \infty} x_n = a $，求  $ \lim_{n \to \infty} (x_n + \lambda x_{n-1} + \cdots + \lambda^n x_0) $。

 $ 34^* $. 设  $ m $ 为正整数， $ I_n = \frac{1^m + 2^m + \cdots + n^m}{n^m} - \frac{n}{m+1} $，求  $ \lim_{n \to \infty} I_n $。

 $ 35^* $. 设  $ x_n = \sum_{k=1}^{n} \frac{e^{k^2}}{k} y_n = \int_0^n e^{x^2} \, dx $，求  $ \lim_{n \to \infty} \frac{x_n}{y_n} $。

36*. 设  $ f(x) $ 在  $ (-1,1) $ 内三阶连续可导，满足  $ f(0)=0 $， $ f'(0)=1 $， $ f''(0)=0 $， $ f'''(0)=-1 $；又设数列  $ \{a_n\} $ 满足  $ a_1 \in (0,1) $， $ a_{n+1} = f(a_n) $ ( $ n=1,2,\cdots $) 严格单调递减且  $ \lim_{n \to \infty} a_n = 0 $。计算  $ \lim_{n \to \infty} na_n^2 $。

(1)  $ \lim_{n \to \infty} \frac{n^2}{\ln^2 n} \left( \sqrt[n]{n} - 1 - \frac{n}{\ln n} \right) $;

(2)  $ \lim_{x \to \infty} e^{-x} \left( 1 + \frac{1}{x} \right)^{x^2} $;

(3)  $ \lim_{x \to 0} \frac{\cos x - e^{\frac{x^2}{2}} + \frac{x^4}{12}}{\sin^6 x} $;

(4)  $ \lim_{x \to 0^+} \frac{x^{\sin x} - (\sin x)^x}{x^{\sin x} - (\sin x)^x} $

38. 当  $ x \to 0 $ 时， $ f(x) = \sqrt[5]{x^2 + \sqrt[3]{x}} - \sqrt[3]{x^2 + \sqrt[5]{x}} $ 是关于 x 的几阶无穷小？

39. 已知  $ \lim_{x \to 0} \frac{(1+x)^{\frac{1}{x}} - (A+Bx+Cx^2)}{x^3} = D \neq 0 $，求常数 A, B, C, D.

40. 求非零常数  $ A $ 与  $ a $ 的值，使  $ \lim_{x \to \infty} x^a \left[ (2x+1) \arcsin \frac{1}{2x+1} - (x+1) \arcsin \frac{1}{x+1} \right] = A $.

41. 求下列极限.

(1)  $ \lim_{n \to \infty} \sum_{k=1}^{n} \sin \left( \frac{1}{n+k} \right) $;

(2)  $ \lim_{n \to \infty} \sum_{k=1}^{n} \ln \frac{n+k}{n+k+1} $;

(3)  $ \lim_{n \to \infty} \sum_{k=1}^{n-1} \left( 1 + \frac{k}{n} \right) \sin \left( \frac{k\pi}{n^2} \right) $;

(4)  $ \lim_{n \to \infty} \frac{1 + \sqrt{2} + \cdots + \sqrt{n}}{\sqrt{n+1} + \sqrt{n+2} + \cdots + \sqrt{n+n}} $;

(5)  $ \lim_{n \to \infty} \frac{(n^2+1)(n^2+2)\cdots(n^2+n)}{(n^2-1)(n^2-2)\cdots(n^2-n)} $.

42. 求下列极限.

(1)  $ \lim_{n \to \infty} \sum_{k=1}^{n} \frac{e^{\frac{k}{n}}}{n + \frac{1}{k}} $;

(2)  $ \lim_{n \to \infty} \sum_{i=1}^{n} \frac{1}{n + \frac{k^2 + 1}{n}} $;

(3)  $ \lim_{n \to \infty} \sum_{k=1}^{n} \frac{\sqrt{kn - 1}}{kn} $;

(4*)  $ \lim_{n \to \infty} \left( \frac{1}{n} - \sin \frac{1}{n} \right)^{\frac{1}{3}} \sqrt[n]{n!} $.

43. 设  $ x_{n}=1+\frac{1}{\sqrt{2}}+\cdots+\frac{1}{\sqrt{n}}-2\sqrt{n} $，证明数列  $ \{x_{n}\} $ 收敛.

44. 设  $ a_{n}=(1+x)(1+x^{2})\cdots(1+x^{n}) $ (0 < x < 1)，证明极限  $ \lim_{n \to \infty} a_{n} $ 存在.

45. 求下列极限.

(1)  $ \lim_{n \to \infty} \frac{5^n n!}{(2n)^n} $; (2)  $ \lim_{n \to \infty} \left[ \frac{1}{2!} + \frac{2}{3!} + \cdots + \frac{n}{(n+1)!} \right] $.

46. 设  $ x_1=1 $,  $ x_2=2 $，且  $ x_{n+2}=\sqrt{x_{n+1}\cdot x_n} $ ( $ n=1,2,\cdots $)，求  $ \lim_{n\to\infty}x_n $.

47. 序列  $ x_{0}, x_{1}, x_{2}, \cdots $ 由下列条件定义： $ x_{0} = a $,  $ x_{1} = b $,  $ x_{n+1} = \frac{x_{n-1} + (2n-1)x_n}{2n} $,  $ n \geq 1 $. 这里 a 与 b 是已知数，试用 a 与 b 表示  $ \lim_{x \to \infty} x_n $.

## 1.3 连续

连续的概念：

 $ f(x) $ 在点  $ x_0 $ 连续  $ \Leftrightarrow \lim_{x \to x_0} f(x) = f(x_0) \Leftrightarrow \lim_{\Delta x \to 0} \Delta y = \lim_{\Delta x \to 0} [f(x_0 + \Delta x) - f(x_0)] = 0 $.

间断点的分类：

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//eba342cc-0683-419f-b5dc-5c0c7a4c258d/markdown_3/imgs/img_in_image_box_365_894_1001_1306.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A33Z%2F-1%2F%2F6ce1f86c4c8e1c839c58791610a404ea3781144947b581453245f3412a24e244" alt="Image" width="43%" /></div>


函数的连续性是微积分的重要基础。连续函数有许多良好的性质，它为问题的研究带来方便。例如，函数在连续点局部有界、局部保号，这对我们做出某些判断很有帮助；连续函数符号与极限符号可交换，这对极限的计算十分方便；闭区间上的连续函数具有良好的整体性质，如有界性定理、最值定理、介值定理和一致连续定理均成立。连续是函数可微的必要条件，是可积的充分条件，函数的很多性质都与其连续性有关。

例1 设 $ f(x)=\lim_{n\to\infty}\frac{\ln(e^n+x^n)}{n} $ (x>0)，讨论 $ f(x) $在定义域内是否连续.

分析 求出极限，得到函数的显表达式，再讨论其连续性.

解 当 0 < x ≤ e 时，有

 $$ f(x)=\lim_{n\to\infty}\frac{\ln(\mathrm{e}^{n}+x^{n})}{n}=\lim_{n\to\infty}\frac{\ln\mathrm{e}^{n}\left(1+\frac{x^{n}}{\mathrm{e}^{n}}\right)}{n}=\lim_{n\to\infty}\frac{n+\ln\left[1+\left(\frac{x}{\mathrm{e}}\right)^{n}\right]}{n}=1. $$ 

当 x > e 时，有

 $$ f(x)=\lim_{n\to\infty}\frac{\ln(e^{n}+x^{n})}{n}=\lim_{n\to\infty}\frac{\ln x^{n}\left(\frac{e^{n}}{x^{n}}+1\right)}{n}=\lim_{n\to\infty}\frac{n\ln x+\ln\left[\left(\frac{e}{x}\right)^{n}+1\right]}{n}=\ln x, $$ 

得

 $$ f(x)=\left\{\begin{aligned}&1,&0<x\leq\mathrm{e}\\ &\ln x,&x>\mathrm{e}\end{aligned}\right.. $$ 

又  $ \lim_{x\to e^-}f(x)=1 $， $ \lim_{x\to e^+}f(x)=\lim_{x\to e^+}\ln x=1 $，则  $ \lim_{x\to e}f(x)=1=f(e) $，所以  $ f(x) $ 在 x=e 处连续。

显然， $ f(x) $ 在 0 < x < e 与 x > e 内是连续的，所以  $ f(x) $ 在其定义域 x > 0 内连续.

例2 已知  $ f(x) $ 是三次多项式，且有  $ \lim_{x \to 2a} \frac{f(x)}{x - 2a} = \lim_{x \to 4a} \frac{f(x)}{x - 4a} = 1 $，求  $ \lim_{x \to 3a} \frac{f(x)}{x - 3a} $.

分析 由已知的两个极限式就可确定  $ f(x) $ 的两个一次因子以及两个待定系数，所以  $ f(x) $ 就完全确定了.

解 由已知，有  $ \lim_{x\to2a}f(x)=\lim_{x\to4a}f(x)=0 $，由  $ f(x) $ 处处连续，知  $ f(2a)=f(4a)=0 $。所以

 $$ f(x)=(Ax+B)(x-2a)(x-4a), $$ 

 $$ \lim_{x\to2a}\frac{f(x)}{x-2a}=\lim_{x\to2a}(Ax+B)(x-4a)=(2aA+B)(-2a)=1, $$ 

 $$ \lim_{x\to4a}\frac{f(x)}{x-4a}=\lim_{x\to4a}(Ax+B)(x-2a)=(4aA+B)(2a)=1. $$ 

解得  $ A=\frac{1}{2a^{2}} $， $ B=-\frac{3}{2a} $。从而有

 $$ \lim_{x\to3a}\frac{f(x)}{x-3a}=\lim_{x\to3a}\frac{\frac{1}{2a^{2}}(x-3a)(x-2a)(x-4a)}{x-3a}=-\frac{1}{2}. $$ 

例 3 设  $ f(x) $ 在区间  $ (0,1) $ 有定义，且  $ e^{x}f(x) $ 与  $ e^{-f(x)} $ 在  $ (0,1) $ 上都是单调递增函数，证明  $ f(x) $ 在  $ (0,1) $ 内连续.

分析 由于单调函数在其定义区间内的任一点都具有左、右极限，所以只需考察  $ f(x) $ 在任意点  $ x_0 \in (0,1) $ 的左、右连续性.

证明 对于  $ x_0 \in (0,1) $，当  $ x_0 < x < 1 $ 时，因为  $ e^x f(x) $ 单调递增，故有

 $$ \mathbf{e}^{x_{0}}\;f(x_{0})\leqslant\mathbf{e}^{x}\;f(x)\Rightarrow\mathbf{e}^{x_{0}-x}\;f(x_{0})\leqslant f(x)\;. $$ 

因为 $ e^{-f(x)} $单调递增，故有

 $$ \mathrm{e}^{-f(x_{0})}\leqslant\mathrm{e}^{-f(x)}\Rightarrow\frac{1}{\mathrm{e}^{f(x_{0})}}\leqslant\frac{1}{\mathrm{e}^{f(x)}}\Rightarrow f(x_{0})\geqslant f(x). $$ 

从而有

 $$ \mathrm{e}^{x_{0}-x}f(x_{0})\leqslant f(x)\leqslant f(x_{0}). $$ 

令  $ x \to x_{0}^{+} $，取极限得  $ f(x_{0} + 0) = f(x_{0}) $，说明  $ f(x) $ 在点  $ x_{0} $ 右连续.

同理，当 0 < x < x_{0} 时，可证得  $ f(x) $ 在点  $ x_{0} $ 左连续.

因此， $ f(x) $ 在点  $ x_{0} $ 处连续。由点  $ x_{0} $ 在  $ (0,1) $ 中的任意性，知  $ f(x) $ 在  $ (0,1) $ 内连续。

评注 单调性给出了函数值的大小关系，要得到极限等式(极限值等于函数值)，自然会想到夹逼原理。例4 讨论下面函数的连续性，若有间断点，则指出其类型。

 $$ f(x)=\left\{\begin{aligned}&\frac{x(2x+\pi)}{2\cos x},&x\leq0,\\&\sin\frac{1}{x^{2}-1},&x>0.\end{aligned}\right.. $$ 

分析 函数没定义的点一定是间断点；分段点也可能出现间断，需讨论左、右连续性.

解 函数在 x=1 以及  $ -k\pi-\frac{\pi}{2} $ (k=0,1,2, $ \cdots $) 处都没定义，所以这些点都是间断点.

在分段点 x=0 处， $ f(+0)=-\sin1 $， $ f(-0)=0 $，所以 x=0 为第一类跳跃间断点；

而  $ \lim_{x\to1}f(x)=\lim_{x\to1}\sin\frac{1}{x^{2}-1} $ 不存在，所以 x=1 为第二类振荡间断点；

 $ \lim_{x\to-\frac{\pi}{2}}\frac{x(2x+\pi)}{2\cos x}=-\frac{\pi}{2} $，所以 $ x=-\frac{\pi}{2} $为第一类可去间断点；

 $ \lim_{x \to -k\pi - \frac{\pi}{2}} \frac{x(2x + \pi)}{2\cos x} = \infty $ (k = 1, 2,  $ \cdots $)，所以  $ x = -k\pi - \frac{\pi}{2} $ 为第二类无穷间断点.

例5 设  $ f $ 在  $ (a,b) $ 内每一点处的左、右极限都存在，又  $ \forall x,y\in(a,b) $，有

 $$ f\left(\frac{x+y}{2}\right)\leqslant\frac{1}{2}\left[f(x)+f(y)\right], $$ 

证明 f 在  $ (a,b) $ 内连续.

分析 只需证明 f 在  $ (a,b) $ 内任一点的左、右极限都与其函数值相等.

证明  $ \forall x_0 \in (a,b) $，记  $ f(x_0 - 0) = A^-(x_0 + b) = A^+(b - b) $， $ f(x_0 + b) = A^+(b - b) = A^+(b - b) $。

下面证明  $ A^{-}=A^{+}=f(x_{0}) $

在所给不等式中，令  $ x = x_{0} $，分别取  $ y \to x_{0}^{-} $ 与  $ y \to x_{0}^{+} $，得

 $$ \left\{\begin{aligned}{}&{{}A^{-}\leqslant\frac{1}{2}f(x_{0})+\frac{1}{2}A^{-},}\\ {}&{{}A^{+}\leqslant\frac{1}{2}f(x_{0})+\frac{1}{2}A^{+}.}\\ \end{aligned}\right.\Rightarrow\left\{\begin{aligned}{}&{{}A^{-}\leqslant f(x_{0}),}\\ {}&{{}A^{+}\leqslant f(x_{0}).}\\ \end{aligned}\right. $$ 

在所给不等式中，又令  $ x = x_{0} - h $,  $ y = x_{0} + h $，取  $ h \to 0^{+} $ 得

 $$ f(x_{0})\leqslant\frac{1}{2}(A^{-}+A^{+}). $$ 

由①，②式可得 $ A^{-}=A^{+}=f(x_{0}) $。由 $ x_{0} $的任意性知f在 $ (a,b) $内连续。

评注 该题的等价命题：区间 I 上的凸（凹）函数不可能有第一类间断点.

例6 设  $ f \in C[a,+\infty) $，并且  $ \lim_{x \to a} f(x) $ 存在，证明  $ f $ 在  $ [a,+\infty) $ 上有界.

分析 由  $ \lim_{x \to +\infty} f(x) $ 存在，知  $ \exists X > 0 $， $ f(x) $ 在  $ (X, +\infty) $ 内有界； $ f(x) $ 在  $ [a, X] $ 上显然有界。从而问题得到解决。

证明 若  $ \lim_{x \to +\infty} f(x) $ 存在，不妨设  $ \lim_{x \to +\infty} f(x) = a $.

对  $ \varepsilon=1 $， $ \exists X>0 $，当 x>X 时，有  $ \left|f(x)-a\right|<1 $。所以，在  $ (X,+\infty) $ 内，有  $ \left|f(x)\right|<\left|a\right|+1 $。

又 $ f(x) $在 $ [a,X] $上连续，故 $ f(x) $在 $ [a,X] $上有界，即 $ \exists M_{1}>0 $，使 $ \left|f(x)\right|<M_{1} $

取  $ M = \max\left\{M_1, |a| + 1\right\} $，则  $ \forall x \in [a, +\infty) $，有  $ \left|f(x)\right| < M $。

评注 一般情况，若  $ f(x) \in C(a,b) $，且  $ \lim_{x \to a^+} f(x) $， $ \lim_{x \to b^-} f(x) $ 均存在，则  $ f(x) $ 在区间  $ (a,b) $ 内一定有界，其中  $ (a,b) $ 可以为无穷区间  $ (-\infty,+\infty) $。

例 7 设函数  $ f(x) $ 在  $ [a,b] $ 上连续，且 a < c < d < b，证明在  $ (a,b) $ 内至少存在一个  $ \xi $，使得  $ pf(c) + qf(d) = (p+q)f(\xi) $。其中 p,q 为任意正常数。

分析 只需证明  $ \frac{pf(c)+qf(d)}{d+a} $ 介于函数  $ f(x) $ 的最小值与最大值之间.

证明 方法1 因为  $ f(x) $ 在  $ [a,b] $ 上连续，则  $ f(x) $ 在  $ [a,b] $ 上有最大值 M、最小值 m，即有

 $$ m\leq f(x)\leq M $$ 

又  $ c,d\in[a,b] $，且 p,q>0，所以

 $$ \begin{aligned}{p m}&{{}\leq p f(c)\leq p M,~q m\leq q f(d)\leq q M}\\ {\Rightarrow(p+q)}&{{}m\leq p f(c)+q f(d)\leq(p+q)M,}\\ {}&{{}\Rightarrow m\leq\frac{p f(c)+q f(d)}{p+a}\leq M,}\\ \end{aligned} $$ 

由介值定理，知在 $ [a,b] $内至少存在一个 $ \xi $，使得

 $$ f(\xi)=\frac{pf(c)+qf(d)}{p+q}\quad 即 \quad pf(c)+qf(d)=(p+q)f(\xi). $$ 

方法 2 令  $ F(x)=(p+q)f(x)-pf(c)-qf(d) $，由已知， $ f(x) $ 在  $ [a,b] $ 上连续，所以  $ F(x) $ 在  $ [a,b] $ 上连续。又

 $$ F(c)=(p+q)f(c)-p f(c)-q f(d)=q[f(c)-f(d)], $$ 

 $$ F(d)=(p+q)f(d)-p f(c)-q f(d)=p[f(d)-f(c)]\;. $$ 

当  $ f(c)-f(d)=0 $ 时，c,d 均可取  $ \xi $

当  $ f(c)-f(d)\neq0 $ 时，又 p>0, q>0，于是有

 $$ F(c)F(d)=-p q[f(c)-f(d)]^{2}<0~, $$ 

由零点定理，知至少存在一个 $ \xi\in(c,d)\subset(a,b) $，使得

 $$ F(\xi)=0\quad 即 \quad pf(c)+qf(d)=(p+q)f(\xi)\ . $$ 

评注 类似可证明，若  $ f(x) \in C(a,b) $， $ \forall x_i \in (a,b) $，以及  $ \forall \lambda_i \in (0,1) (i=1,2,\cdots,n) $， $ \sum_{i=1}^{n} \lambda_i = 1 $，则至少存在一点  $ \xi \in (a,b) $，使  $ f(\xi) = \sum_{i=1}^{n} \lambda_i f(x_i) $（称  $ \sum_{i=1}^{n} \lambda_i f(x_i) $ 为  $ f(x_i) (i=1,2,\cdots,n) $ 的加权平均值）。

例 8 设  $ f(x) $ 在  $ [0,1] $ 上连续， $ f(0)=f(1) $，证明对于任意正整数 n，必存在  $ x_n \in (0,1) $ 使  $ f(x_n)=f\left(x_n+\frac{1}{n}\right) $.

分析 记  $ \varphi(x)=f(x)-f\left(x+\frac{1}{n}\right) $，由上题知  $ \varphi(x) $ 在  $ (0,1) $ 内一定可取到  $ \frac{1}{n}\sum_{i=0}^{n-1}\varphi\left(\frac{i}{n}\right) $，由已知条件易得到  $ \frac{1}{n}\sum_{i=0}^{n-1}\varphi\left(\frac{i}{n}\right)=0 $；也可用反证法证明.

证明 方法 1 令  $ \varphi(x)=f(x)-f\left(x+\frac{1}{n}\right) $，由  $ f(x)\in C[0,1] $，知  $ \varphi(x)\in C\left[0,1-\frac{1}{n}\right] $，所以  $ \varphi(x) $ 存在最大值（设为 M）与最小值（设为 m）。则有

 $$ m\leqslant\varphi\left(\frac{i}{n}\right)\leqslant M\ (i=0,1,\cdots,n-1)\ . $$ 

所以  $ m \leqslant \frac{1}{n} \sum_{i=0}^{n-1} \varphi\left(\frac{i}{n}\right) \leqslant M $，则存在  $ x_{n} \in \left[0,1 - \frac{1}{n}\right] $，使

 $$ \begin{align*}\varphi(x_{n})=&\frac{1}{n}\sum_{i=0}^{n-1}\varphi\bigg(\frac{i}{n}\bigg)=\varphi(0)+\varphi\bigg(\frac{1}{n}\bigg)+\cdots+\varphi\bigg(\frac{n-1}{n}\bigg)\quad.\\=&f(0)-f\bigg(\frac{1}{n}\bigg)+f\bigg(\frac{1}{n}\bigg)-f\bigg(\frac{2}{n}\bigg)+\cdots+f\bigg(\frac{n-1}{n}\bigg)-f(1)\\=&f(0)-f(1)=0\;.\end{align*} $$ 

即

 $$ f(x_{n})=f\left(x_{n}+\frac{1}{n}\right). $$ 

方法2（反证法） 若对$\forall x\in(0,1)$，均有$f(x)>f\left(x+\frac{1}{n}\right)$。取$x_{k}=\frac{k}{n}\left(k=0,1,\cdots,\frac{n-1}{n}\right)$，得

 $$ f(0)>f\left(\frac{1}{n}\right)>f\left(\frac{2}{n}\right)>\cdots>f(1)~, $$ 

这与已知矛盾.

同理在(0,1)内，不可能恒有  $ f(x) < f\left(x + \frac{1}{n}\right) $，所以必存在  $ x_n \in (0,1) $ 使  $ f(x_n) = f\left(x_n + \frac{1}{n}\right) $.

例9 设 $ F_{n}(x)=\ln(1+x)+\ln^{2}(1+x)+\cdots+\ln^{n}(1+x) $，证明对任意自然数n，方程 $ F_{n}(x)=1 $在区间 $ (0,e-1) $内有唯一实根 $ x_{n} $，且 $ \lim_{n\to\infty}x_{n}=\sqrt{e}-1 $.

分析 容易验证  $ F_{n}(x) $ 在区间  $ [0, e-1] $ 端点异号且在区间内  $ F_{n}^{\prime}(x) > 0 $，所以  $ x_{n} $ 存在且唯一。由于  $ x_{n} $ 满足方程  $ F_{n}(x_{n}) = 1 $，所以  $ \lim_{n \to \infty} x_{n} $ 的存在性与计算常用单调有界原理求极限的方法来实现。

解 显然  $ F_{n}(x) \in C[0, e-1] $，且  $ F_{n}(0) = 0 < 1 $， $ F_{n}(e-1) = n > 1 $，所以  $ F_{n}(x) = 1 $ 在  $ (0, e-1) $ 内有根  $ x_{n} $。又

 $$ F_{n}^{\prime}(x)=\frac{1}{1+x}+\frac{2\ln(1+x)}{1+x}+\cdots+\frac{n\ln^{n-1}(1+x)}{1+x}>0 $$ 

所以  $ F_{n}(x)=1 $ 在  $ (0,e-1) $ 内的根唯一.

由于

 $$ F_{n}(x_{n-1})=F_{n-1}(x_{n-1})+\ln^{n}(1+x_{n-1})=1+\ln^{n}(1+x_{n-1})>1=F_{n}(x_{n}), $$ 

又 $ F_{n}(x) $严格单调递增，所以 $ x_{n-1}>x_{n} $，即 $ \{x_{n}\} $单调递减有下界，所以有极限，设 $ \lim_{n\to\infty}x_n=a $

显然0<a<e-1，且有

 $$ F_{n}(x)=\frac{\ln(1+x)-\ln^{n+1}(1+x)}{1-\ln(1+x)}, $$ 

在等式  $ F_{n}(x_{n})=1 $ 两边取极限，得

 $$ \frac{\ln(1+a)}{1-\ln(1+a)}=1\Longrightarrow\ln(1+a)=\frac{1}{2}\Longrightarrow a=\sqrt{\mathsf{e}}-1. $$ 

评注 该题的一般性结论：设  $ f(x) $ 在  $ [a,b] $ 内单调连续，且  $ 0 \leq f(x) \leq 1 $，若方程  $ f(x) + f^2(x) + \cdots + f^n(x) = 1 $ 在  $ (a,b) $ 内有根  $ x_n $，则  $ \{x_n\} $ 必收敛，且  $ \lim_{n \to \infty} x_n = f^{-1}\left(\frac{1}{2}\right) $.

例10 设 $ f \in C[a,b] $，且 $ \forall x \in [a,b] $， $ \exists y \in [a,b] $，使 $ f(y)=\frac{1}{2}|f(x)| $，证明 $ \exists\xi \in [a,b] $，使 $ f(\xi)=0 $。

分析 若  $ f(x) $ 恒为零，所证结论显然成立。否则必有  $ f(x) $ 大于 0 的点，从而只需证明还有  $ f(x) $ 小于 0 的点，为此可考虑函数的最小值点。

证明 方法1 因为  $ f(x) \in C[a,b] $，所以  $ \exists x_0 \in [a,b] $，使  $ f(x_0) = \min_{a \leq x \leq b} \{f(x)\} $.

若  $ f(x_{0})=0 $，则  $ \xi=x_{0} $ 即为所求；

若  $ f(x_0) \neq 0 $，则必有  $ f(x_0) < 0 $，否则  $ \exists y_0 \in [a, b] $，使

 $$ f(y_{0})=\frac{1}{2}\big|f(x_{0})\big|=\frac{1}{2}f(x_{0})<f(x_{0}), $$ 

这与  $ f(x_{0}) $ 为  $ f(x) $ 的最小值相矛盾.

由于 $ f(x_0)<0 $， $ f(y_0)=\frac{1}{2}|f(x_0)|>0 $，由介值定理，知在 $ x_0 $与 $ y_0 $之间存在 $ \xi $，使 $ f(\xi)=0 $。

方法2 由 $ f(y)=\frac{1}{2}\big|f(x)\big| $，对于 $ a,\ \exists x_1\in[a,b] $，使 $ f(x_1)=\frac{|f(a)|}{2} $；对于 $ x_1,\ \exists x_2\in[a,b] $，使 $ f(x_2)=\frac{|f(a)|}{2^2} $。以此类推，可得到数列 $ x_n\in[a,b] $，满足

 $$ f(x_{n})=\frac{\left|f(a)\right|}{2^{n}} $$ 

则  $ \lim_{n\to\infty}f(x_n)=\lim_{n\to\infty}\frac{f(a)}{2^n}=0 $.

因为$\{x_n\}$有界，所以存在收敛子列$\{x_{n_k}\}$，令$x_{n_k} \to \xi (k \to \infty)$，有$\lim_{k \to \infty} f(x_{n_k}) = 0$。又$f(x) \in C[a, b]$，所以$\lim_{k \to \infty} f(x_{n_k}) = f(\xi)$，即$f(\xi) = 0$。

例11 设 $ \varphi\in C(-\infty,+\infty) $，并且 $ \lim_{x\to\infty}\frac{\varphi(x)}{x^n}=0 $，证明：

（1）若 $ n $为奇数，则 $ \exists\xi\in(-\infty,+\infty) $，使 $ \xi^n+\varphi(\xi)=0 $；

（2）若 $ n $为偶数，则 $ \exists\eta\in(-\infty,+\infty) $，使 $ \forall x\in(-\infty,+\infty) $有 $ \eta^n+\varphi(\eta)\leq x^n+\varphi(x) $.

分析 做函数  $ f(x)=x^{n}+\varphi(x) $，对于问题（1）只需说明  $ f(x) $ 在区间  $ (-\infty,+\infty) $ 内会出现异号；对于问题（2）需证明  $ f(x) $ 能取到最小值.

证明 令  $ f(x)=x^{n}+\varphi(x) $，则  $ f(x)\in C(-\infty,+\infty) $.

（1）当n为奇数时，由已知条件，有

 $$ \operatorname*{l i m}_{x\to+\infty}f(x)=\operatorname*{l i m}_{x\to+\infty}x^{n}\left(1+\frac{\varphi(x)}{x^{n}}\right)=+\infty~,\qquad\operatorname*{l i m}_{x\to-\infty}f(x)=\operatorname*{l i m}_{x\to-\infty}x^{n}\left(1+\frac{\varphi(x)}{x^{n}}\right)=-\infty~. $$ 

则 $ \exists\xi\in(-\infty,+\infty) $，使 $ f(\xi)=0 $，即 $ \xi^{n}+\varphi(\xi)=0 $。

（2）当n为偶数时，由已知条件，有

 $$ \lim_{x\to\infty}f(x)=\lim_{x\to\infty}x^n\left(1+\frac{\varphi(x)}{x^n}\right)=+\infty, $$ 

对  $ M = |f(0)| + 1 > 0 $， $ \exists N > 0 $，当  $ |x| > N $ 时，总有  $ f(x) > M > f(0) $。

又  $ f(x) \in C[-N,N] $，所以  $ f(x) $ 在  $ [-N,N] $ 上有最小值，即  $ \exists \eta \in [-N,N] $，使  $ \forall x \in [-N,N] $，有  $ f(\eta) \leq f(x) $。

由于  $ f(\eta) \leq f(0) $，故对  $ \forall x \in (-\infty, +\infty) $，有  $ f(\eta) \leq f(x) $，即  $ \eta^n + \varphi(\eta) \leq x^n + \varphi(x) $。

例 12 证明若  $ a_{n} > |a_{n-1}| + |a_{n-2}| + \cdots + |a_{1}| + |a_{0}| $，则方程

 $$ a_{n}\cos nx+a_{n-1}\cos(n-1)x+\cdots+a_{1}\cos x+a_{0}=0 $$ 

在 $  (0,2\pi)  $内至少有2n个根.

分析 由所给条件，知当 $ \cos nx = -1 $时，方程左边的函数值为负（当 $ \cos nx = 1 $时，为正），而 $ \cos nx $是以 $ \frac{2\pi}{n} $为周期的函数，区间 $ (0,2\pi) $包含 $ \cos nx $的 $ n $个周期区间，故结论成立.

证明 记  $ f(x)=a_{n}\cos nx+a_{n-1}\cos(n-1)x+\cdots+a_{1}\cos x+a_{0} $

当  $ x = \frac{2k\pi}{n} (k \in \mathbb{N}) $ 时，

 $$ f\left(\frac{2k\pi}{n}\right)=a_{n}+a_{n-1}\cos\frac{2k(n-1)\pi}{n}+\cdots+a_{1}\cos\frac{2k\pi}{n}+a_{0} $$ 

 $$ >a_{n}-\left|a_{n-1}\right|-\left|a_{n-2}\right|-\cdots-\left|a_{1}\right|-\left|a_{0}\right|>0\;. $$ 

当  $ x = \frac{2k\pi}{n} + \frac{\pi}{n} (k \in \mathbb{N}) $ 时，

 $$ \begin{aligned}{f\bigg(\frac{2k\pi}{n}+}&{{}\frac{\pi}{n}\bigg)=-a_{n}+a_{n-1}\operatorname{c o s}\frac{(2k+1)(n-1)\pi}{n}+\cdots+a_{1}\operatorname*{c o s}\frac{(2k+1)\pi}{n}+a_{0}}\\ {}&{{}<-a_{n}+\big|a_{n-1}\big|+\big|a_{n-2}\big|+\cdots+\big|a_{1}\big|+\big|a_{0}\big|<0.}\\ \end{aligned} $$ 

所以  $ f(x) $ 在  $ \left(\frac{2k\pi}{n},\frac{2k\pi}{n}+\frac{\pi}{n}\right) $ 与  $ \left(\frac{2k\pi}{n}+\frac{\pi}{n},\frac{2k+2}{n}\pi\right) $ 内都至少各有一个根，即在  $ (0,2\pi) $ 内至少有 2n 个根.

例 13 设  $ f(x) $,  $ g(x) $ 在闭区间  $ [a,b] $ 上连续，并有数列  $ \{x_{n}\} \subset [a,b] $，使得  $ f(x_{n+1}) = g(x_n) $， $ n=1,2,\cdots $，证明存在一点  $ x_0 \in [a,b] $，使得  $ f(x_0) = g(x_0) $.

分析 只需证明函数  $ F(x)=f(x)-g(x) $ 在区间  $ [a,b] $ 内有零点. 由于从题设条件无法判断  $ F(x) $ 的符号，因此可考虑用反证法.

证明 如果结论不成立，则连续函数  $ F(x)=f(x)-g(x) $ 在  $ [a,b] $ 上恒不为零. 于是  $ F(x) $ 恒大于零或恒小于零. 不妨设恒有  $ F(x)>0 $，则它在  $ [a,b] $ 上的最小值 m>0. 由

 $$ f(x_{n+1})=g(x_{n})=g(x_{n})-f(x_{n})+g(x_{n-1}), $$ 

继续递推得到

 $$ f(x_{n+1})=g(x_{n})=\left[g(x_{n})-f(x_{n})\right]+\left[g(x_{n-1})-f(x_{n-1})\right]+\cdots+\left[g(x_{2})-f(x_{2})\right]+g(x_{1})\cdot $$ 

因此

 $$ \begin{align*}g(x_{1})-f(x_{n+1})=&\left[f(x_{n})-g(x_{n})\right]+\left[f(x_{n-1})-g(x_{n-1})\right]+\cdots+\left[f(x_{2})-g(x_{2})\right]\\=&F(x_{n})+F(x_{n-1})+\cdots+F(x_{2})\geqslant(n-1)m.\end{align*} $$ 

可推出  $ \lim_{n\to\infty}f(x_n)=\infty $，这与  $ f(x) $ 在  $ [a,b] $ 上有界矛盾.

评注 该题结论表明：连续函数在闭区间上的迭代运算一定有不动点.

例 14 设函数  $ f(x) \in C[a,b] $， $ g(x) $ 在  $ [a,b] $ 可积且不变号，证明至少存在一点  $ \xi \in [a,b] $，使

 $$ \int_{a}^{b}f(x)g(x)\mathrm{d}x=f(\xi)\int_{a}^{b}g(x)\mathrm{d}x. $$ 

分析 只需证明 $ \frac{\int_{a}^{b}f(x)g(x)dx}{\int_{a}^{b}g(x)dx} $介于函数 $ f(x) $的最小值与最大值之间.

证明 不妨设在 $ [a,b] $上 $ g(x)\geq0 $.

因为 $ f(x)\in C[a,b] $，由最值定理，知 $ f(x) $在 $ [a,b] $上有最大值M和最小值m，即

 $$ m\leq f(x)\leq M. $$ 

则

 $$ \begin{align*}mg(x)&\leq f(x)g(x)\leq Mg(x),\\\int_{a}^{b}mg(x)\mathrm{d}x&\leq\int_{a}^{b}f(x)g(x)\mathrm{d}x\leq\int_{a}^{b}Mg(x)\mathrm{d}x.\end{align*} $$ 

若 $ \int_{a}^{b}g(x)\mathrm{d}x>0 $，则  $ m\leqslant\frac{\int_{a}^{b}f(x)g(x)\mathrm{d}x}{\int_{a}^{b}g(x)\mathrm{d}x}\leqslant M $．由介值定理，知 $ \exists\xi\in[a,b] $，使得

 $$ \frac{\displaystyle\int_{a}^{b}f(x)g(x)\mathrm{d}x}{\displaystyle\int_{a}^{b}g(x)\mathrm{d}x}=f(\xi),\mathrm{\quad 即 }\int_{a}^{b}f(x)g(x)\mathrm{d}x=f(\xi)\int_{a}^{b}g(x)\mathrm{d}x. $$ 

若 $ \int_{a}^{b}g(x)\mathrm{d}x=0 $，由①式知 $ \int_{a}^{b}f(x)g(x)\mathrm{d}x=0 $，则对 $ \forall\xi\in[a,b] $，都有

 $$ \int_{a}^{b}f(x)g(x)\mathrm{d}x=f(\xi)\int_{a}^{b}g(x)\mathrm{d}x. $$ 

评注 该题的结论也叫积分第一中值定理（较常用）。当 $ g(x)\equiv1 $时，就是通常的积分中值定理：

 $$ \int_{a}^{b}f(x)\mathrm{d}x=f(\xi)(b-a) $$ 

例 15 设  $ a, b \in \left(0, \frac{1}{2}\right) $， $ f(x) $ 是定义在  $ \mathbb{R} $ 上的连续函数，且满足  $ f(f(x)) = af(x) + bx $。证明  $ f(x) $ 有唯一的不动点  $ x = 0 $，即  $ f(0) = 0 $。

分析 即证方程  $ f(x)=x $ 有唯一的根 x=0 。由于题设并没给出函数的大小关系，因此很难用零点定理做判断。可考虑用反证法，利用 a,b 的范围制造不等式。如果  $ f(x) $ 具有单调性，那么若其有根，则根就是唯一的。

证明 首先，f 是一一映射.

注意到 $bx$ 可以取任意值，当 $f(x)$ 的定义域为 $\mathbb{R}$ 时，其值域也为 $\mathbb{R}$。即 $f$ 是 $\mathbb{R}$ 上的满射。

另一方面，若  $ f(x) = f(y) $，则有  $ f(f(x)) = f(f(y)) $，所以  $ bx = by $，进而 x = y。即  $ f $ 是  $ \mathbb{R} $ 上的单射。所以  $ f $ 是  $ \mathbb{R} $ 上的一一映射。

下证  $ f(x) $ 有唯一的不动点.

若  $ \forall x \in \mathbb{R} $，均有  $ f(x) > x $，则

 $$ f(f(x))>f(x)\Rightarrow af(x)+bx>f(x)\Rightarrow f(x)<\frac{bx}{1-a}, $$ 

特别地，有  $ f(1)<\frac{b}{1-a}<1 $ ，则矛盾.

若  $ \forall x \in \mathbb{R} $，均有  $ f(x) < x $，则

 $$ f(f(x))<f(x)\Rightarrow af(x)+bx<f(x)\Rightarrow f(x)>\frac{bx}{1-a}, $$ 

特别地，有  $ f(-1) > -\frac{b}{1-a} > -1 $，则矛盾.

所以存在唯一的  $ x_0 \in \mathbb{R} $，使得  $ f(x_0) = x_0 $，且有

 $$ f(f(x_{0}))=a f(x_{0})+b x_{0}\Rightarrow x_{0}=a x_{0}+b x_{0}\Rightarrow x_{0}(1-a-b)=0\Rightarrow x_{0}=0 $$ 

<div style="text-align: center;"><div style="text-align: center;">习题1.3</div> </div>


<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//c12f7a62-4db7-4722-a10c-5c3025bb33a4/markdown_2/imgs/img_in_image_box_1241_1431_1374_1562.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A29Z%2F-1%2F%2Ffa818a4c762b47fdc28e625b4f0d4f375ce949ee0d33d776b440d28717c6ff27" alt="Image" width="9%" /></div>


1. 设  $ f(x)=\left\{\begin{aligned}&\frac{\ln\cos(x-1)}{1-\sin\frac{\pi}{2}x},&x\neq1,\\&1,&x=1,\end{aligned}\right. $，问函数  $ f(x) $ 在 x=1 处是否连续？若不连续，则修改函数  $ f(x) $ 在 x=1 的定义，使之连续.

2. 设  $ f(x)=\left\{\begin{aligned}&\frac{x^{3}+ax+b}{2x^{3}+3x^{2}-1},\quad x\neq-1\\ &c,\quad x=-1\end{aligned}\right. $，试确定 a,b,c 的值，使  $ f(x) $ 在 x=-1 连续.

3. 求  $ f(x)=\lim_{t\to x}\left(\frac{\sin t}{\sin x}\right)^{\frac{x}{\sin t-\sin x}} $ 的间断点并指出其类型.

4. 设  $ f(x)=\begin{cases}\dfrac{\ln(1+ax^3)}{x-\arcsin x},&x<0\\6,&x=0,\\\dfrac{e^{ax}+x^2-ax-1}{x\sin\dfrac{x}{4}},&x>0\end{cases} $，问  $ a $ 为何值时  $ f(x) $ 在  $ x=0 $ 处连续； $ a $ 为何值时， $ x=0 $ 是

 $ f(x) $ 的可去间断点？

5. 设  $ f_{n}(x)=C_{n}^{1}\cos x-C_{n}^{2}\cos^{2}x+\cdots+(-1)^{n-1}C_{n}^{n}\cos^{n}x $，证明：

（1）对任意的自然数n，方程 $ f_{n}(x_{n})=\frac{1}{2} $在区间 $ \left(0,\frac{\pi}{2}\right) $内仅有一根；

（2）设  $ x_{n} \in \left(0, \frac{\pi}{2}\right) $ 满足  $ f_{n}(x_{n}) = \frac{1}{2} $，则  $ \lim_{x \to \infty} x_{n} = \frac{\pi}{2} $.

6. 求证方程  $ x^n + x^{n-1} + \cdots + x^2 + x = 1 $ (n = 2, 3, 4, …) 在 (0,1) 内必有唯一实根  $ x_n $，并求  $ \lim_{n \to \infty} x_n $。

7. 证明方程  $ [x^3] + x^2 = [x^2] + x^3 $ 至少存在一个非整数解，其中  $ [x] $ 表示不大于  $ x $ 的最大整数。

8. 证明  $ f_{n}(x)=x^{n}+nx-2 $ （n 为正整数）在  $ (0,+\infty) $ 上有唯一正根  $ a_{n} $，并计算  $ \lim_{n\to\infty}(1+a_{n})^{n} $

 $ 9^* $. 设  $ f(x) \in C[0,1] $， $ f(0) = f(1) $，证明  $ \exists x_n, y_n \in [0,1] (x_n \neq y_n) $，使得  $ \lim_{n \to \infty} (x_n - y_n) = 0 $ 且  $ f(x_n) = f(y_n) $。

10. 设  $ f \in C(-\infty,+\infty) $，证明对一切  $ x $ 满足  $ f(2x) = f(x)e^x $ 的充分必要条件是  $ f(x) = f(0)e^x $.

11. 设  $ f(x) \in C[0,2] $，且  $ f(0) + f(1) + f(2) = 3 $。证明  $ \exists \xi \in (0,2) $，使  $ f(\xi) = 1 $。

12. 设函数  $ f(x) $ 在  $ [0,1] $ 上非负连续，且  $ f(0) = f(1) = 0 $。证明对任意实数  $ a (0 < a < 1) $，必有  $ \xi, \eta \in [0,1] $，满足  $ \eta - \xi = a $，且  $ f(\xi) = f(\eta) $。

13. 依次求解下列问题：

（1）证明方程 $ e^{x}+x^{2n+1}=0 $有唯一的实根 $ x_{n}(n=0,1,2,\cdots) $;

（2）证明  $ \lim_{n\to\infty}x_n $ 存在，并求其值 A；

（3）证明当 $ n\to\infty $时， $ x_{n}-A $与 $ \frac{1}{n} $是同阶无穷小.

14. 设  $ f(x)=\frac{\sin x}{x} $ ( $ 0 < x \leq 1 $)，证明：

（1）对任意的自然数 $ n\geqslant2 $，存在唯一的 $ x_{n}\in(0,1) $，使得 $ \int_{\frac{1}{n}}^{x_{n}}\frac{\sin x}{x}dx=\int_{x_{n}}^{1}\frac{x}{\sin x}dx $；

(2)  $ \lim_{n\to\infty}x_n $ 存在.

15*. 设函数 $f(x)$ 在 $(-\infty,+\infty)$ 上连续，且 $f[f(x)]=x$. 证明在 $(-\infty,+\infty)$ 上至少有一个 $x_0$ 满足 $f(x_0)=x_0$.

16*. 定义在 $\mathbb{R}$ 上的函数 $f$ 满足：$f$ 在 $x=0$ 连续，且对 $x,y\in\mathbb{R}$, 有 $f(x+y)=f(x)+f(y)$. 证明 $\forall x\in\mathbb{R}$, $f(x)=xf(1)$.

 $ 17^{\circ} $. 证明压缩映射原理.

（1）设  $ f(x) $ 在  $ (-\infty,+\infty) $ 上连续，存在  $ 0<\alpha<1 $ ，使得对任何 x,y 都有

 $$ \left|f(x)-f(y)\right|\leq\alpha\left|x-y\right|. $$ 

证明存在唯一的  $ x_{0} $，使得  $ x_{0}=f(x_{0}) $ （ $ x_{0} $ 称为  $ f(x) $ 的不动点）.

（2）设  $ f(x) $ 在  $ (-\infty,+\infty) $ 上可导且  $ |f'(x)| \leq \alpha $，其中常数  $ \alpha < 1 $。任取  $ x_1 \in (-\infty, +\infty) $，有

 $ x_{n+1}=f(x_{n})(n=1,2,\cdots) $. 证明  $ \lim_{n\to\infty}x_n $ 存在，并且不依赖于初始值  $ x_1 $

#### 综合题1 $ ^{*} $

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//3c85caf0-b47d-4c87-8574-2190dc5311c8/markdown_0/imgs/img_in_image_box_1220_228_1355_359.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A26Z%2F-1%2F%2Feb5dd1021abd6babd26790c14921be688d88b33bf0c4b5f2cd6da6d91232d189" alt="Image" width="9%" /></div>


1. 求  $ y=\sqrt[3]{x+\sqrt{1+x^{2}}}+\sqrt[3]{x-\sqrt{1+x^{2}}} $ 的反函数.

综合题1答案

2. 设  $ \forall x, y $ 为实数，有  $ \frac{f(x) + f(y)}{2} \leqslant f\left(\frac{x + y}{2}\right) $ 且  $ f(x) \geqslant 0 $,  $ f(0) = c $，证明  $ f(x) \equiv c $.

3. 试构造一个整系数多项式  $ ax^{2} + bx + c $，使它在  $ (0,1) $ 内有两个相异的根，同时给出 a 是满足所述条件的最小正整数，并给出证明.

4. 是否存在可微函数  $ f(x) $ 使得：

(1)  $ f(f(x))=1+x^{2}-x^{3}+x^{4}-x^{5} $; (2)  $ f(f(x))=x^{4}+2x^{3}-x-1 $.

若存在，请举例；若不存在，请说明理由。

5. 设数列  $ \left\{a_{n}\right\} $ 满足关系式  $ a_{n+1}=a_{n}+\frac{a_{n}^{2}}{n^{2}} $，其中  $ 0<a_{1}<1 $，证明  $ \left\{a_{n}\right\} $ 有界.

6. 设  $ a, b \in \left(0, \frac{1}{2}\right) $， $ f(x) $ 是定义在  $ \mathbb{R} $ 上的连续函数，且满足  $ f(f(x)) = af(x) + bx $。证明  $ f(x) $ 有唯一的不动点  $ x = 0 $，即  $ f(0) = 0 $。

7. 炮弹击中距地面高度为 h 的正在飞行的飞机. 已知炮弹在地面上发射时有初速度 V, 大炮位置及其仰角都是未知的. 证明大炮位于一圆内, 其圆心在飞机的正下方, 半径是  $ \frac{V}{g}\sqrt{V^{2}-2gh} $ （忽略大气阻力）.

8. 设 $ a_1, a_2, \cdots, a_n $为非负实数，证明  $ \left| \sum_{k=1}^{n} a_k \sin kx \right| \leqslant |\sin x| $的充分必要条件为 $ \sum_{k=1}^{n} ka_k \leqslant 1 $.

9. 证明是否存在自然数 $n$ 使得式子 $(2+\sqrt{2})^n$ 的值的小数部分大于 $0.99\cdots9$

10. 设数列  $ \{x_{n}\} $ 对一切 m 与 n 满足条件  $ 0 \leqslant x_{n+m} \leqslant x_{n} + x_{m} $. 证明数列  $ \left\{\frac{x_{n}}{n}\right\} $ 收敛.

11. 设有实函数  $ f(x) $ 且 0 < x < 1，以  $ f(x) = o(x) $ 表示当  $ x \to 0 $ 时  $ \frac{f(x)}{x} \to 0 $. 试证明以下论断：若  $ \lim_{x \to 0} f(x) = 0 $ 以及  $ f(x) - f\left(\frac{x}{2}\right) = o(x) $，则  $ f(x) = o(x) $.

12. 设  $ -1 < x_0 < 1 $， $ x_n = \sqrt{\frac{1 + x_{n-1}}{2}} (n = 1, 2, \cdots) $，求  $ \lim_{n \to \infty} 4^n (1 - \dot{x}_n) $ 及  $ \lim_{n \to \infty} (x_1 x_2 \cdots x_n) $。

13. 求极限  $ \lim_{n \to \infty} \left[ \sum_{k=1}^{n} \frac{1}{\sqrt{1^3 + 2^3 + \cdots + k^3}} + \frac{\sqrt{2}}{2} \cdot \frac{\sqrt{2 + \sqrt{2}}}{2} \cdot \cdots \cdot \frac{\sqrt{2 + \sqrt{2 + \sqrt{2 + \cdots + \sqrt{2}}}}}{2} \right] $.

14. 给定一个序列  $ \{x_{n}\}(n=1,2,\cdots) $ 且具有性质  $ \lim_{n\to\infty}(x_n-x_{n-2})=0 $，证明  $ \lim_{n\to\infty}\frac{x_n-x_{n-1}}{n}=0 $.

15. 设正项数列  $ \{a_{n}\} $ 单调递减，且  $ \lim_{n\to\infty}\sum_{k=1}^{n}a_{k}=+\infty $，证明  $ \lim_{n\to\infty}\frac{a_{2}+a_{4}+\cdots+a_{2n}}{a_{1}+a_{3}+\cdots+a_{2n-1}}=1 $

16. 设  $ f_{1}(x)=x $,  $ f_{2}(x)=x^{x} $,  $ \cdots $,  $ f_{n}(x)=x^{f_{n-1}(x)} $，求极限  $ \lim_{x\to1}\frac{f_{n}(x)-f_{n-1}(x)}{(1-x)^{n}} $.

17. 设  $ x_1=1 $,  $ x_2=\sqrt{\frac{1}{2}+1} $,  $ x_3=\sqrt{\frac{1}{3}+\sqrt{\frac{1}{2}+1}} $,  $ \cdots $,  $ x_n=\sqrt{\frac{1}{n}+\sqrt{\frac{1}{n-1}+\sqrt{\cdots+\sqrt{\frac{1}{2}+1}}} $} $, 证明  $ \lim_{n\to\infty}x_n=1 $.

18. 设数列  $ x_0 = \sqrt{7} $， $ x_1 = \sqrt{7 - \sqrt{7}} $， $ x_2 = \sqrt{7 - \sqrt{7 + \sqrt{7}}} $， $ x_3 = \sqrt{7 - \sqrt{7 + \sqrt{7 - \sqrt{7}}}} $， $ \cdots $，证明该数列收敛，并计算极限  $ \lim_{n \to \infty} x_n $ 与  $ \lim_{n \to \infty} 16^n (x_n - 2) $。

19. 设 n > 1 为正整数，令  $ S_{n} = \left( \frac{1}{n} \right)^{n} + \left( \frac{2}{n} \right)^{n} + \cdots + \left( \frac{n-1}{n} \right)^{n} $. 证明  $ \left\{ S_{n} \right\} $ 收敛，并求极限  $ \lim_{n \to \infty} S_{n} $.

20. 设数列  $ \left\{a_{n}\right\} $ 满足  $ a_{1}=\frac{\pi}{2} $， $ a_{n+1}=a_{n}-\frac{1}{n+1}\sin a_{n} $ ( $ n\geqslant1 $)，证明数列  $ \left\{na_{n}\right\} $ 收敛.

21. 一数列由递推公式  $ u_1 = b $,  $ u_{n+1} = u_n^2 + (1 - 2a)u_n + a^2 $ ( $ n=1,2,\cdots $) 确定. 当  $ a $ 与  $ b $ 满足何种关系时, 数列  $ \{u_n\} $ 收敛? 它的极限是何值?

22. 设  $ y_{n}=x_{n-1}+rx_{n} (r \geqslant 1) $，且数列  $ \left\{y_{n}\right\} $ 收敛，试讨论数列  $ \left\{x_{n}\right\} $ 的敛散性.

23. 设  $ b_n = \sum_{k=0}^{n} \frac{1}{C_n^k} (n=1,2,\cdots) $，证明：

(1)  $ b_n = \frac{n+1}{2n} b_{n-1} + 1 (n=2,3,\cdots) $; (2)  $ \lim_{n \to \infty} b_n = 2 $.

24. 设  $ a_{1}, b_{1} $ 是任意取定的实数，令

 $$ a_{n}=\int_{0}^{1}\max(b_{n-1},x)\mathrm{d}x,\ b_{n}=\int_{0}^{1}\min(a_{n-1},x)\mathrm{d}x,\ n=2,3,4,\cdots $$ 

证明数列 $ \{a_{n}\} $和 $ \{b_{n}\} $都收敛，并求 $ \lim_{n\to\infty}a_{n} $和 $ \lim_{n\to\infty}b_{n} $.

25. 设  $ F_{0}(x)=e^{x} $， $ F_{n+1}(x)=\int_{0}^{x}F_{n}(t)dt\left(n=0,1,2,\cdots\right) $，求极限  $ \lim_{n\to\infty}n!F_{n}(1) $.

26. 设级数  $ \sum_{n=1}^{\infty}a_{n} $ 收敛，  $ 0<p_{n}<p_{n+1}(n=1,2,\cdots) $.  $ \lim_{n\to\infty}p_{n}=+\infty $, 求  $ \lim_{n\to\infty}\frac{a_{1}p_{1}+a_{2}p_{2}+\cdots+a_{n}p_{n}}{p_{n}} $

27. 设数列  $ \left\{a_{n}\right\} $ 满足  $ a_{1}=1 $， $ a_{n+1}=a_{n}+\frac{1}{a_{1}+a_{2}+\cdots+a_{n}} $ ( $ n\geqslant1 $)，求  $ \lim_{n\to\infty}\frac{a_{n}}{\sqrt{\ln n}} $.

28. 设  $ f(x) = x - (ax + b\sin x)\cos x $，试确定待定常数 a, b 的值，使当  $ x \to 0 $ 时， $ f(x) $ 为 x 的尽可能高阶的无穷小.

29. 设  $ f(x) $ 在  $ (0,+\infty) $ 上二阶可导，  $ \lim_{x\to+\infty}f(x) $ 存在，当  $ 0<x<+\infty $ 时，  $ \left|f''(x)\right|\leq1 $ ，证明  $ \lim_{x\to+\infty}f'(x)=0 $

30.  $ x_{n}=\left(1+\frac{1}{n+1}\right)^{n+1}-\left(1+\frac{1}{n}\right)^{n} $ (n=1,2, $ \cdots $)，证明  $ x_{n} $ 与  $ \frac{1}{n^{2}} $ 是同阶无穷小.

31. 设  $ a_{n} = \sin\left(n\pi\sqrt[3]{n^{3}+3n^{2}+4n-5}\right) $，求极限  $ I = \lim_{n \to \infty} a_{n} $ 与  $ J = \lim_{n \to \infty} n(a_{n} - I) $.

32. 计算下列极限：

(1)  $ \lim_{n \to \infty} \frac{(2n^{1/n} - 2^{1/n})^n}{n^2} $; (2)  $ \lim_{n \to \infty} \frac{n}{\ln n} \left( \frac{\sqrt[n]{n!}}{n} - \frac{1}{e} \right) $; (3)  $ \lim_{x \to 0} \frac{(\tan x - \sin x)(\sqrt{\cos x} - 1)^2}{\tan(\sin x) - \sin(\tan x)} $.

33. 设  $ u_{n}=1+\frac{1}{2}-\frac{2}{3}+\frac{1}{4}+\frac{1}{5}-\frac{2}{6}+\cdots+\frac{1}{3n-2}+\frac{1}{3n-1}-\frac{2}{3n} $，求  $ \lim_{n\to\infty}u_n $.

34. 设  $ I_{n}=n\left(\sum_{k=1}^{n}\sqrt{k}\right)^{2}\left(\sum_{k=1}^{n}\sqrt[3]{k}\right)^{-3}+\sum_{k=1}^{n}\ln\left(1+\frac{1}{n+k}\right)\sin\ln\left(1+\frac{k}{n}\right) $，求  $ \lim_{n\to\infty}I_n $

35. 设  $ \alpha > 0 $，求极限  $ \lim_{n \to \infty} \sum_{k=1}^{n} \frac{1}{n + k^{\alpha}} $.

36. 设多项式  $ P(x) = a_m x^m + a_{m-1} x^{m-1} + \cdots + a_1 x + a_0 (a_m > 0) $，记  $ P(1) $， $ P(2) $， $ \cdots $， $ P(n) $ 的算术均值与几何均值分别为  $ A_n $ 和  $ G_n $，求极限  $ \lim_{n \to \infty} \frac{A_n}{G} $。

37. 设  $ f(x)=\arctan x $，A 为常数，若  $ B=\lim_{n\to\infty}\sum_{i=1}^{n}\left[f\left(\frac{i}{n}\right)-An\right] $ 存在，求 A, B 的值.

38. 设  $ a_{1}=1 $,  $ a_{k}=k(a_{k-1}+1) $ ( $ k=2,3,\cdots $), 求极限  $ \lim_{n\to\infty}\prod_{k=1}^{n}\left(1+\frac{1}{a_{k}}\right) $.

39. 求极限  $ \lim_{n \to \infty} \sqrt{n} \prod_{k=1}^{n} \frac{e^{1 - \frac{1}{k}}}{\left(1 + \frac{1}{k}\right)^{k}} $.

40. 设非负数列  $ \{x_{n}\} $ 满足  $ x_{n+1} \leqslant x_{n} + \frac{\ln n}{n^{\alpha}} (n=2,3,\cdots) $. 证明当  $ \alpha > 1 $ 时， $ \{x_{n}\} $ 收敛.

41. 数列  $ \left\{a_{n}\right\} $ 满足关系式  $ a_{n+1}=a_{n}+\frac{n}{a_{n}} $， $ a_{1}>0 $。证明  $ \lim_{n\to\infty}n(a_{n}-n) $ 存在.

42. 设函数  $ f(x) > 0 $，在区间  $ [0, 1] $ 上连续，证明  $ \lim_{n \to \infty} \sqrt[n]{\sum_{i=1}^{n} \left[ f\left(\frac{i}{n}\right) \right]^n} \frac{1}{n} = \max_{x \in [0,1]} f(x) $.

43. 设  $ a_n = \left( \frac{1 + \sqrt[n]{2} + \sqrt[n]{3} + \cdots + \sqrt[n]{k}}{k} \right)^n $，证明对任意正整数  $ k $，都有  $ \lim_{n \to \infty} a_n > \frac{k}{e} $。

44. 对于实数对  $ (x, y) $，定义数列  $ \{a_n\} $，其中  $ a_0 = x $， $ a_{n+1} = \frac{a_n^2 + y^2}{2} (n = 0, 1, 2, \cdots) $。设区域  $ D = \{(x, y) \mid \text{使得数列} \{a_n\} \text{收敛}\} $，求  $ D $ 的面积。

45. 空气通过盛有  $ CO_{2} $ 吸收剂的圆柱形器皿，已知它吸收  $ CO_{2} $ 的量与  $ CO_{2} $ 的百分浓度及吸收层厚度成正比。有  $ CO_{2} $ 含量为 8% 的空气，通过厚度为 10 厘米的吸收层，其  $ CO_{2} $ 含量为 2%。问：

（1）若通过的吸收层厚度为30厘米，出口处空气中 $ CO_{2} $的含量是多少？

（2）若要使出口处空气中  $ CO_{2} $ 的含量为 1%，其吸收层厚度应为多少？

46. 设有一实值连续的函数，对于所有的实数 x 和 y 满足函数方程  $ f\left(\sqrt{x^2 + y^2}\right) = f(x)f(y) $，及  $ f(1) = 2 $，证明  $ f(x) = 2^{x^2} $.

47. 设  $ \varphi $ 是  $ \mathbb{R} $ 上的严格单调递增连续函数， $ \psi $ 是  $ \varphi $ 的反函数，数列  $ \{x_n\} $ 满足

 $$ x_{n+2}=\psi\left(\left(1-\frac{1}{\sqrt{n}}\right)\varphi(x_{n})+\frac{1}{\sqrt{n}}\varphi(x_{n+1})\right)(n\geqslant2). $$ 

判断 $ \left\{x_{n}\right\} $的敛散性并说明理由.

48. 对于每一个  $ x > e^e $，归纳定义一个数列， $ u_0, u_1, u_2, \cdots $ 如下： $ u_0 = e $， $ u_{n+1} = \log_{u_n} x $ ( $ n = 0, 1, 2, \cdots $)。证明该数列收敛，记  $ g(x) = \lim_{n \to \infty} u_n $，并且当  $ x > e^e $ 时， $ g(x) $ 是连续的。

49. 设  $ f(x) $ 是连续函数，使得对所有的 x 都有  $ f(2x^2 - 1) = 2xf(x) $ 成立。证明对于  $ -1 \leq x \leq 1 $，恒有  $ f(x) = 0 $。

50. 设  $ f:[0,1]\to[0,1] $ 为连续函数， $ f(0)=0 $， $ f(1)=1 $， $ f[f(x)]=x $，证明  $ f(x)=x $。


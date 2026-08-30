# 第3章 一元函数积分学

一元函数积分学包括不定积分和定积分. 不定积分是微分的逆运算, 概念少, 计算多, 是计算定积分、重积分、曲线积分与曲面积分以及求解微分方程的基础. Newton-Leibniz 公式是微积分学的基本公式, 既揭示了定积分与被积函数的原函数或不定积分之间的联系, 也提供了一个有效而简便的定积分计算方法.

本章着重讨论不定积分法以及定积分中的有关问题，并简要介绍广义积分的计算。

### 3.1 竞赛要点与难点

(1) 原函数和不定积分的概念;

(2) 不定积分的基本性质、基本积分公式;

(3) 定积分的概念和基本性质、定积分中值定理、变上限定积分确定的函数及其导数、Newton-Leibniz 公式；

(4) 不定积分和定积分的换元积分法与分部积分法：

(5) 有理函数、三角函数的有理式和简单无理函数的积分;

(6) 广义积分 (也称反常积分);

(7) 定积分的应用: 平面图形的面积、平面曲线的弧长、旋转体的体积及侧面积、平行截面面积为已知的立体体积、功、引力、压力及函数的平均值等.

### 3.2 范例解析与精讲

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//5ed04981-0d53-447c-9e7f-0a549bb38478/markdown_1/imgs/img_in_image_box_124_927_169_969.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A20Z%2F-1%2F%2F4ba18d5bca047c67b9c852a558bb2e0413028370e9440d74323a96a8385ddfde" alt="Image" width="4%" /></div>


#### 题型一、不定积分

不定积分计算的核心，是分析被积函数的特点，通过各种手段，千方百计地将被积表达式转化为基本积分公式中的被积表达式形式。不同的转化方式就构成了不同的求不定积分的技巧和方法。

## 1. 凑微分法

凑微分法, 实质上是第一类换元积分法, 只不过是没有把换元过程和新的变量明确写出来而已. 常用的线性代换、一次根式代换以及凑幂次法等都可以统一处理成凑微分法.

理解并熟记下述公式将有助于我们在解题实践中能够灵活运用凑微分法：

(1)  $ \int f\left(\mathrm{e}^{x}\right)\mathrm{e}^{x}\mathrm{d}x=\int f\left(\mathrm{e}^{x}\right)\mathrm{d}\left(\mathrm{e}^{x}\right); $

(2)

 $$ \int f\left(a x^{n}+b\right)x^{n-1}\mathrm{d}x=\frac{1}{n a}\int f\left(a x^{n}+b\right)\mathrm{d}\left(a x^{n}+b\right); $$ 

(3)  $ \int f(\ln x)\frac{\mathrm{d}x}{x} = \int f(\ln x)\mathrm{d}(\ln x) $;

(4)  $ \int f(\arctan x)\frac{\mathrm{d}x}{1+x^{2}} = \int f(\arctan x)\mathrm{d}(\arctan x) $;

(5)  $ \int f(\tan x)\frac{\mathrm{d}x}{\cos^{2}x} = \int f(\tan x)\mathrm{d}(\tan x); $

(6)

 $$ \int f(\cos x)\sin x\mathrm{d}x=-\int f(\cos x)\mathrm{d}(\cos x); $$ 

(7)  $ \int f(\sin x)\cos x\mathrm{d}x = \int f(\sin x)\mathrm{d}(\sin x); $

(8)

 $$ \int f(\arcsin x)\frac{\mathrm{d}x}{\sqrt{1-x^{2}}}=\int f(\arcsin x)\mathrm{d}(\arcsin x). $$ 

【例 3.1】求不定积分: (I)  $ I = \int \frac{1 - \ln x}{(x - \ln x)^2} \, \mathrm{d}x $; (II)  $ I = \int \frac{1 + \sin 2x}{1 + \cos 2x} \, \mathrm{d}x $.

解 (I)  $ I = \int \frac{\frac{1 - \ln x}{x^{2}}}{\left(1 - \frac{\ln x}{x}\right)^{2}} \mathrm{d}x = -\int \frac{\mathrm{d} \left(1 - \frac{\ln x}{x}\right)}{\left(1 - \frac{\ln x}{x}\right)^{2}} = \frac{1}{1 - \frac{\ln x}{x}} + C = \frac{x}{x - \ln x} + C. $

(Ⅱ)

 $$ \begin{aligned}I&=\int\frac{1+2\sin x\cos x}{2\cos^{2}x}\mathrm{d}x=\frac{1}{2}\int\sec^{2}x\mathrm{d}x-\int\frac{1}{\cos x}\mathrm{d}(\cos x)\\&=\frac{1}{2}\tan x-\ln|\cos x|+C.\end{aligned} $$ 

【例 3.2】求不定积分: (I)  $ I = \int \frac{1 + x}{x(1 + x e^{x})} \, \mathrm{d}x $; (II)  $ I = \int \frac{\mathrm{d}x}{2 e^{-x} + e^{x} + 2} $.

解 (I)  $ I = \int \frac{(1 + x)e^{x}}{x e^{x}(1 + x e^{x})} \, \mathrm{d}x = \int \left( \frac{1}{x e^{x}} - \frac{1}{1 + x e^{x}} \right) \mathrm{d} \left( x e^{x} \right) $

 $  = \ln |x e^{x}| - \ln |1 + x e^{x}| + C = \ln \left| \frac{x e^{x}}{1 + x e^{x}} \right| + C.  $

(Ⅱ)  $ I = \int \frac{e^x}{e^{2x} + 2e^x + 2} \, dx = \int \frac{d(e^x + 1)}{1 + (e^x + 1)^2} = \arctan(e^x + 1) + C. $

【例 3.3】 求不定积分:  $ I = \int \frac{dx}{1 + x^{4}} $

解

 $$ \begin{aligned}I&=\frac{1}{2}\int\frac{\left(1+x^{2}\right)+\left(1-x^{2}\right)}{1+x^{4}}\mathrm{d}x=\frac{1}{2}\int\frac{1+x^{2}}{1+x^{4}}\mathrm{d}x-\frac{1}{2}\int\frac{x^{2}-1}{1+x^{4}}\mathrm{d}x\\&=\frac{1}{2}\int\frac{1+\frac{1}{x^{2}}}{x^{2}+\frac{1}{x^{2}}}\mathrm{d}x-\frac{1}{2}\int\frac{1-\frac{1}{x^{2}}}{x^{2}+\frac{1}{x^{2}}}\mathrm{d}x\\&=\frac{1}{2}\int\frac{\mathrm{d}\left(x-\frac{1}{x}\right)}{\left(x-\frac{1}{x}\right)^{2}+2}-\frac{1}{2}\int\frac{\mathrm{d}\left(x+\frac{1}{x}\right)}{\left(x+\frac{1}{x}\right)^{2}-2}\\&=\frac{1}{2\sqrt{2}}\arctan\frac{x-\frac{1}{x}}{\sqrt{2}}-\frac{1}{4\sqrt{2}}\ln\left|\frac{x+\frac{1}{x}-\sqrt{2}}{x+\frac{1}{x}+\sqrt{2}}\right|+C\\&=\frac{\sqrt{2}}{4}\arctan\frac{x^{2}-1}{\sqrt{2}x}+\frac{1}{4\sqrt{2}}\ln\frac{x^{2}+\sqrt{2}x+1}{x^{2}-\sqrt{2}x+1}+C.\end{aligned} $$ 

【例 3.4】（第六届全国决赛题，2015） 不定积分  $ \int\frac{1+x^{2}}{1+x^{4}}dx $ 等于 ___.

解 参见例 3.3, 应填答案:  $ \frac{1}{\sqrt{2}}\arctan\frac{x^{2}-1}{\sqrt{2}x}+C $.

2. 换元积分法

换元积分的一般方法： $ \int f(x)\mathrm{d}x\xlongequal{x=\varphi(t)}\int f[\varphi(t)]\varphi'(t)\mathrm{d}t=F\left[\varphi^{-1}(x)\right]+C $，其中 $ F(t) $是 $ f[\varphi(t)]\varphi'(t) $的一个原函数， $ \varphi^{-1}(x)=t $是 $ x=\varphi(t) $的反函数.

【例 3.5】（第十一届全国初赛题，2019）设隐函数  $ y = y(x) $ 由方程  $ y^{2}(x - y) = x^{2} $ 所确定，则  $ \int \frac{\mathrm{d}x}{y^{2}} =  $ ___.

解 令 y = tx，与方程  $ y^{2}(x - y) = x^{2} $ 联立，解得  $ x = \frac{1}{t^{2}(1 - t)} $， $ y = \frac{1}{t(1 - t)} $，则  $ \mathrm{d}x = \frac{-2 + 3t}{t^{3}(1 - t)^{2}}\mathrm{d}t $。所以

 $$ \begin{align*}\int\frac{\mathrm{d}x}{y^{2}}&=\int\frac{1}{\frac{1}{t^{2}(1-t)^{2}}}\frac{-2+3t}{t^{3}(1-t)^{2}}\mathrm{d}t=\int\frac{-2+3t}{t}\mathrm{d}t\\&=3t-2\ln|t|+C=\frac{3y}{x}-2\ln\left|\frac{y}{x}\right|+C.\end{align*} $$ 

这一部分重点是几种典型代换：三角代换、根式代换、倒置代换以及二项代换。

1) 三角代换

对于含二次根式的积分，被积函数中含  $ \sqrt{a^{2}-x^{2}} $ 时，可设  $ x=a\sin t $; 含  $ \sqrt{x^{2}+a^{2}} $

时，可设  $ x = a \tan t $; 含  $ \sqrt{x^{2} - a^{2}} $ 时，可设  $ x = a \sec t $; 含  $ \sqrt{ax^{2} + bx + c} $ 时，可经配方化为上述三种情形.

对于积分  $ \int f(\sin x, \cos x) \, dx $，其中  $ f(u, v) $ 是有理函数，利用代换  $ t = \tan \frac{x}{2} $ 可化为有理函数的积分，常称之为万能代换.

【例 3.6】求：(I)  $ I=\int\frac{\mathrm{d}x}{\sqrt{(5+x^{2})^{3}}}; $ (Ⅱ)  $ I=\int\frac{x}{\sqrt{3+2x-x^{2}}}\mathrm{d}x. $

解 (I) 可设  $ x = \sqrt{5}\tan t, t \in \left(-\frac{\pi}{2}, \frac{\pi}{2}\right) $，则  $ \mathrm{d}x = \sqrt{5}\sec^{2}t\mathrm{d}t $，

 $$ I=\int\frac{\sqrt{5}\sec^{2}t}{\sqrt{125}\sec^{3}t}\mathrm{d}t=\frac{1}{5}\int\cos t\mathrm{d}t=\frac{\sin t}{5}+C=\frac{x}{5\sqrt{5+x^{2}}}+C. $$ 

（Ⅱ）因  $ 3 + 2x - x^{2} = 4 - (x - 1)^{2} $，故可设 x - 1 = 2sin t,  $ t \in \left(-\frac{\pi}{2}, \frac{\pi}{2}\right) $，则 x = 1 + 2sin t,  $ dx = 2\cos tdt $。从而

 $$ I=\int(1+2\sin t)\mathrm{d}t=t-2\cos t+C=\arcsin\frac{x-1}{2}-\sqrt{3+2x-x^{2}}+C. $$ 

【例 3.7】(I) 求  $ I=\int\frac{\mathrm{d}x}{\sqrt{(x-a)(b-x)}}(a\neq b) $; (II) 求  $ I=\int\frac{\sin^{2}x}{(\sin x-\cos x-1)^{3}}\mathrm{d}x $.

解 (I) 不妨设 a < b (当 a > b 时可同理求解). 因为

 $$ (x-a)(b-x)=(a+b)x-x^{2}-ab=\left(\frac{a-b}{2}\right)^{2}-\left(x-\frac{a+b}{2}\right)^{2}, $$ 

所以可设  $ x - \frac{a + b}{2} = \frac{b - a}{2} \sin t, t \in \left(-\frac{\pi}{2}, \frac{\pi}{2}\right) $，则  $ \mathrm{d}x = \frac{b - a}{2} \cos t \, \mathrm{d}t $。于是

 $$ \begin{aligned}I&=\int\frac{1}{\sqrt{\left(\frac{a-b}{2}\right)^{2}-\left(\frac{a-b}{2}\sin t\right)^{2}}}\cdot\frac{b-a}{2}\cos t\mathrm{d}t=\int\mathrm{d}t=t+C\\&=\arcsin\frac{x-\frac{a+b}{2}}{\frac{b-a}{2}}+C=\arcsin\frac{2x-a-b}{b-a}+C.\end{aligned} $$ 

（Ⅱ）令  $ t = \tan \frac{x}{2} $，则  $ \sin x = \frac{2t}{1 + t^{2}} $， $ \cos x = \frac{1 - t^{2}}{1 + t^{2}} $， $ dx = \frac{2dt}{1 + t^{2}} $。故

 $$ \begin{aligned}I&=\int\frac{t^{2}}{(t-1)^{3}}\mathrm{d}t=\int\left[\frac{1}{t-1}+\frac{2}{(t-1)^{2}}+\frac{1}{(t-1)^{3}}\right]\mathrm{d}t\\&=\ln|t-1|-\frac{2}{t-1}-\frac{1}{2(t-1)^{2}}+C\end{aligned} $$ 

 $$ =\ln\left|\tan\frac{x}{2}-1\right|-\frac{2}{\tan\frac{x}{2}-1}-\frac{1}{2\left(\tan\frac{x}{2}-1\right)^{2}}+C. $$ 

### 2）根式代换

这种代换一般用于计算某些简单无理函数的积分，其目的在于将被积表达式“有理化”.

(1) 对于含两个一次平方根式  $ \sqrt{x + \alpha} $ 与  $ \sqrt{x + \beta} (\alpha < \beta) $ 的积分，可设

 $$ \sqrt{x+\beta}=\lambda\left(t+\frac{1}{t}\right),\quad\sqrt{x+\alpha}=\lambda\left(t-\frac{1}{t}\right). $$ 

以上两式各自平方后相减，即可求出  $ \lambda $，即  $ 4\lambda^{2} = \beta - \alpha $。

【例 3.8】求  $ I=\int\frac{\mathrm{d}x}{1+\sqrt{x}+\sqrt{1+x}} $

解 设  $ \sqrt{1+x}=\lambda\left(t+\frac{1}{t}\right) $,  $ \sqrt{x}=\lambda\left(t-\frac{1}{t}\right) $，可求出  $ \lambda=\frac{1}{2} $，则  $ t=\sqrt{x}+\sqrt{x+1} $.

 $$ \begin{align*}I&=\frac{1}{2}\int\frac{t^{4}-1}{t^{3}(t+1)}\mathrm{d}t=\frac{1}{2}\left(t-\ln|t|-\frac{1}{t}+\frac{1}{2t^{2}}\right)+C\\&=\frac{x}{2}+\sqrt{x}-\frac{1}{2}\sqrt{x(x+1)}-\frac{1}{2}\ln(\sqrt{x}+\sqrt{x+1})+C.\end{align*} $$ 

(2) 对于含两个一次根式  $ \sqrt[n]{x+a} $ 和  $ \sqrt[m]{x+a} $ 的积分，可取  $ t = \sqrt[k]{x+a} $，这里 k 为 m, n 的最小公倍数，即  $ \frac{1}{m}, \frac{1}{n} $ 的公分母.

【例 3.9】求  $ I=\int\frac{\mathrm{d}x}{\sqrt{1+x}+\sqrt[3]{1+x}} $

解  $ \frac{1}{2} $ 和  $ \frac{1}{3} $ 的公分母为 6，故可设  $ t=\sqrt[6]{1+x} $，则  $ \sqrt{1+x}=t^{3} $， $ \sqrt[3]{1+x}=t^{2} $， $ \mathrm{d}x=6t^{5}\mathrm{d}t $。故

 $$ \begin{aligned}I&=\int\frac{6t^{5}\mathrm{d}t}{t^{3}+t^{2}}=2t^{3}-3t^{2}+6t-6\ln(1+t)+C\\&=2\sqrt{1+x}-3\sqrt[3]{1+x}+6\sqrt[6]{1+x}-6\ln(1+\sqrt[6]{1+x})+C.\end{aligned} $$ 

(3) 对于含有根式  $ \sqrt[m]{\frac{x+a}{x-a}} $ 的积分，可设  $ t = \sqrt[m]{\frac{x+a}{x-a}} $.

【例 3.10】求  $ I=\int\frac{\mathrm{d}x}{\sqrt[3]{(x+1)^2(x-1)^4}} $

解 设  $ t = \sqrt[3]{\frac{x+1}{x-1}} $，则  $ x = 1 + \frac{2}{t^{3} - 1} $，从而

 $$ I=-\frac{3}{2}\int\mathrm{d}t=-\frac{3}{2}t+C=-\frac{3}{2}\sqrt[3]{\frac{x+1}{x-1}}+C. $$ 

3) 倒置代换  $ t = \frac{1}{x + a} $

当被积函数为 x 的有理式或无理式时，往往可利用倒置代换消去分母中所含的因子 x + a 或 x + a 的幂.

【例 3.11】求不定积分: (I)  $ \int \frac{dx}{x^4 (x^2 + 1)}; $ (II)  $ \int \frac{dx}{(1 + x)\sqrt{1 - x^2}}. $

解 (I) 令  $ t = \frac{1}{x} $，则

 $$ \begin{aligned}I&=-\int\frac{t^{4}}{t^{2}+1}\mathrm{d}t=-\int\left(t^{2}-1+\frac{1}{t^{2}+1}\right)\mathrm{d}t\\&=-\left(\frac{t^{3}}{3}-t+\arctan t\right)+C=-\frac{1}{3x^{3}}+\frac{1}{x}-\arctan\frac{1}{x}+C.\end{aligned} $$ 

(Ⅱ) 令  $ t = \frac{1}{x + 1} $，则

 $$ I=-\int\frac{\mathrm{d}t}{\sqrt{2t-1}}=-\sqrt{2t-1}+C=-\sqrt{\frac{1-x}{1+x}}+C. $$ 

4) 二项代换  $ t = x \pm \frac{1}{x} $

【例 3.12】求不定积分: (I)  $ \int \frac{x^{8}(x^{2}+1)}{(x^{2}-1)^{10}}dx $; (II)  $ \int \frac{x^{2}-1}{x^{4}+3x^{2}+1}dx $.

解 (I) 令  $ t = x - \frac{1}{x} $，则  $ \mathrm{d}t = \left(1 + \frac{1}{x^{2}}\right)\mathrm{d}x $，

 $$ I=\int\frac{\mathrm{d}t}{t^{10}}=-\frac{1}{9t^{9}}+C=-\frac{x^{9}}{9\left(x^{2}-1\right)^{9}}+C. $$ 

（Ⅱ）令  $ t = x + \frac{1}{x} $，则  $ \mathrm{d}t = \left(1 - \frac{1}{x^{2}}\right)\mathrm{d}x $，

 $$ I=\int\frac{\mathrm{d}t}{t^{2}+1}=\arctan t+C=\arctan\left(x+\frac{1}{x}\right)+C. $$ 

3. 分部积分法

设  $ u(x), v(x) $ 具有连续导数，则有分部积分公式

 $$ \int u(x)v^{\prime}(x)\mathrm{d}x=u(x)v(x)-\int u^{\prime}(x)v(x)\mathrm{d}x, $$ 

或简记为  $ \int u\,dv = uv - \int v\,du $.

利用分部积分公式, 可以把求不定积分  $ \int u dv $ 转化为求另一个不定积分  $ \int v du $. 一般而言, 后者较前者容易积分.

【例 3.13】 求不定积分  $ I = \int \frac{x^{2}(x \sec^{2}x + \tan x)}{(x \tan x + 1)^{2}} \mathrm{d}x. $

解 注意到  $ \frac{\mathrm{d}}{\mathrm{d}x}(x\tan x+1)=x\sec^{2}x+\tan x $，以及  $ \frac{\mathrm{d}}{\mathrm{d}x}(x\sin x+\cos x)=x\cos x $，所以

 $$ \begin{aligned}I&=\int x^{2}\mathrm{d}\left(-\frac{1}{x\tan x+1}\right)=-\frac{x^{2}}{x\tan x+1}+\int\frac{2x}{x\tan x+1}\mathrm{d}x\\&=-\frac{x^{2}}{x\tan x+1}+2\int\frac{x\cos x}{x\sin x+\cos x}\mathrm{d}x\\&=-\frac{x^{2}}{x\tan x+1}+2\ln\left|x\sin x+\cos x\right|+C.\end{aligned} $$ 

【例 3.14】求不定积分  $ I = \int \arcsin x \arccos x \, dx $.

解

 $$ \begin{aligned}I&=x\arcsin x\arccos x-\int\frac{x(\arccos x-\arcsin x)}{\sqrt{1-x^{2}}}\mathrm{d}x\\&=x\arcsin x\arccos x+\int(\arccos x-\arcsin x)\mathrm{d}\left(\sqrt{1-x^{2}}\right)\\&=x\arcsin x\arccos x+(\arccos x-\arcsin x)\sqrt{1-x^{2}}+2\int\mathrm{d}x\\&=x\arcsin x\arccos x+(\arccos x-\arcsin x)\sqrt{1-x^{2}}+2x+C.\\ \end{aligned} $$ 

【例 3.15】(第四届全国决赛题, 2013) 计算不定积分  $ I = \int x \arctan x \ln \left(1 + x^{2}\right) \, dx $.

解

 $$ \begin{aligned}I&=\frac{1}{2}\int\arctan x\ln\left(1+x^{2}\right)\mathrm{d}\left(1+x^{2}\right)\\&=\frac{1}{2}\left(1+x^{2}\right)\arctan x\ln\left(1+x^{2}\right)-\frac{1}{2}\int\left(1+x^{2}\right)\mathrm{d}\left[\arctan x\ln\left(1+x^{2}\right)\right]\\&=\frac{1}{2}\left(1+x^{2}\right)\arctan x\ln\left(1+x^{2}\right)-\frac{1}{2}\int\ln\left(1+x^{2}\right)\mathrm{d}x-\int x\arctan x\mathrm{d}x.\\ \end{aligned} $$ 

进一步，有

 $$ \begin{align*}\int\ln\left(1+x^{2}\right)\mathrm{d}x&=x\ln\left(1+x^{2}\right)-2\int\frac{x^{2}}{1+x^{2}}\mathrm{d}x=x\ln\left(1+x^{2}\right)-2x+2\arctan x+C_{1},\\\int x\arctan x\mathrm{d}x&=\frac{1}{2}\int\arctan x\mathrm{d}\left(1+x^{2}\right)=\frac{1}{2}\left(1+x^{2}\right)\arctan x-\frac{x}{2}+C_{2}.\end{align*} $$ 

将上述两式代入 $ ^{①} $式并整理，得

 $$ I=\frac{1}{2}\left(1+x^{2}\right)\arctan x\ln\left(1+x^{2}\right)-\frac{1}{2}\left(3+x^{2}\right)\arctan x-\frac{1}{2}x\ln\left(1+x^{2}\right)+\frac{3x}{2}+C, $$ 

其中  $ C = -\frac{C_{1}}{2} - C_{2} $

【例 3.16】 求不定积分  $ I = \int \frac{x^{2} \mathrm{d}x}{(x \sin x + \cos x)^{2}} $

【分析】被积函数是一个结构比较复杂的分式，根据其分母的特征，容易联想到微分运算公式： $ \mathrm{d}\left(\frac{1}{f(x)}\right)=-\frac{f'(x)}{f^{2}(x)}\mathrm{d}x $。这里 $ f(x)=x\sin x+\cos x $， $ f'(x)=x\cos x $。由此得到启发，先将被积函数的分子与分母同时乘以 $ \cos x $，并且令 $ u(x)=\frac{x}{\cos x} $， $ v'(x)=\frac{x\cos x}{(x\sin x+\cos x)^{2}} $，再利用分部积分公式即可使问题简化。

解

 $$ \begin{aligned}I&=\int\frac{x^{2}\mathrm{d}x}{(x\sin x+\cos x)^{2}}=\int\frac{x}{\cos x}\cdot\frac{x\cos x}{(x\sin x+\cos x)^{2}}\mathrm{d}x\\&=-\frac{x}{\cos x}\cdot\frac{1}{x\sin x+\cos x}+\int\frac{1}{x\sin x+\cos x}\left(\frac{x}{\cos x}\right)^{\prime}\mathrm{d}x\\&=-\frac{x}{\cos x(x\sin x+\cos x)}+\int\frac{1}{\cos^{2}x}\mathrm{d}x\\&=-\frac{x}{\cos x(x\sin x+\cos x)}+\tan x+C=\frac{\sin x-x\cos x}{x\sin x+\cos x}+C.\end{aligned} $$ 

在使用分部积分法时，以下几种技巧也是需要掌握的。

### 1）回归法

通过若干次分部积分后, 又得到了原来的积分, 经过简单的代数运算即可求得问题的解. 有的文献称这种方法为 “循环法”.

【例 3.17】求  $ I=\int\frac{x\mathrm{e}^{\arctan x}}{\sqrt{(1+x^{2})^{3}}}\mathrm{d}x. $

解

 $$ \begin{aligned}I&=\int\frac{x}{\sqrt{1+x^{2}}}\mathrm{d}\left(\mathrm{e}^{\arctan x}\right)=\frac{x}{\sqrt{1+x^{2}}}\mathrm{e}^{\arctan x}-\int\mathrm{e}^{\arctan x}\frac{\mathrm{d}x}{\sqrt{\left(1+x^{2}\right)^{3}}}\\&=\frac{x}{\sqrt{1+x^{2}}}\mathrm{e}^{\arctan x}-\int\frac{1}{\sqrt{1+x^{2}}}\mathrm{d}\left(\mathrm{e}^{\arctan x}\right)\\&=\frac{x-1}{\sqrt{1+x^{2}}}\mathrm{e}^{\arctan x}-\int\frac{x\mathrm{e}^{\arctan x}}{\sqrt{\left(1+x^{2}\right)^{3}}}\mathrm{d}x,\end{aligned} $$ 

故  $ I = \frac{1}{2} \frac{x - 1}{\sqrt{1 + x^2}} e^{\arctan x} + C. $

2）拆项法

有些积分，可以通过拆项变为几个积分。其作用有两个方面：

(1) 虽然每一项都不是初等函数, 但是通过非初等部分的相互抵消, 而最后却能求出积分 (例 3.18);

(2) 可能出现“回归”现象 (例 3.19).

【例 3.18】（第三届全国决赛题，2012）求  $ I=\int\left(1+x-\frac{1}{x}\right)\mathrm{e}^{x+\frac{1}{x}}\mathrm{d}x. $

解  $ I=\int\mathrm{e}^{x+\frac{1}{x}}\mathrm{d}x+\int\left(x-\frac{1}{x}\right)\mathrm{e}^{x+\frac{1}{x}}\mathrm{d}x\triangleq I_{1}+I_{2} $，其中  $ I_{1}=\int\mathrm{e}^{x+\frac{1}{x}}\mathrm{d}x $，而

 $$ \begin{align*}I_{2}&=\int x\left(1-\frac{1}{x^{2}}\right)\mathrm{e}^{x+\frac{1}{x}}\mathrm{d}x=\int x\mathrm{e}^{x+\frac{1}{x}}\mathrm{d}\left(x+\frac{1}{x}\right)=\int x\mathrm{d}\left(\mathrm{e}^{x+\frac{1}{x}}\right)\\&=x\mathrm{e}^{x+\frac{1}{x}}-\int\mathrm{e}^{x+\frac{1}{x}}\mathrm{d}x=x\mathrm{e}^{x+\frac{1}{x}}-I_{1},\end{align*} $$ 

故  $ I = I_{1} + I_{2} = x e^{x + \frac{1}{x}} + C $

【例 3.19】求  $ I = \int \sec^3 x \, dx $.

解

 $$ \begin{aligned}I&=\sec x\tan x-\int\sec x\tan^{2}x\mathrm{d}x=\sec x\tan x-\int\sec x\left(\sec^{2}x-1\right)\mathrm{d}x\\&=\sec x\tan x-\int\sec^{3}x\mathrm{d}x+\int\sec x\mathrm{d}x\\&=\frac{1}{2}\sec x\tan x+\frac{1}{2}\ln|\sec x+\tan x|+C.\\ \end{aligned} $$ 

【例 3.20】 求  $ I=\int\frac{x^{2}+6}{(x\cos x-3\sin x)^{2}}\mathrm{d}x. $

解

 $$ \begin{aligned}I&=\int\frac{(x^{2}+6)\left(\cos^{2}x+\sin^{2}x\right)}{(x\cos x-3\sin x)^{2}}\mathrm{d}x\\&=\int\left|\begin{array}{cc}x&3\\ -2&x\end{array}\right|\left|\begin{array}{cc}\cos x&\sin x\\ -\sin x&\cos x\end{array}\right|\frac{\mathrm{d}x}{(x\cos x-3\sin x)^{2}}\\&=\int\left|\begin{array}{cc}x\cos x-3\sin x&x\sin x+3\cos x\\ -2\cos x-x\sin x&x\cos x-2\sin x\end{array}\right|\frac{\mathrm{d}x}{(x\cos x-3\sin x)^{2}}\\&=\int\frac{x\cos x-2\sin x}{x\cos x-3\sin x}\mathrm{d}x+\int\frac{(x\sin x+3\cos x)(2\cos x+x\sin x)}{(x\cos x-3\sin x)^{2}}\mathrm{d}x.\end{aligned} $$ 

由于  $ \frac{\mathrm{d}}{\mathrm{d}x}(x\cos x-3\sin x)=-(2\cos x+x\sin x) $，故可对上述第二个积分利用分部积分，得

 $$ \begin{aligned}I_{1}&=\int\frac{(x\sin x+3\cos x)(2\cos x+x\sin x)}{(x\cos x-3\sin x)^{2}}\mathrm{d}x\\&=\int(x\sin x+3\cos x)\mathrm{d}\left(\frac{1}{x\cos x-3\sin x}\right)\\&=\frac{x\sin x+3\cos x}{x\cos x-3\sin x}-\int\frac{\mathrm{d}(x\sin x+3\cos x)}{x\cos x-3\sin x}\\&=\frac{x\sin x+3\cos x}{x\cos x-3\sin x}-\int\frac{x\cos x-2\sin x}{x\cos x-3\sin x}\mathrm{d}x.\end{aligned} $$ 

 $$ I=\int\frac{x\cos x-2\sin x}{x\cos x-3\sin x}\mathrm{d}x+I_{1}=\frac{x\sin x+3\cos x}{x\cos x-3\sin x}+C. $$ 

【注】这里，利用行列式来表述较为复杂的计算式子，具有过程简捷、结构紧凑、规律性强等明显优点.

##### 3）递推法

这种方法多用于被积函数含有自然数 n 的情形.

【例 3.21】求  $ I_{n}=\int\sin^{n}x\mathrm{d}x $ 的递推公式，并利用所得结果求  $ \int\sin^{4}x\mathrm{d}x $.

解

 $$ \begin{align*}I_{n}&=\int\sin^{n-2}x\left(1-\cos^{2}x\right)\mathrm{d}x=\int\sin^{n-2}x\mathrm{d}x-\int\sin^{n-2}x\cos^{2}x\mathrm{d}x\\&=I_{n-2}-\int\cos x\sin^{n-2}x\mathrm{d}(\sin x)=I_{n-2}-\frac{1}{n-1}\cos x\sin^{n-1}x-\frac{I_{n}}{n-1},\end{align*} $$ 

故  $ I_{n}=\frac{n-1}{n}I_{n-2}-\frac{1}{n}\cos x\sin^{n-1}x(n\neq0,1). $

由于  $ I_{0}=\int dx=x+C $ ，故由上述结果得

 $$ I_{2}=\frac{1}{2}I_{0}-\frac{1}{2}\cos x\sin x=\frac{x}{2}-\frac{1}{4}\sin2x+\frac{C}{2}, $$ 

 $$ \begin{aligned}I_{4}&=\int\sin^{4}x\mathrm{d}x=\frac{3}{4}I_{2}-\frac{1}{4}\cos x\sin^{3}x\\&=\frac{3}{4}\left(\frac{x}{2}-\frac{1}{4}\sin2x+\frac{C}{2}\right)-\frac{1}{8}\sin2x\sin^{2}x\\&=\frac{3}{8}x-\frac{1}{4}\sin2x+\frac{1}{32}\sin4x+C_{1}\quad\left( 其中 \quad C_{1}=\frac{3}{8}C\right).\end{aligned} $$ 

【例 3.22】求  $ I_{n}=\int\frac{\mathrm{d}x}{x^{n}\sqrt{1+x^{2}}} $ 的递推公式，并利用所得结果求  $ \int\frac{\mathrm{d}x}{x^{3}\sqrt{1+x^{2}}} $

解

 $$ \begin{aligned}I_{n}&=\frac{1}{2}\int\frac{\mathrm{d}\left(x^{2}+1\right)}{x^{n+1}\sqrt{1+x^{2}}}=\int\frac{\mathrm{d}\left(\sqrt{x^{2}+1}\right)}{x^{n+1}}\\&=\frac{\sqrt{x^{2}+1}}{x^{n+1}}-\int\sqrt{x^{2}+1}\mathrm{d}\left(\frac{1}{x^{n+1}}\right)\\&=\frac{\sqrt{x^{2}+1}}{x^{n+1}}+(n+1)\int\frac{\sqrt{x^{2}+1}}{x^{n+2}}\mathrm{d}x\\&=\frac{\sqrt{x^{2}+1}}{x^{n+1}}+(n+1)\int\frac{x^{2}+1}{x^{n+2}\sqrt{x^{2}+1}}\mathrm{d}x\\&=\frac{\sqrt{x^{2}+1}}{x^{n+1}}+(n+1)I_{n}+(n+1)I_{n+2},\\ \end{aligned} $$ 

故  $ I_{n+2}=-\frac{n}{n+1}I_{n}-\frac{\sqrt{x^{2}+1}}{(n+1)x^{n+1}}. $

利用三角代换  $ x = \tan t, t \in \left(-\frac{\pi}{2}, \frac{\pi}{2}\right) $ 容易求得

 $$ I_{1}=\int\frac{\mathrm{d}x}{x\sqrt{1+x^{2}}}=\int\frac{\sec^{2}t\mathrm{d}t}{\tan t\sec t}=\int\csc t\mathrm{d}t=\ln|\csc t-\cot t|+C $$ 

 $$ =\ln\frac{\sqrt{1+x^{2}}-1}{\left|x\right|}+C. $$ 

从而可由上述递推公式得

 $$ \begin{aligned}I_{3}&=\int\frac{\mathrm{d}x}{x^{3}\sqrt{1+x^{2}}}=-\frac{1}{2}I_{1}-\frac{\sqrt{1+x^{2}}}{2x^{2}}=-\frac{1}{2}\left(\ln\frac{\sqrt{1+x^{2}}-1}{|x|}+C\right)-\frac{\sqrt{1+x^{2}}}{2x^{2}}\\&=\frac{1}{2}\ln\frac{\sqrt{1+x^{2}}+1}{|x|}-\frac{\sqrt{1+x^{2}}}{2x^{2}}+C_{1}\quad\left( 其中 C_{1}=-\frac{1}{2}C\right).\end{aligned} $$ 

## 4. 部分分式法

这种方法适用于求解被积函数是有理分式函数的不定积分。有理分式分为有理真分式和有理假分式。对于有理假分式，可先将其化为有理整式和有理真分式之和。所谓部分分式法，是首先用待定系数法或者赋特殊值的方法把有理真分式分解成最简真分式的代数和，即分解成部分分式之和，然后采用直接积分或者凑微分等方法求出各个部分分式的不定积分。

在将有理真分式

 $$ \frac{P(x)}{Q(x)}=\frac{a_{0}x^{n}+a_{1}x^{n-1}+\cdots+a_{n-1}x+a_{n}}{b_{0}x^{m}+b_{1}x^{m-1}+\cdots+b_{m-1}x+b_{m}}\quad( 其中 a_{0}\neq0,b_{0}\neq0,n<m) $$ 

分解成部分分式之和的时候，应注意下列两点.

(1) 如果分母 Q(x) 中有因式  $ (x - a)^{k} $，那么分解后有下列 k 个部分分式之和：

 $$ \frac{A_{1}}{x-a}+\frac{A_{2}}{(x-a)^{2}}+\cdots+\frac{A_{k-1}}{(x-a)^{k-1}}+\frac{A_{k}}{(x-a)^{k}}, $$ 

其中  $ A_{1}, A_{2}, \cdots, A_{k} $ 都是常数. 特别地, 如果 k = 1, 那么分解后有  $ \frac{A}{x - a} $.

(2) 如果分母 Q(x) 中有因式  $ (x^{2} + px + q)^{k} $，且其中  $ p^{2} - 4q < 0 $，那么分解后有下列 k 个部分分式之和：

 $$ \frac{M_{1}x+N_{1}}{x^{2}+px+q}+\frac{M_{2}x+N_{2}}{\left(x^{2}+px+q\right)^{2}}+\cdots+\frac{M_{k}x+N_{k}}{\left(x^{2}+px+q\right)^{k}}, $$ 

其中  $ M_{i}, N_{i} (i = 1, 2, \cdots, k) $ 都是常数. 特别地, 如果 k = 1, 那么分解后有  $ \frac{Mx + N}{x^{2} + px + q} $.

【例 3.23】求不定积分: (I)  $ I = \int \frac{x^{2} + 1}{x(x - 1)^{2}} \, dx $; (II)  $ I = \int \frac{2x^{2} + 2x + 13}{(x - 2)(x^{2} + 1)^{2}} \, dx $.

解 (I) 将被积函数分解成部分分式之和:

 $$ \frac{x^{2}+1}{x(x-1)^{2}}=\frac{a}{x}+\frac{b}{(x-1)^{2}}+\frac{c}{x-1}, $$ 

即有

 $$ x^{2}+1=a(x-1)^{2}+bx+cx(x-1)=(a+c)x^{2}+(-2a+b-c)x+a. $$ 

用待定系数法确定系数 a, b, c. 比较同次幂的系数，得

 $$ a+c=1,\quad-2a+b-c=0,\quad a=1. $$ 

解得 a=1, b=2, c=0. 于是

 $$ I=\int\frac{x^{2}+1}{x(x-1)^{2}}\mathrm{d}x=\int\left(\frac{1}{x}+\frac{2}{(x-1)^{2}}\right)\mathrm{d}x=\ln|x|-\frac{2}{x-1}+C. $$ 

(Ⅱ) 将被积函数分解成部分分式之和:

 $$ \frac{2x^{2}+2x+13}{\left(x-2\right)\left(x^{2}+1\right)^{2}}=\frac{a}{x-2}+\frac{bx+c}{x^{2}+1}+\frac{dx+e}{\left(x^{2}+1\right)^{2}}, $$ 

即

 $$ 2x^{2}+2x+13=a\left(x^{2}+1\right)^{2}+(bx+c)(x-2)\left(x^{2}+1\right)+(dx+e)(x-2). $$ 

采用赋特殊值的方法确定系数 a, b, c, d, e.

令 x=2 ，得 25=25a ，故 a=1 。

令 x=i，得  $ 11+2i=(di+e)(i-2)=-d-2e+(e-2d)i $，即

 $$ \left\{\begin{array}{l}-d-2e=11,\\ e-2d=2,\end{array}\right. $$ 

故d=-3,e=-4.

令 x=0 ，得 13=a-2c-2e ，即 13=9-2c ，故 c=-2

令 x=1 ，得 17=4a-2(b+c)-(d+e)，即 2=-2b，故 b=-1。

 $$ \begin{aligned}I&=\int\left[\frac{1}{x-2}+\frac{-x-2}{x^{2}+1}+\frac{-3x-4}{\left(x^{2}+1\right)^{2}}\right]\mathrm{d}x=\int\frac{\mathrm{d}x}{x-2}-\int\frac{x+2}{x^{2}+1}\mathrm{d}x-\int\frac{3x+4}{\left(x^{2}+1\right)^{2}}\mathrm{d}x\\&=\ln|x-2|-\int\frac{x}{x^{2}+1}\mathrm{d}x-2\int\frac{\mathrm{d}x}{x^{2}+1}-3\int\frac{x}{\left(x^{2}+1\right)^{2}}\mathrm{d}x-4\int\frac{\mathrm{d}x}{\left(x^{2}+1\right)^{2}}\\&=\ln|x-2|-\frac{1}{2}\ln\left(x^{2}+1\right)-2\arctan x+\frac{3}{2\left(x^{2}+1\right)}-\frac{2x}{x^{2}+1}-2\arctan x+C\\&=\ln|x-2|-\frac{1}{2}\ln\left(x^{2}+1\right)-\frac{4x-3}{2\left(x^{2}+1\right)}-4\arctan x+C.\\ \end{aligned} $$ 

对于被积函数是三角函数有理式的不定积分, 若采用万能代换  $ t = \tan \frac{x}{2} $, 则往往导致求有理分式函数的积分.

【例 3.24】求  $ I=\int\frac{\sin x}{\sin x-2\cos x+2}dx $.

解 令  $ t = \tan \frac{x}{2} $，则  $ \sin x = \frac{2t}{1 + t^{2}} $， $ \cos x = \frac{1 - t^{2}}{1 + t^{2}} $， $ dx = \frac{2}{1 + t^{2}}dt $。从而

 $$ I=\int\frac{\frac{2t}{1+t^{2}}}{\frac{2t}{1+t^{2}}-2\cdot\frac{1-t^{2}}{1+t^{2}}+2}\cdot\frac{2}{1+t^{2}}\mathrm{d}t=\int\frac{2}{\left(1+2t\right)\left(1+t^{2}\right)}\mathrm{d}t. $$ 

将被积函数分解成部分分式之和： $ \frac{2}{(1+2t)(1+t^{2})}=\frac{a}{1+2t}+\frac{bt+c}{1+t^{2}} $，即有

 $$ 2=a\left(1+t^{2}\right)+(bt+c)(1+2t)=(a+2b)t^{2}+(b+2c)t+(a+c). $$ 

比较系数，得  $ a+c=2, b+2c=0, a+2b=0 $，解得  $ a=\frac{8}{5}, b=-\frac{4}{5}, c=\frac{2}{5} $。于是

 $$ \begin{aligned}I&=\frac{8}{5}\int\frac{1}{1+2t}\mathrm{d}t-\frac{4}{5}\int\frac{t}{1+t^{2}}\mathrm{d}t+\frac{2}{5}\int\frac{1}{1+t^{2}}\mathrm{d}t\\&=\frac{4}{5}\ln|1+2t|-\frac{2}{5}\ln\left(1+t^{2}\right)+\frac{2}{5}\arctan t+C\\&=\frac{4}{5}\ln\left|1+2\tan\frac{x}{2}\right|-\frac{2}{5}\ln\left(1+\tan^{2}\frac{x}{2}\right)+\frac{x}{5}+C\\&=\frac{4}{5}\ln\left|\cos\frac{x}{2}+2\sin\frac{x}{2}\right|+\frac{x}{5}+C.\end{aligned} $$ 

必须指出，尽管部分分式法能够用于求解有理分式函数的不定积分，但正如我们已经看到的，其计算过程太烦琐。因此，在实际计算中，应当优先考虑利用其他方法，如换元积分法或直接积分法等（例3.25、例3.26）。

【例 3.25】 求  $ I=\int\frac{\mathrm{d}x}{x^{2}\left(1+x^{2}\right)^{2}} $

【分析】若采用部分分式法求解本题，则在将被积函数分解成部分分式之和的形式时，由于

 $$ \frac{1}{x^{2}\left(1+x^{2}\right)^{2}}=\frac{a}{x}+\frac{b}{x^{2}}+\frac{c x+d}{1+x^{2}}+\frac{e x+f}{\left(1+x^{2}\right)^{2}}, $$ 

需要确定 6 个待定系数，故运算量较大。而采用换元积分法，就简单得多了。

解 令  $ x = \tan t $，则  $ \mathrm{d}x = \sec^{2}t\mathrm{d}t $。于是

 $$ \begin{aligned}I&=\int\frac{\sec^{2}t\mathrm{d}t}{\tan^{2}t\sec^{4}t}=\int\frac{\mathrm{d}t}{\tan^{2}t\sec^{2}t}=\int\frac{\sec^{2}t-\tan^{2}t}{\tan^{2}t\sec^{2}t}\mathrm{d}t=\int\frac{\mathrm{d}t}{\tan^{2}t}-\int\frac{\mathrm{d}t}{\sec^{2}t}\\&=\int\left(\csc^{2}t-1\right)\mathrm{d}t-\int\cos^{2}t\mathrm{d}t=-\cot t-t-\frac{t}{2}-\frac{1}{4}\sin2t+C\\&=-\frac{1}{x}-\frac{3}{2}\arctan x-\frac{x}{2\left(1+x^{2}\right)}+C.\\ \end{aligned} $$ 

【例 3.26】求  $ I=\int\frac{\mathrm{d}x}{(\sin x+2\sec x)^{2}} $

【分析】这里，被积函数是三角函数有理式，可采用万能代换  $ t = \tan \frac{x}{2} $ 化为有理分式函数，再利用部分分式法求解。这将是一个复杂的计算过程。因此，应考虑综合运用换元积分、分部积分等方法与技巧。

解  $ I=\int\frac{\sec^{2}x\mathrm{d}x}{\sec^{2}x(\sin x+2\sec x)^{2}}=\int\frac{\mathrm{d}(\tan x)}{\left(2\tan^{2}x+\tan x+2\right)^{2}}\xlongequal{t=\tan x}\int\frac{\mathrm{d}t}{\left(2t^{2}+t+2\right)^{2}} $

考虑不定积分  $ I_{1}=\int\frac{dt}{2t^{2}+t+2} $，直接凑微分，可得

 $$ I_{1}=\frac{1}{2}\int\frac{\mathrm{d}t}{\left(t+\frac{1}{4}\right)^{2}+\frac{15}{16}}=\frac{1}{2}\frac{1}{\frac{\sqrt{15}}{4}}\arctan\frac{t+\frac{1}{4}}{\frac{\sqrt{15}}{4}}+C=\frac{2}{\sqrt{15}}\arctan\frac{4t+1}{\sqrt{15}}+C. $$ 

另一方面，利用分部积分，得

 $$ \begin{aligned}I_{1}&=\frac{t}{2t^{2}+t+2}+\int\frac{t(4t+1)\mathrm{d}t}{\left(2t^{2}+t+2\right)^{2}}\\&=\frac{t}{2t^{2}+t+2}+\int\frac{2\left(2t^{2}+t+2\right)-\left(t+\frac{1}{4}\right)-\frac{15}{4}}{\left(2t^{2}+t+2\right)^{2}}\mathrm{d}t\\&=\frac{t}{2t^{2}+t+2}+2\int\frac{\mathrm{d}t}{2t^{2}+t+2}-\frac{1}{4}\int\frac{\mathrm{d}\left(2t^{2}+t+2\right)}{\left(2t^{2}+t+2\right)^{2}}-\frac{15}{4}\int\frac{\mathrm{d}t}{\left(2t^{2}+t+2\right)^{2}}\\&=\frac{t}{2t^{2}+t+2}+2I_{1}+\frac{1}{4\left(2t^{2}+t+2\right)}-\frac{15}{4}I,\\ \end{aligned} $$ 

所以

 $$ \begin{aligned}I&=\frac{4t+1}{15\left(2t^{2}+t+2\right)}+\frac{4}{15}I_{1}=\frac{4t+1}{15\left(2t^{2}+t+2\right)}+\frac{8}{15\sqrt{15}}\arctan\frac{4t+1}{\sqrt{15}}+C_{1}\\&=\frac{4\tan x+1}{15\left(2\tan^{2}x+\tan x+2\right)}+\frac{8}{15\sqrt{15}}\arctan\frac{4\tan x+1}{\sqrt{15}}+C_{1}.\end{aligned} $$ 

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//8ec8a7e3-a076-47c4-8876-f1bed032613b/markdown_2/imgs/img_in_image_box_125_1087_169_1128.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A22Z%2F-1%2F%2F6eb27e6ea1745320cbe249fedbd7f24aefd632bf2b62f9bdf18a8a0fc1c97753" alt="Image" width="4%" /></div>


题型二、定积分的计算

如果  $ F(x) $ 是连续函数  $ f(x) $ 在  $ [a,b] $ 上的任一个原函数，则有 Newton-Leibniz 公式：

 $$ \int_{a}^{b}f(x)\mathrm{d}x=F(b)-F(a). $$ 

利用这一公式，可以将定积分的计算转化为求被积函数的原函数在积分区间两端点处的函数值之差．因此可以说，求定积分即归结为求不定积分．但是在定积分计算中，也有其特殊的性质和技巧．

## 1. 计算定积分的基本方法

定积分的基本计算方法包括

(1) 直接利用 Newton-Leibniz 公式.

(2) 利用定积分的换元法 (不定积分中的几种典型代换也适用于定积分).

如果  $ f(x) $ 在  $ [a,b] $ 上连续,  $ x=\varphi(t) $ 在  $ [\alpha,\beta] $ 上是单值的且有连续导数, 当  $ \alpha\leq t\leq\beta $ 时,  $ a\leq\varphi(t)\leq b,\varphi(\alpha)=a,\varphi(\beta)=b $ , 那么

 $$ \int_{a}^{b}f(x)\mathrm{d}x=\int_{\alpha}^{\beta}f[\varphi(t)]\varphi^{\prime}(t)\mathrm{d}t. $$ 

(3) 利用定积分的分部积分法.

如果  $ u(x), v(x) $ 在  $ [a, b] $ 上具有连续导数  $ u'(x), v'(x) $，那么

 $$ \int_{a}^{b}u(x)v^{\prime}(x)\mathrm{d}x=\left.u(x)v(x)\right|_{a}^{b}-\int_{a}^{b}v(x)u^{\prime}(x)\mathrm{d}x. $$ 

在利用上述三种方法时，应注意以下几点：

(1) 被积函数的适当变形;

(2) 换元函数的灵活选取，且应满足有关条件，换元之后，积分限作相应的变换；

(3) 分部积分时，适当选择  $ u(x) $ 和  $ v'(x) $ 并注意将积分限代入已求出的函数中.

【例 3.27】 计算：(I)  $ I=\int_{0}^{\frac{\pi}{4}}\frac{\mathrm{d}x}{1+\sin x}; $ (II)  $ I=\int_{1}^{\mathrm{e}}\sin(\pi\ln x)\mathrm{d}x. $

解 (I) I =  $ \int_{0}^{\frac{\pi}{4}}\frac{\mathrm{d}x}{1+\cos\left(\frac{\pi}{2}-x\right)}=\int_{0}^{\frac{\pi}{4}}\frac{\mathrm{d}x}{2\cos^{2}\left(\frac{\pi}{4}-\frac{x}{2}\right)}=-\left.\tan\left(\frac{\pi}{4}-\frac{x}{2}\right)\right|_{0}^{\frac{\pi}{4}}=2-\sqrt{2}. $

(Ⅱ) 利用分部积分法，并注意所产生的“回归”现象.

 $$ \begin{align*}I=&\ x\sin(\pi\ln x)|_{1}^{\mathrm{e}}-\pi\int_{1}^{\mathrm{e}}\cos(\pi\ln x)\mathrm{d}x\\=&-\pi x\cos(\pi\ln x)|_{1}^{\mathrm{e}}-\pi^{2}\int_{1}^{\mathrm{e}}\sin(\pi\ln x)\mathrm{d}x=\pi(\mathrm{e}+1)-\pi^{2}I.\end{align*} $$ 

从而  $ I=\frac{\pi(e+1)}{\pi^{2}+1} $

【例 3.28】设函数  $ \varphi(x) $ 满足  $ \varphi'(x)=\arctan(x-1)^{2} $，且  $ \varphi(0)=0 $，求  $ I=\int_{0}^{1}\varphi(x)dx $.

解 利用分部积分，并注意选择合适的  $ u(x) $ 和  $ v'(x) $.

 $$ I=(x-1)\varphi(x)\Big|_{0}^{1}-\int_{0}^{1}(x-1)\varphi^{\prime}(x)\mathrm{d}x $$ 

 $$ \begin{aligned}&=-\int_{0}^{1}(x-1)\arctan(x-1)^{2}\mathrm{d}x\xlongequal{ 令 u=1-x}\int_{0}^{1}u\arctan u^{2}\mathrm{d}u\\&=\left.\frac{u^{2}}{2}\arctan u^{2}\right|_{0}^{1}-\int_{0}^{1}\frac{u^{3}}{1+u^{4}}\mathrm{d}u=\frac{\pi}{8}-\left.\frac{1}{4}\ln\left(1+u^{4}\right)\right|_{0}^{1}\\&=\frac{\pi}{8}-\frac{1}{4}\ln2.\end{aligned} $$ 

2. 计算分段函数的定积分

在计算定积分时，有时需要处理分段函数。可以大致分为三种类型：

(1) 被积函数为分段函数 (例 3.29、例 3.30);

(2) 被积函数含有绝对值 (例 3.31);

(3) 在积分运算过程中（尤其是进行变量代换之后）需分段处理（例 3.32）.

【例 3.29】设  $ f(x)=\left\{\begin{array}{ll}\frac{1}{1+x}, & x \geqslant 0, \\ \frac{1}{1+\mathrm{e}^{x}}, & x < 0,\end{array}\right. $ 求  $ \int_{0}^{2} f(x-1) dx $.

解 令 t = x - 1

 $$ \begin{aligned}\int_{0}^{2}f(x-1)\mathrm{d}x&=\int_{-1}^{1}f(t)\mathrm{d}t=\int_{-1}^{0}f(t)\mathrm{d}t+\int_{0}^{1}f(t)\mathrm{d}t\\&=\int_{-1}^{0}\frac{\mathrm{d}x}{1+\mathrm{e}^{x}}+\int_{0}^{1}\frac{\mathrm{d}x}{1+x}\\&=-\left.\ln\left(1+\mathrm{e}^{-x}\right)\right|_{-1}^{0}+\left.\ln(1+x)\right|_{0}^{1}=\ln(1+\mathrm{e}).\end{aligned} $$ 

【例 3.30】设函数  $ f(x) $ 在  $ (-\infty, +\infty) $ 内恒满足  $ f(x) = f(x - \pi) + \sin x $，且当  $ 0 \leq x < \pi $ 时， $ f(x) = x $。试计算： $ \int_{0}^{3\pi} f(x) \, dx $。

解 这里，被积函数  $ f(x) $ 是分段函数。当  $ \pi \leqslant x < 2\pi $ 时， $ 0 \leqslant x - \pi < \pi $，因此

 $$ f(x)=f(x-\pi)+\sin x=x-\pi+\sin x; $$ 

当  $ 2\pi \leq x < 3\pi $ 时，由于  $ \pi \leq x - \pi < 2\pi $，所以

 $$ f(x)=f(x-\pi)+\sin x=(x-\pi)-\pi+\sin(x-\pi)+\sin x=x-2\pi. $$ 

 $$ \int_{\pi}^{3\pi}f(x)\mathrm{d}x=\int_{\pi}^{2\pi}(x-\pi+\sin x)\mathrm{d}x+\int_{2\pi}^{3\pi}(x-2\pi)\mathrm{d}x=\pi^{2}-2. $$ 

【例 3.31】求  $ I=\int_{a}^{b}x\mathrm{e}^{-|x|}\mathrm{d}x $.

【分析】 含有绝对值的函数也是分段函数. 一般而言, 可按例 3.29 的分段积分法求解这类积分. 但在本例中, 由于积分限都是一般参数, 难以分段处理. 一种可行的方法是,

先求出被积函数的原函数, 再利用 Newton-Leibniz 公式, 但较烦琐. 下面的技巧既简捷也易掌握.

解 若 a > 0, b > 0，则  $ I = \int_{a}^{0} x e^{-x} \mathrm{d} x = -\left(x + 1\right) e^{-x} \bigg|_{a}^{b} = (a + 1) e^{-a} - (b + 1) e^{-b} $

对于一般情形, 可化为上述结果. 这只需利用被积函数  $ xe^{-|x|} $ 的奇偶性, 即得

 $$ I=\int_{a}^{b}x\mathrm{e}^{-|x|}\mathrm{d}x+\int_{|a|}^{a}x\mathrm{e}^{-|x|}\mathrm{d}x+\int_{b}^{|b|}x\mathrm{e}^{-|x|}\mathrm{d}x=\int_{|a|}^{|b|}x\mathrm{e}^{-|x|}\mathrm{d}x. $$ 

因此，有  $ I=(|a|+1)\mathrm{e}^{-|a|}-(|b|+1)\mathrm{e}^{-|b|} $

【例 3.32】求  $ I=\int_{0}^{1}x\arcsin2\sqrt{x(1-x)}\mathrm{d}x $.

解 因  $ x(1-x)=\frac{1}{4}-\left(\frac{1}{2}-x\right)^{2} $，故可令  $ \frac{1}{2}-x=\frac{1}{2}\cos t $，则

 $$ \begin{align*}I&=\frac{1}{4}\int_{0}^{\pi}(1-\cos t)\sin t\arcsin(\sin t)\mathrm{d}t\\&=\frac{1}{4}\int_{0}^{\frac{\pi}{2}}t\sin t(1-\cos t)\mathrm{d}t+\frac{1}{4}\int_{\frac{\pi}{2}}^{\pi}(\pi-t)\sin t(1-\cos t)\mathrm{d}t.\end{align*} $$ 

对上式后一积分作变量代换  $ u = \pi - t $，得

 $$ \int_{\frac{\pi}{2}}^{\pi}(\pi-t)\sin t(1-\cos t)\mathrm{d}t=\int_{0}^{\frac{\pi}{2}}u\sin u(1+\cos u)\mathrm{d}u, $$ 

因此  $ I=\frac{1}{2}\int_{0}^{\frac{\pi}{2}}t\sin t\mathrm{d}t=\left.\frac{1}{2}(-t\cos t)\right|_{0}^{\frac{\pi}{2}}+\frac{1}{2}\int_{0}^{\frac{\pi}{2}}\cos t\mathrm{d}t=\frac{1}{2}. $

## 3. 计算定积分的若干技巧

定积分计算中, 应充分注意到被积函数的特性 (如周期性、奇偶性等) 以及积分区间的对称性, 用以简化计算. 在对三角函数积分时, 这些考虑尤为重要.

以下结论可作为公式使用 (其中  $ f(x) $ 为连续函数):

(1) 若  $ f(x) $ 为偶函数，则  $ \int_{-a}^{a}f(x)\mathrm{d}x=2\int_{0}^{a}f(x)\mathrm{d}x(a>0); $

(2) 若  $ f(x) $ 为奇函数，则  $ \int_{-a}^{a} f(x) \, \mathrm{d}x = 0 \, (a > 0) $;

(3)  $ \int_{-a}^{a} f(x) \, dx = \int_{0}^{a} [f(x) + f(-x)] \, dx \, (a > 0); $

(4) 若  $ f(x) $ 以 T 为周期, 则  $ \int_{a}^{a+T} f(x) \, \mathrm{d}x = \int_{0}^{T} f(x) \, \mathrm{d}x $ (其中 a 为任意实数);

(5)  $ \int_{0}^{\frac{\pi}{2}} f(\sin x) dx = \int_{0}^{\frac{\pi}{2}} f(\cos x) dx; $

(6)

 $$ \int_{0}^{\pi}x f(\sin x)\mathrm{d}x=\frac{\pi}{2}\int_{0}^{\pi}f(\sin x)\mathrm{d}x; $$ 

(7)  $ \int_{0}^{\frac{\pi}{2}}\sin^{2n}x\mathrm{d}x=\frac{(2n-1)!!}{(2n)!!}\cdot\frac{\pi}{2},\int_{0}^{\frac{\pi}{2}}\sin^{2n+1}x\mathrm{d}x=\frac{(2n)!!}{(2n+1)!!} $. 此即 Wallis (沃利斯) 公式, 对余弦函数  $ \cos x $ 也有这两个公式.

此外，变量代换、分部积分、拆项等各种方法与技巧的综合运用，往往也能使某些定积分的计算化难为易或化繁为简。

【例 3.33】求: (I)  $ I=\int_{0}^{n\pi}\sqrt{1-\sin2x}\,dx;\quad(\mathrm{II})\,I=\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\frac{\sin^{4}x}{1+\mathrm{e}^{-x}}dx. $

解 (I) 被积函数  $ \sqrt{1 - \sin 2x} = |\cos x - \sin x| $ 以  $ \pi $ 为周期，故由上述公式 (4) 有

 $$ \begin{aligned}I&=\sum_{k=0}^{n-1}\int_{k\pi}^{(k+1)\pi}|\cos x-\sin x|\mathrm{d}x=n\int_{0}^{\pi}|\cos x-\sin x|\mathrm{d}x\\&=n\int_{0}^{\frac{\pi}{4}}(\cos x-\sin x)\mathrm{d}x+n\int_{\frac{\pi}{4}}^{\pi}(\sin x-\cos x)\mathrm{d}x=2\sqrt{2}n.\end{aligned} $$ 

(Ⅱ) 注意到积分区间关于原点对称, 利用公式 (3) 以及公式 (7) 可得

 $$ I=\int_{0}^{\frac{\pi}{2}}\left[\frac{\sin^{4}x}{1+\mathrm{e}^{-x}}+\frac{\sin^{4}(-x)}{1+\mathrm{e}^{-(-x)}}\right]\mathrm{d}x=\int_{0}^{\frac{\pi}{2}}\sin^{4}x\mathrm{d}x=\frac{3}{4}\cdot\frac{1}{2}\cdot\frac{\pi}{2}=\frac{3\pi}{16}. $$ 

【例 3.34】求：(I)  $ I=\int_{0}^{\frac{\pi}{2}}\frac{\sin^{3}x}{\sin x+\cos x}dx;\quad(\mathrm{II}) $  $ I=\int_{-\frac{\pi}{4}}^{\frac{\pi}{4}}\frac{x}{1+\sin x}dx. $

解 (I) 根据积分区间与被积函数的特征, 可利用公式(5)求解. 故有

 $$ \begin{aligned}I&=\int_{0}^{\frac{\pi}{2}}\frac{\cos^{3}x}{\cos x+\sin x}\mathrm{d}x=\frac{1}{2}\int_{0}^{\frac{\pi}{2}}\frac{\sin^{3}x+\cos^{3}x}{\sin x+\cos x}\mathrm{d}x\\&=\frac{1}{2}\int_{0}^{\frac{\pi}{2}}\left(\sin^{2}x-\sin x\cos x+\cos^{2}x\right)\mathrm{d}x\\&=\frac{1}{2}\int_{0}^{\frac{\pi}{2}}(1-\sin x\cos x)\mathrm{d}x=\frac{\pi-1}{4}.\end{aligned} $$ 

(Ⅱ) 本题的特征适合于利用公式 (3)，但利用公式 (1)，(2) 也不难求解.

 $$ \begin{aligned}I&=\int_{-\frac{\pi}{4}}^{\frac{\pi}{4}}\frac{x(1-\sin x)}{(1+\sin x)(1-\sin x)}\mathrm{d}x=\int_{-\frac{\pi}{4}}^{\frac{\pi}{4}}\left(\frac{x}{\cos^{2}x}-\frac{x\sin x}{\cos^{2}x}\right)\mathrm{d}x\\&=-2\int_{0}^{\frac{\pi}{4}}\frac{x\sin x}{\cos^{2}x}\mathrm{d}x=-\left.2\frac{x}{\cos x}\right|_{0}^{\frac{\pi}{4}}+2\int_{0}^{\frac{\pi}{4}}\sec x\mathrm{d}x\\&=-\frac{\sqrt{2}\pi}{2}+2\ln(\sec x+\tan x)\bigg|_{0}^{\frac{\pi}{4}}=-\frac{\sqrt{2}\pi}{2}+2\ln(1+\sqrt{2}).\end{aligned} $$ 

【例 3.35】（第五届全国初赛题，2013）计算定积分  $ I=\int_{-\pi}^{\pi}\frac{x\sin x\cdot\arctan e^{x}}{1+\cos^{2}x}dx. $

解 对任意 x，恒有  $ \arctan e^{x} + \arctan e^{-x} = \frac{\pi}{2} $（详见本章例 3.47）。利用公式 (3)，得

 $$ \begin{aligned}I&=\int_{0}^{\pi}\frac{x\sin x\cdot(\arctan\mathrm{e}^{x}+\arctan\mathrm{e}^{-x})}{1+\cos^{2}x}\mathrm{d}x\\&=\frac{\pi}{2}\int_{0}^{\pi}\frac{x\sin x}{1+\cos^{2}x}\mathrm{d}x.\end{aligned} $$ 

根据积分区间与被积函数的特征, 可利用公式(6). 因此

 $$ I=\left(\frac{\pi}{2}\right)^{2}\int_{0}^{\pi}\frac{\sin x}{1+\cos^{2}x}\mathrm{d}x=-\left.\frac{\pi^{2}}{4}\arctan(\cos x)\right|_{0}^{\pi}=\frac{\pi^{3}}{8}. $$ 

【例 3.36】（第六届全国初赛题，2014）计算  $ I=\int_{\mathrm{e}^{-2n\pi}}^{1}\left|\frac{\mathrm{d}}{\mathrm{d}x}\left(\cos\ln\frac{1}{x}\right)\right|\mathrm{d}x $，其中 n 为正整数.

解 被积函数与周期函数有关, 可考虑利用公式 (4) 求解. 先作变量代换:  $ u = \ln x $.

 $$ \begin{aligned}I&=\int_{\mathrm{e}^{-2n\pi}}^{1}\left|\frac{\mathrm{d}}{\mathrm{d}x}(\cos\ln x)\right|\mathrm{d}x=\int_{\mathrm{e}^{-2n\pi}}^{1}\left|(\sin\ln x)\frac{1}{x}\right|\mathrm{d}x\\&=\int_{-2n\pi}^{0}|\sin u|\mathrm{d}u=\int_{0}^{2n\pi}|\sin t|\mathrm{d}t\\&=\sum_{k=1}^{2n}\int_{(k-1)\pi}^{k\pi}|\sin t|\mathrm{d}t=\sum_{k=1}^{2n}\int_{0}^{\pi}|\sin t|\mathrm{d}t\\&=2n\int_{0}^{\pi}\sin t\mathrm{d}t=4n.\end{aligned} $$ 

【例 3.37】求: (I)  $ \int_{0}^{1}\frac{\ln(1+x)}{1+x^{2}}\mathrm{d}x $; (II)  $ \int_{0}^{2\pi}\frac{\mathrm{d}x}{2+\cos x} $; (III)  $ \int_{0}^{\frac{\pi}{2}}\frac{\sin x\mathrm{d}x}{1+\sqrt{\sin2x}} $.

解 (I) 令  $ x = \tan t $，则

 $$ \begin{aligned}I&=\int_{0}^{\frac{\pi}{4}}\ln(1+\tan t)\mathrm{d}t=\int_{0}^{\frac{\pi}{4}}\ln(\sin x+\cos x)\mathrm{d}x-\int_{0}^{\frac{\pi}{4}}\ln\cos x\mathrm{d}x\\&=\int_{0}^{\frac{\pi}{4}}\ln\left(\sqrt{2}\cos\left(\frac{\pi}{4}-x\right)\right)\mathrm{d}x-\int_{0}^{\frac{\pi}{4}}\ln\cos x\mathrm{d}x\\&=\frac{\pi}{8}\ln2+\int_{0}^{\frac{\pi}{4}}\ln\cos\left(\frac{\pi}{4}-x\right)\mathrm{d}x-\int_{0}^{\frac{\pi}{4}}\ln\cos x\mathrm{d}x\\&=\frac{\pi}{8}\ln2\quad\left( 对上式前一积分作代换 u=\frac{\pi}{4}-x 即得后一积分 \right).\end{aligned} $$ 

(Ⅱ) $ I=\int_{0}^{\pi}\frac{\mathrm{d}x}{2+\cos x}+\int_{\pi}^{2\pi}\frac{\mathrm{d}x}{2+\cos x} $. 对后一个积分作变量代换： $ x=\pi+t $.

 $$ I=\int_{0}^{\pi}\left(\frac{1}{2+\cos x}+\frac{1}{2-\cos x}\right)\mathrm{d}x=4\int_{0}^{\pi}\frac{\mathrm{d}x}{3+\sin^{2}x}. $$ 

注意到被积函数是周期为 $ \pi $的周期函数，利用公式(4)，得

 $$ I=4\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\frac{\mathrm{d}x}{3+\sin^{2}x}=-\frac{8}{\sqrt{3}}\int_{0}^{\frac{\pi}{2}}\frac{\mathrm{d}(\sqrt{3}\cot x)}{4+3\cot^{2}x}=-\frac{4}{\sqrt{3}}\arctan\left(\frac{\sqrt{3}}{2}\cot x\right)_{0}^{\frac{\pi}{2}}=\frac{2\pi}{\sqrt{3}}. $$ 

（Ⅲ）先作变量代换： $ x = t + \frac{\pi}{4} $，并利用对称性，再令  $ \sqrt{2}\sin t = \sin u $，得

 $$ \begin{aligned}I&=\int_{-\frac{\pi}{4}}^{\frac{\pi}{4}}\frac{\sin\left(t+\frac{\pi}{4}\right)}{1+\sqrt{\sin\left(2t+\frac{\pi}{2}\right)}}\mathrm{d}t=\frac{\sqrt{2}}{2}\int_{-\frac{\pi}{4}}^{\frac{\pi}{4}}\frac{\sin t+\cos t}{1+\sqrt{\cos2t}}\mathrm{d}t\\&=\sqrt{2}\int_{0}^{\frac{\pi}{4}}\frac{\cos t}{1+\sqrt{\cos2t}}\mathrm{d}t=\sqrt{2}\int_{0}^{\frac{\pi}{4}}\frac{\cos t}{1+\sqrt{1-2\sin^{2}t}}\mathrm{d}t\\&=\int_{0}^{\frac{\pi}{2}}\frac{\cos u}{1+\cos u}\mathrm{d}u=\frac{\pi}{2}-\int_{0}^{\frac{\pi}{2}}\frac{\mathrm{d}u}{1+\cos u}\\&=\frac{\pi}{2}-\frac{1}{2}\int_{0}^{\frac{\pi}{2}}\sec^{2}\frac{u}{2}\mathrm{d}u=\frac{\pi}{2}-1.\\ \end{aligned} $$ 

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//9173a6cd-53d8-48c0-81e5-d28d06923dc7/markdown_0/imgs/img_in_image_box_125_824_168_864.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A18Z%2F-1%2F%2Fa4298c0058921ce97a0bab50125ad991c5052004e41c270eab8370b9794a423f" alt="Image" width="4%" /></div>


#### 题型三、定积分的几类典型问题

关于定积分，除计算方法与技巧外，还有以下几类十分典型的问题：

(1) 关于变上限积分的函数;

(2) 定积分的极限问题;

(3) 关于积分等式的证明题;

(4) 证明积分不等式 (详见本节的题型七).

1. 关于变上限积分的函数

如果  $ f(x) $ 在  $ [a,b] $ 上连续,  $ \varphi(x) $ 在  $ [a,b] $ 上可导, 那么

 $$ F(x)=\int_{a}^{\varphi(x)}f(t)\mathrm{d}t $$ 

在  $ [a,b] $ 上可导，且  $ F'(x) = f[\varphi(x)]\varphi'(x) $， $ a \leqslant x \leqslant b $.

研究变上限积分的函数的性质时，往往要利用  $ F(x) $ 的这一特性.

【例 3.38】（I）当  $ x \geqslant 0 $ 时， $ f(x) $ 连续，且满足  $ \int_{0}^{x^{2}(1+x)} f(t) dt = x $，求  $ f(2) $.

（Ⅱ）设  $ f(x) $ 连续，且满足  $ f(x)=x+x^{2}\int_{0}^{1}f(x)\mathrm{d}x+x^{3}\int_{0}^{2}f(x)\mathrm{d}x $，求  $ f(x) $.

解 (I) 欲求  $ f(2) $，需先求出  $ f(x) $. 故只要将所给方程两端对 x 求导即可.

 $$ f\left[x^{2}(1+x)\right]\cdot\left[2x(1+x)+x^{2}\right]=1, $$ 

取 x=1 ，则  $ x^{2}(1+x)=2 $ ，代入上式得  $ f(2)=\frac{1}{5} $

（Ⅱ）令  $ a=\int_{0}^{1}f(x)\mathrm{d}x,b=\int_{0}^{2}f(x)\mathrm{d}x $ ，则所给等式即  $ f(x)=x+ax^{2}+bx^{3} $ 。所以

 $$ a=\int_{0}^{1}f(x)\mathrm{d}x=\int_{0}^{1}\left(x+ax^{2}+bx^{3}\right)\mathrm{d}x=\frac{1}{2}+\frac{a}{3}+\frac{b}{4}, $$ 

 $$ b=\int_{0}^{2}f(x)\mathrm{d}x=\int_{0}^{2}\left(x+ax^{2}+bx^{3}\right)\mathrm{d}x=2+\frac{8a}{3}+4b, $$ 

由此解得  $ a=\frac{3}{8}, b=-1 $ 。故  $ f(x)=x+\frac{3}{8}x^{2}-x^{3} $

【例 3.39】设  $ f(x) $ 是区间  $ \left[0,\frac{\pi}{4}\right] $ 上的单调、可导函数，且满足

 $$ \int_{0}^{f(x)}f^{-1}(t)\mathrm{d}t=\int_{0}^{x}t\frac{\cos t-\sin t}{\sin t+\cos t}\mathrm{d}t, $$ 

其中  $ f^{-1} $ 是 f 的反函数，求  $ f(x) $.

解 对所给等式两端求导，得

 $$ f^{-1}[f(x)]f^{\prime}(x)=x\frac{\cos x-\sin x}{\sin x+\cos x}. $$ 

因为  $ f^{-1}[f(x)] = x $，所以由上式可得  $ f'(x) = \frac{\cos x - \sin x}{\sin x + \cos x} $，从而有

 $$ f(x)=\int\frac{\cos x-\sin x}{\sin x+\cos x}\mathrm{d}x=\ln(\sin x+\cos x)+C. $$ 

再由所给等式得  $ \int_{0}^{f(0)}f^{-1}(t)dt=0 $ 。又据题设知， $ f^{-1}(t) $ 的值域为  $ \left[0,\frac{\pi}{4}\right] $，并且是单调非负函数，所以必有  $ f(0)=0 $ 。由此可得 C=0 。故  $ f(x)=\ln(\sin x+\cos x) $ 。

【例 3.40】设函数  $ f(x) $ 连续，且  $ \int_{0}^{x}tf(2x-t)dt=\frac{1}{2}\arctan x^{2} $. 已知  $ f(1)=1 $，求  $ \int_{1}^{2}f(x)dx $ 的值.

解 被积函数含变上限 x. 令 u = 2x - t，则  $ t = 2x - u, \mathrm{d}t = -\mathrm{d}u $，从而

 $$ \int_{0}^{x}tf(2x-t)\mathrm{d}t=-\int_{2x}^{x}(2x-u)f(u)\mathrm{d}u=2x\int_{x}^{2x}f(u)\mathrm{d}u-\int_{x}^{2x}uf(u)\mathrm{d}u. $$ 

于是

 $$ 2x\int_{x}^{2x}f(u)\mathrm{d}u-\int_{x}^{2x}u f(u)\mathrm{d}u=\frac{1}{2}\arctan x^{2}. $$ 

将上式两边对 x 求导，得

 $$ 2\int_{x}^{2x}f(u)\mathrm{d}u+2x[2f(2x)-f(x)]-[2xf(2x)\cdot2-xf(x)]=\frac{x}{1+x^{4}}, $$ 

即  $ 2\int_{x}^{2x}f(u)\mathrm{d}u=\frac{x}{1+x^{4}}+xf(x) $. 令 x=1, 得

 $$ 2\int_{1}^{2}f(u)\mathrm{d}u=\frac{1}{2}+1=\frac{3}{2}. $$ 

于是  $ \int_{1}^{2}f(x)\mathrm{d}x=\frac{3}{4} $

## 2. 定积分中的极限问题

【例 3.41】设可微函数  $ y = f(x) $ 由方程  $ e^{x-2y} - x^{2}y = 1 $ 所确定. 试求极限:

 $$ I=\lim_{x\to\pi^{+}}\frac{\sin x}{\sqrt{(x-\pi)^{3}}}\int_{0}^{1}f(\sqrt{x-\pi}t)\mathrm{d}t. $$ 

解 首先, 由方程  $ e^{x-2y}-x^{2}y=1 $ 可知, 当 x=0 时 y=0, 即  $ f(0)=0 $, 并根据隐函数求导法则得  $ \mathrm{e}^{x-2y}(1-2y')-2xy-x^{2}y'=0 $, 从而有  $ f'(0)=y'(0)=\frac{1}{2} $.

其次，对极限式中的定积分作变量代换： $ \sqrt{x-\pi}t=u $，则

 $$ \int_{0}^{1}f(\sqrt{x-\pi}t)\mathrm{d}t=\frac{1}{\sqrt{x-\pi}}\int_{0}^{\sqrt{x-\pi}}f(u)\mathrm{d}u. $$ 

于是利用重要极限  $ \lim_{x\to0}\frac{\sin x}{x}=1 $ 以及 L'Hospital 法则，得

 $$ \begin{aligned}I&=\lim_{x\to\pi^{+}}\frac{\sin x}{(x-\pi)^{2}}\int_{0}^{\sqrt{x-\pi}}f(u)\mathrm{d}u=\lim_{x\to\pi^{+}}\frac{-\sin(x-\pi)}{x-\pi}\cdot\frac{\int_{0}^{\sqrt{x-\pi}}f(u)\mathrm{d}u}{x-\pi}\\&=-\frac{1}{2}\lim_{x\to\pi^{+}}\frac{f(\sqrt{x-\pi})}{\sqrt{x-\pi}}\quad( 以下利用导数 f^{\prime}(0) 的定义 )\\&=-\frac{1}{2}\lim_{x\to\pi^{+}}\frac{f(\sqrt{x-\pi})-f(0)}{\sqrt{x-\pi}-0}=-\frac{1}{2}f^{\prime}(0)=-\frac{1}{4}.\end{aligned} $$ 

【例 3.42】（第四届全国决赛题，2013）设函数  $ f(x) $ 在区间  $ [1, +\infty) $ 上连续可导，且

 $$ f^{\prime}(x)=\frac{1}{1+f^{2}(x)}\left[\sqrt{\frac{1}{x}}-\sqrt{\ln\left(1+\frac{1}{x}\right)}\right], $$ 

证明： $ \lim_{x\to+\infty}f(x) $ 存在.

证 利用不等式:  $ \frac{x}{1+x}<\ln(1+x)<x(x>0) $.

易知，当  $ x \geqslant 1 $ 时， $ f'(x) > 0 $ 。所以  $ f(x) $ 在  $ [1, +\infty) $ 上单调增加。因为

 $$ \begin{align*}f^{\prime}(x)&\leqslant\sqrt{\frac{1}{x}}-\sqrt{\ln\left(1+\frac{1}{x}\right)}<\sqrt{\frac{1}{x}}-\sqrt{\frac{\frac{1}{x}}{1+\frac{1}{x}}}=\frac{1}{\sqrt{x}}-\frac{1}{\sqrt{1+x}}\\&=\frac{\sqrt{1+x}-\sqrt{x}}{\sqrt{x(1+x)}}=\frac{1}{(\sqrt{1+x}+\sqrt{x})\sqrt{x(1+x)}}\leqslant\frac{1}{2\sqrt{x^{3}}},\end{align*} $$ 

所以，当 $ x\geqslant1 $时，有

 $$ \begin{align*}f(x)&=f(1)+\int_{1}^{x}f^{\prime}(t)\mathrm{d}t\leqslant f(1)+\frac{1}{2}\int_{1}^{x}\frac{1}{\sqrt{t^{3}}}\mathrm{d}t\\&\leqslant f(1)+\frac{1}{2}\int_{1}^{+\infty}\frac{1}{\sqrt{t^{3}}}\mathrm{d}t=f(1)+1,\end{align*} $$ 

即  $ f(x) $ 在  $ [1,+\infty) $ 上有上界. 根据单调有界准则, 可知  $ \lim_{x\to+\infty}f(x) $ 存在.

【例 3.43】证明： $ \lim_{n\to\infty}\frac{1}{2n+1}\left(\frac{(2n)!!}{(2n-1)!!}\right)^2=\frac{\pi}{2} $

证 当  $ 0 < x < \frac{\pi}{2} $ 时， $ \sin^{2n+1}x < \sin^{2n}x < \sin^{2n-1}x $ 。所以

 $$ \int_{0}^{\frac{\pi}{2}}\sin^{2n+1}x\mathrm{d}x<\int_{0}^{\frac{\pi}{2}}\sin^{2n}x\mathrm{d}x<\int_{0}^{\frac{\pi}{2}}\sin^{2n-1}x\mathrm{d}x. $$ 

利用 Wallis 公式，有

 $$ \frac{(2n)!!}{(2n+1)!!}<\frac{(2n-1)!!}{(2n)!!}\cdot\frac{\pi}{2}<\frac{(2n-2)!!}{(2n-1)!!}, $$ 

 $$ \frac{1}{2n+1}\left(\frac{(2n)!!}{(2n-1)!!}\right)^{2}<\frac{\pi}{2}<\frac{1}{2n}\left(\frac{(2n)!!}{(2n-1)!!}\right)^{2}. $$ 

将上述不等式两边同时减去  $ \frac{1}{2n+1}\left(\frac{(2n)!!}{(2n-1)!!}\right)^2 $，得

 $$ 0<\frac{\pi}{2}-\frac{1}{2n+1}\left(\frac{(2n)!!}{(2n-1)!!}\right)^{2}<\frac{1}{2n(2n+1)}\left(\frac{(2n)!!}{(2n-1)!!}\right)^{2}<\frac{1}{2n}\cdot\frac{\pi}{2}. $$ 

由此利用夹逼法则即得  $ \lim_{n\to\infty}\frac{1}{2n+1}\left(\frac{(2n)!!}{(2n-1)!!}\right)^2=\frac{\pi}{2} $

【例 3.44】设函数  $ f(x) $,  $ g(x) $ 在闭区间  $ [a, b] $ 上连续，且  $ f(x) \geqslant 0 $,  $ g(x) > 0 $ ( $ x \in [a, b] $). 试求极限:  $ \lim_{n \to \infty} \int_{a}^{b} f(x) \sqrt[n]{g(x)} \, \mathrm{d}x $.

解 因为  $ g(x) $ 在  $ [a,b] $ 上连续且恒正，所以  $ g(x) $ 在  $ [a,b] $ 上存在最小值 m 与最大值 M，且 m > 0, M > 0。注意到  $ f(x) \geqslant 0 $，并利用定积分的性质，得

 $$ \sqrt[n]{m}\int_{a}^{b}f(x)\mathrm{d}x\leqslant\int_{a}^{b}f(x)\sqrt[n]{g(x)}\mathrm{d}x\leqslant\sqrt[n]{M}\int_{a}^{b}f(x)\mathrm{d}x. $$ 

由于  $ \lim_{n\to\infty}\sqrt[n]{m}=\lim_{n\to\infty}\sqrt[n]{M}=1 $，故根据夹逼法则，得

 $$ \lim_{n\to\infty}\int_{a}^{b}f(x)\sqrt[n]{g(x)}\mathrm{d}x=\int_{a}^{b}f(x)\mathrm{d}x. $$ 

【注】虽然直接将极限运算取到积分符号里面，也能得到正确结果，即

 $$ \lim_{n\to\infty}\int_{a}^{b}f(x)\sqrt[n]{g(x)}\mathrm{d}x=\int_{a}^{b}f(x)\lim_{n\to\infty}\sqrt[n]{g(x)}\mathrm{d}x=\int_{a}^{b}f(x)\mathrm{d}x, $$ 

但交换求积分与求极限这两种运算的顺序是不可取的，这需要相应的理论作支撑。

【例 3.45】设  $ f(x) $ 是以 T 为周期的连续函数, 证明:

 $$ \lim_{x\to+\infty}\frac{1}{x}\int_{0}^{x}f(t)\mathrm{d}t=\frac{1}{T}\int_{0}^{T}f(t)\mathrm{d}t. $$ 

证 令  $ F(x)=\int_{0}^{x}f(t)\mathrm{d}t-cx $，其中  $ c=\frac{1}{T}\int_{0}^{T}f(t)\mathrm{d}t $，则对任意  $ x\in(-\infty,+\infty) $，有

 $$ F(x+T)-F(x)=\int_{x}^{x+T}f(t)\mathrm{d}t-cT. $$ 

由于  $ f(x) $ 是以 T 为周期的连续函数，故由公式 (4)，有  $ \int_{x}^{x+T} f(t) dt = \int_{0}^{T} f(t) dt $。代入上式，得  $ F(x + T) = F(x) $，所以  $ F(x) $ 也是以 T 为周期的连续函数，因而是有界函数。于是

 $$ \lim_{x\to+\infty}\frac{1}{x}\int_{0}^{x}f(t)\mathrm{d}t=c+\lim_{x\to+\infty}\frac{F(x)}{x}=c=\frac{1}{T}\int_{0}^{T}f(t)\mathrm{d}t. $$ 

【注】利用本题的结论，可知 $ \lim_{x\to+\infty}\frac{1}{x}\int_{0}^{x}\left|\sin t\right|dt=\frac{2}{\pi} $

## 3. 关于积分等式的证明题

证明积分等式主要有三种方法：变量代换、分部积分以及微分法。前两种方法是积分学本身的方法，主要是将积分变形，以证明等式成立。而使用微分法的好处在于，叙述简短、规律性强，且无需任何技巧。此外，在证明含有“介值”的积分等式时，还需结合连续函数介值定理、微分中值定理等结论。

【例 3.46】证明： $ \int_{1}^{a}f\left(x^{2}+\frac{a^{2}}{x^{2}}\right)\frac{\mathrm{d}x}{x}=\int_{1}^{a}f\left(x+\frac{a^{2}}{x}\right)\frac{\mathrm{d}x}{x} $

证 对等式左端作变量代换  $ t=x^{2} $，得

 $$ \begin{align*}\int_{1}^{a}f\left(x^{2}+\frac{a^{2}}{x^{2}}\right)\frac{\mathrm{d}x}{x}=\frac{1}{2}\int_{1}^{a^{2}}f\left(t+\frac{a^{2}}{t}\right)\frac{\mathrm{d}t}{t}\\=\frac{1}{2}\left[\int_{1}^{a}f\left(t+\frac{a^{2}}{t}\right)\frac{\mathrm{d}t}{t}+\int_{a}^{a^{2}}f\left(t+\frac{a^{2}}{t}\right)\frac{\mathrm{d}t}{t}\right].\end{align*} $$ 

对上式右端第2项作倒置代换  $ u=\frac{a^{2}}{t} $，得

 $$ \int_{a}^{a^{2}}f\left(t+\frac{a^{2}}{t}\right)\frac{\mathrm{d}t}{t}=\int_{1}^{a}f\left(u+\frac{a^{2}}{u}\right)\frac{\mathrm{d}u}{u}. $$ 

代入上式即得所证等式.

【例 3.47】设函数  $ f(x) $,  $ g(x) $ 在区间  $ [-a, a] $ 上连续  $ (a > 0) $,  $ g(x) $ 为偶函数，且  $ f(x) $ 满足  $ f(x) + f(-x) = A $ (A 为常数).

(1) 证明： $ \int_{-a}^{a}f(x)g(x)\mathrm{d}x=A\int_{0}^{a}g(x)\mathrm{d}x. $

(2) 利用 (1) 的结论计算定积分:  $ \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}} |\sin x| \arctan e^{x} dx $.

(1) 证  $ \int_{-a}^{a}f(x)g(x)\mathrm{d}x=\int_{-a}^{0}f(x)g(x)\mathrm{d}x+\int_{0}^{a}f(x)g(x)\mathrm{d}x. $ 对右边第一个积分，令 x=-t，并注意到  $ g(x) $ 为偶函数，则有

 $$ \int_{-a}^{0}f(x)g(x)\mathrm{d}x=-\int_{a}^{0}f(-t)g(-t)\mathrm{d}t=\int_{0}^{a}f(-t)g(t)\mathrm{d}t. $$ 

因此，得

 $$ \int_{-a}^{a}f(x)g(x)\mathrm{d}x=\int_{0}^{a}[f(x)+f(-x)]g(x)\mathrm{d}x=A\int_{0}^{a}g(x)\mathrm{d}x. $$ 

(2) 解 取  $ f(x)=\arctan\mathrm{e}^{x} $,  $ g(x)=|\sin x| $，则  $ g(x) $ 为偶函数。为了利用 (1) 的结论，只需验证： $ f(x)+f(-x)=\arctan\mathrm{e}^{x}+\arctan\mathrm{e}^{-x} $ 为常数。由于

 $$ \left(\arctan\mathrm{e}^{x}+\arctan\mathrm{e}^{-x}\right)^{\prime}=\frac{\mathrm{e}^{x}}{1+\mathrm{e}^{2x}}-\frac{\mathrm{e}^{-x}}{1+\mathrm{e}^{-2x}}=0, $$ 

且  $ f(0)=\frac{\pi}{4} $，所以  $ f(x)+f(-x)=\frac{\pi}{2} $，因此

 $$ \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\left|\sin x\right|\arctan\mathrm{e}^{x}\mathrm{d}x=\frac{\pi}{2}\int_{0}^{\frac{\pi}{2}}\sin x\mathrm{d}x=\frac{\pi}{2}. $$ 

【例 3.48】设函数  $ f(x) $ 在闭区间  $ [a,b] $ 上具有连续的二阶导数。试证：存在  $ \xi \in (a,b) $，使

 $$ \int_{a}^{b}f(x)\mathrm{d}x=(b-a)f\left(\frac{a+b}{2}\right)+\frac{1}{24}(b-a)^{3}f^{\prime\prime}(\xi). $$ 

【分析】 对于给出函数具有二阶以上导数的条件的题目，我们往往优先考虑利用 Taylor 公式来解。但应注意到 Taylor 公式的每一项都具有 k 阶导数  $ f^{(k)}(x_0) $ 与增量的 k 次幂  $ (x - x_0)^k $ 对应相乘这一特征。而在本题中，欲证明的等式右端第二项是二阶导数与三次幂相乘。因此可考虑构造一个辅助函数  $ F(x) $，使  $ F'''(x) = f''(x) $，并对  $ F(x) $ 利用 Taylor 公式。自然，最容易想到的是  $ F(x) = \int_a^x f(t) \, dt $。至此，解题思路即有了端倪。

证 考虑辅助函数  $ F(x)=\int_{a}^{x}f(t)dt $，则  $ F(x) $ 在  $ [a,b] $ 上具有连续的三阶导数.

记  $ x_{0}=\frac{a+b}{2} $,  $ h=\frac{b-a}{2} $，对  $ F(x) $ 利用 Taylor 公式，有

 $$ F\left(x_{0}-h\right)=F\left(x_{0}\right)-F^{\prime}\left(x_{0}\right)h+\frac{F^{\prime\prime}\left(x_{0}\right)}{2!}h^{2}-\frac{F^{\prime\prime\prime}\left(\xi_{1}\right)}{3!}h^{3}\quad\left(x_{0}-h<\xi_{1}<x_{0}\right), $$ 

 $$ F\left(x_{0}+h\right)=F\left(x_{0}\right)+F^{\prime}\left(x_{0}\right)h+\frac{F^{\prime\prime}\left(x_{0}\right)}{2!}h^{2}+\frac{F^{\prime\prime\prime}\left(\xi_{2}\right)}{3!}h^{3}\quad\left(x_{0}<\xi_{2}<x_{0}+h\right). $$ 

两式相减，得  $ F(x_{0}+h)-F(x_{0}-h)=2hF'(x_{0})+\frac{1}{6}h^{3}[F'''(\xi_{1})+F'''(\xi_{2})] $，即

 $$ \int_{a}^{b}f(x)\mathrm{d}x=(b-a)f\left(\frac{a+b}{2}\right)+\frac{1}{48}(b-a)^{3}\left[f^{\prime\prime}\left(\xi_{1}\right)+f^{\prime\prime}\left(\xi_{2}\right)\right]. $$ 

再对  $ f''(x) $ 利用闭区间上连续函数的介值定理，存在  $ \xi \in (\xi_1, \xi_2) \subset (a, b) $，使得

 $$ \frac{1}{2}\left[f^{\prime\prime}\left(\xi_{1}\right)+f^{\prime\prime}\left(\xi_{2}\right)\right]=f^{\prime\prime}(\xi). $$ 

代入 $ ^{①} $式，即得所证等式.

【例 3.49】设  $ f(x) $ 在  $ [a,b] $ 上连续，在  $ (a,b) $ 内有二阶导数。证明：存在  $ \xi \in (a,b) $，使得

 $$ \int_{a}^{b}f(x)\mathrm{d}x=\frac{1}{2}[f(a)+f(b)](b-a)-\frac{1}{12}f^{\prime\prime}(\xi)(b-a)^{3}. $$ 

【分析】本题有明确的几何意义，给出了定积分的近似计算中“梯形公式”的理论支持，即对于小区间  $ [a,b] $ 上的连续函数  $ f(x) $，用  $ \frac{1}{2}[f(a)+f(b)](b-a) $ 作为定积分  $ \int_{a}^{b}f(x)\mathrm{d}x $ 的近似值，其“截断误差”为  $ -\frac{1}{12}f''(\xi)(b-a)^3 $， $ \xi\in(a,b) $.

证 (方法1) 用 “k 值法”. 令

 $$ k=\frac{\displaystyle\int_{a}^{b}f(x)\mathrm{d}x-\frac{1}{2}[f(a)+f(b)](b-a)}{-\frac{1}{12}(b-a)^{3}}, $$ 

构造辅助函数

 $$ F(x)=\int_{a}^{x}f(t)\mathrm{d}t-\frac{1}{2}[f(x)+f(a)](x-a)+\frac{k}{12}(x-a)^{3}, $$ 

则  $ F(x) $ 在  $ [a,b] $ 上满足 Rolle 定理的条件，故存在  $ c \in (a,b) $，使  $ F'(c) = 0 $，即

 $$ f(c)-\frac{1}{2}f^{\prime}(c)(c-a)-\frac{1}{2}[f(c)+f(a)]+\frac{k}{4}(c-a)^{2}=0, $$ 

亦即

 $$ f(a)=f(c)+f^{\prime}(c)(a-c)+\frac{k}{2}(a-c)^{2}. $$ 

另一方面，对  $ f(x) $ 利用 Taylor 公式，存在  $ \xi \in (a, c) $ 使得

 $$ f(a)=f(c)+f^{\prime}(c)(a-c)+\frac{1}{2}f^{\prime\prime}(\xi)(a-c)^{2}. $$ 

比较②、③两式，有  $ k = f''(\xi) $. 代入①式即得所证.

（方法 2）先证：若  $ f(x) $ 在  $ [a,b] $ 上具有三阶导数，则存在  $ \xi \in (a,b) $，使

 $$ f(b)=f(a)+\frac{1}{2}\left[f^{\prime}(a)+f^{\prime}(b)\right](b-a)-\frac{1}{12}f^{\prime\prime\prime}(\xi)(b-a)^{3}. $$ 

事实上，令  $ F(x) = f(x) - f(a) - \frac{1}{2}(x - a)[f'(a) + f'(x)] $,  $ G(x) = -\frac{1}{12}(x - a)^3 $，则  $ F(a) = G(a) = 0 $,  $ F'(a) = G'(a) = 0 $。两次利用 Cauchy 中值定理，得

 $$ \frac{F(b)}{G(b)}=\frac{F(b)-F(a)}{G(b)-G(a)}=\frac{F^{\prime}\left(x_{0}\right)}{G^{\prime}\left(x_{0}\right)}=\frac{F^{\prime}\left(x_{0}\right)-F^{\prime}(a)}{G^{\prime}\left(x_{0}\right)-G^{\prime}(a)}=\frac{F^{\prime\prime}(\xi)}{G^{\prime\prime}(\xi)}, $$ 

其中  $ a < \xi < x_{0} < b $. 注意到  $ F''(x) = -\frac{1}{2}(x - a)f'''(x) $,  $ G''(x) = -\frac{1}{2}(x - a) $, 代入上式即得所证.

再回到原题. 令  $ F(x)=\int_{a}^{x}f(t)dt $，则  $ F(x) $ 在  $ [a,b] $ 上具有三阶导数，且  $ F(a)=0 $.

对函数  $  F(x)  $ 利用已证得的④式即可.

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//8314f252-e87a-4612-9ca8-ad8d51e38e65/markdown_0/imgs/img_in_image_box_125_162_169_204.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A18Z%2F-1%2F%2F1c4cc80fbbc86c9e11c636a1470a06b5a729b62c8f11c551536115343a40d123" alt="Image" width="4%" /></div>


#### 题型四、广义积分的计算

广义积分有无穷区间上的广义积分与无界函数的广义积分两种。根据定义，在计算广义积分时，应将其转化为先计算定积分再取极限。事实上，可将这两个步骤一并进行，被积函数的原函数在积分限的值可用极限方式获得。值得注意的是，应区分无界函数的广义积分与定积分。有时，变量代换可将广义积分转化为常义积分，或者将常义积分转化为广义积分。

【例 3.50】求：(1) $ I=\int_{1}^{+\infty}\frac{\arctan x}{x^{2}}\mathrm{d}x;\quad(2) $  $ I=\int_{1}^{2}\left(\frac{1}{x\ln^{2}x}-\frac{1}{(x-1)^{2}}\right)\mathrm{d}x $

解(1)

 $$ \begin{aligned}1)I&=\int_{1}^{+\infty}\arctan x\mathrm{d}\left(-\frac{1}{x}\right)=-\left.\frac{\arctan x}{x}\right|_{1}^{+\infty}+\int_{1}^{+\infty}\frac{\mathrm{d}x}{x\left(1+x^{2}\right)}\\&=\left(-\lim_{x\rightarrow+\infty}\frac{\arctan x}{x}+\frac{\pi}{4}\right)+\int_{1}^{+\infty}\left(\frac{1}{x}-\frac{x}{1+x^{2}}\right)\mathrm{d}x\\&=\frac{\pi}{4}+\left.\left[\ln x-\frac{1}{2}\ln\left(1+x^{2}\right)\right]\right|_{1}^{+\infty}\\&=\frac{\pi}{4}+\lim_{x\rightarrow+\infty}\left[\ln x-\frac{1}{2}\ln\left(1+x^{2}\right)\right]+\frac{1}{2}\ln2\\&=\frac{\pi}{4}+\lim_{x\rightarrow+\infty}\ln\frac{x}{\sqrt{1+x^{2}}}+\frac{1}{2}\ln2=\frac{\pi}{4}+\frac{1}{2}\ln2;\end{aligned} $$ 

 $$ \begin{aligned}(2)I&=\left(-\frac{1}{\ln x}+\frac{1}{x-1}\right)\bigg|_{1}^{2}=1-\frac{1}{\ln2}-\lim_{x\to1^{+}}\left(-\frac{1}{\ln x}+\frac{1}{x-1}\right)\\&=1-\frac{1}{\ln2}-\left(-\frac{1}{2}\right)=\frac{3}{2}-\frac{1}{\ln2}.\end{aligned} $$ 

【例 3.51】试证： $ \int_{0}^{\frac{\pi}{2}}\frac{x\cos x\sin x}{\left(a^{2}\cos^{2}x+b^{2}\sin^{2}x\right)^{2}}\mathrm{d}x=\frac{\pi}{4ab^{2}(a+b)} $（其中 a>0, b>0，且  $ a\neq b $）.

证 令  $ \tan x = t $，则当 x = 0 时，t = 0；当  $ x = \frac{\pi}{2} $ 时， $ t = +\infty $。所以

 $$ \begin{aligned}I&=\int_{0}^{\frac{\pi}{2}}\frac{x\cos x\sin x}{\left(a^{2}+b^{2}\tan^{2}x\right)^{2}\cos^{4}x}\mathrm{d}x=\int_{0}^{\frac{\pi}{2}}\frac{x\tan x}{\left(a^{2}+b^{2}\tan^{2}x\right)^{2}}\mathrm{d}(\tan x)\\&=\int_{0}^{+\infty}\frac{t\arctan t}{\left(a^{2}+b^{2}t^{2}\right)^{2}}\mathrm{d}t=-\frac{1}{2b^{2}}\int_{0}^{+\infty}\arctan t\mathrm{d}\left(\frac{1}{a^{2}+b^{2}t^{2}}\right)\\&=-\frac{1}{2b^{2}}\left[\left.\frac{\arctan t}{a^{2}+b^{2}t^{2}}\right|_{0}^{+\infty}-\int_{0}^{+\infty}\frac{\mathrm{d}t}{\left(a^{2}+b^{2}t^{2}\right)(1+t^{2})}\right]\\&=\frac{1}{2b^{2}\left(a^{2}-b^{2}\right)}\int_{0}^{+\infty}\left(\frac{1}{1+t^{2}}-\frac{b^{2}}{a^{2}+b^{2}t^{2}}\right)\mathrm{d}t\end{aligned} $$ 

 $$ =\frac{1}{2b^{2}\left(a^{2}-b^{2}\right)}\left(\arctan t-\frac{b}{a}\arctan\frac{bt}{a}\right)\bigg|_{0}^{+\infty}=\frac{\pi}{4ab^{2}(a+b)}. $$ 

【例 3.52】证明： $ \int_{0}^{+\infty}\frac{\mathrm{d}x}{1+x^{4}}=\int_{0}^{+\infty}\frac{x^{2}}{1+x^{4}}\mathrm{d}x=\frac{\pi}{2\sqrt{2}} $

证 令  $ x = \frac{1}{t} $，则  $ \mathrm{d}x = -\frac{1}{t^{2}}\mathrm{d}t $.

 $$ \begin{align*}\int_{0}^{+\infty}\frac{\mathrm{d}x}{1+x^{4}}&=\int_{0}^{+\infty}\frac{t^{2}}{1+t^{4}}\mathrm{d}t=\frac{1}{2}\int_{0}^{+\infty}\frac{1+x^{2}}{1+x^{4}}\mathrm{d}x=\frac{1}{2}\int_{0}^{+\infty}\frac{\mathrm{d}\left(x-\frac{1}{x}\right)}{\left(x-\frac{1}{x}\right)^{2}+2}\\&=\frac{1}{2\sqrt{2}}\arctan\left(\frac{x}{\sqrt{2}}-\frac{1}{\sqrt{2}x}\right)\bigg|_{0}^{+\infty}=\frac{1}{2\sqrt{2}}\left[\frac{\pi}{2}-\left(-\frac{\pi}{2}\right)\right]=\frac{\pi}{2\sqrt{2}}.\end{align*} $$ 

【例 3.53】证明： $ \int_{0}^{\frac{\pi}{2}}\ln\sin xdx=\int_{0}^{\frac{\pi}{2}}\ln\cos xdx=-\frac{\pi}{2}\ln2 $

证 令  $ x = \frac{\pi}{2} - t $，则  $ \int_{0}^{\frac{\pi}{2}} \ln \sin x \, dx = \int_{0}^{\frac{\pi}{2}} \ln \cos t \, dt $。再令 x = 2u，得

 $$ \begin{aligned}I&=\int_{0}^{\frac{\pi}{2}}\ln\sin x\mathrm{d}x=2\int_{0}^{\frac{\pi}{4}}\ln\sin2u\mathrm{d}u\\&=2\int_{0}^{\frac{\pi}{4}}\ln2\mathrm{d}u+2\int_{0}^{\frac{\pi}{4}}\ln\sin u\mathrm{d}u+2\int_{0}^{\frac{\pi}{4}}\ln\cos u\mathrm{d}u\\&=\frac{\pi}{2}\ln2+2\int_{0}^{\frac{\pi}{4}}\ln\sin u\mathrm{d}u+2\int_{\frac{\pi}{4}}^{\frac{\pi}{2}}\ln\sin v\mathrm{d}v\quad\left(u=\frac{\pi}{2}-v\right)\\&=\frac{\pi}{2}\ln2+2\int_{0}^{\frac{\pi}{2}}\ln\sin x\mathrm{d}x=\frac{\pi}{2}\ln2+2I.\\ \end{aligned} $$ 

 $$ I=\int_{0}^{\frac{\pi}{2}}\ln\sin x\mathrm{d}x=\int_{0}^{\frac{\pi}{2}}\ln\cos x\mathrm{d}x=-\frac{\pi}{2}\ln2. $$ 

【例 3.54】(第十届全国决赛题, 2019) 设  $ a > 0 $, 则  $ \int_{0}^{+\infty} \frac{\ln x}{x^{2} + a^{2}} \mathrm{d}x = $ ___.

解 记  $ I=\int_{0}^{+\infty}\frac{\ln x}{x^{2}+a^{2}}\mathrm{d}x $．作变量代换：x=at，得

 $$ I=\frac{1}{a}\int_{0}^{+\infty}\frac{\ln a+\ln t}{1+t^{2}}\mathrm{d}t=\frac{\ln a}{a}\int_{0}^{+\infty}\frac{\mathrm{d}t}{1+t^{2}}+\frac{1}{a}\int_{0}^{+\infty}\frac{\ln t}{1+t^{2}}\mathrm{d}t. $$ 

对上式右端第一项，得

 $$ \int_{0}^{+\infty}\frac{\mathrm{d}t}{1+t^{2}}=\arctan t\bigg|_{0}^{+\infty}=\frac{\pi}{2}; $$ 

对右端第二项作代换： $ t=\frac{1}{u} $，得

 $$ I_{1}=\int_{0}^{+\infty}\frac{\ln t}{1+t^{2}}\mathrm{d}t=-\int_{0}^{+\infty}\frac{\ln u}{1+u^{2}}\mathrm{d}u=-I_{1}, $$ 

所以  $ I_{1}=0 $ 。因此，得

 $$ I=\frac{\ln a}{a}\cdot\frac{\pi}{2}+\frac{1}{a}\times0=\frac{\pi\ln a}{2a}. $$ 

【例 3.55】 计算： $ \int_{0}^{+\infty}\frac{e^{-x^{2}}}{\left(x^{2}+\frac{1}{2}\right)^{2}}\mathrm{d}x $.

解 先计算不定积分，得

 $$ \begin{aligned}\int\frac{\mathrm{e}^{-x^{2}}}{\left(x^{2}+\frac{1}{2}\right)^{2}}\mathrm{d}x&=-\int\frac{\mathrm{e}^{-x^{2}}}{2x}\mathrm{d}\left(\frac{1}{x^{2}+\frac{1}{2}}\right)=-\frac{\mathrm{e}^{-x^{2}}}{2x\left(x^{2}+\frac{1}{2}\right)}+\int\frac{1}{2x^{2}+1}\mathrm{d}\left(\frac{\mathrm{e}^{-x^{2}}}{x}\right)\\&=-\frac{\mathrm{e}^{-x^{2}}}{2x^{3}+x}-\int\frac{\mathrm{e}^{-x^{2}}}{x^{2}}\mathrm{d}x=-\frac{\mathrm{e}^{-x^{2}}}{2x^{3}+x}+\frac{\mathrm{e}^{-x^{2}}}{x}+2\int\mathrm{e}^{-x^{2}}\mathrm{d}x\\&=\frac{2x\mathrm{e}^{-x^{2}}}{2x^{2}+1}+2\int\mathrm{e}^{-x^{2}}\mathrm{d}x,\end{aligned} $$ 

因此，得

 $$ \int_{0}^{+\infty}\frac{\mathrm{e}^{-x^{2}}}{\left(x^{2}+\frac{1}{2}\right)^{2}}\mathrm{d}x=\left.\frac{2x\mathrm{e}^{-x^{2}}}{2x^{2}+1}\right|_{0}^{+\infty}+2\int_{0}^{+\infty}\mathrm{e}^{-x^{2}}\mathrm{d}x=2\int_{0}^{+\infty}\mathrm{e}^{-x^{2}}\mathrm{d}x=\sqrt{\pi}. $$ 

【注】这里，利用了已知结果，即 Gauss 积分： $ \int_{0}^{+\infty}e^{-x^{2}}dx=\frac{\sqrt{\pi}}{2} $

【例 3.56】设  $ f(x) $ 在  $ [0,+\infty) $ 上连续，且  $ \int_{A}^{+\infty}\frac{f(x)}{x}\mathrm{d}x $ 收敛，其中常数 A > 0. 试证明：

 $$ \int_{0}^{+\infty}\frac{f(ax)-f(bx)}{x}\mathrm{d}x=f(0)\ln\frac{b}{a}\quad(0<a<b). $$ 

证 任取  $ \delta>0 $ ，有

 $$ \begin{align*}\int_{\delta}^{+\infty}\frac{f(ax)-f(bx)}{x}\mathrm{d}x&=\int_{\delta}^{+\infty}\frac{f(ax)}{x}\mathrm{d}x-\int_{\delta}^{+\infty}\frac{f(bx)}{x}\mathrm{d}x\\&=\int_{a\delta}^{+\infty}\frac{f(u)}{u}\mathrm{d}u-\int_{b\delta}^{+\infty}\frac{f(u)}{u}\mathrm{d}u=\int_{a\hat{\delta}}^{b\delta}\frac{f(u)}{u}\mathrm{d}u\end{align*} $$ 

 $$ =f(\xi)\int_{a\delta}^{b\delta}\frac{1}{u}\mathrm{d}u=f(\xi)\ln\frac{b}{a}\quad(a\delta<\xi<b\delta), $$ 

注意到  $ f(x) $ 的连续性,  $ \lim_{\delta\to0^{+}}f(\xi)=\lim_{\xi\to0^{+}}f(\xi)=f(0) $, 因此

 $$ \int_{0}^{+\infty}\frac{f(ax)-f(bx)}{x}\mathrm{d}x=\lim_{\delta\to0^{+}}\int_{\delta}^{+\infty}\frac{f(ax)-f(bx)}{x}\mathrm{d}x=\lim_{\delta\to0^{+}}f(\xi)\ln\frac{b}{a}=f(0)\ln\frac{b}{a}. $$ 

【注】我们证明的这个等式称为 Frullani（傅汝兰尼）积分公式，在计算广义积分时，有时可利用这个公式直接给出计算结果.

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//8314f252-e87a-4612-9ca8-ad8d51e38e65/markdown_3/imgs/img_in_image_box_125_445_169_486.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A20Z%2F-1%2F%2F76012ff4f90e2fe74f578df367adf05215a948a4ec04578d1a54934f41bcece9" alt="Image" width="4%" /></div>


#### 题型五、定积分在几何中的应用

这里，着重介绍定积分在几何中的三种应用：

(1) 求平面图形的面积;

(2) 求旋转体的体积与侧面积;

(3) 求平面曲线的弧长.

## 1. 求平面图形的面积

设平面图形是由曲线  $ y = f(x)(f(x) \geqslant 0) $ 及直线 x = a, x = b (a < b) 与 x 轴所围成的曲边梯形，其面积为  $ A = \int_{a}^{b} f(x) \, dx $.

一般而言，如果平面图形由曲线  $ y = f_{1}(x) $,  $ y = f_{2}(x) $ 和直线 x = a, x = b (a < b) 所围成，那么其面积计算公式为

 $$ A=\int_{a}^{b}\left|f_{1}(x)-f_{2}(x)\right|\mathrm{d}x. $$ 

设平面图形是由曲线  $ r = r(\theta)(\alpha \leqslant \theta \leqslant \beta) $ 围成的，则其面积为  $ A = \frac{1}{2} \int_{\alpha}^{\beta} [r(\theta)]^2 \, \mathrm{d}\theta $.

【例 3.57】设封闭曲线 L 的极坐标方程为  $ r = \cos 3\theta\left(-\frac{\pi}{6} \leqslant \theta \leqslant \frac{\pi}{6}\right) $，求 L 所围平面图形的面积.

解 所求平面图形的面积为

 $$ \begin{align*}S&=\frac{1}{2}\int_{\alpha}^{\beta}[r(\theta)]^{2}\mathrm{d}\theta=\frac{1}{2}\int_{-\frac{\pi}{6}}^{\frac{\pi}{6}}\cos^{2}3\theta\mathrm{d}\theta=\int_{0}^{\frac{\pi}{6}}\frac{1+\cos6\theta}{2}\mathrm{d}\theta\\&=\frac{1}{2}\left(\theta+\frac{\sin6\theta}{6}\right)\bigg|_{0}^{\frac{\pi}{6}}=\frac{\pi}{12}.\end{align*} $$ 

【例 3.58】设函数  $ f(x)=\frac{x}{1+x}, x \in [0,1] $. 定义函数列：

 $$ f_{1}(x)=f(x),f_{2}(x)=f\left(f_{1}(x)\right),\cdots,f_{n}(x)=f\left(f_{n-1}(x)\right),\cdots. $$ 

记  $ S_{n} $ 是由曲线  $ y = f_{n}(x) $，直线 x = 1 及 x 轴所围平面图形的面积，求极限  $ \lim_{n \to \infty} nS_{n} $.

解 根据题设，得

 $$ f_{2}(x)=f\left(f_{1}(x)\right)=\frac{f_{1}(x)}{1+f_{1}(x)}=\frac{\frac{x}{1+x}}{1+\frac{x}{1+x}}=\frac{x}{1+2x}; $$ 

 $$ f_{3}(x)=f\left(f_{2}(x)\right)=\frac{f_{2}(x)}{1+f_{2}(x)}=\frac{\frac{x}{1+2x}}{1+\frac{x}{1+2x}}=\frac{x}{1+3x}; $$ 

由数学归纳法得  $ f_{n}(x)=\frac{x}{1+nx}(n=1,2,3,\cdots) $. 于是

 $$ S_{n}=\int_{0}^{1}\frac{x}{1+nx}\mathrm{d}x=\frac{1}{n}\int_{0}^{1}\left(1-\frac{1}{1+nx}\right)\mathrm{d}x=\frac{1}{n}-\frac{\ln(1+n)}{n^{2}}. $$ 

因此，有  $ \lim_{n\to\infty}nS_n=\lim_{n\to\infty}\left(1-\frac{\ln(1+n)}{n}\right)=1 $

2. 求旋转体的体积与侧面积

(1) 由 xOy 平面上的曲线  $ y = f(x) $ 与直线 x = a, x = b 以及 x 轴所围成的曲边梯形绕 x 轴旋转而成的旋转体体积为  $ V = \pi \int_{0}^{b} [f(x)]^{2} \, dx $.

(2) 由 xOy 平面上的曲线  $ y = f(x) $ 与直线 x = a, x = b 以及 x 轴所围成的曲边梯形绕 y 轴旋转而成的旋转体体积为  $ V = 2\pi \int_{a}^{b} x f(x) \, dx $.

(3) 由 xOy 平面上的曲线  $ y = f(x) $ ( $ a \leq x \leq b $) 绕 x 轴旋转而成的旋转曲面的面积为

 $$ A=2\pi\int_{a}^{b}f(x)\sqrt{1+\left[f^{\prime}(x)\right]^{2}}\mathrm{d}x. $$ 

【例 3.59】过点  $ P(1,0) $ 作抛物线  $ y = \sqrt{x - 2} $ 的切线，该切线与上述抛物线及 x 轴围成一平面图形. 求此平面图形绕 x 轴旋转一周所成旋转体的体积.

解 设所作切线与抛物线相切于点  $ (x_{0}, \sqrt{x_{0}-2}) $. 因为

 $$ y^{\prime}|_{x=x_{0}}=\left.\frac{1}{2\sqrt{x-2}}\right|_{x=x_{0}}=\frac{1}{2\sqrt{x_{0}-2}}, $$ 

故该切线的方程为  $ y - \sqrt{x_{0} - 2} = \frac{1}{2\sqrt{x_{0} - 2}} (x - x_{0}) $. 又因为该切线过点  $ P(1,0) $，所以

 $$ -\sqrt{x_{0}-2}=\frac{1}{2\sqrt{x_{0}-2}}\left(1-x_{0}\right), $$ 

即  $ x_{0}=3 $ 。从而，切线的方程是  $ y=\frac{1}{2}(x-1) $ 。因此，所求旋转体的体积为

 $$ V=\pi\int_{1}^{3}\frac{1}{4}(x-1)^{2}\mathrm{d}x-\pi\int_{2}^{3}(x-2)\mathrm{d}x=\frac{\pi}{6}. $$ 

【例 3.60】设 D 是由曲线  $ y = \sqrt{1 - x^{2}} (0 \leqslant x \leqslant 1) $ 与  $ \left\{\begin{array}{l} x = \cos^{3} t, \\ y = \sin^{3} t \end{array}\right. $  $ (0 \leqslant t \leqslant \frac{\pi}{2}) $ 围成的平面区域，求 D 绕 x 轴旋转一周所得旋转体的体积和表面积.

【分析】 曲线  $ \left\{\begin{array}{l}x=\cos^{3}t,\quad(0\leqslant t\leqslant\frac{\pi}{2})\\y=\sin^{3}t\end{array}\right. $ 是用参数方程表示的星形线，位于第一象限的部分，其直角坐标方程为  $ x^{\frac{2}{3}}+y^{\frac{2}{3}}=1(0\leqslant x\leqslant1) $. 主要注意两点：一是两条曲线的交点  $ (1,0) $ 与  $ (0,1) $; 二是两条曲线的位置关系，圆  $ y=\sqrt{1-x^{2}} $  $ (0\leqslant x\leqslant1) $ 位于星形线的上方.

解 设 D 绕 x 轴旋转一周所得旋转体的体积为 V，表面积为 A，则

 $$ \begin{aligned}V&=\pi\int_{0}^{1}y^{2}\mathrm{d}x-\pi\int_{\frac{\pi}{2}}^{0}\sin^{6}t\mathrm{d}\left(\cos^{3}t\right)\\&=\pi\int_{0}^{1}\left(1-x^{2}\right)\mathrm{d}x-3\pi\int_{0}^{\frac{\pi}{2}}\sin^{7}t\cos^{2}t\mathrm{d}t\\&=\frac{2\pi}{3}-3\pi\left(\int_{0}^{\frac{\pi}{2}}\sin^{7}t\mathrm{d}t-\int_{0}^{\frac{\pi}{2}}\sin^{9}t\mathrm{d}t\right)\\&=\frac{2\pi}{3}-3\pi\left(\frac{6}{7}\cdot\frac{4}{5}\cdot\frac{2}{3}-\frac{8}{9}\cdot\frac{6}{7}\cdot\frac{4}{5}\cdot\frac{2}{3}\right)=\frac{18}{35}\pi,\end{aligned} $$ 

 $$ \begin{aligned}A&=2\pi\int_{0}^{\frac{\pi}{2}}\sin t\sqrt{\sin^{2}t+\cos^{2}t}\mathrm{d}t+2\pi\int_{0}^{\frac{\pi}{2}}\sin^{3}t\sqrt{9\sin^{2}t\cos^{4}t+9\cos^{2}t\sin^{4}t}\mathrm{d}t\\&=2\pi\int_{0}^{\frac{\pi}{2}}\sin t\mathrm{d}t+6\pi\int_{0}^{\frac{\pi}{2}}\sin^{4}t\cos t\mathrm{d}t=2\pi+\frac{6}{5}\pi=\frac{16}{5}\pi.\end{aligned} $$ 

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//fbe50be0-b972-4b91-b520-5f7af4f83048/markdown_1/imgs/img_in_image_box_125_1049_326_1263.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A27Z%2F-1%2F%2F4a346fdf860bb070302ee8b06b660d9d0352ed1f0bdbd64e0f97eff3eafe99f5" alt="Image" width="18%" /></div>


<div style="text-align: center;"><div style="text-align: center;">图3.1</div> </div>


【注】这里，在计算 $ \int_{0}^{\frac{\pi}{2}}\sin^{7}tdt $ 和 $ \int_{0}^{\frac{\pi}{2}}\sin^{9}tdt $ 时直接利用了 Wallis 公式.

【例 3.61】如图 3.1, 两个相互外切的圆同时内切于半径为 R 的圆 M. 连接三圆心的直线垂直于圆 M 外的直线 EF, 且圆心 M 到 EF 的距离为 2R. 试求两个小圆的半径, 使得这 3 个圆所围成的平面图形绕 EF 旋转时所得旋转体体积最大.

图 3.1 解 只需计算一个圆绕其外一直线旋转所得旋转体体积  $ V_{0} $

即可. 建立坐标系如图 3.1 所示. 设圆的半径为 a, 圆心到转轴的距离为  $ \rho $, 则圆的方程为

 $ x^{2}+(y-\rho)^{2}=a^{2} $. 故有

 $$ \begin{align*}V_{0}&=\pi\int_{-a}^{a}\left[\left(\rho+\sqrt{a^{2}-x^{2}}\right)^{2}-\left(\rho-\sqrt{a^{2}-x^{2}}\right)^{2}\right]\mathrm{d}x\\&=8\pi\rho\int_{0}^{a}\sqrt{a^{2}-x^{2}}\mathrm{d}x=8\pi\rho\cdot\frac{1}{4}\pi a^{2}=2\pi^{2}\rho a^{2}.\end{align*} $$ 

现假设上面小圆的半径为 r，则下面小圆的半径为 R - r，且上、下两个小圆的圆心到转轴的距离分别为 3R - r, 2R - r。于是，所述旋转体的体积为

 $$ \begin{aligned}V&=V_{ 大 }-V_{ 上 }-V_{ 下 }\\&=2\pi^{2}(2R)R^{2}-2\pi^{2}(3R-r)r^{2}-2\pi^{2}(2R-r)(R-r)^{2}\\&=2\pi^{2}\left(2r^{3}-7Rr^{2}+5R^{2}r\right)\quad(0<r<R).\\ \end{aligned} $$ 

由  $ \frac{\mathrm{d}V}{\mathrm{d}r}=2\pi^{2}\left(6r^{2}-14Rr+5R^{2}\right)=0 $ ，可解得  $ r=\frac{7-\sqrt{19}}{6}R $ 。这是函数  $ V(r) $ 在其定义域  $ (0,R) $ 内的唯一驻点。因为在该点处  $ \frac{\mathrm{d}^{2}V}{\mathrm{d}r^{2}}=4\pi^{2}(6r-7R)=-4\sqrt{19}\pi^{2}R<0 $ ，所以当  $ r=\frac{7-\sqrt{19}}{6}R $ 时，函数  $ V(r) $ 取极大值，从而取最大值。

因此，上下两个小圆的半径分别为  $ r = \frac{7 - \sqrt{19}}{6} R $ 与  $ R - r = \frac{\sqrt{19} - 1}{6} R $.

## 3. 求平面曲线的弧长

(1) 如果平面曲线的方程为  $ y = f(x) (a \leq x \leq b) $，则 x 介于 a 与 b 之间的曲线弧长为

 $$ s=\int_{a}^{b}\sqrt{1+\left(y^{\prime}\right)^{2}}\mathrm{d}x=\int_{a}^{b}\sqrt{1+\left[f^{\prime}(x)\right]^{2}}\mathrm{d}x. $$ 

(2) 如果平面曲线的方程由极坐标给出:  $ r = r(\theta)(\alpha \leqslant \theta \leqslant \beta) $，则  $ \theta $ 介于  $ \alpha $ 与  $ \beta $ 之间的曲线弧长为

 $$ s=\int_{\alpha}^{\beta}\sqrt{[r(\theta)]^{2}+[r^{\prime}(\theta)]^{2}}\mathrm{d}\theta. $$ 

(3) 如果平面曲线的方程由参数方程给出： $ x = \varphi(t), y = \psi(t) (\alpha \leqslant t \leqslant \beta) $，则 t 介于  $ \alpha $ 与  $ \beta $ 之间的曲线弧长为

 $$ s=\int_{\alpha}^{\beta}\sqrt{\left[\varphi^{\prime}(t)\right]^{2}+\left[\psi^{\prime}(t)\right]^{2}}\mathrm{d}t. $$ 

需要注意的是，由于上述弧长计算公式中的被积函数都是正的，为使弧长得正值，在确定积分限时应使积分上限大于积分下限。

【例 3.62】 求抛物线  $ y^{2}=4ax $ 的渐屈线（即曲率中心的轨迹曲线） $ 27ay^{2}=4(x-2a)^{3} $ 被该抛物线所截得的一段弧长.

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//fbe50be0-b972-4b91-b520-5f7af4f83048/markdown_3/imgs/img_in_image_box_125_171_400_367.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A28Z%2F-1%2F%2Ff7eb3c34142702f91a4c3cb8a57785f5bafb13f36f00d07b23354d6b24f85a76" alt="Image" width="25%" /></div>


解 首先容易求得两曲线的交点为  $ (8a, \pm 4\sqrt{2}a) $，而渐屈线交 x 轴于点  $ (2a, 0) $（图 3.2）。由于渐屈线在上半平面的方程为

<div style="text-align: center;"><div style="text-align: center;">图3.2</div> </div>


 $$ y=\frac{2}{3}\sqrt{\frac{(x-2a)^{3}}{3a}}, $$ 

因此  $ y' = \sqrt{\frac{x - 2a}{3a}} $ 。故根据对称性，得

 $$ s=2\int_{2a}^{8a}\sqrt{1+\left(y^{\prime}\right)^{2}}\mathrm{d}x=\frac{2}{\sqrt{3a}}\int_{2a}^{8a}\sqrt{x+a}\mathrm{d}x=2(3\sqrt{3}-1)a. $$ 

【例 3.63】 求曲线弧  $ r = a \sin^{3} \frac{\theta}{3} $ 的全长.

解 这里，所给曲线的方程是极坐标表达式。只要能确定 $ \theta $的变化范围，即可利用相应的公式计算出所求弧长。

显然，当 $ \theta=0 $时，r=0。当 $ \theta $从0开始增大时，r也从0开始增大。当 $ \theta=\frac{3\pi}{2} $时，r=a达到最大。当 $ \theta $继续增大时，r开始从a减少。当 $ \theta $增大到 $ 3\pi $时，r减少到0，回到了极点（图3.3）。此时，点 $ (r,\theta) $的轨迹已经形成了一条封闭曲线。可见， $ \theta $的变化范围是 $ [0,3\pi] $。因此所求弧长为

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//fbe50be0-b972-4b91-b520-5f7af4f83048/markdown_3/imgs/img_in_image_box_702_540_932_747.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A28Z%2F-1%2F%2F441d1719b84ba99365950ced4df5e9f2f89e5c6109518c75e1b17058e9948daf" alt="Image" width="21%" /></div>


<div style="text-align: center;"><div style="text-align: center;">图3.3</div> </div>


 $$ \begin{aligned}s&=\int_{0}^{3\pi}\sqrt{[r(\theta)]^{2}+[r^{\prime}(\theta)]^{2}}\mathrm{d}\theta\\&=\int_{0}^{3\pi}\sqrt{a^{2}\sin^{6}\frac{\theta}{3}+a^{2}\sin^{4}\frac{\theta}{3}\cos^{2}\frac{\theta}{3}}\mathrm{d}\theta\\&=a\int_{0}^{3\pi}\sin^{2}\frac{\theta}{3}\mathrm{d}\theta=a\int_{0}^{3\pi}\frac{1}{2}\left(1-\cos\frac{2\theta}{3}\right)\mathrm{d}\theta\\&=a\left(\frac{\theta}{2}-\frac{3}{4}\sin\frac{2\theta}{3}\right)\bigg|_{0}^{3\pi}=\frac{3a\pi}{2}.\end{aligned} $$ 

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//fbe50be0-b972-4b91-b520-5f7af4f83048/markdown_3/imgs/img_in_image_box_125_1100_169_1142.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A28Z%2F-1%2F%2F6253e8642270e84e0973745e0d465b096440d211b93e3dbb9c9033238a0ecd0c" alt="Image" width="4%" /></div>


#### 题型六、定积分在物理中的应用

求解积分学的物理应用问题主要有两种方法：公式法与元素法。在积分学中，有些物理量，如质量、重心、变力做功等，可以用相应的积分公式来表示。有些物理量，如物体对质点的引力等，则需利用元素法求解。元素法又称微元法。

在具体解答过程中, 要注重利用平面区域、空间区域以及曲线弧段等几何体的对称性特征与定积分  $ \int_{0}^{\frac{\pi}{2}}\sin^{n}x dx $ 或  $ \int_{0}^{\frac{\pi}{2}}\cos^{n}x dx $ 的值, 以便于简化计算, 提高计算速度.

## 1. 求物体的质量与重心

若  $ f(x) $ 代表细棒的质量密度，细棒所占区间为  $ [a, b] $，则细棒的质量为

 $$ M=\int_{a}^{b}f(x)\mathrm{d}x, $$ 

重心坐标为

 $$ \bar{x}=\frac{1}{M}\int_{a}^{b}x f(x)\mathrm{d}x. $$ 

【例 3.64】一根长度为 1 的细棒位于 x 轴的区间  $ [0,1] $ 上，其线密度  $ \rho(x)=-x^{2}+2x+1 $，求该细棒的质心坐标  $ \bar{x} $.

解 利用细棒的质心坐标公式, 得

 $$ M=\int_{0}^{1}\rho(x)\mathrm{d}x=\int_{0}^{1}\left(-x^{2}+2x+1\right)\mathrm{d}x=\frac{5}{3}, $$ 

 $$ \bar{x}=\frac{1}{M}\int_{0}^{1}x\rho(x)\mathrm{d}x=\frac{3}{5}\int_{0}^{1}x\left(-x^{2}+2x+1\right)\mathrm{d}x=\frac{3}{5}\times\frac{11}{12}=\frac{11}{20}. $$ 

## 2. 求变力所做的功

若质点沿变力  $ F(x) $ 方向从 x = a 到 x = b 做直线运动，则变力所做的功为

 $$ W=\int_{a}^{b}F(x)\mathrm{d}x. $$ 

【例 3.65】 一容器的内侧是由下述曲线绕 y 轴旋转一周而成的曲面. 该曲线由  $ x^{2}+y^{2}=2y\left(y\geqslant\frac{1}{2}\right) $ 与  $ x^{2}+y^{2}=1\left(y\leqslant\frac{1}{2}\right) $ 连接而成.

(I) 求容器的容积;

(Ⅱ) 若将容器内盛满的水从容器顶部全部抽出，问至少需要做多少功？

【注】长度单位：m，重力加速度为  $ g \, m/s^{2} $，水的密度为  $ 1 \times 10^{3} kg/m^{3} $.

解 (I) 由对称性知，容器位于  $ y = \frac{1}{2} $ 上、下两侧部分的容积相等，因此，只需考察  $ -1 \leqslant y \leqslant \frac{1}{2} $ 部分，曲线可表示为

 $$ x=f(y)=\sqrt{1-y^{2}}\quad\left(-1\leqslant y\leqslant\frac{1}{2}\right). $$ 

因此，容积为

 $$ V=2\int_{-1}^{\frac{1}{2}}\pi f^{2}(y)\mathrm{d}y=2\pi\int_{-1}^{\frac{1}{2}}\left(1-y^{2}\right)\mathrm{d}y=\frac{9}{4}\pi. $$ 

（Ⅱ）将容器内侧曲线表示为 x = f(y)，在 y 轴上取小区间  $ [y, y + \mathrm{d}y] $，对应容器内小薄片水的重力为  $ \rho g \pi f^{2}(y)\mathrm{d}y $，其中  $ \rho $ 为水的密度，g 为重力加速度。抽出这部分水需走过的路程近似为 2 - y，将此薄层水抽出需做的功近似等于  $ \mathrm{d}W = \rho g \pi f^{2}(y)(2 - y)\mathrm{d}y $。所以

 $$ \begin{aligned}W&=\rho g\pi\int_{-1}^{2}f^{2}(y)(2-y)\mathrm{d}y\\&=\rho g\pi\int_{-1}^{\frac{1}{2}}\left(1-y^{2}\right)(2-y)\mathrm{d}y+\rho g\pi\int_{\frac{1}{2}}^{2}\left(2y-y^{2}\right)(2-y)\mathrm{d}y\\&=\rho g\pi\left(\frac{153}{64}+\frac{63}{64}\right)=\frac{27}{8}\rho g\pi.\\ \end{aligned} $$ 

## 3. 利用微元法求引力与压力

有些物理应用问题并没有现成公式，可以利用微元法解决。基本思想都是“以不变代变”“以均匀代不均匀”。本段以求引力和水压力为例，说明微元法的应用。

【例 3.66】一质量为 m 的质点 B 位于质量为 M、长度为 l 的均匀细杆 OA 的延长线上，且与较近的端点 A 的距离为 a。试求：

(I) 细杆 OA 对质点 B 的引力;

(Ⅱ) 当质点 B 在 OA 的延长线上从距离 A 点  $ d_{1} $ 处移近至  $ d_{2} $ 处时，引力所做的功.

【分析】质量分别为  $ m_{1}, m_{2} $ 相距为 r 的两个质点间的引力大小为

 $$ F=k\frac{m_{1}m_{2}}{r^{2}}, $$ 

其中 k 为引力常数；引力的方向沿着两个质点间的连线方向。

解 (I) 以 O 为原点、 $ \overrightarrow{OA} $ 方向为 x 轴建立坐标系。在 x 轴上取小区间  $ [x, x + \mathrm{d}x] $，对应细杆的一小段，其质量为  $ \frac{M}{l} \mathrm{d}x $，与质点 B 间的引力大小为

 $$ \mathrm{d}F=k\frac{m\frac{M}{l}\mathrm{d}x}{(l+a-x)^{2}}=\frac{kMm}{l(l+a-x)^{2}}\mathrm{d}x, $$ 

其中 k 为引力常数。所以，细杆 OA 对质点 B 的引力大小为

 $$ F=\frac{kMm}{l}\int_{0}^{l}\frac{\mathrm{d}x}{(l+a-x)^{2}}=\frac{kMm}{a(l+a)}. $$ 

（Ⅱ）根据（I）的结果，有  $ F(x)=\frac{kMm}{x(l+x)} $ ，故引力所做的功为

 $$ W=\int_{d_{2}}^{d_{1}}F(x)\mathrm{d}x=\int_{d_{2}}^{d_{1}}\frac{kMm}{x(l+x)}\mathrm{d}x=\frac{kMm}{l}\ln\frac{d_{1}\left(d_{2}+l\right)}{d_{2}\left(d_{1}+l\right)}. $$ 

【例 3.67】 某闸门的形状与大小如图 3.4 所示，其中直线 l 为对称轴，闸门的上部为矩形 ABCD，下部由二次抛物线与线段 AB 所围成。当水面与闸门的上端相平时，欲使闸门的矩形部分承受的水压力与闸门的下部承受的水压力之比为 5:4，闸门矩形部分的高 h 应为多少米？

【分析】在液面下深度为 h 处，液体产生的压强 P 等

于深度 h 与液体比重  $ \gamma $ 的乘积： $ P = \gamma h (\gamma = \rho g) $，且同一点

的压强在各个方向均相等.

竖直薄板所受到的侧压力为 F = 压强  $ \times $ 面积.

解 如图 3.5 所示建立坐标系，则抛物线的方程为 y =  $ x^{2} $. 闸门的矩形部分承受的水压力

 $$ P_{1}=2\int_{1}^{1+h}\rho g(h+1-y)\mathrm{d}y=2\rho g\left[(h+1)y-\frac{1}{2}y^{2}\right]\bigg|_{1}^{1+h}=\rho gh^{2}, $$ 

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//b96cafd9-1664-425d-b515-7063481596af/markdown_2/imgs/img_in_image_box_702_296_914_562.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A27Z%2F-1%2F%2Ff2357ef52d2b811ec29934d69a51242fc8f43b297d98e4708114534829a76d37" alt="Image" width="19%" /></div>


<div style="text-align: center;"><div style="text-align: center;">图3.4</div> </div>


其中  $ \rho $ 为水的密度，g 为重力加速度。闸门的下部承受的水压力

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//b96cafd9-1664-425d-b515-7063481596af/markdown_2/imgs/img_in_image_box_125_685_334_940.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A27Z%2F-1%2F%2Fbc075554c75f7d6dc3ba682c48753374814cc0793ebb0fd8da9e6e850ce82ace" alt="Image" width="19%" /></div>


 $$ \begin{align*}P_{2}&=2\int_{0}^{1}\rho g(h+1-y)\sqrt{y}\mathrm{d}y=2\rho g\left[\frac{2}{3}(h+1)y^{\frac{3}{2}}-\frac{2}{5}y^{\frac{5}{2}}\right]\bigg|_{0}^{1}\\&=4\rho g\left(\frac{1}{3}h+\frac{2}{15}\right).\end{align*} $$ 

<div style="text-align: center;"><div style="text-align: center;">图3.5</div> </div>


由题意知  $ \frac{P_{1}}{P_{2}}=\frac{5}{4} $，即

 $$ \frac{h^{2}}{4\left(\frac{1}{3}h+\frac{2}{15}\right)}=\frac{5}{4}. $$ 

解之得  $ h=2, h=-\frac{1}{3} $（舍去），故 h=2，即闸门矩形部分的高应为 2m.

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//b96cafd9-1664-425d-b515-7063481596af/markdown_2/imgs/img_in_image_box_125_1061_169_1102.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A27Z%2F-1%2F%2F60b9cf8d134eb4a7467a469f8571a1fa58f611402206139f7f050513ce811e11" alt="Image" width="4%" /></div>


#### 题型七、积分不等式的证明

积分不等式的证明是应用微积分学的一个重要方面，也是数学竞赛常考题型。不等式的种类繁多，证明方法难易悬殊，所用技巧各异，没有一个统一的处理方法。但是，相当广泛的一类不等式都可利用微分法和积分法给予论证，有些不等式若采用幂级数方法证明亦行之有效，简捷明了。这里，我们集中讨论与定积分有关的不等式的证明。

1\. 利用微分法证明

【例 3.68】证明：当  $ 0 \leqslant a \leqslant 1 $ 时， $ \int_{0}^{a}(1-x^{2})^{\frac{5}{2}}\mathrm{d}x \geqslant \frac{5a\pi}{32} $

【分析】若设  $ f(a)=\int_{0}^{a}\left(1-x^{2}\right)^{\frac{5}{2}}\mathrm{d}x-\frac{5a\pi}{32} $，则所证不等式即  $ f(a)\geqslant0(0\leqslant a\leqslant1) $，换言之，即不存在  $ \xi\in[0,1] $，使得  $ f(\xi)<0 $。我们采用反证法证明之。

证 构造辅助函数  $ f(a)=\int_{0}^{\pi}\left(1-x^{2}\right)^{\frac{5}{2}}\mathrm{d}x-\frac{5a\pi}{32} $，则  $ f(0)=0 $，且  $ f(a) $ 在  $ [0,1] $ 上存在二阶导数：

 $$ f^{\prime}(a)=\left(1-a^{2}\right)^{\frac{5}{2}}-\frac{5\pi}{32},\quad f^{\prime\prime}(a)=-5a\left(1-a^{2}\right)^{\frac{3}{2}}. $$ 

利用变量代换  $ x = \sin t $，容易求得

 $$ f(1)=\int_{0}^{1}\left(1-x^{2}\right)^{\frac{5}{2}}\mathrm{d}x-\frac{5\pi}{32}=\int_{0}^{\frac{\pi}{2}}\cos^{6}t\mathrm{d}t-\frac{5\pi}{32}=\frac{5}{6}\cdot\frac{3}{4}\cdot\frac{1}{2}\cdot\frac{\pi}{2}-\frac{5\pi}{32}=0. $$ 

若假设存在  $ \xi \in [0,1] $，使得  $ f(\xi) < 0 $，则由  $ f(0) = f(1) = 0 $ 可知  $ \xi \in (0,1) $。故  $ f(a) $ 在闭区间  $ [0,1] $ 上的最小值  $ f(a_0) $ 只能在  $ (0,1) $ 内取得，即  $ a_0 \in (0,1) $， $ f(a_0) $ 也是  $ f(a) $ 的极小值，从而  $ f''(a_0) \geq 0 $。此与  $ f''(a) < 0 $ ( $ 0 < a < 1 $) 矛盾，故假设不成立。

因此，对于任意  $ a \in [0,1] $， $ f(a) \geqslant 0 $，即  $ \int_{0}^{a} (1 - x^{2})^{\frac{5}{2}} \mathrm{d}x \geqslant \frac{5a\pi}{32} $.

【例 3.69】(第八届全国初赛题, 2016) 设函数  $ f(x) $ 在区间  $ [0,1] $ 上可导,  $ f(0)=0 $, 且当  $ x\in(0,1) $ 时,  $ 0<f'(x)<1 $. 试证: 当  $ a\in(0,1) $ 时,  $ \left(\int_{0}^{a}f(x)dx\right)^{2}>\int_{0}^{a}f^{3}(x)dx $.

证 设  $ F(x)=\left(\int_{0}^{x}f(t)\mathrm{d}t\right)^{2}-\int_{0}^{x}f^{3}(t)\mathrm{d}t $，则  $ F(x) $ 在  $ [0,1] $ 上可导， $ F(0)=0 $，且

 $$ F^{\prime}(x)=2f(x)\int_{0}^{x}f(t)\mathrm{d}t-f^{3}(x)=f(x)G(x), $$ 

其中  $ G(x)=2\int_{0}^{x}f(t)dt-f^{2}(x) $.

因为  $ f(x) $ 在  $ [0,1] $ 上严格单增，所以当 x > 0 时， $ f(x) > f(0) = 0 $。因此，当  $ x \in (0,1) $ 时，有

 $$ G^{\prime}(x)=2f(x)-2f(x)f^{\prime}(x)=2f(x)\left[1-f^{\prime}(x)\right]>0. $$ 

故 G(x) 在 [0,1] 上严格单增，所以当 x>0 时， $ G(x)>G(0)=0 $，从而有  $ F'(x)>0 $。

于是，当  $ a \in (0,1) $ 时， $ F(a) > F(0) = 0 $，即  $ \left(\int_{0}^{a} f(x) \, dx\right)^{2} > \int_{0}^{a} f^{3}(x) \, dx $.

【例 3.70】设  $ f(x) $ 在  $ [0,1] $ 上有连续二阶导数，且  $ f''(x)<0, f(0)=f(1)=0 $. 证明：

 $$ \int_{0}^{1}\left|\frac{f^{\prime\prime}(x)}{f(x)}\right|\mathrm{d}x>4. $$ 

证 因为  $ f''(x) < 0 $，所以  $ f(x) $ 在  $ [0,1] $ 上是凸函数，即曲线  $ y = f(x) $ 凸向上，亦即该曲线上任一点的纵坐标都大于连接其端点  $ A(0,f(0)) $ 与  $ B(1,f(1)) $ 的线段上对应点的纵坐标。由题设  $ f(0) = f(1) = 0 $ 可知，线段 AB 位于 x 轴上，其上任一点的纵坐标 y = 0。故对于任意  $ x \in (0,1) $， $ f(x) > 0 $。

因为函数  $ f(x) $ 在  $ [0,1] $ 上连续，所以  $ f(x) $ 在  $ [0,1] $ 上必存在最大值。设  $ f(a) $ 是  $ f(x) $ 在  $ [0,1] $ 上的最大值，则  $ f(a) > 0 $，且  $ a \in (0,1) $。在  $ [0,a] $ 与  $ [a,1] $ 上分别利用 Lagrange 中值定理，存在  $ \xi \in (0,a) $ 以及  $ \eta \in (a,1) $，使

 $$ f(a)-f(0)=f^{\prime}(\xi)(a-0),\quad f(1)-f(a)=f^{\prime}(\eta)(1-a), $$ 

即  $ f'(\xi)=\frac{f(a)}{a} $,  $ f'(\eta)=-\frac{f(a)}{1-a} $. 故

 $$ \begin{align*}\int_{0}^{1}\left|\frac{f^{\prime\prime}(x)}{f(x)}\right|\mathrm{d}x&>\frac{1}{f(a)}\int_{\xi}^{\eta}\left|f^{\prime\prime}(x)\right|\mathrm{d}x\geqslant-\frac{1}{f(a)}\int_{\xi}^{\eta}f^{\prime\prime}(x)\mathrm{d}x\\&=\frac{1}{f(a)}\left[f^{\prime}(\xi)-f^{\prime}(\eta)\right]=\frac{1}{f(a)}\left[\frac{f(a)}{a}+\frac{f(a)}{1-a}\right]\\&=\frac{1}{a}+\frac{1}{1-a}=\frac{1}{a(1-a)}\geqslant4.\end{align*} $$ 

【注】本例综合考察连续函数的性质、凸曲线的特征、Lagrange中值定理以及定积分的性质等知识点，并且还需确定二次函数 $ x(1-x) $在区间 $ [0,1] $上的最大值.

【例 3.71】设  $ f(x) $ 二阶可导，且  $ f''(x) \geqslant 0, u(t) $ 为任一连续函数，a > 0. 证明

 $$ \frac{1}{a}\int_{0}^{a}f[u(t)]\mathrm{d}t\geqslant f\left[\frac{1}{a}\int_{0}^{a}u(t)\mathrm{d}t\right]. $$ 

证 对任意  $ x_{0}, x \in (-\infty, +\infty) $，利用 Taylor 公式，存在介于  $ x_{0} $ 与 x 之间的  $ \xi $，使得

 $$ f(x)=f\left(x_{0}\right)+f^{\prime}\left(x_{0}\right)\left(x-x_{0}\right)+\frac{1}{2}f^{\prime\prime}(\xi)\left(x-x_{0}\right)^{2}. $$ 

根据题设条件  $ f''(x) \geqslant 0 $，得

 $$ f(x)\geqslant f\left(x_{0}\right)+f^{\prime}\left(x_{0}\right)\left(x-x_{0}\right). $$ 

取  $ x_{0}=\frac{1}{a}\int_{0}^{a}u(t)\mathrm{d}t,x=u(t) $，代入上式，则有

 $$ f[u(t)]\geqslant f\left[\frac{1}{a}\int_{0}^{a}u(t)\mathrm{d}t\right]+f^{\prime}\left(x_{0}\right)\left[u(t)-x_{0}\right]. $$ 

对上式两端从0到a积分，得

 $$ \begin{align*}\int_{0}^{a}f(u(t))\mathrm{d}t&\geq a f\left(\frac{1}{a}\int_{0}^{a}u(t)\mathrm{d}t\right)+f^{\prime}\left(x_{0}\right)\left(\int_{0}^{a}u(t)\mathrm{d}t-a x_{0}\right)\\&=a f\left(\frac{1}{a}\int_{0}^{a}u(t)\mathrm{d}t\right),\end{align*} $$ 

亦即  $ \frac{1}{a}\int_{0}^{a}f(u(t))\mathrm{d}t\geqslant f\left(\frac{1}{a}\int_{0}^{a}u(t)\mathrm{d}t\right) $.

【注】本例即积分形式的 Jensen（詹森）不等式，取  $ f(x)=\ln x, a=1 $，则是第十届（2018年）全国初赛题（详见例3.90）：设  $ u(x) $ 在  $ [0,1] $ 上连续，且  $ u(x)>0 $，则

 $$ \ln\int_{0}^{1}u(x)\mathrm{d}x\geqslant\int_{0}^{1}\ln u(x)\mathrm{d}x. $$ 

## 2. 利用定积分的性质

这种方法是先找出被积函数满足的不等式，再利用定积分的不等式性质：比较定理、估值定理、函数绝对积分的不等式等，即可得所证不等式，于是定积分不等式的证明就归结为函数不等式的证明.

【例 3.72】证明： $ \frac{\sqrt{3}}{2}\pi<\int_{0}^{1}\sqrt{\frac{x^{2}-x+1}{x-x^{2}}}\mathrm{d}x<\pi. $

证 当  $ x \in [0,1] $ 时， $ \frac{3}{4} \leqslant x^{2} - x + 1 = \left(x - \frac{1}{2}\right)^{2} + \frac{3}{4} \leqslant 1 $ 。所以

 $$ \frac{\sqrt{3}}{2}\int_{0}^{1}\frac{\mathrm{d}x}{\sqrt{x-x^{2}}}\leqslant\int_{0}^{1}\sqrt{\frac{x^{2}-x+1}{x-x^{2}}}\mathrm{d}x\leqslant\int_{0}^{1}\frac{\mathrm{d}x}{\sqrt{x-x^{2}}}. $$ 

作变量代换： $ x - \frac{1}{2} = \frac{1}{2} \sin t $，则  $ \int_{0}^{1} \frac{dx}{\sqrt{x - x^{2}}} = \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}} \frac{\frac{1}{2} \cos t \, dt}{\frac{1}{2} \cos t} = \pi $。代入上式，即得所证不等式.

【例 3.73】设  $ f(x) $ 在区间  $ [0,1] $ 上连续，且对任意  $ x \in [0,1] $，有  $ 0 < m \leqslant f(x) \leqslant M $。证明 Kantorovich（康托洛维奇）不等式：

 $$ 1\leqslant\int_{0}^{1}f(x)\mathrm{d}x\int_{0}^{1}\frac{\mathrm{d}x}{f(x)}\leqslant\frac{(M+m)^{2}}{4Mm}. $$ 

证 利用 Cauchy 积分不等式 (本章例 3.79), 得

 $$ \int_{0}^{1}f(x)\mathrm{d}x\int_{0}^{1}\frac{\mathrm{d}x}{f(x)}\geqslant\left(\int_{0}^{1}\sqrt{f(x)}\sqrt{\frac{1}{f(x)}}\mathrm{d}x\right)^{2}=1. $$ 

另一方面，由  $ m \leqslant f(x) \leqslant M $ 得  $ [f(x) - m][f(x) - M] \leqslant 0 $，即  $ f(x) + \frac{Mm}{f(x)} \leqslant M + m $，所以

 $$ \int_{0}^{1}f(x)\mathrm{d}x+Mm\int_{0}^{1}\frac{\mathrm{d}x}{f(x)}\leqslant M+m. $$ 

而  $ \int_{0}^{1}f(x)\mathrm{d}x+Mm\int_{0}^{1}\frac{\mathrm{d}x}{f(x)}\geqslant2\sqrt{Mm\int_{0}^{1}f(x)\mathrm{d}x\int_{0}^{1}\frac{\mathrm{d}x}{f(x)}} $，代入上式，即证得右边的不等式.

【注】特别地，考虑 m = 1, M = 3，即第十届全国初赛题（2018年），详见本章

【注】特别地，考虑 m=1,M=3，即第十届全国初赛题（2018年），详见本章例3.97.

3. 利用定积分的几何意义

【例 3.74】设函数 f 在  $ [a, b] $ 上连续，且对任意的  $ t \in [0,1] $ 以及任意的  $ x_1, x_2 \in [a, b] $ 恒满足不等式  $ f(tx_1 + (1 - t)x_2) \leq tf(x_1) + (1 - t)f(x_2) $. 证明：

 $$ f\left(\frac{a+b}{2}\right)\leqslant\frac{1}{b-a}\int_{a}^{b}f(x)\mathrm{d}x\leqslant\frac{f(a)+f(b)}{2}. $$ 

【分析】从几何上看，本题所设条件是：连续曲线  $ y = f(x) $ 是向下凸的，如图 3.6，因而右边的不等式比较容易证明．而对于左边的不等式，即矩形  $ aCDb $ 的面积不超过曲边梯形  $ aAQBb $ 的面积，则需将定积分  $ \int_{a}^{b} f(x) \, dx $ 分成两部分  $ \int_{a}^{\frac{a+b}{2}} f(x) \, dx $ 与  $ \int_{\frac{a+b}{2}}^{b} f(x) \, dx $，并设法“叠加”成一项，以体现几何上的“割补”措施.

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//0e14b802-b54a-4334-9d29-036a466bf6e2/markdown_2/imgs/img_in_chart_box_628_719_920_967.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A27Z%2F-1%2F%2Fe844c477dd54da8515f396cc0c560e1858fbe9a1fc81e6d48a0e6c00195425eb" alt="Image" width="27%" /></div>


<div style="text-align: center;"><div style="text-align: center;">图3.6</div> </div>


证  $ x = ta + (1 - t)b $，则  $ \mathrm{d}x = (a - b)\mathrm{d}t $，且当 x = a 时，t = 1；当 x = b 时，t = 0。故

 $$ \begin{align*}\int_{a}^{b}f(x)\mathrm{d}x&=(b-a)\int_{0}^{1}f(ta+(1-t)b)\mathrm{d}t\\&\leqslant(b-a)\int_{0}^{1}[tf(a)+(1-t)f(b)]\mathrm{d}t\\&=(b-a)\frac{f(a)+f(b)}{2}.\end{align*} $$ 

但另一方面，因为

 $$ \int_{a}^{b}f(x)\mathrm{d}x=\int_{a}^{\frac{a+b}{2}}f(x)\mathrm{d}x+\int_{\frac{a+b}{2}}^{b}f(x)\mathrm{d}x, $$ 

对后一积分作变量代换： $ x = a + b - t $，得

 $$ \begin{aligned}\int_{\frac{a+b}{2}}^{b}f(x)\mathrm{d}x&=-\int_{\frac{a+b}{2}}^{a}f(a+b-t)\mathrm{d}t\\&=\int_{a}^{\frac{a+b}{2}}f(a+b-t)\mathrm{d}t.\end{aligned} $$ 

所以

 $$ \begin{align*}\int_{a}^{b}f(x)\mathrm{d}x&=\int_{a}^{\frac{a+b}{2}}[f(x)+f(a+b-x)]\mathrm{d}x\\&\geqslant2\int_{a}^{\frac{a+b}{2}}f\left(\frac{x+(a+b-x)}{2}\right)\mathrm{d}x\\&=2\int_{a}^{\frac{a+b}{2}}f\left(\frac{a+b}{2}\right)\mathrm{d}x=(b-a)f\left(\frac{a+b}{2}\right).\end{align*} $$ 

因此，有  $ f\left(\frac{a+b}{2}\right)\leqslant\frac{1}{b-a}\int_{a}^{b}f(x)\mathrm{d}x\leqslant\frac{f(a)+f(b)}{2} $

利用定积分的几何意义也可证明代数不等式和函数不等式.

【例 3.75】当 a, b > 1 时，证明： $ ab \leqslant e^{a-1} + b \ln b $，并指出何时等号成立.

证 根据定积分的几何意义 (图 3.7), 有

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//0e14b802-b54a-4334-9d29-036a466bf6e2/markdown_3/imgs/img_in_image_box_125_771_414_992.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A28Z%2F-1%2F%2Fd7c1808ca40e238cfdea5cc28eecaa05c753dbb3d77369fe641e8031518d3a8e" alt="Image" width="27%" /></div>


<div style="text-align: center;"><div style="text-align: center;">图3.7</div> </div>


 $$ S_{1}=\int_{0}^{a-1}\mathrm{e}^{y}\mathrm{d}y=\mathrm{e}^{a-1}-1, $$ 

 $$ S_{2}=\int_{1}^{b}\ln x\mathrm{d}x=b(\ln b-1)+1. $$ 

故  $ (a-1)b \leqslant S_{1} + S_{2} = e^{a-1} + b \ln b - b $，即

 $$ a b\leqslant\mathrm{e}^{a-1}+b\ln b. $$ 

显然，当且仅当  $ a = \ln b + 1 $ 时等号成立.

【注】本题也可构造辅助函数  $ f(x)=bx-\mathrm{e}^{x-1}-b\ln b $ (b>1)，证明  $ f(\ln b+1)=0 $ 是  $ f(x) $ 在  $ (1,+\infty) $ 上的最大值，故当 a>1 时， $ f(a)\leq0 $，即  $ ab\leq\mathrm{e}^{a-1}+b\ln b $.

【例 3.76】证明：对于任意正整数 n，有  $ \frac{2}{3}n\sqrt{n}<\sum_{k=1}^{n}\sqrt{k}<\left(\frac{2}{3}n+\frac{1}{2}\right)\sqrt{n} $

证 对于正整数 k，显然有  $ \sqrt{k} > \int_{k-1}^{k} \sqrt{x} \, \mathrm{d}x $ 。所以

 $$ \sum_{k=1}^{n}\sqrt{k}>\sum_{k=1}^{n}\int_{k-1}^{k}\sqrt{x}\mathrm{d}x=\int_{0}^{n}\sqrt{x}\mathrm{d}x=\frac{2}{3}n\sqrt{n}. $$ 

另一方面，注意到  $ \sqrt{x} $ 是上凸函数，故根据定积分的几何意义得

 $$ \frac{1}{2}(\sqrt{k-1}+\sqrt{k})<\int_{k-1}^{k}\sqrt{x}\mathrm{d}x, $$ 

即梯形面积小于曲边梯形面积. 因此有

 $$ \begin{aligned}\sum_{k=1}^{n}\sqrt{k}&=\frac{1}{2}\sum_{k=1}^{n}(\sqrt{k-1}+\sqrt{k})+\frac{1}{2}\sqrt{n}<\sum_{k=1}^{n}\int_{k-1}^{k}\sqrt{x}\mathrm{d}x+\frac{1}{2}\sqrt{n}\\&=\int_{0}^{n}\sqrt{x}\mathrm{d}x+\frac{1}{2}\sqrt{n}=\frac{2}{3}n\sqrt{n}+\frac{1}{2}\sqrt{n}.\end{aligned} $$ 

4. 利用积分中值定理

【例 3.77】设 a > 0,  $ f'(x) $ 在  $ [0, a] $ 上连续，则

 $$ |f(0)|\leqslant\frac{1}{a}\int_{0}^{a}|f(x)|\mathrm{d}x+\int_{0}^{a}|f^{\prime}(x)|\mathrm{d}x. $$ 

证 根据积分中值定理, 存在  $ \xi \in [0, a] $, 使  $ \int_{0}^{a} |f(x)| \, \mathrm{d}x = a |f(\xi)| $. 而

 $$ f(\xi)-f(0)=\int_{0}^{\xi}f^{\prime}(x)\mathrm{d}x, $$ 

 $$ |f(0)|\leqslant|f(\xi)|+\left|\int_{0}^{\xi}f^{\prime}(x)\mathrm{d}x\right|\leqslant\frac{1}{a}\int_{0}^{a}|f(x)|\mathrm{d}x+\int_{0}^{a}|f^{\prime}(x)|\mathrm{d}x. $$ 

【例 3.78】设  $ f(x) $ 为  $ [0,1] $ 上的连续非负单调减函数，证明：对于  $ 0 < \alpha < \beta \leq 1 $，有

 $$ \int_{0}^{\alpha}f(x)\mathrm{d}x\geqslant\frac{\alpha}{\beta}\int_{\alpha}^{\beta}f(x)\mathrm{d}x. $$ 

证 由定积分中值定理，有

 $$ \int_{0}^{\alpha}f(x)\mathrm{d}x=\alpha f\left(\xi_{1}\right),\quad\int_{\alpha}^{\beta}f(x)\mathrm{d}x=\left(\beta-\alpha\right)f\left(\xi_{2}\right)\quad\left(0\leqslant\xi_{1}\leqslant\alpha\leqslant\xi_{2}\leqslant\beta\right). $$ 

因  $ f(x) $ 非负单调减，故当  $ \xi_{1} \leqslant \xi_{2} $ 时， $ f\left(\xi_{1}\right) \geqslant f\left(\xi_{2}\right) \geqslant 0 $，从而有

 $$ \beta\alpha f\left(\xi_{1}\right)\geqslant\alpha(\beta-\alpha)f\left(\xi_{2}\right),\quad\beta\int_{0}^{\alpha}f(x)\mathrm{d}x\geqslant\alpha\int_{a}^{\beta}f(x)\mathrm{d}x, $$ 

即  $ \int_{0}^{\alpha}f(x)\mathrm{d}x\geqslant\frac{\alpha}{\beta}\int_{\alpha}^{\beta}f(x)\mathrm{d}x. $

5. 利用重积分法

【例 3.79】 证明 Cauchy 积分不等式：

 $$ \left[\int_{a}^{b}f(x)g(x)\mathrm{d}x\right]^{2}\leqslant\int_{a}^{b}f^{2}(x)\mathrm{d}x\int_{a}^{b}g^{2}(x)\mathrm{d}x, $$ 

其中  $ f(x), g(x) $ 均为  $ [a, b] $ 上的连续函数.

证 设 D:  $ a \leq x \leq b $,  $ a \leq y \leq b $, 则

 $$ \begin{align*}\left[\int_{a}^{b}f(x)g(x)\mathrm{d}x\right]^{2}&=\int_{a}^{b}f(x)g(x)\mathrm{d}x\int_{a}^{b}f(y)g(y)\mathrm{d}y\\&=\iint\limits_{D}f(x)g(y)\cdot f(y)g(x)\mathrm{d}x\mathrm{d}y\\&\leqslant\iint\limits_{D}\frac{1}{2}\left[f^{2}(x)g^{2}(y)+f^{2}(y)g^{2}(x)\right]\mathrm{d}x\mathrm{d}y\\&=\frac{1}{2}\iint\limits_{D}f^{2}(x)g^{2}(y)\mathrm{d}x\mathrm{d}y+\frac{1}{2}\iint\limits_{D}f^{2}(y)g^{2}(x)\mathrm{d}x\mathrm{d}y\\&=\frac{1}{2}\int_{a}^{b}f^{2}(x)\mathrm{d}x\int_{a}^{b}g^{2}(y)\mathrm{d}y+\frac{1}{2}\int_{a}^{b}f^{2}(y)\mathrm{d}y\int_{a}^{b}g^{2}(x)\mathrm{d}x\\&=\frac{1}{2}\int_{a}^{b}f^{2}(x)\mathrm{d}x\int_{a}^{b}g^{2}(x)\mathrm{d}x+\frac{1}{2}\int_{a}^{b}f^{2}(x)\mathrm{d}x\int_{a}^{b}g^{2}(x)\mathrm{d}x\\&=\int_{a}^{b}f^{2}(x)\mathrm{d}x\int_{a}^{b}g^{2}(x)\mathrm{d}x.\end{align*} $$ 

【注】Cauchy 积分不等式在数学竞赛中往往被用来证明其他积分不等式.

【例 3.80】证明： $ \frac{\pi}{4}\left(1-\frac{1}{\mathrm{e}}\right)<\left(\int_{0}^{1}\mathrm{e}^{-x^{2}}\mathrm{d}x\right)^{2}<\frac{\pi}{4}\left(1-\mathrm{e}^{-\frac{4}{\pi}}\right) $.

证 记  $ D=\{(x,y)\mid0\leqslant x\leqslant1,0\leqslant y\leqslant1\} $，而  $ D_{1}=\{(x,y)\in D\mid x^{2}+y^{2}\leqslant1,x\geqslant0,y\geqslant0\} $，则

 $$ \begin{align*}\left(\int_{0}^{1}\mathrm{e}^{-x^{2}}\mathrm{d}x\right)^{2}&=\int_{0}^{1}\mathrm{e}^{-x^{2}}\mathrm{d}x\int_{0}^{1}\mathrm{e}^{-y^{2}}\mathrm{d}y=\iint\limits_{D}\mathrm{e}^{-\left(x^{2}+y^{2}\right)}\mathrm{d}\sigma\\&>\iint\limits_{D_{1}}\mathrm{e}^{-\left(x^{2}+y^{2}\right)}\mathrm{d}\sigma=\int_{0}^{\frac{\pi}{2}}\mathrm{d}\theta\int_{0}^{1}\mathrm{e}^{-r^{2}}r\mathrm{d}r\\&=\frac{\pi}{4}\left(1-\frac{1}{\mathrm{e}}\right).\end{align*} $$ 

另一方面, 记  $ D_{\rho}=\left\{(x,y)|x^{2}+y^{2}\leqslant\rho^{2},x\geqslant0,y\geqslant0\right\} $, 其中  $ \rho>0 $, 则

 $$ \iint\limits_{D_{\rho}}\mathrm{e}^{-\left(x^{2}+y^{2}\right)}\mathrm{d}\sigma=\int_{0}^{\frac{\pi}{2}}\mathrm{d}\theta\int_{0}^{\rho}\mathrm{e}^{-r^{2}}r\mathrm{d}r=\frac{\pi}{4}\left(1-\mathrm{e}^{-\rho^{2}}\right) $$ 

取  $ \rho=\frac{2}{\sqrt{\pi}} $，圆弧  $ x^{2}+y^{2}=\frac{4}{\pi} $ 将区域 D 划分成 I 与 II 两部分， $ D_{\rho} $ 与 D 的非重叠部分记为 Ⅲ 与 Ⅳ (图 3.8)，注意到区域 Ⅱ 与 Ⅲ ∪ Ⅳ 的面积相等，记这个面积为 A，所以

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//70ac1cc4-d343-4a98-96fc-cadfbafda158/markdown_2/imgs/img_in_image_box_646_171_928_475.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A27Z%2F-1%2F%2Ff031a211f5148bc64100e8948e2eccb9a29cfe211e90bf9dc703141cd550811c" alt="Image" width="26%" /></div>


<div style="text-align: center;"><div style="text-align: center;">图3.8</div> </div>


 $$ \iint\limits_{\mathbb{I}}\mathrm{e}^{-\left(x^{2}+y^{2}\right)}\mathrm{d}\sigma\leqslant A\mathrm{e}^{-\rho^{2}}\leqslant\iint\limits_{\mathbb{M}\cup\mathbb{N}}\mathrm{e}^{-\left(x^{2}+y^{2}\right)}\mathrm{d}\sigma. $$ 

于是，有

 $$ \begin{align*}\iint\limits_{D}\mathrm{e}^{-\left(x^{2}+y^{2}\right)}\mathrm{d}\sigma&=\iint\limits_{\mathbb{I}}\mathrm{e}^{-\left(x^{2}+y^{2}\right)}\mathrm{d}\sigma+\iint\limits_{\mathbb{I}}\mathrm{e}^{-\left(x^{2}+y^{2}\right)}\mathrm{d}\sigma\\&<\iint\limits_{\mathbb{I}}\mathrm{e}^{-\left(x^{2}+y^{2}\right)}\mathrm{d}\sigma+\iint\limits_{\mathbb{M}\cup\mathbb{N}}\mathrm{e}^{-\left(x^{2}+y^{2}\right)}\mathrm{d}\sigma\\&=\iint\limits_{D_{\rho}}\mathrm{e}^{-\left(x^{2}+y^{2}\right)}\mathrm{d}\sigma=\frac{\pi}{4}\left(1-\mathrm{e}^{-\frac{4}{\pi}}\right).\end{align*} $$ 

## 6. 利用幂级数法

这种方法的主要特点是先利用幂级数得到相关的函数不等式，再利用定积分性质证明积分不等式.

设函数  $ f(x) $ 可以展开为 x - x_{0} 的幂级数，即  $ f(x) = \sum_{n=0}^{\infty} a_{n}(x - x_{0})^{n} $，又设  $ S_{n}(x) $ 和  $ R_{n}(x) $ 分别为级数的前 n 项和与余项：

 $$ S_{n}(x)=\sum_{k=0}^{n}a_{k}\left(x-x_{0}\right)^{k},\quad R_{n}(x)=\sum_{k=n+1}^{\infty}a_{n}\left(x-x_{0}\right)^{k}, $$ 

则  $ f(x)=S_{n}(x)+R_{n}(x) $.

如果  $ R_{n}(x)<0 $ , 那么  $ f(x)<S_{n}(x) $; 如果  $ R_{n}(x)>0 $ , 那么  $ f(x)>S_{n}(x) $.

特别地，如果  $ \sum_{n=0}^{\infty}a_{n}(x-x_{0})^{n} $ 在其收敛域内是交错级数， $ \left|a_{n}(x-x_{0})^{n}\right|>\left|a_{n+1}(x-x_{0})^{n+1}\right| $ 且  $ \lim_{n\to\infty}a_{n}(x-x_{0})^{n}=0 $，那么余项  $ R_{n}(x) $ 与其第一项  $ a_{n+1}(x-x_{0})^{n+1} $ 具有相同的符号.

【例 3.81】证明： $ \frac{3}{5}<\int_{0}^{1}e^{-x^{2}}dx<\frac{4}{5} $.

证 根据  $ e^{-x^2} $ 的幂级数展开式易知，对于  $ x \in [0,1] $，有

 $$ 1-x^{2}+\frac{x^{4}}{2!}-\frac{x^{6}}{3!}\leqslant\mathrm{e}^{-x^{2}}\leqslant1-x^{2}+\frac{x^{4}}{2!}, $$ 

其中等号仅当 x=0 时成立. 根据定积分的性质, 得

 $$ \int_{0}^{1}\left(1-x^{2}+\frac{x^{4}}{2!}-\frac{x^{6}}{3!}\right)\mathrm{d}x<\int_{0}^{1}\mathrm{e}^{-x^{2}}\mathrm{d}x<\int_{0}^{1}\left(1-x^{2}+\frac{x^{4}}{2!}\right)\mathrm{d}x. $$ 

因为

 $$ \int_{0}^{1}\left(1-x^{2}+\frac{x^{4}}{2!}-\frac{x^{6}}{3!}\right)\mathrm{d}x=1-\frac{1}{3}+\frac{1}{10}-\frac{1}{42}=\frac{26}{35}>\frac{3}{5}, $$ 

 $$ \int_{0}^{1}\left(1-x^{2}+\frac{x^{4}}{2!}\right)\mathrm{d}x=1-\frac{1}{3}+\frac{1}{10}=\frac{23}{30}<\frac{4}{5}, $$ 

所以  $ \frac{3}{5} < \int_{0}^{1} e^{-x^{2}} \, \mathrm{d}x < \frac{4}{5} $.

【例 3.82】证明： $ \int_{0}^{1}\frac{\sin x}{\sqrt{1-x^{2}}}dx<\int_{0}^{1}\frac{\cos x}{\sqrt{1-x^{2}}}dx<\int_{0}^{1}\frac{\tan x}{\sqrt{1-x^{2}}}dx. $

证 分别记  $ I_{1}=\int_{0}^{1}\frac{\sin x}{\sqrt{1-x^{2}}}dx,I_{2}=\int_{0}^{1}\frac{\cos x}{\sqrt{1-x^{2}}}dx,I_{3}=\int_{0}^{1}\frac{\tan x}{\sqrt{1-x^{2}}}dx. $

首先，对第一个积分作变量代换： $ x = \sin t $，再利用不等式： $ \sin t < t \left(0 < t \leqslant \frac{\pi}{2}\right) $，可得

 $$ I_{1}=\int_{0}^{\frac{\pi}{2}}\sin(\sin t)\mathrm{d}t<\int_{0}^{\frac{\pi}{2}}\sin t\mathrm{d}t=1. $$ 

其次，利用幂级数  $ \cos x = 1 - \frac{x^{2}}{2!} + \frac{x^{4}}{4!} - \cdots + (-1)^{n} \frac{x^{2n}}{(2n)!} + \cdots (-\infty < x < +\infty) $，有

 $$ 1-\frac{x^{2}}{2!}<\cos x<1-\frac{x^{2}}{2!}+\frac{x^{4}}{4!}, $$ 

于是，有

 $$ \int_{0}^{1}\frac{1-\frac{x^{2}}{2!}}{\sqrt{1-x^{2}}}\mathrm{d}x<I_{2}<\int_{0}^{1}\frac{1-\frac{x^{2}}{2!}+\frac{x^{4}}{4!}}{\sqrt{1-x^{2}}}\mathrm{d}x. $$ 

由于

 $$ \int_{0}^{1}\frac{1-\frac{x^{2}}{2!}}{\sqrt{1-x^{2}}}\mathrm{d}x=\frac{1}{2}\int_{0}^{1}\left(\frac{1}{\sqrt{1-x^{2}}}+\sqrt{1-x^{2}}\right)\mathrm{d}x=\frac{1}{2}\left(\frac{\pi}{2}+\frac{\pi}{4}\right)=\frac{3\pi}{8}, $$ 

 $$ \frac{1}{4!}\int_{0}^{1}\frac{x^{4}}{\sqrt{1-x^{2}}}\mathrm{d}x\xlongequal{x=\sin t}\frac{1}{24}\int_{0}^{\frac{\pi}{2}}\sin^{4}t\mathrm{d}t=\frac{\pi}{128}, $$ 

所以

 $$ I_{1}<1<\frac{3\pi}{8}<I_{2}<\frac{3\pi}{8}+\frac{\pi}{128}=\frac{49\pi}{128}<1.203. $$ 

最后，利用  $ \tan x $ 的幂级数展开式，易知：当 0 < x < 1 时， $ \tan x > x + \frac{x^{3}}{3} $，所以

 $$ I_{3}>\int_{0}^{1}\frac{x+\frac{x^{3}}{3}}{\sqrt{1-x^{2}}}\mathrm{d}x\xlongequal{x=\sin t}\int_{0}^{\frac{\pi}{2}}\sin t\mathrm{d}t+\frac{1}{3}\int_{0}^{\frac{\pi}{2}}\sin^{3}t\mathrm{d}t=\frac{11}{9}>1.222>I_{2}. $$ 

### 3.3 真题选讲与点评

【例 3.83】（第九届全国初赛题，2017） 不定积分  $ \int \frac{\mathrm{e}^{-\sin x}\sin2x}{(1-\sin x)^2}\mathrm{d}x = $ ___.

【分析】注意到  $ \sin 2x = 2 \sin x \cos x $，作变量代换： $ t = \sin x $，原积分化为  $ 2 \int \frac{t e^{-t}}{(1-t)^2} dt $，再利用分部积分法求解.

解 原式  $ = 2 \int \frac{\mathrm{e}^{-\sin x} \sin x}{(1 - \sin x)^2} \mathrm{d}(\sin x) \xlongequal{\text{令 } t = \sin x}} 2 \int \frac{t \mathrm{e}^{-t}}{(1 - t)^2} \mathrm{d}t. $ 下面用两种方法计算.

（方法1）

 $$ \begin{align*}\int\frac{t\mathrm{e}^{-t}}{(1-t)^{2}}\mathrm{d}t&=\int t\mathrm{e}^{-t}\mathrm{d}\left(\frac{1}{1-t}\right)=t\mathrm{e}^{-t}\cdot\frac{1}{1-t}-\int\frac{1}{1-t}\mathrm{d}\left(t\mathrm{e}^{-t}\right)\\&=\frac{t\mathrm{e}^{-t}}{1-t}-\int\mathrm{e}^{-t}\mathrm{d}t=\frac{t\mathrm{e}^{-t}}{1-t}+\mathrm{e}^{-t}+C=\frac{\mathrm{e}^{-t}}{1-t}+C.\end{align*} $$ 

(方法2)

 $$ \begin{aligned}\int\frac{t\mathrm{e}^{-t}}{(1-t)^{2}}\mathrm{d}t&=\int\frac{(t-1+1)\mathrm{e}^{-t}}{(1-t)^{2}}\mathrm{d}t=-\int\frac{\mathrm{e}^{-t}}{1-t}\mathrm{d}t+\int\frac{\mathrm{e}^{-t}}{(1-t)^{2}}\mathrm{d}t\\&=-\int\frac{\mathrm{e}^{-t}}{1-t}\mathrm{d}t+\int\mathrm{e}^{-t}\mathrm{d}\left(\frac{1}{1-t}\right)\\&=-\int\frac{\mathrm{e}^{-t}}{1-t}\mathrm{d}t+\left(\frac{\mathrm{e}^{-t}}{1-t}+\int\frac{\mathrm{e}^{-t}}{1-t}\mathrm{d}t\right)\\&=\frac{\mathrm{e}^{-t}}{1-t}+C.\end{aligned} $$ 

因此，原式  $ = \frac{2\mathrm{e}^{-t}}{1-t} + C_{1} = \frac{2\mathrm{e}^{-\sin x}}{1-\sin x} + C_{1} $，其中  $ C_{1} = 2C $.

【例 3.84】(第五届全国初赛题, 2013) 设  $ f(x) $ 在  $ [a, b] $ 上具有连续导数,  $ \left|f(x)\right| \leqslant \pi $, 且  $ f'(x) \geqslant m > 0 $ ( $ a \leqslant x \leqslant b $, m 为常数), 证明:

 $$ \left|\int_{a}^{b}\sin f(x)\mathrm{d}x\right|\leqslant\frac{2}{m}. $$ 

证 因为  $ f'(x) \geqslant m > 0 $ ( $ a \leqslant x \leqslant b $)，所以  $ f(x) $ 在  $ [a, b] $ 上存在严格单调增加的反函数，设  $ x = g(y) $，则  $ 0 < g'(y) = \frac{1}{f'(x)} \leqslant \frac{1}{m} $.

记  $ A = f(a) $,  $ B = f(b) $，则由  $ \left|f(x)\right| \leqslant \pi $ 可知， $ -\pi \leqslant A < B \leqslant \pi $。作变量代换  $ x = g(y) $，则

 $$ \left|\int_{a}^{b}\sin f(x)\mathrm{d}x\right|=\left|\int_{A}^{B}g^{\prime}(y)\sin y\mathrm{d}y\right|\leqslant\frac{1}{m}\int_{0}^{\pi}\sin y\mathrm{d}y=\frac{2}{m}. $$ 

【例 3.85】（第八届全国决赛题，2017） $ \sum_{n=1}^{100}n^{-\frac{1}{2}} $ 的整数部分为 ___.

解 令  $ S = \sum_{n=1}^{100} n^{-\frac{1}{2}} $，问题即求不超过 S 的最大整数 [S]。因为

 $$ S=1+\sum_{n=2}^{100}\int_{n-1}^{n}n^{-\frac{1}{2}}\mathrm{d}x<1+\sum_{n=2}^{100}\int_{n-1}^{n}x^{-\frac{1}{2}}\mathrm{d}x=1+\int_{1}^{100}x^{-\frac{1}{2}}\mathrm{d}x=19, $$ 

 $$ S=\sum_{n=1}^{100}\int_{n}^{n+1}n^{-\frac{1}{2}}\mathrm{d}x>\sum_{n=1}^{100}\int_{n}^{n+1}x^{-\frac{1}{2}}\mathrm{d}x=\int_{1}^{101}x^{-\frac{1}{2}}\mathrm{d}x=2(\sqrt{101}-1)>18, $$ 

所以[S]=18.

【例 3.86】（第一届全国决赛题，2010）已知函数  $ f(x) $ 在区间  $ \left(\frac{1}{4}, \frac{1}{2}\right) $ 内满足  $ f'(x) = \frac{1}{\sin^{3}x + \cos^{3}x} $，求  $ f(x) $.

解

 $$ \begin{aligned}f(x)&=\int\frac{1}{\sin^{3}x+\cos^{3}x}\mathrm{d}x=\int\frac{1}{(\sin x+\cos x)\left(\sin^{2}x+\cos^{2}x-\sin x\cos x\right)}\mathrm{d}x\\&=\int\frac{2\mathrm{d}x}{(\cos x+\sin x)\left[1+(\cos x-\sin x)^{2}\right]}\\&=\frac{2}{3}\int\frac{\mathrm{d}x}{(\cos x+\sin x)}+\frac{2}{3}\int\frac{(\cos x+\sin x)\mathrm{d}x}{1+(\cos x-\sin x)^{2}}\\&=\frac{\sqrt{2}}{3}\int\frac{\mathrm{d}x}{\sin\left(x+\frac{\pi}{4}\right)}+\frac{2}{3}\int\frac{\mathrm{d}(\sin x-\cos x)}{1+(\sin x-\cos x)^{2}}\\&=\frac{\sqrt{2}}{3}\ln\tan\left(\frac{x}{2}+\frac{\pi}{8}\right)+\frac{2}{3}\arctan(\sin x-\cos x)+C.\end{aligned} $$ 

【例 3.87】（第四届全国初赛题，2012）计算  $ \int_{0}^{+\infty}e^{-2x}|\sin x|dx $.

【分析】注意到  $ \left|\sin x\right| $ 是周期为  $ \pi $ 的周期函数，所以应考虑先计算有限个区间上的定积分，再利用广义积分的定义求解.

解 对任意 t > 0，必存在正整数 n，使得  $ n\pi < t \leq (n+1)\pi $，从而有

 $$ \int_{0}^{n\pi}\mathrm{e}^{-2x}|\sin x|\mathrm{d}x\leqslant\int_{0}^{t}\mathrm{e}^{-2x}|\sin x|\mathrm{d}x\leqslant\int_{0}^{(n+1)\pi}\mathrm{e}^{-2x}|\sin x|\mathrm{d}x. $$ 

由于

 $$ \begin{align*}\int_{0}^{n\pi}\mathrm{e}^{-2x}|\sin x|\mathrm{d}x&=\sum_{k=1}^{n}\int_{(k-1)\pi}^{k\pi}\mathrm{e}^{-2x}|\sin x|\mathrm{d}x=\sum_{k=1}^{n}\int_{(k-1)\pi}^{k\pi}(-1)^{k-1}\mathrm{e}^{-2x}\sin x\mathrm{d}x\\&=\left.\frac{1}{5}\sum_{k=1}^{n}(-1)^{k}\mathrm{e}^{-2x}(\cos x+2\sin x)\right|_{(k-1)\pi}^{k\pi}\\&=\frac{\mathrm{e}^{2\pi}+1}{5}\sum_{k=1}^{n}\mathrm{e}^{-2k\pi}=\frac{\mathrm{e}^{2\pi}+1}{5\left(\mathrm{e}^{2\pi}-1\right)}\left(1-\mathrm{e}^{-2n\pi}\right),\end{align*} $$ 

所以

 $$ \lim_{n\to\infty}\int_{0}^{n\pi}\mathrm{e}^{-2x}|\sin x|\mathrm{d}x=\lim_{n\to\infty}\int_{0}^{(n+1)\pi}\mathrm{e}^{-2x}|\sin x|\mathrm{d}x=\frac{1+\mathrm{e}^{2\pi}}{5\left(\mathrm{e}^{2\pi}-1\right)}. $$ 

注意到，当  $ t \to +\infty $ 时， $ n \to +\infty $，因此由①式利用夹逼准则，得

 $$ \int_{0}^{+\infty}\mathrm{e}^{-2x}|\sin x|\mathrm{d}x=\lim_{t\to+\infty}\int_{0}^{t}\mathrm{e}^{-2x}|\sin x|\mathrm{d}x=\frac{\mathrm{e}^{2\pi}+1}{5\left(\mathrm{e}^{2\pi}-1\right)}. $$ 

【例 3.88】（第二届全国决赛题，2011）问是否存在区间 [0, 2] 上的连续可微函数  $ f(x) $，且满足  $ f(0) = f(2) = 1, |f'(x)| \leq 1, \left|\int_{0}^{2} f(x) \, dx\right| \leq 1 $ 请说明理由.

【分析】本题给出的条件从几何上表明：光滑曲线

段  $ y = f(x) $  $ (0 \leq x \leq 2) $ 应嵌在一正方形之中 (图 3.9).

显然，折线段 A1B 的方程为

 $$ y=g(x)=\left\{\begin{aligned}&1-x,&0\leqslant x\leqslant1,\\ &x-1,&1<x\leqslant2,\end{aligned}\right. $$ 

且曲边梯形 OABC 的面积大于曲边梯形 OA1BC 的面积，即

 $$ \int_{0}^{2}f(x)\mathrm{d}x>\int_{0}^{2}g(x)\mathrm{d}x=1. $$ 

因此，从几何直观上分析，这样的函数不存在.

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//021efbd8-5b39-4ab2-889a-58663303c812/markdown_2/imgs/img_in_image_box_654_983_937_1254.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A27Z%2F-1%2F%2F6d0d8a9f37375d85dd046fab1fd14f88e21d8c3b4db85761f50ccc4cb7ad2c88" alt="Image" width="26%" /></div>


<div style="text-align: center;"><div style="text-align: center;">图3.9</div> </div>


解 这样的函数不存在. 假设存在这样的函数  $ f(x) $, 则由  $ \left|f'(x)\right| \leqslant 1 $, 得 -1  $ \leqslant f'(x) \leqslant 1 $. 对  $ f(x) $ 分别在区间  $ [0,1] $ 与  $ [1,2] $ 上应用 Lagrange 中值定理, 并利用  $ f(0) = f(2) = 1 $, 得

 $$ f(x)=f(0)+xf^{\prime}\left(\xi_{1}\right)\geqslant1-x\quad\left(0<\xi_{1}<x\leqslant1\right), $$ 

 $$ f(x)=f(2)+(x-2)f^{\prime}\left(\xi_{2}\right)\geqslant x-1\quad\left(1\leqslant x<\xi_{2}<2\right). $$ 

令  $ g(x)=\left\{\begin{array}{ll}1-x,&0\leqslant x\leqslant1,\\x-1,&1<x\leqslant2,\end{array}\right. $ 则  $ f(x)\geqslant g(x),x\in[0,2] $. 所以

 $$ 1\geqslant\int_{0}^{2}f(x)\mathrm{d}x\geqslant\int_{0}^{2}g(x)\mathrm{d}x=\int_{0}^{1}(1-x)\mathrm{d}x+\int_{1}^{2}(x-1)\mathrm{d}x=1, $$ 

由此得

 $$ \int_{0}^{2}[f(x)-g(x)]\mathrm{d}x=0, $$ 

从而有  $ f(x) \equiv g(x) (0 \leqslant x \leqslant 2) $. 但在 x = 1 处  $ f(x) $ 可导而  $ g(x) $ 不可导，矛盾.

因此，满足题设条件的函数不存在.

【注】结合上述几何直观上分析，类似地可证：设函数  $ f(x) $ 在  $ [0,2] $ 上连续，在  $ (0,2) $ 内可导， $ f(0)=f(2)=1 $，且  $ \left|f'(x)\right|\leqslant1 $。求证： $ 1<\int_{0}^{2}f(x)dx<3 $。

【例 3.89】（第十四届全国初赛 (补赛）题，2022）设曲线  $ C: x^{3} + y^{3} - \frac{3}{2}xy = 0 $.

(1) 已知曲线 C 存在斜渐近线，求其斜渐近线的方程；

(2) 求由曲线 C 所围成的平面图形的面积.

解 (1) 斜渐近线的方程为 y = kx + b，其中  $ k = \lim_{x \to \infty} \frac{y}{x} $， $ b = \lim_{x \to \infty} (y - kx) $.

由方程  $ x^{3}+y^{3}-\frac{3}{2}xy=0 $ 得  $ 1+\left(\frac{y}{x}\right)^{3}-\frac{3}{2x}\cdot\frac{y}{x}=0 $ 。两边取极限  $ x\to\infty $ ，得  $ k=\lim_{x\to\infty}\frac{y}{x}=-1 $ 。

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//021efbd8-5b39-4ab2-889a-58663303c812/markdown_3/imgs/img_in_image_box_126_1029_356_1272.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A28Z%2F-1%2F%2F5fe4a0b9537106277fa932a336d3583de7ef132890a9107194c023770301fd5a" alt="Image" width="21%" /></div>


令 t = y + x，则 y = t - x，代入 C 的方程并整理，可得  $ \frac{t^{3}}{3x^{2}} - \frac{t^{2}}{x} + t - \frac{t}{2x} = -\frac{1}{2} $。两边取极限  $ x \to \infty $，注意到  $ t \to b $，得  $ b = -\frac{1}{2} $。因此，曲线 C 的斜渐近线方程为  $ x + y + \frac{1}{2} = 0 $。

<div style="text-align: center;"><div style="text-align: center;">图3.10</div> </div>


(2) 曲线 C 是 Descartes (笛卡儿) 叶形线 (图 3.10), 其极坐标方程为

 $$ r=\frac{3}{2}\cdot\frac{\cos\theta\sin\theta}{\cos^{3}\theta+\sin^{3}\theta}\quad\left(0\leqslant\theta\leqslant\frac{\pi}{2}\right). $$ 

曲线 C 所围成的平面图形的面积为

 $$ \begin{aligned}A&=\frac{1}{2}\int_{0}^{\frac{\pi}{2}}[r(\theta)]^{2}\mathrm{d}\theta=\frac{9}{8}\int_{0}^{\frac{\pi}{2}}\frac{\cos^{2}\theta\sin^{2}\theta}{\left(\cos^{3}\theta+\sin^{3}\theta\right)^{2}}\mathrm{d}\theta\\&=\frac{9}{8}\int_{0}^{\frac{\pi}{2}}\frac{\tan^{2}\theta\mathrm{d}(\tan\theta)}{\left(1+\tan^{3}\theta\right)^{2}}=\frac{9}{8}\left(-\frac{1}{3}\cdot\frac{1}{1+\tan^{3}\theta}\right)\bigg|_{0}^{\frac{\pi}{2}}\\&=\frac{3}{8}.\end{aligned} $$ 

【注】一般地，Descartes 叶形线的方程为

 $$ x^{3}+y^{3}-3axy=0\quad(a>0), $$ 

其参数方程为  $ x=\frac{3at}{1+t^{3}} $,  $ y=\frac{3at^{2}}{1+t^{3}} $. 本题是  $ a=\frac{1}{2} $ 的情形.

【例 3.90】（第十届全国初赛题，2018）证明：对于连续函数  $ f(x)>0 $ ，有

 $$ \ln\int_{0}^{1}f(x)\mathrm{d}x\geqslant\int_{0}^{1}\ln f(x)\mathrm{d}x. $$ 

证 (方法1) 对  $ \ln x $ 利用 Taylor 公式, 有

 $$ \begin{aligned}\ln x&=\ln x_{0}+\frac{1}{x_{0}}\left(x-x_{0}\right)-\frac{1}{2\xi^{2}}\left(x-x_{0}\right)^{2}\quad( 其中 \xi 介于 x_{0} 与 x 之间 )\\&\leqslant\ln x_{0}+\frac{1}{x_{0}}\left(x-x_{0}\right).\end{aligned} $$ 

取  $ x_{0}=\int_{0}^{1}f(t)dt,x=f(t) $，则  $ x_{0}>0,x>0 $。代入上式，得

 $$ \ln f(t)\leqslant\ln\int_{0}^{1}f(t)\mathrm{d}t+\frac{1}{x_{0}}\left[f(t)-x_{0}\right]. $$ 

对上式两端从0到1积分，得

 $$ \begin{aligned}\int_{0}^{1}\ln f(t)\mathrm{d}t&\leqslant\ln\int_{0}^{1}f(t)\mathrm{d}t+\frac{1}{x_{0}}\left[\int_{0}^{1}f(t)\mathrm{d}t-x_{0}\right]\\&=\ln\int_{0}^{1}f(t)\mathrm{d}t,\end{aligned} $$ 

亦即  $ \ln\int_{0}^{1}f(x)\mathrm{d}x\geqslant\int_{0}^{1}\ln f(x)\mathrm{d}x $

（方法2）将区间[0,1]进行n等分，分点为 $ x_{k}=\frac{k}{n} $，记 $ f(x_{k})=f_{k}(k=1,2,\cdots,n) $，根据定积分的定义，得

 $$ \int_{0}^{1}f(x)\mathrm{d}x=\lim_{n\to\infty}\sum_{k=1}^{n}f\left(x_{k}\right)\frac{1}{n}=\lim_{n\to\infty}\frac{1}{n}\left(f_{1}+f_{2}+\cdots+f_{n}\right), $$ 

 $$ \int_{0}^{1}\ln f(x)\mathrm{d}x=\lim_{n\to\infty}\sum_{k=1}^{n}\ln f\left(x_{k}\right)\frac{1}{n}=\lim_{n\to\infty}\frac{1}{n}\left(\ln f_{1}+\ln f_{2}+\cdots+\ln f_{n}\right). $$ 

利用 Cauchy 平均值不等式，有

 $$ \frac{1}{n}\left(f_{1}+f_{2}+\cdots+f_{n}\right)\geqslant\sqrt[n]{f_{1}\cdot f_{2}\cdot\cdots\cdot f_{n}}. $$ 

对上式取对数，并利用函数  $ \ln x $ 的单调性，得

 $$ \ln\left[\frac{1}{n}\left(f_{1}+f_{2}+\cdots+f_{n}\right)\right]\geqslant\frac{1}{n}\left(\ln f_{1}+\ln f_{2}+\cdots+\ln f_{n}\right). $$ 

两边取极限，并结合①式和②式，得

 $$ \ln\int_{0}^{1}f(x)\mathrm{d}x=\ln\left(\lim_{n\to\infty}\frac{1}{n}\sum_{k=1}^{n}f_{k}\right)\geqslant\lim_{n\to\infty}\frac{1}{n}\sum_{k=1}^{n}\ln f_{k}=\int_{0}^{1}\ln f(x)\mathrm{d}x. $$ 

【注】本题的一般情形即积分形式的 Jensen 不等式，详见本章例 3.71.

【例 3.91】（第八届全国决赛题，2017） 曲线  $ L_{1}: y = \frac{1}{3}x^{3} + 2x $ （ $ 0 \leq x \leq 1 $）绕直线  $ L_{2}: y = \frac{4}{3}x $ 旋转所生成的旋转曲面的面积为 ___.

解 利用微元法. 在曲线  $ L_{1} $ 上任意点  $ (x,y) $ 到直线  $ L_{2} $ 的距离为

 $$ d(x)=\frac{\left|4x-3y\right|}{\sqrt{4^{2}+(-3)^{2}}}=\frac{1}{5}x\left(2+x^{2}\right), $$ 

曲线  $ L_{1} $ 上的弧长微元  $ \mathrm{d}s=\sqrt{1+(y^{\prime})^{2}}\mathrm{d}x=\sqrt{1+(2+x^{2})^{2}}\mathrm{d}x $，因此，旋转曲面的面积为

 $$ A=2\pi\int_{0}^{1}d(x)\sqrt{1+\left(y^{\prime}\right)^{2}}\mathrm{d}x=\frac{2\pi}{5}\int_{0}^{1}x\left(2+x^{2}\right)\sqrt{1+\left(2+x^{2}\right)^{2}}\mathrm{d}x. $$ 

作变量代换： $ t=2+x^{2} $，则

 $$ A=\frac{\pi}{5}\int_{2}^{3}t\sqrt{1+t^{2}}\mathrm{d}t=\left.\frac{\pi}{15}\left(1+t^{2}\right)^{\frac{3}{2}}\right|_{2}^{3}=\frac{\sqrt{5}(2\sqrt{2}-1)}{3}\pi. $$ 

【例 3.92】（第十一届全国决赛题，2021）设函数  $ f(x) $ 在区间  $ [0,1] $ 上具有连续的一阶导数， $ f(0)=f(1)=0 $，且满足  $ \int_{0}^{1}\left[f'(x)\right]^{2}\mathrm{d}x-8\int_{0}^{1}f(x)\mathrm{d}x+\frac{4}{3}=0 $，则  $ f(x)= $ ___.

【分析】注意到 $ \int_{0}^{1}f(x)\mathrm{d}x=-\int_{0}^{1}xf^{\prime}(x)\mathrm{d}x $，所以可根据题设等式“凑”一个简单的函数 $ g(x) $，使得 $ \int_{0}^{1}\left[f^{\prime}(x)-g(x)\right]^{2}\mathrm{d}x=0 $，从而有 $ f^{\prime}(x)=g(x) $。再积分即可得 $ f(x) $。

解 因为  $ f'(x) $ 在  $ [0,1] $ 上连续，所以  $ \int_{0}^{1}f'(x)\mathrm{d}x=f(1)-f(0)=0. $ 又由于

 $$ \int_{0}^{1}f(x)\mathrm{d}x=\left.x f(x)\right|_{0}^{1}-\int_{0}^{1}x f^{\prime}(x)\mathrm{d}x=-\int_{0}^{1}x f^{\prime}(x)\mathrm{d}x, $$ 

故对任意常数 a，都有

 $$ \begin{align*}\int_{0}^{1}\left[f^{\prime}(x)\right]^{2}\mathrm{d}x-8\int_{0}^{1}f(x)\mathrm{d}x&=\int_{0}^{1}\left[f^{\prime}(x)\right]^{2}\mathrm{d}x+8\int_{0}^{1}x f^{\prime}(x)\mathrm{d}x+a\int_{0}^{1}f^{\prime}(x)\mathrm{d}x\\&=\int_{0}^{1}\left[f^{\prime}(x)\right]^{2}\mathrm{d}x-2\int_{0}^{1}\left(-4x+\frac{a}{2}\right)f^{\prime}(x)\mathrm{d}x.\end{align*} $$ 

令  $ g(x) = -4x + \frac{a}{2} $，使得  $ \int_{0}^{1}[g(x)]^{2}dx = \frac{4}{3} $，即  $ (a-4)^{2} = 0 $。这只需取 a = 4。因此

 $$ \int_{0}^{1}\left[f^{\prime}(x)\right]^{2}\mathrm{d}x-8\int_{0}^{1}f(x)\mathrm{d}x+\frac{4}{3}=\int_{0}^{1}\left[f^{\prime}(x)-g(x)\right]^{2}\mathrm{d}x=0, $$ 

从而有  $ f'(x) = g(x) = -4x + 2 $ 。由此得

 $$ f(x)=f(0)+\int_{0}^{x}f^{\prime}(t)\mathrm{d}t=\int_{0}^{x}(-4t+2)\mathrm{d}t=2x-2x^{2}. $$ 

【例 3.93】（第八届全国决赛题，2017）设  $ f(x) $ 为  $ (-\infty, +\infty) $ 上连续的、周期为 1 的周期函数，且满足  $ 0 \leqslant f(x) \leqslant 1 $ 与  $ \int_{0}^{1} f(x) \, dx = 1 $。证明：当  $ 0 \leqslant x \leqslant 13 $ 时，有

 $$ \int_{0}^{\sqrt{x}}f(t)\mathrm{d}t+\int_{0}^{\sqrt{x+27}}f(t)\mathrm{d}t+\int_{0}^{\sqrt{13-x}}f(t)\mathrm{d}t\leqslant11. $$ 

证 根据题设条件  $ 0 \leqslant f(x) \leqslant 1 $，可得

 $$ \int_{0}^{\sqrt{x}}f(t)\mathrm{d}t+\int_{0}^{\sqrt{x+27}}f(t)\mathrm{d}t+\int_{0}^{\sqrt{13-x}}f(t)\mathrm{d}t\leqslant\sqrt{x}+\sqrt{x+27}+\sqrt{13-x}. $$ 

利用 Cauchy 不等式:  $ \left(\sum_{i=1}^{n}a_{i}b_{i}\right)^{2}\leqslant\sum_{i=1}^{n}a_{i}^{2}\sum_{i=1}^{n}b_{i}^{2} $，等号当  $ a_{i} $ 与  $ b_{i} $ 对应成比例时成立，有

 $$ \sqrt{x}+\sqrt{x+27}+\sqrt{13-x}=1\cdot\sqrt{x}+\sqrt{2}\cdot\sqrt{\frac{1}{2}(x+27)}+\sqrt{\frac{2}{3}}\cdot\sqrt{\frac{3}{2}(13-x)} $$ 

 $$ \begin{aligned}&\leqslant\sqrt{1+2+\frac{2}{3}}\cdot\sqrt{x+\frac{1}{2}(x+27)+\frac{3}{2}(13-x)}\\ &=11,\\ \end{aligned} $$ 

且等号成立的充分必要条件是

 $$ \frac{\sqrt{x}}{1}=\frac{\sqrt{\frac{1}{2}(x+27)}}{\sqrt{2}}=\frac{\sqrt{\frac{3}{2}(13-x)}}{\sqrt{\frac{2}{3}}}, $$ 

解得 x=9. 进一步，当 x=9 时，根据  $ f(x) $ 的周期性及  $ \int_{0}^{1}f(x)\mathrm{d}x=1 $，可得

 $$ \begin{aligned}&\int_{0}^{\sqrt{x}}f(t)\mathrm{d}t+\int_{0}^{\sqrt{x+27}}f(t)\mathrm{d}t+\int_{0}^{\sqrt{13-x}}f(t)\mathrm{d}t\\=&\int_{0}^{3}f(t)\mathrm{d}t+\int_{0}^{6}f(t)\mathrm{d}t+\int_{0}^{2}f(t)\mathrm{d}t\\=&3\int_{0}^{1}f(t)\mathrm{d}t+6\int_{0}^{1}f(t)\mathrm{d}t+2\int_{0}^{1}f(t)\mathrm{d}t=11,\end{aligned} $$ 

因此，当且仅当 x=9 时不等式取等号.

【例 3.94】（第六届全国初赛题，2014）设  $ f(x) $ 在区间  $ [a,b] $ 上非负连续、严格单调增加，且对任意的  $ n \in \mathbb{N} $，存在  $ x_n \in [a,b] $ 使得  $ [f(x_n)]^n = \frac{1}{b-a} \int_a^b [f(x)]^n \, \mathrm{d}x $，求极限  $ \lim_{n \to \infty} x_n $。

解 根据题设条件及积分中值定理的几何意义，可推断出  $ \lim_{n\to\infty}x_n=b $，下证之.

 $ \forall\varepsilon>0 $，可要求 $ \varepsilon<\frac{b-a}{2} $，由于 $ f(b-2\varepsilon)<f(b-\varepsilon) $，故存在正整数N，当n>N时，有

 $$ 0<\left[\frac{f(b-2\varepsilon)}{f(b-\varepsilon)}\right]^{n}<\frac{\varepsilon}{b-a}. $$ 

从而有

 $$ \begin{align*}f^{n}(b-2\varepsilon)&<\frac{\varepsilon}{b-a}f^{n}(b-\varepsilon)=\frac{1}{b-a}\int_{b-\varepsilon}^{b}f^{n}(b-\varepsilon)\mathrm{d}x\\&\leqslant\frac{1}{b-a}\int_{b-\varepsilon}^{b}f^{n}(x)\mathrm{d}x\leqslant\frac{1}{b-a}\int_{a}^{b}f^{n}(x)\mathrm{d}x=f^{n}\left(x_{n}\right).\end{align*} $$ 

因为  $ f(x) $ 严格单增，所以 b - 2 $ \varepsilon < x_n $。又总有  $ x_n < b + 2\varepsilon $。于是，当 n > N 时，有  $ \left|x_n - b\right| < 2\varepsilon $。这就证得  $ \lim_{n \to \infty} x_n = b $。

【例 3.95】(第七届全国初赛题, 2015) 设函数  $ f(x) $ 在  $ [0,1] $ 上连续，且  $ \int_{0}^{1}f(x)dx=0 $， $ \int_{0}^{1}xf(x)dx=1 $。试证：

(1) 存在  $ x_0 \in [0,1] $，使得  $ |f(x_0)| > 4 $;

(2) 存在  $ x_1 \in [0,1] $，使得  $ |f(x_1)| = 4 $.

证（1）用反证法. 假设在  $ [0,1] $ 上恒有  $ \left|f(x)\right|\leq4 $，则由题设条件可得

 $$ 1=\left|\int_{0}^{1}\left(x-\frac{1}{2}\right)f(x)\mathrm{d}x\right|\leqslant\int_{0}^{1}\left|\left(x-\frac{1}{2}\right)f(x)\right|\mathrm{d}x\leqslant4\int_{0}^{1}\left|x-\frac{1}{2}\right|\mathrm{d}x=1. $$ 

所以

 $$ \begin{align*}\int_{0}^{1}\left|\left(x-\frac{1}{2}\right)f(x)\right|\mathrm{d}x&=4\int_{0}^{1}\left|x-\frac{1}{2}\right|\mathrm{d}x=1,\\\int_{0}^{1}\left|x-\frac{1}{2}\right|(4-|f(x)|)\mathrm{d}x&=0.\end{align*} $$ 

由于被积函数非负连续, 且积分值为零, 所以被积函数恒为零, 从而有  $ f(x) \equiv 4 $ 或  $ f(x) \equiv -4 $, 此与条件  $ \int_{0}^{1} f(x) \, dx = 0 $ 矛盾. 因此, 存在  $ x_{0} \in [0,1] $ 使得  $ |f(x_{0})| > 4 $.

(2) 根据题设,  $ f(x) $ 为连续函数, 且  $ \int_{0}^{x} f(x) \, \mathrm{d}x = 0 $, 利用积分中值定理, 存在  $ \xi \in (0,1) $, 使得  $ f(\xi) = 0 $. 结合 (1) 的结论, 有  $ |f(x_0)| > 4 > |f(\xi)| $. 对连续函数  $ |f(x)| $ 利用介值定理, 存在介于  $ x_0 $ 与  $ \xi $ 之间的  $ x_1 $, 即  $ x_1 \in [0,1] $, 使得  $ |f(x_1)| = 4 $.

【例 3.96】（第九届全国初赛题，2017）设  $ f(x) $ 是  $ (-\infty,+\infty) $ 上的连续正值函数，且对任意  $ t\in(-\infty,+\infty) $，都有  $ \int_{-\infty}^{+\infty}\mathrm{e}^{-|t-x|}f(x)\mathrm{d}x\leqslant1 $ 。证明：对任意 a,b>0 且 a<b，有

 $$ \int_{a}^{b}f(x)\mathrm{d}x\leqslant\frac{b-a}{2}+1. $$ 

证 对任意  $ t \in (-\infty, +\infty) $ 及对任意 a, b > 0 且 a < b，根据题设条件，得

 $$ \int_{a}^{b}\mathrm{e}^{-|t-x|}f(x)\mathrm{d}x\leqslant\int_{-\infty}^{+\infty}\mathrm{e}^{-|t-x|}f(x)\mathrm{d}x\leqslant1. $$ 

对上式两端关于 t 作定积分，得

 $$ \int_{a}^{b}\left(\int_{a}^{b}\mathrm{e}^{-|t-x|}f(x)\mathrm{d}x\right)\mathrm{d}t\leqslant b-a. $$ 

交换二次积分次序，得

 $$ \int_{a}^{b}\left(\int_{a}^{b}\mathrm{e}^{-|t-x|}\mathrm{d}t\right)f(x)\mathrm{d}x\leqslant b-a. $$ 

经直接计算，有

 $$ \int_{a}^{b}\mathrm{e}^{-|t-x|}\mathrm{d}t=\int_{a}^{x}\mathrm{e}^{t-x}\mathrm{d}t+\int_{x}^{b}\mathrm{e}^{x-t}\mathrm{d}t=2-\mathrm{e}^{a-x}-\mathrm{e}^{x-b}. $$ 

代入②式并整理再利用①式，得

 $$ \begin{align*}\int_{a}^{b}f(x)\mathrm{d}x&\leqslant\frac{b-a}{2}+\frac{1}{2}\int_{a}^{b}\mathrm{e}^{a-x}f(x)\mathrm{d}x+\frac{1}{2}\int_{a}^{b}\mathrm{e}^{x-b}f(x)\mathrm{d}x\\&=\frac{b-a}{2}+\frac{1}{2}\int_{a}^{b}\mathrm{e}^{-|a-x|}f(x)\mathrm{d}x+\frac{1}{2}\int_{a}^{b}\mathrm{e}^{-|b-x|}f(x)\mathrm{d}x\\&\leqslant\frac{b-a}{2}+\frac{1}{2}+\frac{1}{2}=\frac{b-a}{2}+1.\end{align*} $$ 

【例 3.97】(第十届全国初赛题, 2018) 设  $ f(x) $ 在区间  $ [0,1] $ 上连续，且  $ 1 \leqslant f(x) \leqslant 3 $. 证明：

 $$ 1\leqslant\int_{0}^{1}f(x)\mathrm{d}x\int_{0}^{1}\frac{\mathrm{d}x}{f(x)}\leqslant\frac{4}{3}. $$ 

证 利用 Cauchy 积分不等式，得

 $$ \int_{0}^{1}f(x)\mathrm{d}x\int_{0}^{1}\frac{\mathrm{d}x}{f(x)}\geqslant\left(\int_{0}^{1}\sqrt{f(x)}\sqrt{\frac{1}{f(x)}}\mathrm{d}x\right)^{2}=1. $$ 

另一方面，由  $ 1 \leqslant f(x) \leqslant 3 $ 得  $ [f(x)-1][f(x)-3] \leqslant 0 $，由此得  $ f(x)+\frac{3}{f(x)} \leqslant 4 $，所以

 $$ \int_{0}^{1}f(x)\mathrm{d}x+\int_{0}^{1}\frac{3}{f(x)}\mathrm{d}x\leqslant4. $$ 

利用平均值不等式，得  $ \int_{0}^{1}f(x)\mathrm{d}x\int_{0}^{1}\frac{3}{f(x)}\mathrm{d}x\leqslant\frac{1}{4}\left(\int_{0}^{1}f(x)\mathrm{d}x+\int_{0}^{1}\frac{3}{f(x)}\mathrm{d}x\right)^{2}=4 $ ，即

 $$ \int_{0}^{1}f(x)\mathrm{d}x\int_{0}^{1}\frac{\mathrm{d}x}{f(x)}\leqslant\frac{4}{3}. $$ 

【注】这是 Kantorovich 不等式的特别情形 (m=1, M=3)，详见本章例 3.73.

【例 3.98】（第十四届全国初赛题，2022）证明：对任意正整数 n，恒有

 $$ \int_{0}^{\frac{\pi}{2}}x\left(\frac{\sin nx}{\sin x}\right)^{4}\mathrm{d}x\leqslant\left(\frac{n^{2}}{4}-\frac{1}{8}\right)\pi^{2}. $$ 

证 首先, 利用归纳法易证: 当  $ n \geqslant 1 $ 时,  $ |\sin nx| \leqslant n \sin x $  $ (0 \leqslant x \leqslant \frac{\pi}{2}) $.

当 n=1 时， $ \int_{0}^{\frac{\pi}{2}}x\mathrm{d}x=\frac{\pi^{2}}{8} $，等号成立.

当 n > 1 时，因为  $ \left|\sin nx\right| \leqslant 1 $ 及  $ \sin x \geqslant \frac{2}{\pi} x \left(0 \leqslant x \leqslant \frac{\pi}{2}\right) $，所以

 $$ \begin{aligned}\int_{0}^{\frac{\pi}{2}}x\left(\frac{\sin nx}{\sin x}\right)^{4}\mathrm{d}x&=\int_{0}^{\frac{\pi}{2n}}x\left(\frac{\sin nx}{\sin x}\right)^{4}\mathrm{d}x+\int_{\frac{\pi}{2n}}^{\frac{\pi}{2}}x\left(\frac{\sin nx}{\sin x}\right)^{4}\mathrm{d}x\\&\leqslant n^{4}\int_{0}^{\frac{\pi}{2n}}x\mathrm{d}x+\int_{\frac{\pi}{2n}}^{\frac{\pi}{2}}x\left(\frac{1}{\frac{2x}{\pi}}\right)^{4}\mathrm{d}x=\frac{n^{4}}{2}\left(\frac{\pi}{2n}\right)^{2}+\frac{\pi^{4}}{16}\int_{\frac{\pi}{2n}}^{\frac{\pi}{2}}\frac{\mathrm{d}x}{x^{3}}\\&=\frac{n^{2}\pi^{2}}{8}+\frac{\pi^{4}}{16}\cdot\frac{1}{-2x^{2}}\bigg|_{\frac{\pi}{2n}}^{\frac{\pi}{2}}=\frac{n^{2}\pi^{2}}{8}-\frac{\pi^{4}}{16}\left(\frac{2}{\pi^{2}}-\frac{2n^{2}}{\pi^{2}}\right)\\&=\left(\frac{n^{2}}{4}-\frac{1}{8}\right)\pi^{2}.\end{aligned} $$ 

【例 3.99】（第十一届全国决赛题，2021）设函数  $ f(x) $ 在区间  $ [0,1] $ 上具有连续导数，且满足  $ \int_{0}^{1}f(x)\mathrm{d}x=\frac{5}{2},\int_{0}^{1}xf(x)\mathrm{d}x=\frac{3}{2} $，证明：存在  $ \xi\in(0,1) $，使得  $ f'(\xi)=3 $.

【分析】先利用待定系数法，确定一个函数  $ g(x)=x^{2}+ax+b $，使得  $ g(x) $ 在  $ [0,1] $ 上不变号，且  $ \int_{0}^{1}g(x)\left[f'(x)-3\right]\mathrm{d}x=0 $，再根据积分中值定理即可证得结论.

证 令  $ g(x)=x^{2}+ax+b $ ，使得  $ \int_{0}^{1}g(x)\left[f'(x)-3\right]\mathrm{d}x=0 $ ，其中 a, b 待定. 易知

 $$ \begin{align*}\int_{0}^{1}g(x)[f^{\prime}(x)-3]\mathrm{d}x&=g(x)[f(x)-3x]\Big|_{0}^{1}-\int_{0}^{1}g^{\prime}(x)[f(x)-3x]\mathrm{d}x\\ &=(a+b+1)[f(1)-3]-f(0)b-\int_{0}^{1}(2x+a)[f(x)-3x]\mathrm{d}x,\end{align*} $$ 

根据题设条件  $ \int_{0}^{1}f(x)\mathrm{d}x=\frac{5}{2},\int_{0}^{1}xf(x)\mathrm{d}x=\frac{3}{2} $，有

 $$ \begin{aligned}\int_{0}^{1}(2x+a)[f(x)-3x]\mathrm{d}x&=2\int_{0}^{1}x f(x)\mathrm{d}x+a\int_{0}^{1}f(x)\mathrm{d}x-3\int_{0}^{1}x(2x+a)\mathrm{d}x\\&=3+\frac{5a}{2}-\left(2+\frac{3a}{2}\right)=1+a,\end{aligned} $$ 

把②式代入①式，得

 $$ \int_{0}^{1}g(x)\left[f^{\prime}(x)-3\right]\mathrm{d}x=(a+b+1)[f(1)-3]-f(0)b-(1+a)=0. $$ 

令  $ a + b + 1 = 0, b = 0, 1 + a = 0 $，解得 a = -1, b = 0。所以  $ g(x) = x(x - 1) $，从而有

 $$ \int_{0}^{1}x(x-1)\left[f^{\prime}(x)-3\right]\mathrm{d}x=0. $$ 

根据积分中值定理，存在  $ \xi \in (0,1) $，使得  $ \xi(\xi - 1)[f'(\xi) - 3] $，所以  $ f'(\xi) = 3 $。

【例 3.100】（第十届全国决赛题，2019）设  $ f(x) $ 在  $ (-\infty, +\infty) $ 上具有连续导数，且  $ |f(x)| \leqslant 1 $,  $ f'(x) > 0 $,  $ x \in (-\infty, +\infty) $. 证明：对于  $ 0 < \alpha < \beta $，有

 $$ \lim_{n\to\infty}\int_{\alpha}^{\beta}f^{\prime}\left(nx-\frac{1}{x}\right)\mathrm{d}x=0. $$ 

证 令  $ y(x)=x-\frac{1}{nx} $，则  $ y'(x)=1+\frac{1}{nx^{2}}>0 $，所以函数  $ y(x) $ 在  $ [\alpha,\beta] $ 上严格单调增加。记  $ y(x) $ 的反函数为  $ x(y) $，则  $ x(y) $ 定义在  $ \left[\alpha-\frac{1}{n\alpha},\beta-\frac{1}{n\beta}\right] $ 上，且  $ x'(y)=\frac{1}{y'(x)}=\frac{nx^{2}}{1+nx^{2}}>0 $。因此

 $$ \int_{\alpha}^{\beta}f^{\prime}\left(n x-\frac{1}{x}\right)\mathrm{d}x=\int_{\alpha-\frac{1}{n\alpha}}^{\beta-\frac{1}{n\beta}}f^{\prime}(n y)x^{\prime}(y)\mathrm{d}y. $$ 

根据积分中值定理，存在  $ \xi_n \in \left[\alpha - \frac{1}{n\alpha}, \beta - \frac{1}{n\beta}\right] $，使得

 $$ \begin{align*}\left|\int_{\alpha-\frac{1}{n\alpha}}^{\beta-\frac{1}{n\beta}}f^{\prime}(ny)x^{\prime}(y)\mathrm{d}y\right|&=\left|x^{\prime}\left(\xi_{n}\right)\int_{\alpha-\frac{1}{n\alpha}}^{\beta-\frac{1}{n\beta}}f^{\prime}(ny)\mathrm{d}y\right|\\&=\frac{x^{\prime}\left(\xi_{n}\right)}{n}\left|f\left(n\beta-\frac{1}{\beta}\right)-f\left(n\alpha-\frac{1}{\alpha}\right)\right|\leqslant\frac{2}{n}\cdot\frac{n\xi_{n}^{2}}{1+n\xi_{n}^{2}}\leqslant\frac{2}{n}.\end{align*} $$ 

因此

 $$ \left|\int_{\alpha}^{\beta}f^{\prime}\left(nx-\frac{1}{x}\right)\mathrm{d}x\right|\leqslant\frac{2}{n}. $$ 

根据夹逼准则，得  $ \lim_{n\to\infty}\int_{\alpha}^{\beta}f^{\prime}\left(nx-\frac{1}{x}\right)\mathrm{d}x=0. $

【例 3.101】（第十二届全国决赛题，2021）设  $ f(x) $,  $ g(x) $ 是  $ [0,1] \to [0,1] $ 的连续函数，且  $ f(x) $ 单调增加，求证：

 $$ \int_{0}^{1}f(g(x))\mathrm{d}x\leqslant\int_{0}^{1}f(x)\mathrm{d}x+\int_{0}^{1}g(x)\mathrm{d}x. $$ 

证 (方法1) 设  $ F(x)=f(x)-x $，则  $ F(x) $ 是  $ [0,1] $ 上的连续函数，因此问题转化为证明

 $$ \int_{0}^{1}[F(g(x))-F(x)]\mathrm{d}x\leqslant\int_{0}^{1}x\mathrm{d}x=\frac{1}{2}, $$ 

这只需证明  $ \max_{0\leq x\leq1} F(x) - \int_{0}^{1} F(x) \, dx \leq \frac{1}{2} $，即  $ \int_{0}^{1} F(x) \, dx \geq \max_{0\leq x\leq1} F(x) - \frac{1}{2} $.

设  $ \max_{0\leq x\leq1} F(x)=F(x_0)=A $，由于  $ 0\leq f(x)\leq1 $，所以  $ -x\leq F(x)\leq1-x $。因为  $ f(x) $ 单调增加，当  $ x\in[x_0,1] $ 时， $ f(x)\geq f(x_0) $，即  $ F(x)+x\geq F(x_0)+x_0=A+x_0 $，所以

 $$ \begin{align*}\int_{0}^{1}F(x)\mathrm{d}x&=\int_{0}^{x_{0}}F(x)\mathrm{d}x+\int_{x_{0}}^{1}F(x)\mathrm{d}x\geqslant\int_{0}^{x_{0}}(-x)\mathrm{d}x+\int_{x_{0}}^{1}(A+x_{0}-x)\mathrm{d}x\\&=A-\frac{1}{2}+x_{0}\left[1-f\left(x_{0}\right)\right]\geqslant A-\frac{1}{2}=\max_{0\leqslant x\leqslant1}F(x)-\frac{1}{2}.\end{align*} $$ 

（方法 2）利用积分中值定理，存在  $ \xi \in [0,1] $，使得

 $$ \int_{0}^{1}[f(g(x))-g(x)]\mathrm{d}x=f(g(\xi))-g(\xi). $$ 

记  $ \delta = g(\xi) $，则  $ 0 \leqslant \delta \leqslant 1 $。注意到  $ 0 \leqslant f(x) \leqslant 1 $，且  $ f(x) $ 单调增加，所以

 $$ \begin{align*}\int_{0}^{1}f(g(x))\mathrm{d}x&=f(\delta)-\delta+\int_{0}^{1}g(x)\mathrm{d}x\leqslant f(\delta)(1-\delta)+\int_{0}^{1}g(x)\mathrm{d}x\\&=\int_{\delta}^{1}f(\delta)\mathrm{d}x+\int_{0}^{1}g(x)\mathrm{d}x\leqslant\int_{\delta}^{1}f(x)\mathrm{d}x+\int_{0}^{1}g(x)\mathrm{d}x\\&\leqslant\int_{0}^{1}f(x)\mathrm{d}x+\int_{0}^{1}g(x)\mathrm{d}x.\end{align*} $$ 

【例 3.102】（第三届全国决赛题，2012） 讨论  $ \int_{0}^{+\infty}\frac{x}{\cos^{2}x+x^{\alpha}\sin^{2}x}dx $ 的敛散性，其中  $ \alpha $ 是一个实常数.

解 令  $ f(x)=\frac{x}{\cos^{2}x+x^{\alpha}\sin^{2}x} $，因为  $ f(x) $ 在  $ [0,+\infty) $ 上连续，所以定积分  $ \int_{0}^{1}f(x)\mathrm{d}x $ 存在，故只需讨论  $ \int_{1}^{+\infty}f(x)\mathrm{d}x $ 的敛散性.

(1) 若  $ \alpha \leqslant 0 $，则  $ f(x) \geqslant \frac{x}{2} \geqslant \frac{1}{2} $。根据比较判别法可知，积分  $ \int_{1}^{+\infty} f(x) \, dx $ 发散。

(2) 若  $ \alpha > 0 $，记  $ a_{n} = \int_{n\pi}^{(n+1)\pi} f(x) \, dx $，因为  $ f(x) > 0 $，所以积分  $ \int_{1}^{+\infty} f(x) \, dx $ 与级数  $ \sum_{n=1}^{\infty} a_{n} $ 具有相同的敛散性。下面讨论  $ \sum_{n=1}^{\infty} a_{n} $ 的敛散性。对于  $ a_{n} $，显然有

 $$ \int_{n\pi}^{(n+1)\pi}\frac{n\pi}{\cos^{2}x+((n+1)\pi)^{\alpha}\sin^{2}x}\mathrm{d}x\leqslant a_{n}\leqslant\int_{n\pi}^{(n+1)\pi}\frac{(n+1)\pi}{\cos^{2}x+(n\pi)^{\alpha}\sin^{2}x}\mathrm{d}x. $$ 

对任意 b > 0,  $ \frac{1}{\cos^{2}x + b\sin^{2}x} $ 是以  $ \pi $ 为周期的偶函数, 根据定积分的性质, 得

 $$ \int_{n\pi}^{(n+1)\pi}\frac{\mathrm{d}x}{\cos^{2}x+b\sin^{2}x}=\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\frac{\mathrm{d}x}{\cos^{2}x+b\sin^{2}x}=2\int_{0}^{\frac{\pi}{2}}\frac{\mathrm{d}x}{\cos^{2}x+b\sin^{2}x} $$ 

 $$ \begin{aligned}&=2\int_{0}^{\frac{\pi}{2}}\frac{\mathrm{d}(\tan x)}{1+(\sqrt{b}\tan x)^{2}}=\left.\frac{2}{\sqrt{b}}\arctan(\sqrt{b}\tan x)\right|_{0}^{\frac{\pi}{2}}\\&=\frac{2}{\sqrt{b}}\cdot\frac{\pi}{2}=\frac{\pi}{\sqrt{b}},\end{aligned} $$ 

分别取  $  b = \left[ (n + 1)\pi \right]^{\alpha}  $ 和  $  (n\pi)^{\alpha}  $，则由 ① 式得  $ \frac{n\pi^{2}}{\sqrt{((n + 1)\pi)^{\alpha}}} \leqslant a_{n} \leqslant \frac{(n + 1)\pi^{2}}{\sqrt{(n\pi)^{\alpha}}} $，即

 $$ \left(\frac{n}{n+1}\right)^{\frac{\alpha}{2}}\pi^{2-\frac{\alpha}{2}}\leqslant\frac{a_{n}}{n^{1-\frac{\alpha}{2}}}\leqslant\frac{n+1}{n}\pi^{2-\frac{\alpha}{2}}. $$ 

根据夹逼准则, 得  $ \lim_{n\to\infty}\frac{a_n}{n^{1-\frac{\alpha}{2}}}=\pi^{2-\frac{\alpha}{2}} $. 因此, 由级数  $ \sum_{n=1}^{\infty}\frac{1}{n^{\frac{\alpha}{2}-1}} $ 的收敛性及比较判别法可知, 当  $ \alpha>4 $ 时,  $ \sum\infty a_n $ 收敛; 当  $ \alpha\leq4 $ 时,  $ \sum\infty a_n $ 发散.

综上可知，当  $ \alpha > 4 $ 时， $ \int_{0}^{+\infty} f(x) \, dx $ 收敛；当  $ \alpha \leq 4 $ 时， $ \int_{0}^{+\infty} f(x) \, dx $ 发散。

【例 3.103】（第十三届全国初赛 (补赛) 题, 2021）设函数  $ f(x)=\int_{0}^{x}\left(1-\frac{[u]}{u}\right)\mathrm{d}u $，其中  $ [u] $ 表示不超过 u 的最大整数，试讨论  $ \int_{1}^{+\infty}\frac{\mathrm{e}^{f(x)}}{x^{p}}\cos\left(x^{2}-\frac{1}{x^{2}}\right)\mathrm{d}x $ 的敛散性，其中 p>0.

解 对任意正整数 N，当  $ x \in [N, N+1] $ 时，有

 $$ \begin{align*}f(x)&=\int_{0}^{1}\left(1-\frac{[u]}{u}\right)\mathrm{d}u+\sum_{k=1}^{N-1}\int_{k}^{k+1}\left(1-\frac{[u]}{u}\right)\mathrm{d}u+\int_{N}^{x}\left(1-\frac{[u]}{u}\right)\mathrm{d}u\\&=1+\sum_{k=1}^{N-1}\int_{k}^{k+1}\left(1-\frac{k}{u}\right)\mathrm{d}u+\int_{N}^{x}\left(1-\frac{N}{u}\right)\mathrm{d}u\\&=\ln(N!)+x-N\ln x,\end{align*} $$ 

所以  $ \frac{\mathrm{e}^{N}N!}{(N+1)^{N}}\leqslant\mathrm{e}^{f(x)}=\frac{\mathrm{e}^{x}N!}{x^{N}}\leqslant\frac{\mathrm{e}^{N+1}N!}{N^{N}} $ 。根据 Stirling 公式： $ n!\sim\sqrt{2n\pi}\left(\frac{n}{\mathrm{e}}\right)^{n} $，可知当  $ N\to\infty $ 时， $ \frac{\mathrm{e}^{N}N!}{(N+1)^{N}}\sim\frac{1}{\mathrm{e}}\sqrt{2N\pi}\leqslant\frac{1}{\mathrm{e}}\sqrt{2\pi x} $，且  $ \frac{\mathrm{e}^{N+1}N!}{N^{N}}\sim\mathrm{e}\sqrt{2N\pi}\leqslant\mathrm{e}\sqrt{2x\pi} $

因此  $ \mathrm{e}^{f(x)} $ 与  $ \sqrt{x} $ 为同阶无穷大，从而  $ \int_{1}^{+\infty}\frac{\mathrm{e}^{f(x)}}{x^{p}}\cos\left(x^{2}-\frac{1}{x^{2}}\right)\mathrm{d}x $ 的敛散性与  $ \int_{1}^{+\infty}\frac{1}{x^{p-\frac{1}{2}}}\cos\left(x^{2}-\frac{1}{x^{2}}\right)\mathrm{d}x $ 的敛散性相同。令  $ x=\sqrt{y} $，则

 $$ \int_{1}^{+\infty}\frac{1}{x^{p-\frac{1}{2}}}\cos\left(x^{2}-\frac{1}{x^{2}}\right)\mathrm{d}x=\frac{1}{2}\int_{1}^{+\infty}\frac{1}{y^{\frac{2p+1}{4}}}\cos\left(y-\frac{1}{y}\right)\mathrm{d}y. $$ 

对于上式右边的积分，当  $ \frac{2p+1}{4}>1 $，即  $ p>\frac{3}{2} $ 时，积分绝对收敛。又根据 Dirichlet (狄利克雷) 判别法，当 p>0 时，积分收敛。又由于

 $$ \int_{1}^{+\infty}\frac{1}{y^{\frac{2p+1}{4}}}\cos\left(y-\frac{1}{y}\right)\mathrm{d}y=\int_{1}^{+\infty}\frac{\cos y\cos\frac{1}{y}}{y^{\frac{2p+1}{4}}}\mathrm{d}y+\int_{1}^{+\infty}\frac{\sin y\sin\frac{1}{y}}{y^{\frac{2p+1}{4}}}\mathrm{d}y. $$ 

当  $ 0 < p \leqslant \frac{3}{2} $ 时， $ \int_{1}^{+\infty} \frac{\cos y \cos \frac{1}{y}}{y^{\frac{2p+1}{4}}} \mathrm{d}y \sim \int_{1}^{+\infty} \frac{\cos y}{y^{\frac{2p+1}{4}}} \mathrm{d}y = \infty $ 发散；由于  $ \left| \frac{\sin y \sin \frac{1}{y}}{y^{\frac{2p+1}{4}}} \right| \leqslant \frac{1}{y^{\frac{2p+1}{4}}+1} $，而  $ \int_{1}^{+\infty} \frac{\mathrm{d}y}{y^{\frac{2p+1}{4}}+1} $ 收敛，所以  $ \int_{1}^{+\infty} \frac{\sin y \sin \frac{1}{y}}{y^{\frac{2p+1}{4}}} \mathrm{d}y $ 绝对收敛.

综上所述，原积分当  $ 0 < p \leqslant \frac{3}{2} $ 时条件收敛，当  $ p > \frac{3}{2} $ 时绝对收敛。

【例 3.104】（第十五届全国初赛题，2023）设  $ f(x) $ 在  $ [0,1] $ 上有连续的导数，且  $ f(0)=0 $ 求证：

 $$ \int_{0}^{1}f^{2}(x)\mathrm{d}x\leqslant4\int_{0}^{1}(1-x)^{2}\left|f^{\prime}(x)\right|^{2}\mathrm{d}x, $$ 

并求使得上式成为等式的  $ f(x) $.

解 利用分部积分，得

 $$ \begin{aligned}\int_{0}^{1}f^{2}(x)\mathrm{d}x&=\left.(x-1)f^{2}(x)\right|_{0}^{1}-2\int_{0}^{1}(x-1)f(x)f^{\prime}(x)\mathrm{d}x\\&=2\int_{0}^{1}(1-x)f^{\prime}(x)f(x)\mathrm{d}x.\end{aligned} $$ 

根据 Cauchy 积分不等式，得

 $$ \int_{0}^{1}(1-x)f^{\prime}(x)f(x)\mathrm{d}x\leqslant\left(\int_{0}^{1}(1-x)^{2}\left|f^{\prime}(x)\right|^{2}\mathrm{d}x\right)^{\frac{1}{2}}\left(\int_{0}^{1}f^{2}(x)\mathrm{d}x\right)^{\frac{1}{2}}, $$ 

因此，有  $ \int_{0}^{1}f^{2}(x)dx\leqslant4\int_{0}^{1}(1-x)^{2}\left|f'(x)\right|^{2}dx $，其中等号成立当且仅当存在常数c，使得  $ (1-x)f'(x)=cf(x) $。因此当 0<x<1 时，有

 $$ [(1-x)^{c}f(x)]^{\prime}=(1-x)^{c-1}[(1-x)f^{\prime}(x)-c f(x)]=0, $$ 

这等价于  $ f(x)=k(1-x)^{-c} $，其中 k 为常数。当  $ x\to0 $ 时， $ f(x)\to0 $，可得 k=0，所以  $ f(x)=0 $。于是，使得所证不等式成为等式的函数为  $ f(x)=0 $ ( $ 0\leq x\leq1 $)。

【例 3.105】(第十五届全国决赛题, 2024) 定积分  $ \int_{0}^{1}\frac{x^{4}(1-x)^{4}}{1+x^{2}}\mathrm{d}x= $ ___.

解 因为  $ (1-x)^{4}=(1+x^{2}-2x)^{2}=(1+x^{2})^{2}-4x(1+x^{2})+4x^{2} $，所以

 $$ \begin{aligned}I&=\int_{0}^{1}x^{4}(1+x^{2})\mathrm{d}x-4\int_{0}^{1}x^{5}\mathrm{d}x+4\int_{0}^{1}\frac{(x^{6}+1)-1}{1+x^{2}}\mathrm{d}x\\&=\frac{1}{5}+\frac{1}{7}-\frac{2}{3}+4\int_{0}^{1}(x^{4}-x^{2}+1)\mathrm{d}x-4\int_{0}^{1}\frac{\mathrm{d}x}{1+x^{2}}\\&=\frac{22}{7}-\pi.\end{aligned} $$ 

【注】 细心的读者可能已经发现，本题的计算结果由两个重要常数构成：圆周率  $ \pi $ 与圆周率的约率  $ \frac{22}{7} $，这表明用  $ \frac{22}{7} $ 作为  $ \pi $ 的近似值其误差可用一个定积分的值表示出来.

【例 3.106】(第十一届全国初赛题, 2019) 定积分  $ \int_{0}^{\frac{\pi}{2}}\frac{\mathrm{e}^{x}(1+\sin x)}{1+\cos x}\mathrm{d}x= $ ___.

【分析】被积函数同时含有指数函数与三角函数，可考虑用分部积分法，并注意形成“回归”现象.

解 先拆成两项，对第二项用分部积分法，得

 $$ \begin{aligned}I&=\int_{0}^{\frac{\pi}{2}}\frac{\mathrm{e}^{x}(1+\sin x)}{1+\cos x}\mathrm{d}x=\int_{0}^{\frac{\pi}{2}}\frac{\mathrm{e}^{x}}{1+\cos x}\mathrm{d}x+\int_{0}^{\frac{\pi}{2}}\frac{\sin x}{1+\cos x}\mathrm{d}\mathrm{e}^{x}\\&=\int_{0}^{\frac{\pi}{2}}\frac{\mathrm{e}^{x}}{1+\cos x}\mathrm{d}x+\left.\frac{\mathrm{e}^{x}\sin x}{1+\cos x}\right|_{0}^{\frac{\pi}{2}}\\&=\int_{0}^{\frac{\pi}{2}}\frac{\mathrm{e}^{x}}{1+\cos x}\mathrm{d}x+\left.\frac{\mathrm{e}^{x}\sin x}{1+\cos x}\right|_{0}^{\frac{\pi}{2}}\\&=\mathrm{e}^{\frac{\pi}{2}}.\end{aligned}\begin{aligned}-\int_{0}^{\frac{\pi}{2}}\mathrm{e}^{x}\frac{\cos x(1+\cos x)+\sin^{2}x}{(1+\cos x)^{2}}\mathrm{d}x\\-\int_{0}^{\frac{\pi}{2}}\frac{\mathrm{e}^{x}}{1+\cos x}\mathrm{d}x\end{aligned} $$ 

【例 3.107】（第十二届全国初赛题，2020） 证明： $ f(n)=\sum_{m=1}^{n}\int_{0}^{m}\cos\frac{2\pi n[x+1]}{m}\mathrm{d}x $ 等于 n 的所有因子（包括 1 和 n 本身）之和，其中  $ [x+1] $ 表示不超过  $ x+1 $ 的最大整数，并计算  $ f(2021) $.

【分析】被积函数含有取整函数，往往需考虑分段积分，每一小段的长度为1，再分析在每一个小区间上积分的特征.

证 将积分区间  $ [0, m] $ 等分成 m 个小区间  $ [k-1, k] $,  $ k=1,2,\cdots,m $, 得

 $$ \int_{0}^{m}\cos\frac{2\pi n[x+1]}{m}\mathrm{d}x=\sum_{k=1}^{m}\int_{k-1}^{k}\cos\frac{2\pi n[x+1]}{m}\mathrm{d}x $$ 

 $$ =\sum_{k=1}^{m}\int_{k-1}^{k}\cos\frac{2\pi n k}{m}\mathrm{d}x=\sum_{k=1}^{m}\cos k\frac{2\pi n}{m}. $$ 

如果 m 是 n 的因子，那么  $ \int_{0}^{m}\cos\frac{2\pi n[x+1]}{m}\mathrm{d}x=m; $ 否则，根据三角恒等式

 $$ \sum_{k=1}^{m}\cos kt=\cos\frac{m+1}{2}t\cdot\frac{\sin\frac{mt}{2}}{\sin\frac{t}{2}}, $$ 

有  $ \int_{0}^{m}\cos\frac{2\pi n[x+1]}{m}\mathrm{d}x=\cos\left(\frac{m+1}{2}\cdot\frac{2\pi n}{m}\right)\cdot\frac{\sin\left(\frac{m}{2}\cdot\frac{2\pi n}{m}\right)}{\sin\frac{2\pi n}{2m}}=0 $ ，因此得证.

最后，对于 n = 2021，易知 2021 的所有因子为 1, 43, 47, 2021，因此

 $$ f(2021)=1+43+47+2021=2112. $$ 

【例 3.108】（第十四届全国决赛题，2023）证明下列不等式：

(1) 设  $ x \in [0, \pi] $,  $ t \in [0, 1] $, 则  $ \sin tx \geqslant t \sin x $;

(2) 设 p > 0，则  $ \int_{0}^{\frac{\pi}{2}} |\sin u|^{p} \mathrm{d}u \geqslant \frac{\pi}{2(p+1)}; $

(3) 设  $ x \geqslant 0, p > 0 $，则  $ \int_{0}^{x} |\sin u|^{p} \mathrm{d}u \geqslant \frac{x |\sin x|^{p}}{p+1} $.

证 (1) 令  $ F(t) = \sin xt - t \sin x $，则  $ F(0) = F(1) = 0 $，且  $ F''(t) = -x^2 \sin xt \leqslant 0 $。当  $ x \in [0, \pi] $， $ t \in [0,1] $ 时，有  $ F(t) \geqslant 0 $，即  $ \sin tx \geqslant t \sin x $。

(2) 设 p > 0，令  $ u = \frac{\pi}{2} t $，则

 $$ \int_{0}^{\frac{\pi}{2}}\left|\sin u\right|^{p}\mathrm{d}u=\frac{\pi}{2}\int_{0}^{1}\left|\sin\frac{\pi}{2}t\right|^{p}\mathrm{d}t\geqslant\frac{\pi}{2}\int_{0}^{1}\left|t\sin\frac{\pi}{2}\right|^{p}\mathrm{d}t=\frac{\pi}{2(p+1)}. $$ 

(3) 根据对称性，并利用上述结果，得  $ \int_{0}^{\pi}|\sin u|^{p}\mathrm{d}u=2\int_{0}^{\frac{\pi}{2}}|\sin u|^{p}\mathrm{d}u\geqslant\frac{\pi}{p+1} $.

对于  $ x \geqslant 0 $，存在非负整数 k \geqslant 0，使得  $ x = k\pi + v $，其中  $ v \in [0, \pi) $。根据定积分的周期性特征，有  $ \int_{0}^{k\pi} |\sin u|^{p} \mathrm{d}u = k \int_{0}^{\pi} |\sin u|^{p} \mathrm{d}u $， $ \int_{k\pi}^{x} |\sin u|^{p} \mathrm{d}u = \int_{0}^{v} |\sin u|^{p} \mathrm{d}u $。

类似于第（2）题可证， $ \int_{0}^{v}\left|\sin u\right|^{p}\mathrm{d}u\geqslant\frac{v\left|\sin v\right|^{p}}{p+1} $，因此

 $$ \int_{0}^{x}\left|\sin u\right|^{p}\mathrm{d}u=\int_{0}^{k\pi}\left|\sin u\right|^{p}\mathrm{d}u+\int_{k\pi}^{x}\left|\sin u\right|^{p}\mathrm{d}u=k\int_{0}^{\pi}\left|\sin u\right|^{p}\mathrm{d}u+\int_{0}^{v}\left|\sin u\right|^{p}\mathrm{d}u $$ 

 $$ \geqslant\frac{k\pi}{p+1}+\frac{v\left|\sin v\right|^{p}}{p+1}\geqslant\frac{x\left|\sin x\right|^{p}}{p+1}. $$ 

【例 3.109】（第十四届全国决赛题，2023） 设函数  $ f(x) $ 在闭区间  $ [a,b] $ 上具有一阶连续导数，证明：

 $$ \int_{a}^{b}\sqrt{1+\left[f^{\prime}(x)\right]^{2}}\mathrm{d}x\geqslant\sqrt{(a-b)^{2}+(f(a)-f(b))^{2}}, $$ 

并给出等号成立的条件.

证 令  $ F(t)=\int_{a}^{t}\sqrt{1+\left[f'(x)\right]^{2}}\mathrm{d}x-\sqrt{(t-a)^{2}+(f(t)-f(a))^{2}} $ ，则  $ F(a)=0,F(t) $ 在区间  $ (a,b) $ 内可导，且

 $$ \begin{align*}F^{\prime}(t)&=\sqrt{1+\left[f^{\prime}(t)\right]^{2}}-\frac{(t-a)+(f(t)-f(a))f^{\prime}(t)}{\sqrt{(t-a)^{2}+(f(t)-f(a))^{2}}}\\&=\frac{\sqrt{1+\left[f^{\prime}(t)\right]^{2}}\sqrt{(t-a)^{2}+(f(t)-f(a))^{2}}-\left[(t-a)+(f(t)-f(a))f^{\prime}(t)\right]}{\sqrt{(t-a)^{2}+(f(t)-f(a))^{2}}}.\end{align*} $$ 

根据 Cauchy 不等式，得

 $$ (t-a)\cdot1+(f(t)-f(a))f^{\prime}(t)\leqslant\sqrt{1+\left[f^{\prime}(t)\right]^{2}}\sqrt{(t-a)^{2}+(f(t)-f(a))^{2}}, $$ 

可知  $ F'(t) \geqslant 0 $ 。所以  $ F(t) $ 在  $ [a,b] $ 上单调增加，故  $ F(b) \geqslant F(a) $，即得所证不等式。

进一步, 等号成立当且仅当  $ f'(t)=\frac{f(t)-f(a)}{t-a}=k $ (实常数), 即  $ f(t)=f(a)+k(t-a) $, 此时曲线  $ y=f(x) $ 为直线.

【注】不等式具有明显的几何意义：光滑曲线  $ y = f(x) $ 弧上点  $ A(a, f(a)) $ 与  $ B(b, f(b)) $ 之间的弧长不小于直线段 AB 之长.

### 3.4 能力拓展与训练

1. 求下列不定积分：

(1)

 $$ \int\frac{\tan x}{3\sin^{2}x+2\cos^{2}x}\mathrm{d}x; $$ 

(2)

 $$ \int\frac{x^{2}+1}{x\sqrt{x^{4}+1}}\mathrm{d}x; $$ 

(3)

 $$ \int\frac{\mathrm{d}x}{x^{2}\sqrt{1+x^{2}}}; $$ 

(4)

 $$ \int\frac{\ln x}{x\sqrt{1+\ln x}}\mathrm{d}x; $$ 

(5)

 $$ \int\arctan\sqrt{x}\mathrm{d}x; $$ 

(6)

(7)

 $$ \int x\tan x\sec^{4}x\mathrm{d}x; $$ 

 $$ \int\frac{x\mathrm{e}^{x}}{\sqrt{\mathrm{e}^{x}-2}}\mathrm{d}x; $$ 

(8)

 $$ \int\frac{x^{2}+20}{(x\sin x+5\cos x)^{2}}\mathrm{d}x; $$ 

(9)  $ \int \frac{x+1}{\sqrt{x-x^{2}}} \mathrm{d}x; $

(10)  $ \int \frac{1 + \sin x}{1 + \cos x} \mathrm{e}^{x} \mathrm{d}x; $

(11)  $ \int \frac{\ln(1+\mathrm{e}^{-x})}{1+\mathrm{e}^{x}} \mathrm{d}x; $

12)  $ \int \frac{\mathrm{d}x}{\sin 2x + 2\sin x} $;

(13)  $ \int\frac{\mathrm{d}x}{\left(1+\mathrm{e}^{x}\right)^{2}} $;

(14)  $ \int \frac{e^{\arctan x}}{\sqrt{(1+x^2)^3}} \, dx $;

(15)  $ \int \frac{\mathrm{d}x}{\sin x \cos^{3} x}; $

(16)  $ \int \frac{\sqrt{x}}{1 + \sqrt{1 + x}} \mathrm{d}x; $

(17)  $ \int \frac{\mathrm{d}x}{(2x-1)\sqrt{x-x^{2}}}; $

(18)  $ \int \frac{x^{4}}{x^{4} + 5x^{2} + 4} \, dx $;

(19)  $ \int \frac{\cos x + x \sin x}{(x + \cos x)^2} \mathrm{d}x; $

(20)  $ \int \frac{(1 + x^{2})\arcsin x}{x^{2}\sqrt{1 - x^{2}}}dx. $

2. 求下列定积分：

(1)  $ \int_{0}^{3} x\sqrt{1+x}dx; $

(2)  $ \int_{0}^{\frac{\pi}{2}}\sqrt{1-\sin4x}\mathrm{d}x; $

(3) $ \int_{1}^{3}\frac{\mathrm{d}x}{\sqrt{x}(1+x)}; $

(4)  $ \int_{-2}^{2} \min \left\{ x^{2}, \frac{1}{|x|} \right\} dx; $

(5)  $ \int_{0}^{2a} x^{3}\sqrt{2ax - x^{2}} \mathrm{d}x; $

(6)  $ \int_{0}^{1} x^{2} \ln \left(x + \sqrt{1 + x^{2}}\right) dx; $

(7)  $ \int_{0}^{\pi}\frac{x\sin^{3}x}{1+\cos^{2}x}\mathrm{d}x; $

(8)  $ \int_{0}^{a}\frac{\mathrm{d}x}{x+\sqrt{a^{2}-x^{2}}}(a>0); $

(9)  $ \int_{0}^{1} \mathrm{e}^{x} \frac{(1-x)^{2}}{(1+x^{2})^{2}} \mathrm{d}x; $

(10)  $ \int_{1}^{\sqrt{2}} x^{2} \arctan \sqrt{x^{2}-1} \, dx; $

(11)  $ \int_{-1}^{1} \frac{\sqrt{1-x^{2}}}{a-x} \mathrm{d}x (a > 1) $;

(12)  $ \int_{0}^{\frac{\pi}{4}}\frac{1-\sin2x}{1+\sin2x}dx; $

(13)  $ \int_{0}^{2\pi}\frac{\mathrm{d}x}{1+\cos^{2}x}; $

(14)  $ \int_{0}^{3}\arcsin\sqrt{\frac{x}{1+x}}\mathrm{d}x; $

(15)  $ \int_{-1}^{0} x^{4} \sqrt{\frac{1+x}{1-x}} \mathrm{d}x; $

(16)  $ \int_{0}^{1} x (\arctan x)^{2} \, \mathrm{d}x; $

(17)  $ \int_{0}^{1}\frac{\ln(1+x)}{(2-x)^{2}}\mathrm{d}x; $

(18)  $ \int_{0}^{1}\frac{\sqrt{2x+x^{2}}}{1+x}dx; $

(19)  $ \int_{0}^{\pi}\frac{\cos x}{(5-4\cos x)^{2}}\mathrm{d}x; $

(20)  $ \int_{-\frac{1}{2}}^{\frac{1}{2}}\left[\frac{\sin x}{x^{8}+1}+\sqrt{\ln^{2}(1-x)}\right]\,\mathrm{d}x. $

3. 设  $  f(x) = \int_{1}^{\sqrt{x}} e^{-t^{2}} \, dt  $，求  $ \int_{0}^{1} \frac{f(x)}{\sqrt{x}} \, dx $.

4. 设函数  $ f(x)=\left\{\begin{array}{ll}x^{2}, & 0 \leqslant x \leqslant 1, \\ 2-x, & 1 < x \leqslant 2,\end{array}\right. $  $ F(x)=\int_{0}^{x}f(t)dt $  $ (0 \leqslant x \leqslant 2) $，求  $ F(x) $.

5. 设  $ f(x)=\int_{0}^{x}\frac{\cos x}{1+\sin^{2}x}dx $，求  $ \int_{0}^{\frac{\pi}{2}}\frac{f'(x)}{1+f^{2}(x)}dx $.

6. 设  $ f(x)=\int_{1}^{x}\frac{\ln t}{1+t}dt $，其中 x>0，求  $ f(x)+f\left(\frac{1}{x}\right) $.

7. 求下列广义积分：

(1) $ \int_{1}^{+\infty}\frac{\mathrm{d}x}{x\sqrt{x-1}}; $

(2) $ \int_{0}^{+\infty}\frac{\mathrm{d}x}{\left(1+x^{2}\right)\left(4+x^{2}\right)}; $

(3) $ \int_{0}^{+\infty}\frac{\arctan x}{\left(1+x^{2}\right)^{3/2}}\mathrm{d}x; $

(4)  $ \int_{0}^{+\infty}\frac{x\mathrm{e}^{x}}{\left(1+\mathrm{e}^{x}\right)^{2}}\mathrm{d}x; $

(5) $ \int_{0}^{1}\ln\frac{1}{1-x^{2}}\mathrm{d}x; $

(6)  $ \int_{0}^{1}\frac{\arcsin\sqrt{x}}{\sqrt{x(1-x)}}dx; $

(7)  $ \int_{2}^{4}\frac{x\mathrm{d}x}{\sqrt{\left|x^{2}-9\right|}}; $

(8)  $ \int_{0}^{\frac{\pi}{6}}\frac{\mathrm{d}x}{\cos x\sqrt{\sin x}}; $

(9)  $ \int_{0}^{\pi}\frac{\mathrm{d}x}{2+\tan^{2}x}; $

(10)  $ \int_{0}^{1} x^{2} \ln^{3} \frac{1}{x} \mathrm{d}x. $

8. 设  $ \int_{x}^{2\ln2}\frac{dt}{\sqrt{e^{t}-1}}=\frac{\pi}{6} $，求 x.

9. 设  $ f(x)=\left\{\begin{array}{ll}1+x^{2}, & x<0, \\ \mathrm{e}^{-x}, & x\geqslant0,\end{array}\right. $ 求  $ I=\int_{1}^{3}f(x-2)\mathrm{d}x $.

10. 设  $ f(x)=x,x \geqslant 0 $;

 $$ g(x)=\left\{\begin{array}{ll}\sin x,&0\leqslant x\leqslant\frac{\pi}{2},\\0,&x>\frac{\pi}{2}.\end{array}\right. $$ 

分别求当  $ 0 \leqslant x \leqslant \frac{\pi}{2} $ 与  $ x > \frac{\pi}{2} $ 时积分  $ \int_{0}^{x} f(t) g(x - t) dt $ 的表达式.

11. 设  $ 0 \leqslant x \leqslant \frac{\pi}{2} $,  $ f(x) = \int_{0}^{\sin^{2}x} \arcsin \sqrt{t} \, \mathrm{d}t + \int_{0}^{\cos^{2}x} \arccos \sqrt{t} \, \mathrm{d}t $, 求  $ f(x) $.

12. 设  $ f(2)=\frac{1}{2} $,  $ f'(2)=0 $,  $ \int_{0}^{2}f(x)dx=1 $, 求  $ \int_{0}^{1}x^{2}f''(2x)dx $.

13. 设  $ f'(\ln x) = \left\{ \begin{array}{ll} 1, & 0 < x \leq 1, \\ x, & x > 1, \end{array} \right. $ 且  $ f(0) = 0 $，试求函数  $ f(x) $.

14. 已知  $ f'(\sin^{2}x) = \cos 2x + \tan^{2}x $，当 0 < x < 1 时，求  $ f(x) $.

15. 设  $ f(x) $ 在  $ [0,1] $ 上连续，且满足  $ f(x)=\mathrm{e}^{x}+x\int_{0}^{1}f(\sqrt{x})\mathrm{d}x $，求函数  $ f(x) $.

16. 已知曲线  $ y = f(x) $ 在任意点处的切线的斜率为  $ 3x^{2} - 3x - 6 $，且  $ f(2) = -8 $ 是  $ f(x) $ 的极小值。试确定  $ f(x) $，并求  $ f(x) $ 的极大值。

17. 设  $ f(x)=\int_{x}^{x+\frac{\pi}{2}}|\sin t|dt. $

(1) 证明： $ f(x + \pi) = f(x) $;

(2) 求  $ f(x) $ 的最大值和最小值.

18. 设  $ f(x^{2}-1)=\ln\frac{x^{2}}{x^{2}-2} $，且  $ f[\varphi(x)]=\ln x $，求  $ \int\varphi(x)\mathrm{d}x $.

19. 设  $ f(x) $ 在  $ (-\infty, +\infty) $ 上连续，满足  $ f(x) = (x+1)\int_{0}^{x^2} f(t) \, dt + 2. $ 试证： $ f(x) $ 在 x = 0 处取极小值.

20. 设  $ f(x)=\left\{\begin{array}{ll}\frac{\lambda}{\sqrt{1-x^{2}}},&|x|<1,\\0,& 其他 ,\end{array}\right.\int_{-\infty}^{+\infty}f(x)dx=1 $ ，求  $ \lambda $.

21. 已知  $ \int_{0}^{+\infty}\frac{\sin x}{x}\mathrm{d}x=\frac{\pi}{2} $，求 (1)  $ \int_{0}^{+\infty}\left(\frac{\sin x}{x}\right)^{2}\mathrm{d}x $; (2)  $ \int_{0}^{+\infty}\frac{\sin x\cos ax}{x}\mathrm{d}x $.

22. 已知  $ I(a)=\int_{0}^{\pi}\frac{\sin x}{\sqrt{1-2a\cos x+a^{2}}}dx $，求  $ I(a) $ 及  $ \int_{-3}^{2}I(a)da $.

23. 已知  $ f(x) $ 的一个原函数为  $ \frac{\sin x}{x} $，求  $ \int x f'(x) \, dx $.

24. 设  $ \int_{0}^{\pi}\left[f(x)+f''(x)\right]\sin x\mathrm{d}x=5,f(\pi)=2 $ ，求  $ f(0) $

25. 设对一切实数 t,  $ f(t) $ 连续，且  $ f(t) > 0 $,  $ f(-t) = f(t) $. 对于函数

 $$ F(x)=\int_{-a}^{a}|x-t|f(t)\mathrm{d}t,\quad-a\leqslant x\leqslant a, $$ 

试回答下列问题:

(1) 证明  $ F'(x) $ 单调增加;

(2) 当 x 为何值时， $ F(x) $ 取得最小值；

(3) 若  $ F(x) $ 的最小值可表示为  $ f(a)-a^{2}-1 $，试求  $ f(t) $.

26. 设  $ f(2x+a)=xe^{\frac{x}{b}} $ (a,b 是常数,  $ b \neq 0 $),  $ f(x) $ 是连续函数.

(1) 求  $ \int_{a+2b}^{y} f(t) dt $.

(2) 求常数 a 和 b 的值，使对任何 y，都有  $ 2a\int_{a+2b}^{y}f(t)dt=2af(y)-\mathrm{e}^{\frac{1}{2b}(y-a)}. $

27. 设  $ f(x)=\int_{1}^{x}e^{-t^{2}}dt $，求  $ \int_{0}^{1}x^{2}f(x)dx $.

28. 设  $ f(\ln x) = \frac{\ln(1+x)}{x} $，计算  $ \int f(x) \, dx $.

29. 设  $ F(x) $ 为  $ f(x) $ 的原函数，且当  $ x \geqslant 0 $ 时， $ f(x)F(x)=\frac{x\mathrm{e}^{x}}{2(1+x)^{2}} $. 已知  $ F(0)=1, F(x)>0 $. 试求  $ f(x) $.

30. 已知  $ f(x) $ 在区间  $ [0,\pi] $ 上非负连续，且满足  $ f(x)\int_{0}^{x}f(x-t)dt=x\sin^{2}x $，求  $ \int_{0}^{\pi}f(x)dx $ 的值.

31. 求极限： $ \lim_{x \to +\infty} \frac{1}{x} \int_0^x (t - t)^2 \, dt $，其中  $ [t] $ 为取整函数.

32. 求极限： $ \lim_{n\to\infty}\frac{1}{n}\sum_{i=1}^{n}\left(\left[\frac{2n}{i}\right]-2\left[\frac{n}{i}\right]\right) $.

33. 求极限： $ \lim_{n \to \infty} \int_0^n (\{x\}^n + \{-x\}^n) \, \mathrm{d}x $，其中  $ \{x\} = x - [x] $.

34. 设 D 是由曲线  $ y = \sqrt{1 - x^{2}} (0 \leqslant x \leqslant 1) $ 与  $ \left\{\begin{array}{l} x = \cos^{3} t, \\ y = \sin^{3} t \end{array}\right. $  $ (0 \leqslant t \leqslant \frac{\pi}{2}) $ 围成的平面区域，求 D 绕 x 轴旋转一周所得旋转体的体积和表面积.

35. 设 D 是由曲线  $ y = x^{\frac{1}{3}} $，直线 x = a (a > 0) 及 x 轴所围成的平面图形， $ V_{x}, V_{y} $ 分别是 D 绕 x 轴、y 轴旋转一周所得旋转体的体积，满足  $ V_{x} = 10V_{y} $，求 a 的值.

36. 已知  $ f(x) $ 在  $ \left[0,\frac{3\pi}{2}\right] $ 上连续，在  $ \left(0,\frac{3\pi}{2}\right) $ 内是函数  $ \frac{\cos x}{2x-3\pi} $ 的一个原函数， $ f(0)=0 $.

(1) 求  $ f(x) $ 在区间  $ \left[0, \frac{3\pi}{2}\right] $ 上的平均值;

(2) 证明  $ f(x) $ 在区间  $ \left(0, \frac{3\pi}{2}\right) $ 内存在唯一零点.

37. 设  $ f(x) $ 是连续正值函数，证明：

 $$ \int_{0}^{1}\ln f(x+t)\mathrm{d}t=\int_{0}^{x}\ln\frac{f(u+1)}{f(u)}\mathrm{d}u+\int_{0}^{1}\ln f(u)\mathrm{d}u. $$ 

38. 设  $ f(x) $ 是连续函数, 试证:

 $$ \lim_{h\to0}\frac{1}{h}\int_{a}^{x}[f(t+h)-f(t)]\mathrm{d}t=f(x)-f(a). $$ 

39. 证明： $ \int_{0}^{\frac{\pi}{2}}\cos^{n}x\sin nx dx=\frac{1}{2^{n+1}}\left(\frac{2}{1}+\frac{2^{2}}{2}+\cdots+\frac{2^{n}}{n}\right) $，其中n为自然数.

40. 设  $ f(x)=[2x]-2[x] $,  $ x\in[1,+\infty) $.

(1) 证明： $ \int_{1}^{+\infty}\frac{f(x)}{x^{2}}\mathrm{d}x $ 收敛.

(2) 计算:  $ \int_{1}^{+\infty}\frac{f(x)}{x^{2}}\mathrm{d}x. $

41. 设函数  $ f(x) $,  $ g(x) $ 在区间  $ [a, b] $ 上连续，且  $ f(x) $ 单调增加， $ 0 \leqslant g(x) \leqslant 1 $. 证明：

 $$ \int_{a}^{a+\int_{a}^{b}g(t)\mathrm{d}t}f(x)\mathrm{d}x\leqslant\int_{a}^{b}f(x)g(x)\mathrm{d}x. $$ 

42. 设函数  $ \varphi(x) $ 具有二阶导数，且满足  $ \varphi(2) > \varphi(1), \varphi(2) > \int_{2}^{3} \varphi(x) \, dx $，则至少存在一点  $ \xi \in (1,3) $，使得  $ \varphi''(\xi) < 0 $。

43. 计算定积分： $ \int_{0}^{\ln2}\frac{x\mathrm{e}^{x}}{\mathrm{e}^{x}+1}\mathrm{d}x+\int_{\ln2}^{\ln3}\frac{x\mathrm{e}^{x}}{\mathrm{e}^{x}-1}\mathrm{d}x $

44. 求由曲线  $ \left|\ln x\right| + \left|\ln y\right| = 1 $ 所围成的平面图形的面积.

45. 求由曲线  $ y^{2}=x^{2}-x^{4} $ 所围成的平面图形的面积.

46. 设  $ y = f(x) $ 是由方程  $ \arctan \frac{x}{y} = \ln \sqrt{x^{2} + y^{2}} - \frac{1}{2} \ln 2 + \frac{\pi}{4} $ 确定的函数，且满足  $ f(1) = 1 $.

(1) 求曲线  $ y = f(x) $ 在点 (1, 1) 处的曲率;

(2) 求定积分:  $ \int_{0}^{1}\frac{x-f(x)}{x+f(x)}\mathrm{d}x $.

47. 设抛物线  $ y = ax^{2} + bx + c $ 通过（0, 0）和（1, 2）两点，其中 a < -2。试求 a, b, c 的值，使得该抛物线与曲线  $ y = -x^{2} + 2x $ 所围成区域的面积最小。

48. 设  $ f(x) $ 是  $ (-\infty, +\infty) $ 上以 T > 0 为周期的连续函数，证明：

 $$ \lim_{n\to\infty}n\int_{n}^{+\infty}\frac{f(x)}{x^{2}}\mathrm{d}x=\frac{1}{T}\int_{0}^{T}f(x)\mathrm{d}x. $$ 

49. 设曲线  $ y = \cos x \left(0 \leqslant x \leqslant \frac{\pi}{2}\right) $ 与 x 轴、y 轴所围成的平面区域被曲线  $ y = a \sin x, y = b \sin x (a > b > 0) $ 分割成面积相等的三部分，试确定 a, b 之值.

50. 设点 A 位于半径为 a 的圆周内部，且离圆心的距离为 b ( $ 0 \leq b < a $)，从点 A 向圆周上所有点的切线作垂线，求所有垂足所围成的图形的面积.

51. 设  $ f(x) $,  $ g(x) $ 在  $ [0,1] $ 上具有连续的导数，且  $ f(0)=0 $,  $ f'(x)\geqslant0 $,  $ g'(x)\geqslant0 $. 证明：对任何  $ a\in[0,1] $，有

 $$ \int_{0}^{a}g(x)f^{\prime}(x)\mathrm{d}x+\int_{0}^{1}f(x)g^{\prime}(x)\mathrm{d}x\geqslant f(a)g(1). $$ 

52. 设  $ f(x) $ 在  $ [0,1] $ 上连续可导， $ f(0)=0,0\leq f'(x)\leq1 $. 证明：

 $$ \left[\int_{0}^{1}f(x)\mathrm{d}x\right]^{2}\geqslant\int_{0}^{1}f^{3}(x)\mathrm{d}x, $$ 

当且仅当  $ f(x)=x $ 或者 0 时等号成立.

53. 设  $ f(x) $ 在  $ [a,b] $ 上有连续的导数，记  $ A=\frac{1}{b-a}\int_{a}^{b}f(x)\mathrm{d}x $ 。试证明：

 $$ \int_{a}^{b}[f(x)-A]^{2}\mathrm{d}x\leqslant(a-b)^{2}\int_{a}^{b}\left|f^{\prime}(x)\right|^{2}\mathrm{d}x. $$ 

54. 设  $ f(x) $ 在  $ [a,b] $ 上有连续的导数，且  $ f(a)=0 $。求证：

 $$ \int_{a}^{b}f^{2}(x)\mathrm{d}x\leqslant\frac{(a-b)^{2}}{2}\int_{a}^{b}\left[f^{\prime}(x)\right]^{2}\mathrm{d}x. $$ 

55. 设 A, B 是曲线  $ L: y = \ln x $ 上的任意两点，过 AB 的中点且平行于 y 轴的直线交曲线 L 于 Q. 试证明：直线 AB 的斜率大于曲线 L 在 Q 点处的切线的斜率.

56. 证明： $ \int_{0}^{1}\sin x^{a}dx>\int_{0}^{1}\sin^{a}x dx $，其中 a>1.

57. 证明： $ \int_{0}^{\frac{\pi}{2}}\left(e^{\sin x}+e^{-\sin x}\right)dx>\frac{81}{64}\pi $

58. 设  $ f(x) $ 在  $ [0,1] $ 上有连续的导数,  $ f(0)=f(1)=-\frac{1}{6} $. 证明:

 $$ \int_{0}^{1}\left|f^{\prime}(x)\right|^{2}\mathrm{d}x\geqslant2\int_{0}^{1}f(x)\mathrm{d}x+\frac{1}{4}. $$ 

59. 设  $ 0 \leq a, b, c \leq 1 $，证明不等式：

 $$ \frac{a}{b+c+1}+\frac{b}{c+a+1}+\frac{c}{a+b+1}+(1-a)(1-b)(1-c)\leqslant1. $$ 

60. 设  $ f(x) $ 是区间  $ [a,b] $ 上的连续函数,  $ \lambda $ 是一实数, 且对任意  $ x\in(a,b) $, 恒有

 $$ f(x)=\frac{3}{b-a}+\lambda\int_{x}^{b}f(t)f(a+t-x)\mathrm{d}t. $$ 

证明： $ \lambda \leqslant \frac{1}{6} $

61. 设  $ f(x) $ 是  $ [0,1] $ 上的单调减、正值连续函数. 证明：

 $$ \frac{\int_{0}^{1}xf^{2}(x)\mathrm{d}x}{\int_{0}^{1}xf(x)\mathrm{d}x}\leqslant\frac{\int_{0}^{1}f^{2}(x)\mathrm{d}x}{\int_{0}^{1}f(x)\mathrm{d}x}. $$ 

62. 设  $ f(x) $ 在区间  $ [0,1] $ 上有连续的二阶导数，且  $ \left|f''(x)\right| \leqslant 1 $。又设  $ \int_{0}^{1} f(x) \, dx = \int_{0}^{1} x f(x) \, dx = 0 $，证明  $ \left|\int_{0}^{1} x^{2} f(x) \, dx\right| \leqslant \frac{1}{360} $，并给出一个使得等号成立的函数  $ f(x) $。

63. 设  $ f(x), g(x) $ 都是区间  $ [a, b] $ 上的连续函数，且对任意  $ x \in [a, b] $，有  $ g(x) > 0 $。由积分第一中值定理可知，对任意  $ x \in (a, b) $，有  $ \int_{a}^{x} f(t) g(t) \, \mathrm{d}t = f(\xi) \int_{a}^{x} g(t) \, \mathrm{d}t $，其中  $ a \leq \xi \leq x < b $。已知  $ f_{+}'(a) $ 存在且不等于零，求极限： $ \lim_{x \to a^{+}} \frac{\xi - a}{x - a} $。

64. 设  $ f(x) $ 在区间  $ [-1,1] $ 上有连续的二阶导数，证明：存在  $ \xi \in [-1,1] $，使得

 $$ \int_{-1}^{1}x f(x)\mathrm{d}x=\frac{1}{3}\left[2f^{\prime}(\xi)+\xi f^{\prime \prime}(\xi)\right]. $$ 

65. 设  $ f(x) $ 是  $ [a,b] $ 上的连续函数，满足

 $$ \int_{a}^{b}f(x)\mathrm{d}x=\int_{a}^{b}x f(x)\mathrm{d}x=\int_{a}^{b}x^{2}f(x)\mathrm{d}x=0. $$ 

证明： $ f(x) $ 在  $ (a,b) $ 内至少有三个零点.

66. 求抛物线  $ y = x^{2} $ 与直线 y = kx (k > 0) 围成的平面图形绕该直线旋转所成旋转体的体积.

### 3.5 训练全解与分析

1. (1)  $ \frac{1}{6}\ln\left(3\tan^{2}x+2\right)+C $; (2)  $ \frac{1}{2}\ln\left(x^{2}+\sqrt{1+x^{4}}\right)+\frac{1}{2}\ln\left(\sqrt{1+x^{4}}-1\right)-\ln x+C $;

 $$ -\frac{1}{x}\sqrt{1+x^{2}}+C; $$ 

(4) $ \frac{2}{3}\sqrt{1+\ln x}(\ln x-2)+C; $

(5) $ (x+1)\arctan\sqrt{x}-\sqrt{x}+C; $ (6) $ \frac{1}{4}x\sec^{4}x-\frac{1}{12}\tan^{3}x-\frac{1}{4}\tan x+C; $

 $$ 2(x-2)\sqrt{\mathrm{e}^{x}-2}+4\sqrt{2}\arctan\sqrt{\frac{\mathrm{e}^{x}}{2}-1}+C;\quad(8)\frac{5\sin x-x\cos x}{x\sin x+5\cos x}+C; $$ 

 $$ (9)\ \frac{3}{2}\arcsin(2x-1)-\sqrt{x-x^{2}}+C;\quad(10)\ \frac{\mathrm{e}^{x}\sin x}{1+\cos x}+C; $$ 

(11)  $ -\frac{1}{2}\ln^{2}\left(1+\mathrm{e}^{-x}\right)+C;\quad(12)\frac{1}{4}\left(\ln\left|\tan\frac{x}{2}\right|+\frac{1}{2}\tan^{2}\frac{x}{2}\right)+C; $

 $$ x-\ln\left(1+\mathrm{e}^{x}\right)+\frac{1}{1+\mathrm{e}^{x}}+C;\quad(14)\frac{(x+1)\mathrm{e}^{\arctan x}}{2\sqrt{1+x^{2}}}+C; $$ 

(15) $ \frac{1}{2}\tan^{2}x+\ln|\tan x|+C $; (16) $ \sqrt{x(x+1)}+\ln(\sqrt{x}+\sqrt{1+x})-2\sqrt{x}+C $;

 $$ \ln\left|\frac{\sqrt{1-x}-\sqrt{x}}{\sqrt{1-x}+\sqrt{x}}\right|+C;\quad(18)x+\frac{1}{3}\arctan x-\frac{8}{3}\arctan\frac{x}{2}+C; $$ 

 $$ \textcircled{j}\frac{x}{x+\cos x}+C;\quad(20)\;-\frac{\sqrt{1-x^{2}}}{x}\arcsin x+\ln\left|x\right|+\frac{1}{2}(\arcsin x)^{2}+C. $$ 

2. (1) $ \frac{116}{15} $; (2) $ \sqrt{2} $; (3) $ \frac{\pi}{6} $; (4) $ 2\left(\frac{1}{3}+\ln2\right) $; (5)

 $$ (6)\ \frac{1}{3}\ln(1+\sqrt{2})+\frac{1}{9}(\sqrt{2}-2);\quad(7)\ \left(\frac{\pi}{2}-1\right)\pi;\quad(8)\ \frac{\pi}{4}; $$ 

(9)  $ \frac{e}{2} - 1 $; (10)  $ \frac{1}{6}[\sqrt{2}(\pi - 1) - \ln(1 + \sqrt{2})] $; (11)  $ \pi\left(a - \sqrt{a^2 - 1}\right) $;

(12)  $ 1 - \frac{\pi}{4} $; (13)  $ \sqrt{2}\pi $; (14)  $ \frac{4\pi}{3} - \sqrt{3} $; (15)  $ \frac{3\pi}{16} - \frac{8}{15} $;

(16) $ \frac{\pi}{4}\left(\frac{\pi}{4}-1\right)+\frac{1}{2}\ln2;\quad(17)\frac{1}{3}\ln2; $ (18) $ \sqrt{3}-\frac{\pi}{3}; $

(19) $ \frac{4\pi}{27};\quad(20)\frac{3}{2}\ln3-2\ln2. $

3.  $ \frac{1}{e}-1 $. 4. 当  $ 0 \leqslant x \leqslant 1 $ 时,  $ F(x) = \frac{x^{3}}{3} $; 当 1 < x \leqslant 2 时,  $ F(x) = -\frac{x^{2}}{2} + 2x - \frac{7}{6} $.

4.  $ \arctan \frac{\pi}{4} $. 6.  $ \frac{1}{2}(\ln x)^{2} $.

5. (1)  $ \pi $; (2)  $ \frac{\pi}{12} $; (3)  $ \frac{\pi}{2} - 1 $; (4)  $ \ln 2 $; (5)  $ 2 - 2\ln 2 $; (6)  $ \frac{\pi^{2}}{4} $;

(7)  $ \sqrt{5} + \sqrt{7} $; (8)  $ \ln(1 + \sqrt{2}) + \arctan\frac{\sqrt{2}}{2} $; (9)  $ \pi\left(1 - \frac{1}{\sqrt{2}}\right) $; (10)  $ \frac{2}{27} $.

8.  $ \ln 2 $. 9.  $ \frac{7}{3} - \frac{1}{e} $. 10. 当  $ 0 \leqslant x \leqslant \frac{\pi}{2} $ 时,  $ x - \sin x $; 当  $ x > \frac{\pi}{2} $ 时, x - 1.

9.  $ \frac{\pi}{4} $. 12. 0. 13.  $ x(x \leqslant 0) $,  $ \mathrm{e}^{x} - 1 (x > 0) $. 14.  $ -x^{2} - \ln(1 - x) + C $.

 $$ f(x)=\mathrm{e}^{x}+6x.\quad16.f(x)=x^{3}-\frac{3}{2}x^{2}-6x+2,f(-1)=\frac{11}{2}. $$ 

10. (1) 略; (2)  $ \sqrt{2} $,  $ 2 - \sqrt{2} $. 18.  $ 2\ln|x - 1| + x + C $. 19. 略. 20.  $ \frac{1}{\pi} $.

11. (1) $ \frac{\pi}{2} $. (2)当 $ |a|<1 $时, $ \frac{\pi}{2} $;当 $ |a|=1 $时, $ \frac{\pi}{4} $;当 $ |a|>1 $时,0.

12. 当 a < -1 时， $ I(a) = -\frac{2}{a} $; 当 -1  $ \leqslant a \leqslant 1 $ 时， $ I(a) = 2 $; 当 a > 1 时， $ I(a) = \frac{2}{a} $ (注意：当  $ a = \pm 1 $ 时属广义积分);  $ 2\ln 6 + 4 $.

13.  $ \cos x - \frac{2}{x}\sin x + C $. 24. 3. 25. (1) 略; (2)  $ F(0) $ 是最小值; (3)  $ f(t) = 2e^{t^2} - 1 $.

14. (1)  $ b(y - a - 2b)e^{\frac{y - a}{2b}};\quad(2)\ a = 1, b = \frac{1}{2}.\quad27.\quad\frac{1}{6}\left(2\mathrm{e}^{-1} - 1\right). $

 $$ 28.\ x-\left(1+\mathrm{e}^{-x}\right)\ln\left(1+\mathrm{e}^{x}\right)+C.\quad29.\ \frac{x\mathrm{e}^{\frac{x}{2}}}{2(1+x)^{\frac{3}{2}}}. $$ 

15. 对题设等式两边同时在  $ [0,\pi] $ 上积分，得

 $$ \int_{0}^{\pi}f(x)\mathrm{d}x\int_{0}^{x}f(x-t)\mathrm{d}t=\int_{0}^{\pi}x\sin^{2}x\mathrm{d}x. $$ 

对①式左边，令 u = x - t，则  $ \int_{0}^{x} f(x - t) dt = \int_{0}^{x} f(u) du $。再根据重积分的对称性，得

左边  $ \int_{0}^{\pi} f(x) dx \int_{0}^{x} f(u) du = \frac{1}{2} \int_{0}^{\pi} f(x) dx \int_{0}^{\pi} f(u) du = \frac{1}{2} \left( \int_{0}^{\pi} f(x) dx \right)^{2} $.

对①式右边，利用公式得

对①式右边，利用公式得

 $$ \int_{0}^{\pi}x\sin^{2}x\mathrm{d}x=\frac{\pi}{2}\int_{0}^{\pi}\sin^{2}x\mathrm{d}x=\frac{\pi}{2}\int_{0}^{\pi}\frac{1-\cos2x}{2}\mathrm{d}x=\frac{\pi^{2}}{4}. $$ 

代入 $ ^{①} $式，得

 $$ \frac{1}{2}\left(\int_{0}^{\pi}f(x)\mathrm{d}x\right)^{2}=\frac{\pi^{2}}{4}. $$ 

两边开平方，并注意到  $ f(x) $ 的非负性，得  $ \int_{0}^{\pi}f(x)\mathrm{d}x=\frac{\sqrt{2}\pi}{2} $.

31. 当  $ n \leq x < n + 1 $ 时，有

 $$ \begin{align*}\int_{0}^{x}(t-[t])^{2}\mathrm{d}t&=\sum_{k=0}^{n-1}\int_{k}^{k+1}(t-[t])^{2}\mathrm{d}t+\int_{n}^{x}(t-[t])^{2}\mathrm{d}t\\&=\sum_{k=0}^{n-1}\int_{k}^{k+1}(t-k)^{2}\mathrm{d}t+\int_{n}^{x}(t-n)^{2}\mathrm{d}t\\&=\frac{1}{3}\left[n+(x-n)^{2}\right],\end{align*} $$ 

所以

 $$ \frac{n}{3(n+1)}\leqslant\frac{1}{x}\int_{0}^{x}(t-[t])^{2}\mathrm{d}t\leqslant\frac{n+1}{3n}. $$ 

显然  $ \lim_{n\to\infty}\frac{n}{3(n+1)}=\lim_{n\to\infty}\frac{n+1}{3n}=\frac{1}{3} $，且  $ x\to+\infty $ 等价于  $ n\to\infty $。利用夹逼准则，得

 $$ \lim_{x\to+\infty}\frac{1}{x}\int_{0}^{x}(t-[t])^{2}\mathrm{d}t=\frac{1}{3}. $$ 

32. 首先，根据定积分的定义，有

 $$ \begin{align*}I&=\lim_{n\to\infty}\frac{1}{n}\sum_{i=1}^{n}\left(\left[\frac{2n}{i}\right]-2\left[\frac{n}{i}\right]\right)=\int_{0}^{1}\left(\left[\frac{2}{x}\right]-2\left[\frac{1}{x}\right]\right)\mathrm{d}x\\&=\sum_{n=1}^{\infty}\int_{\frac{1}{n+1}}^{\frac{1}{n}}\left(\left[\frac{2}{x}\right]-2\left[\frac{1}{x}\right]\right)\mathrm{d}x.\end{align*} $$ 

当  $ \frac{1}{n+1} < x \leqslant \frac{1}{n} $ 时， $ n \leqslant \frac{1}{x} < n+1 $，所以  $ 2\left[\frac{1}{x}\right]=2n $；另一方面，由于  $ 2n \leqslant \frac{2}{x} < 2n+2 $，再分为两种情形： $ 2n \leqslant \frac{2}{x} < 2n+1 $ 和  $ 2n+1 \leqslant \frac{2}{x} < 2n+2 $。易知

 $$ \left[\frac{2}{x}\right]=\left\{\begin{array}{ll}2n+1,&\frac{1}{n+1}<x\leqslant\frac{2}{2n+1},\\2n,&\frac{2}{2n+1}<x\leqslant\frac{1}{n},\end{array}\right. $$ 

 $$ \begin{aligned}\int_{\frac{1}{n+1}}^{\frac{1}{n}}\left(\left[\frac{2}{x}\right]-2\left[\frac{1}{x}\right]\right)\mathrm{d}x&=\int_{\frac{1}{n+1}}^{\frac{2}{2n+1}}\left(\left[\frac{2}{x}\right]-2\left[\frac{1}{x}\right]\right)\mathrm{d}x+\int_{\frac{2}{2n+1}}^{\frac{1}{n}}\left(\left[\frac{2}{x}\right]-2\left[\frac{1}{x}\right]\right)\mathrm{d}x\\&=\int_{\frac{1}{n+1}}^{\frac{2}{2n+1}}[(2n+1)-2n]\mathrm{d}x+\int_{\frac{2}{2n+1}}^{\frac{1}{n}}[2n-2n]\mathrm{d}x\\&=\frac{2}{2n+1}-\frac{1}{n+1}.\end{aligned} $$ 

因此

 $$ \begin{aligned}I&=\sum_{n=1}^{\infty}\left(\frac{2}{2n+1}-\frac{1}{n+1}\right)=2\sum_{n=1}^{\infty}\left(\frac{1}{2n+1}-\frac{1}{2n+2}\right)\\&=2\sum_{n=1}^{\infty}(-1)^{n-1}\frac{1}{n}-2\left(1-\frac{1}{2}\right)=2\ln2-1.\end{aligned} $$ 

33. 记  $ I_{n}=\int_{0}^{n}\left(\{x\}^{n}+\{-x\}^{n}\right)\mathrm{d}x $，注意到  $ \{x\}^{n}+\{-x\}^{n} $ 是周期等于 1 的周期函数，利用定积分的周期性特征，得

 $$ \begin{aligned}I_{n}&=\sum_{k=1}^{n}\int_{k-1}^{k}(\{x\}^{n}+\{-x\}^{n})\mathrm{d}x=\sum_{k=1}^{n}\int_{0}^{1}(\{x\}^{n}+\{-x\}^{n})\mathrm{d}x\\&=n\int_{0}^{1}(\{x\}^{n}+\{-x\}^{n})\mathrm{d}x=n\int_{0}^{1}(x^{n}+(1-x)^{n})\mathrm{d}x\\&=\frac{2n}{n+1}.\\ \end{aligned} $$ 

所以  $ \lim_{n\to\infty}I_n=\lim_{n\to\infty}\frac{2n}{n+1}=2 $

34.  $ \frac{18\pi}{35},\frac{16\pi}{5}. $ 35.  $ a=7\sqrt{7}. $ 36.(1) $ \frac{1}{3\pi} $;(2)略.

35. 即证

 $$ \begin{align*}\int_{0}^{1}\ln f(x+t)\mathrm{d}t&=\int_{0}^{x}\ln f(u+1)\mathrm{d}u-\int_{0}^{x}\ln f(u)\mathrm{d}u+\int_{0}^{1}\ln f(u)\mathrm{d}u\\&=\int_{0}^{x}\ln f(u+1)\mathrm{d}u+\int_{x}^{1}\ln f(u)\mathrm{d}u.\end{align*} $$ 

下面只需把左端的积分变换成右端的两个积分即可. 作变量代换:  $ x + t = u + 1 $, 则

 $$ \begin{aligned}\int_{0}^{1}\ln f(x+t)\mathrm{d}t&=\int_{x-1}^{x}\ln f(u+1)\mathrm{d}u=\int_{x}^{x+1}\ln f(u)\mathrm{d}u\\&=\int_{1}^{x+1}\ln f(u)\mathrm{d}u+\int_{x}^{1}\ln f(u)\mathrm{d}u\\&=\int_{0}^{x}\ln f(u+1)\mathrm{d}u+\int_{x}^{1}\ln f(u)\mathrm{d}u.\end{aligned} $$ 

38. 对等式左端第一项作变量代换： $ u = t + h $，得  $ \int_{a}^{x} f(t + h) dt = \int_{a + h}^{x + h} f(u) du $，利用 L'Hospital 法则，并结合对积分上限求导法则，得

 $$ \lim_{h\to0}\frac{1}{h}\int_{a}^{x}[f(t+h)-f(t)]\mathrm{d}t=\lim_{h\to0}\frac{\int_{a+h}^{x+h}f(u)\mathrm{d}u-\int_{a}^{x}f(t)\mathrm{d}t}{h} $$ 

 $$ \begin{aligned}&=\lim_{h\to0}[f(x+h)-f(a+h)]\\&=f(x)-f(a).\end{aligned} $$ 

39. 记  $ I_{n}=\int_{0}^{\frac{\pi}{2}}\cos^{n}x\sin nxdx $，利用分部积分，得

 $$ \begin{align*}I_{n}&=-\frac{1}{n}\cos^{n}x\cos nx\Big|_{0}^{\frac{\pi}{2}}-\int_{0}^{\frac{\pi}{2}}\cos^{n-1}x\sin x\cos nx\mathrm{d}x\\&=\frac{1}{n}-\int_{0}^{\frac{\pi}{2}}\cos^{n-1}x\sin x\cos nx\mathrm{d}x.\end{align*} $$ 

把上式与原式相加，得

 $$ \begin{aligned}2I_{n}&=\frac{1}{n}+\int_{0}^{\frac{\pi}{2}}\cos^{n-1}x(\cos x\sin nx-\sin x\cos nx)\mathrm{d}x\\&=\frac{1}{n}+\int_{0}^{\frac{\pi}{2}}\cos^{n-1}x\sin(n-1)x\mathrm{d}x\\&=\frac{1}{n}+I_{n-1}.\\ \end{aligned} $$ 

所以  $ 2^{n+1}I_{n}=\frac{2^{n}}{n}+2^{n}I_{n-1} $. 由此递推，并注意到  $ I_{1}=\int_{0}^{\frac{\pi}{2}}\cos x\sin x dx=\frac{1}{2} $，可得

 $$ \begin{align*}2^{n+1}I_{n}&=\frac{2^{n}}{n}+\left(\frac{2^{n-1}}{n-1}+2^{n-1}I_{n-2}\right)\\&=\frac{2^{n}}{n}+\frac{2^{n-1}}{n-1}+\cdots+\frac{2^{2}}{2}+\frac{2}{1}.\end{align*} $$ 

这就证明了等式： $ I_{n}=\frac{1}{2^{n+1}}\left(\frac{2}{1}+\frac{2^{2}}{2}+\cdots+\frac{2^{n}}{n}\right) $

40. (1) 略; (2)  $ 2\ln2-1 $.

41. 首先，由于  $ 0 \leqslant g(x) \leqslant 1 $，所以  $ 0 \leqslant \int_{a}^{x} g(t) dt \leqslant \int_{a}^{x} dt = x - a, x \in [a, b] $.

其次，令  $ F(u)=\int_{a}^{u}f(x)g(x)\mathrm{d}x-\int_{a}^{a+\int_{a}^{u}g(t)\mathrm{d}t}f(x)\mathrm{d}x(a\leqslant u\leqslant b) $，注意到  $ f(x) $ 单调递增，且  $ a+\int_{a}^{u}g(t)\mathrm{d}t\leqslant u $，所以  $ f\left(a+\int_{a}^{u}g(t)\mathrm{d}t\right)\leqslant f(u) $。因此

 $$ \begin{align*}F^{\prime}(u)&=f(u)g(u)-f\left(a+\int_{a}^{u}g(t)\mathrm{d}t\right)g(u)\\&=\left[f(u)-f\left(a+\int_{a}^{u}g(t)\mathrm{d}t\right)\right]g(u)\\&\geqslant0,\end{align*} $$ 

这表明  $ F(x) $ 在  $ [a,b] $ 上单调递增，所以  $ F(b) \geqslant F(a) = 0 $，即得所证.

42. 利用积分中值定理, 存在  $ a \in (2,3) $, 使得  $ \varphi(2) > \int_{2}^{3} \varphi(x) \, \mathrm{d}x = \varphi(a) $.

对  $ \varphi(x) $ 在  $ [1,2],[2,a] $ 上分别利用 Lagrange 中值定理, 存在  $ \eta_1 \in (1,2),\eta_2 \in (2,a) $, 使得

 $$ \varphi^{\prime}(\eta_{1})=\frac{\varphi(2)-\varphi(1)}{2-1}>0,\quad\varphi^{\prime}(\eta_{2})=\frac{\varphi(a)-\varphi(2)}{a-2}<0. $$ 

再对  $ \varphi'(x) $ 在  $ [\eta_1,\eta_2] $ 上利用 Lagrange 中值定理，存在  $ \xi\in(\eta_1,\eta_2)\subset(1,3) $，使得

 $$ \varphi^{\prime\prime}(\xi)=\frac{\varphi^{\prime}(\eta_{2})-\varphi^{\prime}(\eta_{1})}{\eta_{2}-\eta_{1}}<0. $$ 

43. 作变量代换： $ e^{x}=u $，则  $ I=\int_{1}^{2}\frac{\ln u}{u+1}du+\int_{2}^{3}\frac{\ln u}{u-1}du=I_{1}+I_{2} $。对后一积分再作变量代换：u-1=t，并分部积分，则

 $$ \begin{aligned}I_{2}&=\int_{2}^{3}\frac{\ln u}{u-1}\mathrm{d}u=\int_{1}^{2}\frac{\ln(t+1)}{t}\mathrm{d}t\\&=\ln t\ln(t+1)\bigg|_{1}^{2}-\int_{1}^{2}\frac{\ln t}{t+1}\mathrm{d}u\\&=\ln2\ln3-I_{1}.\\ \end{aligned} $$ 

所以  $ I=I_{1}+I_{2}=\ln2\ln3 $

44. 如图 3.11. 因为

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//389f68a3-f4ad-40d7-8fff-05e48c346e8e/markdown_1/imgs/img_in_image_box_124_849_403_1089.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A18Z%2F-1%2F%2Fc28459a4e3f34b0676c63d873896a4d6a5479f69e31b7079556839c85ca8e938" alt="Image" width="26%" /></div>


 $$ \ln y=\pm(1-|\ln x|)=\pm\left\{\begin{array}{l l}{1+\ln x,}&{0<x<1,}\\ {1-\ln x,}&{x\geqslant1,}\end{array}\right. $$ 

所以  $ y_{1}=\left\{\begin{array}{ll}\frac{1}{\mathrm{e}x},&0<x<1,\\ \frac{x}{\mathrm{e}},&x\geqslant1,\end{array}\right. $  $ y_{2}=\left\{\begin{array}{ll}\mathrm{ex},&0<x<1,\\ \frac{\mathrm{e}}{x},&x\geqslant1.\end{array}\right. $

<div style="text-align: center;"><div style="text-align: center;">图3.11</div> </div>


故所求面积为

 $$ \begin{aligned}A&=\int_{\frac{1}{\mathrm{e}}}^{1}\left(\mathrm{e}x-\frac{1}{\mathrm{e}x}\right)\mathrm{d}x+\int_{1}^{\mathrm{e}}\left(\frac{\mathrm{e}}{x}-\frac{x}{\mathrm{e}}\right)\mathrm{d}x\\&=\frac{1}{2}\left(\mathrm{e}-\frac{3}{\mathrm{e}}\right)+\frac{1}{2}\left(\mathrm{e}+\frac{1}{\mathrm{e}}\right)=\mathrm{e}-\frac{1}{\mathrm{e}}.\end{aligned} $$ 

45. 因为边界曲线方程的直角坐标式比较复杂, 所以应化为参数方程计算为宜.

考虑到边界曲线是关于两条坐标轴均对称的，且经过坐标原点的封闭曲线，故只需计算位于第一象限内的那部分图形的面积.

由  $ y^{2}=x^{2}-x^{4}=x^{2}(1-x^{2})\geqslant0 $ 知  $ \left|x\right|\leqslant1 $ ，可设  $ x=\cos t $ ，则  $ y=\sqrt{\cos^{2}t\sin^{2}t}=\cos t\sin t\left(0\leqslant t\leqslant\frac{\pi}{2}\right) $ 。因此

 $$ A=4\left|\int_{0}^{\frac{\pi}{2}}y(t)x^{\prime}(t)\mathrm{d}t\right|=4\int_{0}^{\frac{\pi}{2}}\sin^{2}t\cos t\mathrm{d}t=4\cdot\frac{1}{3}\sin^{3}t\bigg|_{0}^{\frac{\pi}{2}}=\frac{4}{3}. $$ 

【注】如果平面图形的边界曲线方程能化为参数形式

 $$ \left\{\begin{array}{l}x=x(t),\\ y=y(t)\end{array}\quad(\alpha\leqslant t\leqslant\beta),\right. $$ 

则计算平面图形面积的公式为

 $$ A=\left|\int_{\alpha}^{\beta}x(t)y^{\prime}(t)\mathrm{d}t\right|\quad 或 \quad A=\left|\int_{\alpha}^{\beta}y(t)x^{\prime}(t)\mathrm{d}t\right|. $$ 

46. (1) 对方程  $ \arctan\frac{x}{y}=\ln\sqrt{x^{2}+y^{2}}-\frac{1}{2}\ln2+\frac{\pi}{4} $ 两端关于 x 求导，得

 $$ \frac{1}{1+\left(\frac{x}{y}\right)^{2}}\frac{y-xy^{\prime}}{y^{2}}=\frac{1}{2}\cdot\frac{2x+2yy^{\prime}}{x^{2}+y^{2}}, $$ 

即 $ (x+y)y'=-x+y $. 再关于 x 求导，得 $ (1+y')y'+(x+y)y''=-1+y' $. 将 x=1, y=1 代入，得  $ y'(1)=0, y''(1)=-\frac{1}{2} $. 所以，曲线  $ y=f(x) $ 在点  $ (1,1) $ 处的曲率为

 $$ K=\frac{\left|y^{\prime\prime}\right|}{\sqrt{\left[1+\left(y^{\prime}\right)^{2}\right]^{3}}}=\frac{1}{2}. $$ 

(2) 因为  $ y' = \frac{y - x}{x + y} $ 在区间  $ [0, 1] $ 上连续，且  $ y(0) = \sqrt{2} e^{-\frac{x}{4}} $，所以

 $$ \int_{0}^{1}\frac{x-f(x)}{x+f(x)}\mathrm{d}x=-\int_{0}^{1}f^{\prime}(x)\mathrm{d}x=f(0)-f(1)=\sqrt{2}\mathrm{e}^{-\frac{\pi}{4}}-1. $$ 

47. 根据题设条件知 c=0,  $ a+b=2 $，由此可解得两曲线异于原点的交点为  $ \left(\frac{a}{a+1}, \frac{a(a+2)}{(a+1)^2}\right) $。因为  $ 1 < \frac{a}{a+1} < 2 $，所以两个曲线围成区域的面积为

 $$ \begin{aligned}S&=\int_{0}^{\frac{a}{a+1}}\left[ax^{2}+bx-\left(-x^{2}+2x\right)\right]\mathrm{d}x\\&=\int_{0}^{\frac{a}{a+1}}\left[(a+1)x^{2}-ax\right]\mathrm{d}x\\&=-\frac{a^{3}}{6(a+1)^{2}}\quad(a<-2).\end{aligned} $$ 

经计算，得  $ \frac{\mathrm{d}S}{\mathrm{d}a} = -\frac{a^{2}(a+3)}{6(a+1)^{3}} $。令  $ \frac{\mathrm{d}S}{\mathrm{d}a} = 0 $，解得 a = -3。可见，面积函数  $ S(a) $ 在  $ (-∞, -2) $ 有唯一的驻点，且为极小值点，因此， $ S(-3) $ 是  $ S(a) $ 在  $ (-∞, -2) $ 上的最小值。此时，b = 5。

综上所述，得a=-3,b=5,c=0.

48. 令  $ F(x)=\int_{0}^{x}f(t)dt-kx $，其中  $ k=\frac{1}{T}\int_{0}^{T}f(x)dx $，则  $ F(x) $ 在区间  $ (-∞,+∞) $ 上具有连续的一阶导数，且  $ F'(x)=f(x)-k $。注意到对任意  $ x∈(-∞,+∞) $，恒有

 $$ F(x+T)-F(x)=\int_{x}^{x+T}f(t)\mathrm{d}t-kT, $$ 

因为  $  f(x)  $ 是以 T 为周期的连续函数，所以  $ \int_{x}^{x+T} f(t) dt = \int_{0}^{T} f(t) dt $，因此  $  F(x + T) = F(x)  $，即  $  F(x)  $ 也是周期函数，因而有界。故存在 M > 0，使得  $  |F(x)| \leq M, x \in (-\infty, +\infty)  $。于是

 $$ n\int_{n}^{+\infty}\frac{f(x)}{x^{2}}\mathrm{d}x=n\int_{n}^{+\infty}\frac{k+F^{\prime}(x)}{x^{2}}\mathrm{d}x=kn\int_{n}^{+\infty}\frac{\mathrm{d}x}{x^{2}}+n\int_{n}^{+\infty}\frac{F^{\prime}(x)}{x^{2}}\mathrm{d}x. $$ 

对于上式右端的积分，有  $ \int_{n}^{+\infty}\frac{dx}{x^{2}}=-\left.\frac{1}{x}\right|_{n}^{+\infty}=\frac{1}{n} $，且

 $$ \begin{align*}\int_{n}^{+\infty}\frac{F^{\prime}(x)}{x^{2}}\mathrm{d}x&=\left.\frac{F(x)}{x^{2}}\right|_{n}^{+\infty}+2\int_{n}^{+\infty}\frac{F(x)}{x^{3}}\mathrm{d}x\\&=-\frac{F(n)}{n^{2}}+2\int_{n}^{+\infty}\frac{F(x)}{x^{3}}\mathrm{d}x.\end{align*} $$ 

又由  $ F(x) $ 的有界性，有

 $$ 0\leqslant n\left|\int_{n}^{+\infty}\frac{F(x)}{x^{3}}\mathrm{d}x\right|\leqslant n M\int_{n}^{+\infty}\frac{\mathrm{d}x}{x^{3}}\mathrm{d}x=\frac{M}{2n}\rightarrow0\quad(n\rightarrow\infty), $$ 

故根据夹逼准则得  $ \lim_{n\to\infty}n\int_{n}^{+\infty}\frac{F(x)}{x^{3}}dx=0 $ 。综合上述，可得

 $$ \begin{align*}\lim_{n\to\infty}n\int_{n}^{+\infty}\frac{f(x)}{x^{2}}\mathrm{d}x&=k+\lim_{n\to\infty}n\int_{n}^{+\infty}\frac{F^{\prime}(x)}{x^{2}}\mathrm{d}x\\&=k-\lim_{n\to\infty}\frac{F(n)}{n}+2\lim_{n\to\infty}n\int_{n}^{+\infty}\frac{F(x)}{x^{3}}\mathrm{d}x=k\\&=\frac{1}{T}\int_{0}^{T}f(x)\mathrm{d}x.\end{align*} $$ 

49. 如图 3.12, 设曲线  $ y = a \sin x $,  $ y = b \sin x $ 与曲线  $ y = \cos x $ 分别交于  $ (x_1, y_1) $ 和  $ (x_2, y_2) $，则

 $$ \left\{\begin{array}{l}\cos x_{1}=a\sin x_{1},\\ \cos x_{2}=b\sin x_{2},\end{array}\right. 即 \quad\left\{\begin{array}{l}\cot x_{1}=a,\\ \cot x_{2}=b.\end{array}\right. $$ 

由 a > b 及函数  $ y = \cot x $ 的单调性知： $ x_{1} < x_{2} $. 依题意，有

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//25ce53a0-bde7-4e3c-a151-6741be782537/markdown_0/imgs/img_in_image_box_645_164_936_413.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-08-30T19%3A03%3A18Z%2F-1%2F%2F756ffa3deeb8ece1e6daa753a413838e888fc6803ded0cea9c2d9f946b73507e" alt="Image" width="27%" /></div>


<div style="text-align: center;"><div style="text-align: center;">图3.12</div> </div>


 $$ \begin{aligned}&\int_{0}^{x_{1}}\cos x\mathrm{d}x-\int_{0}^{x_{1}}a\sin x\mathrm{d}x\\=&\int_{0}^{x_{1}}a\sin x\mathrm{d}x+\int_{x_{1}}^{x_{2}}\cos x\mathrm{d}x-\int_{0}^{x_{2}}b\sin x\mathrm{d}x\\=&\int_{0}^{x_{2}}b\sin x\mathrm{d}x+\int_{x_{2}}^{\frac{\pi}{2}}\cos x\mathrm{d}x.\end{aligned} $$ 

积分并整理，得

 $$ \left\{\begin{aligned}2\sin x_{1}+2a\cos x_{1}-2a&=\sin x_{2}+b\cos x_{2}-b,\\ \sin x_{1}+a\cos x_{1}-a&=-b\cos x_{2}+b+1-\sin x_{2}.\end{aligned}\right. $$ 

由 $ ^{①} $式得

 $$ \sin x_{1}=\frac{1}{\sqrt{1+a^{2}}},\quad\cos x_{1}=\frac{a}{\sqrt{1+a^{2}}},\quad\sin x_{2}=\frac{1}{\sqrt{1+b^{2}}},\quad\cos x_{2}=\frac{b}{\sqrt{1+b^{2}}}. $$ 

将其代入 ② 式，并化简，得

 $$ \left\{\begin{array}{l}2\sqrt{1+a^{2}}-2a=\sqrt{1+b^{2}}-b,\\ \sqrt{1+a^{2}}-a=b+1-\sqrt{1+b^{2}}.\end{array}\right. $$ 

解之，得  $ a=\frac{4}{3} $,  $ b=\frac{5}{12} $.

50. 设圆的方程为  $ x^{2}+y^{2}=a^{2} $，点 A 位于  $ (b,0) $，在圆周上任取点  $ P(x_{0},y_{0}) $，过点 P 作圆的切线 L，则 L 的方程为  $ x_{0}x+y_{0}y=a^{2} $，其中  $ (x,y) $ 为 L 上动点的坐标。过点 A 作 L 的垂线 AQ，则直线 AQ 的参数方程为  $ \left\{\begin{array}{l}x=b+x_{0}t,\\ y=y_{0}t.\end{array}\right. $ 代入 L 的方程，解得 Q 所对应的参数为  $ t=1-\frac{b}{a^{2}}x_{0} $，于是 Q 的坐标  $ (x,y) $ 为

 $$ x=b+x_{0}\left(1-\frac{b}{a^{2}}x_{0}\right),\quad y=y_{0}\left(1-\frac{b}{a^{2}}x_{0}\right). $$ 

令  $ x_{0}=a\cos t,y_{0}=a\sin t $ ，代入上式得 Q 的坐标  $ (x,y) $ 为

 $$ x=b+\left(1-\frac{b}{a}\cos t\right)a\cos t=b+a\cos t-b\cos^{2}t, $$ 

 $$ y=\left(1-\frac{b}{a}\cos t\right)a\sin t=a\sin t-b\sin t\cos t. $$ 

显然，垂足的轨迹关于 x 轴对称，且交 x 轴于点  $ (-a,0) $ 与  $ (a,0) $，因此所求面积为

 $$ \begin{align*}S&=2\int_{-a}^{a}y\mathrm{d}x=2\int_{\pi}^{0}(a\sin t-b\sin t\cos t)\mathrm{d}\left(b+a\cos t-b\cos^{2}t\right)\\&=2\int_{0}^{\pi}\left(a^{2}-3ab\cos t+2b^{2}\cos^{2}t\right)\sin^{2}t\mathrm{d}t=\left(a^{2}+\frac{b^{2}}{2}\right)\pi.\end{align*} $$ 

51. 利用积分中值定理, 存在  $ \xi \in [a,1] $, 使得

 $$ \int_{a}^{1}f(x)g^{\prime}(x)\mathrm{d}x=f(\xi)\int_{a}^{1}g^{\prime}(x)\mathrm{d}x=f(\xi)[g(1)-g(a)]. $$ 

根据题设条件  $ f'(x) \geqslant 0 $,  $ g'(x) \geqslant 0 $, 可知  $ f(\xi) \geqslant f(a) $,  $ g(1) \geqslant g(a) $. 因此

 $$ \begin{aligned} 左边 &=\int_{0}^{a}[g(x)f^{\prime}(x)+f(x)g^{\prime}(x)]\mathrm{d}x+\int_{a}^{1}f(x)g^{\prime}(x)\mathrm{d}x\\&=\int_{0}^{a}[f(x)g(x)]^{\prime}\mathrm{d}x+\int_{a}^{1}f(x)g^{\prime}(x)\mathrm{d}x\\&=f(a)g(a)-f(0)g(0)+f(\xi)[g(1)-g(a)]\\&\geqslant f(a)g(a)+f(a)[g(1)-g(a)]=f(a)g(1).\end{aligned} $$ 

52. 设  $ F(x)=\left(\int_{0}^{x}f(t)dt\right)^{2}-\int_{0}^{x}f^{3}(t)dt $，则  $ F(x) $ 在  $ [0,1] $ 上可导， $ F(0)=0 $，且

 $$ F^{\prime}(x)=2f(x)\int_{0}^{x}f(t)\mathrm{d}t-f^{3}(x)=f(x)G(x), $$ 

其中  $ G(x)=2\int_{0}^{x}f(t)dt-f^{2}(x) $.

因为  $ f(x) $ 在  $ [0,1] $ 上单调增加, 所以当 x > 0 时,  $ f(x) \geqslant f(0) = 0 $. 因此, 当  $ x \in (0,1) $ 时, 有

 $$ G^{\prime}(x)=2f(x)-2f(x)f^{\prime}(x)=2f(x)\left[1-f^{\prime}(x)\right]\geqslant0. $$ 

故 G(x) 在 [0,1] 上单调增加，所以当 x>0 时， $ G(x)\geqslant G(0)=0 $，从而有  $ F'(x)\geqslant0 $。

于是， $ F(1) \geqslant F(0) = 0 $，即  $ \left(\int_{0}^{1} f(x) \, \mathrm{d}x\right)^{2} \geqslant \int_{0}^{1} f^{3}(x) \, \mathrm{d}x $.

显然，等号成立  $ \Leftrightarrow F'(x) \equiv 0 \Leftrightarrow f(x) \equiv 0 $ 或  $ f'(x) = 1 $，即  $ f(x) = x $。

53. 根据积分中值定理, 存在  $ c \in [a, b] $, 使得  $ A = \frac{1}{b - a} \int_{a}^{b} f(x) \, \mathrm{d}x = f(c) $.

先后利用 Newton-Leibniz 公式与 Cauchy 积分不等式，得

 $$ \begin{align*}|f(x)-A|^{2}&=|f(x)-f(c)|^{2}=\left(\int_{c}^{x}f^{\prime}(t)\mathrm{d}t\right)^{2}\\&\leqslant\left|\int_{c}^{x}1^{2}\mathrm{d}t\int_{c}^{x}|f^{\prime}(t)|^{2}\mathrm{d}t\right|\leqslant|x-c|\int_{a}^{b}|f^{\prime}(t)|^{2}\mathrm{d}t.\end{align*} $$ 

所以

 $$ \int_{a}^{b}|f(x)-A|^{2}\mathrm{d}x\leqslant\int_{a}^{b}|x-c|\mathrm{d}x\int_{a}^{b}|f^{\prime}(x)|^{2}\mathrm{d}x. $$ 

由于

 $$ \begin{align*}\int_{a}^{b}|x-c|\mathrm{d}x&=\int_{a}^{c}|x-c|\mathrm{d}x+\int_{c}^{b}|x-c|\mathrm{d}x=\int_{a}^{c}(c-x)\mathrm{d}x+\int_{c}^{b}(x-c)\mathrm{d}x\\&=\frac{1}{2}(c-a)^{2}+\frac{1}{2}(b-c)^{2}\leqslant(a-b)^{2},\end{align*} $$ 

所以

 $$ \int_{a}^{b}|f(x)-A|^{2}\mathrm{d}x\leqslant(a-b)^{2}\int_{a}^{b}|f^{\prime}(x)|^{2}\mathrm{d}x. $$ 

54. 注意到  $  f(x) = f(x) - f(a) = \int_{a}^{x} f'(t) \, dt  $，利用 Cauchy 积分不等式得

 $$ f^{2}(x)=\left(\int_{a}^{x}f^{\prime}(t)\mathrm{d}t\right)^{2}\leqslant\int_{a}^{x}1^{2}\mathrm{d}t\int_{a}^{x}|f^{\prime}(t)|^{2}\mathrm{d}t\leqslant(x-a)\int_{a}^{b}|f^{\prime}(t)|^{2}\mathrm{d}t. $$ 

所以

 $$ \int_{a}^{b}f^{2}(x)\mathrm{d}x\leqslant\int_{a}^{b}(x-a)\mathrm{d}x\int_{a}^{b}|f^{\prime}(x)|^{2}\mathrm{d}x=\frac{(a-b)^{2}}{2}\int_{a}^{b}\left|f^{\prime}(x)\right|^{2}\mathrm{d}x. $$ 

55. 设 A, B 的坐标分别为  $ (a, \ln a) $,  $ (b, \ln b) $，不妨设 b > a > 0，则直线 AB 的斜率为  $ k_{AB} = \frac{\ln b - \ln a}{b - a} $。因为 Q 的横坐标为  $ x_{c} = \frac{a + b}{2} $，所以曲线 L 在 Q 点处的切线的斜率为  $ k_{Q} = (\ln x)^{\prime} \bigg|_{x=x_{c}} = \frac{2}{a + b} $。问题要求证明： $ k_{AB} > k_{Q} $，即  $ \frac{\ln b - \ln a}{b - a} > \frac{2}{a + b} $。令  $ x = \frac{b}{a} $，则不等式化为

 $$ \ln x>\frac{2(x-1)}{x+1},\quad x>1. $$ 

设  $ f(x)=\ln x-\frac{2(x-1)}{x+1} $ ( $ x\geqslant1 $)，则  $ f(x) $ 在  $ (1,+\infty) $ 内可导，且

 $$ f^{\prime}(x)=\frac{1}{x}-\frac{4}{(x+1)^{2}}=\frac{(x-1)^{2}}{x(x+1)^{2}}>0\quad(x>1). $$ 

所以  $ f(x) $ 在  $ [1,+\infty) $ 上严格单调递增，对任意 x > 1，有  $ f(x) > f(1) = 0 $，即  $ \ln x > \frac{2(x-1)}{x+1} $.

56. 设  $ f(a)=\sin x^{a}-\sin^{a}x $ ( $ a\geqslant1 $)，易知  $ f(a) $ 在  $ [1,+\infty) $ 内可导，且

 $$ f^{\prime}(a)=a(x^{a-1}\cos x^{a}-\sin^{a-1}\cos x). $$ 

当 0 < x < 1 时， $ \sin x < x, x^{a} < x $，所以  $ \sin x^{a-1} < x^{a-1}, \cos x^{a} > \cos x $。因此  $ f'(a) > 0 $

故当 a > 1 时， $ f(a) > f(1) = 0 $，即  $ \sin x^{a} > \sin^{a}x $，从而有  $ \int_{0}^{1} \sin x^{a} dx > \int_{0}^{1} \sin^{a}x dx $。

57. 利用指数函数  $ e^{x} $ 的 Maclaurin 级数展开式, 得

 $$ \mathrm{e}^{\sin x}=1+\sin x+\frac{1}{2!}\sin^{2}x+\frac{1}{3!}\sin^{3}x+\cdots, $$ 

 $$ \mathrm{e}^{-\sin x}=1-\sin x+\frac{1}{2!}\sin^{2}x-\frac{1}{3!}\sin^{3}x+\cdots, $$ 

所以

 $$ \mathrm{e}^{\sin x}+\mathrm{e}^{-\sin x}=2+\sin^{2}x+\frac{2}{4!}\sin^{4}x+\cdots>2+\sin^{2}x+\frac{2}{4!}\sin^{4}x. $$ 

利用 Wallis 公式, 有

 $$ \begin{aligned}\int_{0}^{\frac{\pi}{2}}\left(\mathrm{e}^{\sin x}+\mathrm{e}^{-\sin x}\right)\mathrm{d}x&>\int_{0}^{\frac{\pi}{2}}\left(2+\sin^{2}x+\frac{1}{12}\sin^{4}x\right)\mathrm{d}x\\&=\pi+\frac{1}{2}\cdot\frac{\pi}{2}+\frac{1}{12}\cdot\frac{3}{4}\cdot\frac{1}{2}\cdot\frac{\pi}{2}\\&=\frac{81}{64}\pi.\end{aligned} $$ 

58. 对任意实数 a，根据 Cauchy 积分不等式，得

 $$ \left(\int_{0}^{1}(x+a)f^{\prime}(x)\mathrm{d}x\right)^{2}\leqslant\int_{0}^{1}(x+a)^{2}\mathrm{d}x\int_{0}^{1}\left|f^{\prime}(x)\right|^{2}\mathrm{d}x. $$ 

另一方面，利用分部积分， $ \int_{0}^{1}(x+a)f'(x)\mathrm{d}x=-\frac{1}{6}-\int_{0}^{1}f(x)\mathrm{d}x $，代入上式，得

 $$ \left(\frac{1}{6}+\int_{0}^{1}f(x)\mathrm{d}x\right)^{2}\leqslant\frac{1}{3}(3a^{2}+3a+1)\int_{0}^{1}\left|f^{\prime}(x)\right|^{2}\mathrm{d}x. $$ 

记  $ \lambda=\frac{1}{3}(3a^{2}+3a+1) $，则问题归结为只需取合适的  $ \lambda\neq0 $ 或 a 使得

 $$ 2\int_{0}^{1}f(x)\mathrm{d}x+\frac{1}{4}\leqslant\frac{1}{\lambda}\left(\frac{1}{6}+\int_{0}^{1}f(x)\mathrm{d}x\right)^{2} $$ 

成立，整理成等价形式，即

 $$ \left(\frac{1}{6}-\lambda+\int_{0}^{1}f(x)\mathrm{d}x\right)^{2}+\lambda\left(\frac{1}{12}-\lambda\right)\geqslant0. $$ 

这只需取  $ \lambda=\frac{1}{12} $，解得  $ a=-\frac{1}{2} $。因此不等式得证。

59. 【分析】显然，不等式关于 a, b, c 具有对称性，而

 $$ (1-a)(1-b)(1-c)=1-(a+b+c)+(ab+bc+ca)-abc, $$ 

因此应考虑将所证不等式拆分成三个对称的不等式，只证其中一个就能得到另外两个，再把三个加起来即得所证．另一方面，把代数不等式转化为积分不等式也是一种很特别的转化技能．具体证明如下：

利用定积分及 Bernoulli 不等式：当  $ -1 \leqslant t \leqslant 0 $ 时， $ (1 + t)^b \leqslant 1 + bt $，可得

 $$ \begin{align*}\frac{1}{b+c+1}&=\int_{0}^{1}x^{b+c}\mathrm{d}t\leqslant\int_{0}^{1}[1+b(x-1)][1+c(x-1)]\mathrm{d}t\\&=\int_{0}^{1}[1+(b+c)(x-1)+bc(x-1)^{2}]\mathrm{d}t\\&=1-\frac{1}{2}(b+c)+\frac{1}{3}bc.\end{align*} $$ 

所以

 $$ \frac{a}{b+c+1}\leqslant a-\frac{1}{2}a(b+c)+\frac{1}{3}abc. $$ 

同理，可得

 $$ \frac{b}{c+a+1}\leqslant b-\frac{1}{2}b(c+a)+\frac{1}{3}abc, $$ 

 $$ \frac{c}{a+b+1}\leqslant c-\frac{1}{2}c(a+b)+\frac{1}{3}abc. $$ 

将上述三式两边分别相加并整理，即得

 $$ \frac{a}{b+c+1}+\frac{b}{c+a+1}+\frac{c}{a+b+1}+(1-a)(1-b)(1-c)\leqslant1. $$ 

60. 对所给等式两边关于 x 作区间  $ [a, b] $ 上的定积分，得

 $$ \int_{a}^{b}f(x)\mathrm{d}x=3+\lambda\int_{a}^{b}\mathrm{d}x\int_{x}^{b}f(t)f(a+t-x)\mathrm{d}t. $$ 

对右端的二次积分交换积分次序，得

 $$ \int_{a}^{b}f(x)\mathrm{d}x=3+\lambda\int_{a}^{b}f(t)\mathrm{d}t\int_{a}^{t}f(a+t-x)\mathrm{d}x. $$ 

作变量代换： $ u = a + t - x $，则有

 $$ \int_{a}^{b}f(x)\mathrm{d}x=3+\lambda\int_{a}^{b}f(t)\mathrm{d}t\int_{a}^{t}f(u)\mathrm{d}u. $$ 

根据对称性，可知  $ \int_{a}^{b}f(t)\mathrm{d}t\int_{a}^{t}f(u)\mathrm{d}u=\frac{1}{2}\left(\int_{a}^{b}f(x)\mathrm{d}x\right)^{2} $，代入上式得

 $$ \int_{a}^{b}f(x)\mathrm{d}x=3+\frac{\lambda}{2}\left(\int_{a}^{b}f(x)\mathrm{d}x\right)^{2}. $$ 

由此可见， $ I=\int_{a}^{b}f(x)\mathrm{d}x\neq0 $，因此

 $$ \lambda=-\frac{6}{I^{2}}+\frac{2}{I}=-6\left(\frac{1}{I}-\frac{1}{6}\right)^{2}+\frac{1}{6}\leqslant\frac{1}{6}. $$ 

61.（方法1）微分法. 令  $ F(t)=\int_{0}^{t}xf^{2}(x)\mathrm{d}x\int_{0}^{t}f(x)\mathrm{d}x-\int_{0}^{t}xf(x)\mathrm{d}x\int_{0}^{t}f^{2}(x)\mathrm{d}x $，则

 $$ \begin{align*}F^{\prime}(x)&=tf^{2}(t)\int_{0}^{t}f(x)\mathrm{d}x+f(t)\int_{0}^{t}xf^{2}(x)\mathrm{d}x\\&\quad-tf(t)\int_{0}^{t}f^{2}(x)\mathrm{d}x-f^{2}(t)\int_{0}^{t}xf(x)\mathrm{d}x\\&=\int_{0}^{t}(t-x)(f(t)-f(x))f(t)f(x)\mathrm{d}x.\end{align*} $$ 

因为  $ f(x) $ 是  $ [0,1] $ 上的单调递减的正值函数，所以  $ (t-x)(f(t)-f(x))f(t)f(x)\leq0 $，从而有  $ F'(x)\leq0 $， $ F(x) $ 是  $ [0,1] $ 上的单调递减函数， $ F(1)\leq F(0)=0 $，即得

 $$ \frac{\int_{0}^{1}xf^{2}(x)\mathrm{d}x}{\int_{0}^{1}xf(x)\mathrm{d}x}\leqslant\frac{\int_{0}^{1}f^{2}(x)\mathrm{d}x}{\int_{0}^{1}f(x)\mathrm{d}x}. $$ 

（方法2）积分法. 记  $ D=\{(x,y)|0\leq x\leq1,0\leq y\leq1\} $，则

 $$ \int_{0}^{1}x f^{2}(x)\mathrm{d}x\int_{0}^{1}f(x)\mathrm{d}x-\int_{0}^{1}x f(x)\mathrm{d}x\int_{0}^{1}f^{2}(x)\mathrm{d}x $$ 

 $$ \begin{aligned}&=\int_{0}^{1}xf^{2}(x)\mathrm{d}x\int_{0}^{1}f(y)\mathrm{d}y-\int_{0}^{1}xf(x)\mathrm{d}x\int_{0}^{1}f^{2}(y)\mathrm{d}y\\&=\iint\limits_{D}xf^{2}(x)f(y)\mathrm{d}x\mathrm{d}y-\iint\limits_{D}xf(x)f^{2}(y)\mathrm{d}y\\&=\iint\limits_{D}x(f(x)-f(y))f(x)f(y)\mathrm{d}x\mathrm{d}y.\end{aligned} $$ 

根据对称性，有

 $$ \begin{align*}&\int_{0}^{1}x f^{2}(x)\mathrm{d}x\int_{0}^{1}f(x)\mathrm{d}x-\int_{0}^{1}x f(x)\mathrm{d}x\int_{0}^{1}f^{2}(x)\mathrm{d}x\\=&\iint\limits_{D}y(f(y)-f(x))f(x)f(y)\mathrm{d}x\mathrm{d}y.\end{align*} $$ 

将上述两式两边分别相加并整理，得

 $$ \begin{align*}&\int_{0}^{1}x f^{2}(x)\mathrm{d}x\int_{0}^{1}f(x)\mathrm{d}x-\int_{0}^{1}x f(x)\mathrm{d}x\int_{0}^{1}f^{2}(x)\mathrm{d}x\\=&\frac{1}{2}\iint\limits_{D}(x-y)(f(x)-f(y))f(x)f(y)\mathrm{d}x\mathrm{d}y.\end{align*} $$ 

利用题设条件，有  $ (x-y)(f(x)-f(y))f(x)f(y)\leqslant0 $ ，故由上式及二重积分的保号性，得

 $$ \int_{0}^{1}x f^{2}(x)\mathrm{d}x\int_{0}^{1}f(x)\mathrm{d}x\leqslant\int_{0}^{1}x f(x)\mathrm{d}x\int_{0}^{1}f^{2}(x)\mathrm{d}x. $$ 

两边同除以  $ \int_{0}^{1}xf(x)\mathrm{d}x\int_{0}^{1}f(x)\mathrm{d}x $ 即得所证.

【注】本题的物理意义：两根长度同为1的细直杆展布在x轴的区间[0,1]上，它们的线密度函数分别为 $ f^{2}(x) $与 $ f(x) $，重心坐标分别为 $ x_{1},x_{2} $，则由本题结论知 $ x_{1}\leq x_{2} $.

62. 根据题设条件, 有  $ \int_{0}^{1} x^{2} f(x) dx = \int_{0}^{1} (x^{2} + ax + b) f(x) dx $, 其中 a, b 为任意实数. 利用分部积分, 得

 $$ \begin{align*}\int_{0}^{1}\left(x^{2}+ax+b\right)f(x)\mathrm{d}x=&\left(\frac{1}{3}+\frac{a}{2}+b\right)f(1)-\left(\frac{1}{12}+\frac{a}{6}+\frac{b}{2}\right)f^{\prime}(1)\\&+\int_{0}^{1}\left(\frac{x^{4}}{12}+\frac{a}{6}x^{3}+\frac{b}{2}x^{2}\right)f^{\prime\prime}(x)\mathrm{d}x.\end{align*} $$ 

令  $ \frac{1}{3}+\frac{a}{2}+b=0,\frac{1}{12}+\frac{a}{6}+\frac{b}{2}=0 $ , 解得 a=-1,  $ b=\frac{1}{6} $ . 注意到  $ \left|f''(x)\right|\leqslant1 $ , 因此

 $$ \left|\int_{0}^{1}x^{2}f(x)\mathrm{d}x\right|\leqslant\int_{0}^{1}\left(\frac{1}{12}x^{4}-\frac{1}{6}x^{3}+\frac{1}{12}x^{2}\right)\mathrm{d}x=\frac{1}{12}\int_{0}^{1}x^{2}(x-1)^{2}\mathrm{d}x=\frac{1}{360}. $$ 

另一方面，欲使等号成立，可要求  $ f''(x)=1 $ ，故可设  $ f(x)=\frac{1}{2}x^{2}+ax+b $ ，因为

 $$ \int_{0}^{1}x^{2}f(x)\mathrm{d}x=\int_{0}^{1}x^{2}\left(\frac{1}{2}x^{2}+ax+b\right)\mathrm{d}x=\frac{1}{10}+\frac{a}{4}+\frac{b}{3}, $$ 

而 $ \int_{0}^{1}x^{2}f(x)\mathrm{d}x=\frac{1}{360} $，即 $ \frac{1}{10}+\frac{a}{4}+\frac{b}{3}=\frac{1}{360} $，所以 $ \frac{a}{4}+\frac{b}{3}=-\frac{7}{72} $。可取 $ a=-\frac{1}{2},b=\frac{1}{12} $。因此 $ f(x)=\frac{1}{2}x^{2}-\frac{1}{2}x+\frac{1}{12} $。

63. 根据题设条件, 对任意  $ x \in (a, b] $,  $ \int_{a}^{x} g(t) dt > 0 $, 有

 $$ \begin{align*}\frac{\xi-a}{x-a}&=\frac{\xi-a}{f(\xi)-f(a)}\cdot\frac{\left[f(\xi)-f(a)\right]\int_{a}^{x}g(t)\mathrm{d}t}{(x-a)\int_{a}^{x}g(t)\mathrm{d}t}\\&=\frac{\xi-a}{f(\xi)-f(a)}\cdot\frac{\int_{a}^{x}f(t)g(t)\mathrm{d}t-f(a)\int_{a}^{x}g(t)\mathrm{d}t}{(x-a)\int_{a}^{x}g(t)\mathrm{d}t}.\end{align*} $$ 

注意到  $ a \leqslant \xi \leqslant x < b $ 及导数定义，所以  $ \lim_{x \to a^{+}} \frac{\xi - a}{f(\xi) - f(a)} = \lim_{\xi \to a^{+}} \frac{\xi - a}{f(\xi) - f(a)} = \frac{1}{f_{+}^{\prime}(a)} $.

利用 L'Hospital 法则及导数定义，得

 $$ \begin{align*}\lim_{x\to a^{+}}\frac{\int_{a}^{x}f(t)g(t)\mathrm{d}t-f(a)\int_{a}^{x}g(t)\mathrm{d}t}{(x-a)\int_{a}^{x}g(t)\mathrm{d}t}&=\lim_{x\to a^{+}}\frac{f(x)g(x)-f(a)g(x)}{\int_{a}^{x}g(t)\mathrm{d}t+(x-a)g(x)}\\=\lim_{x\to a^{+}}\frac{f(x)-f(a)}{x-a}\lim_{x\to a^{+}}\frac{g(x)}{\frac{\int_{a}^{x}g(t)\mathrm{d}t}{x-a}+g(x)}&=f_{+}^{\prime}(a)\frac{g(a)}{g(a)+g(a)}=\frac{f_{+}^{\prime}(a)}{2},\end{align*} $$ 

因此  $ \lim_{x\to a^{+}}\frac{\xi-a}{x-a}=\frac{1}{f_{+}^{\prime}(a)}\cdot\frac{f_{+}^{\prime}(a)}{2}=\frac{1}{2} $

64. 令  $ F(x)=xf(x) $，则  $ F(x) $ 在  $ [-1,1] $ 上有连续的二阶导数， $ F'(x)=f(x)+xf'(x) $，且  $ F''(x)=2f'(x)+xf''(x) $。利用 Taylor 公式，并利用  $ F(0)=0, F'(0)=f(0) $，得

 $$ F(x)=F(0)+F^{\prime}(0)x+\frac{F^{\prime\prime}(\theta x)}{2}x^{2}=f(0)x+\frac{F^{\prime\prime}(\theta x)}{2}x^{2}, $$ 

其中  $ \theta \in (0,1) $. 所以

 $$ \int_{-1}^{1}F(x)\mathrm{d}x=\int_{-1}^{1}f(0)x\mathrm{d}x+\frac{1}{2}\int_{-1}^{1}F^{\prime\prime}(\theta x)x^{2}\mathrm{d}x=\frac{1}{2}\int_{-1}^{1}F^{\prime\prime}(\theta x)x^{2}\mathrm{d}x. $$ 

记  $ m = \min_{-1 \leq x \leq 1} F''(x) $,  $ M = \max_{-1 \leq x \leq 1} F''(x) $，则

 $$ m\int_{-1}^{1}x^{2}\mathrm{d}x\leqslant\int_{-1}^{1}F^{\prime\prime}(\theta x)x^{2}\mathrm{d}x\leqslant M\int_{-1}^{1}x^{2}\mathrm{d}x, $$ 

即  $ \frac{2m}{3} \leqslant \int_{-1}^{1} F''(\theta x)x^{2} \mathrm{d}x \leqslant \frac{2M}{3} $,

因此，有  $ m \leqslant 3 \int_{-1}^{1} F(x) \, \mathrm{d}x \leqslant M $。对  $ F''(x) $ 利用闭区间上连续函数的介值定理，存在  $ \xi \in [-1,1] $，使得  $ 3 \int_{-1}^{1} F(x) \, \mathrm{d}x = F''(\xi) $，即  $ \int_{-1}^{1} x f(x) \, \mathrm{d}x = \frac{1}{3} [2f'(\xi) + \xi f''(\xi)] $。

65. 设  $ F(x)=\int_{a}^{x}f(t)dt $，则  $ F(a)=F(b)=0 $。因为  $ f(x) $ 是  $ [a,b] $ 上连续，所以  $ F(x) $ 在  $ [a,b] $ 上可导，且  $ F'(x)=f(x) $。利用分部积分及题设条件，得

 $$ \int_{a}^{b}F(x)\mathrm{d}x=x F(x)\Big|_{a}^{b}-\int_{a}^{b}x f(x)\mathrm{d}x=0. $$ 

由此利用积分中值定理，存在  $ c \in (a, b) $，使得  $ \int_{0}^{x} F(x) \, \mathrm{d}x = F(c)(b - a) = 0 $，即  $ F(c) = 0 $。

对  $ F(x) $ 在  $ [a,c] $ 与  $ [c,b] $ 上分别利用 Rolle 定理, 存在  $ c_{1}\in(a,c) $ 与  $ c_{2}\in(c,b) $, 使得  $ F'(c_{1})=0, F'(c_{2})=0 $, 即  $ f(c_{1})=0, f(c_{2})=0 $. 这表明  $ f(x) $ 在  $ (a,b) $ 内至少有两个不同的零点.

假设  $ f(x) $ 在  $ (a,b) $ 内恰有两个零点  $ c_{1}, c_{2} $，则可设  $ f(x) = (x - c_{1})(x - c_{2})g(x) $，其中  $ g(x) $ 在  $ [a,b] $ 上连续，且  $ g(x) > 0 (a \leq x \leq b) $.

根据题设条件，对任意常数 A, B，恒有

 $$ \int_{a}^{b}(x^{2}+Ax+B)f(x)\mathrm{d}x=0. $$ 

取  $ A = -c_{1} - c_{2}, B = c_{1}c_{2} $，与  $ f(x) $ 一并代入上式，得

 $$ \int_{a}^{b}(x-c_{1})^{2}(x-c_{2})^{2}g(x)\mathrm{d}x=0. $$ 

由此可得  $ g(x)=0(a \leqslant x \leqslant b) $，矛盾。因此， $ f(x) $ 在  $ (a,b) $ 内至少有三个零点。

66.  $ \frac{\pi k^{5}}{30\sqrt{1+k^{2}}} $.

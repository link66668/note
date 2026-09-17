### 第7章 常微分方程

知识结构

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//7f2d31c5-2b43-4b4a-8acf-c53f45a54a76/markdown_3/imgs/img_in_image_box_260_400_1111_798.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A48Z%2F-1%2F%2F5203e56797c5c225203ce6925441398d8dec81b8b6eff7bcfb91af9f6e76105e" alt="Image" width="58%" /></div>


高等数学中涉及的微分方程主要有3类：一阶微分方程、可降阶高阶微分方程、高阶线性微分方程. 微分方程的主要任务是求满足一定条件的未知函数，其过程通常可归结为以下几个步骤：

（1）建立方程并判断其类型（有时方程并未直接给出，需要一些相关运算或化简才能得到方程）；

(2) 根据方程类型确定求解方法（方程求解都是按分类进行的，读者要熟知各种分类与求解方法）；

（3）解方程确定所求函数（定解问题要明确定解条件，并按条件确定所求特解，必要时需做讨论）. 各类方程的求解方法可概括如下：

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//7f2d31c5-2b43-4b4a-8acf-c53f45a54a76/markdown_3/imgs/img_in_image_box_403_1107_980_1488.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A48Z%2F-1%2F%2F3161d03f2a815c0ac9ff5652c9770ea3cd1f1ae9ec031778d5f7527883e3156a" alt="Image" width="39%" /></div>


<div style="text-align: center;"><div style="text-align: center;">7.1 一阶微分方程</div> </div>


变量可分离方程、线性方程与全微分方程是一阶微分方程中的3种基本形式，其他类型的一阶方程都是通过变量代换转化为这三种之一来求解的。当然仍有大量的一阶微分方程不能通过初等积分方法来求解。如果未知函数所满足的关系式不是微分方程的形式，则需要通过适当的运算（通常为求导运算）或等价转换来建立微分方程。

例1 设  $ f(x) $ 在  $ (0,+\infty) $ 内可导， $ f(x)>0 $，且  $ \lim_{x\to+\infty}f(x)=1 $，又  $ \lim_{h\to0}\left[\frac{f(x+xh)}{f(x)}\right]^{\frac{1}{h}}=e^{\frac{1}{x}} $，求  $ f(x) $.

分析 利用导数的定义算出等式左边的极限就可得到关于  $ f(x) $ 的微分方程.

解

 $$ \mathrm{e}^{\frac{1}{x}}=\lim_{h\to0}\left[\frac{f(x+xh)}{f(x)}\right]^{\frac{1}{h}}=\lim_{h\to0}\left[1+\frac{f(x+xh)-f(x)}{f(x)}\right]^{\frac{1}{h}} $$ 

 $$ \exp\left(\lim_{h\to0}\frac{f(x+xh)-f(x)}{f(x)}\cdot\frac{1}{h}\right)=\exp\left(f'(x)\cdot\frac{x}{f(x)}\right), $$ 

所以

 $$ \frac{1}{x}=f^{\prime}(x)\cdot\frac{x}{f(x)},\  即 \ \frac{f^{\prime}(x)}{f(x)}=\frac{1}{x^{2}}. $$ 

两边积分得  $ f(x)=Ce^{\frac{1}{x}} $。由  $ \lim_{x\to+\infty}f(x)=1 $ 得 C=1，故  $ f(x)=e^{\frac{1}{x}} $。

评注 要求未知函数，首先要建立关于未知函数的方程（代数方程或微分方程），该题以极限形式间接给出了函数的导数.

例2 设f处处可微且对所有 $ xy\neq1 $的实数x,y，都有 $ f(x)+f(y)=f\left(\frac{x+y}{1-xy}\right) $，求 $ f(x) $.

分析 由于 f 处处可微，且所给等式关于变量 x, y 对称，所以在等式两边分别对 x, y 求偏导数，就容易消掉复合函数部分的导数，从而得到形式较简单的微分方程.

解 方法1 在所给等式两边分别对 x 和 y 求偏导数，得

 $$ f^{\prime}(x)=\frac{1+y^{2}}{\left(1-xy\right)^{2}}f^{\prime}\left(\frac{x+y}{1-xy}\right),\quad f^{\prime}(y)=\frac{1+y^{2}}{\left(1-xy\right)^{2}}f^{\prime}\left(\frac{x+y}{1-xy}\right), $$ 

化简得

 $$ (1+x^{2})f^{\prime}(x)=(1+y^{2})f^{\prime}(y)\;. $$ 

由于上式的左端仅依赖于x，而右端仅依赖于y，故它们必为常数K，于是有

 $$ f^{\prime}(x)=\frac{K}{1+x^{2}}, $$ 

积分得

 $$ f(x)=K\arctan x+C. $$ 

又在题设条件的等式中取 y=0，得  $ f(x)+f(0)=f(x) $，故  $ f(0)=0 $，所以 C=0。故所求函数为  $ f(x)=K\arctan x $，其中 K 为常数。

方法 2 令  $ x = \tan\theta $,  $ y = \tan\varphi $，所给等式化为  $ f(\tan\theta) + f(\tan\varphi) = f(\tan(\theta + \varphi)) $，记  $ g(x) = f(\tan x) $，则有  $ g(x) + g(y) = g(x + y) $， $ g(0) = 0 $。由此可得

 $$ \lim_{\Delta x\to0}\frac{g(x+\Delta x)-g(x)}{\Delta x}=\lim_{\Delta x\to0}\frac{g(\Delta x)}{\Delta x},\mathrm{~ 即 ~}g^{\prime}(x)=g^{\prime}(0). $$ 

积分得

 $$ g(x)=g^{\prime}(0)x\ ,\  即 \ f(\tan x)=f^{\prime}(0)x\ ,\quad f(x)=f^{\prime}(0)\arctan x\ . $$ 

评注（1）当直接利用代数方程求未知函数有困难时，要考虑利用函数的可导性来建立微分方程。求解中要尽可能利用初等运算使方程形式得到简化。

(2) 求变量可分离微分方程初值问题的解的方法有两种：一是对分离变量后的方程  $ f(y) \, \mathrm{d}y = g(x) \, \mathrm{d}x $ 做不定积分，再确定其中的常数；二是做定积分  $ \int_{y_{0}}^{y} f(t) \, \mathrm{d}t = \int_{x_{0}}^{x} g(t) \, \mathrm{d}t $ （其中  $ y(x_{0}) = y_{0} $ 为初始条件）.

（3）由“方法2”可知，该题中的条件“f处处可微”可减弱为“ $ f'(0) $存在”

例 3 设  $ f(x) $ 在  $ \mathbb{R} $ 上连续，且对任意  $ x, y \in \mathbb{R} $ 有  $ f(x+y) = f(x) + f(y) + xy(x+y) $，已知  $ f(1) = \frac{2}{3} $，求  $ f(x) $.

分析 题设没有函数可导的信息，无法直接建立微分方程。但可以利用 f 连续来做积分，得到变限积分再求导，从而建立微分方程。

解 记  $ \int_{0}^{1}f(x)dx=a $ ，对任意固定的 x ，等式两边对 y 在  $ [0,1] $ 上积分，有

 $$ \int_{0}^{1}f(x+y)dx=f(x)+a+\frac{x}{3}+\frac{x^{2}}{2}. $$ 

令  $ x + y = t $，积分  $ \int_{0}^{1} f(x + y) \, \mathrm{d}y = \int_{x}^{x+1} f(t) \, \mathrm{d}t $，上式为

 $$ \int_{x}^{x+1}f(t)\mathrm{d}t=f(x)+a+\frac{x}{3}+\frac{x^{2}}{2}, $$ 

可见  $ f(x) $ 可导，等式两边对 x 求导，得

 $$ f(x+1)-f(x)=f^{\prime}(x)+x+\frac{1}{3}. $$ 

在题设等式中取 y=1，得

 $$ f(x+1)-f(x)=\frac{2}{3}+x+x^{2}. $$ 

由①和②式得： $ f'(x)=x^2+\frac{1}{3} $，则 $ f(x)=\frac{1}{3}x^3+\frac{1}{3}x+C $，再由 $ f(1)=\frac{2}{3} $，得 $ C=0 $，所以 $ \dot{f}(x)=\frac{1}{3}x^3+\frac{1}{3}x $。

例4 求方程 $ x\mathrm{d}y-y\mathrm{d}x=\sqrt{x^{2}+y^{2}}\mathrm{d}x $的通解.

分析 这是齐次方程，作变量代换  $ u=\frac{y}{x} $，方程化为变量可分离方程.

解  $ \frac{dy}{dx}=\frac{y+\sqrt{x^{2}+y^{2}}}{x}=\frac{y}{x}\pm\sqrt{1+\left(\frac{y}{x}\right)^{2}} $ （x>0，根式取正；x<0，根式取负）.

当x>0时，令 $ u=\frac{y}{x} $. 方程化为

 $$ u+x u^{\prime}=u+\sqrt{1+u^{2}}\ , 即 \ \frac{\mathrm{d}u}{\sqrt{1+u^{2}}}=\frac{\mathrm{d}x}{x}\ . $$ 

积分得通解

 $ \ln(u+\sqrt{1+u^2})=\ln|x|+\ln|C| $，即  $ \frac{u+\sqrt{1+u^2}}{x}=C $。

代回原变量为  $ y + \sqrt{x^{2} + y^{2}} = C x^{2} $.

当x<0时，类似可得通解  $ -y+\sqrt{x^{2}+y^{2}}=C $。

例5 求微分方程  $ 2yy' = e^{\frac{x^{2} + y^{2}}{x}} + \frac{x^{2} + y^{2}}{x} - 2x $ 的通解.

分析 难以直接看出方程的类型，凑微分方程化为 $ (x^2 + y^2)' = e^{\frac{x^2 + y^2}{x}} + \frac{x^2 + y^2}{x} $，令 $ x^2 + y^2 = u $，易知是齐次方程.

解 令  $ x^{2}+y^{2}=u $ ，则  $ 2x+2yy^{\prime}=u^{\prime} $ ，方程化为

 $$ u^{\prime}=\frac{u}{x}+e^{\frac{u}{x}}\quad( 齐次方程 )． $$ 

令 $ v=\frac{u}{x} $，方程化为 $ e^{-\nu}dv=\frac{1}{x}dx $，积分得通解

 $$ -\mathbf{e}^{-v}=\ln\left|x\right|+C\;,\; 即 -\mathbf{e}^{\frac{x^{2}+y^{2}}{x}}=\ln\left|x\right|+C\;. $$ 

评注 凑微分或作变量代换将方程化为我们熟悉的类型，是解微分方程常用的方法。

例6 求解微分方程  $ (x-2\sin y+3)\mathrm{d}x-(2x-4\sin y-3)\cos y\mathrm{d}y=0 $.

分析 该方程有多种解法，作变量代换可化为变量可分离的方程；该方程也是全微分方程.

解 方法1 凑微分，方程为

 $$ (x-2\sin y+3)\mathrm{d}x-(2x-4\sin y-3)\mathrm{d}(\sin y)=0, $$ 

令 $ \sin y = z $，方程化为

 $$ \frac{\mathrm{d}z}{\mathrm{d}x}=\frac{x-2z+3}{2x-4z-3}, $$ 

再令 x-2z=u，则  $ 1-2\cdot\frac{dz}{dx}=\frac{du}{dx} $ 代入①式得

 $ \frac{1}{2}-\frac{1}{2}\cdot\frac{du}{dx}=\frac{u+3}{2u-3} $，即  $ (3-2u)du=9dx $。

两边积分得  $ 3u - u^{2} = 9x + C $ 。变量还原得原方程的通解

 $$ 3(x-2\sin y)-(x-2\sin y)^{2}=9x+C\;. $$ 

方法2 记 $ P = x - 2\sin y + 3 $， $ Q = -(2x - 4\sin y - 3)\cos y $，有 $ \frac{\partial P}{\partial y} = -2\cos y = \frac{\partial Q}{\partial x} $，所以原方程是全微分方程。做曲线积分

 $$ \begin{aligned}&\int_{(0,0)}^{(x,y)}(x-2\sin y+3)\mathrm{d}x-(2x-4\sin y-3)\cos y\mathrm{d}y\\&=\int_{0}^{x}(x+3)\mathrm{d}x-\int_{0}^{y}(2x-4\sin y-3)\cos y\mathrm{d}y\\&=\frac{1}{2}x^{2}+3x-2x\sin y+2\sin^{2}y+3\sin y.\end{aligned} $$ 

原方程的通解为

 $$ \frac{1}{2}x^{2}+3x-2x\sin y+2\sin^{2}y+3\sin y=C. $$ 

评注（1）对应于方程①的一般形式方程为 $ \frac{dy}{dx}=f\left(\frac{a_1x+b_1y+c_1}{a_2x+b_2y+c_2}\right) $（ $ c_1,c_2 $不全为0），其求解方法为：

● 若  $ \Delta = \begin{vmatrix} a_1 & b_1 \\ a_2 & b_2 \end{vmatrix} \neq 0 $，令  $ x = t + \alpha $， $ y = u + \beta $（ $ \alpha, \beta $ 是方程组  $ \begin{cases} a_1\alpha + b_1\beta + c_1 = 0 \\ a_2\alpha + b_2\beta + c_2 = 0 \end{cases} $ 的解)，则原方程化为齐次方程： $ \frac{du}{dt} = f\left(\frac{a_1t + b_1u}{a_2t + b_2u}\right) $；

若  $ \Delta = \begin{vmatrix} a_1 & b_1 \\ a_2 & b_2 \end{vmatrix} = 0 $，记  $ \frac{a_2}{a_1} = \frac{b_2}{b_1} = \lambda $，令  $ u = a_1 x + b_1 y $，则原方程化为变量可分离方程：

 $ \frac{du}{dx} = a_1 + b_1 f\left(\frac{u + c_1}{\lambda u + c_2}\right) $.

(2) 全微分方程有多种解法，具体参见本节例 12.

例 7 设  $ f(x) $ 在  $ (-\infty,+\infty) $ 上有定义， $ f'(0)=1 $，且对任何  $ x,y\in(-\infty,+\infty) $ 恒有  $ f(x+y)=\mathrm{e}^{y}f(x)+\mathrm{e}^{x}f(y) $，求  $ f(x) $.

分析 利用所给函数关系式来建立微分方程. 由于题设只给出了函数在点 x=0 可导的信息, 所以

只能利用导数的定义来求函数的导数.

解 令 x = y = 0，得  $ f(0) = f(0) + f(0) \Rightarrow f(0) = 0 $。则

 $$ \begin{aligned}&\lim_{y\rightarrow0}\frac{f(x+y)-f(x)}{y}=\lim_{y\rightarrow0}\frac{\mathbf{e}^{y}f(x)+\mathbf{e}^{x}f(y)-f(x)}{y}\\&=\lim_{y\rightarrow0}\left[\mathbf{e}^{x}\cdot\frac{f(y)-f(0)}{y}+f(x)\cdot\frac{\mathbf{e}^{y}-1}{y}\right]=\mathbf{e}^{x}f^{\prime}(0)+f(x),\end{aligned} $$ 

即

 $$ f^{\prime}(x)=\mathrm{e}^{x}+f(x)\Longrightarrow f^{\prime}(x)-f(x)=\mathrm{e}^{x}\;. $$ 

该一阶线性微分方程的通解为

 $$ f(x)=\mathrm{e}^{\int\mathrm{d}x}\left[\int\mathrm{e}^{x}\mathrm{e}^{-\int\mathrm{d}x}\mathrm{d}x+C\right]=\mathrm{e}^{x}[x+C]. $$ 

由  $ f(0)=0 $ ，得 C=0 。所以  $ f(x)=xe^{x} $

评注 一阶线性微分方程  $ y' + p(x)y = q(x) $ 的求解有以下 3 种常见的方法：

① 公式法： $  y = \mathrm{e}^{-\int p(x)dx} \left[ \int q(x)e^{\int p(x)dx} dx + C \right]  $ 或  $  y = \mathrm{e}^{-\int_{x_{0}}^{x} p(t)dt} \left[ \int_{x_{0}}^{x} q(s)e^{\int_{x_{0}}^{s} p(t)dt} ds + C \right]  $.

② 常数变易法：先求对应齐次方程的通解  $ y = C \mathrm{e}^{-\int p(x)dx} $；设非齐次方程的解为  $ y = C(x) \mathrm{e}^{-\int p(x)dx} $，代入非齐次方程解得  $ C(x) = \int q(x) \mathrm{e}^{\int p(x)dx} \, dx + C $，得非齐次方程的通解  $ y = \mathrm{e}^{-\int p(x)dx} \left[ \int q(x) \mathrm{e}^{\int p(x)dx} \, dx + C \right] $.

③ 积分因子法：方程两边乘  $ e^{\int p(x)dx} $，得  $ \frac{d}{dx}\left(e^{\int p(x)dx}y\right)=q(x)e^{\int p(x)dx} $，两边积分得通解.

例8 求微分方程  $ y' = \frac{\cos y}{\cos y \sin 2y - x \sin y} $ 的通解.

分析 若把 x 作为自变量，则这不属于我们熟悉的基本方程类型。由于方程中的 x 是一次的，若把 y 作为自变量，x 作为未知函数，则它就是一阶线性微分方程。

解  $ \frac{dx}{dy}=\frac{\cos y\sin 2y-x\sin y}{\cos y}=\sin 2y-x\tan y $，方程为

 $$ \frac{\mathrm{d}x}{\mathrm{d}y}+(\tan y)\cdot x=\sin2y, $$ 

其通解为

 $$ x=\mathrm{e}^{\ln\cos y}\left(\int\sin2y\cdot\mathrm{e}^{-\ln\cos y}\,\mathrm{d}y+C\right)=\cos y(C-2\cos y). $$ 

评注 一阶微分方程中 x, y 的地位是对等的，有时将 x 视为 y 的函数，方程可变为已知的类型.

例 9 设  $ f(x) $ 为连续函数，解方程  $ f(x)=\mathrm{e}^{x}+\mathrm{e}^{x}\int_{0}^{x}\left[f(t)\right]^{2}dt $.

分析 积分方程，两边求导化为微分方程. 同时要注意利用方程确定定解条件.

解 由  $ f(x) $ 连续知右端函数可导，方程两边求导得

 $$ f^{\prime}(x)=\mathrm{e}^{x}+\mathrm{e}^{x}\int_{0}^{x}\left[f(t)\right]^{2}\mathrm{d}t+\mathrm{e}^{x}\left[f(x)\right]^{2}, $$ 

再将原方程代入得

 $$ f^{\prime}(x)=f(x)+\mathrm{e}^{x}\left[f(x)\right]^{2}. $$ 

这是伯努利（Bernoulli）方程，两边除以  $ f^{2}(x) $，得

 $$ \frac{f^{\prime}(x)}{f^{2}(x)}-\frac{1}{f(x)}=e^{x}\;. $$ 

令 $ u=\frac{1}{f(x)} $，方程化为

 $$ u^{\prime}+u=-\mathrm{e}^{x}\quad( 一阶线性 ). $$ 

解出

 $$ u(x)=C\mathrm{e}^{-x}-\frac{1}{2}\mathrm{e}^{x},\mathrm{~ 即 ~}f(x)=\frac{1}{C\mathrm{e}^{-x}-\frac{1}{2}\mathrm{e}^{x}}. $$ 

由原方程知  $ f(0)=1 $，代入上式得  $ C=\frac{3}{2} $，所以  $ f(x)=\frac{2}{3\mathrm{e}^{-x}-\mathrm{e}^{x}} $.

评注 （1）伯努利方程 $ \frac{dy}{dx}+p(x)y=q(x)y^n (n\neq0,1) $ 的求解方法是：方程两边除以  $ y^n $，凑微分得 $ \frac{1}{1-n}\cdot\frac{dy^{1-n}}{dx}+p(x)y^{1-n}=q(x) $，这是关于  $ y^{1-n} $ 的一阶线性微分方程.

（2）若方程中含有未知函数的积分，则常采用方程两边求导去掉积分号，化为微分方程求解。积分方程通常是定解问题，要注意用方程确定定解条件。

例 10 设初值问题  $ \left\{\begin{array}{l}x\frac{u y}{d x}-(2x^{2}+1)y=x^{2},\ x\geq1\\y(1)=y_{1}\end{array}\right. $ 的解为  $ y(x) $，确定  $ y_{1} $ 的值，使得  $ \lim_{x\to+\infty}y(x) $ 存在，并求该极限.

分析 一阶线性方程容易求得其解. 为便于讨论极限，解的公式中用定积分表示较好.

解 初值问题写成  $ \left\{\begin{aligned}&\frac{\mathrm{d}y}{\mathrm{d}x}-\left(2x+\frac{1}{x}\right)y=x,&x\geqslant1\\ &y(1)=y_{1}\end{aligned}\right. $

由一阶线性方程的求解公式得到

 $$ \begin{aligned}y(x)&=\mathbf{e}^{\int_{1}^{x}\left(2t+\frac{1}{t}\right)\mathrm{d}t}\left[\int_{1}^{x}t\mathbf{e}^{-\int_{1}^{t}\left(2s+\frac{1}{s}\right)\mathrm{d}s}\mathrm{d}t+y_{1}\right]\\&=\mathbf{e}^{-1}x\mathbf{e}^{x^{2}}\left[\int_{1}^{x}\mathbf{e}\cdot\mathbf{e}^{-t^{2}}\mathrm{d}t+y_{1}\right]=x\mathbf{e}^{x^{2}}\left(\int_{1}^{x}\mathbf{e}^{-t^{2}}\mathrm{d}t+y_{1}\mathbf{e}^{-1}\right).\end{aligned} $$ 

注意到  $ \lim_{x\to+\infty}x\mathrm{e}^{x^{2}}=+\infty $， $ \lim_{x\to+\infty}\int_{0}^{x}\mathrm{e}^{-t^{2}}\,\mathrm{d}t=\frac{\sqrt{\pi}}{2} $，要使  $ \lim_{x\to+\infty}y(x) $ 存在，必须有

 $$ \lim_{x\to+\infty}\left(\int_{1}^{x}\mathrm{e}^{-t^{2}}\mathrm{~d}t+y_{1}\mathrm{e}^{-1}\right)=0, $$ 

即

 $$ y_{1}^{^{\prime}}=-\mathbf{e}\lim_{x\to+\infty}\int_{1}^{x}\mathbf{e}^{-t^{2}}\mathrm{d}t=\mathbf{e}\left(\int_{0}^{1}\mathbf{e}^{-t^{2}}\mathrm{d}t-\frac{\sqrt{\pi}}{2}\right). $$ 

此时

 $$ \operatorname*{l i m}_{x\to+\infty}y(x)=\operatorname*{l i m}_{x\to+\infty}\frac{\displaystyle\int_{1}^{x}\mathrm{e}^{-t^{2}}\mathrm{~d}t+y_{1}\mathrm{e}^{-1}}{\displaystyle\frac{1}{x}\mathrm{e}^{-x^{2}}}=\operatorname*{l i m}_{x\to+\infty}\frac{\mathrm{e}^{-x^{2}}}{-\frac{1}{x^{2}}\mathrm{e}^{-x^{2}}-2\mathrm{e}^{-x^{2}}}=-\frac{1}{2}. $$ 

评注 一阶线性方程 $ \frac{dy}{dx}+p(x)y=q(x) $的通解公式常用不定积分表示，但如果要对其解函数的某些性质进行研讨，则用如下定积分形式更方便：

 $$ y(x)=\mathrm{e}^{-\int_{x_{0}}^{x}p(t)\mathrm{d}t}\left(\int_{x_{0}}^{x}q(t)\mathrm{e}^{\int_{x_{0}}^{t}p(s)\mathrm{d}s}\mathrm{\boldmath~d}t+y_{0}\right). $$ 

若  $ y_{0}=y(x_{0}) $，上式就是满足该初值的特解；若  $ y_{0} $ 是任意常数，上式就是通解.

本题方程的解若用不定积分表示，就很难讨论其极限情况. 下题也类似.

例11 设  $ f(x) $ 在  $ (-\infty,+\infty) $ 连续且有界，又设  $ \int_{-\infty}^{0}e^{x}f(x)dx $ 收敛. 求证：

（1）方程  $ y' + y = f(x) $ 只有一个解在  $ (-∞, +∞) $ 有界.

（2）若又有  $ f(x) $ 且以 T 为周期，则上述方程只有一个解是以 T 为周期的.

分析 这是一阶线性常系数微分方程的特解问题. 只需求出其解再验证条件.

证明 （1）方法1 设  $ y(x) $ 是所给方程的有界解. 方程两边乘以积分因子  $ e^{\int dx} = e^{x} $，得

 $$ \left(\mathrm{e}^{x}y\right)^{\prime}=\mathrm{e}^{x}f(x) $$ 

由于 $ \int_{-\infty}^{0}e^{x}f(x)dx $收敛，将上式两边从 $ -\infty $到 $ x $积分，注意到 $ \lim_{x\to-\infty}(e^{x}y(x))=0 $（ $ \because y(x) $有界），得

 $$ \mathrm{e}^{x}y=\int_{-\infty}^{x}\mathrm{e}^{t}f(t)\mathrm{d}t\ , 即 \ y=\mathrm{e}^{-x}\int_{-\infty}^{x}\mathrm{e}^{t}f(t)\mathrm{d}t\ . $$ 

易验证：

①  $ y' = \mathrm{e}^{-x} \cdot \mathrm{e}^x f(x) - \mathrm{e}^{-x} \int_{-\infty}^{x} \mathrm{e}^t f(t) \, \mathrm{d}t = f(x) - y $，即  $ y' + y = f(x) $。这说明①式是满足题中微分方程唯一的解；

②  $ |y(x)| = \left|e^{-x} \int_{-\infty}^{x} e^{t} f(t) \, dt\right| \leqslant e^{-x} \int_{-\infty}^{x} e^{t} M \, dt = M $，其中  $ |f(x)| \leqslant M (x \in (-\infty, +\infty)) $。这说明①式确定的解在  $ (-∞, +∞) $ 内是有界的。

方法2 先求所给方程的通解，再确定常数，使之成为 $ (-∞,+∞) $上的有界解.

由通解公式得所给方程的全部解为

 $$ y=\mathbf{e}^{-x}\left[\int_{0}^{x}\mathbf{e}^{t}f(t)\mathrm{d}t+C\right]. $$ 

对任一常数  $ C $，当  $ x \in [0, +\infty) $ 时，有

 $$ \left|y(x)\right|\leqslant\mathrm{e}^{-x}\left[\int_{0}^{x}\mathrm{e}^{t}M\mathrm{d}t+\left|C\right|\right]=\mathrm{e}^{-x}(M(\mathrm{e}^{x}-1)+\left|C\right|)\leqslant M+\left|C\right|\quad( 有界 ) $$ 

当  $ x \in (-\infty, 0] $ 时，如果  $ \int_{0}^{-\infty} e^{t} f(t) \, dt + C \neq 0 $，即  $ C \neq \int_{-\infty}^{0} e^{t} f(t) \, dt $，就有

 $$ \lim_{x\to-\infty}y(x)=\lim_{x\to-\infty}e^{-x}\left[\int_{0}^{x}e^{t}f(t)dt+C\right]=\infty. $$ 

所以只有当  $ C=\int_{-\infty}^{0}e^{t}f(t)dt $ 时，对应解  $ y=e^{-x}\int_{-\infty}^{x}e^{t}f(t)dt=y^{*} $ 在  $ (-\infty,0] $ 才有界.

综上，方程有且仅有一个解  $ y^{*}=e^{-x}\int_{-\infty}^{x}e^{t}f(t)dt $ 在  $ (-\infty,+\infty) $ 有界.

（2）若  $ y(x) $ 是所给方程的以 T 为周期的解，则它必是有界的，故只可能是  $ y^{*} $

下面验证如果  $ f(x) $ 以 T 为周期，则  $ y^{*} $ 也以 T 为周期.

由于

 $$ \begin{aligned}{y^{*}(x+T)}&{{}=\mathbf{e}^{-(x+T)}\int_{-\infty}^{x+T}\mathbf{e}^{t}f(t)\mathsf{d}t=\mathbf{e}^{-x}\int_{-\infty}^{x+T}\mathbf{e}^{t-T}f(t)\mathsf{d}t}\\ {}&{{}\xlongequal{u=t-T}\mathbf{e}^{-x}\int_{-\infty}^{x}\mathbf{e}^{u}f(u+T)\mathsf{d}u=\mathbf{e}^{-x}\int_{-\infty}^{x}\mathbf{e}^{u}f(u)\mathsf{d}u=y^{*}(x),}\\ \end{aligned} $$ 

由  $ y^{*}(x) $ 的唯一性知原方程只有一个以 T 为周期的解.

评注　这是求微分方程满足某种性质（如有界性、周期性等）的特解，不是初值问题。解决这类问题的常用方法有两种：

① 利用题设条件求解，再验证得到的解符合题目要求.

② 先求出方程的通解，再根据题设条件确定其常数值.

例 12 已知方程  $ (6y + x^2y^2)\mathrm{d}x + (8x + x^3y)\mathrm{d}y = 0 $ 的两边乘以  $ y^3f(x) $ 后便成为全微分方程，试求出可导函数  $ f(x) $，并解此微分方程.

分析  $ Pdx + Qdy = 0 $ 是全微分方程的充要条件是  $ \frac{\partial Q}{\partial x} = \frac{\partial P}{\partial y} $，由此可求得  $ f(x) $.

解 记  $ P(x,y)=(6y^{4}+x^{2}y^{5})f(x) $， $ Q(x,y)=(8xy^{3}+x^{3}y^{4})f(x) $，由  $ \frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y} $，得

 $$ (8y^{3}+3x^{2}y^{4})f(x)+(8xy^{3}+x^{3}y^{4})f^{\prime}(x)=(24y^{3}+5x^{2}y^{4})f(x)\,. $$ 

化简为  $ xf'(x)=2f(x) $，解得  $ f(x)=Cx^{2} $，且全微分方程为

 $$ (6y^{4}+x^{2}y^{5})x^{2}\mathrm{d}x+(8x y^{3}+x^{3}y^{4})x^{2}\mathrm{d}y=0. $$ 

全微分方程求解有以下几种常见的方法.

① 曲线积分法：

 $$ \begin{align*}u(x,y)=&\int_{(0,0)}^{(x,y)}(6y^{4}+x^{2}y^{5})x^{2}\mathrm{d}x+(8xy^{3}+x^{3}y^{4})x^{2}\mathrm{d}y\\=&\int_{0}^{x}0\mathrm{d}x+\int_{0}^{y}(8xy^{3}+x^{3}y^{4})x^{2}\mathrm{d}y=2x^{3}y^{4}+\frac{1}{5}x^{5}y^{5},\end{align*} $$ 

故微分方程的通解为 $ 10x^{3}y^{4}+x^{5}y^{5}=C $.

② 凑微分法：

由于

 $$ \begin{aligned}&(6y^{4}+x^{2}y^{5})x^{2}\mathrm{d}x+(8xy^{3}+x^{3}y^{4})x^{2}\mathrm{d}y\\=&(6x^{2}y^{4}\mathrm{d}x+8x^{3}y^{3}\mathrm{d}y)+(x^{4}y^{5}\mathrm{d}x+x^{5}y^{4}\mathrm{d}y)\\=&2\mathrm{d}(x^{3}y^{4})+\frac{1}{5}\mathrm{d}(x^{5}y^{5})=\mathrm{d}\left(2x^{3}y^{4}+\frac{1}{5}x^{5}y^{5}\right),\end{aligned} $$ 

得方程的通解为  $ 2x^{3}y^{4}+\frac{1}{5}x^{5}y^{5}=C $.

③ 偏积分法：

设原函数为  $ u(x,y) $，即  $ \mathrm{d}u=(6y^{4}+x^{2}y^{5})x^{2}\mathrm{d}x+(8xy^{3}+x^{3}y^{4})x^{2}\mathrm{d}y $，则有

 $$ \frac{\partial u}{\partial x}=(6y^{4}+x^{2}y^{5})x^{2}, $$ 

 $$ \frac{\partial u}{\partial y}=(8xy^{3}+x^{3}y^{4})x^{2}. $$ 

①式对x积分得

 $$ u=2y^{4}x^{3}+\frac{1}{5}x^{5}y^{5}+\varphi(y)\Rightarrow\frac{\partial u}{\partial y}=8y^{3}x^{3}+x^{5}y^{4}+\dot{\varphi}^{\prime}(y). $$ 

比较②、③两式得  $ \varphi'(y)=0\Rightarrow\varphi(y)=C $ ，得方程的通解为  $ 2x^{3}y^{4}+\frac{1}{5}x^{5}y^{5}=C $

评注 对于微分方程  $ Pdx + Qdy = 0 $，若存在  $ \mu = \mu(x, y) $ 使得  $ \mu Pdx + \mu Qdy = 0 $ 为全微分方程，则称  $ \mu $ 为原方程的一个积分因子。求积分因子没有一般性规律，但下面两种情形可利用公式求得：

(1) 若  $ \frac{1}{Q}\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right) $ 与 y 无关，则  $ \mu(x)=\mathrm{e}^{\int\frac{1}{Q}\left(\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}\right)\mathrm{d}x} $ 是方程  $ P\mathrm{d}x+Q\mathrm{d}y=0 $ 的一个积分因子；

(2) 若  $ \frac{1}{P}\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right) $ 与 x 无关，则  $ \mu(y)=\mathrm{e}^{\int\frac{1}{P}\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}y} $ 是方程  $ P\mathrm{d}x+Q\mathrm{d}y=0 $ 的一个积分因子.

例 13 求下列微分方程的通解：

(1)  $ 2xy \, \mathrm{d}x - \left(x^{2} + y^{3} \sin y\right) \, \mathrm{d}y = 0 $;

(2)  $ (y\cos x - x\sin x)\mathrm{d}x + (y\sin x + x\cos x)\mathrm{d}y = 0 $.

分析 两个方程都难以判断其类型，看能否用上题评注中的方法找到积分因子，或通过凑微分化为全微分方程.

解（1）方法1 将方程左端重新组合并凑微分，有

 $$ \begin{align*}&\left(y\mathrm{d}x^{2}-x^{2}\mathrm{d}y\right)-y^{3}\sin y\mathrm{d}y=0\ ,\\&\frac{y\mathrm{d}x^{2}-x^{2}\mathrm{d}y}{y^{2}}-y\sin y\mathrm{d}y=0\ ,\\&\mathrm{d}\left(\frac{x^{2}}{y}\right)-\mathrm{d}\left(\sin y-y\cos y\right)=0\ .\end{align*} $$ 

得方程的通解

 $$ \frac{x^{2}}{y}-\sin y+y\cos y=C. $$ 

方法2 找积分因子，这里P=2xy， $ Q=-\left(x^{2}+y^{3}\sin y\right) $，有

 $$ \frac{1}{P}\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)=\frac{1}{P}\left[-2x-2x\right]=-\frac{2}{y}, $$ 

因而  $ \mu = e^{\int \frac{2}{y} dy} = \frac{1}{y^2} $ 是方程的一个积分因子，用  $ \frac{1}{y^2} $ 乘以原方程得全微分方程，再求解（略）.

（2）方法1 找积分因子，这里  $ P = y \cos x - x \sin x $， $ Q = y \sin x + x \cos x $，有

 $$ \frac{1}{P}\bigg(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\bigg)=\frac{1}{P}\Big[\big(y\cos x+\cos x-x\sin x\big)-\cos x\Big]=1, $$ 

因而  $ \mu = e^{\int dy} = e^y $ 是方程的一个积分因子，用  $ e^y $ 乘以原方程得全微分方程

 $$ \mathbf{e}^{y}\left(y\cos x-x\sin x\right)\mathrm{d}x+\mathbf{e}^{y}\left(y\sin x+x\cos x\right)\mathrm{d}y=0. $$ 

用曲线积分求势函数

 $$ \begin{aligned}u(x,y)=&\int_{(0,0)}^{(x,y)}\mathrm{e}^{y}\left(y\cos x-x\sin x\right)\mathrm{d}x+\mathrm{e}^{y}\left(y\sin x+x\cos x\right)\mathrm{d}y\\ =&\int_{0}^{x}-x\sin x\mathrm{d}x+\int_{0}^{y}\mathrm{e}^{y}\left(y\sin x+x\cos x\right)\mathrm{d}y\\ =&\left[x\cos x-\sin x\right]+\left[\mathrm{e}^{y}(y-1)\sin x+\sin x+(\mathrm{e}^{y}-1)x\cos x\right]\\ =&\mathrm{e}^{y}\left[(y-1)\sin x+x\cos x\right].\end{aligned} $$ 

则原方程的通解为

 $$ \mathbf{e}^{y}\left[(y-1)\sin x+x\cos x\right]=C. $$ 

方法2 将方程左端重新组合并凑微分，有

 $$ \begin{aligned}&\left(y\cos x-x\sin x\right)\mathrm{d}x+\left(y\sin x+x\cos x\right)\mathrm{d}y\\=&\left(y\mathrm{d}\sin x+\sin x\mathrm{d}y\right)-x\sin x\mathrm{d}x+\left[(y-1)\sin x+x\cos x\right]\mathrm{d}y\\=&\mathrm{d}(y\sin x)+\mathrm{d}(x\cos x-\sin x)+\left[(y-1)\sin x+x\cos x\right]\mathrm{d}y\\=&\mathrm{d}\left[(y-1)\sin x+x\cos x\right]+\left[(y-1)\sin x+x\cos x\right]\mathrm{d}y.\end{aligned} $$ 

则原方程可化为

 $$ \frac{\mathrm{d}\left[(y-1)\sin x+x\cos x\right]}{(y-1)\sin x+x\cos x}+\mathrm{d}y=0. $$ 

积分可得通解  $ \mathrm{e}^{y}\left[(y-1)\sin x+x\cos x\right]=C $.

评注 可以证明，凡能用初等积分法求解的一阶微分方程都能通过乘以积分因子化为全微分方程，所以当一个方程的类型难以辨别时，不妨从化为全微分方程（凑微分或求积分因子）的思路去寻找求解方法。

例  $ 14^{*} $ 设 S 是以 L 为边界的光滑曲面，试求可微函数  $ \varphi(x) $，使曲面积分

 $$ \iint\limits_{S}(1-x^{2})\varphi(x)\mathrm{d}y\mathrm{d}z+4xy\varphi(x)\mathrm{d}z\mathrm{d}x+4xz\mathrm{d}x\mathrm{d}y $$ 

与曲面 S 的形状无关.

分析 若曲面积分与曲面的形状无关，则任意闭曲面上的积分为 0，利用高斯公式得到三重积分的恒等式，可得到对应的微分方程.

解 以 L 为边界任作两个光滑曲面  $ S_1 $、 $ S_2 $，它们的法向量指向同一侧，由题意有  $ \iint_{S_1} = \iint_{S_2} $ 。记  $ S^* $ 为  $ S_1 $ 与  $ S_2 $ 所围成的闭曲面，取外侧，则  $ \iint_{S^*} = \iint_{S_1} + \iint_{S_2} = \iint_{S_1} - \iint_{S_2} = 0 $。

记 $ S^{*} $所围立体区域为 $ \Omega $，由高斯公式得

 $$ \iiint_{\Omega}\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)\mathrm{d}V=0\;. $$ 

由 $ \Omega $的任意性得

 $$ \frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}=0\implies-2x\varphi(x)+(1-x^{2})\varphi^{\prime}(x)+4x\varphi(x)+4x=0, $$ 

即  $ \varphi'(x) + \frac{2x}{1-x^{2}}\varphi(x) = -\frac{4x}{1-x^{2}} $，解出  $ \varphi(x) = -Cx^{2} + C - 2 $.

评注 利用曲线积分与路径无关，曲面积分与曲面形状无关等条件可建立微分方程，确定被积式中的某些未知函数。

例 $15^{*}$ 设级数 $\frac{x^{4}}{2.4} + \frac{x^{6}}{2.4.6} + \frac{x^{8}}{2.4.6.8} + \cdots (-\infty < x < +\infty)$ 的和函数为 $S(x)$，求 $S(x)$ 的表达式.

分析 对  $ S(x) $ 求导，找出  $ S'(x) $ 与  $ S(x) $ 的关系，也就是找到  $ S(x) $ 所满足的微分方程，解方程可得  $ S(x) $ 的表达式.

解 （1） $ S(x)=\frac{x^{4}}{2\cdot4}+\frac{x^{6}}{2\cdot4\cdot6}+\frac{x^{8}}{2\cdot4\cdot6\cdot8}+\cdots $，易见  $ S(0)=0 $，

 $$ S^{\prime}(x)=\frac{x^{3}}{2}+\frac{x^{5}}{2\cdot4}+\frac{x^{7}}{2\cdot4\cdot6}+\cdots=x\left(\frac{x^{2}}{2}+\frac{x^{4}}{2\cdot4}+\frac{x^{6}}{2\cdot4\cdot6}+\cdots\right)=x\left[\frac{x^{2}}{2}+S(x)\right], $$ 

因此  $ S(x) $ 是初值问题  $ \left\{\begin{aligned}y^{\prime}&=xy+\frac{x^{3}}{2}\\ y(0)&=0\end{aligned}\right. $ 的解. 方程的通解为

 $$ y=\mathrm{e}^{\int x\mathrm{d}x}\left[\int\frac{x^{3}}{2}\mathrm{e}^{-\int x\mathrm{d}x}\mathrm{d}x+C\right]=-\frac{x^{2}}{2}-1+C\mathrm{e}^{\frac{x^{2}}{2}}, $$ 

由初始条件  $ y(0)=0 $，得 C=1。故  $ S(x)=-\frac{x^{2}}{2}+e^{\frac{x^{2}}{2}}-1 $。

评注 当幂级数的系数为分式，且分母为阶乘形式时，其和函数通常会满足某个微分方程（不一定是一阶方程），找到对应的微分方程是求解的关键。

例  $ 16^{*} $ 求微分方程  $ y + y' = \ln \sqrt{1 + y'^{2}} $ 的通解.

分析 方程的特点是不显含变量 $x$。如果令 $y' = \tan t$，代入方程可得 $y = \ln |\sec t| - \tan t$，若能求得 $x$ 关于变量 $t$ 的表达式，则微分方程的解就找到了（解为参数式函数）。

解 令  $ y' = \tan t $，代入方程得  $ y = \ln |\sec t| - \tan t $。所以

$$\mathrm{d}x=\frac{\mathrm{d}y}{y^{\prime}}=\left(1-\frac{\sec^{2}t}{\tan t}\right)\mathrm{d}t,\text{积分得}x=t-\ln|\tan t|+C.$$

于是得到微分方程参数形式的通解

 $$ \left\{\begin{aligned}{x=t-\operatorname{l n}|\operatorname{t a n}t|+C,}\\ {y=\operatorname{l n}|\operatorname{s e c}t|-\operatorname{t a n}t.}\\ \end{aligned}\right. $$ 

评注（1）通常称微分方程的这类解法叫“参数式解法”。若能消去参数，则就是通积分（隐函数解）。

（2）形如 $ F(y,y')=0 $或 $ F(x,y')=0 $的方程，可考虑用“参数式解法”求解.

对方程  $ F(y,y')=0 $，可令  $ y=\varphi(t) $，由方程解得  $ y'=\psi(t) $（或令  $ y'=\psi(t) $，解得  $ y=\varphi(t) $），再由  $ \mathrm{d}x=\frac{\mathrm{d}y}{y'}=\frac{\varphi'(t)}{\psi(t)}\mathrm{d}t $，积分得  $ x=\int\frac{\varphi'(t)}{\psi(t)}\mathrm{d}t $。即微分方程的通解为  $ \left\{\begin{aligned}x&=\int\frac{\varphi'(t)}{\psi(t)}\mathrm{d}t\\ y&=\varphi(t)\end{aligned}\right. $（显然  $ y=\varphi(t) $ 或  $ y'=\psi(t) $ 的选取具有多样性）。

将上面解法中的 y 换为 x，很容易得到  $ F(x,y')=0 $ 型方程的求解.

例  $ 17^{*} $ 求微分方程  $ y' + x = \sqrt{x^{2} + y} $ 的通解.

分析 很难看出该方程属于哪一类可求解的方程. 若能将等式右端的函数分离变量, 方程的求解就容易了. 为此, 可作变量代换  $ y = x^{2} u $.

解 令  $ y = x^{2} u $，则  $ y' = 2 x u + x^{2} u' $，代入方程化为

 $$ 2xu+x^{2}u^{\prime}+x=x\sqrt{1+u}\ , 即 \frac{\mathrm{d}u}{\sqrt{1+u}-1-2u}=\frac{\mathrm{d}x}{x}\ . $$ 

由于

 $$ \begin{aligned}\int\frac{\mathrm{d}u}{\sqrt{1+u}-1-2u}&\xlongequal{t=\sqrt{1+u}}-\int\frac{2t\mathrm{d}t}{2t^{2}-t-1}=-\frac{1}{3}\int\left[\frac{2}{t-1}+\frac{1}{t+1/2}\right]\mathrm{d}t\\ =-\frac{1}{3}\ln(t-1)^{2}\left(t+\frac{1}{2}\right)+C.\end{aligned} $$ 

所以方程 $ ^{①} $两边积分得

 $$ -\frac{1}{3}\ln(t-1)^{2}\left(t+\frac{1}{2}\right)=\ln x-\frac{1}{3}\ln C\ ,\  即 \left(t^{3}-\frac{3}{2}t^{2}+\frac{1}{2}\right)x^{3}=C\ . $$ 

于是，所给微分方程的通解为

 $$ \left[\left(1+\frac{y}{x^{2}}\right)^{\frac{3}{2}}-\frac{3}{2}\left(1+\frac{y}{x^{2}}\right)^{2}+\frac{1}{2}\right]x^{3}=C\ ,\mathrm{~ 即 }\left(x^{2}+y^{2}\right)^{\frac{3}{2}}-x^{3}-\frac{3}{2}x y=C\ . $$ 

评注 根据方程的特点作变量代换，化方程为已知方程类型是较常见的求解方法.

例  $ 18^{*} $ 考虑 x 的两个可微的且不恒为零的函数，使得它们之商的导数等于它们的导数之商. 如果已知其中一个函数，试求出另一个函数的表达式，并给出这样两个具体函数的例子.

分析 需找出非零函数 $ f(g) $和 $ g $，使得 $ \left(\frac{f}{g}\right)^{\prime}=\frac{f^{\prime}}{g^{\prime}} $。由于 $ f $与 $ g $不可交换，即 $ \left(\frac{f}{g}\right)^{\prime}=\frac{f^{\prime}}{g^{\prime}} $成立时，未必有 $ \left(\frac{g}{f}\right)^{\prime}=\frac{g^{\prime}}{f^{\prime}} $也成立，所以需分别讨论已知 $ f $与已知 $ g $的情况。

解 设  $ f $ 和  $ g $ 是两个满足题设条件的函数，由题意  $ \frac{fg - fg'}{g^2} = \frac{f'}{g'} $ 变形为

 $$ g(g^{\prime}-g)f^{\prime}-g^{\prime2}f=0. $$ 

若 g 是某区间 I 上已知的可微函数，当 g、 $ g^{\prime}-g $ 和  $ g^{\prime} $ 在 I 上都不等于零时，则①式是未知函数 f 的一个一阶线性齐次微分方程，其通解为

 $$ f(x)=C\exp\int\frac{g^{\prime2}}{g(g^{\prime}-g)}\mathrm{d}x\quad\left( 任意常数 C\neq0\right). $$ 

为确定出一个具体的函数，取  $ I = \mathbb{R} $ 和  $ g(x) = e^{\lambda x} $，若  $ \lambda \neq 1 $，由②式可得  $ f(x) = C \exp\left(\frac{\lambda^2}{\lambda - 1}\right) x $。例如选择  $ \lambda = 2 $， $ C = 1 $，便有  $ f(x) = e^{4x} $， $ g(x) = e^{2x} $， $ f(x) / g(x) = e^{2x} $，且  $ (f / g)' = 2e^{2x} = f' / g' $。

若$f$是某区间$I$上已知的可微函数，当$f$在$I$上不等于零时，则①式是未知函数$g$的一个一阶非线性齐次微分方程（“齐次微分方程”的概念与求解，参看7.2节例7评注）。令$g(x)=\mathrm{e}^{\int z(x)\,\mathrm{d}x}$，方程①化为

 $$ f  z^{2}-f^{\prime}  z+f^{\prime}=0\,. $$ 

解得  $ z=\frac{f' \pm \sqrt{f'^2 - 4f'f}}{2f} $，则方程①的通解为

 $$ g(x)=C\exp\int\frac{f^{\prime}\pm\sqrt{f^{\prime2}-4f^{\prime}f}}{2f}\mathrm{d}x\quad( 任意常数 C\neq0). $$ 

若取  $ f(x) = \mathrm{e}^{\lambda x} $（ $ \lambda \neq 1 $），由③式可得  $ g(x) = C \exp\left(\frac{\lambda \pm \sqrt{\lambda^2 - 4\lambda}}{2}\right)x $，取  $ \lambda = 4 $，C = 1，有  $ f(x) = \mathrm{e}^{4x} $， $ g(x) = \mathrm{e}^{2x} $，这与前面所给出的具体例子完全一样.

例 19 设  $ y = y(x) $ 是微分方程  $ \frac{dy}{dx} = \frac{1}{1 + x^2 + y^2} $ 的任意一个解，证明  $ \lim_{x \to +\infty} y(x) $ 与  $ \lim_{x \to -\infty} y(x) $ 都存在.

分析 显然  $ y(x) $ 为严格单调递增函数，只需证明  $ y(x) $ 有界即可.

证明 在  $ y = y(x) $ 的定义域内取  $ x_{0} $，记  $ y_{0} = y(x_{0}) $ 。将  $ y = y(x) $ 代入所给方程，有

 $$ \frac{\mathrm{d}y(x)}{\mathrm{d}x}=\frac{1}{1+x^{2}+y^{2}(x)}>0, $$ 

所以  $ y(x) $ 为严格单调递增函数. 以下证它有界. 由于

 $$ \mathrm{d}y(x)=\frac{1}{1+x^{2}+y^{2}(x)}\mathrm{d}x, $$ 

两边从 $ x_{0} $到x积分，有

 $$ y(x)=y(x_{0})+\int_{x_{0}}^{x}\frac{1}{1+x^{2}+y^{2}(x)}\mathrm{d}x. $$ 

设 $ x \geqslant x_{0} $，于是

 $$ \begin{aligned}y(x)&\leqslant y(x_{0})+\int_{x_{0}}^{x}\frac{1}{1+x^{2}}\mathrm{d}x\\&=y(x_{0})+\arctan x-\arctan x_{0}<y_{0}+\frac{\pi}{2}-\arctan x_{0},\end{aligned} $$ 

y(x) 有上界，所以  $ \lim_{x\to\infty}y(x) $ 存在.

类似可证，当  $ x \leq x_{0} $ 时， $ y(x) $ 有下界，所以  $ \lim_{x \to \infty} y(x) $ 也存在.

例  $ 20^{*} $ 设函数  $ h_{1}(x) $、 $ h_{2}(x) $ 以及  $ g(x) $ 当  $ x \geq x_{0} $ 时连续，且  $ h_{1}(x) \geq h_{2}(x) $，若函数  $ u(x) $ 与  $ v(x) $ 分别是微分方程  $ y' + g(x)y = h_{1}(x) $ 与  $ y' + g(x)y = h_{2}(x) $ 满足初值条件  $ u(x_{0}) = v(x_{0}) = c $ 的解，证明：

（1）当 $ x \geqslant x_{0} $时，有 $ \nu(x) \geqslant u(x) $.

（2）在  $ x > x_{0} $ 的附近，初值问题  $ v' + g(x)v = v^{2} $， $ v(x_{0}) = c $ 的解可以写成

 $$ \nu(x)=\operatorname*{m a x}_{w}\left(c\operatorname{e}^{-\int_{x_{0}}^{x}[g(t)-2w(t)]\mathrm{d}t}-\int_{x_{0}}^{x}\operatorname{e}^{\int_{x}^{s}[g(t)-2w(t)]\mathrm{d}t}w^{2}(s)\mathrm{d}s\right). $$ 

其中，极大值对任何连续函数  $ w(t) $ 在某个区间  $ [x_{0}, x] $ 上是确定的.

分析（1）只需证明方程  $ w' + g(x)w = \varphi(x) $ ( $ \varphi(x) \geq 0 $) 满足初值  $ w(x_0) = 0 $ 的解在  $ x \geq x_0 $ 时非负.

（2）借用（1）的结果，需要构造 $ u(x) $所对应的一阶线性微分方程。由需要证明的结论可看出该方程应该是 $ u'(g-2w)u=-w^2 $。

解 （1）记  $ w(x)=v(x)-u(x) $，  $ \varphi(x)=h_{2}(x)-h_{1}(x) $，由题意知，当  $ x\geqslant x_{0} $ 时，  $ \varphi(x)\geqslant0 $

 $$ u^{\prime}+g(x)u=h_{1}(x)~,\quad v^{\prime}+g(x)v=h_{2}(x)~. $$ 

两式相减得

 $$ w^{\prime}+g(x)w=\varphi(x)\;,\quad w(x_{0})=0. $$ 

满足初值的解为

 $$ w(x)=\mathrm{e}^{-\int_{x_{0}}^{x}g(t)\mathrm{d}t}\left(\int_{x_{0}}^{x}\mathrm{e}^{\int_{x_{0}}^{s}g(t)\mathrm{d}t}\varphi(s)\mathrm{d}s\right). $$ 

当 $ x \geqslant x_{0} $时，显然有 $ w(x) \geqslant 0 $，即 $ v(x) \geqslant u(x) $.

(2)假定 v 在某个区间  $ [x_0, x] $ 上满足  $ v' + g(x)v = v^2 $,  $ v(x_0) = c $, 并在  $ [x_0, x] $ 上任选一个连续函数 w, 则  $ (v - w)^2 \geq 0 $,  $ v^2 \geq 2wv - w^2 $,  $ v' + g(x)v \geq 2wv - w^2 $, 即有

 $$ v^{\prime}+(g-2w)v\geq-w^{2}\;,\quad v(x_{0})=c\;. $$ 

做方程

 $$ u^{\prime}+(g-2w)u=-w^{2}\;,\quad u(x_{0})=c\;. $$ 

方程②的解为

 $$ \begin{aligned}{u(x)}&{{}=\mathsf{e}^{-\int_{x_{0}}^{x}\left[g(t)-2w(t)\right]\mathsf{d}t}\left(c-\int_{x_{0}}^{x}\mathsf{e}^{\int_{x_{0}}^{s}\left[g(t)-2w(t)\right]\mathsf{d}t}w^{2}(s)\mathsf{d}s\right)}\\ {}&{{}=c\mathsf{e}^{-\int_{x_{0}}^{x}\left[g(t)-2w(t)\right]\mathsf{d}t}-\int_{x_{0}}^{x}\mathsf{e}^{\int_{x}^{s}\left[g(t)-2w(t)\right]\mathsf{d}t}w^{2}(s)\mathsf{d}s.}\\ \end{aligned} $$ 

由（1）知  $ \nu(x) \geq u(x) $. 若取  $ w = \nu $，则上面一系列不等式成为等式. 因此

 $$ \nu(x)=\operatorname*{m a x}_{w}\left(c\operatorname{e}^{-\int_{x_{0}}^{x}[g(t)-2w(t)]\mathop{}\mathrm{d}t}-\int_{x_{0}}^{x}\operatorname{e}^{\int_{x}^{s}[g(t)-2w(t)]\mathop{}\mathrm{d}t}w^{2}(s)\mathop{}\mathrm{d}s\right). $$ 

评注 该题中的结论（1）也称为一阶线性微分方程的比较定理，该结论也可推广到二阶线性微分方程的初值问题（见7.2节例18）.

##### 习题7.1

1. 设  $ f(x) $ 在区间  $ (0, +\infty) $ 内有定义，且  $ f'(1) = a \neq 1 $，又设对任意  $ x, y \in (0, +\infty) $，恒有  $ f(xy) = f(x) + f(y) + (x-1)(y-1) $.

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//141cc620-1e63-45b4-87fa-7dc77976115c/markdown_0/imgs/img_in_image_box_1243_981_1377_1109.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A33Z%2F-1%2F%2F4cbc5ebf6d13fdad2fc57225e0a89122dcc1b5f26790c834b4a1ab0e24393576" alt="Image" width="9%" /></div>


<div style="text-align: center;"><div style="text-align: center;">习题 7.1 答案</div> </div>


 $$ f(x) $$ 

2. 若函数  $ y = y(x) $ 连续，且满足  $ x \int_{1}^{x} y(t) \, dt = (x+1) \int_{1}^{x} ty(t) \, dt - x + 1 $，求函数  $ y(x) $.

3. 设函数  $ f(x) $ 在区间 I 上处处可导，对  $ \forall a \in I $，有  $ \lim_{x \to a} \frac{xf(a) - af(x)}{x - a} = a^2 e^a $，求  $ f(x) $.

4. 设函数  $ f(x) $ 可导，且对任何实数 x，h 满足  $ f(x) \neq 0 $， $ f(x+h) = \int_{x}^{x+h} \frac{t(t^2+1)}{f(t)} \, dt + f(x) $。此外， $ f(1) = \sqrt{2} $，求  $ f(x) $ 的表达式。

5. 求下列微分方程的通解：（1） $ \frac{dy}{dx}=\frac{1}{x\sin^2(xy)}-\frac{y}{x} $; （2） $ y'+\frac{y}{x}=y^2-\frac{4}{x^2} $.

6. 微分学中的一个错误结论是： $ (fg)' = f'g' $. 如果  $ f(x) = \mathrm{e}^{x^2} $，是否存在一个开区间  $ (a,b) $ 和定义在  $ (a,b) $ 上的非零函数 g 使得这个错误的乘积对于  $ (a,b) $ 中的 x 是对的.

7. 求下列微分方程的通解: (1)  $ (1-x)y' + y = x $;

 $$ (x^{2}+y^{2}+3)\frac{\mathrm{d}y}{\mathrm{d}x}=2x\left(2y-\frac{x^{2}}{y}\right). $$ 

8. 设 $ \int_{0}^{1}f(tx)dt=\frac{1}{2}f(x)+1 $，其中 $ f(x) $为连续函数，求 $ f(x) $.

9. 设  $ f(x) $ 在  $ (-\infty,+\infty) $ 上可导，且其反函数存在，为  $ g(x) $。若  $ \int_0^{f(x)} g(t) \, \mathrm{d}t + \int_0^x f(t) \, \mathrm{d}t = x e^x - e^x + 1 $，求函数  $ f(x) $。

10. 设  $ \varphi(x) $ 是以  $ 2\pi $ 为周期的连续函数，且  $ \Phi'(x) = \varphi(x) $， $ \Phi(0) = 0 $， $ \Phi(2\pi) \neq 0 $。

（1）求解  $ y' + y \sin x = \varphi(x) e^{\cos x} $;

（2）以上解中是否存在以 $ 2\pi $为周期的解，若有，则求之.

11. 设有微分方程  $ y' - 2y = \varphi(x) $，其中  $ \varphi(x) = \left\{ \begin{aligned} 2, & \quad x < 1, \\ 0, & \quad x > 1. \end{aligned} \right. $，试求在  $ (-\infty, +\infty) $ 内的连续函数  $ y = y(x) $，使之在  $ (-\infty, 1) $ 和  $ (1, +\infty) $ 内都满足所给方程，且满足条件  $ y(0) = 0 $。

12. 设  $ z = z(x, y) $ 在 x > 0 处有连续的二阶偏导数，曲线积分  $ \oint_L \frac{z}{2x} \, \mathrm{d}x + \frac{\partial z}{\partial y} \, \mathrm{d}y = 0 $（其中  $ L $ 是半平面  $ x > 0 $ 内的任一简单闭曲线），求函数  $ z(x, y) $，使满足  $ z(1, y) = \sin y $， $ z(x, \pi) = x \ln x $，并计算曲线积分  $ I = \int_{(1,0)} (\frac{\pi}{2x}) \frac{z}{2x} \, \mathrm{d}x + \frac{\partial z}{\partial y} \, \mathrm{d}y $。

13. 求下列微分方程的通解：

 $$ y^{\prime}+x\sin2y=x\mathrm{e}^{-x^{2}}\cos^{2}y\;;\quad(2)\frac{\mathrm{d}x}{\sqrt{xy}}+\left(\frac{2}{y}-\sqrt{\frac{x}{y^{3}}}\right)\mathrm{d}y=0\;;\quad(3)y^{\prime}=\frac{x\cos y}{\sin2y-x^{2}\sin y+\cos y}. $$ 

14. 求下列微分方程的通解：

(1)  $ \frac{dy}{dx} = \frac{y}{x^6 y^3 - x} $; (2)  $ y' = \frac{4x^3 y}{x^4 + y^2} $.

15. 设函数  $ f(u) $ 有连续的一阶导数， $ f(2)=1 $，且函数  $ z=xf\left(\frac{y}{x}\right)+yf\left(\frac{y}{x}\right) $ 满足

 $$ \frac{\partial z}{\partial x}+\frac{\partial z}{\partial y}=\frac{y}{x}-\left(\frac{y}{x}\right)^{3}\quad(x>0,y>0), $$ 

求z的表达式.

16. 设  $ L: y = y(x) > 0 $ 是从点  $ A(0,1) $ 到点  $ B(x,y) $ 的有向光滑曲线， $ y = y(x) $ 满足关系式

 $$ \int_{L(AB)}\left(6x^{2}-x+2x\sqrt{y}\right)\mathrm{d}x+\frac{1}{2\sqrt{y}}\mathrm{d}y=2x^{3} $$ 

求 $ y(x) $.

17. 求下列微分方程的通解：

(1)  $ (\ln y + 2x - 1)\frac{\mathrm{d}y}{\mathrm{d}x} = 2y $; (2)  $ (x^{2} + y^{2} + y)\mathrm{d}x - x\mathrm{d}y = 0 $;

(3)  $ (xy + y + \sin y)d x + (x + \cos y)d y = 0 $

18*. 求下列微分方程的通解：(1)  $ x^{3} + y'^{3} - 3xy' = 0 $; (2)  $ y'^{3} - y^{2}(a - y') = 0 $.

19. 设  $ y = y(x) $ 满足关系式  $ y(x) = x^{3} - x \int_{1}^{x} \frac{y(t)}{t^{2}} \, dt + y'(x) \, (x > 0) $，且极限  $ \lim_{x \to +\infty} \frac{y(x)}{x^{3}} $ 存在，求  $ y(x) $

20. 设  $ F(x) = f(x)g(x) $，其中函数  $ f(x), g(x) $ 在  $ (-\infty, +\infty) $ 内满足条件  $ f'(x) = g(x) $， $ g'(x) = f(x) $ 且  $ f(0) = 0 $， $ f(x) + g(x) = 2e^x $，求  $ F(x) $ 的表达式.

21. 设微分方程  $ y' + ay = f(x) $ 中的  $ f(x) $ 在区间  $ [0, +\infty) $ 上连续，且  $ \lim_{x \to +\infty} f(x) = b $ （常数），证明：

（1）若常数a>0，则该方程的一切解 $ y(x) $均有 $ \lim_{x\to+\infty}y(x)=\frac{b}{a} $;

（2）若常数 a<0，则该方程仅有一个解  $ y_{1}(x) $ 满足  $ \lim_{x\to+\infty}y_{1}(x)=\frac{b}{a} $，其余的解  $ y(x) $ 均有  $ \lim_{x\to+\infty}y(x)=\infty $，并求出  $ y_{1}(x) $.

## 7.2 高阶微分方程

# 1. 可降阶高阶微分方程

某些高阶微分方程通过适当的变量代换可降低其阶数，最终化为一阶微分方程求解，这就是所谓降阶法。降阶法的关键是要根据方程的特点选取有效的代换。

例1 已知  $ z = x f\left(\frac{y}{x}\right) + 2 y f\left(\frac{x}{y}\right) $，其中 f 二次可微. 若  $ \left.\frac{\partial^{2}z}{\partial x\partial y}\right|_{x=a} = -by^{2} $，求函数 f.

分析 f 是一元函数，对 z 的函数式求  $ \frac{\sigma^{-}z}{\partial x\partial y} $，代入所给偏导数方程便可得到关于 f 的微分方程.

解  $ \frac{\partial z}{\partial x}=f\left(\frac{y}{x}\right)-\frac{y}{x}f^{\prime}\left(\frac{y}{x}\right)+2f^{\prime}\left(\frac{x}{y}\right) $， $ \frac{\partial^{2}z}{\partial x\partial y}=-\frac{y}{x^{2}}f^{\prime\prime}\left(\frac{y}{x}\right)-\frac{2x}{y^{2}}f^{\prime\prime}\left(\frac{x}{y}\right) $.

由 $ \left.\frac{\partial^{2}z}{\partial x\partial y}\right|_{x=a}=-by^{2} $，可得到

 $$ \frac{y}{a^{2}}f^{\prime\prime}\left(\frac{y}{a}\right)+\frac{2a}{y^{2}}f^{\prime\prime}\left(\frac{a}{y}\right)=by^{2}. $$ 

令 y=au，得

 $$ u^{3}f^{\prime\prime}(u)+2f^{\prime\prime}\left(\frac{1}{u}\right)=a^{3}b u^{4}, $$ 

上式中以 $ \frac{1}{u} $换u得

 $$ f^{\prime\prime}\left(\frac{1}{u}\right)+2u^{3}f^{\prime\prime}(u)=a^{3}b\frac{1}{u}. $$ 

上面两式联立可解得

 $$ f^{\prime\prime}(u)=\frac{a^{3}b}{3}\left(\frac{2}{u^{4}}-u\right). $$ 

这是一个可降阶方程，积分两次得  $ f(u)=\frac{a^3b}{3}\left(\frac{1}{3u^2}-\frac{1}{6}u^3\right)+C_1u+C_2 $.

例2 求微分方程  $ (1-x)y''=\frac{1}{5}\sqrt{1+y'^2} $ 满足  $ y(0)=0,\ y'(0)=0 $ 的特解.

分析 此方程不显含 y，属于  $ y'' = f(x, y') $ 型，令  $ y' = p(x) $，将方程转化为一阶方程求解.

解 令  $ y'=p(x) $，则  $ y''=p' $，代入方程得

 $$ (1-x)p^{\prime}=\frac{1}{5}\sqrt{1+p^{2}}\Rightarrow\frac{\mathrm{d}p}{\sqrt{1+p^{2}}}=\frac{\mathrm{d}x}{5(1-x)}. $$ 

积分得

 $ \ln(p+\sqrt{1+p^{2}})=-\frac{1}{5}\ln(1-x)+C_{1} $，由 $ p(0)=0 $，得 $ C_{1}=0 $

即  $ y' + \sqrt{1 + {y'}^{2}} = (1 - x)^{-\frac{1}{5}} $，由此得  $ y' - \sqrt{1 + {y'}^{2}} = -(1 - x)^{\frac{1}{5}} $，两式相加得

 $$ 2y^{\prime}=(1-x)^{\frac{1}{5}}-(1-x)^{\frac{1}{5}} $$ 

积分，并由  $ y(0)=0 $ 得

 $$ y=-\frac{5}{8}(1-x)^{\frac{4}{5}}+\frac{5}{12}(1-x)^{\frac{6}{5}}+\frac{5}{24}. $$ 

评注 在解出 p 的通解后，应及时利用初值条件  $ y'(x_{0}) = y_{0} $ 确定通解中的任意常数，这样可能便后面的计算简化；同时要将关于 p 的通解  $ F(p, x) = 0 $ 化为显函数  $ p = p(x) $ 的形式，以便于下一步求解 y.

例3 求方程 $ y''+(y')^{2}=2e^{-y} $的通解.

分析 此方程不显含 x，属于  $ y'' = f(y, y') $ 型，令  $ y' = p(y) $，将方程转化为一阶方程求解.

解 令  $ y'=p(y) $，则  $ y''=p\frac{dp}{dy} $，原方程可化为

 $$ p\frac{\mathrm{d}p}{\mathrm{d}y}+p^{2}=2\mathrm{e}^{-y}\;. $$ 

这是伯努利方程，令  $ z=p^{2} $，上式化为一阶线性方程  $ \frac{dp}{dx}=q $，其通解为

 $$ z=\mathrm{e}^{-\int2\mathrm{d}y}\left(\int4\mathrm{e}^{-y}\mathrm{e}^{\int2\mathrm{d}y}\mathrm{d}y+c_{1}\right)=4\mathrm{e}^{-y}+c_{1}\mathrm{e}^{-2y}, $$ 

即  $ y^{\prime2}=p^{2}=4e^{-y}+c_1e^{-2y} \Rightarrow y^{\prime}=\pm\sqrt{4e^{-y}+c_1e^{-2y}} $

分离变量并积分得

 $$ \pm\frac{1}{2}\sqrt{4\mathrm{e}^{y}+c_{1}}=x+c_{2}\Rightarrow\mathrm{e}^{y}+c_{3}=\left(x+c_{2}\right)^{2}\left( 其中 c_{3}=\frac{c_{1}}{4}\right). $$ 

故原方程的通解为  $  y = \ln(x^{2} + ax + b)  $ （a, b 为任意常数）.

评注 注意不显含 x 与不显含 y 两类可降阶微分方程在求解中，其二阶导数在形式上的差异.

 $$ y^{\prime}y^{m}-2(y^{n})^{2}=0 $$ 

分析 此方程不显含 x，也不显含 y，因此可按两种方法分别求解，但按不显含 y 的方程求解更简单.

解 方法1 按不显含 y 的方程求解. 令  $ y'=p $，则  $ y''=\frac{dp}{dx} $， $ y'''=\frac{d^2p}{dx^2} $，代入方程得

 $$ p\frac{\mathbf{d}^{2}p}{\mathbf{d}x^{2}}-2\bigg(\frac{\mathbf{d}p}{\mathbf{d}x}\bigg)^{2}=0\quad( 不显含 x) $$ 

令 $ \frac{dp}{dx}=q $，代入上面方程得

 $$ pq\frac{\mathrm{d}q}{\mathrm{d}p}-2q^{2}=0\ . $$ 

当 $ q=\frac{dp}{dx}=y^{\prime\prime}\neq0 $且 $ p\neq0 $时，方程为 $ \frac{dq}{q}=2\frac{dp}{p} $。其通解为

 $$ q=C_{1}p^{2},\mathrm{~ 即 }\frac{\mathrm{d}p}{\mathrm{d}x}=C_{1}p^{2}. $$ 

解出  $ p=\frac{1}{\tilde{C}_{1}x+C_{2}} $（其中  $ \tilde{C}_{1}=-C_{1} $），即  $ \frac{dy}{dx}=\frac{1}{\tilde{C}_{1}x+C_{2}} $，积分得原方程的通解为

 $$ y=\frac{1}{\tilde{C}_{1}}\ln\left|\tilde{C}_{1}x+C_{2}\right|+C_{3}. $$ 

当  $ q = \frac{dp}{dx} = y'' = 0 $ 时，有  $ y = a_1x + a_2 $ （ $ a_1, a_2 $ 为任意常数），也是方程的解。

若  $ p = y' = 0 $，则有  $ y = a $，它已包含在上面的解中。

方法2  $ y^{\prime}y^{m}-2(y^{n})^{2}=0\Rightarrow\frac{y^{\prime}y^{m}-2(y^{n})^{2}}{(y^{\prime})^{3}}=0 $ （当  $ y^{\prime}\neq0 $ 时），即

 $$ \left(\frac{y^{\prime \prime}}{\left(y^{\prime}\right)^{2}}\right)^{\prime}=0\Rightarrow\frac{y^{\prime \prime}}{\left(y^{\prime}\right)^{2}}=C\Rightarrow\left(\frac{1}{y^{\prime}}\right)^{\prime}=C_{1}\Rightarrow\frac{1}{y^{\prime}}=C_{1}x+C_{2}\Rightarrow y^{\prime}=\frac{1}{C_{1}x+C_{2}}. $$ 

积分得通解  $ y=\frac{1}{C_{1}}\ln\left|C_{1}x+C_{2}\right|+C_{3} $. 显然， $ y''=0 $ 的解  $ y=a_{1}x+a_{2} $ 也满足方程.

评注 方程变形时，可能会丢失某些解。只要求出的解中含有独立的任意常数的个数与方程的阶数相同，它就是通解。若题目是求通解，则无须考虑丢失的解。否则，还是应将丢失的解补上。

例5 设函数  $ y = f(x) $ 由参数方程  $ \begin{cases} x = 2t + t^2 \\ y = \psi(t) \end{cases} $ ( $ t > -1 $) 所确定，且  $ \frac{d^2 y}{dx^2} = \frac{1}{4(1 + t)} $，其中  $ \psi(t) $ 具有二阶导数，曲线  $ y = \psi(t) $ 与曲线  $ y + e^{-\frac{1}{2}y} = t $ 在  $ t = 1 $ 处相切，求函数  $ \psi(t) $.

分析 由参数方程求得 $ \frac{d^2y}{dx^2} $，代入等式 $ \frac{d^2y}{dx^2}=\frac{1}{4(1+t)} $可得到 $ \psi(t) $的二阶方程，其余条件即为方程的定解条件.

解 因为

 $$ \frac{\mathrm{d}y}{\mathrm{d}x}=\frac{\psi^{\prime}(t)}{2+2t}\;,\quad\frac{\mathrm{d}^{2}y}{\mathrm{d}x^{2}}=\frac{1}{2+2t}\cdot\frac{(2+2t)\psi^{\prime \prime}(t)-2\psi^{\prime}(t)}{\left(2+2t\right)^{2}}=\frac{(1+t)\psi^{\prime \prime}(t)-\psi^{\prime}(t)}{4\left(1+t\right)^{3}}\;, $$ 

由题设 $ \frac{d^{2}y}{dx^{2}}=\frac{1}{4(1+t)} $，故 $ \frac{(1+t)\psi''(t)-\psi'(t)}{4(1+t)^{3}}=\frac{1}{4(1+t)} $，从而得方程

 $$ (1+t)\psi^{\prime \prime}(t)-\psi^{\prime}(t)=(1+t)^{2}\ , 即 \psi^{\prime \prime}(t)-\frac{1}{1+t}\psi^{\prime}(t)=1+t. $$ 

这是不显含未知函数  $ \psi(t) $ 的方程. 设  $ p = \psi'(t) $，则方程化为

 $$ p^{\prime}-\frac{1}{1+t}p=1+t. $$ 

其通解为

 $$ p=\mathsf{e}^{\int\frac{1}{1+t}\mathsf{d}t}\Bigg[\int(1+t)\mathsf{e}^{-\int\frac{1}{1+t}\mathsf{d}t}\mathsf{d}t+C_{1}\Bigg]=(1+t)\bigg[\int(1+t)(1+t)^{-1}\mathsf{d}t+C_{1}\bigg]=(1+t)(t+C_{1})\:. $$ 

由于曲线  $ y + e^{-\frac{1}{2}y} = t $，当 t = 1 时，y = 0。且  $ y' - \frac{1}{2}e^{-\frac{1}{2}y} y' = 1 \Rightarrow y'\big|_{t=1} = 2 $。

由曲线  $ y=\psi(t) $ 与  $ y+e^{\frac{1}{2}y}=t $ 在 t=1 处相切知  $ \psi(1)=0 $， $ \psi'(1)=2 $。所以  $ p\big|_{t=1}=\psi'(1)=2 $，由①式知  $ C_{1}=0 $。于是  $ \psi'(t)=(1+t)t $。所以

 $$ \dot{\psi}(t)=\int(1+t)t\mathrm{d}t=\frac{1}{3}t^{3}+\frac{1}{2}t^{2}+C_{2}\;. $$ 

由 $ \psi(1)=0 $，知 $ C_{2}=-\frac{5}{6} $，故 $ \psi(t)=\frac{1}{3}t^{3}+\frac{1}{2}t^{2}-\frac{5}{6} $（t>-1）。

例 6 设函数  $ y(x) $ 满足方程  $ y(x)=x^{3}-x\int_{1}^{x}\frac{y(t)}{t^{2}}\mathrm{d}t+y'(x) $ (x>0)，并且  $ \lim_{x\to+\infty}\frac{y(x)}{x^{3}} $ 存在，求函数  $ y(x) $.

分析 积分方程，求导去掉积分号化为微分方程求解. 为达到去掉积分号的效果，求导前需对方程适当变形.

解 将所给方程改写为

 $$ \frac{y(x)}{x}=x^{2}-\int_{1}^{x}\frac{y(t)}{t^{2}}\mathrm{d}t+\frac{y^{\prime}(x)}{x}\left(x>0\right). $$ 

①式两边分别对x求导得

 $$ y^{\prime \prime}-\frac{x+1}{x}y^{\prime}=-2x^{2}\left(x>0\right)\left( 不显含 y\right). $$ 

令 $ p=y' $，则②式成为

 $$ p^{\prime}-\frac{x+1}{x}p=-2x^{2}\left(x>0\right), $$ 

它的通解为

 $$ p=\mathrm{e}^{\int\frac{x+1}{x}\mathrm{d}x}\left(C_{1}+\int-2x^{2}\mathrm{e}^{-\int\frac{x+1}{x}\mathrm{d}x}\mathrm{d}x\right)=C_{1}x\mathrm{e}^{x}+2x^{2}+2x. $$ 

得 $ ^{②} $式的通解为

 $$ y(x)=\int(C_{1}x\mathrm{e}^{x}+2x^{2}+2x)\mathrm{d}x=C_{1}(x-1)\mathrm{e}^{x}+\frac{2}{3}x^{3}+x^{2}+C_{2}. $$ 

由  $ \lim_{x\to+\infty}\frac{y(x)}{x^{3}}=\lim_{x\to+\infty}\frac{C_{1}(x-1)e^{x}+\frac{2}{3}x^{3}+x^{2}+C_{2}}{x^{3}} $ 存在，得  $ C_{1}=0 $ ，代入③式得

 $$ y(x)=\frac{2}{3}x^{3}+x^{2}+C_{2}. $$ 

此外，由①式知  $ y(1)=1+y'(1) $，即  $ \left(\frac{2}{3}x^{3}+x^{2}+C_{2}\right)\bigg|_{x=1}=1+\left(\frac{2}{3}x^{3}+x^{2}+C_{2}\right)^{\prime}\bigg|_{x=1} $，得  $ C_{2}=\frac{10}{3} $，因此所求的函数  $ y(x)=\frac{1}{3}(2x^{3}+3x^{2}+10) $。

例 $ 7^{*} $ 求方程 $ x^{2}yy=(y-xy')^{2} $的通解.

分析 这是关于未知函数 y 及其导数的二次齐次方程，作变量代换  $ y = e^{\int z \, dx} $，可将所求方程化为未知函数 z 的一阶方程.

解 设  $ y = e^{\int z \, dx} $，则  $ y' = z e^{\int z \, dx} $， $ y'' = (z' + z^2) e^{\int z \, dx} $，代入原方程，化简得

 $$ z^{\prime}+\frac{2}{x}z=\frac{1}{x^{2}}. $$ 

解其通解为 $ z=\frac{1}{x}+\frac{C_1}{x^2} $，原方程通解为 $ y=e^{\int\left(\frac{1}{x}+\frac{C_1}{x^2}\right)dx}=C_2xe^{-\frac{C_1}{x}} $

评注 若微分方程  $ F(x,y,y',\cdots,y^{(n)})=0 $ 中的函数 F 是关于未知函数 y 及其导数的齐次函数，即对  $ \forall t, \exists k $ 使  $ F(x,ty,ty',\cdots,ty^{(n)})=t^{k}F(x,y,y',\cdots,y^{(n)}) $，则称该方程为齐次微分方程。对齐次微分方程，令  $ y=e^{\int zdx} $，可达到降阶的效果。

例8 设当x>-1时，可微函数 $ f(x) $满足条件 $ f'(x)+f(x)-\frac{1}{x+1}\int_{0}^{x}f(t)dt=0 $，且 $ f(0)=1 $，证明当 $ x\geq0 $时，有 $ e^{-x}\leq f(x)\leq1 $成立.

分析 方程中含有未知函数的积分形式，需求导消去积分化为一个二阶微分方程. 求解微分方程，再对  $ f(x) $ 做放缩来得到所证结论.

解 将所给等式变形为  $ \left[f'(x) + f(x)\right](x + 1) = \int_{0}^{x} f(t) \, dt $. 两边对 x 求导得

 $$ \begin{align*}\left[f^{\prime\prime}(x)+f^{\prime}(x)\right](x+1)+\left[f^{\prime}(x)+f(x)\right]&=f(x)\ ,\ $ x+1)f^{\prime\prime}(x)+(x+2)f^{\prime}(x)&=0\;.\end{align*} $$ 

即有

这是一个可降阶的二阶微分方程（不显含  $ f(x) $），用分离变量法求得  $ f'(x)=\frac{C\mathrm{e}^{-x}}{x+1} $。由  $ f(0)=1 $ 代入原方程可得  $ f'(0)=-1 $，从而 C = -1，代入  $ f'(x) $，并在  $ [0,x] $ 上做积分得

 $$ f(x)-1=-\int_{0}^{x}\frac{\mathrm{e}^{-t}}{1+t}\mathrm{d}t. $$ 

由于  $ f'(x) = -\frac{e^{-x}}{1+x} < 0 $，所以  $ f(x) $ 单调递减。而  $ f(0) = 1 $，故当  $ x \geq 0 $ 时， $ f(x) \leq 1 $。

又由①式得  $ f(x)=1-\int_{0}^{x}\frac{e^{-t}}{1+t}dt \geqslant 1-\int_{0}^{x}e^{-t}dt=e^{-x} $. 所以当  $ x \geqslant 0 $ 时，有  $ e^{-x} \leqslant f(x) \leqslant 1 $.

# 2. 高阶线性微分方程

这里主要涉及线性微分方程解的结构以及二阶常系数与特殊变系数线性微分方程的求解.

（1）二阶常系数齐次线性微分方程求解（特征根法） $ y''+py'+qy=0 $

① 写出特征方程  $ r^{2} + pr + q = 0 $;

② 求特征方程的根  $ r_{1}, r_{2} $;

③ 根据特征根，由表7.1写出微分方程的通解.

<div style="text-align: center;"><div style="text-align: center;">表7.1</div> </div>




<table border=1 style='margin: auto; word-wrap: break-word;'><tr><td style='text-align: center; word-wrap: break-word;'>特征根</td><td style='text-align: center; word-wrap: break-word;'>通解</td></tr><tr><td style='text-align: center; word-wrap: break-word;'>$ r_1 \ne r_2 $ 为实根</td><td style='text-align: center; word-wrap: break-word;'>$ y = C_1e^{r_1x} + C_2e^{r_2x} $</td></tr><tr><td style='text-align: center; word-wrap: break-word;'>$ r_1 = r_2 $ 为重实根</td><td style='text-align: center; word-wrap: break-word;'>$ y = (C_1 + C_2x)e^{r_1x} $</td></tr><tr><td style='text-align: center; word-wrap: break-word;'>$ r_{1,2} = \alpha \pm i\beta $ 为共轭复根</td><td style='text-align: center; word-wrap: break-word;'>$ y = e^{\alpha x}(C_1 \cos \beta x + C_2 \sin \beta x) $</td></tr></table>

（2）二阶常系数非齐次线性微分方程求解  $ y'' + py' + qy = f(x) $

① 解的结构：

若 Y 是对应齐次方程的通解， $ y^{*} $ 是非齐次方程的一个特解，则非齐次方程的通解为  $ y = Y + y^{*} $

② 特解的确定（待定系数法）：

由自由项  $ f(x) $ 及特征根按表 7.2 确定特解形式，再代入微分方程确定特解形式中的待定系数.

<div style="text-align: center;"><div style="text-align: center;">表7.2</div> </div>




<table border=1 style='margin: auto; word-wrap: break-word;'><tr><td style='text-align: center; word-wrap: break-word;'>$ f(x) $ 的类型</td><td style='text-align: center; word-wrap: break-word;'>特征根</td><td style='text-align: center; word-wrap: break-word;'>特解形式</td></tr><tr><td style='text-align: center; word-wrap: break-word;'>$ e^{\lambda x}P_{m}(x) $\n $ (P_{m}(x) $为m次多项式 $</td><td style='text-align: center; word-wrap: break-word;'>$ \lambda $ 是 k 重特征根  $ (k=0,1,2) $</td><td style='text-align: center; word-wrap: break-word;'>$ y^{*}=x^{k}e^{\lambda x}Q_{m}(x) $\n $ (Q_{m}(x) $为m次系数待定多项式 $</td></tr><tr><td style='text-align: center; word-wrap: break-word;'>$ e^{\lambda x}[P_{l}(x)\cos\omega x+P_{n}(x)\sin\omega x] $\n $ (P_{l}(x),P_{n}(x) $分别为l,n次多项式 $</td><td style='text-align: center; word-wrap: break-word;'>$ \lambda \pm i\omega $ 是 k 重特征根\n $ (k=0,1,2) $</td><td style='text-align: center; word-wrap: break-word;'>$ y^{*}=x^{k}e^{\lambda x}[R_{m}^{(1)}(x)\cos\omega x+R_{m}^{(2)}(x)\sin\omega x] $\n $ (R_{m}^{(1)}(x),R_{m}^{(2)}(x) $为m次系数待定多项式)\n $ m=\max\{l,n\} $</td></tr></table>

（3）欧拉方程求解 $ x^{2}y''+pxy'+qy=f(x) $

作变量代换  $ x = e^{t} $ 或  $ t = \ln x $，方程化为二阶常系数线性微分方程

 $$ D(D-1)y+p D y+q y=f(\mathfrak{e}^{\prime})\quad( 其中 \quad D=\frac{\mathtt{d}}{\mathtt{d}t})。 $$ 

例9 求  $ y'' + 2ay' + a^2y = e^{bx} $ 的通解，a > 0，a，b 为常数.

分析 常系数非齐次线性微分方程的解法是：由特征方程法写出对应齐次方程的通解，由待定系数法确定非齐次方程的特解，再由非齐次方程解的结构写出其通解.

解　对应齐次方程的特征方程为 $ r^{2}+2ar+a^{2}=0 $，特征根为二重根 $ r_{1,2}=-a $，齐次方程通解为

 $$ Y=(C_{1}+C_{2}x)\mathrm{e}^{-\alpha x} $$ 

①当  $ b \neq -a $ 时，  $ \lambda = b $ 不是特征根，设非齐次方程的特解为  $ y^* = A e^{bx} $，代入方程得  $ A = \frac{1}{b^2 + 2ab + a^2} $，所以原非齐次方程的通解为

 $$ y=(C_{1}+C_{2}x)\mathrm{e}^{-ax}+\frac{1}{b^{2}+2ab+a^{2}}\mathrm{e}^{bx}. $$ 

② 当 $b = -a$ 时，$\lambda = b$ 是二重特征根，设非齐次方程的特解为 $y^* = B x^2 e^{bx}$，代入方程得 $B = \frac{1}{2}$，所以原非齐次方程的通解为

 $$ y=(C_{1}+C_{2}x)\mathrm{e}^{-ax}+\frac{1}{2}x^{2}\mathrm{e}^{-ax}. $$ 

评注 当方程中含有字母常数时，需留意它对特征根的影响，从而会影响到齐次方程的通解与非齐次方程的特解.

例 10 解方程  $ y''-3y'+2y=2e^{-x}\cos x+e^{2x}(4x+5) $.

分析 方程右端的自由项是两个不同类型的函数之和，要利用解的叠加原理分别求特解，两特解之和就是原方程的特解.

解 特征方程为  $ r^{2}-3r+2=0 $，两个特征根分别为  $ r_{1}=2 $， $ r_{2}=1 $。对应的齐次方程通解为  $ Y=C_{1}e^{x}+C_{2}e^{2x} $。

为求非齐次方程的一个特解，将原方程分解成两个方程

 $$ y^{\prime \prime}-3y^{\prime}+2y=2\mathrm{e}^{-x}\cos x, $$ 

对方程①， $ \lambda + i\omega = -1 + i $ 不是特征根，设方程的特解为  $ y_1 = e^{-x}(A\cos x + B\sin x) $，代入原方程可以求得  $ A = \frac{1}{5} $， $ B = -\frac{1}{5} $，即  $ y_1 = \frac{1}{5}e^{-x}(\cos x - \sin x) $。

对方程②， $ \lambda=2 $ 是单特征根，设方程的特解为  $ y_2=e^{2x}x(ax+b) $，代入原方程可以求得  $ a=2 $， $ b=1 $，即  $ y_2=e^{2x}(2x^2+x) $。

则  $ y_{1}+y_{2} $ 是原方程的一个特解，得原方程的通解为

 $$ y=C_{1}\mathbf{e}^{x}+C_{2}\mathbf{e}^{2x}+\frac{1}{5}\mathbf{e}^{-x}(\cos x-\sin x)+\mathbf{e}^{2x}(2x^{2}+x). $$ 

评注 非齐次线性微分方程解的叠加原理：

设  $ y_{1} $ 与  $ y_{2} $ 分别为方程  $ y'' + P(x)y' + Q(x)y = f_{1}(x) $ 与  $ y'' + P(x)y' + Q(x)y = f_{2}(x) $ 的解，则  $ y_{1} + y_{2} $ 就是方程  $ y'' + P(x)y' + Q(x)y = f_{1}(x) + f_{2}(x) $ 的解.

例11 求  $ y'' + 2y' - 3y = f(x) $ 满足  $ y(0) = 0 $,  $ y'(0) = 1 $ 的特解，其中  $ f(x) = \left\{ \begin{aligned} & x + 1, & x \geq 0 \\ & e^{x}, & x < 0 \end{aligned} \right. $

分析 由于自由项  $ f(x) $ 是一个分段函数，所以求解方程时要分段进行.

解 易求得方程的通解为

 $$ y=\left\{\begin{aligned}{}&{{}C_{1}\mathsf{e}^{-3x}+C_{2}\mathsf{e}^{x}-\frac{1}{3}x-\frac{5}{9},~x\geqslant0,}\\ {}&{{}C_{3}\mathsf{e}^{-3x}+C_{4}\mathsf{e}^{x}+\frac{1}{4}x\mathsf{e}^{x},\quad x<0.}\\ \end{aligned}\right. $$ 

在x=0处y连续可微，且满足初值条件，则有 $ \begin{cases}y(+0)=y(-0)=0\\y_{-}^{\prime}(0)=y_{+}^{\prime}(0)=1\end{cases} $。即

 $$ \left\{\begin{aligned}{}&{{}C_{1}+C_{2}-\frac{5}{9}=C_{3}+C_{4}=0,}\\ {}&{{}-3C_{1}+C_{2}-\frac{1}{3}=-3C_{3}+C_{4}+\frac{1}{4}=1.}\\ \end{aligned}\right. $$ 

解出  $ C_{1}=-\frac{7}{36} $， $ C_{2}=\frac{3}{4} $， $ C_{3}=-\frac{3}{16} $， $ C_{4}=\frac{3}{16} $，所以所求特解为

 $$ y=\left\{\begin{aligned}{}&{{}-\frac{7}{36}\mathrm{e}^{-3x}+\frac{3}{4}\mathrm{e}^{x}-\frac{1}{3}x-\frac{5}{9},~x\geqslant0,}\\ {}&{{}-\frac{3}{16}\mathrm{e}^{-3x}+\frac{3}{16}\mathrm{e}^{x}+\frac{1}{4}x\mathrm{e}^{x},\quad x<0.}\\ \end{aligned}\right. $$ 

评注 由于自由项函数在分段点两侧的表达式不同，对应的方程也就不同，所以对应齐次方程通解中的常数要用不同的字母表示，同时未知函数在分段点连续、可导，这些常数又存在一定的联系，在确定特解时要充分利用这些信息.

例12 设 $ f(x) $在 $ (-∞,+∞) $二阶可导，且对任意x,y有 $ f^{2}(x)-f^{2}(y)=f(x+y)f(x-y) $，求 $ f(x) $.

分析 要建立微分方程，在方程两边需对 x 或 y 求偏导. 若求一阶导数不能化简方程，则可求二阶.

解 取 x=y=0，可得  $ f(0)=0 $，方程两边对 x 求偏导得

 $$ 2f(x)f^{\prime}(x)=f^{\prime}(x+y)f(x-y)+f(x+y)f^{\prime}(x-y)\;. $$ 

上式两边对 y 求偏导得

 $$ 0=f^{\prime\prime}(x+y)f(x-y)-f(x+y)f^{\prime\prime}(x-y)~, $$ 

令  $ u = x + y $, v = x - y, 得

 $$ f^{\prime\prime}(u)f(v)=f(u)f^{\prime\prime}(v)\Rightarrow\frac{f^{\prime\prime}(u)}{f(u)}=\frac{f^{\prime\prime}(v)}{f(v)}. $$ 

这说明 $ \frac{f''(u)}{f(u)} $与变量取值无关，即 $ \frac{f''(u)}{f(u)}=C $（C为常数），有

 $$ f^{\prime\prime}(u)-C f(u)=0. $$ 

解得

 $$ f(u)=\left\{\begin{aligned}{}&{{}C_{1}\mathsf{e}^{\sqrt{C}u}+C_{2}\mathsf{e}^{-\sqrt{C}u},}&{}&{{}C>0,}\\ {}&{{}C_{1}u+C_{2},}&{}&{{}C=0,}\\ {}&{{}C_{2}\operatorname{c o s}\sqrt{-C}u+C_{1}\operatorname{s i n}\sqrt{-C}u,}&{}&{{}C<0.}\\ \end{aligned}\right. $$ 

由于  $ f(x) $ 连续，并注意到  $ f(0)=0 $ ，可得到：当 C>0 时， $ C_{1}=-C_{2} $ ；当 C=0 时， $ C_{2}=0 $ ；当 C<0 时， $ C_{2}=0 $ 。所以

 $$ f(u)=\left\{\begin{aligned}&C_{1}(\mathrm{e}^{\sqrt{C}x}-\mathrm{e}^{-\sqrt{C}x}),&&C>0,\\ &C_{1}x,&&C=0,\\ &C_{1}\sin\sqrt{-C}u,&&C<0.\end{aligned}\right.\quad( 其中 \;C_{1}\; 为任意常数 ) $$ 

评注 原方程中有两个自变量x, y，求解中一定要将其转化成一个自变量的情形，才便于利用微分方程求解.

例 13 已知  $ y_1 = x e^x + e^{2x} $， $ y_2 = x e^x - e^{-x} $， $ y_3 = x e^x + e^{2x} - e^{-x} $ 都是某二阶非齐次线性微分方程的解，求此微分方程.

分析 由题设条件容易得到对应齐次方程的两个线性无关的解，从而可写出对应齐次线性微分方程。再由非齐次线性微分方程的一个特解就可确定自由项；也可根据非齐次线性微分方程解的结构写出通解，再消去通解中的任意常数得到微分方程。

解 方法1 因为  $ y_{1}, y_{2}, y_{3} $ 是非齐次线性微分方程的解，则  $ y_{3} - y_{1} = -e^{-x} $ 及  $ y_{3} - y_{2} = e^{2x} $ 是对应齐次方程的解，则 r = -1, r = 2 是齐次方程的特征根，特征方程为

 $$ (r+1)(r-2)=0,\  即 r^{2}-r-2=0. $$ 

得所求的非齐次线性微分方程方程为

 $$ y^{\prime \prime}-y^{\prime}-2y=f(x)\;. $$ 

由非齐次线性微分方程解的结构易知， $ x e^{x} $ 也是非齐次线性微分方程的一个特解，代入方程得

 $$ f(x)=(x\mathrm{e}^{x})^{n}-(x\mathrm{e}^{x})^{\prime}-2x\mathrm{e}^{x}=\mathrm{e}^{x}-2x\mathrm{e}^{x}. $$ 

因此所求方程为  $ y'' - y' - 2y = e^x - 2x e^x $。

方法2 根据非齐次线性微分方程解的结构可得到其通解为

 $$ y=C_{1}\mathbf{e}^{-x}+C_{2}\mathbf{e}^{2x}+x\mathbf{e}^{x}. $$ 

求导得

 $$ y^{\prime}=-C_{1}\mathrm{e}^{-x}+2C_{2}\mathrm{e}^{2x}+(x+1)\mathrm{e}^{x}, $$ 

 $$ y^{\prime \prime}=C_{1}\mathbf{e}^{-x}+4C_{2}\mathbf{e}^{2x}+(x+2)\mathbf{e}^{x}. $$ 

从上面3式中消去 $ C_{1} $和 $ C_{2} $即可得到所求的微分方程.

评注 如果已知微分方程的通解，求方程的常用方法是：对通解求导数（求导阶数与通解中任意常数的个数相同），消去任意常数就可得到对应的微分方程；如果所求微分方程是线性的，也可根据解的结构来确定方程中的待定系数或待定函数.

例  $ 14^{*} $ 解微分方程组  $ \frac{dx}{dx}=x+y-3 $， $ \frac{dy}{dx}=-2x+3y+1 $，当 t=0 时，满足条件 x=y=0。

分析 对所给线性微分方程组消元，化为一个未知函数的二阶线性微分方程求解.

解 由第1个方程解出y得

 $$ y=\frac{\mathrm{d}x}{\mathrm{d}t}-x+3\ , $$ 

两边求导得

 $$ \frac{\mathrm{d}y}{\mathrm{d}t}=\frac{\mathrm{d}^{2}x}{\mathrm{d}t^{2}}-\frac{\mathrm{d}x}{\mathrm{d}t}. $$ 

将①，②式代入原来的第2个方程中消去y得

 $$ \frac{\mathrm{d}^{2}x}{\mathrm{d}t^{2}}-\frac{\mathrm{d}x}{\mathrm{d}t}=-2x+3\left(\frac{\mathrm{d}x}{\mathrm{d}t}-x+3\right), $$ 

 $$ \frac{\mathrm{d}^{2}x}{\mathrm{d}t^{2}}-4\frac{\mathrm{d}x}{\mathrm{d}t}+5x=10\;. $$ 

即

由条件  $ x(0)=y(0)=0 $ 得  $ \left.\frac{dx}{dt}\right|_{t=0}=-3 $，方程③满足该初值的解为

 $$ x=\mathrm{e}^{2t}\left(-2\cos t+\sin t\right)+2. $$ 

由 $ ^{①} $式得

 $$ y=\mathrm{e}^{2t}(-\cos t+3\sin t)+1. $$ 

容易验证 $ ^{④} $， $ ^{⑤} $两式中的函数为已知方程组的解.

评注 常系数线性微分方程组的求解方法之一是消元转化为高阶常系数线性微分方程求解.

例 $15^{*}$ 求微分方程 $y'' + y = \frac{1}{\cos x}$ 的通解.

分析 这是二阶常系数非齐次线性微分方程，但自由项不属于用待定系数法的类型。由于对应齐次微分方程的通解易于求得，因此用常数变异法去求非齐次方程的特解。

解 易知对应齐次方程的通解为

 $$ y(x)=C_{1}\cos x+C_{2}\sin x. $$ 

用常数变易法求非齐次微分方程的特解：

设非齐次方程的解为  $ y(x)=C_{1}(x)\cos x+C_{2}(x)\sin x $，则

 $$ y^{\prime}=C_{1}^{\prime}(x)\cos x+C_{2}^{\prime}(x)\sin x-C_{1}(x)\sin x+C_{2}(x)\cos x, $$ 

令

 $$ C_{1}^{\prime}(x)\cos x+C_{2}^{\prime}(x)\sin x=0 $$ 

将③式代入②式再求导得

 $$ y^{\prime \prime}=-C_{1}^{\prime}(x)\sin x+C_{2}^{\prime}(x)\cos x-C_{1}(x)\cos x-C_{2}(x)\sin x, $$ 

将 $ ^{①} $， $ ^{④} $两式代入原方程得

 $$ -C_{1}^{\prime}(x)\sin x+C_{2}^{\prime}(x)\cos x=\frac{1}{\cos x}. $$ 

方程组③，⑤联立求解得  $ C_{1}^{\prime}(x) = -\frac{\sin x}{\cos x} $， $ C_{2}^{\prime}(x) = 1 $，积分得

 $$ C_{1}(x)=\ln|\cos x|+C_{1},\quad C_{2}(x)=x+C_{2}. $$ 

所以，原方程的通解为

 $$ y(x)=C_{1}\cos x+C_{2}\sin x+\cos x\ln|\cos x|+x\sin x. $$ 

评注 常数变易法求解二阶线性方程  $ y'' + py' + qy = f(x) $ 的步骤为：

（1）求对应齐次方程的通解  $ y(x)=C_{1}y_{1}(x)+C_{2}y_{2}(x) $;

(2) 变换常数，令  $ y(x)=C_{1}(x)y_{1}(x)+C_{2}(x)y_{2}(x) $ 是非齐次方程的解，计算

 $$ y^{\prime}(x)=C_{1}^{\prime}(x)y_{1}(x)+C_{2}^{\prime}(x)y_{2}(x)+C_{1}(x)y_{1}^{\prime}(x)+C_{2}(x)y_{2}^{\prime}(x) $$ 

并设 $ C_{1}^{\prime}(x)y_{1}(x)+C_{2}^{\prime}(x)y_{2}(x)=0 $，再求 $ y^{\prime\prime}(x) $。将 $ y(x) $， $ y^{\prime}(x) $， $ y^{\prime\prime}(x) $代入原非齐次方程得

 $$ C_{1}^{\prime}(x)y_{1}^{\prime}(x)+C_{2}^{\prime}(x)y_{2}^{\prime}(x)=f(x)\;; $$ 

（3）解方程组  $ \left\{\begin{array}{l}C_{1}^{\prime}(x)y_{1}(x)+C_{2}^{\prime}(x)y_{2}(x)=0\\C_{1}^{\prime}(x)y_{1}^{\prime}(x)+C_{2}^{\prime}(x)y_{2}^{\prime}(x)=f(x)\end{array}\right. $，得  $ C_{1}^{\prime}(x) $， $ C_{2}^{\prime}(x) $，积分后代入（2）中所设就得到非齐次方程的通解.

例16 设  $ f(x) $ 具有二阶导数，且  $ f(x) + f'(\pi - x) = \sin x $， $ f\left(\frac{\pi}{2}\right) = 0 $。求  $ f(x) $。

分析 方程中含  $ f(x) $ 与  $ f'(\pi - x) $，其中变元分别为 x 与  $ \pi - x $，没法求解。为使方程中只保留一种变元形式，可对方程两边求导得到新的方程，再联立消元、求解。

解 由  $ f(x) + f'(\pi - x) = \sin x $，两边对 x 求导，有

 $$ f^{\prime}(x)-f^{\prime \prime}(\pi-x)=\cos x. $$ 

第2个方程中令 $ x=\pi-u $，并将u仍写为x，得

 $$ f^{\prime}(\pi-x)-f^{\prime \prime}(x)=-\cos x, $$ 

代入第1个方程，得

 $$ f(x)+f^{\prime}(x)=\sin x+\cos x. $$ 

求得通解

 $$ f(x)=C_{1}\cos x+C_{2}\sin x+x\left(-\frac{1}{2}\cos x+\frac{1}{2}\sin x\right). $$ 

初值条件  $ f\left(\frac{\pi}{2}\right)=0 $．又由  $ f(x)+f'(\pi-x)=\sin x $ 得  $ f'\left(\frac{\pi}{2}\right)=1 $．求得特解

 $$ f(x)=\left(\frac{\pi}{4}-\frac{1}{2}-\frac{x}{2}\right)\cos x+\left(-\frac{\pi}{4}+\frac{x}{2}\right)\sin x. $$ 

评注 未知函数与其导数中的自变量不在同一个x处的微分方程又叫“差分—微分方程”。该类方程的求解通常是采用“求导消元法”，将它化为同一变量形式的微分方程来处理。

例 17 设二阶常系数非齐次线性方程为  $ y'' + py' + qy = f(x) $，其中 p, q 为常数。其对应的齐次方程的特征根分别为  $ r_1, r_2 $。证明该方程的通解为

 $$ y=\mathsf{e}^{r_{1}x}\left(\int\mathsf{e}^{-r_{1}x}\left(\mathsf{e}^{r_{2}x}\int\mathsf{e}^{-r_{2}x}f(x)\mathsf{d}x+C_{1}\right)\mathsf{d}x+C_{2}\right). $$ 

分析 由特征根可确定方程中的系数 p 与 q. 为得到积分形式的解，需要作变量代换将二阶微分方程降为一阶方程，再积分求解.

证明 因  $ r_{1}+r_{2}=-p $， $ r_{1}\cdot r_{2}=q $，所以原方程可化为

 $$ (y^{\prime}-r_{1}y)^{\prime}-r_{2}(y^{\prime}-r_{1}y)=f(x). $$ 

令 $ u=y'-ry $，则方程变为一阶线性方程

 $$ u^{\prime}-r_{2}u=f(x). $$ 

通解为

 $$ u=\mathrm{e}^{r_{2}x}\left(\int\mathrm{e}^{-r_{2}x}f(x)\mathrm{d}x+C_{1}\right), $$ 

即

 $$ y^{\prime}-r_{1}y=\mathrm{e}^{r_{2}x}\left(\int\mathrm{e}^{-r_{2}x}f(x)\mathrm{d}x+C_{1}\right). $$ 

再解此一阶线性方程得

 $$ y=\mathrm{e}^{r_{1}x}\left(\int\mathrm{e}^{-r_{1}x}\left(\mathrm{e}^{r_{2}x}\int\mathrm{e}^{-r_{2}x}f(x)\mathrm{d}x+C_{1}\right)\mathrm{d}x+C_{2}\right). $$ 

例  $ 18^{\circ} $ 设  $ h_{1}(x) $ 与  $ h_{2}(x) $ 当  $ x \geqslant x_{0} $ 时连续，且  $ h_{1}(x) \geqslant h_{2}(x) $，若函数  $ f(x) $ 与  $ g(x) $ 分别是下列微分方程①与②满足初值条件  $ y(x_{0}) = c_{1} $， $ y'(x_{0}) = c $，的解（其中  $ p^{2} - 4q \geqslant 0 $）.

 $$ y^{\prime \prime}+py^{\prime}+qy=h_{1}(x), $$ 

 $$ y^{\prime \prime}+p y^{\prime}+q y=h_{2}(x). $$ 

证明当 $ x \geqslant x_{0} $时，有 $ f(x) \geqslant g(x) $.

分析 我们已经知道一阶线性微分方程的比较定理（7.1 节例 20），故只需作变量代换将二阶线性方程转化为一阶线性方程来处理.

证明 因为  $ p^{2}-4q\geqslant0 $，所以对应齐次方程的特征根为实数，设为 a,b，则有  $ p=-(a+b) $，q=ab。从而

 $$ y^{\prime \prime}+p y^{\prime}+q y=(y^{\prime}-a y)^{\prime}-b(y^{\prime}-a y), $$ 

记 $ z=y'-ay $，则方程①，②可分别写成

 $$ z^{\prime}-b z=h_{1}(x), $$ 

 $$ z^{\prime}-b z=h_{2}(x)\;. $$ 

由已知条件知， $ f'(x)-af(x) $ 与  $ g'(x)-ag(x) $ 分别是方程③与④满足初值条件  $ z(x_0)=c_2-ac_1 $ 的

解，根据一阶微分方程的比较定理（7.1 节例 20（1）），有

 $$ f^{\prime}(x)-af(x)\leq g^{\prime}(x)-ag(x) $$ 

令 $ v(x)=g(x)-f(x) $，则有

 $$ \nu^{\prime}(x)-a\nu(x)\geq0, 且 \nu(x_{0})=0. $$ 

显然  $ u(x)=0 $ 是方程  $ u'(x)-au(x)=0 $ 满足初值  $ u(x_0)=0 $ 的解，再次利用一阶微分方程的比较定理得，当  $ x \geq x_0 $ 时，有  $ v(x) \geq u(x)=0 $，即  $ f(x) \geq g(x) $。

评注 本题结论又叫二阶线性微分方程的比较定理，利用该定理我们可以得到许多具体的函数不等式，如2.3节例16，习题2.3第11题等.

例19 求  $ y'' - \frac{3}{x-1} y' - \frac{5}{(x-1)^2} y = 3 $ 的通解.

分析 方程两边同时乘以 $ (x-1)^2 $，是欧拉方程。将 $ x-1=e^t $转化为常系数非齐次线性方程。

解 方程为  $ (x-1)^{2}y''-3(x-1)y'-5y=3(x-1)^{2} $，这是一个欧拉方程.

令  $ x-1=e^{t} $，或  $ t=\ln(x-1) $，记  $ D=\frac{d}{dt} $，方程化为

 $$ D(D-1)y-3D y-5y=3\mathrm{e}^{2t}\Rightarrow D^{2}y-4D y-5y=3\mathrm{e}^{2t}. $$ 

方程的通解为

 $$ y=C_{1}\mathsf{e}^{5t}+C_{2}\mathsf{e}^{-t}-\frac{1}{3}\mathsf{e}^{2t}=C_{1}(x-1)^{5}+C_{2}\frac{1}{x-1}-\frac{1}{3}(x-1)^{2}. $$ 

例  $ 20^{*} $ 设  $ f(x,y) $ 有二阶连续偏导数， $ u(r)=\int_{0}^{\angle\pi}f(r\cos\theta,r\sin\theta)\mathrm{d}\theta $，若  $ f_{11}+f_{22}=\frac{1}{r} $，求函数  $ u(r) $.

分析 只需对函数  $ u(r) $ 求导（一至二阶），将方程  $ f_{11}+f_{22}=\frac{1}{r} $ 转化为  $ u(r) $ 的常微分方程求解.

解 因为  $ f(x,y) $ 有二阶连续偏导数，则

 $$ \frac{\mathrm{d}u}{\mathrm{d}r}=\int_{0}^{2\pi}\frac{\partial}{\partial r}f(r\mathrm{c o s}\theta,\dot{r}\mathrm{s i n}\theta)\mathrm{d}\theta=\int_{0}^{2\pi}(f_{1}\cdot\mathrm{c o s}\theta+f_{2}\cdot\mathrm{s i n}\theta)\mathrm{d}\theta, $$ 

 $$ \frac{\mathrm{d}^{2}u}{\mathrm{d}r^{2}}=\int_{0}^{2\pi}\frac{\partial^{2}}{\partial r^{2}}f(r\mathrm{c o s}\theta,r\mathrm{s i n}\theta)\mathrm{d}\theta=\int_{0}^{2\pi}(f_{11}\cdot\mathrm{c o s}^{2}\theta+2f_{12}\cdot\mathrm{s i n}\theta\mathrm{c o s}\theta+f_{22}\cdot\mathrm{s i n}^{2}\theta)\mathrm{d}\theta. $$ 

又

 $$ \begin{aligned}\frac{\mathrm{d}u}{\mathrm{d}r}=&\int_{0}^{2\pi}f_{1}\mathrm{d}\sin\theta-\int_{0}^{2\pi}f_{2}\mathrm{d}\cos\theta\\=&\left.f_{1}\cdot\sin\theta\right|_{0}^{2\pi}-\int_{0}^{2\pi}[f_{11}(-r\sin\theta)+f_{12}\cdot r\cos\theta]\sin\theta\mathrm{d}\theta-\\&\left.f_{2}\cdot\cos\theta\right|_{0}^{2\pi}+\int_{0}^{2\pi}[f_{21}(-r\sin\theta)+f_{22}\cdot r\cos\theta]\cos\theta\mathrm{d}\theta\\=&\int_{0}^{2\pi}r[f_{11}\cdot\sin^{2}\theta-2f_{12}\cdot\sin\theta\cos\theta+f_{22}\cdot\cos^{2}\theta]\mathrm{d}\theta.\end{aligned} $$ 

由 $ ^{①} $， $ ^{②} $两式可得

 $$ \begin{aligned}&r\frac{\mathrm{d}^{2}u}{\mathrm{d}r^{2}}+\frac{\mathrm{d}u}{\mathrm{d}r}=r\int_{0}^{2\pi}(f_{11}+f_{22})\mathrm{d}\theta=\int_{0}^{2\pi}\mathrm{d}\theta=2\pi\ ,\\ &\\ &\quad r^{2}\frac{\mathrm{d}^{2}u}{\mathrm{d}r^{2}}+r\frac{\mathrm{d}u}{\mathrm{d}r}=2\pi r\quad( 欧拉方程 )\ .\\ \end{aligned} $$ 

即

令  $ r=e^{t} $，记  $ D=\frac{d}{dt} $，则原方程化为

 $$ D(D-1)u+D u=2\pi\mathbf{e}^{t},\quad 即 \quad D^{2}u=2\pi\mathbf{e}^{t}. $$ 

方程通解为

 $$ u=2\pi\mathbf{e}^{t}+C_{1}t+C_{2}=2\pi r+C_{1}\ln r+C_{2}. $$ 

例  $ 21^{*} $ 求微分方程  $ (x^{2}\ln x)y'' - xy' + y = 0 $ 的通解.

分析 该方程形式类似于欧拉方程，可作变量代换  $ x = e^{t} $ 尝试.

解 令  $ x = e^{t} $，则

 $$ x y^{\prime}\ x y^{\prime}=D y,\ x^{2}y^{\prime\prime}=D(D-1)y\left(D=\frac{\mathrm{d}}{\mathrm{d}t}\right), $$ 

方程化为

 $$ t D(D{-}1)y-D y+y=0\Rightarrow(t D{-}1)(D{-}1)y=0\:. $$ 

令 $ u=(D-1)y $，方程为

 $$ t\frac{\mathrm{d}u}{\mathrm{d}t}-u=0~. $$ 

其通解为 $ u=C_{1}t $，即

 $$ \frac{\mathrm{d}y}{\mathrm{d}t}-y=C_{1}t\;. $$ 

该方程的通解为

 $$ y=\mathbf{e}^{-\int-\mathtt{d}t}\left(\int C_{1}t\mathbf{e}^{\int-\mathtt{d}t}\mathrm{d}t+C_{2}\right)=\mathbf{e}^{t}\left(C_{1}\int t\mathbf{e}^{-t}\mathrm{d}t+C_{2}\right)=C_{2}\mathbf{e}^{t}-C_{1}(t+1). $$ 

将  $ x=e^{t} $ 代入，得所给微分方程的通解

 $$ y=C_{2}x-C_{1}(\ln x+1). $$ 

例  $ 22^{*} $ 求方程  $ (\cos x - \sin x)y'' + 2\cos x \cdot y' + (\cos x + \sin x)y = 0 $ 的通解.

分析 这是二阶线性齐次方程，只需求得两个线性无关的的特解就可得到通解. 由方程的系数  $ (\cos x - \sin x) - 2\cos x + (\cos x + \sin x) = 0 $，知  $ y = e^{-x} $ 是方程的一个解，方程的另一个解可通过常数变异法求得.

解 易验证  $ y = e^{-x} $ 是所给方程的一个解. 设  $ y = ue^{-x} $ 是方程的另一个解, 则

 $$ y^{\prime}=u^{\prime}\mathrm{e}^{-x}-u\mathrm{e}^{-x},\quad y^{\prime \prime}=u^{\prime \prime}\mathrm{e}^{-x}-2u^{\prime}\mathrm{e}^{-x}+u\mathrm{e}^{-x}, $$ 

代入方程得

 $$ \begin{aligned}(\cos x-\sin x)u^{\prime \prime}+2\sin x\cdot u^{\prime}&=0\Rightarrow\frac{u^{\prime \prime}}{u^{\prime}}=\frac{2\sin x}{\sin x-\cos x}\\\Rightarrow\ln u^{\prime}=\int\frac{2\sin x}{\sin x-\cos x}\mathrm{d}x&=\int\frac{(\sin x-\cos x)+(\sin x+\cos x)}{\sin x-\cos x}\mathrm{d}x\\&=x+\ln(\sin x-\cos x)+C.\end{aligned} $$ 

由于只需求u的一个特解，因此取C=0，得

 $$ u^{\prime}=\mathrm{e}^{x}(\sin x-\cos x)\Longrightarrow u=-\mathrm{e}^{x}\cos x\;. $$ 

所以方程的另一个特解为  $ y = ue^{-x} = \cos x $。所求方程的通解为

 $$ y=C_{1}\mathrm{e}^{-x}+C_{2}\cos x. $$ 

评注 若线性齐次方程  $ a(x)y'' + b(x)y' + c(x)y = 0 $ 的系数满足  $ a(x) + b(x) + c(x) = 0 $，则  $ y = e^x $ 是方程的一个解；若系数满足  $ a(x) - b(x) + c(x) = 0 $，则  $ y = e^{-x} $ 是方程的一个解.

例  $ 23^{*} $ 设微分方程  $ y'' - \frac{1}{x} y' + q(x) y = 0 $ 的两个特解  $ y_{1}(x) $,  $ y_{2}(x) $ 满足  $ y_{1} y_{2} = 1 $，求该方程的通解.

分析 这是二阶齐次线性微分方程. 要求方程的通解，首先要确定方程中的未知函数  $ q(x) $，再分别求得方程的两个线性无关的特解即可. 显然  $ q(x) $ 可由方程的任意一个非零解唯一确定.

解 因为  $ y_{1}y_{2}=1 $，若  $ y_{1},y_{2} $ 中有一个为常函数，则另一个也必为常函数，且均非 0。设  $ y_{1}=a\neq0 $，代入微分方程，可得  $ q(x)=0 $，此时微分方程为

 $$ y^{\prime \prime}-\frac{1}{x}y^{\prime}=0. $$ 

显然  $ y=x^{2} $ 是该方程的一个解，且与  $ y_{1}=a $ 线性无关. 此时所给方程的通解为

 $$ y=C_{1}+C_{2}x^{2}\quad(C_{1},C_{2} 为任意常数 ) $$ 

若  $ y_{1}, y_{2} $ 中有一个不是常函数，则另一个也不会是常函数，且  $ y_{1}, y_{2} = \frac{1}{y_{1}} $ 线性无关. 此时微分方程的通解为  $ y = C_{1} y_{1} + C_{2} \frac{1}{y_{1}} $. 下面计算  $ y_{1} $.

将 $ y_{1} $与 $ \frac{1}{y_{1}} $代入微分方程，得

 $$ y_{1}^{n}-\frac{1}{x}y_{1}^{\prime}+q(x)y_{1}=0, $$ 

 $$ \left(\frac{1}{y_{1}}\right)^{\prime\prime}-\frac{1}{x}\left(\frac{1}{y_{1}}\right)^{\prime}+q(x)\frac{1}{y_{1}}=0\;. $$ 

②式即为

 $$ -\frac{y_{1}^{^{\prime \prime}}y_{1}-2(y_{1}^{^{\prime}})^{2}}{y_{1}^{3}}+\frac{y_{1}^{^{\prime}}}{x y_{1}^{2}}+q(x)\frac{1}{y_{1}}=0. $$ 

由①式得  $ y_{1}^{\prime\prime}=\frac{1}{x}y_{1}^{\prime}-q(x)y_{1} $，代入③式化简，得

 $$ \frac{2(y_{1}^{^{\prime}})^{2}}{y_{1}^{3}}+2q(x)\frac{1}{y_{1}}=0\Rightarrow q(x)=-\frac{(y_{1}^{^{\prime}})^{2}}{y_{1}^{2}}, $$ 

则 $ ^{①} $式为

 $$ y_{1}^{\prime \prime}-\frac{1}{x}y_{1}^{\prime}-\frac{(y_{1}^{\prime})^{2}}{y_{1}^{2}}y_{1}=0\ , 即 \frac{y_{1}^{\prime \prime}}{y_{1}}-\left(\frac{y_{1}^{\prime}}{y_{1}}\right)^{2}-\frac{1}{x}\frac{y_{1}^{\prime}}{y_{1}}=0\ . $$ 

令  $ z = \frac{y_{1}^{\prime}}{y_{1}} $，④式为

 $$ \frac{\mathrm{d}z}{\mathrm{d}x}-\frac{1}{x}\cdot z=0, $$ 

该方程的一个特解为  $ z = 2x $，由此得到  $ y_1 = C \mathbf{e}^{x^2} $（可取  $ C = 1 $），则  $ y_2 = \mathbf{e}^{-x^2} $。从而原微分方程的通解为  $ y = C_1 \mathbf{e}^{x^2} + C_2 \mathbf{e}^{-x^2} $。

评注 当方程的解是非常函数时，很难找到一个特解来确定  $ q(x) $，只能在方程中代入两个形式特解  $ y_{1} $ 与  $ \frac{1}{y_{1}} $，作为方程组来求解  $ q(x) $ 与  $ y_{1} $。作变量代换  $ z = \frac{y_{1}'}{y_{1}} $ 的目的是将微分方程降阶，便于求解。

例  $ 24^{*} $ 求微分方程  $ x^{2}y''(x)+4(x+1)y'(x)+2y(x)=\frac{2}{x^{3}} $ 满足初始条件  $ y(1)=-\frac{1}{6} $， $ y'(1)=0 $ 的特解.

分析 这是二阶非齐次线性微分方程，变系数，又不是欧拉方程，不便于求解. 看是否能通过凑微分化为“恰当方程”来降阶.

解 先看第1项，由于

 $$ [x^{2}y^{\prime}(x)]^{\prime}=x^{2}y^{\prime\prime}(x)+2x y^{\prime}(x)~, $$ 

所以

 $$ x^{2}y^{\prime \prime}(x)=[x^{2}y^{\prime}(x)]^{\prime}-2xy^{\prime}(x) $$ 

原方程成为

 $$ [x^{2}y^{\prime}(x)]^{\prime}-2xy^{\prime}(x)+4(x+1)y^{\prime}(x)+2y(x)=\frac{2}{x^{3}}, $$ 

即

 $$ [x^{2}y^{\prime}(x)]^{\prime}+2[x y^{\prime}(x)+y(x)]+4y^{\prime}(x)=\frac{2}{x^{3}}\;, $$ 

 $$ [x^{2}y^{\prime}(x)+2xy(x)+4y(x)]^{\prime}=\frac{2}{x^{3}}. $$ 

两边从1到x积分，得

 $$ x^{2}y^{\prime}(x)+2xy(x)+4y(x)-(-1)=-\frac{1}{x^{2}}+1, $$ 

即

 $$ y^{\prime}(x)+\frac{2(x+2)}{x^{2}}y=-\frac{1}{x^{4}}. $$ 

满足  $ y(1) = -\frac{1}{6} $ 和  $ y'(1) = 0 $ 的解为

 $$ y(x)=\mathrm{e}^{-\int_{1}^{x}\frac{2(t+2)}{t^{2}}\mathrm{d}t}\left[-\int_{1}^{x}\frac{1}{s^{4}}\mathrm{e}^{\int_{1}^{s}\frac{2(t+2)}{t^{2}}\mathrm{d}t}\mathrm{d}s+\left(-\frac{1}{6}\right)\right], $$ 

由于 $ \int_{1}^{x}\frac{2(t+2)}{t^{2}}dt=2\ln|x|-\frac{4}{x}+4 $，所以

 $$ y(x)=\frac{\mathrm{e}^{\frac{4}{x}}}{\mathrm{e}^{4}x^{2}}\left[-\int_{1}^{x}\mathrm{e}^{4}s^{-2}\mathrm{e}^{-\frac{4}{s}}\mathrm{d}s-\frac{1}{6}\right]=\frac{\mathrm{e}^{\frac{4}{x}}}{\mathrm{e}^{4}x^{2}}\left[-\frac{\mathrm{e}^{4}}{4}(\mathrm{e}^{-\frac{4}{x}}-\mathrm{e}^{-4})-\frac{1}{6}\right]=-\frac{1}{4x^{2}}+\frac{\mathrm{e}^{\frac{4}{x}}}{12\mathrm{e}^{4}x^{2}}. $$ 

此解的存在区间为 $ (0,+\infty) $.

评注 该方程是一个二阶恰当线性微分方程，可通过凑微分来降阶。关于二阶恰当线性微分方程的判定有下面的定理：

定理 设  $ a_{k}(x) $ (k=0,1,2) 在区间  $ (a,b) $ 内具有二阶连续导数， $ a_{0}(x)\neq0 $， $ f(x) $ 在  $ (a,b) $ 内连续，则线性微分方程

 $$ a_{0}(x)y^{\prime \prime}(x)+a_{1}(x)y^{\prime}(x)+a_{2}(x)y(x)=f(x) $$ 

是二阶恰当线性微分方程的充分必要条件是

 $$ a_{0}^{n}(x)-a_{1}^{\prime}(x)+a_{2}(x)\equiv0,\ x\in(a,b). $$ 

证明 由于

 $$ \begin{align*}a_{0}(x)y^{\prime \prime}(x)=&\left[a_{0}(x)y^{\prime}(x)\right]^{\prime}-a_{0}^{\prime}(x)y^{\prime}(x)=\left[a_{0}(x)y^{\prime}(x)\right]^{\prime}-\left[a_{0}^{\prime}(x)y(x)\right]^{\prime}+a_{0}^{\prime \prime}(x)y(x)\ ,\\&a_{1}(x)y^{\prime}(x)=\left[a_{1}(x)y(x)\right]^{\prime}-a_{1}^{\prime}(x)y(x)\ ,\end{align*} $$ 

代入方程可化为

 $$ \left[a_{0}(x)y^{\prime}(x)+\left(a_{1}(x)-a_{0}^{\prime}(x)\right)y(x)\right]^{\prime}+\left[a_{0}^{n}(x)-a_{1}^{\prime}(x)+a_{2}(x)\right]y(x)=f(x). $$ 

读者可类似讨论更高阶恰当线性微分方程的情况.

例  $ 25^{*} $ 求微分方程  $ \cos^{4}x\frac{\mathrm{d}^{2}y}{\mathrm{d}x^{2}}+2\cos^{2}x(1-\sin x\cos x)\frac{\mathrm{d}y}{\mathrm{d}x}+y=\tan x $ 的通解.

分析 方程是二阶变系数线性微分方程，不易直接求解。注意到 $ \frac{1}{\cos^{2}x}dx=d\tan x $，令 $ \tan x=t $，可将方程化为常系数。

解 令  $ \tan x = t $，则

 $$ \frac{\mathrm{d}y}{\mathrm{d}x}=\frac{\mathrm{d}y}{\mathrm{d}t}\cdot\frac{\mathrm{d}t}{\mathrm{d}x}=\frac{\mathrm{d}y}{\mathrm{d}t}\sec^{2}x, $$ 

 $$ \begin{aligned}\frac{\mathrm{d}^{2}y}{\mathrm{d}x^{2}}=&\frac{\mathrm{d}y}{\mathrm{d}x}\bigg(\frac{\mathrm{d}y}{\mathrm{d}t}\sec^{2}x\bigg)=\frac{\mathrm{d}^{2}y}{\mathrm{d}t^{2}}\cdot\frac{\mathrm{d}t}{\mathrm{d}x}\sec^{2}x+\frac{\mathrm{d}y}{\mathrm{d}t}\cdot2\sec^{2}x\tan x\\=&\frac{\mathrm{d}^{2}y}{\mathrm{d}t^{2}}\sec^{4}x+\frac{\mathrm{d}y}{\mathrm{d}t}\cdot2\sec^{2}x\tan x.\end{aligned} $$ 

将它们代入所给微分方程，得

 $$ \left(\frac{\mathrm{d}^{2}y}{\mathrm{d}t^{2}}+\frac{\mathrm{d}y}{\mathrm{d}t}\cdot2\cos^{2}x\tan x\right)+2(1-\sin x\cos x)\frac{\mathrm{d}y}{\mathrm{d}t}+y=t, $$ 

化简得

 $$ \frac{\mathrm{d}^{2}y}{\mathrm{d}t^{2}}+2\frac{\mathrm{d}y}{\mathrm{d}t}+y=t\;. $$ 

易求得该方程的通解为  $ y=(C_{1}t+C_{2})e^{-t}+t-2 $ 。将  $ \tan x=t $ 代入，得原微分方程的通解为

 $$ y=\left(C_{1}\tan x+C_{2}\right)\mathrm{e}^{-\tan x}+\tan x-2. $$ 

评注 二阶变系数线性微分方程的求解，通常是作变量代换或凑微分，将其化为常系数线性微分方程或恰当方程（降阶）来求解。

例  $ 26^{*} $ 求微分方程  $ y''+(4x+e^{2y})(y')^{3}=0 $ 的通解.

分析 该方程不是线性微分方程，也不属于可降阶方程类型。但方程中含 x 的项仅有一次形式，可考虑将 y 作为自变量，x 作为未知函数来转化方程形式。

解 因为  $ \frac{dy}{dx}=\left(\frac{dx}{dy}\right)^{-1} $，则

 $$ \frac{\mathrm{d}^{2}y}{\mathrm{d}x^{2}}=\frac{\mathrm{d}}{\mathrm{d}x}\left(\frac{\mathrm{d}x}{\mathrm{d}y}\right)^{-1}=\frac{\mathrm{d}}{\mathrm{d}y}\left(\frac{\mathrm{d}x}{\mathrm{d}y}\right)^{-1}\cdot\frac{\mathrm{d}y}{\mathrm{d}x}=-\left(\frac{\mathrm{d}x}{\mathrm{d}y}\right)^{-2}\frac{\mathrm{d}^{2}x}{\mathrm{d}y^{2}}\cdot\frac{\mathrm{d}y}{\mathrm{d}x}=-\frac{\mathrm{d}^{2}x}{\mathrm{d}y^{2}}\cdot\left(\frac{\mathrm{d}y}{\mathrm{d}x}\right)^{3}. $$ 

代入所给方程，得到

 $$ -\frac{\mathrm{d}^{2}x}{\mathrm{d}y^{2}}.\left(\frac{\mathrm{d}y}{\mathrm{d}x}\right)^{3}+(4x+\mathrm{e}^{2y})\left(\frac{\mathrm{d}y}{\mathrm{d}x}\right)^{3}=0， 即 \frac{\mathrm{d}^{2}x}{\mathrm{d}y^{2}}-4x=\mathrm{e}^{2y}\text{．} $$ 

这是二阶常系数非齐次线性微分方程，易求得其通解为

 $$ x=C_{1}\mathrm{e}^{-2y}+C_{2}\mathrm{e}^{2y}+\frac{1}{4}y\mathrm{e}^{2y}\;. $$ 

评注 若读者熟悉反函数二阶导数结论： $ \frac{d^2y}{dx^2}=-\frac{d^2x}{dy^2}\cdot\left(\frac{dy}{dx}\right)^3 $，就容易看出该题作反函数代换的有效性.

<div style="text-align: center;"><div style="text-align: center;">习题7.2</div> </div>


1. 求方程  $ y'' + 2x(y')^2 = 0 $ 满足  $ y(0) = 1 $， $ y'(0) = -\frac{1}{2} $ 的特解.

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//965b1e24-ecf4-43cb-a26d-4f871b5887be/markdown_1/imgs/img_in_image_box_1192_175_1326_304.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A34Z%2F-1%2F%2Fa860e4e9ce564ed5a79e40d87402dd5add1ea3794fef1eada3e3579a9b530c42" alt="Image" width="9%" /></div>


习题 7.2 答案

2. 求方程  $ yy'' + 1 = y'^2 $ 满足条件  $ y(0) = 1 $， $ y'(0) = -\sqrt{2} $ 的特解.

3. 设当 x > -1 时，可微函数  $ f(x) $ 满足条件  $ f'(x) + f(x) - \frac{1}{x+1} \int_0^x f(t) \, dt = 0 $，且  $ f(0) = 1 $。证明当  $ x \geq 0 $ 时，有  $ e^{-x} \leq f(x) \leq 1 $ 成立。

4. 求解微分方程：(1)  $ (y^{m})^{2} - y^{n} y^{(4)} = 0 $; (2)  $ xy^{n} = y'(\ln y' - \ln x) $.

5. 若  $ u = f(xyz) $,  $ f(0) = 0 $,  $ f'(1) = 1 $, 且  $ \frac{\partial^3 u}{\partial x \partial y \partial z} = x^2 y^2 z^2 f''(xyz) $, 求  $ u $.

6. 求方程  $ xyy'' - xy'^{2} = yy' $ 的通解.

7. 求满足  $ x=\int_{0}^{x}f(t)dt+\int_{0}^{x}tf(t-x)dt $ 的可微函数  $ f(x) $，并计算  $ I=\int_{-\frac{\pi}{4}}^{\frac{3\pi}{4}}\left|f(x)\right|^{n}dx $ (n=2,3,\cdots).

8. 求代数多项式  $ F(x) $ 和  $ G(x) $，使得

 $$ \int\left[(2x^{4}-1)\cos x+(8x^{3}-x^{2}-1)\sin x\right]\mathrm{d}x=F(x)\cos x+G(x)\sin x+C. $$ 

9. 求微分方程  $ y'' + a^2 y = \sin x $ 的通解，其中常数 a > 0.

10. 求方程  $ y'' + 4y = \frac{1}{2}(x + \cos 2x) $ 的通解.

11. 设  $ f(x) $ 具有二阶连续导数， $ f(0)=0 $， $ f'(0)=1 $，且

 $$ [x y(x+y)-f(x)y]\mathrm{d}x+[f^{\prime}(x)+x^{2}y]\mathrm{d}y=0 $$ 

为一全微分方程，求  $ f(x) $ 及此全微分方程的通解.

12. 设有曲线积分 $ \oint_L 2[xf(y) + g(y)] \, \mathrm{d}x + [x^2g(y) + 2xy^2 - 2xf(y)] \, \mathrm{d}y = 0 $，其中， $ L $为任意一条平面曲线，求可微函数 $ f(y) $， $ g(y) $。已知 $ f(0) = -2 $， $ g(0) = 1 $。

13. 解微分方程  $ x^{3}y^{m} - x^{2}y^{n} + 2xy' - 2y = x\sin(\ln x) $.

14. 设函数  $ u = f(r) $， $ r = \sqrt{x^2 + y^2 + z^2} $ 满足拉普拉斯方程  $ \frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2} + \frac{\partial^2 u}{\partial z^2} = 0 $，其中  $ f(r) $ 二阶可导，且  $ f(1) = f'(1) = 1 $，求  $ f(r) $。

15. 设函数  $ y = y(x) $ 满足  $ xy + \int_{1}^{x} [3y + t^{2}y^{n}] \, dt = 5 \ln x \, (x \geq 1) $，且  $ y'(1) = 0 $，求  $ y = y(x) $ 的表达式.

16. 设  $ u = u(\sqrt{x^2 + y^2}) $ 具有连续二阶偏导数，且满足  $ \frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2} - \frac{1}{x} \cdot \frac{\partial u}{\partial x} + u = x^2 + y^2 $，试求函数  $ u $ 的表达式.

17. 求区间 $ [0,1] $上的连续函数 $ f(x) $，使之满足

 $$ f(x)=\int_{0}^{1}k(x,y)f(y)\mathrm{d}y+1\ , 其中 k(x,y)=\left\{\begin{aligned}&x(1-y),&x\leqslant y\\&(1-x)y,&x>y\end{aligned}\right.. $$ 

18. 设  $ \varphi(x) $ 是常系数二阶方程  $ y'' + ay' + by = 0 $ 满足条件  $ \varphi(0) = 0, \varphi'(0) = 1 $ 的特解.

（1）证明  $ y(x)=\int_{x}^{x}\varphi(x-t)f(t)dt $ 是方程  $ y''+ay'+by=f(x) $ 的一个特解.

(2) 求  $ y'' + y = \sec x $ 的通解.

19. 设  $ f(x) $ 在  $ (-\infty,+\infty) $ 上连续， $ y(x)=\int_{0}^{x}\cos t dt\int_{0}^{x-t}f(u)du $  $ (-\infty<x<+\infty) $.

（1）证明  $ y = y(x) $ 是微分方程  $ y'' + y' = f(x) $ 满足初始条件  $ y(0) = 0, y'(0) = 0 $ 的解.

（2）求微分方程 $ y''+y'=f(x) $的通解.

20*. 求方程  $ \cos^{4}x \cdot y^{n} + 2\cos^{2}x(1 - \sin x\cos x)y' + y = \tan x $ 的通解.

21 $ ^{*} $. 求下列方程的通解：

(1)  $ \cos x \cdot y'' + (\sin x - 2\cos x)y' + (\cos x - \sin x)y = 0 $;

(2)  $ xy'' + (2x + 1)y' + (x + 1)y = (x^2 + x)e^{-x} $.

22. 设  $ xy = C_{1} e^{x} + C_{2} e^{-x} $ 是某微分方程的通解，求对应的微分方程.

23. 设  $ y'' + p(x)y' = f(x) $ 有一个特解  $ \frac{1}{x} $，对应的齐次方程有一个特解  $ x^{2} $，求该方程的通解.

24 $ ^{*} $. 求下列初值问题的特解：

 $$ \left\{\begin{aligned}&x y^{m}+y^{n}+x y^{\prime}+y=1,\\ &y(\pi)=-1,\ y^{\prime}(\pi)=0,\ y^{n}(\pi)=2.\end{aligned}\right. $$ 

## 7.3 微分方程应用

微分方程在各个领域中都有大量的应用，这里主要涉及几何与物理中的应用。求解过程通常可分为3个步骤：建立方程，解方程，对结果进行必要的讨论（简单问题无须此步）。建立方程是解决问题的核心。

（1）建立方程的主要步骤如下.

① 根据实际问题确定要研究的量（自变量、未知函数、必要的参数等），建立适当的坐标系.

② 找出这些量所满足的基本规律（几何的、物理的、化学的等）.

③ 运用这些规律列出微分方程和定解条件.

（2）列方程常用的方法如下.

① 由已知规律直接列出方程.

在数学、物理、化学等领域，许多自然现象所满足的规律已被人们熟知，并可直接由方程描述，如牛顿第二定律、基尔霍夫定律等.

② 微元分析法.

自然界中许多现象所满足的规律可通过变量的微元之间的关系来描述。对这类问题我们不能直接找到变量之间或变量与导数的关系式，但我们可以通过对变量的局部线性近似（均匀化），并利用已知的规律建立这些微元之间的关系，然后通过取极限或在任意区间上做积分的方法来建立微分方程。

（3）列方程中常见的几何量与物理定律如下.

几何量：切线、法线、曲率、弧长、面积、体积等.

物理定律：力学中的牛顿第二定律、万有引力定律；弹性问题中的虎克定律；电学中的基尔霍夫定律；浓度问题.

例1 在13时到14时的什么时刻，一个时钟的分针恰好与时针重和.

分析 若 t 时刻分针与时针分别位于  $ x(t) $ 和  $ y(t) $ 处，则由  $ x(t)=y(t) $ 就可求得两针重和的时间，所以问题的关键是求得  $ x(t) $ 与  $ y(t) $ 的表达式。由于分针与时针都是做匀速运动，其位置函数是容易求得的。

解 将圆周角 60 等分，设每份为一个单位，又设  $ t \, (\text{min}) $ 时刻分针与时针分别位于  $ x(t) $ 和  $ y(t) $ 处，由于初始时间为 13 时，分针与时针的速度分别为 1 （单位/min）与 5/60 （单位/min），故有

 $$ \begin{cases}\frac{\mathrm{d}x}{\mathrm{d}t}=1\\x(0)=0\end{cases},\quad\begin{cases}\frac{\mathrm{d}y}{\mathrm{d}t}=\frac{1}{12},\\y(0)=5\end{cases} $$ 

解得  $ x=t $， $ y=\frac{1}{12}t+5 $。由 x=y，得  $ t=\frac{60}{11}\min\approx5\min 27s $。即两针在 13 时 5 分 27 秒重和。

例2 设 $ f(x) $是区间 $ [0, +\infty) $上具有连续导数的单调递增函数，且 $ f(0)=1 $，对任意的 $ t\in[0, +\infty) $，

直线 x=0, x=t，曲线  $ y=f(x) $ 以及 x 轴所围成的曲边梯形绕 x 轴旋转一周生成一旋转体，若该旋转体的侧面积在数值上等于其体积的 2 倍，求  $ f(x) $ 的表达式.

分析 只需由  $ f(x) $ 分别表示其旋转体的体积与侧面积就可写出方程.

解 旋转体的体积  $ V=\pi\int_{0}^{t}f^{2}(x)dx $，侧面积  $ S=2\pi\int_{0}^{t}f(x)\sqrt{1+[f'(x)]^{2}}dx $.

由题设条件知

 $$ \int_{0}^{t}f^{2}(x)\mathrm{d}x=\int_{0}^{t}f(x)\sqrt{1+\left[f^{\prime}(x)\right]^{2}}\mathrm{d}x. $$ 

上式两边对 t 求导，得  $ f^{2}(t)=f(t)\sqrt{1+[f'(t)]^{2}} $，即  $ y'=\sqrt{y^{2}-1} $，分离变量积分可得通解

 $$ y+\sqrt{y^{2}-1}=C\mathrm{e}^{t} $$ 

由 $ y(0)=1 $，得 $ C=1 $，故 $ y=f(x)=\frac{1}{2}(\mathrm{e}^{x}+\mathrm{e}^{-x}) $。

例3 求一曲线，使其上每一点的向径与切线的夹角等于切线斜角的 $ \frac{1}{3} $

分析 要刻画曲线上点的向径与角度，用极坐标表示更为方便。利用已知条件及导数的几何意义就可建立微分方程。

解 设曲线的极坐标方程为  $ \rho=\rho(\theta) $， $ \varphi $ 表示曲线上点  $ (\rho,\theta) $ 处极径与曲线切线的夹角，切线的斜角为  $ \alpha $ （如图 7.1 所示），则

 $$ \alpha=\theta+\varphi\Longrightarrow\tan\alpha=\tan(\theta+\varphi)=\frac{\tan\theta+\tan\varphi}{1-\tan\theta\cdot\tan\varphi}. $$ 

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//965b1e24-ecf4-43cb-a26d-4f871b5887be/markdown_3/imgs/img_in_image_box_1018_780_1312_1044.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A37Z%2F-1%2F%2F3d04e65686b9bf71dd2bbbb275baee7cef1d69be1376e181622375622444e823" alt="Image" width="20%" /></div>


<div style="text-align: center;"><div style="text-align: center;">图 7.1</div> </div>


由于  $ \tan\alpha=\frac{dy}{dx}=\frac{\sin\theta d\rho+\rho\cos\theta d\theta}{\cos\theta d\rho-\rho\sin\theta d\theta} $，代入上式化简得

 $$ \tan\varphi=\rho\frac{\mathrm{d}\theta}{\mathrm{d}\rho}. $$ 

由题意  $ \varphi = \frac{\alpha}{3} = \frac{\varphi + \theta}{3} \Rightarrow \varphi = \frac{\theta}{2} $，代入①式得微分方程

 $$ \tan\frac{\theta}{2}=\rho\frac{\mathrm{d}\theta}{\mathrm{d}\rho}. $$ 

分离变量积分得曲线方程  $ \rho = C \sin^2 \frac{\theta}{2} = \frac{1}{2} C (1 - \cos \theta) $.

例4 设函数  $ y = f(x) $ 在  $ \left[\frac{1}{2}, +\infty\right) $ 上连续，且  $ f(2) = \frac{4}{3} $. 若曲线  $ y = f(x) $ 与直线  $ x = \frac{1}{2} $， $ x = t $  $ (t > \frac{1}{2}) $ 及 x 轴围成的平面图形  $ D_t $ 绕 x 轴旋转一周而成的旋转体体积为  $ V(t) = \frac{\pi}{2} \left[ 4t^2 f(t) - f\left( \frac{1}{2} \right) \right] $，求  $ D_t $ 绕 y 轴旋转一周而成的旋转体体积  $ V_y $.

分析 利用旋转体体积公式  $ V(t)=\pi\int_{\frac{1}{2}}f^{2}(x)dx $ 与题设条件可建立未知函数  $ f(x) $ 的积分方程，求导可得到微分方程. 解出  $ f(x) $ 后再求  $ V_{y} $.

解  $ D_{t} $ 绕 x 轴旋转一周而成的旋转体体积为  $ V(t)=\pi\int_{\frac{1}{2}}^{t}f^{2}(t) $，由题意得方程

 $$ \pi\int_{\frac{1}{2}}^{t}f^{2}(x)\mathrm{d}x=\frac{\pi}{2}\left[4t^{2}f(t)-f\left(\frac{1}{2}\right)\right]\left(t\geqslant\frac{1}{2}\right), $$ 

上式两边分别对t求导，得

 $$ f^{2}(t)=4t f(t)+2t^{2}f^{\prime}(t)\Rightarrow y^{\prime}+\frac{2}{t}y=\frac{1}{2t^{2}}y^{2}\ ( 伯努利方程 )． $$ 

求得其通解为

 $$ \frac{1}{y}=t^{2}\left(C+\frac{1}{6t^{3}}\right). $$ 

由  $ f(2)=\frac{4}{3} $，得  $ C=\frac{1}{6} $，代入上式得

 $$ y=f(x)=\frac{6x}{1+x^{3}}\ \left(x\geqslant\frac{1}{2}\right). $$ 

于是

 $$ V_{y}=2\pi\int_{\frac{1}{2}}^{t}x\left|\;f(x)\;\right|\mathrm{d}x=2\pi\int_{\frac{1}{2}}^{t}\frac{6x^{2}}{1+x^{3}}\mathrm{d}x=4\pi\Big[\ln(1+x^{3})\Big]_{\frac{1}{2}}^{t}=4\pi\Bigg[\ln(1+t^{3})-\ln\frac{9}{8}\Bigg]. $$ 

例 5 在上半平面求一条凹的曲线，其上任意一点  $ P(x,y) $ 处的曲率等于此曲线在该点的法线段 PQ 长度的倒数（Q 是法线与 x 轴的交点），且曲线在点  $ (1,1) $ 处的切线与 x 轴平行.

分析 要计算 PQ 的长度，需知道点 Q 的坐标，从而需先写出曲线在点 P 处的法线方程.

解 设曲线方程为  $ y=f(x) $，则它在点 P 处的法线方程为  $ Y-y=-\frac{1}{y^{\prime}}(X-x) $.

令Y=0，得它与x轴的交点为 $ Q(x+yy',0) $，则 $ PQ=\sqrt{(yy')^2+y^2} $，由题设y>0， $ y''>0 $，且 $ \frac{|y''|}{\sqrt{(1+y'^2)^3}}=\frac{1}{\sqrt{(yy')^2+y^2}} $，得 $ \begin{cases}yy''=1+(y')^2\\y(1)=1,\ y'(1)=0\end{cases} $（不显含x）。解得 $ y+\sqrt{y^2-1}=e^{\pm(x+1)} $。

评注 曲线  $ y = f(x) $ 的曲率公式： $ \kappa = \frac{|y''|}{\sqrt{(1 + y'^{2})^3}} $.

例6 一小船A从原点出发，以匀速 $ v_{0} $沿y轴正向行驶。另一小船B从x轴上的点 $ (x_{0},0)(x_{0}<0) $出发，朝A追去，其速度方向始终指向A，速度大小为常数 $ v_{1} $.

（1）求船B的运动方程：

（2）如果 $ v_{1}>v_{0} $，问船B需要多少时间才能追上船A.

分析 这是追击问题. 它所隐含的等量关系有两个：一是船 B 的运动方向（切线方向）始终为 BA 方向；二是两船在相同时间段所走过的路程比等于其速度比. 若船 B 的运动轨迹为  $ y = y(x) $，则船 B 能追上船 A 的标志是  $ y(x) $ 在 x = 0 有意义或  $ \lim_{x \to 0} y(x) $ 存在.

解 （1）设船 B 的轨迹线为  $ y = y(x) $ 。经过时间 t，两船的位置分别为  $ A(0, v_{0}t) $ 与  $ B(x, y) $ 。因为船 B 的速度的方向指向船 A（如图 7.2 所示），故

 $$ \frac{\mathrm{d}y}{\mathrm{d}x}=\frac{v_{0}t-y}{0-x},\mathrm{~ 即 ~}-x\frac{\mathrm{d}y}{\mathrm{d}x}=v_{0}t-y. $$ 

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//b2deb5f1-2e1f-43b4-8f42-5302a59c5ebd/markdown_0/imgs/img_in_image_box_1018_1337_1376_1734.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A44Z%2F-1%2F%2Feebe6172d70db027c05713a2fc54fe2367d951ef44618f5d0e5cd0de38e166b2" alt="Image" width="24%" /></div>


船  $ A $ 所走过的路程为  $ v_0t $，船  $ B $ 所走过的路程为  $ \int_0^x \sqrt{1 + y'^2} \, dx $，

<div style="text-align: center;"><div style="text-align: center;">图 7.2</div> </div>


它们的路程比等于其速度比，有

 $$ \int_{0}^{x}\sqrt{1+y^{\prime2}}\mathrm{d}x\mathrm{~}/\nu_{0}t=\nu_{1}\mathrm{~}/\nu_{0}\mathrm{~},\mathrm{~ 即 ~}\nu_{0}t=\frac{\nu_{0}}{\nu_{1}}\int_{0}^{x}\sqrt{1+y^{\prime2}}\mathrm{d}x\mathrm{~}. $$ 

将②式代入①式得

 $$ -x\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{v_{0}}{v_{1}}\int_{0}^{x}\sqrt{1+y^{\prime2}}\mathrm{d}x-y\;. $$ 

两边对 x 求导，得方程

 $$ x y^{\prime \prime}+\frac{v_{0}}{v_{1}}\sqrt{1+\left(y^{\prime}\right)^{2}}=0,\left. 且有 \left.y\right|_{x=x_{0}}=0\right.,\left.y^{\prime}\right|_{x=x_{0}}=0. $$ 

这是可降阶方程，令  $ p=\frac{\mathrm{d}y}{\mathrm{d}x} $， $ k=\frac{v_{0}}{v_{1}}>0 $，得到  $ \left\{\begin{aligned}x\frac{\mathrm{d}p}{\mathrm{d}x}+k\sqrt{1+p^{2}}&=0\\ p(x_{0})&=0\end{aligned}\right. $

解此初值问题，得  $ p=\frac{1}{2}\left[\left(\frac{x_{0}}{x}\right)^{k}-\left(\frac{x}{x_{0}}\right)^{k}\right] $. 再积分，以及利用  $ y(x_{0})=0 $，于是小船的运动轨迹为

 $$ y(x)=\left\{\begin{aligned}{}&{{}-\frac{x_{0}}{2}\Bigg[\frac{1}{k-1}\Bigg(\frac{x_{0}}{x}\Bigg)^{k-1}+\frac{1}{k+1}\Bigg(\frac{x}{x_{0}}\Bigg)^{k+1}-\frac{2k}{k^{2}-1}\Bigg],}&{k\neq1,}\\ {}&{{}-\frac{x_{0}}{2}\Bigg[\operatorname{l n}\frac{x_{0}}{x}+\frac{1}{2}\Bigg(\frac{x}{x_{0}}\Bigg)^{2}-\frac{1}{2}\Bigg],}&{k=1.}\\ \end{aligned}\right. $$ 

（2）只有当 $ k=\frac{v_{0}}{v_{1}}<1 $时，船B才能追上船A；而当船B追上船A时，其x坐标为0，由于

 $$ \operatorname*{l i m}_{x\to0^{-}}y(x)=\operatorname*{l i m}_{x\to0^{-}}-\frac{x_{0}}{2}\left[\frac{1}{k-1}\left(\frac{x_{0}}{x}\right)^{k-1}+\frac{1}{k+1}\left(\frac{x}{x_{0}}\right)^{k+1}-\frac{2k}{k^{2}-1}\right]=\frac{x_{0}k}{k^{2}-1}\;, $$ 

则船 B 追上船 A 需要费时  $ T = \frac{x_{0} k}{(k^{2} - 1) v_{0}} = \frac{x_{0} v_{1}}{v_{0}^{2} - v_{1}^{2}} $.

例7 如图7.3所示，设河宽为a，一条船从岸边一点O出发驶向对岸，船头总是指向对岸与点O相对的一点B. 假设船在静水中的船速为常数 $ v_{1} $，河流中水的流速为常数 $ v_{2} $，试求船过河所走的路线（曲线方程），并讨论在什么条件下船能到达对岸，以及船能到达点B.

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//b2deb5f1-2e1f-43b4-8f42-5302a59c5ebd/markdown_1/imgs/img_in_image_box_995_978_1348_1307.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A52Z%2F-1%2F%2Fb8f929aabda51f0ab66097380c86d3fbbd4ca17279986aaa228618098a7d826b" alt="Image" width="24%" /></div>


<div style="text-align: center;"><div style="text-align: center;">图 7.3</div> </div>


分析 船的实际速度是其航行速度（大小为静水速度，方向指向

点 B) 及水流速度的合成，由此可建立其航迹的微分方程。若船的航迹方程为  $ x = g(y) $，则船能到达对岸的标志是  $ g(y) $ 在 y = a 有意义或  $ \lim_{x \to a^{-}} g(y) $ 存在；船能到达点 B 的标志是  $ g(a) = 0 $ 或  $ \lim_{x \to a^{-}} g(y) = 0 $。

解：如图建立坐标系，则点  $ B $ 的坐标为  $ (0,a) $，设在时刻  $ t $ 船的位置为  $ P(x,y) $，船实际速度  $ \vec{v} $ 是由船的航行速度  $ v_1 = \left(-\frac{v_1x}{\sqrt{x^2+(a-y)^2}}\right) $， $ \frac{v_1(a-y)}{\sqrt{x^2+(a-y)^2}} $ 与水流速度  $ v_2 = (v_2,0) $ 的合成  $ \vec{v} = v_1 + \vec{v}_2 $，所以有

 $$ \frac{\mathrm{d}x}{\mathrm{d}t}=\nu_{2}-\frac{\nu_{\mathrm{l}}x}{\sqrt{x^{2}+\left(a-y\right)^{2}}}\;,\quad\frac{\mathrm{d}y}{\mathrm{d}t}=\frac{\nu_{\mathrm{l}}(a-y)}{\sqrt{x^{2}+\left(a-y\right)^{2}}}. $$ 

两式做商，消去t得

 $ \frac{\mathrm{d}y}{\mathrm{d}x}=\frac{a-y}{k\sqrt{x^{2}+(a-y)^{2}}-x}\quad\left(k=\frac{v_{2}}{v_{1}}\right) $，初始条件 $ y(0)=0 $

这是齐次方程，解此初值问题，得

 $$ (a-y)^{k}=\frac{a(a-y)}{x+\sqrt{x^{2}+(y-a)^{2}}}, $$ 

变形为

 $$ (a-y)^{1-k}=x+\sqrt{x^{2}+(y-a)^{2}}. $$ 

再将①式分母有理化，变形得

 $$ (a-y)^{1+k}=x-\sqrt{x^{2}+(y-a)^{2}}. $$ 

由 $ ^{②} $， $ ^{③} $式可得

 $$ x=\frac{a}{2}\left[\left(\frac{a-y}{a}\right)^{1-k}-\left(\frac{a-y}{a}\right)^{1+k}\right]. $$ 

讨论：（1）当 $ k<1 $，即 $ v_{2}<v_{1} $时，则 $ \lim_{x\to0}x=0 $，即船可到达点 $ B(0,a) $；

(2) 当 k=1，即  $ v_{2}=v_{1} $ 时，则  $ \lim_{y\to a^{-}}x=\frac{a}{2} $，即船可到达对岸点  $ \left(\frac{a}{2},a\right) $

（3）当k>1，即 $ v_{2}>v_{1} $时， $ \lim_{x\to-\infty}x $不存在，即船不能到达对岸.

例  $ 8^{*} $ 有一个直径为 3 寸水平放置的圆盘，正在按每分钟 4 周旋转。离圆盘较远但在同一平面上有一个点在发光。将一个昆虫放在圆盘的边上离光源最远处，头对光源。这时它立即惊起按每秒 1 寸爬行，而且总是头对着光源。试建立运动的微分方程，并求出昆虫再次到达圆盘的边上的点的坐标。

分析 昆虫的实际爬行速度是圆盘的转动速度与昆虫的爬行速度的合成，由此可建立昆虫运动的微分方程.

解 取圆盘的中心为原点，如图7.4所示建立坐标系. 昆虫开始在点 $ \left(\frac{3}{2},0\right) $处，光源在 $ (-∞,0) $处. 圆盘按反时钟方向旋转. 假设在时间t昆虫位于 $ (x,y) $，即 $ (r,\theta) $处，此时昆虫随圆盘转动的方向为（圆周切线方向） $ e_{\tau}=\left(\frac{-y}{r},\frac{x}{r}\right) $，昆虫的爬行方向为 $ e_{s}=(-1,0) $（当光源离圆盘较远时，可视 $ e_{s} $不变），则昆虫的实际运动速度为 $ \omega r e_{\tau}+e_{s}\left(\omega=\frac{2\pi}{15}\right) $，即有 $ \frac{dx}{dy}=ey-1 $  $ {}^{①} $  $ \frac{dy}{dx}=ex $  $ {}^{②} $

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//b2deb5f1-2e1f-43b4-8f42-5302a59c5ebd/markdown_2/imgs/img_in_image_box_1038_908_1378_1227.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A59Z%2F-1%2F%2Fdff697ae70ccb6726e716c766b490bdfd4da644ef923d33647a87fece2fe076e" alt="Image" width="23%" /></div>


<div style="text-align: center;"><div style="text-align: center;">图 7.4</div> </div>


这是一阶线性微分方程组，除用方程组的知识求解外，还可用下面两种方法求解：

（1）两式相除得

 $$ \frac{\mathrm{d}y}{\mathrm{d}x}=-\frac{\omega x}{1+\omega y}. $$ 

分离变量积分，得昆虫的运动轨迹为  $ x^{2}+\left(y+\frac{1}{\omega}\right)^{2}=A^{2} $，由初始条件  $ x(0)=\frac{3}{2} $， $ y(0)=0 $ 得  $ A^{2}=\left(\frac{3}{2}\right)^{2}+\left(\frac{15}{2\pi}\right)^{2} $。这个圆周与圆盘的边界交于点  $ \left(-\frac{3}{2},0\right) $，即昆虫从这一点离开圆盘。

（2）对①式两边求导，并将②式代入，得

 $$ \frac{\mathrm{d}^{2}x}{\mathrm{d}t^{2}}=-\omega\frac{\mathrm{d}y}{\mathrm{d}t}=-\omega^{2}x\ ,\mathrm{~ 即 }\frac{\mathrm{d}^{2}x}{\mathrm{d}t^{2}}+\omega^{2}x=0\ , $$ 

它的解为  $ x = A\cos(\omega t - \phi) $，代入式①式，得  $ y = A\sin(\omega t - \phi) - \frac{1}{\omega} $，消去参数，得  $ x^{2} + \left(y + \frac{1}{\omega}\right)^{2} = A^{2} $。

评注 （1） $ e_{\tau} $ 表达式的源由：t 时刻圆周方程  $ x = r\cos\theta $， $ y = r\sin\theta $，切向量为  $ (\dot{x},\dot{y}) = (-r\sin\theta,r\cos\theta) = (-y,x) $，单位化即得  $ e_{\tau} $。

(2) 将光源置于坐标轴上的无穷远点对方程的建立至关重要，否则方程形式会较复杂，难以求解.

例 9 设桥墩的水平截面是圆，桥墩上方压力均匀分布，其总压力为  $ P \, \text{kN} $. 又设建桥材料的密度为  $ \mu \, \text{kg/m}^3 $，每个截面圆上的允许压强为  $ k \, \text{kN/m}^2 $，求使材料最省的桥墩形状.

分析 桥墩侧面是旋转曲面，只需求得一条母线即可. 当每个截面圆上的压强等于允许压强时，是材料最省的情况. 可由此建立方程.

解 如图7.5所示，设桥墩侧面由曲线  $ y = f(x) $ 绕x轴旋转而成. 在 x 点处截面上所受的总载荷为上方的压力 P 与区间  $ [0, x] $ 上桥墩的自重之和，即  $ P + \mu g \pi \int_{0}^{x} y^{2}(t) \, dt $. 而该截面的面积为  $ \pi y^{2}(x) $，它允许承受的压强为  $ k \, kN/m^{2} $，得

 $$ P+\mu g\pi\int_{0}^{x}y^{2}(t)\mathrm{d}t=k\pi y^{2}(x)\;. $$ 

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//b2deb5f1-2e1f-43b4-8f42-5302a59c5ebd/markdown_3/imgs/img_in_image_box_1002_374_1290_672.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A41%3A07Z%2F-1%2F%2F0811018ec7e95fc6b7f27972c80f62c4773fc1c5c2ff551636eaf447753033ce" alt="Image" width="19%" /></div>


两边对 x 求导得  $ y' = \frac{\mu g}{2k} y $，解得  $ y = c e^{\frac{\mu g}{2k} x} $，由初始条件  $ y(0) = \sqrt{\frac{P}{k\pi}} $，代入得  $ y = \sqrt{\frac{P}{k\pi}} e^{\frac{\mu g}{2k} x} $.

<div style="text-align: center;"><div style="text-align: center;">图 7.5</div> </div>


例 10 设甲容器中有 100 升盐水，并含盐 10 升，乙容器中有 100 升清水。现以 2 升/分的速率将清水注入甲，搅均匀后以 2 升/分的速率将盐水注入乙容器，搅匀后又以 1 升/分的速率流出乙容器，求乙容器中含盐量的变化规律。

分析 应先求得甲容器中含盐量的变化规律，为此可考虑经过较短时间段 $ [t,t+\Delta t] $，甲容器中含盐量的变化（等量关系：含盐改变量 = 流入量 - 流出量)，取极限建立微分方程，再求解. 类似可求得乙容器中含盐量的变化规律.

解 设 $t$ 时刻，甲容器中含盐量为 $x(t)$，则其浓度为 $\frac{\sigma}{100}$，由 $t$ 到 $t+\Delta t$ 时间段甲容器中盐的改变量为 $\Delta x \approx -\frac{x}{100}2\Delta t$，两边除以 $\Delta t$，取极限 $\Delta t \to 0$ 得

 $$ \frac{\mathrm{d}x}{\mathrm{d}t}=-\frac{x}{50},\quad 初值 x(0)=10. $$ 

解出 $ x=10e^{-\frac{1}{50}t} $

再设 $t$ 时刻，乙容器中含盐量为 $y(t)$，由 $t$ 到 $t+\Delta t$ 时间段流入乙容器的盐量约为 $\frac{10}{100}e^{\frac{1}{50}t}\cdot2\Delta t$，流出乙容器的盐量约为 $\frac{y(t)}{100+t}\cdot\Delta t$，从而

 $$ \Delta y\approx\frac{1}{5}\mathrm{e}^{-\frac{1}{50}t}\Delta t-\frac{y}{100+t}\Delta t\;. $$ 

两边除以 $ \Delta t $，取极限 $ \Delta t\to0 $得

 $ \frac{\mathrm{d}y}{\mathrm{d}t}=\frac{1}{5}\mathrm{e}^{-\frac{1}{50}t}-\frac{y}{100+t} $，初值 $ y(0)=0 $。

解出  $  y = \frac{10}{100 + t} [150 - (150 + t)e^{\frac{t}{50}}]  $.

评注 为叙述及书写方便，题解中常常将增量 $ \Delta t $、 $ \Delta x $、 $ \Delta y $写成其微元 $ dt $、 $ dx $、 $ dy $，这样就可不用求极限而直接写出对应的微分方程.

例 11 某种飞机在机场降落时，为了减小滑行距离，在触地的瞬间，飞机尾部将打开减速伞，以增大阻力，使飞机迅速减速并停下。现有一质量为 9000kg 的飞机，着陆时的水平速度为 700km/h，经

测试，减速伞打开后，飞机所受的总阻力与飞机的速度成正比（比例系数为  $ k = 6.0 \times 10^{6} $）。问从着陆点算起，飞机滑行的最长距离是多少？

分析 需先求得飞机滑行的运动方程. 由于飞机受到的外力仅有空气阻力, 根据牛顿第二定律很容易建立微分方程.

解 方法1 由题设，飞机的质量 m = 9000kg，着陆时的水平速度  $ v_{0} = 700km/h $。从飞机接触跑道时开始计时，设 t 时刻飞机的滑行距离为 x(t)，速度为 v(t)。根据牛顿第二定律，得

 $$ m\frac{\mathrm{d}\nu}{\mathrm{d}t}=-k\nu\;. $$ 

又 $ \frac{\alpha v}{dt}=\frac{\alpha v}{dx}\cdot\frac{\alpha x}{dt}=\nu\frac{\alpha v}{dx} $，代入上式得  $ dx=-\frac{m}{k}dv $，积分得  $ x(t)=-\frac{m}{k}v+C $。由于  $ \nu(0)=\nu_{0} $， $ x(0)=0 $，故得  $ C=\frac{m}{k}\nu_{0} $，从而

 $$ x(t)=\frac{m}{k}[v_{0}-\nu(t)]~. $$ 

当 $ v(t)\to0 $时， $ x(t)\to\frac{mv_0}{k}=\frac{9000\times700}{6.0\times10^6}=1.05\text{ km} $.所以，飞机滑行的最长距离为1.05km.

方法2 根据牛顿第二定律，得  $ m\frac{dv}{dt}=-kv $，所以  $ \frac{dv}{v}=-\frac{k}{m}dt $。

两端积分得通解  $ v = C e^{\frac{k}{m} t} $，代入初始条件  $ v|_{t=0} = v_0 $，解得  $ C = v_0 $，故  $ v(t) = v_0 e^{\frac{k}{m} t} $.

飞机滑行的最长距离为

 $$ x=\int_{0}^{+\infty}\nu(t)\mathrm{d}t=-\frac{m v_{0}}{k}\mathrm{e}^{-\frac{k}{m}t}\bigg|_{0}^{+\infty}=\frac{m v_{0}}{k}=1.05\mathrm{~km}. $$ 

方法3 根据牛顿第二定律，得  $ m\frac{d^{2}x}{dt}=-k\frac{dx}{dt} $，即  $ \frac{d^{2}x}{dt^{2}}+\frac{k}{m}\cdot\frac{dx}{dt}=0 $，其特征方程为  $ r^{2}+\frac{k}{m}r=0 $

解得  $ r_{1}=0,\ r_{2}=-\frac{k}{m} $，故  $ x=C_{1}+C_{2}e^{-\frac{k}{m}t} $.

由  $ x\bigg|_{\iota=0}=0 $,  $ \nu\bigg|_{\iota=0}=\frac{dx}{dt}\bigg|_{\iota=0}=-\frac{kC_{2}}{m}e^{-\frac{k}{m}t}\bigg|_{\iota=0}=\nu_{0} $，得  $ C_{1}=-C_{2}=\frac{mv_{0}}{k} $，于是  $ x(t)=\frac{mv_{0}}{k}(1-e^{-\frac{k}{m}t}) $。当  $ t\to+\infty $ 时， $ x(t)\to\frac{mv_{0}}{k}=1.05 $ km。

例 12 一质量均匀的链条挂在一无摩擦的钉子上，运动开始时，链条的一边下垂 8 米，另一边下垂 10 米，如图 7.6 所示，试问整个链条滑过钉子需多少时间.

分析 需先求得链条下滑的运动方程. 链条下滑是由钉子两侧链条的重量差引起的，由牛顿第二定律容易建立微分方程.

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//87c6871e-d2eb-4040-8ea7-b7e5d85eb826/markdown_0/imgs/img_in_image_box_1173_1213_1383_1587.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A43Z%2F-1%2F%2F8ea3fd55da8680a3a35dbd567cbf117eff7688f9266dc4f2a574a491d16af05b" alt="Image" width="14%" /></div>


<div style="text-align: center;"><div style="text-align: center;">图 7.6</div> </div>


解 设链条的线密度为  $ \mu $，经过时间 t，链条下滑了 x 米，则由牛顿第二定律得

 $$ m\frac{\mathrm{d}^{2}x}{\mathrm{d}t^{2}}=(10+x)\mu g-(8-x)\mu g\quad(m=18\mu)~, $$ 

即

 $$ x^{\prime \prime}-\frac{g}{9}x=\frac{g}{9}\;,\quad x(0)=0,\;x^{\prime}(0)=0\;. $$ 

解此方程得  $ x(t)=\frac{1}{2}(e^{-\frac{1}{3}\sqrt{g}t}+e^{\frac{1}{3}\sqrt{g}t})-1 $.

整个链条滑过钉子，即 x = 8，代入上式得  $ t = \frac{3}{\sqrt{g}} \ln(9 + \sqrt{80}) $ (秒).

<div style="text-align: center;"><div style="text-align: center;">习题7.3</div> </div>


<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//87c6871e-d2eb-4040-8ea7-b7e5d85eb826/markdown_1/imgs/img_in_image_box_1183_182_1318_313.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A45Z%2F-1%2F%2Fa472675d2b027a0a375a2a658b9ba7c38768d01164c84da43c922a3cf6b608c9" alt="Image" width="9%" /></div>


习题7.3答案

1. 设函数 $ f $定义在有限或无限区间 $ I $上， $ I $的左端点为0。若正数 $ x \in I $，则 $ f $在 $ [0,x] $上的平均值等于 $ f(0) $与 $ f(x) $的几何平均值，求满足上述条件的函数 $ f(x) $。

2. 设  $ y = f(x) $ 是第一象限内连接点  $ A(0,1) $,  $ B(1,0) $ 的一段连续曲线， $ M(x, y) $ 为该曲线上任意一点，点 C 为 M 在 x 轴上的投影，O 为坐标原点。若梯形 OCMA 的面积与曲边三角形 CBM 的面积之和为  $ \frac{x^{3}}{6} + \frac{1}{3} $，求  $ f(x) $ 的表达式。

3. 求一曲线，使得在其上任意一点 P 处的切线在 y 轴上的截距等于原点到点 P 的距离.

4. 设函数  $ y(x) $ ( $ x \geq 0 $) 二阶可导，且  $ y'(x) > 0 $， $ y(0) = 1 $。过曲线  $ y = y(x) $ 上任意一点  $ P(x, y) $ 作该曲线的切线及 x 轴的垂线，上述两直线与 x 轴所围成的三角形的面积记为  $ S_1 $，区间  $ [0, x] $ 上以  $ y = y(x) $ 为曲边的梯形面积记为  $ S_2 $，并设  $ 2S_1 - S_2 $ 恒为 1，求此曲线  $ y = y(x) $ 的方程。

5．在第一象限内求一条与 x 轴相切于点 A(e,0) 的凹曲线  $ y = f(x) $， $ f''(x) \geq 0 $，使曲线上任意两点  $ M_{1}, M_{2} $ 之间的弧长，等于曲线在这两点处的切线在 y 轴上截下的线段  $ P_{1}P_{2} $ 之长（图 7.7）.

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//87c6871e-d2eb-4040-8ea7-b7e5d85eb826/markdown_1/imgs/img_in_image_box_1042_685_1328_941.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A45Z%2F-1%2F%2F1df2e768b69baffc8d1879eec4a95b29a7f1467ffabfa7465bf966923d3c031e" alt="Image" width="19%" /></div>


<div style="text-align: center;"><div style="text-align: center;">图7.7</div> </div>


 $ y = y(x) $ 是一向上凸的连续曲线，其上任意一点  $ (x, y) $ 处的曲率为

 $ \frac{1}{\sqrt{1+y'^{2}}} $，且此曲线上点(0,1)处的切线方程为 y=x+1，求该曲线的方程，并求函数  $ y=y(x) $ 的极值.

7.（CPU 降温问题）一台计算机启动后，其芯片 CPU 温度会不断升高，升高速度为  $ 20^{\circ}C/h $。为防止温度无限升高而烧坏 CPU，在计算机启动后就要使用风扇，将恒温空气传送给它，使它冷却降温。根据牛顿冷却定律可知冷却速度和物体与空气的温差成正比。设空气的温度一直保持  $ 15^{\circ}C $ 不变，试求 CPU 温度的变化规律。

（1）试证明在这种冷却方法下，CPU温度T是关于时间t的单调递增函数，但 $ T(t) $有上界；

（2）若已知计算机在启动 1h 后其温度的升高率为  $ 14^{\circ}C/h $，试求在启动 2h 后 CPU 温度的升高率.

8. 拖拉机后面通过长为  $ a \, (m) $ 不可拉伸的钢绳拖拉着一个重物，拖拉机的初始位置在坐标原点，重物的初始位置在  $ A = (0, a) $ 点。现在拖拉机沿 x 轴正向前进，求重物运动的轨迹曲线方程。

9. 从船上向海中沉放某种探测仪器，按探测要求，需确定仪器的下沉深度 y（从海平面算起）与下沉速度 v 之间的函数关系。设仪器在重力作用下，从海平面由静止开始铅直下沉，在下沉过程中还受到阻力和浮子的作用。设仪器的质量为 m，体积为 B，海水密度为  $ \rho $，仪器所受的阻力与下沉速度成正比，比例系数为 k (k > 0)。试建立 y 与 v 所满足的微分方程，并求出函数关系式  $ y = y(v) $。

10. 某湖泊的水量为 V，每年排入湖泊内含污染物 A 的污水量为 V/6，流入湖泊内不含 A 的水量为 V/6，流出湖泊的水量为 V/3. 已知 1999 年年底，湖中 A 的含量为  $ 5m_{0} $，超过国家规定指标，为了治理污染，从 2000 年年初起，限定排入湖泊中含 A 污水的浓度不超过  $ m_{0}/V $. 问至少需经过多少年，湖泊中污染物 A 的含量降至  $ m_{0} $ 以内.（注：设湖水中 A 的浓度是均匀的.）

11. 有一小船从岸边的 O 点出发驶向对岸，假定河流两岸是互相平行的直线，并设船速为 a 方向始终垂直于对岸，又设河宽为 2l，河面上任意一点处的水速与该点到两岸距离之积成正比，比例系数为  $ k=\frac{v_{0}}{l^{2}} $，求小船航行的轨迹方程.

12. 一条鲨鱼在发现血腥味时，总是沿血腥味最浓的方向追寻。在海平面上进行试验表明，如果把坐标原点取在血源处，在海平面上建立直角坐标系，那么点 $ (x,y) $处血液的浓度 u（每百万份水中所含血

的份数）的近似值为  $ u = e^{-(x^{2} + 2y^{2})/10^{4}} $ 。求鲨鱼从点  $ (x_{0}, y_{0}) $ 出发向血源前进的路线。

#### 综合题7 $ ^{*} $

<div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//87c6871e-d2eb-4040-8ea7-b7e5d85eb826/markdown_2/imgs/img_in_image_box_1253_177_1389_307.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-07-04T18%3A40%3A47Z%2F-1%2F%2Fbd27bdd97037f5f69b7af16685865caeae7b78461413057f33c8f0580ac1ae78" alt="Image" width="9%" /></div>


综合题7答案

1. 找出所有的可微函数  $ f:(0,+\infty)\to(0,+\infty) $，对于这样的函数，存在一个正实数 a，使得对于所有的 x>0，有  $ f^{\prime}\left(\frac{a}{x}\right)=\frac{x}{f(x)} $.

2. 设  $ g(x) $ 与  $ f(x) $ 都是以  $ \omega $ 为周期的连续函数，讨论方程

 $$ \frac{\mathrm{d}y}{\mathrm{d}x}=g(x)y+f(x) $$ 

（1）存在唯一以 $ \omega $为周期的周期解的条件，并求出此唯一解；

（2）一切解都是以 $ \omega $为周期的周期解的条件，并求出所有这些解；

（3）不存在以 $ \omega $为周期的解的条件.

3. 设函数  $ a(x) $ 和  $ b(x) $ 在区间  $ [0, +\infty) $ 上连续，并且  $ \lim_{x \to +\infty} a(x) = \alpha < 0 $， $ \left|b(x)\right| \leq \beta $ ( $ \alpha $ 与  $ \beta $ 都是常数). 试证明：

（1）方程 $ \frac{dy}{dx}=a(x)y+b(x) $的一切解在 $ [0,+\infty) $有上界；

（2）若  $ \lim_{x\to+\infty}b(x)=0 $，则该方程的一切解  $ y(x) $ 满足  $ \lim_{x\to+\infty}y(x)=0 $。

4. 设  $ f(x) $ 在  $ [0,+\infty) $ 上具有连续导数，满足  $ 3\left[3+f^2(x)\right]f'(x)=2\left[1+f^2(x)\right]^2e^{-x^2} $，且  $ f(0)\leq1 $。证明存在常数  $ M>0 $，使得  $ x\in[0,+\infty) $ 时，恒有  $ \left|f(x)\right|\leq M $。

5. 设  $ \mu_1(x,y) $ 和  $ \mu_2(x,y) $ 为方程  $ M(x,y)\mathrm{d}x + N(x,y)\mathrm{d}y = 0 $ 的两个积分因子，且  $ \frac{\mu_1}{\mu_2} \neq $ 常数，证明  $ \frac{\mu_1}{\mu_2} = C $ 是该方程的通解，其中  $ C $ 为任意常数.

6. 设函数  $ u = f(\sqrt{x^2 + y^2}) $，满足  $ \frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2} = \iint_{x^2 + t^2 \leq x^2 + v^2} \frac{1}{1 + s^2 + t^2} ds dt $，且  $ \lim_{x \to 0^+} f'(x) = 0 $.

（1）试求函数  $ f'(x) $ 的表达式. （2）若  $ f(0)=0 $ ，求  $ \lim_{x\to0^{+}}\frac{f(x)}{x^{4}} $

7. 设函数  $ f(x) $ 在  $ [0,+\infty) $ 上连续， $ \Omega(t)=\left\{(x,y,z)\mid x^{2}+y^{2}+z^{2}\leq t^{2},z\geq0\right\} $， $ S(t) $ 是  $ \Omega(t) $ 的表面， $ D(t) $ 是  $ \Omega(t) $ 在 xOy 面的投影区域， $ L(t) $ 是  $ D(t) $ 的边界曲线，已知当  $ t\in(0,+\infty) $ 时，恒有

 $$ \oint_{L(t)}f(x^{2}+y^{2})\sqrt{x^{2}+y^{2}}\mathrm{d}s+\oint_{S(t)}(x^{2}+y^{2}+z^{2})\mathrm{d}S=\iint\limits_{D(t)}f(x^{2}+y^{2})\mathrm{d}\sigma+\iiint\limits_{\Omega(t)}\sqrt{x^{2}+y^{2}+z^{2}}\mathrm{d}V, $$ 

求  $ f(x) $ 的表达式.

8. 求微分方程  $ y'' + 3y' + 2y = \frac{1}{e^x + 1} $ 的通解.

9. 求下面初值问题的特解.

 $$ \left\{\begin{aligned}&y^{\prime \prime}+\frac{1}{x}y^{\prime}-\frac{1}{x^{2}}y=\frac{1}{1+x^{2}},\\ &y(1)=0,\ y^{\prime}(1)=\frac{\pi}{4}.\end{aligned}\right. $$ 

10. 求微分方程  $ \frac{d^2y}{dx^2}\cos x - 2\frac{dy}{dx}\sin x + 3y\cos x = e^x $ 的通解.

11. 当  $ \lambda $ 为何值时，方程  $ \int_{0}^{1} \min(x, y) f(y) \, \mathrm{d} y = \lambda f(x) $ 在  $ (0,1) $ 内有不恒等于零的连续解？这些解是什么？

12. 设  $ f(x) $ 和  $ g(x) $ 都有连续导数，满足  $ f'(x) = g(x) $， $ g'(x) = 2\mathrm{e}^{x} - f(x) $，且  $ f(0) = 0 $， $ g(0) = 2 $，求定积分  $ \int_{0}^{\pi}\left[\frac{g(x)}{1+x}-\frac{f(x)}{(1+x)^2}\right]\mathrm{d}x $。

13. 设  $ f(x) $ 在  $ \mathbb{R} $ 上二阶可导，且  $ f(0)=0 $， $ f'(0)=1 $，设  $ g(x,y)=\int_0^y f(xt)dt $ 满足方程  $ \frac{\partial^2 g}{\partial x \partial y} - x y g(x,y) = xy^2 \sin xy $，求  $ g(x,y) $。

14. 求微分方程  $ yy'' + \left(\frac{x}{y} + \ln y\right)(y')^3 = 0 $ 的通解.

15. 求微分方程  $ \left(x^{2}+y^{2}\right)y^{\prime\prime}=2\left(1+y^{\prime2}\right)\left(xy^{\prime}-y\right) $ 的通解.

16. 设有非齐次线性微分方程组  $ \left\{\begin{aligned}\frac{\mathrm{d}x}{\mathrm{d}t}&=\frac{1}{t}x-y+t\\ \frac{\mathrm{d}y}{\mathrm{d}t}&=\frac{1}{t^{2}}x+\frac{2}{t}y-t^{2}\end{aligned}\right. $，已知  $ \left\{\begin{aligned}x&=t^{2}\\ y&=-t\end{aligned}\right. $ 是对应其次微分方程组的一个解，求非齐次线性微分方程组的通解.

17. 设函数  $ y = y(x) $ 是微分方程  $ y'' + 6y' + 5y = f(x) $ 的任一解，其中  $ f(x) $ 是  $ [a, +\infty) $ 上的连续函数，且  $ \lim_{x \to +\infty} f(x) = A $（有限常数），求  $ \lim_{x \to +\infty} y(x) $.

18. 设  $ f(x) $ 是  $ [0,+\infty) $ 上的有界连续函数，证明方程  $ y''+14y'+13y=f(x) $ 的每一个解在  $ [0,+\infty) $ 上都是有界的.

19. 设  $ y = f(x) $ 是微分方程  $ y'' - 2y' - 3y = \ln(1 + x) $ 满足初值条件  $ y(0) = \frac{2}{9} $， $ y'(0) = \frac{11}{3} $ 的解，证明当  $ x > 0 $ 时，有  $ f(x) < e^{3x} - e^{-x} - \frac{1}{3}x + \frac{2}{9} $。

20. 求出所有在 $ [0,+\infty) $上连续，在 $ (0,+\infty) $上函数值为正的函数  $ y = g(x) $，使得对所有  $ x > 0 $，区域  $ R_x = \{(s,t) \mid 0 \leq s \leq x, 0 \leq t \leq g(s)\} $ 的质心的  $ y $ 坐标和  $ g $ 在  $ [0,x] $ 上的平均值相同，并证明结论.

21. 设  $ p_1(x) $,  $ p_2(x) $ 是连续函数， $ y_1(x) $,  $ y_2(x) $ 是方程  $ y'' + p_1(x)y' + p_2(x)y = 0 $ 的两个线性无关的解。证明如果  $ \alpha, \beta $ 是  $ y_1(x) $ 的两个零点，则在  $ \alpha, \beta $ 之间必存在  $ y_2(x) $ 的一个零点。

22. 一个质点在直线上运动，仅有与速度成反比的力作用于其上. 如果初速为每秒 1000 尺，当它经过 1200 尺后，速度为每秒 900 尺. 试计算运行这段距离的时间. 误差不超过百分之一秒.

23. 飞机在机场开始滑行着陆。在着陆时刻已失去垂直速度，水平速度为 $ v_{0} $米/秒。飞机与地面的摩擦系数为 $ \mu $，且飞机运动时所受空气的阻力与速度的平方成正比，在水平方向的比例系数为 $ k_{x} $千克·秒 $ ^{2} $/米 $ ^{2} $，在垂直方向的比例系数为 $ k_{y} $千克·秒 $ ^{2} $/米 $ ^{2} $。设飞机的质量为m千克，求飞机从着陆到停止所需的时间。

24. 有一圆锥形的塔，底半径为 R，高为  $ h (h > R) $，现沿塔身建一登上塔顶的楼梯，要求楼梯曲线在每一点的切线与过该点垂直于 xOy 平面的直线的夹角为  $ \frac{\pi}{4} $，设楼梯入口在点  $ (R, 0, 0) $ 处，试求楼梯曲线的方程（设塔底面为 xOy 平面）。

25. 设过曲线上任意一点  $ M(x,y) $ 的切线 MT 与坐标原点到此点的连线 OM 相交成定角  $ \omega $，求此曲线方程.

26. （四人追逐问题）位于边长为 2a 的一个正方形的 4 个顶点有 4 个人  $ P_{1}, P_{2}, P_{3}, P_{4} $，一开始分别位于点  $ A_{1}(a, a), A_{2}(-a, a), A_{3}(-a, -a), A_{4}(a, -a) $ 处。他们玩依次追逐的游戏， $ P_{1} $ 追逐  $ P_{2} $， $ P_{2} $ 追逐  $ P_{3} $， $ P_{3} $ 追逐  $ P_{4} $， $ P_{4} $ 追逐  $ P_{1} $。求各自追逐路线的方程。

27. 一个质点缚在一根轻的竿 AB 的一端 A 上. 竿长为 a，竿的 B 端有铰链使它能在一个垂直平面上自由转动. 竿在铰链上面竖直的位置处于平衡，然后轻微地扰动它. 证明竿从通过水平位置降到最低位置的时间是  $ \sqrt{a/g}\ln(1+\sqrt{2}) $.

28. 一个质量为  $ m = 1 \, kg $ 的爆竹，以初速度  $ v_0 = 21 \, m/s $ 铅直向上飞向高空，已知在上升的过程中，空气对它的阻力与它运动速度  $ v $ 的平方成正比，比例系数为  $ k = 0.025 \, kg/m $。求该爆竹能够到达的最高高度。

29. 一质点在一与距离 k 次方成反比的有心力作用下运动. 如果质点的运动轨道为一圆(假设有心力由圆周上的点出发)，试求 k 的值.

30.（雨滴下落的速度）有一滴雨滴，以初速度零开始从高空落下，设其初始质量为  $ m_{0}(g) $. 在下落的过程中，由于不断蒸发，所以其质量以  $ a(g/s) $ 的速率逐渐减少. 已知雨滴在下落时，所受到的空气阻力和下落的速度成正比，比例系数为  $ k(>0) $. 试求在时刻  $ t\left(0<t<\frac{m_{0}}{a}\right) $，雨滴的下落速度  $ v(t) $.


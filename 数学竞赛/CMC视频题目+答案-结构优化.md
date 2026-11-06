---
title: CMC视频题目+答案-结构优化
course: 数学竞赛
tags:
  - 数学竞赛
  - 习题
  - OCR整理
created: 2026-11-05
source:
  - "数学竞赛/CMC视频题目+答案.pdf"
  - "数学竞赛/CMC视频题目+答案.pdf_by_PaddleOCR-VL-1.6.md"
---

> 本文依据 PaddleOCR-VL-1.6 转写稿，结合原 PDF 整理《CMC 复习专题（非数学 A 类）》，保留基础篇与强化篇的题目顺序、原编号、子题及难度星级，将附录答案逐题合并到对应题目下方。答案默认折叠，点击“原书参考答案”即可展开完整解答。

> [!note] AI 补充：整理范围与阅读说明
> 原 PDF 与 OCR 文件均保留。目录以 PDF 的印刷目录及原书页码为准（PDF 文件页序比正文页码多 8 页），不采用存在重复跳转的 PDF 书签；书籍类 OCR 的 5 处原图链接原样保留。
> 下文答案均为原书参考答案，未逐题独立验算；已发现的来源矛盾与缺失在相应位置注明。原前言中的“资料仅收录题目”照录，但本版本 PDF 实际已经附有答案。

# 主要内容

- 基础篇：一元极限、一元微分学、一元积分学、微分方程、空间解析几何、多元微分学、多元积分学、无穷级数。
- 强化篇：一元极限、一元微分学、一元积分学、多元积分学、无穷级数。
- 基础篇答案（原附录 A）：已合并至各题下方，默认折叠。
- 强化篇答案（原附录 B～F）：已合并至各题下方，默认折叠。

---

# 书目信息

- 原书名：CMC 复习专题（非数学 A 类）。
- 面向：第十八届全国大学生数学竞赛。
- 整理者：B 站「爱学数学的曙薯」，署名“空曙”，二〇二六年。

> 月色铺沧海 潮生复潮平  
> 莫恨今日丧 他方任翱翔

---

# 前言

本资料面向全国大学生数学竞赛（非数学类），以题目练习为主。题目由 B 站 UP 主 @ 爱学数学的曙薯独自整理，主要来源为官方 CMC 解析教程（非数学类，红色封皮第二版）、往届 CMC 初赛/复赛真题及考研数学一真题。资料仅收录题目，解答见 B 站 @ 爱学数学的曙薯的相关视频，供自主学习。

全书分基础篇与强化篇. 基础篇侧重基础计算与简单证明, 不冲击国赛者可酌情参考; 强化篇多为压轴证明题, 综合性强, 重在数学思维, 适合冲击决赛.

题目按难度分为五级，以 ★ 数量标识：

- 简单题：★，最简单的送分题。
- 基础题：★★，有一定计算量，较简单。
- 较难题：★★★，竞赛常见中档题，需较系统地掌握相关知识。
- 综合题：★★★★，对标竞赛压轴题，需较深思考。
- 压轴题：★★★★★，思维量极大，难度高，具探究价值，可酌情学习。

题目全为手工整理，难免有误；视频内容亦可能出错。已发现错误会在评论区或弹幕更正，欢迎补充。请勿盲信视频，学会题目才是关键。

资料内容可随意二次转发、创作、搬运。祝各位在新一届数学竞赛中取得优异成绩。

空曙

二〇二六年

---
# 第一部分 基础篇

---

# 基础篇·第一章 一元极限

## 1.1 函数极限计算

分清极限计算类型，对于常见的0/0型极限，通常采用泰勒展开进行估阶；无穷处的极限与变限积分一般采用洛必达进行化简。计算途中也要随时注意中值定理，定积分定义，积分放缩等技巧的使用。

**1.** (难度: ★)

$$\lim_{x\to0}\frac{\frac{x^{2}}{3}+1-\sqrt[3]{1+x^{2}}}{\left(\cos x-e^{x^{2}}\right)\sin x^{2}}$$

> [!answer]- 原书参考答案（A.1.1 第 1 题，未逐题独立验算）
> **1.** 第一步：分子用广义二项式展开. 由 $(1+u)^{\frac{1}{3}}=1+\frac{1}{3}u-\frac{1}{9}u^{2}+O(u^{3})$，取 $u=x^{2}$ 得
>
> $$\sqrt[3]{1+x^{2}}=1+\frac{x^{2}}{3}-\frac{x^{4}}{9}+O(x^{6}),$$
>
> 故
>
> $$\frac{x^{2}}{3}+1-\sqrt[3]{1+x^{2}}=\frac{x^{4}}{9}+O(x^{6}).$$
>
> 第二步：把分母中「主项抵消」的部分展开.由
>
> $$\cos x=1-\frac{x^{2}}{2}+\frac{x^{4}}{24}+O(x^{6}),\qquad\mathrm{e}^{x^{2}}=1+x^{2}+\frac{x^{4}}{2}+O(x^{6}),$$
>
> 得
>
> $$\cos x-\mathrm{e}^{x^{2}}=-\frac{3}{2}x^{2}+O(x^{4}),$$
>
> 再乘 $\sin x^{2} \sim x^{2}$，分母为 $-\frac{3}{2}x^{4} + O(x^{6})$.
>
> 第三步：相除. 分子、分母的最高次都是 $x^{4}$，故
>
> $$\lim_{x\to0}\frac{\frac{x^{2}}{3}+1-\sqrt[3]{1+x^{2}}}{\left(\cos x-\mathrm{e}^{x^{2}}\right)\sin x^{2}}=\frac{1/9}{-3/2}=-\frac{2}{27}.$$

**2.** （难度：★）

$$\lim_{x\to+\infty}\frac{x^{2}}{\ln x}\left[(x+3)^{\frac{1}{x}}-x^{\frac{1}{x+3}}\right]$$

> [!answer]- 原书参考答案（A.1.1 第 2 题，未逐题独立验算）
> **2.** 第一步：取对数，把幂差化为指数差.
>
> 记
>
> $$A=\frac{\ln(x+3)}{x},\qquad B=\frac{\ln x}{x+3},$$
>
> 则
>
> $$(x+3)^{\frac{1}{x}}=e^{A},\qquad x^{\frac{1}{x+3}}=e^{B},$$
>
> 且当 $x \to +\infty$ 时 $A \to 0, B \to 0$. 于是原式化为
>
> $$\lim_{x\to+\infty}\frac{x^{2}}{\ln x}\left(e^{A}-e^{B}\right).$$
>
> 下面先化简括号内的 $e^{A}-e^{B}$，给出三种做法.
>
> 做法一（直接泰勒展开）。由 $e^{t}=1+t+\frac{t^{2}}{2}+o(t^{2})(t\to0)$，
>
> $$\begin{aligned}e^{A}-e^{B}&=\left(1+A+\frac{A^{2}}{2}+o(A^{2})\right)-\left(1+B+\frac{B^{2}}{2}+o(B^{2})\right)\\&=(A-B)+\frac{A^{2}-B^{2}}{2}+o(A^{2}+B^{2}).\end{aligned}$$
>
> 其中
>
> $$\frac{A^{2}-B^{2}}{2}=\frac{(A-B)(A+B)}{2}.$$
>
> 要把这一项与 A - B 比大小，先把 A + B 与 A - B 的阶估出来.
>
> (i) A + B 的阶. 由 $\ln(x+3) \sim \ln x (x \to +\infty)$ 得
>
> $$A=\frac{\ln(x+3)}{x}\sim\frac{\ln x}{x},\qquad B=\frac{\ln x}{x+3}\sim\frac{\ln x}{x},$$
>
> 两者都是 $\frac{\ln x}{x}$ 这一级，故
>
> $$A+B\sim\frac{2\ln x}{x}.$$
>
> (ii) A - B 的阶（通分 + 差分估计）. 先通分:
>
> $$A-B=\frac{\ln(x+3)}{x}-\frac{\ln x}{x+3}=\frac{(x+3)\ln(x+3)-x\ln x}{x(x+3)}.$$
>
> 分母 $\sim x^{2}$; 分子是 $g(t) = t\ln t$ 在 t = x 与 $t = x + 3$ 处的差分, 由拉格朗日中值定理 (也就是“差分 $\approx$ 导数 $\times$ 步长”):
>
> $$(x+3)\ln(x+3)-x\ln x=g(x+3)-g(x)=3g^{\prime}(\xi)=3(\ln\xi+1)\sim3\ln x$$
>
> ( $ξ$介于x与 $x+3$之间).于是
>
> $$A-B\sim\frac{3\ln x}{x^{2}}.$$
>
> 把两式代入 $A^{2}-B^{2}=(A-B)(A+B)$，得
>
> $$\frac{A^{2}-B^{2}}{2}\sim\frac{3\ln^{2}x}{x^{3}}.$$
>
> 而 $A-B \sim \frac{3 \ln x}{x^{2}}$，两者的比值为
>
> $$\frac{\frac{3\ln^{2}x}{x^{3}}}{\frac{3\ln x}{x^{2}}}=\frac{\ln x}{x}\to0,$$
>
> 故二次项是比 A - B 更高阶的无穷小，可以并入 $o(A - B)$，得到
>
> $$e^{A}-e^{B}\sim A-B.$$
>
> 做法二（提取公因子）。由
>
> $$e^{A}-e^{B}=e^{B}\left(e^{A-B}-1\right).$$
>
> 当 $x \to +\infty$ 时 $B \to 0$，故 $e^{B} \to 1$；又 $A - B \to 0$，故 $e^{A - B} - 1 \sim A - B$。于是
>
> $$e^{A}-e^{B}\sim A-B.$$
>
> 做法三 (拉格朗日中值定理). 令 $f(t) = e^{t}$. 由拉格朗日中值定理,
>
> $$e^{A}-e^{B}=e^{\xi}(A-B),$$
>
> 其中 $\xi$ 介于 A、B 之间。由 $A, B \to 0$ 知 $\xi \to 0$，从而 $e^{\xi} \to 1$，故
>
> $$e^{A}-e^{B}\sim A-B.$$
>
> 三种做法殊途同归，均得到 $e^{A}-e^{B}\sim A-B$。于是原极限等价于
>
> $$\lim_{x\to+\infty}\frac{x^{2}}{\ln x}\left(A-B\right),$$
>
> 其中
>
> $$A-B=\frac{\ln(x+3)}{x}-\frac{\ln x}{x+3}.$$
>
> 第二步：计算化简后的极限.
>
> 通分，得
>
> $$A-B=\frac{(x+3)\ln(x+3)-x\ln x}{x(x+3)},$$
>
> 于是
>
> $$\frac{x^{2}}{\ln x}(A-B)=\frac{x}{x+3}\cdot\frac{(x+3)\ln(x+3)-x\ln x}{\ln x}.$$
>
> 由于 $\frac{x}{x+3}\rightarrow1$，只需计算
>
> $$L=\lim_{x\to+\infty}\frac{(x+3)\ln(x+3)-x\ln x}{\ln x}.$$
>
> 下面给出三种做法.
>
> 做法一（洛必达法则）。分子、分母都趋于 $+\infty$，满足 $\frac{\infty}{\infty}$ 型洛必达条件。对分子求导：
>
> $$\begin{aligned}&\left[(x+3)\ln(x+3)-x\ln x\right]^{\prime}\\ &=\ln(x+3)+1-\ln x-1\\ &=\ln\left(\frac{x+3}{x}\right)=\ln\left(1+\frac{3}{x}\right),\\ \end{aligned}$$
>
> 分母求导得 $\frac{1}{x}$，于是
>
> $$\begin{aligned}L&=\lim_{x\to+\infty}\frac{\ln(1+\frac{3}{x})}{\frac{1}{x}}\\&=\lim_{x\to+\infty}x\ln\left(1+\frac{3}{x}\right)=3,\end{aligned}$$
>
> 最后一步用到等价无穷小 $\ln(1+t) \sim t (t \to 0)$.
>
> 做法二（中值定理）。令 $g(t)=t\ln t$，则 $g'(t)=\ln t+1$。由拉格朗日中值定理，
>
> $$\begin{aligned}(x+3)\ln(x+3)-x\ln x&=g(x+3)-g(x)\\&=3g^{\prime}(\xi)=3(\ln\xi+1),\end{aligned}$$
>
> 其中 $\xi \in (x, x+3)$. 当 $x \to +\infty$ 时 $\xi \to +\infty$ 且 $\frac{\ln \xi}{\ln x} \to 1$, 故
>
> $$L=\lim_{x\to+\infty}\frac{3(\ln\xi+1)}{\ln x}=3.$$
>
> 做法三（配凑）。对分子作如下配凑：
>
> $$\begin{aligned}&\left(x+3\right)\ln(x+3)-x\ln x\\&=\left(x+3\right)\ln(x+3)-\left(x+3\right)\ln x+3\ln x\\&=\left(x+3\right)\ln\left(1+\frac{3}{x}\right)+3\ln x.\end{aligned}$$
>
> 于是
>
> $$L=\lim_{x\to+\infty}\left[\frac{(x+3)\ln\left(1+\frac{3}{x}\right)}{\ln x}+3\right].$$
>
> 其中由 $(x+3)\ln\left(1+\frac{3}{x}\right)\to3$与 $\ln x\to+\infty$，第一项趋于0，从而
>
> $$L=0+3=3.$$
>
> 综上所述，
>
> $$\lim_{x\to+\infty}\frac{x^{2}}{\ln x}\left[(x+3)^{\frac{1}{x}}-x^{\frac{1}{x+3}}\right]=3.$$

**3.** （难度：★★★）

$$\lim_{x\to0}\frac{\int_{0}^{x}\left[e^{(x-t)^{2}}-1\right]\sin t dt}{x\tan^{3}x}$$

> [!answer]- 原书参考答案（A.1.1 第 3 题，未逐题独立验算）
> **3.** 第一步：把被积函数的主部提出来.由
>
> $$\mathbf{e}^{(x-t)^{2}}-1=(x-t)^{2}+O\big((x-t)^{4}\big),\qquad\sin t=t+O(t^{3})$$
>
> 得 $(0 \leqslant t \leqslant x$，把低阶项一律记成 $O(x^{4})$
>
> $$\left[\mathbf{e}^{(x-t)^{2}}-1\right]\sin t=(x-t)^{2}t+O(x^{4}),$$
>
> 故
>
> $$\int_{0}^{x}\left[\mathbf{e}^{(x-t)^{2}}-1\right]\sin t\mathrm{d}t=\int_{0}^{x}(x-t)^{2}t\mathrm{d}t+O(x^{5}).$$
>
> 第二步：算主部的积分. 令 $t=xu$，则
>
> $$\int_{0}^{x}(x-t)^{2}t\mathrm{d}t=x^{4}\int_{0}^{1}(1-u)^{2}u\mathrm{d}u=x^{4}\left[\frac{u^{2}}{2}-\frac{2u^{3}}{3}+\frac{u^{4}}{4}\right]_{0}^{1}=\frac{x^{4}}{12}.$$
>
> 第三步: 比较分母的阶. 当 $x \to 0$ 时 $\tan x \sim x$, 故 $x \tan^{3} x = x^{4} (1 + O(x^{2}))$. 于是
>
> $$\lim_{x\to0}\frac{\int_{0}^{x}\left[\mathrm{e}^{(x-t)^{2}}-1\right]\sin t\mathrm{d}t}{x\tan^{3}x}=\frac{x^{4}/12+O(x^{5})}{x^{4}\left(1+O(x^{2})\right)}\longrightarrow\frac{1}{12}.$$

**4.** （难度：★★）

$$\lim_{x\to0}\frac{\sqrt{1+\tan x}-\sqrt{1+\sin x}}{x\ln(1+x)-x^{2}}$$

> [!answer]- 原书参考答案（A.1.1 第 4 题，未逐题独立验算）
> **4.** 第一步：分子有理化，把 $x^{3}$ 阶主部提出来.
>
> $$\sqrt{1+\tan x}-\sqrt{1+\sin x}=\frac{\tan x-\sin x}{\sqrt{1+\tan x}+\sqrt{1+\sin x}},$$
>
> 分母中的两个根式都趋于1，故 $\sqrt{1+\tan x}+\sqrt{1+\sin x}\rightarrow2$。又
>
> $$\tan x-\sin x=\left(x+\frac{x^{3}}{3}+O(x^{5})\right)-\left(x-\frac{x^{3}}{6}+O(x^{5})\right)=\frac{x^{3}}{2}+O(x^{5}),$$
>
> 所以分子 $=\frac{x^{3}}{4}+O(x^{5})$
>
> 第二步: 分母展开. 由 $\ln(1+x)=x-\frac{x^{2}}{2}+\frac{x^{3}}{3}+O(x^{4})$,
>
> $$x\ln(1+x)-x^{2}=x\left(x-\frac{x^{2}}{2}+\frac{x^{3}}{3}\right)-x^{2}+O(x^{5})=-\frac{x^{3}}{2}+O(x^{4}).$$
>
> 第三步：相除.
>
> $$\frac{\sqrt{1+\tan x}-\sqrt{1+\sin x}}{x\ln(1+x)-x^{2}}=\frac{\frac{1}{4}x^{3}+O(x^{5})}{-\frac{1}{2}x^{3}+O(x^{4})}\longrightarrow-\frac{1}{2}.$$

**5.** （难度：★★★）

$$\lim_{x\to+\infty}\left[(2x)^{1+\frac{1}{2x}}-x^{1+\frac{1}{x}}-x\right]$$

> [!answer]- 原书参考答案（A.1.1 第 5 题，未逐题独立验算）
> **5.** 第一步: 两项都写成「主项 + 修正项」。由 $e^{u} = 1 + u + O(u^{2})$,
>
> $$(2x)^{1+\frac{1}{2x}}=2x\mathrm{e}^{\frac{\ln2x}{2x}}=2x\left[1+\frac{\ln2x}{2x}+O\left(\frac{\ln^{2}x}{x^{2}}\right)\right]=2x+\ln2x+O\left(\frac{\ln^{2}x}{x}\right),$$
>
> $$x^{1+\frac{1}{x}}=x\mathbf{e}^{\frac{\ln x}{x}}=x\left[1+\frac{\ln x}{x}+O\left(\frac{\ln^{2}x}{x^{2}}\right)\right]=x+\ln x+O\left(\frac{\ln^{2}x}{x}\right).$$
>
> 第二步：相减.
>
> $$(2x)^{1+\frac{1}{2x}}-x^{1+\frac{1}{x}}-x=(2x+\ln2x)-(x+\ln x)-x+O\left(\frac{\ln^{2}x}{x}\right)=\ln2+O\left(\frac{\ln^{2}x}{x}\right),$$
>
> 故原极限为 $\ln2$.

**6.** (难度:★★)

$$\lim_{x\to0}\left(\frac{\arcsin x}{\sin x}\right)^{\cot^{2}x}$$

> [!answer]- 原书参考答案（A.1.1 第 6 题，未逐题独立验算）
> **6.** 第一步: 定类型并取对数. $\frac{\arcsin x}{\sin x} \to 1$, 指数 $\cot^2 x \to +\infty$, 是 $1^\infty$ 型. 记极限为 $L$, 由 $\cot^2 x \sim \frac{1}{x^2}$,
>
> $$\ln L=\lim_{x\to0}\cot^{2}x\ln\frac{\arcsin x}{\sin x}=\lim_{x\to0}\frac{1}{x^{2}}\ln\frac{\arcsin x}{\sin x}.$$
>
> 第二步：把对数内的比展开到 $x^{2}$阶.由
>
> $$\arcsin x=x+\frac{x^{3}}{6}+O(x^{5}),\qquad\sin x=x-\frac{x^{3}}{6}+O(x^{5}),$$
>
> 得
>
> $$\frac{\arcsin x}{\sin x}=\frac{1+\frac{x^{2}}{6}+O(x^{4})}{1-\frac{x^{2}}{6}+O(x^{4})}=1+\frac{x^{2}}{3}+O(x^{4}),$$
>
> 故 $\ln\frac{\arcsin x}{\sin x}=\frac{x^{2}}{3}+O(x^{4}).$
>
> 第三步：代入.
>
> $$\ln L=\lim_{x\to0}\frac{1}{x^{2}}\left(\frac{x^{2}}{3}+O(x^{4})\right)=\frac{1}{3},\qquad L=\mathbf{e}^{\frac{1}{3}}=\sqrt[3]{\mathbf{e}}.$$

**7.** （难度：★★★）

$$\lim_{n\to\infty}\left(\frac{\cos(\pi\sqrt{4n^{2}-1})}{\cos(\pi\sqrt{4n^{2}-3})}\right)^{n^{2}}$$

> [!answer]- 原书参考答案（A.1.1 第 7 题，未逐题独立验算）
> **7.** 先确定类型: 当 $n \to \infty$ 时分子、分母都趋于 1, 而指数 $n^2 \to \infty$, 故这是 $1^\infty$ 型极限. 取对数:
>
> $$\ln L=\lim_{n\to\infty}n^{2}\ln\frac{\cos\left(\pi\sqrt{4n^{2}-1}\right)}{\cos\left(\pi\sqrt{4n^{2}-3}\right)}.$$
>
> 分子部分. 把根式写成 2n 与一个小量之和,
>
> $$\sqrt{4n^{2}-1}=2n\sqrt{1-\frac{1}{4n^{2}}}=2n\left(1-\frac{1}{8n^{2}}+O(n^{-4})\right)=2n-\frac{1}{4n}+O(n^{-3}),$$
>
> 于是
>
> $$\pi\sqrt{4n^{2}-1}=2n\pi-\frac{\pi}{4n}+O(n^{-3}).$$
>
> 由 $\cos(2n\pi+\theta)=\cos\theta$ 得
>
> $$\cos\left(\pi\sqrt{4n^{2}-1}\right)=\cos\left(-\frac{\pi}{4n}+O(n^{-3})\right)=1-\frac{\pi^{2}}{32n^{2}}+O(n^{-4}).$$
>
> 分母部分. 同理, 把 -1 换成 -3:
>
> $$\sqrt{4n^{2}-3}=2n-\frac{3}{4n}+O(n^{-3}),\qquad\pi\sqrt{4n^{2}-3}=2n\pi-\frac{3\pi}{4n}+O(n^{-3}),$$
>
> 于是
>
> $$\cos\left(\pi\sqrt{4n^{2}-3}\right)=\cos\frac{3\pi}{4n}+O(n^{-3})=1-\frac{9\pi^{2}}{32n^{2}}+O(n^{-4}).$$
>
> 比值取对数. 由 $\ln(1+u)=u+O(u^{2})(u\to0)$,
>
> $$\ln\cos\bigl(\pi\sqrt{4n^{2}-1}\bigr)=-\frac{\pi^{2}}{32n^{2}}+O\bigl(n^{-4}\bigr),$$
>
> $$\ln\cos\bigl(\pi\sqrt{4n^{2}-3}\bigr)=-\frac{9\pi^{2}}{32n^{2}}+O\bigl(n^{-4}\bigr),$$
>
> 相减得
>
> $$\ln\frac{\cos\left(\pi\sqrt{4n^{2}-1}\right)}{\cos\left(\pi\sqrt{4n^{2}-3}\right)}=\left(-\frac{\pi^{2}}{32n^{2}}\right)-\left(-\frac{9\pi^{2}}{32n^{2}}\right)+O(n^{-4})=\frac{\pi^{2}}{4n^{2}}+O(n^{-4}).$$
>
> 乘 $n^{2}$得最终结果.
>
> $$\ln L=\lim_{n\to\infty}n^{2}\left(\frac{\pi^{2}}{4n^{2}}+O(n^{-4})\right)=\frac{\pi^{2}}{4},$$
>
> 故
>
> $$L=e^{\pi^{2}/4}.$$

**8.** （难度：★★★）

$$\lim_{n\to\infty}\frac{1}{n^{2}\ln n}\sum_{k=1}^{n}k\ln k$$

> [!answer]- 原书参考答案（A.1.1 第 8 题，未逐题独立验算）
> **8.** 第一步: 用积分放缩把 $\sum k \ln k$ 夹住. $f(x) = x \ln x$ 在 $[1, +\infty)$ 上单调递增, 故对 $k \geqslant 1$
>
> $$\int_{k}^{k+1}x\ln x\mathrm{d}x\geqslant k\ln k\geqslant\int_{k-1}^{k}x\ln x\mathrm{d}x,$$
>
> 对 $k=1,\ldots,n$ 求和, 得
>
> $$\int_{0}^{n}x\ln x\mathrm{d}x\leqslant\sum_{k=1}^{n}k\ln k\leqslant\int_{1}^{n+1}x\ln x\mathrm{d}x.$$
>
> 而 $\int x \ln x \, dx = \frac{x^2}{2} \ln x - \frac{x^2}{4}$，故
>
> $$\int_{0}^{n}x\ln x\mathrm{d}x=\frac{n^{2}}{2}\ln n-\frac{n^{2}}{4},\qquad\int_{1}^{n+1}x\ln x\mathrm{d}x=\frac{(n+1)^{2}}{2}\ln(n+1)-\frac{(n+1)^{2}}{4}+\frac{1}{4}.$$
>
> 第二步: 同除 $n^2 \ln n$ 并取极限. 两端都是 $\left[\frac{n^2}{2} \ln n - \frac{n^2}{4} + O(n \ln n)\right]$ 的形状, 于是
>
> $$\frac{1}{2}-\frac{1}{4\ln n}+O\left(\frac{\ln n}{n}\right)\leqslant\frac{1}{n^{2}\ln n}\sum_{k=1}^{n}k\ln k\leqslant\frac{(n+1)^{2}\ln(n+1)}{2n^{2}\ln n}-\frac{(n+1)^{2}}{4n^{2}\ln n}+O\left(\frac{1}{n}\right),$$
>
> 右端第一项因 $\frac{(n+1)^2}{n^2} \to 1$、 $\frac{\ln(n+1)}{\ln n} \to 1$ 而趋于 $\frac{1}{2}$，其余项趋于 0。由夹逼定理
>
> $$\lim_{n\to\infty}\frac{1}{n^{2}\ln n}\sum_{k=1}^{n}k\ln k=\frac{1}{2}.$$

---

# 基础篇·第二章 一元微分学

## 2.1 求导

明确导数定义, 掌握隐函数与参数方程的求导方法即可, 当之无愧的比赛送分题.

**1.** (难度:★) $f(x)=1-\cos x\sqrt{\cos 2x}\sqrt[3]{\cos 3x}\cdots\sqrt[n]{\cos nx}$，求 $f'(x)$.

> [!answer]- 原书参考答案（A.2.1 第 1 题，未逐题独立验算）
> **1.** 第一步：把乘积部分记出来，用对数求导.令
>
> $$P(x)=\cos x\sqrt{\cos2x}\sqrt[3]{\cos3x}\cdots\sqrt[n]{\cos nx}=\prod_{k=1}^{n}(\cos kx)^{\frac{1}{k}},$$
>
> 则 f = 1 - P, 从而 $f' = -P'$. 在 $\cos kx \neq 0$ ( $k = 1, \ldots, n$) 的区间上取对数:
>
> $$\ln P=\sum_{k=1}^{n}\frac{1}{k}\ln\cos kx.$$
>
> 第二步：两边求导.
>
> $$\frac{P^{\prime}}{P}=\sum_{k=1}^{n}\frac{1}{k}\cdot\frac{-k\sin kx}{\cos kx}=-\sum_{k=1}^{n}\tan kx,\qquad 故 \qquad P^{\prime}=-P\sum_{k=1}^{n}\tan kx.$$
>
> 第三步：回代得 $f'$. 由 P = 1 - f,
>
> $$f^{\prime}(x)=P(x)\sum_{k=1}^{n}\tan kx=\left(\prod_{k=1}^{n}\left(\cos kx\right)^{\frac{1}{k}}\right)\sum_{k=1}^{n}\tan kx=\left[1-f(x)\right]\sum_{k=1}^{n}\tan kx.$$
>
> (结论对一切使 $\cos kx \neq 0$ 的 x 成立, 其余点由连续性延拓.)

**2.** （难度：★）设

$$\left\{\begin{aligned}x&=\cos t^{2},\\ y&=2t\cos t^{2}-\int_{1}^{t^{2}}\frac{\cos u}{\sqrt{u}}\mathrm{d}u,\end{aligned}\right.$$

求 $\left.\frac{d^{2}y}{dx^{2}}\right|_{t=\sqrt{\frac{\pi}{2}}}$

> [!answer]- 原书参考答案（A.2.1 第 2 题，未逐题独立验算）
> **2.** 第一步：先求 $\varphi'(t)$ 与 $\psi'(t)$. 对 $x = \cos t^{2}$ 求导:
>
> $$\varphi^{\prime}(t)=-2t\sin t^{2}.$$
>
> 对 y 求导时，前一项用乘积法则，后一项用变限积分求导公式。这里内层函数是 $u(t) = t^{2}$，故 $u'(t) = 2t$；又 $t = \sqrt{\frac{\pi}{2}} > 0$，在它的附近 $\sqrt{t^{2}} = t$，于是
>
> $$\frac{\mathrm{d}}{\mathrm{d}t}\int_{1}^{t^{2}}\frac{\cos u}{\sqrt{u}}\mathrm{d}u=\frac{\cos t^{2}}{\sqrt{t^{2}}}\cdot2t=\frac{\cos t^{2}}{t}\cdot2t=2\cos t^{2}\qquad(t>0).$$
>
> 所以
>
> $$\begin{aligned}\psi^{\prime}(t)&=\left(2t\cos t^{2}\right)^{\prime}-2\cos t^{2}\\&=2\cos t^{2}-4t^{2}\sin t^{2}-2\cos t^{2}\\&=-4t^{2}\sin t^{2}.\end{aligned}$$
>
> 这里 $2\cos t^{2}$ 与积分项求导得到的 $2\cos t^{2}$ 恰好相互抵消，这是本题设计的用意：抵消之后剩下的表达式非常简洁.
>
> 第二步：求一阶导数.
>
> $$\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{\psi^{\prime}(t)}{\varphi^{\prime}(t)}=\frac{-4t^{2}\sin t^{2}}{-2t\sin t^{2}}=2t.$$
>
> 在 $t = \sqrt{\frac{\pi}{2}}$ 处, $\varphi'(t) = -2t \neq 0$, 函数由参数方程确定, 代入得
>
> $$\frac{\mathrm{d}y}{\mathrm{d}x}\bigg|_{t=\sqrt{\pi/2}}=2\sqrt{\frac{\pi}{2}}=\sqrt{2\pi}.$$
>
> 第三步: 求二阶导数. $\frac{dy}{dx}=2t$ 仍是 t 的函数, 把它再对 x 求导, 需要再除以 $\varphi'(t)$:
>
> $$\frac{\mathrm{d}^{2}y}{\mathrm{d}x^{2}}=\frac{1}{\varphi^{\prime}(t)}\cdot\frac{\mathrm{d}}{\mathrm{d}t}(2t)=\frac{2}{-2t\sin t^{2}}=-\frac{1}{t\sin t^{2}}.$$
>
> 在 $t = \sqrt{\frac{\pi}{2}}$ 处, $t^{2} = \frac{\pi}{2}$, $\sin t^{2} = 1$, 故
>
> $$\frac{\mathrm{d}^{2}y}{\mathrm{d}x^{2}}\bigg|_{t=\sqrt{\pi/2}}=-\frac{1}{\sqrt{\pi/2}}=-\sqrt{\frac{2}{\pi}}.$$

**3.** (难度:★) 对于由方程 $\sin xy + \ln(y - x) = x$ 所确定的隐函数, 求 $\frac{d^2y}{dx^2}$.

> [!answer]- 原书参考答案（A.2.1 第 3 题，未逐题独立验算）
> **3.** 记 u = y - x、c = $\cos xy$、s = $\sin xy$.
>
> 第一步: 两边对 x 求导, 得一阶关系. 由 $(\sin xy)' = c(y + xy')$、 $(\ln u)' = \frac{u’}{u} = \frac{y’ - 1}{u}$,
>
> $$c\left(y+x y^{\prime}\right)+\frac{y^{\prime}-1}{u}=1.$$
>
> 把含 $y'$ 的项并在一起:
>
> $$y^{\prime}\left(x c+\frac{1}{u}\right)=1-y c+\frac{1}{u},\qquad 即 \qquad\boxed{y^{\prime}=\frac{u+1-u y c}{x u c+1}}\qquad\left(u=y-x\right).$$
>
> 第二步: 再对 x 求导. 对 (1) 求导, 其中 $c' = -s(y + xy')$, $u' = y' - 1$:
>
> $$-s\left(y+x y^{\prime}\right)^{2}+2c y^{\prime}+c x y^{\prime\prime}+\frac{y^{\prime\prime}u-\left(y^{\prime}-1\right)^{2}}{u^{2}}=0,$$
>
> 于是
>
> $$\left|y^{\prime\prime}=\frac{u}{x u c+1}\left[s\left(y+x y^{\prime}\right)^{2}-2c y^{\prime}+\frac{\left(y^{\prime}-1\right)^{2}}{u^{2}}\right]\right|$$
>
> (其中 u = y - x, c = $\cos xy$, s = $\sin xy$, $y'$ 用第一步的结果代入即可).

## 2.2 高阶导数

高阶导数相关的题目一般出现在填空，一般有泰勒展开或莱布尼茨求导法则两大做题思路。要注意区分任意点高阶导数、不含参固定点高阶导数与含参固定点高阶导数的区别，选取合适的方法进行求解。

**1.** (难度:★★) $y = \frac{1}{x^{2} + 5x + 6}$，求 $y^{(n)}$

> [!answer]- 原书参考答案（A.2.2 第 1 题，未逐题独立验算）
> **1.** 第一步：先裂项，化成两个幂函数的和.
>
> $$y=\frac{1}{x^{2}+5x+6}=\frac{1}{(x+2)(x+3)}=\frac{1}{x+2}-\frac{1}{x+3}.$$
>
> 第二步:逐项用公式 $\left(\frac{1}{x+a}\right)^{(n)}=\frac{(-1)^{n}n!}{(x+a)^{n+1}}$.
>
> $$y^{(n)}(x)=(-1)^{n}n!\left[\frac{1}{(x+2)^{n+1}}-\frac{1}{(x+3)^{n+1}}\right]=\frac{(-1)^{n}n!\left[(x+3)^{n+1}-(x+2)^{n+1}\right]}{(x+2)^{n+1}(x+3)^{n+1}}.$$
>
> （这一步是「有理分式求 n 阶导」的通法：先裂项成若干个 $\frac{A}{x+a}$，再套上面的公式。）

**2.** (难度: ★★★★) $y = \arcsin x \arccos x$，求 $y^{(n)}(0)$.

> [!answer]- 原书参考答案（A.2.2 第 2 题，未逐题独立验算）
> **2.** 设 $u = \arcsin x$、 $v = \arccos x$，则 $u + v = \frac{\pi}{2}$ 且 $v' = -u'$。利用这个对称关系，可以给 $y = uv$ 找出一个简洁的微分恒等式，再对它用莱布尼茨公式建立递推。第一步：找出 y 满足的恒等式。记 $u = \arcsin x$， $v = \arccos x$，则
>
> $$u+v=\frac{\pi}{2},\qquad u^{\prime}=\frac{1}{\sqrt{1-x^{2}}},\qquad v^{\prime}=-u^{\prime}.$$
>
> 对 y = uv 求导:
>
> $$y^{\prime}=u^{\prime}v+u v^{\prime}=u^{\prime}(v-u)=u^{\prime}\left(\frac{\pi}{2}-2u\right).$$
>
> 两边乘以 $u'$，并利用 $(u')^{2}=\frac{1}{1-x^{2}}$:
>
> $$y^{\prime}\cdot u^{\prime}=(u^{\prime})^{2}\left(\frac{\pi}{2}-2u\right)=\frac{1}{1-x^{2}}\left(\frac{\pi}{2}-2u\right).$$
>
> 又 $u^{\prime}\left(\frac{\pi}{2}-2u\right)=y^{\prime}$，故上式变为
>
> $$y^{\prime}=\frac{1}{1-x^{2}}\left(\frac{\pi}{2}-2u\right)\quad\Longrightarrow\quad(1-x^{2})y^{\prime}=\frac{\pi}{2}-2u.$$
>
> 两边再对 x 求导. 左边用乘积法则, 右边用 $u' = \frac{1}{\sqrt{1 - x^2}}$:
>
> $$-2xy^{\prime}+(1-x^{2})y^{\prime\prime}=-\frac{2}{\sqrt{1-x^{2}}}.$$
>
> 再把右边与 $y'$ 联系起来. 由 $y' = u' \left( \frac{\pi}{2} - 2u \right)$ 及 $u' = \frac{1}{\sqrt{1 - x^{2}}}$, 不能直接消; 换一条路径: 对 $(1 - x^{2})y' = \frac{\pi}{2} - 2u$ 直接求导得
>
> $$-2xy^{\prime}+(1-x^{2})y^{\prime\prime}=-2u^{\prime}=-\frac{2}{\sqrt{1-x^{2}}}.$$
>
> 比较两个思路不如直接再求导一次求恒等式更清爽. 对 $y' = u'\left(\frac{\pi}{2} - 2u\right)$ 两边再求导:
>
> $$y^{\prime\prime}=u^{\prime\prime}\left(\frac{\pi}{2}-2u\right)-2(u^{\prime})^{2}=\frac{x}{(1-x^{2})^{3/2}}\cdot\frac{y^{\prime}}{u^{\prime}}-\frac{2}{1-x^{2}}.$$
>
> 整理得
>
> $$(1-x^{2})y^{\prime\prime}-x y^{\prime}+2=0.$$
>
> （校验：x=0 时 $y(0)=0, y'(0)=\frac{\pi}{2}, y''(0)=-2$ ，代入得 $1\cdot(-2)-0+2=0$ ，成立.）
>
> 第二步：用莱布尼茨公式对(1)求n阶导数.对
>
> $$(1-x^{2})y^{\prime\prime}-x y^{\prime}+2=0$$
>
> 两边求 n 阶导数. $(1 - x^{2})y^{\prime\prime}$ 用莱布尼茨, $1 - x^{2}$ 只贡献 k = 0, 1, 2 三项:
>
> $$(1-x^{2})y^{(n+2)}-2n x y^{(n+1)}-n(n-1)y^{(n)}.$$
>
> $xy'$ 用莱布尼茨, x 只贡献 k = 0, 1 两项:
>
> $$xy^{(n+1)}+ny^{(n)}.$$
>
> 常数2求n阶导数 $(n\geqslant1)$为0.合并：
>
> $$(1-x^{2})y^{(n+2)}-(2n+1)x y^{(n+1)}-n^{2}y^{(n)}=0.$$
>
> 令x=0，即得递推关系
>
> $$y^{(n+2)}(0)=n^{2}y^{(n)}(0)\qquad(n\geqslant1).$$
>
> 第三步：用初值求通项.由
>
> $$y(0)=\arcsin0\cdot\arccos0=0,\qquad y^{\prime}(0)=\frac{\arccos0-\arcsin0}{\sqrt{1-0}}=\frac{\pi}{2},$$
>
> 以及递推式(2):
>
> 偶数阶：由 $y(0)=0$ 及 $y^{(n+2)}(0)=n^{2}y^{(n)}(0)$，得 $y''(0)=1^{2}y(0)=0, y^{(4)}(0)=3^{2}y''(0)=0$，……归纳得 $y^{(2m)}(0)=0(m \geqslant 0)$.
>
> 奇数阶：由 $y'(0) = \frac{\pi}{2}$，得 $y'''(0) = 1^2 y'(0) = \frac{\pi}{2}$， $y^{(5)}(0) = 3^2 y'''(0) = \frac{9\pi}{2}$，
>
> $$y^{(7)}(0)=5^{2}y^{(5)}(0)=\frac{225\pi}{2},\cdots\cdots 归纳得$$
>
> $$y^{(2m+1)}(0)=\frac{\pi}{2}\left[(2m-1)!!\right]^{2}\qquad(m\geqslant0).$$
>
> 故
>
> $$y^{(2m)}(0)=0,\qquad y^{(2m+1)}(0)=\frac{\pi}{2}\left[(2m-1)!!\right]^{2}\quad(m\geqslant0).$$
>
> 这道题的突破口是给 $y = \arcsin x \arccos x$ 找出一个简洁的微分恒等式 $(1 - x^2)y'' - xy' + 2 = 0$，再对它套莱布尼茨公式得到递推式 $y^{(n+2)}(0) = n^2y^{(n)}(0)$。有了递推式，剩下的只是代入初值 $y(0) = 0$、 $y'(0) = \frac{\pi}{2}$ 逐项推出通项。相比之下，用 $\arcsin x$ 的已知高阶导数公式再对 $(\arcsin x)^2$ 做求和的方法虽也能得出结果，但远不如莱布尼茨递推干净。

**3.** (难度:★★) $f(x)=(x+1)^{n}e^{-x^{2}}$，求 $f^{(n)}(-1)$.

> [!answer]- 原书参考答案（A.2.2 第 3 题，未逐题独立验算）
> **3.** 第一步：用莱布尼茨公式. 令 $u = (x + 1)^{n}$、 $v = e^{-x^{2}}$，则
>
> $$f^{(n)}(x)=\sum_{k=0}^{n}C_{n}^{k}u^{(k)}(x)v^{(n-k)}(x).$$
>
> 第二步：在 x = -1 处只有一项存活. $u = (x + 1)^{n}$ 在 x = -1 处有 n 阶零点：
>
> $$u^{(k)}(x)=\frac{n!}{(n-k)!}(x+1)^{n-k},\qquad 当 k<n 时 u^{(k)}(-1)=0,\qquad u^{(n)}(-1)=n!.$$
>
> 所以求和式在 x = -1 处只剩 k = n 这一项：
>
> $$f^{(n)}(-1)=C_{n}^{n}u^{(n)}(-1)v(-1)=n!\cdot\mathrm{e}^{-1}=\frac{n!}{\mathrm{e}}.$$
>
> （含参固定点的高阶导数，关键是先看有没有现成的「零因子」把莱布尼茨展开截断。）

**4.** (难度:★★) $f(x)=\frac{(\sqrt[n]{x}-1)^{n}}{x+1}$，求 $f^{(n)}(1)$.

> [!answer]- 原书参考答案（A.2.2 第 4 题，未逐题独立验算）
> **4.** 函数中没有现成的 $(x-1)^{n}$，需要主动把零因子凑出来.
>
> 第一步: 换元, 把根号化成整数次幂. 令 $t = \sqrt[n]{x}$, 则 $x = t^n$, 于是
>
> $$x-1=t^{n}-1=\left(t-1\right)\left(t^{n-1}+t^{n-2}+\cdots+t+1\right),$$
>
> 从而
>
> $$t-1=\frac{x-1}{1+t+t^{2}+\cdots+t^{n-1}}.$$
>
> 于是
>
> $$\left(\sqrt[n]{x}-1\right)^{n}=(t-1)^{n}=\frac{(x-1)^{n}}{(1+t+t^{2}+\cdots+t^{n-1})^{n}}.$$
>
> 第二步: 写成 $g(x)(x-1)^{n}$ 的形式. 把上式代回 $f(x)$:
>
> $$f(x)=\frac{(x-1)^{n}}{(1+t+t^{2}+\cdots+t^{n-1})^{n}(x+1)}=(x-1)^{n}g(x),$$
>
> 其中
>
> $$g(x)=\frac{1}{\left(1+t+t^{2}+\cdots+t^{n-1}\right)^{n}(x+1)},\qquad t=\sqrt[n]{x}.$$
>
> 第三步：求 $g(1)$ 并套公式. 当 x=1 时 t=1 ，故
>
> $$g(1)=\frac{1}{n^{n}\cdot2}=\frac{1}{2n^{n}},$$
>
> 而 $g(x)$ 在 x=1 附近有定义且可导 (x>0 时 $t=\sqrt[n]{x}$ 光滑)，因此
>
> $$f^{(n)}(1)=n!g(1)=\frac{n!}{2n^{n}}.$$
>
> 校验. 取 n=1 , 则 $f(x)=\frac{x-1}{x+1}$
>
> $$f^{\prime}(1)=\left.\frac{(x+1)-(x-1)}{(x+1)^{2}}\right|_{x=1}=\frac{2}{4}=\frac{1}{2},$$
>
> 与 $\frac{1!}{2\cdot1^1} = \frac{1}{2}$ 一致.

**5.** (难度:★★★★★) $f(x)=(1+\sqrt{x})^{2n+2}$，求 $f^{(n)}(1)$.

> [!answer]- 原书参考答案（A.2.2 第 5 题，未逐题独立验算）
> **5.** 第一步：引入对偶式，并证明它的 n 阶导数为 0.
>
> 令
>
> $$z=(1-\sqrt{x})^{2n+2}.$$
>
> 在 x=1 附近作有理化: 由 $(1-\sqrt{x})(1+\sqrt{x})=1-x$ 得
>
> $$1-\sqrt{x}=\frac{1-x}{1+\sqrt{x}}.$$
>
> 于是
>
> $$z=\frac{(1-x)^{2n+2}}{(1+\sqrt{x})^{2n+2}}=(1-x)^{2n+2}h(x),\qquad h(x)=\frac{1}{(1+\sqrt{x})^{2n+2}}.$$
>
> 由于 x=1 处 $\sqrt{x}$ 光滑, h 在 x=1 附近任意阶可导.
>
> 由莱布尼茨公式，
>
> $$z^{(n)}(1)=\sum_{k=0}^{n}C_{n}^{k}\left[(1-x)^{2n+2}\right]^{(k)}\Big|_{x=1}\cdot h^{(n-k)}(1).$$
>
> 对 $0 \leqslant k \leqslant n < 2n + 2$， $\left[(1 - x)^{2n + 2}\right]^{(k)}$ 中仍含因子 $(1 - x)^{2n + 2 - k}$，在 x = 1 处取值为 0。故上式每一项都是 0，即
>
> $$z^{(n)}(1)=0.$$
>
> 第二步: 计算 $(y+z)^{(n)}(1)$.
>
> 由二项式定理，奇次项两两抵消：
>
> $$y+z=(1+\sqrt{x})^{2n+2}+(1-\sqrt{x})^{2n+2}=2\sum_{j=0}^{n+1}C_{2n+2}^{2j}x^{j}.$$
>
> 记 $a_{j}=C_{2n+2}^{2j}$，上式是一个最高次为 $x^{n+1}$ 的多项式。其 n 阶导数为
>
> $$(y+z)^{(n)}(x)=2\sum_{j=n}^{n+1}a_{j}\frac{j!}{(j-n)!}x^{j-n}.$$
>
> 代入 x=1:
>
> $$\begin{aligned}(y+z)^{(n)}(1)&=2a_{n}n!+2a_{n+1}(n+1)!\\&=2\mathrm{C}_{2n+2}^{2n}n!+2\mathrm{C}_{2n+2}^{2n+2}(n+1)!\\&=(2n+2)(2n+1)n!+2(n+1)!.\\ \end{aligned}$$
>
> 提出 n! 并化简：
>
> $$\begin{aligned}(y+z)^{(n)}(1)&=n![(2n+2)(2n+1)+2(n+1)]\\&=n!\cdot2(n+1)\left[(2n+1)+1\right]\\&=4(n+1)^{2}n!.\end{aligned}$$
>
> 第三步：合并得 $y^{(n)}(1)$.
>
> 由 $y=(y+z)-z$ ，两边求 n 阶导数并代入 x=1:
>
> $$y^{(n)}(1)=(y+z)^{(n)}(1)-z^{(n)}(1)=4(n+1)^{2}n!-0=4(n+1)^{2}n!.$$
>
> 校验. 取 n = 1, 则 $y = (1 + \sqrt{x})^{4}$,
>
> $$y^{\prime}=4(1+\sqrt{x})^{3}\cdot\frac{1}{2\sqrt{x}}=\frac{2(1+\sqrt{x})^{3}}{\sqrt{x}},$$
>
> 故 $y'(1) = 2 \cdot 2^3 = 16$，与 $4 \cdot 2^2 \cdot 1! = 16$ 一致.

**6.** (难度: ★★★) $f(x) = \ln(1 + e^{\sin x})$，求 $f^{(2n-1)}(0)$.

> [!answer]- 原书参考答案（A.2.2 第 6 题，未逐题独立验算）
> **6.** 先说明为什么不能直接展开. $\ln\left(1+e^{\sin x}\right)$ 是「对数 + 指数 + 正弦」的三层复合, 要展开到 2n-1 阶, 计算量巨大且系数没有明显规律. 此时应当考虑函数本身具有的性质.
>
> 第一步:算 $f(x) - f(-x)$.
>
> $$f(x)-f(-x)=\ln\left(1+e^{\sin x}\right)-\ln\left(1+e^{-\sin x}\right)=\ln\frac{1+e^{\sin x}}{1+e^{-\sin x}}.$$
>
> 分子分母同时乘以 $e^{\sin x}$:
>
> $$\frac{1+e^{\sin x}}{1+e^{-\sin x}}=\frac{e^{\sin x}\left(1+e^{\sin x}\right)}{e^{\sin x}+1}=e^{\sin x},$$
>
> 所以
>
> $$f(x)-f(-x)=\ln e^{\sin x}=\sin x.$$
>
> 这个结果非常干净: $f(x) - f(-x)$ 竟然就是一个正弦函数.
>
> **第二步：把 $f(x)$ 拆成偶部与奇部. 记**
>
> $$E(x)=\frac{f(x)+f(-x)}{2}\left( 偶函数 \right),\qquad O(x)=\frac{f(x)-f(-x)}{2}=\frac{\sin x}{2}\left( 奇函数 \right),$$
>
> 则 $f(x)=E(x)+O(x)$. 由偶函数的奇数阶导数在 0 处为 0,
>
> $$f^{(2n-1)}(0)=E^{(2n-1)}(0)+O^{(2n-1)}(0)=O^{(2n-1)}(0).$$
>
> 第三步：求奇部的奇数阶导数. 由 $(\sin x)^{(m)} = \sin\left(x + \frac{m\pi}{2}\right)$,
>
> $$O^{(2n-1)}(0)=\frac{1}{2}\sin\left(\frac{(2n-1)\pi}{2}\right)=\frac{(-1)^{n-1}}{2},$$
>
> 故
>
> $$f^{(2n-1)}(0)=\frac{(-1)^{n-1}}{2}.$$
>
> (校验: n = 1 时 $f'(x) = \frac{e^{\sin x} \cos x}{1 + e^{\sin x}}$, 故 $f'(0) = \frac{1 \cdot 1}{2} = \frac{1}{2}$, 与公式一致.)

## 2.3 （不）等式证明

此块考题与高中内容紧密结合, 完全取决于高中的导数学习水平如何, 故不必赘述.

题目整体略有难度, 但都是常见的函数问题讨论.

**1.** 探讨下列等式是否成立, 若成立, 给出对应证明; 若不成立, 给出要使等式成立时 x, y 所满足的条件.

(1) (难度：★) $\arcsin \sqrt{x} + \arcsin \sqrt{1 - x} = \frac{\pi}{2}$.

(2) (难度: ★) $2 \arctan x + \arcsin \frac{2x}{1 + x^{2}} = \pi$.

(3) (难度:★★) $\arctan x + \arctan y = \arctan \left( \frac{x + y}{1 - xy} \right)$.

> [!answer]- 原书参考答案（A.2.3 第 1 题，未逐题独立验算）
> **1.** (1) 第一步: 两边都是常数的形式, 用「求导后为常数」来做. 令
>
> $$F(x)=\arcsin\sqrt{x}+\arcsin\sqrt{1-x}\qquad(0<x<1).$$
>
> 由 $(\arcsin t)^{\prime}=\frac{1}{\sqrt{1-t^{2}}}$
>
> $$F^{\prime}(x)=\frac{1}{\sqrt{1-x}}\cdot\frac{1}{2\sqrt{x}}+\frac{1}{\sqrt{1-(1-x)}}\cdot\frac{-1}{2\sqrt{1-x}}=\frac{1}{2\sqrt{x(1-x)}}-\frac{1}{2\sqrt{x(1-x)}}=0.$$
>
> 第二步: 代一个方便的点定出常数. 取 $x = \frac{1}{2}$,
>
> $$F\left(\frac{1}{2}\right)=\arcsin\frac{\sqrt{2}}{2}+\arcsin\frac{\sqrt{2}}{2}=\frac{\pi}{4}+\frac{\pi}{4}=\frac{\pi}{2}.$$
>
> 故对一切 $x \in (0,1)$ 都有 $F(x) = \frac{\pi}{2}$;
>
> 第三步：补上端点. 两边取极限得 x=0 与 x=1 时也成立 $(0+\frac{\pi}{2}=\frac{\pi}{2},\frac{\pi}{2}+0=\frac{\pi}{2})$. 所以等式在 **整个 $[0,1]$ 上** 成立. (2) 等式右端是常数, 而左端是 x 的函数, 自然应当证明左端为常数, 再代一个方便的点定出这个常数.
>
> 第一步：在x>1上求导.设
>
> $$F(x)=2\arctan x+\arcsin\frac{2x}{1+x^{2}}\qquad(x>1),$$
>
> 记 $t=\frac{2x}{1+x^{2}}$，则
>
> $$t^{\prime}=\frac{2\left(1+x^{2}\right)-4x^{2}}{\left(1+x^{2}\right)^{2}}=\frac{2\left(1-x^{2}\right)}{\left(1+x^{2}\right)^{2}},\qquad1-t^{2}=\frac{\left(x^{2}-1\right)^{2}}{\left(1+x^{2}\right)^{2}}.$$
>
> 因为 x > 1，所以 $\sqrt{1 - t^{2}} = \frac{x^{2} - 1}{1 + x^{2}}$，于是
>
> $$\begin{aligned}F^{\prime}(x)&=\frac{2}{1+x^{2}}+\frac{1}{\sqrt{1-t^{2}}}\cdot t^{\prime}\\&=\frac{2}{1+x^{2}}+\frac{1+x^{2}}{x^{2}-1}\cdot\frac{2\left(1-x^{2}\right)}{\left(1+x^{2}\right)^{2}}\\&=\frac{2}{1+x^{2}}-\frac{2}{1+x^{2}}=0.\\ \end{aligned}$$
>
> 故 $F(x)$ 在 $(1,+\infty)$ 上为常数.
>
> 第二步: 用连续性把 x = 1 补上. 两个反三角函数都在 x = 1 处连续, 故 $F(x)$ 在 x = 1 处连续; 而
>
> $$F(1)=2\arctan1+\arcsin\frac{2}{2}=2\cdot\frac{\pi}{4}+\frac{\pi}{2}=\pi.$$
>
> 于是对任意 x > 1，在 $(1, +\infty)$ 上取极限即得
>
> $$F(x)=\lim_{s\to1^{+}}F(s)=F(1)=\pi.$$
>
> 又 x=1 时原式显然成立，故 $x \geqslant 1$ 时恒有 $F(x)=\pi$，等式得证。(3) 结论：当且仅当 xy<1 时等式成立；若 xy>1，两端相差 $\pm\pi$.
>
> 第一步：把左右之差看成二元函数. 在 $1 - xy \neq 0$ (即 $xy \neq 1$) 处令
>
> $$F(x,y)=\arctan x+\arctan y-\arctan\frac{x+y}{1-xy}.$$
>
> 把 y 暂时固定，对 x 求偏导（记 $t = \frac{x + y}{1 - xy}$，则 $t_{x} = \frac{1 + y^{2}}{(1 - xy)^{2}}$）：
>
> $$F_{x}=\frac{1}{1+x^{2}}-\frac{1}{1+t^{2}}\cdot\frac{1+y^{2}}{(1-xy)^{2}}.$$
>
> 由 $(1+x^{2})(1+y^{2})=(1-xy)^{2}+(x+y)^{2}$与 $1+t^{2}=\frac{(1-xy)^{2}+(x+y)^{2}}{(1-xy)^{2}}$，直接化为
>
> $$F_{x}=\frac{1}{1+x^{2}}-\frac{1}{1+x^{2}}=0.$$
>
> 第二步: 区域 xy < 1 是连通的, 且在其上 $F \equiv 0$. 在 xy < 1 上 F 对 x、y 的偏导都为 0, 故 F 为常数; 取 $(x, y) = (0, 0)$ 得 F = 0. 所以
>
> $$\arctan x+\arctan y=\arctan\frac{x+y}{1-xy}\qquad(xy<1).$$
>
> 第三步: $xy > 1$ 时相差 $\pm\pi$. 若 $x, y > 0$ 且 $xy > 1$, 则 $\arctan x + \arctan y \in \left(\frac{\pi}{2}, \pi\right)$,
>
> 而 $\arctan \frac{x+y}{1-xy} \in \left(-\frac{\pi}{2}, 0\right)$, 故左端 = 右端 $+\pi$; 若 $x, y < 0$ 且 $xy > 1$, 左端 = 右端 $-\pi$. $(xy = 1$ 时右端无意义. )

**2.** 证明下列不等式：

(1) (难度: ★) $\arctan x + \frac{1}{x} > \frac{\pi}{2}$ (x > 0).

(2) (难度: ★★★★) $a^{b} + b^{a} \leqslant \sqrt{a} + \sqrt{b} \leqslant a^{a} + b^{b} \quad (a > 0, b > 0, a + b = 1)$

(3) (难度: ★★★) $\frac{4}{\pi^{2}} < \frac{1}{x^{2}} - \frac{1}{\tan^{2}x} < \frac{2}{3}$ $(0 < x < \frac{\pi}{2})$.

(4) (难度:★★★) $\sqrt{x} + \sqrt{x + 27} + \sqrt{13 - x} \leqslant 11$ (0 $\leqslant x \leqslant 13$).

(5) (难度: ★★★★) $\left(\frac{2x+2}{2x+1}\right)^{\sqrt{x+1}} > \left(\frac{2x+1}{2x}\right)^{\sqrt{x}}$ (x > 0).

> [!answer]- 原书参考答案（A.2.3 第 2 题，未逐题独立验算）
> **2.** (1) 令 $f(x) = \arctan x + \frac{1}{x} - \frac{\pi}{2} (x > 0)$.
>
> 第一步：求导判单调.
>
> $$f^{\prime}(x)=\frac{1}{1+x^{2}}-\frac{1}{x^{2}}=\frac{x^{2}-\left(1+x^{2}\right)}{x^{2}\left(1+x^{2}\right)}=-\frac{1}{x^{2}\left(1+x^{2}\right)}<0,$$
>
> 故 f 在 $(0,+\infty)$ 上**严格递减**.
>
> 第二步: 看无穷远处的极限. 由 $\arctan x \to \frac{\pi}{2}$、 $\frac{1}{x} \to 0$,
>
> $$\lim_{x\to+\infty}f(x)=\frac{\pi}{2}+0-\frac{\pi}{2}=0.$$
>
> 第三步：由递减性得不等式. 对任意 x > 0，因为 f 严格递减且以 0 为 +∞ 处的极限，故
>
> $$f(x)>0,\qquad 即 \qquad\arctan x+\frac{1}{x}>\frac{\pi}{2}.$$
>
> (2) 第一步: 把不等式写成同一个函数的三处函数值. 两个不等式在交换 a, b 后都不变, 故不妨设
>
> $$a<b,\qquad 即 \qquad0<a<\frac{1}{2}<b<1.$$
>
> （若 $a = b = \frac{1}{2}$，两个不等号都取等号，结论显然。）由 a + b = 1 得 b = 1 - a, a = 1 - b。作函数
>
> $$f(x)=a^{x}+b^{1-x}\qquad(a\leqslant x\leqslant b),$$
>
> 则三个关键点处的函数值分别是
>
> $$f(a)=a^{a}+b^{1-a}=a^{a}+b^{b},$$
>
> $$f\left(\frac{1}{2}\right)=\sqrt{a}+\sqrt{b},$$
>
> $$f(b)=a^{b}+b^{1-b}=a^{b}+b^{a}.$$
>
> 于是原不等式等价于
>
> $$f(b)\leqslant f\left(\frac{1}{2}\right)\leqslant f(a).$$
>
> 两个变量、两个不等式的问题,至此变成了一个函数在区间上的单调性问题.
>
> 第二步： $f'$ 单调，于是只需看端点的符号.
>
> $$f^{\prime}(x)=a^{x}\ln a-b^{1-x}\ln b,$$
>
> $$f^{\prime\prime}(x)=a^{x}\ln^{2}a+b^{1-x}\ln^{2}b>0.$$
>
> 故 $f^{\prime}$ 在 $[a,b]$ 上严格递增. 既然 $f^{\prime}$ 递增, 只要它在右端点处为负, 它在整个区间上就都为负:
>
> $$f^{\prime}(x)\leqslant f^{\prime}(b)<0\qquad(a\leqslant x\leqslant b),$$
>
> 于是 $f(x)$ 在 $[a,b]$ 上严格递减，从而
>
> $$f(a)>f\left(\frac{1}{2}\right)>f(b),$$
>
> 两个不等式同时成立. 问题于是归结为判断 $f'(b)$ 的符号.
>
> 第三步：算 $f'(b)$，把它化归为一个纯对数的不等式.
>
> $$f^{\prime}(b)=a^{b}\ln a-b^{a}\ln b=-\left(a^{b}\ln\frac{1}{a}-b^{a}\ln\frac{1}{b}\right).$$
>
> 因此证 $f'(b) < 0$ 等价于证
>
> $$a^{b}\ln\frac{1}{a}>b^{a}\ln\frac{1}{b}.$$
>
> 记
>
> $$u=\ln\frac{1}{a},\qquad v=\ln\frac{1}{b}\qquad(u>v>0),$$
>
> 则 $a = e^{-u}$, $b=e^{-v}$. 利用 b = 1 - a 与 a = 1 - b, 可以把两个幂指式「压」成同一个形状:
>
> $$a^{b}=e^{-bu}=e^{-u(1-a)}=e^{-u}e^{au}=a e^{au},$$
>
> 同理 $b^{a}=be^{bv}$. 于是
>
> $$a^{b}\ln\frac{1}{a}=(a u)e^{a u},\qquad b^{a}\ln\frac{1}{b}=(b v)e^{b v},$$
>
> 其中 au 表示乘积 $a \ln \frac{1}{a}$, bv 同理. 函数 $z \mapsto ze^{z}$ 在 $(0, +\infty)$ 上严格递增, 所以上面的不等式等价于
>
> $$a u>b v,\qquad 即 \qquad a\ln\frac{1}{a}>b\ln\frac{1}{b}\qquad 即 \qquad a\ln a<b\ln b.$$
>
> 这样，「端点处的导数为负」最终只依赖于一个关于 $\ln$ 的初等不等式.
>
> 第四步: 证明这个对数不等式 (极值点偏移). 断言: 当 $0 < t < \frac{1}{2}$ 时,
>
> $$t\ln t<(1-t)\ln(1-t).$$
>
> 证明如下. 令
>
> $$V(t)=t\ln t-\left(1-t\right)\ln(1-t),$$
>
> 则
>
> $$V^{\prime}(t)=\ln t+1+\ln(1-t)+1=\ln\left[t(1-t)\right]+2.$$
>
> 在 $\left(0,\frac{1}{2}\right)$上， $t(1-t)$从0严格递增到 $\frac{1}{4}$，故 $\ln[t(1-t)]$也严格递增，即 $V'$在 $\left(0,\frac{1}{2}\right)$上严格递增.又
>
> $$V^{\prime}(0+)=-\infty,\qquad V^{\prime}\left(\frac{1}{2}\right)=2-\ln4=2(1-\ln2)>0,$$
>
> 所以存在唯一的 $t_{0}\in\left(0,\frac{1}{2}\right)$，使 $V^{\prime}<0$ 于 $(0,t_{0})$、 $V^{\prime}>0$ 于 $\left(t_{0},\frac{1}{2}\right)$. 于是 V 在 $(0,t_{0})$ 上严格递减、在 $\left(t_{0},\frac{1}{2}\right)$ 上严格递增. 而
>
> $$V(0+)=0,\qquad V\left(\frac{1}{2}\right)=0,$$
>
> 故 V 在前一段上由 0 递减、在后一段上递增到 0，两段上都为负，即
>
> $$V(t)<0\qquad\left(0<t<\frac{1}{2}\right).$$
>
> 回到本题. 第一步已设 a < b，故 $a < \frac{1}{2}$. 在上述断言中取 t = a，得
>
> $$a\ln a<b\ln b,$$
>
> 这正是第三步所需的 $au > bv$. 于是
>
> $$f^{\prime}(b)=-\left(a^{b}\ln\frac{1}{a}-b^{a}\ln\frac{1}{b}\right)<0.$$
>
> 由第二步， $f'(x) < 0$ 在整个 $[a, b]$ 上成立，故 $f(x)$ 严格递减：
>
> $$f(a)>f\left(\frac{1}{2}\right)>f(b),$$
>
> 即
>
> $$a^{a}+b^{b}>\sqrt{a}+\sqrt{b}>a^{b}+b^{a}.$$
>
> 当 a = b = $\frac{1}{2}$ 时两端都等于 $\sqrt{2}$，不等式取等号。综上，原命题得证。（3）直接对 $F(x) = \frac{1}{x^{2}} - \frac{1}{\tan^{2}x}$ 求导，化简后把 x 单独分离为一个一次因子，令其系数为新函数 $u(x) = \frac{\sin x}{\cos^{1/3}x}$。只要证明 $u(x) > x$（直接做差求导即可），就能判定 $F' < 0$，从而 $F(x)$ 在 $\left(0, \frac{\pi}{2}\right)$ 上严格递减，再用两端极限夹住即得双边界不等式。第一步：求导并化简。令
>
> $$F(x)=\frac{1}{x^{2}}-\frac{1}{\tan^{2}x}=\frac{1}{x^{2}}-\cot^{2}x,\qquad0<x<\frac{\pi}{2}.$$
>
> 求导：
>
> $$F^{\prime}(x)=-\frac{2}{x^{3}}+2\cot x\csc^{2}x=-\frac{2}{x^{3}}+\frac{2\cos x}{\sin^{3}x}.$$
>
> 通分，把x从分母里分离出来：
>
> $$F^{\prime}(x)=\frac{2}{x^{3}\sin^{3}x}\left(x^{3}\cos x-\sin^{3}x\right).$$
>
> 分母 $x^{3}\sin^{3}x>0$ ，故 $F'(x)$ 的符号由分子决定. 把分子写成
>
> $$x^{3}\cos x-\sin^{3}x=\cos x\left(x^{3}-\frac{\sin^{3}x}{\cos x}\right)=\cos x\left[x^{3}-u(x)^{3}\right],$$
>
> 其中
>
> $$u(x)=\frac{\sin x}{\cos^{1/3}x}.$$
>
> 由 $\cos x > 0$ ( $0 < x < \frac{\pi}{2}$)， $F'(x)$ 的符号完全等价于 $x^{3} - u(x)^{3}$ 的符号，即只需证明 $u(x) > x$.
>
> 第二步: 做差求导证明 $u(x) > x$. 令
>
> $$g(x)=u(x)-x=\frac{\sin x}{\cos^{1/3}x}-x,\qquad0<x<\frac{\pi}{2}.$$
>
> 显然 $g(0)=0$ 对 u 求导:
>
> $$\begin{aligned}u^{\prime}(x)&=\frac{\mathrm{d}}{\mathrm{d}x}\left[\sin x\cdot\cos^{-1/3}x\right]\\&=\cos x\cdot\cos^{-1/3}x+\sin x\cdot\frac{1}{3}\cos^{-4/3}x\cdot\sin x\\&=\cos^{2/3}x+\frac{\sin^{2}x}{3\cos^{4/3}x}\\&=\frac{3\cos^{2}x+\sin^{2}x}{3\cos^{4/3}x}=\frac{1+2\cos^{2}x}{3\cos^{4/3}x}.\\ \end{aligned}$$
>
> 于是
>
> $$g^{\prime}(x)=u^{\prime}(x)-1=\frac{1+2\cos^{2}x-3\cos^{4/3}x}{3\cos^{4/3}x}.$$
>
> 记 $c = \cos x \in (0,1)$，则 $g'(x)$ 的符号由分子 $1 + 2c^2 - 3c^{4/3}$ 决定。令 $t = c^{2/3} \in (0,1)$，则 $c^2 = t^3$， $c^{4/3} = t^2$，故
>
> $$1+2c^{2}-3c^{4/3}=1+2t^{3}-3t^{2}=(t-1)^{2}(2t+1)>0.$$
>
> （最后一步用到 $t \neq 1$ ，故 $(t-1)^{2} > 0$ ，且 $2t+1 > 0$ ）
>
> 所以 $g'(x)>0$在 $\left(0,\frac{\pi}{2}\right)$上成立，即 $g(x)$严格递增。由 $g(0)=0$，得 $g(x)>0$，即
>
> $$u(x)>x,\qquad 从而 \qquad u(x)^{3}>x^{3},\qquad x^{3}-u(x)^{3}<0.$$
>
> 由 $F'(x)=\frac{2\cos x}{x^{3}\sin^{3}x}(x^{3}-u(x)^{3})<0$ , 得 $F(x)$ 在 $\left(0,\frac{\pi}{2}\right)$ 上严格递减.
>
> 第三步：求两端极限.
>
> 右端 $(x \to 0^{+})$：由 $\frac{1}{\tan^{2}x} = \frac{1}{x^{2}} - \frac{2}{3} + O(x^{2})$（可由 $\tan x = x + \frac{x^{3}}{3} + \cdots$ 得），故
>
> $$F(x)=\frac{1}{x^{2}}-\left(\frac{1}{x^{2}}-\frac{2}{3}+O(x^{2})\right)=\frac{2}{3}+O(x^{2}),$$
>
> 于是
>
> $$\lim_{x\to0^{+}}F(x)=\frac{2}{3}.$$
>
> 左端 $(x \to \frac{\pi}{2})$：此时 $\tan x \to +\infty$， $\frac{1}{\tan^2 x} \to 0$， $\frac{1}{x^2} \to \frac{4}{\pi^2}$，故
>
> $$\lim_{x\to(\pi/2)^{-}}F(x)=\frac{4}{\pi^{2}}.$$
>
> 第四步: 合并. 由 $F(x)$ 在 $\left(0, \frac{\pi}{2}\right)$ 上严格递减,
>
> $$\frac{4}{\pi^{2}}=\lim_{x\to(\pi/2)^{-}}F(x)<F(x)<\lim_{x\to0^{+}}F(x)=\frac{2}{3}.$$
>
> 即
>
> $$\frac{4}{\pi^{2}}<\frac{1}{x^{2}}-\frac{1}{\tan^{2}x}<\frac{2}{3},\qquad0<x<\frac{\pi}{2}.$$
>
> 本题的关键是把 $F'$ 的分子分离成一个 「$x^{3}-u(x)^{3}$」 的形式，其中 $u(x) = \frac{\sin x}{\cos^{1/3}x}$.
>
> 接下来只需对 $g(x) = u(x) - x$ 做差求导，化到 $g'(x) = \frac{(t-1)^{2}(2t+1)}{3t^{2}}$ ( $t = \cos^{2/3}x$)，符号一目了然。这一步的因式分解 $1 + 2t^{3} - 3t^{2} = (t-1)^{2}(2t+1)$ 是全题的关键。(4) 令 $f(x) = \sqrt{x} + \sqrt{x + 27} + \sqrt{13 - x}$ ( $0 \leq x \leq 13$).
>
> 第一步：求导并注意凹性.
>
> $$f^{\prime}(x)=\frac{1}{2\sqrt{x}}+\frac{1}{2\sqrt{x+27}}-\frac{1}{2\sqrt{13-x}},\qquad f^{\prime\prime}(x)=-\frac{1}{4x^{3/2}}-\frac{1}{4(x+27)^{3/2}}-\frac{1}{4(13-x)^{3/2}}<0$$
>
> 所以 f 在 $[0,13]$ 上 **上凸**, $f'$ 严格递减，驻点至多一个.
>
> 第二步：试出驻点. 取 x = 9:
>
> $$f^{\prime}(9)=\frac{1}{2\cdot3}+\frac{1}{2\cdot6}-\frac{1}{2\cdot2}=\frac{1}{6}+\frac{1}{12}-\frac{1}{4}=0,$$
>
> 故x=9是唯一的驻点，且为极大值点.
>
> 第三步：比较三处的值.
>
> $$f(9)=3+6+2=11,\qquad f(0)=0+\sqrt{27}+\sqrt{13}\approx8.8,\qquad f(13)=\sqrt{13}+\sqrt{40}+0\approx9.9,$$
>
> 都小于11. 由 f 上凸、x=9 是唯一极大值点，知 f 的最大值为11，即
>
> $$\sqrt{x}+\sqrt{x+27}+\sqrt{13-x}\leqslant11\qquad(0\leqslant x\leqslant13).$$
>
> (5) 两边取对数，先乘 $\sqrt{2}$，再乘 $\sqrt{2x+1}$，把两个看似不匹配的表达式化为同一个函数
>
> $$F(s)=\sqrt{s(s+1)}\ln\left(1+\frac{1}{s}\right)$$
>
> 在 $s=2x+1$ 与 s=2x 处的值, 从而原不等式等价于 $F(2x+1)>F(2x)$. 第一步: 取对数. 原不等式等价于
>
> $$\sqrt{x+1}\ln\left(1+\frac{1}{2x+1}\right)>\sqrt{x}\ln\left(1+\frac{1}{2x}\right).$$
>
> 第二步：先乘 $\sqrt{2}$
>
> $$\sqrt{2x+2}\ln\left(1+\frac{1}{2x+1}\right)>\sqrt{2x}\ln\left(1+\frac{1}{2x}\right).$$
>
> 第三步：再乘 $\sqrt{2x+1}$
>
> $$\sqrt{(2x+2)(2x+1)}\ln\left(1+\frac{1}{2x+1}\right)>\sqrt{2x(2x+1)}\ln\left(1+\frac{1}{2x}\right).$$
>
> 第四步：识别同构. 令 $s = 2x + 1$，则 2x = s - 1. 不等式 (1) 即
>
> $$\sqrt{s(s+1)}\ln\left(1+\frac{1}{s}\right)>\sqrt{(s-1)s}\ln\left(1+\frac{1}{s-1}\right).$$
>
> 两边恰是同一个函数
>
> $$F(s)=\sqrt{s(s+1)}\ln\left(1+\frac{1}{s}\right)$$
>
> 在 $s=2x+1$ 与 s=2x=s-1 处的值. 只需证 $F(x)$ 在 $(0,+\infty)$ 上严格递增.
>
> 第五步：证 $F(x)$ 严格递增。把 $F(x)$ 写成
>
> $$F(s)=\sqrt{s(s+1)}\left[\ln(s+1)-\ln s\right].$$
>
> 求导：
>
> $$\begin{aligned}F^{\prime}(s)&=\frac{2s+1}{2\sqrt{s(s+1)}}\ln\left(1+\frac{1}{s}\right)-\frac{1}{\sqrt{s(s+1)}}\\&=\frac{1}{2\sqrt{s(s+1)}}\left[(2s+1)\ln\left(1+\frac{1}{s}\right)-2\right].\end{aligned}$$
>
> 令 $u = \frac{1}{s} > 0$，则 $(2s + 1)\ln(1 + \frac{1}{s}) - 2 = \frac{(2 + u)\ln(1 + u) - 2u}{u}$.
>
> 记 $\varphi(u)=(2+u)\ln(1+u)-2u(u>0)$. $\varphi(0)=0$, 且
>
> $$\varphi^{\prime}(u)=\ln(1+u)-\frac{u}{1+u},\qquad\varphi^{\prime}(0)=0,$$
>
> $$\varphi^{\prime\prime}(u)=\frac{u}{(1+u)^{2}}>0.$$
>
> 故 $\varphi^{\prime}$ 严格递增, $\varphi^{\prime}>0,\varphi>0$ , 从而 $F^{\prime}(s)>0$
>
> 第六步：结论. 由 $2x+1>2x$ 及 $F(x)$ 严格递增， $F(2x+1)>F(2x)$，即原不等式成立. 关键是「先乘 $\sqrt{2}$，再乘 $\sqrt{2x+1}$」这两步，把两边化为同一函数在两点取值. 之后只需证 $F(x)$ 递增，归结为一个纯对数不等式 $(2+u)\ln(1+u)>2u$.

---

# 基础篇·第三章 一元积分学

## 3.1 不定积分

### 3.1.1 凑微分法

核心公式 $dy = y' dx$，将合适的函数凑成对应的微分，以整体法解题，是解决不定积分最朴素的思路之一.

**1.** 常见凑微分

(1) (难度: ★★) $\int\frac{1+x}{x(1+xe^{x})}dx$

(2) (难度: ★★) $\int \frac{1 - \ln x}{x \ln x} dx$

> [!answer]- 原书参考答案（A.3.1 第 1 题，未逐题独立验算）
> **1.** (1) 注意到 $\mathrm{d}(xe^{x}) = (1 + x)e^{x}\mathrm{d}x$，而被积函数的分子恰好是 $1 + x$，于是先给分子「补」上因子 $e^{x}$:
>
> $$\frac{1+x}{x\left(1+xe^{x}\right)}=\frac{(1+x)e^{x}}{xe^{x}\left(1+xe^{x}\right)}.$$
>
> 令$u=xe^{x}$, 则 $(1+x)e^{x}\mathrm{d}x=\mathrm{d}u,$ 从而
>
> $$\int\frac{1+x}{x\left(1+xe^{x}\right)}\mathrm{d}x=\int\frac{\mathrm{d}u}{u(1+u)}=\int\left(\frac{1}{u}-\frac{1}{1+u}\right)\mathrm{d}u=\ln\left|\frac{u}{1+u}\right|+C.$$
>
> 代回$u=xe^{x}$,得
>
> $$\int\frac{1+x}{x\left(1+xe^{x}\right)}\mathrm{d}x=\ln\left|\frac{xe^{x}}{1+xe^{x}}\right|+C.$$
>
> (2) 分子分母都含 $\ln x$，而 $(\ln x)' = \frac{1}{x}$，于是 $\frac{dx}{x}$ 恰好可以打包成 $d(\ln x)$，整体换元即可。令 $u = \ln x$，则 $du = \frac{dx}{x}$，于是
>
> $$\int\frac{1-\ln x}{x\ln x}\mathrm{d}x=\int\frac{1-u}{u}\mathrm{d}u=\int\left(\frac{1}{u}-1\right)\mathrm{d}u=\ln|u|-u+C.$$
>
> 回代 $u = \ln x$ 得
>
> $$\int\frac{1-\ln x}{x\ln x}\mathrm{d}x=\ln\left|\ln x\right|-\ln x+C=\ln\left|\frac{\ln x}{x}\right|+C.$$
>
> 参考答案写成 $\ln\left|\frac{\ln x}{x}\right| + C$ 更紧凑. 这类题的关键是先把「共同的因子」找出来: 本题中 $\frac{1}{x}$ 与 $\ln x$ 是绑定出现的.

**2.** 有理积分

(1) (难度: ★★) $\int\frac{x^{2}+1}{x^{4}+1}dx$

(2) (难度: ★★) $\int \frac{x^{2}-1}{x^{4}+1} dx$

(3) (难度: ★★★) $\int \frac{1}{x^{4}+1} dx$

(4) (难度: ★★) $\int \frac{x^{2}+1}{x\sqrt{x^{4}+1}}dx$

(5) (难度: ★★) $\int\frac{x^{8}(x^{2}+1)}{(x^{2}-1)^{10}}dx$

(6) (难度: ★★) $\int \frac{x^{2}-1}{x^{4}+3x^{2}+1} dx$

> [!answer]- 原书参考答案（A.3.1 第 2 题，未逐题独立验算）
> **2.** 第一问. 分子分母同时除以 $x^{2}$:
>
> $$\frac{x^{2}+1}{x^{4}+1}=\frac{1+\frac{1}{x^{2}}}{x^{2}+\frac{1}{x^{2}}}=\frac{\mathrm{d}\left(x-\frac{1}{x}\right)}{\left(x-\frac{1}{x}\right)^{2}+2},$$
>
> 这里用到 $x^{2}+\frac{1}{x^{2}}=\left(x-\frac{1}{x}\right)^{2}+2$ 。令 $u=x-\frac{1}{x}$，则
>
> $$\int\frac{x^{2}+1}{x^{4}+1}\mathrm{d}x=\int\frac{\mathrm{d}u}{u^{2}+2}=\frac{1}{\sqrt{2}}\arctan\frac{u}{\sqrt{2}}+C=\frac{1}{\sqrt{2}}\arctan\frac{x^{2}-1}{\sqrt{2}x}+C.$$
>
> 第二问. 同样地除以 $x^{2}$:
>
> $$\frac{x^{2}-1}{x^{4}+1}=\frac{1-\frac{1}{x^{2}}}{x^{2}+\frac{1}{x^{2}}}=\frac{\mathrm{d}\left(x+\frac{1}{x}\right)}{\left(x+\frac{1}{x}\right)^{2}-2},$$
>
> 令 $u = x + \frac{1}{x}$，则
>
> $$\begin{aligned}\int\frac{x^{2}-1}{x^{4}+1}\mathrm{d}x&=\int\frac{\mathrm{d}u}{u^{2}-2}=\frac{1}{2\sqrt{2}}\ln\left|\frac{u-\sqrt{2}}{u+\sqrt{2}}\right|+C\\&=\frac{1}{2\sqrt{2}}\ln\left|\frac{x^{2}-\sqrt{2}x+1}{x^{2}+\sqrt{2}x+1}\right|+C.\end{aligned}$$
>
> 第三问. 注意
>
> $$\frac{x^{2}+1}{x^{4}+1}-\frac{x^{2}-1}{x^{4}+1}=\frac{2}{x^{4}+1},$$
>
> 所以第三个积分等于前两个积分之差的一半：
>
> $$\int\frac{\mathrm{d}x}{x^{4}+1}=\frac{1}{2\sqrt{2}}\arctan\frac{x^{2}-1}{\sqrt{2}x}-\frac{1}{4\sqrt{2}}\ln\left|\frac{x^{2}-\sqrt{2}x+1}{x^{2}+\sqrt{2}x+1}\right|+C.$$
>
> (4)(2)令 $u=x^{2}$，则 $du=2x\,dx$、 $\frac{dx}{x}=\frac{du}{2u}$，于是
>
> $$\int\frac{x^{2}+1}{x\sqrt{x^{4}+1}}\mathrm{d}x=\frac{1}{2}\int\frac{u+1}{u\sqrt{u^{2}+1}}\mathrm{d}u=\frac{1}{2}\int\left(\frac{1}{\sqrt{u^{2}+1}}+\frac{1}{u\sqrt{u^{2}+1}}\right)\mathrm{d}u,$$
>
> 其中 $\int \frac{du}{\sqrt{u^2+1}} = \ln \left(u + \sqrt{u^2+1}\right)$, $\int \frac{du}{u\sqrt{u^2+1}} = \ln \frac{u}{1+\sqrt{u^2+1}}$, 所以原式
>
> $$= \frac{1}{2} \ln \left(x^2 + \sqrt{x^4+1}\right) + \frac{1}{2} \ln \frac{x^2}{1 + \sqrt{x^4+1}} + C.$$
>
> (5) 分母是 $\left(x^{2}-1\right)^{10}$，分子是 $x^{8}\left(x^{2}+1\right)$，两者的次数相差 10，是典型的倒代换或「同除 $x^{10}$」的动机：同除之后分母变成 $\left(x-\frac{1}{x}\right)^{10}$，分子变成 $1+\frac{1}{x^{2}}$，恰好是前者的导数. 分子分母同除 $x^{10}$:
>
> $$\frac{x^{8}(x^{2}+1)}{(x^{2}-1)^{10}}=\frac{\frac{x^{2}+1}{x^{2}}}{\left(\frac{x^{2}-1}{x}\right)^{10}}=\frac{1+\frac{1}{x^{2}}}{\left(x-\frac{1}{x}\right)^{10}},$$
>
> 而 $\mathrm{d}\left(x-\frac{1}{x}\right)=\left(1+\frac{1}{x^{2}}\right)\mathrm{d}x$ ，于是
>
> $$\int\frac{x^{8}(x^{2}+1)}{(x^{2}-1)^{10}}\mathrm{d}x=\int\left(x-\frac{1}{x}\right)^{-10}\mathrm{d}\left(x-\frac{1}{x}\right)=-\frac{1}{9}\left(x-\frac{1}{x}\right)^{-9}+C.$$
>
> 这类题几乎不需要真正的「换元」步骤，只要用 $(x^{2}-1)^{10}=x^{10}\left(x-\frac{1}{x}\right)^{10}$ 这一个恒等式，就能把被积函数一眼看成 $\frac{du}{u^{10}}$. (6)(3) 分子分母同除 $x^{2}$:
>
> $$\frac{x^{2}-1}{x^{4}+3x^{2}+1}=\frac{1-\frac{1}{x^{2}}}{\left(x+\frac{1}{x}\right)^{2}+1},$$
>
> 令 $u = x + \frac{1}{x}$，则 $\mathrm{d}u = \left(1 - \frac{1}{x^{2}}\right)\mathrm{d}x$，故
>
> $$\int\frac{x^{2}-1}{x^{4}+3x^{2}+1}\mathrm{d}x=\int\frac{\mathrm{d}u}{u^{2}+1}=\arctan\left(x+\frac{1}{x}\right)+C.$$

**3.** 三角积分

(1) (难度: ★★) $\int \frac{\tan x}{3\sin^{2}x + 2\cos^{2}x} \, dx$

(2) (难度: ★★) $\int \frac{1}{\sin x \cos^{3} x} dx$

> [!answer]- 原书参考答案（A.3.1 第 3 题，未逐题独立验算）
> **3.** (1) 分母提出 $\cos^{2}x$:
>
> $$3\sin^{2}x+2\cos^{2}x=\cos^{2}x\left(3\tan^{2}x+2\right).$$
>
> 于是被积表达式化为
>
> $$\frac{\tan x}{3\sin^{2}x+2\cos^{2}x}\mathrm{d}x=\frac{\tan x\sec^{2}x}{3\tan^{2}x+2}\mathrm{d}x=\frac{u\mathrm{d}u}{3u^{2}+2},$$
>
> 其中 $u = \tan x$. 所以
>
> $$\int\frac{\tan x}{3\sin^{2}x+2\cos^{2}x}\mathrm{d}x=\frac{1}{6}\ln\left(3\tan^{2}x+2\right)+C.$$
>
> (2) 被积函数只含 $\sin x$ 与 $\cos x$，用 $\sin^2 x + \cos^2 x = 1$ 把分子「补」出来，就能拆成两项：一项整体是 $\sin x \, dx = -\mathrm{d}(\cos x)$，另一项化为 $\frac{1}{\sin x \cos x}$。把分子写成 $\sin^2 x + \cos^2 x$：
>
> $$\int\frac{\mathrm{d}x}{\sin x\cos^{3}x}=\int\frac{\sin^{2}x+\cos^{2}x}{\sin x\cos^{3}x}\mathrm{d}x=\int\frac{\sin x}{\cos^{3}x}\mathrm{d}x+\int\frac{\mathrm{d}x}{\sin x\cos x}.$$
>
> 第一项：
>
> $$\int\frac{\sin x}{\cos^{3}x}\mathrm{d}x=-\int\cos^{-3}x\mathrm{d}(\cos x)=\frac{1}{2\cos^{2}x}.$$
>
> 第二项用恒等变形
>
> $$\frac{1}{\sin x\cos x}=\frac{\sin^{2}x+\cos^{2}x}{\sin x\cos x}=\frac{\sin x}{\cos x}+\frac{\cos x}{\sin x},$$
>
> 故
>
> $$\int\frac{\mathrm{d}x}{\sin x\cos x}=\int\left(\tan x+\cot x\right)\mathrm{d}x=-\ln|\cos x|+\ln|\sin x|=\ln|\tan x|.$$
>
> 合起来
>
> $$\int\frac{\mathrm{d}x}{\sin x\cos^{3}x}=\frac{1}{2\cos^{2}x}+\ln|\tan x|+C.$$
>
> 第二项的两种算法都值得记住: 一是化为 $\int \frac{2\,dx}{\sin 2x}$ 后用 $\int \csc u\,du = \ln \left| \tan \frac{u}{2} \right|$;
>
> 二是直接拆成 $\tan x + \cot x$. 后者更快.

**4.** 非常规的硬凑微分技巧

(1) (难度: ★★★) $\int \frac{x^{2}(x\sec^{2}x+\tan x)}{(x\tan x+1)^{2}}dx$

(2) (难度: ★★★) $\int \frac{x^{2}}{(x \sin x + \cos x)^{2}} \, dx$

(3) (难度: ★★★★) $\int \frac{x^{2} + 20}{(x \sin x + 5 \cos x)^{2}} \, dx$

(4) (难度: ★★★) $\int \frac{\cos x + x \sin x}{(x + \cos x)^2} \, dx$

> [!answer]- 原书参考答案（A.3.1 第 4 题，未逐题独立验算）
> **4.** (1) 第一步: 认出分子里的「导数结构」。记 $P = 1 + x \tan x$，则 $P' = \tan x + x \sec^2 x$，恰是分子中的括号，于是所给积分为 $\int \frac{x^2 P'}{p^2} dx$。
>
> 第二步: 用 $\left(\frac{x^{2}}{P}\right)^{\prime}$ 拆开. 由 $\left(\frac{x^{2}}{P}\right)^{\prime}=\frac{2xP-x^{2}P^{\prime}}{P^{2}}=\frac{2x}{P}-\frac{x^{2}P^{\prime}}{P^{2}}$ 得
>
> $$\frac{x^{2}P^{\prime}}{P^{2}}=\frac{2x}{P}-\left(\frac{x^{2}}{P}\right)^{\prime}.$$
>
> 第三步:剩下的 $\int\frac{x}{P}dx$还是凑微分.由 $\frac{x}{1+x\tan x}=\frac{x\cos x}{\cos x+x\sin x}$与 $(\cos x+x\sin x)^{\prime}=x\cos x$,得 $\int\frac{x}{P}dx=\ln|\cos x+x\sin x|$.代入第二步即得
>
> $$\int\frac{x^{2}\left(x\sec^{2}x+\tan x\right)}{\left(x\tan x+1\right)^{2}}\mathrm{d}x=2\ln|\cos x+x\sin x|-\frac{x^{2}}{1+x\tan x}+C.$$
>
> (2) 分母是 $\sin^{3}x + \cos^{3}x$，而分子 $\sin x - \cos x$ 恰好是 $s = \sin x + \cos x$ 的导数的相反数。于是整个积分可以只用 s 表示，不必再做「自相关」那一手。令
>
> $$s=\sin x+\cos x,\qquad p=\sin x\cos x,$$
>
> 则 $s' = \cos x - \sin x$，故 $(\sin x - \cos x)dx = -ds$，且 $p = \frac{s^2 - 1}{2}$。由立方和公式
>
> $$\sin^{3}x+\cos^{3}x=s(1-p)=s\left(1-\frac{s^{2}-1}{2}\right)=\frac{s\left(3-s^{2}\right)}{2},$$
>
> 于是
>
> $$\int\frac{\sin x-\cos x}{\sin^{3}x+\cos^{3}x}\mathrm{d}x=-2\int\frac{\mathrm{d}s}{s\left(3-s^{2}\right)}.$$
>
> 部分分式分解
>
> $$\frac{1}{s\left(3-s^{2}\right)}=\frac{1}{3}\left(\frac{1}{s}+\frac{s}{3-s^{2}}\right),$$
>
> 故
>
> $$-2\cdot\frac{1}{3}\int\left(\frac{1}{s}+\frac{s}{3-s^{2}}\right)\mathrm{d}s=-\frac{2}{3}\ln\left|s\right|+\frac{1}{3}\ln\left|3-s^{2}\right|+C.$$
>
> 由 $3 - s^{2} = 2 (1 - \sin x \cos x)$，回代即得
>
> $$\int\frac{\sin x-\cos x}{\sin^{3}x+\cos^{3}x}\mathrm{d}x=\frac{1}{3}\ln\left|1-\sin x\cos x\right|-\frac{2}{3}\ln\left|\sin x+\cos x\right|+C.$$
>
> 本题与正文例题 $\int \frac{dx}{\sin^3 x + \cos^3 x}$ 同族: 分母完全相同, 差别只在分子. 因为分子恰好是 s 的导数, 本题不需要解「关于 $f(x)$ 的方程」, 只要一路换元即可——值得对比体会两者的区别. (3) 第一步: 分母已是平方, 去试形如 $\frac{a \sin x + bx \cos x}{x \sin x + 5 \cos x}$ 的导数. 记 $P = x \sin x + 5 \cos x$, 则 $P' = \sin x + x \cos x - 5 \sin x = x \cos x - 4 \sin x$.
>
> 第二步: 把 $\frac{5 \sin x - x \cos x}{P}$ 求导. 由商的求导法则,
>
> $$\left(\frac{5\sin x-x\cos x}{P}\right)^{\prime}=\frac{\left(4\cos x+x\sin x\right)P-\left(5\sin x-x\cos x\right)\left(x\cos x-4\sin x\right)}{P^{2}},$$
>
> 其中分子展开为（记 $c = \cos x$, $s = \sin x$）
>
> $$(4c+x s)(x s+5c)-(5s-x c)(x c-4s)=20\left(c^{2}+s^{2}\right)+x^{2}\left(s^{2}+c^{2}\right)=x^{2}+20.$$
>
> 第三步：写出结果.
>
> $$\int\frac{x^{2}+20}{\left(x\sin x+5\cos x\right)^{2}}\mathrm{d}x=\frac{5\sin x-x\cos x}{x\sin x+5\cos x}+C.$$
>
> (4)(8) 注意分子恰是 $\left(\frac{x}{\cos x}\right)^{\prime}$ 的配套:
>
> $$\left(\frac{x}{\cos x}\right)^{\prime}=\frac{\cos x+x\sin x}{\cos^{2}x}.$$
>
> 令 $u = \frac{x}{\cos x}$，则 $\cos x + x \sin x = \cos^2 x \cdot u'$，而 $x + \cos x = \cos x (1 + u)$，于是
>
> $$\int\frac{\cos x+x\sin x}{(x+\cos x)^{2}}\mathrm{d}x=\int\frac{\cos^{2}x u^{\prime}}{\cos^{2}x(1+u)^{2}}\mathrm{d}x=\int\frac{\mathrm{d}u}{(1+u)^{2}}=-\frac{\cos x}{x+\cos x}+C.$$

**5.** 齐次三角积分

(1) (难度: ★★★★) $\int \frac{1}{\sin^{3}x + \cos^{3}x} \, dx$

(2) (难度: ★) $\int \frac{\sin x + 2 \cos x}{2 \sin x - \cos x} \, dx$

> [!answer]- 原书参考答案（A.3.1 第 5 题，未逐题独立验算）
> **5.** (1) 分母是三次三角函数, 用 $s = \sin x - \cos x$ 把它化成代数式. 由 $s^{2} = 1 - 2\sin x\cos x$、 $(\sin x + \cos x)^{2} = 2 - s^{2}$, 得
>
> $$\sin^{3}x+\cos^{3}x=(\sin x+\cos x)(1-\sin x\cos x)=\sqrt{2-s^{2}}\cdot\frac{1+s^{2}}{2},\qquad\mathrm{d}s=(\cos x+\sin x)\mathrm{d}x=\sqrt{2-s^2}\,\mathrm{d}x,$$
>
> 于是原式= $\int\frac{2ds}{(2-s^{2})(1+s^{2})}$
>
> 用部分分式 $\frac{2}{(2-s^{2})(1+s^{2})}=\frac{2/3}{2-s^{2}}+\frac{2/3}{1+s^{2}}$ （比对系数：一次项系数为0，常数项均为 $\frac{2}{3}$），故
>
> $$\int\frac{\mathrm{d}x}{\sin^{3}x+\cos^{3}x}=\frac{1}{3\sqrt{2}}\ln\left|\frac{\sqrt{2}+\sin x-\cos x}{\sqrt{2}-\sin x+\cos x}\right|+\frac{2}{3}\arctan\left(\sin x-\cos x\right)+C.$$
>
> (2) 观察分子与分母导数的关系: $(2\sin x - \cos x)' = 2\cos x + \sin x$ 恰为分子, 故
>
> $$\int\frac{\sin x+2\cos x}{2\sin x-\cos x}\mathrm{d}x=\ln\left|2\sin x-\cos x\right|+C.$$

### 3.1.2 换元积分法

对合适部分进行换元，可对不定积分进行较大程度的化简，注意常见的几种代换模式，熟练掌握相关计算.

**1.** 倒代换

(1) (难度: ★) $\int \frac{1}{x^{4}(x^{2}+1)} dx$

(2) (难度: ★★) $\int \frac{1}{x + x^{2026}} dx$

> [!answer]- 原书参考答案（A.3.2 第 1 题，未逐题独立验算）
> **1.** (1) (9) 作倒代换 $x = \frac{1}{t}$，则 $\mathrm{d}x = -\frac{\mathrm{d}t}{t^{2}}$、 $x^{4}(x^{2} + 1) = \frac{1 + t^{2}}{t^{6}}$，于是
>
> $$\int\frac{\mathrm{d}x}{x^{4}\left(x^{2}+1\right)}=-\int\left(t^{2}-1+\frac{1}{1+t^{2}}\right)\mathrm{d}t=-\frac{1}{3x^{3}}+\frac{1}{x}+\arctan x+C.$$
>
> (2) 令 $t = \frac{1}{x}$，则 $x = \frac{1}{t}$、 $\mathrm{d}x = -\frac{\mathrm{d}t}{t^{2}}$，于是
>
> $$\frac{\mathrm{d}x}{x+x^{2026}}=\frac{-\frac{\mathrm{d}t}{t^{2}}}{\frac{1}{t}+\frac{1}{t^{2026}}}=-\frac{t^{2024}}{t^{2025}+1}\mathrm{d}t.$$
>
> 所以
>
> $$\int\frac{\mathrm{d}x}{x+x^{2026}}=-\frac{1}{2025}\int\frac{\mathrm{d}\left(t^{2025}+1\right)}{t^{2025}+1}=-\frac{1}{2025}\ln\left|t^{2025}+1\right|+C.$$
>
> 回代 $t = \frac{1}{x}$，得
>
> $$\int\frac{\mathrm{d}x}{x+x^{2026}}=-\frac{1}{2025}\ln\left|1+x^{-2025}\right|+C=\ln\left|x\right|-\frac{1}{2025}\ln\left|1+x^{2025}\right|+C.$$

**2.** 三角代换

(1) (难度: ★★) $\int \frac{dx}{\sqrt{(x-a)(b-x)}}$

(2) (难度: ★★★) $\int \frac{\sin^{2} x}{(\sin x - \cos x - 1)^{3}} \, dx$

(3) (难度: ★★★) $\int \frac{1}{\sqrt{(x^{2}+5)^{3}}} dx$

> [!answer]- 原书参考答案（A.3.2 第 2 题，未逐题独立验算）
> **2.** (1) 根号里是二次式, 先配方化为 $\sqrt{R^{2}-u^{2}}$ 的形状, 再套 $\int\frac{du}{\sqrt{R^{2}-u^{2}}}=\arcsin\frac{u}{R}$. 配方:
>
> $$(x-a)(b-x)=-x^{2}+(a+b)x-ab=\frac{(b-a)^{2}}{4}-\left(x-\frac{a+b}{2}\right)^{2}.$$
>
> 于是
>
> $$\begin{aligned}\int\frac{\mathrm{d}x}{\sqrt{(x-a)(b-x)}}&=\int\frac{\mathrm{d}\left(x-\frac{a+b}{2}\right)}{\sqrt{\left(\frac{b-a}{2}\right)^{2}-\left(x-\frac{a+b}{2}\right)^{2}}}\\&=\arcsin\frac{2x-a-b}{b-a}+C.\end{aligned}$$
>
> 本题只在 a < x < b 上有意义（根号内为正），此时 $\left|\frac{2x - a - b}{b - a}\right| < 1$，反正弦取主值即可。若题目要求在更大的区间上讨论，就需要分段处理。（2）令 $t = \tan \frac{x}{2}$，则
>
> $$\sin x=\frac{2t}{1+t^{2}},\qquad\cos x=\frac{1-t^{2}}{1+t^{2}},\qquad\mathrm{d}x=\frac{2\mathrm{d}t}{1+t^{2}}.$$
>
> 关键的一步是先算分母：
>
> $$\sin x-\cos x-1=\frac{2t-\left(1-t^{2}\right)-\left(1+t^{2}\right)}{1+t^{2}}=\frac{2(t-1)}{1+t^{2}}.$$
>
> 于是
>
> $$\frac{\sin^{2}x\mathrm{d}x}{\left(\sin x-\cos x-1\right)^{3}}=\frac{\frac{4t^{2}}{\left(1+t^{2}\right)^{2}}\cdot\frac{2\mathrm{d}t}{1+t^{2}}}{\frac{8(t-1)^{3}}{\left(1+t^{2}\right)^{3}}}=\frac{t^{2}\left(1+t^{2}\right)}{(t-1)^{3}}\mathrm{d}t.$$
>
> 接下来做多项式除法与部分分式分解：
>
> $$\frac{t^{2}\left(1+t^{2}\right)}{(t-1)^{3}}=\frac{t^{4}+t^{2}}{(t-1)^{3}}=t+3+\frac{7t^{2}-8t+3}{(t-1)^{3}},$$
>
> 而令 w = t - 1，由 $7t^{2} - 8t + 3 = 7w^{2} + 6w + 2$ 得
>
> $$\frac{7t^{2}-8t+3}{(t-1)^{3}}=\frac{7}{t-1}+\frac{6}{(t-1)^{2}}+\frac{2}{(t-1)^{3}}.$$
>
> 逐项积分：
>
> $$\begin{aligned}\int\left(t+3+\frac{7}{t-1}+\frac{6}{(t-1)^{2}}+\frac{2}{(t-1)^{3}}\right)\mathrm{d}t\\=\frac{t^{2}}{2}+3t+7\ln|t-1|-\frac{6}{t-1}-\frac{1}{(t-1)^{2}}+C.\end{aligned}$$
>
> 最后把 $t = \tan \frac{x}{2}$ 回代，即得
>
> $$\begin{aligned}\int\frac{\sin^{2}x}{\left(\sin x-\cos x-1\right)^{3}}\mathrm{d}x&=\frac{1}{2}\tan^{2}\frac{x}{2}+3\tan\frac{x}{2}+7\ln\left|\tan\frac{x}{2}-1\right|\\&\quad-\frac{6}{\tan\frac{x}{2}-1}-\frac{1}{\left(\tan\frac{x}{2}-1\right)^{2}}+C.\end{aligned}$$
>
> (3) 令 $x = \sqrt{5} \tan t \left( -\frac{\pi}{2} < t < \frac{\pi}{2} \right)$，则 $\mathrm{d}x = \sqrt{5} \sec^2 t \, \mathrm{d}t$，且
>
> $$\sqrt{\left(x^{2}+5\right)^{3}}=\left(5\sec^{2}t\right)^{3/2}=5\sqrt{5}\sec^{3}t.$$
>
> 于是
>
> $$\int\frac{\mathrm{d}x}{\sqrt{\left(x^{2}+5\right)^{3}}}=\int\frac{\sqrt{5}\sec^{2}t}{5\sqrt{5}\sec^{3}t}\mathrm{d}t=\frac{1}{5}\int\cos t\mathrm{d}t=\frac{1}{5}\sin t+C.$$
>
> 由 $\tan t = \frac{x}{\sqrt{5}}$ 得 $\sin t = \frac{x}{\sqrt{x^{2} + 5}}$，所以
>
> $$\int\frac{\mathrm{d}x}{\sqrt{\left(x^{2}+5\right)^{3}}}=\frac{x}{5\sqrt{x^{2}+5}}+C.$$

**3.** 根式代换

(1) (难度: ★) $\int \frac{1}{\sqrt{1+x} + \sqrt[3]{1+x}} \, dx$

(2) (难度: ★★) $\int \frac{1}{1 + \sqrt{x} + \sqrt{1 + x}} \, dx$

> [!answer]- 原书参考答案（A.3.2 第 3 题，未逐题独立验算）
> **3.** （1）两个根式的次数为2与3，取最小公倍数6，令
>
> $$u=\sqrt[6]{1+x},\qquad1+x=u^{6},\qquad\mathrm{d}x=6u^{5}\mathrm{d}u.$$
>
> 此时 $\sqrt{1+x}=u^{3}$、 $\sqrt[3]{1+x}=u^{2}$，于是
>
> $$\int\frac{6u^{5}\mathrm{d}u}{u^{3}+u^{2}}=\int\frac{6u^{3}}{u+1}\mathrm{d}u=6\int\left(u^{2}-u+1-\frac{1}{u+1}\right)\mathrm{d}u,$$
>
> 最后一步是多项式除法.逐项积分得
>
> $$6\left(\frac{u^{3}}{3}-\frac{u^{2}}{2}+u-\ln|u+1|\right)+C=2u^{3}-3u^{2}+6u-6\ln|u+1|+C.$$
>
> 回代 $u = \sqrt[6]{1 + x}$，即得
>
> $$\int\frac{\mathrm{d}x}{\sqrt{1+x}+\sqrt[3]{1+x}}=2\sqrt{1+x}-3\sqrt[3]{1+x}+6\sqrt[6]{1+x}-6\ln\left(\sqrt[6]{1+x}+1\right)+C.$$
>
> (2) 令
>
> $$u=\sqrt{x}+\sqrt{1+x},$$
>
> 则由 $\left(\sqrt{1+x}+\sqrt{x}\right)\left(\sqrt{1+x}-\sqrt{x}\right)=1$得 $\frac{1}{u}=\sqrt{1+x}-\sqrt{x}$.两式相加减，解出
>
> $$\sqrt{1+x}=\frac{1}{2}\left(u+\frac{1}{u}\right),\qquad\sqrt{x}=\frac{1}{2}\left(u-\frac{1}{u}\right),\qquad x=\frac{1}{4}\left(u-\frac{1}{u}\right)^{2}.$$
>
> 于是
>
> $$\mathrm{d}x=\frac{1}{2}\left(u-\frac{1}{u}\right)\left(1+\frac{1}{u^{2}}\right)\mathrm{d}u=\frac{u^{4}-1}{2u^{3}}\mathrm{d}u,$$
>
> 而 $1 + \sqrt{x} + \sqrt{1 + x} = 1 + u$. 所以
>
> $$\int\frac{\mathrm{d}x}{1+\sqrt{x}+\sqrt{1+x}}=\frac{1}{2}\int\frac{u^{4}-1}{u^{3}(1+u)}\mathrm{d}u=\frac{1}{2}\int\left(1-\frac{1}{u}+\frac{1}{u^{2}}-\frac{1}{u^{3}}\right)\mathrm{d}u,$$
>
> 其中用到 $u^{4}-1=(u^{2}+1)(u-1)(u+1)$. 逐项积分得
>
> $$\frac{1}{2}\left(u-\ln u-\frac{1}{u}+\frac{1}{2u^{2}}\right)+C.$$
>
> 回代 $u = \sqrt{x} + \sqrt{1 + x}$，即得
>
> $$\int\frac{\mathrm{d}x}{1+\sqrt{x}+\sqrt{1+x}}=\frac{1}{2}\left(u-\ln u-\frac{1}{u}+\frac{1}{2u^{2}}\right)+C,\qquad u=\sqrt{x}+\sqrt{1+x}.$$

**4.** 隐函数积分

(1) (难度: ★★★) $y^{2}(x-y)=x^{2}$，求 $\int\frac{1}{y^{2}}dx$

> [!answer]- 原书参考答案（A.3.2 第 4 题，未逐题独立验算）
> **4.** 方程关于 x, y 是齐次的, 取等比例换元 $t = \frac{y}{x}$, 即 y = tx. 代入 $y^{2}(x - y) = x^{2}$:
>
> $$t^{2}x^{2}\cdot x(1-t)=x^{2}\qquad\Longrightarrow\qquad t^{2}x(1-t)=1,$$
>
> 所以
>
> $$x=\frac{1}{t^{2}(1-t)},\qquad y=tx=\frac{1}{t(1-t)}.$$
>
> 对 x 求导:
>
> $$\frac{\mathrm{d}x}{\mathrm{d}t}=\frac{\mathrm{d}}{\mathrm{d}t}\left[t^{-2}(1-t)^{-1}\right]=\frac{3t-2}{t^{3}(1-t)^{2}}.$$
>
> 于是
>
> $$\frac{1}{y^{2}}\mathrm{d}x=t^{2}(1-t)^{2}\cdot\frac{3t-2}{t^{3}(1-t)^{2}}\mathrm{d}t=\frac{3t-2}{t}\mathrm{d}t=\left(3-\frac{2}{t}\right)\mathrm{d}t.$$
>
> 积分并回代 $t = \frac{y}{x}$:
>
> $$\int\frac{1}{y^{2}}\mathrm{d}x=3t-2\ln\left|t\right|+C=\frac{3y}{x}-2\ln\left|\frac{y}{x}\right|+C.$$

### 3.1.3 分部积分法

分部积分的题目一般不会单独考察，通常都会结合凑微分和换元积分，这里只列举一些比较经典的分部积分计算题。

**1.** (难度: ★★★) $\int x \ln(x^{2}+1)\arctan x \, dx$

> [!answer]- 原书参考答案（A.3.3 第 1 题，未逐题独立验算）
> **1.** 第一步：先把 $x \ln(x^{2}+1)$ 凑成 $v'$，这样分部积分能把 $\ln$ 消掉。取 $v = \frac{(x^{2}+1)(\ln(x^{2}+1)-1)}{2}$，则
>
> $$v^{\prime}=\frac{2x\left(\ln(x^{2}+1)-1\right)+2x}{2}=x\ln(x^{2}+1).$$
>
> 第二步：分部积分.
>
> $$\int x\ln(x^{2}+1)\arctan x\mathrm{d}x=v\arctan x-\int\frac{v}{1+x^{2}}\mathrm{d}x=v\arctan x-\frac{1}{2}\int\left[\ln(x^{2}+1)-1\right]\mathrm{d}x.$$
>
> 第三步: 用 $\int \ln(x^{2}+1)dx = x\ln(x^{2}+1) - 2x + 2\arctan x$ 收尾.
>
> $$\int x\ln(x^{2}+1)\arctan x\mathrm{d}x=\frac{(x^{2}+1)\left(\ln(x^{2}+1)-1\right)}{2}\arctan x-\frac{x}{2}\ln(x^{2}+1)+\frac{3x}{2}-\arctan x+C$$

**2.** (难度: ★★★★) $\int \frac{e^{-\sin x} \sin 2x}{(1 - \sin x)^2} \, dx$

> [!answer]- 原书参考答案（A.3.3 第 2 题，未逐题独立验算）
> **2.** 先是三角与指数的混合, 先凑 $\mathrm{d}(\sin x)$ 把它变成关于 $t = \sin x$ 的积分; 化出来的 $\frac{2te^{-t}}{(1-t)^2}$ 恰好是 「$te^{-t}$」 乘以 $\frac{1}{(1-t)^2}$, 而后者正是 $\frac{1}{1-t}$ 的导数, 于是直接分部. 令 $t = \sin x$, 则 $\mathrm{d}t = \cos x \, \mathrm{d}x$, 而
>
> $$\sin2x\mathrm{d}x=2\sin x\cos x\mathrm{d}x=2t\mathrm{d}t,$$
>
> 于是
>
> $$\int\frac{e^{-\sin x}\sin2x}{\left(1-\sin x\right)^{2}}\mathrm{d}x=\int\frac{2te^{-t}}{(1-t)^{2}}\mathrm{d}t.$$
>
> 注意 $d\left(\frac{1}{1-t}\right)=\frac{dt}{(1-t)^2}$，分部积分得
>
> $$2\int t e^{-t}\mathrm{d}\left(\frac{1}{1-t}\right)=\frac{2t e^{-t}}{1-t}-2\int\frac{\left(t e^{-t}\right)^{\prime}}{1-t}\mathrm{d}t.$$
>
> 由 $(te^{-t})^{\prime}=e^{-t}-te^{-t}=e^{-t}(1-t)$，上式中的积分化为
>
> $$-2\int\frac{e^{-t}(1-t)}{1-t}\mathrm{d}t=-2\int e^{-t}\mathrm{d}t=2e^{-t},$$
>
> 所以
>
> $$\int\frac{2t e^{-t}}{(1-t)^{2}}\mathrm{d}t=\frac{2t e^{-t}}{1-t}+2e^{-t}+C=2e^{-t}\left(\frac{t}{1-t}+1\right)+C=\frac{2e^{-t}}{1-t}+C.$$
>
> 回代 $t = \sin x$，即得
>
> $$\int\frac{e^{-\sin x}\sin2x}{\left(1-\sin x\right)^{2}}\mathrm{d}x=\frac{2e^{-\sin x}}{1-\sin x}+C.$$
>
> 本题能「干净收尾」，全靠 $(1-t)$ 这个因子在分部后被约掉。如果分部后新出现的积分比原来的还复杂，说明 u、dv 的选取需要重来——这正是判断分部积分是否走对路的一条实用标准。

**3.** (难度:★★★) $\int \frac{e^{\arctan x}}{\sqrt{(1+x^2)^3}} \, dx$

> [!answer]- 原书参考答案（A.3.3 第 3 题，未逐题独立验算）
> **3.** 先换元. 令 $t = \arctan x$, 则 $\mathrm{d}t = \frac{\mathrm{d}x}{1 + x^{2}}$, 且
>
> $$\sqrt{1+x^{2}}=\sec t,\qquad\frac{1+x^{2}}{\sqrt{\left(1+x^{2}\right)^{3}}}=\frac{1}{\sqrt{1+x^{2}}}=\cos t.$$
>
> 于是
>
> $$\int\frac{e^{\arctan x}}{\sqrt{\left(1+x^{2}\right)^{3}}}\mathrm{d}x=\int e^{t}\cos t\mathrm{d}t=\frac{e^{t}}{2}\left(\sin t+\cos t\right)+C.$$
>
> 最后回代 $\sin t = \frac{x}{\sqrt{1 + x^2}}$、 $\cos t = \frac{1}{\sqrt{1 + x^2}}$:
>
> $$\int\frac{e^{\arctan x}}{\sqrt{(1+x^{2})^{3}}}\mathrm{d}x=\frac{e^{\arctan x}(1+x)}{2\sqrt{1+x^{2}}}+C.$$

**4.** (难度: ★★★) $\int\left(1+x-\frac{1}{x}\right)e^{x+\frac{1}{x}}dx$

> [!answer]- 原书参考答案（A.3.3 第 4 题，未逐题独立验算）
> **4.** 「多项式乘以指数函数」的结构, 指数里还含 $\frac{1}{x}$, 第一反应应当是「猜原函数」: 试一试 $\left(xe^{x+\frac{1}{x}}\right)^{\prime}$ 是否就是被积函数. 直接求导:
>
> $$\left(x e^{x+\frac{1}{x}}\right)^{\prime}=e^{x+\frac{1}{x}}+x e^{x+\frac{1}{x}}\left(1-\frac{1}{x^{2}}\right)=e^{x+\frac{1}{x}}\left(1+x-\frac{1}{x}\right),$$
>
> 其中用到 $x\left(1-\frac{1}{x^{2}}\right)=x-\frac{1}{x}$. 也就是说, 被积函数恰好是 $xe^{x+\frac{1}{x}}$ 的导数, 于是
>
> $$\int\left(1+x-\frac{1}{x}\right)e^{x+\frac{1}{x}}\mathrm{d}x=x e^{x+\frac{1}{x}}+C.$$
>
> 本题不需要分部积分. 看到「多项式 × 指数」，且多项式与指数内部的导数有关联时，先试「多项式 × 指数」整体求导，往往一步到位. 前一小节「借助求导公式凑微分」讲的正是这个思路.

**5.** (难度: ★★★★) $\int x^{2} \ln(x + \sqrt{x^{2} + 1}) \, dx$

> [!answer]- 原书参考答案（A.3.3 第 5 题，未逐题独立验算）
> **5.** 第一步: 分部积分 (取 $v = \frac{x^{3}}{3}$).
>
> $$\int x^{2}\ln\left(x+\sqrt{x^{2}+1}\right)\mathrm{d}x=\frac{x^{3}}{3}\ln\left(x+\sqrt{x^{2}+1}\right)-\frac{1}{3}\int\frac{x^{3}}{\sqrt{x^{2}+1}}\mathrm{d}x.$$
>
> 第二步：算剩下的积分. 令 $u = x^{2} + 1 \left( \mathrm{d}u = 2x \mathrm{d}x \right)$
>
> $$\int\frac{x^{3}}{\sqrt{x^{2}+1}}\mathrm{d}x=\frac{1}{2}\int\frac{u-1}{\sqrt{u}}\mathrm{d}u=\frac{1}{2}\left(\frac{2}{3}u^{3/2}-2u^{1/2}\right)=\frac{\left(x^{2}-2\right)\sqrt{x^{2}+1}}{3}.$$
>
> 第三步：合并.
>
> $$\int x^{2}\ln\left(x+\sqrt{x^{2}+1}\right)\mathrm{d}x=\frac{x^{3}}{3}\ln\left(x+\sqrt{x^{2}+1}\right)-\frac{\left(x^{2}-2\right)\sqrt{x^{2}+1}}{9}+C.$$

**6.** (难度: ★★★) $\int \frac{1 + \sin x}{1 + \cos x} e^{x} \, dx$

> [!answer]- 原书参考答案（A.3.3 第 6 题，未逐题独立验算）
> **6.** 分子分母都含 $1 + \cos x$，提示把角统一到 $\frac{x}{2} : \frac{1}{1 + \cos x} = \frac{1}{2} \sec^{2} \frac{x}{2}, \frac{\sin x}{1 + \cos x} = \tan \frac{x}{2}$。注意 $\sec^{2} \frac{x}{2}$ 正好可以凑成 $d(\tan \frac{x}{2})$。由半角公式
>
> $$\frac{1+\sin x}{1+\cos x}=\frac{1}{2}\sec^{2}\frac{x}{2}+\tan\frac{x}{2}.$$
>
> 因此
>
> $$\int\frac{1+\sin x}{1+\cos x}e^{x}\mathrm{d}x=\int e^{x}\left(\frac{1}{2}\sec^{2}\frac{x}{2}+\tan\frac{x}{2}\right)\mathrm{d}x.$$
>
> 注意到
>
> $$\mathrm{d}\left(\tan\frac{x}{2}\right)=\frac{1}{2}\sec^{2}\frac{x}{2}\mathrm{d}x,$$
>
> 所以
>
> $$\int e^{x}\left(\frac{1}{2}\sec^{2}\frac{x}{2}+\tan\frac{x}{2}\right)\mathrm{d}x=\int e^{x}\mathrm{d}\left(\tan\frac{x}{2}\right)+\int e^{x}\tan\frac{x}{2}\mathrm{d}x.$$
>
> 对第一项分部积分：
>
> $$\int e^{x}\mathrm{d}\left(\tan\frac{x}{2}\right)=e^{x}\tan\frac{x}{2}-\int e^{x}\tan\frac{x}{2}\mathrm{d}x.$$
>
> 代回即得
>
> $$\int\frac{1+\sin x}{1+\cos x}e^{x}\mathrm{d}x=e^{x}\tan\frac{x}{2}+C.$$
>
> （也可直接看出
>
> $$\mathrm{d}\left(e^{x}\tan\frac{x}{2}\right)=e^{x}\left(\tan\frac{x}{2}+\frac{1}{2}\sec^{2}\frac{x}{2}\right)\mathrm{d}x,$$
>
> 恰好等于被积表达式.）这里的两项并不是分别积分,而是合起来恰好是一个乘积的导数.遇到「和式」不能硬拆时,先试着把整体写成 $(fg)^{\prime}$的形状,往往一步就能看出来.此外,能直接凑微分时不必额外换元.

## 3.2 定积分

### 3.2.1 借助函数性质及换元计算

定积分的计算, 相比于不定积分, 多了对于函数性质本身的考虑, 对称性、周期性的应用与区间再现的处理, 是常见且重要的考察方向.

**1.** 计算下列定积分

(1) (难度: ★★★) $\int_{0}^{\frac{\pi}{2}}\ln\sin x\,dx$

(2) (难度: ★★★) $\int_{0}^{1}\frac{\ln(x+1)}{x^{2}+1}dx$

(3) (难度: ★★) $\int_{0}^{+\infty}\frac{\ln x}{x^{2}+a^{2}}dx$

(4) (难度: ★★) $\int_{-\pi}^{\pi}\frac{x\sin x\arctan e^{x}}{1+\cos^{2}x}\mathrm{d}x$

> [!answer]- 原书参考答案（A.3.4 第 1 题，未逐题独立验算）
> **1.** (1) 记 $I = \int_{0}^{\pi/2} \ln \sin x \, dx$. 作区间再现 $x = \frac{\pi}{2} - t$，由 $\sin\left(\frac{\pi}{2} - t\right) = \cos t$ 得
>
> $$I=\int_{0}^{\pi/2}\ln\cos t\mathrm{d}t=\int_{0}^{\pi/2}\ln\cos x\mathrm{d}x.$$
>
> 把两式相加：
>
> $$2I=\int_{0}^{\pi/2}\ln(\sin x\cos x)\mathrm{d}x=\int_{0}^{\pi/2}\left(\ln\sin2x-\ln2\right)\mathrm{d}x.$$
>
> 其中
>
> $$\int_{0}^{\pi/2}\ln\sin2x\mathrm{d}x\overset{u=2x}{=}\frac{1}{2}\int_{0}^{\pi}\ln\sin u\mathrm{d}u=\frac{1}{2}\cdot2\int_{0}^{\pi/2}\ln\sin u\mathrm{d}u=I,$$
>
> 这里用了 $\sin(\pi-u)=\sin u$.于是
>
> $$2I=I-\frac{\pi}{2}\ln2\quad\Longrightarrow\quad I=-\frac{\pi}{2}\ln2.$$
>
> (2) 分母 $x^2 + 1$ 是三角代换 $x = \tan t$ 的典型信号; 换元后区间变成 $\left[0, \frac{\pi}{4}\right]$, 且被积式化为 $\ln(1 + \tan t)$, 这正是区间再现 $t \to \frac{\pi}{4} - t$ 最擅长处理的结构. 令 $x = \tan t$, 则 $\mathrm{d}x = \sec^2 t \, \mathrm{d}t$, $x: 0 \to 1$ 对应 $t: 0 \to \frac{\pi}{4}$, 于是
>
> $$I=\int_{0}^{1}\frac{\ln(1+x)}{1+x^{2}}\mathrm{d}x=\int_{0}^{\pi/4}\ln(1+\tan t)\mathrm{d}t.$$
>
> 作区间再现 $t \rightarrow \frac{\pi}{4} - t$ 。利用
>
> $$\tan\left(\frac{\pi}{4}-t\right)=\frac{1-\tan t}{1+\tan t},\qquad1+\tan\left(\frac{\pi}{4}-t\right)=\frac{2}{1+\tan t},$$
>
> 得 $\ln\left(1+\tan\left(\frac{\pi}{4}-t\right)\right)=\ln2-\ln(1+\tan t)$，于是
>
> $$I=\int_{0}^{\pi/4}\left[\ln2-\ln(1+\tan t)\right]\mathrm{d}t=\frac{\pi}{4}\ln2-I.$$
>
> 故 $I=\frac{\pi}{8}\ln2$ 。另一条路线是令 $x=\frac{1-t}{1+t}$，它把区间 $[0,1]$ 仍映到 $[0,1]$，并把 $1+x$、 $1+x^{2}$ 同时简化。两种做法本质相同：都是把积分「复原为自己」，再与原式联立。
>
> (3) 第一步：换元 x = at，把参数从对数里拆出来。由 $\ln x = \ln a + \ln t$ 、dx = a dt、 $x^{2} + a^{2} = a^{2}(1 + t^{2})$
>
> $$\int_{0}^{+\infty}\frac{\ln x}{x^{2}+a^{2}}\mathrm{d}x=\frac{1}{a}\left[\ln a\int_{0}^{+\infty}\frac{\mathrm{d}t}{1+t^{2}}+\int_{0}^{+\infty}\frac{\ln t}{1+t^{2}}\mathrm{d}t\right].$$
>
> 第二步：算两个标准积分. $\int_{0}^{+\infty}\frac{dt}{1+t^{2}}=\frac{\pi}{2}$; 第二个积分作 $t\to\frac{1}{t}$变成自身的相反数，故
>
> $$\int_{0}^{+\infty}\frac{\ln t}{1+t^{2}}\mathrm{d}t=\int_{0}^{+\infty}\frac{-\ln t}{1+t^{2}}\mathrm{d}t=0.$$
>
> 第三步: 写出结果. $\int_{0}^{+\infty}\frac{\ln x}{x^{2}+a^{2}}dx=\frac{\pi\ln a}{2a}$ (a>0). (4) 把被积函数记作 $f(x)$. 它既非奇函数也非偶函数, 但区间关于原点对称, 于是先算 $f(x)+f(-x)$:
>
> $$f(x)+f(-x)=\frac{x\sin x}{1+\cos^{2}x}\left(\arctan e^{x}+\arctan e^{-x}\right).$$
>
> 当 t > 0 时 $\arctan t + \arctan \frac{1}{t} = \frac{\pi}{2}$，取 $t = e^{x}$ 得
>
> $$f(x)+f(-x)=\frac{\pi}{2}\cdot\frac{x\sin x}{1+\cos^{2}x}.$$
>
> 于是
>
> $$\int_{-\pi}^{\pi}f(x)\mathrm{d}x=\frac{\pi}{2}\int_{0}^{\pi}\frac{x\sin x}{1+\cos^{2}x}\mathrm{d}x.$$
>
> 记 $J = \int_{0}^{\pi} \frac{x \sin x}{1 + \cos^{2} x} \, dx$，作区间再现 $x = \pi - t$:
>
> $$J=\int_{0}^{\pi}\frac{\left(\pi-t\right)\sin t}{1+\cos^{2}t}\mathrm{d}t=\pi\int_{0}^{\pi}\frac{\sin x}{1+\cos^{2}x}\mathrm{d}x-J.$$
>
> 而
>
> $$\int_{0}^{\pi}\frac{\sin x}{1+\cos^{2}x}\mathrm{d}x\stackrel{u=\cos x}{=}\int_{-1}^{1}\frac{\mathrm{d}u}{1+u^{2}}=\frac{\pi}{2},$$
>
> 故 $2J = \pi \cdot \frac{\pi}{2} = \frac{\pi^{2}}{2}$，即 $J = \frac{\pi^{2}}{4}$。代回得
>
> $$\int_{-\pi}^{\pi}\frac{x\sin x\arctan e^{x}}{1+\cos^{2}x}\mathrm{d}x=\frac{\pi}{2}\cdot\frac{\pi^{2}}{4}=\frac{\pi^{3}}{8}.$$

**2.** (难度:★★★★)对于正整数 n, 计算定积分 $\int_{e^{-2n\pi}}^{1}\left|\frac{\mathrm{d}(\cos\ln\frac{1}{x})}{\mathrm{d}x}\right|\mathrm{d}x$.

> [!answer]- 原书参考答案（A.3.4 第 2 题，未逐题独立验算）
> **2.** 被积函数是对一个复合函数求导后取绝对值, 先把导数算出来, 再看它是否恰好是某个换元的「配套因子」. 记 $y = \cos \ln \frac{1}{x}$. 由链式法则
>
> $$y^{\prime}=-\sin\ln\frac{1}{x}\cdot\left(\ln\frac{1}{x}\right)^{\prime}=-\sin\ln\frac{1}{x}\cdot\left(-\frac{1}{x}\right)=\frac{1}{x}\sin\ln\frac{1}{x},$$
>
> 故被积函数为 $\left|y'\right| = \frac{1}{x} \left|\sin \ln \frac{1}{x}\right|$。令 $u = \ln \frac{1}{x}$，则 $du = -\frac{dx}{x}$，且 $x = e^{-2n\pi}$ 对应 $u = 2n\pi, x = 1$ 对应 u = 0。于是
>
> $$\int_{e^{-2n\pi}}^{1}\frac{1}{x}\left|\sin\ln\frac{1}{x}\right|\mathrm{d}x=\int_{0}^{2n\pi}\left|\sin u\right|\mathrm{d}u.$$
>
> 区间 $[0,2n\pi]$ 恰好含 $n$ 个 $\sin u$ 的完整周期，而 $\int_{0}^{2\pi}|\sin u|\,\mathrm{d}u=4$，所以原积分的值为 $4n$。本题的「绝对值」恰好被换元后的周期结构吃掉：换元把被积式化为 $\sin u$， $\left[\frac{1}{x}\sin\ln\frac{1}{x}\right]$ 变成 $\sin u$，把长度不规则的区间变成整数个周期，这是处理周期被积函数的标准套路。

**3.** (难度:★★★★) 求函数 $f(x) = e^{-2x} \sin x$ (x > 0) 与 x 轴正半轴所围的封闭图形的面积.

> [!answer]- 原书参考答案（A.3.4 第 3 题，未逐题独立验算）
> **3.** 面积就是 $\left|y\right|$ 在 $(0,+\infty)$ 上的积分. 零点为 $x=k\pi\left(k=0,1,2,\cdots\right)$, 在 $(k\pi,(k+1)\pi)$ 上 $\sin x$ 的符号为 $(-1)^{k}$, 故
>
> $$S=\sum_{k=0}^{\infty}\int_{k\pi}^{(k+1)\pi}e^{-2x}|\sin x|\mathrm{d}x.$$
>
> 对第 $k$ 段作平移 $t = x - k\pi$，则 $|\sin x| = |\sin t|$，而 $e^{-2x} = e^{-2k\pi}e^{-2t}$，于是每一段都化归到同一个基本积分：
>
> $$\int_{k\pi}^{(k+1)\pi}e^{-2x}|\sin x|\mathrm{d}x=e^{-2k\pi}\int_{0}^{\pi}e^{-2t}\sin t\mathrm{d}t.$$
>
> 其中
>
> $$\int_{0}^{\pi}e^{-2t}\sin t\mathrm{d}t=\left.\frac{e^{-2t}(-2\sin t-\cos t)}{5}\right|_{0}^{\pi}=\frac{1+e^{-2\pi}}{5}.$$
>
> 常数因子只与 k 有关，可以提到求和号外，于是
>
> $$S=\frac{1+e^{-2\pi}}{5}\sum_{k=0}^{\infty}e^{-2k\pi}=\frac{1+e^{-2\pi}}{5}\cdot\frac{1}{1-e^{-2\pi}}=\frac{1}{5}\cdot\frac{1+e^{-2\pi}}{1-e^{-2\pi}}.$$

**4.** (难度：★★★★★) 对于正数 $\alpha$, 判断反常积分 $\int_{0}^{+\infty}\frac{x}{\cos^{2}x+x^{\alpha}\sin^{2}x}dx$ 的敛散性.

> [!answer]- 原书参考答案（A.3.4 第 4 题，未逐题独立验算）
> **4.** 记 $I = \int_{0}^{+\infty} \frac{x \, dx}{\cos^2 x + x^\alpha \sin^2 x} \, (\alpha > 0)$. 这里 $x$ 与 $x^\alpha$ 相对 $\sin^2, \cos^2$ 是缓慢变化的，于是按「分段求主部」处理.
>
> 第一步: 在每个长度为 $\pi$ 的段上把 $x, x^{\alpha}$ 看成常数. 在 $[k\pi, (k+1)\pi]$ 上取 $x \approx k\pi$, 记 $b = (k\pi)^{\alpha} > 0$, 则
>
> $$I_{k}:=\int_{k\pi}^{(k+1)\pi}\frac{x\mathrm{d}x}{\cos^{2}x+x^{\alpha}\sin^{2}x}\approx k\pi\int_{0}^{\pi}\frac{\mathrm{d}\theta}{\cos^{2}\theta+b\sin^{2}\theta}.$$
>
> 由标准值 $\int_{0}^{\pi}\frac{\mathrm{d}\theta}{\cos^{2}\theta+b\sin^{2}\theta}=\frac{\pi}{\sqrt b}$（$\tan\theta$ 换元即得），得
>
> $$I_{k}\approx\frac{k\pi\cdot\pi}{\sqrt{(k\pi)^{\alpha}}}=\pi^{2-\frac{\alpha}{2}}k^{1-\frac{\alpha}{2}}.$$
>
> 第二步: 比较判别. 被积函数在每个 $[k\pi,(k+1)\pi]$ 上连续, 且 $x$、 $x^{\alpha}$ 在段内的相对变化不超过 $O(1/k)$, 故存在与 k 无关的 $c_2 \geq c_1 > 0$ 使
>
> $$c_{1}k^{1-\frac{\alpha}{2}}\leqslant I_{k}\leqslant c_{2}k^{1-\frac{\alpha}{2}}\qquad(k 充分大 ),$$
>
> 于是 $I = \sum_{k \geq 0} I_{k}$ 与 $\sum k^{1 - \frac{\alpha}{2}}$ 同敛散.
>
> 第三步: 结论. $\sum k^{1-\frac{\alpha}{2}}$ 收敛当且仅当 $\frac{\alpha}{2}-1>1$, 即
>
> $\alpha>4$ 时收敛； $0<\alpha\leq4$ 时发散.

### 3.2.2 费曼积分法

用含参积分的求导公式间接求解积分, 可用于解决部分用常规方法无法计算的定积分.

**1.** 计算下列定积分

(1) (难度: ★★★★) $\int_{0}^{\pi}\ln(2+\cos x)dx$

(2) (难度: ★★★★) $\int_{0}^{+\infty}\frac{\sin x}{x}dx$

> [!answer]- 原书参考答案（A.3.5 第 1 题，未逐题独立验算）
> **1.** (1) 对数内部没有分母，只能把参数设进真数里. 令
>
> $$F(a)=\int_{0}^{\pi}\ln(a+\cos x)\mathrm{d}x,\qquad a>1,$$
>
> 所求为 $F(2)$. 对 a 求导:
>
> $$F^{\prime}(a)=\int_{0}^{\pi}\frac{\mathrm{d}x}{a+\cos x}\overset{t=\tan\frac{x}{2}}{=}\int_{0}^{+\infty}\frac{2\mathrm{d}t}{(a+1)+(a-1)t^{2}}=\frac{\pi}{\sqrt{a^{2}-1}}.$$
>
> 于是
>
> $$F(a)=\pi\ln\left(a+\sqrt{a^{2}-1}\right)+C.$$
>
> 为定出 C, 令 a = 1. 此时
>
> $$F(1)=\int_{0}^{\pi}\ln(1+\cos x)\mathrm{d}x.$$
>
> 利用 $1 + \cos x = 2 \cos^{2} \frac{x}{2}$，得
>
> $$F(1)=\int_{0}^{\pi}\left[\ln2+2\ln\left(\cos\frac{x}{2}\right)\right]\mathrm{d}x=\pi\ln2+2\int_{0}^{\pi}\ln\left(\cos\frac{x}{2}\right)\mathrm{d}x.$$
>
> 令 $u = \frac{x}{2}$，则 $\mathrm{d}x = 2\mathrm{d}u$，且 $x: 0 \to \pi$ 对应 $u: 0 \to \frac{\pi}{2}$，所以
>
> $$\int_{0}^{\pi}\ln\left(\cos\frac{x}{2}\right)\mathrm{d}x=2\int_{0}^{\pi/2}\ln(\cos u)\mathrm{d}u.$$
>
> 这里用到经典积分
>
> $$\int_{0}^{\pi/2}\ln(\sin u)\mathrm{d}u=\int_{0}^{\pi/2}\ln(\cos u)\mathrm{d}u=-\frac{\pi}{2}\ln2,$$
>
> 其中第一个等号由 $u \mapsto \frac{\pi}{2} - u$ 的对称性得到，该积分之前已经讨论并计算过。因此
>
> $$\int_{0}^{\pi}\ln\left(\cos\frac{x}{2}\right)\mathrm{d}x=2\left(-\frac{\pi}{2}\ln2\right)=-\pi\ln2.$$
>
> 于是
>
> $$F(1)=\pi\ln2+2(-\pi\ln2)=-\pi\ln2.$$
>
> 又由 $F(a)=\pi\ln\left(a+\sqrt{a^{2}-1}\right)+C$ , 当 a=1 时
>
> $$F(1)=\pi\ln1+C=C.$$
>
> 故 $C = -\pi\ln2$. 从而
>
> $$F(a)=\pi\ln\frac{a+\sqrt{a^{2}-1}}{2},\qquad\int_{0}^{\pi}\ln(2+\cos x)\mathrm{d}x=\pi\ln\frac{2+\sqrt{3}}{2}.$$
>
> (2) 被积函数本身不是绝对收敛的, 直接设参会遇到收敛性麻烦, 于是乘上收敛因子 $e^{-ax}$:
>
> $$F(a)=\int_{0}^{+\infty}e^{-ax}\frac{\sin x}{x}\mathrm{d}x,\qquad a\geqslant0,$$
>
> 则 F(0) 就是所求积分. 对 a 求导 (只对 $e^{-ax}$ 求导):
>
> $$F^{\prime}(a)=-\int_{0}^{+\infty}e^{-ax}\sin x\mathrm{d}x=-\frac{1}{1+a^{2}}.$$
>
> 积分得 $F(a) = -\arctan a + C$. 又 $a \to +\infty$ 时 $F(a) \to 0$, 而 $-\arctan a \to -\frac{\pi}{2}$, 故 $C = \frac{\pi}{2}$, 即
>
> $$F(a)=\frac{\pi}{2}-\arctan a.$$
>
> 令a=0得
>
> $$\int_{0}^{+\infty}\frac{\sin x}{x}\mathrm{d}x=F(0)=\frac{\pi}{2}.$$
>
> 最后补上 $F(+\infty)=0$ 的理由: 由 $\left|\frac{\sin x}{x}\right|\leq1$ 得
>
> $$|F(a)|\leqslant\int_{0}^{+\infty}e^{-ax}\mathrm{d}x=\frac{1}{a}\to0\qquad(a\to+\infty),$$
>
> 这正是「夹逼放缩成 $\frac{1}{a}$」

**2.** (难度:★★★) 已知 $\alpha > 0$, 计算不定积分 $\int_{0}^{+\infty} \frac{2 \arctan \alpha x}{x (x^{2} + 1)} \, dx$.

> [!answer]- 原书参考答案（A.3.5 第 2 题，未逐题独立验算）
> **2.** 把 $\alpha$ 看成参数，令
>
> $$F(\alpha)=\int_{0}^{+\infty}\frac{2\arctan(\alpha x)}{x\left(x^{2}+1\right)}\mathrm{d}x,\qquad F(0)=0.$$
>
> 对 $\alpha$ 求导，被积函数中只有 $\arctan(\alpha x)$ 含 $\alpha$:
>
> $$F^{\prime}(\alpha)=\int_{0}^{+\infty}\frac{2x}{1+\alpha^{2}x^{2}}\cdot\frac{1}{x\left(x^{2}+1\right)}\mathrm{d}x=\int_{0}^{+\infty}\frac{2\mathrm{d}x}{\left(1+x^{2}\right)\left(1+\alpha^{2}x^{2}\right)}.$$
>
> 把有理式拆开：
>
> $$\frac{2}{\left(1+x^{2}\right)\left(1+\alpha^{2}x^{2}\right)}=\frac{2}{1-\alpha^{2}}\left(\frac{1}{1+x^{2}}-\frac{\alpha^{2}}{1+\alpha^{2}x^{2}}\right),$$
>
> 于是
>
> $$F^{\prime}(\alpha)=\frac{2}{1-\alpha^{2}}\left(\frac{\pi}{2}-\alpha^{2}\cdot\frac{\pi}{2\alpha}\right)=\frac{\pi}{1-\alpha^{2}}(1-\alpha)=\frac{\pi}{1+\alpha}.$$
>
> （$\alpha=1$ 时按极限理解, 结论不变.) 积分得 $F(\alpha)=\pi\ln(1+\alpha)+C$, 由 $F(0)=0$ 得 $C=0$, 故
>
> $$\int_{0}^{+\infty}\frac{2\arctan\alpha x}{x\left(x^{2}+1\right)}\mathrm{d}x=\pi\ln(1+\alpha).$$

**3.** (难度: ★★★★★) 计算定积分 $\int_{0}^{1}\frac{\ln(x+\sqrt{1-x^{2}})}{x}dx$.

> [!answer]- 原书参考答案（A.3.5 第 3 题，未逐题独立验算）
> **3.** 被积式中 $x + \sqrt{1 - x^2}$ 提示三角换元 $x = \sin t$; 换元后出现 $\cot t$, 于是区间再现 $t \to \frac{\pi}{2} - t$ 会把 $\cot t$ 补成 $\cot t + \tan t = \frac{1}{\sin t \cos t}$, 正好凑出 $\frac{\ln(1 + \sin 2t)}{\sin 2t}$ 这一「费曼型」结构. 令 $x = \sin t$ $(0 \leq t \leq \frac{\pi}{2})$, 则 $\frac{dx}{x} = \cot t \, dt$, 且 $x + \sqrt{1 - x^2} = \sin t + \cos t$. 于是
>
> $$I=\int_{0}^{\pi/2}\ln(\sin t+\cos t)\cot t\mathrm{d}t.$$
>
> 作区间再现 $t \to \frac{\pi}{2} - t$, $\cot$ 与 $\tan$ 互换而 $\sin t + \cos t$ 不变, 故
>
> $$I=\int_{0}^{\pi/2}\ln(\sin t+\cos t)\tan t\mathrm{d}t.$$
>
> 两式相加：
>
> $$2I=\int_{0}^{\pi/2}\ln(\sin t+\cos t)\left(\tan t+\cot t\right)\mathrm{d}t=\int_{0}^{\pi/2}\frac{\ln(\sin t+\cos t)}{\sin t\cos t}\mathrm{d}t.$$
>
> 利用 $(\sin t + \cos t)^{2} = 1 + \sin 2t$ 与 $\sin t \cos t = \frac{1}{2} \sin 2t$:
>
> $$2I=\int_{0}^{\pi/2}\frac{\frac{1}{2}\ln(1+\sin2t)}{\frac{1}{2}\sin2t}\mathrm{d}t=\int_{0}^{\pi/2}\frac{\ln(1+\sin2t)}{\sin2t}\mathrm{d}t.$$
>
> 令 u = 2t，则 $2I = \frac{1}{2} \int_{0}^{\pi} \frac{\ln(1 + \sin u)}{\sin u} \, \mathrm{d}u$。而练习 3.2 的结论给出 $\int_{0}^{\pi} \frac{\ln(1 + \sin u)}{\sin u} \, \mathrm{d}u = \frac{\pi^{2}}{4}$，故 $2I = \frac{\pi^{2}}{8}$，即 $I = \frac{\pi^{2}}{16}$。本题是「三角换元 + 区间再现 + 费曼积分」三步连用的典型。值得注意的是最后一步所用的积分就是练习 3.2 的 $\int_{0}^{\pi} \frac{\ln(1 + \sin x)}{\sin x} \, \mathrm{d}x = \frac{\pi^{2}}{4}$，它本身要靠费曼积分法（把参数设进 $\ln$ 的真数）才能算出。

### 3.2.3 递推积分

以数列的角度看待定积分,也是常见的处理思路之一,此处仅列举几例相当典型的递推积分,对于递推积分的处理,核心是找到相邻项之间的关系,进而对积分进行估阶和计算.

**1.** 对于正整数 n，寻找下列递推积分相邻几项之间满足的函数关系.

(1) (难度: ★★) $I_{n} = \int_{0}^{\frac{\pi}{2}} \sin^{n} x \, dx$

(2) (难度:★★) $J_{n} = \int_{0}^{\frac{\pi}{2}} \tan^{n} x \, dx$

(3) (难度: ★★★★) $K_{n} = \int_{0}^{\frac{\pi}{2}} \sin nx \cos^{n} x \, dx$

> [!answer]- 原书参考答案（A.3.6 第 1 题，未逐题独立验算）
> **1.** (1) 把 $\sin^{n}x$ 拆成 $\sin^{n-1}x \cdot \sin x$，分部积分:
>
> $$I_{n}=\int_{0}^{\pi/2}\sin^{n-1}x\mathrm{d}(-\cos x)=(n-1)\int_{0}^{\pi/2}\sin^{n-2}x\cos^{2}x\mathrm{d}x.$$
>
> 边界项为零（两端都含因子 $\cos x$ 或被积式为零），再用 $\cos^{2}x = 1 - \sin^{2}x$:
>
> $$I_{n}=(n-1)\left(I_{n-2}-I_{n}\right)\quad\Longrightarrow\quad n I_{n}=(n-1)I_{n-2},$$
>
> 即 $I_{n}=\frac{n-1}{n}I_{n-2}$ (n≥2). 由 $I_{0}=\frac{\pi}{2}$、 $I_{1}=1$ 连乘得
>
> $$I_{2m}=\frac{(2m-1)!!}{(2m)!!}\cdot\frac{\pi}{2},\qquad I_{2m+1}=\frac{(2m)!!}{(2m+1)!!},$$
>
> 这就是华里士（Wallis）公式.
>
> (2) 由递推式可得
>
> $$nI_{n}I_{n-1}=\left(n-1\right)I_{n-1}I_{n-2}=\cdots=I_{1}I_{0}=\frac{\pi}{2},$$
>
> 即 $I_{n}I_{n-1}=\frac{\pi}{2n}$ 恒成立. 另一方面, 在 $\left(0,\frac{\pi}{2}\right)$ 上 $0\leqslant\sin x\leqslant1$, 故 $\sin^{n}x\leqslant\sin^{n-1}x\leqslant\sin^{n-2}x$, 逐项积分得
>
> $$I_{n}\leqslant I_{n-1}\leqslant I_{n-2}=\frac{n}{n-1}I_{n}.$$
>
> 代入 $I_{n}I_{n-1}=\frac{\pi}{2n}$:
>
> $$I_{n}^{2}\leqslant\frac{\pi}{2n}\leqslant I_{n}I_{n-2}=\frac{n}{n-1}I_{n}^{2},$$
>
> 即 $\frac{n-1}{n} \cdot \frac{\pi}{2n} \leqslant I_n^2 \leqslant \frac{\pi}{2n}$. 两端同乘以 $n$ 后都趋于 $\frac{\pi}{2}$, 由夹逼定理得 $nI_n^2 \to \frac{\pi}{2}$, 即
>
> $$\lim_{n\to\infty}\sqrt{n}I_{n}=\sqrt{\frac{\pi}{2}}.$$
>
> 把它写回双阶乘，就得到一个重要的极限式：
>
> $$\lim_{m\to\infty}\sqrt{m}\frac{(2m-1)!!}{(2m)!!}=\frac{1}{\sqrt{\pi}}.$$
>
> (2) 记 $J_{n} = \int_{0}^{\pi/2} \tan^{n} x \, dx$. 先在 $[0, X] (X < \pi/2)$ 上算相邻两项的关系，再让 $X \to \frac{\pi}{2}$ 讨论敛散.
>
> 第一步:相邻两项相加会凑出 $\sec^{2}x$.
>
> $$\int_{0}^{X}\left(\tan^{n}x+\tan^{n-2}x\right)\mathrm{d}x=\int_{0}^{X}\tan^{n-2}x\mathrm{d}\left(\tan x\right)=\frac{\tan^{n-1}X}{n-1}\qquad(n\geqslant2).$$
>
> 即 $J_{n}(X) + J_{n-2}(X) = \frac{\tan^{n-1}X}{n-1}$.
>
> 第二步: 判断敛散. $x \to \frac{\pi}{2}^{-}$ 时 $\tan x \sim \left(\frac{\pi}{2} - x\right)^{-1}$, 故 $\tan^{n} x \sim \left(\frac{\pi}{2} - x\right)^{-n}$, 于是
>
> $$\left\{\begin{aligned}&\int_{0}^{\pi/2}\tan^{n}x\mathrm{d}x=\frac{\pi}{2},&n=0;\\ & 发散 ,&n\geqslant1.\\ \end{aligned}\right.$$
>
> 所以对 $n \geqslant 2$ 第一步的关系式在 $X \to \frac{\pi}{2}$ 时两端同时趋于 $+\infty$，只能保留有限形式
>
> $$\int_{0}^{X}\left(\tan^{n}x+\tan^{n-2}x\right)\mathrm{d}x=\frac{\tan^{n-1}X}{n-1}.$$
>
> 第三步：与标准形态对照. 若把上限改成 $\frac{\pi}{4}$，则递推关系变成干净的
>
> $$\int_{0}^{\pi/4}\left(\tan^{n}x+\tan^{n-2}x\right)\mathrm{d}x=\frac{1}{n-1}\qquad(n\geqslant2).$$
>
> (3) $K_{n}$ 的被积式里 $\sin nx$ 与 $\cos^{n}x$ 的「幂次」相同，用 $\sin nx = \sin(n-1)x \cos x + \cos(n-1)x \sin x$ 拆开后，第二块恰好能凑 $d(\cos^{n+1}x)$ 做分部；第一块记为 $A_{n} = \int_{0}^{\pi/2} \sin(n-1)x \cos^{n+1}x \, dx$，再用积化和差把 $A_{n}$ 与 $A_{n-1}$ 联系起来。由 $\sin nx = \sin(n-1)x \cos x + \cos(n-1)x \sin x$，
>
> $$K_{n}=A_{n}+I_{2},$$
>
> 其中
>
> $$A_{n}=\int_{0}^{\pi/2}\sin(n-1)x\cos^{n+1}x\mathrm{d}x,\qquad I_{2}=\int_{0}^{\pi/2}\cos(n-1)x\sin x\cos^{n}x\mathrm{d}x.$$
>
> 对 $I_{2}$ 分部积分 (取 $\mathrm{d}v = \sin x \cos^{n} x \, \mathrm{d}x, v = -\frac{\cos^{n+1}x}{n+1}$):
>
> $$I_{2}=\frac{1}{n+1}-\frac{n-1}{n+1}A_{n},$$
>
> （边界项为 $\frac{1}{n+1}$，因为 $\cos^{n+1}\frac{\pi}{2}=0$、 $\cos0\cdot\cos^{n+1}0=1$）. 故
>
> $$K_{n}=A_{n}+\frac{1}{n+1}-\frac{n-1}{n+1}A_{n}=\frac{1+2A_{n}}{n+1}.$$
>
> 再对 $A_{n}$ 用积化和差
>
> $$\sin(n-1)x\cos x=\frac{1}{2}\left[\sin nx+\sin(n-2)x\right],$$
>
> 得
>
> $$A_{n}=\frac{1}{2}\int_{0}^{\pi/2}\left[\sin nx+\sin(n-2)x\right]\cos^{n}x\mathrm{d}x=\frac{1}{2}\left(K_{n}+A_{n-1}\right),$$
>
> 其中第二个积分的被积式正是 $A_{n-1}$. 把 $2A_{n} = K_{n} + A_{n-1}$ 代入 (*) 得 $nK_{n} = 1 + A_{n-1}$, 再由 n-1 处的 (*) 有
>
> $$A_{n-1}=\frac{nK_{n-1}-1}{2},$$
>
> 于是
>
> $$nK_{n}=1+\frac{nK_{n-1}-1}{2}\quad\Longrightarrow\quad2nK_{n}=nK_{n-1}+1,$$
>
> 即
>
> $$K_{n}=\frac{1}{2}\left(K_{n-1}+\frac{1}{n}\right),\qquad K_{1}=\frac{1}{2}.$$
>
> 可直接验证：
>
> $$K_{2}=\frac{1}{2}\left(\frac{1}{2}+\frac{1}{2}\right)=\frac{1}{2},\qquad K_{3}=\frac{1}{2}\left(\frac{1}{2}+\frac{1}{3}\right)=\frac{5}{12},$$
>
> 与直接计算一致. 由递推式还能解出通项
>
> $$K_{n}=\frac{1}{2^{n-1}}K_{1}+\sum_{k=2}^{n}\frac{1}{2^{n-k+1}k}.$$

---

# 基础篇·第四章 微分方程

## 4.1 一阶微分方程

一阶微分方程的整体难度较低，主要把不同种类微分方程的主流解法即可，算是基础送分题。

### 4.1.1 可分离变量的微分方程

**1.** (难度: ★) $y' + \sin \frac{x + y}{2} = \sin \frac{x - y}{2}$

> [!answer]- 原书参考答案（A.4.1 第 1 题，未逐题独立验算）
> 1\. 移项并用和差化积公式：
>
> $$y^{\prime}=\sin\frac{x-y}{2}-\sin\frac{x+y}{2}=-2\cos\frac{x}{2}\sin\frac{y}{2}.$$
>
> 右端可以拆成「只含 x」与「只含 y」两部分的乘积, 故方程可分离变量. 当 $\sin\frac{y}{2}\neq0$ 时,
>
> $$\frac{\mathrm{d}y}{\sin\frac{y}{2}}=-2\cos\frac{x}{2}\mathrm{d}x.$$
>
> 两边积分，左端作代换 $v=\frac{y}{2}$ 得
>
> $$\int\frac{\mathrm{d}y}{\sin\frac{y}{2}}=2\ln\left|\tan\frac{y}{4}\right|,$$
>
> 右端为 $-4\sin\frac{x}{2}$，于是
>
> $$\tan\frac{y}{4}=k e^{-2\sin\frac{x}{2}}\qquad(k\neq0).$$
>
> 另外, 当 $\sin \frac{y}{2} = 0$ 即 $y = 2m\pi$ ( $m \in \mathbb{Z}$) 时, $y' \equiv 0$, 等式两端同为 0, 故 $y \equiv 2m\pi$ 也都是解.

**2.** (难度:★★) $y' + \frac{y}{x} = y^{2} - \frac{4}{x^{2}}$

> [!answer]- 原书参考答案（A.4.1 第 2 题，未逐题独立验算）
> **2.** 左端含 $y' + \frac{y}{x}$，把它整体凑成 $\frac{(xy)'}{x}$：两边同乘 x，得
>
> $$xy^{\prime}+y=x\left(y^{2}-\frac{4}{x^{2}}\right)=xy^{2}-\frac{4}{x}.$$
>
> 令 u = xy，则 $u' = xy' + y$，且 $xy^{2} = \frac{(xy)^{2}}{x} = \frac{u^{2}}{x}$，代入得
>
> $$u^{\prime}=\frac{u^{2}-4}{x}\quad\Longrightarrow\quad\frac{\mathrm{d}u}{u^{2}-4}=\frac{\mathrm{d}x}{x}.$$
>
> 由 $\frac{1}{u^{2}-4}=\frac{1}{4}\left(\frac{1}{u-2}-\frac{1}{u+2}\right)$，积分得
>
> $$\frac{1}{4}\ln\left|\frac{u-2}{u+2}\right|=\ln x+C,$$
>
> 即通解
>
> $$\frac{xy-2}{xy+2}=kx^{4}\qquad(k\neq0).$$
>
> 另外 $u = \pm 2$ 给出 $y = \pm \frac{2}{x}$，代入原方程可知它们也是解.

**3.** (难度:★★) $\frac{dy}{dx} = \frac{3x^{2} + y^{2} - 6x + 3}{2xy - 2y}$

> [!answer]- 原书参考答案（A.4.1 第 3 题，未逐题独立验算）
> **3.** 分子 $3x^{2}+y^{2}-6x+3=3(x-1)^{2}+y^{2}$，分母 2y (x-1). 令 u = x-1、v = y，方程就是齐次的；再把 $v^{2}$ 看成整体，就变成线性方程. 令 u = x-1、v = y，则 $\frac{dv}{du} = \frac{3u^{2}+v^{2}}{2uv}$，即
>
> $$\frac{\mathrm{d}v}{\mathrm{d}u}=\frac{3u}{2v}+\frac{v}{2u}\quad\Longrightarrow\quad2v\frac{\mathrm{d}v}{\mathrm{d}u}=3u+\frac{v^{2}}{u}.$$
>
> 令 $z = v^{2}$，则 $z' = \frac{3u + z / u}{1}$，即 $z' - \frac{z}{u} = 3u$。两边同乘 $u^{-1}$：
>
> $$\left(\frac{z}{u}\right)^{\prime}=3\quad\Longrightarrow\quad z=3u^{2}+C u.$$
>
> 回代 $z=y^{2}$、u=x-1，得通解
>
> $$y^{2}=3\left(x-1\right)^{2}+C\left(x-1\right).$$
>
> 分式方程先看「分子分母能不能配成关于同一个量的式子」.本题配方后 u、v 同时出现,说明应当把 $v^{2}$ 而不是 v 当作未知函数.

**4.** (难度:★★★) 求在区间 $(0, +\infty)$ 上满足 $f' \left( \frac{1}{x} \right) = \frac{x}{f(x)}$ 的函数 $f(x)$.

> [!answer]- 原书参考答案（A.4.1 第 4 题，未逐题独立验算）
> **4.** 条件中同时出现 x 与 $\frac{1}{x}$，把 x 换成 $\frac{1}{x}$ 得到第二个等式；两个等式联立可造出 $f(x)f\left(\frac{1}{x}\right)$ 这个不变量。题设对一切 x > 0 成立。把 x 换成 $\frac{1}{x}$，得
>
> $$f^{\prime}(x)=\frac{1}{xf\left(\frac{1}{x}\right)}\quad\Longrightarrow\quad f^{\prime}(x)f\left(\frac{1}{x}\right)=\frac{1}{x}.$$
>
> 记 $g(x)=f(x)f\left(\frac{1}{x}\right)$，由（1）与题设 $f'\left(\frac{1}{x}\right)=\frac{x}{f(x)}$ 得
>
> $$g^{\prime}(x)=f^{\prime}(x)f\left(\frac{1}{x}\right)-\frac{1}{x^{2}}f(x)f^{\prime}\left(\frac{1}{x}\right)=\frac{1}{x}-\frac{1}{x^{2}}\cdot x=0,$$
>
> 故 $g(x) \equiv k^{2}$，其中 $k = f(1) \neq 0$。代回 (1):
>
> $$f^{\prime}(x)=\frac{f(x)}{k^{2}x}\quad\Longrightarrow\quad(\ln|f(x)|)^{\prime}=\frac{1}{k^{2}x}\quad\Longrightarrow\quad f(x)=kx^{\frac{1}{k^{2}}}.$$
>
> 代回验证: 由 $f\left(\frac{1}{x}\right)=kx^{-\frac{1}{k^2}}$ 得 $f'(x)f\left(\frac{1}{x}\right)=\frac{1}{x}$，且 $f'\left(\frac{1}{x}\right)=\frac{1}{k}x^{1-\frac{1}{k^2}}=\frac{x}{f(x)}$，两式都成立. 「 $x$与 $\frac{1}{x}$同时出现」的函数方程，标准动作是换元后与原式联立；构造不变量（这里是 $f(x)f\left(\frac{1}{x}\right)$）能把导数条件降成代数条件.

### 4.1.2 齐次微分方程

**1.** (难度：★) $xy' = \sqrt{x^2 - y^2} + y$

> [!answer]- 原书参考答案（A.4.2 第 1 题，未逐题独立验算）
> **1.** 原方程要求 $x^{2}-y^{2} \geqslant 0$ ，即 $\left|y\right| \leqslant \left|x\right|$，且 $x \neq 0$ （否则方程变为 $\sqrt{-y^{2}}+y=0$ ，只能得 y $\leqslant$ 0，不含导数项，不是通常意义的微分方程）。因此定义域为两条射线 x > 0 与 x < 0。
>
> 情形一：x>0. 两边除以x:
>
> $$y^{\prime}=\frac{y}{x}+\sqrt{1-\left(\frac{y}{x}\right)^{2}}.$$
>
> 令 $t=\frac{y}{x}$，则 y=tx、 $y'=t+xt'$，代入得
>
> $$x t^{\prime}=\sqrt{1-t^{2}}\quad\Longrightarrow\quad\frac{\mathrm{d}t}{\sqrt{1-t^{2}}}=\frac{\mathrm{d}x}{x}.$$
>
> 积分得
>
> $$\arcsin t=\ln x+C_{1},$$
>
> 即
>
> $$y=x\sin\left(\ln x+C_{1}\right)\qquad(x>0).$$
>
> 情形二：x<0. 此时 $\sqrt{x^{2}-y^{2}}=|x|\sqrt{1-(y/x)^{2}}=-x\sqrt{1-(y/x)^{2}}$，故
>
> $$\frac{\sqrt{x^{2}-y^{2}}}{x}=-\sqrt{1-\left(\frac{y}{x}\right)^{2}}.$$
>
> 两边除以x后得
>
> $$y^{\prime}=\frac{y}{x}-\sqrt{1-\left(\frac{y}{x}\right)^{2}}.$$
>
> 同样令 $t = \frac{y}{x}$，代入得
>
> $$x t^{\prime}=-\sqrt{1-t^{2}}\quad\Longrightarrow\quad\frac{\mathrm{d}t}{\sqrt{1-t^{2}}}=-\frac{\mathrm{d}x}{x}.$$
>
> 积分得
>
> $$\arcsin t=-\ln|x|+C_{2},$$
>
> 即
>
> $$y=x\sin\left(-\ln|x|+C_{2}\right)\qquad(x<0).$$
>
> 合并．两类情形可统一写为
>
> $$\arcsin\frac{y}{x}=sgn(x)\ln|x|+C,$$
>
> 或者分两段写成
>
> $$y=\left\{\begin{aligned}&x\sin\left(\ln x+C_{1}\right),&&x>0,\\ &x\sin\left(-\ln(-x)+C_{2}\right),&&x<0,\end{aligned}\right.$$
>
> 其中 $C_{1}, C_{2}$为任意常数.
>
> 退化解. 当 $t = \pm1$, 即 y = ±x 时, $\sqrt{1 - t^{2}} = 0$, 容易验证它们也满足原方程, 可单独列出.
>
> 因此原方程的通解为
>
> $$\left\{\begin{array}{l}y=x\sin\left(\ln x+C_{1}\right),\quad x>0,\\ y=x\sin\left(-\ln(-x)+C_{2}\right),\quad x<0,\end{array}\right.\quad 以及 y=\pm x.$$

**2.** (难度:★★) $\frac{dy}{dx} = \frac{x + 2y - 1}{3x + 5y - 2}$

> [!answer]- 原书参考答案（A.4.2 第 2 题，未逐题独立验算）
> **2.** 系数行列式 $\begin{vmatrix}1&2\\ 3&5\end{vmatrix} = -1 \neq 0$，故可作平移。令
>
> $$X=x+A,\qquad Y=y+B,$$
>
> 要求常数项消掉：
>
> $$\begin{aligned}A+2B-1&=0,&3A+5B-2&=0&\Longrightarrow&A&=-1,&B&=1.\end{aligned}$$
>
> 于是 X = x - 1, Y = y + 1, 方程化为齐次方程
>
> $$\frac{\mathrm{d}Y}{\mathrm{d}X}=\frac{X+2Y}{3X+5Y}.$$
>
> 再令 $t = \frac{Y}{X}$，得
>
> $$X\frac{\mathrm{d}t}{\mathrm{d}X}=\frac{1+2t}{3+5t}-t=\frac{1-t-5t^{2}}{3+5t},$$
>
> 分离变量并积分：
>
> $$\int\frac{3+5t}{1-t-5t^{2}}\mathrm{d}t=\ln\left|X\right|+C.$$
>
> 由 $1 - t - 5t^{2} = -5 (t - r_{1}) (t - r_{2})$，其中 $r_{1,2} = \frac{-1 \pm \sqrt{21}}{10}$，可算得
>
> $$-\frac{1}{2}\ln\left|1-t-5t^{2}\right|-\frac{5}{2\sqrt{21}}\ln\left|\frac{t-r_{1}}{t-r_{2}}\right|=\ln|X|+C.$$
>
> 把 $t = \frac{y+1}{x-1}$、X = x - 1 代回即得隐式通解.

**3.** (难度:★★★) $(2x^{3}+3xy^{2}-7x)\mathrm{d}x+(3x^{2}y-2y^{3}+8y)\mathrm{d}y=0$

> [!answer]- 原书参考答案（A.4.2 第 3 题，未逐题独立验算）
> **3.** 先验证是否为全微分方程: 只需比较两个交叉偏导. $P = 2x^{3} + 3xy^{2} - 7x$, Q = $3x^{2}y - 2y^{3} + 8y$, 且
>
> $$\frac{\partial P}{\partial y}=6xy=\frac{\partial Q}{\partial x},$$
>
> 故为全微分方程. 沿折线（自 $(0,0)$）积分：
>
> $$u=\int_{0}^{x}\left(2t^{3}-7t\right)\mathrm{d}t+\int_{0}^{y}\left(3x^{2}s-2s^{3}+8s\right)\mathrm{d}s,$$
>
> 即
>
> $$u=\frac{x^{4}}{2}+\frac{3x^{2}y^{2}}{2}-\frac{7x^{2}}{2}-\frac{y^{4}}{2}+4y^{2}.$$
>
> 两边同乘2，得通解
>
> $$x^{4}+3x^{2}y^{2}-7x^{2}-y^{4}+8y^{2}=C.$$
>
> 全微分方程的积分结果中常数可以任意乘一个非零倍数,答案写成整系数形式更清爽.

### 4.1.3 一阶线性微分方程

**1.** (难度: ★) $y' = -\frac{1 + y^2}{x - \arctan y}$

> [!answer]- 原书参考答案（A.4.3 第 1 题，未逐题独立验算）
> **1.** 把 x 看作 y 的函数, 原式即
>
> $$\frac{\mathrm{d}x}{\mathrm{d}y}=-\frac{x-\arctan y}{1+y^{2}}\quad\Longrightarrow\quad\frac{\mathrm{d}x}{\mathrm{d}y}+\frac{1}{1+y^{2}}x=\frac{\arctan y}{1+y^{2}}.$$
>
> 这是关于 $x(y)$ 的一阶线性方程，积分因子为 $e^{\arctan y}$. 两边同乘它：
>
> $$\left(x e^{\arctan y}\right)^{\prime}=\frac{\arctan y}{1+y^{2}}e^{\arctan y}.$$
>
> 令 $u = \arctan y$，则 $\mathrm{d}u = \frac{\mathrm{d}y}{1 + y^2}$，于是
>
> $$x e^{\arctan y}=\int u e^{u}\mathrm{d}u=(u-1)e^{u}+C,$$
>
> 即
>
> $$x=\arctan y-1+Ce^{-\arctan y}.$$

**2.** (难度: ★★★) $x\frac{dy}{dx} - y = x^{2} + y^{2}$

> [!answer]- 原书参考答案（A.4.3 第 2 题，未逐题独立验算）
> **2.** 两边同乘2y:
>
> $$2yy^{\prime}=\frac{2y^{2}}{x}+4x.$$
>
> 令$u=y^{2}$, 则 $u^{\prime}=2yy^{\prime}$，方程化为
>
> $$u^{\prime}-\frac{2}{x}u=4x,$$
>
> 这是关于 u 的一阶线性方程. 积分因子为 $e^{-2\ln x} = x^{-2}$, 两边同乘 $x^{-2}$:
>
> $$\left(u x^{-2}\right)^{\prime}=\frac{4}{x}\quad\Longrightarrow\quad u x^{-2}=4\ln x+C.$$
>
> 所以 $u = x^{2}(4 \ln x + C)$，即
>
> $$y^{2}=x^{2}\left(4\ln x+C\right)\qquad(x>0).$$

**3.** (难度: ★★★) $\frac{dy}{dx} = \frac{\sec y}{x + 2\sin y}$

> [!answer]- 原书参考答案（A.4.3 第 3 题，未逐题独立验算）
> **3.** $\frac{dy}{dx}$ 出现在分母位置，把 x 看成 y 的函数。由 $\frac{dx}{dy} = (x + 2\sin y)\cos y = x\cos y + \sin 2y$，这是关于 $x(y)$ 的一阶线性方程，积分因子为 $e^{-\sin y}$。两边同乘它：
>
> $$\left(x e^{-\sin y}\right)^{\prime}=\sin2y\cdot e^{-\sin y}.$$
>
> 令 $v = \sin y$，则 $\sin 2y \, \mathrm{d}y = 2v \, \mathrm{d}v$，于是
>
> $$x e^{-\sin y}=\int2v e^{-v}\mathrm{d}v=-2\left(v+1\right)e^{-v}+C,$$
>
> 故通解为
>
> $$x=C e^{\sin y}-2\left(1+\sin y\right).$$

**4.** (难度: ★★★) $\frac{dy}{dx} + \frac{y}{x} = y^{2} \ln x$

> [!answer]- 原书参考答案（A.4.3 第 4 题，未逐题独立验算）
> **4.** 这是 n = 2 的伯努利方程. 两边同乘 $y^{-2}$:
>
> $$y^{-2}y^{\prime}+\frac{1}{x}y^{-1}=\ln x.$$
>
> 令 $u = y^{-1}$，则 $u' = -y^{-2}y'$，方程化为
>
> $$u^{\prime}-\frac{1}{x}u=-\ln x.$$
>
> 积分因子为 $x^{-1}$，两边同乘 $x^{-1}$：
>
> $$\left(\frac{u}{x}\right)^{\prime}=-\frac{\ln x}{x}\quad\Longrightarrow\quad\frac{u}{x}=-\frac{1}{2}\ln^{2}x+C.$$
>
> 所以 $u = x \left( C - \frac{1}{2} \ln^{2} x \right)$，即
>
> $$xy\left(C-\frac{1}{2}\ln^{2}x\right)=1$$

### 4.1.4 全微分方程

**1.** (难度:★★) $(6x^{2}y+4y^{3})\mathrm{d}y+(12x^{3}+6xy^{2})\mathrm{d}x=0$

> [!answer]- 原书参考答案（A.4.4 第 1 题，未逐题独立验算）
> **1.** 这里 $P = 12x^{3} + 6xy^{2}$、$Q=6x^{2}y+4y^{3}$，且
>
> $$\frac{\partial P}{\partial y}=12xy=\frac{\partial Q}{\partial x},$$
>
> 故为全微分方程. 取 $(x_{0},y_{0})=(0,0)$ 沿折线积分:
>
> $$u=\int_{0}^{x}12t^{3}\mathrm{d}t+\int_{0}^{y}\left(6x^{2}s+4s^{3}\right)\mathrm{d}s=3x^{4}+3x^{2}y^{2}+y^{4}.$$
>
> 所以通解为 $3x^{4}+3x^{2}y^{2}+y^{4}=C$.

**2.** (难度:★★★) $y \, dx + (2x^{2}y - x) \, dy = 0$

> [!answer]- 原书参考答案（A.4.4 第 2 题，未逐题独立验算）
> **2.** 记 $P=y,\ Q=2x^{2}y-x$. 先检验是否为恰当方程:
>
> $$\frac{\partial P}{\partial y}=1,\qquad\frac{\partial Q}{\partial x}=4xy-1.$$
>
> 两者不相等，故原方程不是恰当方程。
>
> 计算
>
> $$\frac{1}{Q}\left(\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}\right)=\frac{1-(4xy-1)}{2x^{2}y-x}=\frac{2-4xy}{x(2xy-1)}=-\frac{2}{x}.$$
>
> 它只与 x 有关, 因此积分因子 $\mu$ 只含 x, 由公式
>
> $$\mu(x)=\exp\left(\int\frac{1}{Q}\left(\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}\right)\mathrm{d}x\right)$$
>
> 得
>
> $$\mu(x)=\exp\left(\int-\frac{2}{x}\mathrm{d}x\right)=\exp(-2\ln|x|)=x^{-2}.$$
>
> 两边同乘积分因子 $x^{-2}$:
>
> $$\frac{y}{x^{2}}\mathrm{d}x+\left(2y-\frac{1}{x}\right)\mathrm{d}y=0.$$
>
> 再检验：此时
>
> $$\frac{\partial}{\partial y}\left(\frac{y}{x^{2}}\right)=\frac{1}{x^{2}},\qquad\frac{\partial}{\partial x}\left(2y-\frac{1}{x}\right)=\frac{1}{x^{2}},$$
>
> 两者相等，故乘完积分因子后方程已是恰当方程。
>
> 求原函数 $F(x, y)$ 使
>
> $$\mathrm{d}F=\frac{y}{x^{2}}\mathrm{d}x+\left(2y-\frac{1}{x}\right)\mathrm{d}y.$$
>
> 对 x 积分:
>
> $$F(x,y)=\int\frac{y}{x^{2}}\mathrm{d}x=-\frac{y}{x}+\varphi(y).$$
>
> 再对 y 求偏导:
>
> $$\frac{\partial F}{\partial y}=-\frac{1}{x}+\varphi^{\prime}(y)=2y-\frac{1}{x},$$
>
> 故 $\varphi'(y) = 2y$，积分得 $\varphi(y) = y^{2}$。于是
>
> $$F(x,y)=y^{2}-\frac{y}{x}.$$
>
> 因此通解为
>
> $$y^{2}-\frac{y}{x}=C,\qquad 即 \qquad xy^{2}-y=Cx.$$

**3.** (难度: ★★★) $(e^{x} + 3y^{2}) \mathrm{d}x + 2xy \mathrm{d}y = 0$

> [!answer]- 原书参考答案（A.4.4 第 3 题，未逐题独立验算）
> **3.** $\frac{\partial P}{\partial y}=6y,\frac{\partial Q}{\partial x}=2y$ ,不是全微分方程.计算
>
> $$\frac{1}{Q}\left(\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}\right)=\frac{6y-2y}{2xy}=\frac{2}{x},$$
>
> 只与 x 有关，故积分因子为
>
> $$\mu=e\int\limits_{}^{}\frac{2}{x}\mathrm{d}x=x^{2}.$$
>
> 两边同乘 $x^{2}$:
>
> $$\left(x^{2}e^{x}+3x^{2}y^{2}\right)\mathrm{d}x+2x^{3}y\mathrm{d}y=0,$$
>
> 此时交叉偏导都为 $6x^{2}y$. 沿折线积分:
>
> $$u=\int_{0}^{x}t^{2}e^{t}\mathrm{d}t+\int_{0}^{y}2x^{3}s\mathrm{d}s=e^{x}\left(x^{2}-2x+2\right)-2+x^{3}y^{2}.$$
>
> 所以通解为
>
> $$x^{3}y^{2}+e^{x}\left(x^{2}-2x+2\right)=C.$$

## 4.2 高阶微分方程

相比于一阶微分方程，高阶微分方程的处理思路更加套路、模板化，整体难度更低，一定要注意把握不同类别微分方程的具体解法。

### 4.2.1 可降阶的微分方程

**1.** (难度：★) $y'' + 2x(y')^2 = 0$

> [!answer]- 原书参考答案（A.4.5 第 1 题，未逐题独立验算）
> **1.** 方程不显含 y，令 p = y，则 $y'' = p'$，方程化为
>
> $$xp^{\prime}=p+xp^{2}\quad\Longrightarrow\quad p^{\prime}-\frac{1}{x}p=p^{2}.$$
>
> 这是关于 $p$ 的伯努利方程 $(n=2)$。$p \equiv 0$ 给出一族解 $y \equiv C$。当 $p \neq 0$ 时两边同乘 $p^{-2}$：
>
> $$p^{-2}p^{\prime}-\frac{1}{x}p^{-1}=1.$$
>
> 令 $u = p^{-1}$，则 $u' = -p^{-2}p'$，得
>
> $$u^{\prime}+\frac{1}{x}u=-1\quad\Longrightarrow\quad(x u)^{\prime}=-x,$$
>
> 故 $xu = -\frac{x^{2}}{2} + C_{1}$，即
>
> $$p=\frac{1}{u}=\frac{2x}{2C_{1}-x^{2}}.$$
>
> 再积分一次：
>
> $$y=\int\frac{2x}{2C_{1}-x^{2}}\mathrm{d}x=-\ln\left|2C_{1}-x^{2}\right|+C_{2}.$$
>
> 连同 $y \equiv C$ 一并写出，即为通解.

**2.** (难度：★) $y'' + y(y')^{2} = 0$

> [!answer]- 原书参考答案（A.4.5 第 2 题，未逐题独立验算）
> **2.** 方程不显含 x, 令 $p = y'$, 用 $y'' = p \frac{dp}{dy}$ 代入:
>
> $$y p\frac{\mathrm{d}p}{\mathrm{d}y}=p^{2}\quad\Longrightarrow\quad p\left(y\frac{\mathrm{d}p}{\mathrm{d}y}-p\right)=0.$$
>
> 若 $p \equiv 0$，得 $y \equiv C$。若 $p \neq 0$，则
>
> $$\frac{\mathrm{d}p}{p}=\frac{\mathrm{d}y}{y}\quad\Longrightarrow\quad p=C_{1}y,$$
>
> 即 $\frac{dy}{dx}=C_{1}y$，故 $y=C_{2}e^{C_{1}x}$。因此通解为
>
> $$y=C_{2}e^{C_{1}x}\qquad\left( 含 y\equiv C 这一族 \right).$$

### 4.2.2 二阶线性微分方程

**1.** (难度: ★) $y'' - 4y' + 3y = 2xe^{3x}$

> [!answer]- 原书参考答案（A.4.6 第 1 题，未逐题独立验算）
> **1.** 特征方程 $\lambda^{2}-4\lambda+3=0$ 的根为 $\lambda_{1}=1$、 $\lambda_{2}=3$，故 $y_{h}=C_{1}e^{x}+C_{2}e^{3x}$.
>
> 右端中含 $e^{3x}$，而3恰是单重特征根，故设
>
> $$y^{*}=x\left(ax+b\right)e^{3x}.$$
>
> 记 $y^{*}=Q(x)e^{3x}$ ( $Q=ax^{2}+bx$)，直接计算得
>
> $$y^{\ast\prime\prime}-4y^{\ast\prime}+3y^{\ast}=\left[Q^{\prime\prime}+2Q^{\prime}\right]e^{3x}.$$
>
> 由 $Q'=2ax+b$、 $Q''=2a$，得
>
> $$2a+4ax+2b=2x\quad\Longrightarrow\quad a=\frac{1}{2},\quad b=-\frac{1}{2}.$$
>
> 所以通解为
>
> $$y=C_{1}e^{x}+C_{2}e^{3x}+\frac{1}{2}\left(x^{2}-x\right)e^{3x}.$$

**2.** (难度:★★) $y'' - 2y' - 3y = e^{3x} + \cos x$

> [!answer]- 原书参考答案（A.4.6 第 2 题，未逐题独立验算）
> **2.** 特征方程 $\lambda^{2}-2\lambda-3=0$ 的根为 $\lambda_{1}=3$、 $\lambda_{2}=-1$，故 $y_{h}=C_{1}e^{3x}+C_{2}e^{-x}$。对 $e^{3x}:\alpha=3$ 是单重特征根，设 $y_{1}^{*}=Axe^{3x}$，代入得 4A=1，即 $A=\frac{1}{4}$。对 $\cos x:\pm i$ 不是特征根，设 $y_{2}^{*}=B\cos x+D\sin x$，代入得
>
> $$y_{2}^{*}{}^{\prime \prime}-2y_{2}^{*}{}^{\prime}-3y_{2}^{*}=\left(-4B-2D\right)\cos x+\left(2B-4D\right)\sin x=\cos x.$$
>
> 比较系数: -4B - 2D = 1、2B - 4D = 0, 解得 $B = -\frac{1}{5}$、 $D = -\frac{1}{10}$.
>
> 由叠加原理，通解为
>
> $$y=C_{1}e^{3x}+C_{2}e^{-x}+\frac{1}{4}xe^{3x}-\frac{1}{5}\cos x-\frac{1}{10}\sin x.$$

**3.** (难度:★★★) $\cos^{4}x\frac{\mathrm{d}^{2}y}{\mathrm{d}x^{2}}+2\cos^{2}x(1-\sin x\cos x)\frac{\mathrm{d}y}{\mathrm{d}x}+y=\tan x$

> [!answer]- 原书参考答案（A.4.6 第 3 题，未逐题独立验算）
> **3.** 两边同除 $\cos^{4}x$，并令 $t = \tan x$、 $y = Y(t)$。由变换公式以及 $\sec^{2}x = 1 + t^{2}$、 $\frac{\sin x \cos x}{\cos^{2}x} = t$，得
>
> $$y^{\prime}=\left(1+t^{2}\right)Y^{\prime},\qquad y^{\prime\prime}=\left(1+t^{2}\right)^{2}Y^{\prime\prime}+2t\left(1+t^{2}\right)Y^{\prime}.$$
>
> 又
>
> $$\frac{2\left(1-\sin x\cos x\right)}{\cos^{2}x}=2\left(1+t^{2}-t\right),\qquad\frac{\tan x}{\cos^{4}x}=t\left(1+t^{2}\right)^{2}.$$
>
> 代入并约去公因子 $(1+t^{2})^{2}$，方程化为
>
> $$Y^{\prime\prime}+2Y^{\prime}+Y=t.$$
>
> 特征方程 $\left(\lambda+1\right)^{2}=0$ 有二重根 -1，故 $Y_{h}=\left(C_{1}+C_{2}t\right)e^{-t}$. 设 $Y^{*}=at+b$ 代入得 $2a+at+b=t$，即 a=1、b=-2. 所以
>
> $$Y=\left(C_{1}+C_{2}t\right)e^{-t}+t-2,$$
>
> 换回 $t = \tan x$:
>
> $$y=\left(C_{1}+C_{2}\tan x\right)e^{-\tan x}+\tan x-2.$$

### 4.2.3 欧拉方程

**1.** (难度: ★★) $x^{2}y'' - xy' + y = x^{2} + 1$

> [!answer]- 原书参考答案（A.4.7 第 1 题，未逐题独立验算）
> **1.** 令 $x=e^t$, 则 $x^{2}y'' = D(D - 1)y$, $xy' = Dy$, 且 $x^{2} = e^{2t}$. 方程化为
>
> $$D(D-1)y-Dy+y=e^{2t}+1\quad\Longrightarrow\quad(D-1)^{2}y=e^{2t}+1.$$
>
> 特征方程 $\left(\lambda-1\right)^{2}=0$ 有二重根1，故 $y_{h}=\left(C_{1}+C_{2}t\right)e^{t}$
>
> 对 $e^{2t}$ 设 $Ae^{2t}$，代入得 A = 1；对常数 1 设 B，代入得 B = 1。所以
>
> $$y=\left(C_{1}+C_{2}t\right)e^{t}+e^{2t}+1=\left(C_{1}+C_{2}\ln x\right)x+x^{2}+1.$$

**2.** (难度: ★★) $x^{3}y''' + x^{2}y'' - 4xy' = 3x^{2}$

> [!answer]- 原书参考答案（A.4.7 第 2 题，未逐题独立验算）
> **2.** 令 $x=e^t$, 则 $x^{3}y''' = D(D-1)(D-2)y$, $x^{2}y'' = D(D-1)y$, $xy' = Dy$, 且 $3x^{2} = 3e^{2t}$. 方程化为
>
> $$[D(D-1)(D-2)+D(D-1)-4D]y=3e^{2t}.$$
>
> 逐项展开并合并：
>
> $$D\left(D^{2}-2D-3\right)y=D(D-3)(D+1)y=3e^{2t}.$$
>
> 特征根为0,3,-1，故 $y_{h}=C_{1}+C_{2}e^{3t}+C_{3}e^{-t}$.设特解 $Ae^{2t}$，代入得 $2\cdot(-1)\cdot3A=-6A=3$，即 $A=-\frac{1}{2}$.于是
>
> $$y=C_{1}+C_{2}x^{3}+\frac{C_{3}}{x}-\frac{1}{2}x^{2}.$$

### 4.2.4 微分方程解的结构

**1.** (难度:★★★) 已知 $y_{1}=e^{x}$, $y_{2}=u(x)e^{x}$ 是微分方程 $(2x-1)y''-(2x+1)y'+2y=0$ 的解，且 $u(0)=-1$, $u(-1)=e$，据此求该微分方程的通解.

> [!answer]- 原书参考答案（A.4.8 第 1 题，未逐题独立验算）
> **1.** 已知 $y_1 = e^x$ 是一个解，另一个解写成 $y_2 = u(x)e^x$，代入后 $u$ 满足的方程应当降为一阶。令 $y = ue^x$，则 $y' = (u' + u)e^x$、 $y'' = (u'' + 2u' + u)e^x$。代入方程：
>
> $$\left(2x-1\right)u^{\prime\prime}+\left(2x-3\right)u^{\prime}=0.$$
>
> 令 $w = u'$，则 $\frac{w'}{w} = -\frac{2x - 3}{2x - 1} = -1 + \frac{2}{2x - 1}$，积分得
>
> $$w=C\left(2x-1\right)e^{-x}.$$
>
> 于是
>
> $$u=C\int\left(2x-1\right)e^{-x}\mathrm{d}x=-C\left(2x+1\right)e^{-x}+C_{2}.$$
>
> 由 u(0) = -1 得 C = 1 (常数 $C_{2}$ 可并入另一个基本解)，故 $u = -(2x + 1)e^{-x}$，满足 $u(-1) = e$.
>
> 所以 $y_{2}=u(x)e^{x}=-(2x+1)$，通解为
>
> $$y=C_{1}e^{x}+C_{2}\left(2x+1\right).$$
>
> 条件 $u(-1) = e$ 其实是「冗余」的：一旦由 $u(0) = -1$ 定出 C = 1, $u(-1) = e$ 自动成立，它起的是校验作用.

**2.** (难度: ★★★★) 设方程 $y'' - \frac{1}{x}y' + a(x)y = 0 (a \neq 0)$ 有使得 $y_1 y_2 = 1$ 的两个不同特解，据此求该微分方程通解.

> [!answer]- 原书参考答案（A.4.8 第 2 题，未逐题独立验算）
> **2.** 已知 $y_{1}$ 是解、 $y_{2}=1/y_{1}$ 也是解，各给一个等式。先把两个等式都写出来，消去未知的 $a(x)$，得到只含 $y_{1}$ 的方程；这时出现的项恰好是 $\frac{y_{1}^{\prime}}{y_{1}}$ 和 $\frac{y_{1}^{\prime\prime}}{y_{1}}$，再自然设 $u=\frac{y_{1}^{\prime}}{y_{1}}$ 降阶。设方程为
>
> $$y^{\prime\prime}-\frac{1}{x}y^{\prime}+a(x)y=0,\qquad a(x)\neq0.$$
>
> 第一步： $y_{1}$ 是解. 代入得
>
> $$y_{1}^{\prime\prime}-\frac{1}{x}y_{1}^{\prime}+a(x)y_{1}=0.$$
>
> 由(1)解出 $a(x)y_{1}^{2}$备用：
>
> $$a(x)y_{1}=-\frac{y_{1}^{\prime\prime}}{y_{1}}+\frac{1}{x}\cdot\frac{y_{1}^{\prime}}{y_{1}}\quad\Longrightarrow\quad a(x)y_{1}^{2}=-y_{1}y_{1}^{\prime\prime}+\frac{1}{x}y_{1}y_{1}^{\prime}.$$
>
> 第二步： $y_{2}=1/y_{1}$ 也是解. 先算
>
> $$y_{2}^{\prime}=-\frac{y_{1}^{\prime}}{y_{1}^{2}},\qquad y_{2}^{\prime\prime}=\frac{2y_{1}^{\prime2}}{y_{1}^{3}}-\frac{y_{1}^{\prime\prime}}{y_{1}^{2}}.$$
>
> 代入方程并乘以 $y_{1}^{3}$:
>
> $$2y_{1}^{\prime2}-y_{1}y_{1}^{\prime\prime}+\frac{1}{x}y_{1}y_{1}^{\prime}+a(x)y_{1}^{2}=0.$$
>
> 第三步：消去 $a(x)$. 把 $(1^{\prime})$ 代入 (2):
>
> $$2y_{1}^{\prime2}-y_{1}y_{1}^{\prime\prime}+\frac{1}{x}y_{1}y_{1}^{\prime}-y_{1}y_{1}^{\prime\prime}+\frac{1}{x}y_{1}y_{1}^{\prime}=0,$$
>
> 整理得
>
> $$(y_{1}^{\prime})^{2}-y_{1}y_{1}^{\prime\prime}+\frac{1}{x}y_{1}y_{1}^{\prime}=0.$$
>
> 第四步: 自然设 $u = \frac{y_{1}'}{y_{1}}$. 把 (3) 两边除以 $y_{1}^{2}$:
>
> $$\left(\frac{y_{1}^{\prime}}{y_{1}}\right)^{2}-\frac{y_{1}^{\prime\prime}}{y_{1}}+\frac{1}{x}\cdot\frac{y_{1}^{\prime}}{y_{1}}=0.$$
>
> 令 $u = \frac{y_{1}^{\prime}}{y_{1}}$，则 $\frac{y_{1}^{\prime\prime}}{y_{1}} = u^{\prime} + u^{2}$，代入得
>
> $$u^{2}-\left(u^{\prime}+u^{2}\right)+\frac{u}{x}=0\quad\Longrightarrow\quad u^{\prime}=\frac{u}{x}.$$
>
> 因为 $a(x) \neq 0$，由 $(1^{\prime})$ 可知 $u \neq 0$，故可分离变量：
>
> $$\frac{u^{\prime}}{u}=\frac{1}{x}\quad\Longrightarrow\quad\ln|u|=\ln|x|+C_{0}\quad\Longrightarrow\quad u=kx\qquad(k\neq0).$$
>
> 第五步: 求 $y_{1}$、 $a(x)$ 与通解. 由 $u = \frac{y_{1}^{\prime}}{y_{1}} = kx$ 得
>
> $$\ln|y_{1}|=\frac{kx^{2}}{2}+C\quad\Longrightarrow\quad y_{1}=Ce^{kx^{2}/2}.$$
>
> 取 C = 1，得 $y_{1} = e^{kx^{2}/2}$，从而 $y_{2} = e^{-kx^{2}/2}$，两者线性无关.
>
> 再由 $(1^{\prime})$求 $a(x)$:
>
> $$a(x)=-\frac{y_{1}^{\prime\prime}}{y_{1}}+\frac{1}{x}\cdot\frac{y_{1}^{\prime}}{y_{1}}=-(k+k^{2}x^{2})+k=-k^{2}x^{2}.$$
>
> 故通解为
>
> $$y=C_1e^{kx^2/2}+C_2e^{-kx^2/2},\qquad a(x)=-k^2x^2\left(k\ne0\right).$$
>
> 本题的关键是“先消元、后设 $u$”。如果一上来就设 $u = y'_1 / y_1$，虽然也能做，但显得突兀。先代入两个解消去 $a(x)$，方程 (3) 里自然出现 $y'_1 / y_1$ 和 $y'' / y_1$，这时再设 $u$ 就顺理成章了。另外， $a \neq 0$ 保证了 $k \neq 0$，否则 $y_1, y_2$ 都退化为常数，不满足线性无关。

**3.** (难度:★★★) 验证 $y_{1} = \frac{\sin x}{x}$ 是微分方程 $y'' + \frac{2}{x}y' + y = 0$ 的解，并求其通解.

> [!answer]- 原书参考答案（A.4.8 第 3 题，未逐题独立验算）
> **3.** 先验证. 由 $y_{1}=\frac{\sin x}{x}$ 得
>
> $$y_{1}^{\prime}=\frac{x\cos x-\sin x}{x^{2}},\qquad y_{1}^{\prime\prime}=\frac{\left(2-x^{2}\right)\sin x-2x\cos x}{x^{3}}.$$
>
> 于是
>
> $$y_{1}^{\prime\prime}+\frac{2}{x}y_{1}^{\prime}+y_{1}=\frac{\left(2-x^{2}\right)\sin x-2x\cos x}{x^{3}}+\frac{2x\cos x-2\sin x}{x^{3}}+\frac{x^{2}\sin x}{x^{3}}=0,$$
>
> 故 $y_{1}$确为解.
>
> 这里 $p(x)=\frac{2}{x}$，由公式
>
> $$y_{2}=y_{1}\int\frac{1}{y_{1}^{2}}e^{-\int p\mathrm{d}x}\mathrm{d}x=\frac{\sin x}{x}\int\frac{x^{2}}{\sin^{2}x}\cdot\frac{1}{x^{2}}\mathrm{d}x=\frac{\sin x}{x}\int\frac{\mathrm{d}x}{\sin^{2}x}.$$
>
> 由 $\int\frac{dx}{\sin^{2}x} = -\cot x$，得
>
> $$y_{2}=-\frac{\cos x}{x}.$$
>
> 所以通解为
>
> $$y=\frac{C_{1}\sin x+C_{2}\cos x}{x}\qquad(x>0).$$

## 4.3 微分方程物理应用

一些与微分方程常见的物理/几何应用题，重点是根据实际情景列出微分方程，相对而言并不是难题。

**1.** (难度:★★★) 设物体 A 从点 (0,1) 出发, 以速度大小为常数 v 沿着 y 轴正向运动. 物体 B 从点 $(-1,0)$ 与 A 同时出发, 其速度大小为 2v, 方向始终指向 A, 试建立物体 B 的运动轨迹所满足的微分方程, 并写出初始条件.

> [!answer]- 原书参考答案（A.4.9 第 1 题，未逐题独立验算）
> **1.** 两条线索: 切线始终指向 A (几何条件), 以及 B 走过的弧长等于 2vt (速度条件). 设 t 时刻 $A = (0,1+vt)$、 $B = (x,y(x))$. 由切线过 A:
>
> $$y^{\prime}=\frac{(1+v t)-y}{0-x}\quad\Longrightarrow\quad v t=y-1-x y^{\prime}.$$
>
> 又 B 走过的弧长为 2vt (速度是 v 的两倍):
>
> $$\int_{-1}^{x}\sqrt{1+(y^{\prime})^{2}}\mathrm{d}\xi=2v t.$$
>
> 记 $s = vt = \frac{1}{2} \int_{-1}^{x} \sqrt{1 + (y')^2} \, \mathrm{d}\xi$，把 (1) 对 x 求导得
>
> $$\frac{\mathrm{d}s}{\mathrm{d}x}=y^{\prime}-\left(y^{\prime}+xy^{\prime\prime}\right)=-xy^{\prime\prime},$$
>
> 而由(2)得 $\sqrt{1+(y')^{2}}=2\frac{ds}{dx}$.两式联立即得B的轨迹方程
>
> $$2xy^{\prime\prime}+\sqrt{1+\left(y^{\prime}\right)^{2}}=0,$$
>
> 初始条件为
>
> $$y(-1)=0,\qquad y^{\prime}(-1)=1.$$
>
> B 的初始方向是 $(h,k)=(1,1)$，故 $y^{\prime}(-1)=1$；两个初始条件正好对应二阶方程的通解常数.

**2.** (难度:★★) 质量为 m 的炮弹以初速 $v_{0}$ 自地面垂直向上发射, 设空气阻力始终与炮弹速度的平方成正比, 比例系数为 k, 重力加速度 g 为已知, 求炮弹的最高射程和所需的时间.

> [!answer]- 原书参考答案（A.4.9 第 2 题，未逐题独立验算）
> **2.** 取向上为正方向，设 t 时刻速度为 $v(t)$，则受力为重力与空气阻力的合力，故
>
> $$m\frac{\mathrm{d}v}{\mathrm{d}t}=-mg-kv^{2}\quad\Longrightarrow\quad\frac{\mathrm{d}v}{\mathrm{d}t}=-g-\frac{k}{m}v^{2}.$$
>
> 记 $a=\frac{k}{m}$. 分离变量并由 $v(0)=v_{0}$ 积分:
>
> $$t=\int_{v}^{v_{0}}\frac{\mathrm{d}s}{g+a s^{2}}=\frac{1}{\sqrt{a g}}\left[\arctan\left(s\sqrt{\frac{a}{g}}\right)\right]_{v}^{v_{0}}.$$
>
> 令 v=0，得到达最高点的时间
>
> $$T=\frac{1}{\sqrt{a g}}\arctan\left(v_{0}\sqrt{\frac{a}{g}}\right)=\sqrt{\frac{m}{k g}}\arctan\left(v_{0}\sqrt{\frac{k}{m g}}\right).$$
>
> 求高度时把 v 看成 x 的函数，由 $\frac{dv}{dt} = v\frac{dv}{dx}$ 得
>
> $$v\frac{\mathrm{d}v}{\mathrm{d}x}=-\left(g+a v^{2}\right)\quad\Longrightarrow\quad\mathrm{d}x=-\frac{v\mathrm{d}v}{g+a v^{2}},$$
>
> 于是
>
> $$H=\int_{0}^{v_{0}}\frac{v\mathrm{d}v}{g+a v^{2}}=\frac{1}{2a}\ln\left(1+\frac{a v_{0}^{2}}{g}\right)=\frac{m}{2k}\ln\left(1+\frac{k v_{0}^{2}}{m g}\right).$$

**3.** (难度: ★★★) 一条缉毒犬在嗅到毒品散发的气味后始终朝着毒品味最浓烈的方向搜寻, 实验表明, 如果以毒品所在位置为坐标原点建立平面直角坐标系, 那么任意点 $(x, y)$ 处毒品气味的浓烈程度可表示为 $f(x, y) = e^{-\frac{x^2 + 2y^2}{10^5}}$. 求这条缉毒犬从点 $(1, 1)$ 出发搜寻到毒品所走过的路径.

> [!answer]- 原书参考答案（A.4.9 第 3 题，未逐题独立验算）
> **3.** 「气味最浓的方向」就是梯度的方向，轨迹的切线方向与梯度方向平行. 记 $c = 10^{5}$，则
>
> $$\frac{\partial f}{\partial x}=-\frac{2x}{c}e^{-\frac{x^{2}+2y^{2}}{c}},\qquad\frac{\partial f}{\partial y}=-\frac{4y}{c}e^{-\frac{x^{2}+2y^{2}}{c}}.$$
>
> 轨迹沿最速上升方向，故
>
> $$\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{\partial f/\partial y}{\partial f/\partial x}=\frac{4y}{2x}=\frac{2y}{x}.$$
>
> 分离变量得 $y=Cx^2$. 由起点 (1,1) 得 C = 1, 故轨迹为
>
> $$y=x^{2},\qquad x\in[0,1],$$
>
> 即从 $(1,1)$沿抛物线走向原点.

---

# 基础篇·第五章 空间解析几何

## 5.1 向量

与高中知识结合较紧密的考察方向，相对而言比较基础，需要额外注意和向量积、混合积相关的新内容.

**1.** (难度:★★) 设单位向量 $\overrightarrow{OA}$, $\overrightarrow{OB}$ 夹角为 $\theta$，且 a, b > 0，求:

$$\lim_{\theta\rightarrow0}\frac{\left(\left\|a\overrightarrow{O A}\right\|+\left\|b\overrightarrow{O B}\right\|-\left\|a\overrightarrow{O A}+b\overrightarrow{O B}\right\|\right)}{\theta^{2}}.$$

> [!answer]- 原书参考答案（A.5.1 第 1 题，未逐题独立验算）
> **1.** 先画出两个单位向量.
>
> <div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//2689de67-00e3-43fe-bb78-bc0b6095dc11/markdown_2/imgs/img_in_image_box_528_480_710_646.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-11-05T13%3A08%3A24Z%2F-1%2F%2Fe3f0c1242c5127f4af00b887ad8972c4423670b4215c0df4ad9944cdc9fd7f2e" alt="Image" width="15%" /></div>
>
> 因为 $\overrightarrow{OA}, \overrightarrow{OB}$ 都是单位向量, 所以
>
> $$|\overrightarrow{O A}|=|\overrightarrow{O B}|=1.$$
>
> 于是分子是
>
> $$\boldsymbol{a}+\boldsymbol{b}-\left|\boldsymbol{a}\overrightarrow{O A}+\boldsymbol{b}\overrightarrow{O B}\right|.$$
>
> 用内积计算模长：
>
> $$\left|\overrightarrow{a O A}+b\overrightarrow{O B}\right|^{2}=a^{2}+b^{2}+2a b\cos\theta,$$
>
> 所以
>
> $$\left|\overrightarrow{a O A}+b\overrightarrow{O B}\right|=\sqrt{a^{2}+b^{2}+2a b\cos\theta}.$$
>
> 分子有理化：
>
> $$a+b-\sqrt{a^{2}+b^{2}+2ab\cos\theta}=\frac{(a+b)^{2}-\left(a^{2}+b^{2}+2ab\cos\theta\right)}{a+b+\sqrt{a^{2}+b^{2}+2ab\cos\theta}}.$$
>
> 这里 $(a+b)^{2}-(a^{2}+b^{2}+2ab\cos\theta)=2ab(1-\cos\theta)$. 因此
>
> $$\lim_{\theta\to0}\frac{a+b-\sqrt{a^{2}+b^{2}+2ab\cos\theta}}{\theta^{2}}=\frac{2ab}{2(a+b)}\lim_{\theta\to0}\frac{1-\cos\theta}{\theta^{2}}=\frac{ab}{2(a+b)}.$$

**2.** （难度：★★★★）证明以下向量等式.

(1) $(\mathbf{a} \times \mathbf{b}) \times \mathbf{c} = (\mathbf{a} \cdot \mathbf{c})\mathbf{b} - (\mathbf{b} \cdot \mathbf{c})\mathbf{a}$.

(2) $(\mathbf{a} \times \mathbf{b}) \cdot (\mathbf{c} \times \mathbf{d}) = \begin{vmatrix} \mathbf{a} \cdot \mathbf{c} & \mathbf{a} \cdot \mathbf{d} \\ \mathbf{b} \cdot \mathbf{c} & \mathbf{b} \cdot \mathbf{d} \end{vmatrix}$.

> [!answer]- 原书参考答案（A.5.1 第 2 题，未逐题独立验算）
> **2.** （1）设
>
> $$\vec{a}=(a_{1},a_{2},a_{3}),\quad\vec{b}=(b_{1},b_{2},b_{3}),\quad\vec{c}=(c_{1},c_{2},c_{3}).$$
>
> 先算
>
> $$\vec{a}\times\vec{b}=\left(a_{2}b_{3}-a_{3}b_{2},a_{3}b_{1}-a_{1}b_{3},a_{1}b_{2}-a_{2}b_{1}\right).$$
>
> 再把这个结果与 $\overrightarrow{c}$ 作外积，逐项展开合并，就能得到
>
> $$(\vec{a}\times\vec{b})\times\vec{c}=(\vec{a}\cdot\vec{c})\vec{b}-(\vec{b}\cdot\vec{c})\vec{a}.$$
>
> 这个公式不必每次推导，直接当结论记忆即可。
>
> (2) 令 $\overrightarrow{u} = \overrightarrow{a} \times \overrightarrow{b}$. 由混合积的轮换性,
>
> $$\vec{u}\cdot(\vec{c}\times\vec{d})=(\vec{u}\times\vec{c})\cdot\vec{d}.$$
>
> 再把 $\vec{u} = \vec{a} \times \vec{b}$ 代入，用 (1):
>
> $$\vec{u}\times\vec{c}=(\vec{a}\times\vec{b})\times\vec{c}=(\vec{a}\cdot\vec{c})\vec{b}-(\vec{b}\cdot\vec{c})\vec{a}.$$
>
> 两边与 $\overrightarrow{d}$ 作内积：
>
> $$\vec{u}\cdot(\vec{c}\times\vec{d})=(\vec{a}\cdot\vec{c})(\vec{b}\cdot\vec{d})-(\vec{b}\cdot\vec{c})(\vec{a}\cdot\vec{d}).$$
>
> 这就是要证的式子.

**3.** (难度:★★★★) 在一个以 O 为球心的球内有一定点 P, 球面上有 A, B, C 三个动点, 且始终有 $\angle APB = \angle BPC = \angle CPA = \frac{\pi}{2}$. 以 PA, PB, PC 为棱作平行六面体, 点 Q 是与点 P 相对应的顶点. 证明: 点 Q 的运动轨迹是球面.

> [!answer]- 原书参考答案（A.5.1 第 3 题，未逐题独立验算）
> **3.** 把球心放到原点，用 $\overrightarrow{OA}$， $\overrightarrow{OB}$， $\overrightarrow{OC}$ 表示 $\overrightarrow{OQ}$。因为 PA, PB, PC 两两垂直，展开模长时所有交叉项都可以用内积为零消掉。设球半径为 R，取球心 O 为原点。记
>
> $$\overrightarrow{p}=\overrightarrow{OP},\quad\overrightarrow{a}=\overrightarrow{OA},\quad\overrightarrow{b}=\overrightarrow{OB},\quad\overrightarrow{c}=\overrightarrow{OC}.$$
>
> 因为 A, B, C 都在球面上, 所以
>
> $$|\vec{a}|=|\vec{b}|=|\vec{c}|=R.$$
>
> <div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//2689de67-00e3-43fe-bb78-bc0b6095dc11/markdown_3/imgs/img_in_image_box_489_1092_753_1347.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-11-05T13%3A08%3A36Z%2F-1%2F%2Fb0e87f0037450eb49673a0ca2fdfb645a1c59a42980faee1af74492a5a25403c" alt="Image" width="22%" /></div>
>
> 先看 P 与 A 的关系:
>
> $$\overrightarrow{P A}=\overrightarrow{O A}-\overrightarrow{O P}=\overrightarrow{a}-\overrightarrow{p}.$$
>
> 同理
>
> $$\overrightarrow{PB}=\overrightarrow{b}-\overrightarrow{p},\qquad\overrightarrow{PC}=\overrightarrow{c}-\overrightarrow{p}.$$
>
> 记
>
> $$\overrightarrow{u}=\overrightarrow{P A},\quad\overrightarrow{v}=\overrightarrow{P B},\quad\overrightarrow{w}=\overrightarrow{P C}.$$
>
> 由题意， $\vec{u}, \vec{v}, \vec{w}$ 两两垂直，所以
>
> $$\vec{u}\cdot\vec{v}=\vec{v}\cdot\vec{w}=\vec{w}\cdot\vec{u}=0.$$
>
> 平行六面体中，与 P 相对的顶点 Q 满足
>
> $$\overrightarrow{PQ}=\overrightarrow{PA}+\overrightarrow{PB}+\overrightarrow{PC}=\overrightarrow{u}+\overrightarrow{v}+\overrightarrow{w}.$$
>
> 所以
>
> $$\overrightarrow{O Q}=\overrightarrow{O P}+\overrightarrow{P Q}=\overrightarrow{p}+\overrightarrow{u}+\overrightarrow{v}+\overrightarrow{w}.$$
>
> 两边取模长平方：
>
> $$|\overrightarrow{O Q}|^{2}=|\overrightarrow{p}+\overrightarrow{u}+\overrightarrow{v}+\overrightarrow{w}|^{2}.$$
>
> 展开内积：
>
> $$|\overrightarrow{O Q}|^{2}=|\vec{u}|^{2}+|\vec{v}|^{2}+|\vec{w}|^{2}+|\vec{p}|^{2}+2(\vec{u}\cdot\vec{v}+\vec{v}\cdot\vec{w}+\vec{w}\cdot\vec{u})+2\vec{p}\cdot(\vec{u}+\vec{v}+\vec{w}).$$
>
> 因为 $\vec{u}, \vec{v}, \vec{w}$ 两两垂直，中间三项都是 0，所以
>
> $$|\overrightarrow{O Q}|^{2}=|\overrightarrow{u}|^{2}+|\overrightarrow{v}|^{2}+|\overrightarrow{w}|^{2}+|\overrightarrow{p}|^{2}+2\overrightarrow{p}\cdot(\overrightarrow{u}+\overrightarrow{v}+\overrightarrow{w}).$$
>
> 下面用余弦定理把 $|\vec{u}|^2$, $|\vec{v}|^2$, $|\vec{w}|^2$ 换成球半径和 $\vec{p}$. 以 $\vec{u} = \vec{a} - \vec{p}$ 为例:
>
> $$|\vec{u}|^{2}=|\vec{a}-\vec{p}|^{2}=|\vec{a}|^{2}+|\vec{p}|^{2}-2\vec{a}\cdot\vec{p}=R^{2}+|\vec{p}|^{2}-2\vec{a}\cdot\vec{p}.$$
>
> 同理，
>
> $$|\vec{v}|^{2}=R^{2}+|\vec{p}|^{2}-2\vec{b}\cdot\vec{p},$$
>
> $$|\vec{w}|^{2}=R^{2}+|\vec{p}|^{2}-2\vec{c}\cdot\vec{p}.$$
>
> 三式相加：
>
> $$|\vec{u}|^{2}+|\vec{v}|^{2}+|\vec{w}|^{2}=3R^{2}+3|\vec{p}|^{2}-2\vec{p}\cdot(\vec{a}+\vec{b}+\vec{c}).$$
>
> 又因为
>
> $$\vec{a}+\vec{b}+\vec{c}=(\vec{p}+\vec{u})+(\vec{p}+\vec{v})+(\vec{p}+\vec{w})=\vec{u}+\vec{v}+\vec{w}+3\vec{p},$$
>
> 所以
>
> $$|\vec{u}|^{2}+|\vec{v}|^{2}+|\vec{w}|^{2}=3R^{2}+3|\vec{p}|^{2}-2\vec{p}\cdot(\vec{u}+\vec{v}+\vec{w})-6|\vec{p}|^{2}.$$
>
> 代回 $|\overrightarrow{OQ}|^2$ 的展开式:
>
> $$|\overrightarrow{O Q}|^{2}=3R^{2}-2|\overrightarrow{p}|^{2}.$$
>
> 右边只与球半径 R 和定点 P 有关, 不随 A, B, C 变化. 所以 Q 到球心 O 的距离恒为
>
> $$\sqrt{3R^{2}-2|O P|^{2}}.$$
>
> 因此 $Q$ 的轨迹是以 $O$ 为球心、半径为 $\sqrt{3R^2 - 2|OP|^2}$ 的球面。这一步里最关键是 $\vec{u}, \vec{v}, \vec{w}$ 两两垂直，展开模长时交叉项全部消失；中间把 $|\vec{a} - \vec{p}|^2$ 展开的过程，本质上就是余弦定理。

**4.** (难度:★★★) 记 $\overrightarrow{OA}$ 与 $\overrightarrow{OB}$ 夹角为 $\alpha$，且有:

$$\left\|\overrightarrow{OA}\right\|=1,\quad\left\|\overrightarrow{OB}\right\|=2,\quad\overrightarrow{OP}=(1-\lambda)\overrightarrow{OA},\quad\overrightarrow{OQ}=\lambda\overrightarrow{OB},\quad0<\lambda<1.$$

(1) 问当 $\lambda$ 取何值时, $\left\| \overrightarrow{PQ} \right\|$ 取最小值;

(2) 设 (1) 中的 $\lambda$ 满足 $0 < \lambda < \frac{1}{5}$，求 $\alpha$ 的取值范围.

> [!answer]- 原书参考答案（A.5.1 第 4 题，未逐题独立验算）
> **4.** 把 $\left|\overrightarrow{PQ}\right|^{2}$ 写成关于 $\lambda$ 的二次函数，先求最小值；再让最小值点落在 $(0,\frac{1}{5})$ 中反解 $\alpha$。设 $\cos\alpha=t$。由题意，
>
> $$\overrightarrow{PQ}=\overrightarrow{OQ}-\overrightarrow{OP}=\lambda\overrightarrow{OB}-(1-\lambda)\overrightarrow{OA}.$$
>
> 两边平方，用内积展开：
>
> $$|\overrightarrow{P Q}|^{2}=\lambda^{2}|\overrightarrow{O B}|^{2}+(1-\lambda)^{2}|\overrightarrow{O A}|^{2}-2\lambda(1-\lambda)\overrightarrow{O A}\cdot\overrightarrow{O B}.$$
>
> 代入 $|\overrightarrow{OA}| = 1$, $|\overrightarrow{OB}| = 2$ 以及
>
> $$\overrightarrow{OA}\cdot\overrightarrow{OB}=2\cos\alpha=2t,$$
>
> 得
>
> $$|\overrightarrow{PQ}|^{2}=4\lambda^{2}+(1-\lambda)^{2}-4\lambda(1-\lambda)t.$$
>
> 展开并按 $\lambda$降幂排列：
>
> $$|\overrightarrow{PQ}|^{2}=(5+4t)\lambda^{2}-(2+4t)\lambda+1.$$
>
> 这是关于 $\lambda$ 的开口向上的二次函数, 最小值在
>
> $$\lambda=\frac{2+4t}{2(5+4t)}=\frac{1+2t}{5+4t}.$$
>
> (2) 由条件
>
> $$0<\frac{1+2t}{5+4t}<\frac{1}{5}.$$
>
> 因为 $t = \cos \alpha \in [-1, 1]$，所以 $5 + 4t > 0$。左边不等式给出
>
> $$1+2t>0\quad\Longrightarrow\quad t>-\frac{1}{2}.$$
>
> 右边不等式给出
>
> $$5(1+2t)<5+4t\quad\Longrightarrow\quad5+10t<5+4t\quad\Longrightarrow\quad t<0.$$
>
> 所以
>
> $$-\frac{1}{2}<\cos\alpha<0.$$
>
> 因此
>
> $$\frac{\pi}{2}<\alpha<\frac{2\pi}{3}.$$
>
> 向量长度问题先平方，把夹角信息收进内积，问题就变成二次函数讨论.

**5.** (难度:★★★★) 设四边形 $A_{1}A_{2}A_{3}A_{4}$ 为圆 O 的内接四边形, 且以下四个点 $H_{1}, H_{2}, H_{3}, H_{4}$ 依次是 $\triangle A_{2}A_{3}A_{4}, \triangle A_{3}A_{4}A_{1}, \triangle A_{4}A_{1}A_{2}, \triangle A_{1}A_{2}A_{3}$ 的垂心. 求证: $H_{1}, H_{2}, H_{3}, H_{4}$ 四点共圆.

> [!answer]- 原书参考答案（A.5.1 第 5 题，未逐题独立验算）
> **5.** 把圆心放到原点，用顶点向量写出四个三角形的垂心向量；四个垂心与原四边形四个顶点之间只是中心对称。设圆半径为 R，取圆心 O 为原点，记
>
> $$\overrightarrow{O A_{i}}=\overrightarrow{a}_{i},\qquad|\overrightarrow{a}_{i}|=R,\quad i=1,2,3,4.$$
>
> 先看三角形 $A_{2}A_{3}A_{4}$. 它的三个顶点都在以 O 为圆心的圆上, 高中向量结论告诉我们: 它的垂心 $H_{1}$ 满足
>
> $$\overrightarrow{OH_{1}}=\overrightarrow{a}_{2}+\overrightarrow{a}_{3}+\overrightarrow{a}_{4}.$$
>
> 同理，
>
> $$\overrightarrow{OH_{2}}=\overrightarrow{a}_{1}+\overrightarrow{a}_{3}+\overrightarrow{a}_{4},$$
>
> $$\overrightarrow{OH_{3}}=\overrightarrow{a}_{1}+\overrightarrow{a}_{2}+\overrightarrow{a}_{4},$$
>
> $$\overrightarrow{OH_{4}}=\overrightarrow{a}_{1}+\overrightarrow{a}_{2}+\overrightarrow{a}_{3}.$$
>
> 令
>
> $$\vec{S}=\vec{a}_{1}+\vec{a}_{2}+\vec{a}_{3}+\vec{a}_{4}.$$
>
> 则
>
> $$\overrightarrow{OH_{i}}=\overrightarrow{S}-\overrightarrow{a}_{i},$$
>
> 所以
>
> $$\overrightarrow{OH_{i}}+\overrightarrow{OA_{i}}=\overrightarrow{S}-\overrightarrow{a}_{i}+\overrightarrow{a}_{i}=\overrightarrow{S}.$$
>
> 这说明 $H_{i}$ 与 $A_{i}$ 关于定点 $\frac{S}{2}$ 中心对称. 中心对称把圆变成另一个圆, 所以 $H_{1}, H_{2}, H_{3}, H_{4}$ 四点共圆. “三个顶点在圆上的三角形, 垂心向量等于三个顶点向量之和” 是本题唯一需要记住的向量结论.

## 5.2 直线与平面

掌握直线和平面方程的基本求法，会对各种角度和距离计算，即可完全应对直线和平面相关内容的考察。

**1.** (难度:★) 求直线 $l_{1}:\left\{\begin{aligned}&x-y=0,\\ &z=0,\end{aligned}\right.$ 与直线 $l_{2}:\frac{x-2}{4}=\frac{y-1}{-2}=\frac{z-3}{-1}$ 的距离.

> [!answer]- 原书参考答案（A.5.2 第 1 题，未逐题独立验算）
> > [!warning] AI 补充：原题与原书答案条件不一致
> > 第 1 题题干给出 $l_1:x-y=0,\ z=0$，但原书答案使用的方向向量及点 $P_1=(1,-1,2)$ 与该直线不符；第 2 题题干指定经过 $(4,-3,1)$，原书答案却代入 $P=(1,2,3)$。已对照原书第 19、139～140 页确认，以下保留原答案，不将其视为这两道原题的已核验解答。
>
> **1.** 两条直线的方向向量分别是
>
> $$\vec{s}_{1}=(1,2,-1),\qquad\vec{s}_{2}=(2,-1,1).$$
>
> 在 $l_{1}$ 上取点 $P_{1}=(1,-1,2)$，在 $l_{2}$ 上取点 $P_{2}=(2,1,3)$，则
>
> $$\overrightarrow{P_{1}P_{2}}=(1,2,1).$$
>
> 先求与 $\overrightarrow{s}_{1}, \overrightarrow{s}_{2}$ 都垂直的向量：
>
> $$\vec{s}_{1}\times\vec{s}_{2}=(2\cdot1-(-1)(-1),(-1)\cdot2-1\cdot1,1\cdot(-1)-2\cdot2)=(1,-3,-5).$$
>
> 它的模为
>
> $$|\vec{s}_{1}\times\vec{s}_{2}|=\sqrt{1+9+25}=\sqrt{35}.$$
>
> 两条异面直线的距离, 等于 $\overrightarrow{P_{1}P_{2}}$ 在公垂线方向上的投影长度:
>
> $$d=\frac{|\overrightarrow{P_{1}P_{2}}\cdot(\overrightarrow{s}_{1}\times\overrightarrow{s}_{2})|}{|\overrightarrow{s}_{1}\times\overrightarrow{s}_{2}|}=\frac{|1-6-5|}{\sqrt{35}}=\frac{10}{\sqrt{35}}=\frac{2\sqrt{35}}{7}.$$

**2.** (难度: ★) 求通过直线 $L : \left\{ \begin{aligned} 2x + y - 3z + 2 &= 0, \\ 5x + 5y - 4z + 3 &= 0, \end{aligned} \right.$ 的两个互相垂直的平面 $\pi_{1}, \pi_{2}$，其中一个平面过点 $(4, -3, 1)$.

> [!answer]- 原书参考答案（A.5.2 第 2 题，未逐题独立验算）
> > [!warning] AI 补充：原题与原书答案条件不一致
> > 本题的原书答案代入点与题干指定点不一致，详细对照说明见本节第 1 题折叠答案内的警告；以下仍保留原答案，尚未核验。
>
> **2.** 通过直线 l 的平面束为
>
> $$\lambda(2x+y-3z+2)+\mu(5x+5y-4z+3)=0.$$
>
> 先找过点 P(1,2,3) 的那个平面. 把 P 代入两个平面式子:
>
> $$2+2-9+2=-3,\qquad5+10-12+3=6.$$
>
> 因为 P 要在束中的平面上，所以
>
> $$-3\lambda+6\mu=0\quad\Longrightarrow\quad\lambda=2\mu.$$
>
> 取 $\lambda = 2, \mu = 1$，得过 P 的平面
>
> $$2(2x+y-3z+2)+(5x+5y-4z+3)=0,$$
>
> 化简为
>
> $$\Pi_{1}:9x+7y-10z+7=0.$$
>
> 它的法向量是
>
> $$\vec{n}_{1}=(9,7,-10).$$
>
> 再找束中与 $\Pi_{1}$ 垂直的平面. 原两个平面的法向量为
>
> $$\vec{n}_{A}=(2,1,-3),\qquad\vec{n}_{B}=(5,5,-4).$$
>
> 束中任意平面的法向量是
>
> $$\vec{n}=\lambda\vec{n}_{A}+\mu\vec{n}_{B}.$$
>
> 要求 $\vec{n} \perp \vec{n}_1$，即 $\vec{n} \cdot \vec{n}_1 = 0$:
>
> $$\lambda(55)+\mu(120)=0.$$
>
> 取 $\lambda = -24, \mu = 11$，得到
>
> $$\vec{n}_{2}=-24(2,1,-3)+11(5,5,-4)=(7,31,28).$$
>
> 再在 l 上取一点. 令 z = 0, 解
>
> $$\begin{cases}2x+y=-2,\\5x+5y=-3,\end{cases}$$
>
> 得 $x = -\frac{7}{5}$, $y = \frac{4}{5}$，所以点为
>
> $$\left(-\frac{7}{5},\frac{4}{5},0\right).$$
>
> 把该点代入 7x + 31y + 28z + D = 0，得
>
> $$7\cdot\left(-\frac{7}{5}\right)+31\cdot\frac{4}{5}+D=0\quad\Longrightarrow\quad D=-15.$$
>
> 所以另一个平面为
>
> $$\Pi_{2}:~7x+31y+28z-15=0.$$

**3.** (难度:★) 求一过原点和点 $(6, -3, 2)$，且与平面 $4x - y + 2z = 8$ 垂直的平面方程.

> [!answer]- 原书参考答案（A.5.2 第 3 题，未逐题独立验算）
> **3.** 设所求平面的法向量为 $\mathbf{n} = (A, B, C)$.
>
> 第一步：由「与已知平面垂直」给出一个方程.两平面垂直当且仅当法向量垂直，而 $4x-y+2z=8$的法向量是 $(4,-1,2)$，故
>
> $$\mathbf{n}\cdot(4,-1,2)=0.$$
>
> 第二步:由「过原点与 $(6,-3,2)$」给出另一个方程. 平面过原点, 故“过点 $(6,-3,2)$”等价于向量 $(6,-3,2)$ 与 n 垂直:
>
> $$\mathbf{n}\cdot(6,-3,2)=0.$$
>
> 第三步：解出 n. 满足上面两个条件的 n 与两向量都垂直，取叉积
>
> $$\mathbf{n}=(6,-3,2)\times(4,-1,2)=\left|\begin{matrix}\mathbf{i}&\mathbf{j}&\mathbf{k}\\ 6&-3&2\\ 4&-1&2\end{matrix}\right|=(-4,-4,6)\parallel(2,2,-3).$$
>
> 第四步：写出方程。平面过原点，故
>
> $$\boxed{2x+2y-3z=0}.$$

**4.** （难度：★★）求与四条直线

$$L_{1}:\left\{\begin{aligned}x&=1,\\ y&=0,\end{aligned}\right.\quad L_{2}:\left\{\begin{aligned}y&=1,\\ z&=0,\end{aligned}\right.\quad L_{3}:\left\{\begin{aligned}z&=1,\\ x&=0,\end{aligned}\right.\quad L_{4}:x=y=-2z$$

都相交的直线 l 的方程.

> [!answer]- 原书参考答案（A.5.2 第 4 题，未逐题独立验算）
> **4.** 设所求直线与 $L_{1}, L_{2}, L_{3}$ 的交点分别是
>
> $$P_{1}=\left(1,0,u\right),\quad P_{2}=\left(v,1,0\right),\quad P_{3}=\left(0,w,1\right).$$
>
> 这里 u, v, w 都是待定参数. 因为 $P_{1}, P_{2}, P_{3}$ 在一条直线上, 所以向量
>
> $$\overrightarrow{P_{2}P_{1}}=(1-v,-1,u),\quad\overrightarrow{P_{3}P_{1}}=(-1,w,1-u)$$
>
> 平行. 设比例常数为 k, 则
>
> $$(1-v,-1,u)=k(-1,w,1-u).$$
>
> 逐分量写出：
>
> $$1-v=-k,\qquad-1=k w,\qquad u=k(1-u).$$
>
> 由第二式得 $k = -\frac{1}{w}$. 代入第一式:
>
> $$1-v=\frac{1}{w}\quad\Longrightarrow\quad v=1-\frac{1}{w}.$$
>
> 代入第三式：
>
> $$u=-\frac{1}{w}(1-u)\quad\Longrightarrow\quad u=-\frac{1}{w}+\frac{u}{w}\quad\Longrightarrow\quad u\left(1-\frac{1}{w}\right)=-\frac{1}{w}.$$
>
> 两边同乘w:
>
> $$u(w-1)=-1\quad\Longrightarrow\quad u=\frac{1}{1-w}.$$
>
> 第三步：写出所求直线的参数方程. 所求直线过
>
> $$P_{1}=\left(1,0,\frac{1}{1-w}\right),$$
>
> 方向向量可取 $\overrightarrow{P_1P_2}$:
>
> $$\overrightarrow{P_{1}P_{2}}=(v-1,1-0,0-u)=\left(-\frac{1}{w},1,-\frac{1}{1-w}\right)\sim\left(1,-w,\frac{w}{1-w}\right)$$
>
> （最后一步是同乘 -w，只改变方向的倍数）. 于是所求直线的参数方程为
>
> $$\begin{cases}x=1+t,\\y=-wt,&(t\in\mathbb{R}),\\z=\frac{1}{1-w}+\frac{w}{1-w}t\end{cases}$$
>
> 而 $L_{4}: x = y = -2z$ 的参数方程为
>
> $$\begin{cases}x=s,\\y=s,&(s\in\mathbb{R}).\\z=-\frac{s}{2}\end{cases}$$
>
> 第四步: 联立两组参数方程, 定出 w (把化简过程完整写出来). 让两条直线相交, 就是让上面两组方程有公共解:
>
> $$1+t=s,\qquad-wt=s,\qquad\frac{1}{1-w}+\frac{w}{1-w}t=-\frac{s}{2}.$$
>
> 由第一式 t = s - 1，代入第二式消去 t:
>
> $$\begin{aligned}-w(s-1)=s&\implies-ws+w=s\implies s(1+w)=w\\&\implies s=\frac{w}{1+w}\quad(w\neq-1),\end{aligned}$$
>
> 同时 $t = s - 1 = \frac{w}{1 + w} - 1 = -\frac{1}{1 + w}$. 把 t, s 代入第三式:
>
> $$\frac{1+w t}{1-w}=-\frac{s}{2}\implies2(1+w t)=-s(1-w),$$
>
> 把 $t = -\frac{1}{1 + w}$、 $s = \frac{w}{1 + w}$ 代入:
>
> $$\begin{aligned}2\left(1-\frac{w}{1+w}\right)=-\frac{w(1-w)}{1+w}&\Longrightarrow\frac{2}{1+w}=\frac{w(w-1)}{1+w}\\&\Longrightarrow2=w^{2}-w\Longrightarrow w^{2}-w-2=0.\end{aligned}$$
>
> 解得 w = 2 或 w = -1. 但 w = -1 时上面求 s 的一步要除以 $w + 1$ (回到联立方程组看: 此时第一式 $1 + t = s$ 与第二式 t = s 同时成立会给出 1 = 0), 故 w = -1 舍去, 取 w = 2.
>
> 于是
>
> $$u=\frac{1}{1-2}=-1,\qquad v=1-\frac{1}{2}=\frac{1}{2},$$
>
> 即 $P_{1}=(1,0,-1)$、 $P_{2}=\left(\frac{1}{2},1,0\right)$，方向向量
>
> $$\overrightarrow{P_{1}P_{2}}=\left(-\frac{1}{2},1,1\right)\sim(-1,2,2).$$
>
> 所以所求直线的参数方程是
>
> $$\begin{cases}x=1-r,\\y=2r,&(r\in\mathbb{R}),\\z=-1+2r\end{cases}$$
>
> 化成对称式即 $\frac{x-1}{-1}=\frac{y}{2}=\frac{z+1}{2}$.

## 5.3 曲线与曲面

空间解析几何中最综合的考察方向，主要核心是通过设参数，求解各种曲面方程。此块内容是多元积分学的基础，唯有掌握曲线曲面，才能更好地应对后续的多元积分计算。

**1.** (难度:★★) 设 M 是以三个正半轴为母线的半圆锥面, 求其方程.

> [!answer]- 原书参考答案（A.5.3 第 1 题，未逐题独立验算）
> **1.** 三条正半轴分别是 x 轴、y 轴、z 轴的正半部分，它们关于直线
>
> $$l:x=y=z$$
>
> 对称. 所以这个半圆锥面可以看成: 把 x 轴正半轴绕直线 l 旋转一周得到.
>
> 设 $P=(t,0,0)$ 是 x 轴正半轴上一点，它旋转后得到
>
> $$P^{\prime}=(x,y,z).$$
>
> 第一个不变量：到原点的距离不变，所以
>
> $$|OP^{\prime}|=|OP|\quad\Longrightarrow\quad x^{2}+y^{2}+z^{2}=t^{2}.$$
>
> 第二个不变量: 旋转前后对应点连线垂直于转轴. 转轴方向为
>
> $$\vec{l}=(1,1,1),$$
>
> 而
>
> $$\overrightarrow{PP^{\prime}}=(t-x,-y,-z).$$
>
> 所以
>
> $$\overrightarrow{P P^{\prime}}\cdot\overrightarrow{l}=0\quad\Longrightarrow\quad t-x-y-z=0,$$
>
> 即
>
> $$t=x+y+z.$$
>
> 把 $t = x + y + z$ 代入 $x^{2} + y^{2} + z^{2} = t^{2}$
>
> $$(x+y+z)^{2}=x^{2}+y^{2}+z^{2}.$$
>
> 展开并移项：
>
> $$xy+yz+zx=0.$$
>
> 取 $x + y + z \geqslant 0$ 的那一支，就是所求半圆锥面.

**2.** (难度:★★★) 求直线 $\frac{x-1}{1}=\frac{y}{2}=\frac{z}{2}$ 绕直线 x=y=z 旋转所得的旋转曲面方程.

> [!answer]- 原书参考答案（A.5.3 第 2 题，未逐题独立验算）
> **2.** 转轴方向为
>
> $$\vec{a}=(1,1,1).$$
>
> 把母线写成参数式. 令
>
> $$\frac{x-1}{1}=\frac{y}{2}=\frac{z}{2}=u,$$
>
> 则母线上任意一点为
>
> $$P(u)=(1+u,2u,2u).$$
>
> 旋转后对应点设为 $P' = (x, y, z)$.
>
> 第一个不变量: 沿转轴方向的投影不变. 对点 $P(u)$
>
> $$P(u)\cdot\overrightarrow{a}=(1+u)+2u+2u=1+5u.$$
>
> 对点 $P'$，同样有
>
> $$P^{\prime}\cdot\overrightarrow{a}=x+y+z.$$
>
> 所以
>
> $$x+y+z=1+5u\quad\Longrightarrow\quad u=\frac{x+y+z-1}{5}.$$
>
> 第二个不变量: 到转轴的距离不变. 先算 $P(u)$ 到转轴的距离平方. 点 $P(u)$ 的模长平方为
>
> $$|P(u)|^{2}=(1+u)^{2}+(2u)^{2}+(2u)^{2}=1+2u+9u^{2}.$$
>
> 沿转轴方向的投影平方为
>
> $$\frac{(1+5u)^{2}}{3}.$$
>
> 所以 $P(u)$ 到转轴距离的平方为
>
> $$|P(u)|^{2}-\frac{(1+5u)^{2}}{3}=\frac{2(u-1)^{2}}{3}.$$
>
> 点 $P'$ 到转轴距离的平方为
>
> $$|P^{\prime}|^{2}-\frac{(x+y+z)^{2}}{3}=x^{2}+y^{2}+z^{2}-\frac{(x+y+z)^{2}}{3}.$$
>
> 两边相等：
>
> $$x^{2}+y^{2}+z^{2}-\frac{(x+y+z)^{2}}{3}=\frac{2(u-1)^{2}}{3}.$$
>
> 把 $u = \frac{x + y + z - 1}{5}$ 代入，整理得
>
> $$25(x^{2}+y^{2}+z^{2})-9(x+y+z)^{2}+8(x+y+z)-24=0.$$

**3.** (难度:★★★★) 求与直线 $L_{1}:\frac{x-6}{3}=\frac{y}{2}=\frac{z-1}{1}$ 和直线 $L_{2}:\frac{x}{3}=\frac{y-8}{2}=\frac{z+4}{-2}$ 都相交且与平面 $2x+3y-5=0$ 平行的动直线产生的曲面方程.

> [!answer]- 原书参考答案（A.5.3 第 3 题，未逐题独立验算）
> **3.** 先在两条直线上设出交点. 令
>
> $$P=(6+3s,2s,1+s),\qquad Q=(3t,8+2t,-4-2t).$$
>
> 于是动直线方向为
>
> $$\overrightarrow{PQ}=(3t-6-3s,8+2t-2s,-5-2t-s).$$
>
> 动直线与平面 $2x + 3y - 5 = 0$ 平行，而该平面的法向量是
>
> $$\vec{n}=(2,3,0).$$
>
> 所以
>
> $$\overrightarrow{PQ}\cdot\overrightarrow{n}=0.$$
>
> 也就是
>
> $$2(3t-6-3s)+3(8+2t-2s)=0.$$
>
> 展开：
>
> $$6t-12-6s+24+6t-6s=0\quad\Longrightarrow\quad t=s-1.$$
>
> 把 t = s - 1 代回，动直线过
>
> $$P=\left(6+3s,2s,1+s\right),$$
>
> 方向向量可写成
>
> $$\vec{s}=(-3,2,-1-s).$$
>
> 设动直线上点为 $(x,y,z)$，则
>
> $$\begin{cases}x=6+3s-3r,\\ \\y=2s+2r,\\ \\z=1+s-r(1+s).\end{cases}$$
>
> 由前两式解出 $s, r$:
>
> $$s=\frac{2x+3y-12}{12},\qquad r=\frac{3y-2x+12}{12}.$$
>
> 代入第三式，先写出
>
> $$z=1+\frac{2x+3y-12}{12}-\frac{3y-2x+12}{12}\cdot\frac{2x+3y}{12}.$$
>
> 两边乘144，展开并合并：
>
> $$144z=(2x+3y)(2x-3y),$$
>
> 即
>
> $$4x^{2}-9y^{2}=144z.$$
>
> 这就是动直线扫出的曲面.

**4.** （难度：★★★★）求与三条直线

$$L_{1}:\left\{\begin{aligned}&y-1=0,\\ &x+2z=0,\end{aligned}\right.\quad L_{2}:\left\{\begin{aligned}&y-z=0,\\ &x-2=0,\end{aligned}\right.\quad L_{3}:\frac{x}{2}=\frac{y+1}{0}=\frac{z}{1}$$

都相交的动直线产生的曲面方程.

> [!answer]- 原书参考答案（A.5.3 第 4 题，未逐题独立验算）
> **4.** 在三条已知直线上分别设交点，令三点共线；再让动直线与题目条件配合，最后消去参数. 设交点
>
> $$P_{1}=\left(-2t,1,t\right),\quad P_{2}=\left(2,s,s\right),\quad P_{3}=\left(2u,-1,u\right).$$
>
> 三点共线，所以向量
>
> $$\overrightarrow{P_{2}P_{1}}=(2+2t,s-1,s-t),\quad\overrightarrow{P_{3}P_{1}}=(2u+2t,-2,u-t)$$
>
> 平行. 设比例常数为 k, 则
>
> $$(2+2t,s-1,s-t)=k(2u+2t,-2,u-t).$$
>
> 看第二个分量：
>
> $$k=\frac{s-1}{-2}=\frac{1-s}{2}.$$
>
> 于是前两个关系写为
>
> $$2+2t=\frac{1-s}{2}(2u+2t)=(1-s)(u+t),$$
>
> $$s-t=\frac{1-s}{2}(u-t).$$
>
> 第二式两边乘2:
>
> $$2(s-t)=(1-s)(u-t).$$
>
> 把它与第一式相减：
>
> $$2(1+t)-2(s-t)=(1-s)\big[(u+t)-(u-t)\big].$$
>
> 左边为 $2(1+2t-s)$，右边为 $2t(1-s)$。两边除以2:
>
> $$1+2t-s=t-t s.$$
>
> 移项得
>
> $$1+t-s(1-t)=0\quad\Longrightarrow\quad s=\frac{1+t}{1-t}.$$
>
> 再代回第一式：
>
> $$1-s=1-\frac{1+t}{1-t}=-\frac{2t}{1-t}.$$
>
> 所以
>
> $$2(1+t)=-\frac{2t}{1-t}(u+t).$$
>
> 两边除以2并乘1-t:
>
> $$(1+t)(1-t)=-t(u+t).$$
>
> 左边为 $1 - t^{2}$，右边为 $-tu - t^{2}$。消去 $-t^{2}$：
>
> $$1=-t u\quad\Longrightarrow\quad u=-\frac{1}{t}.$$
>
> 于是动直线过 $(-2t,1,t)$，方向向量可取
>
> $$\left(2(1-t^{2}),2t,1+t^{2}\right).$$
>
> 设动直线参数为 r:
>
> $$\begin{cases}x=-2t+2r(1-t^{2}),\\y=1+2rt,\\z=t+r(1+t^{2}).\end{cases}$$
>
> 记 a = rt = $\frac{y-1}{2}$. 由前两式解出 t, r 的表达式, 再代入第三式消参, 得
>
> $$x^{2}+4y^{2}-4z^{2}=4.$$
>
> 多个参数时，先解线性方程把一部分参数表示出来，再代回剩余约束.

**5.** (难度: ★★★★★) 设一球面的方程为 $x^{2} + y^{2} + (z + 1)^{2} = 4$，从原点向球上任意一点 Q 处的切平面作垂线，垂足为 P，当 Q 在球面上变动时，求 P 的运动轨迹所满足的曲线方程.

> [!answer]- 原书参考答案（A.5.3 第 5 题，未逐题独立验算）
> **5.** 球心在 z 轴上，切平面的法向量就是 $\overrightarrow{CQ}$。把垂足 P 写成法向量的倍数，再用 “P 在切平面上” 和 “Q 在球面上” 这两个条件逐步消去 Q 的坐标。设
>
> $$Q=(a,b,c).$$
>
> 因为 Q 在球面 $x^{2}+y^{2}+(z+1)^{2}=4$ 上，所以
>
> $$a^{2}+b^{2}+(c+1)^{2}=4.$$
>
> 球心为 C = (0,0,-1)，故 Q 处切平面的法向量为
>
> $$\overrightarrow{CQ}=(a,b,c+1).$$
>
> 设切平面上任一点为 $(x,y,z)$. 切平面过 Q, 所以
>
> $$a(x-a)+b(y-b)+(c+1)(z-c)=0.$$
>
> 移项，把含 x, y, z 的项留在左边：
>
> $$a x+b y+(c+1)z=a^{2}+b^{2}+(c+1)c.$$
>
> 下面用（1）式把（2）式右边化成只含 c 的形式. 由（1）得
>
> $$a^{2}+b^{2}=4-(c+1)^{2}=3-2c-c^{2},$$
>
> 所以
>
> $$a^{2}+b^{2}+(c+1)c=(3-2c-c^{2})+(c^{2}+c)=3-c.$$
>
> 于是切平面方程化简为
>
> $$a x+b y+(c+1)z=3-c.$$
>
> 从原点向切平面作垂线，垂足 P 一定在法线上，所以可以设
>
> $$\overrightarrow{OP}=\lambda(a,b,c+1),$$
>
> 也就是
>
> $$P=\left(\lambda a,\lambda b,\lambda(c+1)\right).$$
>
> 把 P 的坐标代入切平面方程 (3):
>
> $$a(\lambda a)+b(\lambda b)+(c+1)\lambda(c+1)=3-c.$$
>
> 左边提出 $\lambda$:
>
> $$\lambda\left(a^{2}+b^{2}+(c+1)^{2}\right)=3-c.$$
>
> 再利用（1）式：
>
> $$4\lambda=3-c,$$
>
> 所以
>
> $$\lambda=\frac{3-c}{4}.$$
>
> 接下来消去a, b, c. 先算 P 到原点的距离平方:
>
> $$|\overrightarrow{OP}|^{2}=(\lambda a)^{2}+(\lambda b)^{2}+(\lambda(c+1))^{2}=\lambda^{2}(a^{2}+b^{2}+(c+1)^{2}).$$
>
> 由(1)式，右边括号为4，所以
>
> $$|\overrightarrow{OP}|^{2}=4\lambda^{2}.$$
>
> 记
>
> $$\rho^{2}=|\overrightarrow{OP}|^{2}=x^{2}+y^{2}+z^{2}.$$
>
> 由(1)式可知 $(c+1)^{2}\leqslant4$，即 $-3\leqslant c\leqslant1$，所以3-c>0，从而由(4)知 $\lambda>0$。因此
>
> $$\rho=2\lambda.$$
>
> 另一方面，由 P 的第三个坐标
>
> $$z=\lambda(c+1)$$
>
> 解出 c:
>
> $$c+1=\frac{z}{\lambda},\qquad c=\frac{z}{\lambda}-1.$$
>
> 把(6)代入(4):
>
> $$\lambda=\frac{3-\left(\frac{z}{\lambda}-1\right)}{4}=\frac{4-\frac{z}{\lambda}}{4}=1-\frac{z}{4\lambda}.$$
>
> 两边同乘4 $\lambda$:
>
> $$4\lambda^{2}=4\lambda-z.$$
>
> 再由(5)把 $\lambda=\frac{\rho}{2}$代入(7):
>
> $$4\left(\frac{\rho}{2}\right)^{2}=4\cdot\frac{\rho}{2}-z,$$
>
> 即
>
> $$\rho^{2}=2\rho-z.$$
>
> 把z移项：
>
> $$\rho^{2}+z=2\rho.$$
>
> 两边平方，并把 $\rho^{2}=x^{2}+y^{2}+z^{2}$ 代回：
>
> $$(\rho^{2}+z)^{2}=4\rho^{2},$$
>
> 也就是
>
> $$(x^{2}+y^{2}+z^{2}+z)^{2}=4(x^{2}+y^{2}+z^{2}).$$
>
> 这道题有三个消去对象 a, b, c: a, b 通过模长 $\rho$ 合并掉, c 再通过 P 的 z 坐标和比例式 $\lambda = \frac{3 - c}{4}$ 消掉.

**6.** (难度: ★★★) 设曲面 $z = x^{2} + y^{2} - 2x - y - \frac{5}{4}$ 在区域 D: $x \geqslant 0, y \geqslant 0, 2x + y \leqslant 3$ 上的最低点 P 处的切平面为 $\Pi$，曲线 $\left\{\begin{aligned}x^{2} + y^{2} + z^{2} &= 6,\\ x + y + z &= 0\end{aligned}\right.$ 在点 $M(1,1,-2)$ 处的切线为 L；又设 L 在平面 $\Pi$ 上的投影为 $L_{1}$，求点 P 到投影 $L_{1}$ 的距离.

> [!answer]- 原书参考答案（A.5.3 第 6 题，未逐题独立验算）
> **6.** 先求曲面最低点和切平面，再求曲线切线方向，最后把点到投影直线的距离化成向量外积. 配方：
>
> $$z=x^{2}+y^{2}-2x-y-\frac{5}{4}=(x-1)^{2}+\left(y-\frac{1}{2}\right)^{2}-\frac{5}{2}.$$
>
> 在 D 内最低点为
>
> $$P=\left(1,\frac{1}{2},-\frac{5}{2}\right),$$
>
> 最低点处的切平面是
>
> $$z=-\frac{5}{2}.$$
>
> 曲线在 M(1,1,-2) 处, 两个曲面的法向量分别为
>
> $$\vec{n}_{1}=(2,2,-4),\qquad\vec{n}_{2}=(1,1,1).$$
>
> 切线方向为
>
> $$\vec{s}=\vec{n}_{1}\times\vec{n}_{2}=(6,-6,0),$$
>
> 可取
>
> $$\vec{s}=(1,-1,0).$$
>
> 所以切线
>
> $$L:\ (1+t,1-t,-2).$$
>
> 它在平面 $z = -\frac{5}{2}$ 上的投影就是把 z 改成 $-\frac{5}{2}$，其余不变：
>
> $$L_{1}:\left(1+t,1-t,-\frac{5}{2}\right).$$
>
> 在 $L_{1}$上取点
>
> $$Q=\left(1,1,-\frac{5}{2}\right).$$
>
> 则
>
> $$\overrightarrow{QP}=\left(0,-\frac{1}{2},0\right).$$
>
> 点到直线的距离为
>
> $$d=\frac{|\overrightarrow{QP}\times\overrightarrow{s}|}{|\overrightarrow{s}|}=\frac{1/2}{\sqrt{2}}=\frac{\sqrt{2}}{4}.$$
>
> 投影到水平面 $z = -\frac{5}{2}$ 时，只需要改 z 坐标.

**7.** (难度: ★★★★) 由椭球面 $S: \frac{x^{2}}{a^{2}} + \frac{y^{2}}{b^{2}} + \frac{z^{2}}{c^{2}} = 1$ 的中心 O 任意引三条相互垂直的射线，与椭球面 S 分别交于 $P_{1}, P_{2}, P_{3}$. 设 $\left\| \overrightarrow{OP_{i}} \right\| = r_{i}, i = 1, 2, 3$，证明：

$$\frac{1}{r_{1}^{2}}+\frac{1}{r_{2}^{2}}+\frac{1}{r_{3}^{2}}=\frac{1}{a^{2}}+\frac{1}{b^{2}}+\frac{1}{c^{2}}.$$

> [!answer]- 原书参考答案（A.5.3 第 7 题，未逐题独立验算）
> **7.** 三条互相垂直的射线可以看成三个互相垂直的单位向量；把椭球条件写成方向余弦，再对三条射线求和。设三条射线上的单位向量为 $\overrightarrow{u}_{1}$， $\overrightarrow{u}_{2}$， $\overrightarrow{u}_{3}$，它们两两垂直且长度都是1。记
>
> $$\overrightarrow{OP_{i}}=r_{i}\overrightarrow{u_{i}},\qquad i=1,2,3.$$
>
> 因为 $P_{i}$ 在椭球面
>
> $$\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}+\frac{z^{2}}{c^{2}}=1$$
>
> 上，所以
>
> $$\frac{1}{r_{i}^{2}}=\frac{u_{i1}^{2}}{a^{2}}+\frac{u_{i2}^{2}}{b^{2}}+\frac{u_{i3}^{2}}{c^{2}}.$$
>
> 对i=1,2,3求和：
>
> $$\sum_{i=1}^{3}\frac{1}{r_{i}^{2}}=\frac{1}{a^{2}}\sum_{i}u_{i1}^{2}+\frac{1}{b^{2}}\sum_{i}u_{i2}^{2}+\frac{1}{c^{2}}\sum_{i}u_{i3}^{2}.$$
>
> 三个单位向量两两垂直，所以它们组成一组正交基。在正交基中，每个坐标分量的平方和等于1，即
>
> $$\sum_{i}u_{i1}^{2}=\sum_{i}u_{i2}^{2}=\sum_{i}u_{i3}^{2}=1.$$
>
> 因此
>
> $$\sum_{i=1}^{3}\frac{1}{r_{i}^{2}}=\frac{1}{a^{2}}+\frac{1}{b^{2}}+\frac{1}{c^{2}}.$$
>
> 三个两两垂直的单位向量组成标准正交基, 每个方向上的分量平方和为 1, 这就是本题的核心.

**8.** (难度:★★★★) 球面 S 与直线 $L_{1}:\frac{x-1}{3}=\frac{y+4}{6}=\frac{z-6}{4}$ 相切于点 A(1,-4,6),

且该球面与直线 $L_{2}:\frac{x-4}{2}=\frac{y+3}{1}=\frac{z-2}{-6}$ 相切于点 B(4,-3,2).

(1) 求球面 S 的方程.

(2) 设点 P 为球面 S 上的动点, 过点 P 作任意三条两两垂直的弦, 记它们的长度分别为 a, b, c, 证明: $a^{2} + b^{2} + c^{2}$ 为定值.

> [!answer]- 原书参考答案（A.5.3 第 8 题，未逐题独立验算）
> **8.** 球心在两条切点法线的交点上；第二问把弦长平方写成球半径与投影，再用三条弦方向两两垂直求和. (1) 设球心 O = (X, Y, Z). 因为球与 $L_{1}$ 在 A 点相切，所以 $\overrightarrow{OA}$ 垂直于 $L_{1}$ 的方向向量 (3, 6, 4):
>
> $$3(X-1)+6(Y+4)+4(Z-6)=0\quad\Longrightarrow\quad3X+6Y+4Z=3.$$
>
> 同理， $\overrightarrow{OB}$ 垂直于 $L_{2}$ 的方向向量 (2,1,-6):
>
> $$2(X-4)+(Y+3)-6(Z-2)=0\quad\Longrightarrow\quad2X+Y-6Z=-7.$$
>
> 又 A, B 都在球面上, 所以
>
> $$|\overrightarrow{OA}|=|\overrightarrow{OB}|.$$
>
> 两边平方展开，得到
>
> $$3X+Y-4Z=-12.$$
>
> 联立
>
> $$\begin{cases}3X+6Y+4Z=3,\\2X+Y-6Z=-7,\\3X+Y-4Z=-12,\end{cases}$$
>
> 解得
>
> $$O=(-5,3,0).$$
>
> 半径平方为
>
> $$R^{2}=|\overrightarrow{OA}|^{2}=(-6)^{2}+7^{2}+(-6)^{2}=121.$$
>
> 所以球面方程为
>
> $$(x+5)^{2}+(y-3)^{2}+z^{2}=121.$$
>
> (2) 设三条两两垂直弦的单位方向为 $\vec{u}_{1}, \vec{u}_{2}, \vec{u}_{3}$，记
>
> $$\overrightarrow{p}=\overrightarrow{OP}.$$
>
> 因为 P 在球面上, 所以
>
> $$|\overrightarrow{p}|=R.$$
>
> 过 P 沿方向 $\overrightarrow{u}_{i}$ 的弦，长度平方为
>
> $$L_{i}^{2}=4(\overrightarrow{p}\cdot\overrightarrow{u_{i}})^{2}.$$
>
> 这是因为球心到弦的距离为 $\sqrt{R^{2}-(\vec{p}\cdot\vec{u}_{i})^{2}}$，半弦长用勾股定理求得，再平方乘四.对三条两两垂直的方向求和：
>
> $$a^{2}+b^{2}+c^{2}=4\sum_{i=1}^{3}(\overrightarrow{p}\cdot\overrightarrow{u}_{i})^{2}.$$
>
> 由于 $\vec{u}_1, \vec{u}_2, \vec{u}_3$ 是三个互相垂直的单位向量，向量 $\vec{p}$ 在这三个方向上的投影平方和等于 $|\vec{p}|^2$，所以
>
> $$a^{2}+b^{2}+c^{2}=4R^{2}=484.$$
>
> 第二问不要被“三条弦”吓住；把每条弦长度平方写成 $4(\vec{p} \cdot \vec{u}_{i})^{2}$，求和时正交基性质自然消掉交叉项。

---

# 基础篇·第六章 多元微分学

## 6.1 多元极限

主要作为与多元微分相关的衔接内容,不会作重点考察,了解一般二元极限的求解即可.

**1.** (难度:★★) 证明: 极限 $\lim_{{x \to 0 \atop y \to 0}} \frac{xy}{\sqrt{x + y + 1} - 1}$ 不存在.

> [!answer]- 原书参考答案（A.6.1 第 1 题，未逐题独立验算）
> **1.** 先对分子作根式有理化：
>
> $$\sqrt{x^{2}+y^{2}}-\sqrt{x^{2}-xy+y^{2}}=\frac{xy}{\sqrt{x^{2}+y^{2}}+\sqrt{x^{2}-xy+y^{2}}}.$$
>
> 所以原式为
>
> $$F(x,y)=\frac{xy}{x+y}\cdot\frac{1}{\sqrt{x^{2}+y^{2}}+\sqrt{x^{2}-xy+y^{2}}}.$$
>
> 这里最容易犯的错误是：因为
>
> $$\left|\frac{x}{x+y}\right|\leq1$$
>
> 而把 $\frac{xy}{x+y}$直接放大成 $|y|$.这个不等号在 $x+y<0$时根本不成立.因此不能这样夹逼.
>
> 取路径 y = x. 当 x > 0 时，
>
> $$\sqrt{x^{2}+y^{2}}=\sqrt{2}x,\qquad\sqrt{x^{2}-xy+y^{2}}=x,$$
>
> 代入(1)得
>
> $$F(x,x)=\frac{x^{2}}{2x}\cdot\frac{1}{(\sqrt{2}+1)x}=\frac{1}{2(\sqrt{2}+1)}.$$
>
> 再取路径 $y=-x+x^2$，即 $x+y=x^2$。当 $x\to0$ 时,
>
> $$xy=x(-x+x^{2})=-x^{2}+x^{3},$$
>
> 且两个根式都趋于0，它们之和与 $|x|$同阶.于是
>
> $$F(x,-x+x^{2})=\frac{-x^{2}+x^{3}}{x^{2}}\cdot\frac{1}{\sqrt{x^{2}+y^{2}}+\sqrt{x^{2}-x y+y^{2}}}\to-\infty.$$
>
> 两条路径的极限不同，所以原极限不存在.

**2.** (难度:★) 求极限: $\lim_{{x \to 0 \atop y \to 0}} \frac{(y - x)x}{\sqrt{x^2 + y^2}}$.

> [!answer]- 原书参考答案（A.6.1 第 2 题，未逐题独立验算）
> **2.** 分子是两个小量相乘，分母是 $\sqrt{x^{2}+y^{2}}$. 直接用 $|x|\leq\rho$ 夹逼. 记 $\rho=\sqrt{x^{2}+y^{2}}$. 因为
>
> $$\left|x\right|\leqslant\rho,\qquad\left|y-x\right|\leqslant\left|y\right|+\left|x\right|\leqslant2\rho,$$
>
> 所以
>
> $$0\leqslant\left|\frac{(y-x)x}{\sqrt{x^{2}+y^{2}}}\right|=\frac{|y-x||x|}{\rho}\leqslant\frac{2\rho\cdot\rho}{\rho}=2\rho\rightarrow0.$$
>
> 因此极限为 0. 二元极限中最常用的两个基本不等式是 $|x| \leqslant \rho$、 $|xy| \leqslant \frac{x^2 + y^2}{2}$.

**3.** (难度:★★) 设可微函数 $f(x,y)$ 满足 $\frac{\partial f}{\partial x} = -f(x,y)$, $f\left(0,\frac{\pi}{2}\right) = 1$ 且有:

$$\lim_{n\to\infty}\left(\frac{f\left(0,y+\frac{1}{n}\right)}{f(0,y)}\right)^{n}=e^{\cot y},$$

据此求 $f(x,y)$.

> [!answer]- 原书参考答案（A.6.1 第 3 题，未逐题独立验算）
> **3.** 由 $\frac{\partial f}{\partial x} = -f(x, y)$ 先解出 $f(x, y)$ 关于 x 的结构，得到只含 y 的待定函数；再用极限式求这个待定函数的对数导数。把 y 看作常数，解
>
> $$\frac{\partial f}{\partial x}=-f(x,y),$$
>
> 得
>
> $$f(x,y)=C(y)e^{-x}.$$
>
> 于是 $f(0,y)=C(y)$. 由
>
> $$\lim_{n\to\infty}\left(\frac{C\left(y+\frac{1}{n}\right)}{C(y)}\right)^{n}=e^{\cot y}$$
>
> 取对数：
>
> $$\lim_{n\to\infty}n\ln\frac{C\left(y+\frac{1}{n}\right)}{C(y)}=\cot y.$$
>
> 设 $h=\frac{1}{n}$，则
>
> $$\lim_{h\to0}\frac{\ln C(y+h)-\ln C(y)}{h}=\cot y,$$
>
> 即
>
> $$\frac{C^{\prime}(y)}{C(y)}=\cot y.$$
>
> 积分得
>
> $$\ln C(y)=\ln\sin y+\ln C_{0},$$
>
> 所以 $C(y)=C_{0}\sin y$ 。又 $f(0,\pi/2)=1$ ，即 $C(\pi/2)=1$ ，故 $C_{0}=1$ 。于是
>
> $$f(x,y)=e^{-x}\sin y.$$
>
> 形如 $\left(\frac{a_{n+1}}{a_n}\right)^n$ 的极限取对数后就是对数导数, 这是由离散信息反解连续函数的常用技巧.

## 6.2 复合函数偏导数

中档难度的计算题代表, 多元积分的复合偏导数计算相对比较繁琐, 一定要了解一般的计算思路, 多加练习, 提高计算准确率.

**1.** (难度:★★★) 设 $F(x_{1}, x_{2}, x_{3}) = \int_{0}^{2\pi} f(x_{1} + x_{3} \cos \varphi, x_{2} + x_{3} \sin \varphi) \, \mathrm{d}\varphi$，其中 $f(u, v)$ 具有二阶连续偏导数. 已知:

$$\frac{\partial F}{\partial x_{i}}=\int_{0}^{2\pi}\frac{\partial}{\partial x_{i}}\left[f(x_{1}+x_{3}\cos\varphi,\ x_{2}+x_{3}\sin\varphi)\right]\mathrm{d}\varphi,$$

$$\frac{\partial^{2}F}{\partial x_{i}^{2}}=\int_{0}^{2\pi}\frac{\partial^{2}}{\partial x_{i}^{2}}\left[f(x_{1}+x_{3}\cos\varphi,\ x_{2}+x_{3}\sin\varphi)\right]\mathrm{d}\varphi,\quad i=1,2,3.$$

试求 $x_{3}\left(\frac{\partial^{2}F}{\partial x_{1}^{2}}+\frac{\partial^{2}F}{\partial x_{2}^{2}}-\frac{\partial^{2}F}{\partial x_{3}^{2}}\right)-\frac{\partial F}{\partial x_{3}}$ 并化简.

> [!answer]- 原书参考答案（A.6.2 第 1 题，未逐题独立验算）
> **1.** 老老实实先对 $x_{1}, x_{2}, x_{3}$ 求偏导，把所有二阶项都写进积分号里；最后对 $\varphi$ 分部积分，把 $\frac{\partial F}{\partial x_{3}}$ 化成与前面二阶项相同的积分，二者相减为 0。这里 $f = f(u, v)$，而 u, v 由 $x_{1}, x_{2}, x_{3}$ 给出。记
>
> $$u=x_{1}+x_{3}\cos\varphi,\qquad v=x_{2}+x_{3}\sin\varphi.$$
>
> 先算一、二阶偏导（积分号下求导，边界项为零）：
>
> $$\frac{\partial F}{\partial x_{3}}=\int_{0}^{2\pi}\left(\frac{\partial f}{\partial u}\cos\varphi+\frac{\partial f}{\partial v}\sin\varphi\right)\mathrm{d}\varphi,$$
>
> $$\frac{\partial^{2}F}{\partial x_{3}^{2}}=\int_{0}^{2\pi}\left(\frac{\partial^{2}f}{\partial u^{2}}\cos^{2}\varphi+2\frac{\partial^{2}f}{\partial u\partial v}\sin\varphi\cos\varphi+\frac{\partial^{2}f}{\partial v^{2}}\sin^{2}\varphi\right)\mathrm{d}\varphi,$$
>
> $$\frac{\partial^{2}F}{\partial x_{1}^{2}}=\int_{0}^{2\pi}\frac{\partial^{2}f}{\partial u^{2}}\mathrm{d}\varphi,\qquad\frac{\partial^{2}F}{\partial x_{2}^{2}}=\int_{0}^{2\pi}\frac{\partial^{2}f}{\partial v^{2}}\mathrm{d}\varphi.$$
>
> 所以
>
> $$\begin{aligned}&\frac{\partial^{2}F}{\partial x_{1}^{2}}+\frac{\partial^{2}F}{\partial x_{2}^{2}}-\frac{\partial^{2}F}{\partial x_{3}^{2}}\\ &=\int_{0}^{2\pi}\left(\sin^{2}\varphi\frac{\partial^{2}f}{\partial u^{2}}-2\sin\varphi\cos\varphi\frac{\partial^{2}f}{\partial u\partial v}+\cos^{2}\varphi\frac{\partial^{2}f}{\partial v^{2}}\right)\\ \end{aligned}$$
>
> > [!warning] AI 补充：原书公式疑有漏项
> > 原书第 156 页这一积分式末尾未写 $\mathrm{d}\varphi$；下文又引用“与（*）比较”，但此处未显示（*）标号。转写保留原式，不将缺失部分静默补入。
>
> 下面处理 $\frac{\partial F}{\partial x_{3}}$，直接对两项分部积分：
>
> $$\int_{0}^{2\pi}f_{u}\cos\varphi\mathrm{d}\varphi=\int_{0}^{2\pi}f_{u}\mathrm{d}(\sin\varphi)=[f_{u}\sin\varphi]_{0}^{2\pi}-\int_{0}^{2\pi}\sin\varphi\mathrm{d}f_{u}.$$
>
> 因为 $f_{u}$ 关于 $\varphi$ 以 $2\pi$ 为周期，边界项为零。又
>
> $$\mathrm{d}f_{u}=f_{u u}\mathrm{d}u+f_{u v}\mathrm{d}v=x_{3}(-f_{u u}\sin\varphi+f_{u v}\cos\varphi)\mathrm{d}\varphi,$$
>
> 所以
>
> $$\int_{0}^{2\pi}f_{u}\cos\varphi\mathrm{d}\varphi=x_{3}\int_{0}^{2\pi}\left(f_{u u}\sin^{2}\varphi-f_{u v}\sin\varphi\cos\varphi\right)\mathrm{d}\varphi.$$
>
> 同理
>
> $$\int_{0}^{2\pi}f_{v}\sin\varphi\mathrm{d}\varphi=\int_{0}^{2\pi}f_{v}\mathrm{d}(-\cos\varphi)=[-f_{v}\cos\varphi]_{0}^{2\pi}+\int_{0}^{2\pi}\cos\varphi\mathrm{d}f_{v},$$
>
> 边界项仍为零，且
>
> $$\mathrm{d}f_{v}=f_{u v}\mathrm{d}u+f_{v v}\mathrm{d}v=x_{3}(-f_{u v}\sin\varphi+f_{v v}\cos\varphi)\mathrm{d}\varphi,$$
>
> 故
>
> $$\int_{0}^{2\pi}f_{v}\sin\varphi\mathrm{d}\varphi=x_{3}\int_{0}^{2\pi}\left(-f_{uv}\sin\varphi\cos\varphi+f_{vv}\cos^{2}\varphi\right)\mathrm{d}\varphi.$$
>
> 两式相加得
>
> $$\frac{\partial F}{\partial x_{3}}=x_{3}\int_{0}^{2\pi}\left(f_{uu}\sin^{2}\varphi-2f_{uv}\sin\varphi\cos\varphi+f_{vv}\cos^{2}\varphi\right)\mathrm{d}\varphi.$$
>
> 与 $^{*}$比较，立即得到
>
> $$x_{3}\left(\frac{\partial^{2}F}{\partial x_{1}^{2}}+\frac{\partial^{2}F}{\partial x_{2}^{2}}-\frac{\partial^{2}F}{\partial x_{3}^{2}}\right)-\frac{\partial F}{\partial x_{3}}=0.$$
>
> 先求偏导，再对 $\varphi$ 分部积分： $\frac{\partial F}{\partial x_3}$ 分部后与 $x_3\left(\frac{\partial^2 F}{\partial x_1^2} + \frac{\partial^2 F}{\partial x_2^2} - \frac{\partial^2 F}{\partial x_3^2}\right)$ 的积分完全一样，相减为 0. 这里没有引入任何辅助函数，直接分部积分即可.

**2.** (难度：★★★) 设函数 $f(x,y)$ 具有连续偏导数, 且对任意 x,y, 满足:

$$\left(\frac{\partial f}{\partial x}\right)^{2}+\left(\frac{\partial f}{\partial y}\right)^{2}=4.$$

又设 $g(u,v)=f\left(uv,\frac{1}{2}(u^{2}-v^{2})\right)$，且对任意 u,v，满足：

$$a\left(\frac{\partial g}{\partial u}\right)^{2}-b\left(\frac{\partial g}{\partial v}\right)^{2}=u^{2}+v^{2}.$$

据此求常数a,b的值.

> [!answer]- 原书参考答案（A.6.2 第 2 题，未逐题独立验算）
> **2.** 先算出 $\frac{\partial g}{\partial u}, \frac{\partial g}{\partial v}$，再计算 $\left(\frac{\partial g}{\partial u}\right)^{2} + \left(\frac{\partial g}{\partial v}\right)^{2}$. 只要把交叉项配成平方和，就能用 $\left(\frac{\partial f}{\partial x}\right)^{2} + \left(\frac{\partial f}{\partial y}\right)^{2} = 4$. 这里 $g = g(x, y)$，而 x, y 由 u, v 给出. 记 x = uv, $y = \frac{1}{2}(u^{2} - v^{2})$. 则
>
> $$\frac{\partial x}{\partial u}=v,\quad\frac{\partial x}{\partial v}=u,\quad\frac{\partial y}{\partial u}=u,\quad\frac{\partial y}{\partial v}=-v.$$
>
> 所以
>
> $$\frac{\partial g}{\partial u}=\frac{\partial f}{\partial x}v+\frac{\partial f}{\partial y}u,\qquad\frac{\partial g}{\partial v}=\frac{\partial f}{\partial x}u-\frac{\partial f}{\partial y}v.$$
>
> 于是
>
> $$\begin{aligned}\left(\frac{\partial g}{\partial u}\right)^{2}+\left(\frac{\partial g}{\partial v}\right)^{2}&=(v\frac{\partial f}{\partial x}+u\frac{\partial f}{\partial y})^{2}+(u\frac{\partial f}{\partial x}-v\frac{\partial f}{\partial y})^{2}\\&=(u^{2}+v^{2})(\left(\frac{\partial f}{\partial x}\right)^{2}+\left(\frac{\partial f}{\partial y}\right)^{2}).\end{aligned}$$
>
> 由 $\left(\frac{\partial f}{\partial x}\right)^{2}+\left(\frac{\partial f}{\partial y}\right)^{2}=4$，得
>
> $$\left(\frac{\partial g}{\partial u}\right)^{2}+\left(\frac{\partial g}{\partial v}\right)^{2}=4(u^{2}+v^{2}).$$
>
> 即
>
> $$\frac{1}{4}\left(\frac{\partial g}{\partial u}\right)^{2}+\frac{1}{4}\left(\frac{\partial g}{\partial v}\right)^{2}=u^{2}+v^{2}.$$
>
> 与
>
> $$a\left(\frac{\partial g}{\partial u}\right)^{2}-b\left(\frac{\partial g}{\partial v}\right)^{2}=u^{2}+v^{2}$$
>
> 比较，得
>
> $$a=\frac{1}{4},\quad b=-\frac{1}{4}.$$
>
> 本题的几何意义是: 线性变换 $(x, y) \mapsto (uv, \frac{1}{2}(u^2 - v^2))$ 是保“到原点距离”的伸缩, 所以偏导向量的模长信息被完整保留.

**3.** (难度：★★★★) 设 $z = z(x, y)$ 具有一阶连续偏导数, $w = w(u, v)$ 是由方程组

$$u=x^{2}+y^{2},\quad v=\frac{1}{x}+\frac{1}{y},\quad z=e^{w+x+y}$$

所确定的隐函数. 试将方程 $y\frac{\partial z}{\partial x}-x\frac{\partial z}{\partial y}=(y-x)z(x\neq y)$ 化成 $\frac{\partial w}{\partial u},\frac{\partial w}{\partial v}$ 所满足的关系式.

> [!answer]- 原书参考答案（A.6.2 第 3 题，未逐题独立验算）
> **3.** 由 $z = e^{w+x+y}$， $\frac{\partial z}{\partial x}$， $\frac{\partial z}{\partial y}$ 都含 z 因子。把原式除以 z 后，只剩 w 对 u，v 的偏导；再比较系数即可。
>
> $$链条：w\longrightarrow(u,v)\longrightarrow(x,y),\qquad z\longrightarrow(w,x,y).$$
>
> 由 $z=e^{w+x+y}$，有
>
> $$\frac{\partial z}{\partial x}=z(\frac{\partial w}{\partial x}+1),\qquad\frac{\partial z}{\partial y}=z(\frac{\partial w}{\partial y}+1).$$
>
> 又 $w = w(u, v)$，且
>
> $$\frac{\partial u}{\partial x}=2x,\quad\frac{\partial u}{\partial y}=2y,\quad\frac{\partial v}{\partial x}=-\frac{1}{x^{2}},\quad\frac{\partial v}{\partial y}=-\frac{1}{y^{2}}.$$
>
> 所以
>
> $$\frac{\partial w}{\partial x}=2x\frac{\partial w}{\partial u}-\frac{1}{x^{2}}\frac{\partial w}{\partial v},\qquad\frac{\partial w}{\partial y}=2y\frac{\partial w}{\partial u}-\frac{1}{y^{2}}\frac{\partial w}{\partial v}.$$
>
> 代入：
>
> $$\begin{aligned}y\frac{\partial z}{\partial x}-x\frac{\partial z}{\partial y}&=z\left[y(\frac{\partial w}{\partial x}+1)-x(\frac{\partial w}{\partial y}+1)\right]\\&=z\left[y\frac{\partial w}{\partial x}-x\frac{\partial w}{\partial y}+y-x\right].\end{aligned}$$
>
> 而
>
> $$y\frac{\partial w}{\partial x}-x\frac{\partial w}{\partial y}=y\left(2x\frac{\partial w}{\partial u}-\frac{1}{x^{2}}\frac{\partial w}{\partial v}\right)-x\left(2y\frac{\partial w}{\partial u}-\frac{1}{y^{2}}\frac{\partial w}{\partial v}\right)=\left(\frac{x}{y^{2}}-\frac{y}{x^{2}}\right)\frac{\partial w}{\partial v}.$$
>
> 原方程 $y\frac{\partial z}{\partial x}-x\frac{\partial z}{\partial y}=(y-x)z$ 两边除以 z:
>
> $$\left(\frac{x}{y^{2}}-\frac{y}{x^{2}}\right)\frac{\partial w}{\partial v}+\left(y-x\right)=y-x.$$
>
> 即
>
> $$\left(\frac{x}{y^{2}}-\frac{y}{x^{2}}\right)\frac{\partial w}{\partial v}=0.$$
>
> 当 $x\neq y$时，
>
> $$\frac{x}{y^{2}}-\frac{y}{x^{2}}=\frac{x^{3}-y^{3}}{x^{2}y^{2}}\neq0,$$
>
> 所以
>
> $$\frac{\partial w}{\partial v}=0.$$
>
> 本题先利用 $z = e^{w+x+y}$ 把 $\frac{\partial z}{\partial x}, \frac{\partial z}{\partial y}$ 与 $\frac{\partial w}{\partial x}, \frac{\partial w}{\partial y}$ 联系起来，再除以 z，是消去指数因子的关键.

**4.** (难度:★★) 若函数 $f(x,y,z)$ 对任意 t > 0 恒满足关系式: $f(tx,ty,tz) = t^{k}f(x,y,z)$，则称之为 k 次齐次函数. 试证: k 次齐次可微函数 $f(x,y,z)$ 满足关系式:

$$x\frac{\partial f}{\partial x}+y\frac{\partial f}{\partial y}+z\frac{\partial f}{\partial z}=k f(x,y,z).$$

> [!answer]- 原书参考答案（A.6.2 第 4 题，未逐题独立验算）
> **4.** 这里 $g = g(t)$，其中 $g(t) = f(tx, ty, tz)$。把 x, y, z 暂时看作常数，令
>
> $$g(t)=f(tx,ty,tz).$$
>
> 由题设 $g(t)=t^{k}f(x,y,z)$. 对 t 用复合函数链式法则:
>
> $$g^{\prime}(t)=x\frac{\partial f}{\partial x}(t x,t y,t z)+y\frac{\partial f}{\partial y}(t x,t y,t z)+z\frac{\partial f}{\partial z}(t x,t y,t z).$$
>
> 另一方面，直接对 $t^{k}f(x,y,z)$ 求导得
>
> $$g^{\prime}(t)=kt^{k-1}f(x,y,z).$$
>
> 令t=1，即得
>
> $$x\frac{\partial f}{\partial x}(x,y,z)+y\frac{\partial f}{\partial y}(x,y,z)+z\frac{\partial f}{\partial z}(x,y,z)=k f(x,y,z).$$

**5.** (难度:★★★) 设 $x = e^{u+v}$, $y=e^{u-v}$，且满足方程:

$$x^{2}\frac{\partial^{2}z}{\partial x^{2}}+y^{2}\frac{\partial^{2}z}{\partial y^{2}}+x\frac{\partial z}{\partial x}+y\frac{\partial z}{\partial y}=0.$$

证明： $\frac{\partial^{2}z}{\partial u^{2}}+\frac{\partial^{2}z}{\partial v^{2}}=0.$

> [!answer]- 原书参考答案（A.6.2 第 5 题，未逐题独立验算）
> **5.** 令 $r = u + v$、s = u - v，则 $x = e^{r}$， $y = e^{s}$。把 $\frac{\partial}{\partial u}$， $\frac{\partial}{\partial v}$ 写成 $x\frac{\partial}{\partial x} \pm y\frac{\partial}{\partial u}$，二阶求和即可。
>
> 链条：
>
> $$z\longrightarrow(x,y)\longrightarrow(u,v).$$
>
> 因为
>
> $$\frac{\partial x}{\partial u}=x,\quad\frac{\partial y}{\partial u}=y,\quad\frac{\partial x}{\partial v}=x,\quad\frac{\partial y}{\partial v}=-y,$$
>
> 所以
>
> $$\frac{\partial z}{\partial u}=x\frac{\partial z}{\partial x}+y\frac{\partial z}{\partial y},$$
>
> $$\frac{\partial z}{\partial v}=x\frac{\partial z}{\partial x}-y\frac{\partial z}{\partial y}.$$
>
> 于是
>
> $$\frac{\partial^{2}z}{\partial u^{2}}=x\frac{\partial z}{\partial x}+y\frac{\partial z}{\partial y}+x^{2}\frac{\partial^{2}z}{\partial x^{2}}+2xy\frac{\partial^{2}z}{\partial x\partial y}+y^{2}\frac{\partial^{2}z}{\partial y^{2}},$$
>
> $$\frac{\partial^{2}z}{\partial v^{2}}=x\frac{\partial z}{\partial x}+y\frac{\partial z}{\partial y}+x^{2}\frac{\partial^{2}z}{\partial x^{2}}-2xy\frac{\partial^{2}z}{\partial x\partial y}+y^{2}\frac{\partial^{2}z}{\partial y^{2}}.$$
>
> 两式相加：
>
> $$\frac{\partial^{2}z}{\partial u^{2}}+\frac{\partial^{2}z}{\partial v^{2}}=2\left[x^{2}\frac{\partial^{2}z}{\partial x^{2}}+y^{2}\frac{\partial^{2}z}{\partial y^{2}}+x\frac{\partial z}{\partial x}+y\frac{\partial z}{\partial y}\right]=0.$$
>
> 指数代换 $x = e^{u+v}, y = e^{u-v}$ 的要点是 $\frac{\partial}{\partial u}, \frac{\partial}{\partial v}$ 对 $x \frac{\partial}{\partial x}, y \frac{\partial}{\partial y}$ 有“加减”对称结构.

**6.** (难度：★★★) 设 $z = z(x, y)$ 具有二阶连续偏导数, 满足方程

$$3\frac{\partial^{2}z}{\partial x^{2}}-2\frac{\partial^{2}z}{\partial x\partial y}-\frac{\partial^{2}z}{\partial y^{2}}=0,$$

已知变换 $\left\{\begin{aligned}u&=x+ay,\\ v&=x-3y\end{aligned}\right.$ 可将该方程化为 $\frac{\partial^{2}z}{\partial u\partial v}=0$，求常数 a.

> [!answer]- 原书参考答案（A.6.2 第 6 题，未逐题独立验算）
> **6.** 写出 $\frac{\partial z}{\partial x}$, $\frac{\partial z}{\partial y}$, $\frac{\partial^{2}z}{\partial x^{2}}$, $\frac{\partial^{2}z}{\partial y^{2}}$, $\frac{\partial^{2}z}{\partial x\partial y}$ 关于 $\frac{\partial z}{\partial u}$, $\frac{\partial z}{\partial v}$ 的表达式，代入原方程，令 $\frac{\partial^{2}z}{\partial u^{2}}$ 的系数为零.
>
> 链条： $z \longrightarrow (u, v) \longrightarrow (x, y)$.
>
> 由
>
> $$u=x+a y,\qquad v=x-3y,$$
>
> 得
>
> $$\frac{\partial z}{\partial x}=\frac{\partial z}{\partial u}+\frac{\partial z}{\partial v},\qquad\frac{\partial z}{\partial y}=a\frac{\partial z}{\partial u}-3\frac{\partial z}{\partial v}.$$
>
> 继续求二阶偏导：
>
> $$\frac{\partial^{2}z}{\partial x^{2}}=\frac{\partial^{2}z}{\partial u^{2}}+2\frac{\partial^{2}z}{\partial u\partial v}+\frac{\partial^{2}z}{\partial v^{2}},$$
>
> $$\frac{\partial^{2}z}{\partial y^{2}}=a^{2}\frac{\partial^{2}z}{\partial u^{2}}-6a\frac{\partial^{2}z}{\partial u\partial v}+9\frac{\partial^{2}z}{\partial v^{2}},$$
>
> $$\frac{\partial^{2}z}{\partial x\partial y}=a\frac{\partial^{2}z}{\partial u^{2}}+(a-3)\frac{\partial^{2}z}{\partial u\partial v}-3\frac{\partial^{2}z}{\partial v^{2}}.$$
>
> 代入原方程：
>
> $$3\frac{\partial^{2}z}{\partial x^{2}}-2\frac{\partial^{2}z}{\partial x\partial y}-\frac{\partial^{2}z}{\partial y^{2}}=(3-2a-a^{2})\frac{\partial^{2}z}{\partial u^{2}}+(12+4a)\frac{\partial^{2}z}{\partial u\partial v}.$$
>
> 要使方程化为 $\frac{\partial^{2}z}{\partial u\partial v}=0$，必须让 $\frac{\partial^{2}z}{\partial u^{2}}$ 的系数为 0:
>
> $$3-2a-a^{2}=0\quad\Longrightarrow\quad a=1 或 a=-3.$$
>
> 但 a = -3 会使 u = x - 3y 与 v = x - 3y 相同，变换退化，所以舍去。故 a = 1。变换退化的判断：两个新变量必须独立，不能成比例。

**7.** (难度：★★★★) 设 $f(x, y)$ 存在二阶偏导数. 证明: $f(x, y) = g(x) h(y)$ 的充分必要条件是:

$$f\frac{\partial^{2}f}{\partial x\partial y}=\frac{\partial f}{\partial x}\cdot\frac{\partial f}{\partial y}.$$

> [!answer]- 原书参考答案（A.6.2 第 7 题，未逐题独立验算）
> **7.** 必要性 ( $\Rightarrow$). 若 $f(x,y)=g(x)h(y)$, 则
>
> $$f_{x}=g^{\prime}h,\quad f_{y}=gh^{\prime},\quad f_{xy}=g^{\prime}h^{\prime}\implies ff_{xy}=gg^{\prime}hh^{\prime}=f_{x} f_{y}.$$
>
> 充分性 ( $\Leftrightarrow$). 设 $ff_{xy} = f_{x}f_{y}$.
>
> 若 $f \equiv 0$，取 $g \equiv 0, h \equiv 1$ 即可；下面设 f 不恒为零，并先在 $f \neq 0$ 的区域上讨论（记该区域为 $D_{0}$）。
>
> 在 $D_{0}$上，把条件两边同除 $f^{2}$:
>
> $$\frac{\partial}{\partial x}\left(\frac{f_{y}}{f}\right)=\frac{f_{x y}f-f_{y}f_{x}}{f^{2}}=0,$$
>
> 故 $\frac{f_{y}}{f}$ 与 x 无关，记为 $\varphi(y)$. 又 $\frac{f_{y}}{f} = \frac{\partial}{\partial y} \ln |f|$，于是
>
> $$\frac{\partial}{\partial y}\ln|f(x,y)|=\varphi(y)\implies\ln|f(x,y)|=\Phi(y)+G(x),\qquad\Phi^{\prime}=\varphi,$$
>
> 即 $\left|f(x,y)\right| = \mathrm{e}^{G(x)} \mathrm{e}^{\Phi(y)}$，从而在 $D_0$ 上
>
> $$f(x,y)=g(x)h(y),\qquad g=\pm\mathrm{e}^{G},~h=\mathrm{e}^{\Phi}.$$
>
> 最后由 f 连续（且 $D_{0}$ 在定义域中稠密），该分解式可连续延拓到整个定义域.

## 6.3 隐函数偏导数

隐函数求偏导的公式相对便于记忆，较好操作，但难点是要意识到题目的考察是隐函数求偏导，这就需要一定程度的训练，学会用隐函数进行偏导的求解。

**1.** (难度:★★) 设 $x\cos y + y\cos z + z\cos x = 1$，求 $\frac{\partial z}{\partial x}, \frac{\partial z}{\partial y}$.

> [!answer]- 原书参考答案（A.6.3 第 1 题，未逐题独立验算）
> **1.** 这里 $F = F(x, y, z)$，且 $z = z(x, y)$。令
>
> $$F(x,y,z)=x\cos y+y\cos z+z\cos x-1.$$
>
> 分别对 x, y, z 求偏导:
>
> $$\frac{\partial F}{\partial x}=\cos y-z\sin x,$$
>
> $$\frac{\partial F}{\partial y}=-x\sin y+\cos z,$$
>
> $$\frac{\partial F}{\partial z}=-y\sin z+\cos x.$$
>
> 由隐函数求导公式，
>
> $$\frac{\partial z}{\partial x}=-\frac{\frac{\partial F}{\partial x}}{\frac{\partial F}{\partial z}}=-\frac{\cos y-z\sin x}{\cos x-y\sin z}=\frac{z\sin x-\cos y}{\cos x-y\sin z},$$
>
> $$\frac{\partial z}{\partial y}=-\frac{\frac{\partial F}{\partial y}}{\frac{\partial F}{\partial z}}=-\frac{-x\sin y+\cos z}{\cos x-y\sin z}=\frac{x\sin y-\cos z}{\cos x-y\sin z}.$$

**2.** (难度:★★★★) 设函数 $z = f(x, y)$ 具有二阶连续偏导数，且 $\frac{\partial f}{\partial y} \neq 0$. 证明: 对任意常数 C, $f(x, y) = C$ 为直线的充分必要条件是

$$(f_{y})^{2}f_{x x}-2f_{x}f_{y}f_{x y}+f_{y y}(f_{x})^{2}=0.$$

> [!answer]- 原书参考答案（A.6.3 第 2 题，未逐题独立验算）
> **2.** 把 $f(x,y) = C$ 看成隐函数 $y = y(x)$，两次求导得到 $y''$. 曲线为直线当且仅当 $y'' = 0$. 这里 $f = f(x,y)$，而 $y = y(x)$. 由 $\frac{\partial f}{\partial y} \neq 0$，隐函数存在，设 $y = y(x)$. 对 $f(x,y) = C$ 求导:
>
> $$\frac{\partial f}{\partial x}+\frac{\partial f}{\partial y}y^{\prime}=0,$$
>
> 所以
>
> $$y^{\prime}=-\frac{\frac{\partial f}{\partial x}}{\frac{\partial f}{\partial y}}.$$
>
> 再求导. 注意 $\frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}$ 仍通过 x, y 依赖 x:
>
> $$y^{\prime\prime}=-\frac{(\frac{\partial^{2}f}{\partial x^{2}}+\frac{\partial^{2}f}{\partial x\partial y}y^{\prime})\frac{\partial f}{\partial y}-\frac{\partial f}{\partial x}(\frac{\partial^{2}f}{\partial x\partial y}+\frac{\partial^{2}f}{\partial y^{2}}y^{\prime})}{\left(\frac{\partial f}{\partial y}\right)^{2}}.$$
>
> 把 $y' = -\frac{\frac{\partial f}{\partial x}}{\frac{\partial f}{\partial y}}$ 代入并通分：
>
> $$y^{\prime\prime}=-\frac{\frac{\partial^{2}f}{\partial x^{2}}\left(\frac{\partial f}{\partial y}\right)^{2}-2\frac{\partial^{2}f}{\partial x\partial y}\frac{\partial f}{\partial x}\frac{\partial f}{\partial y}+\frac{\partial^{2}f}{\partial y^{2}}\left(\frac{\partial f}{\partial x}\right)^{2}}{\left(\frac{\partial f}{\partial y}\right)^{3}}.$$
>
> 因为 $\frac{\partial f}{\partial y} \neq 0$，所以
>
> $$y^{\prime\prime}=0\Longleftrightarrow\frac{\partial^{2}f}{\partial x^{2}}\left(\frac{\partial f}{\partial y}\right)^{2}-2\frac{\partial^{2}f}{\partial x\partial y}\frac{\partial f}{\partial x}\frac{\partial f}{\partial y}+\frac{\partial^{2}f}{\partial y^{2}}\left(\frac{\partial f}{\partial x}\right)^{2}=0.$$
>
> 此条件与常数 C 无关. 于是: 若对任意 C, 曲线 $f(x, y) = C$ 都是直线, 则上述等式处处成立; 反过来, 若上述等式处处成立, 则每条水平曲线的 $y'' = 0$, 故为直线. 水平集为直线的条件等价于隐函数二阶导数为零; 不要只求一阶导就下结论.

**3.** (难度：★★★★) 设 $y = f(x, t)$，而 t 是由方程 $F(x, y, t) = 0$ 所确定的 x, y 的函数，其中 f, F 都具有一阶连续偏导数. 试证明:

$$\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{\frac{\partial f}{\partial x}\frac{\partial F}{\partial t}-\frac{\partial f}{\partial t}\frac{\partial F}{\partial x}}{\frac{\partial f}{\partial t}\frac{\partial F}{\partial y}+\frac{\partial F}{\partial t}}.$$

> [!answer]- 原书参考答案（A.6.3 第 3 题，未逐题独立验算）
> **3.** 把 t 看成由 $F(x,y,t)=0$ 确定的隐函数 $t=t(x,y)$，再把 $y=f(x,t(x,y))$ 写成 $G(x,y)=0$，用隐函数公式求 $\mathrm{d}y/\mathrm{d}x$.
>
> $$链条：\ y\longrightarrow(x,t),\qquad t\longrightarrow(x,y).$$
>
> 由 $F(x,y,t)=0$ 确定 $t=t(x,y)$，其偏导为
>
> $$\frac{\partial t}{\partial x}=-\frac{\frac{\partial F}{\partial x}}{\frac{\partial F}{\partial t}},\qquad\frac{\partial t}{\partial y}=-\frac{\frac{\partial F}{\partial y}}{\frac{\partial F}{\partial t}}.$$
>
> 令
>
> $$G(x,y)=f(x,t(x,y))-y=0.$$
>
> 由隐函数求导，
>
> $$\frac{\mathrm{d}y}{\mathrm{d}x}=-\frac{\frac{\partial G}{\partial x}}{\frac{\partial G}{\partial y}}.$$
>
> 先求
>
> $$\frac{\partial G}{\partial x}=\frac{\partial f}{\partial x}+\frac{\partial f}{\partial t}\frac{\partial t}{\partial x}=\frac{\partial f}{\partial x}-\frac{\frac{\partial f}{\partial t}\frac{\partial F}{\partial x}}{\frac{\partial F}{\partial t}}=\frac{\frac{\partial f}{\partial x}\frac{\partial F}{\partial t}-\frac{\partial f}{\partial t}\frac{\partial F}{\partial x}}{\frac{\partial F}{\partial t}}.$$
>
> 再求
>
> $$\frac{\partial G}{\partial y}=\frac{\partial f}{\partial t}\frac{\partial t}{\partial y}-1=-\frac{\frac{\partial f}{\partial t}\frac{\partial F}{\partial y}}{\frac{\partial F}{\partial t}}-1=-\frac{\frac{\partial f}{\partial t}\frac{\partial F}{\partial y}+\frac{\partial F}{\partial t}}{\frac{\partial F}{\partial t}}.$$
>
> 所以
>
> $$\frac{\mathrm{d}y}{\mathrm{d}x}=-\frac{\frac{\partial G}{\partial x}}{\frac{\partial G}{\partial y}}=\frac{\frac{\partial f}{\partial x}\frac{\partial F}{\partial t}-\frac{\partial f}{\partial t}\frac{\partial F}{\partial x}}{\frac{\partial f}{\partial t}\frac{\partial F}{\partial y}+\frac{\partial F}{\partial t}}.$$
>
> 本题把 t 当作 x,y 的函数是消元的核心; 若把 t 也看作独立变量, 容易漏掉 $\frac{\partial t}{\partial x}$, $\frac{\partial t}{\partial y}$.

**4.** (难度:★★) 设 $u = u(x, y)$ 是由方程 $u + e^{u} = xy$ 所确定的二元函数, 求 $\frac{\partial^{2}u}{\partial x\partial y}$.

> [!answer]- 原书参考答案（A.6.3 第 4 题，未逐题独立验算）
> **4.** 这里 $F = F(x, y, u)$，而 $u = u(x, y)$。令 $F(x, y, u) = u + e^{u} - xy$，则
>
> $$\frac{\partial F}{\partial x}=-y,\qquad\frac{\partial F}{\partial y}=-x,\qquad\frac{\partial F}{\partial u}=1+e^{u}.$$
>
> 所以
>
> $$\frac{\partial u}{\partial x}=-\frac{-y}{1+e^{u}}=\frac{y}{1+e^{u}},$$
>
> $$\frac{\partial u}{\partial y}=-\frac{-x}{1+e^{u}}=\frac{x}{1+e^{u}}.$$
>
> 再对 y 求一次偏导，注意 u 本身也依赖 y:
>
> $$\frac{\partial^{2}u}{\partial x\partial y}=\frac{\partial}{\partial y}\left(\frac{y}{1+e^{u}}\right)=\frac{(1+e^{u})-y\cdot e^{u}\frac{\partial u}{\partial y}}{(1+e^{u})^{2}}.$$
>
> 把 $\frac{\partial u}{\partial y}=\frac{x}{1+e^{u}}$代入：
>
> $$\frac{\partial^{2}u}{\partial x\partial y}=\frac{1+e^{u}-\frac{xye^{u}}{1+e^{u}}}{(1+e^{u})^{2}}=\frac{1}{1+e^{u}}-\frac{xye^{u}}{(1+e^{u})^{3}}.$$
>
> 若想用原方程化简，可由 $1 + e^{u} = \frac{xy}{u}$ 继续整理.

## 6.4 多元极值/最值

中档题的争流砥柱，拥有全高数上下册最顶级的计算量，所以重点是多算多练。

**1.** (难度: ★★★★) 设二元函数 $f(x, y)$ 在平面上有连续的二阶偏导数. 对任何角 $\alpha$, 定义一元函数 $g_{\alpha}(t) = f(t \cos \alpha, t \sin \alpha)$. 若对任何 $\alpha$, 都有 $\left.\frac{\mathrm{d}g_{\alpha}(t)}{\mathrm{d}t}\right|_{t=0} = 0$ 且 $\left.\frac{\mathrm{d}^{2}g_{\alpha}(t)}{\mathrm{d}t^{2}}\right|_{t=0} > 0$. 证明: $f(0, 0)$ 是 $f(x, y)$ 的极小值.

> [!answer]- 原书参考答案（A.6.4 第 1 题，未逐题独立验算）
> **1.** 把每个方向上的二阶导 $g_{\theta}^{\prime\prime}(0)$ 写成 $A\cos^2\theta + 2B\cos\theta\sin\theta + C\sin^2\theta$，其中 $A, B, C$ 是原点处的三个二阶偏导。用辅助角公式求这个式子的最小值，由它恒大于 0 推出 $AC - B^2 > 0$，再配合 $A > 0$，最后用 $AC - B^2$ 判别法下结论。这里 $g_{\theta}(t) = f(t\cos\theta, t\sin\theta)$。记
>
> $$A=\frac{\partial^{2}f}{\partial x^{2}}(0,0),\qquad B=\frac{\partial^{2}f}{\partial x\partial y}(0,0),\qquad C=\frac{\partial^{2}f}{\partial y^{2}}(0,0).$$
>
> 对 $g_{\theta}(t)=f(t\cos\theta,t\sin\theta)$ 用链式法则：
>
> $$g_{\theta}^{\prime}(t)=\frac{\partial f}{\partial x}(t\cos\theta,t\sin\theta)\cos\theta+\frac{\partial f}{\partial y}(t\cos\theta,t\sin\theta)\sin\theta.$$
>
> 由 $g_{\theta}^{\prime}(0)=0$对任意 $\theta$成立，分别取 $\theta=0,\frac{\pi}{2}$得
>
> $$\frac{\partial f}{\partial x}(0,0)=0,\qquad\frac{\partial f}{\partial y}(0,0)=0.$$
>
> 再对 t 求导并令 t = 0:
>
> $$g_{\theta}^{\prime\prime}(0)=A\cos^{2}\theta+2B\cos\theta\sin\theta+C\sin^{2}\theta>0.$$
>
> 用二倍角公式把(1)化为
>
> $$g_{\theta}^{\prime\prime}(0)=\frac{A+C}{2}+\frac{A-C}{2}\cos2\theta+B\sin2\theta.$$
>
> 对后两项用辅助角公式：
>
> $$\frac{A-C}{2}\cos2\theta+B\sin2\theta=R\sin(2\theta+\varphi),\qquad R=\sqrt{\left(\frac{A-C}{2}\right)^{2}+B^{2}}.$$
>
> 因为(1)对一切 $\theta$成立,所以它的最小值也大于0:
>
> $$\frac{A+C}{2}-R>0.$$
>
> 两边平方：
>
> $$\frac{(A+C)^{2}}{4}>\frac{(A-C)^{2}}{4}+B^{2}\quad\Longrightarrow\quad AC-B^{2}>0.$$
>
> 又在(1)中取 $\theta=0$，得 $A=g_{0}^{\prime\prime}(0)>0$。于是 $AC-B^{2}>0$且A>0，按 $AC-B^{2}$判别法， $f(0,0)$是极小值。“每个方向的二阶导都为正”通过辅助角公式翻译成 $AC-B^{2}>0$且A>0，这正是 $AC-B^{2}$判别法需要的条件。

**2.** (难度:★★★) 证明: 函数 $z = (1 + e^{y}) \cos x - ye^{y}$ 有无穷多个极大值而无一极小值.

> [!answer]- 原书参考答案（A.6.4 第 2 题，未逐题独立验算）
> **2.** 先解全部驻点，再用 $A = \frac{\partial^{2}f}{\partial x^{2}}$、 $B = \frac{\partial^{2}f}{\partial x\partial y}$、 $C = \frac{\partial^{2}f}{\partial y^{2}}$ 和判别式 $AC-B^2$ 分类. 解
>
> $$\frac{\partial f}{\partial x}=\cos x=0,\qquad\frac{\partial f}{\partial y}=-2y=0,$$
>
> 得
>
> $$x=\frac{\pi}{2}+k\pi,\qquad y=0,\quad k\in\mathbb{Z}.$$
>
> 二阶偏导为
>
> $$A=\frac{\partial^{2}f}{\partial x^{2}}=-\sin x,\qquad B=\frac{\partial^{2}f}{\partial x\partial y}=0,\qquad C=\frac{\partial^{2}f}{\partial y^{2}}=-2.$$
>
> 判别式为
>
> $$AC-B^{2}=(-\sin x)(-2)-0^{2}=2\sin x.$$
>
> 当 $x = \frac{\pi}{2} + 2k\pi$ 时, $\sin x = 1$, 所以 $AC - B^{2} = 2 > 0$, 且 A = -1 < 0, 这些点是极大值点:
>
> $$f\left(\frac{\pi}{2}+2k\pi,0\right)=1.$$
>
> 这样的 k 有无穷多个，所以函数有无穷多个极大值.
>
> 当 $x = \frac{3\pi}{2} + 2k\pi$ 时, $\sin x = -1$, 所以 $AC - B^{2} = -2 < 0$, 这些点是鞍点, 不是极值.
>
> 由于驻点只有这两类, 而第二类全是鞍点, 所以函数没有极小值. 判定极值后要把 k 分奇偶: 两类驻点的 $AC-B^2$ 符号相反.

**3.** (难度:★★) 求函数 $f(x,y) = 3x^{2} + 3y^{2} - 2x^{3}$ 在区域 D: $x^{2} + y^{2} \leq 2$ 上的最大值与最小值.

> [!answer]- 原书参考答案（A.6.4 第 3 题，未逐题独立验算）
> **3.** 配方把函数写成到定点距离的平方，再比较该定点到圆盘中心和边界的位置。配方：
>
> $$f(x,y)=x^{2}+y^{2}-2x-4y=(x-1)^{2}+(y-2)^{2}-5.$$
>
> 点(1,2)到原点距离为 $\sqrt{5}<3$，所以(1,2)在区域内部，内部最小值为
>
> $$f(1,2)=-5.$$
>
> 区域边界为 $x^{2}+y^{2}=9$. 设 $x=3\cos t, y=3\sin t$, 则
>
> $$f(3\cos t,3\sin t)=9-6\cos t-12\sin t=9-6\sqrt{5}\sin(t+\varphi),$$
>
> 其中 $\varphi$ 为某个辅助角。所以边界上最大值为 $9 + 6\sqrt{5}$，最小值为 $9 - 6\sqrt{5}$。比较内部点与边界点：最小值为内部点 -5；最大值为边界点 $9 + 6\sqrt{5}$。故
>
> $$\max_{D}f(x,y)=9+6\sqrt{5},\qquad\min_{D}f(x,y)=-5.$$
>
> 圆盘上的二次函数配方后，“到定点距离”就是全部信息：定点在圆内则最小值取在内部，最大值取在离定点最远的边界点.

**4.** (难度: ★★★★) 求函数 $f(x, y, z) = \ln x + 2 \ln y + 4 \ln z$ 在球面 $x^{2} + y^{2} + z^{2} = 7R^{2}$ 上的最大值 (x > 0, y > 0, z > 0), 其中 R > 0 为常数，并由此证明: 当 a > 0, b > 0, c > 0 时，恒有

$$a b^{2}c^{4}\leqslant1024\left(\frac{a+b+c}{7}\right)^{7}.$$

> [!answer]- 原书参考答案（A.6.4 第 4 题，未逐题独立验算）
> **4.** **第一步：用拉格朗日乘数法求条件最值。** 求 $f = \ln x + 2\ln y + 4\ln z$ 在 $x^{2} + y^{2} + z^{2} = 7R^{2}(x, y, z > 0)$ 上的最大值。令
>
> $$L=\ln x+2\ln y+4\ln z-\lambda\left(x^{2}+y^{2}+z^{2}-7R^{2}\right),$$
>
> 由 $L_{x}=L_{y}=L_{z}=0$ 得
>
> $$\frac{1}{x}=2\lambda x,\qquad\frac{2}{y}=2\lambda y,\qquad\frac{4}{z}=2\lambda z\implies x^{2}=\frac{1}{2\lambda},\quad y^{2}=\frac{1}{\lambda},\quad z^{2}=\frac{2}{\lambda}.$$
>
> 代入约束 $\frac{1}{2\lambda} + \frac{1}{\lambda} + \frac{2}{\lambda} = 7R^{2}$ 得 $\lambda = \frac{1}{2R^{2}}$，于是
>
> $$x=R,\qquad y=\sqrt{2}R,\qquad z=2R.$$
>
> （边界上 $x,y,z\to0^{+}$ 时 $f\to-\infty$ ，故最大值必在此内部驻点取得。）
>
> **第二步: 写出最大值.** 由 $f_{\max} = f(R, \sqrt{2}R, 2R) = \ln R + 2\ln\left(\sqrt{2}R\right) + 4\ln(2R) = 7\ln R + 5\ln2 = \ln\left(32R^{7}\right)$,
>
> $$\ln x+2\ln y+4\ln z\leqslant\ln\left(32R^{7}\right)\implies xy^{2}z^{4}\leqslant32R^{7}=32\left(\frac{x^{2}+y^{2}+z^{2}}{7}\right)^{7/2}.$$
>
> **第三步：代入 $x = \sqrt{a}$, $y = \sqrt{b}$, $z = \sqrt{c}$ 即得要证的不等式.** 此时 $xy^{2}z^{4} = a^{1/2}bc^{2}$，上式两边取 $\frac{2}{7}$ 次幂：
>
> $$\left(a b^{2}c^{4}\right)^{1/7}=\left(a^{1/2}b c^{2}\right)^{2/7}\leqslant32^{2/7}\cdot\frac{a+b+c}{7}.$$
>
> 由 $32^{2/7}=2^{10/7}$，两边取7次幂得
>
> $$a b^{2}c^{4}\leqslant2^{10}\left(\frac{a+b+c}{7}\right)^{7}=1024\left(\frac{a+b+c}{7}\right)^{7}.$$

**5.** (难度:★★★★) 设 $\Sigma_{1}:\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}+\frac{z^{2}}{c^{2}}=1$，其中 a>b>c>0, $\Sigma_{2}:z^{2}=x^{2}+y^{2}$， $\Gamma$ 为 $\Sigma_{1}$ 和 $\Sigma_{2}$ 的交线. 求椭球面 $\Sigma_{1}$ 在 $\Gamma$ 上各点的切平面到原点距离的最大值和最小值.

> [!answer]- 原书参考答案（A.6.4 第 5 题，未逐题独立验算）
> **5.** 设点 $P = (x, y, z) \in \Gamma$. 椭球面 $\Sigma_1$ 在 P 处的切平面为
>
> $$\frac{x X}{a^{2}}+\frac{y Y}{b^{2}}+\frac{z Z}{c^{2}}=1,$$
>
> 它到原点的距离为
>
> $$d=\frac{1}{\sqrt{D^{2}}},\qquad D^{2}=\frac{x^{2}}{a^{4}}+\frac{y^{2}}{b^{4}}+\frac{z^{2}}{c^{4}}.$$
>
> **第一步：把两个约束化成 $u=x^2,\ v=y^2$ 上的一个线性约束.** 由 $\Gamma$ 满足 $z^{2} = x^{2} + y^{2}$ 与 $\frac{x^{2}}{a^{2}} + \frac{y^{2}}{b^{2}} + \frac{z^{2}}{c^{2}} = 1$，消去 z 得
>
> $$\alpha u+\beta v=1,\qquad\alpha=\frac{1}{a^{2}}+\frac{1}{c^{2}},\quad\beta=\frac{1}{b^{2}}+\frac{1}{c^{2}},\quad u,v\geqslant0.$$
>
> 而
>
> $$D^{2}=\frac{u}{a^{4}}+\frac{v}{b^{4}}+\frac{u+v}{c^{4}}=\gamma u+\delta v,\qquad\gamma=\frac{1}{a^{4}}+\frac{1}{c^{4}},\quad\delta=\frac{1}{b^{4}}+\frac{1}{c^{4}}.$$
>
> **第二步：线性目标在一条线段上取最值，最值必在端点取得.** 在 $\alpha u + \beta v = 1 (u, v \geqslant 0)$ 上，
>
> $$D^{2}=\gamma u+\delta v\in\left\{\frac{\gamma}{\alpha}\left( 即 v=0\right),\frac{\delta}{\beta}\left( 即 u=0\right)\right\} 所张成的区间 ,$$
>
> 其中
>
> $$\frac{\gamma}{\alpha}=\frac{a^{4}+c^{4}}{a^{2}c^{2}\left(a^{2}+c^{2}\right)},\qquad\frac{\delta}{\beta}=\frac{b^{4}+c^{4}}{b^{2}c^{2}\left(b^{2}+c^{2}\right)}.$$
>
> **第三步：写出结论.** 由 $d = 1/\sqrt{D^{2}}$
>
> $$d_{\mathrm{max}}=\frac{1}{\sqrt{\min\left\{\frac{a^{4}+c^{4}}{a^{2}c^{2}(a^{2}+c^{2})},\frac{b^{4}+c^{4}}{b^{2}c^{2}(b^{2}+c^{2})}\right\}}},\qquad d_{\mathrm{min}}=\frac{1}{\sqrt{\max\left\{\frac{a^{4}+c^{4}}{a^{2}c^{2}(a^{2}+c^{2})},\frac{b^{4}+c^{4}}{b^{2}c^{2}(b^{2}+c^{2})}\right\}}}$$
>
> （两个端点分别对应 y = 0 与 x = 0 的两类交点，都在 $\Gamma$ 上，故这两个值都确实能取到。）

## 6.5 多元微分应用

一些与多元微分相关的应用题, 难度不大, 主要是掌握切平面、法平面和法向量的计算方式.

**1.** (难度:★★) 证明: 曲面 $x^{\frac{2}{3}} + y^{\frac{2}{3}} + z^{\frac{2}{3}} = \pi^{\frac{2}{3}}$ 上任意点处的切平面在坐标轴上的截距的平方和为常数.

> [!answer]- 原书参考答案（A.6.5 第 1 题，未逐题独立验算）
> **1.** 先求曲面在任意点的法向量, 再写出切平面的截距式, 最后把截距平方代入原曲面方程. 这里 $F = F(x, y, z)$. 设曲面
>
> $$F(x,y,z)=x^{\frac{2}{3}}+y^{\frac{2}{3}}+z^{\frac{2}{3}}-\pi^{\frac{2}{3}}=0.$$
>
> 任取曲面上一点 $P = (a, b, c)$，则
>
> $$a^{\frac{2}{3}}+b^{\frac{2}{3}}+c^{\frac{2}{3}}=\pi^{\frac{2}{3}}.\tag{1}$$
>
> 法向量为
>
> $$\left(\frac{2}{3}a^{-\frac{1}{3}},\frac{2}{3}b^{-\frac{1}{3}},\frac{2}{3}c^{-\frac{1}{3}}\right),$$
>
> 所以切平面方程可写成
>
> $$a^{-\frac{1}{3}}(x-a)+b^{-\frac{1}{3}}(y-b)+c^{-\frac{1}{3}}(z-c)=0.$$
>
> 利用（1）化简为
>
> $$a^{-\frac{1}{3}}x+b^{-\frac{1}{3}}y+c^{-\frac{1}{3}}z=\pi^{\frac{2}{3}}.$$
>
> 化成截距式：
>
> $$\frac{x}{\pi^{\frac{2}{3}}a^{\frac{1}{3}}}+\frac{y}{\pi^{\frac{2}{3}}b^{\frac{1}{3}}}+\frac{z}{\pi^{\frac{2}{3}}c^{\frac{1}{3}}}=1.$$
>
> 所以三截距的平方和为
>
> $$\left(\pi^{\frac{2}{3}}a^{\frac{1}{3}}\right)^{2}+\left(\pi^{\frac{2}{3}}b^{\frac{1}{3}}\right)^{2}+\left(\pi^{\frac{2}{3}}c^{\frac{1}{3}}\right)^{2}=\pi^{\frac{4}{3}}\left(a^{\frac{2}{3}}+b^{\frac{2}{3}}+c^{\frac{2}{3}}\right).$$
>
> 由(1)得该值为 $\pi^{\frac{4}{3}}\cdot\pi^{\frac{2}{3}}=\pi^{2}$，为常数。曲面呈 $x^{\alpha}+y^{\alpha}+z^{\alpha}$ 型时，法向量与截距的关系通常能把截距平方和还原成原曲面方程。

**2.** (难度:★★) 设 f 为可微函数. 试证: 曲面 $z = xf\left(\frac{y}{x}\right)$ 上任一点 $(x, y, z)$ ( $x \neq 0$) 处的切平面都过某一固定点.

> [!answer]- 原书参考答案（A.6.5 第 2 题，未逐题独立验算）
> **2.** 记 $u = \frac{y}{x}$，则
>
> $$z=xf(u).$$
>
> 求偏导：
>
> $$\frac{\partial z}{\partial x}=f(u)+x f^{\prime}(u)\cdot\left(-\frac{y}{x^{2}}\right)=f(u)-u f^{\prime}(u),$$
>
> $$\frac{\partial z}{\partial y}=xf^{\prime}(u)\cdot\frac{1}{x}=f^{\prime}(u).$$
>
> 任取曲面上一点 $P_{0}=(x_{0},y_{0},z_{0})$，令 $u_{0}=\frac{y_{0}}{x_{0}}$。该点法向量可取
>
> $$\vec{n}=\left(-\frac{\partial z}{\partial x},-\frac{\partial z}{\partial y},1\right)=\left(-f(u_{0})+u_{0}f^{\prime}(u_{0}),-f^{\prime}(u_{0}),1\right).$$
>
> 切平面方程为
>
> $$(-f(u_{0})+u_{0}f^{\prime}(u_{0}))(x-x_{0})-f^{\prime}(u_{0})(y-y_{0})+(z-z_{0})=0.$$
>
> 整理：
>
> $$z=\left(f(u_{0})-u_{0}f^{\prime}(u_{0})\right)x+f^{\prime}(u_{0})y+z_{0}-\left(f(u_{0})-u_{0}f^{\prime}(u_{0})\right)x_{0}+f^{\prime}(u_{0})y_{0}.$$
>
> 因为 $z_{0}=x_{0}f(u_{0})$，且 $y_{0}=x_{0}u_{0}$，所以常数项为
>
> $$x_{0}f(u_{0})-\left(f(u_{0})-u_{0}f^{\prime}(u_{0})\right)x_{0}+f^{\prime}(u_{0})x_{0}u_{0}=0.$$
>
> 因此切平面是过原点的平面，即
>
> $$z=\left(f(u_{0})-u_{0}f^{\prime}(u_{0})\right)x+f^{\prime}(u_{0})y.$$

**3.** (难度:★★★) 证明: 曲面 $z + \sqrt{x^{2} + y^{2} + z^{2}} = x^{3}f\left(\frac{y}{x}\right)$ 上任意点处的切平面在 Oz 轴上的截距与切点到坐标原点的距离之比为常数, 并求出此常数.

> [!answer]- 原书参考答案（A.6.5 第 3 题，未逐题独立验算）
> **3.** 把曲面写成 $F(x,y,z)=0$，写出 z 轴截距。关键是用曲面方程把 $a\frac{\partial F}{\partial x}+b\frac{\partial F}{\partial y}$ 中的复杂项消掉。这里 $F=F(x,y,z)$。任取曲面上一点 $P=(a,b,c)$，记
>
> $$r=\sqrt{a^{2}+b^{2}+c^{2}},\qquad F(x,y,z)=z+\sqrt{x^{2}+y^{2}+z^{2}}-x^{3}f\left(\frac{y}{x}\right).$$
>
> 令 $u = \frac{y}{a}$. 先算偏导:
>
> $$\frac{\partial F}{\partial x}=\frac{x}{r}-3x^{2}f\left(\frac{y}{x}\right)+x y f^{\prime}\left(\frac{y}{x}\right),$$
>
> $$\frac{\partial F}{\partial y}=\frac{y}{r}-x^{2}f^{\prime}\left(\frac{y}{x}\right),$$
>
> $$\frac{\partial F}{\partial z}=1+\frac{z}{r}.$$
>
> 在点P处，
>
> $$a\frac{\partial F}{\partial x}+b\frac{\partial F}{\partial y}=\frac{a^{2}+b^{2}}{r}-3a^{3}f(u).$$
>
> 由曲面方程 $c + r = a^{3}f(u)$，得
>
> $$a\frac{\partial F}{\partial x}+b\frac{\partial F}{\partial y}=\frac{a^{2}+b^{2}}{r}-3(c+r)=\frac{a^{2}+b^{2}-3r(c+r)}{r}.$$
>
> 切平面在 Oz 轴上的截距设为 Z. 把 x=0, y=0, z=Z 代入
>
> $$\frac{\partial F}{\partial x}(x-a)+\frac{\partial F}{\partial y}(y-b)+\frac{\partial F}{\partial z}(z-c)=0,$$
>
> 得
>
> $$-a\frac{\partial F}{\partial x}-b\frac{\partial F}{\partial y}+\frac{\partial F}{\partial z}(Z-c)=0.$$
>
> 所以
>
> $$\frac{\partial F}{\partial z}(Z-c)=a\frac{\partial F}{\partial x}+b\frac{\partial F}{\partial y}.$$
>
> 代入 $\frac{\partial F}{\partial z} = \frac{r + c}{r}$ 并整理:
>
> $$\frac{r+c}{r}(Z-c)=\frac{a^{2}+b^{2}-3r(c+r)}{r}.$$
>
> 两边乘 r，并利用
>
> $$a^{2}+b^{2}=r^{2}-c^{2}=(r-c)(r+c),$$
>
> 得
>
> $$(r+c)(Z-c)=(r+c)(r-c)-3r(r+c)=(r+c)(-2r-c).$$
>
> 约去 $r+c$，得
>
> $$\begin{array}{r} Z-c=-2r-c\quad\Longrightarrow\quad Z=-2r.\end{array}$$
>
> 所以 Oz 轴上的截距的绝对值为 2r，与切点到原点距离之比为 2。本题的消元关键是把 $a^{3}f(u)$ 整体换成 $c+r$，不要展开 $f'$；否则会出现无法消掉的导数项。

## 6.6 相关零碎知识点

### 6.6.1 曲率

**1.** (难度:★) 设曲线 L 的极坐标方程为 $r = \theta$，求曲线 L 在点 $(r, \theta) = (\pi, \pi)$ 处的曲率半径.

> [!answer]- 原书参考答案（A.6.6·曲率 第 1 题，未逐题独立验算）
> **1.** 极坐标曲线 $r = r(\theta)$ 的曲率公式为
>
> $$\kappa=\frac{\left|r^{2}+2r^{\prime2}-r r^{\prime\prime}\right|}{\left(r^{2}+r^{\prime2}\right)^{3/2}},\qquad 曲率半径 \rho=\frac{1}{\kappa}.$$
>
> 第一步：代入 $r = \theta$。由 r = $\theta$ 得 $r' = 1$， $r'' = 0$，故
>
> $$\kappa(\theta)=\frac{\theta^{2}+2}{\left(\theta^{2}+1\right)^{3/2}}.$$
>
> 第二步：在 $\theta=\pi$处求值并取倒数.
>
> $$\rho(\pi)=\frac{1}{\kappa(\pi)}=\frac{\left(\pi^{2}+1\right)^{3/2}}{\pi^{2}+2}.$$
>
> （顺带一提： $r = \theta$ 是阿基米德螺线， $\theta$ 越大曲率越小、曲率半径越大，与上式一致。）

### 6.6.2 方向导数

**1.** (难度: ★★) 已知二元函数

$$f(x,y)=\left\{\begin{aligned}&x+y+\frac{x^{3}y}{x^{4}+y^{2}},&(x,y)\neq(0,0),\\ &0,&(x,y)=(0,0).\end{aligned}\right.$$

求 $f(x,y)$ 在点 $(0,0)$ 处沿着方向 $(\cos\alpha,\cos\beta)$ 的方向导数.

> [!answer]- 原书参考答案（A.6.6·方向导数 第 1 题，未逐题独立验算）
> **1.** 直接用定义. 令方向向量 $\overrightarrow{e} = (\cos \alpha, \cos \beta)$，则
>
> $$f(t\cos\alpha,t\cos\beta)=t(\cos\alpha+\cos\beta)+\frac{t^{4}\cos^{3}\alpha\cos\beta}{t^{4}\cos^{4}\alpha+t^{2}\cos^{2}\beta}.$$
>
> 当 $\cos\beta\neq0$时，
>
> $$\frac{t^{4}\cos^{3}\alpha\cos\beta}{t^{4}\cos^{4}\alpha+t^{2}\cos^{2}\beta}=\frac{t^{2}\cos^{3}\alpha\cos\beta}{t^{2}\cos^{4}\alpha+\cos^{2}\beta},$$
>
> 所以
>
> $$\frac{f(t\cos\alpha,t\cos\beta)-0}{t}=\cos\alpha+\cos\beta+\frac{t\cos^{3}\alpha\cos\beta}{t^{2}\cos^{4}\alpha+\cos^{2}\beta}.$$
>
> 最后一项当 $t \to 0^{+}$ 时趋于 0; 若 $\cos \beta = 0$, 则该项恒为 0. 故
>
> $$\frac{\partial f}{\partial\overrightarrow{e}}(0,0)=\cos\alpha+\cos\beta.$$

**2.** (难度:★) 设直线 L 是直线 $\left\{\begin{aligned}&2x-z-3=0,\\&y-2z+4=0\end{aligned}\right.$ 在平面 $x+y-z=5$ 上的投影.

求函数 $f(x,y,z)=\cos^{2}xy+\frac{y}{z^{2}}$ 在点 $P(0,-1,1)$ 处沿直线 L 的方向导数.

> [!answer]- 原书参考答案（A.6.6·方向导数 第 2 题，未逐题独立验算）
> **2.** 先求原直线的方向向量，再把它投影到已知平面上；方向导数就是偏导向量 $\left(\frac{\partial f}{\partial x},\frac{\partial f}{\partial y},\frac{\partial f}{\partial z}\right)$与单位方向向量的内积. 这里 $f=f(x,y,z)$. 原直线是两个平面的交线：
>
> $$2x-z-3=0,\qquad y-2z+4=0.$$
>
> 两平面法向量为
>
> $$\vec{n}_{1}=(2,0,-1),\qquad\vec{n}_{2}=(0,1,-2),$$
>
> 所以直线方向为
>
> $$\overrightarrow{d}=\overrightarrow{n}_{1}\times\overrightarrow{n}_{2}=(1,4,2).$$
>
> 投影平面 $x + y - z = 5$ 的法向量为 $\vec{n} = (1, 1, -1)$. 把 $\vec{d}$ 投影到该平面:
>
> $$\vec{p}=\vec{d}-\frac{\vec{d}\cdot\vec{n}}{\vec{n}\cdot\vec{n}}\vec{n}.$$
>
> 计算
>
> $$\vec{d}\cdot\vec{n}=1+4-2=3,\quad\vec{n}\cdot\vec{n}=3,$$
>
> 所以
>
> $$\vec{p}=(1,4,2)-\frac{3}{3}(1,1,-1)=(0,3,3).$$
>
> 取单位方向
>
> $$\vec{e}=\left(0,\frac{1}{\sqrt{2}},\frac{1}{\sqrt{2}}\right).$$
>
> 函数 $f(x,y,z)=\cos^{2}(xy)+\frac{y}{z^{2}}$ 的偏导按分量计算：
>
> $$\frac{\partial f}{\partial x}=-2y\cos(x y)\sin(x y),$$
>
> $$\frac{\partial f}{\partial y}=-2x\cos(x y)\sin(x y)+\frac{1}{z^{2}},$$
>
> $$\frac{\partial f}{\partial z}=-\frac{2y}{z^{3}}.$$
>
> 在 $P(0,-1,1)$处，xy=0，所以
>
> $$\left(\frac{\partial f}{\partial x},\frac{\partial f}{\partial y},\frac{\partial f}{\partial z}\right)\bigg|_{P}=(0,1,2).$$
>
> 故方向导数为
>
> $$\frac{\partial f}{\partial\vec{e}}=\left(\frac{\partial f}{\partial x},\frac{\partial f}{\partial y},\frac{\partial f}{\partial z}\right)\bigg|_{P}\cdot\vec{e}=\frac{1+2}{\sqrt{2}}=\frac{3}{\sqrt{2}}.$$
>
> 直线在平面上的投影方向, 是直线方向减去它在平面法向量上的分量; 先求方向再算偏导, 步骤就不会乱.

**3.** (难度:★★) 设 $1_{j}, j = 1, 2, \ldots, n$ 是 xOy 平面上点 $P_{0}$ 处的 n > 2 个方向向量, 相邻两个向量之间的夹角为 $\frac{2\pi}{n}$, 又设函数 $f(x, y)$ 在点 $P_{0}$ 处有连续偏导数, 证明

$$\sum_{j=1}^{n}\frac{\partial f(P_{0})}{\partial\mathbf{1}_{j}}=0.$$

> [!answer]- 原书参考答案（A.6.6·方向导数 第 3 题，未逐题独立验算）
> **3.** 方向导数等于 $\frac{\partial f}{\partial x}\cos\theta_j + \frac{\partial f}{\partial y}\sin\theta_j$，所以求和后只需证明 $\sum\cos\theta_j = \sum\sin\theta_j = 0$。用积化和差把每项拆成相邻两项之差，即可整体抵消。这里 $f = f(x, y)$。设
>
> $$\vec{l}_{j}=(\cos\theta_{j},\sin\theta_{j}),\qquad\theta_{j}=\theta_{0}+\frac{2\pi j}{n},\quad j=1,2,\ldots,n.$$
>
> 因为 $f(x,y)$ 在 $P_{0}$ 有连续偏导数，所以 $f(x,y)$ 在 $P_{0}$ 可微，方向导数公式成立：
>
> $$\frac{\partial f(P_{0})}{\partial\overrightarrow{l_{j}}}=\frac{\partial f}{\partial x}(P_{0})\cos\theta_{j}+\frac{\partial f}{\partial y}(P_{0})\sin\theta_{j}.$$
>
> 所以只需证明
>
> $$\sum_{j=1}^{n}\cos\theta_{j}=0,\qquad\sum_{j=1}^{n}\sin\theta_{j}=0.$$
>
> 先用积化和差：
>
> $$\cos\theta_{j}=\frac{\sin\left(\theta_{j}+\frac{\pi}{n}\right)-\sin\left(\theta_{j}-\frac{\pi}{n}\right)}{2\sin\frac{\pi}{n}}.$$
>
> 注意
>
> $$\theta_{j}+\frac{\pi}{n}=\theta_{j+1}-\frac{\pi}{n},$$
>
> 所以
>
> $$\begin{aligned}\sum_{j=1}^{n}\cos\theta_{j}&=\frac{1}{2\sin\frac{\pi}{n}}\sum_{j=1}^{n}\left[\sin\left(\theta_{j+1}-\frac{\pi}{n}\right)-\sin\left(\theta_{j}-\frac{\pi}{n}\right)\right]\\&=0.\end{aligned}$$
>
> 同理，
>
> $$\sin\theta_{j}=\frac{\cos\left(\theta_{j}-\frac{\pi}{n}\right)-\cos\left(\theta_{j}+\frac{\pi}{n}\right)}{2\sin\frac{\pi}{n}},$$
>
> 求和时相邻项相互抵消，得
>
> $$\sum_{j=1}^{n}\sin\theta_{j}=0.$$
>
> 于是
>
> $$\sum_{j=1}^{n}\frac{\partial f(P_{0})}{\partial\overrightarrow{l_{j}}}=\frac{\partial f}{\partial x}(P_{0})\cdot0+\frac{\partial f}{\partial y}(P_{0})\cdot0=0.$$
>
> 用积化和差时，分母 $2\sin\frac{\pi}{n}$ 对 $n\geqslant2$ 恒不为零；相邻两项首尾相接是求和为0的本质.

### 6.6.3 梯度

**1.** (难度: ★★★) 设函数 $f(x, y)$ 处处可微, 已知向量 $\mathbf{l}_{1}$ 与 $\mathbf{l}_{2}$ 的夹角为 $\theta \in (0, \pi)$, 证明:

$$\|\mathrm{grad}f(x,y)\|^{2}\leq\frac{2}{\sin^{2}\theta}\left[\left(\frac{\partial f}{\partial l_{1}}\right)^{2}+\left(\frac{\partial f}{\partial l_{2}}\right)^{2}\right].$$

> [!answer]- 原书参考答案（A.6.6·梯度 第 1 题，未逐题独立验算）
> **1.** 把 $\frac{\partial f}{\partial x}$, $\frac{\partial f}{\partial y}$ 分别记为 p, q, 方向导数写成 p, q 与方向角的式子; 然后对两个方向导数的平方和用 $2\theta$ 的辅助角公式, 化成 “常数 + 正弦”, 从而取下界. 记
>
> $$\frac{\partial f}{\partial x}=p,\qquad\frac{\partial f}{\partial y}=q,$$
>
> 并令
>
> $$P=p^{2}+q^{2},\qquad Q=p^{2}-q^{2},\qquad T=2p q.$$
>
> 取坐标旋转，使两个单位方向分别为
>
> $$\vec{l}_{1}=(\cos\varphi,\sin\varphi),\qquad\vec{l}_{2}=(\cos(\varphi+\theta),\sin(\varphi+\theta)).$$
>
> 则
>
> $$d_{1}=\frac{\partial f}{\partial\overrightarrow{l}_{1}}=p\cos\varphi+q\sin\varphi,$$
>
> $$d_{2}=\frac{\partial f}{\partial\vec{l}_{2}}=p\cos(\varphi+\theta)+q\sin(\varphi+\theta).$$
>
> 用二倍角公式：
>
> $$d_{1}^{2}=\frac{P}{2}+\frac{Q}{2}\cos2\varphi+\frac{T}{2}\sin2\varphi,$$
>
> $$d_{2}^{2}=\frac{P}{2}+\frac{Q}{2}\cos(2\varphi+2\theta)+\frac{T}{2}\sin(2\varphi+2\theta).$$
>
> 相加，并用积化和差：
>
> $$\begin{aligned}d^{2}_{1}+d^{2}_{2}&=P+\frac{Q}{2}[\cos2\varphi+\cos(2\varphi+2\theta)]+\frac{T}{2}[\sin2\varphi+\sin(2\varphi+2\theta)]\\&=P+\cos\theta\left[Q\cos(2\varphi+\theta)+T\sin(2\varphi+\theta)\right].\end{aligned}$$
>
> 对括号里的式子用辅助角公式. 因为
>
> $$Q^{2}+T^{2}=(p^{2}-q^{2})^{2}+4p^{2}q^{2}=(p^{2}+q^{2})^{2}=P^{2},$$
>
> 所以
>
> $$Q\cos(2\varphi+\theta)+T\sin(2\varphi+\theta)=P\sin(2\varphi+\theta+\delta).$$
>
> 于是
>
> $$d_{1}^{2}+d_{2}^{2}=P\left[1+\cos\theta\sin(2\varphi+\theta+\delta)\right].$$
>
> 由于正弦项的最小值为 -1，得
>
> $$d_{1}^{2}+d_{2}^{2}\geqslant P(1-\left|\cos\theta\right|).$$
>
> 再由基本不等式 $2|\cos\theta| \leqslant 1 + \cos^2\theta$，有
>
> $$1-\left|\cos\theta\right|\geqslant1-\frac{1+\cos^{2}\theta}{2}=\frac{1-\cos^{2}\theta}{2}=\frac{\sin^{2}\theta}{2}.$$
>
> 因此
>
> $$d_{1}^{2}+d_{2}^{2}\geqslant\frac{P}{2}\sin^{2}\theta,$$
>
> 即
>
> $$P\leqslant\frac{2}{\sin^{2}\theta}(d_{1}^{2}+d_{2}^{2}).$$
>
> 把 $P=\left(\frac{\partial f}{\partial x}\right)^{2}+\left(\frac{\partial f}{\partial y}\right)^{2}$ 和 $d_{1}, d_{2}$ 的定义代回，就是
>
> $$\left(\frac{\partial f}{\partial x}\right)^{2}+\left(\frac{\partial f}{\partial y}\right)^{2}\leqslant\frac{2}{\sin^{2}\theta}\left[\left(\frac{\partial f}{\partial\overrightarrow{l_{1}}}\right)^{2}+\left(\frac{\partial f}{\partial\overrightarrow{l_{2}}}\right)^{2}\right].$$
>
> 这里辅助角公式是作用在 $2\varphi + \theta$ 上, 不是直接对原方向导数; 目的是把两个方向导数的平方和写成 $P[1 + \cos\theta \sin(\cdots)]$, 再取正弦的最小值.

### 6.6.4 旋度

**1.** (难度:★) 求向量场 $\overrightarrow{F}(x,y,z) = xy\mathbf{i} - yz\mathbf{j} + zx\mathbf{k}$ 的旋度 $\operatorname{rot}\overrightarrow{F}(1,1,0)$.

> [!answer]- 原书参考答案（A.6.6·旋度 第 1 题，未逐题独立验算）
> **1.** 由旋度公式,
>
> $$\mathrm{rot}\overrightarrow{F}=\left(\frac{\partial(zx)}{\partial y}-\frac{\partial(-yz)}{\partial z},\frac{\partial(xy)}{\partial z}-\frac{\partial(zx)}{\partial x},\frac{\partial(-yz)}{\partial x}-\frac{\partial(xy)}{\partial y}\right)=(y,-z,-x).$$
>
> 代入 $(1,1,0)$:
>
> $$\mathrm{rot}\overrightarrow{F}(1,1,0)=(1,0,-1).$$

### 6.6.5 散度

**1.** (难度:★) 求向量场 $\mathbf{u}(x, y, z) = xy^2\mathbf{i} + ye^z\mathbf{j} + x\ln(1 + z^2)\mathbf{k}$ 在点 $P(1, 1, 0)$ 处的散度 $\operatorname{div}\mathbf{u}$.

> [!answer]- 原书参考答案（A.6.6·散度 第 1 题，未逐题独立验算）
> **1.** 
>
> $$\mathrm{div}\vec{u}=\frac{\partial(xy^{2})}{\partial x}+\frac{\partial(ye^{z})}{\partial y}+\frac{\partial(x\ln(1+z^{2}))}{\partial z}=y^{2}+e^{z}+\frac{2xz}{1+z^{2}}.$$
>
> 代入 $P(1,1,0)$:
>
> $$\mathrm{div}\vec{u}(1,1,0)=1+1+0=2.$$

---

# 基础篇·第七章 多元积分学

## 7.1 重积分

### 7.1.1 二重积分

重积分里最简单的一类,学会二重积分的换序、雅可比换元与对称性的应用即可.

**1.** (难度:★★) 计算积分 $\int_{0}^{2\pi} dx \int_{x}^{2\pi} \frac{x \sin^{2} t}{t^{2}} dt$.

> [!answer]- 原书参考答案（A.7.1·二重积分 第 1 题，未逐题独立验算）
> **1.** 内层被积函数里的 $\frac{\sin^{2}t}{t^{2}}$ 的原函数不是初等函数，而且分子上还带着外层变量 x （不能当常数提出来），所以必须交换积分次序.
>
> 第一步：画出积分区域. 由积分限得
>
> $$D=\{(x,t)\mid0\leqslant x\leqslant2\pi,x\leqslant t\leqslant2\pi\},$$
>
> 即正方形 $[0,2\pi]\times[0,2\pi]$ 中直线 t=x 上方的那个三角形.
>
> <div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//4d3729b7-3451-4bfc-a16c-097e9c7144b5/markdown_1/imgs/img_in_image_box_510_468_738_687.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-11-05T13%3A08%3A15Z%2F-1%2F%2F7df57fe7b7bed66a4596689821f633f61e6510edcb83254bde71eaeba40d6319" alt="Image" width="19%" /></div>
>
> 第二步: 换序 (改看成"先 x 后 $t''$)。把同一个 D 用另一组不等式描述: 先让 t 在 $[0,2\pi]$ 上跑, 再让 x 从 0 走到 t, 即
>
> $$D=\left\{\left(x,t\right)\mid0\leqslant t\leqslant2\pi,0\leqslant x\leqslant t\right\}.$$
>
> 于是
>
> $$\int_{0}^{2\pi}\mathrm{d}x\int_{x}^{2\pi}\frac{x\sin^{2}t}{t^{2}}\mathrm{d}t=\int_{0}^{2\pi}\mathrm{d}t\int_{0}^{t}\frac{x\sin^{2}t}{t^{2}}\mathrm{d}x.$$
>
> 第三步：先算内层（对 x 积分）。此时 t 是常数， $\frac{\sin^{2}t}{t^{2}}$ 可以提到积分号外：
>
> $$\int_{0}^{t}\frac{x\sin^{2}t}{t^{2}}\mathrm{d}x=\frac{\sin^{2}t}{t^{2}}\int_{0}^{t}x\mathrm{d}x=\frac{\sin^{2}t}{t^{2}}\cdot\frac{t^{2}}{2}=\frac{\sin^{2}t}{2}.$$
>
> 第四步：算外层。
>
> $$\int_{0}^{2\pi}\frac{\sin^{2}t}{2}\mathrm{d}t=\frac{1}{2}\int_{0}^{2\pi}\frac{1-\cos2t}{2}\mathrm{d}t=\frac{1}{2}\cdot\pi=\frac{\pi}{2}.$$
>
> 所以原式 $=\frac{\pi}{2}$

**2.** (难度:★★★)已知平面区域 $D=\left\{(x,y)\mid(y-2x)^{2}\leqslant4-y^{2},0\leqslant y\leqslant2\right\}$，计算

$$I=\iint_{D}\frac{(x-y)^{2}}{x^{2}+y^{2}}\mathrm{d}x\mathrm{d}y.$$

> [!answer]- 原书参考答案（A.7.1·二重积分 第 2 题，未逐题独立验算）
> **2.** 积分区域是椭圆 $(y-2x)^{2}+y^{2}\leqslant4$ 的上半部分，而被积函数对 $(x,y)$ 是零次齐次的，故先作线性换元把区域变成半圆盘.
>
> **第一步：换元 u = y - 2x, v = y.** 此时区域化为
>
> $$u^{2}+v^{2}\leqslant4,\qquad v\geqslant0$$
>
> （由 $u^{2}+v^{2}\leqslant4$ 自动有 $0\leqslant v\leqslant2$ ，故原题中的 $0\leqslant y\leqslant2$ 是多余的）. 又 $x=\frac{v-u}{2}$
>
> $$\left|\frac{\partial(x,y)}{\partial(u,v)}\right|=\left|\begin{matrix}-\frac{1}{2}&\frac{1}{2}\\ 0&1\end{matrix}\right|=\frac{1}{2},\qquad x-y=-\frac{u+v}{2},\qquad x^{2}+y^{2}=\frac{(v-u)^{2}+4v^{2}}{4}.$$
>
> 于是
>
> $$I=\frac{1}{2}\iint_{u^{2}+v^{2}\leqslant4,v\geqslant0}\frac{(u+v)^{2}}{(v-u)^{2}+4v^{2}}\mathrm{d}u\mathrm{d}v.$$
>
> **第二步: 极坐标 $u = 2r \cos \theta$, $v = 2r \sin \theta$ ( $0 \leq r \leq 1$, $0 \leq \theta \leq \pi$).** 被积函数与 r 无关:
>
> $$\frac{(u+v)^{2}}{(v-u)^{2}+4v^{2}}=\frac{(\cos\theta+\sin\theta)^{2}}{(\sin\theta-\cos\theta)^{2}+4\sin^{2}\theta},\qquad\mathrm{d}u\,\mathrm{d}v=4r\,\mathrm{d}r\,\mathrm{d}\theta,$$
>
> 故
>
> $$I=\frac{1}{2}\cdot4\cdot\frac{1}{2}\int_{0}^{\pi}\frac{(\cos\theta+\sin\theta)^{2}}{(\sin\theta-\cos\theta)^{2}+4\sin^{2}\theta}\mathrm{d}\theta=\int_{0}^{\pi}\frac{1+\sin2\theta}{3-\sin2\theta-2\cos2\theta}\mathrm{d}\theta.$$
>
> **第三步：算这个三角积分.** 令 $\varphi = 2\theta$，并把分母写成 $3 - \sqrt{5}\sin(\varphi + \delta)$ ( $\cos\delta = \frac{1}{\sqrt{5}}$, $\sin\delta = \frac{2}{\sqrt{5}}$)，则
>
> $$I=\frac{1}{2}\int_{0}^{2\pi}\frac{1+\sin\varphi}{3-\sin\varphi-2\cos\varphi}\mathrm{d}\varphi=\frac{1}{2}\left[\frac{2\pi}{\sqrt{9-5}}+\frac{\pi}{5}\right]=\frac{1}{2}\left[\pi+\frac{\pi}{5}\right]=\frac{3\pi}{5}.$$
>
> （其中第二个积分用 $\int_{0}^{2\pi}\frac{\sin\varphi}{3-\sqrt{5}\sin\varphi}\mathrm{d}\varphi=\frac{\pi}{\sqrt{5}}$、 $\cos\delta=\frac{1}{\sqrt{5}}$ 算出。）

**3.** (难度: ★★★) 设 D 是由直线 x + y = 1 与两坐标轴围成的三角形区域, 求

$$\iint_{D}\frac{(x+y)\ln\left(1+\frac{y}{x}\right)}{\sqrt{1-x-y}}\mathrm{d}x\mathrm{d}y.$$

> [!answer]- 原书参考答案（A.7.1·二重积分 第 3 题，未逐题独立验算）
> **3.** 被积函数中同时出现 x + y、 $\frac{y}{x}$、1 - x - y 三种结构，令
>
> $$u=x+y,\qquad v=\frac{y}{x}.$$
>
> 反解出x,y:
>
> $$x=\frac{u}{1+v},\qquad y=\frac{uv}{1+v}.$$
>
> 再换区域: $x \geqslant 0, y \geqslant 0$ 等价于 $u \geqslant 0, v \geqslant 0$; 而 $x + y \leqslant 1$ 就是 u $\leqslant 1$. 所以
>
> $$D^{\prime}=\left\{(u,v)\mid0\leqslant u\leqslant1,0\leqslant v<+\infty\right\}.$$
>
> 算雅可比行列式：
>
> $$\frac{\partial x}{\partial u}=\frac{1}{1+v},\quad\frac{\partial x}{\partial v}=-\frac{u}{(1+v)^{2}},$$
>
> $$\frac{\partial y}{\partial u}=\frac{v}{1+v},\quad\frac{\partial y}{\partial v}=\frac{u}{(1+v)^{2}},$$
>
> 故
>
> $$\frac{\partial(x,y)}{\partial(u,v)}=\frac{1}{1+v}\cdot\frac{u}{(1+v)^{2}}+\frac{u}{(1+v)^{2}}\cdot\frac{v}{1+v}=\frac{u}{(1+v)^{2}},$$
>
> 于是 $\mathrm{d}x\,\mathrm{d}y=\frac{u}{(1+v)^{2}}\,\mathrm{d}u\,\mathrm{d}v$. 被积函数化为
>
> $$\frac{u\ln(1+v)}{\sqrt{1-u}}.$$
>
> 所以
>
> $$\begin{aligned}I&=\int_{0}^{1}\int_{0}^{+\infty}\frac{u\ln(1+v)}{\sqrt{1-u}}\cdot\frac{u}{(1+v)^{2}}\mathrm{d}v\mathrm{d}u\\&=\left(\int_{0}^{1}\frac{u^{2}}{\sqrt{1-u}}\mathrm{d}u\right)\left(\int_{0}^{+\infty}\frac{\ln(1+v)}{(1+v)^{2}}\mathrm{d}v\right).\end{aligned}$$
>
> 第一个积分令 u = 1 - t:
>
> $$\int_{0}^{1}\frac{u^{2}}{\sqrt{1-u}}\mathrm{d}u=\int_{0}^{1}\frac{(1-t)^{2}}{\sqrt{t}}\mathrm{d}t=2-\frac{4}{3}+\frac{2}{5}=\frac{16}{15}.$$
>
> 第二个积分令 w = 1 + v，再用分部积分：
>
> $$\int_{0}^{+\infty}\frac{\ln(1+v)}{(1+v)^{2}}\mathrm{d}v=\int_{1}^{+\infty}\frac{\ln w}{w^{2}}\mathrm{d}w=\left[-\frac{\ln w}{w}\right]_{1}^{+\infty}+\int_{1}^{+\infty}\frac{1}{w^{2}}\mathrm{d}w=1.$$
>
> $$I=\frac{16}{15}\times1=\frac{16}{15}.$$
>
> 因此

**4.** (难度:★★★) 设 $D: 1 \leq x^{2} + y^{2} \leq 4$，求积分

$$I=\iint_{D}(x+y^{2})e^{-(x^{2}+y^{2}-4)}\mathrm{d}x\mathrm{d}y.$$

> [!answer]- 原书参考答案（A.7.1·二重积分 第 4 题，未逐题独立验算）
> **4.** 区域是圆环，先看对称性：被积函数里的 x 一次项直接积掉， $y^{2}$ 项用轮换对称凑成 $\frac{x^{2}+y^{2}}{2}$，再上极坐标. D 关于 y 轴对称，而 $xe^{-(x^{2}+y^{2}-4)}$ 关于 x 是奇函数，所以
>
> $$\iint_{D}x\mathbf{e}^{-(x^{2}+y^{2}-4)}\mathrm{d}\sigma=0.$$
>
> 圆环在 x 与 y 互换下不变，由轮换对称性
>
> $$\iint_{D}y^{2}\mathrm{e}^{-(x^{2}+y^{2}-4)}\mathrm{d}\sigma=\iint_{D}x^{2}\mathrm{e}^{-(x^{2}+y^{2}-4)}\mathrm{d}\sigma,$$
>
> 于是
>
> $$I=\frac{1}{2}\iint_{D}(x^{2}+y^{2})\mathbf{e}^{-(x^{2}+y^{2}-4)}\mathrm{d}\sigma.$$
>
> 用极坐标 $x = \rho \cos \theta$, $y = \rho \sin \theta$, 其中 $0 \leq \theta \leq 2\pi$, $1 \leq \rho \leq 2$:
>
> $$I=\frac{1}{2}\int_{0}^{2\pi}\mathrm{d}\theta\int_{1}^{2}\rho^{2}\mathrm{e}^{-(\rho^{2}-4)}\rho\mathrm{d}\rho=\pi\int_{1}^{2}\rho^{3}\mathrm{e}^{4-\rho^{2}}\mathrm{d}\rho.$$
>
> 令 $u = \rho^2$, $\mathrm{d}u = 2\rho\,\mathrm{d}\rho$, 则 $\rho^3\,\mathrm{d}\rho = \frac{1}{2}u\,\mathrm{d}u$,
>
> $$\int_{1}^{2}\rho^{3}\mathrm{e}^{-\rho^{2}}\mathrm{d}\rho=\frac{1}{2}\int_{1}^{4}u\mathrm{e}^{-u}\mathrm{d}u=\frac{1}{2}\left[-(u+1)\mathrm{e}^{-u}\right]_{1}^{4}=\frac{1}{2}\left(2\mathrm{e}^{-1}-5\mathrm{e}^{-4}\right).$$
>
> 所以
>
> $$I=\pi\mathbf{e}^{4}\cdot\frac{1}{2}\left(2\mathbf{e}^{-1}-5\mathbf{e}^{-4}\right)=\pi\left(\mathbf{e}^{3}-\frac{5}{2}\right).$$
>
> 圆环上的标准两连击：先让奇函数项归零，再用 $x^{2}$ 与 $y^{2}$ 的轮换把被积函数凑成 $\frac{1}{2}(x^{2}+y^{2})$.

**5.** (难度:★★★★) 设 $f(x,y)$ 为 $\mathbb{R}^2$ 上的非负连续函数, 若极限 $I = \lim_{t \to +\infty} \iint_{x^2 + y^2 \leq t^2} f(x,y) \, \mathrm{d}\sigma$ 存在且有限, 则称广义积分 $\iint_{\mathbb{R}^2} f(x,y) \, \mathrm{d}\sigma$ 收敛于 I.

(1) 设 $\iint_{\mathbb{R}^{2}} f(x,y) \, d\sigma$ 收敛于 I，证明： $\lim_{t \to +\infty} \iint_{-t < x < t, -t < y < t} f(x,y) \, d\sigma$ 存在且等于 I.

(2) 设 $\iint_{\mathbb{R}^{2}} e^{ax^{2}+2bxy+cy^{2}} \, \mathrm{d}\sigma$ 收敛于 I，其中实二次型 $ax^{2}+2bxy+cy^{2}$ 在正交变换下的标准型为 $\lambda_{1}u^{2}+\lambda_{2}v^{2}$，证明： $\lambda_{1},\lambda_{2}$ 均小于 0.

> [!answer]- 原书参考答案（A.7.1·二重积分 第 5 题，未逐题独立验算）
> **5.** (1) 用两个区域互相夹逼: 正方形内含于大圆、小圆内含于正方形. (2) 若某个 $\lambda \geqslant 0$, 取正方形 $[-t/\sqrt{2}, t/\sqrt{2}]^{2}$, 此时被积函数可拆成两个一维积分的乘积, 其中一项趋于无穷, 另一项有正下界, 乘起来发散. (1) 记
>
> $$C_{t}=\{x^{2}+y^{2}\leqslant t^{2}\},\qquad D_{t}=\{|x|\leqslant t,|y|\leqslant t\}.$$
>
> 显然 $C_t \subset D_t \subset C_{\sqrt{2}t}$. 由 $f(x, y) \geq 0$,
>
> $$\iint_{C_{t}}f(x,y)\mathrm{d}\sigma\leqslant\iint_{D_{t}}f(x,y)\mathrm{d}\sigma\leqslant\iint_{C_{\sqrt{2}t}}f(x,y)\mathrm{d}\sigma.$$
>
> 当 $t \to +\infty$ 时，两端都趋于 I，由夹逼定理
>
> $$\lim_{t\to+\infty}\iint_{D_{t}}f(x,y)\mathrm{d}\sigma=I.$$
>
> (2) 作正交变换把二次型化为标准形，即用 $(u, v)$ 记原来 $(x, y)$ 的坐标，则
>
> $$ax^{2}+2bxy+cy^{2}=\lambda_{1}u^{2}+\lambda_{2}v^{2}.$$
>
> 反设 $\lambda_{1} \geqslant 0$. 取正方形区域
>
> $$S_{t}=\left\{\left(u,v\right)\Bigm|\left|u\right|\leqslant\frac{t}{\sqrt{2}},\ \left|v\right|\leqslant\frac{t}{\sqrt{2}}\right\}.$$
>
> 在 $S_{t}$上，
>
> $$\begin{aligned}\iint_{S_{t}}\mathbf{e}^{ax^{2}+2bxy+cy^{2}}\mathrm{d}u\mathrm{d}v&=\iint_{S_{t}}\mathbf{e}^{\lambda_{1}u^{2}+\lambda_{2}v^{2}}\mathrm{d}u\mathrm{d}v\\&=\left(\int_{-t/\sqrt{2}}^{t/\sqrt{2}}\mathbf{e}^{\lambda_{1}u^{2}}\mathrm{d}u\right)\left(\int_{-t/\sqrt{2}}^{t/\sqrt{2}}\mathbf{e}^{\lambda_{2}v^{2}}\mathrm{d}v\right).\end{aligned}$$
>
> 因为 $\lambda_{1} \geqslant 0$，所以 $e^{\lambda_{1}u^{2}} \geqslant 1$，第一个因子满足
>
> $$\int_{-t/\sqrt{2}}^{t/\sqrt{2}}\mathrm{e}^{\lambda_{1}u^{2}}\mathrm{d}u\geqslant\sqrt{2}t\longrightarrow+\infty.$$
>
> 第二个因子总有一个与 t 无关的正下界: 当 $\lambda_{2} \geqslant 0$ 时它 $\geqslant \sqrt{2}t$, 当 $\lambda_{2} < 0$ 时它收敛到 $\sqrt{\pi/|\lambda_{2}|}$, 总之
>
> $$\int_{-t/\sqrt{2}}^{t/\sqrt{2}}\mathrm{e}^{\lambda_{2}v^{2}}\mathrm{d}v\geqslant c>0$$
>
> 对充分大的 t 成立. 于是
>
> $$\iint_{S_{t}}\mathbf{e}^{a x^{2}+2b x y+c y^{2}}\mathrm{d}u\mathrm{d}v\geqslant c\sqrt{2}t\;\longrightarrow\;+\infty,$$
>
> 与广义积分收敛矛盾. 故 $\lambda_1 < 0$, 同理 $\lambda_2 < 0$. (2) 的本质是: 要使 $\iint e^q \, d\sigma$ 收敛, 必须有 $q \to -\infty$, 也就是 $q$ 负定, 即两个特征值都小于 0. 取正方形 $[-t/\sqrt{2}, t/\sqrt{2}]^2$ 的好处是被积函数可拆成两个一维积分的乘积, 放缩更直接.

### 7.1.2 三重积分

相比二重积分，计算难度略微增加，但计算思路与二重积分基本相同，同样需要一定量的计算训练。

**1.** (难度:★★★★) 设 $\Omega$ 是由平面 $\Pi_{1}: x = 0$、 $\Pi_{2}: x = y$、 $\Pi_{3}: y = z$、 $\Pi_{4}: z = 1$ 和 $\Pi_{5}: z = 2$ 围成的空间区域, 求三重积分

$$\iiint_{\Omega}\frac{\mathrm{d}x\mathrm{d}y\mathrm{d}z}{\sqrt{y^{2}+z^{2}}}.$$

> [!answer]- 原书参考答案（A.7.1·三重积分 第 1 题，未逐题独立验算）
> **1.** 先画区域. 在平面 y = z、x = y 与 x = 0 中: x = 0 给出 $x \geqslant 0, x = y$ 与 y = z 给出 $0 \leqslant x \leqslant y \leqslant z$. 再用 z = 1, z = 2 截出高度, 于是
>
> $$\Omega=\left\{\left(x,y,z\right)\mid1\leqslant z\leqslant2,0\leqslant y\leqslant z,0\leqslant x\leqslant y\right\}.$$
>
> <div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//85d68146-9e04-4ea8-952c-cdb18bae5543/markdown_1/imgs/img_in_image_box_431_1032_813_1409.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-11-05T13%3A08%3A27Z%2F-1%2F%2F79c1d926bab1ee77254dc430b2c87e7701527d714ab11b064b14014ea5d3ec37" alt="Image" width="32%" /></div>
>
> 图中的竖直虚线就是「先一后二」的积分路线: 固定 $(x,y)$，让 z 从下底穿到上底. 按先一后二计算:
>
> $$I=\int_{1}^{2}\mathrm{d}z\int_{0}^{z}\mathrm{d}y\int_{0}^{y}\frac{\mathrm{d}x}{\sqrt{y^{2}+z^{2}}}.$$
>
> 最内层对 x 积分最简单：
>
> $$\int_{0}^{y}\frac{\mathrm{d}x}{\sqrt{y^{2}+z^{2}}}=\frac{y}{\sqrt{y^{2}+z^{2}}}.$$
>
> 再对 y 积分，凑微分得
>
> $$\int_{0}^{z}\frac{y\mathrm{d}y}{\sqrt{y^{2}+z^{2}}}=\left[\sqrt{y^{2}+z^{2}}\right]_{0}^{z}=\sqrt{2z^{2}}-\sqrt{z^{2}}=(\sqrt{2}-1)z.$$
>
> 最后对 z 积分：
>
> $$I=\left.\int_{1}^{2}(\sqrt{2}-1)z\mathrm{d}z=(\sqrt{2}-1)\cdot\frac{z^{2}}{2}\right|_{1}^{2}=\frac{3}{2}(\sqrt{2}-1).$$

**2.** (难度:★★★★) 设 $\Omega=\{(x,y,z)\mid0\leqslant x,y,z\leqslant1\}$，在此空间内，求三重积分：

$$I=\iiint_{\Omega}\frac{1}{(1+x^{2}+y^{2}+z^{2})^{2}}\mathrm{d}x\mathrm{d}y\mathrm{d}z.$$

> [!answer]- 原书参考答案（A.7.1·三重积分 第 2 题，未逐题独立验算）
> **2.** 区域和被测函数对 x, y 完全对称，所以先把正方体沿平面 y = x 折成两半：
>
> $$I=2\int_{0}^{1}\mathrm{d}z\iint_{D_{xy}}\frac{\mathrm{d}x\mathrm{d}y}{(1+x^{2}+y^{2}+z^{2})^{2}},\qquad D_{xy}=\{0\leqslant y\leqslant x\leqslant1\}.$$
>
> 这里选先二后一：截面 $D_{xy}$ 与 z 无关，截面积好写. 对 $D_{xy}$ 用极坐标，边界 x=1 即 $\rho=\frac{1}{\cos\theta}$，而 $0\leqslant y\leqslant x$ 即 $0\leqslant\theta\leqslant\frac{\pi}{4}$，故
>
> $$\begin{aligned}\iint_{D_{xy}}\frac{\mathrm{d}x\mathrm{d}y}{(1+x^{2}+y^{2}+z^{2})^{2}}&=\int_{0}^{\pi/4}\mathrm{d}\theta\int_{0}^{1/\cos\theta}\frac{\rho\mathrm{d}\rho}{(1+\rho^{2}+z^{2})^{2}}\\&=\int_{0}^{\pi/4}\left(\frac{1}{2}\cdot\frac{1}{1+z^{2}}-\frac{1}{2}\cdot\frac{1}{\sec^{2}\theta+z^{2}+1}\right)\mathrm{d}\theta\\&=\frac{\pi}{8}\cdot\frac{1}{1+z^{2}}-\frac{1}{2}\int_{0}^{\pi/4}\frac{\mathrm{d}\theta}{\sec^{2}\theta+z^{2}+1}.\end{aligned}$$
>
> 于是
>
> $$I=\frac{\pi}{4}\int_{0}^{1}\frac{\mathrm{d}z}{1+z^{2}}-J=\frac{\pi}{4}\cdot\frac{\pi}{4}-J=\frac{\pi^{2}}{16}-J,$$
>
> 其中
>
> $$J=\int_{0}^{1}\mathrm{d}z\int_{0}^{\pi/4}\frac{\mathrm{d}\theta}{\sec^{2}\theta+z^{2}+1}=\int_{0}^{\pi/4}\mathrm{d}\theta\int_{0}^{1}\frac{\mathrm{d}z}{\sec^{2}\theta+z^{2}+1}.$$
>
> 对后一个积分令 $z = \tan t$，则 $\mathrm{d}z = \sec^{2}t\,\mathrm{d}t$，且 $t$ 从 $0$ 到 $\frac{\pi}{4}$，于是
>
> $$J=\int_{0}^{\pi/4}\mathrm{d}\theta\int_{0}^{\pi/4}\frac{\sec^{2}t}{\sec^{2}t+\sec^{2}\theta}\mathrm{d}t.$$
>
> 把 $\theta$与t互换，J的表达式不变，所以
>
> $$2J=\int_{0}^{\pi/4}\int_{0}^{\pi/4}\frac{\sec^{2}t+\sec^{2}\theta}{\sec^{2}t+\sec^{2}\theta}\mathrm{d}t\mathrm{d}\theta=\int_{0}^{\pi/4}\int_{0}^{\pi/4}\mathrm{d}t\mathrm{d}\theta=\frac{\pi^{2}}{16},$$
>
> 即 $J = \frac{\pi^{2}}{32}$. 因此
>
> $$I=\frac{\pi^{2}}{16}-\frac{\pi^{2}}{32}=\frac{\pi^{2}}{32}.$$

**3.** (难度：★★★★) 求抛物面 $z = x^{2} + y^{2} + 1$ 上任意一点 $P_{0}(x_{0}, y_{0}, z_{0})$ 处的切平面与抛物面 $z = x^{2} + y^{2}$ 所围成的立体的体积.

> [!answer]- 原书参考答案（A.7.1·三重积分 第 3 题，未逐题独立验算）
> **3.** 切平面在 $P_{0}$ 附近与抛物面之间夹出一个「小帽」，把坐标原点平移到 $P_{0}$ 的投影处，高度差会是漂亮的 $1-r^{2}$. 设 $P_{0}(x_{0},y_{0},z_{0})$，则 $z_{0}=x_{0}^{2}+y_{0}^{2}+1$. 记 $\rho_{0}^{2}=x_{0}^{2}+y_{0}^{2}$，抛物面在 $P_{0}$ 处的切平面为
>
> $$z=z_{0}+2x_{0}(x-x_{0})+2y_{0}(y-y_{0})=2x_{0}x+2y_{0}y+1-\rho_{0}^{2}.$$
>
> 在两曲面所围立体内，取以 $(x_{0},y_{0})$为原点的极坐标：
>
> $$x=x_{0}+r\cos\theta,\qquad y=y_{0}+r\sin\theta.$$
>
> 代入切平面：
>
> $$2x_{0}x+2y_{0}y+1-\rho_{0}^{2}=\rho_{0}^{2}+2r\rho_{0}\cos(\theta-\theta_{0})+1,$$
>
> 而抛物面
>
> $$x^{2}+y^{2}=\rho_{0}^{2}+2r\rho_{0}\cos(\theta-\theta_{0})+r^{2}.$$
>
> 两者之差（立体的高）为
>
> $$h=1-r^{2}.$$
>
> 当 r = 1 时高为 0，说明交线是 r = 1 的圆，于是
>
> $$V=\int_{0}^{2\pi}\mathrm{d}\theta\int_{0}^{1}(1-r^{2})r\mathrm{d}r=2\pi\left[\frac{r^{2}}{2}-\frac{r^{4}}{4}\right]_{0}^{1}=2\pi\cdot\frac{1}{4}=\frac{\pi}{2}.$$
>
> 切平面与抛物面围成的体积，与切点位置无关：把原点搬到切点正下方后，高恒为 $1-r^{2}$.

**4.** (难度:★★★★) 设 $\Omega = \{(x, y, z) \mid x^2 + y^2 + z^2 \leq R^2\}$，求 $\iiint_{\Omega} x^2 \, \mathrm{d}V$.

> [!answer]- 原书参考答案（A.7.1·三重积分 第 4 题，未逐题独立验算）
> **4.** 球体上 $\iiint_{\Omega} x^{2} \, \mathrm{d}V$、 $\iiint_{\Omega} y^{2} \, \mathrm{d}V$、 $\iiint_{\Omega} z^{2} \, \mathrm{d}V$ 三者相等，把 $x^{2}$ 换成 $\frac{1}{3}(x^{2}+y^{2}+z^{2})$。球体 $\Omega$ 关于 x,y,z 完全对称，故
>
> $$\iiint_{\Omega}x^{2}\mathrm{d}V=\iiint_{\Omega}y^{2}\mathrm{d}V=\iiint_{\Omega}z^{2}\mathrm{d}V=\frac{1}{3}\iiint_{\Omega}(x^{2}+y^{2}+z^{2})\mathrm{d}V.$$
>
> 用球坐标，
>
> $$\iiint_{\Omega}(x^{2}+y^{2}+z^{2})\mathrm{d}V=\int_{0}^{2\pi}\mathrm{d}\theta\int_{0}^{\pi}\mathrm{d}\varphi\int_{0}^{R}r^{4}\sin\varphi\mathrm{d}r=2\pi\cdot2\cdot\frac{R^{5}}{5}=\frac{4\pi R^{5}}{5}.$$
>
> 所以
>
> $$\iiint_{\Omega}x^{2}\mathrm{d}V=\frac{1}{3}\cdot\frac{4\pi R^{5}}{5}=\frac{4\pi R^{5}}{15}.$$
>
> 只要区域与积分变量具有轮换或对称关系, 就先写 $\iiint_{\Omega} x^{2} \, \mathrm{d}V = \frac{1}{3} \iiint_{\Omega} (x^{2} + y^{2} + z^{2}) \, \mathrm{d}V$, 球坐标一步即可.

**5.** （难度：★★★★）计算三重积分

$$\iiint_{\Omega}\frac{xyz}{x^{2}+y^{2}}\mathrm{d}x\mathrm{d}y\mathrm{d}z,$$

其中 $\Omega$ 是由曲面 $(x^{2}+y^{2}+z^{2})^{2}=2xy$ 围成的区域在第一卦限的部分.

> [!answer]- 原书参考答案（A.7.1·三重积分 第 5 题，未逐题独立验算）
> **5.** 区域 $\Omega$ 是第一卦限内 $(x^{2}+y^{2}+z^{2})^{2}\leqslant2xy$ 的部分，用球坐标最方便.
>
> **第一步:把曲面化成 r 的显式.** 取 $x = r \sin \varphi \cos \theta$, $y = r \sin \varphi \sin \theta$, $z = r \cos \varphi$, 则 $x^2 + y^2 = r^2 \sin^2 \varphi$, 于是
>
> $$\left(x^{2}+y^{2}+z^{2}\right)^{2}=2xy\iff r^{4}=2r^{2}\sin^{2}\varphi\cos\theta\sin\theta\iff r^{2}=\sin^{2}\varphi\sin2\theta.$$
>
> 第一卦限对应 $0 \leqslant \theta \leqslant \frac{\pi}{2}, 0 \leqslant \varphi \leqslant \frac{\pi}{2}$，故
>
> $$\Omega:0\leqslant r\leqslant\sin\varphi\sqrt{\sin2\theta},\quad0\leqslant\theta,\varphi\leqslant\frac{\pi}{2}.$$
>
> **第二步：化简被积函数并分离变量.**
>
> $$\frac{xyz}{x^{2}+y^{2}}=\frac{r^{3}\sin^{2}\varphi\cos\varphi\cos\theta\sin\theta}{r^{2}\sin^{2}\varphi}=r\cos\varphi\sin\theta\cos\theta,\qquad\mathrm{d}V=r^{2}\sin\varphi\mathrm{d}r\mathrm{d}\varphi\mathrm{d}\theta,$$
>
> 故被积式 $= r^3 \sin \varphi \cos \varphi \sin \theta \cos \theta \, \mathrm{d}r \, \mathrm{d}\varphi \, \mathrm{d}\theta$，三个变量完全分离。
>
> **第三步：逐层积分.**
>
> $$I=\frac{1}{4}\int_{0}^{\pi/2}\mathrm{d}\theta\int_{0}^{\pi/2}\mathrm{d}\varphi\sin^{5}\varphi\cos\varphi\cdot\sin^{2}2\theta\sin\theta\cos\theta=\frac{1}{4}\left(\int_{0}^{\pi/2}\sin^{5}\varphi\cos\varphi\mathrm{d}\varphi\right)\left(\int_{0}^{\pi/2}\sin^{2}2\theta\sin\theta\cos\theta\mathrm{d}\theta\right),$$
>
> (这里已用 $\int_{0}^{R} r^{3} dr = \frac{R^{4}}{4}$ 与 $R^{4} = \sin^{4} \varphi \sin^{2} 2\theta$.) 而
>
> $$\int_{0}^{\pi/2}\sin^{5}\varphi\cos\varphi\mathrm{d}\varphi=\frac{1}{6},\qquad\int_{0}^{\pi/2}\sin^{2}2\theta\sin\theta\cos\theta\mathrm{d}\theta=4\int_{0}^{\pi/2}\sin^{3}\theta\cos^{3}\theta\mathrm{d}\theta=4\cdot\frac{1}{12}=\frac{1}{3}$$
>
> 所以
>
> $$I=\frac{1}{4}\cdot\frac{1}{6}\cdot\frac{1}{3}=\frac{1}{72}.$$

**6.** (难度：★★★★) 某物体所在的空间区域为 $\Omega: x^{2} + y^{2} + 2z^{2} \leqslant x + y + 2z$，密度函数为 $x^{2} + y^{2} + z^{2}$，求质量 M.

> [!answer]- 原书参考答案（A.7.1·三重积分 第 6 题，未逐题独立验算）
> **6.** 先把区域配方, 发现是中心在 $\left(\frac{1}{2}, \frac{1}{2}, \frac{1}{2}\right)$ 的椭球, 然后平移; 平移后的一次项用对称性消掉, 剩下的二次项套椭球公式. 把区域配方:
>
> $$x^{2}-x+y^{2}-y+2z^{2}-2z\leqslant0\iff\left(x-\frac{1}{2}\right)^{2}+\left(y-\frac{1}{2}\right)^{2}+2\left(z-\frac{1}{2}\right)^{2}\leqslant1.$$
>
> 平移
>
> $$X=x-\frac{1}{2},\qquad Y=y-\frac{1}{2},\qquad Z=z-\frac{1}{2},$$
>
> 则 $\Omega$ 变为椭球 $X^{2} + Y^{2} + 2Z^{2} \leqslant 1$. 密度函数变成
>
> $$\rho=X^{2}+Y^{2}+Z^{2}+X+Y+Z+\frac{3}{4}.$$
>
> 椭球关于三个坐标平面都对称, 一次项 $X + Y + Z$ 的积分都为 0; 又 X, Y 的地位相同, 故 $\iiint X^2 = \iiint Y^2$. 由椭球公式 (半轴 a, b, c 时 $\iiint x^2 \, \mathrm{d}V = \frac{4\pi}{15} a^3 bc$):
>
> $$\iiint_{\Omega}X^{2}\mathrm{d}V=\frac{4\pi}{15}\cdot\frac{1}{\sqrt{2}},\qquad\iiint_{\Omega}Y^{2}\mathrm{d}V=\frac{4\pi}{15}\cdot\frac{1}{\sqrt{2}},\qquad\iiint_{\Omega}Z^{2}\mathrm{d}V=\frac{4\pi}{15}\cdot\frac{1}{2\sqrt{2}}.$$
>
> 三者相加
>
> $$\iiint_{\Omega}(X^{2}+Y^{2}+Z^{2})\mathrm{d}V=\frac{10\pi}{15\sqrt{2}}=\frac{\sqrt{2}\pi}{3}.$$
>
> 又椭球体积
>
> $$V=\frac{4}{3}\pi\cdot1\cdot1\cdot\frac{1}{\sqrt{2}}=\frac{2\sqrt{2}\pi}{3},$$
>
> 所以
>
> $$M=\frac{\sqrt{2}\pi}{3}+\frac{3}{4}\cdot\frac{2\sqrt{2}\pi}{3}=\frac{\sqrt{2}\pi}{3}+\frac{\sqrt{2}\pi}{2}=\frac{5\sqrt{2}\pi}{6}.$$
>
> 区域不含参数时，先配方平移；平移后一次项必然积为0，剩下的只有「常数×体积」与「坐标平方的椭球公式」。

**7.** （难度：★★★★★）计算三重积分

$$I=\iiint_{V}\left|5x+y+z\right|\cdot\left|x+4y-z\right|\mathrm{d}x\mathrm{d}y\mathrm{d}z,$$

其中 $V=\left\{(x,y,z)\mid x^{2}+y^{2}+\frac{z^{2}}{9}\leqslant1\right\}$.

> [!answer]- 原书参考答案（A.7.1·三重积分 第 7 题，未逐题独立验算）
> **7.** 先把椭球压成球, 再取正交变换把两个线性因子变成两个坐标; 最后只剩下 $\iiint |uv| \, dv$.
>
> 作替换 $z = 3z'$，则 $\mathrm{d}V = 3\mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z'$，区域变成单位球 $V_0: x^2 + y^2 + z'^2 \leq 1$:
>
> $$I=3\iiint_{V_{0}}\left|5x+y+3z^{\prime}\right|\left|x+4y-3z^{\prime}\right|\mathrm{d}x\mathrm{d}y\mathrm{d}z^{\prime}.$$
>
> 记
>
> $$a_{1}=(5,1,3),\qquad a_{2}=(1,4,-3).$$
>
> 则 $a_{1}$ 与 $a_{2}$ 正交（对应分量乘积之和为 $5+4-9=0$），且
>
> $$|a_{1}|=\sqrt{35},\qquad|a_{2}|=\sqrt{26}.$$
>
> 把它们分别单位化, 再补上第三个方向, 组成正交变换 $(u, v, w)$, 满足
>
> $$5x+y+3z^{\prime}=\sqrt{35}u,\qquad x+4y-3z^{\prime}=\sqrt{26}v.$$
>
> 正交变换保持单位球与体积元素，于是
>
> $$I=3\sqrt{35}\sqrt{26}\iiint_{V_{0}}\left|u v\right|\mathrm{d}u\mathrm{d}v\mathrm{d}w=3\sqrt{910}\iiint_{u^{2}+v^{2}+w^{2}\leqslant1}\left|u v\right|\mathrm{d}u\mathrm{d}v\mathrm{d}w.$$
>
> 用球坐标算最后一个积分：
>
> $$\iiint_{V_{0}}\left|u v\right|\mathrm{d}V=\int_{0}^{1}r^{4}\mathrm{d}r\int_{0}^{\pi}\sin^{3}\varphi\mathrm{d}\varphi\int_{0}^{2\pi}\left|\cos\theta\sin\theta\right|\mathrm{d}\theta,$$
>
> 其中
>
> $$\int_{0}^{1}r^{4}\mathrm{d}r=\frac{1}{5},\qquad\int_{0}^{\pi}\sin^{3}\varphi\mathrm{d}\varphi=\frac{4}{3},\qquad\int_{0}^{2\pi}\left|\cos\theta\sin\theta\right|\mathrm{d}\theta=2.$$
>
> 所以
>
> $$I=3\sqrt{910}\cdot\frac{1}{5}\cdot\frac{4}{3}\cdot2=\frac{8\sqrt{910}}{5}.$$
>
> 关键是找到两个互相正交的向量 $(5,1,3)$ 与 $(1,4,-3)$; 正交变换把球保持不变, 于是被积函数只剩 $\left|uv\right|$ 这种最简单的形式.

## 7.2 第一类积分

### 7.2.1 第一类曲线积分

第一类曲线积分的考察主要聚焦在其对称性和参数法换元，相对比较基础，稍微注意即可.

**1.** (难度:★★) 计算 $I = \int_{\Gamma}(x^{2} + y^{2} + z^{2})\,ds$，其中 $\Gamma$ 是:

(1) 螺线 $x=a\cos t,\ y=a\sin t,\ z=bt\ (0\leq t\leq2\pi)$.

(2) 曲面 $x^{2}+y^{2}+z^{2}=\frac{9}{2}$ 与平面 x+z=1 的交线.

> [!answer]- 原书参考答案（A.7.2·第一类曲线积分 第 1 题，未逐题独立验算）
> **1.** (1) 由
>
> $$x^{\prime2}+y^{\prime2}+z^{\prime2}=a^{2}\sin^{2}t+a^{2}\cos^{2}t+b^{2}=a^{2}+b^{2}$$
>
> 得 $\mathrm{d}s = \sqrt{a^{2} + b^{2}}\mathrm{d}t$. 又
>
> $$x^{2}+y^{2}+z^{2}=a^{2}+b^{2}t^{2},$$
>
> 所以
>
> $$I=\sqrt{a^{2}+b^{2}}\int_{0}^{2\pi}(a^{2}+b^{2}t^{2})\mathrm{d}t=\sqrt{a^{2}+b^{2}}\left(2\pi a^{2}+\frac{8\pi^{3}b^{2}}{3}\right).$$
>
> (2) 曲线 $\Gamma$ 在球面 $x^{2} + y^{2} + z^{2} = \frac{9}{2}$ 上，所以被积函数恒等于 $\frac{9}{2}$，积分等于 $\frac{9}{2}$ 乘曲线弧长.
>
> $\Gamma$ 是平面 $x + z = 1$ 截球面所得的圆. 平面到原点 O 的距离为
>
> $$d=\frac{\left|0+0-1\right|}{\sqrt{1^{2}+1^{2}}}=\frac{1}{\sqrt{2}},$$
>
> 所以圆的半径
>
> $$r=\sqrt{\frac{9}{2}-d^{2}}=\sqrt{\frac{9}{2}-\frac{1}{2}}=2,$$
>
> 弧长为 $2\pi r = 4\pi$. 于是
>
> $$I=\frac{9}{2}\cdot4\pi=18\pi.$$

**2.** (难度: ★★) 设曲线 L 为球面 $x^{2} + y^{2} + z^{2} = 4$ 与平面 $x + y + z = 3$ 的交线, 求曲线积分

$$\int_{L}(x^{2}+2xy)\mathrm{d}s.$$

> [!answer]- 原书参考答案（A.7.2·第一类曲线积分 第 2 题，未逐题独立验算）
> **2.** 曲线 L 由球面与平面交出，两个方程在 x, y, z 轮换下都不变，所以三个坐标的平方积分相等；再用 $\frac{5}{2}$ 的轮换和凑出 xy 的积分。L 是球面 $x^{2} + y^{2} + z^{2} = 4$ 与平面 $x + y + z = 3$ 的交线，它是一个圆。把 x, y, z 轮换，两个方程都不变，故
>
> $$\int_{L}x^{2}\mathrm{d}s=\int_{L}y^{2}\mathrm{d}s=\int_{L}z^{2}\mathrm{d}s,\qquad\int_{L}x y\mathrm{d}s=\int_{L}y z\mathrm{d}s=\int_{L}z x\mathrm{d}s.$$
>
> 因此
>
> $$\int_{L}x^{2}\mathrm{d}s=\frac{1}{3}\int_{L}(x^{2}+y^{2}+z^{2})\mathrm{d}s=\frac{1}{3}\cdot4\int_{L}\mathrm{d}s=\frac{4}{3}|L|,$$
>
> $$\int_{L}x y\mathrm{d}s=\frac{1}{3}\int_{L}(x y+y z+z x)\mathrm{d}s.$$
>
> 又由
>
> $$(x+y+z)^{2}=x^{2}+y^{2}+z^{2}+2(x y+y z+z x),$$
>
> 把 $x + y + z = 3$, $x^{2} + y^{2} + z^{2} = 4$ 代入得
>
> $$9=4+2(xy+yz+zx)\implies xy+yz+zx=\frac{5}{2},$$
>
> 所以
>
> $$\int_{L}x y\mathrm{d}s=\frac{1}{3}\cdot\frac{5}{2}|L|=\frac{5}{6}|L|.$$
>
> 最后算 $|L|$: 原点到平面 $x + y + z = 3$ 的距离为 $\frac{3}{\sqrt{3}} = \sqrt{3}$，故截圆半径为 $\sqrt{4 - 3} = 1$，于是 $|L| = 2\pi$。代入得
>
> $$I=\frac{4}{3}\cdot2\pi+2\cdot\frac{5}{6}\cdot2\pi=6\pi.$$
>
> 第一类曲线积分里，只要曲线方程轮换对称，就能把被积函数拆成对称的几项，各用一个常数换掉，最后只剩弧长.

**3.** (难度: ★★★★) 设 $\Gamma$ 为空间曲线 $\left\{\begin{aligned}x^{2}+y^{2}+z^{2}&=1,\\ x+2y+3z&=0,\end{aligned}\right.$ 求第一型曲线积分:

$$\oint_{\Gamma}\left[(x+y)^{2}+(y+z)^{2}+(x+z)^{2}\right]\mathrm{d}s.$$

> [!answer]- 原书参考答案（A.7.2·第一类曲线积分 第 3 题，未逐题独立验算）
> **3.** **第一步：先化简被积式.** 展开得
>
> $$\begin{aligned}(x+y)^2+(y+z)^2+(z+x)^2&=2(x^2+y^2+z^2)+2(xy+yz+zx)\\&=(x^2+y^2+z^2)+(x+y+z)^2.\end{aligned}$$
>
> 在 $\Gamma$上 $x^{2}+y^{2}+z^{2}=1$，故所求积分为
>
> $$I=\oint_{\Gamma}\left[1+(x+y+z)^{2}\right]\mathrm{d}s=2\pi+\oint_{\Gamma}(x+y+z)^{2}\mathrm{d}s$$
>
> （Γ是球面的一个**大圆**:它由过球心的平面截得，半径1，周长 $2\pi$）.
>
> **第二步: 算 $\oint_{\Gamma}(x+y+z)^2\,\mathrm{d}s$。** 对大圆 $\Gamma$ (所在平面的单位法向量 $\mathbf{n} = \frac{(1,2,3)}{\sqrt{14}}$)，对任意单位向量 $\mathbf{a}$ 有
>
> $$\oint_{\Gamma}(\mathbf{a}\cdot\mathbf{r})^{2}\mathrm{d}s=\pi\left(1-(\mathbf{a}\cdot\mathbf{n})^{2}\right).$$
>
> （把 $\mathbf{r}$ 在平面内用标准正交基参数化即得： $\oint(\mathbf{a}\cdot\mathbf{r})^{2}ds = \pi\|\mathbf{a}_{\parallel}\|^2 = \pi (1-(\mathbf{a}\cdot\mathbf{n})^{2})$）
>
> ）取 $\mathbf{a} = \frac{(1,1,1)}{\sqrt{3}}$，则 $\mathbf{a}\cdot\mathbf{n} = \frac{6}{\sqrt{42}}$，于是
>
> $$\oint_{\Gamma}(x+y+z)^{2}\mathrm{d}s=3\oint_{\Gamma}(\mathbf{a}\cdot\mathbf{r})^{2}\mathrm{d}s=3\pi\left(1-\frac{36}{42}\right)=3\pi\cdot\frac{1}{7}=\frac{3\pi}{7}.$$
>
> **第三步：合并.**
>
> $$I=2\pi+\frac{3\pi}{7}=\frac{17\pi}{7}.$$
>
> （另一条路更直接：由轮换对称 $\oint_{\Gamma} x^{2} ds = \frac{1}{3} \oint_{\Gamma} (x^{2} + y^{2} + z^{2}) ds = \frac{2\pi}{3}$，再由 $2(xy + yz + zx) = (x + y + z)^{2} - 1$ 代入，结果相同。）

### 7.2.2 第一类曲面积分

第一类积分的核心考察内容，涉及众多处理技巧，既可通过投影和换元直接计算，也可借助高斯定理转为第二类积分间接计算，考察内容相对综合，一定要注意多加练习。

**1.** (难度: ★★) 计算

$$I=\iint_{\Sigma}(x+y+z)\mathrm{d}S,$$

其中 $\Sigma$ 是平面 $y + z = 5$ 被柱面 $x^{2} + y^{2} = 25$ 所截部分.

> [!answer]- 原书参考答案（A.7.2·第一类曲面积分 第 1 题，未逐题独立验算）
> **1.** **第一步：把 $\Sigma$ 上的被积函数用表面坐标表示。** $\Sigma$ 是平面 $y + z = 5$ 被柱面 $x^{2} + y^{2} = 25$ 截下的部分，在 $\Sigma$ 上 z = 5 - y，故
>
> $$x+y+z=x+5.$$
>
> **第二步:把第一类曲面积分投影到 xOy 面.** 平面 $z = 5 - y$ 的 $\mathrm{d}S = \sqrt{1 + z_{x}^{2} + z_{y}^{2}} \, \mathrm{d}x \, \mathrm{d}y = \sqrt{1 + 0 + 1} \, \mathrm{d}x \, \mathrm{d}y = \sqrt{2} \, \mathrm{d}x \, \mathrm{d}y$; 投影区域就是柱面所围的圆盘 $x^{2} + y^{2} \leqslant 25$. 于是
>
> $$I=\iint_{\Sigma}(x+y+z)\mathrm{d}S=\sqrt{2}\iint_{x^{2}+y^{2}\leqslant25}(x+5)\mathrm{d}x\mathrm{d}y.$$
>
> **第三步: 用对称性算两个积分.** $\iint_{x^2+y^2\leq25} x \, \mathrm{d}x \, \mathrm{d}y = 0$ (关于 $y$ 轴对称), 而 $\iint_{x^2+y^2\leq25} 5 \, \mathrm{d}x \, \mathrm{d}y = 5 \cdot 25\pi = 125\pi$. 所以
>
> $$I=\sqrt{2}\cdot125\pi=125\sqrt{2}\pi.$$

**2.** (难度:★★★) 设曲面 $\Sigma : \frac{x^{2}}{a^{2}} + \frac{y^{2}}{b^{2}} + \frac{z^{2}}{c^{2}} = 1 (a > 0, b > 0, c > 0)$ 上任意一点 $(x, y, z)$ 处的切平面为 $\Pi$, $\varphi(x, y, z)$ 是原点到平面 $\Pi$ 的距离, 计算曲面积分

$$\iint_{\Sigma}\frac{\mathrm{d}S}{\varphi(x,y,z)}.$$

> [!answer]- 原书参考答案（A.7.2·第一类曲面积分 第 2 题，未逐题独立验算）
> **2.** 先求切平面与 $\varphi$. 把曲面写成
>
> $$F(x,y,z)=\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}+\frac{z^{2}}{c^{2}}-1=0,$$
>
> 则在点 $(x,y,z)$处可取法向量
>
> $$\vec{n}=\left(\frac{2x}{a^{2}},\frac{2y}{b^{2}},\frac{2z}{c^{2}}\right).$$
>
> 切平面方程为
>
> $$\frac{x X}{a^{2}}+\frac{y Y}{b^{2}}+\frac{z Z}{c^{2}}=1,$$
>
> 原点到它的距离就是
>
> $$\varphi=\frac{1}{\sqrt{\frac{x^{2}}{a^{4}}+\frac{y^{2}}{b^{4}}+\frac{z^{2}}{c^{4}}}}.$$
>
> 记
>
> $$N=\sqrt{\frac{x^{2}}{a^{4}}+\frac{y^{2}}{b^{4}}+\frac{z^{2}}{c^{4}}},$$
>
> 则 $\frac{1}{\varphi}=N$，于是
>
> $$I=\iint_{\Sigma}N\mathrm{d}S.$$
>
> 注意到 $\vec{n}$ 的模长恰为 2N，故方向余弦为
>
> $$\cos\alpha=\frac{1}{2N}\cdot\frac{2x}{a^{2}}=\frac{x}{a^{2}N},\quad\cos\beta=\frac{y}{b^{2}N},\quad\cos\gamma=\frac{z}{c^{2}N}.$$
>
> 逐项相乘相加可以验证
>
> $$\frac{x}{a^{2}}\cos\alpha+\frac{y}{b^{2}}\cos\beta+\frac{z}{c^{2}}\cos\gamma=\frac{1}{N}\left(\frac{x^{2}}{a^{4}}+\frac{y^{2}}{b^{4}}+\frac{z^{2}}{c^{4}}\right)=\frac{N^{2}}{N}=N,$$
>
> 两边同乘 dS 并利用三个面积元公式, 得
>
> $$N\mathrm{d}S=\frac{x}{a^{2}}\mathrm{d}y\mathrm{d}z+\frac{y}{b^{2}}\mathrm{d}z\mathrm{d}x+\frac{z}{c^{2}}\mathrm{d}x\mathrm{d}y.$$
>
> 这里 $\Sigma$ 是闭曲面，取外侧正好符合高斯定理的方向要求（此时 $\cos\alpha, \cos\beta, \cos\gamma$ 就是外法线的方向余弦）。取
>
> $$P=\frac{x}{a^{2}},\qquad Q=\frac{y}{b^{2}},\qquad R=\frac{z}{c^{2}},$$
>
> 则
>
> $$\frac{\partial P}{\partial x}=\frac{1}{a^{2}},\qquad\frac{\partial Q}{\partial y}=\frac{1}{b^{2}},\qquad\frac{\partial R}{\partial z}=\frac{1}{c^{2}}.$$
>
> 由高斯定理，
>
> $$I=\iiint_{\Omega}\left(\frac{1}{a^{2}}+\frac{1}{b^{2}}+\frac{1}{c^{2}}\right)\mathrm{d}x\mathrm{d}y\mathrm{d}z=\left(\frac{1}{a^{2}}+\frac{1}{b^{2}}+\frac{1}{c^{2}}\right)\cdot\frac{4\pi a b c}{3}.$$
>
> 即
>
> $$I=\frac{4\pi}{3}\left(\frac{bc}{a}+\frac{ac}{b}+\frac{ab}{c}\right).$$

**3.** (难度: ★★★★★) 计算 $\iint_{\Sigma} z \, dS$，其中 $\Sigma$ 是柱面 $x^{2} + z^{2} = 2az$ (a > 0) 被圆锥面 $z = \sqrt{x^{2} + y^{2}}$ 所割下的部分曲面.

> [!answer]- 原书参考答案（A.7.2·第一类曲面积分 第 3 题，未逐题独立验算）
> **3.** 先看清 $\Sigma$ 是哪一块. 柱面 $x^{2}+z^{2}=2az$ 即
>
> $$x^{2}+(z-a)^{2}=a^{2},$$
>
> 它的纵坐标满足 $0 \leqslant z \leqslant 2a$ 。把曲面上的点代入锥面条件 $z^{2} \geqslant x^{2} + y^{2}$，并利用 $x^{2} = 2az - z^{2}$，得
>
> $$z^{2}\geqslant(2az-z^{2})+y^{2}\Longleftrightarrow y^{2}\leqslant2z(z-a),$$
>
> 它要求 $z \geqslant a$。所以被圆锥面「割下」的正是 $z \in [a, 2a]$ 的那一块。
>
> 方法一：直接参数化. 令
>
> $$x=a\sin\theta,\qquad z=a(1+\cos\theta),\qquad y=y,$$
>
> 则 $x^2 + (z - a)^2 = a^2$ 恒成立，且 $z = a(1 + \cos\theta)$ 取遍 $[a, 2a]$ 对应 $\theta \in \left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$。由 $y^2 \leq 2z(z - a)$ 得
>
> $$|y|\leqslant\sqrt{2a(1+\cos\theta)\cdot a\cos\theta}=a\sqrt{2\cos\theta\left(1+\cos\theta\right)}.$$
>
> 算面积因子: 把曲面上的点记为 $\overrightarrow{X}(\theta, y)$，则
>
> $$\frac{\partial\vec{X}}{\partial\theta}=(a\cos\theta,0,-a\sin\theta),\qquad\frac{\partial\vec{X}}{\partial y}=(0,1,0),$$
>
> 两者对应分量乘积相加：
>
> $$\left(\frac{\partial\vec{X}}{\partial\theta}\right)\cdot\left(\frac{\partial\vec{X}}{\partial y}\right)=a\cos\theta\cdot0+0\cdot1+\left(-a\sin\theta\right)\cdot0=0,$$
>
> 且各自模长平方为 $a^{2}$ 与 1，所以面积因子为 a，即 $\mathrm{d}S = a\,\mathrm{d}\theta\,\mathrm{d}y$。于是
>
> $$\begin{aligned}I&=\int_{-\pi/2}^{\pi/2}\int_{-Y}^{Y}a(1+\cos\theta)\cdot a\mathrm{d}y\mathrm{d}\theta=2a^{3}\sqrt{2}\int_{-\pi/2}^{\pi/2}(1+\cos\theta)^{3/2}\sqrt{\cos\theta}\mathrm{d}\theta\\&=4a^{3}\sqrt{2}\int_{0}^{\pi/2}(1+\cos\theta)^{3/2}\sqrt{\cos\theta}\mathrm{d}\theta,\end{aligned}$$
>
> 其中 $Y = a\sqrt{2\cos\theta(1 + \cos\theta)}$. 令 $u = 1 + \cos\theta$, 则 $\mathrm{d}\theta = -\frac{\mathrm{d}u}{\sqrt{u(2 - u)}}, \cos\theta = u - 1$, 于是
>
> $$\int_{0}^{\pi/2}(1+\cos\theta)^{3/2}\sqrt{\cos\theta}\mathrm{d}\theta=\int_{1}^{2}u\sqrt{\frac{u-1}{2-u}}\mathrm{d}u.$$
>
> 再令$u-1=t^2$,得
>
> $$\int_{1}^{2}u\sqrt{\frac{u-1}{2-u}}\mathrm{d}u=2\int_{0}^{1}\frac{t^{2}+t^{4}}{\sqrt{1-t^{2}}}\mathrm{d}t=2\left(\frac{\pi}{4}+\frac{3\pi}{16}\right)=\frac{7\pi}{8},$$
>
> （用到 $\int_{0}^{1}\frac{t^{2}dt}{\sqrt{1-t^{2}}}=\frac{\pi}{4}$， $\int_{0}^{1}\frac{t^{4}dt}{\sqrt{1-t^{2}}}=\frac{3\pi}{16}$。）所以
>
> $$I=4a^{3}\sqrt{2}\cdot\frac{7\pi}{8}=\frac{7\sqrt{2}}{2}\pi a^{3}.$$
>
> 方法二：投影到 xOy 面．由前面的讨论， $\Sigma$ 是柱面 $x^{2}+(z-a)^{2}=a^{2}$ 在 $z\geqslant a$ 的部分，因此可显式化为
>
> $$z=a+\sqrt{a^{2}-x^{2}},\qquad-a\leqslant x\leqslant a.$$
>
> 对固定的 x, z 也随之固定，而 y 由锥面条件 $y^{2} \leqslant 2z (z - a)$ 限制，即
>
> $$|y|\leqslant Y(x):=\sqrt{2z(z-a)}.$$
>
> 于是曲面 $\Sigma$ 在 xOy 面上的投影区域为
>
> $$D_{xy}=\left\{(x,y)\mid-a\leqslant x\leqslant a,-Y(x)\leqslant y\leqslant Y(x)\right\}.$$
>
> 面积元为
>
> $$\mathrm{d}S=\sqrt{1+z_{x}^{2}+z_{y}^{2}}\mathrm{d}x\mathrm{d}y.$$
>
> 由 $z=a+\sqrt{a^{2}-x^{2}}$，得
>
> $$z_{x}=\frac{-x}{\sqrt{a^{2}-x^{2}}},\qquad z_{y}=0,$$
>
> 所以
>
> $$\sqrt{1+z_{x}^{2}+z_{y}^{2}}=\sqrt{1+\frac{x^{2}}{a^{2}-x^{2}}}=\sqrt{\frac{a^{2}}{a^{2}-x^{2}}}=\frac{a}{\sqrt{a^{2}-x^{2}}}.$$
>
> 因此
>
> $$\begin{aligned}I&=\iint_{\Sigma}z\mathrm{d}S=\int_{-a}^{a}\int_{-Y(x)}^{Y(x)}z\cdot\frac{a}{\sqrt{a^{2}-x^{2}}}\mathrm{d}y\mathrm{d}x\\&=\int_{-a}^{a}\frac{2azY(x)}{\sqrt{a^{2}-x^{2}}}\mathrm{d}x.\end{aligned}$$
>
> 下面计算这个定积分. 令
>
> $$x=a\sin\psi,\qquad\psi\in\left[-\frac{\pi}{2},\frac{\pi}{2}\right],$$
>
> 则
>
> $$\mathrm{d}x=a\cos\psi\mathrm{d}\psi,\qquad\sqrt{a^{2}-x^{2}}=a\cos\psi,$$
>
> 且
>
> $$z=a+\sqrt{a^{2}-x^{2}}=a(1+\cos\psi),$$
>
> $$Y(x)=\sqrt{2z(z-a)}=\sqrt{2a(1+\cos\psi)\cdot a\cos\psi}=a\sqrt{2\cos\psi(1+\cos\psi)}.$$
>
> 代入 I 的表达式:
>
> $$\begin{aligned}I&=\int_{-\pi/2}^{\pi/2}\frac{2a\cdot a(1+\cos\psi)\cdot a\sqrt{2\cos\psi(1+\cos\psi)}}{a\cos\psi}\cdot a\cos\psi\mathrm{d}\psi\\&=2a^{3}\sqrt{2}\int_{-\pi/2}^{\pi/2}(1+\cos\psi)^{3/2}\sqrt{\cos\psi}\mathrm{d}\psi.\end{aligned}$$
>
> 被积函数关于 $\psi$ 为偶函数，故
>
> $$I=4a^{3}\sqrt{2}\int_{0}^{\pi/2}(1+\cos\psi)^{3/2}\sqrt{\cos\psi}\mathrm{d}\psi.$$
>
> 这与方法一得到的积分完全相同. 为完整起见, 再算一遍该积分. 令
>
> $$u=1+\cos\psi,$$
>
> 则
>
> $$\cos\psi=u-1,\qquad\mathrm{d}\psi=-\frac{\mathrm{d}u}{\sqrt{u(2-u)}},$$
>
> 且 $\psi:0\to\frac{\pi}{2}$ 对应 u:2 $\rightarrow$1. 于是
>
> $$\int_{0}^{\pi/2}(1+\cos\psi)^{3/2}\sqrt{\cos\psi}\mathrm{d}\psi=\int_{1}^{2}u\sqrt{\frac{u-1}{2-u}}\mathrm{d}u.$$
>
> 再令
>
> $$u-1=t^{2},\qquad t\in[0,1],$$
>
> 则
>
> $$u=1+t^{2},\qquad\mathrm{d}u=2t\mathrm{d}t,\qquad2-u=1-t^{2},$$
>
> 所以
>
> $$\int_{1}^{2}u\sqrt{\frac{u-1}{2-u}}\mathrm{d}u=\int_{0}^{1}(1+t^{2})\cdot\frac{t}{\sqrt{1-t^{2}}}\cdot2t\mathrm{d}t=2\int_{0}^{1}\frac{t^{2}+t^{4}}{\sqrt{1-t^{2}}}\mathrm{d}t.$$
>
> 利用
>
> $$\int_{0}^{1}\frac{t^{2}}{\sqrt{1-t^{2}}}\mathrm{d}t=\frac{\pi}{4},\qquad\int_{0}^{1}\frac{t^{4}}{\sqrt{1-t^{2}}}\mathrm{d}t=\frac{3\pi}{16},$$
>
> 得
>
> $$\int_{1}^{2}u\sqrt{\frac{u-1}{2-u}}\mathrm{d}u=2\left(\frac{\pi}{4}+\frac{3\pi}{16}\right)=\frac{7\pi}{8}.$$
>
> 因此
>
> $$I=4a^{3}\sqrt{2}\cdot\frac{7\pi}{8}=\frac{7\sqrt{2}}{2}\pi a^{3}.$$

**4.** (难度:★★★★) 设函数 $f(x)$ 连续, a, b, c 为常数, $\Sigma$ 是单位球面 $x^{2} + y^{2} + z^{2} = 1$, 求证:

$$\iint_{\Sigma}f(ax+by+cz)\mathrm{d}S=2\pi\int_{-1}^{1}f\left(\sqrt{a^{2}+b^{2}+c^{2}}u\right)\mathrm{d}u.$$

> [!answer]- 原书参考答案（A.7.2·第一类曲面积分 第 4 题，未逐题独立验算）
> **4.** 被积函数只依赖线性组合 $ax + by + cz$，先作正交变换把它变成一个坐标 u，再把球面按 u 分层、上下两个半球分别投影。记 $\delta = \sqrt{a^{2} + b^{2} + c^{2}}$。若 $\delta = 0$，两边都是 $4\pi f(0)$，结论成立。下面设 $\delta > 0$。
>
> 先作正交变换
>
> $$u=\frac{a x+b y+c z}{\delta},$$
>
> 并把 u 扩充为一张正交矩阵（即再取两个与 $\left(\frac{a}{\delta}, \frac{b}{\delta}, \frac{c}{\delta}\right)$ 正交的单位向量 v, w). 正交变换把单位球面变到单位球面, 且面积元素 dS 不变, 于是
>
> $$\iint_{\Sigma}f(ax+by+cz)\mathrm{d}S=\iint_{u^{2}+v^{2}+w^{2}=1}f(\delta u)\mathrm{d}S.$$
>
> 把球面按 u = t 分成上下两片 $w = \pm\sqrt{1-t^{2}-v^{2}}$，两片等值，于是
>
> $$\iint_{u^{2}+v^{2}+w^{2}=1}f(\delta u)\mathrm{d}S=2\int_{-1}^{1}\mathrm{d}t\int_{-\sqrt{1-t^{2}}}^{\sqrt{1-t^{2}}}\frac{f(\delta t)}{\sqrt{1-t^{2}-v^{2}}}\mathrm{d}v.$$
>
> 这里用了投影公式 $\mathrm{d}S=\frac{\mathrm{d}u\,\mathrm{d}v}{|w|}=\frac{\mathrm{d}u\,\mathrm{d}v}{\sqrt{1-u^{2}-v^{2}}}$。内层积分为
>
> $$\int_{-\sqrt{1-t^{2}}}^{\sqrt{1-t^{2}}}\frac{\mathrm{d}v}{\sqrt{1-t^{2}-v^{2}}}=\pi,$$
>
> 它不依赖t.所以
>
> $$\iint_{\Sigma}f(ax+by+cz)\mathrm{d}S=2\pi\int_{-1}^{1}f(\delta u)\mathrm{d}u.$$
>
> 这是泊松公式. 两个要点: 正交变换保持球面与面积元素; 按 u 分层后, 内层对 v 的积分恒为 $\pi$.

**5.** （难度：★★★★★）计算

$$I=\int_{0}^{\frac{\pi}{2}}\mathrm{d}\theta\int_{0}^{\frac{\pi}{2}}\frac{\sin\varphi\ln(2-\sin\varphi\cos\theta)}{2-2\sin\varphi\cos\theta+\sin^{2}\varphi\cos^{2}\theta}\mathrm{d}\varphi.$$

> [!answer]- 原书参考答案（A.7.2·第一类曲面积分 第 5 题，未逐题独立验算）
> **5.** 被积函数的样子提示这是球面第一卦限上的第一类曲面积分: $x = \sin \varphi \cos \theta$. 化成曲面积分后再投影到 xOy, 对 y 积分立刻得到一个常数. 把 $x = \sin \varphi \cos \theta$, $y = \sin \varphi \sin \theta$, $z = \cos \varphi$ 看成单位球面的参数, 则
>
> $$\mathrm{d}S=\sin\varphi\,\mathrm{d}\varphi\,\mathrm{d}\theta,\qquad x=\sin\varphi\cos\theta.$$
>
> 于是原式是第一卦限球面 $\Sigma$上的第一类曲面积分
>
> $$I=\iint_{\Sigma}\frac{\ln(2-x)}{2-2x+x^{2}}\mathrm{d}S.$$
>
> 把 $\Sigma$ 投影到 xOy 平面，投影区域为 $D: x^{2} + y^{2} \leqslant 1, x \geqslant 0, y \geqslant 0$，且
>
> $$\mathrm{d}S=\frac{\mathrm{d}x\mathrm{d}y}{\sqrt{1-x^{2}-y^{2}}},$$
>
> 所以
>
> $$I=\iint_{D}\frac{\ln(2-x)}{2-2x+x^{2}}\cdot\frac{\mathrm{d}x\mathrm{d}y}{\sqrt{1-x^{2}-y^{2}}}.$$
>
> 先对 y 积分 $(0 \leqslant y \leqslant \sqrt{1 - x^{2}})$ :
>
> $$\int_{0}^{\sqrt{1-x^{2}}}\frac{\mathrm{d}y}{\sqrt{1-x^{2}-y^{2}}}=\left[\arcsin\frac{y}{\sqrt{1-x^{2}}}\right]_{0}^{\sqrt{1-x^{2}}}=\frac{\pi}{2},$$
>
> 于是
>
> $$I=\frac{\pi}{2}\int_{0}^{1}\frac{\ln(2-x)}{2-2x+x^{2}}\mathrm{d}x=\frac{\pi}{2}\int_{0}^{1}\frac{\ln(2-x)}{1+(1-x)^{2}}\mathrm{d}x.$$
>
> 令u=1-x,则
>
> $$I=\frac{\pi}{2}\int_{0}^{1}\frac{\ln(1+u)}{1+u^{2}}\mathrm{d}u.$$
>
> 再令 $u = \tan t \, (0 \leqslant t \leqslant \frac{\pi}{4})$，得
>
> $$\int_{0}^{1}\frac{\ln(1+u)}{1+u^{2}}\mathrm{d}u=\int_{0}^{\pi/4}\ln(1+\tan t)\mathrm{d}t.$$
>
> 用 $t \rightarrow \frac{\pi}{4} - t$ 把上式记为 A，则
>
> $$A=\int_{0}^{\pi/4}\ln\frac{2}{1+\tan t}\mathrm{d}t=\frac{\pi}{4}\ln2-A\implies A=\frac{\pi}{8}\ln2.$$
>
> 所以
>
> $$I=\frac{\pi}{2}\cdot\frac{\pi}{8}\ln2=\frac{\pi^{2}\ln2}{16}.$$
>
> 两步都是「先认出球坐标、再换回熟悉的积分」：先化成第一类曲面积分，投影后对 $y$ 积分得到常数 $\frac{\pi}{2}$，最后用 $\tan t$ 换元与对称性求出 $\ln(1+\tan t)$ 的积分.

**6.** (难度:★★★★★) 计算

$$I=\int_{0}^{2\pi}\mathrm{d}\varphi\int_{0}^{\pi}\sin\theta e^{\sin\theta(\cos\varphi-\sin\varphi)}\mathrm{d}\theta.$$

> [!answer]- 原书参考答案（A.7.2·第一类曲面积分 第 6 题，未逐题独立验算）
> **6.** 指数上的 $\sin\theta(\cos\varphi-\sin\varphi)$ 就是球面上坐标 x-y，所以把原式看成单位球面上的 $\iint\limits_{D}e^{x-y}\,dS$，再用正交变换把 x-y 变成一个坐标。用单位球面的参数
>
> $$x=\sin\theta\cos\varphi,\quad y=\sin\theta\sin\varphi,\quad z=\cos\theta,\qquad\mathrm{d}S=\sin\theta\mathrm{d}\theta\mathrm{d}\varphi,$$
>
> 则
>
> $$\sin\theta(\cos\varphi-\sin\varphi)=x-y,\qquad\theta\in[0,\pi],\varphi\in[0,2\pi],$$
>
> 所以原式就是
>
> $$I=\iint_{x^{2}+y^{2}+z^{2}=1}\mathrm{e}^{x-y}\mathrm{d}S.$$
>
> 取正交变换使
>
> $$u=\frac{x-y}{\sqrt{2}},$$
>
> 并把 u 扩充为完整的正交变换. 正交变换保持单位球与 dS, 于是
>
> $$x-y=\sqrt{2}u,\qquad I=\iint_{u^{2}+v^{2}+w^{2}=1}\mathrm{e}^{\sqrt{2}u}\mathrm{d}S.$$
>
> 把球面按 u = t 分成上下两片，则
>
> $$I=2\int_{-1}^{1}\mathrm{d}t\int_{-\sqrt{1-t^{2}}}^{\sqrt{1-t^{2}}}\frac{\mathrm{e}^{\sqrt{2}t}}{\sqrt{1-t^{2}-v^{2}}}\mathrm{d}v=2\pi\int_{-1}^{1}\mathrm{e}^{\sqrt{2}t}\mathrm{d}t,$$
>
> 其中内层积分 $\int_{-\sqrt{1-t^{2}}}^{\sqrt{1-t^{2}}}\frac{dv}{\sqrt{1-t^{2}-v^{2}}}=\pi.$ 计算得
>
> $$I=2\pi\cdot\frac{\mathbf{e}^{\sqrt{2}}-\mathbf{e}^{-\sqrt{2}}}{\sqrt{2}}=\sqrt{2}\pi\left(\mathbf{e}^{\sqrt{2}}-\mathbf{e}^{-\sqrt{2}}\right).$$
>
> 认出「 $\sin\theta(\cos\varphi-\sin\varphi)=x-y$」是第一步；之后就是泊松公式的直接应用。

## 7.3 第二类积分

### 7.3.1 第二类曲线积分

第二类曲线积分,除了参数法换元计算,还要学会应用格林公式或斯托克斯公式进行转化计算,同时要注意积分与路径无关的考察方向.

**1.** (难度:★★) 计算 $I = \int_{L} -y \, \mathrm{d}x + x \, \mathrm{d}y$, L: 沿曲线 $y = \sqrt{2x - x^{2}}$ 从 A(2,0) 到 O(0,0).

> [!answer]- 原书参考答案（A.7.3·第二类曲线积分 第 1 题，未逐题独立验算）
> **1.** 曲线即 $(x-1)^{2}+y^{2}=1$ 的上半圆. 取参数
>
> $$x=1+\cos t,\qquad y=\sin t,\qquad0\leqslant t\leqslant\pi,$$
>
> 当 t=0 时得 $A(2,0)$，当 $t=\pi$ 时得 $O(0,0)$，方向一致。于是
>
> $$\mathrm{d}x=-\sin t\mathrm{d}t,\qquad\mathrm{d}y=\cos t\mathrm{d}t,$$
>
> 而被积表达式化为
>
> $$-y\mathrm{d}x+x\mathrm{d}y=-\sin t\cdot(-\sin t)\mathrm{d}t+\left(1+\cos t\right)\cos t\mathrm{d}t=1+\cos t.$$
>
> $$I=\int_{0}^{\pi}(1+\cos t)\mathrm{d}t=\left[t+\sin t\right]_{0}^{\pi}=\pi.$$
>
> 所以

**2.** (难度:★★★) 设 L 为平面区域 $D = \{(x,y) \mid 0 \leqslant x \leqslant \pi, 0 \leqslant y \leqslant \pi\}$ 的正向边界曲线, 试证明:

(1)

$$\oint_{L}x e^{\sin y}\mathrm{d}y-y e^{-\sin x}\mathrm{d}x=\oint_{L}x e^{-\sin y}\mathrm{d}y-y e^{\sin x}\mathrm{d}x;$$

(2)

$$\oint_{L}xe^{\sin y}\mathrm{d}y-ye^{-\sin x}\mathrm{d}x\leqslant\frac{5}{2}\pi^{2}.$$

> [!answer]- 原书参考答案（A.7.3·第二类曲线积分 第 2 题，未逐题独立验算）
> **2.** 两个环路积分都用格林公式化成同一个二重积分；(2) 的关键是把 $e^{\sin y} + e^{-\sin y}$ 与 $2 + \sin^{2} y$ 作比较. (1) 对第一个积分
>
> $$I_{1}=\oint_{L}x\mathbf{e}^{\sin y}\mathrm{d}y-y\mathbf{e}^{-\sin x}\mathrm{d}x,$$
>
> 取 $P = -ye^{-\sin x}$， $Q = xe^{\sin y}$。则
>
> $$\frac{\partial Q}{\partial x}=\mathrm{e}^{\sin y},\qquad\frac{\partial P}{\partial y}=-\mathrm{e}^{-\sin x},$$
>
> 由格林公式
>
> $$I_{1}=\iint_{D}\left(\mathbf{e}^{\sin y}+\mathbf{e}^{-\sin x}\right)\mathrm{d}\sigma.$$
>
> 对第二个积分, 取 $P = -ye^{\sin x}$, $Q = xe^{-\sin y}$, 则
>
> $$\frac{\partial Q}{\partial x}=\mathbf{e}^{-\sin y},\qquad\frac{\partial P}{\partial y}=-\mathbf{e}^{\sin x},$$
>
> 于是
>
> $$I_{2}=\iint_{D}\left(\mathbf{e}^{-\sin y}+\mathbf{e}^{\sin x}\right)\mathrm{d}\sigma.$$
>
> 正方形 $D = \{0 \leqslant x \leqslant \pi, 0 \leqslant y \leqslant \pi\}$ 关于直线 y = x 对称，把 x 与 y 互换得
>
> $$\iint_{D}\mathrm{e}^{\sin y}\mathrm{d}\sigma=\iint_{D}\mathrm{e}^{\sin x}\mathrm{d}\sigma,\qquad\iint_{D}\mathrm{e}^{-\sin x}\mathrm{d}\sigma=\iint_{D}\mathrm{e}^{-\sin y}\mathrm{d}\sigma,$$
>
> 所以 $I_{1}=I_{2}$，即(1)成立.
>
> (2) 由上面的对称性，
>
> $$I_{1}=\iint_{D}\left(\mathrm{e}^{\sin y}+\mathrm{e}^{-\sin y}\right)\mathrm{d}\sigma=\pi\int_{0}^{\pi}\left(\mathrm{e}^{\sin y}+\mathrm{e}^{-\sin y}\right)\mathrm{d}y.$$
>
> 对任意实数t，
>
> $$\mathbf{e}^{t}+\mathbf{e}^{-t}=2\left(1+\frac{t^{2}}{2!}+\frac{t^{4}}{4!}+\cdots\right)\geqslant2+t^{2},$$
>
> 取 $t = \sin y$ 得
>
> $$\begin{aligned}e^{\sin y}+e^{-\sin y}\geqslant2+\sin^{2}y.\end{aligned}$$
>
> 于是
>
> $$I_{1}\geqslant\pi\int_{0}^{\pi}\left(2+\sin^{2}y\right)\mathrm{d}y=\pi\left(2\pi+\frac{\pi}{2}\right)=\frac{5}{2}\pi^{2}.$$
>
> (1) 是把两条曲线上的积分都化到同一个二重积分；(2) 的估计只用了一个初等不等式 $\mathrm{e}^{t} + \mathrm{e}^{-t} \geqslant 2 + t^{2}$，最后 $\int_{0}^{\pi} \sin^{2} y \, \mathrm{d}y = \frac{\pi}{2}$ 刚好凑出 $\frac{5}{2}\pi$.

**3.** (难度:★★★) 计算 $I = \int_{L} (2x + \sin y) \, \mathrm{d}x + x \cos y \, \mathrm{d}y$, L 为从 $(0,0)$ 到 $\left(2, \frac{\pi}{2}\right)$ 的曲线 $y = \frac{\pi}{8}x^{2}$.

> [!answer]- 原书参考答案（A.7.3·第二类曲线积分 第 3 题，未逐题独立验算）
> **3.** 先检验与路径无关的条件, 若成立就找势函数, 一步代端点. 记
>
> $$P=2x+\sin y,\qquad Q=x\cos y.$$
>
> 则
>
> $$\frac{\partial P}{\partial y}=\cos y=\frac{\partial Q}{\partial x},$$
>
> 且 P, Q 在整个平面上连续可偏导, 所以积分与路径无关, 可以找势函数 F(x, y): 由
>
> $$\frac{\partial F}{\partial x}=2x+\sin y$$
>
> 得 $F(x,y)=x^{2}+x\sin y+g(y)$; 再由
>
> $$\frac{\partial F}{\partial y}=x\cos y+g^{\prime}(y)=x\cos y$$
>
> 得 $g'(y) = 0$，取 $g(y) \equiv 0$。因此
>
> $$I=F\left(2,\frac{\pi}{2}\right)-F(0,0)=\left(4+2\sin\frac{\pi}{2}\right)-0=6.$$
>
> 看到 L 是弯的曲线而积分与路径无关, 就不要参数化 L, 直接换折线或找势函数.

**4.** (难度:★★★★) 计算 $I = \int_{L} \frac{x \, \mathrm{d}y - y \, \mathrm{d}x}{4x^{2} + y^{2}}$，其中 L 取点 A(-1,0) 沿 $y = -\sqrt{1 - x^{2}}$ 至点 B(1,0) 再沿 $y^{2} = 2(1 - x)$ 至点 C(-1,2) 的路径.

> [!answer]- 原书参考答案（A.7.3·第二类曲线积分 第 4 题，未逐题独立验算）
> **4.** 被积函数在原点不可导，不能直接补线用格林，要「补线 + 挖洞」，把绕原点的闭路换成一个小椭圆。记
>
> $$P=\frac{-y}{4x^{2}+y^{2}},\qquad Q=\frac{x}{4x^{2}+y^{2}}.$$
>
> 在原点以外的点，
>
> $$\frac{\partial P}{\partial y}=\frac{y^{2}-4x^{2}}{(4x^{2}+y^{2})^{2}}=\frac{\partial Q}{\partial x},$$
>
> 但它只在 $(x,y)\neq(0,0)$有意义.
>
> 把 L 与两条直线段补成闭曲线 Γ: L 从 A(-1,0) 沿下半单位圆到 B(1,0)，再沿 $y^{2}=2(1-x)$ 到 C(-1,2)，最后沿 x=-1 回到 A. 这条闭曲线内部包含原点. 在原点外挖去一个小椭圆 $l_{\varepsilon}$: $4x^{2}+y^{2}=\varepsilon^{2}$ (取逆时针)，由格林公式
>
> $$\oint_{\Gamma}\frac{x\mathrm{d}y-y\mathrm{d}x}{4x^{2}+y^{2}}=\oint_{l_{\varepsilon}}\frac{x\mathrm{d}y-y\mathrm{d}x}{4x^{2}+y^{2}}.$$
>
> 在小椭圆上参数化
>
> $$x=\frac{\varepsilon}{2}\cos t,\qquad y=\varepsilon\sin t,\qquad0\leqslant t\leqslant2\pi,$$
>
> 则 $4x^{2}+y^{2}=\varepsilon^{2}$，且
>
> $$x\mathrm{d}y-y\mathrm{d}x=\frac{\varepsilon^{2}}{2}\cos^{2}t\mathrm{d}t+\frac{\varepsilon^{2}}{2}\sin^{2}t\mathrm{d}t=\frac{\varepsilon^{2}}{2}\mathrm{d}t.$$
>
> 所以
>
> $$\oint_{l_{\varepsilon}}\frac{x\mathrm{d}y-y\mathrm{d}x}{4x^{2}+y^{2}}=\int_{0}^{2\pi}\frac{1}{2}\mathrm{d}t=\pi,$$
>
> 即 $I=\pi$ 。原点处的奇点必须用「挖洞」处理：把小椭圆按逆时针取，方向对了结果就是 $+π$ 。

**5.** (难度:★★★) 计算积分 $I = \oint_{\Gamma} (\sqrt{3}y - x) \, dx - 5z \, dz$，其中曲线 $\Gamma: \begin{cases} x^2 + y^2 + z^2 = 8, \\ x^2 + y^2 = 2z, \end{cases}$

其方向为从 z 轴正方向往坐标原点看去取逆时针方向.

> [!answer]- 原书参考答案（A.7.3·第二类曲线积分 第 5 题，未逐题独立验算）
> **5.** 两个方程里都有 $x^{2} + y^{2}$，先解出 z，把三维问题压成一个大圆上的平面问题。由 $x^{2} + y^{2} = 2z$ 与 $x^{2} + y^{2} + z^{2} = 8$ 得
>
> $$2z+z^{2}=8\implies z^{2}+2z-8=0\implies z=2\quad(z>0).$$
>
> 所以 $\Gamma$ 就是平面 z=2 上的圆 $x^{2}+y^{2}=4$，且 z 为常数、dz=0。于是
>
> $$I=\oint_{\Gamma}\left(\sqrt{3}y-x\right)\mathrm{d}x.$$
>
> 用格林公式 (区域 $x^2 + y^2 \leq 4$, 正向), 取 $P = \sqrt{3}y - x$, $Q = 0$:
>
> $$I=\iint_{x^{2}+y^{2}\leqslant4}\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}\sigma=\iint_{x^{2}+y^{2}\leqslant4}(-\sqrt{3})\mathrm{d}\sigma=-\sqrt{3}\cdot4\pi=-4\sqrt{3}\pi.$$
>
> 空间曲线积分里, 先看有没有变量被两个方程「锁死」; 这里 $z \equiv 2$, 积分立刻降为平面上的格林公式.

**6.** (难度：★★★★) 设曲线 $\Gamma$ 为 $x^{2} + y^{2} + z^{2} = 1$, $x + z = 1$, $x \geqslant 0$, $y \geqslant 0$, $z \geqslant 0$ 上从点 $A(1,0,0)$ 到点 $B(0,0,1)$ 的一段，求曲线积分：

$$I=\int_{\Gamma}y\mathrm{d}x+z\mathrm{d}y+x\mathrm{d}z.$$

> [!answer]- 原书参考答案（A.7.3·第二类曲线积分 第 6 题，未逐题独立验算）
> **6.** 曲线是球面与平面的交线，消去z后得到一个椭圆，参数化后直接代入。由 $x+z=1$得z=1-x，代入球面方程：
>
> $$x^{2}+y^{2}+(1-x)^{2}=1\implies2\left(x-\frac{1}{2}\right)^{2}+y^{2}=\frac{1}{2},$$
>
> 即
>
> $$\frac{\left(x-\frac{1}{2}\right)^{2}}{\frac{1}{4}}+\frac{y^{2}}{\frac{1}{2}}=1.$$
>
> 取参数
>
> $$x=\frac{1}{2}+\frac{1}{2}\cos t,\qquad y=\frac{1}{\sqrt{2}}\sin t,\qquad z=\frac{1}{2}-\frac{1}{2}\cos t,\qquad0\leqslant t\leqslant\pi,$$
>
> 则 t=0 对应 $A(1,0,0)$, $t=\pi$ 对应 $B(0,0,1)$，方向正好是从 A 到 B. 此时
>
> $$\mathrm{d}x=-\frac{1}{2}\sin t\mathrm{d}t,\qquad\mathrm{d}y=\frac{1}{\sqrt{2}}\cos t\mathrm{d}t,\qquad\mathrm{d}z=\frac{1}{2}\sin t\mathrm{d}t.$$
>
> 于是
>
> $$I=\int_{0}^{\pi}(y\mathrm{d}x+z\mathrm{d}y+x\mathrm{d}z)$$
>
> $$=\int_{0}^{\pi}\left[-\frac{1}{2\sqrt{2}}\sin^{2}t+\frac{1}{2\sqrt{2}}\cos t\left(1-\cos t\right)+\frac{1}{4}\left(1+\cos t\right)\sin t\right]\mathrm{d}t.$$
>
> 利用
>
> $$\int_{0}^{\pi}\sin^{2}t\mathrm{d}t=\frac{\pi}{2},\int_{0}^{\pi}\cos t\mathrm{d}t=0,\int_{0}^{\pi}\cos^{2}t\mathrm{d}t=\frac{\pi}{2},\int_{0}^{\pi}(1+\cos t)\sin t\mathrm{d}t=2,$$
>
> 得
>
> $$I=-\frac{1}{2\sqrt{2}}\cdot\frac{\pi}{2}+\frac{1}{2\sqrt{2}}\left(0-\frac{\pi}{2}\right)+\frac{1}{4}\cdot2=-\frac{\pi}{2\sqrt{2}}+\frac{1}{2}=\frac{1}{2}-\frac{\sqrt{2}\pi}{4}.$$
>
> 这类题不要用斯托克斯: 要补的线太多, 直接参数化最快. 参数 t 的上下限必须与「从 A 到 B」的方向一致.

**7.** (难度：★★★★) 已知 $\Sigma$ 为曲面 $4x^{2} + y^{2} + z^{2} = 1 (x \geqslant 0, y \geqslant 0, z \geqslant 0)$ 的上侧, $\Gamma$ 为 $\Sigma$ 的边界曲线, 其正向与 $\Sigma$ 的法向量符合右手螺旋法则, 计算曲线积分

$$I=\int_{\Gamma}(yz^{2}-\cos z)\mathrm{d}x+2xz^{2}\mathrm{d}y+\left(2xyz+x\sin z\right)\mathrm{d}z.$$

> [!answer]- 原书参考答案（A.7.3·第二类曲线积分 第 7 题，未逐题独立验算）
> **7.** 闭曲线上的第二类曲线积分，用斯托克斯公式转成曲面积分；行列式里的三个偏导算完后只剩两项，再投影。记
>
> $$P=y z^{2}-\cos z,\qquad Q=2x z^{2},\qquad R=2x y z+x\sin z.$$
>
> 由斯托克斯公式 ( $\Gamma$ 的正向与 $\Sigma$ 的法向量符合右手螺旋法则)
>
> $$I=\iint_{\Sigma}\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}\right)\mathrm{d}y\mathrm{d}z+\left(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x}\right)\mathrm{d}z\mathrm{d}x+\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}x\mathrm{d}y.$$
>
> 逐项计算：
>
> $$\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}=2xz-4xz=-2xz,$$
>
> $$\begin{aligned}\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x}&=(2yz+\sin z)-(2yz+\sin z)=0,\\\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}&=2z^{2}-z^{2}=z^{2}.\end{aligned}$$
>
> 所以
>
> $$I=\iint_{\Sigma}-2xz\mathrm{d}y\mathrm{d}z+z^{2}\mathrm{d}x\mathrm{d}y.$$
>
> $\Sigma$ 是椭球面 $4x^{2}+y^{2}+z^{2}=1$ 在第一卦限的部分, 取上侧, 可看成 $z=\sqrt{1-4x^{2}-y^{2}}$, 其投影区域为
>
> $$D:4x^{2}+y^{2}\leqslant1,\qquad x\geqslant0,y\geqslant0.$$
>
> 上侧时
>
> $$\mathrm{d}y\mathrm{d}z=-z_{x}\mathrm{d}x\mathrm{d}y=\frac{4x}{z}\mathrm{d}x\mathrm{d}y,\qquad\mathrm{d}x\mathrm{d}y=\mathrm{d}x\mathrm{d}y,$$
>
> 其中 $z = \sqrt{1 - 4x^{2} - y^{2}}$. 代入得
>
> $$I=\iint_{D}(-2xz)\cdot\frac{4x}{z}\mathrm{d}x\mathrm{d}y+\iint_{D}z^{2}\mathrm{d}x\mathrm{d}y=\iint_{D}\left(1-12x^{2}-y^{2}\right)\mathrm{d}x\mathrm{d}y.$$
>
> 作换元 u = 2x, v = y, 则 $\mathrm{d}x\,\mathrm{d}y = \frac{1}{2}\mathrm{d}u\,\mathrm{d}v$，区域变为单位圆在第一象限的部分。于是
>
> $$\iint_{D}1\mathrm{d}x\mathrm{d}y=\frac{\pi}{8},\qquad\iint_{D}x^{2}\mathrm{d}x\mathrm{d}y=\frac{\pi}{128},\qquad\iint_{D}y^{2}\mathrm{d}x\mathrm{d}y=\frac{\pi}{32}.$$
>
> 所以
>
> $$I=\frac{\pi}{8}-12\cdot\frac{\pi}{128}-\frac{\pi}{32}=\frac{4\pi}{32}-\frac{3\pi}{32}-\frac{\pi}{32}=0.$$
>
> 斯托克斯公式算完后常剩两项,再按「上侧投影」写成 $z_{x},z_{y}$的形式;本题数字是配好的,结果为0.

### 7.3.2 第二类曲面积分

可通过高斯定理转三重积分，或与第一类曲面积分进行相应转换，计算思路相对固定，但要注意多加练习.

**1.** (难度:★★) 计算 $I = \iint_{\Sigma} x \, \mathrm{d}y \, \mathrm{d}z + y \, \mathrm{d}z \, \mathrm{d}x + z \, \mathrm{d}x \, \mathrm{d}y$，其中 $\Sigma$ 取曲面 $z = x^{2} + y^{2}$ 在第一卦限对应于 $0 \leqslant z \leqslant 1$ 部分的下侧.

> [!answer]- 原书参考答案（A.7.3·第二类曲面积分 第 1 题，未逐题独立验算）
> **1.** 曲面 $z = x^{2} + y^{2}$ 写成 $F(x, y, z) = x^{2} + y^{2} - z = 0$，则
>
> $$\left(\frac{\partial F}{\partial x},\frac{\partial F}{\partial y},\frac{\partial F}{\partial z}\right)=(2x,2y,-1),\qquad|\vec{n}|=\sqrt{4x^{2}+4y^{2}+1}.$$
>
> 这个法向量指向「上侧」的反方向？逐项看：它的 z 分量为 -1 < 0，也就是指向下方，正是题目要的下侧。于是所取那一侧的方向余弦为
>
> $$\cos\alpha=\frac{2x}{\sqrt{4x^{2}+4y^{2}+1}},\qquad\cos\beta=\frac{2y}{\sqrt{4x^{2}+4y^{2}+1}},$$
>
> $$\cos\gamma=\frac{-1}{\sqrt{4x^{2}+4y^{2}+1}}.$$
>
> 把积分化为第一类：
>
> $$I=\iint_{\Sigma}\left(x\cos\alpha+y\cos\beta+z\cos\gamma\right)\mathrm{d}S=\iint_{\Sigma}\frac{2x^{2}+2y^{2}-z}{\sqrt{4x^{2}+4y^{2}+1}}\mathrm{d}S.$$
>
> 代入曲面方程 $z = x^{2} + y^{2}$，分子化为
>
> $$2(x^{2}+y^{2})-z=z,$$
>
> 即
>
> $$I=\iint_{\Sigma}\frac{z}{\sqrt{4x^{2}+4y^{2}+1}}\mathrm{d}S.$$
>
> 再用投影法: $z = z(x, y)$ 的投影区域为
>
> $$D=\{(x,y)\mid x\geqslant0,y\geqslant0,x^{2}+y^{2}\leqslant1\},$$
>
> 且
>
> $$\mathrm{d}S=\sqrt{1+z_{x}^{2}+z_{y}^{2}}\mathrm{d}x\mathrm{d}y=\sqrt{4x^{2}+4y^{2}+1}\mathrm{d}x\mathrm{d}y,$$
>
> 两个根号恰好约掉：
>
> $$I=\iint_{D}z\mathrm{d}x\mathrm{d}y=\iint_{D}(x^{2}+y^{2})\mathrm{d}x\mathrm{d}y.$$
>
> 用极坐标：
>
> $$I=\int_{0}^{\pi/2}\int_{0}^{1}\rho^{2}\cdot\rho\mathrm{d}\rho\mathrm{d}\theta=\frac{\pi}{2}\cdot\frac{1}{4}=\frac{\pi}{8}.$$

**2.** (难度：★★★★) 设 $\Sigma$ 为曲面 $z = 1 - x^{2} - 2y^{2} (z \geqslant 0)$ 的上侧, 且函数 $f(u)$ 连续, 计算曲面积分

$$I=\iint_{\Sigma}2y^{2}f(x+y)\mathrm{d}y\mathrm{d}z+x y\left[\frac{1}{4}-f(x-y)\right]\mathrm{d}z\mathrm{d}x+(z-x y^{2})\mathrm{d}x\mathrm{d}y.$$

> [!answer]- 原书参考答案（A.7.3·第二类曲面积分 第 2 题，未逐题独立验算）
> **2.** f 不可用高斯定理 (只连续), 只能化成第一类曲面积分再投影; 投影后含 $f(x+y)$、 $f(x-y)$ 的项关于 y 是奇函数, 自动消失. 曲面 $z = 1 - x^{2} - 2y^{2} (z \geqslant 0)$ 的投影区域为
>
> $$D:\ x^{2}+2y^{2}\leq1,$$
>
> 且
>
> $$z_{x}=-2x,\qquad z_{y}=-4y.$$
>
> 取上侧时
>
> $$\mathrm{d}y\mathrm{d}z=-z_{x}\mathrm{d}x\mathrm{d}y=2x\mathrm{d}x\mathrm{d}y,$$
>
> $$\mathrm{d}z\mathrm{d}x=-z_{y}\mathrm{d}x\mathrm{d}y=4y\mathrm{d}x\mathrm{d}y,\qquad\mathrm{d}x\mathrm{d}y=\mathrm{d}x\mathrm{d}y.$$
>
> 代入被积函数并整理：
>
> $$\begin{aligned}I=\iint_{D}\left\{2y^{2}f(x+y)\cdot2x+xy\left[\frac{1}{4}-f(x-y)\right]\cdot4y\right.\\ \left.+\left(1-x^{2}-2y^{2}-xy^{2}\right)\right\}\mathrm{d}x\mathrm{d}y,\end{aligned}$$
>
> 即
>
> $$I=\iint_{D}\Big\{4xy^{2}\left[f(x+y)-f(x-y)\right]+1-x^{2}-2y^{2}\Big\}\mathrm{d}x\mathrm{d}y.$$
>
> 区域 D 关于 x 轴对称, 当 $y \to -y$ 时
>
> $$4xy^{2}\left[f(x+y)-f(x-y)\right]\longrightarrow4xy^{2}\left[f(x-y)-f(x+y)\right],$$
>
> 即第一项关于 y 是奇函数，它在 D 上的积分为 0。所以
>
> $$I=\iint_{D}\left(1-x^{2}-2y^{2}\right)\mathrm{d}x\mathrm{d}y.$$
>
> D 是半轴为 a = 1, $b = \frac{1}{\sqrt{2}}$ 的椭圆，由
>
> $$\iint_{D}1\mathrm{d}x\mathrm{d}y=\pi ab=\frac{\pi}{\sqrt{2}},\iint_{D}x^{2}\mathrm{d}x\mathrm{d}y=\frac{\pi}{4\sqrt{2}},\iint_{D}y^{2}\mathrm{d}x\mathrm{d}y=\frac{\pi}{8\sqrt{2}},$$
>
> 得
>
> $$I=\frac{\pi}{\sqrt{2}}-\frac{\pi}{4\sqrt{2}}-2\cdot\frac{\pi}{8\sqrt{2}}=\frac{\pi}{\sqrt{2}}-\frac{\pi}{4\sqrt{2}}-\frac{\pi}{4\sqrt{2}}=\frac{\pi}{2\sqrt{2}}=\frac{\sqrt{2}\pi}{4}.$$
>
> f 只连续时不能高斯；转第一类后，含 $f(x+y)$、 $f(x-y)$ 的两项一个正号一个负号，被 $y \to -y$ 的对称性消掉，这是本题的设计。合并同类项时注意 $xy^{2}$ 项与 $-xy^{2}$ 项恰好抵消。

**3.** （难度：★★★★）对于四次齐次函数

$$f(x,y,z)=a_{1}x^{4}+a_{2}y^{4}+a_{3}z^{4}+3a_{4}x^{2}y^{2}+3a_{5}y^{2}z^{2}+3a_{6}x^{2}z^{2},$$

计算曲面积分 $\iint_{\Sigma} f(x,y,z) \, \mathrm{d}S$，其中 $\Sigma: x^2 + y^2 + z^2 = 1$.

> [!answer]- 原书参考答案（A.7.3·第二类曲面积分 第 3 题，未逐题独立验算）
> **3.** $f(x,y,z)$ 是四次齐次函数，由欧拉公式 $x\frac{\partial f}{\partial x}+y\frac{\partial f}{\partial y}+z\frac{\partial f}{\partial z}=4f(x,y,z)$; 又球面上 $\cos\alpha=x$ 等，于是可以把曲面积分转成第二类积分再用高斯定理. $f(x,y,z)$ 是四次齐次函数，由欧拉公式
>
> $$x\frac{\partial f}{\partial x}+y\frac{\partial f}{\partial y}+z\frac{\partial f}{\partial z}=4f(x,y,z).$$
>
> 在单位球面上 $\cos\alpha=x,\cos\beta=y,\cos\gamma=z$ , 所以
>
> $$\iint_{\Sigma}f(x,y,z)\mathrm{d}S=\frac{1}{4}\iint_{\Sigma}\frac{\partial f}{\partial x}\mathrm{d}y\mathrm{d}z+\frac{\partial f}{\partial y}\mathrm{d}z\mathrm{d}x+\frac{\partial f}{\partial z}\mathrm{d}x\mathrm{d}y.$$
>
> 用高斯定理 (区域为单位球):
>
> $$\iint_{\Sigma}f(x,y,z)\mathrm{d}S=\frac{1}{4}\iiint_{\Omega}\left(\frac{\partial^{2}f}{\partial x^{2}}+\frac{\partial^{2}f}{\partial y^{2}}+\frac{\partial^{2}f}{\partial z^{2}}\right)\mathrm{d}V.$$
>
> 写出二阶偏导：
>
> $$\frac{\partial^{2}f}{\partial x^{2}}=12a_{1}x^{2}+6a_{4}y^{2}+6a_{6}z^{2},$$
>
> $$\frac{\partial^{2}f}{\partial y^{2}}=12a_{2}y^{2}+6a_{4}x^{2}+6a_{5}z^{2},\qquad\frac{\partial^{2}f}{\partial z^{2}}=12a_{3}z^{2}+6a_{5}y^{2}+6a_{6}x^{2}.$$
>
> 三者相加，按 $x^{2},y^{2},z^{2}$归并：
>
> $$12(a_{1}+a_{2}+a_{3})+12(a_{4}+a_{5}+a_{6})$$
>
> 为系数之和. 又
>
> $$\iiint_{\Omega}x^{2}\mathrm{d}V=\iiint_{\Omega}y^{2}\mathrm{d}V=\iiint_{\Omega}z^{2}\mathrm{d}V=\frac{4\pi}{15},$$
>
> 所以
>
> $$\begin{aligned}\iint_{\Sigma}f(x,y,z)\mathrm{d}S&=\frac{1}{4}\cdot\frac{4\pi}{15}\cdot12(a_{1}+a_{2}+a_{3}+a_{4}+a_{5}+a_{6})\\&=\frac{4\pi}{5}(a_{1}+a_{2}+a_{3}+a_{4}+a_{5}+a_{6}).\end{aligned}$$
>
> 两步都要用上: 欧拉公式把 $f(x, y, z)$ 换成 $\frac{1}{4}(xf_x + yf_y + zf_z)$，再把 $\cos \alpha = x$ 代入转成第二类积分; 最后高斯定理把问题变成 「$\iiint_{\Omega}x^2\,\mathrm{d}V$」。

**4.** （难度：★★★★）计算

$$I=\iint_{\Sigma}\frac{\mathrm{d}y\,\mathrm{d}z}{\cos^{2}x}+\frac{\mathrm{d}z\,\mathrm{d}x}{\cos^{2}y}+\frac{\mathrm{d}x\,\mathrm{d}y}{\cos^{2}z},$$

其中 $\Sigma$ 取曲面 $z = \sqrt{1 - x^{2} - y^{2}}$ 的上侧.

> [!answer]- 原书参考答案（A.7.3·第二类曲面积分 第 4 题，未逐题独立验算）
> **4.** 先把第二类化成第一类：上半球面的外法向就是 $(x, y, z)$；再用对称性把前两项消掉，只剩第三项，最后投影加极坐标。 $\Sigma$ 是上半球面 $z = \sqrt{1 - x^{2} - y^{2}}$ 的上侧，其外法向的单位方向余弦为
>
> $$\cos\alpha=x,\qquad\cos\beta=y,\qquad\cos\gamma=z.$$
>
> 于是
>
> $$I=\iint_{\Sigma}\left(\frac{x}{\cos^{2}x}+\frac{y}{\cos^{2}y}+\frac{z}{\cos^{2}z}\right)\mathrm{d}S.$$
>
> 上半球面关于 yOz 平面对称, 而 $\frac{x}{\cos^{2}x}$ 关于 x 是奇函数, 故第一项积分为 0; 同理第二项积分也为 0. 于是
>
> $$I=\iint_{\Sigma}\frac{z}{\cos^{2}z}\mathrm{d}S.$$
>
> 把 $\Sigma$ 投影到 xOy 平面, 投影区域为单位圆 D, 且 $\mathrm{d}S=\frac{\mathrm{d}x\,\mathrm{d}y}{z}$, 所以
>
> $$I=\iint_{D}\frac{1}{\cos^{2}z}\mathrm{d}x\mathrm{d}y,\qquad z=\sqrt{1-x^{2}-y^{2}}.$$
>
> 用极坐标 $x = r \cos \theta$, $y = r \sin \theta$:
>
> $$I=\int_{0}^{2\pi}\mathrm{d}\theta\int_{0}^{1}\frac{r}{\cos^{2}\sqrt{1-r^{2}}}\mathrm{d}r=2\pi\int_{0}^{1}\frac{r}{\cos^{2}\sqrt{1-r^{2}}}\mathrm{d}r.$$
>
> 令 $u = \sqrt{1 - r^2}$，则 $r \, dr = -u \, du$，且 $r: 0 \to 1$ 对应 $u: 1 \to 0$：
>
> $$I=2\pi\int_{0}^{1}\frac{u}{\cos^{2}u}\mathrm{d}u.$$
>
> 由分部积分
>
> $$\int_{0}^{1}\frac{u}{\cos^{2}u}\mathrm{d}u=\int_{0}^{1}u\mathrm{d}(\tan u)=[u\tan u]_{0}^{1}-\int_{0}^{1}\tan u\mathrm{d}u=\tan1+\ln\cos1,$$
>
> 所以
>
> $$I=2\pi(\tan1+\ln\cos1).$$
>
> 上半球面的外法向写成 $(x,y,z)$ 是第一步；对称性消掉两项后， $\mathrm{d}S=\frac{\mathrm{d}xdy}{z}$ 与 $\cos^{2}z$ 里的 z 恰好约掉一个 z，这是本题的巧处.

**5.** （难度：★★★★）计算

$$I=\iint_{\Sigma}x y\mathrm{d}y\mathrm{d}z+y\sqrt{x^{2}+z^{2}}\mathrm{d}z\mathrm{d}x+y z\mathrm{d}x\mathrm{d}y,$$

其中 $\Sigma$ 是两球面 $x^{2}+y^{2}+z^{2}=a^{2}$、 $x^{2}+y^{2}+z^{2}=4a^{2}$ 以及圆锥面 $x^{2}-y^{2}+z^{2}=0$ ( $y\geqslant0$) 所围成的空间区域 $\Omega$ 的边界曲面的外侧.

> [!answer]- 原书参考答案（A.7.3·第二类曲面积分 第 5 题，未逐题独立验算）
> **5.** **第一步: 散度.** 记 P = xy, $Q = y\sqrt{x^{2} + z^{2}}$, R = yz, 则
>
> $$\mathrm{div}\left(P,Q,R\right)=y+\sqrt{x^{2}+z^{2}}+y=2y+\sqrt{x^{2}+z^{2}}.$$
>
> $\Sigma$ 是 $\Omega$ 的外侧封闭曲面，故由高斯公式
>
> $$I=\iiint_{\Omega}\left[2y+\sqrt{x^{2}+z^{2}}\right]\mathrm{d}V.$$
>
> **第二步: 把 $\Omega$ 用球坐标写出来.** $\Omega$ 是 $a \leq r \leq 2a$ 且 $y \geq \sqrt{x^2 + z^2}$ 的部分. 令 $y = r \cos \varphi$、 $\sqrt{x^2 + z^2} = r \sin \varphi$ ( $\varphi$ 为与 y 轴的夹角, $\theta \in [0, 2\pi]$), 则 $y \geq \sqrt{x^2 + z^2}$ 即
>
> $$0\leqslant\varphi\leqslant\frac{\pi}{4},\qquad a\leqslant r\leqslant2a,\qquad0\leqslant\theta\leqslant2\pi,\qquad\mathrm{d}V=r^{2}\sin\varphi\mathrm{d}r\mathrm{d}\varphi\mathrm{d}\theta.$$
>
> **第三步: 分别算两块.** 由 $\int_{a}^{2a} r^{3} dr = \frac{15a^{4}}{4}$、 $\int_{0}^{\pi/4} \sin \varphi \cos \varphi d\varphi = \frac{1}{4}$、 $\int_{0}^{\pi/4} \sin^{2} \varphi d\varphi = \frac{\pi}{8} - \frac{1}{4} = 0.1415\ldots$.
>
> $$\iiint_{\Omega}y\mathrm{d}V=2\pi\cdot\frac{1}{4}\cdot\frac{15a^{4}}{4}=\frac{15\pi a^{4}}{8},\qquad\iiint_{\Omega}\sqrt{x^{2}+z^{2}}\mathrm{d}V=2\pi\left(\frac{\pi}{8}-\frac{1}{4}\right)\frac{15a^{4}}{4}=\frac{15\pi a^{4}(\pi-2)}{16}$$
>
> **第四步：合并。** 注意第一块要乘系数2:
>
> $$I=2\cdot\frac{15\pi a^{4}}{8}+\frac{15\pi a^{4}(\pi-2)}{16}=\frac{15\pi a^{4}}{4}+\frac{15\pi a^{4}(\pi-2)}{16}=\frac{15\pi a^{4}(\pi+2)}{16}.$$

**6.** (难度:★★★) 设 $\Sigma$ 是一个光滑封闭曲面, 方向朝外, 给定第二型曲面积分

$$I=\iint_{\Sigma}(x^{3}-x)\mathrm{d}y\mathrm{d}z+(2y^{3}-y)\mathrm{d}z\mathrm{d}x+(3z^{3}-z)\mathrm{d}x\mathrm{d}y.$$

试确定曲面 $\Sigma$，使得积分 I 的值最小，并求该最小值.

> [!answer]- 原书参考答案（A.7.3·第二类曲面积分 第 6 题，未逐题独立验算）
> **6.** 先用高斯定理把 I 写成三重积分，被积函数是 $3(x^{2}+2y^{2}+z^{2}-1)$; 要让积分最小，区域就取成被积函数为负的那部分，即椭圆 $x^{2}+2y^{2}+z^{2}\leq1$. 设 $\Sigma$ 围成的区域为 $\Omega$，由高斯定理
>
> $$\begin{aligned}I&=\iiint_{\Omega}\left[\frac{\partial}{\partial x}(x^{3}-x)+\frac{\partial}{\partial y}(2y^{3}-y)+\frac{\partial}{\partial z}(3z^{3}-z)\right]\mathrm{d}V\\=\iiint_{\Omega}\left(3x^{2}-1+6y^{2}-1+3z^{2}-1\right)\mathrm{d}V&=3\iiint_{\Omega}\left(x^{2}+2y^{2}+z^{2}-1\right)\mathrm{d}V.\end{aligned}$$
>
> 被积函数 $3(x^{2}+2y^{2}+z^{2}-1)$ 在椭球 $x^{2}+2y^{2}+z^{2}\leqslant1$ 内为负、在外为正.要让 $\Omega$ 上的积分最小，就取
>
> $$\Omega:\ x^{2}+2y^{2}+z^{2}\leqslant1,$$
>
> 即 $\Sigma$ 为椭球面 $x^{2}+2y^{2}+z^{2}=1$ 的外侧.
>
> 此时由椭球公式 (半轴 $a=1$, $b=\frac{1}{\sqrt{2}}$, $c=1$):
>
> $$\iiint_{\Omega}x^{2}\mathrm{d}V=\frac{4\pi}{15}a^{3}bc=\frac{4\pi}{15\sqrt{2}},$$
>
> $$\iiint_{\Omega}y^{2}\mathrm{d}V=\frac{4\pi}{15}ab^{3}c=\frac{4\pi}{30\sqrt{2}},$$
>
> $$\iiint_{\Omega}^{}z^{2}\mathrm{d}V=\frac{4\pi}{15}abc^{3}=\frac{4\pi}{15\sqrt{2}},$$
>
> 故
>
> $$\iiint_{\Omega}\left(x^{2}+2y^{2}+z^{2}\right)\mathrm{d}V=\frac{4\pi}{15\sqrt{2}}+\frac{4\pi}{15\sqrt{2}}+\frac{4\pi}{15\sqrt{2}}=\frac{4\pi}{5\sqrt{2}}.$$
>
> 又
>
> $$V(\Omega)=\frac{4}{3}\pi a b c=\frac{4\pi}{3\sqrt{2}},$$
>
> 所以
>
> $$I_{\min}=3\left(\frac{4\pi}{5\sqrt{2}}-\frac{4\pi}{3\sqrt{2}}\right)=3\cdot\frac{4\pi}{\sqrt{2}}\cdot\left(\frac{1}{5}-\frac{1}{3}\right)=-\frac{4\sqrt{2}\pi}{5}.$$
>
> 「使积分最小」的曲面，就是让三重积分的被积函数在区域内尽量为负：这里正好是 $x^{2}+2y^{2}+z^{2}\leq1$。

**7.** (难度:★★★) 设球体 $(x-1)^2 + (y-1)^2 + (z-1)^2 \leq 12$ 被平面 $P: x + y + z = 6$ 所截的小球缺为 $\Omega$，对应于小球缺的球冠记为 $\Sigma$，方向指向球外，求第二型曲面积分

$$I=\iint_{\Sigma}x\mathrm{d}y\mathrm{d}z+y\mathrm{d}z\mathrm{d}x+z\mathrm{d}x\mathrm{d}y.$$

> [!answer]- 原书参考答案（A.7.3·第二类曲面积分 第 7 题，未逐题独立验算）
> **7.** 球冠不封闭，补上平面上的圆盘后再用高斯定理；圆盘上的积分直接是常数乘面积.
>
> 球心为 C(1,1,1), 半径 $R=2\sqrt{3}$. 平面 P: $x+y+z=6$ 到球心的距离为
>
> $$d=\frac{\left|1+1+1-6\right|}{\sqrt{3}}=\sqrt{3},$$
>
> 故所截圆盘半径为
>
> $$\rho=\sqrt{R^{2}-d^{2}}=\sqrt{12-3}=3,\qquad 面积 S=9\pi.$$
>
> Ω 是球缺, 其高 $h = R - d = \sqrt{3}$, 体积为
>
> $$V=\frac{\pi h^{2}}{3}(3R-h)=\frac{\pi\cdot3}{3}\left(6\sqrt{3}-\sqrt{3}\right)=5\sqrt{3}\pi.$$
>
> 把球冠 $\Sigma$ 与平面圆盘 $\Sigma_{0}$ 合起来构成封闭曲面，法向都指向球外（对 $\Omega$ 而言，圆盘的外法向指向 $-(1,1,1)$ 方向），由高斯定理
>
> $$\iint_{\Sigma}+\iint_{\Sigma_{0}}=\iiint_{\Omega}\left(1+1+1\right)\mathrm{d}V=3V=15\sqrt{3}\pi.$$
>
> 在圆盘 $\Sigma_0$ 上, $x + y + z = 6$, 外法向的方向余弦为 $\left(-\frac{1}{\sqrt{3}}, -\frac{1}{\sqrt{3}}, -\frac{1}{\sqrt{3}}\right)$, 于是 $\iint_{\Sigma_0} x \, \mathrm{d}y \, \mathrm{d}z + y \, \mathrm{d}z \, \mathrm{d}x + z \, \mathrm{d}x \, \mathrm{d}y = \iint_{\Sigma_0} \frac{-(x + y + z)}{\sqrt{3}} \, \mathrm{d}S = \frac{-6}{\sqrt{3}} \cdot 9\pi = -18\sqrt{3}\pi$. 所以
>
> $$I=15\sqrt{3}\pi-\left(-18\sqrt{3}\pi\right)=33\sqrt{3}\pi.$$
>
> 补面时方向要算准: 圆盘相对 $\Omega$ 的外法向是 $-\frac{(1,1,1)}{\sqrt{3}}$, 所以它在总和里贡献的是 $-18\sqrt{3}\pi$, 减号容易漏.

**8.** (难度:★★★★) 设 $\Omega$ 是由曲面 $\Sigma : \frac{x^{2}}{9} + \frac{y^{2}}{16} + \frac{(z-3)^{2}}{4} = 1$ 围成的有界区域, $\mathbf{r} = (x, y, z)$, n 是 $\Sigma$ 的外法向量, 证明:

$$\iint_{\Sigma}\cos(\mathbf{r},\mathbf{n})\mathrm{d}S=\iiint_{\Omega}\frac{2}{\|\mathbf{r}\|}\mathrm{d}x\mathrm{d}y\mathrm{d}z.$$

> [!answer]- 原书参考答案（A.7.3·第二类曲面积分 第 8 题，未逐题独立验算）
> **8.** 把 $\cos(r,n)$ 用方向余弦与分量写成普通的乘加形式，再对 $\frac{x}{R},\frac{y}{R},\frac{z}{R}$ 用高斯定理. 记
>
> $$R=\left|r\right|=\sqrt{x^{2}+y^{2}+z^{2}}.$$
>
> 设 $\Sigma$ 的外法向方向余弦为 $\cos\alpha, \cos\beta, \cos\gamma$，则
>
> $$\cos(r,n)=\frac{x\cos\alpha+y\cos\beta+z\cos\gamma}{R}.$$
>
> 于是
>
> $$\iint_{\Sigma}\cos(r,n)\mathrm{d}S=\iint_{\Sigma}\frac{x}{R}\cos\alpha\mathrm{d}S+\frac{y}{R}\cos\beta\mathrm{d}S+\frac{z}{R}\cos\gamma\mathrm{d}S,$$
>
> 而这正好是第二类曲面积分
>
> $$\iint_{\Sigma}\frac{x}{R}\mathrm{d}y\mathrm{d}z+\frac{y}{R}\mathrm{d}z\mathrm{d}x+\frac{z}{R}\mathrm{d}x\mathrm{d}y.$$
>
> 椭球 $\frac{x^{2}}{9}+\frac{y^{2}}{16}+\frac{(z-3)^{2}}{4}=1$ 的中心为 $(0,0,3)$，而原点代入左边得 $\frac{9}{4}>1$，说明原点不在 $\Omega$ 内，故 R>0 在 $\Omega$ 上恒成立. 对
>
> $$P=\frac{x}{R},\qquad Q=\frac{y}{R},\qquad S=\frac{z}{R}$$
>
> 用高斯定理：
>
> $$\frac{\partial P}{\partial x}=\frac{R^{2}-x^{2}}{R^{3}},\qquad\frac{\partial Q}{\partial y}=\frac{R^{2}-y^{2}}{R^{3}},\qquad\frac{\partial S}{\partial z}=\frac{R^{2}-z^{2}}{R^{3}}.$$
>
> 三者相加
>
> $$\frac{3R^{2}-\left(x^{2}+y^{2}+z^{2}\right)}{R^{3}}=\frac{3R^{2}-R^{2}}{R^{3}}=\frac{2}{R}.$$
>
> 所以
>
> $$\iint_{\Sigma}\cos(r,n)\mathrm{d}S=\iiint_{\Omega}\frac{2}{R}\mathrm{d}x\mathrm{d}y\mathrm{d}z=\iiint_{\Omega}\frac{2}{|r|}\mathrm{d}x\mathrm{d}y\mathrm{d}z.$$
>
> 本题只用到「方向余弦把第一类与第二类互化」以及高斯定理，全程都是普通乘加；注意先说明原点不在积分区域内。

**9.** (难度: ★★★★) 设 $\Omega$ 是由光滑的简单闭合曲面 $\Sigma$ 围成的有界闭区域, 函数 $u(x, y, z)$ 和 $v(x, y, z)$ 在 $\Omega$ 上有二阶连续偏导数, $\frac{\partial u}{\partial \mathbf{n}}, \frac{\partial v}{\partial \mathbf{n}}$ 分别表示 u 与 v 沿 $\Sigma$ 的外法线方向 $\mathbf{n}$ 的方向导数, 规定:

$$\Delta u=\frac{\partial^{2}u}{\partial x^{2}}+\frac{\partial^{2}u}{\partial y^{2}}+\frac{\partial^{2}u}{\partial z^{2}},$$

试证明：

$$\iint_{\Sigma}\left(v\frac{\partial u}{\partial\mathbf{n}}-u\frac{\partial v}{\partial\mathbf{n}}\right)\mathrm{d}S=\iiint_{\Omega}(v\Delta u-u\Delta v)\mathrm{d}x\mathrm{d}y\mathrm{d}z.$$

> [!answer]- 原书参考答案（A.7.3·第二类曲面积分 第 9 题，未逐题独立验算）
> **9.** 两边的差别只在「乘法求导后多出来的那一块」： $\frac{\partial}{\partial x}\left(v\frac{\partial u}{\partial x}\right)$ 会多出 $\frac{\partial v}{\partial x}\frac{\partial u}{\partial x}$，两个积分正好抵消。记
>
> $$A_{u}=\frac{\partial u}{\partial x}\cos\alpha+\frac{\partial u}{\partial y}\cos\beta+\frac{\partial u}{\partial z}\cos\gamma,$$
>
> $A_v$ 同理, 其中 $(\cos \alpha, \cos \beta, \cos \gamma)$ 是 $\Sigma$ 的外法线方向余弦. 由方向余弦与第二类曲面积分的关系,
>
> $$\iint_{\Sigma}v A_{u}\mathrm{d}S=\iint_{\Sigma}v\frac{\partial u}{\partial x}\mathrm{d}y\mathrm{d}z+v\frac{\partial u}{\partial y}\mathrm{d}z\mathrm{d}x+v\frac{\partial u}{\partial z}\mathrm{d}x\mathrm{d}y.$$
>
> 用高斯定理：
>
> $$\iint_{\Sigma}v A_{u}\mathrm{d}S=\iiint_{\Omega}\left[\frac{\partial}{\partial x}\left(v\frac{\partial u}{\partial x}\right)+\frac{\partial}{\partial y}\left(v\frac{\partial u}{\partial y}\right)+\frac{\partial}{\partial z}\left(v\frac{\partial u}{\partial z}\right)\right]\mathrm{d}V.$$
>
> 把每个乘积求导展开：
>
> $$\frac{\partial}{\partial x}\left(v\frac{\partial u}{\partial x}\right)=v\frac{\partial^{2}u}{\partial x^{2}}+\frac{\partial v}{\partial x}\frac{\partial u}{\partial x},$$
>
> 其余两项同理，于是
>
> $$\iint_{\Sigma}v A_{u}\mathrm{d}S=\iiint_{\Omega}v B_{u}\mathrm{d}V+\iiint_{\Omega}\left(\frac{\partial u}{\partial x}\frac{\partial v}{\partial x}+\frac{\partial u}{\partial y}\frac{\partial v}{\partial y}+\frac{\partial u}{\partial z}\frac{\partial v}{\partial z}\right)\mathrm{d}V,$$
>
> 其中 $B_{u}=\frac{\partial^{2}u}{\partial x^{2}}+\frac{\partial^{2}u}{\partial y^{2}}+\frac{\partial^{2}u}{\partial z^{2}}.$
>
> 完全对称地，
>
> $$\iint_{\Sigma}u A_{v}\mathrm{d}S=\iiint_{\Omega}u B_{v}\mathrm{d}V+\iiint_{\Omega}\left(\frac{\partial u}{\partial x}\frac{\partial v}{\partial x}+\frac{\partial u}{\partial y}\frac{\partial v}{\partial y}+\frac{\partial u}{\partial z}\frac{\partial v}{\partial z}\right)\mathrm{d}V.$$
>
> 两式相减，最后的括号项完全相同、相互抵消，得
>
> $$\iint_{\Sigma}\left(v A_{u}-u A_{v}\right)\mathrm{d}S=\iiint_{\Omega}\left(v B_{u}-u B_{v}\right)\mathrm{d}V.$$
>
> 这就是格林第二公式. 全程只用「方向余弦把第一类化成第二类」和「乘积求导」，没有任何别的工具.

---

# 基础篇·第八章 无穷级数

## 8.1 裂项

裂项的考察,主要是学会如何去裂项,与高中相关的数列内容联系紧密,可以边做题,边感受.

**1.** (难度:★★) 设 x > 0 或 x < -1, 求级数

$$\sum_{n=1}^{\infty}\ln\frac{\left\lbrack1+(n-1)x\right\rbrack(1+2nx)}{(1+nx)\left\lbrack1+2(n-1)x\right\rbrack}$$

的和.

> [!answer]- 原书参考答案（A.8.1 第 1 题，未逐题独立验算）
> **1.** 通项是对数的商，直接写成「对数之差」就能裂项；但 x < -1 时有些因子是负的，逐个取对数会出错，所以更稳妥的做法是先把前 N 项的乘积累起来，再一次性取对数。记
>
> $$u_{n}=\ln\frac{\left[1+(n-1)x\right](1+2nx)}{(1+nx)\left[1+2(n-1)x\right]}.$$
>
> 则
>
> $$S_{N}=\ln\prod_{n=1}^{N}\frac{\left[1+(n-1)x\right](1+2n x)}{(1+n x)\left[1+2(n-1)x\right]}.$$
>
> 把分子、分母各自的连乘展开：
>
> $$\prod_{n=1}^{N}\left[1+(n-1)x\right]=1\cdot(1+x)(1+2x)\cdot\cdot\cdot(1+(N-1)x),$$
>
> $$\prod_{n=1}^{N}(1+2nx)=(1+2x)(1+4x)\cdot\cdot\cdot(1+2Nx),$$
>
> $$\prod_{n=1}^{N}(1+nx)=(1+x)(1+2x)\cdot\cdot\cdot(1+Nx),$$
>
> $$\prod_{n=1}^{N}\left[1+2(n-1)x\right]=1\cdot(1+2x)(1+4x)\cdot\cdot\cdot(1+2(N-1)x).$$
>
> 公共因子 $(1+x)(1+2x)\cdots(1+(N-1)x)$ 与 $(1+2x)(1+4x)\cdots(1+2(N-1)x)$ 全部约去，只剩
>
> $$S_{N}=\ln\frac{1+2Nx}{1+Nx}=\ln\frac{2+\frac{1}{N}}{1+\frac{1}{N}}\longrightarrow\ln2.$$
>
> 所以级数的和为 $\ln 2$. x > 0 时所有因子都为正, 逐项取对数即可; x < -1 时 $1 + (n - 1)x < 0$, 但分子、分母中负因子的个数相同, 商的符号不变, 连乘约分后的结果完全一样, 这就是先乘后取对数的好处.

**2.** (难度:★★★) 求数项级数 $\sum_{n=1}^{\infty}\frac{n+2}{n!+(n+1)!+(n+2)!}$ 的和.

> [!answer]- 原书参考答案（A.8.1 第 2 题，未逐题独立验算）
> **2.** 分母是三个连着写的阶乘, 先把最小的 n! 提出来做公因式, 分母就会变成 n! 乘一个关于 n 的多项式, 再与分子约分, 剩下的正好能拆成 $\frac{1}{(n+1)!} - \frac{1}{(n+2)!}$. 提出 n!:
>
> $$n!+(n+1)!+(n+2)!=n!\left[1+(n+1)+(n+1)(n+2)\right].$$
>
> 括号内
>
> $$1+(n+1)+(n+1)(n+2)=(n+2)(1+n+1)=(n+2)^{2},$$
>
> 所以
>
> $$\frac{n+2}{n!+(n+1)!+(n+2)!}=\frac{n+2}{n!(n+2)^{2}}=\frac{1}{n!(n+2)}.$$
>
> 又 $(n+2)!={(n+2)(n+1)n!}$，即 $\frac{1}{n!(n+2)}=\frac{n+1}{(n+2)!}$，于是
>
> $$\frac{1}{n!(n+2)}=\frac{(n+2)-1}{(n+2)!}=\frac{1}{(n+1)!}-\frac{1}{(n+2)!}.$$
>
> 求和：
>
> $$S_{N}=\left(\frac{1}{2!}-\frac{1}{3!}\right)+\left(\frac{1}{3!}-\frac{1}{4!}\right)+\cdots=\frac{1}{2}-\frac{1}{(N+2)!}\longrightarrow\frac{1}{2}.$$
>
> 所以原级数的和为 $\frac{1}{2}$. 阶乘裂项的通用套路: 先把分母统一到同一个 (较小的) 阶乘上, 再把分子写成「分母中最大的那个因子减去常数」. 本题中 $(n+2)-1$ 就是关键的一步.

**3.** (难度:★★★) 设数列 $\{a_{n}\}$ 满足 $a_{1}=5$ ，且 $3a_{n+1}=(a_{n}+1)^{3}-5$ (n=1,2, $\ldots$). 求级数 $\sum_{n=1}^{\infty}\frac{a_{n}-1}{a_{n}^{2}+a_{n}+1}$ 的值.

> [!answer]- 原书参考答案（A.8.1 第 3 题，未逐题独立验算）
> **3.** 要凑出不动点. 先把递推式两边都往「不动点」处平移: 由 $3a_{n+1}=(a_{n}+1)^{3}-5$ 解不动点得 $x_0=1$ (此时 $f(x)=x$ 有重根), 令 $u_{n}=a_{n}-1$, 则 $3u_{n+1}=(u_{n}+2)^{3}-8=u_{n}(u_{n}^{2}+6u_{n}+12)$. 第一步: 换元. 令 $u_{n}=a_{n}-1$, 由 $u_{1}=5-1=4$, 且
>
> $$3u_{n+1}=3a_{n+1}-3=\left(a_{n}+1\right)^{3}-8=\left(u_{n}+2\right)^{3}-8=u_{n}\left(u_{n}^{2}+6u_{n}+12\right).$$
>
> 而
>
> $$u_{n}^{2}+6u_{n}+12=u_{n}^{2}+6u_{n}+9+3=(u_{n}+3)^{2}+3.$$
>
> 第二步：找一个「好」的差分. 注意
>
> $$3\left(u_{n+1}+3\right)=u_{n}\left(u_{n}^{2}+6u_{n}+12\right)+9=\left(u_{n}+3\right)\left(u_{n}^{2}+3u_{n}+3\right),$$
>
> 最后一步直接展开可验证. 由上式解出
>
> $$u_{n}^{2}+3u_{n}+3=\frac{3\left(u_{n+1}+3\right)}{u_{n}+3},$$
>
> 所以待求的通项可以改写为
>
> $$\frac{u_{n}}{u_{n}^{2}+3u_{n}+3}=\frac{u_{n}\left(u_{n}+3\right)}{3\left(u_{n+1}+3\right)}.$$
>
> 另一方面
>
> $$\frac{1}{u_{n}+3}-\frac{1}{u_{n+1}+3}=\frac{u_{n+1}-u_{n}}{\left(u_{n}+3\right)\left(u_{n+1}+3\right)},$$
>
> 而
>
> $$u_{n+1}-u_{n}=\frac{u_{n}\left(u_{n}^{2}+6u_{n}+12\right)}{3}-u_{n}=\frac{u_{n}\left(u_{n}+3\right)^{2}}{3},$$
>
> 代入得
>
> $$\frac{1}{u_{n}+3}-\frac{1}{u_{n+1}+3}=\frac{u_{n}\left(u_{n}+3\right)^{2}}{3\left(u_{n}+3\right)\left(u_{n+1}+3\right)}=\frac{u_{n}\left(u_{n}+3\right)}{3\left(u_{n+1}+3\right)}=\frac{u_{n}}{u_{n}^{2}+3u_{n}+3}.$$
>
> 第三步：求和. 由 $u_{1}=4>1$ 及 $u_{n+1}=\frac{u_{n}(u_{n}^{2}+6u_{n}+12)}{3}>u_{n}$ 知 $\{u_{n}\}$ 单调递增；若它有界，就会收敛于某个 u>0 且 $3u=u(u^2+6u+12)$，即 $u^{2}+6u+9=0$，推出 u=-3，矛盾. 所以 $u_{n}\to\infty$，从而 $\frac{1}{u_{n+1}+3}\to0$. 于是
>
> $$\sum_{n=1}^{\infty}\frac{a_{n}-1}{a_{n}^{2}+a_{n}+1}=\sum_{n=1}^{\infty}\left(\frac{1}{u_{n}+3}-\frac{1}{u_{n+1}+3}\right)=\frac{1}{u_{1}+3}=\frac{1}{7}.$$
>
> 注意 $a_{n}^{2}+a_{n}+1=(a_{n}-1)^{2}+3(a_{n}-1)+3=u_{n}^{2}+3u_{n}+3$ 。不动点 $x_{0}=1$ 是 $f(x)-x$ 的二重根，这正是「先换元、再取倒数」的信号：换元后右端出现了 $(u_{n}+3)$ 这个整体因子，取倒数就自动裂项了。

**4.** (难度:★★★★) 求级数 $\sum_{n=1}^{\infty} \arctan \frac{2}{8n^{2}-4n-1}$ 的值.

> [!answer]- 原书参考答案（A.8.1 第 4 题，未逐题独立验算）
> **4.** 这是反正切裂项. 按公式, 需要把 $\frac{2}{8n^{2}-4n-1}$ 凑成 $\frac{k}{d_{n}d_{n+1}+1}$, 其中 $d_{n}=kn+t$.
>
> 用待定系数法试最小的整数解即可. 设 $d_{n}=kn+t$ (k>0), 则 $d_{n+1}=kn+k+t$,
>
> 于是
>
> $$d_{n}d_{n+1}+1=k^{2}n^{2}+k(2t+k)n+t(t+k)+1.$$
>
> 要求 $\frac{2}{8n^{2}-4n-1}=\frac{k}{d_{n}d_{n+1}+1}$，把两个分母化成对应次数的多项式，就是
>
> $$k^{2}n^{2}+k(2t+k)n+t(t+k)+1=\frac{k}{2}\left(8n^{2}-4n-1\right)=4kn^{2}-2kn-\frac{k}{2}.$$
>
> 比较系数: $n^{2}$ 项给出 $k^{2}=4k$, 即 k=4; n 项给出 $k(2t+k)=-2k$, 即 $2t+k=-2$, 也就是 t=-3. 把 k=4, t=-3 代入常数项检验: $t(t+k)+1=(-3)\cdot1+1=-2$, 而 $-\frac{k}{2}=-2$, 恰好吻合.
>
> 于是 $d_{n}=4n-3, d_{n+1}=4n+1$ ，并且
>
> $$d_{n}d_{n+1}+1=(4n-3)(4n+1)+1=16n^{2}-8n-2=2\left(8n^{2}-4n-1\right),$$
>
> 所以
>
> $$\frac{2}{8n^{2}-4n-1}=\frac{4}{d_{n}d_{n+1}+1}=\frac{k}{d_{n}d_{n+1}+1}\qquad(k=4).$$
>
> 由反正切差角公式
>
> $$\arctan\frac{2}{8n^{2}-4n-1}=\arctan\frac{1}{4n-3}-\arctan\frac{1}{4n+1}.$$
>
> 两种下标分别是 1,5,9, $\cdots$ 与 5,9,13, $\cdots$,前后正好首尾相接,故
>
> $$S_{N}=\arctan1-\arctan\frac{1}{4N+1}\longrightarrow\frac{\pi}{4}.$$
>
> 所以原级数的和为 $\frac{\pi}{4}$．「待定系数」的实操顺序是：先用 $n^{2}$的系数定出k，再用n的系数与常数项反解t；若解不是整数，就回到原式去「观察」因式分解．本题的正解是把 $8n^{2}-4n-1$写成 $\frac{(4n-3)(4n+1)+1}{2}$，即k=4、 $d_{n}=4n-3$.

**5.** (难度:★★★★) 设 $\{a_{n}\}$, $\{b_{n}\}$ 均为正项数列, $a_{1}=b_{1}=1$, $b_{n}=a_{n}b_{n-1}-2$ (n≥2). 若 $\{b_{n}\}$ 有上界, 证明级数 $\sum_{n=1}^{\infty}\frac{1}{a_{1}a_{2}\cdots a_{n}}$ 收敛, 并求其和.

> [!answer]- 原书参考答案（A.8.1 第 5 题，未逐题独立验算）
> **5.** 令 $T_{n}=a_{1}a_{2}\cdots a_{n}$，则 $a_{n}=T_{n}/T_{n-1}$. 代入递推式并两边除以 $T_{n}$，直接得到 $\frac{1}{T_{n}}$ 的裂项. 再证明 $b_{n}/T_{n} \rightarrow 0$ 即可. 记 $T_{n} = a_{1}a_{2} \cdots a_{n}$，则 $T_{1} = 1$，且 $a_{n} = \frac{T_{n}}{T_{n-1}} (n \geqslant 2)$.
>
> 由 $b_{n}=a_{n}b_{n-1}-2$ ，代入 $a_{n}=\frac{T_{n}}{T}$
>
> $$b_{n}=\frac{T_{n}}{T_{n-1}}b_{n-1}-2.$$
>
> 两边同时除以 $T_{n}$:
>
> $$\frac{b_{n}}{T_{n}}=\frac{b_{n-1}}{T_{n-1}}-\frac{2}{T_{n}},$$
>
> 即
>
> $$\frac{1}{T_{n}}=\frac{1}{2}\left(\frac{b_{n-1}}{T_{n-1}}-\frac{b_{n}}{T_{n}}\right).$$
>
> 令 $c_{n}=\frac{b_{n}}{T_{n}}$，则(1)化为
>
> $$\frac{1}{T_{n}}=\frac{1}{2}(c_{n-1}-c_{n})\qquad(n\geqslant2).$$
>
> 且 $c_{1}=\frac{b_{1}}{T_{1}}=1$
>
> 对 n=1 到 N 求和:
>
> $$\begin{aligned}\sum_{n=1}^{N}\frac{1}{T_{n}}&=\frac{1}{T_{1}}+\frac{1}{2}\sum_{n=2}^{N}(c_{n-1}-c_{n})\\&=1+\frac{1}{2}(c_{1}-c_{N})=\frac{3}{2}-\frac{1}{2}c_{N}.\end{aligned}$$
>
> 下面证明 $c_{N} \rightarrow 0$ 。由 $b_{n} = a_{n}b_{n-1} - 2$ 得 $a_{n} = \frac{b_{n} + 2}{b_{n-1}}$ ，所以
>
> $$T_{n}=\prod_{k=2}^{n}\frac{b_{k}+2}{b_{k-1}}=\frac{(b_{2}+2)\cdots(b_{n}+2)}{b_{1}b_{2}\cdots b_{n-1}},$$
>
> 从而
>
> $$c_{n}=\frac{b_{n}}{T_{n}}=\prod_{k=2}^{n}\frac{b_{k}}{b_{k}+2}.$$
>
> 因为 $\{b_{n}\}$ 有上界，设 $b_{n} \leqslant M$，则每个因子
>
> $$\frac{b_{k}}{b_{k}+2}\leqslant\frac{M}{M+2}<1,$$
>
> 所以
>
> $$0<c_{n}\leqslant\left(\frac{M}{M+2}\right)^{n-1}\longrightarrow0.$$
>
> 因此 $c_{N} \rightarrow 0$ ，级数收敛，且
>
> $$\sum_{n=1}^{\infty}\frac{1}{T_{n}}=\lim_{N\to\infty}\left(\frac{3}{2}-\frac{1}{2}c_{N}\right)=\frac{3}{2}.$$
>
> 先由 $a_{n}=T_{n}/T_{n-1}$ 代入递推式得到裂项，再证明 $c_{N}\rightarrow0$ ，比先构造 $c_{n}$ 更自然.有上界条件只用于保证 $c_{N}\rightarrow0$.

**6.** (难度: ★★★★) 证明级数

$$\sum_{n=1}^{\infty}\frac{1-\frac{1}{2}+\frac{1}{3}-\cdots+\frac{(-1)^{n-1}}{n}}{n(n+1)}$$

收敛，并求其和.

> [!answer]- 原书参考答案（A.8.1 第 6 题，未逐题独立验算）
> **6.** 关键是发现对 $a_{n}=\ln\left(1+\frac{1}{n}\right)$ 有恒等式 $a_{2n}+a_{2n+1}=a_{n}$，两边平方后就能把乘积 $a_{2n}a_{2n+1}$ 拆成三个平方项之差. 记
>
> $$a_{n}=\ln\left(1+\frac{1}{n}\right)=\ln\frac{n+1}{n}\qquad(n\geqslant1).$$
>
> 则
>
> $$a_{2n}+a_{2n+1}=\ln\frac{2n+1}{2n}+\ln\frac{2n+2}{2n+1}=\ln\frac{2n+2}{2n}=\ln\frac{n+1}{n}=a_{n}.$$
>
> 两边平方：
>
> $$a_{2n}^{2}+2a_{2n}a_{2n+1}+a_{2n+1}^{2}=a_{n}^{2},$$
>
> 即原级数的通项满足
>
> $$u_{n}=a_{2n}a_{2n+1}=\frac{1}{2}\left(a_{n}^{2}-a_{2n}^{2}-a_{2n+1}^{2}\right).$$
>
> 于是前 N 项和
>
> $$\sum_{n=1}^{N}u_{n}=\frac{1}{2}\left[\sum_{n=1}^{N}a_{n}^{2}-\sum_{n=1}^{N}\left(a_{2n}^{2}+a_{2n+1}^{2}\right)\right]=\frac{1}{2}\left[\sum_{n=1}^{N}a_{n}^{2}-\sum_{k=2}^{2N+1}a_{k}^{2}\right].$$
>
> 把第一个和式中的 $a_{2}^{2}, \ldots, a_{N}^{2}$ 与第二个和式中的对应项抵消，得
>
> $$\sum_{n=1}^{N}u_{n}=\frac{1}{2}\left[a_{1}^{2}-\sum_{k=N+1}^{2N+1}a_{k}^{2}\right].$$
>
> 由 $a_k^2 \leqslant \frac{1}{k^2}$ 及 $\sum \frac{1}{k^2}$ 收敛知 $\sum_{k=N+1}^{2N+1} a_k^2 \to 0$，所以原级数收敛，且
>
> $$\sum_{n=1}^{\infty}u_{n}=\frac{1}{2}a_{1}^{2}=\frac{1}{2}\ln^{2}2.$$
>
> 本题没有用「放缩」去估计收敛速度, 而是靠一个精确的代数恒等式把部分和写成有限的项; 最后判断尾部趋于 0 时才用到最简单的放缩 $a_{k}^{2} \leqslant \frac{1}{k^{2}}$.

## 8.2 求和函数

无穷级数的核心计算考察方向, 计算量偏大, 主要掌握通过逐项求导或逐项积分对和函数的求解.

**1.** (难度:★★) 求幂级数 $\sum_{n=0}^{\infty}(-1)^{n}\frac{2n^{2}+1}{(2n)!}x^{2n}$ 的收敛域与和函数.

> [!answer]- 原书参考答案（A.8.2 第 1 题，未逐题独立验算）
> **1.** 这是缺项幂级数, 直接对通项 $u_{n}=(-1)^{n}\frac{2n^{2}+1}{(2n)!}x^{2n}$ 用比值法:
>
> $$\left|\frac{u_{n+1}}{u_{n}}\right|=\frac{2(n+1)^{2}+1}{2n^{2}+1}\cdot\frac{(2n)!}{(2n+2)!}\cdot x^{2}=\frac{2(n+1)^{2}+1}{(2n^{2}+1)(2n+2)(2n+1)}x^{2}\longrightarrow0,$$
>
> 对任何实数 x 都成立, 所以收敛半径 $R = +\infty$, 收敛域为 $(-\infty, +\infty)$.
>
> 下用已知展开式求和. 由
>
> $$\cos x=\sum_{n=0}^{\infty}(-1)^{n}\frac{x^{2n}}{(2n)!}$$
>
> 出发，逐项求导两次得到
>
> $$\sum_{n=0}^{\infty}(-1)^{n}\frac{2n x^{2n}}{(2n)!}=-x\sin x,\qquad\sum_{n=0}^{\infty}(-1)^{n}\frac{2n(2n-1)x^{2n}}{(2n)!}=-x^{2}\cos x.$$
>
> 两式都来自把 $\cos$ 的展开逐项求导再乘 x (或 $x^{2}$)。又
>
> $$2n^{2}=\frac{1}{2}\left[2n(2n-1)+2n\right],$$
>
> 所以
>
> $$\sum_{n=0}^{\infty}(-1)^{n}\frac{2n^{2}x^{2n}}{(2n)!}=\frac{1}{2}\left(-x^{2}\cos x-x\sin x\right).$$
>
> 再加上 $\sum(-1)^{n}\frac{x^{2n}}{(2n)!} = \cos x$，得
>
> $$S(x)=\cos x-\frac{1}{2}\left(x^{2}\cos x+x\sin x\right),$$
>
> 收敛域为 $(-∞,+∞)$.

**2.** (难度:★★★★) 求级数 $\sum_{n=1}^{\infty}\left(1+\frac{1}{2}+\frac{1}{3}+\cdots+\frac{1}{n}\right)x^{n}$ 的收敛半径及和函数.

> [!answer]- 原书参考答案（A.8.2 第 2 题，未逐题独立验算）
> **2.** 记 $H_{n}=1+\frac{1}{2}+\cdots+\frac{1}{n}, H_{0}=0, S(x)=\sum_{n\geq1}H_{n}x^{n}$. 关键在于 $H_{n}$ 满足的递推关系
>
> $$H_{n}-H_{n-1}=\frac{1}{n},$$
>
> 即 $H_{n}=H_{n-1}+\frac{1}{n}$. 把它代进去:
>
> $$S(x)=\sum_{n\geqslant1}H_{n-1}x^{n}+\sum_{n\geqslant1}\frac{x^{n}}{n}=x\sum_{n\geqslant0}H_{n}x^{n}+\left(-\ln(1-x)\right),$$
>
> 其中第一个和式就是 $xS(x)$，第二个和式用了 $\sum_{n\geq1}\frac{x^n}{n} = -\ln(1-x)$ ( $|x|<1$)。于是
>
> $$S(x)=x S(x)-\ln(1-x),$$
>
> 解这个一次方程得
>
> $$S(x)=\frac{-\ln(1-x)}{1-x}\qquad(|x|<1).$$
>
> 由 $H_n \sim \ln n$, $\lim_{n \to \infty} \sqrt[n]{H_n} = 1$, 故收敛半径 $R = 1$.

**3.** (难度: ★★★★★) 求级数 $\sum_{n=1}^{\infty}\sum_{i=1}^{n}\frac{(n+1)-i}{i}x^{n}$ 的收敛域与和函数.

> [!answer]- 原书参考答案（A.8.2 第 3 题，未逐题独立验算）
> **3.** 先算内层和: $\sum_{i=1}^{n}\frac{(n+1)-i}{i}=(n+1)H_{n}-n$，于是原级数就是 $\sum[(n+1)H_{n}-n]x^{n}$，用两个已知和函数 （$\sum H_{n}x^{n}$ 与 $\sum nx^{n}$） 拆开. 第一步: 算内层和.
>
> $$\sum_{i=1}^{n}\frac{(n+1)-i}{i}=(n+1)\sum_{i=1}^{n}\frac{1}{i}-\sum_{i=1}^{n}1=(n+1)H_{n}-n.$$
>
> 所以原级数为
>
> $$\sum_{n=1}^{\infty}\left[(n+1)H_{n}-n\right]x^{n}=\sum_{n=1}^{\infty}n H_{n}x^{n}+\sum_{n=1}^{\infty}H_{n}x^{n}-\sum_{n=1}^{\infty}n x^{n}.$$
>
> 第二步：三个和函数.
>
> $$\sum_{n=1}^{\infty}H_{n}x^{n}=-\frac{\ln(1-x)}{1-x},\qquad\sum_{n=1}^{\infty}nx^{n}=\frac{x}{(1-x)^{2}},$$
>
> 后者求导可得; 而由第一式两边乘以 x 再求导:
>
> $$\sum_{n=1}^{\infty}nH_{n}x^{n}=x\frac{\mathrm{d}}{\mathrm{d}x}\left\lbrack-\frac{\ln(1-x)}{1-x}\right\rbrack=\frac{x\left\lbrack1-\ln(1-x)\right\rbrack}{(1-x)^{2}},$$
>
> 其中用到了
>
> $$\frac{\mathrm{d}}{\mathrm{d}x}\left\lbrack-\frac{\ln(1-x)}{1-x}\right\rbrack=\frac{1-\ln(1-x)}{(1-x)^{2}}.$$
>
> 第三步：合并.
>
> $$\sum_{n=1}^{\infty}\left[(n+1)H_{n}-n\right]x^{n}=\frac{x\left[1-\ln(1-x)\right]}{(1-x)^{2}}-\frac{\ln(1-x)}{1-x}-\frac{x}{(1-x)^{2}}.$$
>
> 后两项通分到 $(1-x)^{2}$:
>
> $$-\frac{\ln(1-x)}{1-x}=-\frac{(1-x)\ln(1-x)}{(1-x)^{2}},\qquad-\frac{x}{(1-x)^{2}}=\frac{-x}{(1-x)^{2}},$$
>
> 于是分子为
>
> $$x-x\ln(1-x)-(1-x)\ln(1-x)-x=-\ln(1-x),$$
>
> 即
>
> $$\sum_{n=1}^{\infty}\left(\sum_{i=1}^{n}\frac{(n+1)-i}{i}\right)x^{n}=-\frac{\ln(1-x)}{(1-x)^{2}}\qquad(-1<x<1).$$
>
> 第一个分母 $\frac{1}{(1-x)^2}$ 的「求导」，与 8.2.2 中「 $\ln(1-x)$ 型求和」是同一套路。全部计算都在 $|x|<1$ 内进行，端点 $x=\pm1$ 处级数发散（通项不趋于 0），故收敛域为 $(-1,1)$。

**4.** (难度:★★★) 记幂级数 $\sum_{n=1}^{\infty}\frac{x^{2n-1}}{(2n-1)!!}$ 的和函数为 $s(x)$，试导出 $s(x)$ 所满足的一阶常微分方程初值问题，并由此求出 $s(x)$.

> [!answer]- 原书参考答案（A.8.2 第 4 题，未逐题独立验算）
> **4.** 先看通项比值：
>
> $$\left|\frac{u_{n+1}}{u_{n}}\right|=\frac{(2n-1)!!}{(2n+1)!!}x^{2}=\frac{x^{2}}{2n+1}\longrightarrow0,$$
>
> 故收敛半径 $R = +\infty$.
>
> 注意 $(2n-1)!!=(2n-1)(2n-3)!!$，逐项求导得
>
> $$s^{\prime}(x)=\sum_{n\geqslant1}\frac{(2n-1)x^{2n-2}}{(2n-1)!!}=\sum_{n\geqslant1}\frac{x^{2n-2}}{(2n-3)!!}=1+\sum_{n\geqslant2}\frac{x^{2n-2}}{(2n-3)!!}.$$
>
> 在第二个和式中提出一个x，并把下标写成原来的形式：
>
> $$\sum_{n\geqslant2}\frac{x^{2n-2}}{(2n-3)!!}=x\sum_{n\geqslant1}\frac{x^{2n-1}}{(2n-1)!!}=x s(x).$$
>
> 所以
>
> $$s^{\prime}(x)=1+x s(x),\qquad s(0)=0.$$
>
> 这是一阶线性方程 $s' - xs = 1$，积分因子为 $e^{-x^2/2}$：
>
> $$\left(s\mathbf{e}^{-x^{2}/2}\right)^{\prime}=\mathbf{e}^{-x^{2}/2},$$
>
> 两边从0到x积分 $(s(0)=0)$:
>
> $$s(x)\mathrm{e}^{-x^{2}/2}=\int_{0}^{x}\mathrm{e}^{-t^{2}/2}\mathrm{d}t,$$
>
> 故
>
> $$s(x)=\mathrm{e}^{x^{2}/2}\int_{0}^{x}\mathrm{e}^{-t^{2}/2}\mathrm{d}t.$$

**5.** （难度：★★★）设

$$f(x)=\left\{\begin{aligned}&\frac{x^{2}+1}{x}\arctan x,&x\neq0,\\ &1,&x=0\end{aligned}\right.$$

的麦克劳林展开式 $f(x)=\sum_{n=0}^{\infty}a_{n}x^{n}$，求幂级数 $\sum_{n=1}^{\infty}|a_{2n}|x^{n}\quad(0<x<1)$ 的和函数.

> [!answer]- 原书参考答案（A.8.2 第 5 题，未逐题独立验算）
> **5.** 分母 $16n^{2}-1=(4n-1)(4n+1)$，先裂项成 $\frac{1}{2}\left(\frac{1}{4n-1}-\frac{1}{4n+1}\right)$，再用 $\operatorname{artanh}$ 与 $\arctan$ 的展开分别求和. 裂项：
>
> $$\frac{x^{2n}}{16n^{2}-1}=\frac{x^{2n}}{(4n-1)(4n+1)}=\frac{1}{2}\left(\frac{x^{2n}}{4n-1}-\frac{x^{2n}}{4n+1}\right).$$
>
> 记 $s = \sqrt{x}$，则 $x^{2n} = s^{4n}$.
>
> 第一部分：
>
> $$\sum_{n=1}^{\infty}\frac{s^{4n}}{4n-1}=s\int_{0}^{s}\frac{u^{2}}{1-u^{4}}\mathrm{d}u=\frac{s}{2}\left(\operatorname{artanh} s-\arctan s\right).$$
>
> 第二部分：
>
> $$\sum_{n=1}^{\infty}\frac{s^{4n}}{4n+1}=\frac{1}{s}\int_{0}^{s}\frac{u^{4}}{1-u^{4}}\mathrm{d}u=\frac{1}{s}\left[\frac{1}{2}\left(\operatorname{artanh} s+\arctan s\right)-s\right].$$
>
> 两部分相减再乘 $\frac{1}{2}$，并代回 $s=\sqrt{x}$:
>
> $$\begin{aligned}\sum_{n=1}^{\infty}\frac{x^{2n}}{16n^{2}-1}=\frac{1}{2}+\frac{1}{4}\Big[&\left(\sqrt{x}-\frac{1}{\sqrt{x}}\right)\operatorname{artanh}\sqrt{x}\\&-\left(\sqrt{x}+\frac{1}{\sqrt{x}}\right)\arctan\sqrt{x}\Big]\quad(0<|x|<1).\end{aligned}$$
>
> 令 x=1，注意 $\arctan1=\frac{\pi}{4}$、第一项中 $\sqrt{x}-\frac{1}{\sqrt{x}}=0$，得
>
> $$\sum_{n=1}^{\infty}\frac{1}{16n^{2}-1}=\frac{1}{2}-\frac{\pi}{8}.$$
>
> x = 1 处虽然超出了幂级数内部的范围, 但 $\sum\frac{1}{16n^{2}-1}$ 本身收敛, 且和函数在 x = 1 处连续, 所以可以把 $x \to 1^{-}$ 的极限直接读成端点值.

**6.** (难度:★★★★) 设数列 $\{a_{n}\}$ 满足 $a_{0}=1, a_{1}=0, a_{n+1}=\frac{1}{n+1}(na_{n}+a_{n-1})$ ( $n \geq 1$)，求幂级数 $\sum_{n=0}^{\infty}a_{n}x^{n}$ 的收敛半径与和函数.

> [!answer]- 原书参考答案（A.8.2 第 6 题，未逐题独立验算）
> **6.** 系数满足 $(n+1)a_{n+1}=na_n+a_{n-1}$，把含 n 的项都翻译成「求导」，就得到 S 的一阶微分方程。记 $S(x)=\sum_{n=0}^{\infty}a_nx^n$，则 $S'(x)=\sum_{n\geq1}na_nx^{n-1}$。由
>
> $$(n+1)a_{n+1}=na_{n}+a_{n-1}\qquad(n\geqslant1)$$
>
> 两边乘 $x^{n}$并对 $n\geqslant1$求和：
>
> $$\sum_{n\geqslant1}(n+1)a_{n+1}x^{n}=\sum_{n\geqslant1}na_{n}x^{n}+\sum_{n\geqslant1}a_{n-1}x^{n}.$$
>
> 左端令 $m = n + 1$: $\sum_{m \geq 2} ma_m x^{m-1} = S'(x) - a_1 = S'(x)$ (因为 $a_1 = 0$); 右端第一项为 $xS'(x)$, 第二项为 $xS(x)$. 所以
>
> $$S^{\prime}(x)=x S^{\prime}(x)+x S(x),$$
>
> 即
>
> $$S^{\prime}(x)\left(1-x\right)=xS(x)\quad\Longrightarrow\quad\frac{S^{\prime}(x)}{S(x)}=\frac{x}{1-x}.$$
>
> 积分: $\ln S = -x - \ln(1 - x) + C$，即 $S = \frac{C' e^{-x}}{1 - x}$。由 $S(0) = a_0 = 1$ 得 $C' = 1$，故
>
> $$\sum_{n=0}^{\infty}a_{n}x^{n}=\frac{\mathrm{e}^{-x}}{1-x}.$$
>
> 收敛半径由分母1-x的零点决定 $\left(\frac{e^{-x}}{1-x}\right.$在x=-1处解析，在x=1处有奇点)
>
> ，故 R=1. 验证： $\frac{e^{-x}}{1-x}$ 中 $x^{n}$ 的系数为 $\sum_{m=0}^{n}\frac{(-1)^{m}}{m!}$，其中 n=2 时为 $1-1+\frac{1}{2}=\frac{1}{2}=a_{2}, n=3$ 时为 $\frac{1}{3}=a_{3}$，与递推一致.

**7.** (难度:★★★★★) 证明级数 $1 + \sum_{n=1}^{\infty}(-1)^{n}\frac{2\cdot4\cdot6\cdots(2n)}{3\cdot5\cdot7\cdots(2n+1)}$ 收敛，并求其和.

> [!answer]- 原书参考答案（A.8.2 第 7 题，未逐题独立验算）
> **7.** 所求和可以看成幂级数 $S(x) = \sum_{n \geq 1} (-1)^n \frac{(2n)!!}{(2n+1)!!} x^{2n+1}$ 在 x = 1 处的值再加 1.
>
> 收敛性用 Wallis 积分 $I_{n}=\int_{0}^{\pi/2}\sin^{n}x\,\mathrm{d}x$ 判断: 恰好有 $I_{2n+1}=\frac{(2n)!!}{(2n+1)!!}$，把 $a_{n}$ 换成积分就没有难度了. 求和的方程由系数关系 $(2n+1)a_{n}=2na_{n-1}$ 给出. 记
>
> $$a_{n}=\frac{2\cdot4\cdot\cdots(2n)}{3\cdot5\cdot\cdots(2n+1)}=\frac{(2n)!!}{(2n+1)!!}\qquad(a_{0}=1).$$
>
> 第一步：证明收敛. 因为
>
> $$\frac{a_{n+1}}{a_{n}}=\frac{(2n+2)!!}{(2n+3)!!}\cdot\frac{(2n+1)!!}{(2n)!!}=\frac{2n+2}{2n+3}<1,$$
>
> 所以 $\{a_n\}$ 是递减的正数列。再记 $I_n = \int_0^{\pi/2} \sin^n x \, dx$，由分部积分
>
> $$I_{n}=\int_{0}^{\pi/2}\sin^{n-1}x\sin x\mathrm{d}x=\frac{n-1}{n}\int_{0}^{\pi/2}\sin^{n-2}x\mathrm{d}x=\frac{n-1}{n}I_{n-2}\qquad(n\geqslant2).$$
>
> 由 $I_{0}=\frac{\pi}{2}$、 $I_{1}=1$，反复用上式可归纳得到
>
> $$I_{2n+1}=\frac{(2n)!!}{(2n+1)!!}=a_{n}.$$
>
> 又 $\{I_{n}\}$递减，故 $I_{n}<I_{n-1}$，把它与 $nI_{n}=(n-1)I_{n-2}$相乘：
>
> $$nI_{n}I_{n-1}=(n-1)I_{n-2}I_{n-1}=\cdots=I_{1}I_{0}=\frac{\pi}{2}$$
>
> （一直降到最后一步），于是
>
> $$n I_{n}^{2}<n I_{n}I_{n-1}=\frac{\pi}{2}\quad\Longrightarrow\quad0<I_{n}<\sqrt{\frac{\pi}{2n}},$$
>
> 令 $n \to \infty$ 得 $I_{n} \to 0$，从而 $0 < a_{n} = I_{2n+1} \to 0$。 $\{a_{n}\}$ 递减趋于 0，由莱布尼茨判别法，级数 $1 + \sum_{n=1}^{\infty} (-1)^{n} a_{n}$ 收敛。
>
> 第二步：设和函数并建立方程.设
>
> $$S(x)=\sum_{n=1}^{\infty}(-1)^{n}\frac{(2n)!!}{(2n+1)!!}x^{2n+1}=\sum_{n=1}^{\infty}(-1)^{n}a_{n}x^{2n+1},$$
>
> 则所求之和为 $1 + S(1)$. 由系数关系
>
> $$(2n+1)a_{n}=\frac{(2n)!!}{(2n-1)!!}=2n a_{n-1}\qquad(n\geqslant1)$$
>
> 得
>
> $$S^{\prime}(x)=\sum_{n\geqslant1}(-1)^{n}(2n+1)a_{n}x^{2n}=x\left(\sum_{n\geqslant1}(-1)^{n}a_{n-1}x^{2n}\right)^{\prime}.$$
>
> 而
>
> $$\sum_{n\geqslant1}(-1)^{n}a_{n-1}x^{2n}=-x^{2}\sum_{m\geqslant0}(-1)^{m}a_{m}x^{2m}=-x^{2}\left(1+\frac{S(x)}{x}\right)=-x^{2}-xS(x),$$
>
> 所以
>
> $$\begin{aligned}S^{\prime}(x)&=x\left(-x^{2}-xS(x)\right)^{\prime}=x\left(-2x-S(x)-xS^{\prime}(x)\right)\\&=-2x^{2}-xS(x)-x^{2}S^{\prime}(x),\end{aligned}$$
>
> 整理得 $S(x)$ 满足的一阶线性方程与初值
>
> $$\left(1+x^{2}\right)S^{\prime}(x)+x S(x)=-2x^{2},\qquad 即 S^{\prime}(x)+\frac{x}{1+x^{2}}S(x)=-\frac{2x^{2}}{1+x^{2}},S(0)=0.$$
>
> 第三步：解出 $S(x)$. 积分因子为
>
> $$\mathrm{e}^{\int\frac{x}{1+x^{2}}\mathrm{d}x}=\mathrm{e}^{\frac{1}{2}\ln(1+x^{2})}=\sqrt{1+x^{2}},$$
>
> 于是
>
> $$\left(S\sqrt{1+x^{2}}\right)^{\prime}=\sqrt{1+x^{2}}\cdot\left(-\frac{2x^{2}}{1+x^{2}}\right)=-\frac{2x^{2}}{\sqrt{1+x^{2}}}.$$
>
> 由 $\int\frac{t^{2}}{\sqrt{1+t^{2}}}\,\mathrm{d}t=\frac{t\sqrt{1+t^{2}}-\ln\left(t+\sqrt{1+t^{2}}\right)}{2}$ 并从 0 到 x 积分，
>
> $$S(x)\sqrt{1+x^{2}}=\ln\left(x+\sqrt{1+x^{2}}\right)-x\sqrt{1+x^{2}},$$
>
> 即
>
> $$S(x)=\frac{\ln\left(x+\sqrt{1+x^{2}}\right)}{\sqrt{1+x^{2}}}-x.$$
>
> 第四步：取 x = 1. 级数 $\sum(-1)^{n}a_{n}$ 收敛，且 $S(x)$ 在 x = 1 处连续，故
>
> $$\sum_{n=1}^{\infty}(-1)^{n}\frac{(2n)!!}{(2n+1)!!}=S(1)=\frac{\ln\left(1+\sqrt{2}\right)}{\sqrt{2}}-1,$$
>
> 所以
>
> $$1+\sum_{n=1}^{\infty}(-1)^{n}\frac{2\cdot4\cdot\cdots(2n)}{3\cdot5\cdot\cdots(2n+1)}=\frac{\ln\left(1+\sqrt{2}\right)}{\sqrt{2}}.$$
>
> 两条关键信息: $a_n = I_{2n+1}$ 让收敛性变成 Wallis 积分的简单估计, $(2n+1)a_n = 2na_{n-1}$ 让幂级数变成一阶线性方程. 顺带得到一个可复用的结论: $\sum_{n \geq 0} \frac{(2n)!!}{(2n+1)!!} x^{2n+1} = \frac{\arcsin x}{\sqrt{1-x^2}} (|x| < 1)$, 本题的和函数就是它的交错版本.

**8.** （难度：★★★★★）求级数

$$\sum_{n=1}^{\infty}\frac{1}{3}\cdot\frac{2}{5}\cdot\frac{3}{7}\cdots\frac{n}{2n+1}\cdot\frac{1}{n+1}$$

之和.

> [!answer]- 原书参考答案（A.8.2 第 8 题，未逐题独立验算）
> **8.** 先把一般项化简: $\frac{n!}{3\cdot5\cdots(2n+1)} = \frac{(2n)!!}{2^n(2n+1)!!}$. 记 $c_n = \frac{(2n)!!}{(2n+1)!!}$, 则所求为 $\sum_{n\geq1}\frac{c_n}{2^n(n+1)} = \frac{1}{2}\sum_{n\geq1}\frac{c_n}{n+1}\left(\frac{1}{2}\right)^n$. 只要造出以 $c_n$ 为系数的母函数 $B(x) = \sum_{n\geq1}c_nx^{2n+1}$, 它满足一个一阶线性方程. 由 $n! = \frac{(2n)!!}{2^n}$, 原级数的通项 $\frac{1}{2}\ldots\frac{n}{2}\ldots\frac{1}{n} = \frac{n!}{n!}\ldots\frac{1}{1} = \frac{c_n}{c_n} = \frac{(2n)!!}{(2n+1)!!}$
>
> $$\frac{1}{3}\cdot\frac{2}{5}\cdots\frac{n}{2n+1}\cdot\frac{1}{n+1}=\frac{n!}{(2n+1)!!}\cdot\frac{1}{n+1}=\frac{c_{n}}{2^{n}(n+1)},\qquad c_{n}=\frac{(2n)!!}{(2n+1)!!}.$$
>
> 第一步：造母函数.设
>
> $$S_{1}(x)=\sum_{n=1}^{\infty}\frac{c_{n}x^{n+1}}{n+1},\qquad B(x)=\sum_{n=1}^{\infty}c_{n}x^{2n+1}\qquad(0<x<1),$$
>
> 则所求和恰为 $T = \sum_{n \geq 1} \frac{c_n}{2^n (n+1)} = 2S_1\left(\frac{1}{2}\right)$（因为 $S_1\left(\frac{1}{2}\right) = \sum_{n \geq 1} \frac{c_n}{n+1}2^{-(n+1)} = \frac{T}{2}$）. 又
>
> $$S_{1}^{\prime}(x)=\sum_{n\geq1}c_{n}x^{n}=\frac{1}{\sqrt{x}}\sum_{n\geq1}c_{n}\left(\sqrt{x}\right)^{2n}=\frac{B\big(\sqrt{x}\big)}{\sqrt{x}},$$
>
> 所以只要求出 B 的封闭形式.
>
> 第二步: 求 $B(x)$. 注意 $(2n+1)c_n = \frac{(2n)!!}{(2n-1)!!}$，逐项求导得
>
> $$B^{\prime}(x)=\sum_{n\geqslant1}(2n+1)c_{n}x^{2n}=\sum_{n\geqslant1}\frac{(2n)!!}{(2n-1)!!}x^{2n}=2x^{2}+\sum_{n\geqslant2}\frac{(2n)!!}{(2n-1)!!}x^{2n}.$$
>
> 在 $n \geqslant 2$ 的项中把因子 2n 拿出来凑成求导，并注意 $\frac{(2n)!!}{(2n-1)!!} = 2n c_{n-1}$
>
> $$\sum_{n\geqslant2}\frac{(2n)!!}{(2n-1)!!}x^{2n}=x\left(\sum_{n\geqslant2}\frac{(2n-2)!!}{(2n-1)!!}x^{2n}\right)^{\prime}=x\left(x^{2}\sum_{m\geqslant1}c_{m}x^{2m}\right)^{\prime}=x\big(xB(x)\big)^{\prime}.$$
>
> 于是
>
> $$B^{\prime}=2x^{2}+x\left(B+xB^{\prime}\right)\quad\Longrightarrow\quad\left(1-x^{2}\right)B^{\prime}-xB=2x^{2},\qquad B(0)=0.$$
>
> 两边同乘积分因子 $\mathrm{e}^{-\frac{1}{2}\ln(1-x^{2})}=\frac{1}{\sqrt{1-x^{2}}}$:
>
> $$\left(B\sqrt{1-x^{2}}\right)^{\prime}=\frac{2x^{2}}{\sqrt{1-x^{2}}},\qquad B\sqrt{1-x^{2}}=\int_{0}^{x}\frac{2t^{2}}{\sqrt{1-t^{2}}}\mathrm{d}t.$$
>
> 用 $t = \sin \theta$ 换元得 $\int_{0}^{x} \frac{2t^{2}}{\sqrt{1-t^{2}}} dt = \int_{0}^{\arcsin x} 2 \sin^{2} \theta d\theta = \arcsin x - x \sqrt{1-x^{2}}$,
>
> 故
>
> $$B(x)=\frac{\arcsin x-x\sqrt{1-x^{2}}}{\sqrt{1-x^{2}}}.$$
>
> 第三步：由 B 求 $S_{1}$. 代入 $S_{1}^{\prime}$
>
> $$S_{1}^{\prime}(x)=\frac{1}{\sqrt{x}}\cdot\frac{\arcsin\sqrt{x}-\sqrt{x}\sqrt{1-x}}{\sqrt{1-x}}=\frac{\arcsin\sqrt{x}}{\sqrt{x(1-x)}}-1.$$
>
> 再作换元 $t = \sin^2 \theta$ ( $dt = 2 \sin \theta \cos \theta \, d\theta$, $\sqrt{t(1 - t)} = \sin \theta \cos \theta$):
>
> $$S_{1}(x)=\int_{0}^{x}\left(\frac{\arcsin\sqrt{t}}{\sqrt{t(1-t)}}-1\right)\mathrm{d}t=\int_{0}^{\arcsin\sqrt{x}}2\theta\mathrm{d}\theta-x=\left(\arcsin\sqrt{x}\right)^{2}-x.$$
>
> 第四步: 取 $x = \frac{1}{2}$. 此时 $\arcsin \frac{\sqrt{2}}{2} = \frac{\pi}{4}$, 于是
>
> $$T=2S_{1}\biggl(\frac{1}{2}\biggr)=2\left[\left(\frac{\pi}{4}\right)^{2}-\frac{1}{2}\right]=\frac{\pi^{2}}{8}-1.$$
>
> 整题的骨架是「母函数+一阶线性方程」:B的方程由 $c_{n}$的相邻比 $c_{n}=\frac{2n}{2n+1}c_{n-1}$驱动,解出B后再积分一次得到 $S_{1}$.注意B的定义是 $\sum_{n\geq1}c_{n}x^{2n+1}$（从n=1起）,所以B(0)=0;若错写成从n=0起,多出的x项会让方程与结果整体错位.

**9.** (难度:★★★★) 证明级数 $\sum_{n=1}^{\infty}\ln\left(1+\frac{1}{2n}\right)\ln\left(1+\frac{1}{2n+1}\right)$ 收敛，并求其和.

> [!answer]- 原书参考答案（A.8.2 第 9 题，未逐题独立验算）
> **9.** 记 $d_{m}=\ln\frac{m+1}{m}$，则所给通项为 $d_{2n}d_{2n+1}$
>
> 第一步:用恒等式把「对数之积」变成「对数平方」。由 $\ln a \cdot \ln b = \frac{1}{2} \left[ \ln^2(ab) - \ln^2 a - \ln^2 b \right]$，并注意
>
> $$\frac{2n+1}{2n}\cdot\frac{2n+2}{2n+1}=\frac{n+1}{n},$$
>
> 得
>
> $$d_{2n}d_{2n+1}=\frac{1}{2}\left[\ln^{2}\frac{n+1}{n}-\ln^{2}\frac{2n+1}{2n}-\ln^{2}\frac{2n+2}{2n+1}\right].$$
>
> 第二步：求和时三类项恰好抵消。记 S 为所求和，则
>
> $$S=\frac{1}{2}\Big[\underbrace{\sum_{m\geqslant1}\ln^{2}\frac{m+1}{m}}_{(*)}-\underbrace{\sum_{m 偶 ,m\geqslant2}\ln^{2}\frac{m+1}{m}}_{(**)}-\underbrace{\sum_{m 奇 ,m\geqslant3}\ln^{2}\frac{m+1}{m}}_{(***)}\Big].$$
>
> 而 $(**)+(***)$正好是 $(\ast)$中 $m\geqslant2$的全部项，两部分相消，只剩 $(\ast)$中的m=1
>
> 一项：
>
> $$S=\frac{1}{2}\ln^{2}\frac{2}{1}=\frac{1}{2}\left(\ln2\right)^{2}.$$
>
> 第三步：交代收敛性. 由 $\ln\left(1+\frac{1}{2n}\right)\sim\frac{1}{2n}$、 $\ln\left(1+\frac{1}{2n+1}\right)\sim\frac{1}{2n+1}$，通项 $\sim\frac{1}{4n^{2}}$，故级数收敛，其和为
>
> $$\sum_{n=1}^{\infty}\ln\left(1+\frac{1}{2n}\right)\ln\left(1+\frac{1}{2n+1}\right)=\frac{(\ln2)^{2}}{2}$$

**10.** (难度:★★★★) 设 $u_{n}=\int_{0}^{1}\frac{dt}{(1+t^{4})^{n}}$ ( $n\geqslant1$), 证明:

(1) 数列 $\{u_{n}\}$ 收敛.

(2) 级数 $\sum_{n=1}^{\infty}(-1)^{n}u_{n}$ 条件收敛.

(3) 当 $p \geqslant 1$ 时，级数 $\sum_{n=1}^{\infty} \frac{u_{n}}{n^{p}}$ 收敛，并求级数 $\sum_{n=1}^{\infty} \frac{u_{n}}{n}$ 的和.

> [!answer]- 原书参考答案（A.8.2 第 10 题，未逐题独立验算）
> **10.** (1) 先用单调性说明收敛, 再用分段估计证明极限为 0; (2) 先证 $u_n \downarrow 0$, 再由 $1 + t^4 \leqslant 1 + t$ 得到 $u_n$ 的下界, 从而绝对发散; (3) 对 $t(1 + t^4)^{-n}$ 求导再积分, 得到 $u_n$ 与 $u_{n+1}$ 的递推关系, 然后裂项. (1) 对 $t \in [0,1]$ 有
>
> $$0<\frac{1}{(1+t^{4})^{n+1}}\leqslant\frac{1}{(1+t^{4})^{n}},$$
>
> 逐项积分得 $0 < u_{n+1} \leqslant u_n$，即 $\{u_n\}$ 单调递减且有下界 0，故收敛.
>
> 下面用分段估计证明极限为0.取
>
> $$c_{n}=\frac{1}{n^{1/8}}\qquad(n\geqslant1),$$
>
> 把积分拆成两段：
>
> $$u_{n}=\int_{0}^{c_{n}}\frac{\mathrm{d}t}{(1+t^{4})^{n}}+\int_{c_{n}}^{1}\frac{\mathrm{d}t}{(1+t^{4})^{n}}.$$
>
> 第一段：被积函数 $\leqslant1$，故
>
> $$\int_{0}^{c_{n}}\frac{\mathrm{d}t}{(1+t^{4})^{n}}\leqslant c_{n}.$$
>
> 第二段：被积函数在 $[c_n,1]$上递减，所以
>
> $$\int_{c_{n}}^{1}\frac{\mathrm{d}t}{(1+t^{4})^{n}}\leqslant\frac{1-c_{n}}{(1+c_{n}^{4})^{n}}.$$
>
> 于是
>
> $$0<u_{n}\leqslant c_{n}+\frac{1-c_{n}}{(1+c_{n}^{4})^{n}}.$$
>
> 把 $c_{n}=n^{-1/8}$代入， $c_{n}^{4}=n^{-1/2}$，故
>
> $$(1+c_{n}^{4})^{n}=\left(1+\frac{1}{\sqrt{n}}\right)^{n}\geqslant1+\sqrt{n}\longrightarrow+\infty,$$
>
> 因此 $\frac{1-c_{n}}{(1+c_{n}^{4})^{n}}\rightarrow0$。又 $c_{n}\rightarrow0$，所以右端整体趋于0。
>
> 由夹逼定理，
>
> $$\lim_{n\to\infty}u_{n}=0.$$
>
> (2) 由于 $u_n \downarrow 0$，由莱布尼茨判别法知 $\sum (-1)^n u_n$ 收敛.
>
> 再看绝对收敛性. 当 $0 \leqslant t \leqslant 1$ 时 $t^{4} \leqslant t$, 即 $1 + t^{4} \leqslant 1 + t$, 于是
>
> $$u_{n}=\int_{0}^{1}\frac{\mathrm{d}t}{\left(1+t^{4}\right)^{n}}\geqslant\int_{0}^{1}\frac{\mathrm{d}t}{(1+t)^{n}}=\frac{1-2^{1-n}}{n-1}\qquad(n\geqslant2).$$
>
> 右端与 $\frac{1}{n}$ 同阶，故 $\sum u_n$ 发散，即 $\sum (-1)^n u_n$ 条件收敛.
>
> (3) 因为 $u_{n} \leqslant u_{1} (n \geqslant 1)$，而 $p \geqslant 1$ 时 $\sum \frac{1}{n^{p}}$ 收敛，所以 $\sum \frac{u_{n}}{n^{p}}$ 收敛.
>
> 下面求 $\sum\frac{u_n}{n}$. 考虑函数 $t(1+t^4)^{-n}$ 的导数:
>
> $$\frac{\mathrm{d}}{\mathrm{d}t}\left[\frac{t}{\left(1+t^{4}\right)^{n}}\right]=\frac{1}{\left(1+t^{4}\right)^{n}}-\frac{4n t^{4}}{\left(1+t^{4}\right)^{n+1}}.$$
>
> 两边从0到1积分：
>
> $$\frac{1}{2^{n}}=u_{n}-4n\int_{0}^{1}\frac{t^{4}}{\left(1+t^{4}\right)^{n+1}}\mathrm{d}t.$$
>
> 又
>
> $$\int_{0}^{1}\frac{t^{4}}{\left(1+t^{4}\right)^{n+1}}\mathrm{d}t=\int_{0}^{1}\frac{\left(1+t^{4}\right)-1}{\left(1+t^{4}\right)^{n+1}}\mathrm{d}t=u_{n}-u_{n+1},$$
>
> 代入得
>
> $$\frac{1}{2^{n}}=u_{n}-4n\left(u_{n}-u_{n+1}\right)\quad\Longrightarrow\quad\frac{u_{n}}{n}=4\left(u_{n}-u_{n+1}\right)+\frac{1}{n2^{n}}.$$
>
> 求和 $(u_{N+1}\rightarrow0)$:
>
> $$\sum_{n=1}^{\infty}\frac{u_{n}}{n}=4u_{1}+\sum_{n=1}^{\infty}\frac{1}{n2^{n}}=4u_{1}+\ln2,$$
>
> 其中用到 $\sum_{n\geq1}\frac{1}{n2^n}=-\ln\left(1-\frac{1}{2}\right)=\ln2$.而
>
> $$u_{1}=\int_{0}^{1}\frac{\mathrm{d}t}{1+t^{4}}=\frac{\pi+2\ln\left(1+\sqrt{2}\right)}{4\sqrt{2}},$$
>
> 所以
>
> $$\sum_{n=1}^{\infty}\frac{u_{n}}{n}=\frac{\pi+2\ln\left(1+\sqrt{2}\right)}{\sqrt{2}}+\ln2.$$
>
> (1) 中 $c_{n} = \frac{1}{n^{1/8}}$ 的选取是关键: $c_{n} \to 0$ 保证第一段趋于 0，而 $c_{n}^{4} = n^{-1/2}$ 使得 $(1 + c_{n}^{4})^{n} \geq 1 + \sqrt{n} \to \infty$，第二段也趋于 0。两段同时被夹逼到 0，这是处理 $\int_{0}^{1}(1 + t^{4})^{-n}dt$ 这类积分的常用手法。

## 8.3 幂级数展开

求和函数的逆运用, 相对而言难度并不算高, 除河南复赛外, 考察频率并不高, 可适当练习.

**1.** (难度:★) 设 a, b 均为正数, 函数 $\frac{1}{(1-ax)(1-bx)}$ 的麦克劳林展开式记为 $\sum_{n=0}^{\infty} u_{n}x^{n}$, 求幂级数 $\sum_{n=0}^{\infty} u_{n}^{2}x^{n}$ 的和函数.

> [!answer]- 原书参考答案（A.8.3 第 1 题，未逐题独立验算）
> **1.** 先把 $\frac{1}{(1-ax)(1-bx)}$ 拆成部分分式，立刻得到 $u_{n}$ 的通项；平方之后每一项都是 $a^{p}b^{q}$ 型的几何级数。先作部分分式分解：
>
> $$\frac{1}{(1-ax)(1-bx)}=\frac{1}{a-b}\left(\frac{a}{1-ax}-\frac{b}{1-bx}\right),$$
>
> 于是
>
> $$u_{n}=\frac{a^{n+1}-b^{n+1}}{a-b}\qquad(a\neq b).$$
>
> 平方：
>
> $$u_{n}^{2}=\frac{a^{2n+2}-2(ab)^{n+1}+b^{2n+2}}{(a-b)^{2}},$$
>
> 逐项求和（都是几何级数）：
>
> $$\sum_{n=0}^{\infty}u_{n}^{2}x^{n}=\frac{1}{(a-b)^{2}}\left[\frac{a^{2}}{1-a^{2}x}-\frac{2ab}{1-abx}+\frac{b^{2}}{1-b^{2}x}\right],$$
>
> 收敛域由三个分母同时不为零且公比小于1决定，即
>
> $$|x|<\frac{1}{\max\left\{a^{2},a b,b^{2}\right\}}.$$
>
> 若 a = b，则 $u_{n} = (n+1)a^{n}$，上式是 $a \to b$ 时的极限，结果为 $\frac{a^{2}(1+a^{2}x)}{(1-a^{2}x)^{3}}$，可以作为一个练习自行验证.

**2.** (难度:★★★) 求函数 $f(x)=\left(\sum_{n=1}^{\infty}x^{n}\right)^{2}(|x|<1)$ 的麦克劳林级数中 $x^{2019}$ 的系数.

> [!answer]- 原书参考答案（A.8.3 第 2 题，未逐题独立验算）
> **2.** $\sum_{n\geq1}x^n$ 就是几何级数, 平方之后先求出和函数, 再用 $\frac{1}{(1-x)^2}$ 的展开读出系数. 因为 $\sum_{n=1}^{\infty}x^n = \frac{x}{1-x}$, 所以
>
> $$f(x)=\left(\frac{x}{1-x}\right)^{2}=\frac{x^{2}}{(1-x)^{2}}=x^{2}\sum_{n=0}^{\infty}(n+1)x^{n}=\sum_{n=0}^{\infty}(n+1)x^{n+2}.$$
>
> 要取 $x^{2019}$，令 $n+2 = 2019$，即 n = 2017，系数为 $n+1 = 2018 \cdot \frac{1}{(1-x)^2} = \sum(n+1)x^n$ 与 $\frac{1}{1-x} = \sum x^n$ 是幂级数展开里出现频率最高的两个公式，务必记牢.

**3.** (难度:★★★) 求函数 $f(x)=\frac{1+x}{(1-x)^3}$ 的幂级数展开式.

> [!answer]- 原书参考答案（A.8.3 第 3 题，未逐题独立验算）
> **3.** $\frac{1}{(1-x)^{3}}$ 的展开是已知的（由 $\frac{1}{(1-x)^{2}}$ 再求导一次得到），乘上 $(1+x)$ 后合并同类项即可. 由
>
> $$\frac{1}{(1-x)^{2}}=\sum_{n=0}^{\infty}(n+1)x^{n}$$
>
> 两边求导：
>
> $$\frac{2}{(1-x)^{3}}=\sum_{n=1}^{\infty}n(n+1)x^{n-1}=\sum_{n=0}^{\infty}(n+1)(n+2)x^{n},$$
>
> 即
>
> $$\frac{1}{(1-x)^{3}}=\sum_{n=0}^{\infty}\frac{(n+1)(n+2)}{2}x^{n}.$$
>
> 于是
>
> $$\begin{aligned}\frac{1+x}{(1-x)^{3}}&=\sum_{n=0}^{\infty}\frac{(n+1)(n+2)}{2}x^{n}+\sum_{n=0}^{\infty}\frac{n(n+1)}{2}x^{n}\\&=\sum_{n=0}^{\infty}\frac{(n+1)\left[(n+2)+n\right]}{2}x^{n}.\end{aligned}$$
>
> 括号内 $(n+1)[(n+2)+n]=(n+1)(2n+2)=2(n+1)^{2}$，所以
>
> $$\frac{1+x}{(1-x)^{3}}=\sum_{n=0}^{\infty}(n+1)^{2}x^{n}\qquad(|x|<1).$$
>
> 结论 $\frac{1+x}{(1-x)^3} = \sum(n+1)^2 x^n$ 值得直接记住，它与 $\frac{x(1+x)}{(1-x)^3} = \sum n^2 x^n$ 只差一个 x.

**4.** (难度: ★★★★) 求函数 $f(x)=\frac{1+2x+3x^{2}}{(1+x+x^{2}+x^{3})^{2}}$ 的麦克劳林级数中 $x^{2019}$ 的系数.

> [!answer]- 原书参考答案（A.8.3 第 4 题，未逐题独立验算）
> **4.** 分母 $1 + x + x^{2} + x^{3}$ 可以因式分解成 $\frac{1 - x^{4}}{1 - x}$，平方后变成 $\frac{(1 - x)^{2}}{(1 - x^{4})^{2}}$，而 $\frac{1}{(1 - x^{4})^{2}}$ 的展开只在 4 的倍数次幂上出现。因为
>
> $$1+x+x^{2}+x^{3}=\frac{1-x^{4}}{1-x},$$
>
> 所以
>
> $$f(x)=\frac{1+2x+3x^{2}}{\left(1+x+x^{2}+x^{3}\right)^{2}}=\frac{\left(1+2x+3x^{2}\right)(1-x)^{2}}{\left(1-x^{4}\right)^{2}}.$$
>
> 先算分子：
>
> $$\left(1+2x+3x^{2}\right)\left(1-2x+x^{2}\right)=1-4x^{3}+3x^{4}.$$
>
> 再由
>
> $$\frac{1}{\left(1-x^{4}\right)^{2}}=\sum_{k=0}^{\infty}(k+1)x^{4k}$$
>
> 得
>
> $$f(x)=\left(1-4x^{3}+3x^{4}\right)\sum_{k=0}^{\infty}(k+1)x^{4k}.$$
>
> 要取 $x^{2019}$: 因为 2019 = 4 × 504 + 3, 只能来自 $-4x^{3}$ 与 $(k+1)x^{4k}$ 相乘, 此时 4k = 2016, 即 k = 504, 于是系数为
>
> $$-4\times(504+1)=-2020.$$
>
> 这类「只问某一项系数」的题,关键是先把函数化成 $\frac{P(x)}{(1-x^m)^n}$的形状,然后按m的余数分类讨论,能省掉大量展开.

## 8.4 傅里叶级数

无穷级数的边缘考点,但一旦考察,就是拉分题,一定要额外注意,给出一定的练习空间.

**1.** (难度:★) 设函数 $f(x)=x^{2}, 0 \leqslant x < 1$，而正弦级数 $S(x)=\sum_{n=1}^{\infty} b_{n} \sin n \pi x$，其中 $b_{n}=2 \int_{0}^{1} f(x) \sin n \pi x \, dx$，求 $S\left(-\frac{1}{2}\right)$.

> [!answer]- 原书参考答案（A.8.4 第 1 题，未逐题独立验算）
> **1.** 只问和函数在某一点的值, 不需要把系数全部算出来: 正弦级数对应的是 $f(x)$ 的奇延拓, 而奇函数的和函数满足 $S(-x) = -S(x)$, 再把 $-\frac{1}{2}$ 搬回 $(0,1)$ 内判断是不是连续点即可. 在 $[0,1]$ 上作奇延拓 (再以 2 为周期延拓) 后, $S(x)$ 就是延拓函数的傅里叶级数的和函数. 由奇性
>
> $$S\left(-\frac{1}{2}\right)=-S\left(\frac{1}{2}\right).$$
>
> 而 $x=\frac{1}{2}$ 落在 $(0,1)$ 内部，是 $f(x)=x^{2}$ 的连续点，由狄利克雷收敛定理
>
> $$S\left(\frac{1}{2}\right)=f\left(\frac{1}{2}\right)=\frac{1}{4}.$$
>
> 所以
>
> $$S\left(-\frac{1}{2}\right)=-\frac{1}{4}.$$
>
> 「正弦级数 / 余弦级数」实际上是把函数先作奇延拓 / 偶延拓再展开. 求 $S(x_0)$ 时先用奇偶性与周期性把 $x_0$ 搬回原区间, 再看它是连续点还是间断点, 这样完全不用算积分.

**2.** （难度：★）设函数

$$f(x)=\left\{\begin{aligned}&x^{2},&0\leqslant x\leqslant\frac{1}{2},\\ &1-x,&\frac{1}{2}<x\leqslant1\end{aligned}\right.$$

的余弦级数 $\frac{a_{0}}{2}+\sum_{n=1}^{\infty}a_{n}\cos n\pi x\left(-\infty<x<+\infty\right)$，对应的和函数为 $S(x)$，其中 $a_{n}=2\int_{0}^{1}f(x)\cos n\pi x dx(n\geqslant1)$. 求 $S(x)$ 在 $x=-\frac{9}{2}$ 处的函数值.

> [!answer]- 原书参考答案（A.8.4 第 2 题，未逐题独立验算）
> **2.** 余弦级数对应偶延拓，周期为2. 用 $S(-x) = S(x)$ 与 $S(x + 2) = S(x)$ 把 $-\frac{9}{2}$ 搬到基本区间 $(0,1)$ 内的 $\frac{1}{2}$，再看这一点是不是间断点. 余弦级数对应 $f(x)$ 的偶延拓，其和函数 $S(x)$ 是偶函数，且以2为周期. 于是
>
> $$S\left(-\frac{9}{2}\right)=S\left(-\frac{9}{2}+2\times2\right)=S\left(-\frac{1}{2}\right)=S\left(\frac{1}{2}\right).$$
>
> 在 $x = \frac{1}{2}$ 处 $f(x)$ 有跳跃: 左极限为
>
> $$f\left(\frac{1}{2}^{-}\right)=\left(\frac{1}{2}\right)^{2}=\frac{1}{4},$$
>
> 右极限为
>
> $$f\left(\frac{1}{2}^{+}\right)=1-\frac{1}{2}=\frac{1}{2}.$$
>
> 由狄利克雷收敛定理，
>
> $$S\left(\frac{1}{2}\right)=\frac{f\left(\frac{1}{2}^{-}\right)+f\left(\frac{1}{2}^{+}\right)}{2}=\frac{\frac{1}{4}+\frac{1}{2}}{2}=\frac{3}{8}.$$
>
> 所以 $S\left(-\frac{9}{2}\right)=\frac{3}{8}$. 本题两个「坑」: 一是要用周期性把 $\frac{9}{2}$ 化简成 $\frac{1}{2}$，二是 $\frac{1}{2}$ 恰好是分段点，必须取左右极限的平均而不是函数值.

**3.** (难度:★★★)

(1) 将 $[-π, π)$ 上的函数 $f(x) = |x|$ 展开成 Fourier 级数，并证明 $\sum_{k=1}^{\infty} \frac{1}{k^2} = \frac{π^2}{6}$.

(2）求积分 $I=\int_{0}^{+\infty}\frac{u}{1+e^{u}}du$

> [!answer]- 原书参考答案（A.8.4 第 3 题，未逐题独立验算）
> **3.** (1) $|x|$ 是偶函数, 只用算 $a_n$, 展开后在 $x=0$ 处代入即可得到奇数项的和, 再补上偶数项. (2) 先把 $\frac{1}{1+e^u}$ 写成 $\frac{e^{-u}}{1+e^{-u}}$, 用几何级数展开后逐项积分. (1) $f(x)=|x|$ 为偶函数, $b_n=0$, 且
>
> $$a_{0}=\frac{1}{\pi}\int_{-\pi}^{\pi}\left|x\right|\mathrm{d}x=\frac{1}{\pi}\cdot\pi^{2}=\pi,$$
>
> $$a_{n}=\frac{2}{\pi}\int_{0}^{\pi}x\cos nx\mathrm{d}x=\frac{2}{\pi}\cdot\frac{(-1)^{n}-1}{n^{2}}=\left\{\begin{aligned}&-\frac{4}{\pi n^{2}},&n 为奇数 ,\\ &0,&n 为偶数 .\end{aligned}\right.$$
>
> 所以
>
> $$|x|=\frac{\pi}{2}-\frac{4}{\pi}\sum_{m=1}^{\infty}\frac{\cos(2m-1)x}{(2m-1)^{2}}\qquad(-\pi\leqslant x\leqslant\pi).$$
>
> 在其中取 x=0: 左端为 0, 于是
>
> $$0=\frac{\pi}{2}-\frac{4}{\pi}\sum_{m=1}^{\infty}\frac{1}{(2m-1)^{2}}\quad\Longrightarrow\quad\sum_{m=1}^{\infty}\frac{1}{(2m-1)^{2}}=\frac{\pi^{2}}{8}.$$
>
> 记 $A=\sum_{k\geq1}\frac{1}{k^{2}}$，把它按奇偶项拆开：奇数项之和为 $\frac{\pi^{2}}{8}$，偶数项之和为 $\frac{1}{4}A$，故
>
> $$A=\frac{\pi^{2}}{8}+\frac{1}{4}A\quad\Longrightarrow\quad A=\frac{\pi^{2}}{6}.$$
>
> (2) 对 u > 0 有 $\frac{1}{1 + e^{u}} = \frac{e^{-u}}{1 + e^{-u}} = \sum_{n=1}^{\infty}(-1)^{n-1}e^{-nu}$，逐项积分：
>
> $$I=\int_{0}^{+\infty}\frac{u}{1+\mathrm{e}^{u}}\mathrm{d}u=\sum_{n=1}^{\infty}(-1)^{n-1}\int_{0}^{+\infty}u\mathrm{e}^{-n u}\mathrm{d}u=\sum_{n=1}^{\infty}\frac{(-1)^{n-1}}{n^{2}}.$$
>
> 由(1)的结论（把 $x^{2}$ 的展开在0处取值） $\sum_{n=1}^{\infty}\frac{(-1)^{n-1}}{n^{2}}=\frac{\pi^{2}}{12}$，所以
>
> $$I=\frac{\pi^{2}}{12}.$$
>
> (1) 里 $\sum\frac{1}{(2m-1)^2}=\frac{\pi^2}{8}$ 是「奇偶拆分法」的标准用法: 由奇数项之和反解出 $\zeta(2)$，避免再算一遍傅里叶系数.

**4.** (难度:★★★★) 将函数 $f(x)=x(\pi-x)$ 在 $[0,\pi]$ 上展成正弦级数，并利用所得结果求积分 $\int_{0}^{1}\frac{\ln^{2}x}{1+x^{2}}dx$.

> [!answer]- 原书参考答案（A.8.4 第 4 题，未逐题独立验算）
> **4.** 先按正弦级数的公式算 $b_{n}$ (两次分部积分), 再把 $x = \frac{\pi}{2}$ 代入得到 $\beta(3) = \sum \frac{(-1)^{m-1}}{(2m-1)^3}$; 最后用 $x = e^{-t}$ 把所求积分化成同一个级数. 第一步: 算 $b_{n}$.
>
> $$b_{n}=\frac{2}{\pi}\int_{0}^{\pi}x(\pi-x)\sin nx\mathrm{d}x.$$
>
> 先算两个基本积分：
>
> $$\int_{0}^{\pi}x\sin nx\mathrm{d}x=-\frac{\pi(-1)^{n}}{n},\qquad\int_{0}^{\pi}x^{2}\sin nx\mathrm{d}x=-\frac{\pi^{2}(-1)^{n}}{n}+\frac{2\left[(-1)^{n}-1\right]}{n^{3}}.$$
>
> 于是
>
> $$\int_{0}^{\pi}x(\pi-x)\sin nx\mathrm{d}x=\pi\int_{0}^{\pi}x\sin nx\mathrm{d}x-\int_{0}^{\pi}x^{2}\sin nx\mathrm{d}x=\frac{2\left[1-(-1)^{n}\right]}{n^{3}},$$
>
> 所以
>
> $$b_{n}=\frac{4\left[1-(-1)^{n}\right]}{\pi n^{3}}=\left\{\begin{aligned}&\frac{8}{\pi n^{3}},&n 为奇数 ,\\ &0,&n 为偶数 .\end{aligned}\right.$$
>
> 因此
>
> $$x(\pi-x)=\frac{8}{\pi}\sum_{m=1}^{\infty}\frac{\sin(2m-1)x}{(2m-1)^{3}}\qquad(0\leqslant x\leqslant\pi).$$
>
> 第二步：取 $x = \frac{\pi}{2}$. 此时 $\sin\frac{(2m-1)\pi}{2} = (-1)^{m-1}$，左端为 $\frac{\pi^{2}}{4}$，故
>
> $$\frac{\pi^{2}}{4}=\frac{8}{\pi}\sum_{m=1}^{\infty}\frac{(-1)^{m-1}}{(2m-1)^{3}}\quad\Longrightarrow\quad\sum_{m=1}^{\infty}\frac{(-1)^{m-1}}{(2m-1)^{3}}=\frac{\pi^{3}}{32}.$$
>
> 第三步: 算积分. 作替换 $x = e^{-t}$ ( $t: 0 \to +\infty$, $\mathrm{d}x = -e^{-t} \mathrm{d}t$, $\ln x = -t$):
>
> $$\int_{0}^{1}\frac{\ln^{2}x}{1+x^{2}}\mathrm{d}x=\int_{0}^{+\infty}\frac{t^{2}\mathrm{e}^{-t}}{1+\mathrm{e}^{-2t}}\mathrm{d}t=\sum_{n=0}^{\infty}(-1)^{n}\int_{0}^{+\infty}t^{2}\mathrm{e}^{-(2n+1)t}\mathrm{d}t.$$
>
> 因为 $\int_{0}^{+\infty}t^{2}e^{-(2n+1)t}dt=\frac{2}{(2n+1)^{3}}$，所以
>
> $$\int_{0}^{1}\frac{\ln^{2}x}{1+x^{2}}\mathrm{d}x=2\sum_{n=0}^{\infty}\frac{(-1)^{n}}{(2n+1)^{3}}=2\cdot\frac{\pi^{3}}{32}=\frac{\pi^{3}}{16}.$$
>
> 本题体现了傅里叶级数的第二个用途: 用它算出某个数项级数的和, 再把别的积分(数列)化成这个级数. 第二步选点是关键——取 $x = \frac{\pi}{2}$ 才能让 $\sin \frac{(2m-1)\pi}{2}$ 变成 $\pm1$.

**5.** (难度:★★★★) 将定义在 $[-π, π)$ 上的函数 $y(x) = \sin(zx)$ ( $z \neq 0$) 进行周期为 $2π$ 的傅里叶展开, 并由此证明:

$$\frac{\sin\pi z}{\pi z}+\frac{\sin\pi z}{\pi}\sum_{n=1}^{\infty}\frac{2(-1)^{n}z}{z^{2}-n^{2}}=1.$$

> [!answer]- 原书参考答案（A.8.4 第 5 题，未逐题独立验算）
> > [!warning] AI 补充：原题与答案所用函数不一致
> > 原书第 41 页第 5 题写的是 $y(x)=\sin(zx)$，而附录 A.8.4 第 5 题按 $\cos(zx)$ 展开。此处及答案均保留原书内容，函数及参数适用范围需进一步核验。
>
> **5.** $\cos z x$ 是偶函数, 只用算余弦系数. 算出 $a_n$ 后在 $x = 0$ 处代入, 就得到所需恒等式. 设 $f(x) = \cos z x$, 其中 $z \ne 0$ 且 $z \notin \mathbb{Z}$. 它是偶函数, 故 $b_n = 0$, 且
>
> $$a_{0}=\frac{2}{\pi}\int_{0}^{\pi}\cos z x\mathrm{d}x=\frac{2\sin\pi z}{\pi z}.$$
>
> 当 $n \geqslant 1$时，用积化和差：
>
> $$\begin{aligned}a_{n}&=\frac{2}{\pi}\int_{0}^{\pi}\cos zx\cos nx\mathrm{d}x\\&=\frac{1}{\pi}\int_{0}^{\pi}\left[\cos(z-n)x+\cos(z+n)x\right]\mathrm{d}x\\&=\frac{1}{\pi}\left[\frac{\sin(z-n)\pi}{z-n}+\frac{\sin(z+n)\pi}{z+n}\right].\\ \end{aligned}$$
>
> 注意 $\sin(z \pm n)\pi = \sin\pi z\cos n\pi = (-1)^n\sin\pi z$，于是
>
> $$\begin{aligned}a_{n}&=\frac{(-1)^{n}\sin\pi z}{\pi}\left(\frac{1}{z-n}+\frac{1}{z+n}\right)\\&=\frac{2z(-1)^{n}\sin\pi z}{\pi\left(z^{2}-n^{2}\right)}.\end{aligned}$$
>
> 所以
>
> $$\begin{aligned}\cos z x&=\frac{\sin\pi z}{\pi z}\\&\quad+\frac{\sin\pi z}{\pi}\sum_{n=1}^{\infty}\frac{2(-1)^{n}z\cos n x}{z^{2}-n^{2}}\quad(-\pi<x<\pi).\end{aligned}$$
>
> 在上式中取 x=0: 左端为 1, $\cos nx=1$, 即得
>
> $$\frac{\sin\pi z}{\pi z}+\frac{\sin\pi z}{\pi}\sum_{n=1}^{\infty}\frac{2(-1)^{n}z}{z^{2}-n^{2}}=1.$$
>
> 把恒等式两边同乘 $\frac{\pi}{\sin\pi z}$，它就变成经典的余割部分分式
>
> $$\frac{\pi}{\sin\pi z}=\frac{1}{z}+2z\sum_{n\geqslant1}\frac{(-1)^{n}}{z^{2}-n^{2}}.$$
>
> 记忆时可以只记这一条, 考场上再乘 $\frac{\sin\pi z}{\pi}$ 还原.

**6.** (难度：★★★★★) 设 $f(x)$ 是以 $2\pi$ 为周期的连续函数, 已知 $f(x)$ 的 Fourier 系数为 $a_{n}$, $b_{n}$. 令 $F(x) = \frac{1}{\pi} \int_{-\pi}^{\pi} f(t) f(x + t) dt$. 求函数 $F(x)$ 的 Fourier 系数, 并利用结果证明：

$$\frac{1}{\pi}\int_{-\pi}^{\pi}f^{2}(x)\mathrm{d}x=\frac{a_{0}^{2}}{2}+\sum_{n=1}^{\infty}(a_{n}^{2}+b_{n}^{2}).$$

> [!answer]- 原书参考答案（A.8.4 第 6 题，未逐题独立验算）
> **6.** 递推式两边都含 n，把 $na_n$ 认成 $xS'(x)$ 的系数、 $a_{n-1}$ 认成 $xS(x)$ 的系数，就能得到 S 的可分离微分方程。设 $S(x) = \sum_{n=0}^{\infty} a_nx^n$，则 $xS'(x) = \sum_{n \geq 0} na_nx^n$。由
>
> $$na_{n}=\frac{2}{3}a_{n-1}-(n-1)a_{n-1}\qquad(n\geqslant2)$$
>
> 两边乘 $x^{n}$并对 $n\geqslant2$求和：
>
> $$\sum_{n\geqslant2}na_{n}x^{n}=\frac{2}{3}\sum_{n\geqslant2}a_{n-1}x^{n}-\sum_{n\geqslant2}(n-1)a_{n-1}x^{n}.$$
>
> 左端 = $xS'(x) - a_{1}x = xS'(x) - 5x$; 右端第一项 = $\frac{2}{3}x(S-3)$; 右端第二项, 令 m = n - 1 得
>
> $$\sum_{n\geqslant2}(n-1)a_{n-1}x^{n}=x\sum_{m\geqslant1}m a_{m}x^{m}=x^{2}S^{\prime}(x).$$
>
> 所以
>
> $$x S^{\prime}-5x=\frac{2}{3}x\left(S-3\right)-x^{2}S^{\prime},$$
>
> 两边除以x并整理：
>
> $$\left(1+x\right)S^{\prime}=3+\frac{2}{3}S,\qquad S(0)=a_{0}=3.$$
>
> 分离变量：
>
> $$\frac{\mathrm{d}S}{3+\frac{2}{3}S}=\frac{\mathrm{d}x}{1+x}\quad\Longrightarrow\quad\frac{3}{2}\ln\left(3+\frac{2}{3}S\right)=\ln(1+x)+C.$$
>
> 由 $S(0)=3$ 得 $\frac{3}{2}\ln5=C$，即
>
> $$\ln\frac{3+\frac{2}{3}S}{5}=\frac{2}{3}\ln(1+x)\quad\Longrightarrow\quad3+\frac{2}{3}S=5(1+x)^{2/3},$$
>
> 故
>
> $$\sum_{n=0}^{\infty}a_{n}x^{n}=\frac{3}{2}\left[5(1+x)^{2/3}-3\right].$$
>
> 检验: $S(0) = \frac{3}{2}(5 - 3) = 3 = a_{0}, S'(x) = 5(1 + x)^{-1/3}, S'(0) = 5 = a_{1}$，与题设一致. 解出 S 后一定用 $S(0) = a_{0}$ 与 $S'(0) = a_{1}$ 回代检验, 这一步既能定常数, 也能及时发现系数整理时的错误.

**7.** (难度：★★★★★) 设 $f(x)$ 在 $\mathbb{R}$ 上可导, 且满足 $f(x) = f(x + 2) = f(x + \sqrt{3})$, 用 Fourier 级数理论证明 $f(x)$ 为常数.

> [!answer]- 原书参考答案（A.8.4 第 7 题，未逐题独立验算）
> **7.** $f(x)$ 以2为周期,可以展开成周期为2的傅里叶级数; $\left[\hat{f}(x)=f(x+\sqrt{3})\right]$ 这一条会对系数产生一组线性方程. 把 $a_{n},b_{n}$ 看成二维向量,方程组就是 $(E-A_{n})X_{n}=0$, 只要证明系数行列式不为零,函数就只能是常数. 第一步:写出周期为2的傅里叶展开. 因为 $f(x)$ 以2为周期、在 $\mathbb{R}$ 上可导,其傅里叶级数在 $\mathbb{R}$ 上一致收敛,且
>
> $$f(x)=\frac{a_{0}}{2}+\sum_{n=1}^{\infty}\left(a_{n}\cos n\pi x+b_{n}\sin n\pi x\right),$$
>
> 其中
>
> $$a_{n}=\int_{-1}^{1}f(t)\cos n\pi t\mathrm{d}t,\quad b_{n}=\int_{-1}^{1}f(t)\sin n\pi t\mathrm{d}t.$$
>
> 第二步：把 x 换成 $x + \sqrt{3}$. 利用和角公式：
>
> $$\begin{aligned}f(x+\sqrt{3})&=\frac{a_{0}}{2}+\sum_{n\geqslant1}\left[a_{n}\cos\left(n\pi x+n\pi\sqrt{3}\right)\right.\\&\quad\left.+b_{n}\sin\left(n\pi x+n\pi\sqrt{3}\right)\right]\\&=\frac{a_{0}}{2}+\sum_{n\geqslant1}\left[\left(a_{n}\cos n\pi\sqrt{3}+b_{n}\sin n\pi\sqrt{3}\right)\cos n\pi x\right.\\&\quad\left.+\left(b_{n}\cos n\pi\sqrt{3}-a_{n}\sin n\pi\sqrt{3}\right)\sin n\pi x\right].\end{aligned}$$
>
> 第三步: 比较系数, 写成矩阵方程. 由 $f(x + \sqrt{3}) = f(x)$, 两边傅里叶系数对应相等:
>
> $$a_{n}=a_{n}\cos n\pi\sqrt{3}+b_{n}\sin n\pi\sqrt{3},$$
>
> $$b_{n}=b_{n}\cos n\pi\sqrt{3}-a_{n}\sin n\pi\sqrt{3}.$$
>
> 记
>
> $$X_{n}=\begin{pmatrix}a_{n}\\ b_{n}\end{pmatrix},\quad A_{n}=\begin{pmatrix}\cos n\pi\sqrt{3}&\sin n\pi\sqrt{3}\\ -\sin n\pi\sqrt{3}&\cos n\pi\sqrt{3}\end{pmatrix},$$
>
> 则上式即 $X_{n}=A_{n}X_{n}$，亦即 $(E-A_{n})X_{n}=0$。只需证 $\left|E-A_{n}\right|\neq0$。
>
> 第四步：计算行列式并说明非零.
>
> $$E-A_{n}=\begin{pmatrix}1-\cos n\pi\sqrt{3}&-\sin n\pi\sqrt{3}\\ \sin n\pi\sqrt{3}&1-\cos n\pi\sqrt{3}\end{pmatrix},$$
>
> $$\begin{aligned}\left|\boldsymbol{E}-\boldsymbol{A}_{n}\right|&=\left(1-\cos n\pi\sqrt{3}\right)^{2}+\sin^{2}n\pi\sqrt{3}\\&=1+\cos^{2}n\pi\sqrt{3}-2\cos n\pi\sqrt{3}+\sin^{2}n\pi\sqrt{3}\\&=2(1-\cos n\pi\sqrt{3}).\end{aligned}$$
>
> 假设 $|E - A_n| = 0$，则 $\cos n\pi\sqrt{3} = 1$，即 $n\pi\sqrt{3} = 2k\pi$ ( $k \in \mathbb{Z}$)，于是 $\sqrt{3} = 2k/n \in \mathbb{Q}$，与 $\sqrt{3}$ 是无理数矛盾。故 $|E - A_n| \ne 0$，从而
>
> > [!warning] AI 补充：原书答案末尾缺失
> > 原书第 228 页第 7 题在“故 $|E-A_n|\ne0$，从而”处结束，下一页直接进入“第三部分 强化篇答案”。原 PDF 此处也未给出后续结论，不是整理时删去，暂不补造。

---

# 第二部分 强化篇

---

# 强化篇·第一章 一元极限

## 1.1 常规数列处理

数列极限中，有相当一类的考题，都需要紧密结合高中数列的处理思路，配方，取倒数，裂项，三角换元，这些技巧已在高中阶段频繁接触，故不再赘述。

**1.** (难度:★★) 设数列 $\{x_{n}\}$ 满足 $x_{1}=\frac{1}{2}$， $x_{n+1}=x_{n}^{2}+x_{n}$ ( $n\geqslant1$)。求极限：

$$\lim_{n\to\infty}\left(\frac{1}{1+x_{1}}+\frac{1}{1+x_{2}}+\cdots+\frac{1}{1+x_{n}}\right).$$

> [!answer]- 原书参考答案（B.0.1 第 1 题，未逐题独立验算）
> **1.** 递推式右边可以因式分解: $x_{n+1} = x_n(x_n + 1)$. 这个“乘积”结构正好让 $\frac{1}{1 + x_n}$ 裂成两个倒数之差, 求和即可望远镜相消. 由 $x_{n+1} = x_n^2 + x_n = x_n(x_n + 1)$ 得
>
> $$\frac{1}{1+x_{n}}=\frac{1}{x_{n}}-\frac{1}{x_{n+1}}.$$
>
> 于是
>
> $$\sum_{k=1}^{n}\frac{1}{1+x_{k}}=\frac{1}{x_{1}}-\frac{1}{x_{n+1}}=2-\frac{1}{x_{n+1}}.$$
>
> 又 $x_{n+1}=x_{n}(x_{n}+1)>x_{n}>0$ ，故 $\{x_{n}\}$ 递增. 若它有上界，则收敛，设极限为 L，在递推式两边取极限得 $L=L^{2}+L$ ，即 L=0 ；但 $x_{n}\geqslant x_{1}=\frac{1}{2}$ 恒成立，矛盾. 所以 $x_{n}\rightarrow\infty$ ，从而 $\frac{1}{x_{n+1}}\rightarrow0$ ，故
>
> $$\lim_{n\to\infty}\sum_{k=1}^{n}\frac{1}{1+x_{k}}=2.$$
>
> 本节的“取倒数”用在这里，是为了裂项：先看出 $x_{n+1}$是两个相邻项的乘积，再取倒数才能把 $\frac{1}{1+x_n}$拆成 $\frac{1}{x_n}-\frac{1}{x_{n+1}}$。若直接对原式求和是算不出来的。

**2.** (难度:★★) 记 $a_{n} = \sqrt{2 - \sqrt{2 + \sqrt{2 + \cdots + \sqrt{2}}}}$ (n 重根号), 求极限 $\lim_{n \to \infty} 2^{n} a_{n}$.

> [!answer]- 原书参考答案（B.0.1 第 2 题，未逐题独立验算）
> **2.** 第一步：找递推关系. 把 $a_{n+1}$ 中最内层的 n-1 重根号记为 c，则
>
> $$a_{n}=\sqrt{2-c},\qquad a_{n+1}=\sqrt{2-\sqrt{2+c}}.$$
>
> 由第一式得 $c=2-a_{n}^{2}$，代入第二式得
>
> $$a_{n+1}=\sqrt{2-\sqrt{4-a_{n}^{2}}}\qquad(a_{1}=\sqrt{2}).$$
>
> 第二步: 三角换元. 因为 $0 < a_{n} \leqslant \sqrt{2} < 2$, 可设
>
> $$a_{n}=2\sin\theta_{n},\qquad\theta_{n}\in\left(0,\frac{\pi}{4}\right].$$
>
> 此时 $\sqrt{4-a_{n}^{2}}=2\cos\theta_{n}$，代入递推式得
>
> $$a_{n+1}=\sqrt{2-2\cos\theta_{n}}=2\sin\frac{\theta_{n}}{2},$$
>
> 即 $\theta_{n+1}=\frac{\theta_{n}}{2}$
>
> 第三步：求通项。由 $a_{1}=\sqrt{2}=2\sin\frac{\pi}{4}$得 $\theta_{1}=\frac{\pi}{4}$，故
>
> $$\theta_{n}=\frac{\pi}{2^{n+1}},\qquad a_{n}=2\sin\frac{\pi}{2^{n+1}}.$$
>
> 第四步: 求极限. 利用 $\sin t \sim t (t \to 0)$,
>
> $$\lim_{n\to\infty}2^{n}a_{n}=\lim_{n\to\infty}2^{n+1}\sin\frac{\pi}{2^{n+1}}=\pi.$$

**3.** (难度:★) 设数列 $\{x_{n}\}$ 定义为 $x_{1}=1, x_{2}=2$，且 $x_{n+2}=\sqrt{x_{n}x_{n+1}}, n=1,2,\cdots$。证明极限 $\lim_{n\to\infty}x_n$ 存在并求其值。

> [!answer]- 原书参考答案（B.0.1 第 3 题，未逐题独立验算）
> **3.** 由 $x_{1}=1>0, x_{2}=2>0$ 及递推式知 $x_{n}>0$，故可以取对数.
>
> 第一步：取对数，化为线性递推. 令 $b_{n} = \ln x_{n}$，则
>
> $$b_{n+2}=\ln\sqrt{x_{n}x_{n+1}}=\frac{b_{n}+b_{n+1}}{2},\qquad 即 \qquad2b_{n+2}=b_{n+1}+b_{n}.$$
>
> 第二步：用特征根法求通项. 特征方程为 $2r^{2}=r+1$ ，即
>
> $$2r^{2}-r-1=0\implies r_{1}=1,\qquad r_{2}=-\frac{1}{2}.$$
>
> 两根不等，故
>
> $$b_{n}=C_{1}\cdot1^{n}+C_{2}\left(-\frac{1}{2}\right)^{n}.$$
>
> 由 $b_{1}=\ln1=0$ 、 $b_{2}=\ln2$ 得
>
> $$C_{1}-\frac{C_{2}}{2}=0,\qquad C_{1}+\frac{C_{2}}{4}=\ln2,$$
>
> 解得 $C_{1}=\frac{2}{3}\ln2$, $C_{2}=\frac{4}{3}\ln2$.
>
> 第三步: 求极限. 因为 $\left|-\frac{1}{2}\right|<1$, 故 $\left(-\frac{1}{2}\right)^{n}\to0$, 从而
>
> $$b_{n}\longrightarrow\frac{2}{3}\ln2=\ln2^{\frac{2}{3}},$$
>
> 即极限存在，且
>
> $$\lim_{n\to\infty}x_{n}=2^{\frac{2}{3}}.$$

**4.** (难度:★★) 设数列 $\{a_{n}\}$ 满足 $a_{1}=1, a_{n+1}=\frac{a_{n}}{(n+1)(a_{n}+1)}$. 求 $\lim_{n\to\infty}n!a_{n}$.

> [!answer]- 原书参考答案（B.0.1 第 4 题，未逐题独立验算）
> **4.** 第一步：凑出新数列. 待求的是 $n!a_{n}$，故记 $b_{n}=n!a_{n}$. 把递推式两边同乘 $(n+1)!$:
>
> $$(n+1)!a_{n+1}=\frac{(n+1)!a_{n}}{(n+1)(a_{n}+1)}=\frac{n!a_{n}}{a_{n}+1},$$
>
> 即
>
> $$b_{n+1}=\frac{b_{n}}{a_{n}+1},\qquad a_{n}=\frac{b_{n}}{n!}.$$
>
> 第二步：取倒数.
>
> $$\frac{1}{b_{n+1}}=\frac{a_{n}+1}{b_{n}}=\frac{1}{b_{n}}+\frac{a_{n}}{b_{n}}=\frac{1}{b_{n}}+\frac{1}{n!}.$$
>
> 第三步：累加求和. 由 $b_{1}=1!\cdot a_{1}=1$ 得
>
> $$\frac{1}{b_{n}}=\frac{1}{b_{1}}+\sum_{k=1}^{n-1}\frac{1}{k!}=\sum_{k=0}^{n-1}\frac{1}{k!},$$
>
> 故
>
> $$b_{n}=\frac{1}{\sum\limits_{k=0}^{n-1}\frac{1}{k!}}\longrightarrow\frac{1}{e},$$
>
> 即 $\lim_{n\to\infty}n!a_n=\frac{1}{e}$

**5.** (难度:★★★★) 设 $f(x)$ 为仅有正实数根的多项式函数, $\frac{f'(x)}{f(x)} = -\sum_{n=0}^{\infty} C_{n} x^{n}$. 证明: $C_{n} > 0$, 极限 $\lim_{n \to \infty} \frac{1}{\sqrt[n]{C_n}}$ 存在, 并求出该极限.

> [!answer]- 原书参考答案（B.0.1 第 5 题，未逐题独立验算）
> **5.** $f(x)$ 只有正实根（设最小根为 $M_1$，重数为 $P$），把 $\frac{f'(x)}{f(x)}$ 按部分分式展开，就能把 $C_n$ 写成“各根的负 $n+1$ 次幂之和”，从而用最小根夹逼出 $\sqrt[n]{C_n}$ 的极限。设 $f(x)$ 的正根为 $0 < \gamma_1 \leq \gamma_2 \leq \cdots \leq \gamma_m$，记 $M_1 = \min\{\gamma_1, \ldots, \gamma_m\}$，并设最小根是 $P$ 重根（ $P \geq 1$）。写成
>
> $$f(x)=A\prod_{i=1}^{m}(x-\gamma_{i}),$$
>
> 其中 $A \neq 0$.由
>
> $$\frac{f^{\prime}(x)}{f(x)}=\sum_{k=1}^{m}\frac{1}{x-\gamma_{k}}=-\sum_{k=1}^{m}\frac{1}{\gamma_{k}}\cdot\frac{1}{1-\frac{x}{\gamma_{k}}}=-\sum_{n=0}^{+\infty}\left(\sum_{k=1}^{m}\frac{1}{\gamma_{k}^{n+1}}\right)x^{n}$$
>
> （收敛半径即 $M_{1}$，故对 $|x|<M_{1}$ 的展开合法），与题设 $\frac{f'(x)}{f(x)}=-\sum_{n=0}^{+\infty}C_{n}x^{n}$ 比较系数得
>
> $$C_{n}=\sum_{k=1}^{m}\frac{1}{\gamma_{k}^{n+1}}>0.$$
>
> 下面估计 $C_{n}$ 的上、下界. 由于各 $\gamma_{k} \geqslant M_{1}$，有 $\frac{1}{\gamma_{k}^{n+1}} \leqslant \frac{1}{M_{1}^{n+1}}$，故
>
> $$C_{n}\leq\frac{m}{M_{1}^{n+1}};$$
>
> 另一方面，最小根有 P 个（重根也计入），每一项都等于 $\frac{1}{M_{1}^{n+1}}$，故
>
> $$C_{n}\geq\frac{P}{M_{1}^{n+1}}.$$
>
> 两边开n次方：
>
> $$\frac{P^{1/n}}{M_{1}^{1+1/n}}\leqslant C_{n}^{1/n}\leqslant\frac{m^{1/n}}{M_{1}^{1+1/n}}.$$
>
> 令 $n \to \infty$，由 $P^{1/n} \to 1$、 $m^{1/n} \to 1$、 $M_{1}^{1/n} \to 1$ 及夹逼定理，
>
> $$\lim_{n\to\infty}\sqrt[n]{C_{n}}=\frac{1}{M_{1}},\qquad 即 \qquad\lim_{n\to\infty}\frac{1}{\sqrt[n]{C_{n}}}=M_{1}.$$
>
> 关键有两处: 一是把 $\frac{f'}{f}$ 拆成 $\sum \frac{1}{x - \gamma_k}$ 后展开成幂级数; 二是用最小根夹逼——最小根 (即使有重根) 提供的项在 $n \to \infty$ 时“最大”, 其余各项相对于它高阶小, 所以极限只由最小根决定. 写的时候要说明“重根按重数计入”, 也就是这里的 P.

**6.** (难度：★★★★★) 设数列 $\{a_{n}\}$ 满足 $a_{1} = \frac{\pi}{2}$, $a_{n+1} = a_{n} - \frac{\sin a_{n}}{n+1}$, $n \geqslant 1$. 求证:数列 $\{na_{n}\}$ 收敛.

> [!answer]- 原书参考答案（B.0.1 第 6 题，未逐题独立验算）
> **6.** 要证 $\{na_{n}\}$ 收敛, 自然先看它的单调性: 由 $(n+1)a_{n+1}-na_{n}=a_{n}-\sin a_{n}>0$ 知它单调递增, 所以只需再证它有上界. 上界可以从“ $a_{n}$ 衰减得足够快”得到 (方法二), 也可以用倒数的差分求和来估计 (方法一). 第一步: $a_{n}$ 单调递减趋于 0, 且 $a_{n}\in\left(0,\frac{\pi}{2}\right]$. 由
>
> $$a_{n+1}-a_{n}=-\frac{\sin a_{n}}{n+1}<0$$
>
> 知$\{a_n\}$递减;又$a_{n+1} \geqslant a_n\left(1 - \frac{1}{n+1}\right) = \frac{n}{n+1}a_n > 0$,故$a_n \in\left(0, \frac{\pi}{2}\right]$恒成立,
>
> 从而$a_n \to A \geqslant 0$.若$A > 0$,则存在$N$,当$n > N$时$a_n > \frac{A}{2}$,于是
>
> $$a_{n+1}-a_{n}<-\sin\frac{A}{2}\cdot\frac{1}{n+1},$$
>
> 累加得 $a_{n+1} < a_N - \sin \frac{A}{2} \sum_{k=N}^{n} \frac{1}{k+1} \to -\infty$，与 $a_n > 0$ 矛盾。故 A = 0。
>
> 方法一：倒数差分. 由 $(n+1)a_{n+1}-na_n=a_n-\sin a_n>0$知 $\{na_n\}$单调递增. 又 $a_n-\sin a_n<\frac{1}{6}a_n^3$，且 $a_{n+1}>\frac{n}{n+1}a_n$，故
>
> $$\frac{1}{na_{n}}-\frac{1}{(n+1)a_{n+1}}=\frac{(n+1)a_{n+1}-na_{n}}{n(n+1)a_{n}a_{n+1}}<\frac{\frac{1}{6}a_{n}^{3}}{n(n+1)a_{n}a_{n+1}}<\frac{a_{n}}{6n^{2}}\leqslant\frac{\pi}{12n^{2}}.$$
>
> (最后一步用了 $a_n \leq \frac{\pi}{2}$.) 对 $k = 1, \ldots, n$ 累加:
>
> $$\frac{1}{a_{1}}-\frac{1}{(n+1)a_{n+1}}\leqslant\frac{\pi}{12}\sum_{k=1}^{n}\frac{1}{k^{2}}<\frac{\pi}{12}\cdot\frac{\pi^{2}}{6}=\frac{\pi^{3}}{72}.$$
>
> 于是
>
> $$\frac{1}{(n+1)a_{n+1}}>\frac{1}{a_{1}}-\frac{\pi^{3}}{72}=\frac{2}{\pi}-\frac{\pi^{3}}{72}>0,$$
>
> 即
>
> $$(n+1)a_{n+1}<\frac{1}{\frac{2}{\pi}-\frac{\pi^{3}}{72}}.$$
>
> 所以 $\{na_{n}\}$ 单调递增且有上界，故收敛.
>
> 方法二：先估 $a_{n}$ 的阶，再估 $na_{n}$ 的上界。由 $a_{n}-\sin a_{n}\leqslant\left(1-\frac{2}{\pi}\right)a_{n}$ （因 $\sin a_{n}\geqslant\frac{2}{\pi}a_{n}$ 在 $\left[0,\frac{\pi}{2}\right]$ 上成立），代入 $(n+1)a_{n+1}-na_{n}=a_{n}-\sin a_{n}$ 得
>
> $$\frac{a_{n+1}}{a_{n}}\leqslant1-\frac{2}{\pi}\cdot\frac{1}{n+1},$$
>
> 故
>
> $$a_{n}\leqslant\frac{\pi}{2}\prod_{k=2}^{n}\left(1-\frac{2}{\pi}\cdot\frac{1}{k}\right),$$
>
> 取对数并用 $\ln(1-t) \leq -t$:
>
> $$\ln a_{n}\leqslant\ln\frac{\pi}{2}-\frac{2}{\pi}\sum_{k=2}^{n}\frac{1}{k}<\ln\frac{\pi}{2}-\frac{2}{\pi}\ln n,$$
>
> 即 $a_{n} < \frac{\pi}{2} \cdot \frac{1}{n^{2/\pi}}$.
>
> 再由 $(n+1)a_{n+1}-na_n=a_n-\sin a_n\leqslant\frac{1}{6}a_n^3$累加：
>
> $$(n+1)a_{n+1}\leqslant a_{1}+\frac{1}{6}\sum_{k=1}^{n}a_{k}^{3}\leqslant a_{1}+\frac{1}{6}\cdot\frac{\pi^{3}}{8}\sum_{k=1}^{n}\frac{1}{k^{6/\pi}}.$$
>
> 因为 $\frac{6}{\pi} > 1$，级数 $\sum \frac{1}{k^{6/\pi}}$ 收敛，故存在常数 M > 0，使 $(n+1)a_{n+1} \leqslant M$，即 $\{na_n\}$ 有上界。又已证 $\{na_n\}$ 单调递增，故 $\{na_n\}$ 收敛。两套方法的分工很清楚：方法一直接用 $a_n - \sin a_n < \frac{1}{6}a_n^3$ 对 $\frac{1}{na_n}$ 作差分，靠 $\sum \frac{1}{k^2} < \frac{\pi^2}{6}$ 得到上界；方法二先用 $\sin a_n \geqslant \frac{2}{\pi}a_n$ 把 $a_n$ 估成 $O(n^{-2/\pi})$，于是 $\sum a_k^3$ 收敛（因为 $6/\pi > 1$），再由累加得到 $na_n$ 有上界。两条路都说明：这道题的“难点”其实是对 $a_n$ 衰减速度的估计。

## 1.2 压缩映射

对于 $a_{n+1}=f(a_{n})$ 类型的数列递推求极限，压缩映射是较为通用的方法，除此之外，部分题目也可使用单调有界原则，该类题型是竞赛中的高频考点.

**1.** (难度:★★★) 设 a > 0, $x_{1} > 0$, 定义: $x_{n+1} = \frac{1}{4} \left( 3x_{n} + \frac{a}{x_{n}^{3}} \right)$ ( $n \geqslant 1$). 证明: 极限 $\lim_{n \to \infty} x_{n}$ 存在并求其值.

> [!answer]- 原书参考答案（B.0.2 第 1 题，未逐题独立验算）
> **1.** 这个迭代式是“用牛顿法求 $a^{1/4}$”的公式：不动点满足 $x^{4}=a$ ，即 $x=a^{1/4}$ 。证法有两条路——单调有界（用四元均值不等式拿到下界）与压缩映射（在下界之外估计 $\left|f^{\prime}(x)\right|$，都写一遍。记 $f(x)=\frac{1}{4}\left(3x+\frac{a}{x^{3}}\right)$，则 $x_{n+1}=f(x_{n})$，且由 $x_1>0$ 归纳得 $x_n>0$ 。
>
> 方法一（单调有界）. 由四元均值不等式，
>
> $$x_{n+1}=\frac{x_{n}+x_{n}+x_{n}+\frac{a}{x_{n}^{3}}}{4}\geqslant\left(x_{n}^{3}\cdot\frac{a}{x_{n}^{3}}\right)^{\frac{1}{4}}=a^{\frac{1}{4}},$$
>
> 即 $\{x_n\}$ 有下界 $a^{1/4}$; 又
>
> $$x_{n+1}\leqslant x_{n}\iff\frac{1}{4}\left(3x_{n}+\frac{a}{x_{n}^{3}}\right)\leqslant x_{n}\iff x_{n}^{4}\geqslant a,$$
>
> 而 $x_{n} \geqslant a^{1/4}$ 正是 $x_{n}^{4} \geqslant a$，故 $\{x_{n}\}$ 单调递减有下界，从而收敛。设极限为 $x_{0}$，在递推式两边取极限得 $4x_{0} = 3x_{0} + \frac{a}{x_{0}^{3}}$，即 $x_{0}^{4} = a$，故 $x_{0} = a^{1/4}$。
>
> 方法二 (压缩映射). 在 $x \geqslant a^{1/4}$ 上
>
> $$f^{\prime}(x)=\frac{3}{4}\left(1-\frac{a}{x^{4}}\right)\in\left[0,\frac{3}{4}\right),$$
>
> 取 $M = \frac{3}{4} < 1$，由中值定理 $\left|x_{n+1} - a^{1/4}\right| \leqslant \frac{3}{4} \left|x_n - a^{1/4}\right|$，迭代得 $x_n \to a^{1/4}$.
>
> 综上， $\lim_{n\to\infty}x_n=a^{1/4}$. 两个方法的分工很典型：均值不等式负责“有界” $(x_n\geqslant a^{1/4}$ 既是有下界，也是 $\left|f'(x)\right|\leqslant\frac{3}{4}$的前提)，有了它，单调有界与压缩映射都能收尾.顺带一句：由 $\frac{x_{n+1}-a^{1/4}}{x_n-a^{1/4}}\rightarrow f'(a^{1/4})=0$ 可见牛顿迭代是“超线性收敛”，比一般压缩映射快得多.

**2.** (难度:★★) 设 $x_{1}=2021, x_{n}^{2}-2(x_{n}+1)x_{n+1}+2021=0$, 求 $\lim_{n\to\infty}x_n$.

> [!answer]- 原书参考答案（B.0.2 第 2 题，未逐题独立验算）
> **2.** 条件是“二次方程”的形式，先把 $x_{n+1}$ 解出来，写成 $x_{n+1} = f(x_n)$；再由 $x_1 > 0$ 归纳得到 $x_n > 0$（有界），最后在不动点附近验证 $|f'(x)| < 1$。也可以用单调有界准则：这个 $f(x)$ 恰好是“用牛顿法解 $x^2 + 2x - 2021 = 0$”的迭代式。第一步：把递推式解成显式。由 $x_n^2 - 2(x_n + 1)x_{n+1} + 2021 = 0$ 得
>
> $$x_{n+1}=\frac{x_{n}^{2}+2021}{2(x_{n}+1)}=:f(x_{n}).$$
>
> 由 $x_{1}=2021>0$ ，归纳可得 $x_{n}>0$
>
> 第二步: 求不动点. 解 $x = f(x)$:
>
> $$2x^{2}+2x=x^{2}+2021\quad\Longrightarrow\quad x^{2}+2x-2021=0\quad\Longrightarrow\quad x_{0}=-1+\sqrt{2022}$$
>
> （另一根为负，舍去）.
>
> 第三步：验证压缩条件并估计范围. 直接计算
>
> $$f^{\prime}(x)=\frac{x^{2}+2x-2021}{2(x+1)^{2}}=\frac{1}{2}\left(1-\frac{2022}{(x+1)^{2}}\right),$$
>
> 它在 x > 0 上单调递增，且 $f'(x_{0}) = 0$。又由
>
> $$f(x)-x=\frac{2021-x^{2}-2x}{2(x+1)}=-\frac{(x-x_{0})(x+x_{0}+2)}{2(x+1)}$$
>
> 可知：当 $x \geqslant x_{0}$ 时 $f(x) \leqslant x$ ，且 $f(x) \geqslant f(x_{0}) = x_{0}$ 。故只要 $x_{1} \geqslant x_{0}$ ，就有
>
> $$x_{1}\geqslant x_{2}\geqslant x_{3}\geqslant\cdots\geqslant x_{0},$$
>
> 数列单调递减有下界，从而收敛，极限必为不动点 $x_{0}$
>
> 第四步：给出结论（也可用压缩映射）。在 $[x_{0},2021]$上
>
> $$|f^{\prime}(x)|\leqslant f^{\prime}(2021)=\frac{1}{2}\left(1-\frac{2022}{2022^{2}}\right)<\frac{1}{2},$$
>
> 取 $M = \frac{1}{2} < 1$，由中值定理 $\left|x_{n+1} - x_0\right| \leqslant M \left|x_n - x_0\right|$，迭代得 $x_n \to x_0$。因此
>
> $$\lim_{n\to\infty}x_{n}=\sqrt{2022}-1.$$
>
> 两个方法 (单调有界、压缩映射) 都能做, 但顺序不要颠倒: 先证有界 (本题是 $x_n > 0$, 并进一步说明 $x_n \in [x_0, 2021]$), 才有资格谈 $|f'(x)|$ 的上界. 注意 $f'(x_0) = 0$, 这正是“牛顿迭代”的特征——不动点处导数为零, 收敛极快.

**3.** (难度:★★) 设数列 $\{x_{n}\}$ 满足 $x_{0}=2, x_{n}=2+\frac{1}{x_{n-1}}, n=1,2,\cdots$. 求 $\lim_{n\to\infty}x_n$.

> [!answer]- 原书参考答案（B.0.2 第 3 题，未逐题独立验算）
> **3.** 第一步：确定数列所在的范围. $x_{0}=2>0$; 若 $x_{n-1}>0$, 则 $x_{n}=2+\frac{1}{x_{n-1}}>2>0$. 由数学归纳法, $x_{n}>2$ 对一切 n 成立.
>
> 第二步: 找不动点. 记 $f(x) = 2 + \frac{1}{x}$, 则 $x_{n} = f(x_{n-1})$, 且 $f(x)$ 在 $[2, +\infty)$ 上连续, 故若极限为 $x_{0}^{*}$, 就应满足
>
> $$x_{0}^{*}=2+\frac{1}{x_{0}^{*}}\quad\Longrightarrow\quad(x_{0}^{*})^{2}-2x_{0}^{*}-1=0\quad\Longrightarrow\quad x_{0}^{*}=1+\sqrt{2}$$
>
> (另一根 $1-\sqrt{2}<0$舍去).
>
> 第三步：验证压缩条件. 在 $[2,+\infty)$上
>
> $$|f^{\prime}(x)|=\frac{1}{x^{2}}\leqslant\frac{1}{4}.$$
>
> 取 $M = \frac{1}{4} < 1$，由拉格朗日中值定理，
>
> $$|x_{n}-x_{0}^{*}|=|f(x_{n-1})-f(x_{0}^{*})|\leqslant\frac{1}{4}|x_{n-1}-x_{0}^{*}|\leqslant\cdots\leqslant\left(\frac{1}{4}\right)^{n}|x_{0}-x_{0}^{*}|.$$
>
> 令 $n\to\infty$,得
>
> $$\lim_{n\to\infty}x_{n}=1+\sqrt{2}.$$

**4.** (难度:★★★★) 设 $a_{1}, b_{1}$ 为任意给定的实数, 数列 $\{a_{n}\}$ 和 $\{b_{n}\}$ 的定义为:

$$\left\{\begin{aligned}a_{n+1}&=\int_{0}^{1}\max\{b_{n},x\}\mathrm{d}x,\\ b_{n+1}&=\int_{0}^{1}\min\{a_{n},x\}\mathrm{d}x,\end{aligned}\right.\quad n=1,2,\cdots.$$

试证明: 数列 $\{a_n\}$ 和 $\{b_n\}$ 都收敛, 且 $\lim_{n \to \infty} a_n = 2 - \sqrt{2}$, $\lim_{n \to \infty} b_n = \sqrt{2} - 1$.

> [!answer]- 原书参考答案（B.0.2 第 4 题，未逐题独立验算）
> **4.** 被积函数 max、min 怎么写，取决于 $b_n$ 与 x、 $a_n$ 与 x 的大小关系，所以第一步必须先把 $a_n, b_n$ 的取值范围定下来，才能去掉 $\max, \min$ 分段积分。第一步：定范围。 $b_{n+1} \leqslant \int_0^1 x \, dx = \frac{1}{2} < 1, a_{n+1} \geqslant \int_0^1 x \, dx = \frac{1}{2}$; 又 $0 \leqslant x \leqslant 1$ 时 $\max\{b_n, x\} \leqslant 1$、 $\min\{a_n, x\} \geqslant 0$，故 $a_{n+1} \leqslant 1, b_{n+1} \geqslant 0$。所以
>
> $$n\geqslant2 时 \quad a_{n}\in\left[\frac{1}{2},1\right],\quad b_{n}\in\left[0,\frac{1}{2}\right].$$
>
> 第二步:去掉 $\max, \min$. 当 $n \geqslant 2$ 时 $b_n \in \left[0, \frac{1}{2}\right]$、 $a_n \in \left[\frac{1}{2}, 1\right]$, 都落在 $[0,1]$ 内, 于是
>
> $$a_{n+1}=\int_{0}^{b_{n}}b_{n}\mathrm{d}x+\int_{b_{n}}^{1}x\mathrm{d}x=\frac{1}{2}b_{n}^{2}+\frac{1}{2},$$
>
> $$b_{n+1}=\int_{0}^{a_{n}}x\mathrm{d}x+\int_{a_{n}}^{1}a_{n}\mathrm{d}x=a_{n}-\frac{1}{2}a_{n}^{2}.$$
>
> 消去 $b_{n}$ （把 n 换成 n-1）得
>
> $$a_{n+1}=f(a_{n-1}),\qquad f(x)=\frac{1}{2}\left(x-\frac{1}{2}x^{2}\right)^{2}+\frac{1}{2},\qquad x\in\left[\frac{1}{2},1\right].$$
>
> 注意得到的是 $a_{n+1}$ 与 $a_{n-1}$ 之间的关系，所以下面要按奇偶分开处理.
>
> 第三步: 奇偶两个子列各自压缩. 由 $f\left(\left[\frac{1}{2},1\right]\right)\subset\left[\frac{1}{2},1\right]$、 $f'(x)=x\left(1-\frac{1}{2}x\right)(1-x)\leqslant\frac{3}{8}$ 及 $f(2-\sqrt{2})=2-\sqrt{2}$ (代入可验), 再结合第一步 $n\geqslant2$ 时 $a_n\in\left[\frac{1}{2},1\right]$, 取
>
> $$c_{n}=a_{2n+1},\qquad d_{n}=a_{2n+2}\qquad(n\geqslant0),$$
>
> 则 $c_{n+1}=f(c_n)$， $d_{n+1}=f(d_n)$，且 $c_0=a_3$， $d_0=a_4$ 都在 $\left[\frac{1}{2},1\right]$ 内.于是
>
> $$\left|c_{n+1}-(2-\sqrt{2})\right|\leqslant\frac{3}{8}\left|c_{n}-(2-\sqrt{2})\right|,$$
>
> $$|d_{n+1}-(2-\sqrt{2})|\leqslant\frac{3}{8}\left|d_{n}-(2-\sqrt{2})\right|,$$
>
> 两个子列都以几何速度收敛到 $2 - \sqrt{2}$，从而整个数列满足 $\lim_{n \to \infty} a_n = 2 - \sqrt{2}$。再由 $b_n = a_{n-1} - \frac{1}{2} a_{n-1}^2 (n \geq 2)$ 取极限：
>
> $$\lim_{n\to\infty}b_{n}=2-\sqrt{2}-\frac{(2-\sqrt{2})^{2}}{2}=\sqrt{2}-1.$$
>
> ”先算范围、再去 $\max / \min$ 、最后压缩映射”是这类题的三段式. 注意 $f(x)$ 在 $\left[\frac{1}{2}, 1\right]$ 上的压缩系数是 $\frac{3}{8}$，比1小得多，所以收敛很快.

**5.** (难度：★★★★★) 设数列 $\{a_{n}\}$ 满足 $a_{n+2} = \sqrt{a_{n+1}} + \sqrt{a_{n}}$, $a_{1} > 0$, $a_{2} > 0$. 证明 $\lim_{n \to \infty} a_{n}$ 存在，并求其值.

> [!answer]- 原书参考答案（B.0.2 第 5 题，未逐题独立验算）
> **5.** 记 $f(x) = \sqrt{x}$，则 $a_{n+2} = f(a_{n+1}) + f(a_n)$，且 $f(4) = 2$。于是
>
> $$|a_{n+2}-4|=|f(a_{n+1})+f(a_{n})-2f(4)|\leqslant|f(a_{n+1})-f(4)|+|f(a_{n})-f(4)|,$$
>
> 对两项分别用中值定理 ( $\xi_{n+1}$ 在 $a_{n+1}$ 与 4 之间, $\xi_{n}$ 在 $a_{n}$ 与 4 之间):
>
> $$|a_{n+2}-4|\leqslant\frac{|a_{n+1}-4|}{2\sqrt{\xi_{n+1}}}+\frac{|a_{n}-4|}{2\sqrt{\xi_{n}}}.$$
>
> 记 $d_{n}=|a_{n}-4|$，则
>
> $$d_{n+2}\leqslant\frac{d_{n+1}}{2\sqrt{\xi_{n+1}}}+\frac{d_{n}}{2\sqrt{\xi_{n}}},$$
>
> 这是一个二阶压缩型递推. 关键是要让两个系数之和严格小于1, 即
>
> $$\frac{1}{2\sqrt{\xi_{n+1}}}+\frac{1}{2\sqrt{\xi_{n}}}<1.$$
>
> 为此只需 $\xi_{n}$ 有一个不依赖于 n 的固定下界 c > 1. 下面先证明这一点.
>
> 第一步: 存在 k, 使 $a_{k} > 1$. 反设对一切 $n \geqslant 1$ 都有 $a_{n} \leqslant 1$. 由 $0<a_n\leqslant1$ 得 $\sqrt{a_{n}} \geqslant a_{n}$, 于是
>
> $$a_{n+2}=\sqrt{a_{n+1}}+\sqrt{a_{n}}\geqslant a_{n+1}+a_{n}\geqslant0,$$
>
> 即 $a_{n+2} - a_{n+1} \geqslant a_n \geqslant 0$，故 $\{a_n\}$ 从第2项起单调递增。令 $M = \max\{a_1, a_2\} > 0$，由 $a_{n+2} \geqslant a_{n+1} + a_n$ 归纳可得
>
> $$a_{n}\geqslant(n-1)M\qquad(n\geqslant2),$$
>
> 于是 n 充分大时必有 $a_{n}>1$ ，与假设矛盾。所以存在 $k\geqslant1$ ，使 $a_{k}>1$
>
> 第二步: 存在 N, 当 $n \geqslant N$ 时 $a_{n} > 2$. 由 $a_{k} > 1$ 得 $\sqrt{a_{k}} > 1$, 又 $\sqrt{a_{k-1}} > 0$, 故
>
> $$a_{k+1}=\sqrt{a_{k}}+\sqrt{a_{k-1}}>1,\qquad a_{k+2}=\sqrt{a_{k+1}}+\sqrt{a_{k}}>1+1=2.$$
>
> 同理，对一切 $n \geqslant k + 2$ 都有 $a_n>2$。取 $N = k + 2$，则当 $n \geqslant N$ 时 $a_{n} > 2$。
>
> 第三步：压缩放缩。当 $n \geqslant N$ 时 $a_{n} > 2$，而 $\xi_{n}$ 在 $a_{n}$ 与 4 之间，故 $\xi_{n} > 2$，于是
>
> $$\frac{1}{2\sqrt{\xi_{n}}}<\frac{1}{2\sqrt{2}},\qquad d_{n+2}\leq\frac{d_{n+1}+d_{n}}{2\sqrt{2}}.$$
>
> 两个系数之和为 $\frac{1}{2\sqrt{2}}+\frac{1}{2\sqrt{2}}=\frac{1}{\sqrt{2}}<1$，二阶压缩递推成立.
>
> 第四步： $d_{n}\to0$ 令 $q=\frac{1}{2\sqrt{2}}<\frac{1}{2}$，则 $d_{n+2}\leqslant q(d_{n+1}+d_{n})$ 记
>
> $$X_{n}=\begin{pmatrix}d_{n+1}\\ d_{n}\end{pmatrix},\qquad X_{n+1}\leqslant A X_{n},\qquad A=\begin{pmatrix}q&q\\ 1&0\end{pmatrix},$$
>
> 其特征方程为
>
> $$\lambda^{2}-q\lambda-q=0.$$
>
> 因为 $q < \frac{1}{2}$，两个特征根的模都小于 1，故存在 C > 0 与 0 < r < 1，使 $\|A^n\| \leq Cr^n \to 0$，从而 $d_n \to 0$。
>
> 第五步：取极限。由 $d_{n}=|a_{n}-4|\rightarrow0$得
>
> $$\lim_{n\to\infty}a_{n}=4.$$

## 1.3 Stolz 定理

离散形式的洛必达，经常用于对数列极限估阶。经常会作为压轴性质大题考察，了解Stolz定理的适用条件，并学会在合适情境下使用即可。

**1.** (难度:★★★) 设函数 $f(x)$ 在区间 $(-1,1)$ 内三阶连续可导, 且满足 $f(0)=0, f'(0)=1, f''(0)=0, f'''(0)=-1$. 又设数列 $\{a_{n}\}$ 满足 $a_{1} \in (0,1), a_{n+1}=f(a_{n})$ ( $n=1,2,3,\cdots$), 严格单调减少且 $\lim_{n \to \infty} a_{n}=0$. 计算 $\lim_{n \to \infty} na_{n}^{2}$.

> [!answer]- 原书参考答案（B.0.3 第 1 题，未逐题独立验算）
> **1.** $f(x)$ 在 0 处的泰勒展开只保留到三阶就够了（题给三阶导数信息，正是“皮亚诺余项”的信号）. 展开后 $a_{n+1} = a_n - \frac{a_n^3}{6} + o(a_n^3)$，形式和 $\nu x_{n+1} = \arctan x_n$ 一模一样，于是对 $\frac{1}{a_n^2}$ 用 Stolz. 第一步：皮亚诺余项的泰勒展开. 由 $f(0) = 0, f'(0) = 1, f''(0) = 0, f'''(0) = -1$ 得
>
> $$f(x)=x-\frac{x^{3}}{6}+o(x^{3})\qquad(x\to0),$$
>
> 故
>
> $$a_{n+1}=a_{n}-\frac{a_{n}^{3}}{6}+o(a_{n}^{3}),\qquad a_{n}-a_{n+1}=\frac{a_{n}^{3}}{6}+o(a_{n}^{3}).$$
>
> (题设已给出 $a_{n}>0$ 且 $a_{n}\rightarrow0$.)
>
> 第二步: 对 $\frac{1}{a_{n}^{2}}$ 用 Stolz.
>
> $$\frac{1}{a_{n+1}^{2}}-\frac{1}{a_{n}^{2}}=\frac{a_{n}^{2}-a_{n+1}^{2}}{a_{n}^{2}a_{n+1}^{2}}=\frac{(a_{n}-a_{n+1})(a_{n}+a_{n+1})}{a_{n}^{2}a_{n+1}^{2}}\sim\frac{\frac{a_{n}^{3}}{6}\cdot2a_{n}}{a_{n}^{2}\cdot a_{n}^{2}}=\frac{1}{3}.$$
>
> $\left\{\frac{1}{a_{n}^{2}}\right\}$ 严格递增趋于 $+\infty$，由 Stolz 定理
>
> $$\lim_{n\to\infty}\frac{1}{na_{n}^{2}}=\lim_{n\to\infty}\left(\frac{1}{a_{n+1}^{2}}-\frac{1}{a_{n}^{2}}\right)=\frac{1}{3},$$
>
> 所以
>
> $$\lim_{n\to\infty}na_{n}^{2}=3.$$
>
> “泰勒展开估阶 + Stolz 收尾” 是本节的固定套路：先用展开把 $a_{n} - a_{n+1}$ 化成 $a_{n}$ 的幂次，于是 $\frac{1}{a_{n}^{2}}$ 的差分就趋向常数。注意系数： $f'''(0) = -1$ 给出的是 $\frac{a_{n}^{3}}{6}$，对应极限3;若是 $\arctan x\left(-\frac{x^{3}}{3}\right)$，对应的是 $\frac{3}{2}$.

**2.** (难度:★★★) 设数列 $\{x_{n}\}$ 定义为 $x_{n+1} = \left( \sum_{k=1}^{n} x_{k} \right)^{\frac{1}{2}}$. 证明极限 $\lim_{n \to \infty} \frac{x_n}{n}$ 存在并求其值.

> [!answer]- 原书参考答案（B.0.3 第 2 题，未逐题独立验算）
> **2.** 先把递推式改写成 $x_{n+1}^2 = S_n$，这样 $x_{n+2}^2 = S_{n+1} = S_n + x_{n+1}$ 就给出一个只含 $x$ 的递推式。由它看出 $x_{n+2} - x_{n+1} \to \frac{1}{2}$，从而 $x_n \sim \frac{n}{2}$；严格化用 Stolz. (设 $x_1 > 0$。由定义 $x_{n+1} = \left( \sum_{k=1}^{n} x_k \right)^{1/2} > 0$，故 $x_n > 0$。)
>
> 第一步：改写递推式. 记 $S_{n}=x_{1}+\cdots+x_{n}$，则 $x_{n+1}^{2}=S_{n}$，于是
>
> $$x_{n+2}^{2}=S_{n+1}=S_{n}+x_{n+1}=x_{n+1}^{2}+x_{n+1}.$$
>
> 两边相减：
>
> $$x_{n+2}^{2}-x_{n+1}^{2}=x_{n+1}\quad\Longrightarrow\quad x_{n+2}-x_{n+1}=\frac{x_{n+1}}{x_{n+1}+x_{n+2}}.$$
>
> 第二步: 说明 $x_{n} \to \infty$, 从而差分趋于 $\frac{1}{2}$. 由上式 $x_{n+2} > x_{n+1}$, 即 $\{x_{n}\}$ 从第2项起单调递增. 反设 $\{x_{n}\}$ 有界, 则它收敛, 设极限为 A > 0. 在
>
> $$x_{n+2}-x_{n+1}=\frac{x_{n+1}}{x_{n+1}+x_{n+2}}$$
>
> 中令 $n \to \infty$，得 $0 = \frac{A}{2A} = \frac{1}{2}$，矛盾。故 $x_n \to \infty$。
>
> 又由 $0 < x_{n+2} - x_{n+1} \leqslant 1$ 及 $x_{n+1} \to +\infty$ 得 $\frac{x_{n+2}}{x_{n+1}} = 1 + \frac{x_{n+2} - x_{n+1}}{x_{n+1}} \to 1$，从而
>
> $$x_{n+2}-x_{n+1}=\frac{x_{n+1}}{x_{n+1}+x_{n+2}}\longrightarrow\frac{1}{2}.$$
>
> 第三步: 用 Stolz 求 $\frac{x_{n}}{n}$.
>
> $$\lim_{n\to\infty}\frac{x_{n}}{n}=\lim_{n\to\infty}\frac{x_{n+1}-x_{n}}{(n+1)-n}=\lim_{n\to\infty}(x_{n+1}-x_{n})=\frac{1}{2}.$$
>
> 本题的“台阶”是 $x_{n+2}-x_{n+1}=\frac{x_{n+1}}{x_{n+1}+x_{n+2}}$ ：右边夹在0与1之间，且当 $x_{n}\rightarrow\infty$ 时趋于 $\frac{1}{2}$ 。所以关键的一步（也是最容易被跳过的一步）是先证明 $x_{n}\rightarrow\infty$ ——没有它，Stolz 的条件就无从谈起。

**3.** (难度:★★★★) 设 $0 < x_0 < \pi$，当 $n \geqslant 1$ 时， $x_n = \frac{1}{n} \sum_{k=0}^{n-1} \sin x_k$，求极限： $\lim_{n \to \infty} x_n \sqrt{\ln n}$.

> [!answer]- 原书参考答案（B.0.3 第 3 题，未逐题独立验算）
> **3.** 先写出 $x_{n}$ 的递推式，再证明它递减趋于 0；于是 $\frac{1}{x_{n}^{2}}$ 递增趋于无穷，适合用 Stolz 定出 $x_{n}^{2}\ln n$ 的极限，最后开方. 第一步：递推式. 由 $x_{n}=\frac{1}{n}\sum_{k=0}^{n-1}\sin x_{k}$ 得 $(n+1)x_{n+1}-nx_{n}=\sin x_{n}$.
>
> 第二步： $x_{n}\in(0,1)$且递减趋于0.归纳可得 $x_{n}\in(0,1)$;又由 $n(x_{n+1}-x_{n})+x_{n+1}=\sin x_{n}\leq x_{n}$得 $x_{n+1}\leq x_{n}$，故 $\{x_{n}\}$递减有下界，设 $A=\lim_{n\to\infty}x_n$.对其用Stolz得 $A=\sin A$，结合 $0\leq A\leq1$得A=0.
>
> 第三步：用 Stolz 求 $x_{n}^{2} \ln n$.
>
> $$\lim_{n\to\infty}x_{n}^{2}\ln n=\lim_{n\to\infty}\frac{\ln\left(1+\frac{1}{n}\right)}{\frac{1}{x_{n+1}^{2}}-\frac{1}{x_{n}^{2}}}=\lim_{n\to\infty}\frac{1}{n}\cdot\frac{x_{n+1}^{2}x_{n}^{2}}{x_{n}+x_{n+1}}\cdot\frac{n+1}{x_{n}-\sin x_{n}}.$$
>
> $$\begin{aligned} 由 x_{n}^{2}\sim\frac{1}{n}、x_{n}-\sin x_{n}\sim\frac{x_{n}^{3}}{6}\sim\frac{1}{6n^{3/2}}, 上式 \\\sim\frac{1}{n}\cdot\frac{1/n^{2}}{2/\sqrt{n}}\cdot6n\cdot n^{3/2}=3.\end{aligned}$$
>
> 第四步：开方. $\lim_{n\to\infty}x_n\sqrt{\ln n}=\sqrt{3}$. 先估阶、再 Stolz: 算出 $x_{n}^{2}\ln n\to3$ , 可知 $x_{n}\sim\sqrt{\frac{3}{\ln n}}$——注意它不是 $\frac{c}{\sqrt{n}}$ 型（对数型衰减极慢），一开始猜“ $x_{n}\sqrt{n}\to$ 常数”会跑偏.

**4.** (难度:★★★★) 已知数列 $\{x_{n}\}$ 的定义为: $x_{1} > 0$，且存在正整数 $k \geq 3$，使得 $n \geq 1$ 时都有

$$x_{n+1}=x_{n}+\frac{1}{x_{n}}+\frac{2}{x_{n}^{2}}+\cdots+\frac{k}{x_{n}^{k}}.$$

确定常数 $\lambda, \mu$ 且 $\mu \neq 0$，使得 $\lim_{n \to \infty} nx_{n}^{\lambda} = \mu$.

> [!answer]- 原书参考答案（B.0.3 第 4 题，未逐题独立验算）
> **4.** 要说明“只有 $\lambda = -2$ 可以”，不能只验证 -2 行得通。正确做法是：先设 $nx_{n}^{\lambda} \to \mu \neq 0$ 成立，推出 $x_{n}^{\lambda} \sim \frac{\mu}{n}$，再令 $t = -\lambda$，则 $x_{n}^{t} \sim \frac{n}{\mu}$——”与 n 同阶”这种形状正好能用 Stolz; Stolz 后会出现 $x_{n+1}^{t} - x_{n}^{t}$，用乘法公式因式分解，就能看出 t > 2、t < 2 都不可能，只有 t = 2 成立。第一步： $x_{n} \to \infty$。由 $x_{n+1} - x_{n} > 0$ 知 $\{x_{n}\}$ 递增；若它有界，设极限为 S > 0，在递推式两边取极限会出现 $\frac{1}{S} + \cdots > 0$ 的矛盾，故
>
> $$x_{n}\to\infty,\qquad\frac{x_{n+1}}{x_{n}}\to1.$$
>
> 第二步：把结论“归一化”。设 $nx_{n}^{\lambda} \rightarrow \mu \neq 0$，令 $t = -\lambda$，则 $x_{n}^{t} = n \left(x_{n}^{\lambda}\right)^{-1}$，所以条件等价于
>
> $$\frac{x_{n}^{t}}{n}\longrightarrow\frac{1}{\mu}\neq0.$$
>
> 也就是说， $x_{n}^{t}$ 必须与 n 同阶——这种“除以 n”的形状正好适合用 Stolz.
>
> 第三步：Stolz + 乘法公式. 由 Stolz 定理 (分母取 n)，若 $\frac{x_{n}^{t}}{n}$ 有极限，则
>
> $$\lim_{n\to\infty}\frac{x_{n}^{t}}{n}=\lim_{n\to\infty}\left(x_{n+1}^{t}-x_{n}^{t}\right).$$
>
> 由递推式得 $x_{n+1}-x_n=\frac{1}{x_n}+O\left(\frac{1}{x_n^2}\right)\sim\frac{1}{x_n}$. 再用乘法公式 (等价地, 对 $x^t$ 用中值定理) 因式分解:
>
> $$x_{n+1}^{t}-x_{n}^{t}=\left(x_{n+1}-x_{n}\right)\cdot\frac{x_{n+1}^{t}-x_{n}^{t}}{x_{n+1}-x_{n}},$$
>
> 其中分式部分（记 $\xi_{n}$在 $x_{n}$与 $x_{n+1}$之间）满足
>
> $$\frac{x_{n+1}^{t}-x_{n}^{t}}{x_{n+1}-x_{n}}=t\xi_{n}^{t-1}\sim t x_{n}^{t-1},$$
>
> 于是
>
> $$x_{n+1}^{t}-x_{n}^{t}\sim\frac{1}{x_{n}}\cdot t x_{n}^{t-1}=t x_{n}^{t-2}.$$
>
> 第四步：比较t与2.
>
> 若 $t > 2$: 则 $tx_{n}^{t-2} \to +\infty$, 即 $x_{n+1}^{t} - x_{n}^{t} \to +\infty$, 由 Stolz 得 $\frac{x_{n}^{t}}{n} \to +\infty$,
>
> 与” $\frac{x_{n}^{t}}{n}\rightarrow\frac{1}{\mu}$（有限非零）”矛盾；
>
> 若 t<2: 则 $tx_{n}^{t-2}\rightarrow0$ , 即 $x_{n+1}^{t}-x_{n}^{t}\rightarrow0$ , 由 Stolz 得 $\frac{x_{n}^{t}}{n}\rightarrow0$ , 与 $\frac{x_{n}^{t}}{n}\rightarrow\frac{1}{\mu}\neq0$ 矛盾;
>
> 只有 t=2: 此时 $x_{n+1}^{2}-x_{n}^{2}\rightarrow2$ , 由 Stolz 得 $\frac{x_{n}^{2}}{n}\rightarrow2$ , 与第二步要求的 $\frac{x_{n}^{t}}{n}\rightarrow\frac{1}{\mu}$ 相容.
>
> 所以只能是 t=2，即 $\lambda=-2$，且由 $\frac{x_{n}^{2}}{n}\rightarrow2$ 得
>
> $$nx_{n}^{-2}=\frac{n}{x_{n}^{2}}\longrightarrow\frac{1}{2},\qquad 即 \qquad\mu=\frac{1}{2}.$$
>
> 关键是先把结论归一化：令 $t = -\lambda$，把 $nx_{n}^{\lambda} \to \mu$ 等价地写成 $\frac{x_{n}^{t}}{n} \to \frac{1}{\mu}$，这样 $x_{n}^{t}$ 与 n 同阶，才能放心用 Stolz. Stolz 之后的 $x_{n+1}^{t} - x_{n}^{t}$ 用乘法公式拆成 $\left(x_{n+1} - x_{n}\right) \times tx_{n}^{t-1}$，与 $x_{n+1} - x_{n} \sim \frac{1}{x_{n}}$ 合并即得 $tx_{n}^{t-2}$；由于 $x_{n} \to \infty$，它的极限只有 $+\infty$、0、常数 t 三种，分别对应 t > 2、t < 2、t = 2，而前两种都与 $\frac{x_{n}^{t}}{n}$ 收敛到非零数“矛盾。这样才真正证明了”只有 $\lambda = -2$”。

**5.** (难度：★★★★★) 设 $\{a_{n}\}$ 满足 $a_{1}>1, a_{n+1}(a_{n}^{2}-1)=a_{n}^{3}$. 求:

(1) $A = \lim_{n \to \infty} \frac{a_n}{\sqrt{n}};$

(2) $\lim_{n \to \infty} \frac{n}{\ln n} \left( \frac{a_n}{\sqrt{n}} - A \right)$.

> [!answer]- 原书参考答案（B.0.3 第 5 题，未逐题独立验算）
> **5.** 先把递推式解成 $a_{n+1} = \frac{a_n^3}{a_n^2 - 1}$，用反证法确定 $a_n \to \infty$。估阶的关键是 $a_{n+1} - a_n = \frac{a_n}{a_n^2 - 1}$，用“乘法公式”配出 $a_{n+1}^2 - a_n^2$ 再用 Stolz. (1) 由 $a_{n+1} = \frac{a_n^3}{a_n^2 - 1}$ 得 $a_{n+1} - a_n = \frac{a_n}{a_n^2 - 1} > 0$，故 $\{a_n\}$ 递增（且 $a_n > 1$）。若 $a_n \to S$ 有限，则 $S = \frac{S^3}{S^2 - 1}$，即 $S = 0$，与 $S > 0$ 矛盾，故 $a_n \to \infty$，且 $\frac{a_{n+1}}{a_n} \to 1$。
>
> 由乘法公式与 Stolz:
>
> $$\lim_{n\to\infty}\frac{a_{n}^{2}}{n}=\lim_{n\to\infty}\left(a_{n+1}^{2}-a_{n}^{2}\right),$$
>
> 而
>
> $$a_{n+1}^{2}-a_{n}^{2}=(a_{n+1}+a_{n})(a_{n+1}-a_{n})=2a_{n}\cdot\frac{a_{n}}{a_{n}^{2}-1}\longrightarrow2.$$
>
> 故 $A = \lim_{n \to \infty} \frac{a_n}{\sqrt{n}} = \sqrt{2}$.
>
> (2) 先把 $a_{n}-\sqrt{2n}$ 有理化:
>
> $$\frac{n}{\ln n}\left(\frac{a_{n}}{\sqrt{n}}-A\right)=\frac{\sqrt{n}}{a_{n}+\sqrt{2n}}\cdot\frac{a_{n}^{2}-2n}{\ln n},$$
>
> 其中由 $a_n \sim \sqrt{2n}$ 得 $\frac{\sqrt{n}}{a_n + \sqrt{2n}} \longrightarrow \frac{1}{2\sqrt{2}}$. 再算第二个因子: 由
>
> $$a_{n+1}^{2}-a_{n}^{2}=\frac{a_{n}^{2}(2a_{n}^{2}-1)}{(a_{n}^{2}-1)^{2}}$$
>
> 可得 $a_{n+1}^2 - a_n^2 - 2 = \frac{3a_n^2 - 2}{(a_n^2 - 1)^2}$，用 Stolz 定理（分母取 $\ln n$）：
>
> $$\lim_{n\to\infty}\frac{a_{n}^{2}-2n}{\ln n}=\lim_{n\to\infty}\frac{a_{n+1}^{2}-a_{n}^{2}-2}{\ln\left(1+\frac{1}{n}\right)}=\lim_{n\to\infty}\frac{3n}{a_{n}^{2}}.$$
>
> 由 $a_{n}^{2} \sim 2n$ 得 $\frac{3n}{a_{n}^{2}} \to \frac{3}{2}$，于是 $\lim_{n \to \infty} \frac{n}{\ln n} \left( \frac{a_{n}}{\sqrt{n}} - A \right) = \frac{1}{2\sqrt{2}} \cdot \frac{3}{2} = \frac{3\sqrt{2}}{8}$。两个技术动作：配平方（凑 Stolz 的差分）与通分（把 $a_{n} - \sqrt{2n}$ 有理化，其中 $\frac{\sqrt{n}}{a_{n} + \sqrt{2n}}$ 是“非零因子”，可以先把极限算出来提走）。

**6.** (难度：★★★★) 设 $\{a_{n}\}_{n=0}^{\infty}$ 是一个数列, $a, \lambda$ 为有限数. 求证:

(1) 若 $\lim_{n \to \infty} a_n = a$，则 $\lim_{n \to \infty} \frac{a_1 + a_2 + \cdots + a_n}{n} = a$;

(2) 设 p 是一个固定的正整数，且 $\lim_{n\to\infty}(a_{n+p}-a_n)=\lambda$，则 $\lim_{n\to\infty}\frac{a_n}{n}=\frac{\lambda}{p}$.

> [!answer]- 原书参考答案（B.0.3 第 6 题，未逐题独立验算）
> **6.** (1) 记 $S_{n} = a_{1} + a_{2} + \cdots + a_{n}$. $\{n\}$ 严格递增趋于 $+ \infty$，由 Stolz 定理，
>
> $$\lim_{n\to\infty}\frac{S_{n}}{n}=\lim_{n\to\infty}\frac{S_{n+1}-S_{n}}{(n+1)-n}=\lim_{n\to\infty}a_{n+1}=a.$$
>
> (2) 对每个 $1 \leq k \leq p-1$，取子列 $b_n^k = a_{pn-k}$。把 $k = 0,1,\ldots,p-1$ 对应的子列拼起来，正好覆盖数列 $\{a_n\}$ 的全部项。由 Stolz 定理 (分母取 $n$)，
>
> $$\lim_{n\to\infty}\frac{b_{n}^{k}}{n}=\lim_{n\to\infty}\frac{b_{n+1}^{k}-b_{n}^{k}}{(n+1)-n}=\lim_{n\to\infty}\left(a_{pn+p-k}-a_{pn-k}\right)=\lambda,$$
>
> 因此
>
> $$\lim_{n\to\infty}\frac{a_{pn-k}}{pn-k}=\lim_{n\to\infty}\frac{a_{pn-k}}{n}\cdot\frac{n}{pn-k}=\lambda\cdot\frac{1}{p}=\frac{\lambda}{p}.$$
>
> 也就是说, 任一子列 $\left\{\frac{a_{pn-k}}{pn-k}\right\}$ 都收敛到 $\frac{\lambda}{p}$; 把这些子列拼起来就得到整个数列, 故
>
> $$\lim_{n\to\infty}\frac{a_{n}}{n}=\frac{\lambda}{p}.$$

**7.** (难度：★★★★) 设 $a_{1}>0, \alpha>0$, 数列 $\{a_{n}\}$ 由如下递推式定义:

$$a_{n+1}=a_{n}+\left(\frac{n}{S_{n}}\right)^{\alpha},\quad n=1,2,\cdots,$$

其中 $S_{n}=a_{1}+a_{2}+\cdots+a_{n},\lim_{n\to\infty}\frac{na_{n}}{S_{n}}$ 收敛.

(1) 证明: $\lim_{n \to \infty} \frac{a_n^{\alpha+1}}{n}$ 收敛;

(2) 求 $\lim_{n \to \infty} \frac{na_n}{S_n}$.

> [!answer]- 原书参考答案（B.0.3 第 7 题，未逐题独立验算）
> **7.** $\frac{na_{n}}{S_{n}}$ 是“平均意义”下的量. 先证 $a_{n} \to \infty$ (从而 $a_{n+1}/a_{n} \to 1$), 再用拉格朗日中值定理把 $a_{n}^{\alpha+1}$ 的差分与 $a_{n+1} - a_{n}$ 联系起来. (1) 由 $a_{n+1} - a_{n} = \left(\frac{n}{S_{n}}\right)^{\alpha} > 0$ 知 $\{a_{n}\}$ 递增; 若 $a_{n} \to S$ 有限, 则 $\frac{S_{n}}{n} \to S$, 取极限得 $S = S + \frac{1}{S^{\alpha}}$, 矛盾. 故 $a_{n} \to \infty$, 进而
>
> $$\frac{a_{n+1}}{a_{n}}=1+\frac{na_{n}^{\alpha}}{S_{n}^{\alpha}}\cdot\frac{1}{a_{n}^{\alpha+1}}\longrightarrow1.$$
>
> 又由中值定理 $(a_{n} \leqslant \xi_{n} \leqslant a_{n+1}$，故 $\xi_{n}/a_{n} \to 1)$
>
> $$a_{n+1}^{\alpha+1}-a_{n}^{\alpha+1}=(\alpha+1)(a_{n+1}-a_{n})\xi_{n}^{\alpha}=(\alpha+1)\left(\frac{n a_{n}}{S_{n}}\right)^{\alpha}\left(\frac{\xi_{n}}{a_{n}}\right)^{\alpha},$$
>
> 用 Stolz (分母取 n) 得
>
> $$\lim_{n\to\infty}\frac{a_{n}^{\alpha+1}}{n}=\left(\alpha+1\right)\lim_{n\to\infty}\left(\frac{na_{n}}{S_{n}}\right)^{\alpha},$$
>
> 右端收敛，故左端收敛.
>
> (2) 设 $A = \lim_{n \to \infty} \frac{na_n}{S_n}$，则上式为 $(\alpha + 1)A^\alpha$。再由 Stolz
>
> $$A=\lim_{n\to\infty}\frac{(n+1)a_{n+1}-na_{n}}{S_{n+1}-S_{n}}=1+\lim_{n\to\infty}\frac{n}{a_{n+1}}\left(\frac{n}{S_{n}}\right)^{\alpha}=1+\frac{1}{(\alpha+1)A^{\alpha}}\cdot1\cdot A^{\alpha},$$
>
> 故 $A = 1 + \frac{1}{\alpha+1} = \frac{\alpha+2}{\alpha+1}$. 最后一招是“把已知极限的因子提出来”: 把 $\frac{na_{n}}{S_{n}}$ 从式子里识别出来, 直接代入 $A^{\alpha}$, 比硬算整个极限省力得多.

## 1.4 多数列极限

对于多个数列的混合项定义，可借助递推定义对数列进行消元，转为单数列问题。无法消元的问题一般会考虑极限存在准则证明极限存在，随后通过两边同时取极限的方法解决问题。在处理多数列问题时，同样不要忘记，矩阵是非常优秀的研究工具。

**1.** (难度:★★★★)设数列 $\{x_{n}\}$与 $\{y_{n}\}$定义为

$$\begin{cases}x_{0}=1-\alpha,\\y_{0}=\alpha,\end{cases}$$

当 $n \geqslant 1$时，满足：

$$\left\{\begin{aligned}x_{n+1}&=(1-\gamma)x_{n}+\beta x_{n}y_{n},\\ y_{n+1}&=y_{n}-\beta x_{n}y_{n},\end{aligned}\right.$$

其中 $\alpha, \beta, \gamma \in (0,1)$ 为实常数. 证明 $\lim_{n \to \infty} x_n, \lim_{n \to \infty} y_n$ 均存在, 并求 $\lim_{n \to \infty} x_n$.

> [!answer]- 原书参考答案（B.0.4 第 1 题，未逐题独立验算）
> **1.** 第一步：把两个式子相加. 把两式相加得
>
> $$x_{n+1}+y_{n+1}=x_{n}+y_{n}-\gamma x_{n}.$$
>
> 记 $S_{n}=x_{n}+y_{n}$，则 $S_{n+1}=S_{n}-\gamma x_{n}$
>
> 第二步: 证明 $x_n, y_n, x_n + y_n \in (0,1)$. 用数学归纳法. $n = 0$ 时 $x_0 = 1 - \alpha \in (0,1)$, $y_0 = \alpha \in (0,1)$, $S_0 = 1$, 成立. 设 $x_k, y_k, S_k \in (0,1)$, 则
>
> $$S_{k+1}=S_{k}-\gamma x_{k}<S_{k}<1,\qquad y_{k+1}=y_{k}(1-\beta x_{k})\in(0,1),$$
>
> $$x_{k+1}=x_{k}\big[(1-\gamma)+\beta y_{k}\big]>0,\qquad S_{k+1}>0,$$
>
> 故 $S_{k+1} \in (0,1)$; 再由 $y_{k+1} \in (0,1)$、 $S_{k+1} \in (0,1)$ 得 $x_{k+1} = S_{k+1} - y_{k+1} \in (0,1)$.
>
> 归纳完成.
>
> 第三步: 单调性. 由 $S_{n+1} - S_n = -\gamma x_n < 0$ 知 $\{S_n\}$ 递减且有下界 0; 由 $y_{n+1} = y_n (1 - \beta x_n) < y_n$ 知 $\{y_n\}$ 递减且有下界 0. 于是 $\lim_{n \to \infty} S_n$ 与 $\lim_{n \to \infty} y_n$ 都存在, 从而
>
> $$\lim_{n\to\infty}x_{n}=\lim_{n\to\infty}(S_{n}-y_{n})$$
>
> 也存在.
>
> 第四步: 求值. 设 $\lim_{n \to \infty} x_n = A$, $\lim_{n \to \infty} y_n = B$. 在递推式中令 $n \to \infty$:
>
> $$A=(1-\gamma)A+\beta AB,\qquad B=B-\beta AB.$$
>
> 由第二式得 $\beta AB = 0$; 因为 $\beta \in (0,1)$，故 A = 0 或 B = 0。若 B = 0，由第一式得 $A = (1 - \gamma)A$，即 $\gamma A = 0$，仍得 A = 0。所以
>
> $$\lim_{n\to\infty}x_{n}=0.$$

**2.** (难度:★★★) 给定 3 个数列 $\{x_{n}\}, \{y_{n}\}, \{z_{n}\}$ 满足 $x_{1} = -2, y_{1} = 1, z_{1} = -1$. 且 $n \geqslant 1$ 时有

$$\left\{\begin{aligned}x_{n+1}&=3x_{n}-6y_{n}-z_{n},\\ y_{n+1}&=-x_{n}+2y_{n}+z_{n},\\ z_{n+1}&=x_{n}+3y_{n}-z_{n},\end{aligned}\right.$$

求 $\lim_{n\to\infty}\frac{x_n+y_n+z_n}{3^n+5^n}$

> [!answer]- 原书参考答案（B.0.4 第 2 题，未逐题独立验算）
> **2.** 第一步：写成矩阵形式.
>
> $$X_{n}=\begin{pmatrix}x_{n}\\ y_{n}\\ z_{n}\end{pmatrix},\qquad A=\begin{pmatrix}3&-6&-1\\ -1&2&1\\ 1&3&-1\end{pmatrix},\qquad X_{n+1}=A X_{n}.$$
>
> 第二步：求特征值与特征向量.
>
> $$|A-\lambda E|=-\lambda^{3}+4\lambda^{2}+7\lambda-10=-(\lambda-1)(\lambda-5)(\lambda+2),$$
>
> 故特征值为 $\lambda_{1}=1,\lambda_{2}=5,\lambda_{3}=-2$ ，三个特征值互异，A 可对角化. 对应的特征向量分别取
>
> $$\xi_{1}=(5,1,4)^{\mathrm{T}},\qquad\xi_{2}=(-3,1,0)^{\mathrm{T}},\qquad\xi_{3}=(1,2,-7)^{\mathrm{T}}.$$
>
> （例如对 $\lambda_{2}=5$，解 $(A-5E)\xi=0$ 得 -3x+y=0, z=0，取 $\xi_{2}=(-3,1,0)^{\mathrm{T}}$。）
>
> 第三步：把 $X_{1}$ 用特征向量表示. 设 $X_{1} = \alpha_{1}\xi_{1} + \alpha_{2}\xi_{2} + \alpha_{3}\xi_{3}$，代入 $X_{1} = (-2, 1, -1)^{\mathrm{T}}$ 解得
>
> $$\alpha_{1}=0,\qquad\alpha_{2}=\frac{5}{7},\qquad\alpha_{3}=\frac{1}{7}.$$
>
> 于是 $X_{n}=A^{n-1}X_{1}=\frac{5}{7}\cdot5^{n-1}\xi_{2}+\frac{1}{7}\cdot(-2)^{n-1}\xi_{3}$
>
> 第四步: 求所需极限. 注意 $x_{n} + y_{n} + z_{n} = (1,1,1)X_{n}$，而 $(1,1,1)\xi_{2} = -2, (1,1,1)\xi_{3} = 1 + 2 - 7 = -4$。故
>
> $$x_{n}+y_{n}+z_{n}=-\frac{10}{7}\cdot5^{n-1}-\frac{4}{7}\cdot\left(-2\right)^{n-1}=-\frac{2}{7}\cdot5^{n}-\frac{4}{7}\cdot\left(-2\right)^{n-1}.$$
>
> 由 $\frac{5^{n}}{3^{n}+5^{n}}\rightarrow1$、 $\frac{(-2)^{n-1}}{3^{n}+5^{n}}\rightarrow0$得
>
> $$\lim_{n\to\infty}\frac{x_{n}+y_{n}+z_{n}}{3^{n}+5^{n}}=-\frac{2}{7}.$$

**3.** (难度: ★★★★) 已知 $a_{n} + \sqrt{3}b_{n} = (3 + \sqrt{3})^{n}$，其中 $a_{n}, b_{n}$ 均为整数，求极限 $\lim_{n \to \infty} \frac{a_{n}}{b_{n}}$.

> [!answer]- 原书参考答案（B.0.4 第 3 题，未逐题独立验算）
> **3.** $a_{n} + \sqrt{3}b_{n} = (3 + \sqrt{3})^{n}$ 且 $a_{n}, b_{n}$ 都是整数，说明可以用“共轭”把 $a_{n}, b_{n}$ 解出来： $(3 - \sqrt{3})^{n}$ 与 $(3 + \sqrt{3})^{n}$ 的展开只差根号项的符号。依次比较 $(3 + \sqrt{3})^{n}$ 与 $(3 - \sqrt{3})^{n}$ 的展开，或直接由数学归纳法可得
>
> $$(3+\sqrt{3})^{n}=a_{n}+\sqrt{3}b_{n},\qquad(3-\sqrt{3})^{n}=a_{n}-\sqrt{3}b_{n}.$$
>
> 两式相加、相减得
>
> $$a_{n}=\frac{(3+\sqrt{3})^{n}+(3-\sqrt{3})^{n}}{2},\qquad b_{n}=\frac{(3+\sqrt{3})^{n}-(3-\sqrt{3})^{n}}{2\sqrt{3}},$$
>
> 于是
>
> $$\frac{a_{n}}{b_{n}}=\sqrt{3}\frac{(3+\sqrt{3})^{n}+(3-\sqrt{3})^{n}}{(3+\sqrt{3})^{n}-(3-\sqrt{3})^{n}}=\sqrt{3}\frac{1+\left(\frac{3-\sqrt{3}}{3+\sqrt{3}}\right)^{n}}{1-\left(\frac{3-\sqrt{3}}{3+\sqrt{3}}\right)^{n}}.$$
>
> 而
>
> $$0<\frac{3-\sqrt{3}}{3+\sqrt{3}}=\frac{(3-\sqrt{3})^{2}}{6}=2-\sqrt{3}<1,$$
>
> 故 $\left(\frac{3-\sqrt{3}}{3+\sqrt{3}}\right)^{n}\rightarrow0$,从而
>
> $$\lim_{n\to\infty}\frac{a_{n}}{b_{n}}=\sqrt{3}.$$
>
> $a_{n}+\sqrt{3}b_{n}=(3+\sqrt{3})^{n}$ 这类题的标准做法是“配上共轭式 $a_{n}-\sqrt{3}b_{n}=(3-\sqrt{3})^{n}$，把 $a_{n}, b_{n}$ 解出来，再让公比小于1的那一项消失。它和1.5.2的矩阵方法是一回事： $3\pm\sqrt{3}$ 正是对应矩阵的两个特征值。

**4.** (难度：★★★★★) 给定 3 个数列 $\{a_{n}\}, \{b_{n}\}, \{c_{n}\}$ 满足 $a_{1}=1$, $b_{1}=c_{1}=0$. 且 $n \geqslant 2$ 时有:

$$a_{n}=a_{n-1}+\frac{c_{n-1}}{n},\quad b_{n}=b_{n-1}+\frac{a_{n-1}}{n},\quad c_{n}=c_{n-1}+\frac{b_{n-1}}{n}.$$

证明：

$$\lim_{n\to\infty}\sqrt{n}\left[(a_{n}-b_{n})^{2}+(b_{n}-c_{n})^{2}+(c_{n}-a_{n})^{2}\right]=0.$$

> [!answer]- 原书参考答案（B.0.4 第 4 题，未逐题独立验算）
> **4.** 先把三个递推式两两相减，换成“差值数列” $x_{n}=a_{n}-b_{n}$， $y_{n}=b_{n}-c_{n}$， $z_{n}=c_{n}-a_{n}$。这三个量只用两条现成的关系就够了：其一，由定义恒有 $x_{n}+y_{n}+z_{n}=0$，两边平方即可把三个交叉项写成 $-\frac{1}{2}$ 倍平方和；其二，三式的增量分别是 $\frac{z_{n-1}}{n}$， $\frac{x_{n-1}}{n}$， $\frac{y_{n-1}}{n}$，把三式分别平方再相加，左边正好凑出平方和的增量。两件事合起来，平方和就满足一个乘式递推，剩下只是无穷乘积估阶。记
>
> $$x_{n}=a_{n}-b_{n},\qquad y_{n}=b_{n}-c_{n},\qquad z_{n}=c_{n}-a_{n},$$
>
> 则 $x_{n}+y_{n}+z_{n}=0$ 。由题设三式两两相减（注意 $a_{n}-a_{n-1}=\frac{c_{n-1}}{n}$ 等）可得
>
> $$x_{n}=x_{n-1}+\frac{z_{n-1}}{n},\qquad y_{n}=y_{n-1}+\frac{x_{n-1}}{n},\qquad z_{n}=z_{n-1}+\frac{y_{n-1}}{n}.$$
>
> 第一步：由 $x_{n}+y_{n}+z_{n}=0$ 得交叉项。把 $x_{n}+y_{n}+z_{n}=0$ 两边平方，得
>
> $$x_{n}^{2}+y_{n}^{2}+z_{n}^{2}+2\left(x_{n}y_{n}+y_{n}z_{n}+z_{n}x_{n}\right)=0,$$
>
> 即
>
> $$x_{n}y_{n}+y_{n}z_{n}+z_{n}x_{n}=-\frac{1}{2}Q_{n},\qquad Q_{n}=x_{n}^{2}+y_{n}^{2}+z_{n}^{2}.$$
>
> 第二步：三式平方相加，得乘式递推。记 $\Delta x=x_{n}-x_{n-1}$，则
>
> $$\Delta x=\frac{z_{n-1}}{n},\qquad\Delta y=\frac{x_{n-1}}{n},\qquad\Delta z=\frac{y_{n-1}}{n},$$
>
> 于是
>
> $$\Delta x^{2}+\Delta y^{2}+\Delta z^{2}=\frac{z_{n-1}^{2}+x_{n-1}^{2}+y_{n-1}^{2}}{n^{2}}=\frac{Q_{n-1}}{n^{2}},$$
>
> 而交叉部分（把 $\Delta x, \Delta y, \Delta z$ 代入，三个交叉项恰好还是那三个）
>
> $$x_{n-1}\Delta x+y_{n-1}\Delta y+z_{n-1}\Delta z=\frac{x_{n-1}y_{n-1}+y_{n-1}z_{n-1}+z_{n-1}x_{n-1}}{n}=-\frac{Q_{n-1}}{2n}.$$
>
> 展开
>
> $$Q_{n}=Q_{n-1}+2\left(x_{n-1}\Delta x+y_{n-1}\Delta y+z_{n-1}\Delta z\right)+\left(\Delta x^{2}+\Delta y^{2}+\Delta z^{2}\right),$$
>
> 即得
>
> $$Q_{n}=Q_{n-1}\left(1-\frac{1}{n}+\frac{1}{n^{2}}\right)=Q_{n-1}\cdot\frac{n^{2}-n+1}{n^{2}}.$$
>
> 第三步：无穷乘积估阶.迭代得
>
> $$Q_{n}=Q_{1}\prod_{k=2}^{n}\frac{k^{2}-k+1}{k^{2}},$$
>
> 其中
>
> $$Q_{1}=(a_{1}-b_{1})^{2}+(b_{1}-c_{1})^{2}+(c_{1}-a_{1})^{2}=1+0+1=2.$$
>
> 对 $k \geqslant 2$ ，记 $t_{k} = \frac{1}{k} - \frac{1}{k^{2}}$ ，则 $0<t_k<1$ 且 $\frac{k^{2} - k + 1}{k^{2}} = 1 - t_{k}$ ，由 $\ln(1 - t) \leqslant -t (0 < t < 1)$ 得
>
> $$\sum_{k=2}^{n}\ln\frac{k^{2}-k+1}{k^{2}}\leqslant-\sum_{k=2}^{n}\frac{1}{k}+\sum_{k=2}^{n}\frac{1}{k^{2}}.$$
>
> 两部分分别估. 调和部分用积分放缩，
>
> $$\sum_{k=2}^{n}\frac{1}{k}>\int_{2}^{n+1}\frac{\mathrm{d}x}{x}=\ln(n+1)-\ln2;$$
>
> 平方倒数部分逐项放大到级数
>
> $$\sum_{k=2}^{n}\frac{1}{k^{2}}<\sum_{k=1}^{+\infty}\frac{1}{k^{2}}=\frac{\pi^{2}}{6}.$$
>
> 于是
>
> $$\sum_{k=2}^{n}\ln\frac{k^{2}-k+1}{k^{2}}<-\ln(n+1)+\ln2+\frac{\pi^{2}}{6},$$
>
> 两边取指数得
>
> $$Q_{n}<\frac{4e^{\pi^{2}/6}}{n+1}.$$
>
> 第四步：夹逼。注意 $Q_{n}=(a_{n}-b_{n})^{2}+(b_{n}-c_{n})^{2}+(c_{n}-a_{n})^{2}$，于是
>
> $$0\leqslant\sqrt{n}\left[(a_{n}-b_{n})^{2}+(b_{n}-c_{n})^{2}+(c_{n}-a_{n})^{2}\right]=\sqrt{n}Q_{n}<\frac{4e^{\pi^{2}/6}\sqrt{n}}{n+1}\longrightarrow0,$$
>
> 由夹逼定理,所要证的极限为0.这里只用两条最朴素的关系:由
>
> $$x_{n}+y_{n}+z_{n}=0$$
>
> 平方得”交叉项$=-\frac{1}{2}$平方和";由三式平方相加得
>
> $$Q_{n}=Q_{n-1}\left(1-\frac{1}{n}+\frac{1}{n^{2}}\right).$$
>
> 关键认识是: 三个差值的平方和自身满足乘式递推, 而系数 $1 - \frac{1}{n} + \frac{1}{n^2} = 1 - \left(\frac{1}{n} - \frac{1}{n^2}\right)$ 连乘起来恰好是 $\frac{1}{n}$ 量级. 最后这步用的是 1.1 节“无穷乘积”例题的同一套路——累乘、取对数、调和部分积分放缩、平方倒数部分用 $\sum 1/k^2 = \pi^2/6$, 常数不藏着, 直接算出 $Q_n < \frac{4e^{\pi^2/6}}{n+1}$, 于是 $\sqrt{n} Q_n \to 0$. 凡是这种“三个量循环接力”的递推, 都值得先算一算差值的平方和.

## 1.5 函数零点列极限

对于带参函数的零点极限，通常采用夹逼定理的方法确定极限大小。此类题目与一元微分学结合紧密，需要结合导数讨论零点个数与位置，需要较深厚的高中导数分析能力。

**1.** (难度:★★★) 设 $f_{n}(x)=x^{n}+nx-2$.

(1) 证明: 对任意正整数 n, $f_{n}(x)$ 在 $(0, +\infty)$ 有唯一的实根.

(2) 设 $a_{n}$ 是 $f_{n}(x)$ 的正实根，求极限： $\lim_{n\to\infty}(1+a_{n})^{n}$.

> [!answer]- 原书参考答案（B.0.5 第 1 题，未逐题独立验算）
> **1.** (1) 当 x > 0 时 $f_{n}^{\prime}(x) = nx^{n-1} + n > 0$，故 $f_{n}$ 在 $(0, +\infty)$ 上严格递增，至多有一个零点。又
>
> $$f_{n}(0)=-2<0,\qquad f_{n}\left(\frac{2}{n}\right)=\left(\frac{2}{n}\right)^{n}>0,$$
>
> 由零点存在定理， $f_{n}$ 在 $\left(0,\frac{2}{n}\right)$ 内有零点，再由单调性知零点唯一.
>
> (2) 由(1)知 $0 < a_{n} < \frac{2}{n}$. 把 $a_{n}^{n} + na_{n} - 2 = 0$ 反解得 $a_{n} = \frac{2 - a_{n}^{n}}{n}$，于是
>
> $$\frac{2-\left(\frac{2}{n}\right)^{n}}{n}<a_{n}<\frac{2}{n},$$
>
> 由夹逼定理得 $na_{n} \to 2$. 又 $a_{n} \to 0$, 故 $n \ln(1 + a_{n}) \sim na_{n} \to 2$, 于是
>
> $$\lim_{n\to\infty}(1+a_{n})^{n}=\lim_{n\to\infty}e^{n\ln(1+a_{n})}=e^{2}.$$

**2.** (难度:★★★) 设函数 $f_{n}(x) = e^{nx} + x - e^{n}$

(1) 证明: 对任意正整数 n, 方程 $f_{n}(x) = 0$ 在区间 $(0,1)$ 内有且仅有一个实数根 $r_{n}$.

(2) 证明: 极限 $\lim_{n \to \infty} r_n$ 存在并求其值.

> [!answer]- 原书参考答案（B.0.5 第 2 题，未逐题独立验算）
> **2.** 先证唯一性（单调 + 端点异号），再把 $r_{n}$ 从方程 $e^{nr_{n}} + r_{n} = e^{n}$ 里反解出来，用 $r_{n} < 1$ 夹逼. (1) 当 $x \in (0,1)$ 时 $f_{n}^{\prime}(x) = n e^{nx} + 1 > 0$，故 $f_{n}$ 在 $(0,1)$ 上严格递增，至多有一个零点. 又
>
> $$f_{n}(0)=1-e^{n}<0,\qquad f_{n}(1)=e^{n}+1-e^{n}=1>0,$$
>
> 由零点存在定理， $f_{n}$ 在 $(0,1)$ 内有零点，再由单调性知零点唯一.
>
> (2) 由 $f_{n}(r_{n})=0$ 得 $e^{nr_{n}}=e^{n}-r_{n}$，两边取对数并反解得
>
> $$r_{n}=\frac{1}{n}\ln\left(e^{n}-r_{n}\right).$$
>
> 由(1)知$0<r_n<1$，故 $e^{n}-r_{n}>e^{n}-1$，于是
>
> $$\frac{1}{n}\ln\left(e^{n}-1\right)<r_{n}<1.$$
>
> 而 $\frac{1}{n}\ln(e^{n}-1)=1+\frac{1}{n}\ln(1-e^{-n})\rightarrow1$ ，由夹逼定理
>
> $$\lim_{n\to\infty}r_{n}=1.$$
>
> 两步：先定范围 $(0 < r_n < 1)$，再反解 + 夹逼。反解时用的是题目的等式本身 $(e^{nr_n} = e^n - r_n)$，这一步把 $r_n$ 与 1 的差压成了 $\frac{1}{n} \ln(1 - e^{-n})$ 这样的无穷小。

**3.** (难度：★★★★★) 证明方程 $e^{-x} + \cos 2x + x \sin x = 0$ 在每个区间 $((2n-1)\pi, (2n+1)\pi)$ 内恰有两个根 $x_{2n-1} < x_{2n}, n \geqslant 1$，并证明极限 $\lim_{n \to \infty} (-1)^n n (x_n - n\pi)$ 存在并求其值.

> [!answer]- 原书参考答案（B.0.5 第 3 题，未逐题独立验算）
> **3.** 记
>
> $$f(x)=e^{-x}+\cos2x+x\sin x,\qquad c_{n}=e^{-2n\pi}(n\geqslant1),$$
>
> 则 $0 < c_{n} \leqslant e^{-2\pi} < 1$ 。以下用到两个简单事实：
>
> $$\sqrt{2}\pi>4,\qquad\frac{\sqrt{2}}{2}<1.$$
>
> 第一步: 平移, 把每个区间化为同一个形状. 当 $x \in ((2n-1)\pi, (2n+1)\pi)$ 时, 令 $x = 2n\pi + t$, 则 $t \in (-\pi, \pi)$, 并且
>
> $$e^{-x}=c_{n}e^{-t},\qquad\cos2x=\cos(4n\pi+2t)=\cos2t,$$
>
> $$x\sin x=(2n\pi+t)\sin(2n\pi+t)=(2n\pi+t)\sin t.$$
>
> 所以 $f(x)=0$ 在该区间内等价于
>
> $$\varphi_{n}(t):=c_{n}e^{-t}+\cos2t+(2n\pi+t)\sin t=0,\qquad t\in(-\pi,\pi).$$
>
> 这一步把「对每个 n 都要重新讨论」变成了「对一切 $n \geqslant 1$ 一次性估计」，其中与 n 有关的部分只有 $c_{n} \leqslant e^{-2\pi} < 1$ 与 $2n\pi + t$.
>
> 第二步： $t\in(0,\pi)$ 时 $\varphi_{n}(t)>0$ ，这一段无根．当 $t\in\left(0,\frac{\pi}{4}\right)\cup\left(\frac{3\pi}{4},\pi\right)$ 时 $\cos2t>0$ ，而 $c_{n}e^{-t}>0$ 、 $(2n\pi+t)\sin t>0$ ，故 $\varphi_{n}(t)>0$
>
> 当 $t \in \left[\frac{\pi}{4}, \frac{3\pi}{4}\right]$ 时 $\sin t \geqslant \frac{\sqrt{2}}{2}$，且 $2n\pi + t \geqslant 2\pi + \frac{\pi}{4} = \frac{9\pi}{4}$，于是
>
> $$\left(2n\pi+t\right)\sin t\geqslant\frac{9\pi}{4}\cdot\frac{\sqrt{2}}{2}=\frac{9\sqrt{2}\pi}{8}>\frac{9}{2}>1\geqslant-\cos2t,$$
>
> 仍有 $\varphi_{n}(t)>0$ 。所以 $(0,\pi)$ 内没有根。
>
> 第三步： $t \in (-\pi, 0)$ 时恰有两根。令 $s = -t \in (0, \pi)$，则
>
> $$\psi_{n}(s):=\varphi_{n}(-s)=c_{n}e^{s}+\cos2s-\left(2n\pi-s\right)\sin s.$$
>
> 把 $(0,\pi)$分成三段，逐段判断 $\psi_{n}$的走向与符号.
>
> (i) 左段 $s \in (0, \frac{\pi}{4})$. 此时 $\sin 2s > 0$, 故 $-2\sin 2s < 0$, 于是
>
> $$\begin{aligned}\psi_{n}^{\prime}(s)&=c_{n}e^{s}-2\sin2s+\sin s-\left(2n\pi-s\right)\cos s\\ &<c_{n}e^{s}+\sin s-\left(2n\pi-s\right)\cos s.\end{aligned}$$
>
> 由 $s \leqslant \frac{\pi}{4}$ 及 $\cos s$ 在 $(0, \frac{\pi}{2})$ 上递减，
>
> $$\left(2n\pi-s\right)\cos s\geqslant\left(2\pi-\frac{\pi}{4}\right)\frac{\sqrt{2}}{2}=\frac{7\sqrt{2}\pi}{8}>\frac{7}{2},$$
>
> 而
>
> $$c_{n}e^{s}+\sin s\leqslant e^{-7\pi/4}+\frac{\sqrt{2}}{2}<1+\frac{\sqrt{2}}{2}<2<\frac{7}{2},$$
>
> 所以 $\psi_{n}^{\prime}(s)<0:\psi_{n}$ 在 $(0,\frac{\pi}{4})$ 上严格递减. 又
>
> $$\psi_{n}(0)=1+c_{n}>0,$$
>
> 而 $\psi_{n}\left(\frac{\pi}{4}\right)<0$ (见下一段)，故 $\psi_{n}$ 在 $(0,\frac{\pi}{4})$ 上恰有一个零点.
>
> (ii) 中段 $s \in \left[\frac{\pi}{4}, \frac{3\pi}{4}\right]$. 此时 $\sin s \geqslant \frac{\sqrt{2}}{2}$，且 $2n\pi - s \geqslant 2n\pi - \frac{3\pi}{4} \geqslant \frac{5\pi}{4}$，所以
>
> $$\left(2n\pi-s\right)\sin s\geqslant\frac{5\pi}{4}\cdot\frac{\sqrt{2}}{2}=\frac{5\sqrt{2}\pi}{8}>\frac{5}{2},$$
>
> 而
>
> $$c_{n}e^{s}+\cos2s\leqslant c_{n}e^{3\pi/4}+1\leqslant e^{-5\pi/4}+1<2<\frac{5}{2},$$
>
> 于是 $\psi_{n}(s) < 0$: 这一段没有零点.
>
> (iii) 右段 $s \in \left[\frac{3\pi}{4}, \pi\right)$. 此时 $\sin s > 0$、 $\cos s < 0$, 又 $2s \in \left(\frac{3\pi}{2}, 2\pi\right)$ 给出 $\sin 2s < 0$, 所以
>
> $$\psi_{n}^{\prime}(s)=c_{n}e^{s}-2\sin2s+\sin s-\left(2n\pi-s\right)\cos s$$
>
> 中的四项都为正，即 $\psi_{n}^{\prime}(s)>0:\psi_{n}$ 在 $\left[\frac{3\pi}{4},\pi\right)$ 上严格递增。结合
>
> $$\psi_{n}\left(\frac{3\pi}{4}\right)<0,\qquad\psi_{n}(\pi)=1+c_{n}e^{\pi}>0,$$
>
> 可知 $\psi_{n}$ 在 $\left(\frac{3\pi}{4},\pi\right)$ 上恰有一个零点.
>
> 综合三段： $\psi_{n}$ 在 $(0,\pi)$ 上恰有两个零点
>
> $$s_{1}\in\left(0,\frac{\pi}{4}\right),\qquad s_{2}\in\left(\frac{3\pi}{4},\pi\right).$$
>
> 第四步：换回原变量. $f(x)$ 在 $((2n-1)\pi,(2n+1)\pi)$ 内的两个根就是 $x=2n\pi-s$，即
>
> $$x_{2n}=2n\pi-s_{1}\in\left(2n\pi-\frac{\pi}{4},2n\pi\right),$$
>
> $$x_{2n-1}=2n\pi-s_{2}\in\left((2n-1)\pi,2n\pi-\frac{3\pi}{4}\right).$$
>
> 这两个区间都是 $((2n-1)\pi,(2n+1)\pi)$ 的子区间，且后者完全位于前者左边，故 $x_{2n-1}<x_{2n}$；又由第二、三步，该区间内再没有别的根。命题得证。在每个区间内令 $x=n\pi+t$ $(t\in(-\pi,\pi))$，方程化为 $2t^{2}-(-1)^{n}n\pi t-1-e^{-n\pi}-O(t^{3})=0$，它在该区间内恰有两个解（对应抛物线 $2t^{2}=(-1)^{n}n\pi t+1+\cdots$ 的两个交点）。令 $\tau=nt$，则 $(-1)^{n}\pi\tau=-1+O(n^{-2})$，故
>
> $$\lim_{n\to\infty}(-1)^{n} n\left(x_{n}-n\pi\right)=-\frac{1}{\pi}.$$

**4.** (难度:★★★★★) 设 $F(x)=\int_{0}^{x}e^{-t}\left(1+\frac{t}{1!}+\frac{t^{2}}{2!}+\cdots+\frac{t^{n}}{n!}\right)dt$，其中 n>1 为整数. 证明: 方程 $F(x)=\frac{n}{2}$ 在区间 $\left(\frac{n}{2},n\right)$ 内至少有一个根.

> [!answer]- 原书参考答案（B.0.5 第 4 题，未逐题独立验算）
> **4.** 只需比较 $F\left(\frac{n}{2}\right)$ 与 $\frac{n}{2}$、 $F(n)$ 与 $\frac{n}{2}$ 的大小: 前者容易 (把幂级数放大成 $e^{t}$), 后者要做一个巧妙的配对把 $e^{-n}\sum\frac{n^{k}}{k!}$ 控制住. $F(x)$ 的被积函数连续且为正, 故 $F(x)$ 在 $\left(\frac{n}{2}, n\right)$ 上单调递增.
>
> 第一步: $F\left(\frac{n}{2}\right) < \frac{n}{2}$. 由 $1 + \frac{t}{1} + \cdots + \frac{t^n}{n!} < e^t$ 得
>
> $$F\left(\frac{n}{2}\right)=\int_{0}^{\frac{n}{2}}e^{-t}\left(1+\frac{t}{1}+\cdots+\frac{t^{n}}{n!}\right)\mathrm{d}t<\int_{0}^{\frac{n}{2}}e^{-t}e^{t}\mathrm{d}t=\frac{n}{2}.$$
>
> 第二步： $F(n) > \frac{n}{2}$. 对 $F(n)$ 作分部积分：
>
> $$F(n)=-\int_{0}^{n}\left(1+\frac{t}{1}+\cdots+\frac{t^{n}}{n!}\right)\mathrm{d}\left(e^{-t}\right),$$
>
> 即
>
> $$F(n)=1-e^{-n}\sum_{k=0}^{n}\frac{n^{k}}{k!}(n+1-k)=n+1-e^{-n}S_{1},$$
>
> 其中 $S_{1}=\sum_{k=0}^{n}(n+1-k)\frac{n^{k}}{k!}$. 把 $S_{1}$ 的系数“倒过来”记
>
> $$S_{2}=\sum_{k=0}^{n}(k+1)\frac{n^{k}}{k!},$$
>
> 则 $S_{2}>S_{1}$，且
>
> $$S_{1}+S_{2}=\left(n+2\right)\sum_{k=0}^{n}\frac{n^{k}}{k!}>2S_{1}\implies S_{1}<\frac{n+2}{2}\sum_{k=0}^{n}\frac{n^{k}}{k!}.$$
>
> 于是（注意 $\sum_{k=0}^{n}\frac{n^{k}}{k!}<e^{n}$）
>
> $$F(n)>n+1-\frac{n+2}{2}e^{-n}\sum_{k=0}^{n}\frac{n^{k}}{k!}>n+1-\frac{n+2}{2}=\frac{n}{2}.$$
>
> 第三步:零点定理.由 $F\left(\frac{n}{2}\right)-\frac{n}{2}<0$、 $F(n)-\frac{n}{2}>0$及 $F(x)$连续、单调递增,故 $F(x)=\frac{n}{2}$在 $\left(\frac{n}{2},n\right)$内至少有一个根.本题的两个技术点:(1)用 $1+\frac{t}{1}+\cdots+$
>
> $\frac{t^n}{n!} < e^t$ 把 $F\left(\frac{n}{2}\right)$ 压到 $\frac{n}{2}$ 以下; (2) 对 $F(n)$ 分部积分后, 把“系数 $n+1-k$ 与 $k+1$”配对 $(S_1+S_2)$, 再配 $\sum \frac{n^k}{k!} < e^n$, 得到 $F(n) > \frac{n}{2}$. 配对求和是这类“带阶乘的积分”的常用手法.

## 1.6 积分极限

定积分与极限结合，计算时通常方法为先猜后证，猜出对应极限后，需与原始积分做差放缩使余项为无穷小。同时，适当了解一致收敛、拉普拉斯方法等数学系知识，也便于帮助理解此类题目。

**1.** (难度:★★★) 设 $I_{n}=n\int_{1}^{a}\frac{\mathrm{d}x}{1+x^{n}}$，其中 a>1. 求极限 $\lim_{n\to\infty}I_{n}$.

> [!answer]- 原书参考答案（B.0.6 第 1 题，未逐题独立验算）
> **1.** 作换元 $t = \frac{1}{x}$，则 $\mathrm{d}x = -\frac{\mathrm{d}t}{t^{2}}$，且 $x:1 \to a$ 对应 $t:1 \to \frac{1}{a}$，于是
>
> $$I_{n}=n\int_{\frac{1}{a}}^{1}\frac{t^{n-2}}{t^{n}+1}\mathrm{d}t=\int_{\frac{1}{a}}^{1}\frac{1}{t}\cdot\frac{\mathrm{d}(t^{n})}{t^{n}+1}=\int_{\frac{1}{a}}^{1}\frac{1}{t}\mathrm{d}\ln(t^{n}+1).$$
>
> 分部积分 (注意 t = 1 处 $\ln(t^{n} + 1) = \ln 2$) 得
>
> $$I_{n}=\ln2+\int_{\frac{1}{a}}^{1}\frac{\ln(t^{n}+1)}{t^{2}}\mathrm{d}t.$$
>
> 再由 $0 < \ln(t^{n} + 1) \leqslant t^{n} (0 < t \leqslant 1)$ 得
>
> $$|I_{n}-\ln2|\leqslant\int_{\frac{1}{a}}^{1}\frac{t^{n}}{t^{2}}\mathrm{d}t=\frac{1-\left(\frac{1}{a}\right)^{n-1}}{n-1}\longrightarrow0,$$
>
> 由夹逼定理， $\lim_{n\to\infty}I_n=\ln2$

**2.** (难度: ★★★★) 求极限 $\lim_{n \to \infty} n \int_{0}^{1} \frac{e^{x}}{1 + (nx)^{2} + n^{3}x^{4}} \, dx$.

> [!answer]- 原书参考答案（B.0.6 第 2 题，未逐题独立验算）
> **2.** 先用 t = nx 把 n 挪到积分限，并把被积式整理成 $\frac{e^{t/n}}{1 + t^2 + t^4/n} (e^{t/n} \to 1, \, t^4/n \to 0)$，于是它应当收敛到 $\frac{1}{1 + t^2}$；再把差放缩成 $O(1/n)$。作换元 t = nx，则 $\mathrm{d}x = \frac{\mathrm{d}t}{n}$，且 $x: 0 \to 1$ 对应 $t: 0 \to n$，于是
>
> $$I_{n}=n\int_{0}^{1}\frac{e^{x}}{1+(nx)^{2}+n^{3}x^{4}}\mathrm{d}x=\int_{0}^{n}\frac{e^{t/n}}{1+t^{2}+\frac{t^{4}}{n}}\mathrm{d}t.$$
>
> 把它与 $\int_{0}^{n}\frac{dt}{t^{2}+1}$ 比较:
>
> $$\left|I_{n}-\int_{0}^{n}\frac{\mathrm{d}t}{t^{2}+1}\right|=\left|\int_{0}^{n}\left(\frac{e^{t/n}}{1+t^{2}+\frac{t^{4}}{n}}-\frac{1}{t^{2}+1}\right)\mathrm{d}t\right|$$
>
> $$\leqslant\int_{0}^{n}\frac{\left(t^{2}+1\right)\left(e^{t/n}-1\right)+\frac{t^{4}}{n}}{\left(t^{2}+1\right)\left(1+t^{2}+\frac{t^{4}}{n}\right)}\mathrm{d}t\leqslant\int_{0}^{n}\frac{\frac{t}{n}e}{t^{2}+1}\mathrm{d}t+\int_{0}^{n}\frac{t^{4}}{\left(t^{2}+1\right)\left(n t^{2}+t^{4}\right)}\mathrm{d}t.$$
>
> 第一项用 $\int_{0}^{n}\frac{t}{t^{2}+1}dt=\frac{1}{2}\ln(n^{2}+1)$ 得
>
> $$\int_{0}^{n}\frac{\frac{t}{n}e}{t^{2}+1}\mathrm{d}t\leqslant\frac{e}{n}\int_{0}^{n}\frac{t}{t^{2}+1}\mathrm{d}t=\frac{e}{2n}\ln\left(n^{2}+1\right)\longrightarrow0;$$
>
> 第二项
>
> $$\begin{aligned}\int_{0}^{n}\frac{t^{4}}{\left(t^{2}+1\right)\left(nt^{2}+t^{4}\right)}\mathrm{d}t&=\int_{0}^{n}\frac{t^{2}}{t^{2}+1}\cdot\frac{\mathrm{d}t}{n+t^{2}}\\&\leqslant\int_{0}^{n}\frac{\mathrm{d}t}{n+t^{2}}=\frac{1}{\sqrt{n}}\arctan\sqrt{n}\longrightarrow0.\end{aligned}$$
>
> 两项都趋于0.由夹逼定理
>
> $$\lim_{n\to\infty}I_{n}=\int_{0}^{+\infty}\frac{\mathrm{d}t}{t^{2}+1}=\frac{\pi}{2}.$$
>
> 做法与 1.6.2 完全一致: 换元把 n 挪走, 再与 $\frac{1}{1+t^{2}}$ 比较、把差放缩成无穷小. 注意被积式里的 $t^{4}/n$ 相当于在 $1+t^{2}$ 上加了一个小量, 而分母“反而变大”使得整式偏小, 这正是需要两边都估计的原因.

**3.** (难度:★★★) 对于连续可导的函数 $y = f(x)$，满足：

$$\begin{cases}\dfrac{\mathrm{d}y}{\mathrm{d}x}-xy=xe^{x^{2}},\\y(0)=1.\end{cases}$$

(1) 求 $y = f(x)$ 的解析式.

(2) 证明: $\lim_{n \to \infty} \int_{0}^{1} \frac{nf(x)}{n^{2}x^{2}+1} dx = \frac{\pi}{2}$.

> [!answer]- 原书参考答案（B.0.6 第 3 题，未逐题独立验算）
> **3.** (1) 是一道一阶线性微分方程, 用积分因子 $e^{-x^{2}/2}$ 即可. (2) 先把 n 通过换元 t = nx 挪到积分限上, 再比较 $e^{t^{2}/n^{2}}$ 与 1, 把差放缩成无穷小. (1) 方程 $y' - xy = xe^{x^{2}}$ 的积分因子为 $e^{-x^{2}/2}$, 两边同乘得
>
> $$\left(ye^{-x^{2}/2}\right)^{\prime}=xe^{x^{2}/2},$$
>
> 故 $ye^{-x^2/2} = \int xe^{x^2/2} \, dx = e^{x^2/2} + C$，即 $y = e^{x^2} + C e^{x^2/2}$。由 $y(0) = 1$ 得 $1 = 1 + C$，即 C = 0，所以
>
> $$f(x)=e^{x^{2}}.$$
>
> (2) 作换元 t = nx，则 $\mathrm{d}x = \frac{\mathrm{d}t}{n}$，于是
>
> $$I_{n}=\int_{0}^{1}\frac{n f(x)}{n^{2}x^{2}+1}\mathrm{d}x=\int_{0}^{n}\frac{e^{t^{2}/n^{2}}}{t^{2}+1}\mathrm{d}t.$$
>
> 由 $\left|e^{u}-1\right|\leqslant|u|e^{|u|}$ ( $u=\frac{t^{2}}{n^{2}},t\leqslant n$) 得
>
> $$\left|I_{n}-\int_{0}^{n}\frac{\mathrm{d}t}{t^{2}+1}\right|\leqslant\int_{0}^{n}\frac{\left|e^{t^{2}/n^{2}}-1\right|}{t^{2}+1}\mathrm{d}t\leqslant\frac{e}{n^{2}}\int_{0}^{n}\frac{t^{2}}{t^{2}+1}\mathrm{d}t\leqslant\frac{e}{n}\longrightarrow0.$$
>
> 由夹逼定理，
>
> $$\lim_{n\to\infty}I_{n}=\int_{0}^{+\infty}\frac{\mathrm{d}t}{t^{2}+1}=\frac{\pi}{2}.$$
>
> 整道题就是本节”换元 + 比较”的模板：换元把 n 挪到积分限，比较时把 $|e^u - 1|$ 控制成 $|u|e^{|u|}$，于是误差被夹成 $O\left(\frac{1}{n}\right)$。注意积分上限随 n 变到 $+\infty$，最终极限是反常积分 $\int_0^{+\infty} \frac{dt}{t^2 + 1} = \frac{\pi}{2}$。

**4.** （难度：★★★★）求极限：

$$\lim_{n\to\infty}\int_{0}^{1}\frac{\left(1+x+\frac{x^{2}}{2}+\cdots+\frac{x^{n-1}}{n-1}\right)^{n+1}}{\left(1+x+\frac{x^{2}}{2}+\cdots+\frac{x^{n}}{n}\right)^{n}}\mathrm{d}x.$$

> [!answer]- 原书参考答案（B.0.6 第 4 题，未逐题独立验算）
> **4.** 记 $S_{n}(x)=1+x+\cdots+\frac{x^{n}}{n}$，则 $\frac{S_{n-1}(x)^{n+1}}{S_{n}(x)^{n}}=S_{n-1}(x)\left(\frac{S_{n-1}}{S_{n}}\right)^{n}$，而 $\left(\frac{S_{n-1}}{S_{n}}\right)^{n}=\exp\left[-\frac{x^{n}}{S_{n}}(1+o(1))\right]\rightarrow1(x<1)$，且被积函数 $\leqslant S_{n-1}\leqslant\mathrm{e}$，故由控制收敛定理
>
> $$\lim_{n\to\infty}\int_{0}^{1}\frac{\left(1+x+\cdots+\frac{x^{n-1}}{n-1}\right)^{n+1}}{\left(1+x+\cdots+\frac{x^{n}}{n}\right)^{n}}\mathrm{d}x=\int_{0}^{1}\mathrm{e}^{x}\mathrm{d}x=\mathrm{e}-1.$$

**5.** (难度:★★★★★) 设 $I_{n} = \int_{0}^{10n} \left(1 - \left|\sin\frac{x}{n}\right|\right)^{n} dx$, $n \in \mathbb{N}^{*}$, 求极限 $\lim_{n \to \infty} I_{n}$.

> [!answer]- 原书参考答案（B.0.6 第 5 题，未逐题独立验算）
> **5.** 令 x = nt: $I_{n} = n \int_{0}^{10} (1 - |\sin t|)^{n} dt$. [0,10] 内 $k\pi (k = 0,1,2,3)$ 附近各有贡献: 端点 t = 0 贡献 1, 内点 $t = \pi, 2\pi, 3\pi$ 各贡献 2, 故
>
> $$\lim_{n\to\infty}I_{n}=1+2+2+2=7.$$

---

# 强化篇·第二章 一元微分学

## 2.1 函数构造相关证明

最常规的考察方式, 通过构造函数, 结合中值定理, 完成与其相关的各种存在性证明.

**1.** (难度:★★★) 设函数 $f(x)$ 在 $[0, +\infty)$ 上连续，且 $\int_{0}^{1} f(x) \, dx = \frac{1}{2}$， $\lim_{x \to +\infty} \frac{f(x)}{x} = 0$。证明: 存在 $\xi \in (0, +\infty)$，使得 $f(\xi) - \xi = 0$。

> [!answer]- 原书参考答案（C.0.1 第 1 题，未逐题独立验算）
> **1.** 第一步：把结论写成“某个函数等于0”。结论是 $f(\xi)+\xi=0$，于是令
>
> $$F(x)=f(x)+x.$$
>
> 要证的结论就是"F(x) 在 $(0,+\infty)$ 内有零点". 两个条件各管一头: 积分条件负责造出 F(x) $\leq$ 0 的位置, 极限条件负责造出 F(x) > 0 的位置.
>
> 第二步: 由积分条件得到 $F(x)$ 的非正性. 注意 $\int_{0}^{1}x\,dx=\frac{1}{2}$, 故
>
> $$\int_{0}^{1}F(x)\mathrm{d}x=\int_{0}^{1}f(x)\mathrm{d}x+\int_{0}^{1}x\mathrm{d}x=-\frac{1}{2}+\frac{1}{2}=0.$$
>
> 于是只有两种可能：
>
> 若 $F(x)$ 在 $[0,1]$ 上恒非负，则由 $\int_{0}^{1}F(x)\,\mathrm{d}x=0$ 与 $F(x)$ 连续知 $F(x)\equiv0$，取 $\xi=\frac{1}{2}$ 即得 $f\left(\frac{1}{2}\right)+\frac{1}{2}=0$，结论成立；
>
> 否则 $(F(x)$ 在 $[0,1]$ 上取到负值) 存在 $c\in[0,1]$，使 $F(c)<0$.
>
> 第三步：由极限条件得到 $F(x)$ 的正性。因为 $\lim_{x\to+\infty}\frac{f(x)}{x}=0$，所以
>
> $$\lim_{x\to+\infty}\frac{F(x)}{x}=\lim_{x\to+\infty}\left(\frac{f(x)}{x}+1\right)=1>0.$$
>
> 由极限的保号性，存在 X > 0，使当 x > X 时 $\frac{F(x)}{x} > 0$，即 $F(x) > 0$。取定一个 $x_{1} > X$（不妨再要求 $x_{1} > 1$），就有 $F(x_{1}) > 0$。
>
> 第四步: 用零点存在定理收尾. 在第二种情形下, $F(x)$ 在 $[c, x_1]$ 上连续, 且 $F(c) < 0$, $F(x_1) > 0$, 由零点存在定理, 存在 $\xi \in (c, x_1) \subset (0, +\infty)$, 使 $F(\xi) = 0$, 即
>
> $$f(\xi)+\xi=0.$$
>
> 本题示范了基本模型的完整流程: 先把结论写成 $F(\xi) = 0$, 再用两个已知条件分别把 $F(x)$ 逼到“异号”, 最后用零点存在定理. 若 $F(x)$ 在端点处同号 (零点定理失效), 才需要构造 $F(x)$ 的原函数、改用罗尔定理 (见下面的子目).

**2.** (难度:★★★)设函数 $f(x)$在 $[0,1]$上连续，在 $(0,1)$内可导，且有 $f(1)=4\int_{0}^{\frac{1}{4}}e^{1-x^{3}}f(x)dx$.

证明:至少存在一点 $\xi\in(0,1)$，使得 $f'(\xi)=3\xi^{2}f(\xi)$.

> [!answer]- 原书参考答案（C.0.1 第 2 题，未逐题独立验算）
> **2.** 第一步：把结论化成“某函数的导数为0”——先解微分方程.要证的结论是
>
> $$f^{\prime}(\xi)-3\xi^{2}f(\xi)=0.$$
>
> 把 $\xi$换成x，得到微分方程
>
> $$y^{\prime}-3x^{2}y=0.$$
>
> 这是一个可分离变量的一阶线性方程：
>
> $$\frac{\mathrm{d}y}{y}=3x^{2}\mathrm{d}x\implies\ln|y|=x^{3}+C\implies y=C e^{x^{3}},$$
>
> 即
>
> $$ye^{-x^{3}}=C.$$
>
> 按2.2.1的基本模型，取辅助函数
>
> $$F(x)=f(x)e^{-x^{3}},\qquad F^{\prime}(x)=e^{-x^{3}}\left[f^{\prime}(x)-3x^{2}f(x)\right].$$
>
> 只要找到两点使 $F(x)$ 相等，罗尔定理就能给出所要的 $\xi$.
>
> 第二步: 把条件翻译成 $F(x)$ 的端点条件. 把题设的等式两边同时乘 e 的合适幂次, 凑出 $F(x)$:
>
> $$f(1)=4\int_{0}^{\frac{1}{4}}e^{1-x^{3}}f(x)\mathrm{d}x=4e\int_{0}^{\frac{1}{4}}e^{-x^{3}}f(x)\mathrm{d}x=4e\int_{0}^{\frac{1}{4}}F(x)\mathrm{d}x.$$
>
> 由积分中值定理（也即第一积分中值定理），存在 $c \in \left[0, \frac{1}{4}\right]$，使
>
> $$\int_{0}^{\frac{1}{4}}F(x)\mathrm{d}x=F(c)\cdot\frac{1}{4},$$
>
> 代入得 $f(1)=4e\cdot\frac{F(c)}{4}=eF(c)$，即
>
> $$F(c)=\frac{f(1)}{e}=f(1)e^{-1}=F(1).$$
>
> 第三步:罗尔定理收尾.由于 $F(x)$ 在 $[c,1]$ 上连续、在 $(c,1)$ 内可导,且 $F(c) = F(1)$,由罗尔定理,存在 $\xi \in (c,1) \subset (0,1)$,使 $F'(\xi) = 0$,即
>
> $$e^{-\xi^{3}}\left[f^{\prime}(\xi)-3\xi^{2}f(\xi)\right]=0\implies f^{\prime}(\xi)=3\xi^{2}f(\xi).$$
>
> 怎么想到构造 $F(x) = f(x)e^{-x^3}$ 就是上面第一步做的“解微分方程”：结论里 $f(x)$ 与 $f'(x)$ 的系数构成了一阶线性方程 $y' - 3x^2y = 0$，它的通解是 $y = Ce^{x^3}$，把常数分离出来就得到 $ye^{-x^3} = C$——这正是辅助函数。题目中那个 $e^{1-x^3}$ 也不是巧合，它就是为凑出 $F(x) = f(x)e^{-x^3}$ 而设计的。

**3.** (难度:★★★★) 设函数 $f(x)$ 在区间 $[0,1]$ 上二阶可导, $f(0)=0$, 且 $f(1)=1$. 求证: 存在 $\xi \in (0,1)$, 使得 $\xi f''(\xi) + (1+\xi)f'(\xi) = 1 + \xi$.

> [!answer]- 原书参考答案（C.0.1 第 3 题，未逐题独立验算）
> **3.** 第一步: 把结论写成微分方程. 把 $\xi$ 换成 x, 并注意右端的 $1 + x$ 与 $(1 + x)y'$ 需要"配平":
>
> $$xy^{\prime \prime}+(1+x)y^{\prime}-(1+x)=0\iff xy^{\prime \prime}+(1+x)\left(y^{\prime}-1\right)=0.$$
>
> 这是一个二阶线性方程；下面先把它解出来。
>
> 第二步：解方程（先找特解，再解齐次方程）.
>
> (i) 找特解: 取 y = x, 此时 $y' = 1$、 $y'' = 0$, 代入左边得
>
> $$x\cdot0+(1+x)\cdot1-(1+x)=0,$$
>
> 故 y = x 是特解.
>
> (ii) 解齐次方程 $xy'' + (1 + x)y' = 0$: 令 u = y', 则 $xu' + (1 + x)u = 0$, 即
>
> $$\frac{u^{\prime}}{u}=-\frac{1}{x}-1\implies\ln|u|=-\ln x-x+C\implies u=\frac{C_{1}e^{-x}}{x}.$$
>
> (iii) 写出通解：
>
> $$y=x+C_{1}\int\frac{e^{-x}}{x}\mathrm{d}x+C_{2}$$
>
> （含两个任意常数 $C_{1}, C_{2}$）.
>
> 第三步：对通解求导，把常数解出来。由上式
>
> $$y^{\prime}=1+\frac{C_{1}e^{-x}}{x}\implies C_{1}=x e^{x}\left[y^{\prime}(x)-1\right],$$
>
> 即常数 $C_{1}$ 恰好由 $G(x)=y'(x)-1$ 乘上 $xe^{x}$ 表示，而 $C_{2}$ 只出现在通解本身里。于是辅助函数取
>
> $$G(x)=x e^{x}\left[f^{\prime}(x)-1\right],$$
>
> 它满足
>
> $$G^{\prime}(x)=e^{x}\Big\{x f^{\prime\prime}(x)+(1+x)\left[f^{\prime}(x)-1\right]\Big\},$$
>
> 所以 $G'(\xi) = 0$ 正是所要证的等式.
>
> 第四步：凑出 $G(x)$ 的两个等值点。注意
>
> $$G(0)=0\cdot e^{0}\left[f^{\prime}(0)-1\right]=0.$$
>
> 还需要一个 $G(x)$ 取 0 的点. 由拉格朗日中值定理, 存在 $c \in (0,1)$, 使
>
> $$f^{\prime}(c)=\frac{f(1)-f(0)}{1-0}=1,$$
>
> 于是 $f'(c)-1=0$ ，从而
>
> $$G(c)=ce^{c}\left[f^{\prime}(c)-1\right]=0=G(0).$$
>
> 第五步:罗尔定理收尾. 在 $[0,c]$ 上对 $G(x)$ 用罗尔定理, 存在 $\xi \in (0,c) \subset (0,1)$, 使 $G'(\xi) = 0$, 即
>
> $$\xi f^{\prime\prime}(\xi)+(1+\xi)\left[f^{\prime}(\xi)-1\right]=0\implies\xi f^{\prime\prime}(\xi)+(1+\xi)f^{\prime}(\xi)=1+\xi.$$
>
> 构造思路小结. 这类二阶构造题的固定流程是: (1) 把结论里的 $\xi$ 换成 x, 写出微分方程; (2) 求出含两个常数的通解 (本题先找特解 y = x, 再解齐次方程, 得到 $y = x + C_1 \int \frac{e^{-x}}{x} \, dx + C_2$); (3) 对通解求导, 把常数解出来——本题得到 $C_1 = xe^x [y'(x) - 1]$, 取它的右侧作辅助函数; (4) 用已知条件凑出两个等值点, 再用罗尔定理. 题目里的 $f(1) - f(0)$ 恰好等于 1, 正是为了让中值点满足 $f'(c) = 1$.

**4.** (难度:★★★★) 设函数 $f(x)$ 在 $(-\infty, +\infty)$ 上二阶可导，且 $f(0) = 0$. 证明: 存在 $\xi \in \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$，使得 $f''(\xi) = 3f'(\xi) \tan \xi + 2f(\xi)$.

> [!answer]- 原书参考答案（C.0.1 第 4 题，未逐题独立验算）
> **4.** 把结论里的 $\xi$ 换成 x，得到二阶线性方程
>
> $$y^{\prime\prime}-3y^{\prime}\tan x-2y=0.$$
>
> 关键是把3拆成$1+2$：把$\tan x=\frac{\sin x}{\cos x}$化开后，$3y'\tan x$里的“3”正好是两块“平衡”出来的——一块来自$(y'\cos x)'$（系数1），另一块来自$(2y\sin x)'$（系数2）。按这个平衡去配，就能把方程整理成$(y'\cos x-2y\sin x)'=0$，从而先解出一阶方程$y'\cos x-2y\sin x=C_{1}$，再积一次得到含$C_{1},C_{2}$的通解。最后对通解求导，把常数$C_{1}$用$y,y'$表示出来——那个表达式就是辅助函数。第一步：先看$3=1+2$的平衡，把方程整理成“某个导数等于$0$”。把$\tan x=\frac{\sin x}{\cos x}$代入后两边同乘$\cos x$（在$\left(-\frac{\pi}{2},\frac{\pi}{2}\right)$内$\cos x>0$），
>
> $$y^{\prime\prime}\cos x-3y^{\prime}\sin x-2y\cos x=0.$$
>
> 左边的 $3y' \sin x$ 是两块拼起来的 (这就是 $3 = 1 + 2$)：
>
> $$\underbrace{y^{\prime\prime}\cos x-y^{\prime}\sin x}_{ 来自 (y^{\prime}\cos x)^{\prime}}\underbrace{-2y^{\prime}\sin x-2y\cos x}_{ 来自 (2y\sin x)^{\prime}}=0,$$
>
> 于是
>
> $$\left[y^{\prime}\cos x-2y\sin x\right]^{\prime}=0.$$
>
> 第二步: 解出通解 (含两个常数). 上式表明 $y' \cos x - 2y \sin x$ 是常数, 记作 $C_1$:
>
> $$y^{\prime}\cos x-2y\sin x=C_{1}.$$
>
> 这是一个一阶线性微分方程，把它整理成标准形式（两边同除 $\cos x$，在 $\left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$ 内 $\cos x > 0$）：
>
> $$y^{\prime}-2y\tan x=\frac{C_{1}}{\cos x},\qquad 即 \qquad y^{\prime}+P(x)y=Q(x),$$
>
> 其中
>
> $$P(x)=-2\tan x,\qquad Q(x)=\frac{C_{1}}{\cos x}.$$
>
> 套用一阶线性方程的通解公式 $y = e^{-\int P(x) \, dx}$ $\left[ \int Q(x) e^{\int P(x) \, dx} \, dx + C_2 \right]$.
>
> 先算两个因子：
>
> $$\int P(x)\mathrm{d}x=\int-2\tan x\mathrm{d}x=2\ln\cos x,$$
>
> $$e^{\int P(x)d x}=\cos^{2}x,\quad e^{-\int P(x)d x}=\frac{1}{\cos^{2}x}.$$
>
> 代入公式:
>
> $$\begin{aligned}y&=\frac{1}{\cos^{2}x}\left[\int\frac{C_{1}}{\cos x}\cdot\cos^{2}x\mathrm{d}x+C_{2}\right]=\frac{1}{\cos^{2}x}\left[C_{1}\int\cos x\mathrm{d}x+C_{2}\right]\\&=\frac{C_{1}\sin x+C_{2}}{\cos^{2}x},\end{aligned}$$
>
> 也就是
>
> $$y\cos^{2}x=C_{1}\sin x+C_{2}.$$
>
> 第三步：对通解求导，把常数“解出来”。对通解两边求导：
>
> $$y^{\prime}\cos^{2}x-2y\sin x\cos x=C_{1}\cos x\implies C_{1}=y^{\prime}\cos x-2y\sin x,$$
>
> 而由通解本身
>
> $$C_{2}=y\cos^{2}x-C_{1}\sin x.$$
>
> 也就是说: 常数 $C_{1}$ 恰好由 $F(x)=y'\cos x-2y\sin x$ 表示, 而 $C_{2}$ 只出现在 $G(x)=y\cos^{2}x$ 里.
>
> 第四步：把 $f(x)$ 代进去，用罗尔定理. 取
>
> $$F(x)=f^{\prime}(x)\cos x-2f(x)\sin x,\qquad G(x)=f(x)\cos^{2}x,$$
>
> 则 $G'(x) = \cos x F(x)$，且由 $f(0) = 0$ 与 $\cos \left( \pm \frac{\pi}{2} \right) = 0$ 得
>
> $$G(0)=f(0)\cdot1=0,\qquad G\Big(\pm\frac{\pi}{2}\Big)=f\Big(\pm\frac{\pi}{2}\Big)\cdot0=0.$$
>
> 分别在 $\left[-\frac{\pi}{2},0\right]$ 与 $\left[0,\frac{\pi}{2}\right]$ 上用罗尔定理，存在 $c_{1}\in\left(-\frac{\pi}{2},0\right)$、 $c_{2}\in\left(0,\frac{\pi}{2}\right)$，使 $G'(c_{1})=G'(c_{2})=0$；因该两点处 $\cos x\neq0$，故
>
> $$F(c_{1})=F(c_{2})=0.$$
>
> 第五步：对 $F(x)$ 用罗尔定理，回到原方程. 在 $[c_{1}, c_{2}] \subset \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$ 上对 $F(x)$ 用罗尔定理，存在 $\xi \in (c_{1}, c_{2})$，使 $F'(\xi) = 0$. 再由第一步的恒等式
>
> $$F^{\prime}(x)=\left[f^{\prime}(x)\cos x-2f(x)\sin x\right]^{\prime}=\cos x\left[f^{\prime\prime}(x)-3f^{\prime}(x)\tan x-2f(x)\right]$$
>
> 以及 $\cos\xi>0$，即得
>
> $$f^{\prime\prime}(\xi)-3f^{\prime}(\xi)\tan\xi-2f(\xi)=0.$$
>
> 整道题的来源是”解微分方程”：方程 $y''-3y'\tan x-2y=0$的通解是 $y=\frac{C_1\sin x+C_2}{\cos^2 x}$，对它求导就得到 $C_1=y'\cos x-2y\sin x$——这正是辅助函数 $F(x)$的来历；而通解里的 $y\cos^2 x=C_1\sin x+C_2$直接提示我们取 $G(x)=f(x)\cos^2 x$（它在 $0,\pm\frac{\pi}{2}$处为零，负责提供两个等值点）。配系数时的技巧就一条：把3拆成 $1+2$，让两块求导的贡献在中括号里”平衡”成 $-3y'\sin x$。

**5.** (难度:★★) 设函数 $f(x)$ 在 $[a,b]$ 上连续，在 $(a,b)$ 内二阶可导，且 $f(a)=f(b)=0$， $\int_{a}^{b}f(x)dx=0$。证明：

(1) 存在不相同的 $x_1, x_2 \in (a, b)$，使得 $f'(x_i) = f(x_i)$， $i = 1, 2$;

(2) 存在 $\xi \in (a, b)$, $\xi \neq x_i$, $i = 1, 2$, 使得 $f''(\xi) = f(\xi)$.

> [!answer]- 原书参考答案（C.0.1 第 5 题，未逐题独立验算）
> **5.** (1) $f'(x) = f(x)$ 等价于 $[f(x)e^{-x}]' = 0$，所以要先找 $f(x)e^{-x}$ 的三个零点：端点 a, b 各给一个，再用 $\int_{a}^{b} f(x) \, \mathrm{d}x = 0$ 在内部找第三个. (2) $f''(x) = f(x)$ 等价于 $[e^{x}(f'(x) - f(x))]' = 0$，而 (1) 找到的两个点正好是这个函数的两个零点. (1) 由 $f(a) = f(b) = 0$ 与 $\int_{a}^{b} f(x) \, \mathrm{d}x = 0$ 可知：若 $f(x)$ 在 $(a, b)$ 内不取零（恒正或恒负），则积分不可能为 0；故存在 $c \in (a, b)$ 使 $f(c) = 0$，且 a < c < b.
>
> 要证的是 $f'(x_{i}) = f(x_{i})$，即 $f'(x) - f(x) = 0$。这是一个一阶线性方程（可分离变量），先把它解出来：
>
> $$\frac{\mathrm{d}y}{y}=\mathrm{d}x\implies\ln|y|=x+C\implies y=C e^{x}\implies y e^{-x}=C.$$
>
> 所以辅助函数取 $G(x)=f(x)e^{-x}$，此时 $G'(x)=e^{-x}[f'(x)-f(x)]$。由上面的条件，
>
> $$G(a)=f(a)e^{-a}=0,\qquad G(c)=f(c)e^{-c}=0,\qquad G(b)=f(b)e^{-b}=0.$$
>
> 分别在 $[a,c]$ 与 $[c,b]$ 上用罗尔定理，存在 $x_{1}\in(a,c)$、 $x_{2}\in(c,b)$，使
>
> $$G^{\prime}(x_{1})=G^{\prime}(x_{2})=0.$$
>
> 而 $G'(x) = e^{-x} [f'(x) - f(x)]$，故 $f'(x_1) = f(x_1)$、 $f'(x_2) = f(x_2)$，且 $x_1 \neq x_2$。
>
> (2) 要证 $f''(x) = f(x)$，即二阶线性方程 $y'' - y = 0$.
>
> 第一步: 解出通解. 它的两个线性无关特解是 $e^{x}$ 与 $e^{-x}$，故通解为
>
> $$y=C_{1}e^{x}+C_{2}e^{-x},\qquad 对它求导得 \qquad y^{\prime}=C_{1}e^{x}-C_{2}e^{-x}.$$
>
> 第二步：两式相加减，把常数解出来.
>
> $$y^{\prime}+y=2C_{1}e^{x}\implies C_{1}=\frac{y^{\prime}(x)+y(x)}{2e^{x}},$$
>
> $$y^{\prime}-y=-2C_{2}e^{-x}\implies C_{2}=-\frac{e^{x}}{2}\left[y^{\prime}(x)-y(x)\right].$$
>
> 本题用只含 $C_{2}$ 的那一式：由(1)已知 $f'(x_{1}) = f(x_{1})$、 $f'(x_{2}) = f(x_{2})$，也就是 $y' - y$ 在 $x_{1}, x_{2}$ 两处都为 0.
>
> **第三步：构造辅助函数并用罗尔定理.取**
>
> $$H(x)=e^{x}\left[f^{\prime}(x)-f(x)\right]=-2C_{2},\qquad H^{\prime}(x)=e^{x}\left[f^{\prime\prime}(x)-f(x)\right].$$
>
> 由 (1) 知 $H(x_1) = H(x_2) = 0$。对 $H(x)$ 在 $[x_1, x_2]$ 上用罗尔定理，存在 $\xi \in (x_1, x_2) \subset (a, b)$（自然 $\xi \neq x_1, x_2$），使 $H'(\xi) = 0$，故 $f''(\xi) = f(\xi)$。骨架是“解微分方程 + 求导解常数”：先由一阶方程 $y' - y = 0$ 的通解 $y = Ce^x$（即 $ye^{-x} = C$）找到两个点；再由二阶方程 $y'' - y = 0$ 的通解 $y = C_1e^x + C_2e^{-x}$ 求导，把常数写成 $C_1 = \frac{y' + y}{2e^x}$、 $C_2 = -\frac{e^x}{2}(y' - y)$，取只含 $C_2$ 的那一式作辅助函数。识别信号：结论里出现“函数与它的导数相等”时，就去解对应的线性方程、再把常数解出来。

**6.** (难度:★★) 设函数 $f(x)$ 在区间 $[0,1]$ 上连续，在 $(0,1)$ 内可微， $f(0)=f(1)=0$，且 $f\left(\frac{1}{2}\right)=1$. 证明:

(1) 存在 $\xi \in \left( \frac{1}{2}, 1 \right)$，使得 $f(\xi) = \xi$;

(2) 存在 $\eta \in (0, \xi)$，使得 $f'(\eta) = f(\eta) - \eta + 1$.

> [!answer]- 原书参考答案（C.0.1 第 6 题，未逐题独立验算）
> **6.** (1) 要证 $f(\xi) = \xi$，直接令 $F(x) = f(x) - x$，看两端符号；(2) 要证 $f'(\eta) = f(\eta) - \eta + 1$，把它整理成 $f'(\eta) - 1 = f(\eta) - \eta$，也就是 $F'(\eta) = F(\eta)$——这正是 $(e^{-x}F(x))' = 0$ 的形状。而 (1) 得到的 $\xi$ 恰好提供一个零点，与 $F(0) = 0$ 一起构成罗尔定理需要的两个等值点。 (1) $F(x) = f(x) - x$ 在 $[0,1]$ 上连续，且
>
> $$F\left(\frac{1}{2}\right)=1-\frac{1}{2}=\frac{1}{2}>0,\quad\quad F(1)=0-1=-1<0,$$
>
> 由零点存在定理，存在 $\xi \in \left( \frac{1}{2}, 1 \right)$，使 $F(\xi) = 0$，即 $f(\xi) = \xi$。
>
> (2) 由 (1) 已知 $F(\xi)=0$，而结论 $f'(\eta)=f(\eta)-\eta+1$ 可改写成
>
> $$f^{\prime}(\eta)-1-\left[f(\eta)-\eta\right]=0,\qquad 即 \qquad F^{\prime}(\eta)-F(\eta)=0.$$
>
> 先把微分方程解出来, 再构造: 令 $y = F(x)$, 则 $F'(x) - F(x) = 0$ 是一阶线性方程 (可分离变量),
>
> $$\frac{\mathrm{d}y}{y}=\mathrm{d}x\implies\ln|y|=x+C\implies y=C e^{x},$$
>
> 即 $F(x)e^{-x}=C$ 。把常数分离出来，就得到辅助函数
>
> $$G(x)=e^{-x}F(x)=e^{-x}\left[f(x)-x\right],\qquad G^{\prime}(x)=e^{-x}\left[F^{\prime}(x)-F(x)\right],$$
>
> 则 $G(0) = e^0 [f(0) - 0] = 0$; 又由 (1) 知 $G(\xi) = e^{-\xi} F(\xi) = 0$. 对 $G(x)$ 在 $[0, \xi]$ 上用罗尔定理, 存在 $\eta \in (0, \xi)$, 使
>
> $$G^{\prime}(\eta)=e^{-\eta}\left[f^{\prime}(\eta)-1-f(\eta)+\eta\right]=0,$$
>
> 即 $f'(\eta) = f(\eta) - \eta + 1$. 第(1)问求出的零点在第(2)问里当“第二个等值点”用，这是“多问递进”题目的常见结构：先把结论化成“某函数的导数为0”，再去凑两个等值点. 这里 $f'(x) - f(x)$ 型的构造配的就是 $e^{-x}$.

**7.** (难度:★★★) 设 $f(x)$ 是 $[-1,1]$ 上的二阶可导的奇函数, 证明: 存在 $\xi \in (-1,1)$, 使得 $f''(\xi) - f'(\xi) + f(1) = 0$.

> [!answer]- 原书参考答案（C.0.1 第 7 题，未逐题独立验算）
> **7.** 结论右边的 $f(1)$ 提示我们让两个单位区间上的中值点“取到同一个导数值”：在 $[0,1]$ 与 $[-1,0]$ 上分别用拉格朗日中值定理，再由 $f(x)$ 是奇函数 $(f(0)=0,f(-1)=-f(1))$ 把两个导数值都变成 $f(1)$. 有了两个导数值相等的位置，构造 $e^{-x}[f'(x)-f(1)]$ 就能用罗尔定理收尾. 由 $f(x)$ 是 $[-1,1]$ 上的奇函数，得 $f(0)=0,f(-1)=-f(1)$.
>
> 第一步: 在两个单位区间上各取一个中值点. 在 [0,1] 上用拉格朗日中值定理, 存在 $c \in (0,1)$, 使
>
> $$f^{\prime}(c)=\frac{f(1)-f(0)}{1-0}=f(1);$$
>
> 在 $[-1,0]$ 上再用一次，存在 $d \in (-1,0)$，使
>
> $$f^{\prime}(d)=\frac{f(0)-f(-1)}{0-(-1)}=0-\left[-f(1)\right]=f(1).$$
>
> 于是 $f'(c) = f'(d) = f(1)$，其中 d < 0 < c.
>
> **第二步：解出微分方程，构造辅助函数.要证的是**
>
> $$f^{\prime\prime}(\xi)-f^{\prime}(\xi)+f(1)=0.$$
>
> 令 $u(x)=f'(x)-f(1)$，则 $u'(x)=f''(x)$，上式等价于
>
> $$u^{\prime}-u=0.$$
>
> 解这个一阶线性方程：
>
> $$\frac{\mathrm{d}u}{u}=\mathrm{d}x\implies\ln|u|=x+C\implies u=C e^{x},$$
>
> 即 $u(x)e^{-x}=C$ 。于是取
>
> $$U(x)=e^{-x}u(x)=e^{-x}\left[f^{\prime}(x)-f(1)\right],\qquad U^{\prime}(x)=e^{-x}\left[f^{\prime\prime}(x)-f^{\prime}(x)+f(1)\right].$$
>
> 由第一步，
>
> $$U(c)=e^{-c}\left[f^{\prime}(c)-f(1)\right]=0,\qquad U(d)=e^{-d}\left[f^{\prime}(d)-f(1)\right]=0.$$
>
> 对 $U(x)$ 在 $[d,c] \subset (-1,1)$ 上用罗尔定理，存在 $\xi \in (d,c)$，使 $U'(\xi) = 0$，故
>
> $$f^{\prime\prime}(\xi)-f^{\prime}(\xi)+f(1)=0.$$
>
> “由整数点的值反推中值点”是这类题目的主要思路：先用拉格朗日把区间的两个端点换成中值点的导数值，再用奇偶性（或周期性、对称性）把两个导数值凑成同一个数，最后罗尔定理一次收尾。辅助函数里的 $e^{-x}$来自 $f''-f'+C=0$的积分因子。

**8.** (难度：★★★★★) 设 $f(x)$ 在 $[a,b]$ 上连续，在 $(a,b)$ 内可微，且 $f(x)$ 为非线性函数. 证明: 存在 $\xi \in (a,b)$，使得 $\left|f'(\xi)\right| > \left|\frac{f(b) - f(a)}{b - a}\right|$.

> [!answer]- 原书参考答案（C.0.1 第 8 题，未逐题独立验算）
> **8.** 结论等价于“存在 $\xi$，使 $f'(\xi)$ 超过（或低于）差商 $k = \frac{f(b) - f(a)}{b - a}$”。取 $F(x) = f(x) - f(a) - k(x - a)$，它把“差商”从 $f(x)$ 里减掉，且 $F(a) = F(b) = 0$、 $F(x)$ 不恒为 0。 $|F(x)|$ 的最大值点处 $F'(x) = 0$，而在最大值点的左右两侧，割线斜率必然一正一负——正的那个超过 k，负的那个低于 k，取绝对值就得到了结论。记 $k = \frac{f(b) - f(a)}{b - a}$，并令 $F(x) = f(x) - f(a) - k(x - a)$。(构造的依据：把差商 k 从 $f(x)$ 里减掉，就把“与差商比较”化成了“与 0 比较”，同时换来 $F(a) = F(b) = 0$ 这一对端点条件。)则 $F(a) = F(b) = 0$，而 $f(x)$ 不是线性函数说明 $F(x)$ 不恒为 0。
>
> 第一步: 取 $|F|$ 的最大值点. 因为 $F(x)$ 在 $[a, b]$ 上连续, 存在 $c \in [a, b]$, 使 $|F(c)| = \max_{a \leq x \leq b} |F(x)|$. 由于 $F(a) = F(b) = 0$ 而 $F(x)$ 不恒为 0, 有 $|F(c)| > 0$, 故 $c \in (a, b)$ 是内部点. 由费马定理, $F'(c) = 0$.
>
> 不妨设 $F(c) > 0$ ( $F(c) < 0$ 时把下面的论证整体取相反数即可)，于是对一切 $x \in [a, b]$ 有 $F(x) \leq F(c)$.
>
> 第二步: 在最大值点的两侧用中值定理. 由拉格朗日中值定理, 存在 $\xi_1 \in (a, c)$ 与 $\xi_2 \in (c, b)$, 使
>
> $$F^{\prime}(\xi_{1})=\frac{F(c)-F(a)}{c-a}>0,\qquad F^{\prime}(\xi_{2})=\frac{F(b)-F(c)}{b-c}<0.$$
>
> 代入 $F'(x) = f'(x) - k$，即得 $f'(\xi_1) > k$、 $f'(\xi_2) < k$。
>
> 第三步：分两种情况取 $\xi$。若 $k \geqslant 0$，取 $\xi = \xi_1$，则 $f'(\xi_1) > k = |k|$；若 k < 0，取 $\xi = \xi_2$，则 $f'(\xi_2) < k < 0$，故 $|f'(\xi_2)| = -f'(\xi_2) > -k = |k|$。两种情况都得到
>
> $$\left|f^{\prime}(\xi)\right|>\left|\frac{f(b)-f(a)}{b-a}\right|.$$
>
> “不是线性函数”这个条件正是用来保证 $|F|$的最大值在内部取到的。两个技术点：
>
> 一是构造函数时把差商减掉（使 $F(a)=F(b)=0$）；二是用“最大值点两侧割线斜率一正一负”来制造一端超过、一端低于差商。

**9.** (难度：★★★★★) 设函数 $f(x)$ 在 $(-1,1)$ 上二阶可导, $f(0)=1$, 且当 $x\geqslant0$ 时,

$$f(x)\geqslant0,\quad f^{\prime}(x)\leqslant0,\quad f^{\prime\prime}(x)\leqslant f(x).$$

证明： $f'(0) \geqslant -\sqrt{2}$.

> [!answer]- 原书参考答案（C.0.1 第 9 题，未逐题独立验算）
> **9.** 先把方程 $y'' - y = 0$ 解出来: 它的通解是
>
> $$y=C_{1}e^{x}+C_{2}e^{-x},\qquad 求导得 \qquad y^{\prime}=C_{1}e^{x}-C_{2}e^{-x}.$$
>
> 把两式相乘（这样含 x 的因子就消掉了）：
>
> $$(y+y^{\prime})(y-y^{\prime})=4C_{1}C_{2}\implies y^{2}-{y^{\prime}}^{2}=4C_{1}C_{2} 是常数 ,$$
>
> 即 ${y'}^2-y^2$ 只由两个常数决定——它是方程 $y'' = y$ 的“守恒量”. 所以本题取
>
> $$g(x)=\left[f^{\prime}(x)\right]^{2}-\left[f(x)\right]^{2},$$
>
> 而条件 $f''(x) \leqslant f(x)$ 与 $f'(x) \leqslant 0$ 放在一起，正好让
>
> $$g^{\prime}(x)=2f^{\prime}(x)\left[f^{\prime\prime}(x)-f(x)\right]\leqslant0,$$
>
> 即这个“能量”单调不增. 于是可以比较 $g(x)$ 与 $g(0)$，把 $[f'(0)]^2$ 控制在 $1 + [f'(x)]^2 - [f(x)]^2$ 之内；再用拉格朗日中值定理把 $f'(c)$ 用 $\frac{f(x) - 1}{x}$ 控制住，最后令 $x \to 1^-$.
>
> > [!warning] AI 补充：原书不等号方向疑点
> > 本题原书给出 $f'(x)\leq0$ 且 $f''(x)-f(x)\leq0$，两者乘积应非负，但原书第 266～267 页将 $g'(x)=2f'(x)[f''(x)-f(x)]$ 写为 $\leq0$，并称 $g$ 单调不增。以下推导仍按原书保留，不能据此认为证明已成立。
>
> 第一步：构造 $g(x) = [f'(x)]^2 - [f(x)]^2$. 对 $x \geq 0$,
>
> $$g^{\prime}(x)=2f^{\prime}(x)\left[f^{\prime\prime}(x)-f(x)\right]\leq0,$$
>
> 其中用了 $f'(x) \leq 0$与 $f''(x) - f(x) \leq 0$. 故 $g(x) \leq g(0)$，而
>
> $$g(0)=\left[f^{\prime}(0)\right]^{2}-\left[f(0)\right]^{2}=\left[f^{\prime}(0)\right]^{2}-1,$$
>
> 于是
>
> $$\left[f^{\prime}(0)\right]^{2}\leqslant1+\left[f^{\prime}(x)\right]^{2}-\left[f(x)\right]^{2}$$
>
> 第二步: 用中值定理控制 $f'(x)$. 因为 $f'(x) \leqslant 0, f(x)$ 在 $[0,1)$ 上单调不增, 故
>
> $$0\leqslant f(x)\leqslant f(0)=1\qquad(0<x<1).$$
>
> 由拉格朗日中值定理，存在 $c \in (0, x)$，使
>
> $$f^{\prime}(c)=\frac{f(x)-f(0)}{x}=\frac{f(x)-1}{x},$$
>
> 从而 $\left|f'(c)\right| \leqslant \frac{1}{x}$，即 $\left[f'(c)\right]^2 \leqslant \frac{1}{x^2}$.
>
> 第三步：在 $(\ast)$中代入并取极限。把c代入 $(\ast)$，并注意 $f(c)\geqslant0$：
>
> $$\left[f^{\prime}(0)\right]^{2}\leqslant1+\left[f^{\prime}(c)\right]^{2}-\left[f(c)\right]^{2}\leqslant1+\frac{1}{x^{2}}.$$
>
> 令 $x \to 1^{-}$，得 $[f'(0)]^{2} \leq 2$，即
>
> $$-\sqrt{2}\leq f^{\prime}(0)\leq\sqrt{2},\qquad 特别地 \qquad f^{\prime}(0)\geq-\sqrt{2}.$$
>
> 本题的两个"零件": 一是构造 $f'(x)^2 - f(x)^2$ (它求导后正好出现已知的 $f'(x) \leq 0$ 与 $f''(x) \leq f(x)$); 二是用中值定理把"某个中值点的导数"与 $\frac{f(x) - 1}{x}$ 联系起来, 再把 $x \to 1^-$ 把系数压到 1.

**10.** (难度：★★★★★) 设函数 $f(x)$ 在 $[-2,2]$ 上二阶可导, $\left|f(x)\right| \leqslant 1$, 且 $[f(0)]^2 + [f'(0)]^2 = 4$. 试证: 在 $(-2,2)$ 内至少存在一点 $\xi$, 使得 $f(\xi) + f''(\xi) = 0$.

> [!answer]- 原书参考答案（C.0.1 第 10 题，未逐题独立验算）
> **10.** 第一步:为什么要构造 $f^{2}(x) + f'(2)(x)$. 把 $\xi$ 换成 x, 要证的等式是 $f(x) + f''(x) = 0$.
>
> 它是二阶线性方程 $y'' + y = 0$ 的形状, 通解为
>
> $$f(x)=C_{1}\cos x+C_{2}\sin x,\qquad f^{\prime}(x)=-C_{1}\sin x+C_{2}\cos x.$$
>
> 解出两个常数并作“平方和”（这正是2.2.4子目讲的特殊处理）：
>
> $$C_{1}=f(x)\cos x-f^{\prime}(x)\sin x,\qquad C_{2}=f(x)\sin x+f^{\prime}(x)\cos x,$$
>
> $$C_{1}^{2}+C_{2}^{2}=f^{2}(x)+f^{\prime2}(x).$$
>
> 也就是说， $f(x)+f''(x)=0$ 的“症结”在 $f^{2}(x)+{f^{\prime}}^{2}(x)$ 上——于是令
>
> $$g(x)=\left[f(x)\right]^{2}+\left[f^{\prime}(x)\right]^{2}.$$
>
> 第二步: 算 $g(x)$ 的导数, 把条件对上去.
>
> $$g^{\prime}(x)=2f(x)f^{\prime}(x)+2f^{\prime}(x)f^{\prime\prime}(x)=2f^{\prime}(x)\left[f(x)+f^{\prime\prime}(x)\right],$$
>
> 而 $g(0) = [f(0)]^2 + [f'(0)]^2 = 4$。于是“存在 $\xi$ 使 $f(\xi) + f''(\xi) = 0$”就等价于“存在 $\xi$ 使 $g'(\xi) = 0$（且 $f'(\xi) \neq 0$）”。
>
> 第三步：用 $|f(x)| \leqslant 1$ 造出两个“低点”。对 x = 2：由拉格朗日中值定理，存在 $\xi_1 \in (0,2)$，使
>
> $$f^{\prime}(\xi_{1})=\frac{f(2)-f(0)}{2-0},$$
>
> 结合 $\left|f(x)\right|\leq1$ 得
>
> $$\left|f^{\prime}(\xi_{1})\right|\leqslant\frac{\left|f(2)\right|+\left|f(0)\right|}{2}\leqslant1.$$
>
> 于是
>
> $$g(\xi_{1})=\left[f(\xi_{1})\right]^{2}+\left[f^{\prime}(\xi_{1})\right]^{2}\leqslant1+1=2.$$
>
> 同理，对 x = -2 用一次中值定理，可得存在 $\xi_2 \in (-2, 0)$，使 $g(\xi_2) \leq 2$。
>
> 第四步：在 $[\xi_{2},\xi_{1}]$ 上取最大值。因为 $\xi_{2}<0<\xi_{1}$，且
>
> $$g(0)=4>2\geqslant g(\xi_{1}),\qquad g(0)=4>2\geqslant g(\xi_{2}),$$
>
> 所以 $g(x)$ 在闭区间 $[\xi_2, \xi_1]$ 上的最大值不可能在端点 $\xi_1, \xi_2$ 处取到，只能在内部某点 $\xi_3 \in (\xi_2, \xi_1)$ 处取到。由费马定理，
>
> $$g^{\prime}(\xi_{3})=0,\qquad 即 \qquad2f^{\prime}(\xi_{3})\left[f(\xi_{3})+f^{\prime\prime}(\xi_{3})\right]=0.$$
>
> 第五步：说明 $f'(\xi_{3}) \neq 0$ 。若 $f'(\xi_{3}) = 0$ ，则
>
> $$g(\xi_{3})=\left[f(\xi_{3})\right]^{2}\leqslant1<4=g(0),$$
>
> 这与"g( $\xi_{3}$)是[ $\xi_{2}$, $\xi_{1}$]上的最大值"矛盾.故 $f'(\xi_{3})\neq0$,从而
>
> $$f(\xi_{3})+f^{\prime\prime}(\xi_{3})=0.$$
>
> 取 $\xi = \xi_3 \in (\xi_2, \xi_1) \subset (-2, 2)$ 即得结论.
>
> 构造思路小结. 本题是“特殊处理”的标准范例: 单看 $f(x)$ 或 $f'(x)$ 都凑不出条件, 但把两个常数作平方和得到 $f^{2}(x) + f'(2)(x)$ 之后, 条件 $f^{2}(0) + f'(2)(0) = 4$ 与 $|f(x)| \leq 1$ 立刻就“对上了”——前者给出高点, 后者给出低点, 中间必有极值点.

**11.** (难度: ★★★) 设函数 $f(x)$ 在区间 [0,1] 上连续，在 (0,1) 内可导，且 $f(0) = 0$, $f(1) = 1$. 证明:

(1) 存在 $x_0 \in (0,1)$，使得 $f(x_0) = 2 - 3x_0$;

(2) 存在 $\xi, \eta \in (0,1)$, $\xi \neq \eta$, 使得 $[1 + f'(\xi)][1 + f'(\eta)] = 4$.

> [!answer]- 原书参考答案（C.0.1 第 11 题，未逐题独立验算）
> **11.** (1) 要证 $f(x_{0}) = 2 - 3x_{0}$，把它整理成 $f(x_{0}) + 3x_{0} - 2 = 0$，令 $F(x) = f(x) + 3x - 2$，看两端符号即可. (2) 结论里 $[1 + f'(\xi)] [1 + f'(\eta)] = 4$ 提示我们把 $1 + f'$ 与两段差商联系起来: (1) 给出的 $x_{0}$ 正好把 $[0,1]$ 分成两段，分别用拉格朗日中值定理，两个差商的乘积恰好是 4. (1) 令 $F(x) = f(x) + 3x - 2$. 由 $f(0) = 0$, $f(1) = 1$ 得
>
> $$F(0)=-2<0,\qquad F(1)=1+3-2=2>0.$$
>
> 由零点存在定理，存在 $x_{0}\in(0,1)$，使 $F(x_{0})=0$，即 $f(x_{0})=2-3x_{0}$.
>
> (2) 在 $[0, x_0]$ 上用拉格朗日中值定理，存在 $\xi \in (0, x_0)$，使
>
> $$f^{\prime}(\xi)=\frac{f(x_{0})-f(0)}{x_{0}}=\frac{2-3x_{0}}{x_{0}};$$
>
> 在 $[x_0,1]$ 上再用一次，存在 $\eta\in(x_0,1)$，使
>
> $$f^{\prime}(\eta)=\frac{f(1)-f(x_{0})}{1-x_{0}}=\frac{1-(2-3x_{0})}{1-x_{0}}=\frac{3x_{0}-1}{1-x_{0}}.$$
>
> 于是 (注意 $x_{0} \in (0,1)$，分母均不为零)
>
> $$\left[1+f^{\prime}(\xi)\right]\left[1+f^{\prime}(\eta)\right]=\frac{2-2x_{0}}{x_{0}}\cdot\frac{2x_{0}}{1-x_{0}}=4.$$
>
> 第(1)问是“把结论写成 $F(x)=0$再用零点定理”的标准用法;第(2)问的关键是看出结论中的4来自两段差商之积,所以要用第(1)问给出的分点把区间拆开.两问之间的这种“呼应”在构造类题目里很常见.

**12.** (难度:★★) 设函数 $f(x)$ 在 $[a,b]$ 上连续，在 $(a,b)$ 内可导，且 $f'(x) \neq 0$。试证：存在 $\xi, \eta \in (a,b)$，使得

$$\frac{f^{\prime}(\xi)}{f^{\prime}(\eta)}=\frac{e^{b}-e^{a}}{b-a}\cdot e^{-\eta}.$$

> [!answer]- 原书参考答案（C.0.1 第 12 题，未逐题独立验算）
> **12.** 结论右边出现 $\frac{e^{b}-e^{a}}{b-a}e^{-\eta}$，其中 $\frac{f(b)-f(a)}{b-a}$ 与 $\frac{f(b)-f(a)}{e^{b}-e^{a}}$ 是两个差商：前者由拉格朗日中值定理给出，后者由柯西中值定理（取 $g(x)=e^{x}$）给出，两者相除正好把 $f(b)-f(a)$ 消掉。第一步：拉格朗日中值定理。存在 $\xi\in(a,b)$，使
>
> $$f^{\prime}(\xi)=\frac{f(b)-f(a)}{b-a},\qquad 即 \qquad f(b)-f(a)=f^{\prime}(\xi)(b-a).$$
>
> 第二步:柯西中值定理.取 $g(x)=e^x$,它在 $[a,b]$上连续、在 $(a,b)$内可导且 $g'(x)=e^x\neq0$.对 $f(x)$与 $g(x)$用柯西中值定理,存在 $\eta\in(a,b)$,使
>
> $$\frac{f(b)-f(a)}{e^{b}-e^{a}}=\frac{f^{\prime}(\eta)}{e^{\eta}},\qquad 即 \qquad f(b)-f(a)=\frac{f^{\prime}(\eta)}{e^{\eta}}\left(e^{b}-e^{a}\right).$$
>
> 第三步: 两式相除. 把两个关于 $f(b) - f(a)$ 的表达式相除 $(f'(x) \neq 0$ 保证分母不为零):
>
> $$\frac{f^{\prime}(\xi)}{f^{\prime}(\eta)}=\frac{e^{b}-e^{a}}{b-a}e^{-\eta}.$$
>
> ”一个中值点配拉格朗日、另一个中值点配柯西”是双中值题目的两种基本套路之一.本题的识别信号是:结论右边同时出现 $\frac{f(b)-f(a)}{b-a}$型与 $\frac{f(b)-f(a)}{e^{b}-e^{a}}$型的量,而它们正好是两种差商.

**13.** (难度:★★★★) 设 $f(x)$ 在区间 $[0,1]$ 上连续，在 $(0,1)$ 内可导， $f'(x) > 0$，且 $f(0) = 0$， $f(1) = 1$。试证明：对任意给定的正数 $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{n}$，在 $(0,1)$ 内存在不同的数 $x_{1}, x_{2}, \cdots, x_{n}$，使得

$$\sum_{i=1}^{n}\frac{\lambda_{i}}{f^{\prime}(x_{i})}=\sum_{i=1}^{n}\lambda_{i}.$$

> [!answer]- 原书参考答案（C.0.1 第 13 题，未逐题独立验算）
> **13.** 记 $\Lambda = \lambda_1 + \cdots + \lambda_n$. 由 f 严格递增、 $f(0) = 0$、 $f(1) = 1$ 知 $f^{-1}$ 存在，令
>
> $$x_{i}=f^{-1}\left(\frac{\lambda_{1}+\cdots+\lambda_{i}}{\Lambda}\right)\qquad(i=1,\ldots,n-1),$$
>
> 则 $0 =: x_0 < x_1 < \cdots < x_n := 1$ 且 $f(x_i) - f(x_{i-1}) = \frac{\lambda_i}{\Lambda}$. 在 $[x_{i-1}, x_i]$ 上用拉格朗日中值定理，取 $x_i^* \in (x_{i-1}, x_i)$ 使
>
> $$f^{\prime}(x_{i}^{*})=\frac{f(x_{i})-f(x_{i-1})}{x_{i}-x_{i-1}}=\frac{\lambda_{i}}{\Lambda\left(x_{i}-x_{i-1}\right)},\qquad\mathrm{ 故 }\quad\frac{\lambda_{i}}{f^{\prime}(x_{i}^{*})}=\Lambda\left(x_{i}-x_{i-1}\right).$$
>
> 各 $x_{i}^{*}$ 落在互不相交的区间 $(x_{i-1}, x_{i})$ 内，故两两不同；求和得
>
> $$\sum_{i=1}^{n}\frac{\lambda_{i}}{f^{\prime}(x_{i}^{*})}=\Lambda\sum_{i=1}^{n}(x_{i}-x_{i-1})=\Lambda=\sum_{i=1}^{n}\lambda_{i}.$$

## 2.2 泰勒展开及函数证明

通过在某点处展开或任意点展开，进行微分等式或不等式的证明.

**1.** (难度:★★★) 设函数 $f(x)$ 有二阶导数, $f'(0) = f'(1)$, $\left|f''(x)\right| \leq 1$, 证明:

(1) 当 $x \in (0,1)$ 时， $|f(x) - f(0)(1 - x) - f(1)x| \leq \frac{x(1 - x)}{2}$;

(2) $\left|\int_{0}^{1}f(x)dx-\frac{f(0)+f(1)}{2}\right|\leqslant\frac{1}{12}.$

> [!answer]- 原书参考答案（C.0.2 第 1 题，未逐题独立验算）
> **1.** 两问都靠”在固定点（端点0与1）各展开一次”.
>
> 第一步: 在两个端点分别写出泰勒展开. 对任意 $x \in (0,1)$, 由带拉格朗日余项的泰勒公式,
>
> $$f(x)=f(0)+f^{\prime}(0)x+\frac{f^{\prime\prime}(\xi_{1})}{2}x^{2}\qquad(0<\xi_{1}<x),$$
>
> $$f(x)=f(1)+f^{\prime}(1)(x-1)+\frac{f^{\prime\prime}(\xi_{2})}{2}(x-1)^{2}\qquad(x<\xi_{2}<1).$$
>
> （同一个点 x 分别“从左边 0”和“从右边 1”展开，两次得到的余项点是不同的。）
>
> 第二步: 用 $f'(0) = f'(1)$ 把一次项消掉. 把第一式乘 $(1 - x)$、第二式乘 x, 两式相加: 左端是
>
> $$f(x)(1-x)+f(x)x=f(x);$$
>
> 右端的一次项是
>
> $$f^{\prime}(0)x(1-x)+f^{\prime}(1)x(x-1)=x(1-x)\left[f^{\prime}(0)-f^{\prime}(1)\right]=0,$$
>
> 于是
>
> $$f(x)=f(0)(1-x)+f(1)x+\frac{x(1-x)}{2}\left[xf^{\prime \prime}(\xi_{1})+(1-x)f^{\prime \prime}(\xi_{2})\right].$$
>
> 第三步: 估计余项, 得到 (1). 由 $\left|f''(x)\right| \leqslant 1$,
>
> $$\begin{aligned}\left|f(x)-f(0)(1-x)-f(1)x\right|&\leq\frac{x(1-x)}{2}\left[x\left|f^{\prime\prime}(\xi_{1})\right|+(1-x)\left|f^{\prime\prime}(\xi_{2})\right|\right]\\&\leq\frac{x(1-x)}{2}\left[x+(1-x)\right]=\frac{x(1-x)}{2}.\end{aligned}$$
>
> 第四步: 把 (1) 在 [0,1] 上积分, 得到 (2). 由 (1) 知对一切 $x \in (0,1)$,
>
> $$-\frac{x(1-x)}{2}\leqslant f(x)-f(0)(1-x)-f(1)x\leqslant\frac{x(1-x)}{2},$$
>
> 在 $[0,1]$ 上积分（注意 $\int_{0}^{1}x(1-x)dx=\frac{1}{2}-\frac{1}{3}=\frac{1}{6}$）：
>
> $$-\frac{1}{12}\leqslant\int_{0}^{1}f(x)\mathrm{d}x-\left[f(0)\int_{0}^{1}(1-x)\mathrm{d}x+f(1)\int_{0}^{1}x\mathrm{d}x\right]\leqslant\frac{1}{12},$$
>
> 而两个积分的值都是 $\frac{1}{2}$，所以
>
> $$\left|\int_{0}^{1}f(x)dx-\frac{f(0)+f(1)}{2}\right|\leq\frac{1}{12}.$$
>
> 本题的套路值得记住: 当结论里同时出现 $f(0)$, $f(1)$ 与 $x(1-x)$ 这样的“两端点对称”的结构时, 就在两个端点各展开一次, 再用题目给的 $f'(0) = f'(1)$ 把一次项消掉.

**2.** (难度:★★★★) 设 $f(x) \in C^{4}(-\infty,+\infty)$，且满足

$$f(x+h)=f(x)+f^{\prime}(x)h+\frac{1}{2}f^{\prime\prime}(x+\theta h)h^{2},$$

其中 $\theta$ 是与 x, h 无关的常数，证明： $f(x)$ 是不超过三次的多项式.

> [!answer]- 原书参考答案（C.0.2 第 2 题，未逐题独立验算）
> **2.** "f(x) 是不超过三次的多项式" 等价于 $f^{(4)} \equiv 0$，所以要在二阶以上做文章。题设的等式里 $f(x+h)$ 是 $x+h$ 处的值、 $f''(x+\theta h)$ 又是“中间点”处的值，于是两处都作泰勒展开：把 $f(x+h)$ 在 x 处展到四阶，把 $f''(x+\theta h)$ 在 x 处展到二阶，一起代入题设等式，再与完整的四阶展开式相减—— $h^3$ 与 $h^4$ 的系数就给出了含 $f'''(x)$、 $f^{(4)}(\eta)$、 $f^{(4)}(\xi)$ 的关系式。令 $h \to 0^+$ 定出 $\theta$，再分情形讨论即可。第一步：两处泰勒展开。取 $h > 0$。由带拉格朗日余项的泰勒公式，
>
> $$\begin{aligned}f(x+h)&=f(x)+f^{\prime}(x)h+\frac{f^{\prime \prime}(x)}{2}h^{2}+\frac{f^{\prime \prime \prime}(x)}{6}h^{3}\\&\quad+\frac{f^{(4)}(\xi)}{24}h^{4},\qquad x<\xi<x+h;\end{aligned}$$
>
> $$f^{\prime\prime}(x+\theta h)=f^{\prime\prime}(x)+f^{\prime\prime\prime}(x)\theta h+\frac{f^{(4)}(\eta)}{2}(\theta h)^{2},$$
>
> 其中 $\eta$介于x与 $x+\theta h$之间.
>
> 第二步：代入题设，与(1)相减.题设给的是
>
> $$f(x+h)=f(x)+f^{\prime}(x)h+\frac{1}{2}f^{\prime\prime}(x+\theta h)h^{2}.$$
>
> 把(2)代入(3)，得
>
> $$f(x+h)=f(x)+f^{\prime}(x)h+\frac{f^{\prime\prime}(x)}{2}h^{2}+\frac{\theta}{2}f^{\prime\prime\prime}(x)h^{3}+\frac{\theta^{2}}{4}f^{(4)}(\eta)h^{4}.$$
>
> 把(1)与(4)相减：
>
> $$\left(\frac{1}{6}-\frac{\theta}{2}\right)f^{\prime\prime\prime}(x)h^{3}+\left(\frac{1}{24}f^{(4)}(\xi)-\frac{\theta^{2}}{4}f^{(4)}(\eta)\right)h^{4}=0,$$
>
> 两边乘24再除以 $h^{3}(h>0)$:
>
> $$4(1-3\theta)f^{\prime\prime\prime}(x)=\left(6\theta^{2}f^{(4)}(\eta)-f^{(4)}(\xi)\right)h.$$
>
> 第三步：令 $h \to 0^{+}$，先定出 $\theta$。(5) 的左端与 h 无关；当 $h \to 0^{+}$ 时 $\eta \to x$、 $\xi \to x$，由 $f^{(4)}$ 连续知右端的括号趋于有限值，故
>
> $$\lim_{h\to0^{+}}4(1-3\theta)f^{\prime\prime\prime}(x)=\lim_{h\to0^{+}}\left(6\theta^{2}f^{(4)}(\eta)-f^{(4)}(\xi)\right)h=0,$$
>
> 即
>
> $$4(1-3\theta)f^{\prime\prime\prime}(x)=0\qquad(\forall x\in\mathbb{R}).$$
>
> 第四步：分两种情形.
>
> (i) 若 $f'''(x) \equiv 0$: 则 $f(x)$ 是不超过三次的多项式, 结论成立.
>
> (ii) 若 $f'''(x) \neq 0$: 由上式必有 $\theta = \frac{1}{3}$. 把它代回 (5):
>
> $$\left(\frac{2}{3}f^{(4)}(\eta)-f^{(4)}(\xi)\right)h=0\qquad(\forall h>0),\qquad 即 \qquad\frac{2}{3}f^{(4)}(\eta)=f^{(4)}(\xi).$$
>
> 再令 $h \to 0^{+}$，由 $f^{(4)}$ 连续得 $\eta \to x$、 $\xi \to x$，故
>
> $$\frac{2}{3}f^{(4)}(x)=f^{(4)}(x)\implies f^{(4)}(x)=0\qquad(\forall x\in\mathbb{R}).$$
>
> 两种情形都得到 $f^{(4)} \equiv 0$，所以 $f(x)$ 是不超过三次的多项式。本题的两个关键动作：
>
> (1) 把“中间点” $x + \theta h$ 也展开（先展开 $f''(x + \theta h)$ 到二阶），这样才能和 $f(x + h)$ 的四阶展开”对齐到 $h^{4}$ ；（2）比较同次幂的系数得到（5），再令 $h \to 0^{+}$ 把 $\theta$ 定出来 $\left(\theta = \frac{1}{3}\right)$，最后由 $\frac{2}{3}f^{(4)} = f^{(4)}$ 逼出 $f^{(4)} \equiv 0$.

**3.** (难度: ★★★) 设函数 $f(x)$ 在区间 $[-1,1]$ 上三阶可导, $f(-1) = 0$, $f(1) = 1$, $f'(0) = 0$. 证明: 存在 $\xi \in (-1,1)$, 使得 $\left|f'''(\xi)\right| \geqslant 3$.

> [!answer]- 原书参考答案（C.0.2 第 3 题，未逐题独立验算）
> **3.** 三个条件里给了 $f'(0) = 0$，最省事的做法是在 x = 0 处（固定点）展到三阶——这样一次项自动消失；再把两个端点 $x = \pm 1$ 分别代进去，得到两个含 $f'''(\zeta)$ 的等式。两式相减可以消掉 $f(0)$ 与 $f''(0)$，只剩 $f'''(\xi_1) + f'''(\xi_2) = 6$，于是两者中必有一个的绝对值不小于 3。第一步：在 0 处展开（注意 $f'(0) = 0$）。对每个 x，存在介于 0 与 x 之间的 $\zeta$，使
>
> $$f(x)=f(0)+f^{\prime}(0)x+\frac{f^{\prime\prime}(0)}{2}x^{2}+\frac{f^{\prime\prime\prime}(\zeta)}{6}x^{3}=f(0)+\frac{f^{\prime\prime}(0)}{2}x^{2}+\frac{f^{\prime\prime\prime}(\zeta)}{6}x^{3}.$$
>
> 第二步: 把 x = 1 与 x = -1 分别代进去. 存在 $\xi_1 \in (0,1)$ 与 $\xi_2 \in (-1,0)$, 使
>
> $$f(0)+\frac{1}{2}f^{\prime\prime}(0)+\frac{1}{6}f^{\prime\prime\prime}(\xi_{1})=f(1)=1,$$
>
> $$f(0)+\frac{1}{2}f^{\prime\prime}(0)-\frac{1}{6}f^{\prime\prime\prime}(\xi_{2})=f(-1)=0.$$
>
> 第三步：把(1)与(2)相减，消去 $f(0)$与 $f''(0)$.
>
> $$\frac{1}{6}\left[f^{\prime\prime\prime}(\xi_{1})+f^{\prime\prime\prime}(\xi_{2})\right]=1,\qquad 即 \qquad f^{\prime\prime\prime}(\xi_{1})+f^{\prime\prime\prime}(\xi_{2})=6.$$
>
> 第四步：取绝对值最大的那一个.记
>
> $$M=\max\left\{\left|f^{\prime\prime\prime}(\xi_{1})\right|,\ \left|f^{\prime\prime\prime}(\xi_{2})\right|\right\},$$
>
> 由三角不等式
>
> $$6=\left|f^{\prime\prime\prime}(\xi_{1})+f^{\prime\prime\prime}(\xi_{2})\right|\leq\left|f^{\prime\prime\prime}(\xi_{1})\right|+\left|f^{\prime\prime\prime}(\xi_{2})\right|\leq2M,$$
>
> 故 $M \geqslant 3$: $\xi_1, \xi_2$ 中至少有一个 (记作 $\xi \in (-1,1)$) 满足 $|f'''(\xi)| \geqslant 3$. 本题只需”在 0 处展开一次、代两个端点、两式相减”三步. 两个细节: 第一, 展开必须用带拉格朗日余项的形式; 第二, 两次代入得到的余项点是 $\xi_1 \in (0,1)$ 与 $\xi_2 \in (-1,0)$, 一般不是同一个点, 不能合并成一个 $\xi$, 最后只能用“两数之和为 6, 则至少有一个不小于 $3$”来收尾.

**4.** (难度:★★★) 设函数在区间 $[0,1]$ 上具有二阶导数，且有正常数 $A,B$ 使得 $|f(x)|\leq A,\ |f''(x)|\leq B$。证明：对任意 $x\in[0,1]$, 有

$$|f^{\prime}(x)|\leqslant2A+\frac{B}{2}.$$

> [!answer]- 原书参考答案（C.0.2 第 4 题，未逐题独立验算）
> **4.** 结论中出现的是 $f'(x)$——“任意点处的导数”. 若在 0 或 1 处展开, 式子里只会出现 $f'(0)$、 $f'(1)$, 与 $f'(x)$ 无关; 正确做法是把 x 当展开中心, 去展开两个固定点 0、1, 再把两式相减消去 $f(x)$. 对固定的 $x \in [0,1]$, 把 $f(0)$、 $f(1)$ 在 x 处展开: 存在 $\xi_1 \in (0,x)$、 $\xi_2 \in (x,1)$, 使
>
> $$f(0)=f(x)-xf^{\prime}(x)+\frac{x^{2}}{2}f^{\prime\prime}(\xi_{1}),$$
>
> $$f(1)=f(x)+(1-x)f^{\prime}(x)+\frac{(1-x)^{2}}{2}f^{\prime\prime}(\xi_{2}).$$
>
> 两式相减，消去 $f(x)$:
>
> $$f(1)-f(0)=f^{\prime}(x)+\frac{(1-x)^{2}}{2}f^{\prime\prime}(\xi_{2})-\frac{x^{2}}{2}f^{\prime\prime}(\xi_{1}),$$
>
> 即
>
> $$f^{\prime}(x)=f(1)-f(0)+\frac{x^{2}}{2}f^{\prime\prime}(\xi_{1})-\frac{(1-x)^{2}}{2}f^{\prime\prime}(\xi_{2}).$$
>
> 由 $\left|f(x)\right|\leqslant A$、 $\left|f''(x)\right|\leqslant B$，
>
> $$\left|f^{\prime}(x)\right|\leqslant\left|f(1)\right|+\left|f(0)\right|+\frac{x^{2}+(1-x)^{2}}{2}B\leqslant2A+\frac{B}{2}\left[x^{2}+(1-x)^{2}\right].$$
>
> 而 $x^{2}+(1-x)^{2}=2\left(x-\frac{1}{2}\right)^{2}+\frac{1}{2}\leqslant1\left(0\leqslant x\leqslant1\right)$，故 $\left|f'(x)\right|\leqslant2A+\frac{B}{2}$。识别信号：结论里出现 $f'(x)$、 $f''(x)$ 这类“任意点”的导数，就把这一点当展开中心，去展开题目给出的定点。估计时注意 $x^{2}+(1-x)^{2}$ 在 $[0,1]$ 上的取值范围是 $\left[\frac{1}{2},1\right]$，最大值在端点取到。

**5.** (难度：★★★) 设函数 $f(x)$ 在闭区间 $[-1,1]$ 上具有连续的三阶导数, $f(-1) = 0$, $f(1) = 1$, 且 $f'(0) = 0$. 求证: 至少存在一点 $x_0 \in (-1,1)$, 使得 $f'''(x_0) = 3$.

> [!answer]- 原书参考答案（C.0.2 第 5 题，未逐题独立验算）
> **5.** 三个条件里给了 $f'(0) = 0$，最省事的做法是在 x = 0 处（固定点）展到三阶——一次项自动消失；再把两个端点 x = 1 与 x = -1 分别代进去，得到两个含 $f'''(\zeta)$ 的等式。两式相减， $f(0)$ 与 $f''(0)$ 都被消掉，只剩 $f'''(\xi_1) + f'''(\xi_2) = 6$。两个数的和为 6，说明它们的平均值就是 3；而题目比上一题多给了“ $f'''$ 连续”这一条，于是可以用介值定理把这个平均值取到。第一步：在 0 处展开（注意 $f'(0) = 0$）。对每个 $x \in [-1,1]$，存在介于 0 与 x 之间的 $\zeta$，使
>
> $$f(x)=f(0)+f^{\prime}(0)x+\frac{f^{\prime\prime}(0)}{2}x^{2}+\frac{f^{\prime\prime\prime}(\zeta)}{6}x^{3}=f(0)+\frac{f^{\prime\prime}(0)}{2}x^{2}+\frac{f^{\prime\prime\prime}(\zeta)}{6}x^{3}.$$
>
> 第二步: 把 x = 1 与 x = -1 分别代进去. 存在 $\xi_{1} \in (0,1)$ 与 $\xi_{2} \in (-1,0)$, 使
>
> $$f(0)+\frac{1}{2}f^{\prime\prime}(0)+\frac{1}{6}f^{\prime\prime\prime}(\xi_{1})=f(1)=1,$$
>
> $$f(0)+\frac{1}{2}f^{\prime\prime}(0)-\frac{1}{6}f^{\prime\prime\prime}(\xi_{2})=f(-1)=0.$$
>
> 第三步：两式相减，消去 $f(0)$ 与 $f''(0)$.
>
> $$\frac{1}{6}\left[f^{\prime\prime\prime}(\xi_{1})+f^{\prime\prime\prime}(\xi_{2})\right]=1,\qquad 即 \qquad f^{\prime\prime\prime}(\xi_{1})+f^{\prime\prime\prime}(\xi_{2})=6.$$
>
> 第四步: 用介值定理取到平均值 3. 由 $f'''$ 在 $[-1,1]$ 上连续知它在 $[\xi_2, \xi_1]$ 上连续, 从而取到介于 $f'''(\xi_2)$ 与 $f'''(\xi_1)$ 之间的一切值, 特别地取到它们的平均值
>
> $$\frac{f^{\prime \prime \prime}(\xi_{1})+f^{\prime \prime \prime}(\xi_{2})}{2}=3.$$
>
> 即存在 $x_0 \in (\xi_2, \xi_1) \subset (-1, 1)$，使 $f'''(x_0) = 3$。本题与“存在 $\xi$ 使 $|f'''(\xi)| \geq 3''$ 的唯一差别在最后一步：那里由“两数之和为 $6''$ 只能推出“有一个的绝对值不小于 $3''$，这里多了 $f'''$ 连续这一条件，就可以用介值定理把 3 精确取到。
>
> 本题还有一个“辅助多项式”的写法：取 $P(x) = \frac{x^3}{2} - \left[f(0) - \frac{1}{2}\right]x^2$，则 $P''' \equiv 3$，且令 $F(x) = f(x) - P(x)$ 后有
>
> $$F(-1)=F(0)=F(1)=f(0),\qquad F^{\prime}(0)=f^{\prime}(0)=0.$$
>
> 由 $F(-1) = F(0) = F(1)$ 与罗尔定理, $F'$ 在 $(-1,0)$ 与 $(0,1)$ 内各有一个零点, 再加上 $F'(0) = 0$, 共有三个零点; 于是 $F''$ 有两个零点, 最后 $F'''$ 有一个零点 $\xi$, 即 $f'''(\xi) = 3$.

**6.** (难度:★★★★) 对于连续函数 $f(x) > 0$, 证明: $\ln \int_{0}^{1} f(x) \, dx \geqslant \int_{0}^{1} \ln f(x) \, dx$.

> [!answer]- 原书参考答案（C.0.2 第 6 题，未逐题独立验算）
> **6.** 要证的是“积分后再取对数”不小于“先取对数再积分”，这类“凸性不等式”最常用的武器是泰勒展开.取 $g(x)=\ln x$，它的二阶导数 $g''(x)=-\frac{1}{x^{2}}<0$，说明 $g(x)$ 的图像在每一点切线的下方：
>
> $$\ln x\leqslant\ln x_{0}+\frac{1}{x_{0}}(x-x_{0})\qquad(x>0).$$
>
> 把 x 换成 $f(t)$ 再对 t 积分，右边只剩下 $\ln x_{0}$ 与 $\frac{1}{x_{0}}\left[\int_{0}^{1}f(t)dt-x_{0}\right]$; 最后取 $x_{0}=\int_{0}^{1}f(t)dt$，右边恰好就是 $\ln\int_{0}^{1}f(x)dx$。第一步：把 $\ln x$ 在 $x=x_0$ 处泰勒展开。因为 $f(x)>0$ 且在 $[0,1]$ 上连续，所以 $x_{0}=\int_{0}^{1}f(t)dt>0$。取 $g(x)=\ln x$，则 $g'(x)=\frac{1}{x}$、 $g''(x)=-\frac{1}{x^{2}}$。对任意 x>0，由带拉格朗日余项的泰勒公式，存在 $\zeta$ 介于 $x_{0}$ 与 x 之间，使
>
> $$\ln x=\ln x_{0}+\frac{1}{x_{0}}(x-x_{0})-\frac{1}{2\zeta^{2}}(x-x_{0})^{2}\leqslant\ln x_{0}+\frac{1}{x_{0}}(x-x_{0}),$$
>
> 最后一步正是“ $g''<0$，故余项不超过 $0''$．
>
> 第二步: 把 $x = f(t)$ 代入并积分. 由 $f(t) > 0$, 取 $x = f(t) (t \in [0,1])$:
>
> $$\ln f(t)\leqslant\ln x_{0}+\frac{1}{x_{0}}\left[f(t)-x_{0}\right].$$
>
> 在 $[0,1]$ 上对 $t$ 积分（$x_0$ 与 $\ln x_0$ 都是常数）：
>
> $$\begin{aligned}\int_{0}^{1}\ln f(t)\mathrm{d}t&\leqslant\int_{0}^{1}\ln x_{0}\mathrm{d}t+\frac{1}{x_{0}}\int_{0}^{1}\left[f(t)-x_{0}\right]\mathrm{d}t\\&=\ln x_{0}+\frac{1}{x_{0}}\left[\int_{0}^{1}f(t)\mathrm{d}t-x_{0}\right].\end{aligned}$$
>
> 第三步：取 $x_{0}=\int_{0}^{1}f(t)dt$ 。此时上式右端为
>
> $$\ln x_{0}+\frac{1}{x_{0}}\left(x_{0}-x_{0}\right)=\ln x_{0}=\ln\int_{0}^{1}f(t)d t,$$
>
> 故
>
> $$\int_{0}^{1}\ln f(t)\mathrm{d}t\leqslant\ln\int_{0}^{1}f(t)\mathrm{d}t,$$
>
> 这就是要证的结论 $(f(x)$ 为常数函数时，两个余项都退化为 0，等号成立）。两个关键动作：一是“用凸性把 $\ln$ 换成一次函数”必须在切点处展开（切点 $x_0$ 最后才被定出来）；二是 $x_0$ 的取法——它必须是 $\int_0^1 f(x) \, dx$，这样右边第一项与第二项才会合并成 $\ln \int_0^1 f(x) \, dx$。同一种做法适用于任何凹函数 $g(x)$ ( $g''(x) \leq 0$)： $\ln \int_0^1 f(x) \, dx \geq \int_0^1 \ln f(x) \, dx$ 与 $e^{\int_0^1 g(x) \, dx} \leq \int_0^1 e^{g(x)} \, dx$ 是同一个套路的两个方向。

**7.** (难度:★★★★) 设函数 $f(x)$ 在 $[a,b]$ 上连续，在 $(a,b)$ 内二阶可导，且 $\left|f''(x)\right| \leqslant 1$.

证明: 在曲线 $y = f(x)$ ( $a \leqslant x \leqslant b$) 上必存在点 A, B, C，使得 $\triangle ABC$ 的面积 $S_{\triangle ABC} \geqslant \frac{(b - a)^3}{16}$.

> [!answer]- 原书参考答案（C.0.2 第 7 题，未逐题独立验算）
> **7.** 三点组成的三角形面积可以写成“三点坐标的行列式的一半”：
>
> $$S_{\triangle ABC}=\frac{1}{2}\left|D(x)\right|,\qquad D(x)=\begin{vmatrix}{{{a}}}&{{{f(a)}}}&{{{1}}} \\{{{b}}}&{{{f(b)}}}&{{{1}}} \\{{{x}}}&{{{f(x)}}}&{{{1}}}\end{vmatrix},$$
>
> 这样”三点面积”就化成了”一个函数 $D''$ 的问题,而且 $D(a)=D(b)=0$.对 D 用拉格朗日插值余项 (相当于在任意点 x 处展开、再代入两个端点消去 $D'(x)$):存在 $\xi \in (a,b)$ 使
>
> $$D(x)=\frac{D^{\prime\prime}(\xi)}{2}(x-a)(x-b),$$
>
> 而 $D''(x)=(b-a)f''(x)$，于是 $\left|D(x)\right|\geqslant\frac{b-a}{2}(x-a)(b-x)$。要让右端尽量大，把x 取在 $(x-a)(b-x)$ 的最大值点，也就是中点 $\frac{a+b}{2}$ 即可。第一步：把面积写成行列式. 设 $A(a,f(a))$、 $B(b,f(b))$、 $C(x,f(x))$，其中 $x \in (a,b)$，并记
>
> $$D(x)=\begin{vmatrix}{{{a}}}&{{{f(a)}}}&{{{1}}} \\{{{b}}}&{{{f(b)}}}&{{{1}}} \\{{{x}}}&{{{f(x)}}}&{{{1}}}\end{vmatrix}=(b-a)f(x)+\left[f(a)-f(b)\right]x+af(b)-bf(a).$$
>
> 则 $S_{\triangle ABC} = \frac{1}{2} |D(x)|$，且由直接计算得
>
> $$D(a)=0,\qquad D(b)=0,\qquad D^{\prime\prime}(x)=(b-a)f^{\prime\prime}(x).$$
>
> 第二步: 对 $D$ 用拉格朗日插值余项. 把 $D(x)$ 看成”以 $a,b$ 为节点的插值余项”(等价于在任意点 $x$ 处展开后消去 $D'(x)$, 见正文 2.2.5): 存在 $\xi \in (a,b)$, 使
>
> $$D(x)=\frac{D^{\prime\prime}(\xi)}{2}(x-a)(x-b).$$
>
> 于是
>
> $$\begin{aligned}\left|D(x)\right|&=\frac{\left|D^{\prime\prime}(\xi)\right|}{2}(x-a)(b-x)=\frac{b-a}{2}\left|f^{\prime\prime}(\xi)\right|(x-a)(b-x)\\&\geq\frac{b-a}{2}(x-a)(b-x),\end{aligned}$$
>
> 最后一步用了 $\left|f''\right|\geqslant1$.
>
> 第三步：取 $x = \frac{a + b}{2}$. 此时
>
> $$(x-a)(b-x)=\frac{b-a}{2}\cdot\frac{b-a}{2}=\frac{(b-a)^{2}}{4},$$
>
> 故
>
> $$\left|D\left(\frac{a+b}{2}\right)\right|\geqslant\frac{b-a}{2}\cdot\frac{(b-a)^{2}}{4}=\frac{(b-a)^{3}}{8}.$$
>
> 取 $C\left(\frac{a+b}{2}, f\left(\frac{a+b}{2}\right)\right)$，则
>
> $$S_{\triangle ABC}=\frac{1}{2}\left|D\left(\frac{a+b}{2}\right)\right|\geqslant\frac{(b-a)^{3}}{16}.$$
>
> 三个要点: (1) 用行列式把“面积”翻译成“一个函数 $D''$，三点共线就对应 D = 0; (2) $D(a) = D(b) = 0$ 使拉格朗日插值余项只剩下 $\frac{D''(\xi)}{2}(x - a)(x - b)$ 这一项，这一步正是“任意点展开后消元”；(3) $(x - a)(b - x)$ 的最大值点是中点，所以把 C 取在中点最划算. 注意只能“取一个 $x''$ 来达到 $\frac{(b - a)^3}{8}$: 对一般的 x 只有 $|D(x)| \geq \frac{b - a}{2}(x - a)(b - x)$.

**8.** (难度：★★★★★) 设 $f(x)$ 在 $[a,b]$ 上有连续二阶导数, 对 $\forall x \in [a,b]$, 满足 $|f(x)| \leq A$, $|f''(x)| \leq B$, 且存在 $x_0 \in [a,b]$ 使得 $|f'(x_0)| \leq D$, 其中 $A,B,D$ 均为正常数. 证明: $|f'(x)| \leq 2\sqrt{AB} + D$, $\forall x \in [a,b]$.

> [!answer]- 原书参考答案（C.0.2 第 8 题，未逐题独立验算）
> **8.** 要证的右边是 $D + 2\sqrt{AB}$，其中 $D$ 的来源很特别：它来自存在一点 $x_0$ 使 $|f'(x_0)| \leq D$”。
>
> 先试探两条路。若在固定点 $x_0$ 处展开，式子里出现的是 $f'(x_0)$ 与 $f''$，根本不会出现要估计的 $f'(x)$；若在任意点 $x$ 处展开，虽然能把 $f'(x)$ “反解”出来，但得到的是 $\frac{2A}{|y - x|} + \frac{B}{2}|y - x|$ 这样的形状，与 $D$ 无关，放缩不出 $D$。所以这只能是一道综合题：把区间按 $|x - x_0|$ 与 $2\sqrt{A/B}$ 的大小分成两段，每一段用一件最合适的工具。
>
> 第一段（离 $x_0$ 近， $|x - x_0| \leq 2\sqrt{A/B}$）：要出现 $D$，只能凑导数差再用拉格朗日，把 $f'(x) - f'(x_0)$ 与 $f''$ 联系起来，得到 $D + B|x - x_0| \leq D + 2\sqrt{AB}$。
>
> 第二段（离 $x_0$ 远）：用任意点展开反解 $f'(x)$，得到 $\frac{2A}{|y - x|} + \frac{B}{2}|y - x|$ 这样的“对勾”形状。直接套基本不等式得到的是“下界”，方向反了；正确做法是把 $|y - x|$ 取到它的最低点 $2\sqrt{A/B}$，此时右端恰好是 $2\sqrt{AB}$——而这样的 $y$ 由介值定理保证存在. 第一段: 当 $\left|x - x_0\right| \leqslant 2\sqrt{A/B}$ 时, 凑导数差 + 拉格朗日. 由拉格朗日中值定理, 存在 $\xi_1$ 介于 x 与 $x_0$ 之间, 使
>
> $$f^{\prime}(x)-f^{\prime}(x_{0})=(x-x_{0})f^{\prime\prime}(\xi_{1}),$$
>
> 于是
>
> $$\left|f^{\prime}(x)\right|\leqslant\left|f^{\prime}(x_{0})\right|+\left|f^{\prime\prime}(\xi_{1})\right|\left|x-x_{0}\right|\leqslant D+B\cdot2\sqrt{\frac{A}{B}}=D+2\sqrt{A B}.$$
>
> （这一步之所以能出现 D，正是因为它把 $f'(x)$ 与 $f'(x_0)$ 凑成了“导数差”，再交给拉格朗日中值定理。）
>
> 第二段: 当 $|x - x_0| > 2\sqrt{A/B}$ 时, 任意点展开 + 取最低点. 先任取 $y \in [a, b]$, $y \neq x$, 由带拉格朗日余项的泰勒公式 (在 x 处展开), 存在 $\eta$ 介于 x 与 y 之间, 使
>
> $$f(y)=f(x)+f^{\prime}(x)(y-x)+\frac{f^{\prime\prime}(\eta)}{2}(y-x)^{2},$$
>
> 反解出 $f'(x)$:
>
> $$f^{\prime}(x)=\frac{f(y)-f(x)}{y-x}-\frac{f^{\prime\prime}(\eta)}{2}(y-x),$$
>
> 于是
>
> $$\left|f^{\prime}(x)\right|\leqslant\frac{\left|f(y)\right|+\left|f(x)\right|}{\left|y-x\right|}+\frac{B}{2}\left|y-x\right|\leqslant\frac{2A}{\left|y-x\right|}+\frac{B}{2}\left|y-x\right|.$$
>
> 右端关于 $|y - x|$ 是“对勾”形状，它在 $|y - x| = 2\sqrt{\frac{A}{B}}$ 处取到最小值：
>
> $$\frac{2A}{2\sqrt{A/B}}+\frac{B}{2}\cdot2\sqrt{\frac{A}{B}}=\sqrt{AB}+\sqrt{AB}=2\sqrt{AB}.$$
>
> 直接套基本不等式只会得到“不小于 $2\sqrt{AB}'$”（方向与我们要的相反），所以改为主动把 $\left|y - x\right|$ 取到最低点：取 $y = t_0$，使 $\left|t_0 - x\right| = 2\sqrt{\frac{A}{B}}$。
>
> 这样的 $t_{0}$ 一定存在: $\left|x-t\right|$ 关于 t 在 $[a,b]$ 上连续, 而由本段的前提
>
> $$0=\left|x-x\right|<2\sqrt{\frac{A}{B}}<\left|x-x_{0}\right|,$$
>
> 故由介值定理, 存在 $t_{0}$ 介于 x 与 $x_{0}$ 之间, 使 $\left|t_{0}-x\right|=2\sqrt{\frac{A}{B}}$. 把 $y=t_{0}$ 代入上面的估计, 得
>
> $$\left|f^{\prime}(x)\right|\leqslant\frac{2A}{2\sqrt{A/B}}+\frac{B}{2}\cdot2\sqrt{\frac{A}{B}}=2\sqrt{A B}\leqslant D+2\sqrt{A B}.$$
>
> 两段合起来, 对一切 $x \in [a,b]$ 都有 $|f'(x)| \leqslant D + 2\sqrt{AB}$. 这道题的价值在”识别题型": 结论里既有”任意点的 $f'(x)$”, 又有来自”某一点的 $f'(x)$”的常数 D, 说明单独的固定点展开或任意点展开都不够, 必须分区间、换工具. 两个技术点: 一是”凑导数差 + 拉格朗日”是唯一能凭空造出 D 的手段; 二是 $\frac{2A}{|y-x|} + \frac{B}{2}|y-x|$ 这个”对勾”形状要取最低点, 而不是套基本不等式——基本不等式给出的恰是反方向的下界.

**9.** (难度:★★★) 设 $f(x)$ 在 $(-\infty, +\infty)$ 内三阶导数连续, 证明: 存在 $\xi \in (-\infty, +\infty)$ 使得

$$f(\xi)f^{\prime}(\xi)f^{\prime\prime}(\xi)f^{\prime\prime\prime}(\xi)\geqslant0.$$

> [!answer]- 原书参考答案（C.0.2 第 9 题，未逐题独立验算）
> **9.** 反证. 若对一切 x 都有 $f(x)f'(x)f''(x)f'''(x) < 0$, 则 $f, f', f'', f'''$ 都无零点, 各自保持定号. 把 f 换成 $-f$ (四个因子的乘积不变) 可设 $f(x) > 0$. 于是 $f'(x)f''(x)f'''(x) < 0$, 即 $f', f'', f'''$ 中负号个数为奇数.
>
> 情形一： $f' < 0$。此时 f > 0 且单调递减，故 f 在 $+\infty$ 处有有限极限；又 $f''$ 定号（ $f'$ 单调），故 $f'(x) \to 0 (x \to +\infty)$。
>
> 若 $f'' > 0$，则由 $f'f''f''' < 0$ 得 $f''' > 0$，即 $f''$ 递增；于是 $x \geq 0$ 时 $f''(x) \geq f''(0) > 0$，从而
>
> $$f^{\prime}(x)\geqslant f^{\prime}(0)+x f^{\prime\prime}(0)\longrightarrow+\infty\quad(x\to+\infty),$$
>
> 与 $f'(x)<0$矛盾.
>
> 若 $f''<0$，则 $f'''<0$，即 $f'$ 递减；于是 $x\geq0$ 时 $f'(x)\leq f'(0)<0$，从而 $f(x)\to-\infty(x\to+\infty)$，与 $f(x)>0$ 矛盾。
>
> 情形二： $f^{\prime}>0$。此时 f>0 且单调递增，故 f 在 $-\infty$ 处有有限极限，同样由 $f^{\prime}$ 的单调性得 $f^{\prime}(x)\to0(x\to-\infty)$。
>
> 若 $f'' > 0$，则 $f''' < 0$，即 $f''$ 递减；于是 $x \leq 0$ 时 $f''(x) \geq f''(0) > 0$，从而
>
> $$f^{\prime}(x)\leqslant f^{\prime}(0)+x f^{\prime\prime}(0)\longrightarrow-\infty\quad(x\to-\infty),$$
>
> 与 $f'(x)>0$矛盾.
>
> 若 $f''<0$，则 $f'''>0$，即 $f''$ 递增；于是 $x\geq0$ 时 $f''(x)\leq f''(0)<0$，从而
>
> $$f^{\prime}(x)\leqslant f^{\prime}(0)+x f^{\prime\prime}(0)\longrightarrow-\infty\quad(x\to+\infty),$$
>
> 仍与 $f'(x) > 0$ 矛盾.
>
> 两种情形都不可能，故反设不成立，即存在 $\xi \in \mathbb{R}$，使
>
> $$f(\xi)f^{\prime}(\xi)f^{\prime\prime}(\xi)f^{\prime\prime\prime}(\xi)\geqslant0.$$

---

# 强化篇·第三章 一元积分学

## 3.1 定积分定义

将难以直接计算的极限转为对应的定积分，进而进行间接求解。在定积分转化时，同时也要考虑夹逼定理进行对应的放缩，最后仍需注意对定积分定义估测极限的余项差的分析。

**1.** (难度: ★) 求极限

$$\lim_{n\to\infty}\frac{\left(1^{2025}+2^{2025}+\cdots+n^{2025}\right)^{2025}}{\left(1^{2024}+2^{2024}+\cdots+n^{2024}\right)^{2026}}.$$

> [!answer]- 原书参考答案（D.0.1 第 1 题，未逐题独立验算）
> **1.** 第一步：分子、分母各写成定积分定义的形式. 记所求极限为 I. 分别把两个幂和式提出 n 的方幂, 使 $\frac{k}{n}$ 显式出现:
>
> $$\sum_{k=1}^{n}k^{2025}=n^{2026}\cdot\frac{1}{n}\sum_{k=1}^{n}\left(\frac{k}{n}\right)^{2025},\qquad\sum_{k=1}^{n}k^{2024}=n^{2025}\cdot\frac{1}{n}\sum_{k=1}^{n}\left(\frac{k}{n}\right)^{2024}.$$
>
> 代入后，分子出现 $n^{2026\cdot2025}$ 、分母出现 $n^{2025\cdot2026}$ ，两者相等，正好抵消：
>
> $$I=\lim_{n\to\infty}\frac{\left(\frac{1}{n}\sum_{k=1}^{n}\left(\frac{k}{n}\right)^{2025}\right)^{2025}}{\left(\frac{1}{n}\sum_{k=1}^{n}\left(\frac{k}{n}\right)^{2024}\right)^{2026}}.$$
>
> 第二步：对两个 Riemann 和取极限. 由定积分定义,
>
> $$\lim_{n\to\infty}\frac{1}{n}\sum_{k=1}^{n}\left(\frac{k}{n}\right)^{2025}=\int_{0}^{1}x^{2025}\mathrm{d}x=\frac{1}{2026},$$
>
> $$\lim_{n\to\infty}\frac{1}{n}\sum_{k=1}^{n}\left(\frac{k}{n}\right)^{2024}=\int_{0}^{1}x^{2024}\mathrm{d}x=\frac{1}{2025}.$$
>
> 幂函数连续、取幂运算保持极限，代入得
>
> $$\begin{aligned}I&=\frac{\left(\frac{1}{2026}\right)^{2025}}{\left(\frac{1}{2025}\right)^{2026}}\\&=\frac{2025^{2026}}{2026^{2025}}.\end{aligned}$$

**2.** （难度：★★）求极限

$$\lim_{n\to\infty}\sin\frac{\pi}{n}\left(\sqrt{1+\frac{1}{n}}+\sqrt{1+\frac{2}{n}}+\cdots+\sqrt{1+\frac{n}{n}}\right).$$

> [!answer]- 原书参考答案（D.0.1 第 2 题，未逐题独立验算）
> **2.** 第一步: 把 $\sin\frac{\pi}{n}$ 拆成 $\frac{\pi}{n}$ 乘一个趋于 1 的因子”.
>
> $$\sin\frac{\pi}{n}=\frac{\sin(\pi/n)}{\pi/n}\cdot\frac{\pi}{n},\qquad\lim_{n\to\infty}\frac{\sin(\pi/n)}{\pi/n}=1.$$
>
> 原式中的和式配上系数 $\frac{\pi}{n}$ 后, 就是一个标准的 Riemann 和:
>
> $$\frac{\pi}{n}\sum_{k=1}^{n}\sqrt{1+\frac{k}{n}}=\pi\cdot\frac{1}{n}\sum_{k=1}^{n}\sqrt{1+\frac{k}{n}}\longrightarrow\pi\int_{0}^{1}\sqrt{1+x}\mathrm{d}x.$$
>
> 第二步：分别取极限再相乘.由
>
> $$\int_{0}^{1}\sqrt{1+x}\mathrm{d}x=\frac{2}{3}(1+x)^{3/2}\Big|_{0}^{1}=\frac{2}{3}\left(2\sqrt{2}-1\right),$$
>
> 得原极限
>
> $$\lim_{n\to\infty}\frac{\sin(\pi/n)}{\pi/n}\cdot\frac{\pi}{n}\sum_{k=1}^{n}\sqrt{1+\frac{k}{n}}=\frac{2}{3}\pi\left(2\sqrt{2}-1\right).$$
>
> 这里“凑乘除”与“做差”本质相同：把 $\sin\frac{\pi}{n}$ 换成一个趋于1的因子与 $\frac{\pi}{n}$的乘积，误差是被压到0的高阶量，无需再作两边夹逼.

**3.** （难度：★★★）求极限

$$\lim_{n\to\infty}\sqrt{n}\left(1-\sum_{k=1}^{n}\frac{1}{n+\sqrt{k}}\right).$$

> [!answer]- 原书参考答案（D.0.1 第 3 题，未逐题独立验算）
> **3.** 把常数1写成 $\sum_{k=1}^{n}\frac{1}{n}$，与和式统一形式：
>
> $$S=\sqrt{n}\left(\sum_{k=1}^{n}\frac{1}{n}-\sum_{k=1}^{n}\frac{1}{n+\sqrt{k}}\right)=\sqrt{n}\sum_{k=1}^{n}\frac{\sqrt{k}}{n(n+\sqrt{k})}=\sum_{k=1}^{n}\frac{1}{n+\sqrt{k}}\sqrt{\frac{k}{n}}.$$
>
> 与等价的 Riemann 和做差：
>
> $$\begin{aligned}\left|S-\frac{1}{n}\sum_{k=1}^{n}\sqrt{\frac{k}{n}}\right|&=\left|\sum_{k=1}^{n}\left(\frac{1}{n+\sqrt{k}}-\frac{1}{n}\right)\sqrt{\frac{k}{n}}\right|=\left|\sum_{k=1}^{n}\frac{\sqrt{k}}{n(n+\sqrt{k})}\sqrt{\frac{k}{n}}\right|\\&=\sum_{k=1}^{n}\frac{k}{n\sqrt{n}\left(n+\sqrt{k}\right)}\leqslant\sum_{k=1}^{n}\frac{k}{n\sqrt{n}\cdot n}=\frac{n+1}{2n^{3/2}}\longrightarrow0.\end{aligned}$$
>
> 由夹逼定理，
>
> $$\lim_{n\to\infty}\left|S-\frac{1}{n}\sum_{k=1}^{n}\sqrt{\frac{k}{n}}\right|=0,\qquad\lim_{n\to\infty}\frac{1}{n}\sum_{k=1}^{n}\sqrt{\frac{k}{n}}=\int_{0}^{1}\sqrt{x}\mathrm{d}x=\frac{2}{3},$$
>
> 故 $\lim_{n\to\infty}S=\frac{2}{3}$

**4.** （难度：★★★）求极限

$$\lim_{n\to\infty}\sum_{k=1}^{n}\frac{(2k-1)^{4}}{n^{5}+k^{4}}.$$

> [!answer]- 原书参考答案（D.0.1 第 4 题，未逐题独立验算）
> **4.** 通项 $(2k-1)^{4}$ 与 $16k^{4}$ 只差一个低阶项，故先与 $\frac{16}{n}\sum\left(\frac{k}{n}\right)^{4}$ 做差，把差拆成两部分分别放缩。记 $S_{n}=\sum_{k=1}^{n}\frac{(2k-1)^{4}}{n^{5}+k^{4}}$，并取等价的 Riemann 和
>
> $$R_{n}=\frac{16}{n}\sum_{k=1}^{n}\left(\frac{k}{n}\right)^{4}=\sum_{k=1}^{n}\frac{16k^{4}}{n^{5}},\qquad\lim_{n\to\infty}R_{n}=16\int_{0}^{1}x^{4}\mathrm{d}x=\frac{16}{5}.$$
>
> 做差（把 $16k^{4}$ 写成 $(2k)^{4}$，便于与 $(2k-1)^{4}$ 配对）：
>
> $$\begin{aligned}\left|S_{n}-R_{n}\right|&=\left|\sum_{k=1}^{n}\left(\frac{(2k-1)^{4}}{n^{5}+k^{4}}-\frac{16k^{4}}{n^{5}}\right)\right|=\left|\sum_{k=1}^{n}\frac{(2k-1)^{4}n^{5}-(2k)^{4}n^{5}-16k^{8}}{n^{5}(n^{5}+k^{4})}\right|\\&\leqslant\sum_{k=1}^{n}\frac{\left|(2k-1)^{4}-(2k)^{4}\right|}{n^{5}+k^{4}}+\sum_{k=1}^{n}\frac{16k^{8}}{n^{5}(n^{5}+k^{4})}.\end{aligned}$$
>
> 第一项: 由 $\left|(2k-1)^{4}-(2k)^{4}\right|=(8k^{2}-4k+1)(4k-1)$，且 $k \leqslant n$ 时 $8k^{2}-4k+1 \leqslant 9n^{2}$、 $4k-1 \leqslant 5n$，故
>
> $$\sum_{k=1}^{n}\frac{\left|(2k-1)^{4}-(2k)^{4}\right|}{n^{5}+k^{4}}\leqslant\sum_{k=1}^{n}\frac{9n^{2}\cdot5n}{n^{5}}=\frac{45}{n}.$$
>
> 第二项: 由 $k^{8} \leqslant n^{8}$、 $n^{5} + k^{4} \geqslant n^{5}$,
>
> $$\sum_{k=1}^{n}\frac{16k^{8}}{n^{5}(n^{5}+k^{4})}\leqslant\sum_{k=1}^{n}\frac{16n^{8}}{n^{5}\cdot n^{5}}=\frac{16}{n}.$$
>
> 于是 $\left|S_{n}-R_{n}\right|\leqslant\frac{61}{n}\rightarrow0$ ，由夹逼定理 $S_{n}$ 与 $R_{n}$ 同极限，故
>
> $$\lim_{n\to\infty}S_{n}=\frac{16}{5}.$$
>
> 这是"做差放缩"的标准写法: 把通项拆成"标准 Riemann 和项 + 余项", 余项分成"分子误差"与"分母误差"两块分别控制. 注意比较目标是 $16\left(\frac{k}{n}\right)^4$ 而不要写成 $(2k-1)^4 \to 16k^4$ 后直接取极限.

**5.** (难度:★★★) 设 $f(x,y)$ 在 $D=\left\{(x,y)\mid0\leqslant x\leqslant1,0\leqslant y\leqslant1\right\}$ 上连续, 且 $f(x,y)=f(y,x),\iint_{D}f(x,y)dxdy=A$, 求极限:

$$\lim_{n\to\infty}\sum_{i=1}^{2n}\sum_{j=1}^{i}\frac{1}{2n^{2}}f\left(\frac{i}{2n},\frac{j}{2n}\right).$$

> [!answer]- 原书参考答案（D.0.1 第 5 题，未逐题独立验算）
> **5.** 第一步：认面积元，把系数凑成 $\frac{1}{(2n)^2}$. 两层求和的步长都是 $\frac{1}{2n}$，故面积元应是 $\frac{1}{(2n)^2} = \frac{1}{4n^2}$. 提出常数因子 4:
>
> $$\sum_{i=1}^{2n}\sum_{j=1}^{i}\frac{1}{n^{2}}f\left(\frac{i}{2n},\frac{j}{2n}\right)=4\sum_{i=1}^{2n}\sum_{j=1}^{i}\frac{1}{4n^{2}}f\left(\frac{i}{2n},\frac{j}{2n}\right).$$
>
> 第二步: 从求和范围读出积分区域. 内层上限为 i, 即 $\frac{j}{2n} \leq \frac{i}{2n}$, 也就是 $y \leq x$; 外层跑遍 $[0,1]$, 故区域为
>
> $$D_{1}=\left\{\left(x,y\right)\mid0\leqslant x\leqslant1,\;0\leqslant y\leqslant x\right\}.$$
>
> 由二重积分定义，
>
> $$\lim_{n\to\infty}\sum_{i=1}^{2n}\sum_{j=1}^{i}\frac{1}{4n^{2}}f\bigg(\frac{i}{2n},\frac{j}{2n}\bigg)=\iint_{D_{1}}f(x,y)\mathrm{d}x\mathrm{d}y.$$
>
> 第三步：用对称性把 $\iint_{D_{1}} f(x,y) \, dx \, dy$ 算出来. 把正方形 D 沿对角线 y = x 分成
>
> $$D_{1}=\left\{0\leqslant y\leqslant x\leqslant1\right\},\qquad D_{2}=\left\{0\leqslant x\leqslant y\leqslant1\right\}.$$
>
> 在 $D_{2}$ 上作换元 $(x,y) \mapsto (y,x)$，它把 $D_{2}$ 一一映到 $D_{1}$，且 $dxdy$ 不变，于是
>
> $$\iint_{D_{2}}f(x,y)\mathrm{d}x\mathrm{d}y=\iint_{D_{1}}f(y,x)\mathrm{d}x\mathrm{d}y.$$
>
> 又 $f(x,y)=f(y,x)$，所以 $\iint_{D_1}f(x,y)dxdy=\iint_{D_2}f(x,y)dxdy=\frac{1}{2}\iint_{D}f(x,y)dxdy=\frac{A}{2}$.
>
> 第四步：代入系数. 原极限
>
> $$=4\iint_{D_{1}}f(x,y)\mathrm{d}x\mathrm{d}y=4\cdot\frac{A}{2}=2A.$$

**6.** (难度：★★★★) 已知 $f(x)$ 在 $[a, b]$ 上二阶连续可导, 据此求下列极限:

(1)

$$\lim_{n\to\infty}n\left(\int_{a}^{b}f(x)\mathrm{d}x-\frac{b-a}{n}\sum_{k=1}^{n}f\left(a+\frac{k}{n}(b-a)\right)\right).$$

(2)

$$\lim_{n\to\infty}n^{2}\left(\int_{a}^{b}f(x)dx-\frac{b-a}{n}\sum_{k=1}^{n}f\left(a+\frac{2k-1}{2n}(b-a)\right)\right).$$

> [!answer]- 原书参考答案（D.0.1 第 6 题，未逐题独立验算）
> **6.** 两问的共同思路是：把定积分按相同的分点拆成 n 个小段，与和式逐项配对相减，再对每个小区间作中值或泰勒估计。两者的差别只在取样点：右端点取到的是一阶余项，中点取到的是二阶余项。
>
> (1) 右端点取值: 一阶余项. 把积分写成
>
> $$\begin{aligned}&\int_{a}^{b}f(x)\mathrm{d}x-\frac{b-a}{n}\sum_{k=1}^{n}f\biggl(a+\frac{k}{n}(b-a)\biggr)\\&\quad=\sum_{k=1}^{n}\int_{a+\frac{k-1}{n}(b-a)}^{a+\frac{k}{n}(b-a)}f(x)\mathrm{d}x-\sum_{k=1}^{n}\int_{a+\frac{k-1}{n}(b-a)}^{a+\frac{k}{n}(b-a)}f\biggl(a+\frac{k}{n}(b-a)\biggr)\mathrm{d}x\\&\quad=\sum_{k=1}^{n}\int_{a+\frac{k-1}{n}(b-a)}^{a+\frac{k}{n}(b-a)}\biggl[f(x)-f\biggl(a+\frac{k}{n}(b-a)\biggr)\biggr]\mathrm{d}x.\end{aligned}$$
>
> 在小区间上对 $f(x)-f\left(a+\frac{k}{n}(b-a)\right)$ 用拉格朗日中值定理: 存在 $\xi$ 介于 x 与 $a+\frac{k}{n}(b-a)$ 之间, 使
>
> $$f(x)-f\left(a+\frac{k}{n}(b-a)\right)=\left(x-a-\frac{k}{n}(b-a)\right)f^{\prime}(\xi).$$
>
> 因子 x - a - $\frac{k}{n}$ (b - a) 在小区间上恒非正、不变号，故由第一积分中值定理，存在
>
> $$\eta_{k}\in\left[a+\frac{k-1}{n}(b-a),a+\frac{k}{n}(b-a)\right],$$
>
> 使
>
> $$\begin{aligned}&\int_{a+\frac{k-1}{n}(b-a)}^{a+\frac{k}{n}(b-a)}\left(x-a-\frac{k}{n}(b-a)\right)f^{\prime}(\xi)\mathrm{d}x\\&\quad=f^{\prime}(\eta_{k})\int_{a+\frac{k-1}{n}(b-a)}^{a+\frac{k}{n}(b-a)}\left(x-a-\frac{k}{n}(b-a)\right)\mathrm{d}x\\&\quad=-\frac{(b-a)^{2}}{2n^{2}}f^{\prime}(\eta_{k}),\end{aligned}$$
>
> 最后一个积分是把小区间平移到 $\left[-\frac{b-a}{n},0\right]$ 上算出的. 对 k 求和:
>
> $$\begin{aligned}\int_{a}^{b}&f(x)\mathrm{d}x-\frac{b-a}{n}\sum_{k=1}^{n}f\bigg(a+\frac{k}{n}(b-a)\bigg)\\&=-\frac{(b-a)^{2}}{2n^{2}}\sum_{k=1}^{n}f^{\prime}(\eta_{k}).\end{aligned}$$
>
> 两边乘 n，并把它写成 $\frac{b-a}{2}\cdot\frac{b-a}{n}\sum_{k=1}^{n}f'(\eta_{k})$ 的形式:
>
> $$\begin{aligned}n&\left(\int_{a}^{b}f(x)\mathrm{d}x-\frac{b-a}{n}\sum_{k=1}^{n}f\bigg(a+\frac{k}{n}(b-a)\bigg)\right)\\&=-\frac{b-a}{2}\cdot\frac{b-a}{n}\sum_{k=1}^{n}f^{\prime}(\eta_{k})\\&\longrightarrow-\frac{b-a}{2}\int_{a}^{b}f^{\prime}(x)\mathrm{d}x=-\frac{b-a}{2}\left(f(b)-f(a)\right).\end{aligned}$$
>
> (2) 中点取值：二阶余项. 记
>
> $$x_{k}=a+\frac{k-1}{n}(b-a),\qquad y_{k}=a+\frac{k}{n}(b-a),$$
>
> $$z_{k}=\frac{x_{k}+y_{k}}{2}=a+\frac{2k-1}{2n}(b-a),$$
>
> 即 $z_{k}$ 是小区间 $[x_{k}, y_{k}]$ 的中点. 逐项配对相减:
>
> $$\begin{aligned}\int_{a}^{b}f(x)\mathrm{d}x-\frac{b-a}{n}\sum_{k=1}^{n}f(z_{k})\\=\sum_{k=1}^{n}\int_{x_{k}}^{y_{k}}\left[f(x)-f(z_{k})\right]\mathrm{d}x.\end{aligned}$$
>
> 在 $z_{k}$处作带拉格朗日余项的泰勒展开：
>
> $$f(x)=f(z_{k})+f^{\prime}(z_{k})(x-z_{k})+\frac{f^{\prime\prime}(\theta_{k})}{2}(x-z_{k})^{2},$$
>
> 其中 $\theta_{k} \in [x_{k}, y_{k}]$. 因 $\int_{x_{k}}^{y_{k}} (x - z_{k}) \, \mathrm{d}x = 0$ (被积因子关于 $z_{k}$ 反对称), 一次项积分为零, 于是
>
> $$\begin{aligned}\int_{x_{k}}^{y_{k}}&\left[f(x)-f(z_{k})\right]\mathrm{d}x\\&=\frac{1}{2}\int_{x_{k}}^{y_{k}}f^{\prime\prime}(\theta_{k})(x-z_{k})^{2}\mathrm{d}x\\&=\frac{1}{2}f^{\prime\prime}(\xi_{k})\int_{x_{k}}^{y_{k}}(x-z_{k})^{2}\mathrm{d}x,\end{aligned}$$
>
> 其中第二步又用了第一积分中值定理（因子 $(x-z_{k})^{2}\geqslant0$不变号）.而
>
> $$\int_{x_{k}}^{y_{k}}(x-z_{k})^{2}\mathrm{d}x=\int_{-\frac{b-a}{2n}}^{\frac{b-a}{2n}}u^{2}\mathrm{d}u=\frac{(b-a)^{3}}{12n^{3}},$$
>
> 所以
>
> $$\begin{aligned}&\int_{a}^{b}f(x)\mathrm{d}x-\frac{b-a}{n}\sum_{k=1}^{n}f(z_{k})\\&\quad=\frac{(b-a)^{3}}{24n^{3}}\sum_{k=1}^{n}f^{\prime\prime}(\xi_{k}).\end{aligned}$$
>
> 两边乘 $n^{2}$，再写成 $\frac{(b-a)^{2}}{24} \cdot \frac{b-a}{n} \sum_{k=1}^{n} f''(\xi_{k})$ 的形式：
>
> $$\begin{aligned}n^{2}&\left(\int_{a}^{b}f(x)\mathrm{d}x-\frac{b-a}{n}\sum_{k=1}^{n}f(z_{k})\right)\\&=\frac{(b-a)^{2}}{24}\cdot\frac{b-a}{n}\sum_{k=1}^{n}f^{\prime\prime}(\xi_{k})\\&\longrightarrow\frac{(b-a)^{2}}{24}\int_{a}^{b}f^{\prime\prime}(x)\mathrm{d}x=\frac{(b-a)^{2}}{24}\left(f^{\prime}(b)-f^{\prime}(a)\right).\end{aligned}$$

## 3.2 原函数法

基础的做题方法, 往往也可以处理并不基础的题目. 将变限积分看作新函数, 以微分学的视角研究问题, 同样是值得去尝试的一个做题思路.

**1.** (难度: ★★★) 设函数 $f(x)$ 在闭区间 $[a, b]$ 上具有连续的二阶导数. 试证: 存在 $\xi \in (a, b)$, 使

$$\int_{a}^{b}f(x)\mathrm{d}x=(b-a)f\left(\frac{a+b}{2}\right)+\frac{1}{24}(b-a)^{3}f^{\prime\prime}(\xi).$$

> [!answer]- 原书参考答案（D.0.2 第 1 题，未逐题独立验算）
> **1.** 第一步：把积分写成原函数，转化为“函数值之差”问题.令
>
> $$F(x)=\int_{a}^{x}f(t)\mathrm{d}t,$$
>
> 则
>
> $$F(a)=0,\qquad F^{\prime}(x)=f(x),\qquad F^{\prime\prime}(x)=f^{\prime}(x),\qquad F^{\prime\prime\prime}(x)=f^{\prime\prime}(x),$$
>
> 且 $\int_{a}^{b}f(x)dx = F(b)$. 于是结论化归为: 用 $F'''(\xi) = f''(\xi)$ 表达 $F(b)$.
>
> 第二步: 在区间中点处对 $F(x)$ 作三阶泰勒展开. 记中点为 $\frac{a+b}{2}$. 由带拉格朗日余项的泰勒公式,
>
> $$\begin{aligned}F(x)&=F\biggl(\frac{a+b}{2}\biggr)+f\biggl(\frac{a+b}{2}\biggr)\biggl(x-\frac{a+b}{2}\biggr)\\&\quad+\frac{f^{\prime}\left(\frac{a+b}{2}\right)}{2}\left(x-\frac{a+b}{2}\right)^{2}+\frac{f^{\prime\prime}(\zeta)}{6}\left(x-\frac{a+b}{2}\right)^{3},\end{aligned}$$
>
> 其中 $\zeta$ 落在 x 与 $\frac{a+b}{2}$ 之间.
>
> 第三步：代入 x = a、x = b，两式相减。注意
>
> $$a-\frac{a+b}{2}=-\frac{b-a}{2},\qquad b-\frac{a+b}{2}=\frac{b-a}{2},\qquad\frac{1}{6}\cdot\frac{(b-a)^{3}}{8}=\frac{(b-a)^{3}}{48}.$$
>
> 代入 $x = a$ (余项点记为 $\xi_1 \in \left(a, \frac{a+b}{2}\right)$):
>
> $$\begin{aligned}0=F(a)={}&F\biggl(\frac{a+b}{2}\biggr)-\frac{b-a}{2}f\biggl(\frac{a+b}{2}\biggr)\\&+\frac{(b-a)^{2}}{8}f^{\prime}\biggl(\frac{a+b}{2}\biggr)-\frac{(b-a)^{3}}{48}f^{\prime\prime}(\xi_{1}).\end{aligned}$$
>
> 代入 $x = b$（余项点记为 $\xi_2 \in \left( \frac{a + b}{2}, b \right)$）：
>
> $$\begin{aligned}\int_{a}^{b}f(x)\mathrm{d}x=F(b)={}&F\biggl(\frac{a+b}{2}\biggr)+\frac{b-a}{2}f\biggl(\frac{a+b}{2}\biggr)\\&+\frac{(b-a)^{2}}{8}f^{\prime}\biggl(\frac{a+b}{2}\biggr)+\frac{(b-a)^{3}}{48}f^{\prime\prime}(\xi_{2}).\end{aligned}$$
>
> (2)-(1)，含 $F(x)$与 $f'(x)$的项全部消去：
>
> $$\begin{aligned}\int_{a}^{b}f(x)\mathrm{d}x&=(b-a)f\bigg(\frac{a+b}{2}\bigg)\\&\quad+\frac{(b-a)^{3}}{48}\left[f^{\prime\prime}(\xi_{1})+f^{\prime\prime}(\xi_{2})\right].\end{aligned}$$
>
> 第四步: 用介值性把两处 $f''(x)$ 合并成一处. 由 $f''(x)$ 连续, $\frac{f''(\xi_1) + f''(\xi_2)}{2}$ 介于 $f''(\xi_1)$ 与 $f''(\xi_2)$ 之间, 故存在 $\xi \in (\xi_1, \xi_2) \subset (a, b)$, 使
>
> $$f^{\prime\prime}(\xi)=\frac{f^{\prime\prime}(\xi_{1})+f^{\prime\prime}(\xi_{2})}{2}.$$
>
> 代入即得
>
> $$\int_{a}^{b}f(x)\mathrm{d}x=(b-a)f\left(\frac{a+b}{2}\right)+\frac{(b-a)^{3}}{24}f^{\prime\prime}(\xi).$$

**2.** (难度:★★★) 设函数 $f(x)$ 在 $[a,b]$ 上有连续的二阶导数. 证明: 存在 $\xi \in (a,b)$, 使

$$\int_{a}^{b}f(x)\mathrm{d}x=\frac{1}{2}[f(a)+f(b)](b-a)-\frac{1}{12}f^{\prime\prime}(\xi)(b-a)^{3}.$$

> [!answer]- 原书参考答案（D.0.2 第 2 题，未逐题独立验算）
> **2.** 下面给出两种写法.
>
> 解一（两次分部积分，把 dx 凑成 $\mathrm{d}\left(x-\frac{a+b}{2}\right)$）。因为 $\mathrm{d}x=\mathrm{d}\left(x-\frac{a+b}{2}\right)$，先分部积分一次：
>
> $$\begin{aligned}\int_{a}^{b}f(x)\mathrm{d}x&=\left[f(x)\left(x-\frac{a+b}{2}\right)\right]_{a}^{b}-\int_{a}^{b}\left(x-\frac{a+b}{2}\right)f^{\prime}(x)\mathrm{d}x\\&=\frac{b-a}{2}\left[f(a)+f(b)\right]-\int_{a}^{b}\left(x-\frac{a+b}{2}\right)f^{\prime}(x)\mathrm{d}x,\end{aligned}$$
>
> 其中边界项为 $f(b) \cdot \frac{b-a}{2} - f(a) \cdot \left(-\frac{b-a}{2}\right) = \frac{b-a}{2} [f(a) + f(b)]$. 再对 $\int_{a}^{b} \left( x - \frac{a+b}{2} \right) f'(x)\,\mathrm{d}x$ 分部积分（取 $v = \frac{1}{2} \left( x - \frac{a+b}{2} \right)^2$）：
>
> $$\begin{aligned}\int_{a}^{b}\left(x-\frac{a+b}{2}\right)f^{\prime}(x)\mathrm{d}x&=\frac{(b-a)^{2}}{8}\left[f^{\prime}(b)-f^{\prime}(a)\right]\\&\quad-\frac{1}{2}\int_{a}^{b}\left(x-\frac{a+b}{2}\right)^{2}f^{\prime\prime}(x)\mathrm{d}x,\end{aligned}$$
>
> 因为 $\left(x-\frac{a+b}{2}\right)^{2}$ 在两端的值都是 $\frac{(b-a)^{2}}{4}$. 于是
>
> $$\begin{aligned}\int_{a}^{b}f(x)\mathrm{d}x=\frac{b-a}{2}\left[f(a)+f(b)\right]-\frac{(b-a)^{2}}{8}\left[f^{\prime}(b)-f^{\prime}(a)\right]\\+\frac{1}{2}\int_{a}^{b}\left(x-\frac{a+b}{2}\right)^{2}f^{\prime\prime}(x)\mathrm{d}x.\end{aligned}$$
>
> 把 $f'(b) - f'(a) = \int_{a}^{b} f''(t) \, dt$ 代入，得
>
> $$\int_{a}^{b}f(x)\mathrm{d}x-\frac{b-a}{2}\left[f(a)+f(b)\right]=\int_{a}^{b}f^{\prime\prime}(t)\left[\frac{1}{2}\left(t-\frac{a+b}{2}\right)^{2}-\frac{(b-a)^{2}}{8}\right]\mathrm{d}t.$$
>
> 右边方括号里的函数是以 $\frac{a+b}{2}$为最低点的抛物线，且在 $t=a,b$处恰好为0，因此它在 $[a,b]$上恒不为正、且不变号。由第一积分中值定理，存在 $\xi\in(a,b)$，使
>
> $$\begin{aligned}\int_{a}^{b}f^{\prime \prime}(t)&\left[\frac{1}{2}\left(t-\frac{a+b}{2}\right)^{2}-\frac{(b-a)^{2}}{8}\right]\mathrm{d}t\\&=f^{\prime \prime}(\xi)\int_{a}^{b}\left[\frac{1}{2}\left(t-\frac{a+b}{2}\right)^{2}-\frac{(b-a)^{2}}{8}\right]\mathrm{d}t,\end{aligned}$$
>
> 而
>
> $$\int_{a}^{b}\left[\frac{1}{2}\left(t-\frac{a+b}{2}\right)^{2}-\frac{(b-a)^{2}}{8}\right]\mathrm{d}t=\frac{1}{2}\cdot\frac{(b-a)^{3}}{12}-\frac{(b-a)^{3}}{8}=-\frac{(b-a)^{3}}{12},$$
>
> 所以
>
> $$\int_{a}^{b}f(x)\mathrm{d}x=\frac{1}{2}\left[f(a)+f(b)\right](b-a)-\frac{1}{12}f^{\prime\prime}(\xi)(b-a)^{3}.$$
>
> 解二（在 $x=\frac{a+b}{2}$ 处作带积分余项的泰勒展开，推荐）. 由带积分余项的泰勒公式，
>
> $$f(x)=f\left(\frac{a+b}{2}\right)+f^{\prime}\left(\frac{a+b}{2}\right)\left(x-\frac{a+b}{2}\right)+\int_{\frac{a+b}{2}}^{x}f^{\prime\prime}(t)(x-t)\mathrm{d}t.$$
>
> (1) 把上式在 $[a, b]$ 上积分. 一次项的积分为 $f' \left( \frac{a+b}{2} \right) \int_{a}^{b} \left( x - \frac{a+b}{2} \right) \, \mathrm{d}x = 0;$ 对积分余项交换积分次序 $(t > \frac{a+b}{2}$ 时 x 从 t 到 b, $t < \frac{a+b}{2}$ 时 x 从 a 到 t):
>
> $$\int_{a}^{b}\int_{\frac{a+b}{2}}^{x}f^{\prime\prime}(t)(x-t)\mathrm{d}t\mathrm{d}x=\frac{1}{2}\int_{a}^{\frac{a+b}{2}}f^{\prime\prime}(t)\left(t-a\right)^{2}\mathrm{d}t+\frac{1}{2}\int_{\frac{a+b}{2}}^{b}f^{\prime\prime}(t)\left(b-t\right)^{2}\mathrm{d}t.$$
>
> 于是
>
> $$\begin{aligned}\int_{a}^{b}f(x)\mathrm{d}x&=(b-a)f\bigg(\frac{a+b}{2}\bigg)+\frac{1}{2}\int_{a}^{\frac{a+b}{2}}f^{\prime\prime}(t)(t-a)^{2}\mathrm{d}t\\&\quad+\frac{1}{2}\int_{\frac{a+b}{2}}^{b}f^{\prime\prime}(t)(b-t)^{2}\mathrm{d}t.\end{aligned}\tag{1}$$
>
> (2) 把 $f(a)$ 与 $f(b)$ 也在 $x = \frac{a+b}{2}$ 处展开再相加. 由同一个公式,
>
> $$f(a)=f\left(\frac{a+b}{2}\right)+f^{\prime}\left(\frac{a+b}{2}\right)\left(a-\frac{a+b}{2}\right)+\int_{\frac{a+b}{2}}^{a}f^{\prime\prime}(t)(a-t)\mathrm{d}t,$$
>
> $$f(b)=f\left(\frac{a+b}{2}\right)+f^{\prime}\left(\frac{a+b}{2}\right)\left(b-\frac{a+b}{2}\right)+\int_{\frac{a+b}{2}}^{b}f^{\prime\prime}(t)(b-t)\mathrm{d}t.$$
>
> 两式相加时 $\left(a-\frac{a+b}{2}\right)+\left(b-\frac{a+b}{2}\right)=0$ ，一次项消掉；再把 $\int_{\frac{a+b}{2}}^{a}f''(t)(a-t)\,\mathrm{d}t=\int_{a}^{\frac{a+b}{2}}f''(t)(t-a)\,\mathrm{d}t$ 换向，得
>
> $$f(a)+f(b)=2f\left(\frac{a+b}{2}\right)+\int_{a}^{\frac{a+b}{2}}f^{\prime\prime}(t)(t-a)\mathrm{d}t+\int_{\frac{a+b}{2}}^{b}f^{\prime\prime}(t)(b-t)\mathrm{d}t,$$
>
> 两边乘 $\frac{b-a}{2}$:
>
> $$\begin{aligned}\frac{b-a}{2}\left[f(a)+f(b)\right]&=(b-a)f\bigg(\frac{a+b}{2}\bigg)+\frac{b-a}{2}\int_{a}^{\frac{a+b}{2}}f^{\prime\prime}(t)(t-a)\mathrm{d}t\\&\quad+\frac{b-a}{2}\int_{\frac{a+b}{2}}^{b}f^{\prime\prime}(t)(b-t)\mathrm{d}t.\quad(2)\end{aligned}$$
>
> (3) 两式相减，两段权函数合而为一。用 (1) 减 (2):
>
> $$\begin{aligned}\int_{a}^{b}f(x)\mathrm{d}x-\frac{b-a}{2}\left[f(a)+f(b)\right]\\=\int_{a}^{\frac{a+b}{2}}f^{\prime\prime}(t)\left[\frac{1}{2}(t-a)^{2}-\frac{b-a}{2}(t-a)\right]\mathrm{d}t\\+\int_{\frac{a+b}{2}}^{b}f^{\prime\prime}(t)\left[\frac{1}{2}(b-t)^{2}-\frac{b-a}{2}(b-t)\right]\mathrm{d}t.\end{aligned}$$
>
> 而两段方括号里的函数其实是同一个：
>
> $$\frac{1}{2}(t-a)^{2}-\frac{b-a}{2}(t-a)=-\frac{(t-a)(b-t)}{2}\qquad\left(a\leqslant t\leqslant\frac{a+b}{2}\right),$$
>
> $$\frac{1}{2}(b-t)^{2}-\frac{b-a}{2}(b-t)=-\frac{(t-a)(b-t)}{2}\qquad\left(\frac{a+b}{2}\leqslant t\leqslant b\right),$$
>
> 所以
>
> $$\int_{a}^{b}f(x)\mathrm{d}x-\frac{b-a}{2}\left[f(a)+f(b)\right]=-\frac{1}{2}\int_{a}^{b}(t-a)(b-t)f^{\prime\prime}(t)\mathrm{d}t.$$
>
> 右边的不变号权函数 $-\frac{(t-a)(b-t)}{2}$ 在 $[a,b]$ 上恒不为正，由第一积分中值定理，存在 $\xi \in (a,b)$，使
>
> $$\begin{aligned}-\frac{1}{2}\int_{a}^{b}(t-a)(b-t)f^{\prime\prime}(t)\mathrm{d}t&=-\frac{1}{2}f^{\prime\prime}(\xi)\int_{a}^{b}(t-a)(b-t)\mathrm{d}t\\&=-\frac{1}{2}f^{\prime\prime}(\xi)\cdot\frac{(b-a)^{3}}{6}=-\frac{1}{12}f^{\prime\prime}(\xi)(b-a)^{3},\end{aligned}$$
>
> 故
>
> $$\int_{a}^{b}f(x)\mathrm{d}x=\frac{1}{2}\left[f(a)+f(b)\right](b-a)-\frac{1}{12}f^{\prime\prime}(\xi)(b-a)^{3}.$$
>
> 注. 解二的两个关键动作: 一是把 $f(a)$、 $f(b)$ 也在 $x = \frac{a+b}{2}$ 处展开再相加, 这样 $f\left(\frac{a+b}{2}\right)$ 才与端点信息 $\frac{b-a}{2}[f(a) + f(b)]$ 对上 (相加后一次项恰好抵消); 二是两段的权函数最后合并成同一个 $-\frac{(t-a)(b-t)}{2}$——它既不变号, 积分又恰好等于 $-\frac{(b-a)^3}{12}$, 这正是结论中 $\frac{1}{12}$ 的来源. (解二的积分中值定理用到了 $f''(x)$ 的连续性; 若只设“有二阶导数”, 用达布介值性代替亦可.)

**3.** (难度:★★) 设函数 $f(x)$, $g(x)$ 在区间 $[a, b]$ 上连续, 且 $f(x)$ 单调增加, $0 \leq g(x) \leq 1$, 证明:

(1)

$$0\leqslant\int_{a}^{x}g(t)\mathrm{d}t\leqslant x-a,x\in[a,b];$$

(2)

$$\int_{a}^{a+}\int_{a}^{b}g(t)\mathrm{d}t_{f(x)}\mathrm{d}x\leqslant\int_{a}^{b}f(x)g(x)\mathrm{d}x.$$

> [!answer]- 原书参考答案（D.0.2 第 3 题，未逐题独立验算）
> **3.** (1) 由 $0 \leqslant g(x) \leqslant 1$ 直接积分放缩; (2) 把待证不等式两边之差设成变限积分函数 $F(x)$，用 $f(x)$ 的单调性判断 $F'(x)$ 的符号. (1) 由 $g(x) \geqslant 0$，当 $x \geqslant a$ 时 $\int_{a}^{x} g(t) \, dt \geqslant 0$; 又 $g(x) \leqslant 1$，故
>
> $$\int_{a}^{x}g(t)\mathrm{d}t\leqslant\int_{a}^{x}1\mathrm{d}t=x-a.$$
>
> 所以 $0 \leqslant \int_{a}^{x} g(t) \, dt \leqslant x - a$.
>
> (2) 设
>
> $$F(x)=\int_{a}^{a+}\int_{a}^{x}g(t)\mathrm{d}t\\f(u)\mathrm{d}u-\int_{a}^{x}f(u)g(u)\mathrm{d}u,\qquad F(a)=0.$$
>
> 求导（外层的积分上限 $a + \int_{a}^{x} g(t) \, dt$ 也是 x 的函数，要用复合函数求导）：
>
> $$\begin{aligned}F^{\prime}(x)&=g(x)f\bigg(a+\int_{a}^{x}g(t)\mathrm{d}t\bigg)-f(x)g(x)\\&=g(x)\left[f\bigg(a+\int_{a}^{x}g(t)\mathrm{d}t\bigg)-f(x)\right].\end{aligned}$$
>
> 由(1)知 $a+\int_{a}^{x}g(t)dt\leqslant x$; 又 $f(x)$单调增加,故
>
> $$f\bigg(a+\int_{a}^{x}g(t)\mathrm{d}t\bigg)\leqslant f(x),$$
>
> 结合 $g(x) \geqslant 0$ 得 $F'(x) \leqslant 0$，即 $F(x)$ 在 $[a,b]$ 上单调递减。于是对一切 $x \in [a,b]$，
>
> $$\int_{a}^{a+}\int_{a}^{x}g(t)\mathrm{d}t_{f(u)}\mathrm{d}u\leqslant\int_{a}^{x}f(u)g(u)\mathrm{d}u.$$
>
> 取 x = b 即得结论. 把 $a + \int_{a}^{x} g(t) \, dt$ 看成中间变量是本题的关键: 它既可以代入 $f(x)$, 又可以用 (1) 的结论与 x 比较大小, 从而给 $F'(x)$ 定号.

**4.** (难度:★★) 设函数 $f(x)$ 在区间 $[0,1]$ 上可导, $f(0)=0$, 且当 $x\in(0,1)$ 时, $0<f'(x)<1$. 试证: 当 $a\in(0,1)$ 时,

$$\left(\int_{0}^{a}f(x)\mathrm{d}x\right)^{2}>\int_{0}^{a}f^{3}(x)\mathrm{d}x.$$

> [!answer]- 原书参考答案（D.0.2 第 4 题，未逐题独立验算）
> **4.** 第一步：把待证不等式设成函数.令
>
> $$F(x)=\left(\int_{0}^{x}f(t)\mathrm{d}t\right)^{2}-\int_{0}^{x}f^{3}(t)\mathrm{d}t,\qquad x\in[0,1],$$
>
> 则 $F(0)=0$，只要证明当 $x\in(0,1)$ 时 $F(x)>0$。
>
> 第二步: 求导, 把问题化为 $f(x)$ 与 $\int_{0}^{x} f(t) \, dt$ 的关系.
>
> $$F^{\prime}(x)=2f(x)\int_{0}^{x}f(t)\mathrm{d}t-f^{3}(x)=f(x)\left[2\int_{0}^{x}f(t)\mathrm{d}t-f^{2}(x)\right].$$
>
> 第三步：先说明 $f(x) > 0$ 。由 $f(0) = 0$ 且 $f'(x) > 0, f(x)$ 在 $[0,1]$ 上单调递增，故当 $x \in (0,1)$ 时 $f(x) > f(0) = 0$ 。
>
> 第四步：再说明方括号恒正.令
>
> $$g(x)=2\int_{0}^{x}f(t)\mathrm{d}t-f^{2}(x),$$
>
> 则 $g(0)=0$ ，且
>
> $$g^{\prime}(x)=2f(x)-2f(x)f^{\prime}(x)=2f(x)\left[1-f^{\prime}(x)\right]>0\quad(x\in(0,1)),$$
>
> 最后一步用了 $f(x) > 0$ 与 0 < $f'(x) < 1$ 。故 $g(x)$ 在 $[0,1]$ 上单调递增， $g(x) > g(0) = 0$ 。
>
> 第五步: 合成. 由 $f(x) > 0$, $g(x) > 0$ 得 $F'(x) > 0$, 故 $F(x)$ 在 $[0,1]$ 上单调递增. 对任意 $a \in (0,1)$, 有 $F(a) > F(0) = 0$, 即
>
> $$\left(\int_{0}^{a}f(x)\mathrm{d}x\right)^{2}>\int_{0}^{a}f^{3}(x)\mathrm{d}x.$$

**5.** （难度：★★★）设函数 $f(x)$ 在 $[0,1]$ 上连续，且

$$\int_{0}^{1}f(x)\mathrm{d}x=0,\quad\int_{0}^{1}x f(x)\mathrm{d}x=1,$$

试证：

(1) 存在 $x_0 \in [0,1]$，使得 $|f(x_0)| > 4$;

(2) 存在 $x_1 \in [0,1]$，使得 $|f(x_1)| = 4$.

> [!answer]- 原书参考答案（D.0.2 第 5 题，未逐题独立验算）
> **5.** 第一步：把两个积分条件升级为原函数的凹凸性条件. 令
>
> $$F(x)=\int_{0}^{x}f(t)\mathrm{d}t,\qquad G(x)=\int_{0}^{x}F(t)\mathrm{d}t.$$
>
> 由 $\int_{0}^{1}f(x)dx=0$ 得 $F(0)=F(1)=0$ ，且 $G(0)=0, G'(x)=F(x), G''(x)=f(x)$
>
> 再处理第二个条件：
>
> $$\int_{0}^{1}x f(x)\mathrm{d}x=\left.\int_{0}^{1}x\mathrm{d}F(x)=x F(x)\right|_{0}^{1}-\left.\int_{0}^{1}F(x)\mathrm{d}x=0-G(1)=1,\right.$$
>
> 故 $G(1) = -1$.
>
> (1) 反证: 先假设 $|f(x)| \leq 4$, 用凹凸性把 $G(x)$ 夹住. 假设对一切 $x \in [0,1]$ 有 $|f(x)| \leq 4$, 即 $-4 \leq G''(x) \leq 4$.
>
> 令 $h_{1}(x) = G(x) + 2x^{2}$. 则 $h_{1}^{\prime\prime}(x) = G^{\prime\prime}(x) + 4 \geqslant 0$, $h_{1}^{\prime}$ 单调递增; 又 $h_{1}^{\prime}(0) = G^{\prime}(0) = F(0) = 0$, 故 $h_{1}^{\prime}(x) \geqslant 0$, $h_{1}$ 单调递增, 于是
>
> $$h_{1}(x)\geqslant h_{1}(0)=G(0)=0\quad\Longrightarrow\quad G(x)\geqslant-2x^{2}.$$
>
> 令 $h_2(x) = G(x) - 2x^2 + 4x - 1$. 则 $h_2''(x) = G''(x) - 4 \leq 0$, $h_2'$ 单调递减；又 $h_2'(1) = G'(1) - 4 + 4 = F(1) = 0$, 故当 $x \leq 1$ 时 $h_2'(x) \geq h_2'(1) = 0$, $h_2$ 单调递增，于是
>
> $$\begin{aligned}h_{2}(x)&\leqslant h_{2}(1)=G(1)-2+4-1=-1-2+4-1=0\\&\Longrightarrow G(x)\leqslant2x^{2}-4x+1.\end{aligned}$$
>
> 取 $x = \frac{1}{2}$：由上式两端同时给出
>
> $$-\frac{1}{2}\leqslant G\left(\frac{1}{2}\right)\leqslant\frac{1}{2}-2+1=-\frac{1}{2},\qquad 故 \qquad G\left(\frac{1}{2}\right)=-\frac{1}{2}.$$
>
> 又 $h_1\left(\frac{1}{2}\right) = G\left(\frac{1}{2}\right) + \frac{1}{2} = 0$，而 $h_1 \geq 0$ 且 $h_1$ 单调递增，所以 $h_1 \equiv 0$，即 $G(x) = -2x^2$， $x \in \left[0, \frac{1}{2}\right]$。
>
> 同理 $h_2\left(\frac{1}{2}\right) = G\left(\frac{1}{2}\right) - 2 \cdot \frac{1}{4} + 4 \cdot \frac{1}{2} - 1 = -\frac{1}{2} - \frac{1}{2} + 2 - 1 = 0$，而 $h_2 \leq 0$ 且 $h_2$ 单调递增，所以 $h_2 \equiv 0$，即 $G(x) = 2x^2 - 4x + 1$， $x \in \left[\frac{1}{2}, 1\right]$。
>
> 于是 $G''(x) = -4 (0 < x < \frac{1}{2})$， $G''(x) = 4 (\frac{1}{2} < x < 1)$。但 $G''(x) = f(x)$ 在 $[0,1]$ 上连续， $G''(\frac{1}{2})$ 不可能同时等于 -4 与 4，矛盾。故存在 $x_0 \in [0,1]$，使 $|f(x_0)| > 4$。
>
> (2) 用介值性把 $|f(x)|$ 从 0 拉到 4。记 $M = \max_{0 \leq x \leq 1} |f(x)|$，由 (1) 知 $M \geq |f(x_0)| > 4$。又由积分中值定理，存在 $x_2 \in (0,1)$ 使 $f(x_2) = \int_0^1 f(x) \, dx = 0$，于是 $\min_{0 \leq x \leq 1} |f(x)| = 0$。因 $|f(x)|$ 在 $[0,1]$ 上连续，而 $0 < 4 < M$，由介值定理，存在 $x_1 \in [0,1]$ 使 $|f(x_1)| = 4$。

**6.** (难度：★★★) 设函数 $f(x)$ 在区间 [0,1] 上具有连续导数, 且满足

$$\int_{0}^{1}f(x)\mathrm{d}x=\frac{5}{2},\qquad\int_{0}^{1}x f(x)\mathrm{d}x=\frac{3}{2}.$$

证明: 存在 $\xi \in (0,1)$, 使得 $f'(\xi) = 3$.

> [!answer]- 原书参考答案（D.0.2 第 6 题，未逐题独立验算）
> **6.** 第一步: 把两个积分条件升级为原函数的高阶导数条件. 令
>
> $$F(x)=\int_{0}^{x}f(t)\mathrm{d}t,\qquad h(x)=\int_{0}^{x}F(t)\mathrm{d}t.$$
>
> 于是 $F(0)=0$、 $F(1)=\frac{5}{2}$、 $F'(x)=f(x)$; $h(0)=0$、 $h'(x)=F(x)$、 $h''(x)=f(x)$、 $h'''(x)=f'(x)$.
>
> 对第二个条件作分部积分：
>
> $$\int_{0}^{1}x f(x)\mathrm{d}x=\left.\int_{0}^{1}x\mathrm{d}F(x)=x F(x)\right|_{0}^{1}-\left.\int_{0}^{1}F(x)\mathrm{d}x=\frac{5}{2}-h(1),\right.$$
>
> 结合 $\int_{0}^{1}xf(x)\mathrm{d}x=\frac{3}{2}$ 得
>
> $$h(1)=1,\qquad h^{\prime}(0)=F(0)=0,\qquad h^{\prime}(1)=F(1)=\frac{5}{2}.$$
>
> 要证的结论 $f'(\xi)=3$ 即 $h'''(\xi)-3=0$.
>
> 第二步：作辅助多项式，把端点条件凑齐.设辅助多项式为
>
> $$P(x)=h(x)-ax^{3}-bx^{2},$$
>
> 其中a,b待定.目标是让P在两端点处的值与一阶导数值都为零,即 $P(0)=P(1)=0$、 $P'(0)=P'(1)=0$.逐条代入 $(P'(x)=h'(x)-3ax^{2}-2bx)$:
>
> $$P(0)=h(0)=0,\qquad P^{\prime}(0)=h^{\prime}(0)=0$$
>
> 自动满足：余下两条给出
>
> $$\left\{\begin{aligned}&P(1)=1-a-b=0,\\ &P^{\prime}(1)=\frac{5}{2}-3a-2b=0.\end{aligned}\right.$$
>
> 解得 $a=\frac{1}{2}$、 $b=\frac{1}{2}$. 故
>
> $$P(x)=h(x)-\frac{1}{2}x^{3}-\frac{1}{2}x^{2},\qquad P(0)=P(1)=0,\quad P^{\prime}(0)=P^{\prime}(1)=0.$$
>
> 第三步：连续用罗尔定理，把零点逐阶下传。由 $P(0)=P(1)=0$，存在 $c_{1}\in(0,1)$ 使 $P'(c_{1})=0$。于是 $P'$ 在 $0,c_{1},1$ 三点取值都为零：在 $[0,c_{1}]$ 与 $[c_{1},1]$ 上分别用罗尔定理，存在 $c_{2}\in(0,c_{1})$、 $c_{3}\in(c_{1},1)$，使
>
> $$P^{\prime\prime}(c_{2})=0,\qquad P^{\prime\prime}(c_{3})=0.$$
>
> 再对 $P''$ 在 $[c_2, c_3]$ 上用罗尔定理，存在 $\xi \in (c_2, c_3) \subset (0, 1)$，使 $P'''(\xi) = 0$。而
>
> $$P^{\prime\prime\prime}(x)=h^{\prime\prime\prime}(x)-3=f^{\prime}(x)-3,$$
>
> 故 $f^{\prime}(\xi)=3$

**7.** (难度：★★★) 设 $f(x)$ 是 $[0,1]$ 上的单调递减的正值连续函数, 证明:

$$\frac{\int_{0}^{1}xf^{2}(x)d x}{\int_{0}^{1}xf(x)d x}\leqslant\frac{\int_{0}^{1}f^{2}(x)d x}{\int_{0}^{1}f(x)d x}.$$

> [!answer]- 原书参考答案（D.0.2 第 7 题，未逐题独立验算）
> **7.** 两个分母都为正 $(f(x) > 0, x \geqslant 0)$，故原不等式等价于
>
> $$\int_{0}^{1}x f^{2}(x)\mathrm{d}x\int_{0}^{1}f(x)\mathrm{d}x\leqslant\int_{0}^{1}f^{2}(x)\mathrm{d}x\int_{0}^{1}x f(x)\mathrm{d}x.$$
>
> 把上限1换成变量x，令
>
> $$F(x)=\int_{0}^{x}f^{2}(t)\mathrm{d}t\int_{0}^{x}t f(t)\mathrm{d}t-\int_{0}^{x}t f^{2}(t)\mathrm{d}t\int_{0}^{x}f(t)\mathrm{d}t,$$
>
> 则 $F(0) = 0$.
>
> 关键点: $f(x)$ 只有连续性, 不能对它求导; 只能对变限积分求导. 由变限积分求导与乘积法则,
>
> $$\begin{aligned}F^{\prime}(x)&=f^{2}(x)\int_{0}^{x}tf(t)\mathrm{d}t+xf(x)\int_{0}^{x}f^{2}(t)\mathrm{d}t\\&\quad-xf^{2}(x)\int_{0}^{x}f(t)\mathrm{d}t-f(x)\int_{0}^{x}tf^{2}(t)\mathrm{d}t\\&=f(x)\left[f(x)\int_{0}^{x}(t-x)f(t)\mathrm{d}t+\int_{0}^{x}(x-t)f^{2}(t)\mathrm{d}t\right]\\&=f(x)\int_{0}^{x}(x-t)\left[f(t)-f(x)\right]f(t)\mathrm{d}t.\end{aligned}$$
>
> (先把第一、二项合并、第三、四项合并,各自提出公因子 $f(x)$,再用 $(t-x)f(x)+(x-t)f(t)=(x-t)[f(t)-f(x)]$,即得最后一行.)
>
> 在 $0 \leqslant t \leqslant x \leqslant 1$ 上， $f(x)$ 单调递减给出 $f(t) \geqslant f(x)$，又 $x-t\geqslant0$、 $f(t) > 0$、 $f(x) > 0$，故被积式非负， $F'(x) \geqslant 0$，即 $F(x)$ 在 $[0,1]$ 上单调递增。于是
>
> $$F(1)\geqslant F(0)=0,$$
>
> 这正是所要证的不等式. 全过程只对变限积分求导, 没有用到 $f(x)$ 的可导性.

## 3.3 牛莱公式

一元积分学中证明题的底层逻辑，将函数之差变为对应积分，再根据积分性质进行放缩或计算。当之无愧，最夯定理，借助牛莱公式就足以解决各类压轴难题。

**1.** (难度: ★★★) 设 $f(x)$ 在 $[a, b]$ 上有连续的导数, 且 $f(a) = 0$. 求证:

$$\int_{a}^{b}f^{2}(x)\mathrm{d}x\leqslant\frac{(b-a)^{2}}{2}\int_{a}^{b}[f^{\prime}(x)]^{2}\mathrm{d}x.$$

> [!answer]- 原书参考答案（D.0.3 第 1 题，未逐题独立验算）
> **1.** 第一步: 用零点把 $f(x)$ 写成导数的积分. 由 $f(a)=0$, 对 $x\in[a,b]$,
>
> $$\left|f(x)\right|=\left|f(x)-f(a)\right|=\left|\int_{a}^{x}f^{\prime}(t)\mathrm{d}t\right|\leqslant\int_{a}^{x}\left|f^{\prime}(t)\right|\mathrm{d}t.$$
>
> 第二步：平方后用柯西-施瓦兹不等式.
>
> $$\begin{aligned}f^{2}(x)=|f(x)|^{2}&\leqslant\left(\int_{a}^{x}\left|f^{\prime}(t)\right|\mathrm{d}t\right)^{2}\\&\leqslant\left(\int_{a}^{x}1^{2}\mathrm{d}t\right)\left(\int_{a}^{x}\left|f^{\prime}(t)\right|^{2}\mathrm{d}t\right)=(x-a)\int_{a}^{x}\left|f^{\prime}(t)\right|^{2}\mathrm{d}t.\end{aligned}$$
>
> 再放大积分上限, 把它整体换成 $[a, b]$ 上的积分:
>
> $$f^{2}(x)\leqslant(x-a)\int_{a}^{b}\left|f^{\prime}(t)\right|^{2}\mathrm{d}t.$$
>
> 第三步：对 x 积分. 上式两端在 $[a,b]$ 上对 x 积分，右边提出与 x 无关的积分：
>
> $$\int_{a}^{b}f^{2}(x)\mathrm{d}x\leqslant\int_{a}^{b}(x-a)\mathrm{d}x\int_{a}^{b}\left|f^{\prime}(t)\right|^{2}\mathrm{d}t=\frac{(b-a)^{2}}{2}\int_{a}^{b}\left|f^{\prime}(t)\right|^{2}\mathrm{d}t.$$
>
> （这里 $\int_{a}^{b}(x-a)dx=\frac{(b-a)^{2}}{2}$ ）把右端的哑变量 t 换回 x 即得结论.

**2.** (难度:★★★) 设函数 $f(x)$ 在 $[a,b]$ 上有连续的导数, $A = \frac{1}{b-a} \int_{a}^{b} f(x) \, dx$. 试证明:

$$\int_{a}^{b}[f(x)-A]^{2}\mathrm{d}x\leqslant\frac{(b-a)^{2}}{2}\int_{a}^{b}[f^{\prime}(x)]^{2}\mathrm{d}x.$$

> [!answer]- 原书参考答案（D.0.3 第 2 题，未逐题独立验算）
> **2.** 先找一个点 $x_{0}$ 使 $f(x_{0}) = A$ (积分中值定理)，把 A 换成函数值，再按 x 落在 $x_{0}$ 左侧还是右侧分别用牛顿-莱布尼茨公式与柯西-施瓦兹. 由积分中值定理，存在 $x_{0} \in (a, b)$，使
>
> $$A=\frac{1}{b-a}\int_{a}^{b}f(x)\mathrm{d}x=f(x_{0}).$$
>
> 当 $a<x\leq x_0$ 时：
>
> $$|f(x)-A|=|f(x_{0})-f(x)|=\left|\int_{x}^{x_{0}}f^{\prime}(t)\mathrm{d}t\right|\leqslant\int_{x}^{x_{0}}\left|f^{\prime}(t)\right|\mathrm{d}t,$$
>
> 平方并用柯西-施瓦兹：
>
> $$|f(x)-A|^{2}\leqslant(x_{0}-x)\int_{x}^{x_{0}}\left|f^{\prime}(t)\right|^{2}\mathrm{d}t\leqslant(x_{0}-x)\int_{a}^{b}\left|f^{\prime}(t)\right|^{2}\mathrm{d}t.$$
>
> 当 $x_{0}<x<b$时：同理
>
> $$|f(x)-A|^{2}\leqslant(x-x_{0})\int_{x_{0}}^{x}\left|f^{\prime}(t)\right|^{2}\mathrm{d}t\leqslant(x-x_{0})\int_{a}^{b}\left|f^{\prime}(t)\right|^{2}\mathrm{d}t.$$
>
> 于是
>
> $$\int_{a}^{b}\left|f(x)-A\right|^{2}\mathrm{d}x\leqslant\left[\int_{a}^{x_{0}}(x_{0}-x)\mathrm{d}x+\int_{x_{0}}^{b}(x-x_{0})\mathrm{d}x\right]\int_{a}^{b}\left|f^{\prime}(t)\right|^{2}\mathrm{d}t.$$
>
> 而两个积分之和
>
> $$\begin{aligned}&\int_{a}^{x_{0}}(x_{0}-x)\mathrm{d}x+\int_{x_{0}}^{b}(x-x_{0})\mathrm{d}x\\&\quad=\frac{(x_{0}-a)^{2}}{2}+\frac{(b-x_{0})^{2}}{2}\\=&\frac{(b-a)^{2}}{4}+\left(x_{0}-\frac{a+b}{2}\right)^{2}\leqslant\frac{(b-a)^{2}}{2},\end{aligned}$$
>
> 最后一步因为 $\left(x_{0}-\frac{a+b}{2}\right)^{2}\leqslant\frac{(b-a)^{2}}{4}$. 故
>
> $$\int_{a}^{b}\left|f(x)-A\right|^{2}\mathrm{d}x\leqslant\frac{(b-a)^{2}}{2}\int_{a}^{b}\left|f^{\prime}(x)\right|^{2}\mathrm{d}x.$$
>
> 把两个平方项配方： $\frac{(x_0-a)^2}{2}+\frac{(b-x_0)^2}{2}=\frac{(b-a)^2}{4}+\left(x_0-\frac{a+b}{2}\right)^2$。因为 $x_0\in(a,b)$，它严格小于 $\frac{(b-a)^2}{2}$，所以结论中的 $\leq$ 有余量。

**3.** (难度：★★★★) 若函数 $f(x)$ 在 $[0,a]$ 上导函数连续且 $f(0)=0$ 证明:

$$\int_{0}^{a}\left|f(x)f^{\prime}(x)\right|\mathrm{d}x\leqslant\frac{a}{2}\int_{0}^{a}[f^{\prime}(x)]^{2}\mathrm{d}x.$$

> [!answer]- 原书参考答案（D.0.3 第 3 题，未逐题独立验算）
> **3.** $f(0)=0$ 给出 $f(x)=\int_{0}^{x}f'(t)dt;$ 把 $\left|f(x)\right|$ 换成 $\int_{0}^{x}\left|f'(t)\right|$ dt 之后出现 $\left(\int_{0}^{x}\left|f'(t)\right|\mathrm{d}t\right)\left|f'(x)\right|$ 的结构, 它正好是 $\frac{1}{2}\left(\int_{0}^{x}\left|f'(t)\right|\mathrm{d}t\right)^{2}$ 的导数, 可以凑微分. 由 $f(0)=0$ 与牛顿-莱布尼茨公式, $f(x)=\int_{0}^{x}f'(t)\mathrm{d}t$, 于是
>
> $$\left|f(x)f^{\prime}(x)\right|=\left|\int_{0}^{x}f^{\prime}(t)\mathrm{d}t\right|\cdot\left|f^{\prime}(x)\right|\leqslant\left(\int_{0}^{x}\left|f^{\prime}(t)\right|\mathrm{d}t\right)\left|f^{\prime}(x)\right|.$$
>
> 令
>
> $$F(x)=\int_{0}^{x}\left|f^{\prime}(t)\right|\mathrm{d}t,\qquad F^{\prime}(x)=\left|f^{\prime}(x)\right|,$$
>
> 则
>
> $$\begin{aligned}\int_{0}^{a}\left|f(x)f^{\prime}(x)\right|\mathrm{d}x\\\leqslant\int_{0}^{a}F(x)F^{\prime}(x)\mathrm{d}x=\int_{0}^{a}F(x)\mathrm{d}F(x)\\=\frac{1}{2}F^{2}(x)\Big|_{0}^{a}=\frac{1}{2}\left[F(a)\right]^{2}.\end{aligned}$$
>
> 再由柯西-施瓦兹不等式，
>
> $$\begin{aligned}\frac{1}{2}\left[F(a)\right]^{2}&=\frac{1}{2}\left(\int_{0}^{a}\left|f^{\prime}(t)\right|\mathrm{d}t\right)^{2}\\\leqslant\frac{1}{2}\left(\int_{0}^{a}1^{2}\mathrm{d}t\right)&\left(\int_{0}^{a}\left|f^{\prime}(t)\right|^{2}\mathrm{d}t\right)\\&=\frac{a}{2}\int_{0}^{a}\left|f^{\prime}(t)\right|^{2}\mathrm{d}t.\end{aligned}$$
>
> 故 $\int_{0}^{a}\left|f(x)f'(x)\right|\mathrm{d}x\leqslant\frac{a}{2}\int_{0}^{a}\left|f'(x)\right|^{2}\mathrm{d}x.$. 看到 $f(x)f'(x)$ 就凑 $f(x)\mathrm{d}f(x)$: 带绝对值时先用 $\left|\int_{0}^{x}f'(t)\mathrm{d}t\right|\leqslant\int_{0}^{x}\left|f'(t)\right|\mathrm{d}t$ 把 $\left|f(x)\right|$ 换成 $F(x)$, 再对 $F(x)F'(x)$ 凑微分; 最后一步才对 $F(a)$ 用柯西-施瓦兹. 两处用法不同, 不要混.

**4.** (难度:★★★) 在 $[0,2]$ 上有连续导数的函数 $f(x)$，满足 $f(0) = f(2) = 0$，并设 $M = \max\{|f(x)|\}$， $x \in [0,2]$，由此完成下列证明：

(1) 存在 $\zeta \in (0,2)$，使得 $\left|f'(\zeta)\right| \geqslant M$.

(2) 若 $\forall x \in (0,2), |f'(x)| \leqslant M$, 则 M = 0.

> [!answer]- 原书参考答案（D.0.3 第 4 题，未逐题独立验算）
> **4.** (1) 用拉格朗日中值定理, 按最大值点的位置分段. 因 $|f(x)|$ 在 $[0,2]$ 上连续, 存在 $c \in [0,2]$ 使 $|f(c)| = M$. 若 c = 0 或 2, 则 M = 0, 结论显然; 下面设 $c \in (0,2)$, 此时 $f(x)$ 在 c 处取到内部极值, 且
>
> $$\left|f^{\prime}(\xi_{1})\right|=\left|\frac{f(c)-f(0)}{c-0}\right|=\frac{M}{c},\qquad\xi_{1}\in(0,c),$$
>
> $$\left|f^{\prime}(\xi_{2})\right|=\left|\frac{f(c)-f(2)}{c-2}\right|=\frac{M}{2-c},\qquad\xi_{2}\in(c,2).$$
>
> 若 $c \leqslant 1$，则 $\frac{M}{c} \geqslant M$，取 $\zeta = \xi_1$ 即得 $|f'(\zeta)| \geqslant M$；若 $c > 1$，则 2 - c < 1， $\frac{M}{2 - c} > M$，取 $\zeta = \xi_2$ 同样有 $|f'(\zeta)| \geqslant M$。
>
> (2) 反证: 设 M > 0, 用牛莱公式把 M 与 c 夹出来. 设 M > 0, 并设 $|f(c)| = M$.
>
> 若 c=0 或 2，则 $M=\left|f(c)\right|=0$，与 M>0 矛盾，故 $c\in(0,2)$。由 $f(0)=0$ 与牛莱公式，
>
> $$M=\left|f(c)\right|=\left|\int_{0}^{c}f^{\prime}(t)\mathrm{d}t\right|\leqslant\int_{0}^{c}\left|f^{\prime}(t)\right|\mathrm{d}t\leqslant\int_{0}^{c}M\mathrm{d}t=Mc,$$
>
> 又由 $f(2)=0$
>
> $$M=\left|f(2)-f(c)\right|=\left|\int_{c}^{2}f^{\prime}(t)\mathrm{d}t\right|\leqslant\int_{c}^{2}\left|f^{\prime}(t)\right|\mathrm{d}t\leqslant\int_{c}^{2}M\mathrm{d}t=M(2-c).$$
>
> 因 $M > 0$，由 $M \leqslant Mc$ 得 $c \geqslant 1$，由 $M \leqslant M(2 - c)$ 得 $2 - c \geqslant 1$，即 $c \leqslant 1$，故 c = 1，且上面两个不等式链的全部不等号都取等号。
>
> 取等号说明 $\int_{0}^{1}\left(M-\left|f'(t)\right|\right)\,\mathrm{d}t=0$; 被积函数 $M-\left|f'(t)\right|\geq0$ 且连续, 故在 $[0,1]$ 上恒为零, 即 $\left|f'(t)\right|=M$ ( $0\leq t\leq1$). 同理 $\left|f'(t)\right|=M$ ( $1\leq t\leq2$). 由于 $f'(x)$ 连续、在每段上不为零, $f'(x)$ 在 $[0,1]$ 上不变号, 而 $f(0)=0$, $\left|f(1)\right|=M$, 故不妨设 $f(1)=M>0$, 于是
>
> $$f(x)=Mx\ (0\leqslant x\leqslant1),\qquad f(x)=M(2-x)\ (1\leqslant x\leqslant2).$$
>
> 但此时 $f'(1^{-}) = M$、 $f'(1^{+}) = -M$， $f(x)$ 在 x = 1 处不可导，与 $f(x)$ 在 $[0,2]$ 上有连续导数矛盾。故假设不成立，M = 0。

**5.** (难度：★★★★★) 定义在 $[0,1]$ 上的可导函数 $f(x)$，有

$$\left|\int_{0}^{1}f(x)\mathrm{d}x\right|<\int_{0}^{1}\left|f(x)\right|\mathrm{d}x.$$

(1) 求证: $f(x)$ 在 $(0,1)$ 上必有零点;

(2) 设 $f(x)$ 在 $(0,1)$ 上的一个零点为 $x_0$，据此探究 $\int_0^1 |f(x)|\,\mathrm{d}x$ 与 $\int_0^1 (1 - |x - x_0|)|f'(x)|\,\mathrm{d}x$ 的大小关系.

> [!answer]- 原书参考答案（D.0.3 第 5 题，未逐题独立验算）
> **5.** (1) 若 $f(x)$ 在 $(0,1)$ 上无零点，则 $f(x)$ 恒正或恒负，此时 $\left|\int_{0}^{1}f(x)dx\right|=\int_{0}^{1}|f(x)|dx$，与条件矛盾. (2) 以 $x_{0}$ 为零点把 $[0,1]$ 分成两段，各用牛莱公式放缩，再把两个累次积分换序，最后合成权重 $1-|x-x_{0}|$. (1) 反证. 若 $f(x)$ 在 $(0,1)$ 上无零点，由 $f(x)$ 连续， $(0,1)$ 上恒有 $f(x)>0$ 或恒有 $f(x)<0$，从而 $\left|\int_{0}^{1}f(x)dx\right|=\int_{0}^{1}|f(x)|dx$，与条件矛盾. 故 $f(x)$ 在 $(0,1)$ 上必有零点.
>
> (2) 设 $f(x_0) = 0, x_0 \in (0,1)$. 分段估计:
>
> $$\begin{aligned}0<x\leqslant x_{0}:\quad&|f(x)|=\\ |f(x_{0})-f(x)|=\left|\int_{x}^{x_{0}}f^{\prime}(t)\mathrm{d}t\right|\\ \leqslant\int_{x}^{x_{0}}\left|f^{\prime}(t)\right|\mathrm{d}t&\leqslant\int_{x}^{1}\left|f^{\prime}(t)\right|\mathrm{d}t;\end{aligned}$$
>
> $$\begin{aligned}x_0<x<1:\quad |f(x)|&=|f(x)-f(x_0)|=\left|\int_{x_0}^{x}f^{\prime}(t)\mathrm{d}t\right|\\&\leqslant\int_{x_0}^{x}|f^{\prime}(t)|\mathrm{d}t\leqslant\int_0^x|f^{\prime}(t)|\mathrm{d}t.\end{aligned}$$
>
> 于是
>
> $$\int_{0}^{1}\left|f(x)\right|\mathrm{d}x\leqslant\int_{0}^{x_{0}}\mathrm{d}x\int_{x}^{1}\left|f^{\prime}(t)\right|\mathrm{d}t+\int_{x_{0}}^{1}\mathrm{d}x\int_{0}^{x}\left|f^{\prime}(t)\right|\mathrm{d}t.$$
>
> 把两个累次积分换序 (第一个在区域 $0 \leq x \leq x_0$, $x \leq t \leq 1$ 上, 第二个在 $x_0 \leq x \leq 1$, $0 \leq t \leq x$ 上):
>
> $$\int_{0}^{x_{0}}\mathrm{d}x\int_{x}^{1}\left|f^{\prime}(t)\right|\mathrm{d}t=\int_{0}^{x_{0}}t\left|f^{\prime}(t)\right|\mathrm{d}t+\int_{x_{0}}^{1}x_{0}\left|f^{\prime}(t)\right|\mathrm{d}t,$$
>
> $$\int_{x_{0}}^{1}\mathrm{d}x\int_{0}^{x}\left|f^{\prime}(t)\right|\mathrm{d}t=\int_{0}^{x_{0}}(1-x_{0})\left|f^{\prime}(t)\right|\mathrm{d}t+\int_{x_{0}}^{1}(1-t)\left|f^{\prime}(t)\right|\mathrm{d}t.$$
>
> 两式相加，
>
> $$\int_{0}^{1}\left|f(x)\right|\mathrm{d}x\leqslant\int_{0}^{x_{0}}(1+t-x_{0})\left|f^{\prime}(t)\right|\mathrm{d}t+\int_{x_{0}}^{1}(1+x_{0}-t)\left|f^{\prime}(t)\right|\mathrm{d}t.$$
>
> 而在 $[0,x_{0}]$ 上 $1+t-x_{0}=1-|t-x_{0}|$，在 $[x_{0},1]$ 上 $1+x_{0}-t=1-|t-x_{0}|$，故
>
> $$\int_{0}^{1}\left|f(x)\right|\mathrm{d}x\leqslant\int_{0}^{1}\left(1-\left|x-x_{0}\right|\right)\left|f^{\prime}(x)\right|\mathrm{d}x.$$
>
> 等号不能成立: 否则各步放缩都须取等, 特别地由 $\int_{x}^{1}|f'(t)|\,\mathrm{d}t = \int_{x}^{x_{0}}|f'(t)|\,\mathrm{d}t$ $(x < x_{0})$ 可得 $f'(x) \equiv 0$ 于 $[x_{0},1]$, 由 $\int_{0}^{x}|f'(t)|\,\mathrm{d}t = \int_{x_{0}}^{x}|f'(t)|\,\mathrm{d}t$ $(x > x_{0})$ 可得 $f'(x) \equiv 0$ 于 $[0,x_{0}]$, 于是 $f(x)$ 为常数; 又 $f(x_{0}) = 0$, 故 $f(x) \equiv 0$, 与题设 $\left|\int_{0}^{1}f(x)\,\mathrm{d}x\right| < \int_{0}^{1}|f(x)|\,\mathrm{d}x$ 矛盾. 所以
>
> $$\int_{0}^{1}\left|f(x)\right|\mathrm{d}x<\int_{0}^{1}\left(1-\left|x-x_{0}\right|\right)\left|f^{\prime}(x)\right|\mathrm{d}x.$$
>
> 两个关键动作: (1) 把 $|f(x)|$ 放成“从零点到 x 的 $|f'(x)|$ 积分”; (2) 换序—— $|f'(x)|$ 与 x 无关, 换序之后 x 的权重正好拼成 $1 - |x - x_0|$ (即“离 $x_0$ 的距离”). 严格性由“若取等则 $f'(x) \equiv 0$, 从而 $f(x) \equiv 0$, 与题设矛盾”排除.

**6.** (难度：★★★★★) 设连续可微的非负函数 $f(x)$，满足: $\left|f'(x)-f'(y)\right| \leqslant M|x-y|$ 恒成立. 证明:

$$[f^{\prime}(x)]^{2}\leqslant2Mf(x)$$

对任意的x恒成立.

> [!answer]- 原书参考答案（D.0.3 第 6 题，未逐题独立验算）
> **6.** 第一步: 先固定 $x$，把下界写成关于 $x_0$ 的二次函数。目标是“把 $f(x)$ 用 $f'(x)$ 从下方撑起来”，而 $f'$ 的界只能通过两点之差用上。先设 $x_0 < x$，由 Lipschitz 条件，对 $t \in [x_0, x]$ 有
>
> $$f^{\prime}(t)\geqslant f^{\prime}(x)-M(x-t),$$
>
> 两边在 $[x_{0}, x]$ 上积分，并用 $f(x_{0}) \geqslant 0$:
>
> $$\begin{aligned}f(x)&=f(x_{0})+\int_{x_{0}}^{x}f^{\prime}(t)\mathrm{d}t\geqslant\int_{x_{0}}^{x}\left[f^{\prime}(x)-M(x-t)\right]\mathrm{d}t\\&=\left[f^{\prime}(x)-Mx\right](x-x_{0})+\frac{M}{2}\left(x^{2}-x_{0}^{2}\right)\\&=-\frac{M}{2}x_{0}^{2}+Mxx_{0}+xf^{\prime}(x)-\frac{M}{2}x^{2}.\end{aligned}$$
>
> 第二步: 整理对称轴, 得到“想取”的 $x_{0}$. 把最后一式看成关于 $x_{0}$ 的二次函数 $g(x_{0})$: 开口向下, 对称轴在
>
> $$x_{0}=\frac{M x-f^{\prime}(x)}{M}=x-\frac{f^{\prime}(x)}{M},$$
>
> 此处取到最大值 $g\left(x - \frac{f'(x)}{M}\right) = \frac{f'(x)^2}{2M}$. 若就取这个 $x_0$，似乎立刻得到 $f(x) \geq \frac{f'(x)^2}{2M}$.
>
> **第三步：探究——发现它和 $f'(x)$ 的符号强相关.**
>
> $f'(x) > 0$ 时 $x_0 = x - \frac{f'(x)}{M} < x$，与上面的假设 $x_0 < x$ 一致，可行；
>
> $f'(x) < 0$ 时 $x_{0} = x - \frac{f'(x)}{M} > x$，与 $x_{0} < x$ 方向相反，那段积分区间 $[x_{0}, x]$ 根本不存在，这一步失效；
>
> $f'(x)=0$ 时 $x_{0}=x$，积分区间退化为一点，只能得到 $f(x)\geqslant0$.
>
> 可见”取对称轴”只在 $f'(x)>0$时成立，取法与 $f'(x)$的符号强相关，所以下面必须按符号分类讨论.
>
> 情形一: $f'(x) > 0$. 取 $x_0 = x - \frac{f'(x)}{M} < x$. 对 $t \in [x_0, x]$ 有 $f'(t) \geq f'(x) - M(x - t)$, 由牛莱公式并利用 $f(x_0) \geq 0$,
>
> $$f(x)=f(x_{0})+\int_{x_{0}}^{x}f^{\prime}(t)\mathrm{d}t\geqslant\int_{x_{0}}^{x}\left[f^{\prime}(x)-M(x-t)\right]\mathrm{d}t.$$
>
> 作换元 $u = x - t$ ( $t: x_0 \to x$ 对应 $u: \frac{f'(x)}{M} \to 0$):
>
> $$\int_{x_{0}}^{x}\left[f^{\prime}(x)-M(x-t)\right]\mathrm{d}t=\int_{0}^{\frac{f^{\prime}(x)}{M}}\left(f^{\prime}(x)-M u\right)\mathrm{d}u=\frac{f^{\prime}(x)^{2}}{2M},$$
>
> 故 $\left|f^{\prime}(x)\right|^{2}=f^{\prime}(x)^{2}\leqslant2Mf(x)$.
>
> 情形二： $f'(x) < 0$。取 $x_0 = x - \frac{f'(x)}{M} > x$。对 $t \in [x, x_0]$ 有 $f'(t) \leq f'(x) + M(t - x)$，由牛莱公式并利用 $f(x_0) \geq 0$，
>
> $$f(x)=f(x_{0})-\int_{x}^{x_{0}}f^{\prime}(t)\mathrm{d}t\geqslant-\int_{x}^{x_{0}}\left[f^{\prime}(x)+M(t-x)\right]\mathrm{d}t.$$
>
> 作换元 $u = t - x$ ( $t: x \to x_0$ 对应 $u: 0 \to \frac{|f'(x)|}{M}$，注意 $-f'(x) = |f'(x)|$:
>
> $$-\int_{x}^{x_{0}}\left[f^{\prime}(x)+M(t-x)\right]\mathrm{d}t=-\int_{0}^{\frac{|f^{\prime}(x)|}{M}}\left(f^{\prime}(x)+M u\right)\mathrm{d}u=\frac{|f^{\prime}(x)|^{2}}{2M},$$
>
> 故 $\left|f'(x)\right|^{2}\leq2Mf(x)$.
>
> 情形三： $f'(x)=0$。此时 $\left|f'(x)\right|^2=0\leqslant2Mf(x)$成立。
>
> 综上，对任意 $x \in \mathbb{R}$ 都有 $|f'(x)|^2 \leqslant 2M f(x)$.

## 3.4 分段估计

一元积分学证明的常见思想，将一个难以分析的表达式拆为若干部分逐一分析。同时，分段估计的题目，也是拉普拉斯方法所代表的一类做题技巧，和极限定义结合，可以解决顶级难度的压轴证明题。

**1.** (难度: ★★★) 是否存在区间 $[0,2]$ 上的连续可微函数 $f(x)$，满足：

$$f(0)=f(2)=1,\quad|f^{\prime}(x)|\leqslant1,\quad\left|\int_{0}^{2}f(x)\mathrm{d}x\right|\leqslant1?$$

请说明理由。

> [!answer]- 原书参考答案（D.0.4 第 1 题，未逐题独立验算）
> **1.** 第一步：把端点条件写成两个单调函数.令
>
> $$F(x)=f(x)+x-1,\qquad G(x)=f(x)-x+1.$$
>
> 则
>
> $$F^{\prime}(x)=f^{\prime}(x)+1\geqslant0,\qquad G^{\prime}(x)=f^{\prime}(x)-1\leqslant0,$$
>
> 故 $F(x)$ 单调递增、 $G(x)$ 单调递减. 又
>
> $$F(0)=f(0)-1=0,\qquad G(2)=f(2)-2+1=0.$$
>
> 由 $F(0)=0$ 与 $F(x)$ 单调递增得 $F(x)\geqslant0(x\geqslant0)$，即 $f(x)\geqslant1-x$; 由 $G(2)=0$ 与 $G(x)$ 单调递减得 $G(x)\geqslant0(x\leqslant2)$，即 $f(x)\geqslant x-1$. 也就是说， $f(x)$ 的图像在 $[0,1]$ 上不低于直线 y=1-x，在 $[1,2]$ 上不低于直线 y=x-1.
>
> <div style="text-align: center;"><img src="https://pplines-online.bj.bcebos.com/deploy/official/paddleocr/pp-ocr-vl-16-online//6dd22682-b586-4b2f-ace4-0ed2a1c7e4fb/markdown_3/imgs/img_in_image_box_507_947_742_1130.jpg?authorization=bce-auth-v1%2FALTAKDN8mY5KlNI7zaRpLmOqrw%2F2026-11-05T13%3A10%3A31Z%2F-1%2F%2F150c11d150908b280f9d0eb7f023c93dd6554e6c9a6a1796beb980d28ed358a5" alt="Image" width="19%" /></div>
>
> 图中阴影面积（两个三角形之和）为 $\frac{1}{2}+\frac{1}{2}=1$.
>
> 第二步：把两条下界积分.
>
> $$\int_{0}^{2}f(x)\mathrm{d}x\geqslant\int_{0}^{1}(1-x)\mathrm{d}x+\int_{1}^{2}(x-1)\mathrm{d}x=\frac{1}{2}+\frac{1}{2}=1.$$
>
> 第三步:由 $\left|\int_{0}^{2}f(x)dx\right|\leqslant1$逼出等号,再检查x=1处的可导性.因为 $\int_{0}^{2}f(x)dx\geqslant$
>
> 1 且 $\left|\int_{0}^{2}f(x)dx\right|\leqslant1$ , 故
>
> $$\int_{0}^{2}f(x)\mathrm{d}x=1,$$
>
> 且第一步中的两个不等式都处处取等号，即
>
> $$f(x)=1-x\;(0\leqslant x\leqslant1),\qquad f(x)=x-1\;(1\leqslant x\leqslant2).$$
>
> 但此时
>
> $$f^{\prime}(1^{-})=-1,\qquad f^{\prime}(1^{+})=1,$$
>
> $f(x)$ 在 x=1 处不可导，与 $f(x)$ 连续可微矛盾。所以这样的 $f(x)$ 不存在。

**2.** (难度：★★★★★) 设 $f(x)$, $g(x)$ 是 $[0,1] \rightarrow [0,1]$ 的连续函数, 且 $f(x)$ 单调增加. 求证:

$$\int_{0}^{1}f(g(x))\mathrm{d}x\leqslant\int_{0}^{1}f(x)\mathrm{d}x+\int_{0}^{1}g(x)\mathrm{d}x.$$

> [!answer]- 原书参考答案（D.0.4 第 2 题，未逐题独立验算）
> **2.** 把 $f(x)$ 拆成 $F(x) + x$ ( $F(x) = f(x) - x$)，不等式就只含 $F(x)$; 再看 $F(x)$ 的最大值点 c，以 c 为分点: 左侧用 $f(x) \in [0,1]$ 给 $F(x) \geq -x$，右侧用 $f(x)$ 单调增加给 $F(x) \geq M + c - x$. 令 $F(x) = f(x) - x$，则 $f(x) = F(x) + x$. 代入并把两边的 $\int_{0}^{1} g(x) \, dx$ 约去 (注意 $\int_{0}^{1} x \, dx = \frac{1}{2}$)，原不等式等价于
>
> $$\int_{0}^{1}F(g(x))\mathrm{d}x\leqslant\int_{0}^{1}F(x)\mathrm{d}x+\frac{1}{2}.$$
>
> 设 $M = \max_{0 \leq x \leq 1} F(x) = F(c)$，则 $F(g(x)) \leq M$，故 $\int_{0}^{1} F(g(x)) \, \mathrm{d}x \leq M$；于是只要证 $\int_{0}^{1} F(x) \, \mathrm{d}x + \frac{1}{2} \geq M$。
>
> 注意 $F(x)+x=f(x)\in[0,1]$. 在 $[0,c]$ 上 $f(x)\geqslant0$ 给出 $F(x)\geqslant-x$, 故 $\int_{0}^{x}F(x)\mathrm{d}x\geqslant$ $-\frac{c^{2}}{2}$; 在 $[c,1]$ 上由 $f(x)$ 单调增加, $f(x)\geqslant f(c)=F(c)+c=M+c$, 即 $F(x)\geqslant M+c-x$, 故
>
> $$\int_{c}^{1}F(x)\mathrm{d}x\geqslant\int_{c}^{1}(M+c-x)\mathrm{d}x=(M+c)(1-c)-\frac{1-c^{2}}{2}.$$
>
> 两段相加得 $\int_{0}^{1}F(x)\mathrm{d}x\geqslant(M+c)(1-c)-\frac{1}{2}$，于是
>
> $$\int_{0}^{1}F(x)\mathrm{d}x+\frac{1}{2}-M\geqslant(M+c)(1-c)-M=c\left(1-M-c\right)\geqslant0,$$
>
> 最后一步用了 $M + c = F(c) + c = f(c) \leq 1$。故 (1) 成立，原不等式得证。“作差函数 $F(x) = f(x) - x$” 是把 $f(x) \in [0,1]$ 变成 $F(x) \geq -x$ 的关键；分点取 $F(x)$ 的最大值点 $c$，是因为只有 $c$ 的右侧才能用上 $f(x)$ 的单调性。

**3.** (难度: ★★★★) 证明: 对任意正整数 n, 恒有

$$\int_{0}^{\frac{\pi}{2}}x\left|\frac{\sin nx}{\sin x}\right|^{4}\mathrm{d}x\leqslant\left(\frac{n^{2}}{4}+\frac{1}{8}\right)\pi^{2}.$$

> [!answer]- 原书参考答案（D.0.4 第 3 题，未逐题独立验算）
> **3.** 被积函数里的 $\left(\frac{\sin nx}{\sin x}\right)^4$在两端“性质相反”: 靠0处 $\frac{\sin nx}{\sin x}\approx n$，有上界 $n^4$; 靠 $\frac{\pi}{2}$处商不再大，但 $\frac{1}{\sin^4 x}$会爆，要用割线 $\sin x\geq\frac{2}{\pi}x$控制. 单独用哪一条都会丢精度，所以要待定分点 $\delta_n$、分段放缩，最后选 $\delta_n$使两段平衡. 第一步: 先证 $\sin nx\leq n\sin x$（ $0<x<\frac{\pi}{2}$）. 对n归纳. n=1,2显然; 设n=k时成立，则
>
> $$\sin(k+1)x=\sin x\cos kx+\cos x\sin kx\leqslant\sin x+k\sin x=(k+1)\sin x,$$
>
> 故对一切正整数 n 都有 $\sin nx \leqslant n \sin x$.
>
> 第二步：取分点 $\delta_{n}$，把积分拆成两段.
>
> $$\int_{0}^{\frac{\pi}{2}}x\left(\frac{\sin nx}{\sin x}\right)^{4}\mathrm{d}x=\int_{0}^{\delta_{n}}x\left(\frac{\sin nx}{\sin x}\right)^{4}\mathrm{d}x+\int_{\delta_{n}}^{\frac{\pi}{2}}x\left(\frac{\sin nx}{\sin x}\right)^{4}\mathrm{d}x.$$
>
> 近段 $(0 < x \leqslant \delta_{n})$：由第一步， $\left( \frac{\sin nx}{\sin x} \right)^{4} \leqslant n^{4}$，故
>
> $$\int_{0}^{\delta_{n}}x\left(\frac{\sin nx}{\sin x}\right)^{4}\mathrm{d}x\leqslant n^{4}\int_{0}^{\delta_{n}}x\mathrm{d}x=\frac{n^{4}}{2}\delta_{n}^{2}.$$
>
> 远段 $\left(\delta_{n}\leqslant x\leqslant\frac{\pi}{2}\right)$：由 $\sin x$ 在 $[0,\pi]$ 上是凹函数（图像在弦的上方）， $\sin x\geqslant\frac{2}{\pi}x$ 故
>
> $$\left(\frac{\sin nx}{\sin x}\right)^{4}\leqslant\frac{1}{\sin^{4}x}\leqslant\left(\frac{\pi}{2x}\right)^{4},$$
>
> $$\int_{\delta_{n}}^{\frac{\pi}{2}}x\left(\frac{\sin nx}{\sin x}\right)^{4}\mathrm{d}x\leqslant\frac{\pi^{4}}{16}\int_{\delta_{n}}^{\frac{\pi}{2}}\frac{\mathrm{d}x}{x^{3}}=\frac{\pi^{4}}{32}\left(\frac{1}{\delta_{n}^{2}}-\frac{4}{\pi^{2}}\right).$$
>
> 两段相加：
>
> $$\int_{0}^{\frac{\pi}{2}}x\left(\frac{\sin nx}{\sin x}\right)^{4}\mathrm{d}x\leqslant\frac{n^{4}}{2}\delta_{n}^{2}+\frac{\pi^{4}}{32}\cdot\frac{1}{\delta_{n}^{2}}-\frac{\pi^{2}}{8}.$$
>
> 第三步：取 $\delta_{n}=\frac{\pi}{2n}$. 此时 $\frac{n^{4}}{2}\cdot\frac{\pi^{2}}{4n^{2}}=\frac{n^{2}\pi^{2}}{8},\frac{\pi^{4}}{32}\cdot\frac{4n^{2}}{\pi^{2}}=\frac{n^{2}\pi^{2}}{8}$，故
>
> $$\int_{0}^{\frac{\pi}{2}}x\left(\frac{\sin nx}{\sin x}\right)^{4}\mathrm{d}x\leqslant\frac{n^{2}\pi^{2}}{8}+\frac{n^{2}\pi^{2}}{8}-\frac{\pi^{2}}{8}=\left(\frac{n^{2}}{4}-\frac{1}{8}\right)\pi^{2}.$$
>
> 分段的两条工具刚好互补：靠0处用 $\sin nx \leqslant n\sin x$（那里 $\sin x \sim x$，商有界），靠 $\frac{\pi}{2}$处用割线 $\sin x \geqslant \frac{2}{\pi}x$（把 $\sin^{4}x$换成 $x^{4}$）。分点由“两段同量级”定出：令 $\frac{n^{4}}{2}\delta_{n}^{2} = \frac{\pi^{4}}{32\delta_{n}^{2}}$，得 $\delta_{n} = \frac{\pi}{2n}$。

**4.** (难度：★★★★★) 设 $f(x)$ 在 $[0,1]$ 上有连续二阶导数, 且有 $f''(x) < 0$, $f(0) = f(1) = 0$, 证明:

$$\int_{0}^{1}\left|\frac{f^{\prime\prime}(x)}{f(x)}\right|\mathrm{d}x>4.$$

> [!answer]- 原书参考答案（D.0.4 第 4 题，未逐题独立验算）
> **4.** 先用 $f''(x) \leqslant 0$ 说明 $f(x) > 0$ (否则 $\frac{1}{f(x)}$ 无从谈起)，把分母放大成 M; 再把 $\int_{0}^{1}|f''(x)|\,\mathrm{d}x$ 减弱到最值点两侧两个中值点之间的 $[\xi_1, \xi_2]$，用 $f'(x)$ 的两个值之差算出结果。因 $f''(x) \leqslant 0$, $f(x)$ 上凸、图像在弦的上方，而两端 $f(0) = f(1) = 0$，故 $f(x) \geqslant 0$; 又 M > 0，若某个内点取值为 0，由上凸性可推出 $f(x) \equiv 0$，与 M > 0 矛盾，所以 $f(x) > 0$ (0 < x < 1)。
>
> 设 $f(c)=M$ 。由 $\frac{1}{f(x)}\geq\frac{1}{M}$
>
> $$\int_{0}^{1}\frac{\left|f^{\prime\prime}(x)\right|}{f(x)}\mathrm{d}x\geqslant\frac{1}{M}\int_{0}^{1}\left|f^{\prime\prime}(x)\right|\mathrm{d}x.$$
>
> 在 $[0,c]$、 $[c,1]$ 上分别用拉格朗日中值定理: 存在 $\xi_1 \in (0,c)$、 $\xi_2 \in (c,1)$，使
>
> $$f^{\prime}(\xi_{1})=\frac{M}{c},\qquad f^{\prime}(\xi_{2})=-\frac{M}{1-c}.$$
>
> 把区间减弱到 $[\xi_{1},\xi_{2}]$ 并放缩：
>
> $$\begin{aligned}\int_{0}^{1}\left|f^{\prime\prime}(x)\right|\mathrm{d}x&\geqslant\int_{\xi_{1}}^{\xi_{2}}\left|f^{\prime\prime}(x)\right|\mathrm{d}x\\ \geqslant\left|\int_{\xi_{1}}^{\xi_{2}}f^{\prime\prime}(x)\mathrm{d}x\right|&=\left|f^{\prime}(\xi_{2})-f^{\prime}(\xi_{1})\right|=\frac{M}{c(1-c)}\geqslant4M\end{aligned}$$
>
> $(c(1-c)\leq\frac{1}{4})$. 故原积分 $\geq\frac{1}{M}\cdot4M=4.$ (1) $f''(x)\leq0$ 这里只用来”保证 $f(x)>0''$，使分母有意义；(2) 真正出力的是”最值点两侧的两个拉格朗日点”——它把 $f''(x)$ 的积分换成 $f'(x)$ 的两个值之差 $\frac{M}{c(1-c)}$，再用 $c(1-c)\leq\frac{1}{4}$ 收口.

**5.** (难度：★★★★★) 设 $f(x)$ 在 $[a,b]$ 上非负连续, 严格单调增加, 且对任意的 $n \in \mathbb{N}$, 存在 $x_n \in [a,b]$, 使得

$$[f(x_{n})]^{n}=\frac{1}{b-a}\int_{a}^{b}[f(x)]^{n}\mathrm{d}x.$$

求极限 $\lim_{n \to \infty} x_n$.

> [!answer]- 原书参考答案（D.0.4 第 5 题，未逐题独立验算）
> **5.** 三种解法都指向同一件事: $\left(\int_{a}^{b}f^{n}(x)dx\right)^{1/n}$ 的极限由 $f(x)$ 在区间上的最大值 $f(b)$ 决定 (这正是拉普拉斯方法的主部). 因此
>
> $$f(x_{n})=\frac{1}{(b-a)^{1/n}}\left(\int_{a}^{b}f^{n}(x)\mathrm{d}x\right)^{1/n}\longrightarrow f(b),$$
>
> 再由 $f(x)$ 严格单调增加且连续，得 $x_n \to b$。下面把这个“主部”用三种方式兑现。
>
> 解法一（上下夹逼）。由 $f(x) \leq f(b)$，
>
> $$f(x_{n})\leqslant\frac{1}{(b-a)^{1/n}}\left(\int_{a}^{b}f^{n}(b)\mathrm{d}x\right)^{1/n}=f(b).$$
>
> 另一方面，只保留靠近 $b$ 的一小段 $\left[b - \frac{1}{n}, b\right]$ ($n$ 充分大时 $b - \frac{1}{n} > a$)。由积分中值定理，存在 $\xi_n \in \left(b - \frac{1}{n}, b\right)$，使
>
> $$\int_{b-\frac{1}{n}}^{b}f^{n}(x)\mathrm{d}x=\frac{1}{n}f^{n}(\xi_{n}),$$
>
> 于是
>
> $$f(x_{n})>\frac{1}{(b-a)^{1/n}}\left(\frac{1}{n}f^{n}(\xi_{n})\right)^{1/n}=\frac{1}{(b-a)^{1/n}}\cdot\frac{1}{n^{1/n}}f(\xi_{n}).$$
>
> 因 $\xi_{n} \to b$、 $f(x)$ 连续，故 $f(\xi_{n}) \to f(b)$；又 $\frac{1}{(b-a)^{1/n}} \to 1$、 $\frac{1}{n^{1/n}} \to 1$，所以右端趋于 $f(b)$。由夹逼定理 $f(x_{n}) \to f(b)$，从而 $x_{n} \to b$。
>
> 解法二 ( $\varepsilon$-近邻). 对任意 $\varepsilon > 0$ (足够小), n 充分大时,
>
> $$f^{n}(x_{n})=\frac{1}{b-a}\int_{a}^{b}f^{n}(x)\mathrm{d}x>\frac{1}{b-a}\int_{b-\varepsilon}^{b}f^{n}(x)\mathrm{d}x\geqslant\frac{\varepsilon}{b-a}f^{n}(b-\varepsilon).$$
>
> 因 $\frac{f(b-2\varepsilon)}{f(b-\varepsilon)}<1$，取 N 充分大，使 n>N 时
>
> $$\left[\frac{f(b-2\varepsilon)}{f(b-\varepsilon)}\right]^{n}<\frac{\varepsilon}{b-a},$$
>
> 于是 $f^n(x_n) > f^n(b-2\varepsilon)$，即 $f(x_n) > f(b-2\varepsilon)$。因 $f(x)$ 严格单调增加，故 $x_n > b-2\varepsilon$，从而 $|x_n-b| < 2\varepsilon$。由 $\varepsilon > 0$ 任意，得 $\lim_{n \to \infty} x_n = b$。
>
> 解法三 (直接算主部). 由 $\lim_{x\to b^{-}}\ln\frac{f(x)}{f(b)}=0$, 对任意 $\varepsilon>0$, 存在 $\delta>0$, 使当 $x\in(b-\delta,b)$ 时
>
> $$\ln f(b)-\varepsilon<\ln f(x)<\ln f(b)+\varepsilon,\qquad 即 \qquad e^{-\varepsilon}f(b)<f(x)<e^{\varepsilon}f(b).$$
>
> 于是
>
> $$\delta e^{-n\varepsilon}f^{n}(b)\leqslant\int_{b-\delta}^{b}f^{n}(x)\mathrm{d}x\leqslant\delta e^{n\varepsilon}f^{n}(b),\qquad\int_{a}^{b-\delta}f^{n}(x)\mathrm{d}x\leqslant(b-a)f^{n}(b-\delta).$$
>
> 把两式相加并开 n 次方：
>
> $$\delta^{\frac{1}{n}}e^{-\varepsilon}f(b)\leqslant\left(\int_{a}^{b}f^{n}(x)\mathrm{d}x\right)^{\frac{1}{n}}\leqslant(\delta e^{n\varepsilon}f^{n}(b)+(b-a)f^{n}(b-\delta))^{\frac{1}{n}}.$$
>
> 令 $n \to \infty$: 左端趋于 $e^{-\varepsilon}f(b)$，右端趋于 $\max\{e^{\varepsilon}f(b), f(b-\delta)\} = e^{\varepsilon}f(b)$，由夹逼定理
>
> $$e^{-\varepsilon}f(b)\leqslant\lim_{n\to\infty}\left(\int_{a}^{b}f^{n}(x)\mathrm{d}x\right)^{\frac{1}{n}}\leqslant e^{\varepsilon}f(b).$$
>
> 再令 $\varepsilon \to 0^{+}$，得 $\lim_{n \to \infty} \left( \int_{a}^{b} f^{n}(x) \, dx \right)^{\frac{1}{n}} = f(b)$。于是
>
> $$f(x_{n})=\frac{1}{(b-a)^{1/n}}\left(\int_{a}^{b}f^{n}(x)\mathrm{d}x\right)^{1/n}\longrightarrow f(b),$$
>
> 由 $f(x)$ 严格单调增加且连续, 得 $\lim_{n\to\infty}x_n=b$.

**6.** (难度:★★★★★) 设 $u_{n} = \int_{0}^{1} \frac{1}{(1 + t^{4})^{n}} dt$, 确定正实数 p, q, 使得

$$\lim_{n\to\infty}n^{p} u_{n}=q.$$

> [!answer]- 原书参考答案（D.0.4 第 6 题，未逐题独立验算）
> **6.** $\frac{1}{(1+t^{4})^{n}} = e^{-n \ln(1+t^{4})}$，而 $\ln(1+t^{4}) \sim t^{4} (t \to 0^{+})$，所以主部来自 t = 0 附近的一小段：作换元 $u = nt^{4}$ 后积分化成 $\Gamma$ 函数；t 不接近 0 的部分是指数衰减，乘任何 $n^{p}$ 都趋于 0。第一步：用 $\ln(1+t^{4}) \sim t^{4}$ 给被积函数定指数阶。因为 $\lim_{t \to 0} \frac{\ln(1+t^{4})}{t^{4}} = 1$，对任意 $\varepsilon > 0$，存在 $\delta \in (0,1)$，使 $t \in (0, \delta)$ 时
>
> $$(1-\varepsilon)t^{4}<\ln(1+t^{4})<(1+\varepsilon)t^{4},$$
>
> 故
>
> $$e^{-n(1+\varepsilon)t^{4}}<\frac{1}{(1+t^{4})^{n}}<e^{-n(1-\varepsilon)t^{4}}.$$
>
> 第二步：远处 $(t\geqslant\delta)$指数衰减.此时 $(1+t^{4})^{n}\geqslant(1+\delta^{4})^{n}$，故
>
> $$0<\int_{\delta}^{1}\frac{\mathrm{d}t}{(1+t^{4})^{n}}\leqslant\frac{1-\delta}{(1+\delta^{4})^{n}},$$
>
> 于是对任意 p > 0 都有 $\lim_{n \to \infty} n^p \int_{\delta}^1 \frac{dt}{(1 + t^4)^n} = 0$.
>
> 第三步：近处 $(0 < t < \delta)$换元成Γ函数。由上界
>
> $$\int_{0}^{\delta}\frac{\mathrm{d}t}{(1+t^{4})^{n}}<\int_{0}^{\delta}e^{-n(1-\varepsilon)t^{4}}\mathrm{d}t,$$
>
> 作换元 $u = n(1 - \varepsilon)t^4$，则 $\mathrm{d}t = \frac{u^{-3/4}}{4n^{1/4}(1 - \varepsilon)^{1/4}}\mathrm{d}u$，于是
>
> $$\int_{0}^{\delta}\frac{\mathrm{d}t}{(1+t^{4})^{n}}<\frac{1}{4n^{1/4}(1-\varepsilon)^{1/4}}\int_{0}^{+\infty}u^{-3/4}e^{-u}\mathrm{d}u=\frac{\Gamma\left(\frac{1}{4}\right)}{4n^{1/4}(1-\varepsilon)^{1/4}}.$$
>
> 同理由下界 $e^{-n(1+\varepsilon)t^{4}}$ 与同一个换元，
>
> $$\int_{0}^{\delta}\frac{\mathrm{d}t}{(1+t^{4})^{n}}>\frac{1}{4n^{1/4}(1+\varepsilon)^{1/4}}\int_{0}^{n(1+\varepsilon)\delta^{4}}u^{-3/4}e^{-u}\mathrm{d}u.$$
>
> 第四步: 合并, 定出 p 与 q. 第二步说明远处的贡献乘 $n^{1/4}$ 后趋于 0. 对近处, 因 $\int_{0}^{n(1+\varepsilon)\delta^{4}} u^{-3/4} e^{-u} du \to \Gamma\left(\frac{1}{4}\right)$, 当 n 充分大时
>
> $$\frac{1-\eta}{(1+\varepsilon)^{1/4}}<\frac{n^{1/4}\int_{0}^{\delta}\frac{\mathrm{d}t}{(1+t^{4})^{n}}}{\frac{1}{4}\Gamma\left(\frac{1}{4}\right)}<\frac{1}{(1-\varepsilon)^{1/4}}$$
>
> ( $\eta>0$ 任意). 令 $\varepsilon\to0^{+}$ 即得
>
> $$\lim_{n\to\infty}n^{1/4}\int_{0}^{\delta}\frac{\mathrm{d}t}{(1+t^{4})^{n}}=\frac{1}{4}\Gamma\left(\frac{1}{4}\right),$$
>
> 再加上远处趋于0的部分，
>
> $$\lim_{n\to\infty}n^{1/4}u_{n}=\frac{1}{4}\Gamma\left(\frac{1}{4}\right).$$
>
> 故 $p = \frac{1}{4}$， $q = \frac{1}{4}\Gamma\left(\frac{1}{4}\right)$。结构就是“近段 = $\Gamma$ 积分、远段指数衰减”：近段换元 $u = nt^{4}$ 提出 $n^{-1/4}$，剩下 $\int_{0}^{+\infty} u^{-3/4} e^{-u} du = \Gamma\left(\frac{1}{4}\right)$；远处被 $(1 + \delta^{4})^{-n}$ 压掉，乘任何多项式都趋于 0。

## 3.5 不等式配凑

与不等式相关的证明题,通常涉及基本的配方、拆项等代数技巧,同时要结合柯西不等式进行配凑,难度相对较高,除了待定配凑以外,瞪眼法也是不错的处理思路.

**1.** (难度:★★★★) 设函数 $f(x)$ 在区间 $[0,1]$ 上有连续的一阶导数, 且满足:

$$f(0)=f(1)=0,\quad\int_{0}^{1}[f^{\prime}(x)]^{2}\mathrm{d}x-8\int_{0}^{1}f(x)\mathrm{d}x+\frac{4}{3}=0.$$

据此求 $f(x)$ 的表达式.

> [!answer]- 原书参考答案（D.0.5 第 1 题，未逐题独立验算）
> **1.** 第一步: 用端点条件把 $\int_{0}^{1} f(x) \, dx$ 换成 $\int_{0}^{1} x f'(x) \, dx$.
>
> $$\int_{0}^{1}f^{\prime}(x)\mathrm{d}x=f(1)-f(0)=0,$$
>
> $$\int_{0}^{1}f(x)\mathrm{d}x=x f(x)\Big|_{0}^{1}-\int_{0}^{1}x f^{\prime}(x)\mathrm{d}x=-\int_{0}^{1}x f^{\prime}(x)\mathrm{d}x.$$
>
> 代入题设条件, 得
>
> $$\int_{0}^{1}\left[f^{\prime}(x)\right]^{2}\mathrm{d}x+8\int_{0}^{1}x f^{\prime}(x)\mathrm{d}x+\frac{4}{3}=0.$$
>
> 第二步：待定a,b，把左边配成完全平方.设
>
> $$\begin{aligned}Q(a,b)&=\int_{0}^{1}\left(f^{\prime}(x)+ax+b\right)^{2}\mathrm{d}x\\&=\int_{0}^{1}\left[f^{\prime2}(x)+2a x f^{\prime}(x)+2b f^{\prime}(x)+(ax+b)^{2}\right]\mathrm{d}x.\end{aligned}$$
>
> 利用第一步的两个等式 ( $\int_0^1 f'(x) \, \mathrm{d}x = 0$ 使 $2b \int_0^1 f'(x) \, \mathrm{d}x$ 消失, $\int_0^1 x f'(x) \, \mathrm{d}x = -\int_0^1 f(x) \, \mathrm{d}x$,
>
> $$Q(a,b)=\int_{0}^{1}\left[f^{\prime}(x)\right]^{2}\mathrm{d}x-2a\int_{0}^{1}f(x)\mathrm{d}x+\int_{0}^{1}(ax+b)^{2}\mathrm{d}x.$$
>
> 要让 $Q(a,b)$ 与 (1) 的左边一致: 先比对含 $\int_{0}^{1}f(x)dx$ 的项, 由 -2a = -8 得 a = 4; 再比对常数项, 要求
>
> $$\int_{0}^{1}(4x+b)^{2}\mathrm{d}x=\frac{16}{3}+4b+b^{2}=\frac{4}{3},$$
>
> 即 $b^{2}+4b+4=0$ , 得 b=-2. 第三步：由非负性逼出等号. 把 a=4, b=-2 代回：
>
> $$\int_{0}^{1}\left(f^{\prime}(x)+4x-2\right)^{2}\mathrm{d}x=\int_{0}^{1}\left[f^{\prime}(x)\right]^{2}\mathrm{d}x-8\int_{0}^{1}f(x)\mathrm{d}x+\frac{4}{3}=0.$$
>
> 被积函数连续且非负，积分为0说明它恒为0，即
>
> $$f^{\prime}(x)=-4x+2,\qquad f(x)=-2x^{2}+2x+C.$$
>
> 由 $f(0)=0$ 得 C=0，此时 $f(1)=0$ 也成立. 故
>
> $$f(x)=-2x^{2}+2x.$$

**2.** (难度:★★★★) 设 $f(x)$ 在区间 $[0,1]$ 上有连续的二阶导数, 且满足:

$$|f^{\prime\prime}(x)|\leqslant1,\quad\int_{0}^{1}f(x)\mathrm{d}x=\int_{0}^{1}x f(x)\mathrm{d}x=0.$$

证明： $\left|\int_{0}^{1}x^{2}f(x)dx\right|\leqslant\frac{1}{360}$，并给出一个使得等号成立的函数 $f(x)$.

> [!answer]- 原书参考答案（D.0.5 第 2 题，未逐题独立验算）
> **2.** 第一步：待定 p, q，把 $x^{2}f(x)$ 换成 $(x^{2} + px + q)f(x)$. 由条件 $\int_{0}^{1}f(x)dx=\int_{0}^{1}xf(x)dx=0$，对任意常数 p, q 都有
>
> $$\int_{0}^{1}x^{2}f(x)\mathrm{d}x=\int_{0}^{1}\left(x^{2}+p x+q\right)f(x)\mathrm{d}x.$$
>
> 记 $P(x) = x^{2} + px + q$. 这样配的目的, 是让 $P(x)$ 恰好是某个 $F(x)$ 的二阶导数、并且 $F(x)$ 与 $F'(x)$ 在两端都为 0——两次分部积分的边界项就全部消失, 只剩 $\int_{0}^{1} F(x) f''(x) \, dx$.
>
> 第二步：由边界条件定出 p,q. 取 $F(x)$ 使 $F''(x)=P(x)$，即
>
> $$F(x)=\frac{1}{12}x^{4}+\frac{p}{6}x^{3}+\frac{q}{2}x^{2}+C_{1}x+C_{2}.$$
>
> 由 $F(0)=F'(0)=0$ 得 $C_{1}=C_{2}=0$ ，即 $F(x)=\frac{1}{12}x^{4}+\frac{p}{6}x^{3}+\frac{q}{2}x^{2}$ 。再要求 $F(1)=F'(1)=0$ ：
>
> $$F(1)=\frac{1}{12}+\frac{p}{6}+\frac{q}{2}=0,\qquad F^{\prime}(1)=\frac{1}{3}+\frac{p}{2}+q=0,$$
>
> 即 $1+2p+6q=0$、 $2+3p+6q=0$，解得 p=-1、 $q=\frac{1}{6}$。于是
>
> $$P(x)=x^{2}-x+\frac{1}{6},\qquad F(x)=\frac{1}{12}x^{2}(x-1)^{2}.$$
>
> 第三步：两次分部积分.
>
> $$\begin{aligned}\int_{0}^{1}x^{2}f(x)\mathrm{d}x&=\int_{0}^{1}F^{\prime\prime}(x)f(x)\mathrm{d}x=F^{\prime}(x)f(x)\Big|_{0}^{1}-\int_{0}^{1}F^{\prime}(x)f^{\prime}(x)\mathrm{d}x\\&=-F(x)f^{\prime}(x)\Big|_{0}^{1}+\int_{0}^{1}F(x)f^{\prime\prime}(x)\mathrm{d}x.\end{aligned}$$
>
> 由 $F(0)=F(1)=F'(0)=F'(1)=0$ ，四个边界项全为0，故
>
> $$\int_{0}^{1}x^{2}f(x)\mathrm{d}x=\int_{0}^{1}F(x)f^{\prime\prime}(x)\mathrm{d}x.$$
>
> 第四步：放缩。注意 $F(x)=\frac{1}{12}x^{2}(x-1)^{2}\geqslant0$ ，且 $\left|f''(x)\right|\leqslant1$ ，故
>
> $$\begin{aligned}\left|\int_{0}^{1}x^{2}f(x)\mathrm{d}x\right|&\leqslant\int_{0}^{1}F(x)\left|f^{\prime\prime}(x)\right|\mathrm{d}x\leqslant\int_{0}^{1}F(x)\mathrm{d}x\\&=\frac{1}{12}\int_{0}^{1}x^{2}(x-1)^{2}\mathrm{d}x=\frac{1}{12}\cdot\frac{1}{30}=\frac{1}{360}.\end{aligned}$$
>
> 第五步: 等号成立的例子. 等号要求 $F(x) > 0$ 处都有 $f''(x) = 1$, 取 $f''(x) \equiv 1$, 即
>
> $$f(x)=\frac{1}{2}x^{2}+C_{1}x+C_{2}.$$
>
> 代入 $\int_{0}^{1}f(x)dx=0,\quad\int_{0}^{1}xf(x)dx=0:$
>
> $$\frac{1}{6}+\frac{C_{1}}{2}+C_{2}=0,\qquad\frac{1}{8}+\frac{C_{1}}{3}+\frac{C_{2}}{2}=0,$$
>
> 解得 $C_{1}=-\frac{1}{2}$、 $C_{2}=\frac{1}{12}$. 故 $f(x)=\frac{1}{2}x^{2}-\frac{1}{2}x+\frac{1}{12}$ 时等号成立.

**3.** (难度:★★★★) 设 $f(x)$ 在 $[a,b]$ 上具有一阶连续导数, 证明:

$$\int_{a}^{b}\sqrt{1+[f^{\prime}(x)]^{2}}\mathrm{d}x\geqslant\sqrt{(b-a)^{2}+(f(a)-f(b))^{2}},$$

并给出等号成立的条件.

> [!answer]- 原书参考答案（D.0.5 第 3 题，未逐题独立验算）
> **3.** 第一步：待定常数 u, v，把 $f'(x)$ 送进柯西不等式. 要让 $f'(x)$ 的积分借牛顿-莱布尼茨公式消掉，就设法把 $\sqrt{1+[f'(x)]^2}$ 与一个因子相乘、用柯西不等式放成 $u + v f'(x)$ 的形状. 设 u, v 为待定常数 $(u^2 + v^2 > 0)$，由柯西不等式
>
> $$\sqrt{1+\left[f^{\prime}(x)\right]^{2}}\cdot\sqrt{u^{2}+v^{2}}\geqslant1\cdot u+f^{\prime}(x)\cdot v$$
>
> (两边的平方差为 $(1 + f'(2)(x))\left(u^2 + v^2\right) - (u + vf'(x))^2 = (uf'(x) - v)^2 \geqslant 0$.
>
> 两边积分:
>
> $$\sqrt{u^{2}+v^{2}}\int_{a}^{b}\sqrt{1+[f^{\prime}(x)]^{2}}\mathrm{d}x\geqslant u(b-a)+v\left(f(b)-f(a)\right),$$
>
> 即
>
> $$\int_{a}^{b}\sqrt{1+\left[f^{\prime}(x)\right]^{2}}\mathrm{d}x\geqslant\frac{u(b-a)+v\left(f(b)-f(a)\right)}{\sqrt{u^{2}+v^{2}}}.$$
>
> 第二步：选 u, v 使右端最大. 记 A = b - a, B = f(b) - f(a). 由柯西不等式
>
> $$\left(u\boldsymbol{A}+v\boldsymbol{B}\right)^{2}\leqslant\left(u^{2}+v^{2}\right)\left(\boldsymbol{A}^{2}+\boldsymbol{B}^{2}\right),$$
>
> 当 $(u,v)$与 $(A,B)$成比例（即 $uB=vA$，也就是 $\frac{u}{A}=\frac{v}{B}$）时取等号，此时
>
> $$\frac{uA+vB}{\sqrt{u^{2}+v^{2}}}=\sqrt{A^{2}+B^{2}}.$$
>
> 所以只要取一对满足 $\frac{u}{A}=\frac{v}{B}$ 的 u,v (例如 u=A, v=B)，(1) 就化为
>
> $$\int_{a}^{b}\sqrt{1+[f^{\prime}(x)]^{2}}\mathrm{d}x\geqslant\sqrt{(b-a)^{2}+(f(b)-f(a))^{2}}.$$
>
> 第三步：等号条件. 柯西不等式取等要求 $f'(x) \equiv \frac{v}{u} = \frac{f(b) - f(a)}{b - a}$ 为常数, 此时
>
> $$f(x)=f(a)+\frac{f(b)-f(a)}{b-a}(x-a).$$
>
> 反之，当 $f(x)$ 为这个线性函数时，两处柯西不等式都取等号，故等号成立的条件正是“ $f(x)$ 为线性函数”.

**4.** (难度：★★★★★) 设 $f(x)$ 在 $[1,2]$ 上具有一阶连续导数, $f(1)=0$, $f(2)=1$, 求

$$\int_{1}^{2}\frac{\sqrt{1+[f^{\prime}(x)]^{2}}}{x}\mathrm{d}x$$

的最小值, 并给出取最小值时 $f(x)$ 的表达式.

> [!answer]- 原书参考答案（D.0.5 第 4 题，未逐题独立验算）
> **4.** 与例题 3.6.1 同一思路: 待定常数 a, 把 $\frac{1}{x}$ 拆成 $\sqrt{a^{2}+\left(\sqrt{\frac{1}{x^{2}}-a^{2}}\right)^{2}}$, 再用柯西不等式把 $f'(x)$ 分离出来 $(f'$ 的积分由 $f(2)-f(1)=1$ 算掉 $)$ ; 最后由取等条件与端点值定出 a. 第一步: 待定 a, 用柯西不等式分离 $f'(x)$. 设 $a\in\left(0,\frac{1}{2}\right)$, 把 $\frac{1}{x}$ 写成
>
> $$\frac{1}{x}=\sqrt{a^{2}+\left(\sqrt{\frac{1}{x^{2}}-a^{2}}\right)^{2}},$$
>
> 由柯西不等式，
>
> $$\frac{\sqrt{1+\left[f^{\prime}(x)\right]^{2}}}{x}\geqslant\sqrt{\frac{1}{x^{2}}-a^{2}}+a f^{\prime}(x)$$
>
> （平方差为 $\left(af'(x)-\sqrt{\frac{1}{x^2}-a^2}\right)^2\geqslant0$）. 两边在 $[1,2]$ 上积分，并用 $\int_{1}^{2}f'(x)dx=f(2)-f(1)=1$:
>
> $$\int_{1}^{2}\frac{\sqrt{1+[f^{\prime}(x)]^{2}}}{x}\mathrm{d}x\geqslant\int_{1}^{2}\sqrt{\frac{1}{x^{2}}-a^{2}}\mathrm{d}x+a.$$
>
> **第二步：由取等条件与端点值定出a.取等要求**
>
> $$f^{\prime}(x)=\frac{a}{\sqrt{\frac{1}{x^{2}}-a^{2}}}=\frac{ax}{\sqrt{1-a^{2}x^{2}}},\qquad 积分得 \qquad f(x)=-\frac{1}{a}\sqrt{1-a^{2}x^{2}}+C.$$
>
> 由 $f(1)=0$ 、 $f(2)=1$ 得 $-\frac{1}{a}\sqrt{1-a^{2}}+C=0$ 与 $-\frac{1}{a}\sqrt{1-4a^{2}}+C=1$ ，两式相减得
>
> $$\sqrt{1-a^{2}}-\sqrt{1-4a^{2}}=a,$$
>
> 解得 $a^{2}=\frac{1}{5}$， $a=\frac{1}{\sqrt{5}}$，代回得 C=2。于是
>
> $$f(x)=-\sqrt{5-x^{2}}+2.$$
>
> 第三步：算出最小值。把 $a=\frac{1}{\sqrt{5}}$ 代回：
>
> $$\int_{1}^{2}\frac{\sqrt{1+[f^{\prime}(x)]^{2}}}{x}\mathrm{d}x\geqslant\int_{1}^{2}\sqrt{\frac{1}{x^{2}}-\frac{1}{5}}\mathrm{d}x+\frac{1}{\sqrt{5}}.$$
>
> 令 $x = \sqrt{5} \sin \theta$，则 $\frac{dx}{x} = \frac{\cos \theta}{\sin \theta} d\theta$、 $\sqrt{\frac{1}{x^2} - \frac{1}{5}} = \frac{\cos \theta}{\sqrt{5} \sin \theta}$，故
>
> $$\int_{1}^{2}\sqrt{\frac{1}{x^{2}}-\frac{1}{5}}\mathrm{d}x=\int_{\arcsin\frac{1}{\sqrt{5}}}^{\arcsin\frac{2}{\sqrt{5}}}\frac{\cos^{2}\theta}{\sin\theta}\mathrm{d}\theta=\ln\frac{3+\sqrt{5}}{2}-\frac{1}{\sqrt{5}},$$
>
> 所以最小值为 $\ln\frac{3+\sqrt{5}}{2}$，取到时 $f(x)=-\sqrt{5-x^{2}}+2$。把 1/x 拆成一个常数项与一个平方项之和“是钥匙：柯西不等式把它变成 $\sqrt{\frac{1}{x^{2}}-a^{2}}+af'(x)$，其中 $af'(x)$ 的积分由 $f(2)-f(1)=1$ 给出。待定的 a 由“取等时的曲线要恰好经过两个端点”定出。

## 3.6 周期类证明

周期类的证明题核心是借助函数的周期性，进行区间拆分和放缩，经常会用到平移区间的技巧。此类题目在竞赛中也有不小的出现频率。

**1.** (难度:★★★) 已知微分方程 $y' + y = p(x)$，其中 $p(x)$ 在实数域上连续。证明: 若 $p(x)$ 是周期为 T 的周期函数，则该微分方程存在唯一的以 T 为周期的解。

> [!answer]- 原书参考答案（D.0.6 第 1 题，未逐题独立验算）
> **1.** 一阶线性方程的通解可以直接写出来: $y(x) = e^{-x} \left( \int_{0}^{x} e^{t} p(t) \, dt + C \right)$. 只要算出 $y(x + T) - y(x)$，再选唯一的 C 让它为 0 即可. 一阶线性方程 $y' + y = p(x)$ 的通解为
>
> $$y(x)=e^{-x}\left(\int_{0}^{x}e^{t}p(t)\mathrm{d}t+C\right).$$
>
> 由 $p(x+T)=p(x)$，把 $y(x+T)$ 里的积分换元 t=u+T:
>
> $$\int_{0}^{x+T}e^{t}p(t)\mathrm{d}t=\int_{-T}^{x}e^{u+T}p(u+T)\mathrm{d}u=e^{T}\int_{-T}^{x}e^{u}p(u)\mathrm{d}u.$$
>
> 于是
>
> $$\begin{aligned}y(x+T)-y(x)&=e^{-(x+T)}\left(e^{T}\int_{-T}^{x}e^{u}p(u)\mathrm{d}u+C\right)-e^{-x}\left(\int_{0}^{x}e^{t}p(t)\mathrm{d}t+C\right)\\&=e^{-x}\left(\int_{-T}^{0}e^{t}p(t)\mathrm{d}t+C\left(e^{-T}-1\right)\right).\end{aligned}$$
>
> 因此 y 以 T 为周期当且仅当
>
> $$\int_{-T}^{0}e^{t}p(t)\mathrm{d}t+C\left(e^{-T}-1\right)=0,\qquad 即 \qquad C=\frac{\int_{-T}^{0}e^{t}p(t)\mathrm{d}t}{1-e^{-T}}.$$
>
> 因 $p(x)$ 连续且以 T 为周期，这个积分存在且唯一，故 C 被唯一确定：方程存在唯一的以 T 为周期的解。关键在于“平移”：把 $\int_{0}^{x+T} p(u) \, \mathrm{d}u$ 平移到 $\int_{-T}^{x} p(u) \, \mathrm{d}u$ 时，p 的周期性使 $p(u+T) = p(u)$，只多出常数因子 $e^{T}$，恰好被外面的 $e^{-(x+T)}$ 抵消；这样 $y(x+T) - y(x)$ 就只与 $\int_{-T}^{0} e^{t} p(t) \, \mathrm{d}t$ 和 C 有关。

**2.** （难度：★★★）证明下列不等式：

(1) 设 $x \in [0, \pi]$, $t \in [0, 1]$, 则 $\sin(tx) \geq t \sin x$;

(2) 设 p > 0, 则 $\int_{0}^{\frac{\pi}{2}} |\sin u|^{p} \mathrm{d}u \geqslant \frac{\pi}{2(p+1)};$

(3) 设 $x \geqslant 0$, p > 0, 则 $\int_{0}^{x} |\sin u|^{p} \, \mathrm{d}u \geqslant \frac{x |\sin x|^{p}}{p+1}$.

> [!answer]- 原书参考答案（D.0.6 第 2 题，未逐题独立验算）
> **2.** 三问都是用单调性或“弦”控制 $|\sin u|^{p}$: (1) 作差求导; (2) 用弦 $\sin u \geq \frac{2}{\pi} u$; (3) 先按整周期拆开、余项上再用弦 $\sin y \geq \frac{\sin t}{t} y$. (1) 设 $g(x) = \sin(tx) - t \sin x$,
>
> 则 $g'(x) = t (\cos(tx) - \cos x)$. 当 $x \in [0, \pi]$、 $t \in [0,1]$ 时 $0 \leq tx \leq x \leq \pi$，而 $\cos$ 在 $[0, \pi]$ 上单调递减，故 $\cos(tx) \geq \cos x$，于是 $g'(x) \geq 0$， $g(x)$ 单调递增， $g(x) \geq g(0) = 0$，即 $\sin(tx) \geq t \sin x$.
>
> (2) 由弦不等式 $\sin u \geqslant \frac{2}{\pi} u$ ( $u \in [0, \frac{\pi}{2}]$)，
>
> $$\int_{0}^{\frac{\pi}{2}}\left|\sin u\right|^{p}\mathrm{d}u\geqslant\int_{0}^{\frac{\pi}{2}}\left(\frac{2}{\pi}u\right)^{p}\mathrm{d}u=\left(\frac{2}{\pi}\right)^{p}\frac{\left(\frac{\pi}{2}\right)^{p+1}}{p+1}=\frac{\pi}{2(p+1)}.$$
>
> (3) 令 $x = k\pi + t$, k 为非负整数、 $t \in [0, \pi)$. 由周期性,
>
> $$\int_{0}^{x}|\sin u|^{p}\mathrm{d}u=k\int_{0}^{\pi}|\sin u|^{p}\mathrm{d}u+\int_{0}^{t}|\sin y|^{p}\mathrm{d}y.$$
>
> 在 $[0,t]$ 上用弦 $\sin y \geqslant \frac{\sin t}{t} y$ (t=0 时两端均为 0):
>
> $$\int_{0}^{t}|\sin y|^{p}\mathrm{d}y\geqslant\int_{0}^{t}\left(\frac{\sin t}{t}y\right)^{p}\mathrm{d}y=\frac{|\sin t|^{p}t}{p+1},$$
>
> 又由 (2) 及对称性 $\int_{0}^{\pi}|\sin u|^{p}du\geqslant\frac{\pi}{p+1}$，故
>
> $$\begin{aligned}\int_{0}^{x}|\sin u|^{p}\mathrm{d}u&\geqslant\frac{k\pi}{p+1}+\frac{|\sin t|^{p}t}{p+1}\\=\frac{k\pi+t|\sin t|^{p}}{p+1}&\geqslant\frac{(k\pi+t)|\sin t|^{p}}{p+1}=\frac{x|\sin x|^{p}}{p+1}\end{aligned}$$
>
> （最后一步用 $\left|\sin t\right|^{p}\leqslant1$、 $x=k\pi+t$、 $\left|\sin(k\pi+t)\right|=\left|\sin t\right|$。证毕。（3）是“先处理整周期、再处理余项”的样板：整周期部分由（2）给出 $\frac{\pi}{p+1}$，余项在 $[0,t]$ 上用弦 $\sin y\geqslant\frac{\sin t}{t}y$；最后再把 $\left|\sin t\right|^{p}\leqslant1$ 用上，把 $\frac{k\pi}{p+1}$ 抬成 $\frac{k\pi\left|\sin t\right|^{p}}{p+1}$。

**3.** (难度:★★★★) 设函数 $\varphi(x)$ 连续且周期为 1, $\int_{0}^{1}\varphi(x)dx=0$, 函数 $f(x)$ 在 $[0,1]$ 上有连续的导函数. 设

$$a_{n}=\int_{0}^{1}f(x)\varphi(n x)\mathrm{d}x.$$

证明： $\sum_{n=1}^{\infty}a_{n}^{2}$ 收敛.

> [!answer]- 原书参考答案（D.0.6 第 3 题，未逐题独立验算）
> **3.** 先把 $\varphi(nx)$ 的周期用掉: 换元 u = nx、再逐段平移成 $[0,1]$ 上的积分; 然后与 $\sum f\left(\frac{k}{n}\right)$ 作差 ( $\int_{0}^{1}\varphi(y)dy = 0$ 使常数项消失), 做差放缩得到 $\left|a_{n}\right| \leqslant \frac{C}{n}$. 第一步: 换元并逐段平移. 令 $u = nx$ ( $\mathrm{d}x = \frac{1}{n}\mathrm{d}u$), 再对每段平移 y = u - k, 由 $\varphi$ 以 1 为周期,
>
> $$a_{n}=\frac{1}{n}\int_{0}^{n}f\Big(\frac{u}{n}\Big)\varphi(u)\mathrm{d}u=\frac{1}{n}\int_{0}^{1}\left[\sum_{k=0}^{n-1}f\left(\frac{k+y}{n}\right)\right]\varphi(y)\mathrm{d}y.$$
>
> 第二步: 与 $\sum f\left(\frac{k}{n}\right)$ 作差. 因为 $\int_{0}^{1}\varphi(y)\mathrm{d}y=0$, 常数 $\sum_{k=0}^{n-1}f\left(\frac{k}{n}\right)$ 乘上 $\varphi(y)$ 的积分为 0, 故
>
> $$a_{n}=\frac{1}{n}\int_{0}^{1}\left[\sum_{k=0}^{n-1}\left(f\left(\frac{k+y}{n}\right)-f\left(\frac{k}{n}\right)\right)\right]\varphi(y)\mathrm{d}y.$$
>
> 第三步：做差放缩. 因 $f^{\prime}$ 在 $[0,1]$ 上连续，存在 M > 0 使 $\left|f'(x)\right| \leqslant M$，于是
>
> $$\left|f\left(\frac{k+y}{n}\right)-f\left(\frac{k}{n}\right)\right|\leq\frac{My}{n}\leq\frac{M}{n}.$$
>
> 代入上式，
>
> $$\begin{aligned}\left|a_{n}\right|&\leqslant\frac{1}{n}\int_{0}^{1}\left(\sum_{k=0}^{n-1}\frac{M}{n}\right)\left|\varphi(y)\right|\mathrm{d}y\\&=\frac{M}{n}\int_{0}^{1}\left|\varphi(y)\right|\mathrm{d}y=\frac{C}{n},\end{aligned}$$
>
> $$C=M\int_{0}^{1}\left|\varphi(y)\right|\mathrm{d}y.$$
>
> 第四步：收敛. 于是 $a_{n}^{2}\leqslant\frac{C^{2}}{n^{2}}$，而 $\sum_{n=1}^{+\infty}\frac{1}{n^{2}}$ 收敛，由比较判别法即得 $\sum_{n=1}^{+\infty}a_{n}^{2}$ 收敛. 关键是第一步“换元 + 逐段平移”，把 $\varphi(nx)$ 的周期换成积分区间 $[0,1]$; 随后与 $f\left(\frac{k}{n}\right)$ 作差（这一步正是 $\int_{0}^{1}\varphi(y)dy=0$ 的用处：常数项被消掉），再用 $\left|f'(x)\right|\leqslant M$ 做差放缩，得到 $\left|a_{n}\right|=O\left(\frac{1}{n}\right)$.

**4.** (难度:★★★★) 设函数 $f(x)$ 是区间 $(0, +\infty)$ 上的非负连续函数, 且存在 T, M > 0, 使得对任意 a > 0, 恒有

$$\frac{1}{T}\int_{a}^{a+T}f(x)\mathrm{d}x\leqslant M.$$

证明：对任意 b, c > 0，恒有

$$\int_{0}^{c}e^{b(x-c)}f(x)\mathrm{d}x\leqslant\frac{M T}{1-e^{-b T}}.$$

> [!answer]- 原书参考答案（D.0.6 第 4 题，未逐题独立验算）
> **4.** 第一步：把条件翻译成“任意长度 T 的区间上积分不超过 $MT''$. 由换元 x = a + u,
>
> $$\int_{a}^{a+T}f(x)\mathrm{d}x=\int_{0}^{T}f(u+a)\mathrm{d}u\leqslant MT.$$
>
> 第二步: 把上限写成 $c = nT + \gamma$, 先分离出余项. 设 $c = nT + \gamma$, 其中 n 为非负整数、 $\gamma \in [0, T)$. 把积分拆成
>
> $$\int_{0}^{c}e^{b(x-c)}f(x)\mathrm{d}x=\int_{0}^{\gamma}e^{b(x-c)}f(x)\mathrm{d}x+\int_{\gamma}^{nT+\gamma}e^{b(x-c)}f(x)\mathrm{d}x.$$
>
> 余项那段 $(0<x<\gamma)$上 $e^{b(x-c)}\leq e^{-bnT}$，故
>
> $$\int_{0}^{\gamma}e^{b(x-c)}f(x)\mathrm{d}x\leqslant e^{-b n T}\int_{0}^{\gamma}f(x)\mathrm{d}x\leqslant M T e^{-b n T}$$
>
> （最后一步用了第一步的结论）. 第三步: 整周期部分逐段用条件. 在 $[\gamma, nT + \gamma]$ 上以 T 为步长分段: 令 $x = u + \gamma + kT$ ( $u \in [0, T]$、 $k = 0,1,\ldots,n-1$)，则
>
> $$x-c=u+\gamma+kT-\left(nT+\gamma\right)=u-\left(n-k\right)T,$$
>
> 故
>
> $$\int_{\gamma}^{nT+\gamma}e^{b(x-c)}f(x)\mathrm{d}x=\sum_{k=0}^{n-1}e^{-b(n-k)T}\int_{0}^{T}e^{bu}f(u+\gamma+kT)\mathrm{d}u.$$
>
> 由 $e^{bu} \leqslant e^{bT}$ 与第一步的结论（每段的积分不超过 MT），
>
> $$\sum_{k=0}^{n-1}e^{-b(n-k)T}\int_{0}^{T}e^{bu}f(u+\gamma+kT)\mathrm{d}u\leqslant MT e^{bT}\sum_{k=0}^{n-1}e^{-b(n-k)T}=MT\cdot\frac{1-e^{-nbT}}{1-e^{-bT}}.$$
>
> 第四步：合并并放大.
>
> $$\begin{aligned}\int_{0}^{c}e^{b(x-c)}f(x)\mathrm{d}x&\leqslant MT e^{-bnT}+MT\cdot\frac{1-e^{-nbT}}{1-e^{-bT}}\\&=MT\cdot\frac{1-e^{-(n+1)bT}}{1-e^{-bT}}\leqslant\frac{MT}{1-e^{-bT}}\end{aligned}$$
>
> （最后一步用 $1 - e^{-(n+1)bT} < 1$）. 证毕.

**5.** (难度:★★★★★) 设 $I_{n}=\int_{0}^{\pi}\frac{\sin x}{1+\cos^{2}nx}dx$, n 为正整数. 证明:

$$\lim_{n\to\infty}I_{n}=\sqrt{2}.$$

> [!answer]- 原书参考答案（D.0.6 第 5 题，未逐题独立验算）
> **5.** 记 $I_{n} = \int_{0}^{\pi} \frac{\sin x}{1 + \cos^{2} nx} \, dx$.
>
> 第一步：换元 $t = nx$，把积分切成 n 个“整周期”。因 $\cos^{2}t$ 以 $\pi$ 为周期，
>
> $$I_{n}=\frac{1}{n}\int_{0}^{n\pi}\frac{\sin\frac{t}{n}}{1+\cos^{2}t}\mathrm{d}t=\frac{1}{n}\sum_{k=0}^{n-1}\int_{k\pi}^{(k+1)\pi}\frac{\sin\frac{t}{n}}{1+\cos^{2}t}\mathrm{d}t,$$
>
> 而每个整周期上“快变因子”的积分是同一个定值：
>
> $$\int_{k\pi}^{(k+1)\pi}\frac{\mathrm{d}t}{1+\cos^{2}t}=\int_{0}^{\pi}\frac{\mathrm{d}t}{1+\cos^{2}t}=\frac{\pi}{\sqrt{2}}.$$
>
> 第二步: 把缓变的 $\sin \frac{t}{n}$ 换成它在各周期起点的值, 估计余项. 在 $t \in [k\pi, (k+1)\pi]$ 上,
>
> $$\left|\sin\frac{t}{n}-\sin\frac{k\pi}{n}\right|\leqslant\frac{1}{n}\left|t-k\pi\right|\leqslant\frac{\pi}{n},$$
>
> 故
>
> $$\left|I_{n}-\frac{\pi}{\sqrt{2}}\cdot\frac{1}{n}\sum_{k=0}^{n-1}\sin\frac{k\pi}{n}\right|\leqslant\frac{1}{n}\cdot n\cdot\frac{\pi}{n}\cdot\frac{\pi}{\sqrt{2}}=\frac{\pi^{2}}{\sqrt{2}n}\longrightarrow0.$$
>
> 第三步：剩下的和式是标准的定积分定义。
>
> $$\frac{\pi}{\sqrt{2}}\cdot\frac{1}{n}\sum_{k=0}^{n-1}\sin\frac{k\pi}{n}\longrightarrow\frac{\pi}{\sqrt{2}}\cdot\frac{1}{\pi}\int_{0}^{\pi}\sin x\mathrm{d}x=\frac{\pi}{\sqrt{2}}\cdot\frac{2}{\pi}=\sqrt{2}.$$
>
> 于是 $\lim_{n\to\infty}I_n=\sqrt{2}$. (这类题的通法: 先用换元把快变因子化为“整周期”, 用它在整周期上的中值把主部提出来, 缓变的部分再按定积分定义求和.)

## 3.7 升维打击

将函数的大小关系进行积分，变为积分的大小关系，再通过二重积分的换序技巧间接证明不等式，是较为巧妙的一元积分证明题解决思路。该考法在竞赛中出现过1次，且经常在河南省决赛中出现。

**1.** (难度: ★★★) 证明:

$$\sqrt{1-e^{-1}}<\frac{2}{\sqrt{\pi}}\int_{0}^{1}e^{-x^{2}}\mathrm{d}x<\sqrt{1-e^{-2}}.$$

> [!answer]- 原书参考答案（D.0.7 第 1 题，未逐题独立验算）
> **1.** 根号提示”两边平方”; 平方之后两个定积分相乘, 正好把它读成正方形上的二重积分. 被积函数只与 $x^{2} + y^{2}$ 有关, 用内接、外接的两个四分之一圆把正方形夹住即可. 记 $I = \int_{0}^{1} e^{-x^{2}} \, dx$, 则
>
> $$I^{2}=\iint_{0\leqslant x,y\leqslant1}e^{-(x^{2}+y^{2})}\mathrm{d}x\mathrm{d}y.$$
>
> 上界. 正方形包含在四分之一圆 $\left\{x^{2}+y^{2}\leqslant2,x,y\geqslant0\right\}$ 内, 故
>
> $$\begin{aligned}I^{2}&<\iint_{x^{2}+y^{2}\leqslant2,x,y\geqslant0}e^{-(x^{2}+y^{2})}\mathrm{d}x\mathrm{d}y=\int_{0}^{\frac{\pi}{2}}\mathrm{d}\theta\int_{0}^{\sqrt{2}}\rho e^{-\rho^{2}}\mathrm{d}\rho\\&=\frac{\pi}{2}\cdot\frac{1-e^{-2}}{2}=\frac{\pi}{4}\left(1-e^{-2}\right).\end{aligned}$$
>
> 下界. 四分之一圆 $\left\{x^{2}+y^{2}\leqslant1,x,y\geqslant0\right\}$ 包含在正方形内, 故
>
> $$I^{2}>\int_{0}^{\frac{\pi}{2}}\mathrm{d}\theta\int_{0}^{1}\rho e^{-\rho^{2}}\mathrm{d}\rho=\frac{\pi}{4}\left(1-e^{-1}\right).$$
>
> 两边开方、再同乘 $\frac{2}{\sqrt{\pi}}$，即得
>
> $$\sqrt{1-e^{-1}}<\frac{2}{\sqrt{\pi}}\int_{0}^{1}e^{-x^{2}}\mathrm{d}x<\sqrt{1-e^{-2}}.$$
>
> 这是”把定积分的平方升成二重积分”的标准动作:平方 → 二重 → 用区域包含关系放缩 → 极坐标算出两端.凡是看到 $\left( \int_0^1 f(x) \, dx \right)^2$ 与根号成对出现,都可以先想这一步.

**2.** (难度：★★★) 设 $f(x)$ 为实数域上的非负连续函数, 且满足:

$$\int_{x}^{\frac{\pi}{2}}f(t-x)f(t)d t=\cos^{4}x.$$

据此求 $\frac{2}{\pi}\int_{0}^{\frac{\pi}{2}}f(x)dx.$

> [!answer]- 原书参考答案（D.0.7 第 2 题，未逐题独立验算）
> **2.** 第一步：把条件在 $[0,\frac{\pi}{2}]$ 上再积一次. 被积函数 $f(t-x)f(t)$ 中 t 与 x 分不开，逐点放缩无从下手. 把等式两边同时对 x 积分，左边就成了三角形区域上的二重积分：
>
> $$\int_{0}^{\frac{\pi}{2}}\left(\int_{x}^{\frac{\pi}{2}}f(t-x)f(t)\mathrm{d}t\right)\mathrm{d}x=\int_{0}^{\frac{\pi}{2}}\cos^{4}x\mathrm{d}x=\frac{3\pi}{16}.$$
>
> 第二步：交换次序，认出 $\frac{1}{2}F^{2}$.积分区域是 $0\leqslant x\leqslant t\leqslant\frac{\pi}{2}$，交换次序得
>
> $$\int_{0}^{\frac{\pi}{2}}\int_{x}^{\frac{\pi}{2}}f(t-x)f(t)\mathrm{d}t\mathrm{d}x=\int_{0}^{\frac{\pi}{2}}f(t)\left(\int_{0}^{t}f(t-x)\mathrm{d}x\right)\mathrm{d}t.$$
>
> 对固定的 t 作换元 u = t - x，内层积分就是 $\int_{0}^{t} f(u) \, \mathrm{d}u = F(t)$，其中 $F(t) = \int_{0}^{t} f(u) \, \mathrm{d}u$，且 $F(0) = 0$。于是
>
> $$\int_{0}^{\frac{\pi}{2}}F(t)f(t)\mathrm{d}t=\int_{0}^{\frac{\pi}{2}}F(t)\mathrm{d}F(t)=\frac{1}{2}F^{2}\Big(\frac{\pi}{2}\Big).$$
>
> 第三步: 解出结果. 与第一步的 $\frac{3\pi}{16}$ 联立:
>
> $$\frac{1}{2}F^{2}\Big(\frac{\pi}{2}\Big)=\frac{3\pi}{16}\implies F\Big(\frac{\pi}{2}\Big)=\int_{0}^{\frac{\pi}{2}}f(x)\mathrm{d}x=\sqrt{\frac{3\pi}{8}}.$$
>
> 所以
>
> $$\frac{2}{\pi}\int_{0}^{\frac{\pi}{2}}f(x)\mathrm{d}x=\frac{2}{\pi}\sqrt{\frac{3\pi}{8}}=\frac{\sqrt{6}}{2\sqrt{\pi}}=\sqrt{\frac{3}{2\pi}}.$$

**3.** (难度：★★★★★) 设 $f(x)$ 是 $(-\infty, +\infty)$ 上的连续正值函数, 且对任意 $t \in (-\infty, +\infty)$, 都有

$$\int_{-\infty}^{+\infty}e^{-|t-x|}f(x)\mathrm{d}x\leqslant1.$$

证明：对任意 a, b > 0 且 a < b，有

$$\int_{a}^{b}f(x)\mathrm{d}x\leqslant\frac{b-a}{2}+1.$$

> [!answer]- 原书参考答案（D.0.7 第 3 题，未逐题独立验算）
> **3.** 条件是”对每个 $t$ 的一重积分不等式”，逐点放缩无从下手。把 $t$ 在 $[a,b]$ 上再积一次，左边就成了区域上的二重积分；交换次序后把 $x$ 的积分范围收缩到 $[a,b]$，再用 $t = a$、 $t = b$ 两端的条件把带权项控制住。把已知条件在 $t \in [a,b]$ 上积分：
>
> $$\int_{a}^{b}\int_{-\infty}^{+\infty}e^{-|t-x|}f(x)\mathrm{d}x\mathrm{d}t\leqslant b-a.$$
>
> 被积函数非负，交换次序：
>
> $$\int_{-\infty}^{+\infty}f(x)\left(\int_{a}^{b}e^{-|t-x|}\mathrm{d}t\right)\mathrm{d}x\leqslant b-a.$$
>
> 只保留 $x \in [a, b]$ 的那一段（被积函数非负，丢掉的部分 $\geq 0$）：
>
> $$\int_{a}^{b}f(x)\left(\int_{a}^{b}e^{-|t-x|}\mathrm{d}t\right)\mathrm{d}x\leqslant b-a.$$
>
> 当 $x \in [a, b]$ 时
>
> $$\int_{a}^{b}e^{-|t-x|}\mathrm{d}t=\left(1-e^{-(x-a)}\right)+\left(1-e^{-(b-x)}\right)=2-e^{a-x}-e^{x-b},$$
>
> 代入并移项：
>
> $$2\int_{a}^{b}f(x)\mathrm{d}x\leqslant b-a+\int_{a}^{b}\left(e^{a-x}+e^{x-b}\right)f(x)\mathrm{d}x.$$
>
> 再把条件分别取 t = a, t = b:
>
> $$\int_{a}^{b}e^{a-x}f(x)\mathrm{d}x\leqslant\int_{-\infty}^{+\infty}e^{-|a-x|}f(x)\mathrm{d}x\leqslant1,$$
>
> $$\int_{a}^{b}e^{x-b}f(x)\mathrm{d}x\leqslant\int_{-\infty}^{+\infty}e^{-|b-x|}f(x)\mathrm{d}x\leqslant1.$$
>
> 故 $\int_{a}^{b}\left(e^{a-x}+e^{x-b}\right)f(x)\mathrm{d}x\leqslant2$ ,于是
>
> $$2\int_{a}^{b}f(x)\mathrm{d}x\leqslant b-a+2\implies\int_{a}^{b}f(x)\mathrm{d}x\leqslant\frac{b-a+2}{2}.$$
>
> 关键动作有两个: 一是把条件再积一次 (升维), 把“每个 t 的信息”摊成区域的带权信息; 二是减弱积分区间, 把 x 限制在 [a, b] 上, 这样两端的指数权重 $e^{a-x}$、 $e^{x-b}$ 都 $\leq 1$, 可以直接用条件 t = a、t = b 收口.

---

# 强化篇·第四章 多元积分学

## 4.1 物理与几何应用

考察频率并不高的应用题,重点是了解不同应用情境下对应的公式,记住公式并学会用公式,是重中之重.

### 4.1.1 质心

**1.** (难度：★★★) 在空间直角坐标系下, 设 $\Omega$ 是空间曲面

$$(x-8)^{2}+(y-\sin\pi z)^{2}=\sin\pi z,\quad0\leqslant z\leqslant1$$

所围成的空间区域. 现有一个物体全部位于空间 $\Omega$ 内且完全填充空间 $\Omega$，该物体在 $\Omega$ 内任意一点密度 $\rho(x,y,z)=kz(k>0)$.

(1) 求该物体的质量.

(2) 求该物体质心的竖坐标.

> [!answer]- 原书参考答案（E.0.1·质心 第 1 题，未逐题独立验算）
> **1.** 固定 $z$ 时截面是一个圆, 面积是 $\pi \sin \pi z$. 于是三重积分直接降为一维定积分, 两次分部积分即可. 对固定的 $z \in [0,1]$, 区域 $\Omega$ 的截面为
>
> $$(x-8)^{2}+(y-\sin\pi z)^{2}\leqslant\sin\pi z,$$
>
> 这是一个圆, 半径为 $\sqrt{\sin\pi z}$, 面积为 $\pi\sin\pi z$.
>
> (1) 质量
>
> $$M=\iiint_{\Omega}k z\mathrm{d}V=\int_{0}^{1}k z\cdot\pi\sin\pi z\mathrm{d}z=k\pi\int_{0}^{1}z\sin\pi z\mathrm{d}z.$$
>
> 而
>
> $$\int_{0}^{1}z\sin\pi z\mathrm{d}z=\left[-\frac{z\cos\pi z}{\pi}\right]_{0}^{1}+\frac{1}{\pi}\int_{0}^{1}\cos\pi z\mathrm{d}z=\frac{1}{\pi}+\frac{1}{\pi}\cdot0=\frac{1}{\pi},$$
>
> 所以
>
> $$M=k\pi\cdot\frac{1}{\pi}=k.$$
>
> (2) 竖坐标
>
> $$\bar{z}=\frac{1}{M}\iiint_{\Omega}z\cdot k z\mathrm{d}V=\frac{k}{k}\int_{0}^{1}z^{2}\cdot\pi\sin\pi z\mathrm{d}z=\pi\int_{0}^{1}z^{2}\sin\pi z\mathrm{d}z.$$
>
> 两次分部积分：
>
> $$\int_{0}^{1}z^{2}\sin\pi z\mathrm{d}z=\left[-\frac{z^{2}\cos\pi z}{\pi}\right]_{0}^{1}+\frac{2}{\pi}\int_{0}^{1}z\cos\pi z\mathrm{d}z,$$
>
> $$\int_{0}^{1}z\cos\pi z\mathrm{d}z=\left[\frac{z\sin\pi z}{\pi}\right]_{0}^{1}-\frac{1}{\pi}\int_{0}^{1}\sin\pi z\mathrm{d}z=0+\frac{1}{\pi^{2}}\left[\cos\pi z\right]_{0}^{1}=-\frac{2}{\pi^{2}}.$$
>
> 第一项为 $\frac{1}{\pi}$，所以
>
> $$\int_{0}^{1}z^{2}\sin\pi z\mathrm{d}z=\frac{1}{\pi}+\frac{2}{\pi}\left(-\frac{2}{\pi^{2}}\right)=\frac{1}{\pi}-\frac{4}{\pi^{3}}=\frac{\pi^{2}-4}{\pi^{3}},$$
>
> $$\bar{z}=\pi\cdot\frac{\pi^{2}-4}{\pi^{3}}=1-\frac{4}{\pi^{2}}.$$
>
> 截面是圆、且圆的面积只与 $z$ 有关, 就把三重积分写成 $\int \pi \sin \pi z \cdot (\cdots) \, \mathrm{d}z$, 一维问题比换元好用得多.

### 4.1.2 转动惯量

**1.** (难度:★★★★) 设 l 是过原点, 方向为 $(\alpha, \beta, \gamma)$ 的直线, 其中 $\alpha^{2} + \beta^{2} + \gamma^{2} = 1$. 密度为 1 的均匀椭球 $\frac{x^{2}}{a^{2}} + \frac{y^{2}}{b^{2}} + \frac{z^{2}}{c^{2}} \leqslant 1$ 绕直线 l 旋转, 其中 0 < c < b < a.

(1) 求其转动惯量.

(2) 求其转动惯量关于方向 $(\alpha, \beta, \gamma)$ 的最大值和最小值.

> [!answer]- 原书参考答案（E.0.1·转动惯量 第 1 题，未逐题独立验算）
> **1.** 先记住均匀椭球绕三条坐标轴的转动惯量, 再用「方向余弦的组合」写出绕任意过原点直线的转动惯量; 最值问题就变成求一个线性加权的最大最小. 椭球 $\frac{x^{2}}{a^{2}} + \frac{y^{2}}{b^{2}} + \frac{z^{2}}{c^{2}} \leqslant 1$ 的质量为 $M = \frac{4}{3} \pi abc$. 绕三条坐标轴:
>
> $$J_{x}=\iiint_{\Omega}(y^{2}+z^{2})\mathrm{d}V=\frac{4\pi}{15}ab^{3}c+\frac{4\pi}{15}abc^{3}=\frac{M}{5}(b^{2}+c^{2}),$$
>
> $$J_{y}=\frac{M}{5}(c^{2}+a^{2}),\qquad J_{z}=\frac{M}{5}(a^{2}+b^{2}).$$
>
> (1) 设直线 l 的方向余弦为 $(\alpha, \beta, \gamma)$, $\alpha^{2} + \beta^{2} + \gamma^{2} = 1$. 把绕 l 的转动惯量按三个坐标方向分解, 得
>
> $$J_{l}=\alpha^{2}J_{x}+\beta^{2}J_{y}+\gamma^{2}J_{z}=\frac{M}{5}\left[\alpha^{2}(b^{2}+c^{2})+\beta^{2}(c^{2}+a^{2})+\gamma^{2}(a^{2}+b^{2})\right].$$
>
> 用 $M = \frac{4}{3}\pi abc$ 写开, 就是
>
> $$J_{l}=\frac{4\pi a b c}{15}\left[\alpha^{2}(b^{2}+c^{2})+\beta^{2}(c^{2}+a^{2})+\gamma^{2}(a^{2}+b^{2})\right].$$
>
> (2) 把上式整理成
>
> $$J_{l}=\frac{M}{5}\left[a^{2}+b^{2}+c^{2}-\left(a^{2}\alpha^{2}+b^{2}\beta^{2}+c^{2}\gamma^{2}\right)\right].$$
>
> 要把 $J_{l}$ 取最大, 就要让括号里的加权和最小; 由于 0 < c < b < a, 加权和中系数最小的是 $c^{2}$, 故取 $\gamma^{2} = 1$ 时它最小, 等于 $c^{2}$:
>
> $$J_{max}=\frac{M}{5}(a^{2}+b^{2})\qquad( 绕 z 轴 ).$$
>
> 同理，加权和最大时取 $\alpha^{2}=1$ ，等于 $a^{2}$
>
> $$J_{\min}=\frac{M}{5}(b^{2}+c^{2})\qquad( 绕 x 轴 ).$$
>
> 均匀椭球的三条主轴转动惯量要记牢：绕 x 轴是 $\frac{M}{5}(b^{2}+c^{2})$，其余两式轮换；绕任意过原点直线的转动惯量就是这三个数按方向余弦平方加权.

### 4.1.3 万有引力

**1.** (难度：★★★) 设曲面 $\Sigma: z^{2} = x^{2} + y^{2}, 1 \leqslant z \leqslant 2$，其面密度为常数 $\rho$。求在原点处的质量为 1 的质点和 $\Sigma$ 之间的引力（记引力常数为 G）。

> [!answer]- 原书参考答案（E.0.1·万有引力 第 1 题，未逐题独立验算）
> **1.** 圆锥面关于 z 轴对称, 引力只剩 z 方向分量; 把圆锥方程与 dS 一起代入, 根号会整齐地约掉. 质点在原点, $\Sigma$ 关于 z 轴对称, 故 $F_{x} = F_{y} = 0$, 只需算
>
> $$F_{z}=G\iint_{\Sigma}\frac{\rho(z-0)}{\left(x^{2}+y^{2}+z^{2}\right)^{3/2}}\mathrm{d}S=G\rho\iint_{\Sigma}\frac{z}{\left(x^{2}+y^{2}+z^{2}\right)^{3/2}}\mathrm{d}S.$$
>
> 在圆锥 $z = \sqrt{x^{2} + y^{2}} (1 \leqslant z \leqslant 2)$ 上， $x^{2} + y^{2} = z^{2}$，所以
>
> $$\left(x^{2}+y^{2}+z^{2}\right)^{3/2}=\left(2z^{2}\right)^{3/2}=2\sqrt{2}z^{3}.$$
>
> 又 $z_{x}=\frac{x}{z}$, $z_{y}=\frac{y}{z}$, 故
>
> $$\mathrm{d}S=\sqrt{1+z_{x}^{2}+z_{y}^{2}}\mathrm{d}x\mathrm{d}y=\sqrt{1+\frac{x^{2}+y^{2}}{z^{2}}}\mathrm{d}x\mathrm{d}y=\sqrt{2}\mathrm{d}x\mathrm{d}y.$$
>
> 投影区域为 $D: 1 \leq x^{2} + y^{2} \leq 4$。于是
>
> $$F_{z}=G\rho\iint_{D}\frac{z}{2\sqrt{2}z^{3}}\cdot\sqrt{2}\mathrm{d}x\mathrm{d}y=\frac{G\rho}{2}\iint_{D}\frac{\mathrm{d}x\mathrm{d}y}{x^{2}+y^{2}}.$$
>
> 用极坐标：
>
> $$\iint_{D}\frac{\mathrm{d}x\mathrm{d}y}{x^{2}+y^{2}}=\int_{0}^{2\pi}\mathrm{d}\theta\int_{1}^{2}\frac{r}{r^{2}}\mathrm{d}r=2\pi\ln2,$$
>
> 所以
>
> $$F_{z}=G\pi\rho\ln2>0,$$
>
> 即引力大小为 $G\pi\rho\ln2$，方向沿 z 轴指向圆锥面。 $F_z > 0$ 表示引力把原点处的质点往上方（圆锥所在的一侧）拉；这类题的常规套路是「对称性定方向 + 圆锥方程把分母化简」。

## 4.2 挖洞法

考研数学常客，但竞赛中并不经常涉及，仅在第十六届初赛题中出现了一次，还是要作一定了解，以备不时之需。

**1.** (难度: ★★★) 计算曲线积分

$$I=\oint_{L}\frac{x\mathrm{d}y-y\mathrm{d}x}{4x^{2}+y^{2}},$$

其中 L 是以点 $(1,0)$ 为中心，R 为半径的圆周 $(R>1)$，取逆时针方向.

> [!answer]- 原书参考答案（E.0.2 第 1 题，未逐题独立验算）
> **1.** 分母 $4x^{2} + y^{2}$ 只在原点为零，而圆心是 $(1,0)$、半径 R > 1，原点落在圆内，所以要挖洞。洞的形状取“与分母同族”的椭圆 $4x^{2} + y^{2} = \varepsilon^{2}$，这样在洞上分母恒为 $\varepsilon^{2}$。记
>
> $$P=-\frac{y}{4x^{2}+y^{2}},\qquad Q=\frac{x}{4x^{2}+y^{2}},$$
>
> 直接求导得
>
> $$\frac{\partial Q}{\partial x}=\frac{y^{2}-4x^{2}}{\left(4x^{2}+y^{2}\right)^{2}}=\frac{\partial P}{\partial y},$$
>
> 即 Qx - Py = 0. 取 $L_{\varepsilon} : 4x^{2} + y^{2} = \varepsilon^{2}$ (顺时针)，它与 L 围成区域 D，由格林公式
>
> $$\oint_{L_{\varepsilon}+L}P\mathrm{d}x+Q\mathrm{d}y=\iint_{D}0\mathrm{d}x\mathrm{d}y=0\implies I=-\oint_{L_{\varepsilon}}P\mathrm{d}x+Q\mathrm{d}y.$$
>
> 在 $L_{\varepsilon}$上 $4x^{2}+y^{2}=\varepsilon^{2}$，于是
>
> $$\begin{aligned}\oint_{L_{\varepsilon}}P\mathrm{d}x+Q\mathrm{d}y&=\frac{1}{\varepsilon^{2}}\oint_{L_{\varepsilon}}(-y\mathrm{d}x+x\mathrm{d}y)\\&=-\frac{1}{\varepsilon^{2}}\iint_{4x^{2}+y^{2}\leqslant\varepsilon^{2}}2\mathrm{d}x\mathrm{d}y=-\frac{2}{\varepsilon^{2}}\cdot\frac{\pi\varepsilon^{2}}{2}\\&=-\pi.\end{aligned}$$
>
> 所以 $I = \pi$。洞取成”与分母同族”的椭圆最省事：在 $4x^2 + y^2 = \varepsilon^2$ 上分母是常数，积分降成 $\oint(-y\mathrm{d}x + x\mathrm{d}y)$，再用格林公式换成面积 $\frac{\pi\varepsilon^2}{2}$。若挖成圆洞，分母在洞上仍随点变化，反而多出麻烦。

**2.** （难度：★★★）计算第二型曲面积分

$$I=\iint_{\Sigma}\frac{x\mathrm{d}y\mathrm{d}z+y\mathrm{d}z\mathrm{d}x+z\mathrm{d}x\mathrm{d}y}{(x^{2}+y^{2}+z^{2})^{\frac{3}{2}}},$$

其中 $\Sigma$ 是椭球面 $x^{2}+2y^{2}+3z^{2}=1$，方向取外侧.

> [!answer]- 原书参考答案（E.0.2 第 2 题，未逐题独立验算）
> **2.** 第一步：算散度，确认“除原点外处处为零”。记 $r = \sqrt{x^{2} + y^{2} + z^{2}}$，并令
>
> $$P=\frac{x}{r^{3}},\qquad Q=\frac{y}{r^{3}},\qquad R=\frac{z}{r^{3}}.$$
>
> 由
>
> $$\frac{\partial P}{\partial x}=\frac{r^{2}-3x^{2}}{r^{5}},\qquad\frac{\partial Q}{\partial y}=\frac{r^{2}-3y^{2}}{r^{5}},\qquad\frac{\partial R}{\partial z}=\frac{r^{2}-3z^{2}}{r^{5}}$$
>
> 得 $\frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z} = \frac{3r^{2} - 3r^{2}}{r^{5}} = 0 (r > 0)$. 所以只要把原点这个奇点挖掉, 高斯公式就能用.
>
> 第二步：挖洞。取小球面 $\Sigma_{\varepsilon}: x^{2} + y^{2} + z^{2} = \varepsilon^{2}$，定向取内侧（法向量指向球心）。由 $\Sigma$ 与 $\Sigma_{\varepsilon}$ 围成的区域记作 $\Omega$，由高斯公式
>
> $$\iint_{\Sigma}+\iint_{\Sigma_{\varepsilon}}=\iiint_{\Omega}0\mathrm{d}V=0\implies I=-\iint_{\Sigma_{\varepsilon}}.$$
>
> 第三步：在小球面上算出结果。在 $\Sigma_{\varepsilon}$上 $r=\varepsilon$。因为 $\Sigma_{\varepsilon}$取的是内侧，与外侧相差一个负号，再用高斯公式把外侧的积分换成三重积分：
>
> $$\begin{aligned}\iint_{\Sigma_{\varepsilon}}&x\mathrm{d}y\mathrm{d}z+y\mathrm{d}z\mathrm{d}x+z\mathrm{d}x\mathrm{d}y\\&=-\iint_{-\Sigma_{\varepsilon}}x\mathrm{d}y\mathrm{d}z+y\mathrm{d}z\mathrm{d}x+z\mathrm{d}x\mathrm{d}y=-\iiint_{x^{2}+y^{2}+z^{2}\leqslant\varepsilon^{2}}3\mathrm{d}V\\&=-3\cdot\frac{4}{3}\pi\varepsilon^{3}=-4\pi\varepsilon^{3}.\end{aligned}$$
>
> 于是
>
> $$I=-\frac{1}{\varepsilon^{3}}\cdot\left(-4\pi\varepsilon^{3}\right)=4\pi.$$
>
> 注意结果与 $\Sigma$ 的形状无关: 散度为零, 挖洞后 $\Omega$ 上的三重积分就是零, 所以真正起作用的只有“洞”上的积分. 这正是挖洞法最省事的地方.

**3.** （难度：★★★★★）设

$$I_{\alpha}(r)=\int_{C}\frac{y\mathrm{d}x-x\mathrm{d}y}{(x^{2}+y^{2})^{\alpha}},$$

其中 $\alpha$ 为常数，曲线 C 为椭圆 $x^{2}+xy+y^{2}=r^{2}$，取正向，求极限 $\lim_{r\to\infty}I_{\alpha}(r)$.

> [!answer]- 原书参考答案（E.0.2 第 3 题，未逐题独立验算）
> **3.** 第一步：算 $Q_{x}-P_{y}$ 记
>
> $$P=\frac{y}{(x^{2}+y^{2})^{\alpha}},\qquad Q=\frac{-x}{(x^{2}+y^{2})^{\alpha}},$$
>
> 求导得
>
> $$\frac{\partial Q}{\partial x}=\frac{(2\alpha-1)x^{2}-y^{2}}{(x^{2}+y^{2})^{\alpha+1}},\qquad\frac{\partial P}{\partial y}=\frac{x^{2}-(2\alpha-1)y^{2}}{(x^{2}+y^{2})^{\alpha+1}},$$
>
> $$\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=\frac{2(\alpha-1)}{(x^{2}+y^{2})^\alpha}.$$
>
> 原点仍是奇点, 仍要挖洞; 但与上一个例题不同, 这里 $Q_{x}-P_{y}\neq0$, 所以挖洞之后二重积分这一项必须保留.
>
> 第二步: 挖一个圆洞. 取 $C_{\varepsilon}: x^2 + y^2 = \varepsilon^2$, 定向取顺时针 (这样它才是区域 $D_r = \{x^2 + xy + y^2 \leq r^2, x^2 + y^2 \geq \varepsilon^2\}$ 的正向内边界). 由格林公式
>
> $$\oint_{C_{\varepsilon}+C}P\mathrm{d}x+Q\mathrm{d}y=\iint_{D_{r}}\frac{2(\alpha-1)}{(x^{2}+y^{2})^\alpha}\mathrm{d}x\mathrm{d}y,$$
>
> 于是
>
> $$I_{\alpha}(r)=2(\alpha-1)\iint_{D_{r}}\frac{\mathrm{d}x\mathrm{d}y}{(x^{2}+y^{2})^{\alpha}}-\oint_{C_{\varepsilon}}P\mathrm{d}x+Q\mathrm{d}y.$$
>
> 又 $C_{\varepsilon}$ 顺时针，与逆时针相差一个负号，故
>
> $$\begin{aligned}\oint_{C_{\varepsilon}}P\mathrm{d}x+Q\mathrm{d}y&=\frac{1}{\varepsilon^{2\alpha}}\oint_{C_{\varepsilon}}(y\mathrm{d}x-x\mathrm{d}y)\\&=-\frac{1}{\varepsilon^{2\alpha}}\iint_{x^{2}+y^{2}\leqslant\varepsilon^{2}}(-1-1)\mathrm{d}x\mathrm{d}y=\frac{2\pi}{\varepsilon^{2\alpha-2}}.\end{aligned}$$
>
> 第三步：换元把椭圆区域拉成圆区域. 作正交变换
>
> $$x=\frac{u+v}{\sqrt{2}},\qquad y=\frac{u-v}{\sqrt{2}},$$
>
> 它的 Jacobi 行列式为 1，且
>
> $$x^{2}+xy+y^{2}=\frac{3u^{2}+v^{2}}{2},\qquad x^{2}+y^{2}=u^{2}+v^{2}.$$
>
> 再取极坐标 $u = \rho \cos \theta$、 $v = \rho \sin \theta$，区域 $x^2 + xy + y^2 \leq r^2$ 化为
>
> $$\rho\leqslant\frac{r}{\sqrt{\frac{3\cos^{2}\theta+\sin^{2}\theta}{2}}}=:R(\theta),$$
>
> 于是
>
> $$I_{\alpha}(r)=2(\alpha-1)\int_{0}^{2\pi}\int_{\varepsilon}^{R(\theta)}\rho^{1-2\alpha}\mathrm{d}\rho\mathrm{d}\theta-\frac{2\pi}{\varepsilon^{2\alpha-2}}.$$
>
> 由 $\int\rho^{1-2\alpha}d\rho = -\frac{\rho^{2-2\alpha}}{2(\alpha-1)}$ 得
>
> $$I_{\alpha}(r)=-\int_{0}^{2\pi}\left[R(\theta)\right]^{2-2\alpha}\mathrm{d}\theta+2\pi\varepsilon^{2-2\alpha}-\frac{2\pi}{\varepsilon^{2\alpha-2}}.$$
>
> 因为 $\varepsilon^{2-2\alpha} = \varepsilon^{-(2\alpha-2)}$，最后两项正好相消，故
>
> $$I_{\alpha}(r)=-r^{2-2\alpha}\int_{0}^{2\pi}\left(\frac{3\cos^{2}\theta+\sin^{2}\theta}{2}\right)^{\alpha-1}\mathrm{d}\theta.$$
>
> 第四步：讨论参数. 记 $K(\alpha) = \int_{0}^{2\pi}\left(\frac{3\cos^{2}\theta+\sin^{2}\theta}{2}\right)^{\alpha-1}d\theta > 0$，则 $I_{\alpha}(r) = -r^{2-2\alpha}K(\alpha)$ ( $\alpha=1$ 时 $K(1)=2\pi$)，于是
>
> $$\lim_{r\to+\infty}I_{\alpha}(r)=\left\{\begin{aligned}&-\infty,&\alpha<1,\\ &-2\pi,&\alpha=1,\\ &0,&\alpha>1.\end{aligned}\right.$$

## 4.3 构造法

非数竞赛多次出现，通过构造不同的曲线/曲面积分，巧妙化解待解的重积分，相当的优雅简洁。

**1.** (难度:★★★) 设函数 $f(x,y)$ 在区域 $D: x^{2} + y^{2} \leq 1$ 上具有二阶连续偏导数, 且

$$\frac{\partial^{2}f}{\partial x^{2}}+\frac{\partial^{2}f}{\partial y^{2}}=e^{-(x^{2}+y^{2})},$$

证明：

$$\iint_{D}\left(x\frac{\partial f}{\partial x}+y\frac{\partial f}{\partial y}\right)\mathrm{d}x\mathrm{d}y=\frac{\pi}{2e}.$$

> [!answer]- 原书参考答案（E.0.3 第 1 题，未逐题独立验算）
> **1.** 第一步：照着“边界 + 待求式”构造 P, Q. 边界是 $x^{2} + y^{2} = 1$, 第一步把 $x^{2} + y^{2}$ 选进去；待求式里出现 $f_{x}, f_{y}$，第二步就让它出在 Q, P 上. 按模板取
>
> $$Q=(x^{2}+y^{2})f_{x},\qquad P=-(x^{2}+y^{2})f_{y},$$
>
> 则
>
> $$\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=\left(x^{2}+y^{2}\right)\left(f_{x x}+f_{y y}\right)+2\left(x f_{x}+y f_{y}\right).$$
>
> 取 $L: x^{2} + y^{2} = 1$ (正向)，由格林公式
>
> $$\oint_{L}P\mathrm{d}x+Q\mathrm{d}y=\iint_{D}(x^{2}+y^{2})\left(f_{xx}+f_{yy}\right)\mathrm{d}x\mathrm{d}y+2\iint_{D}\left(xf_{x}+yf_{y}\right)\mathrm{d}x\mathrm{d}y.$$
>
> 第二步：在边界上把 $x^{2}+y^{2}$ 换成 1. 在 L 上 $x^{2}+y^{2}=1$，于是
>
> $$\oint_{L}P\mathrm{d}x+Q\mathrm{d}y=\oint_{L}\left(f_{x}\mathrm{d}y-f_{y}\mathrm{d}x\right)=\iint_{D}\left(f_{x x}+f_{y y}\right)\mathrm{d}x\mathrm{d}y,$$
>
> 这一步把曲面积分里的 $x^{2} + y^{2}$ 消掉之后, 正好又能用一次格林公式, 剩下的就是 $f_{xx} + f_{yy}$ 的积分.
>
> 第三步：把两处的积分都算出来。由条件与极坐标，
>
> $$\iint_{D}\left(f_{x x}+f_{y y}\right)\mathrm{d}x\mathrm{d}y=\iint_{D}e^{-(x^{2}+y^{2})}\mathrm{d}x\mathrm{d}y=2\pi\int_{0}^{1}\rho e^{-\rho^{2}}\mathrm{d}\rho=\pi\left(1-e^{-1}\right),$$
>
> $$\begin{aligned}\iint_{D}(x^{2}+y^{2})\left(f_{xx}+f_{yy}\right)\mathrm{d}x\mathrm{d}y&=\iint_{D}(x^{2}+y^{2})e^{-(x^{2}+y^{2})}\mathrm{d}x\mathrm{d}y\\&=2\pi\int_{0}^{1}\rho^{3}e^{-\rho^{2}}\mathrm{d}\rho=\pi-\frac{2\pi}{e}.\end{aligned}$$
>
> 代入第一步的等式:
>
> $$\begin{aligned}\pi\left(1-e^{-1}\right)&=\pi-\frac{2\pi}{e}+2\iint_{D}\left(x f_{x}+y f_{y}\right)\mathrm{d}x\mathrm{d}y\\\Longrightarrow\quad\iint_{D}\left(x f_{x}+y f_{y}\right)\mathrm{d}x\mathrm{d}y&=\frac{\pi}{2e}.\end{aligned}$$

**2.** (难度：★★★) 设函数 $f(x,y)$ 在闭区域 $D=\left\{(x,y)\mid x^{2}+y^{2}\leq1\right\}$ 上具有二阶连续偏导数, 且

$$\frac{\partial^{2}f}{\partial x^{2}}+\frac{\partial^{2}f}{\partial y^{2}}=x^{2}+y^{2},$$

求极限：

$$\lim_{r\to0^{+}}\frac{\iint_{x^{2}+y^{2}\leqslant r^{2}}\left(x\frac{\partial f}{\partial x}+y\frac{\partial f}{\partial y}\right)\mathrm{d}x\mathrm{d}y}{(\tan r-\sin r)^{2}}.$$

> [!answer]- 原书参考答案（E.0.3 第 2 题，未逐题独立验算）
> **2.** 与上一题同一构造，只是把半径4换成变量 r. 取含 $x^{2}+y^{2}$ 因子的 P, Q，在圆周 $x^{2}+y^{2}=r^{2}$ 上这个因子恰好是 $r^{2}$，可以直接提出来再用一次格林公式；于是所有的量都能用 r 表示. 最后与 $(\tan r-\sin r)^{2}$ 比较阶即可. 取
>
> $$P=-\left(x^{2}+y^{2}\right)f_{y},\qquad Q=\left(x^{2}+y^{2}\right)f_{x},$$
>
> 则
>
> $$\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=2\left(x f_{x}+y f_{y}\right)+\left(x^{2}+y^{2}\right)\left(f_{x x}+f_{y y}\right).$$
>
> 记 $L_{r}:x^{2}+y^{2}=r^{2}$（正向）， $D_{r}$为其内部，
>
> $$A(r):=\iint_{D_{r}}\left(x f_{x}+y f_{y}\right)\mathrm{d}x\mathrm{d}y.$$
>
> 由格林公式
>
> $$\oint_{L_{r}}P\mathrm{d}x+Q\mathrm{d}y=2A(r)+\iint_{D_{r}}\left(x^{2}+y^{2}\right)\left(f_{xx}+f_{yy}\right)\mathrm{d}x\mathrm{d}y.$$
>
> 在 $L_{r}$上 $x^{2}+y^{2}=r^{2}$，故
>
> $$\begin{aligned}\oint_{L_{r}}P\mathrm{d}x+Q\mathrm{d}y&=r^{2}\oint_{L_{r}}\left(-f_{y}\mathrm{d}x+f_{x}\mathrm{d}y\right)\\&=r^{2}\iint_{D_{r}}\left(f_{xx}+f_{yy}\right)\mathrm{d}x\mathrm{d}y=r^{2}\iint_{D_{r}}\left(x^{2}+y^{2}\right)\mathrm{d}x\mathrm{d}y=\frac{\pi}{2}r^{6};\end{aligned}$$
>
> 又
>
> $$\iint_{D_{r}}\left(x^{2}+y^{2}\right)\left(f_{xx}+f_{yy}\right)\mathrm{d}x\mathrm{d}y=\iint_{D_{r}}\left(x^{2}+y^{2}\right)^{2}\mathrm{d}x\mathrm{d}y=2\pi\int_{0}^{r}\rho^{5}\mathrm{d}\rho=\frac{\pi}{3}r^{6}.$$
>
> 两式相减得 $2A(r)=\frac{\pi}{2}r^{6}-\frac{\pi}{3}r^{6}=\frac{\pi}{6}r^{6}$，即
>
> $$A(r)=\iint_{x^{2}+y^{2}\leqslant r^{2}}\left(x f_{x}+y f_{y}\right)\mathrm{d}x\mathrm{d}y=\frac{\pi}{12}r^{6}.$$
>
> 再由 $\tan r = r + \frac{r^3}{3} + o(r^3)$、 $\sin r = r - \frac{r^3}{6} + o(r^3)$ 得 $\tan r - \sin r \sim \frac{r^3}{2}$，于是
>
> $$\lim_{r\to0^{+}}\frac{A(r)}{(\tan r-\sin r)^{2}}=\lim_{r\to0^{+}}\frac{\frac{\pi}{12}r^{6}}{\frac{r^{6}}{4}}=\frac{\pi}{3}.$$
>
> 把上一题的"定半径"换成"变半径"是本类题最常见的推广. 要点有两个: 一是构造里的 $x^{2}+y^{2}$ 在圆周上等于 $r^{2}$，可以把 $r^{2}$ 提到积分号外; 二是最后必须把 $(\tan r-\sin r)^{2}$ 的阶写清楚 $(r^{6})$，否则极限算不出来.

**3.** (难度:★★★★) 设函数 $f(x,y)$ 在区域 $D = \{(x,y) \mid x^{2} + y^{2} \leq a^{2}\}$ 上具有一阶连续偏导数, 且满足:

$$f(x,y)\big|_{x^{2}+y^{2}=a^{2}}=a^{2},\qquad\max\left[\left(\frac{\partial f}{\partial x}\right)^{2}+\left(\frac{\partial f}{\partial y}\right)^{2}\right]=a^{2},$$

其中a>0. 证明：

$$\left|\iint_{D}f(x,y)\mathrm{d}x\mathrm{d}y\right|\leqslant\frac{4}{3}\pi a^{4}.$$

> [!answer]- 原书参考答案（E.0.3 第 3 题，未逐题独立验算）
> **3.** 边界上 $f(x,y)=a^{2}$ 是常数, 所以第一步把 $f(x,y)$ 选进构造; 待求式是 $\iint_{D}f(x,y)\,\mathrm{d}x\,\mathrm{d}y$, 用 $P=-yf(x,y), Q=xf(x,y)$ 可以让 $Q_{x}-P_{y}$ 里出现 $2f(x,y)$. 剩下的 $\iint_{D}(xf_{x}+yf_{y})\,\mathrm{d}x\,\mathrm{d}y$ 用柯西-施瓦兹与 $\max\sqrt{f_{x}^{2}+f_{y}^{2}}=a$ 控制. 取
>
> $$P=-y f(x,y),\qquad Q=x f(x,y),$$
>
> 则
>
> $$\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=2f(x,y)+x f_{x}+y f_{y}.$$
>
> 取 $L: x^{2} + y^{2} = a^{2}$ (正向)，由格林公式
>
> $$\oint_{L}P\mathrm{d}x+Q\mathrm{d}y=2\iint_{D}f\mathrm{d}x\mathrm{d}y+\iint_{D}\left(x f_{x}+y f_{y}\right)\mathrm{d}x\mathrm{d}y.$$
>
> 在L上 $f(x,y)=a^{2}$，故
>
> $$\oint_{L}P\mathrm{d}x+Q\mathrm{d}y=a^{2}\oint_{L}\left(-y\mathrm{d}x+x\mathrm{d}y\right)=a^{2}\cdot2\iint_{D}\mathrm{d}x\mathrm{d}y=2\pi a^{4}.$$
>
> 于是
>
> $$2\iint_{D}f\mathrm{d}x\mathrm{d}y=2\pi a^{4}-\iint_{D}\left(x f_{x}+y f_{y}\right)\mathrm{d}x\mathrm{d}y,$$
>
> 由柯西-施瓦兹不等式，
>
> $$\left|x f_{x}+y f_{y}\right|\leqslant\sqrt{x^{2}+y^{2}}\sqrt{f_{x}^{2}+f_{y}^{2}}\leqslant a\sqrt{x^{2}+y^{2}},$$
>
> 故
>
> $$\begin{aligned}\left|\iint_{D}f\mathrm{d}x\mathrm{d}y\right|&\leqslant\pi a^{4}+\frac{a}{2}\iint_{D}\sqrt{x^{2}+y^{2}}\mathrm{d}x\mathrm{d}y\\&=\pi a^{4}+\frac{a}{2}\cdot2\pi\int_{0}^{a}\rho^{2}\mathrm{d}\rho=\pi a^{4}+\frac{1}{3}\pi a^{4}=\frac{4}{3}\pi a^{4}.\end{aligned}$$
>
> 容易犯的错是: 看到边界上 $f(x,y) = a^2$ 就只把 $a^2$ 写进去, 忘了还要“再挑一个别的函数”去凑出 $2f(x,y)$. 正确做法是让构造里既有边界条件 $(f(x,y))$ 、又有能把 $\iint_D f(x,y) \, dx \, dy$ 逼出来的因子 $(x,y)$ . 放缩时用 $\sqrt{x^2 + y^2}$ 而不是常数 a, 才能得到 $\frac{4}{3}\pi a^4$ 而不是更松的界.

**4.** (难度: ★★★★) 设 $\Omega$ 是由光滑的简单封闭曲面 $\Sigma$ 围成的有界闭区域, 函数 $f(x, y, z)$ 在 $\Omega$ 上有连续二阶偏导数, 且 $f(x, y, z)|_{(x, y, z) \in \Sigma} = 0$. 记 $\nabla f$ 为 $f(x, y, z)$ 的梯度, 并令

$$\Delta f=\frac{\partial^{2}f}{\partial x^{2}}+\frac{\partial^{2}f}{\partial y^{2}}+\frac{\partial^{2}f}{\partial z^{2}}.$$

证明：对任意常数 C > 0，恒有：

$$C\iiint_{\Omega}f^{2}\mathrm{d}x\mathrm{d}y\mathrm{d}z+\frac{1}{C}\iiint_{\Omega}(\Delta f)^{2}\mathrm{d}x\mathrm{d}y\mathrm{d}z\geqslant2\iiint_{\Omega}\|\nabla f\|^{2}\mathrm{d}x\mathrm{d}y\mathrm{d}z.$$

> [!answer]- 原书参考答案（E.0.3 第 4 题，未逐题独立验算）
> **4.** 边界上 $f(x,y,z)=0$ ，所以第一步把 $f(x,y,z)$ 选进构造；待求式里同时出现 $f_{x}^{2}+f_{y}^{2}+f_{z}^{2}$ 与 $f(x,y,z)\left(f_{xx}+f_{yy}+f_{zz}\right)$，而 $P=f(x,y,z)f_{x}$ 、 $Q=f(x,y,z)f_{y}$ 、 $R=f(x,y,z)f_{z}$ 的散度正好是两者之和。边界上 $f(x,y,z)=0$ 使通量为零，于是得到 $\iiint_{\Omega}\left(f_{x}^{2}+f_{y}^{2}+f_{z}^{2}\right)\mathrm{d}V=-\iiint_{\Omega}f(x,y,z)\left(f_{xx}+f_{yy}+f_{zz}\right)\mathrm{d}V$；剩下的只是两次基本不等式。取 $\Sigma$ 为外侧，并取 $P=f(x,y,z)f_{x}$ 、 $Q=f(x,y,z)f_{y}$ 、 $R=f(x,y,z)f_{z}$。由 $f(x,y,z)\big|_{\Sigma}=0$ 知
>
> $$\iint_{\Sigma}\left(P\mathrm{d}y\mathrm{d}z+Q\mathrm{d}z\mathrm{d}x+R\mathrm{d}x\mathrm{d}y\right)=0,$$
>
> 而由高斯公式
>
> $$\begin{aligned}\iint_{\Sigma}&\left(P\mathrm{d}y\mathrm{d}z+Q\mathrm{d}z\mathrm{d}x+R\mathrm{d}x\mathrm{d}y\right)\\&=\iiint_{\Omega}\left(f_{x}^{2}+f_{y}^{2}+f_{z}^{2}+f(x,y,z)\left(f_{xx}+f_{yy}+f_{zz}\right)\right)\mathrm{d}V.\end{aligned}$$
>
> 于是
>
> $$\iiint_{\Omega}\left(f^{2}_{x}+f^{2}_{y}+f^{2}_{z}\right)\mathrm{d}V=-\iiint_{\Omega}f(x,y,z)\left(f_{xx}+f_{yy}+f_{zz}\right)\mathrm{d}V.$$
>
> 由基本不等式 (对两个积分用 $Cu + \frac{v}{C} \geqslant 2\sqrt{uv}$) 与柯西-施瓦兹不等式:
>
> $$\begin{aligned}C\iiint_{\Omega}&f^{2}(x,y,z)\mathrm{d}V\\&+\frac{1}{C}\iiint_{\Omega}\left(f_{x x}+f_{y y}+f_{z z}\right)^{2}\mathrm{d}V\\&\geq2\sqrt{\iiint_{\Omega}f^{2}\mathrm{d}V\cdot\iiint_{\Omega}\left(f_{x x}+f_{y y}+f_{z z}\right)^{2}\mathrm{d}V}\\&\geq2\iiint_{\Omega}\left|f(x,y,z)\left(f_{x x}+f_{y y}+f_{z z}\right)\right|\mathrm{d}V\\&\geq2\left|\iiint_{\Omega}f(x,y,z)\left(f_{x x}+f_{y y}+f_{z z}\right)\mathrm{d}V\right|\\&=2\iiint_{\Omega}\left(f_{x}^{2}+f_{y}^{2}+f_{z}^{2}\right)\mathrm{d}V.\end{aligned}$$
>
> 三步走：边界条件 $f(x,y,z)=0$ 选进 P,Q,R $\rightarrow$ 高斯公式给出”偏导平方和”与“ $f(x,y,z)$ 乘偏导二阶和”的恒等式 $\rightarrow$ 再用基本不等式与柯西不等式收口.凡是同时出现 $f(x,y,z)$、 $f_{xx}+f_{yy}+f_{zz}$、 $f_{x}^{2}+f_{y}^{2}+f_{z}^{2}$ 的题,都值得先算一下散度 $(f(x,y,z)f_{x})_{x}+(f(x,y,z)f_{y})_{y}+(f(x,y,z)f_{z})_{z}$.

---

# 强化篇·第五章 无穷级数

## 5.1 常规审敛法

常规的证明,涉及一般的比较、比值审敛法、拉格朗日判别法和对应的代数放缩,核心实际上是想办法把待求级数与p级数进行比较.

**1.** (难度:★★) 证明方程 $x = \tan x$ 有无穷多个正根, 且所有正根 $\{x_n\}$ 可按递增顺序排序为 $0 < x_1 < x_2 < \cdots < x_n$, 并证明级数 $\sum_{n=1}^{\infty} \cot^2 x_n$ 收敛.

> [!answer]- 原书参考答案（F.0.1 第 1 题，未逐题独立验算）
> **1.** 先要在每个 $\left(n\pi-\frac{\pi}{2},n\pi+\frac{\pi}{2}\right)$ 上“抓到”一个根（介值定理），再用 $x_{n}>\left(n\pi-\frac{\pi}{2}\right)$ 把 $\cot^{2}x_{n}=\frac{1}{x_{n}^{2}}$ 控制住——把超越方程的信息换成初等不等式.（1）根的存在性. 记 $f(x)=x-\tan x$. 在每个小区间 $\left(n\pi-\frac{\pi}{2},n\pi+\frac{\pi}{2}\right)$ 上 $f(x)$ 连续，且
>
> $$\lim_{x\to\left(n\pi-\frac{\pi}{2}\right)^{+}}f(x)=+\infty,\qquad\lim_{x\to\left(n\pi+\frac{\pi}{2}\right)^{-}}f(x)=-\infty,$$
>
> 由介值定理，存在 $x_n \in (n\pi - \frac{\pi}{2}, n\pi + \frac{\pi}{2})$ 使 $f(x_n) = 0$，即 $x_n = \tan x_n$。这些区间互不相交，故 $x_n$ 有无穷多个、可按递增顺序排列 $0 < x_1 < x_2 < \cdots$。
>
> (2) 级数收敛. 由 $x_{n}=\tan x_{n}$ 知 $\cot^{2}x_{n}=\frac{1}{\tan^{2}x_{n}}=\frac{1}{x_{n}^{2}}$; 又 $x_{n}>n\pi-\frac{\pi}{2}$, 故
>
> $$0<\cot^{2}x_{n}<\frac{1}{\left(n\pi-\frac{\pi}{2}\right)^{2}}=\frac{1}{\pi^{2}\left(n-\frac{1}{2}\right)^{2}}.$$
>
> 由 $\sum \frac{1}{\left(n - \frac{1}{2}\right)^2}$ 收敛、比较判别法， $\sum \cot^2 x_n$ 收敛。” $x_n = \tan x_n$” 把 $\tan$ 换成了 $x_n$，“ $x_n > n\pi - \frac{\pi}{2}$” 又给出 $x_n$ 的下界，两步之后 $\cot^2 x_n$ 就被一个 p 级数的通项压住了。这种“用方程的根所在区间来估阶”是级数与方程结合的常用手法。

**2.** (难度:★★★) 设 x 是正实数, $B_{n}(x)=\sum_{k=1}^{n}k^{x}$, 判别级数 $\sum_{n=2}^{\infty}\frac{B_{n}(\log_{2}n)}{(n\log_{2}n)^{2}}$ 的敛散性.

> [!answer]- 原书参考答案（F.0.1 第 2 题，未逐题独立验算）
> **2.** 分母里的 $\log_{2} n$ 提示把它换成 $\ln n$; 关键是把 $B_{n}(\log_{n} 2)$ 压成 $2n$——因为 $k \leq n$ 时 $k^{\log_{n} 2} \leq n^{\log_{n} 2} = 2$, 每一项都不超过 2. 剩下的就是与 $\sum \frac{1}{n \ln^{2} n}$ 比较. 由 $k \leq n$ 得 $k^{\log_{n} 2} \leq n^{\log_{n} 2} = 2$, 故
>
> $$B_{n}\left(\log_{n}2\right)=\sum_{k=1}^{n}k^{\log_{n}2}\leqslant2n.$$
>
> 记 $a_{n}=\frac{B_{n}\left(\log_{2}2\right)}{\left(n\log_{2}n\right)^{2}}$ , 则
>
> $$0\leqslant a_{n}\leqslant\frac{2n}{n^{2}\left(\log_{2}n\right)^{2}}=\frac{2}{n\left(\log_{2}n\right)^{2}}=\frac{2(\ln2)^{2}}{n(\ln n)^{2}}.$$
>
> 由积分判别法, $\sum_{n=2}^{+\infty}\frac{1}{n(\ln n)^2}$收敛 $\left(\int_{2}^{+\infty}\frac{dx}{x(\ln x)^2}=\frac{1}{\ln 2}\right)$，故原级数收敛.两处技巧:一是”把 $k^{\log_n 2}$在 $k\leq n$上统一放大成2”，二是”把 $\log_2 n$换成 $\ln n$”（常数因子不影响敛散性）.

**3.** (难度:★★★) 设 $I_{n} = \int_{0}^{\frac{\pi}{4}} \tan^{n} x \, dx$，其中 n 为正整数.

(1) 对于 $n \geqslant 2$，计算 $I_{n} + I_{n-2}$.

(2) 设 p 为实数, 讨论级数 $\sum_{n=1}^{\infty}(-1)^{n}I_{n}^{p}$ 的敛散性.

> [!answer]- 原书参考答案（F.0.1 第 3 题，未逐题独立验算）
> **3.** 第(1)问是送分的: 把 $\tan^{n}x$ 写成 $\tan^{n-2}x(\sec^{2}x-1)$，凑出 $\mathrm{d}(\tan x)$ 就得到 $I_{n}+I_{n-2}$. 第(2)问要先由递推式夹出 $I_{n}\sim\frac{1}{2n}$，再分别用“p级数”和“莱布尼茨判别法”判绝对收敛与条件收敛. (1) 由 $\sec^{2}x=1+\tan^{2}x$,
>
> $$I_{n}=\int_{0}^{\frac{\pi}{4}}\tan^{n-2}x\left(\sec^{2}x-1\right)\mathrm{d}x=\int_{0}^{\frac{\pi}{4}}\tan^{n-2}x\mathrm{d}(\tan x)-I_{n-2},$$
>
> 故 $I_{n} + I_{n-2} = \frac{\tan^{n-1}x}{n-1}\bigg|_{0}^{\frac{\pi}{4}} = \frac{1}{n-1}$.
>
> (2) 在 $[0,\frac{\pi}{4}]$ 上 $\tan x\leq1$ ，故 $I_{n}$ 关于 n 递减. 于是由 $I_{n}+I_{n+2}=\frac{1}{n+1}$ 、 $I_{n}\geq I_{n+2}$ 得
>
> $$\frac{1}{2(n+1)}\leqslant I_{n}\leqslant\frac{1}{2(n-1)}\qquad(n\geqslant2),$$
>
> 即 $I_{n}\sim\frac{1}{2n}$，且 $I_{n}\downarrow0$。
>
> 当 $p > 1$ 时 $I_n^p \leqslant \frac{1}{(2(n-1))^p}$，由 $\sum \frac{1}{n^p}$ 收敛知 $\sum I_n^p$ 收敛，故原级数绝对收敛；
>
> 当 $0 < p \leqslant 1$ 时：$I_n^p \downarrow 0$，由莱布尼茨判别法原级数收敛；但 $\sum I_n^p$ 与 $\sum \frac{1}{n^p}$ 同敛散、发散，故原级数条件收敛；
>
> 当 $p \leqslant 0$ 时 $I_n^p \geqslant 1$，通项不趋于 $0$，级数发散。两处细节：一是递推式只给出 $I_n + I_{n-2}$，要靠单调性把它夹成 $I_n \sim \frac{1}{2n}$；二是 $p \leqslant 0$ 的情形别忘了（通项不趋于 $0$）。

**4.** (难度:★★★) 设数列 $\{F_{n}\}$ 满足 $F_{0}=1, F_{1}=1, F_{n}=F_{n-1}+F_{n-2} (n \geqslant 2)$.

(1) 证明: 当 $n \geqslant 1$ 时, $\left(\frac{3}{2}\right)^{n-1} \leqslant F_{n} \leqslant 2^{n-1}$.

(2) 讨论级数 $\sum_{n=0}^{\infty}\frac{1}{F_{n}}$ 和 $\sum_{n=2}^{\infty}\frac{1}{\ln F_{n}}$ 的敛散性.

> [!answer]- 原书参考答案（F.0.1 第 4 题，未逐题独立验算）
> **4.** 第(1)问是“用递推式做归纳放缩”: 由 $F_{n}=F_{n-1}+F_{n-2}$ 与 $F_{n-1}\geqslant F_{n-2}$ 得 $F_{n}\leqslant2F_{n-1}$，由 $F_{n-2}\leqslant\frac{1}{2}F_{n-1}$ 得 $F_{n}\geqslant\frac{3}{2}F_{n-1}$，累乘即得. 第(2)问直接比较——注意除法的方向. (1) 由 $F_{n}=F_{n-1}+F_{n-2}>F_{n-1}$ 知 $\{F_{n}\}$ 递增，故 $F_{n-2}\leqslant F_{n-1}(n\geqslant2)$. 于是
>
> $$F_{n}=F_{n-1}+F_{n-2}\leqslant2F_{n-1},\qquad F_{n}=F_{n-1}+F_{n-2}\geqslant F_{n-1}+\frac{1}{2}F_{n-1}=\frac{3}{2}F_{n-1}.$$
>
> 分别累乘（并用 $F_{1}=1$）即得 $\left(\frac{3}{2}\right)^{n-1}\leqslant F_{n}\leqslant2^{n-1}\left(n\geqslant1\right)$
>
> (2) 由 $F_{n} \geqslant \left(\frac{3}{2}\right)^{n-1}$ 得 $\frac{1}{F_{n}} \leqslant \left(\frac{2}{3}\right)^{n-1}$，而 $\sum \left(\frac{2}{3}\right)^{n-1}$ 收敛，故 $\sum \frac{1}{F_{n}}$ 收敛.
>
> 由 $F_{n} \leqslant 2^{n-1}$ 得 $\ln F_{n} \leqslant (n-1)\ln2$，故 $\frac{1}{\ln F_{n}} \geqslant \frac{1}{(n-1)\ln2} (n \geqslant 2)$，而 $\sum \frac{1}{(n-1)\ln2}$ 发散，故 $\sum \frac{1}{\ln F_{n}}$ 发散。递归数列“估阶”的通用套路：用递推式把 $F_{n}$ 与 $F_{n-1}$ 的大小关系压成一个常数倍，再累乘。放缩方向决定结论方向——上界给“收敛”，下界给“发散”。

**5.** (难度:★★★) 设级数 $\sum_{n=1}^{\infty} u_{n}$ 各项均为正数, $\{v_{n}\}$ 为一正实数列, 记 $a_{n} = \frac{u_{n} v_{n}}{u_{n+1}} - v_{n+1}$, 已知 $\lim_{n \to \infty} a_{n} = a$, a 为有限正数或正无穷, 证明级数 $\sum_{n=1}^{\infty} u_{n}$ 收敛.

> [!answer]- 原书参考答案（F.0.1 第 5 题，未逐题独立验算）
> **5.** $a_{n}$ 的分子是 $u_{n}v_{n}$ 的差分，而 $a_{n}\to a>0$ 说明这个差分是正的，于是 $\{u_{n}v_{n}\}$ 从某项起单调递减；只要它还有下界就收敛，差分之和也跟着收敛——剩下的只是把 $u_{n+1}$ 与差分之比用 $a_{n}$ 的极限控制住. 记 $b_{n}=u_{n}v_{n}$. 由 $\lim_{n\to\infty}a_{n}=a>0$, 存在 $N$, 使 $n>N$ 时 $a_{n}>\frac{a}{2}>0$ ($a=+\infty$ 时取 $a_{n}>2$), 于是
>
> $$b_{n}-b_{n+1}=a_{n}u_{n+1}>0\qquad(n>N),$$
>
> 即 $\{b_{n}\}$从第N项起单调递减;又 $b_{n}=u_{n}v_{n}>0$,故 $\{b_{n}\}$收敛,从而 $\sum_{k>N}(b_{k}-b_{k+1})$收敛.
>
> (i) a 为有限正数. 因为 $\lim_{n\to\infty}\frac{a_n}{a}=1$ , 而 $b_n-b_{n+1}=a_n u_{n+1}$，由极限形式的比较判别法， $\sum u_{n+1}$ 与 $\sum(b_n-b_{n+1})$ 同敛散，故 $\sum u_n$ 收敛.
>
> (ii) $a = +\infty$. 此时 n 充分大时 $a_{n} \geqslant 2$, 故
>
> $$u_{n+1}\leqslant\frac{1}{2}\left(b_{n}-b_{n+1}\right)\Longrightarrow\sum_{k=N+1}^{n}u_{k+1}\leqslant\frac{1}{2}\left(b_{N+1}-b_{n+1}\right)\leqslant\frac{1}{2}b_{N+1},$$
>
> 部分和有界， $\sum u_{n}$ 收敛。两种情形共用同一个思想：把待求级数 $\sum u_{n}$ 与“已知收敛的差分级数 $\sum(b_{n}-b_{n+1})$”作比较。需要说明的是，论证用到了 $u_{n}v_{n}>0$ （保证差分之和收敛）；若允许 $v_{n}<0$ 任意取值，结论不成立，例如 $u_{n}=\frac{1}{n}$， $v_{n}=-n\ln n$ 时 $a_{n}\rightarrow1>0$，但 $\sum u_{n}$ 发散。

**6.** (难度:★★★) 设 $\{u_n\}, \{c_n\}$ 为正实数列, 试证明:

(1) 若对所有的正整数 n，满足 $c_{n}u_{n}-c_{n+1}u_{n+1}\leqslant0$，且 $\sum_{n=1}^{\infty}\frac{1}{c_{n}}$ 发散，则级数 $\sum_{n=1}^{\infty}u_{n}$ 也发散.

(2) 若对所有的正整数 n，满足 $c_{n}\frac{u_{n}}{u_{n+1}}-c_{n+1}\geqslant a(a>0)$，且 $\sum_{n=1}^{\infty}\frac{1}{c_{n}}$ 收敛，则级数 $\sum_{n=1}^{\infty}u_{n}$ 也收敛.

> [!answer]- 原书参考答案（F.0.1 第 6 题，未逐题独立验算）
> **6.** 两问都是“把 $c_n$ 当成对照级数”：(1) 条件说明 $\{c_n u_n\}$ 单调递增，于是 $u_n$ 与 $\frac{1}{c_n}$ 的比就是 $c_n u_n$，同阶；(2) 条件说明 $c_n u_n$ 每次下降至少 $a u_{n+1}$，累加就给出 $\sum u_n$ 的上界。(1) 由 $c_n u_n \leq c_{n+1} u_{n+1}$ 知 $\{c_n u_n\}$ 单调递增，设极限为 $A \in (0, +\infty)$。
>
> 若 $A$ 有限：则 $\lim_{n \to \infty} \frac{u_n}{1/c_n} = \lim_{n \to \infty} c_n u_n = A > 0$，由极限形式的比较判别法， $\sum u_n$ 与 $\sum \frac{1}{c_n}$ 同敛散，故 $\sum u_n$ 发散。
>
> 若 $A = +\infty$: 则 $\frac{1/c_n}{u_n} = \frac{1}{c_n u_n} \to 0$, 即 $u_n$ 比 $\frac{1}{c_n}$ 至少“大一阶”；由 $\sum \frac{1}{c_n}$ 发散知 $\sum u_n$ 也发散.
>
> (2) 由 $c_{n}\frac{u_{n}}{u_{n+1}}-c_{n+1}\geqslant a$ 得
>
> $$c_{n}u_{n}-c_{n+1}u_{n+1}\geqslant a u_{n+1}>0,$$
>
> 故 $\{c_{n}u_{n}\}$ 单调递减且为正，有极限. 对 $k=1,\ldots,n$ 累加：
>
> $$a\sum_{k=1}^{n}u_{k+1}\leqslant c_{1}u_{1}-c_{n+1}u_{n+1}<c_{1}u_{1},$$
>
> 即 $\sum_{k=1}^{n+1} u_k \leqslant u_1 + \frac{c_1 u_1}{a}$ 有界，故 $\sum u_n$ 收敛. (1) 是“用商比较”，要分“极限有限”和“极限为 $+ \infty$”两种情形；(2) 是“用差分给出 $\sum u_n$ 的有界性”. 这两问合起来就是 Kummer 型判敛法的基本框架.

**7.** (难度:★★★★) 设 $a_{n}=\int_{0}^{\frac{\pi}{2}}x\left(\frac{\sin nx}{\sin x}\right)^{3}dx, n=1,2,\ldots$ ，探究 $\sum_{n=1}^{\infty}\frac{1}{a_{n}}$ 的敛散性.

> [!answer]- 原书参考答案（F.0.1 第 7 题，未逐题独立验算）
> **7.** 第一步：先证明 $a_{n}$ 与 n 同阶（上界）. 沿用“待定分点、两段放缩”的做法：取 $\delta_{n} = \frac{\pi}{2n}$，把 $\left[0, \frac{\pi}{2}\right]$ 拆成两段.
>
> 近段 $(0 < x \leqslant \delta_{n})$ 用 $\sin nx \leqslant n \sin x$ $(0 < x < \frac{\pi}{2})$，故 $\left( \frac{\sin nx}{\sin x} \right)^{3} \leqslant n^{3}$，
>
> $$\int_{0}^{\delta_{n}}x\left(\frac{\sin nx}{\sin x}\right)^{3}\mathrm{d}x\leqslant n^{3}\int_{0}^{\delta_{n}}x\mathrm{d}x=\frac{n^{3}\delta_{n}^{2}}{2}=\frac{\pi^{2}}{8}n.$$
>
> 远段 $\left(\delta_{n}\leqslant x\leqslant\frac{\pi}{2}\right)$ 用割线 $\sin x\geqslant\frac{2}{\pi}x$ ，故 $\left(\frac{\sin nx}{\sin x}\right)^{3}\leqslant\left(\frac{\pi}{2x}\right)^{3}$
>
> $$\int_{\delta_{n}}^{\frac{\pi}{2}}x\left(\frac{\sin nx}{\sin x}\right)^{3}\mathrm{d}x\leqslant\frac{\pi^{3}}{8}\int_{\delta_{n}}^{\frac{\pi}{2}}\frac{\mathrm{d}x}{x^{2}}=\frac{\pi^{3}}{8}\left(\frac{1}{\delta_{n}}-\frac{2}{\pi}\right)=\frac{\pi^{2}}{4}\left(n-1\right).$$
>
> 两段相加得 $a_{n} \leqslant Cn$，其中 $C = \frac{\pi^{2}}{8} + \frac{\pi^{2}}{4} = \frac{3\pi^{2}}{8}$ 与 n 无关.
>
> 第二步: 下界. 由 $\sin x \leqslant x$ 与 $\sin t \geqslant \frac{2}{\pi}t$ $(t \in \left[0, \frac{\pi}{2}\right])$, 当 $0 < x \leqslant \frac{\pi}{2n}$ 时 $nx \in \left(0, \frac{\pi}{2}\right]$, 于是
>
> $$\frac{\sin nx}{\sin x}\geqslant\frac{\frac{2}{\pi}\cdot nx}{x}=\frac{2n}{\pi},\qquad\int_{0}^{\frac{\pi}{2n}}x\left(\frac{\sin nx}{\sin x}\right)^{3}\mathrm{d}x\geqslant\left(\frac{2n}{\pi}\right)^{3}\cdot\frac{1}{2}\left(\frac{\pi}{2n}\right)^{2}=\frac{n}{\pi}.$$
>
> 故 $\frac{n}{\pi}\leq a_{n}\leq\frac{3\pi^{2}}{8}n.$
>
> 第三步：比较判别. 由第一步、第二步, $\frac{1}{a_{n}}$与 $\frac{1}{n}$同阶：
>
> $$\frac{8}{3\pi^{2}}\cdot\frac{1}{n}\leqslant\frac{1}{a_{n}}\leqslant\frac{\pi}{n}.$$
>
> 而调和级数 $\sum_{n=1}^{\infty}\frac{1}{n}$ 发散，故 $\sum_{n=1}^{\infty}\frac{1}{a_{n}}$ 发散.

**8.** （难度：★★★★）设 $\{u_{n}\}$是正数列，满足 $\frac{u_{n+1}}{u_{n}}=1-\frac{\alpha}{n}+O\left(\frac{1}{n^{\beta}}\right)$，其中 $\alpha>0,\beta>1$.

（1）对于 $v_{n}=n^{\alpha}u_{n}$，判断级数 $\sum_{n=1}^{\infty}\ln\frac{v_{n+1}}{v_{n}}$ 的敛散性.

(2) 讨论级数 $\sum_{n=1}^{\infty} u_{n}$ 的敛散性.

> [!answer]- 原书参考答案（F.0.1 第 8 题，未逐题独立验算）
> **8.** 条件给的是”比值的二阶展开”，故套路是取对数读阶：把 $v_{n}=n^{\alpha}u_{n}$代进去， $\alpha\ln(1+\frac{1}{n})$与 $\ln(1-\frac{\alpha}{n}+O(n^{-\beta}))$中的一次项正好相消，只剩 $-\frac{\alpha(\alpha+1)}{2n^{2}}$起主导——于是 $\sum\ln\frac{v_{n+1}}{v_{n}}$收敛， $v_{n}$有正极限，结论随之而来。(1)由 $v_{n}=n^{\alpha}u_{n}$
>
> $$\ln\frac{v_{n+1}}{v_{n}}=\alpha\ln\left(1+\frac{1}{n}\right)+\ln\left(1-\frac{\alpha}{n}+O\left(\frac{1}{n^{\beta}}\right)\right).$$
>
> 用 $\ln(1+x)=x-\frac{x^{2}}{2}+O(x^{3})$:
>
> $$\alpha\ln\left(1+\frac{1}{n}\right)=\frac{\alpha}{n}-\frac{\alpha}{2n^{2}}+O\left(\frac{1}{n^{3}}\right),$$
>
> $$\ln\left(1-\frac{\alpha}{n}+O\left(\frac{1}{n^{\beta}}\right)\right)=-\frac{\alpha}{n}-\frac{\alpha^{2}}{2n^{2}}+O\left(\frac{1}{n^{\min(\beta,3)}}\right).$$
>
> 两式相加，一次项相消：
>
> $$\ln\frac{v_{n+1}}{v_{n}}=-\frac{\alpha(\alpha+1)}{2n^{2}}+O\left(\frac{1}{n^{\min(\beta,3)}}\right).$$
>
> 由于 $\min(\beta,3)>1$，右端是绝对可和的，故 $\sum\ln\frac{v_{n+1}}{v_n}$ 收敛。
>
> (2) 裂项：
>
> $$\sum_{k=1}^{n-1}\ln\frac{v_{k+1}}{v_{k}}=\ln v_{n}-\ln v_{1},$$
>
> 由(1)的收敛性知 $\ln v_{n}$收敛，即 $v_{n}\to C>0$。于是
>
> $$u_{n}=\frac{v_{n}}{n^{\alpha}}\sim\frac{C}{n^{\alpha}},$$
>
> 故 $\sum u_n$ 与 $\sum \frac{1}{n^\alpha}$ 同敛散: $\alpha > 1$ 时收敛, $0 < \alpha \leq 1$ 时发散. 本题是"Raabe 型条件" ( $\S6.2$ 例题) 的升级版: 那次只到一阶, 这次带高阶余项. 核心动作始终是"取对数 $\rightarrow$ 展开到二次项 $\rightarrow$ 累加".

## 5.2 定义类审敛

定义类的证明基于极限的基本定义,用 $\varepsilon-N$语言进行简单的放缩证明.必要时会涉及柯西收敛准则、阿贝尔变换等重要定理的应用.题目难度取决于对定义本身的理解,算是非常合格的压轴考察方向.

**1.** (难度:★★★★) 设级数 $\sum_{n=1}^{\infty} u_{n} (u_{n} > 0)$ 发散, 又设 $S_{n} = \sum_{k=1}^{n} u_{k}$, 证明:

(1) $\sum_{n=1}^{\infty}\frac{u_{n}}{S_{n}}$ 发散.

(2) $\sum_{n=1}^{\infty}\frac{u_{n}}{S_{n}^{2}}$ 收敛.

> [!answer]- 原书参考答案（F.0.2 第 1 题，未逐题独立验算）
> **1.** 思路. 两问的通项都含 $S_n$，而 $S_n \to \infty$（因为 $\sum u_n$ 发散）. 第（1）问要保持“发散”，用柯西收敛准则最合适: 只要能找到任意靠后的一段（而不是一项）和恒大于某个正数，就发散. 第（2）问要保持“收敛”，用拉格朗日中值定理把 $\frac{u_n}{S_n^2}$ 认成 $-\frac{1}{x}$ 在 $S_{n-1}, S_n$ 上的差（因为 $\left(\frac{1}{x}\right)' = -\frac{1}{x^2}$，求导正好给不出 $S_n^2$），于是“一项”被换成“一个望远镜”，累加即可.
>
> (1) 由 $\sum u_n$ 发散、 $u_n > 0$ 知 $S_n \to \infty$。于是对任意固定的 $n$，可取 $p$ 使 $S_{n+p} > 2S_n$。由 $u_k > 0$、 $S_k \leq S_{n+p}$ ( $n \leq k \leq n+p$)，
>
> $$\sum_{k=n}^{n+p}\frac{u_{k}}{S_{k}}>\frac{1}{S_{n+p}}\sum_{k=n}^{n+p}u_{k}=\frac{S_{n+p}-S_{n-1}}{S_{n+p}}=1-\frac{S_{n-1}}{S_{n+p}}>1-\frac{1}{2}=\frac{1}{2}.$$
>
> 由柯西收敛准则， $\sum \frac{u_{n}}{S_{n}}$ 发散.
>
> (2) 取 $g(x) = -\frac{1}{x}$. 对 $n \geqslant 2$, 由拉格朗日中值定理, 存在 $\xi_n \in (S_{n-1}, S_n)$, 使
>
> $$g(S_{n})-g(S_{n-1})=\left(S_{n}-S_{n-1}\right)g^{\prime}(\xi_{n})=\frac{u_{n}}{\xi_{n}^{2}}\geqslant\frac{u_{n}}{S_{n}^{2}}.$$
>
> (注意 $\xi_{n} \leqslant S_{n}$，所以 $\frac{1}{\xi_{n}^{2}} \geqslant \frac{1}{S_{n}^{2}}$——把 $\xi_{n}$ 换成 $S_{n}$ 是放大.) 求和：
>
> $$\sum_{k=1}^{n}\frac{u_{k}}{S_{k}^{2}}=\frac{u_{1}}{S_{1}^{2}}+\sum_{k=2}^{n}\frac{u_{k}}{S_{k}^{2}}\leqslant\frac{1}{u_{1}}+g(S_{n})-g(S_{1})=\frac{2}{u_{1}}-\frac{1}{S_{n}}<\frac{2}{u_{1}}.$$
>
> 故部分和有界， $\sum\frac{u_{n}}{S_{n}^{2}}$ 收敛.

**2.** (难度:★★★★) 设 $\{u_{n}\}$ 是单调增加的正数列, 证明级数 $\sum_{n=1}^{\infty}\left(1-\frac{u_{n}}{u_{n+1}}\right)$ 收敛的充要条件是 $\{u_{n}\}$ 有上界.

> [!answer]- 原书参考答案（F.0.2 第 2 题，未逐题独立验算）
> **2.** 通项写成 $\frac{u_{n+1}-u_{n}}{u_{n+1}}$，分子是“差分、可望远镜相消”，分母需要换成一个不依赖于 n 的常数——这就把“上界”和“收敛”联系起来了。必要性用柯西收敛准则：若 $u_{n}$ 无上界，就能找到一段使部分和恒大于 $\frac{1}{2}$。充分性（ $u_{n}$ 有上界 $\Rightarrow \sum \left(1 - \frac{u_{n}}{u_{n+1}}\right)$ 收敛）。设 $u_{n} \leq M$。由 $u_{n}$ 单调增加有上界， $\{u_{n}\}$ 收敛，故 $\sum (u_{n+1} - u_{n})$ 收敛。又 $u_{n+1} \geq u_{1} > 0$，故
>
> $$0\leqslant1-\frac{u_{n}}{u_{n+1}}=\frac{u_{n+1}-u_{n}}{u_{n+1}}\leqslant\frac{u_{n+1}-u_{n}}{u_{1}},$$
>
> 于是部分和
>
> $$\sum_{k=1}^{n}\left(1-\frac{u_{k}}{u_{k+1}}\right)\leqslant\frac{u_{n+1}-u_{1}}{u_{1}}\leqslant\frac{M-u_{1}}{u_{1}},$$
>
> 有界，从而级数收敛.
>
> 必要性（级数收敛 $\Rightarrow u_n$ 有上界）. 反设 $u_n$ 无上界，则由单调增加知 $u_n \to \infty$. 于是对任意 $n$，存在 $p$ 使 $u_{n+p} > 2u_n$. 由 $u_k \leq u_{n+p+1}$ ( $k \leq n + p + 1$)，
>
> $$\begin{aligned}\sum_{k=n}^{n+p}\left(1-\frac{u_{k}}{u_{k+1}}\right)&=\sum_{k=n}^{n+p}\frac{u_{k+1}-u_{k}}{u_{k+1}}>\frac{\sum\limits_{k=n}^{n+p}\left(u_{k+1}-u_{k}\right)}{u_{n+p+1}}\\&=\frac{u_{n+p+1}-u_{n}}{u_{n+p+1}}=1-\frac{u_{n}}{u_{n+p+1}}>\frac{1}{2}.\end{aligned}$$
>
> 这说明级数不满足柯西收敛准则，与“级数收敛”矛盾。故 $u_{n}$ 有上界。充分性靠“分母换成 $u_{1}$”，必要性靠“柯西收敛准则找到一段和”。这类“级数收敛 $\Leftrightarrow$ 数列有界”的等价命题，最好把两个方向的着眼点分别记牢：一边比大小，一边找反例段。

**3.** (难度:★★★) 设 $0 < a_n < 1$, $n = 1, 2, \ldots$, 且 $\lim_{n \to \infty} \frac{\ln \frac{1}{a_n}}{\ln n} = q$, $q$ 为有限数或无穷.

(1) 证明: 当 q > 1 时级数 $\sum_{n=1}^{\infty} a_{n}$ 收敛; 当 q < 1 时级数 $\sum_{n=1}^{\infty} a_{n}$ 发散.

(2) 讨论 q = 1 时级数 $\sum_{n=1}^{\infty} a_{n}$ 的敛散性.

> [!answer]- 原书参考答案（F.0.2 第 3 题，未逐题独立验算）
> **3.** $\frac{\ln\frac{1}{a_n}}{\ln n}=q$ 的意思是“ $\frac{1}{a_n}$ 关于 n 是 q 次幂量级”，把它翻回 $a_n$ 就是 $a_n$ 与 $\frac{1}{n^q}$ 同阶. 用极限语言把这个“同阶”写成不等式 $n^{-(q+\varepsilon)}<a_n<n^{-(q-\varepsilon)}$，两端都是 p 级数，结论立得；q=1 时两端的指数都会退化成 1，说明临界情形要另找例子.(1) 对任意 $\varepsilon>0$，存在 N，使 n>N 时
>
> $$\left|\frac{\ln\frac{1}{a_{n}}}{\ln n}-q\right|<\varepsilon\implies\frac{1}{n^{q+\varepsilon}}<a_{n}<\frac{1}{n^{q-\varepsilon}}.$$
>
> 若 $q > 1$，取 $\varepsilon = \frac{q - 1}{2}$，则 $a_n < \frac{1}{n^{1 + \frac{q - 1}{2}}}$，由比较判别法 $\sum a_n$ 收敛。
>
> 若 $q < 1$，取 $\varepsilon = \frac{1 - q}{2}$，则 $a_n > \frac{1}{n^{1 - \frac{1 - q}{2}}}$，由比较判别法 $\sum a_n$ 发散。
>
> (2) q = 1 时敛散性不定. 取 $a_{n} = \frac{1}{n \ln^{2} n}$, 则 $\frac{\ln \frac{1}{a_{n}}}{\ln n} = \frac{\ln n + 2 \ln \ln n}{\ln n} \to 1$, 而 $\sum \frac{1}{n \ln^{2} n}$ 收敛;
>
> 取 $a_{n}=\frac{1}{n\ln n}$，则 $\frac{\ln\frac{1}{a_{n}}}{\ln n}=\frac{\ln n+\ln\ln n}{\ln n}\rightarrow1$，而 $\sum\frac{1}{n\ln n}$ 发散.
>
> 故 q = 1 时无法由 $\frac{\ln \frac{1}{a_n}}{\ln n}$ 的极限判断敛散性." 取对数读阶" 是把幂指结构变成 p 级数的标准桥梁. q = 1 正好落在临界位置: 对数因子的阶变成了决定因素, 所以必须用两个反例说明" 不定".

**4.** (难度:★★★) $\sum_{n=1}^{\infty}a_{n}$ 与 $\sum_{n=1}^{\infty}b_{n}$ 为正项级数, 证明:

(1) 若 $\lim_{n\to\infty}\left(\frac{a_n}{a_{n+1}b_n}-\frac{1}{b_{n+1}}\right)>0$，则 $\sum_{n=1}^{\infty}a_n$ 收敛.

(2) 若 $\lim_{n\to\infty}\left(\frac{a_n}{a_{n+1}b_n}-\frac{1}{b_{n+1}}\right)<0$ , 且 $\sum_{n=1}^{\infty}b_n$ 发散, 则 $\sum_{n=1}^{\infty}a_n$ 发散.

> [!answer]- 原书参考答案（F.0.2 第 4 题，未逐题独立验算）
> **4.** 条件里的主项是 $\frac{a_{n}}{a_{n+1}b_{n}}$，而 $\frac{1}{b_{n+1}}$ 是“跟着来的”；把它整理成 $\frac{1}{a_{n+1}}\left(\frac{a_{n}}{b_{n}}-\frac{a_{n+1}}{b_{n+1}}\right)$
>
> 就能看出: 极限的符号决定了 $\left\{\frac{a_{n}}{b_{n}}\right\}$ 的变化方向, 再加上“极限保号性”, 就能把 $a_{n+1}$ 用两个 $\frac{a_{k}}{b_{k}}$ 的差控制住, 从而对 $a_{n}$ 求和. 注意
>
> $$\frac{a_{n}}{a_{n+1}b_{n}}-\frac{1}{b_{n+1}}=\frac{1}{a_{n+1}}\left(\frac{a_{n}}{b_{n}}-\frac{a_{n+1}}{b_{n+1}}\right).$$
>
> （1）设该极限为 A > 0. 由极限的保号性，存在 N，使 n > N 时
>
> $$\frac{1}{a_{n+1}}\left(\frac{a_{n}}{b_{n}}-\frac{a_{n+1}}{b_{n+1}}\right)>\frac{A}{2}>0,$$
>
> 即 $\frac{a_{n}}{b_{n}}>\frac{a_{n+1}}{b_{n+1}}\quad(n>N)$，故 $\left\{\frac{a_{n}}{b_{n}}\right\}$从第N项起单调递减且为正，从而收敛。又
>
> $$a_{n+1}<\frac{2}{A}\left(\frac{a_{n}}{b_{n}}-\frac{a_{n+1}}{b_{n+1}}\right),$$
>
> 对 $n = N + 1, \ldots, m$ 求和:
>
> $$\sum_{k=N+1}^{m}a_{k+1}<\frac{2}{A}\left(\frac{a_{N+1}}{b_{N+1}}-\frac{a_{m+1}}{b_{m+1}}\right)<\frac{2}{A}\cdot\frac{a_{N+1}}{b_{N+1}}.$$
>
> 故部分和有界， $\sum a_{n}$ 收敛.
>
> (2) 设该极限 < 0. 由保号性，存在 N，使 n > N 时
>
> $$\frac{1}{a_{n+1}}\left(\frac{a_{n}}{b_{n}}-\frac{a_{n+1}}{b_{n+1}}\right)<0\implies a_{n+1}>\frac{b_{n+1}}{b_{n}}a_{n},$$
>
> 反复使用得 $a_{n} > \frac{a_{N}}{b_{N}} b_{n} (n > N)$. 于是
>
> $$\sum_{k=N+1}^{m}a_{k}>\frac{a_{N}}{b_{N}}\sum_{k=N+1}^{m}b_{k},$$
>
> 由 $\sum b_n$ 发散知 $\sum a_n$ 发散. 本题的两次判断都只用“保号性”而没有用极限的值——题设只给了符号, 没给具体极限, 这正是保号性最适合的场合.

**5.** (难度:★★★★★) 设对于任何收敛于 0 的序列 $\{x_{n}\}$，级数 $\sum_{n=1}^{\infty}a_{n}x_{n}$ 都是收敛的，由此证明级数 $\sum_{n=1}^{\infty}|a_{n}|$ 收敛.

> [!answer]- 原书参考答案（F.0.2 第 5 题，未逐题独立验算）
> **5.** 要证明的结论是“ $\sum|a_n|$收敛”，而条件只给了“对一切 $x_n \to 0$， $\sum a_nx_n$收敛”。正面不好下手，就反证+构造反例序列：把 $|a_n|$的贡献按“分段”集中起来，在第 $i$段里统一取 $x_n = \frac{\mathrm{sgn}(a_n)}{i}$，这样每段的贡献都 $\geq 1$，而 $x_n \to 0$仍然成立。反设 $\sum|a_n|$发散。此时可取正整数
>
> $$1=m_{1}<m_{2}<\cdots<m_{i}<\cdots$$
>
> 使 $\sum_{k=m_i}^{m_{i+1}-1}|a_k|>i$ (因为尾部不可能都趋于 0, 逐段往前推进即可).
>
> 定义数列 $\{x_{n}\}$:
>
> $$x_{n}=\frac{\operatorname{sgn}(a_{n})}{i},\qquad m_{i}\leqslant n\leqslant m_{i+1}-1.$$
>
> 则当 $n \to \infty$ 时 $i \to +\infty$，故 $x_n \to 0$；又
>
> $$\sum_{k=m_{i}}^{m_{i+1}-1}a_{k}x_{k}=\frac{1}{i}\sum_{k=m_{i}}^{m_{i+1}-1}\left|a_{k}\right|>1.$$
>
> 于是对任意 $n_{1}$
>
> $$\sum_{k=m_{1}}^{m_{n+1}-1}a_{k}x_{k}=\sum_{i=1}^{n}\sum_{k=m_{i}}^{m_{i+1}-1}a_{k}x_{k}>n,$$
>
> 即部分和无界， $\sum a_nx_n$ 发散，与题设“任何 $x_n \to 0$ 都使 $\sum a_nx_n$ 收敛”矛盾。
>
> 故 $\sum|a_n|$ 收敛. 这是“分段 + 柯西收敛准则”的顶级用法: 一次柯西准则只能抓住有限的几段, 这里要把无穷多段拼接起来 $(m_1 < m_2 < \cdots)$ 才能得到“部分和无界”. 这个构造值得记住.

**6.** (难度：★★★★★) 已知 $\{a_{n}\}, \{b_{n}\}$ 是正项数列, 且 $b_{n+1} - b_n \geq \delta > 0$ （$n=1,2,\ldots$）. 证明: 若级数 $\sum_{n=1}^{\infty} a_{n}$ 收敛, 则级数

$$\sum_{n=1}^{\infty}\frac{n\sqrt[n]{(a_{1}a_{2}\cdots a_{n})(b_{1}b_{2}\cdots b_{n})}}{b_{n}b_{n+1}}$$

收敛.

> [!answer]- 原书参考答案（F.0.2 第 6 题，未逐题独立验算）
> **6.** 通项里有 $\sqrt[n]{(a_1\cdots a_n)(b_1\cdots b_n)}$，先用几何平均不等式把它压成 $\frac{1}{n}\sum a_k b_k = \frac{S_n}{n}$；再用 $b_{n+1} - b_n \geqslant \delta$ 得到 $\frac{1}{b_n} - \frac{1}{b_{n+1}} \geqslant \frac{\delta}{b_n b_{n+1}}$，于是 $\sum \frac{S_k}{b_k b_{k+1}}$ 被 $\sum a_k$ 控制——这一步本质是阿贝尔变换（把 $\sum a_k b_k \cdot \frac{1}{b_k b_{k+1}}$ 重新组合）。记 $S_n = \sum_{k=1}^{n} a_k b_k$。由几何平均不等式，
>
> $$\sqrt[n]{\left(a_{1}a_{2}\cdots a_{n}\right)\left(b_{1}b_{2}\cdots b_{n}\right)}\leq\frac{1}{n}\sum_{k=1}^{n}a_{k}b_{k}=\frac{S_{n}}{n},$$
>
> 故原级数的通项满足
>
> $$\frac{n\sqrt[n]{(a_{1}\cdots a_{n})\left(b_{1}\cdots b_{n}\right)}}{b_{n}b_{n+1}}\leqslant\frac{S_{n}}{b_{n}b_{n+1}}.$$
>
> 又由 $b_{n+1}-b_n\geqslant\delta>0$
>
> $$\frac{1}{b_{n}}-\frac{1}{b_{n+1}}=\frac{b_{n+1}-b_{n}}{b_{n}b_{n+1}}\geqslant\frac{\delta}{b_{n}b_{n+1}}\implies\frac{1}{b_{n}b_{n+1}}\leqslant\frac{1}{\delta}\left(\frac{1}{b_{n}}-\frac{1}{b_{n+1}}\right).$$
>
> 于是
>
> $$\sum_{k=1}^{n}\frac{S_{k}}{b_{k}b_{k+1}}\leqslant\frac{1}{\delta}\sum_{k=1}^{n}S_{k}\left(\frac{1}{b_{k}}-\frac{1}{b_{k+1}}\right)=\frac{1}{\delta}\left[\sum_{k=1}^{n}a_{k}-\frac{S_{n}}{b_{n+1}}\right]\leqslant\frac{1}{\delta}\sum_{k=1}^{+\infty}a_{k}$$
>
> (中间一步是阿贝尔变换: $\sum S_k\left(\frac{1}{b_k}-\frac{1}{b_{k+1}}\right)=\sum_{k=1}^{n}a_k-\frac{S_n}{b_{n+1}}$). 由 $\sum a_k$ 收敛知 $\sum\frac{S_n}{b_n b_{n+1}}$ 收敛, 再由比较判别法, 原级数收敛. 两个技术点: 一是”几何平均 ≤ 算术平均”把 $\sqrt[n]{\prod}$ 换掉; 二是把 $a_k b_k$ 写成” $\left(\frac{1}{b_k}-\frac{1}{b_{k+1}}\right)$ 的伴侣”用阿贝尔变换求和——之所以要这么做, 是因为分析时发现”需要 $a_k b_k$ 的部分和 $S_k$”.

**7.** (难度:★★★★★) 设 $\{u_{n}\}$ 为单调递减的正项数列, $\lim_{n\to\infty}u_n=0$, $\{a_n\}$ 为一实数列, 级数 $\sum_{n=1}^{\infty}a_n u_n$ 收敛, 证明:

$$\lim_{n\to\infty}(a_{1}+a_{2}+\cdots+a_{n})u_{n}=0.$$

> [!answer]- 原书参考答案（F.0.2 第 7 题，未逐题独立验算）
> **7.** 思路: 为什么非用阿贝尔变换不可. 要估的是 $\left(\sum_{k=1}^{n}a_{k}\right)u_{n}$, 而题目给的信息只有 $\sum a_{n}u_{n}$ 收敛”——关于 $a_{n}$ 本身, 我们什么都不知道 (它可以无界). 所以唯一的出路是把 $a_{n}$ 拆成
>
> $$a_{n}=(a_{n} u_{n})\cdot\frac{1}{u_{n}},$$
>
> 让已知收敛的那个级数带着它的部分和 $A_{n}=\sum_{k=1}^{n}a_{k}u_{k}$ 进入求和号，再用阿贝尔变换 (分部求和) 把 $\sum a_{k}$ 换成 $\sum A_{k}$ 乘权重”。能这么做的前提正是 $u_{n}$ 单调递减：这时 $\frac{1}{u_{k}}-\frac{1}{u_{k+1}}\geq0$，权重非负，逐项估计才压得住。
>
> 第一步：分部求和. 记 $A_{n}=\sum_{k=1}^{n}a_{k}u_{k}$， $A=\sum_{k=1}^{+\infty}a_{k}u_{k}$ (于是 $A_{n}\to A$，且 $A_{0}=0$)。由 $a_{k}=\frac{A_{k}-A_{k-1}}{u_{k}}$，对 $\sum(A_{k}-A_{k-1})b_{k}(b_{k}=\frac{1}{u_{k}})$ 作阿贝尔变换：
>
> $$S_{n}:=\sum_{k=1}^{n}a_{k}=\frac{A_{n}}{u_{n}}+\sum_{k=1}^{n-1}A_{k}\left(\frac{1}{u_{k}}-\frac{1}{u_{k+1}}\right).$$
>
> 第二步：把 A 从 $A_{k}$ 中拆出来. 用 $A_{k} = A - (A - A_{k})$ 以及 $\sum_{k=1}^{n-1}\left(\frac{1}{u_{k}} - \frac{1}{u_{k+1}}\right) = \frac{1}{u_{1}} - \frac{1}{u_{n}}$
>
> $$S_{n}=\frac{A_{n}}{u_{n}}+A\left(\frac{1}{u_{1}}-\frac{1}{u_{n}}\right)-\sum_{k=1}^{n-1}\left(A-A_{k}\right)\left(\frac{1}{u_{k}}-\frac{1}{u_{k+1}}\right).$$
>
> 两边乘 $u_{n}$:
>
> $$u_{n}S_{n}=\left(A_{n}-A\right)+\frac{A u_{n}}{u_{1}}-u_{n}\sum_{k=1}^{n-1}\left(A-A_{k}\right)\left(\frac{1}{u_{k}}-\frac{1}{u_{k+1}}\right).$$
>
> 第三步：分三段估计．给定 $\varepsilon>0$．由 $A_{n}\rightarrow A$， $u_{n}\rightarrow0$，可取N，使n>N时
>
> $$\left|A_{n}-A\right|<\varepsilon,\qquad\frac{u_{n}}{u_{1}}<\varepsilon;$$
>
> 又$\{A-A_k\}$有界,取$M>0$使$|A-A_k|\leq M$对一切$k$成立.把右端的和按$k\leq N$与$N<k<n$拆成两段:
>
> $k \leq N$ 的有限项: 总和是一个与 n 无关的常数 $C_{N}$, 乘上 $u_{n}$ 后随 $n \to \infty$ 趋于 0;
>
> • N < k < n 的项: 此时 $\left|A - A_{k}\right| < \varepsilon$，而 $\sum_{k=N+1}^{n-1}\left(\frac{1}{u_{k}} - \frac{1}{u_{k+1}}\right) = \frac{1}{u_{N+1}} - \frac{1}{u_{n}}$，故这一段不超过
>
> $$\varepsilon u_{n}\left(\frac{1}{u_{N+1}}-\frac{1}{u_{n}}\right)=\varepsilon\left(\frac{u_{n}}{u_{N+1}}-1\right)<\varepsilon.$$
>
> 于是当 n 充分大时 $|u_n S_n| < 3\varepsilon$。由 $\varepsilon$ 任意小，
>
> $$\lim_{n\to\infty}\left(a_{1}+a_{2}+\cdots+a_{n}\right)u_{n}=0.$$

**8.** (难度：★★★★★) 设 $\sum_{n=0}^{\infty}a_{n}x^{n}$ 的收敛半径为 1, $\lim_{n\to\infty}na_{n}=0$, 且 $\lim_{x\to1^{-}}\sum_{n=0}^{\infty}a_{n}x^{n}=A$, 证明: $\sum_{n=0}^{\infty}a_{n}$ 收敛且 $\sum_{n=0}^{\infty}a_{n}=A$.

> [!answer]- 原书参考答案（F.0.2 第 8 题，未逐题独立验算）
> **8.** 要把“部分和 $\sum_{k=0}^{n} a_{k}$”与“无穷和 $A$”拉近，最省事的桥是取 $x = 1 - \frac{1}{n}$：此时 $S(x) - A$ 已经由函数极限控制住。剩下的差别是“ $a_{k} x^{k}$”与“ $a_{k}$”以及“尾部 $k > n$”，于是把待估量拆成三段，每段各用一种条件去压： $1 - x^{k} \leqslant k (1 - x) = \frac{k}{n}$ 压前段， $ka_{k} \to 0$ 压尾部，函数的极限压第三段。记 $S(x) = \sum_{n=0}^{+\infty} a_{n} x^{n}$，题设给 $\lim_{x \to 1^{-}} S(x) = A$。
>
> 第一步:取特殊的x.令 $x=1-\frac{1}{n}$.由 $\lim_{x\to1^{-}}S(x)=A$,对任意 $\varepsilon>0$,当n充分大时
>
> $$\left|S\left(1-\frac{1}{n}\right)-A\right|<\varepsilon.$$
>
> 第二步：三段配凑.
>
> $$\begin{aligned}\left|\sum_{k=0}^{n}a_{k}-A\right|\leqslant&\sum_{k=0}^{n}\left|a_{k}\right|\left[1-\left(1-\frac{1}{n}\right)^{k}\right]\\&+\sum_{k=n+1}^{+\infty}\left|a_{k}\right|\left(1-\frac{1}{n}\right)^{k}+\left|S\left(1-\frac{1}{n}\right)-A\right|.\end{aligned}$$
>
> 第三步：逐段估计.
>
> 第一段. 由 $1 - (1 - t)^{k} \leqslant kt (t \in [0,1])$ 与 $x = 1 - \frac{1}{n}$,
>
> $$\sum_{k=0}^{n}\left|a_{k}\right|\left[1-\left(1-\frac{1}{n}\right)^{k}\right]\leqslant\frac{1}{n}\sum_{k=1}^{n}k\left|a_{k}\right|.$$
>
> 由 $ka_k \to 0$ 知 $\frac{1}{n} \sum_{k=1}^{n} k |a_k| \to 0$ (部分和的算术平均仍趋于 0)，故 $n$ 充分大时该量 $< \varepsilon$。
>
> 第二段. 由 $ka_k \to 0$，当 $k$ 充分大时 $|a_k| < \frac{\varepsilon}{n}$ ( $k > n$ 时更有 $|a_k| \leq \frac{\varepsilon}{n}$):
>
> $$\sum_{k=n+1}^{+\infty}\left|a_{k}\right|\left(1-\frac{1}{n}\right)^{k}\leqslant\frac{\varepsilon}{n}\sum_{k=n+1}^{+\infty}\left(1-\frac{1}{n}\right)^{k}=\frac{\varepsilon}{n}\cdot n\left(1-\frac{1}{n}\right)^{n+1}\leqslant\varepsilon.$$
>
> (末一步用了等比求和 $\sum_{k=n+1}^{+\infty}\left(1-\frac{1}{n}\right)^{k}=n\left(1-\frac{1}{n}\right)^{n+1}$.)
>
> 第三段. 由第一步 $<\varepsilon$.
>
> 三段合起来: $n$ 充分大时 $\left|\sum_{k=0}^{n} a_{k} - A\right| < 3\varepsilon$, 故 $\sum_{n=0}^{+\infty} a_{n}$ 收敛且其和为 $A$. 三段的理由是各不相同的: 第一段是“把 $x^{k}$ 换成 $1$”, 第二段是“把尾部压成几何级数”, 第三段是“用函数的极限”. 注意 $x = 1 - \frac{1}{n}$ 的选取——它同时让 $1 - x = \frac{1}{n}$ 很小、又让 $n(1 - \frac{1}{n})^{n+1}$ 保持有界.

## 5.3 积分放缩

积分放缩是级数证明里的重要技巧,通过将离散的级数和化为对应的定积分计算,对于一些几乎无法分析的级数敛散性分析有奇效.

**1.** (难度:★★) 已知非负递减的连续函数 $f(x)$ 定义在 $[0, +\infty)$. 设 $a_{n} = \sum_{k=1}^{n} f(k) - \int_{1}^{n} f(x) \, dx$, 求证: $\lim_{n \to \infty} a_{n}$ 存在.

> [!answer]- 原书参考答案（F.0.3 第 1 题，未逐题独立验算）
> **1.** 思路. “和－积分”这种形式, 最自然的想法是看它单调有界. 作差 $a_{n+1} - a_n$, 只剩下“右端点处的函数值”与“最后一段上的积分”之比, 而这两者由单调性直接可比; 再看下界, 把“和减积分”拆成若干个小区间上的差, 每一项都非负.
>
> 第一步： $\{a_{n}\}$ 单调递减.
>
> $$a_{n+1}-a_{n}=f(n+1)-\int_{n}^{n+1}f(x)\mathrm{d}x.$$
>
> 由积分中值定理，存在 $\xi_{n} \in (n, n+1)$ 使 $\int_{n}^{n+1} f(x) \, \mathrm{d}x = f(\xi_{n})$。因为 $f(x)$ 单调递减且 $\xi_{n} < n+1$，所以 $f(\xi_{n}) \geqslant f(n+1)$，从而
>
> $$a_{n+1}-a_{n}=f(n+1)-f(\xi_{n})\leqslant0.$$
>
> 即 $\{a_{n}\}$单调递减.
>
> 第二步： $\{a_{n}\}$ 有下界. 把和与积分按同样的分点配对:
>
> $$a_{n}=\sum_{k=1}^{n}f(k)-\int_{1}^{n}f(x)\mathrm{d}x=\sum_{k=1}^{n-1}\left[f(k)-\int_{k}^{k+1}f(x)\mathrm{d}x\right]+f(n).$$
>
> 在 $[k,k+1]$ 上 $f(x)\leq f(k)$，故每个方括号都 $\geq0$；又 $f(n)\geq0$。所以 $a_{n}\geq0$。
>
> 第三步：收尾. $\{a_{n}\}$ 单调递减且有下界，故 $\lim_{n\to\infty}a_{n}$ 存在.

**2.** (难度:★★★) 证明级数 $\sum_{n=1}^{\infty}\frac{1}{n^{2}}\sum_{k=1}^{n}\csc^{2}\frac{k\pi}{2n+1}$ 发散.

> [!answer]- 原书参考答案（F.0.3 第 2 题，未逐题独立验算）
> **2.** 只要证明通项不趋于 0 就够了. 把内层的 $\sum \csc^{2}$ 用积分放缩换成 cot 的差, 再估计出它 $\sim \frac{4n^{2}}{\pi^{2}}$, 于是通项 $\sim \frac{4}{\pi^{2}} \neq 0$. 记 $a_{n} = \sum_{k=1}^{n} \csc^{2}\frac{k\pi}{2n+1}$. 由积分放缩,
>
> $$\begin{aligned}a_{n}&>\int_{1}^{n}\csc^{2}\frac{\pi x}{2n+1}\mathrm{d}x+\csc^{2}\frac{n\pi}{2n+1}\\&=\frac{2n+1}{\pi}\left(\cot\frac{\pi}{2n+1}-\cot\frac{n\pi}{2n+1}\right)+\csc^{2}\frac{n\pi}{2n+1}.\end{aligned}$$
>
> 当 $n \to \infty$ 时 $\cot \frac{\pi}{2n+1} \sim \frac{2n+1}{\pi}$、 $\cot \frac{n\pi}{2n+1} = O(1)$，故
>
> $$a_{n}\sim\frac{2n+1}{\pi}\cdot\frac{2n+1}{\pi}=\frac{(2n+1)^{2}}{\pi^{2}},$$
>
> 于是
>
> $$\frac{1}{n^{2}}a_{n}\sim\frac{4}{\pi^{2}}\neq0\qquad(n\to\infty),$$
>
> 即原级数的通项不趋于 0, 级数发散. $\sum \csc^2$ 没有显式公式 (它的和与 $\csc^2$ 的取值有关), 但“判发散”只需要量级: 用积分放缩把它换成 $\cot$ 的差, 就能读出 n 次幂的阶.

**3.** (难度:★★★★) 当 $x \to 1^{-}$时, 求与 $\sum_{n=1}^{\infty} x^{n^{2}}$ 等价的无穷大量.

> [!answer]- 原书参考答案（F.0.3 第 3 题，未逐题独立验算）
> **3.** 思路. 把 $x^{n^{2}} = e^{n^{2}\ln x}$ 看成 $f(y) = e^{y^{2}\ln x}$ 在整数点处的取值. 因为 $\ln x < 0, f(x)$ 非负且单调递减, 正好用积分放缩把无穷级数夹在两个无穷积分之间; 而要算的无穷积分是标准的高斯积分.
>
> 第一步:积分放缩夹住级数.由 $f(y)=e^{y^{2}\ln x}$非负递减,
>
> $$\int_{1}^{n+1}e^{y^{2}\ln x}\mathrm{d}y<\sum_{k=1}^{n}x^{k^{2}}<\int_{0}^{n}e^{y^{2}\ln x}\mathrm{d}y.$$
>
> 令 $n\to\infty$:
>
> $$\int_{1}^{+\infty}e^{y^{2}\ln x}\mathrm{d}y\leqslant\sum_{n=1}^{+\infty}x^{n^{2}}\leqslant\int_{0}^{+\infty}e^{y^{2}\ln x}\mathrm{d}y.$$
>
> 第二步：算出高斯积分. 记 $a = -\ln x > 0$，则
>
> $$\int_{0}^{+\infty}e^{-ay^{2}}\mathrm{d}y=\frac{\sqrt{\pi}}{2\sqrt{a}}=\frac{\sqrt{\pi}}{2\sqrt{-\ln x}}.$$
>
> 把右边这个量记作 $G(x)$，则上式两边同除 $G(x)$ 得
>
> $$\frac{1}{G(x)}\int_{1}^{+\infty}e^{y^{2}\ln x}\mathrm{d}y\leqslant\frac{1}{G(x)}\sum_{n=1}^{+\infty}x^{n^{2}}\leqslant1.$$
>
> 第三步: 左端的比值趋于 1. 左端的分子与 $\int_{0}^{+\infty}$ 只差 $[0,1]$ 上的一段:
>
> $$1-\frac{1}{G(x)}\int_{1}^{+\infty}e^{-ay^{2}}\mathrm{d}y=\frac{2\sqrt{a}}{\sqrt{\pi}}\int_{0}^{1}e^{-ay^{2}}\mathrm{d}y\leqslant\frac{2\sqrt{a}}{\sqrt{\pi}}\longrightarrow0\qquad(a\to0^{+}).$$
>
> 第四步：夹逼。由夹逼定理，
>
> $$\sum_{n=1}^{+\infty}x^{n^{2}}\sim\frac{\sqrt{\pi}}{2\sqrt{-\ln x}}\sim\frac{\sqrt{\pi}}{2\sqrt{1-x}}\qquad(x\to1^{-}),$$
>
> 最后一处用了 $-\ln x=-\ln(1-(1-x))\sim1-x$.

**4.** (难度: ★★★★★) 求证: 级数 $\sum_{n=1}^{\infty} \sum_{k=1}^{\infty} \frac{(-1)^{\left\lfloor \sqrt{n} \right\rfloor}}{n^{2}+k^{2}}$ 收敛, 其中 $\lfloor x \rfloor$ 表示不超过 x 的最大整数.

> [!answer]- 原书参考答案（F.0.3 第 4 题，未逐题独立验算）
> **4.** 先对 k 求和: $\sum_{k}\frac{1}{n^{2}+k^{2}}$ 与 $\frac{\pi}{2n}$ 只差 $O(\frac{1}{n^{2}})$ (积分放缩), 于是原级数 $=\pi\sum\frac{(-1)^{[\sqrt{n}]}}{2n}+$ (绝对收敛项). 剩下那部分按 $m=[\sqrt{n}]$ 分组, 每组之和 $b_{m}\approx\frac{\pi}{2}\ln\frac{(m+1)^{2}}{m^{2}}\sim\frac{\pi}{m}$, 单调递减趋于 0, 用莱布尼茨判别法收尾. 第一步: 对 k 求和, 分离出主项. 由积分放缩,
>
> $$\frac{\pi}{2n}-\frac{1}{n}\arctan\frac{1}{n}\leqslant\sum_{k=1}^{+\infty}\frac{1}{n^{2}+k^{2}}\leqslant\frac{\pi}{2n},$$
>
> 结合 $\arctan\frac{1}{n}=O\left(\frac{1}{n}\right)$，得
>
> $$\left|\sum_{k=1}^{+\infty}\frac{1}{n^{2}+k^{2}}-\frac{\pi}{2n}\right|<\frac{1}{n^{2}}.$$
>
> 记 $a_{n}=\sum_{k=1}^{+\infty}\frac{(-1)^{\left[\sqrt{n}\right]}}{n^{2}+k^{2}}$，则
>
> $$a_{n}=(-1)^{[\sqrt{n}]}\left(\frac{\pi}{2n}+O\left(\frac{1}{n^{2}}\right)\right).$$
>
> 第二步： $O\left(\frac{1}{n^{2}}\right)$ 那部分绝对收敛. 因为 $\sum\frac{1}{n^{2}}$ 收敛.
>
> 第三步：主项按 $[\sqrt{n}]$ 分组. 记 $c_{n}=\frac{\pi(-1)^{\left[\sqrt{n}\right]}}{2n}$. 当 $m^{2}\leqslant n\leqslant(m+1)^{2}-1$ 时 $[\sqrt{n}]=m,$ 令
>
> $$b_{m}=\sum_{n=m^{2}}^{(m+1)^{2}-1}\frac{\pi}{2n}.$$
>
> 由积分放缩，
>
> $$b_{m}=\frac{\pi}{2}\sum_{n=m^{2}}^{(m+1)^{2}-1}\frac{1}{n}\geqslant\frac{\pi}{2}\sum_{n=m^{2}}^{(m+1)^{2}-1}\int_{n}^{n+1}\frac{\mathrm{d}x}{x}=\frac{\pi}{2}\int_{m^{2}}^{(m+1)^{2}}\frac{\mathrm{d}x}{x}=\frac{\pi}{2}\ln\frac{(m+1)^{2}}{m^{2}},$$
>
> $$b_{m}\leqslant\frac{\pi}{2}\sum_{n=m^{2}}^{(m+1)^{2}-1}\int_{n-1}^{n}\frac{\mathrm{d}x}{x}=\frac{\pi}{2}\int_{m^{2}-1}^{(m+1)^{2}-1}\frac{\mathrm{d}x}{x}=\frac{\pi}{2}\ln\frac{(m+1)^{2}-1}{m^{2}-1},$$
>
> (左边用了 $\frac{1}{n} \geqslant \int_{n}^{n+1} \frac{dx}{x} = \ln \frac{n+1}{n}$; 右边用了 $\frac{1}{n} \leqslant \int_{n-1}^{n} \frac{dx}{x} = \ln \frac{n}{n-1}$——两者都由 $\frac{1}{x}$在 $(0,+\infty)$上单调递减得到; 两次求和都“首尾相接”成望远镜, 所以只剩下两个对数.)
>
> 两端都趋于0: 左端 $\ln\frac{m+1}{m}\to0$ , 右端 $\frac{\pi}{2}\ln\frac{m(m+2)}{(m-1)(m+1)}\to0$ 。由夹逼定理, $b_{m}\to0$ 。
>
> 第四步： $\{b_{m}\}$ 单调递减. 由上式
>
> $$b_{m}\leqslant\frac{\pi}{2}\ln\frac{m(m+2)}{(m-1)(m+1)}<\frac{\pi}{2}\ln\frac{m^{2}}{(m-1)^{2}}\leqslant b_{m-1},$$
>
> 即 $\{b_{m}\}$单调递减 $(m \geqslant 2)$.
>
> 第五步：莱布尼茨收尾。由莱布尼茨判别法 $\sum_{m=1}^{+\infty}(-1)^{m}b_{m}$ 收敛，即 $\sum c_{n}$ 收敛；再与第二步合起来，原级数收敛。（第十六届全国大学生数学竞赛初赛压轴）三步：对 k 求和 $\rightarrow$ 分离主项（主项是 $\frac{\pi}{2n}$，误差 $O(n^{-2})$ 绝对收敛）、按 $[\sqrt{n}]$ 分组（每组之和 $b_{m} \sim \frac{\pi}{m}$）、证明 $\{b_{m}\}$ 单调递减用莱布尼茨。最容易漏的是第四步——分组求和之后必须验证单调性。

## 5.4 余项分析

近些年兴起的对级数项与其收敛值之差的累计求和的分析，会涉及逐项积分和放缩的技巧。该类题目在定积分定义中也曾有压轴题方向的考察，但鉴于该题与级数的关系不大，会在后续的定积分定义专题详细阐述。

**1.** (难度:★★★★) 设正项级数 $\sum_{n=1}^{\infty}a_{n}$ 收敛, 证明: 存在收敛的正项级数 $\sum_{n=1}^{\infty}b_{n}$, 使得 $\lim_{n\to\infty}\frac{a_{n}}{b_{n}}=0$.

> [!answer]- 原书参考答案（F.0.4 第 1 题，未逐题独立验算）
> **1.** 思路（怎么想到的）。要找一个“收敛得比 $\sum a_n$ 还慢”的级数，最直接的念头是让 $b_n$ 由裂项产生，这样求和能自动收敛。
>
> 第一次尝试: 用部分和 $S_n$ 裂项. 试 $b_n = f(S_n) - f(S_{n-1})$, 则 $\sum b_n = f(S_n) - f(S_1)$ 收敛 (因为 $S_n \to S$). 可惜由中值定理
>
> $$b_{n}=\left(S_{n}-S_{n-1}\right)f^{\prime}(\xi_{n})=a_{n}f^{\prime}(\xi_{n}),\qquad\xi_{n}\in\left(S_{n-1},S_{n}\right),$$
>
> 于是 $\frac{a_{n}}{b_{n}}=\frac{1}{f'(\xi_{n})}$.要它趋于0,就得让 $f'(\xi_{n})\to+\infty$;但 $S_{n}\to S$是个有限数, $f'(S)$不可能等于 $+\infty$.所以这条路走不通.
>
> 第二次尝试: 改用余项 $\gamma_{n}$. 关键在于余项
>
> $$\gamma_{n}=\sum_{k=n}^{+\infty}a_{k}$$
>
> 趋于0，而 $a_{n}=\gamma_{n}-\gamma_{n+1}$仍是裂项的形状.于是取 $b_{n}=f(\gamma_{n})-f(\gamma_{n+1})$:它仍能裂项求和，而 $\xi_{n}\in(\gamma_{n+1},\gamma_{n})\to0$，只要 $f^{\prime}(0^{+})=+\infty$就能让 $\frac{a_{n}}{b_{n}}=\frac{1}{f^{\prime}(\xi_{n})}\to0$.这样的 $f(x)$一大把，取 $f(x)=\sqrt{x}$最简单.
>
> 第一步: 定义 $b_n$。由 $\sum a_n$ 收敛, $\gamma_n = \sum_{k=n}^{+\infty} a_k$ 有意义, 且 $\gamma_n$ 递减趋于 0、 $a_n = \gamma_n - \gamma_{n+1}$. 取
>
> $$b_{n}=\sqrt{\gamma_{n}}-\sqrt{\gamma_{n+1}}>0.$$
>
> 第二步： $\sum b_n$ 收敛。裂项：
>
> $$\sum_{k=1}^{n}b_{k}=\sqrt{\gamma_{1}}-\sqrt{\gamma_{n+1}}\;\longrightarrow\;\sqrt{\gamma_{1}}\qquad(n\to\infty),$$
>
> 故 $\sum b_n$ 收敛（其和为 $\sqrt{\gamma_1}$）.
>
> 第三步： $\frac{a_{n}}{b_{n}}\rightarrow0$。由中值定理，存在 $\xi_{n}\in(\gamma_{n+1},\gamma_{n})$使
>
> $$b_{n}=\left(\gamma_{n}-\gamma_{n+1}\right)\cdot\frac{1}{2\sqrt{\xi_{n}}}=\frac{a_{n}}{2\sqrt{\xi_{n}}},$$
>
> 于是
>
> $$\frac{a_{n}}{b_{n}}=2\sqrt{\xi_{n}}\longrightarrow0\qquad(n\rightarrow\infty),$$
>
> 因为 $\xi_{n}\to0$ (它夹在 $\gamma_{n+1}$ 与 $\gamma_{n}$ 之间). 证毕.

**2.** (难度:★★★★) 设 $a_{n}=\sum_{k=1}^{n}\frac{(-1)^{k-1}}{k}-\ln2$，证明 $\sum_{n=1}^{\infty}a_{n}$ 收敛并求其值.

> [!answer]- 原书参考答案（F.0.4 第 2 题，未逐题独立验算）
> **2.** 思路. 这里的 $a_{n}$ 本身就是“部分和减极限”, 也就是余项, 直接算 $\sum a_{n}$ 没有现成公式. 但注意
>
> $$\frac{(-1)^{k-1}}{k}=\int_{0}^{1}(-1)^{k-1}x^{k-1}\mathrm{d}x,\qquad\ln2=\int_{0}^{1}\frac{\mathrm{d}x}{1+x},$$
>
> 把两项都写成 [0,1] 上的积分, $a_n$ 就合并成一个积分; 再对 $k$ 求和时算出几何和 $\sum(-x)^k$, 就得到一个能直接取极限的显式表达式. 这就是"统一形式".
>
> 第一步：把 $a_{n}$ 写成一个积分.
>
> $$\begin{aligned}a_{n}&=\int_{0}^{1}\sum_{k=1}^{n}(-1)^{k-1}x^{k-1}\mathrm{d}x-\int_{0}^{1}\frac{\mathrm{d}x}{1+x}\\&=\int_{0}^{1}\frac{1-(-x)^{n}}{1+x}\mathrm{d}x-\int_{0}^{1}\frac{\mathrm{d}x}{1+x}=\int_{0}^{1}\frac{-(-x)^{n}}{1+x}\mathrm{d}x,\end{aligned}$$
>
> 即 $a_{n}=(-1)^{n+1}\int_{0}^{1}\frac{x^{n}}{1+x}dx.$
>
> 第二步: 对 k 求和（用几何和）. 由 $\sum_{k=1}^{n}(-x)^{k}=\frac{-x(1-(-x)^{n})}{1+x}$,
>
> $$\begin{aligned}\sum_{k=1}^{n}a_{k}&=-\int_{0}^{1}\frac{\sum\limits_{k=1}^{n}(-x)^{k}}{1+x}\mathrm{d}x=\int_{0}^{1}\frac{x\left(1-(-x)^{n}\right)}{(1+x)^{2}}\mathrm{d}x\\&=\int_{0}^{1}\frac{x}{(1+x)^{2}}\mathrm{d}x+\int_{0}^{1}\frac{(-x)^{n+1}}{(1+x)^{2}}\mathrm{d}x.\end{aligned}$$
>
> 第三步：取极限. 因为
>
> $$\int_{0}^{1}\frac{x}{(1+x)^{2}}\mathrm{d}x=\left[\ln(1+x)+\frac{1}{1+x}\right]_{0}^{1}=\ln2-\frac{1}{2},$$
>
> 而 $\left|\int_{0}^{1}\frac{(-x)^{n+1}}{(1+x)^{2}}\mathrm{d}x\right|\leqslant\int_{0}^{1}x^{n+1}\mathrm{d}x=\frac{1}{n+2}\to0$ , 所以
>
> $$\sum_{n=1}^{+\infty}a_{n}=\lim_{n\to\infty}\sum_{k=1}^{n}a_{k}=\ln2-\frac{1}{2}.$$

**3.** (难度:★★★★) 设 $a_{n}=\sum_{k=1}^{n}\frac{1}{k}-\ln n$

(1) 证明: 极限 $\lim_{n \to \infty} a_n$ 存在.

(2) 记 $\lim_{n\to\infty}a_n=C$，讨论级数 $\sum_{n=1}^{\infty}(a_n-C)$ 的敛散性.

> [!answer]- 原书参考答案（F.0.4 第 3 题，未逐题独立验算）
> **3.** 思路. 第(1)问是“和减积分”, 直接看单调有界 (与上一个例题同一套路). 第(2)问要判断“余项 $a_{n}-C$ 到底有多小”: 把 $a_{n}-C$ 写成 $k \geqslant n$ 的尾巴, 再用 $\ln\left(1+\frac{1}{k}\right)=\frac{1}{k}-\frac{1}{2k^{2}}+O\left(\frac{1}{k^{3}}\right)$ 读出它的阶——这就是余项估计.
>
> (1) 把 $a_{n}$ 改写成余项之和. 因为 $\ln n = \sum_{k=1}^{n-1} \ln\left(1 + \frac{1}{k}\right)$,
>
> $$a_{n}=\sum_{k=1}^{n}\frac{1}{k}-\sum_{k=1}^{n-1}\ln\left(1+\frac{1}{k}\right)=\sum_{k=1}^{n-1}\left[\frac{1}{k}-\ln\left(1+\frac{1}{k}\right)\right]+\frac{1}{n}.$$
>
> 由 $\ln(1+x)<x(x>0)$知每一项都为正，故 $a_{n}>0,\{a_{n}\}$有下界。又由 $\ln(1+x)>\frac{x}{1+x}$（取 $x=\frac{1}{n}$）得
>
> $$a_{n+1}-a_{n}=\frac{1}{n+1}-\ln\left(1+\frac{1}{n}\right)<0,$$
>
> 故 $\{a_{n}\}$ 单调递减. 于是 $\lim_{n\to\infty}a_{n}=C$ 存在 (这就是 Euler 常数).
>
> (2) 读出 $a_{n}-C$ 的阶. 把差值写成尾巴:
>
> $$a_{n}-C=\sum_{k=n+1}^{+\infty}\left[\ln\left(1+\frac{1}{k}\right)-\frac{1}{k}\right]+\ln\left(1+\frac{1}{n}\right).$$
>
> 用 $\ln\left(1+\frac{1}{k}\right)-\frac{1}{k}=-\frac{1}{2k^{2}}+O\left(\frac{1}{k^{3}}\right)$得
>
> $$\sum_{k=n+1}^{+\infty}\left[\ln\left(1+\frac{1}{k}\right)-\frac{1}{k}\right]=-\frac{1}{2n}+O\left(\frac{1}{n^{2}}\right),$$
>
> 又 $\ln\left(1+\frac{1}{n}\right)=\frac{1}{n}+O\left(\frac{1}{n^{2}}\right)$. 两式相加:
>
> $$a_{n}-C=\frac{1}{2n}+O\left(\frac{1}{n^{2}}\right)\sim\frac{1}{2n}>0.$$
>
> 由 $\sum\frac{1}{n}$ 发散、比较判别法， $\sum_{n=1}^{+\infty}(a_{n}-C)$ 发散.
>
> （另解：由 Stolz 定理， $\lim_{n\to\infty}\frac{a_n-C}{\frac{1}{n}}=\lim_{n\to\infty}\frac{a_{n+1}-a_n}{-\frac{1}{n(n+1)}}=\lim_{n\to\infty}\frac{\ln\left(1+\frac{1}{n}\right)-\frac{1}{n+1}}{\frac{1}{n(n+1)}}=\frac{1}{2}\neq0$，同样得出发散。）

---

# 整理小结

> [!note] AI 补充
> 本文件保留原书基础篇与强化篇的题目顺序，将原附录 A～F 的答案逐题合并到对应题目下方，共 302 个默认折叠答案框（含合并编号的多小题）；题目与答案均沿用原编号，标题最多到 H3。原目录的 163 个条目及页码完整保留，答案条目跳转至合并后的相应题目章节。
> 已修复可核实的 OCR 错字、难度星级、公式定界符、断裂公式与少量跨页错序，未以概括替代原有题解，也未为原书缺失处补造答案。
> 原书答案中的条件矛盾、符号疑点和末尾缺失已保留在对应答案框内，仍应结合原 PDF 复核。

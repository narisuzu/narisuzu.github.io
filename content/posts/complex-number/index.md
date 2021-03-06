---
title: "如何構造複數域"
description: 
date: 2021-09-13T20:57:55+08:00
image: 
math: true
license: 
hidden: false
comments: true
draft: false
---
$$
\gdef\imi{\mathrm{i}}
$$

## 序

其實複數運算的幾何意義和代數意義是十分割裂的. 以至於我們不得不通過證明二者的等價性才能確認他們具有相同的行爲. 然而在學校中學到的複數向來是從 $\sqrt{-1}$ 等於幾開始的, 也是從此定義的.

但在使用時, 卻常常使用其幾何意義，即模和幅角. 僅在計算加法時才勉爲其難的求下反三角函數以方便二部相加.

但是從實數定義的經驗中可以看到. 對於幾個等價的命題, 只需定其中一個爲公理. 則其餘皆爲基本定理. 所以本文不以 $\imi \coloneqq \sqrt{-1}$ 作爲虛數單位的定義. 而是以幾何直觀感受到的平面點集出發來定義複數.

## Euclid 二維空間

我們定義無理數的時候是使用 Dedekind 分割有理數域來完成的. 但 Dedekind 定理表示實數是完備的，因此必然不能再在一根充滿了有理數和無理數的數軸上做文章. 但是, 一根不行可以兩根. 而且很方便的是, 我們已經有了一種集合, 其每個元素是實二元組. 那就是 $\R^2$. 高中我們就學過的平面向量, 再熟悉不過了.

但我們說 $\R^2$ 不是一個數域, 因爲其未定義封閉的乘法運算. 仔細想來 $\R^2$ 上只有

- 加法: $(x_1, y_1) + (x_2, y_2) = (x_1+x_2, y_1 + y_2)$
- 數乘: $k(x, y) = (kx, ky)$
- 內積: $(x_1, y_1)\cdot (x_2, y_2) = x_1x_2 + y_1y_2$

顯然易證, 加法運算封閉, 滿足交換和結合律. 且 $\forall (x,y) \in \R^2$ , $\exists$ 加法單位元 $(0,0)$ , $\exists$ 加法逆元 $(-x,-y)$ , 那麼, 我們可以再定義一個乘法運算, 使該集合之能夠稱爲一個域. 可以嘗試定義乘法爲

- 乘法: $(x_1,y_1)(x_2,y_2) = (x_1x_2-y_1y_2, x_1y_2+x_2y_1)$

加上乘法定義後, $\R^2$ 是否成域了呢? 不妨驗證一下. 因爲域僅僅對加法和乘法提出了要求, 所以縱使忽略內積和數乘運算也無礙「定義乘法的 $\R^2$ 」其成爲一個域. 因此我們添加一個乘法運算, 去除數乘和內積運算. 將修飾過的這個平面點集叫做 $\Complex$.

在這樣的定義下，顯然乘法封閉. 且 $\forall (x,y) \in \Complex$, 有

- $ (1,0)(x,y) = (x,y) $
- $\displaystyle \left(\frac{x}{x^2 + y^2}, -\frac{y}{x^2+y^2}\right)(x, y) = (1, 0)$

則 $(1,0)$ 是乘法單位元. $\displaystyle \left(\frac{x}{x^2 + y^2}, -\frac{y}{x^2+y^2}\right)$ 是乘法逆元. 而且乘法的交換律、結合律、分配率也並不難證. 因此 $\Complex$ 是一個域.

先不討論其性質, 我們可以注意到 $\Complex$ 和 $\R^2$ (2 維 Euclid 空間) 的元素在結構上是相似的. 最直觀的感受是這兩個集合都是一個平面點集. 但若想從 $\R^2$ 上得到一個域. 定義乘法的方式並不只一種. 而且 $\Complex$ 是最奇形怪狀的一種. 我們不妨假設另外一種乘法的定義方式:

- 🐱乘法: $(x_1, y_1)(x_2, y_2) = (x_1x_2, y_1y_2)$

🐱乘法顯然比我們前文那種又乘又加又減的乘法看起來要「自然合理」的多. 也不難看出, 🐱乘法同樣存在乘法單位: $(1,1)$ , 乘法逆元 $(x^{-1}, y^{-1})$ (這個乘法逆元看起來也比上面那個又是平方分數又是負號的形式簡單不少), 並且交換律和結合律也是顯然成立的. 對於分配率更不難驗證:

$$
\begin{aligned}
&(x_1, y_1)[(x_2, y_2) + (x_3, y_3)] \cr
=& (x_1x_2+x_1x_3, y_1y_2+y_1y_3) \cr
=& (x_1,y_1)(x_2,y_2) + (x_1,y_1)(x_3,y_3)
\end{aligned}
$$

很明顯這種構造乘法的方式也能形成一個域, 這說明乘法的定義方法不唯一. 但 $\Complex$ 的這種奇形怪狀的乘法有什麼特殊之處呢? 在我們探討之前不妨先把 $\Complex$ 書成我們習慣的形式.

定義: $1 = (1,0), \imi = (0, 1)$, 則任意複數 $(a, b)$  都可以寫成 $$(a, 0)+ (0 ,b) =  a + b\imi$$

這裏也能看出 $\R^2$ 的數乘是 $\Complex$ 乘法的一個特例. 下文我們都將使用 $a + b\imi$ 的形式表示複數, 以便和不能進行乘法運算的二維向量區別開來

## 幾何意義

從上面的過程可知在點集和加法的行爲上, $\Complex$ 和 $\R^2$ 是一樣的, 不如說在我們定義 $\Complex$ 的思路下, 名爲「複平面」的二維平面點集和平行四邊形定則是完全繼承自 $\R^2$ 的. 因爲在學習二維向量的時候，集合是平面點集、加法是平行四邊形定則、數乘是長度倍增、內積是投影長度. 一切運算都有直觀的幾何意義, 所以在討論與之相似的 $\Complex$ 時也遵從相似的思路. 我們定義的乘法究竟有什麼奇妙深刻的意義, 縱使其代數式長的像奇形種一樣也依然不捨棄他.

高中時我們學過極座標. 不妨設一點 $(x, y)$


前文有例驗證, 使平面點集成域的乘法不止一種定義方式. 那麼隨意選擇一種方式都有其對應的幾何意義, 不過 $\Complex$ 的乘法是旋轉罷了. 這麼看來我們並沒有動機去選擇 $\Complex$ 中的乘法定義, 至少在定義時我們不知道這種定義有什麼具體現實的意義. 鳴鈴不禁考慮, 雖然我們已經知道了 $\Complex$ 中乘法有着十分重要的現實意義, 那麼可否直接從現實需求的考慮出發，即對平面向量的旋轉作爲一種工具, 從而推導出一套和 $\Complex$ 等價的結構和運算來? 事實上可以, 旋轉是線性代數中很常見的一種線性變換. 我們可以嘗試從這裏着手...

### 逆推

在實數軸上, 一個動點可以進行兩種運動平移 $x \to x + \Delta x$ 與倍增 $ x \to kx $.
很自然的對於平面一點也有平移 $(x,y) \to (x + \Delta x, y+ \Delta y)$, 但物理經驗告訴我們, 轉動也是平面動點的一種運動方式. 我們能否找到一個變換, 使之可以將一個點轉向 $\theta$ ? 線性代數告訴我們確實可以. 設

$$
\boldsymbol{A} = \begin{bmatrix}
\cos \theta & -\sin\theta \cr
\sin\theta & \cos\theta
\end{bmatrix}
$$

則 $\boldsymbol{v_1} = \boldsymbol{Av}$ 表示 $\boldsymbol{v} = (x, y)$ 逆時針旋轉 $\theta$ 得到 $\boldsymbol{v_1} = (x_1, y_1)$ .
其實 $\theta$ 可以用任意向量來表示, 設對於向量 $\boldsymbol{v_0} = (x_0, y_0)$ 有 $\displaystyle \frac{y_0}{x_0} = \tan\theta$. 則

$$
\boldsymbol{A} = \frac{1}{\sqrt{x_0^2 +y_0^2}}
\begin{bmatrix}
x_0 & -y_0 \cr
y_0 & x_0
\end{bmatrix}
$$

那麼對於 $\boldsymbol{v_2} = \boldsymbol{Bv}$ , 其中

$$
\boldsymbol{B} = \Vert \boldsymbol{v_0}\Vert \boldsymbol{A} = \begin{bmatrix}
x_0 & -y_0 \cr
y_0 & x_0
\end{bmatrix}
$$

則表示 $\boldsymbol{v_0}$ 在旋轉了 $\arg(\boldsymbol{v_0})$ 外還增了 $\Vert \boldsymbol{v_0}\Vert $ 倍. 而複數的乘法實際上就是這個過程.

如果我們將前文的複數定義作爲公理, 則很容易證明對於每一個 $\boldsymbol{B}$ , $\exists$唯一對應的向量 $\boldsymbol{v_0} = (x_0, y_0)$ , 從而使 $\forall \boldsymbol{v} = (x,y) \in \R^2$ 有:

$$ \boldsymbol{Bv} = (x_0 + \imi y_0)(x + \imi y)$$

其中等號左邊表示矩陣乘法，右邊表示之前定義的複數乘法. 反之如果以矩陣來定義複數及其運算, 則前文所述的各種性質也容易證明.

使用線性變換的視角對於乘法的幾何意義很直觀, 如果 $y_0 = 0$ 則 $\boldsymbol{v_0}$ 在 $x$ 軸(實軸)上, 等於旋轉 $0$ 或 $\pi$ (具體數值看 $x_0$ 的正負) 後倍增 $\Vert \boldsymbol{v_0}\Vert  = |x_0|$ . 這其實等價於直接倍增 $x_0$ . 同時在形式上 $\boldsymbol{B}$ 可以寫成

$$
\boldsymbol{B} = \begin{bmatrix}
x_0 & 0 \cr
0 & x_0
\end{bmatrix} = x_0\boldsymbol{I}
$$

其中, $\boldsymbol{I}$ 是二階單位陣. 由簡單的線性代數芝士可知.

$$
\boldsymbol{Bv} = x_0\boldsymbol{I}\begin{bmatrix}x\cr y\end{bmatrix} = x_0\begin{bmatrix}x\cr y\end{bmatrix}
$$

從數乘的幾何意義知其爲倍增 $x_0$ . 和前面的分析完全相同. 這說明 $\R^2$ 中的數乘運算其實是 $\Complex$ 中乘法運算的一種特殊情況. 再令 $\boldsymbol{\vec{v}} = (x, 0)$. 則不難想見, 雖然變量還是二維的, 但所有的點都在 $x$ 軸上. 那麼實數的乘法其實也是一種特殊情況. 即小節最開始的實數乘法運算的倍增意義. 於是我們也可以從矩陣變換來定義複數. 對於矩陣 $\boldsymbol{A}$ 對應的複數 $\cos\theta + \imi\sin\theta$ , 正是歐拉公式右邊的形式.

## 總結

從高中到大學，複數域都是先定義 $\imi$ 的. 並且 $\imi$ 從解決了數學危機的大功臣一下變成了複振幅. 這種過度顯得很不自然. 本文提供了兩類不同的思路去發現並定義複數並推出其一切性質. 但應該注意的是本文中的兩種思路. 因爲合法的乘法規則不止一條, 並且任舉一條合法的乘法規則時都不知該規則會帶來怎樣的座標變換. 從另一條思路, 座標變換不止一種, 所以從任意變換出發都無法立即判別其是否滿足乘法規則的定律. 但合法的變換矩陣一定只由兩個實數構成, 即可以和平面點集中的點一一對應. 不然不滿足乘法的定義.

那麼作爲一名工科生, 我們最早使用到複數是在電路中描述正弦量, 天然是爲了尋找某種結構以應用旋轉而發的. 所以從旋轉變換的角度出發來構造複數便顯得尤爲自然, 而解決 $\sqrt{-1}$ 的定義不過是這條路上的副產物而已.

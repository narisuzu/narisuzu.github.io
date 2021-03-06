---
title: "小學之上，線代之下"
date: 2020-06-05T23:38:04+08:00
draft: false
math: true
image: cover.jpg
description: "不使用線性代數概念對方程、自變量和解集的關係的感性理解"
tags: ["線性代數"]
---

## $m$ 和 $n$

$m \times n$ 線性方程組中，共有 $n$ 個變量，$m$ 條線性方程

感性的來看，方程組中的每一條方程都是一種「約束」，在所有方程的共同約束下，變量的取值範圍（解集）被確定下來，每一條方程的「約束」都是將變量的解集縮小. 舉例來看，設獨立變量 $x$ 與 $y$ 均爲實數，設一個方程組，假設開始時方程組內沒有任何方程. 這時 $(x, y)$ 的解集就是整個 $\mathbb{R}^2$，幾何上看就是整個 $xOy$ 平面.

現在，給方程組內加入一條方程
$$2x + y = 1 \tag{1}$$
這時顯然有許多點不能出現在解集中了，比如座標原點 $(0, 0)$，因爲 $2 \times 0 + 0 \neq 1$，幾何上看，就是原點不在 $(1)$ 式確定的直線上. 這時，可以這麼感性的理解解集上發生的變化：因爲 $(1)$ 式的加入，解集不能再「肆無忌憚」的想取什麼就取什麼了，解集中的解必須同時「服從」所有方程規定的「條件」. 換句話說解集從原來的整個平面被方程 $(1)$「約束」成了一條直線.

這時讓我們加入第二條方程
$$3x + y = 0 \tag{2}$$
這時，連原來的一條直線上的點都取不到了，解集中僅僅剩下 $(-1, 3)$ 了，顯然地，兩個方程顯然比一個方程的條件更加「嚴苛」，解集不止要「服從」$(1)$ 式還要「服從」$(2)$ 式，而能同時服從這兩個條件的點，就只剩下 $(-1, 3)$ 了.

如果我們再加入一個方程會怎麼樣？, 假設其爲
$$2x - 2y = 4 \tag{3}$$
這時，連解集中僅剩的一個點 $(-1 ,3)$ 也不能滿足新加入的這個方程的約束了. 這時，解集爲 $\varnothing$，方程組就沒有解了.

## 相容性

因而可知，在上述的例子中，當方程組中若

a. 沒有方程或僅有 $(1)$ 式： 解集爲無限集  
b. 有 $(1)$ 和 $(2)$ 式：解集爲有限集  
c. 有 $(1)$, $(2)$ 和 $(3)$ 式： 解集爲 $\varnothing$  

我們稱當解集爲 $\varnothing$ 時方程組是不相容的 (inconsistent)，解集非空時方程組是相容的 (consistent)，

脫去集合論的外衣，當解集爲

無限集 $\implies$ 方程組有無窮多解  
有限集 $\implies$ 方程組有有限個解. (對於線性方程組有唯一解)  
$\varnothing$ $\implies$ 方程組無解

因此有結論：**相容的線性方程組解集必非空**.

## 亞定與超定

- 當方程的個數多於未知數的個數 ($m > n$)，則稱方程組是超定的(overdetermined)

- 當方程的個數少於未知數的個數 ($m < n$)，則稱方程組是亞定的(underdetermined)

還拿前例舉例：
情況a中 $m < n$，方程組亞定，
情況c中 $m > n$，方程組超定.

字面理解，亞定，就是線性方程組的「約束」不足，超定，就是「約束」過多，從而造成方程組可能無窮多解或無解這兩種極端情況.

**但是超定並不意味不相容**(雖然現實中通常都不相容)，還是上面的例子，如果所加入的式 $(3)$ 改成 $2x - 2y = -8$ 的話，就會驚喜的發現，加入前解集中唯一的解 $(-1 ,3)$ 依然滿足新加入的方程，則方程組雖然同樣是超定的，但是相容的. 現實中這種概率實在太低了，因此超定往往不相容.

同樣的，亞定也不意味相容.
如上述例子中當方程組中沒有方程時，加入的方程改爲 $0x + 0y = 1$，則 $(x, y)$ 取遍 $\mathbb{R}^2$ 域中的所有點，都將無法滿足之，解集爲空而方程組不相容.
但是，只要亞定的方程組相容，其一定有無窮多解.
因爲在解相容的亞定方程的過程中，總能將 $n - m$ 個變量先視爲不需要解的參量(或稱自由變量)，把他們當作常數寫在等號右邊，最後的解在形式上總是包含這些自由變量.
這時，每個自由變量都可以在定義域 $\mathbb{R}$ 中任意取值，則 $m$ 個解出來的變量的值也跟隨着變化，可以視爲 $m$ 個多元線性函數，其值域也是 $\mathbb{R}$，因而有無窮多解.

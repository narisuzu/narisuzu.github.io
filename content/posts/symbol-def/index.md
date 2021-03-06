---
title: "符號定義"
description: "鳴鈴文本標準化之二"
date: 2021-06-09T04:35:29+08:00
draft: false
math: true
categories: ["standard"]
---
$$
\gdef\uv#1{\hat{\boldsymbol{#1}}}
\gdef\dif{\mathop{}\\!\mathrm{d}}
\gdef\imi{\mathrm{i}}
\gdef\imj{\mathrm{j}}
\gdef\elr{\mathrm{e}}
\gdef\Ft{\mathscr{F}}
\gdef\Lt{\mathscr{L}}
\gdef\dB{\mathrm{dB}}
\gdef\Hz{\mathrm{Hz}}
\gdef\Ohm{\Omega}
\gdef\Volt{\mathrm{V}}
\gdef\Amp{\mathrm{A}}
\gdef\Wat{\mathrm{W}}
\gdef\Col{\mathrm{C}}
\gdef\Far{\mathrm{F}}
\gdef\Var{\mathrm{Var}}
\gdef\milli{\mathrm{m}}
\gdef\micro{\mu}
\gdef\kilo{\mathrm{k}}
\gdef\grad{\mathop{\mathrm{grad}}}
\gdef\dive{\mathop{\mathrm{div}}}
\gdef\rot{\mathop{\mathrm{rot}}}
\gdef\perm#1#2{\^#1\\! P_#2}
\gdef\sgn{\mathop{\mathrm{sgn}}}
$$

本文主要對站內的理工科符號設立標準。因爲博客所設分野較廣，所以呢對於符號的使用需要有一定的原則.
首先，對於標點符號，應采用半角標點。對於公式符號的標準，參考了 ISO、IUPAC、Unicode 和教科書等處的公式后，總結出僅適用於本站的標準。
在本站的其他文章當中底公式符號等若無特殊注明之處皆應爲本頁所載之含義。

一般而言，本標準有幾個原則所約束：

- 變量使用斜體
- 向量/矢量/矩陣等複合量使用粗體
- 算符和單位不適用斜體
- 矩陣使用方括號

```LaTeX
$$
\gdef\uv#1{\hat{\boldsymbol{#1}}}
\gdef\dif{\mathop{}\\!\mathrm{d}}
\gdef\imi{\mathrm{i}}
\gdef\imj{\mathrm{j}}
\gdef\elr{\mathrm{e}}
\gdef\Ft{\mathscr{F}}
\gdef\Lt{\mathscr{L}}
\gdef\dB{\mathrm{dB}}
\gdef\Hz{\mathrm{Hz}}
\gdef\Ohm{\Omega}
\gdef\Volt{\mathrm{V}}
\gdef\Amp{\mathrm{A}}
\gdef\Wat{\mathrm{W}}
\gdef\Col{\mathrm{C}}
\gdef\Far{\mathrm{F}}
\gdef\Var{\mathrm{Var}}
\gdef\milli{\mathrm{m}}
\gdef\micro{\mu}
\gdef\kilo{\mathrm{k}}
\gdef\grad{\mathop{\mathrm{grad}}}
\gdef\dive{\mathop{\mathrm{div}}}
\gdef\rot{\mathop{\mathrm{rot}}}
\gdef\perm#1#2{\^#1\\! P_#2}
\gdef\sgn{\mathop{\mathrm{sgn}}}
$$
```

## 通用

### 量的表記

符號 | 含義 | 自定義宏
----|-----| ---
$\boldsymbol{a}$ | 向量
$\vec{\boldsymbol{b}}$ | 行向量
$x$, $y$ ... | 實變量
$z$, $s$ ... | 複變量
$n$ | 離散變量
$t$ | 時間變量
$f()$ | 實單值函數
$F()$ | 複變函數
$\boldsymbol{f}()$ | 向量值函數
$\boldsymbol{A}()$ | 場函數
$x_n$ | 序列
$\theta$ | 角度，與$z$軸夾角
$\varphi$ | 相角，輻角，功角，與$x$軸夾角
$\varOmega$ | 立體角
$C$, $C_1$, $C_2$ ...| 常量
$\uv\imath$, $\uv\jmath$, $\uv{r}$ ...| 單位向量 | `\uv{}`
$\boldsymbol{e}_1$, $\boldsymbol{e}_2$ ...| 基
$\boldsymbol{M}$ | 矩陣
$\delta(t)$ | 單位衝激函數
$u(t)$ | 單位階躍函數
$\sgn$ | 符號函數 | `\sgn`
$\varPhi$ | 通量

### 常數

符號 | 含義 | 自定義宏
----|-----| ---
$\imi$, $\imj$ | 虛數單位 | `\imi` `\imj`
$\elr$ | 自然底數 | `\elr`
$\pi$ | 圓周率
$\varepsilon_0$ | 真空電容率
$\mu_0$ | 真空電導率
$c$| 真空光速

### 算子或算符

符號 | 含義 | 自定義宏
----|-----| ---
$\dif$ | 微分 | `\dif`
$x'$, $\dot{x}$, $\dfrac{\dif x}{\dif t}$ | 導數
$\int$ | 積分，積分器
$\Ft$|Fourier 變換| `\Ft`
$\Lt$|Laplace 變換| `\Lt`
$\cdot$, $<\ >$ | 内積
$\times$ | 外積
$\ast$ | 捲積
$\Im$ | 虛部
$\Re$ | 實部
$\nabla$, $\grad$ | 梯度 | `\grad`
$\nabla\cdot$, $\dive$ |散度 | `\dive`
$\nabla\times$, $\rot$ | 旋度 | `\rot`
$\perm{n}{r}$| $n$中選$r$的排列數
$n \choose r$| $n$中選$r$的組合數
$\det$ | 方陣的行列式
$^\mathrm{T}$|轉置

### 常用過程量

符號 | 含義 | 自定義宏
----|-----| ---
$\dif t$ | 時間微分
$\dif\ell$ | 綫元
$\dif\boldsymbol\ell$ | 有向綫元
$\dif{S}$ | 面元
$\dif\boldsymbol{S}$ | 有向面元
$\dif V$| 體元
$\dif\varOmega$ | 立體角元

### 集合與空間

集合 | 含義
----|----
$\R$ | 實數
$\mathbb{C}$ | 複數
$\N$ | 自然數
$\R^n$ | $n$ 維歐幾里得空間

### 單位與量綱

單位 | 含義 | 自定義宏
---|---|---
$\Ohm$| 歐姆 | `\Ohm`
$\Hz$ | 赫茲| `\Hz`
$\dB$ | 分貝| `\dB`
$\Volt$ | 伏特| `\Volt`
$\Amp$ | 安培| `\Amp`
$\Wat$ | 瓦特| `\Wat`
$\Var$ | 乏| `\Var`
$\Col$ | 庫倫| `\Col`
$\Far$ | 法拉| `\Far`
$\degree$ | 角度
$\micro$ | $10^{-6}$ | `\micro`
$\milli$ | $10^{-3}$ | `\milli`
$\kilo$ | $10^3$ | `\kilo`

## 科別

### 電磁學

符號 | 含義 | 例
-----|------- | ---
$[\ ]$, $\dim$ | 量綱 | $[F] = N = \mathrm{kg\cdot m\cdot s^{-2}}$
$\rho$ | 體密度
$\sigma$ | 面密度
$\lambda$ | 綫密度

### 電路理論

符號 | 含義 | 例
-----|------|---
$\parallel$ | 并聯 | $\dot{Z_1}\parallel\dot{Z_2} = \dfrac{\dot{Z_1}\dot{Z_2}}{\dot{Z_1}+\dot{Z_2}}$
$A\phase{\varphi}$ | 相量 | $\dot{I}\coloneqq I\elr^{\imj\varphi_i} = I \phase{\varphi_i}$

### 無機化學與分析化學

符號 | 含義 | 例
-----|----- | ----
$[\ ]$ | 濃度 | $K_\text{a} = \dfrac{\ce{[H+][X-]}}{\ce{[HX]}}$
$\ominus$ | 標準狀態 | $\Delta_\mathrm{r} G_\mathrm{m}^\ominus$

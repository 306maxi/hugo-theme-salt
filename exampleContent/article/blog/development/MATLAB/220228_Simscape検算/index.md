---
title: "SimscapeモデルとSimulinkモデルで結果を比較"
linkTitle: "Simscape導入"
date: 2022-02-28
categories:
categories: "Development"
pickups: ["MBD"]
tags:
- MATLAB
- Simulink
- Simscape
- 運動方程式
- 2自由度共振系
description: >
  簡単な2自由度の回転運動をSimscapeでモデリングした結果，モデル要素や接続が十分かどうかを判断できず，振る舞いが確からしいかどうかの確証を得られないという懸念が生じた．
  そこで，検算としてSimscapeのプリミティブモデルで物理モデルを組んだものが，運動方程式からSimulinkの微分演算モデルとして組んだものと同じ振る舞いとなるかを検証する．
marp: true
theme: slide_style
size: 16:9
paginate: true
headingDivider: 3
header: SimscapeモデルとSimulinkモデルで結果を比較
footer: (C)2022 PUES Corp.
---
目的
---
- プラントモデルとして，回転機械の2自由度振動系を考える
- 上記のターゲットをSimscapeのプリミティブ要素から，運動モデルをモデリングしてみる
- 同一ターゲットを運動方程式からSimulinkの微分方程式でモデリングしたモデルとSimscapeのモデルとで結果を比較し，モデリングの妥当性を確認するのが目的

ターゲット
---
$$
W_m=\frac{1}{2}\left(  \frac{J_Ls^2+K}{J_mJ_Ls^2+(J_m+J_L)K} \right)T_m
$$

|値|意味|単位|
|-|-|-|
|Tm, TL|伝達トルク|Nm|
|Wm, WL|角速度|rad/s|
|Jm, JL|イナーシャ|kgm^2|
|K|シャフトのねじり剛性|Nm/rad|

結果
---
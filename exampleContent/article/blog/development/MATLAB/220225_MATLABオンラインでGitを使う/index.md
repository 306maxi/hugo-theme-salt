---
title: "MATLABオンラインでGitを使うには"
linkTitle: "Git統合"
date: 2022-02-25
categories: "Development"
pickups: ["MATLAB"]
tags:
- 開発環境
- 構成管理
- Git
- MATLAB
- Simulink
description: >
  オフライン版のMATLAB/SimulinkではGitリポジトリ操作が統合されている．同様の機能をオンライン版のMATLABで使うにはどのようにすれば良いのかを確認する．
marp: true
theme: slide_style
size: 16:9
paginate: true
headingDivider: 2
header: MATLAB online
footer: (C)2022 PUES Corp.
---

## Gitリポジトリからのクローン
Fileメニューから可能．
GitHubのリポジトリからクローンができることを確認している．  

<br><aside>
💡 社内ローカルのGitサーバにあるリポジトリは外部からアクセスを許可していないのでクローン不可．ファイルでアップロードするか，外部のGitリポジトリを経由する必要あり．
</aside>

## Gitへのコミット
できない．

[Git on Matlab online](https://jp.mathworks.com/matlabcentral/answers/829363-git-on-matlab-online)

>現在、MATLAB Online では git 統合 / ソース管理統合はサポートされていません。この要望は関係者に伝えました。将来のリリースで実装されるかもしれません。

ということらしい

## 2022-03-11追記
いつの間にかGitの項目が!
→ 2022aになっていることが要因かと  

![w:800px](2022-03-11-14-28-52.png)

---

## スライド

<iframe src="slide.html"
            title="スライド表示" width="480" height="270">
</iframe>

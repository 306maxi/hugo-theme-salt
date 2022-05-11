---
date: 2022-04-25
title: "自動運転動向(2022/04版)"
linkTitle: "AutonomousVehicles"
description: "地域ごとの自動運転車OEMなどの動向(2022/04版)"
categories: "Development"
pickups: ["AutonomousVehicle"]
tags:
- 自動運転
share: true
toc: true
comment: true
archives: ["2022年4月"]

marp: true
theme: slide_style
size: 16:9
paginate: true
headingDivider: 2
header: 自動運転動向(2022/04版)
footer: (C)2022 PUES Corp.
---
# <!-- fit --> :memo: 自動運転車両の技術動向 | Lv2+からLv4まで

<!-- _class: title -->

## 国内動向

- あまり注視してこなかったので，現時点であまり情報ない．
- トヨタ(=ウーブンα)がやっとLiDAR捨てる決断をする気である，というくらいが最近のトピック．
[トヨタ子会社ウーブン、自動運転開発に安価なカメラ採用](https://jp.reuters.com/article/toyota-wovenplanet-idJPKCN2LZ00Z)
- おそらく各社のレベル2+...レベル3(ホンダ，日産，スバル)は地図データのある高速道路上でのみ機能する仕組み．一般道ではほぼ使えないはず．スバルが将来的にEyeSightを一般道に拡張したいという記述を見た気がする．
[一般道の自動運転、スバルが実用化へ…歩行者・信号をＡＩが識別](https://www.yomiuri.co.jp/economy/20210920-OYT1T50259/)

## 中国

- 出自がIT系ベンチャー系のいわゆる新興御三家（NIO，XPEV，LI）ではレベル2+(NoA機能相当)はすでに実用段階(ただし，LiDAR+高精度地図によるSLAMのはず．確かNIOがMobileEyeの第4世代(EyeQ4)のローンチカスタマだったか．日産などが同第3世代(EyeQ3))
- ほぼほぼ，TeslaのAPと同等の自律走行性能があるという評を聞く．ただしLiDAR併用．(ローンチ当初よく高速の壁にぶつかっていたが...最近は聞かない)
[死亡事故続く「中国版テスラ」　NIOの車は「自動運転」できない](https://jidounten-lab.com/u_nio-autonomous-tesla)
- 従来の地場OEMはまだLevel2+にちょっと手が届かないくらいの認識．(日系OEMの後方グループと同じ程度の立ち位置？)
- XpengはTeslaと同じく，[自動運転用MPU(SoC)を自前開発に着手](https://36kr.jp/127838/)
- いちおう中華枠のPoleStarもLiDAR搭載．

## 北米

- LiDAR+高精度地図によるジオフェンス方式で，何年も前から先行しているのはWaymo/Cruise(ホンダと提携)/Lyft(トヨタと提携)，旧Toyota Research Instituteもここ．
- 最近，昨年(2021)の当局への各社の運行車両運行距離と事故報告のレポート見たが走行距離と停止回数の少なさはWaymoなどのロボTaxi商用サービスは十分実用域と思える．
- NvidiaのTegra一時の勢いに陰りが見える気がしている．(IVI系の需要はまだあると思うが，AMDが追い上げてきている様に思う)

- [PureVision推進派](https://business.nikkei.com/atcl/seminar/19/00030/061100192/) 
  - 昨年の量産車から前方衝突監視用に搭載していたレーダセンサを削除している．
  - FSDも同等の考えに基づく．(FSD Betaは5/5時点の最新リリースでv10.12．もうまもなくシングルスタック版がリリースか)
> LiDARは(自動車には)無用の長物だ，と[教祖さま](https://techcrunch.com/2019/04/22/anyone-relying-on-lidar-is-doomed-elon-musk-says/)の論．

- インテル子会社なので北米枠に．MobileEyeの商用レベル4タクシーは2021/12月時点で[欧州の許認可待ち](https://www.calcalistech.com/ctechnews/article/rjx3jpgec)．(車両はNIOがベース)
MobileEyeとレンタカー会社の合弁でサブブランド化する様子 : [Moovit AV Mobility Service Robotaxi](https://www.youtube.com/watch?v=EKo18TJ5JCE)
正確なシステム情報を得ていないが，MobileEyeの通常のVisionベースに加えてLiDARを搭載しているように見える．(もともとNIOのes8は量産車にもLiDAR搭載だったと思う)

## 欧州

- OEMの動きに特筆すべきところは無いと思うが，[ドイツがレベル4の公道走行を許可する法案](https://jidounten-lab.com/u_germany-autonomous-law)を通しているので，世界で唯一の一般走行環境での試験場となる可能性が高い．

## 所感

- レベル4の商用TAXIサービスはWaymoなどODD(Operational Design Domain)限定の方式で一定のゴールが見えている様に思う．
- 対して，一般ドライバに代わる自動運転は現在のLiDARを使った方式の延長線上に無いという考えに賛同する．ひとつの方向性としてはEnd-to-Endの機械学習になると思う．
- 一般的に言われているLiDARの欠点は，雨や雪などの気象条件による乱反射，トンネルなどの走行での乱反射によるError，得られる点群画素の解像度の低さおよび色域情報がないためにオブジェクト認識がしにくい(具体的には標識など形状は分かるが文字を読めない)ために補完するセンサとしてカメラが必要ということ．

※ Factの確認は公開Web記事などベース(一般メディアの記述はそれなりにバイアスや誤情報が含まれるているという前提でどうぞ)．参照元情報は別途(内容に誤りあれば都度修正)
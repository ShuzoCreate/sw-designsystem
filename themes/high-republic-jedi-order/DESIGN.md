---
version: alpha
name: High Republic Jedi Order
description: >
  ハイ・リパブリック期ジェダイ・オーダーの様式（非スクリーン系：世界観
  ヴィジュアルからの落とし込み）。白×金の礼装、スターライト・ビーコンの
  窓明かり、放射する翼状のクレスト。「寺院と灯台」— 公共の光としての
  黄金時代のデザインシステム。プリクエル期の禁欲的な茶とは別物。
colors:
  ivory: "#F2EDE2"
  white: "#FBF9F4"
  robe-shadow: "#DCD3C0"
  gold: "#C9A24B"
  gold-deep: "#8A6D2F"
  amber: "#E8B45C"
  beacon-blue: "#9FC4E8"
  ink: "#3A3226"
typography:
  display:
    fontFamily: "'Cormorant Garamond', 'EB Garamond', serif"
    fontSize: 2.2rem
    fontWeight: 500
    letterSpacing: 0.06em
    lineHeight: 1.25
  inscription:
    fontFamily: "Jost, Futura, sans-serif"
    fontSize: 0.7rem
    fontWeight: 400
    letterSpacing: 0.32em
    lineHeight: 1.5
  body:
    fontFamily: "Jost, Futura, sans-serif"
    fontSize: 0.95rem
    fontWeight: 300
    letterSpacing: 0.03em
    lineHeight: 1.7
  aurebesh:
    fontFamily: "Aurebesh, 'Aurebesh AF', sans-serif"
    fontSize: 0.75rem
    fontWeight: 400
    letterSpacing: 0.14em
    lineHeight: 1.4
rounded:
  arc: 999px
  soft: 14px
spacing:
  sm: 10px
  md: 18px
  lg: 32px
  xl: 56px
components:
  crest:
    style: radial-wings
    color: "{colors.gold}"
    fill: solid-allowed
    use: emblem-and-section-marks
  cartouche:
    shape: elongated-plate-notched-ends
    corner-ornament: fan-sunburst
    border: double-line
    use: title-plates
  deco-flourish:
    style: fan-arrow-dingbats
    use: flanking-headings-and-rules
  gilt-border:
    style: woven-geometric
    stroke: "1.5px {colors.gold}"
    use: panel-and-page-edges
  beacon-window:
    style: point-light-grid
    color: "{colors.amber}"
    use: background-texture
  halo:
    style: soft-backlight
    color: "{colors.white}"
    use: focal-elements
  pylon-card:
    orientation: vertical
    background: "{colors.white}"
    border: "{colors.gold}"
    crown: crest
  saber-line:
    style: thin-luminous-rule
    color: "{colors.beacon-blue}"
---

## Overview

High Republic Jedi Orderは、共和国の黄金時代（ハイ・リパブリック期）のジェダイの様式である。これはスクリーンUIではない — 白×金の礼装、スターライト・ビーコンの建築、放射する翼状の紋章という**世界観ヴィジュアルからの落とし込み**であり、物理世界の語彙をそのままwebの素材システムに翻訳する（織り縁取り→ボーダー、窓明かり→背景テクスチャ、後光→発光の扱い）。

大原則は **「寺院と灯台 — 光は公共物である」**。この時代のジェダイは辺境を照らす灯台であり、その意匠は開かれ、輝き、歓迎する。同じジェダイでもプリクエル期の禁欲的な茶の修道士とは別の組織に見えるほど印象が異なる — 本テーマは時代をハイ・リパブリックに固定する。

装飾の語彙は**アール・デコ**である。公式のブランドアイデンティティ（書籍・キーアート）が既にそれを宣言している：扇型（サンバースト）の角飾りを持つ金のカルトゥーシュ、二重線のデコフレーム、テキストを挟む小さな飾り記号、白地に置かれたベタ金の紋章。エレガントで装飾的だが、細い線と幾何学に規律されており、ゴテゴテしたラグジュアリーには決してならない。メイス・ウィンドゥのエレクトラム装飾のライトセーバーが後年まで残るように、金属細工の優美さがこの時代の記憶である。

## Colors

パレットは「白の階調 ＋ 金の系統 ＋ 灯火の2色」。

- **white (#FBF9F4) / ivory (#F2EDE2) / robe-shadow (#DCD3C0):** 礼装の白布の階調。地はこの3段で構成し、影すら温かい。
- **gold (#C9A24B) / gold-deep (#8A6D2F):** 金属装飾の金。線・縁取り・飾り記号の色。**面での使用は紋章とカルトゥーシュにのみ許す**（白地にベタ金の紋章は公式アイデンティティの中核。ただし金の面を背景に使うのは成金 — 大面積は常に白）。
- **amber (#E8B45C):** ビーコンの窓明かり。点として灯る温かい光。
- **beacon-blue (#9FC4E8):** ライトセーバーとステーション照明の淡青。唯一の寒色で、聖なる区切りに少量。
- **ink (#3A3226):** 文字の暖かい黒（純黒ではない）。

黒・グレー・彩度の高い色は存在しない。警告色も存在しない — この様式は危機を語らない。

## Typography

- **見出しは古典的セリフ**（Cormorant系）。碑文の風格だが、nubianの宮廷的な柔らかさより開かれた明快さ。
- **銘（inscription）は極広トラッキングの細サンセリフ大文字。** 石に刻む間隔で、金または墨。
- 本文は細身サンセリフのゆったりした行間 — 経典の読みやすさ。
- オーレベッシュは金の装飾銘として、クレストや縁取りに織り込む。

## Layout

- **中心と放射。** 紋章的な中心軸のシンメトリー。主題を中央に、周囲へ放射状に展開する。
- 余白は豊かに。詰めない — 空間そのものが荘厳さ。
- 縦のピュロン（柱）状カードを並べる構成が基本単位（ビーコンの尖塔群のリズム）。
- ページの縁は gilt-border で額装される。

## Elevation & Depth

- **影ではなく後光。** 焦点要素は背後からの柔らかい白い光（halo）で浮かぶ。ドロップシャドウは存在しない。
- 深度は白の階調差（white > ivory > robe-shadow）で作る浅浮き彫り。
- beacon-window の点状光がテクスチャとして最奥に灯る。
- 全体の印象は「逆光の中の白」— 常にどこかが発光している。

## Shapes

- **円環・放射・翼状。** クレストは中心から放射する翼のモチーフ。円弧とアーチが枠の基本。
- 直角は避け、角は大きな弧か柔らかい丸みで受ける。
- 縁取りは幾何学的な織り模様（連続する菱形・翼形の繰り返し）。ページ・パネルの枠は**二重線＋角の段差（デコのステップ）**で組み、要所の角に扇飾りを置く。
- 鋭利なもの・亀裂・非対称は存在しない（それはsith-orderの語彙）。

## Components

- **crest:** 放射翼のエンブレム。**ベタ金のシルエット**が正式形（白地に置く）。線画版は小サイズの章標用。
- **cartouche:** 端を段状に切った横長の銘板。二重線の枠、四隅に扇型（サンバースト）の飾り。タイトル・ブランド表示の正式な器。
- **deco-flourish:** 見出しや罫線を挟む小さな扇・矢羽の飾り記号。◄ TEXT ► の要領で、テキストの両脇に対で置く。
- **gilt-border:** 織り模様の金縁。パネルとページの額装。
- **beacon-window:** 点状の窓明かりグリッド。背景テクスチャとして最奥に。
- **halo:** 焦点要素の背後の柔らかい後光。ボタンやカードのホバー状態もこれで表現する。
- **pylon-card:** 縦長の白いカード。金の細縁、頂部に小さなクレスト。
- **saber-line:** beacon-blueの細い発光罫線。聖なる区切りにのみ使う。

## Do's and Don'ts

**Do:**

- 白の階調と金の細工で組み、常にどこかを後光で光らせる
- アール・デコの語彙（扇・サンバースト・カルトゥーシュ・二重線フレーム・飾り記号）で装飾の密度を上げる — エレガントは装飾の欠如ではない
- 中心軸シンメトリーと放射の幾何を守る
- 金は線に、amberは点に、beacon-blueは聖なる区切りに
- 余白を荘厳さとして扱う
- 時代をハイ・リパブリックに固定する（茶の修道士ローブはプリクエル期 — 混ぜない）

**Don't:**

- ドロップシャドウ・暗い面・純黒を使わない
- 金のベタ面を紋章・カルトゥーシュ以外に広げない（金は細工であって塗装ではない — 大面積の地は常に白）
- 警告色・エラー色を導入しない（危機はこの様式の語彙にない）
- 鋭利な角・亀裂・非対称を持ち込まない
- スクリーンUI的な計器・データ表示を捏造しない（これは世界の様式であって画面の様式ではない）

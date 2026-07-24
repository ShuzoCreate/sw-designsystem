---
version: alpha
name: Star Tours
description: >
  スター・ツアーズ社の宇宙港パブリックUI（アトラクション実機系）。
  電飾ブルーに発光する出発案内板、三角形のブランドモチーフ、英語と
  オーレベッシュの二言語交互表示。1980年代が思い描いた銀河の民間航空 —
  レトロフューチャーそのものをアイデンティティとして扱う。
colors:
  void: "#0A1030"
  indigo: "#1A2A6E"
  electric: "#3F7FFF"
  glow-cyan: "#6FCFFF"
  chrome: "#C9CFD8"
  flip-orange: "#E8562B"
  gate-amber: "#F2A93C"
typography:
  brand:
    fontFamily: "Michroma, 'Bank Gothic', Eurostile, sans-serif"
    fontSize: 1.4rem
    fontWeight: 400
    letterSpacing: 0.1em
    lineHeight: 1.2
  board:
    fontFamily: "'Share Tech Mono', 'VT323', monospace"
    fontSize: 0.95rem
    fontWeight: 400
    letterSpacing: 0.06em
    lineHeight: 1.5
  aurebesh:
    fontFamily: "Aurebesh, 'Aurebesh AF', sans-serif"
    fontSize: 0.9rem
    fontWeight: 400
    letterSpacing: 0.08em
    lineHeight: 1.4
rounded:
  none: 0px
  sm: 4px
spacing:
  sm: 8px
  md: 14px
  lg: 24px
  xl: 38px
components:
  departure-board:
    columns: [destination, flight, time, status, gate]
    row-style: gradient-bar
    thumbnail: planet-disc
    bilingual: alternating
  gradient-bar:
    fill: "linear {colors.indigo} → {colors.electric}"
    end-cap: arrow-or-chamfer
  triangle-frame:
    shape: triangle
    use: brand-and-destination-preview
  gate-sign:
    text: "{colors.glow-cyan}"
    arrow: "{colors.gate-amber}"
    bilingual: stacked
  segment-column:
    style: stacked-light-segments
    color: "{colors.glow-cyan}"
  flip-board:
    style: led-flip
    color: "{colors.flip-orange}"
    noise: scanline
  chrome-bezel:
    material: brushed-metal
    highlight: specular
---

## Overview

Star Toursは、旅行会社スター・ツアーズ社の宇宙港パブリックUIである（アトラクション実機系テーマ）。出発案内板、ゲート誘導サイン、手荷物検査、安全ビデオ — 銀河の「民間航空」の様式であり、現実の空港サイネージの書式（DESTINATION / FLIGHT / TIME / STATUS / GATE）を銀河に翻訳したもの。

大原則は **「1980年代が思い描いた銀河の空港」**。アトラクションの制作年代に由来するレトロフューチャー — 電飾の滲み、ブラウン管的なブルーム、ブラシメタルの筐体、面取りされた多角形フレーム — は劣化ではなく本質である。現代のフラットUIの精細さではなく、**光る看板としての物質感**で作る。

wayfindingとの違い：あちらは銀河内在のオーレベッシュ単独標示。こちらは**観光客のための二言語表示**（英語とオーレベッシュの交互・併記）が許される唯一のテーマ — スター・ツアーズ社は「外の人」を銀河に迎える会社だから。

## Colors

パレットは「濃紺の夜 ＋ 電飾ブルーの発光 ＋ クロームと限定アクセント」。

- **void (#0A1030) / indigo (#1A2A6E):** 漆黒〜濃紺の地と、バーのグラデーション暗部。画面と看板は常に発光体として夜に浮かぶ。
- **electric (#3F7FFF):** 電飾ブルー。バーのグラデーション明部、フレームの発光。この様式の主役。
- **glow-cyan (#6FCFFF):** 発光文字・サインテキスト。electricより明るい光の色。
- **chrome (#C9CFD8):** ブラシメタル。ロゴ、ベゼル、筐体。スペキュラハイライトを持つ唯一の「素材色」。
- **flip-orange (#E8562B):** フリップボード・警告系の赤橙。対比アクセント。
- **gate-amber (#F2A93C):** ゲート矢印・強調の琥珀。

ブルー系が支配し、橙・琥珀は対比として限定使用。緑や紫は存在しない。

## Typography

- **二言語交互表示がブランドの核。** 英語（幅広ブロック体）とオーレベッシュが交互に切り替わる、または上下に併記される。どちらかを省略しない。
- **オーレベッシュの代替**: 実フォントが利用できない場合は省略せず、短い直線・対角線の線分をグリッド上に組んだ擬似グリフをSVGで生成して装飾に用いる（テキストの置換ではなく併記・装飾として）。 文言を追加・変更できない制約下では、見出しの直下に擬似グリフの装飾行を添えて二言語の体裁を保つ。
- 英語はワイドなテクノサンセリフ（Michroma/Bank Gothic系）— 80年代SFのブロック体。
- 案内板の中身は等幅で、**列見出し＋行データの空港書式**に整列する。
- フリップボード面ではドットマトリクス風に劣化してよい。

## Layout

- **空港のメタファーを忠実に。** 出発案内板は5列（DESTINATION / FLIGHT / TIME / STATUS / GATE）、行は目的地ごとのグラデーションバー、左端に惑星のサムネイルディスク。
- サインは水平バーが基本単位。バーの端は矢印またはチャンファーで終端する。
- バー間にセグメント光柱（縦に積んだ発光セグメント）を区切りとして立てる。
- 三角形（ロゴのモチーフ）が目的地プレビューやブランド表示のフレームとして反復する。

## Elevation & Depth

- 深度は**筐体の物質**で作る。ブラシメタルのベゼル、看板の厚み、埋め込みの奥行き。
- 発光はブラウン管的な滲み（bloom）を伴う。特にフリップボードは走査線ノイズ必須。
- クロームのスペキュラ（鏡面ハイライト）がこの様式にだけ許された贅沢。
- 画面内のドロップシャドウは存在しない — 影は現実の筐体が落とすもの。

## Shapes

- **三角形がブランドモチーフ。** ロゴ、目的地カード、装飾に一貫して現れる。
- 面取りされたシャープな多角形フレーム（角丸ではなく短い斜めカット）— 80年代の「未来のハードウェア」。
- 惑星サムネイルは正円のディスク。
- バーは横長で、グラデーション（indigo→electric）を持つ。端は矢印形かチャンファー。

## Components

- **departure-board:** 5列の出発案内板。行=グラデーションバー＋惑星ディスク＋等幅データ。英語版とオーレベッシュ版が交互に切り替わる。
- **gradient-bar:** indigo→electricのグラデーション横バー。行・サインの基本単位。
- **triangle-frame:** 三角形のフレーム。ブランド表示と目的地プレビュー用。
- **gate-sign:** ゲート誘導。glow-cyanの文字＋gate-amberの矢印、二言語併記。
- **segment-column:** 縦積みの発光セグメント柱。サイン間の区切り。
- **flip-board:** 赤橙LEDのフリップボード。走査線ノイズ付き。レトロ側の端。
- **chrome-bezel:** ブラシメタルの筐体・ベゼル。ロゴにも使う。

## Do's and Don'ts

**Do:**

- 空港サイネージの書式（5列、STATUS語彙、ゲート番号）を銀河語彙に翻訳して使う
- 英語とオーレベッシュを常に対で扱う（交互切替か併記）
- 電飾の滲み・ブラウン管のブルームを残す — レトロは劣化ではなく本質
- 三角形モチーフとグラデーションバーを反復する
- クロームの物質感を要所に

**Don't:**

- 現代のフラットデザイン・高精細タイポに寄せない
- 二言語のどちらかを省略しない（単独表記は wayfinding の掟）
- 緑・紫・多色相を持ち込まない
- 角丸カードUIにしない — 面取り多角形の世界
- 「光る看板」の物質感を失わない（画面はいつも筐体の中にある）

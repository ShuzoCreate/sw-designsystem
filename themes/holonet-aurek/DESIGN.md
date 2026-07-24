---
version: alpha
name: HoloNet Aurek
description: >
  holonetの完全再現変種（第一種・原液）。装飾の強さは色数ではなく、
  「単色相のトーン階層」「地の塗り面」「入れ子の多重フレーム」で作る。
  ギャラクシーズ・エッジの決済端末やテクのバイザーがそのまま映る、
  世界観の再現に全比重を置いた展示級テーマ。
colors:
  background: "#04070D"
  fill-deep: "#0E1B3A"
  fill-band: "#1B2F66"
  fill-zone: "#3A5FB0"
  stroke: "#A9D4FF"
  text: "#D8ECFF"
  muted: "#24406B"
  frame-gold: "#D9A94F"
  affirm: "#3BE86A"
  caution: "#FFB53D"
  alert: "#FF3B30"
typography:
  aurebesh:
    fontFamily: "Aurebesh, 'Aurebesh AF', sans-serif"
    fontSize: 1rem
    fontWeight: 400
    letterSpacing: 0.1em
    lineHeight: 1.3
  display:
    fontFamily: "Michroma, Orbitron, Eurostile, sans-serif"
    fontSize: 1.6rem
    fontWeight: 400
    letterSpacing: 0.14em
    lineHeight: 1.2
  label:
    fontFamily: "Michroma, Orbitron, Eurostile, sans-serif"
    fontSize: 0.62rem
    fontWeight: 400
    letterSpacing: 0.22em
    lineHeight: 1.35
  numeric:
    fontFamily: "'Share Tech Mono', 'JetBrains Mono', monospace"
    fontSize: 0.9rem
    fontWeight: 400
    letterSpacing: 0.08em
    lineHeight: 1.2
rounded:
  none: 0px
  sm: 3px
spacing:
  xs: 3px
  sm: 6px
  md: 10px
  lg: 16px
  xl: 26px
components:
  bezel-frame:
    stroke: "{colors.stroke}"
    nested-lines: 3
    corner-step: true
    corner-cell: 10px
    chamfer: 14px
  band:
    background: "{colors.fill-band}"
    text-color: "{colors.text}"
    rule: "1px {colors.stroke}"
  zone:
    background: "{colors.fill-zone}"
    texture: scanline-grid
    content-color: "{colors.text}"
  icon-cell:
    border: "1px {colors.stroke}"
    background: "{colors.fill-deep}"
    glyph-color: "{colors.stroke}"
  data-column:
    script: aurebesh
    color: "{colors.stroke}"
    on: "{colors.fill-deep}"
  visor-variant:
    frame: "{colors.frame-gold}"
    frame-nested: 4
    inner-zone: "{colors.fill-zone}"
---

## Overview

HoloNet Aurekは、holonetの**完全再現変種（アウレク＝第一字母＝原液）**である。holonetが作中様式を現代のスクリーンで運用できるよう整えたバランス版なら、Aurekは整える前の姿 — ギャラクシーズ・エッジの決済端末、テクのバイザー、CWの艦内モニタにそのまま映っているもの — を再現する。

**装飾の強さは色数ではない。** 作中画面も色相はごく少ない。強いのは装飾の密度であり、それは次の3つで作られる：

1. **単色相のトーン階層** — 同じブルーを暗い帯・中明度の面・明るい線と文字に振り分ける
2. **地の塗り面** — 画面を帯とゾーンの「色の面」で埋め、素の黒をほとんど残さない
3. **入れ子の多重フレーム** — 枠中枠、段付きコーナー、隅のセル

アクセシビリティと情報の速度はこのテーマの目標ではない。展示・プロップ・没入体験のためのテーマであり、それらが最重要のユースケースには適用しない。

## Colors

パレットは「ブルー1系統のトーンランプ ＋ 枠専用ゴールド ＋ 限定ステータス3色」。

- **background (#04070D):** ベゼルの外、機器の黒。画面内ではほぼ見えない。
- **fill-deep (#0E1B3A):** 最も暗い塗り面。アイコンセルの地、余白帯。
- **fill-band (#1B2F66):** ヘッダ／フッタの帯。タイトルとメタ情報が乗る。
- **fill-zone (#3A5FB0):** 主役のコンテンツゾーン。画面中央の明るい面。作中で最も特徴的な「青く光る面」。
- **stroke (#A9D4FF):** 線・枠・グリフの色。**線の色はこれ一色**。
- **text (#D8ECFF):** 見出し・本文。strokeよりわずかに白い。
- **muted (#24406B):** 塗り面上の非アクティブ・補助線。
- **frame-gold (#D9A94F):** 第2色相はこれのみ。**枠と縁取り専用**（テクのバイザー様式）。コンテンツには使わない。
- **affirm / caution / alert:** holonetと同じ意味論。**1画面に1色まで**（APPROVEDの緑帯、警告の赤帯）。

**トーン隣接の禁則:** 近接色相を同一トーンで隣接させない（シアンの線をブルーの線の隣に置く等は禁止）。隣り合う要素は必ず2段以上トーンを離す — 暗い帯の上に明るい線、明るい面の上に白いグリフ。色相を変えるときは役割も変える（gold=枠、blue=中身）。

## Typography

- **オーレベッシュが第一言語。** タイトルにはラテンの直後にオーレベッシュを併記し、キャプション・データ列はオーレベッシュ主体。判読性より文字環境の再現が優先。
- **オーレベッシュの代替**: 実フォントが利用できない場合は省略せず、短い直線・対角線の線分をグリッド上に組んだ擬似グリフをSVGで生成して装飾に用いる（テキストの置換ではなく併記・装飾として）。 オーレベッシュを欠いた画面はこのテーマとして不合格である。
- ラテンは大文字・ワイドトラッキングの幾何学サンセリフ（Michroma系）。決済端末の「WELCOME」のように、見出しは大きく堂々と帯に乗せる。
- 数値はモノスペース。塗り面の隅に小さく散らす。
- 文字は常に塗り面の上に置く。黒地に直接置く文字は最小限。

## Layout

- **1画面＝1ベゼル。** 複数パネルを黒地に浮かべるのではなく、画面全体を1つの多重フレームで囲い、**内部を帯とゾーンで分割**する。これが浮遊パネル型のholonetとの最大の構造差。
- 標準構成: ヘッダ帯（タイトル）→ 主ゾーン（塗り面＋ピクトグラム＋メッセージ）→ 区切り線 → アイコン行 → フッタ帯（微小メタ情報）。
- **装飾密度の下限**: 主要セクションには必ず ①タブヘッダまたは帯タイトル、②ティック列か随伴線、③コーナーセルのいずれか2つ以上を伴わせる。装飾のないプレーンなカードが並んだ時点でこのテーマではない。
- 分割は水平の帯が基本。帯の境界には必ず線か段差を入れる。
- 余白は fill-deep の面で埋める。「何もない黒」を作らない。

## Elevation & Depth

- 深度はトーンで作る: 暗い帯（奥）→ 明るいゾーン（主役）→ 白い線と文字（最前面）。
- グローは控えめに全体へ。線が個別に強く光るより、**面がバックライトのように発光**している印象（LCDの面発光）。
- 塗り面には微細なテクスチャ（走査線、微細グリッド）を敷いてよい。
- ドロップシャドウ・無彩色ぼかしは相変わらず禁止。

## Shapes

- **入れ子の多重フレーム。** 外枠2px＋内側に1pxの随伴線を2〜3本。等間隔ではなく、途中で段差・切り欠き・小部屋を作りながら走らせる。
- **段付きコーナー。** 単純なチャンファーではなく、2〜3段の階段状に折れる角。
- **コーナーセル。** フレームの隅に小さな正方形・矩形の「部屋」を作る（テクのバイザーの四隅）。
- タブ・ノッチ・突起はholonet同様に使ってよいが、必ずフレーム系統色（strokeまたはgold）で。
- 角丸はほぼゼロ。ゾーンの角は大きめのチャンファーで落とす。

## Components

- **bezel-frame:** 画面全体を囲う多重フレーム。stroke色の外枠＋随伴線＋段付きコーナー＋コーナーセル。visor-variantではgold。
- **band:** fill-bandの水平帯。ヘッダ（タイトル＋オーレベッシュ）とフッタ（微小メタ情報）に使う。上下は1pxのstroke線で締める。
- **zone:** fill-zoneの主役面。走査線テクスチャ、白いピクトグラムとメッセージが乗る。縁は内側に1pxの随伴線。
- **icon-cell:** fill-deepの地にstrokeの枠とグリフを持つ小さなセル。横一列に並べる（カードブランド行の様式）。
- **data-column:** fill-deep上を流れるオーレベッシュ列。
- **データ表示（チャート）:** ゾーンの塗り面の中に置く。バーはfill-zone→strokeのグラデ塗り＋1pxの随伴枠、値ラベルは等幅＋擬似オーレベッシュ併記。細い線グラフより太い塗りバーが正しい。
- **visor-variant:** gold多重フレーム＋内部にfill-zoneのカプセル形ゾーン1つ。二色相構成の正しい形（枠=gold／中身=blue、トーンも役割も分離）。

## Do's and Don'ts

**Do:**

- 画面を塗り面（帯・ゾーン）で埋め、素の黒を残さない
- 枠は多重に、角は段付きに、隅にはセルを
- ブルー1系統のトーン階層で奥行きと強弱を作る
- オーレベッシュを第一言語として使う
- goldは枠専用、ステータス色は1画面1色まで

**Don't:**

- 色数を増やして「賑やか」を作らない — 装飾の強さは面と枠の密度で作る
- 近接色相を同一トーンで隣接させない（シアン×ブルー問題）
- 細い単線の枠だけで済ませない（それはholonetの抑制）
- 複数パネルを黒地に浮かべない — 1ベゼル内部を分割する
- 「読みやすくするため」の引き算をしない — それはholonetの仕事（漂白の禁止）

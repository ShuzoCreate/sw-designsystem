---
version: alpha
name: Medcenter
description: >
  銀河の医療施設の様式。暗闇に浮かぶ半透明のガラス円環が、鼓動と分子を
  静かに数え続ける生命維持の光学言語。勢力を横断する技術ドメインで、
  アイスシアンの正常、緑の生体情報、サーモンレッドの警告だけで構成される。
colors:
  background: "#0B141E"
  steel: "#1C242E"
  vital: "#8FE0F0"
  pale: "#EAF6F8"
  bio: "#8FE070"
  alert: "#E8465C"
  glass: "rgba(143, 224, 240, 0.14)"
typography:
  label:
    fontFamily: "Jost, 'Avenir Next', sans-serif"
    fontSize: 0.62rem
    fontWeight: 300
    letterSpacing: 0.22em
    lineHeight: 1.4
  numeric:
    fontFamily: "'Share Tech Mono', 'JetBrains Mono', monospace"
    fontSize: 0.8rem
    fontWeight: 400
    letterSpacing: 0.1em
    lineHeight: 1.3
  aurebesh:
    fontFamily: "Aurebesh, 'Aurebesh AF', sans-serif"
    fontSize: 0.7rem
    fontWeight: 400
    letterSpacing: 0.14em
    lineHeight: 1.3
rounded:
  full: 999px
  none: 0px
spacing:
  xs: 4px
  sm: 8px
  md: 14px
  lg: 22px
  xl: 36px
components:
  scan-ring:
    shape: circle
    stroke: 1.5px
    color: "{colors.pale}"
    glow: soft-bloom
  vitals-bars:
    style: thin-vertical-bars
    color: "{colors.vital}"
    baseline: true
  glass-panel:
    background: "{colors.glass}"
    border: "1px rgba(234,246,248,0.35)"
    blur: subtle
  helix:
    style: double-helix
    color: "{colors.bio}"
  orbit-diagram:
    style: concentric-orbits
    color: "{colors.vital}"
  numeric-column:
    color: "{colors.vital}"
    alert-color: "{colors.alert}"
  warning-glyph:
    shape: triangle
    color: "{colors.alert}"
---

## Overview

Medcenterは、銀河の医療の様式である。ポリス・マッサの分娩監視、クラウド・シティの義手手術、レジスタンス艦のメディポッド — 時代と勢力を横断して、医療のスクリーンだけは同じ言語を話す。holonetが「情報の計器盤」なら、これは**生命の観測装置**だ。

大原則は **「ガラスの円環が、身体に触れずに浮かぶ」**。UIは不透明なパネルではなく、半透明のホログラフィック・レイヤーとして患者の周囲に重畳する。太い線も塗り面もなく、極細のリング・目盛り・波形が静かに明滅する。機械が生命に対して謙虚であること — 画面が主張せず、身体が主役であることが、この様式の倫理である。

## Colors

パレットは「暗い地 ＋ アイスシアンの正常 ＋ 生体の緑 ＋ 警告のサーモン」。

- **background (#0B141E) / steel (#1C242E):** メドベイの暗がりと金属躯体。UIの背後で沈黙する。
- **vital (#8FE0F0):** アイスシアン。稼働中・スキャン中・正常値。この様式の基調で、画面のほぼすべての線と数値。
- **pale (#EAF6F8):** ほぼ白。スキャンリング・光学照準など「物理的な光」の中立色。
- **bio (#8FE070):** 生体分子の緑。DNA螺旋、化学構造、検体。vitalと明確に区別された「生命情報」レイヤー。
- **alert (#E8465C):** サーモンレッド。異常・警告・要注視。**使用は例外的** — 常に少量で、現れた瞬間に画面の意味が変わる。
- **glass:** vitalの半透明面。パネルの地に使う唯一の「面」。

色は3系統（vital/bio/alert）のみで、装飾色は存在しない。ここはkuat-sienarと同じ厳格さだが、任務色ではなく**生死の意味論**で分かれる。

## Typography

- **極細サンセリフ、広めの字間**（Jost/Avenir系 light）。医療機器の刻印のような控えめなラベル。大文字だが、軍用テーマの威圧的なトラッキングより柔らかい。
- **数値は等幅**で小さく、円弧に沿って曲げて配置されることもある。
- オーレベッシュの数値・記号列が「読めなくてもそれらしい」情報密度を作る。段落テキストは存在しない。
- 文字はすべて発光の弱いvital色。alert時のみ赤へ。

## Layout

- **患者が中心、UIは衛星。** レイアウトの原点はスクリーンではなく身体。リングは患者を囲み、パネルは寝台の脇に浮かぶ。
- 円・同心円・円弧を骨格に、矩形パネルは従属的。
- 密度は低〜中。監視するのは数本のバイタルであり、艦橋のような情報の飽和はない。
- 余白は暗がり。埋めない。

## Elevation & Depth

- **すべて半透明のホログラフィック・レイヤー。** 背後の空間が透ける。不透明な面はない。
- 深度は視差で表現する：手前に細く明るい円弧、奥に粗く暗いグリッド。2〜3層。
- 発光はソフトなブルーム。ネオンの鋭さではなく、冷たい蛍光。
- 六角形グリッドや細かい格子が最奥のテクスチャ層として敷かれることがある。

## Shapes

- **円環・同心円・円弧が最頻出。** スキャンリング（光輪）、目盛り環、照準環。矩形より円が常に優先。
- **線は細く均一（1〜1.5px）**、角丸のない鋭い幾何。太線はこの様式に存在しない。
- パネルの縁は硬い枠線ではなく、エッジグローで滲む半透明の境界。
- 波形は縦バーの列（心拍・脈波）。連続曲線よりも離散バー。

## Components

- **scan-ring:** 患者を囲む光輪状のリング。pale色、ゆっくり回転・明滅。スキャン範囲の物理的表示。
- **vitals-bars:** 細い縦バーの列による脈波・心拍表示。基線を持つ。
- **glass-panel:** vitalの半透明ガラス面＋淡い縁。浮遊するデータパネルの地。
- **helix:** bioの二重螺旋・分子鎖。生体分子データの定番グラフィック。
- **orbit-diagram:** 同心軌道リング＋発光球。バイタルの抽象的視覚化。
- **numeric-column:** 等幅の数値列。異常値のみalertに変わる。
- **warning-glyph:** 赤い三角＋感嘆符。この様式でほぼ唯一の明示的ピクトグラム。

## Do's and Don'ts

**Do:**

- UIを半透明に保ち、背後の空間（身体）を透けさせる
- 円環と円弧を骨格にする
- 線は細く、発光は柔らかく、密度は抑える
- alertは例外として温存する — 現れた瞬間に意味が変わる色であること
- bioの緑は生体分子データ専用に守る

**Don't:**

- 不透明なパネル・塗り面・チャンファー枠を持ち込まない（それはholonet系）
- 太線・強いネオングロー・走査線ノイズを使わない
- 画面を情報で飽和させない — 監視は静かであること
- alertを装飾や強調に流用しない
- 3系統以外の色を追加しない

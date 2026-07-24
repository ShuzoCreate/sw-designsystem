---
version: alpha
name: Wayfinding
description: >
  銀河のサイネージ言語（非スクリーン系）。オーレベッシュ単独表記の発光文字が、
  場所の身分と温度を色と形状だけで語り分ける。機能一色の高架標識、商業の
  高彩度スクリーン、庶民のガラス管ネオンという3つのレジスタを持つ。
colors:
  night: "#0A0C14"
  panel-dark: "#14161E"
  teal: "#3FC8C8"
  ad-magenta: "#E040A0"
  ad-orange: "#F28A2B"
  neon-red: "#E8352A"
  neon-ice: "#7FD8F0"
  neon-green: "#4CD97A"
typography:
  aurebesh-display:
    fontFamily: "Aurebesh, 'Aurebesh AF', sans-serif"
    fontSize: 1.6rem
    fontWeight: 400
    letterSpacing: 0.12em
    lineHeight: 1.2
  aurebesh-caption:
    fontFamily: "Aurebesh, 'Aurebesh AF', sans-serif"
    fontSize: 0.8rem
    fontWeight: 400
    letterSpacing: 0.16em
    lineHeight: 1.3
rounded:
  plate: 6px
  neon-oval: 999px
spacing:
  sm: 8px
  md: 16px
  lg: 28px
components:
  register:
    functional: "black plate + teal single-hue + arrow"
    commercial: "high-saturation stacked screens"
    vernacular: "glass-tube neon, oval frames"
  overhead-plate:
    background: "{colors.panel-dark}"
    text: "{colors.teal}"
    arrow: required
  stacked-band:
    style: multi-tier-tower
    hue-per-band: allowed
  tube-neon:
    style: glass-tube
    frame: oval
    pair: two-color
  arrow-glyph:
    style: chunky-triangular
---

## Overview

Wayfindingは、銀河の**サイネージ**の様式である — スクリーンUIではなく、物としての発光標示（非スクリーン系テーマ）。高架のオーバーヘッド標識、歓楽街の積層看板、食堂のガラス管ネオン。

大原則は2つ。第一に **「オーレベッシュ単独表記」** — 銀河の標示は翻訳を添えない。読めない者のための併記は存在せず、文字そのものが風景である。第二に **「場所の身分が色と形を決める」** — 同じ発光文字が、レジスタ（用途階級）によってまったく違う顔になる。

スクリーンUIとの境界線：**情報が動的・映像的ならスクリーン系テーマの領分、静的な銘板・発光素材ならwayfinding**。動く広告スクリーンはcoruscant-neonの範囲だったが、本テーマの商業レジスタに吸収する。

## Colors

パレットは「夜の地 ＋ 3レジスタの発光」。

- **night (#0A0C14) / panel-dark (#14161E):** 都市の夜と標示板の地。サイネージは常に暗さの中で光る。
- **teal (#3FC8C8):** 機能レジスタの単色。方向標示・インフラ標識はこの一色＋矢印だけで完結する。
- **ad-magenta (#E040A0) / ad-orange (#F28A2B):** 商業レジスタの高彩度。猥雑さが正しさであり、複数色相の同時使用も許される唯一のレジスタ。
- **neon-red (#E8352A) / neon-ice (#7FD8F0) / neon-green (#4CD97A):** 庶民レジスタのガラス管ネオン。**2色ペア**（赤×水色、緑×赤）で使うのが definitive。

レジスタを混ぜない。高架標識に商業の色数を持ち込んだ瞬間、身分の言語が壊れる。

## Typography

- **オーレベッシュのみ。ラテン文字の併記禁止。** これがこの様式の最大の掟であり、作中の標示は一貫して翻訳を持たない。
- 機能レジスタ: 端正な等間隔、単色発光、矢印と同格に扱う。
- 商業レジスタ: 大きく、詰め気味に、重ねて。可読性より圧。
- 庶民レジスタ: ガラス管の物理制約による丸みのある字形。二段書き（店名＋業種）が定番。

## Layout

- **標示は1メッセージ1枚。** 文＋矢印、店名＋業種、それ以上を1枚に載せない。
- 商業レジスタのみ**積層**する — 異なる色相の帯・画面を縦に積んだタワー（4段前後）。
- 高架・壁面・建築と一体化して設置される。独立したポールサインは少ない。
- 遠景では標示は都市の光のノイズになる。個の可読性より群の風景。

## Elevation & Depth

- 深度は**筐体の物理**。プレートの厚み、ガラス管の浮き、埋め込みの奥行き。
- 発光は素材由来 — LEDバンドの均一光、ガラス管の芯のある光、スクリーンのバックライト。それぞれ滲み方が違う。
- 商業レジスタのみブルーム強め。機能レジスタは滲まない。

## Shapes

- **プレート**（機能）: 暗い矩形板、控えめな角丸、太い三角矢印。
- **積層バンド**（商業）: 段ごとに色相の違う横帯タワー。
- **楕円フレーム**（庶民）: ガラス管ネオンの定番外形。二重楕円＋二段書き。
- 矢印はチャンキーな三角形。細い洗練された矢印は使わない。

## Components

- **register:** functional / commercial / vernacular の3用途階級。設置場所の身分で選ぶ。
- **overhead-plate:** 高架・天井の方向標示。panel-darkの地＋teal単色＋矢印必須。
- **stacked-band:** 商業の積層看板。段ごとの色相変更を許可。
- **tube-neon:** ガラス管ネオン。楕円フレーム、2色ペア、二段書き。
- **arrow-glyph:** 太い三角矢印。方向情報の主役。

## Do's and Don'ts

**Do:**

- オーレベッシュ単独で書く
- レジスタを設置場所の身分で選び、混ぜない
- 1枚1メッセージを守る
- 発光の質を素材（LED／ガラス管／スクリーン）で描き分ける
- 矢印を文字と同格に扱う

**Don't:**

- ラテン文字を併記しない（それをやるのはstar-toursだけ — あれは観光客向けの例外）
- 機能標示に2色相以上を使わない
- 動的・映像的な表示を持ち込まない（それはスクリーン系テーマの領分）
- 細く上品な矢印・繊細な罫線を使わない
- 標示を情報で満載にしない

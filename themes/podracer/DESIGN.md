---
version: alpha
name: Podracer
description: >
  アウター・リムの即興計器言語。規格なき継ぎ接ぎ — 機能が生き残りを決める。
  錆と砂埃の筐体に移植された不揃いの計器たち。統一規格が存在しないこと
  自体が美的シグネチャーであり、このDESIGN.mdは「逸脱の許容範囲」を定義する。
colors:
  housing: "#5C4A3A"
  dust: "#8A7B68"
  dark: "#2B241D"
  amber: "#F2A93C"
  cyan: "#4FBFDB"
  magenta: "#E0439A"
  green: "#4CD97A"
  signal-red: "#E04A2B"
typography:
  glyph:
    fontFamily: "Aurebesh, 'Aurebesh AF', sans-serif"
    fontSize: 0.8rem
    fontWeight: 400
    letterSpacing: 0.06em
    lineHeight: 1.2
  readout:
    fontFamily: "'VT323', 'Share Tech Mono', monospace"
    fontSize: 1.1rem
    fontWeight: 400
    letterSpacing: 0.08em
    lineHeight: 1.15
rounded:
  bezel: 999px
  panel: 10px
spacing:
  sm: 6px
  md: 12px
  lg: 20px
components:
  round-bezel:
    shape: circle-or-teardrop
    housing: "{colors.housing}"
    weathering: required
  patch-panel:
    rule: mismatched-sizes-allowed
    alignment: none
  engine-diagram:
    style: twin-line-schematic
    state-colors: ad-hoc
  bracket-reticle:
    shape: corner-brackets
  bar-cluster:
    style: mixed-format-bars
  wiring:
    style: exposed
    routing: surface
  crt-bleed:
    scanline: true
    bloom: heavy
    smudge: allowed
---

## Overview

Podracerは、モス・エスパの経済圏 — 中古と鹵獲と改造で回るアウター・リム — の計器様式である。ポッドレーサーのコックピット、実況ブースの寄せ集めモニター壁、石造アーチに埋め込まれた後付けセンサー。

大原則は **「規格の不在がアイデンティティ」**。同じ双発エンジン監視画面ですら、状態ごとに緑バー、青縞、白フレアと無節操に色が変わる。実況ブースでは筐体寸法も形式も異なるモニターが無秩序に並ぶ。これは怠慢ではなく生態系だ — 動く部品だけが生き残り、統一デザインなど誰も発注していない。ただし完全な無秩序ではなく、**生き残った部品には共通の血** — 円形ベゼル、滲む発光、剥き出しの配線 — が流れている。このDESIGN.mdが定義するのは規格ではなく、その「逸脱の許容範囲」である。

## Colors

パレットは「砂と錆の筐体 ＋ その場しのぎの発光色」。

- **housing (#5C4A3A) / dust (#8A7B68) / dark (#2B241D):** 打痕のある金属、砂岩、焦げ茶の暗部。UIの地はスクリーンではなく風化した物体。
- **amber (#F2A93C):** コックピット計器の支配色。迷ったらこれ。
- **cyan (#4FBFDB):** 寄せ集めモニターの色。別の機械から来た部品の色。
- **magenta (#E0439A) / green (#4CD97A) / signal-red (#E04A2B):** その場しのぎのパラメータ色。

**色の意味論は存在しない — それがこの様式の掟である。** 赤=危険のような体系を作り込んではならない。色はパラメータごとにその場で割り当ててよい。ただし条件が2つ：①1つの計器の中では読み分けられること、②全体としてamberが支配的であること（そうしないとただのカオスになり、タトゥイーンの琥珀色の空気が消える）。

## Typography

- オーレベッシュは**手彫りのように不揃い**でよい。量産フォントの均質さを避け、字形・ウェイトの揺れを許容する。
- 数値はドットマトリクス／セグメント風（VT323系）。計器ごとにサイズが違ってよい。
- ラテン風UIと絵記号が同じ壁に混在してよい（実況ブースの寄せ集め）。
- 統一書体という概念自体を持ち込まない。

## Layout

- **整列しない。** 統一グリッドは存在しない。計器は「取り付けられる場所に取り付けられた」配置であり、間隔も軸も揃わない。
- 寸法の異なるパネルの同居が標準（patch-panel）。大きなモニターの隣に小さな丸ゲージ。
- ただし各計器の内部は機能的 — 読めない計器は捨てられて生き残らない。無秩序は計器の「間」にあり、「中」にはない。
- 配線・パイプが計器の間を這う。UIの領域は配線に侵食されてよい。

## Elevation & Depth

- 深度は**物理的な取り付け**の深さ。埋め込まれた丸窓、飛び出したゲージ、ねじ止めされたモニター。
- 発光はブラウン管的な強い滲み（bloom）。エッジのシャープなデジタル発光は存在しない。
- ガラス面の曇り・反射・指紋を許容する。視認性より使い込まれた実在感。
- 走査線・ノイズ・にじみが常在。

## Shapes

- **円形・涙滴形のベゼル**が繰り返し現れる唯一の共通モチーフ。丸窓、丸ゲージ、丸モニター。
- 角括弧のブラケット照準（HUD、フレーム装飾）。
- 双発エンジンのライン図（左右対称の2ユニット概略図）が定番グラフィック。
- 筐体は風化必須（weathering: required）— 新品のきれいな枠はこの世界に存在しない。
- 角丸は大きめでいびつでよい。

## Components

- **round-bezel:** 円形／涙滴形の計器窓。錆びたhousingに埋め込まれ、風化が必須。
- **patch-panel:** 寸法・形式の不揃いなパネルの寄せ集め。整列させないことが正しい。
- **engine-diagram:** 双発エンジンのライン概略図。状態表示の色はその場割り当て（ad-hoc）。
- **bracket-reticle:** 角括弧のHUD照準。
- **bar-cluster:** 形式の混ざったバー群（縦バー、縞バー、ドット列が同居）。
- **wiring:** 剥き出しの表面配線。計器と計器を物理的につなぐ視覚要素。
- **crt-bleed:** 強いブルーム＋走査線＋曇りのオーバーレイ。

## Do's and Don'ts

**Do:**

- 計器ごとに形式・寸法・色を変える — 揃えないことが正しい
- amberを支配色に保ち、その下で色をその場割り当てする
- 円形ベゼル・滲む発光・剥き出し配線という「最低限の共通の血」は守る
- 筐体を風化させる（錆・打痕・砂埃・曇り）
- 各計器の内部は読めるように — 機能しない部品は生き残らない。**風化・曇り・にじみは可読性の最低線を割らないこと**（ラベルと数値が一読できない計器は「壊れた部品」であり、この世界では捨てられている）

**Don't:**

- 色の意味体系を作り込まない（赤=危険で統一、はこの世界にない）
- グリッドに整列させない、書体を統一しない
- 新品の質感・シャープなデジタル発光・クリーンな枠を使わない
- 1画面に情報を統合しない — 計器は分散した物体の群れであること
- 他テーマの規律（チャンファー、ヘアライン、単色相システム）を持ち込まない

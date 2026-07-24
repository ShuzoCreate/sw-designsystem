---
version: alpha
name: First Order
description: >
  ファースト・オーダーの黒曜ガラス様式。磨き上げられた漆黒の面に
  血赤のヘアライン線画と精密なモジュール群。帝国美学を先鋭化した、
  冷たく静かな威圧のインターフェース。
colors:
  background: "#08080B"
  gloss: "#101017"
  crimson: "#FF1F2F"
  crimson-dim: "#5A0F14"
  steel: "#C9CED6"
  steel-dim: "#3A3F49"
  cobalt: "#3E55FF"
  signal: "#FFD23A"
typography:
  display:
    fontFamily: "'Saira Condensed', 'Roboto Condensed', 'Arial Narrow', sans-serif"
    fontSize: 1.4rem
    fontWeight: 500
    letterSpacing: 0.3em
    lineHeight: 1.15
  label:
    fontFamily: "'Saira Condensed', 'Roboto Condensed', 'Arial Narrow', sans-serif"
    fontSize: 0.68rem
    fontWeight: 400
    letterSpacing: 0.34em
    lineHeight: 1.3
  numeric:
    fontFamily: "'IBM Plex Mono', 'Share Tech Mono', monospace"
    fontSize: 0.85rem
    fontWeight: 400
    letterSpacing: 0.06em
    lineHeight: 1.25
rounded:
  none: 0px
spacing:
  xs: 3px
  sm: 6px
  md: 10px
  lg: 18px
  xl: 30px
components:
  module:
    border-color: "{colors.steel-dim}"
    border-width: 1px
    background: "{colors.gloss}"
    header-color: "{colors.steel}"
  tracking-grid:
    line-color: "{colors.crimson}"
    line-dim: "{colors.crimson-dim}"
    line-width: 1px
    target-color: "{colors.signal}"
  dot-column:
    dot-color: "{colors.crimson}"
    dot-off: "{colors.crimson-dim}"
    dot-size: 4px
  schematic:
    line-color: "{colors.cobalt}"
    overlay-color: "{colors.crimson}"
  status-strip:
    background: "{colors.crimson}"
    text-color: "{colors.background}"
---

## Overview

First Orderは、スターキラー基地・フィナライザー・スプレマシーの艦内に見られるファースト・オーダーの様式である。銀河帝国の系譜を継ぎながら、より冷たく、より静かに、より精密に研ぎ澄まされている。

大原則は **「黒曜石の板に、血で引いたヘアライン」**。スクリーンは磨かれた黒ガラスであり、そこに1pxの赤い線が完璧な精度で走る。holonetの線が「情報の光」なら、First Orderの線は「監視の光」である。飾りは一切なく、対称と反復と直線だけが権威を語る。ユーザーを歓迎しない — 従わせるUIである。

## Colors

パレットは「黒2階調 ＋ 赤2階調 ＋ 鋼2階調 ＋ 限定信号色2」。

- **background (#08080B):** 漆黒。青みを帯びた黒曜石。
- **gloss (#101017):** モジュール内部の面。光沢の気配だけ僅かに明るい。
- **crimson (#FF1F2F):** 主役の血赤。追跡グリッド、データ線、警告。この様式の「インク」。
- **crimson-dim (#5A0F14):** 赤の残light。非アクティブ、グリッド補助線、消灯ドット。
- **steel (#C9CED6):** 鋼の白。構造線、モジュール見出し、罫線。赤より一段「事務的」な情報。
- **steel-dim (#3A3F49):** 鋼の影。枠線、区切り。
- **cobalt (#3E55FF):** スキーマティック専用の青。機関図・回路図にのみ現れる。
- **signal (#FFD23A):** 追跡対象のマーカー黄。画面内に一点だけ許される最大強調。

運用: 黒が80%、crimson系 12%、steel系 6%、cobalt/signal 2%。**緑は存在しない** — この様式に「承認」の色はなく、正常は沈黙（消灯）で示す。

## Typography

- **コンデンス（縦長）サンセリフ、極端に広いトラッキング**（0.3em以上）。大文字のみ。文字を一つずつ引き離して刻印する、規律の文字組み。
- 見出しはsteel、データ値はcrimson。色で「構造／内容」を分ける。
- 数値は等幅（IBM Plex Mono系）で小さく、桁を揃えて列にする。
- 文字は小さくてよい。読ませるためではなく、記録されていることを示すための文字である。

## Layout

- **モジュールの反復。** 同寸の矩形モジュールを規則正しく敷き詰める。holonetの非対称な寄せ集め感を排し、完全なグリッド整列。
- **密度は高く、しかし静か。** 要素は多いが、各要素の主張は最小。アクティブな箇所だけがcrimsonに点る。
- 中央に主ビューポート（追跡グリッド）、両翼に細いデータ列という対称構成が基本。
- ヘッダは細い罫線1本とラベルのみ。飾り帯は使わない。

## Elevation & Depth

- 深度は**ガラスの光沢**で示す。面の端にわずかなハイライト（steelの1pxエッジ）、要素自体に影はない。
- crimsonのグローは最小限 — 鋭く滲まない発光。holonetより硬く、vectorscopeより細い。
- レイヤーは明度でなく**点灯/消灯**で区別する。手前=点灯（crimson）、奥=残光（crimson-dim）。
- 反射・映り込みの気配（微かな縦のハイライト）は様式の一部。

## Shapes

- **完全な直角。** 角丸ゼロ。チャンファーすら使わない（それは民間のholonet）。矩形、台形、細長い帯だけで構成する。
- **ヘアライン（1px）主義。** 線は常に細く、正確に。太線は存在しない。
- **ドットの列。** 状態表示は正方形に近い小さなドット／短冊の整列（dot-column）。点灯パターンが唯一の「動き」。
- 台形の切り落とし（コンソール筐体の角度）は許されるが、装飾的ノッチは不可。

## Components

- **module:** steel-dimの1px枠＋glossの面＋steelの小さな見出し。同寸で敷き詰める基本単位。**内容物で満たすこと** — ドット列やストリップは筐体の高さいっぱいまで反復させる。空隙の目立つモジュールは規律の欠如に見え、この様式を壊す。
- **tracking-grid:** crimsonのヘアラインによる透視／球面グリッド。補助線はcrimson-dim。追跡対象はsignal黄の塊で、画面内に一つだけ。
- **dot-column:** crimsonドットの縦列インジケータ。点灯/消灯のパターンで状態を伝える。
- **schematic:** cobalt線の機関図・回路図。crimsonのオーバーレイで注記が重なる。
- **status-strip:** 唯一の塗り面。crimsonの帯に黒の大文字。警告・封鎖・命令の表示専用。

## Do's and Don'ts

**Do:**

- 1pxのヘアラインで、完璧な直線と対称を保つ
- 正常状態を沈黙（消灯・crimson-dim）で、異常だけをcrimsonで語らせる
- モジュールを同寸で反復し、規律を見せる
- signal黄は画面に一点だけ — 追跡対象、最重要マーカーのみ
- 黒ガラスの光沢（微かなエッジハイライト）を残す

**Don't:**

- 角丸・チャンファー・ノッチなどの造形的装飾を使わない
- 緑を使わない（承認・安全の色はこの様式に存在しない）。汎用UIの状態表示は **正常=沈黙（steel-dim/消灯）、注意=steelの輪郭、遮断・警告=crimsonの塗り** に写像する。signal黄はバッジ色ではなく「追跡中の一件」専用
- 太い線、強いグロー、にじみを使わない
- 非対称なコラージュ的レイアウトにしない（それはholonet/vectorscope）
- 温かみのある色、人間味のある書体を持ち込まない

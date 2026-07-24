---
version: alpha
name: Kuat-Sienar
description: >
  クワット・ドライヴ・ヤーズ（KDY）とシエナー・フリート・システムズ（SFS）が
  機体と共に納品する艦載管制様式（ローグ・ワン／アンドー期の帝国艦隊に遍在）。1画面1色相の単色システム
  （緑・赤・青・白のステーション別）、精密なヘアライン、頂点から放射する
  扇形幾何、半透明の塗りウェッジ。理路整然とした無機質さで統治を可視化する。
colors:
  background: "#0A0D0C"
  surface: "#121815"
  green: "#59E87F"
  red: "#FF4726"
  blue: "#7FB0FF"
  blue-wedge: "#3D63C4"
  white: "#EDF2F4"
  lavender: "#9C8FE8"
  amber: "#E8A33C"
typography:
  aurebesh:
    fontFamily: "Aurebesh, 'Aurebesh AF', sans-serif"
    fontSize: 0.85rem
    fontWeight: 400
    letterSpacing: 0.08em
    lineHeight: 1.4
  label:
    fontFamily: "Michroma, Orbitron, Eurostile, sans-serif"
    fontSize: 0.6rem
    fontWeight: 400
    letterSpacing: 0.26em
    lineHeight: 1.35
  numeric:
    fontFamily: "'Share Tech Mono', 'JetBrains Mono', monospace"
    fontSize: 0.82rem
    fontWeight: 400
    letterSpacing: 0.06em
    lineHeight: 1.25
rounded:
  none: 0px
  frame: 14px
spacing:
  xs: 4px
  sm: 8px
  md: 12px
  lg: 20px
  xl: 32px
components:
  station-panel:
    hue: one-per-panel
    border-width: 1.5px
    corner-radius: "{rounded.frame}"
    tab-notch: true
  radial-fan:
    line-width: 1px
    origin: vertex
    density: high
  range-wedge:
    fill: translucent
    stroke: 1px
  ring-dial:
    style: radial-tick-ring
    tick-count: 60+
  segment-pill:
    shape: rounded-pill
    glow: strong
  trapezoid-chip:
    shape: trapezoid
    states: outline-or-filled
  dot-grid:
    dot-size: 3px
    use: status-matrix
  tick-ruler:
    style: irregular-survey
---

## Overview

Kuat-Sienarは、ローグ・ワンと『アンドー』に映る帝国艦隊の管制様式である。スター・デストロイヤーの艦橋ピット（クワット・ドライヴ・ヤーズ建造）、TIEファイターのコックピット（シエナー・フリート・システムズ製）、デス・スターの兵器管制 — これらの計器盤は機体を製造した軍需メーカーが機体と一緒に納品するものであり、様式は勢力ではなく**メーカー群のデザイン言語**として銀河に流通している。帝国はその最大の顧客というだけだ（だからこの名は「帝国全体の標準UI」を主張しない — ISBの白いオフィス端末や旧式のvectorscope系CRTも帝国内に併存する）。連名はSienar-JaemusやKuat-Entrallaと同じ、銀河企業の命名文法に倣う。

帝国艦のスクリーンは装飾のためでなく**統治の精度を誇示するため**にある。理路整然とし、無機質で、冷たく美しい。

3つの原則：

1. **1画面1色相の単色システム。** ステーションごとに任務の色（緑=航行/機関、赤=兵装/警戒、青=索敵/照準、白=計測）が与えられ、その画面はその色相だけで描かれる。vectorscopeの「1ビューポート1フォスファー」の直系だが、太いブラウン管の素朴さではなく——
2. **ヘアラインの精密幾何。** 1pxの線が、頂点から放射する扇、等間隔の目盛り、完全な同心円を描く。手描きの揺らぎは存在しない。
3. **塗りは扇形で。** 面の塗りは半透明のウェッジ（扇形・楔形）として現れる。レンジの範囲、出力の割合 — 量は角度と面積で語られる。

firstorderはこの様式の直系の末裔である（imperialから曲線と多色を奪い、赤だけを残したもの）。

## Colors

パレットは「黒＋任務色4系統＋補助2色」。**同時に使うのではなく、パネルごとに1色相を選ぶ**。

- **background (#0A0D0C):** かすかに緑がかった黒。艦の消灯面。
- **surface (#121815):** パネル内部の面。ごくわずかに持ち上げる。
- **green (#59E87F):** 航行・機関・船体状態。ISD制御盤の線画。
- **red (#FF4726):** 兵装・警戒・封鎖。帝国の象徴色。橙寄りの赤。
- **blue (#7FB0FF) / blue-wedge (#3D63C4):** 索敵・照準・レンジ。線はblue、塗りウェッジはblue-wedge（同系統の暗色 — トーンで分離）。
- **white (#EDF2F4):** 計測・基準線・中立データ。白い放射ダイヤル。amberと同様に、**どのパネルにも基準線・輪郭として少量置ける例外色**（青のレンジファンに白のISD線画と基準線、など）。
- **lavender (#9C8FE8):** whiteパネルの補助アクセント（インジケータ、選択状態）。
- **amber (#E8A33C):** オーレベッシュの銘・注記専用。どのパネルにも少量置ける唯一の色。

対比色は1パネルに1つまで（緑の線画に赤の充填ゲージ、青のレンジに赤の目標マーカー）。3色相目は存在しない。

## Typography

- **オーレベッシュが実務の文字。** ラベル・注記・数値はオーレベッシュ主体（amberまたはパネル色相）。ラテンは運用上の最小限（このテーマを汎用UIに適用する場合のみ、Michroma系の大文字・極広トラッキングを許す）。
- **オーレベッシュの代替**: 実フォントが利用できない場合は省略せず、短い直線・対角線の線分をグリッド上に組んだ擬似グリフをSVGで生成して装飾に用いる（テキストの置換ではなく併記・装飾として）。
- 本文段落が存在する数少ない様式（保安局の報告書端末）。オーレベッシュの整然としたテキストブロックを、細い行間で組む。
- 数値は等幅。目盛りに沿って小さく、機械的に。

## Layout

- **パネル＝ステーション。** 各パネルは任務単位で、自分の色相を持つ。1画面に複数パネルを並べる場合も、パネル間で色相が混ざらない。
- **放射と対称。** 主役のグラフィックは頂点・中心から放射する（扇、リング、レンジファン）。左右対称のペア構成（Empire UIの左右パネル）を好む。
- 縁は目盛り（不等間隔の測量目盛り）、ドットグリッド、小さな状態チップで縁取る。
- 密度は高いが、holonet-aurekのような装飾の飽和ではなく、**計測器の必然としての密度**。

## Elevation & Depth

- 深度はほぼゼロ。すべて同一のガラス面。
- 塗りウェッジの半透明の重なりだけが唯一の「層」。重なりは同系色の濃淡で表現する。
- グローは色相ごとに控えめに。redのみやや強い発光を許す（警戒の色だから）。
- 影・ぼかし・グラデーション装飾は存在しない。

## Shapes

- **角丸フレーム（frame = 14px）＋タブ切り欠き。** 帝国の枠は角が丸い（Empire UIの赤枠）。角丸の途中にタブ・段差・切り欠きが入る。チャンファーは使わない（それはholonet系）。
- **放射扇（radial-fan）。** 1本の頂点から数十本のヘアラインが扇状に開く。
- **六角形・シェブロン。** 六角の環、山形（chevron）の入れ子。円よりも六角を好む。
- **台形チップ。** 状態表示は台形の小片の列（塗り/輪郭の2状態）。
- **ピルセグメント。** 強い発光を持つ丸端の短冊が数珠つなぎになる。
- 白い基準線は水平・垂直・斜めの完全な直線のみ。

## Components

- **station-panel:** 角丸＋タブ切り欠きの枠。パネル色相の1.5px線。内部はbackground（塗り面はウェッジのみ）。
- **radial-fan:** 頂点から放射するヘアライン群。レンジファン、走査扇、装飾格子。
- **range-wedge:** 半透明の塗り扇形。レンジ・出力・カバレッジの量的表示。輪郭1px＋塗り。
- **ring-dial:** 60本以上の放射ティックで構成される円環計器。中心にオーレベッシュの略号。
- **segment-pill:** 発光する丸端短冊の列。エネルギー流・進行の表示。
- **trapezoid-chip:** 台形の状態チップ列。塗り=活性、輪郭=待機。
- **dot-grid:** 小ドットの行列。多数の系統の一括状態表示。
- **tick-ruler:** 不等間隔の測量目盛り。基準値の位置だけ長い。

## Do's and Don'ts

**Do:**

- パネルごとに任務色1色相を選び、それだけで描く（対比1色まで）
- 量は角度と面積（ウェッジ）で示す
- 放射・対称・等間隔 — 幾何学の規律を守る
- オーレベッシュを実務の文字として使い、amberの銘を添える
- 角丸フレームにタブと切り欠きを入れる

**Don't:**

- 複数の任務色を1パネルに混ぜない
- 線を太らせない（太線はvectorscopeの素朴さ。帝国は常にヘアライン）
- チャンファー・ブラケット・多段ノッチを使わない（それはholonet系の民間装飾）
- 有機的な曲線・手描きの揺らぎを持ち込まない
- 汎用UIに適用する場合、状態色は任務色の割当に従わせる（成功/失敗の慣習色より任務の色相が優先）

---
version: alpha
name: Nubian
description: >
  ナブー王室船（J-type 327 Nubian級）の計器様式。銀河で唯一の「明るい」スクリーンUI —
  クリームとピーチの温かな地に、円形の計器、コーラルに発光する縁、
  セージグリーンの銘板。量産品ではなく工芸品として作られた優雅なインターフェース。
colors:
  shell: "#E9DCC6"
  blush: "#D9A38A"
  ground: "#F3C9A2"
  coral: "#FF8A55"
  ember: "#E85C30"
  plum: "#3A1B33"
  sage: "#8FA84E"
  sky: "#9FC6E4"
  violet: "#B48AC8"
typography:
  display:
    fontFamily: "'Cormorant Garamond', 'EB Garamond', serif"
    fontSize: 1.6rem
    fontWeight: 500
    letterSpacing: 0.12em
    lineHeight: 1.3
  label:
    fontFamily: "Jost, Futura, 'Avenir Next', sans-serif"
    fontSize: 0.72rem
    fontWeight: 400
    letterSpacing: 0.22em
    lineHeight: 1.4
  numeric:
    fontFamily: "Jost, Futura, 'Avenir Next', sans-serif"
    fontSize: 1rem
    fontWeight: 300
    letterSpacing: 0.1em
    lineHeight: 1.2
rounded:
  full: 999px
  soft: 20px
spacing:
  xs: 6px
  sm: 10px
  md: 16px
  lg: 28px
  xl: 44px
components:
  dial:
    shape: circle
    ring-color: "{colors.coral}"
    ring-glow: "0 0 18px"
    face: "{colors.ground}"
    segment-color: "{colors.ember}"
  plaque:
    background: "{colors.sage}"
    text-color: "{colors.shell}"
    shape: capsule
  viewport-inset:
    background: "{colors.plum}"
    frame-color: "{colors.coral}"
    content-tint: "{colors.sky}"
  gauge-arc:
    track-color: "{colors.blush}"
    fill-color: "{colors.ember}"
  console:
    background: "{colors.shell}"
    seam-color: "{colors.blush}"
---

## Overview

Nubianは、ナブー王室のスターシップ（TPMのロイヤル・スターシップ、AOTCの王室クルーザー）に見られる計器様式である。名はクワイ＝ガンが劇中で船を呼んだ「J-type 327 Nubian」から — 船体設計・建造はシード王宮造船工廠、推進系はヌービア・スター・ドライブズで、「ヌビアン」は映画自身がこの船に与えた呼称である。銀河のスクリーンがほぼ例外なく「暗闇に光る線」であるなか、ナブーだけが**明るい地に描く**。クロームの船体と同じ思想 — 機能を隠さず装飾として磨き上げる — がUIにも貫かれ、量産品ではなく銀細工師が作った工芸品のように見える。

大原則は **「計器は宝飾、画面は陶磁」**。スクリーンはクリーム地の陶板のようで、円形の計器がコーラル色の熱を帯びて発光し、緑の銘板が要所に打たれる。冷たい情報機器の気配を徹底的に排し、温かく、対称で、優雅であること。

## Colors

パレットは「温かな地色3階調 ＋ 発光するコーラル ＋ 差し色3色」。

- **shell (#E9DCC6):** 筐体・コンソールのクリーム。大面積の地。
- **blush (#D9A38A):** 地色の影側。継ぎ目、トラック、非アクティブ。
- **ground (#F3C9A2):** 計器盤面のピーチ。発光しているような温かい面。
- **coral (#FF8A55):** この様式の「光」。計器の縁、リング、アクティブ要素。常に柔らかなハロー（グロー）を伴う。
- **ember (#E85C30):** コーラルの濃色。ゲージの充填、重要セグメント、強調。
- **plum (#3A1B33):** 唯一の暗色。スキーマティックや映像を映す小窓（viewport-inset）の奥。暗色は「窓の中」にのみ存在する。
- **sage (#8FA84E):** 銘板・ラベルの緑。オーレベッシュの刻印用。
- **sky (#9FC6E4):** 小窓内のワイヤーフレーム・映像のトーン。
- **violet (#B48AC8):** 3D表示の透過体、装飾的アクセント。稀に。

運用: shell/blush/ground で75%、coral/ember 15%、plum窓 5%、sage/sky/violet 5%。**黒は存在しない**。影すら茶系（blushを暗くした色）で描く。

## Typography

- **見出しはセリフ体**（Cormorant Garamond系）。銀河で唯一、人文主義的な文字が許される様式。刻印のような落ち着いた字間。
- **ラベル・数値は細身の幾何学サンセリフ**（Jost/Futura系、ライト級）。大文字＋広めトラッキングだが、holonetの機械的な硬さではなく、案内板の上品さ。
- オーレベッシュはsageの銘板（plaque）に刻む。銘板はカプセル形で、要所に少数。
- 数字は細く、目盛りに沿って円弧状に配置されることが多い。

## Layout

- **対称と同心。** レイアウトの基本は円と、円を並べた対称構成。矩形グリッドではなく、大きな円形計器を中心に衛星のように小計器を配す。
- **余白は豊か。** holonetの詰め込みと正反対に、計器と計器の間に地色をたっぷり取る。
- 曲線の流れ。コンソールの継ぎ目（seam）は曲線で、UIの区切りも直線より弧を好む。
- 情報は「一目で読む計器」単位。表やリストを避け、ダイヤル・アーク・銘板で伝える。

## Elevation & Depth

- 深度は**素材の重なり**で表現する：陶板の上に金属リング、その上にガラスの小窓。各層はわずかな暖色の影（ドロップシャドウではなく、blush系の接地影）を持つ。
- coralの発光は熱のようなハロー。シアン系のシャープなネオンではなく、夕陽の滲み。
- plumの小窓だけが「奥」を持つ — 暗い奥行きにskyの線画が浮かぶ。それ以外の面は浅浮き彫り。

## Shapes

- **円、楕円、カプセル。** 直角はこの様式に存在しない。ビューポートも計器も銘板もすべて丸みで構成する。
- **リングとセグメント。** 円形計器の縁は太いcoralのリングで、扇状に分割されたセグメント（ember）が状態を示す。
- **角丸は大きく柔らかく**（soft = 20px、多くは完全な円/カプセル）。
- 縁取りは二重線や細い金属モールのように繊細に。太い無骨な枠はない。

## Components

- **dial:** 円形計器。coralの発光リング＋ground面＋中心のシンボルまたは小窓。縁に沿ってティックと細数字。**必ずshellの物理ベゼル（成形された台座）に埋まって見えること** — 画面に直接描かれた円ではなく、筐体に嵌め込まれた計器である。密度は同心方向に稼ぐ：ベゼル→発光リング→セグメント環→目盛り環→数字環→小窓、とリングを重畳させる。
- **plaque:** sageのカプセル銘板。オーレベッシュ（または大文字ラベル）をshell色で刻む。計器の上下に添える。
- **viewport-inset:** plumの暗い小窓。skyトーンの映像・ワイヤーフレームを映す。縁はcoralの細いモール。
- **gauge-arc:** 円弧ゲージ。blushのトラックにemberの充填。先端に小さな球。
- **console:** shellの大きな曲面パネル。blushの曲線シームで領域を仕切る。

## Do's and Don'ts

**Do:**

- 明るい地に描く — 暗色はplumの小窓の中だけ
- 円・楕円・カプセルで構成し、対称に配置する
- coralの発光に柔らかなハローを与える（夕陽の滲み、シアンの鋭さは禁物）
- セリフ体の見出しと細身サンセリフのラベルで上品に
- 余白を豊かに取り、計器を宝飾のように独立させる

**Don't:**

- 黒・純白・シアンを使わない（冷たい色はこの様式を殺す）。汎用UIの警告にも赤を導入しない — 状態は **良好=sageの塗り、注意=emberの輪郭、警告=emberの塗り** で写像する
- 直角、チャンファー、鋭い切り欠きを使わない
- 情報を詰め込まない — 表やデータグリッドはこの世界にない
- 機械的なモノスペース数字の羅列を避ける
- グリッチ、走査線、ノイズ演出を持ち込まない（工芸品は劣化しない）

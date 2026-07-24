---
version: alpha
name: HoloNet
description: >
  銀河でもっとも広く普及したスクリーンUIの標準様式。漆黒の背景に、
  シアン／ブルーを主体とした発光する線と文字だけで情報を描く。
  時代・場所・組織を特定しない、銀河の共通視覚言語。
colors:
  background: "#04070D"
  surface: "#0A1420"
  primary: "#5BD8FF"
  line: "#2E7BFF"
  muted: "#1B3A55"
  affirm: "#3BE86A"
  caution: "#FFB53D"
  alert: "#FF3B30"
  text: "#D8F4FF"
typography:
  display:
    fontFamily: "Michroma, Orbitron, Eurostile, sans-serif"
    fontSize: 1.5rem
    fontWeight: 400
    letterSpacing: 0.18em
    lineHeight: 1.2
  label:
    fontFamily: "Michroma, Orbitron, Eurostile, sans-serif"
    fontSize: 0.75rem
    fontWeight: 400
    letterSpacing: 0.24em
    lineHeight: 1.4
  numeric:
    fontFamily: "'Share Tech Mono', 'JetBrains Mono', monospace"
    fontSize: 1rem
    fontWeight: 400
    letterSpacing: 0.08em
    lineHeight: 1.2
  aurebesh:
    fontFamily: "Aurebesh, 'Aurebesh AF', sans-serif"
    fontSize: 0.7rem
    fontWeight: 400
    letterSpacing: 0.12em
    lineHeight: 1.2
rounded:
  none: 0px
  sm: 2px
spacing:
  xs: 4px
  sm: 8px
  md: 12px
  lg: 20px
  xl: 32px
components:
  panel-frame:
    border-color: "{colors.line}"
    border-width: 1.5px
    chamfer: 16px
    notch-depth: 8px
    background: "{colors.background}"
    glow: "0 0 8px"
  gauge-segmented:
    segment-on: "{colors.primary}"
    segment-off: "{colors.muted}"
    segment-gap: "{spacing.xs}"
    segment-radius: "{rounded.sm}"
  grid-wireframe:
    line-major: "{colors.line}"
    line-minor: "{colors.muted}"
    line-width: 1px
    marker-friendly: "{colors.affirm}"
    marker-hostile: "{colors.alert}"
  status-chip:
    background-affirm: "{colors.affirm}"
    background-alert: "{colors.alert}"
    text-color: "{colors.text}"
    chamfer: 8px
  button-keypad:
    border-color: "{colors.primary}"
    background: "{colors.surface}"
    text-color: "{colors.primary}"
    chamfer: 6px
  divider-tick:
    color: "{colors.muted}"
    tick-length: 6px
    tick-gap: "{spacing.sm}"
---

## Overview

HoloNetは、スター・ウォーズの銀河でもっとも普及したスクリーンUIの標準様式である。反乱軍の作戦室からアウター・リムの決済端末まで、時代（プリクエル〜シークエル）と場所を問わず現れる。共和国とも帝国とも紐付かない、いわば銀河ベーシック標準語の視覚版。

大原則は **「暗闇の中で、光る線そのものが情報である」**。スクリーンは常に暗い環境（コックピット、艦橋、酒場のカウンター）で光ることを前提とし、UIは面の塗りではなく発光するストローク（線・文字・目盛り）で構成される。背景は表示面ではなく「無」であり、そこに引かれた線がすべての意味を担う。

これは現代のフラットデザインの再解釈ではない。ベクタースキャンCRTとオシロスコープの語彙 — ワイヤーフレーム、レーダー掃引、セグメントゲージ — を持つレトロフューチャーな計器盤である。

## Colors

パレットは「漆黒の地 ＋ 発光する数色」で構成され、**色は装飾ではなく意味論**である。

- **background (#04070D):** ごくわずかに青みを帯びた漆黒。画面の70〜85%を占める。純黒 (#000) より一段浮いた「通電しているガラス」の色。
- **surface (#0A1420):** パネル内部をわずかに持ち上げる暗青。使うのは階層を示す最小限の場面のみ。
- **primary (#5BD8FF):** シアン。本文テキスト、アイコン、アクティブなゲージ、グリッドの主線。この様式の「インク」。
- **line (#2E7BFF):** 深いブルー。パネル枠、構造線、ワイヤーフレームの輪郭。primaryより一段沈み、構造と内容を描き分ける。
- **muted (#1B3A55):** 非アクティブ。消灯セグメント、グリッド補助線、待機状態。
- **affirm (#3BE86A):** グリーン。承認・完了・味方・航行クリア。「APPROVED」の帯、味方機マーカー。
- **caution (#FFB53D):** アンバー。注意・スキャン中・照準過程。レーダーの掃引扇、追尾中の目標。
- **alert (#FF3B30):** レッド。敵性・警告・拒否。敵機マーカー、警告テキスト。
- **text (#D8F4FF):** 発光する白（シアンの残光を含む）。最重要の見出し語のみ。

運用比率の目安: background/surface 80%、primary/line 15%、affirm/caution/alert 合わせて5%。アクセント3色は同一ビューに同時に多用しない — 意味が衝突する。

発光（グロー）は色と同色相で行う。シアンの線にはシアンのにじみ。白いドロップシャドウや無彩色のぼかしは存在しない。

## Typography

- **すべて大文字、ワイドトラッキング。** 見出し (display) は0.18em、ラベル (label) は0.24em。文字は詰めずに「計器の刻印」として置く。
- **書体は幾何学的テクノサンセリフ**（Michroma / Orbitron / Eurostile系）。ヒューマニストな丸みや手書き感は禁止。
- **数値はモノスペース** (numeric)。座標、残量、クレジット額など、桁が変動しても揺れないこと。
- **オーレベッシュの併記** (aurebesh)。見出しの脇や下に小さく添える装飾的コ・ブランディングとして使う。作中ではそれが本文だが、この再現においては雰囲気の担保が役割。ラテン文字なしでオーレベッシュ単独の重要情報を作らない。
- **オーレベッシュの代替**: 実フォントが利用できない場合は省略せず、短い直線・対角線の線分をグリッド上に組んだ擬似グリフをSVGで生成して装飾に用いる（テキストの置換ではなく併記・装飾として）。
- 長文の段落は存在しない。テキストは常に短いラベル、ステータス語、数値である。

## Layout

- **情報密度は高く、余白はタイト。** これは閲覧するドキュメントではなく監視する計器盤。spacing スケール（4/8/12/20/32px）の範囲で詰める。
- **非対称なパネル分割。** メインのビューポート（星図、レーダー、スケマティック）を大きく取り、脇に細いゲージ列・データ列を沿わせる。均等グリッドの整列よりも、機能ブロックの寄せ集め感が正しい。
- **縁は目盛りで飾る。** パネルの辺にはティックマーク（目盛り列）、短い座標値、小さな注記が並ぶ。空いた縁は計器の未使用領域であり、装飾で埋めない。
- **画面端まで使う。** ステータス行やIDコードは四隅に張り付く。中央寄せの安全マージンという概念はない。

## Elevation & Depth

**影は存在しない。深度は光で表現する。**

- 手前・アクティブ = 明るく、強いグロー。奥・非アクティブ = muted に沈む。
- レイヤーの重なりはドロップシャドウではなく、輝度差と輪郭線の有無で描く。
- モーダルやフォーカスは、背後の線の輝度を落とす（消灯に近づける）ことで成立させる。
- ワイヤーフレームの3D表現（透視グリッド、球面グリッド）は奥行きを線の密度と細さで示す。フォグやブラーは使わない。

## Shapes

- **角丸ではなくチャンファー（45°の面取り）。** パネルの角は16px程度で斜めに落とす。全角を落とす必要はなく、対角2箇所などの非対称も様式内。
- **ノッチと切り欠き。** 枠線の途中に段差・切り欠き・突起を入れ、機械部品の成形物らしさを出す。純粋な矩形は避ける。
- **輪郭線ファースト。** 領域は塗りではなく1〜1.5pxの枠線で示す。塗り面を使うのはstatus-chipの帯とゲージのセグメントのみ。
- **円は計器として使う。** レーダーの同心円、照準環、球面ワイヤーフレーム。装飾の円形アバターは存在しない。
- 角丸 (rounded.sm = 2px) はセグメントやチップの角の「刺さり」を取る用途に限る。

## Components

- **panel-frame:** チャンファー付きの枠線パネル。1.5pxの line 色ストローク、同色のグロー、内部は background。タイトルは枠の上辺に食い込む形で置き、脇にオーレベッシュを添える。
- **gauge-segmented:** イコライザ状の分割バーゲージ。点灯セグメントは primary（状態により affirm/caution/alert）、消灯は muted。連続的なプログレスバーは使わない — 必ず離散セグメント。
- **grid-wireframe:** 透視グリッド／レーダー。主線 line、補助線 muted、掃引や照準は caution。マーカーは味方 affirm・敵性 alert のシルエットアイコン。
- **status-chip:** 「APPROVED」式の結果表示帯。唯一の大きな塗り面。チャンファー付き矩形に affirm/alert の塗り、白い大文字テキスト。画面の主役として中央に置いてよい。
- **button-keypad:** 物理キーパッド由来の押下要素。surface の地に primary の枠と文字。ホバー/押下はグロー強度の変化で表現する。
- **divider-tick:** 目盛り列による区切り。実線の代わりに短いティックの繰り返しで領域を区切る。

## Do's and Don'ts

**Do:**

- 線・文字・目盛りを発光させ、それ以外を闇に沈める
- 色の意味論を守る（青=情報、緑=肯定、黄=注意、赤=脅威）
- チャンファー、ノッチ、ティックマークで機械的な輪郭を作る
- 数値・座標・IDコードを縁に散らして計器感を出す
- グローは常に同色相で

**Don't:**

- 塗り面で領域を作らない（status-chipとゲージセグメントを除く）
- ドロップシャドウ、無彩色のぼかし、フォグを使わない
- 大きな角丸、カード型UI、グラデーション豊富なモダンスタイルを持ち込まない
- アクセント3色（affirm/caution/alert)を装飾目的で使わない
- 小文字の長文、ヒューマニストな書体、ゆったりした余白を使わない

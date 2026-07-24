---
version: alpha
name: ISB
description: >
  帝国保安局の様式（『アンドー』）— 無彩色の連続階調で語る無機質・硬質の
  官僚制建築。儀礼空間は明るい面が主役でファセット浮彫は稀少な仕上げ、
  実務空間はチャコール〜黒が主役で白は縁を締める細い輪郭線。
  データは暗端の中の琥珀の微光、警告は赤の点。監視官僚制の大聖堂。
colors:
  white: "#EDEEF0"
  white-shadow: "#CDD0D4"
  grey: "#9BA0A6"
  lacquer: "#0B0C0E"
  glass: "#3C4046"
  data-amber: "#E8A33C"
  signal-red: "#D93A2B"
  cog-grey: "#85888C"
typography:
  label:
    fontFamily: "'Saira Condensed', 'Roboto Condensed', sans-serif"
    fontSize: 0.66rem
    fontWeight: 500
    letterSpacing: 0.3em
    lineHeight: 1.35
  numeric:
    fontFamily: "'IBM Plex Mono', 'Share Tech Mono', monospace"
    fontSize: 0.78rem
    fontWeight: 400
    letterSpacing: 0.08em
    lineHeight: 1.3
  aurebesh:
    fontFamily: "Aurebesh, 'Aurebesh AF', sans-serif"
    fontSize: 0.7rem
    fontWeight: 400
    letterSpacing: 0.12em
    lineHeight: 1.3
rounded:
  none: 0px
  ring: 999px
spacing:
  xs: 4px
  sm: 8px
  md: 14px
  lg: 24px
  xl: 44px
components:
  facet-wall:
    pattern: triangular-relief
    scale: fine
    contrast: low
    shading: soft
    use: rare-signature-accent
  sunburst-crown:
    style: radial-louver-ring
    blades: 48+
    color: "{colors.white}"
    use: single-instance-fixture
  edge-light:
    style: thin-contour-line
    color: "{colors.white}"
    use: outline-for-dark-volumes
  lacquer-inlay:
    material: gloss-black
    corner: hard
    inset-screens: true
  cog-idle:
    glyph: imperial-cog
    color: "{colors.cog-grey}"
    on: "{colors.glass}"
  indicator-dots:
    size: 3-5px
    colors: ["{colors.data-amber}", "{colors.signal-red}"]
    quantity: sparse
  ring-layout:
    geometry: circle-and-radial
    use: primary-composition
  data-ledger:
    color: "{colors.data-amber}"
    on: "{colors.lacquer}"
    density: minimal
---

## Overview

ISBは、『アンドー』に映る帝国保安局の様式である。核となるイメージは**無彩色の連続階調で語る官僚制建築**。会議室や聴聞室のような儀礼の空間は、白灰のファセット（三角形の低浮彫）を稀少な仕上げとして持つ明るいモノリスであり、制服の白い人間までもがその表面の一部になる。一方、監視室やワークステーション区画のような実務の空間は、チャコール〜黒がほぼ全面を占め、白は輪郭を締める細い縁光としてのみ現れる。データは暗端の中で琥珀に微光し、警告は赤い点として刺さる。

kuat-sienar（軍・艦載）が「統治の精度の誇示」なら、ISBは**監視官僚制の大聖堂**である。装飾はなく、しかし貧相でもない — 幾何学の反復そのものが権威を語る。温かみは存在しない。柔らかさも存在しない。硬質、清潔、完全。

**この様式の洗練は「引き算」から生まれる。** ファセット浮彫は聴聞室の壁のような特別な瞬間にのみ、ごく控えめに現れる仕上げであり、画面を埋め尽くす繰り返し柄ではない。素面の無地こそが基本であること。同様に、白が常に主役とは限らない — 監視室やワークステーション区画はチャコール〜黒がほぼ全面を占め、白は輪郭を締める細い縁光としてのみ現れる。**どちらの明暗に振るかは空間の格で選び、グレースケールの階調で語る**（白か黒かの二択ではない）。この引き算と諧調の精度こそが「一昔前のジオメトリック背景パターン」から遠ざける唯一の道である。

## Colors

パレットは「white→lacquerの連続した無彩色の階調 ＋ 微小な信号」。5色の無彩色トークンは**離散した2色（白／黒）ではなく、ひとつづきの明度スケール**として扱う。

- **white (#EDEEF0) → white-shadow (#CDD0D4) → grey (#9BA0A6) → glass (#3C4046) → lacquer (#0B0C0E):** 明から暗への連続階調。**冷たい中性色**（温かみのある骨白・クリームは誤り）。

**空間の格で、この階調のどこを主役にするかが決まる（2レジスタ）：**
- **儀礼レジスタ**（会議室、聴聞室前室）: white / white-shadow が支配的。lacquerは家具・スクリーン筐体としてごく少量、硬い塊として置かれる。
- **実務レジスタ**（監視室、ワークステーション区画）: glass / lacquer が支配的。white は縁を締める細い輪郭線（edge-light）としてのみ現れる — 面としては使わない。

どちらのレジスタでも、**使う階調は隣接する2〜3段に絞る**（whiteといきなりlacquerを同じ画面で同格に対比させない）。段を飛ばさず滑らかに移行することが「洗練」であり、極端な白黒二値は素人っぽさの原因になる。

- **data-amber (#E8A33C):** データの琥珀。暗い面（glass/lacquer）の中の小さな読み出しにのみ。
- **signal-red (#D93A2B):** 警告・稼働中の赤い点。ドット単位で使う。
- **cog-grey (#85888C):** アイドル画面の帝国コグ。glass面に低コントラストで。

明るい面の上に彩色を置かない — 色（琥珀・赤）は必ず glass・lacquer などスケールの暗端の中に封じられる。

## Typography

- コンデンス大文字・極広トラッキング、ウェイトはやや強め（500）— 硬質な刻印。
- 明るい面の上の文字は grey/lacquer の無彩色のみ。暗い面の上の文字は white/grey。彩色文字（琥珀）は暗端の中だけ。
- 数値は等幅で少量。台帳は疎ら（数行、広い行間）— 情報を出し惜しむ者が情報を持つ者である。
- オーレベッシュは銘板・部署コードとして少量。

## Layout

- **円環と放射が第一幾何。** 円環のテーブル、扇形の座席、放射状の天井ルーバー。ISBの部屋は円と放射でできており、直交グリッドは従属的。
- **レジスタごとに地と図が反転する。** 儀礼レジスタでは明るい面が地、lacquerの塊が図。実務レジスタではglass/lacquerが地、edge-lightで縁取られた要素が図。1つの画面内でレジスタを混在させない。
- 対称・求心的な構図。中心に向かって権力が集まる部屋の構造をそのまま使う。
- **余白は無地であることが基本。** テクスチャ（facet-wall）は例外的なごちそうであり、常時働いているものではない。空白を埋めたくなったら、まず「本当に埋める必要があるか」を疑う。

## Elevation & Depth

- **深度は諧調の推移。** 明暗スケールを隣接ステップで移行させることで浅い立体感を作る（whiteからwhite-shadowへ、glassからlacquerへ）。段を飛ばした急な明暗差は使わない。
- **黒い塊はedge-lightで締める。** lacquer/glassの暗い塊は、縁に沿った細い白／grey の輪郭線（edge-light）でシルエットを明確にする。ソフトなグローや周辺減光ではなく、精密な1本の線であること — これが「しまった黒」を作る唯一の方法。
- 黒漆の面は鏡面反射（微かなハイライト）を持つ。
- **発光・グローは存在しない。** 琥珀のデータも「点灯」であって「発光」ではない — 滲まない。
- 儀礼レジスタでは天井のサンバースト（放射ルーバー、1空間に1基のみ）が光源。実務レジスタは環境光が冷たく低く、光源は画面内に写り込まない。

## Shapes

- **鋭い直線と完全な円環。** 角丸なし。曲線は円環と放射にのみ許される。
- **ファセット（三角形の低浮彫）は稀少な署名要素。** コントラストは低く（隣接する2階調のみ）、スケールは細かく、儀礼レジスタの特定の壁面1箇所程度に留める。画面全体のタイル壁紙にしない — それは幾何学模様の背景パターンであり、この様式の無機質さを損なう。
- **放射ルーバー**（sunburst-crown）: 48枚以上の白い羽根が環状に並ぶ王冠。1構成に1基のみの実際の照明器具として扱う。反復する装飾モチーフではない。
- 黒漆の塊は台形・帯・円弧 — 常にハードエッジ、常にedge-lightで縁取る。
- 装飾的な切り欠き・ブラケット・チャンファーは一切ない。

## Components

- **facet-wall:** 三角形低浮彫の白灰テクスチャ。**低コントラスト・細かいスケール・稀少使用**（1画面に多くて1箇所、儀礼レジスタの壁面のみ）。ページ全体の地には使わない。
- **sunburst-crown:** 放射状ルーバーの環。1構成に1基、実在の照明器具として。見出し・中心要素の背後に象徴的に使うのは可だが複数配置しない。
- **edge-light:** 暗い塊の輪郭を締める細い白／grey の一本線。ソフトなグローの代替であり、精密さの担保。
- **lacquer-inlay:** 黒漆のスラブ。ハードエッジ、微かな鏡面、edge-light併用。スクリーン・データ・操作系はすべてこの中に象嵌される。
- **cog-idle:** glass面のコグ透かし。無操作のスクリーンの標準状態。
- **indicator-dots:** 琥珀・赤の微小ドット列。黒漆の縁に沿って疎らに。
- **ring-layout:** 円環＋放射の構図テンプレート。中央に主題、環状に従属要素。
- **data-ledger:** 黒漆内の琥珀の台帳。数行・広い行間・滲まない点灯。
- **データ表示（チャート）:** 黒漆の中でも「彩色は点」を守る — 柱はglassの灰、琥珀は値ラベル・現在値マーカーの点にのみ。琥珀の大きな塗り面はこの様式の禁欲を壊す。可能なら円環・放射（リング進捗、扇形配分）を優先する。

## Do's and Don'ts

**Do:**

- 明暗スケールを隣接ステップで使い、儀礼／実務のレジスタで主役の階調を切り替える
- ファセットは稀少・低コントラストな署名要素として、多くて1画面1箇所に留める
- 黒い塊はedge-light（細い一本線）で締める — ソフトなグローではなく精密な輪郭で
- 円環と放射で構図を組む
- 彩色（琥珀・赤）は暗端の中に封じ、点として使う

**Don't:**

- 温かい白（クリーム・ボーン）にしない — 冷たい中性の無彩色であること
- ファセットや幾何学模様を画面全体のタイル壁紙・背景パターンにしない（それは量産テンプレートの意匠であり、この様式の無機質な洗練を壊す）
- 白と黒をいきなり同格に対比させない（段を飛ばした二値化は素人っぽさの原因）
- 発光・グロー・滲みを使わない（点灯はするが発光はしない）
- 明るい面の上に彩色を直接置かない
- 角丸・チャンファー・装飾切り欠きを使わない
- レジスタを混同しない — 儀礼レジスタで黒を主役にしない、実務レジスタで白を面として広げない（実務空間ではglass/lacquerが多数派で正しい）

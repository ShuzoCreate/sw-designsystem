# starwars-md — screen languages of a galaxy

スター・ウォーズ**作中に登場するスクリーンUI**のヴィジュアルを再現する、テーマ別 DESIGN.md 集。

商業的な「スター・ウォーズ風デザイン」ではなく、作中世界のキャラクターが実際に見ているスクリーン — コックピットの計器、艦橋のディスプレイ、決済端末 — のUIそのものを対象にしています。

**▶ ギャラリー: https://shuzocreate.github.io/sw-designsystem/**

## DESIGN.md とは

各テーマは [google-labs-code/design.md](https://github.com/google-labs-code/design.md) のフォーマット仕様に従った `DESIGN.md` — 色・書体・形状のトークンと様式の掟を、コーディングエージェント向けに記述したファイルです。

テーマの `DESIGN.md` をエージェントに渡すだけで、そのテーマに沿った画面を生成できます。ギャラリーの各テーマページにある「汎用UIへの適用」は、プロジェクトのコンテキストを持たないエージェントが `DESIGN.md` だけを読んで同一の汎用アプリを着装した実例です。

```
# 例: 好きなテーマの DESIGN.md をエージェントに渡す
themes/holonet/DESIGN.md   → 銀河標準のダーク×ネオンで実装させる
themes/nubian/DESIGN.md    → ナブー王室船のエレガント様式で実装させる
```

## テーマ

| テーマ | 概要 |
|---|---|
| [HoloNet](themes/holonet/DESIGN.md) | 銀河標準のダーク×ネオン |
| [Nubian](themes/nubian/DESIGN.md) | 銀河唯一のエレガント |
| [First Order](themes/firstorder/DESIGN.md) | 黒曜ガラスと血赤の線 |
| [High Republic Jedi Order](themes/high-republic-jedi-order/DESIGN.md) | 白と金、寺院と灯台 |
| [Vectorscope](themes/vectorscope/DESIGN.md) | 無銘の単色ベクターCRT |
| [ISB](themes/isb/DESIGN.md) | 監視官僚の骨白と炭黒 |
| [Kuat-Sienar](themes/kuat-sienar/DESIGN.md) | 帝国艦隊の単色管制 |
| [Star Tours](themes/star-tours/DESIGN.md) | 80年代が描いた銀河民間航空 |
| [Medcenter](themes/medcenter/DESIGN.md) | 暗闇に浮かぶガラスの円環 |
| [Podracer](themes/podracer/DESIGN.md) | アウター・リムの即興計器 |
| [HoloNet Aurek](themes/holonet-aurek/DESIGN.md) | 銀河標準の、最も濃い姿 |
| [Sith Order](themes/sith-order/DESIGN.md) | 暗闇に走るひとつの光の傷 |
| [Wayfinding](themes/wayfinding/DESIGN.md) | 銀河のオーレベッシュ・サイネージ |
| [Visor](themes/visor/DESIGN.md) | 視界そのものが計器 |

## 構成

```
themes/<name>/DESIGN.md  … テーマ本体（トークン定義＋設計根拠）。これが成果物
docs/                    … ビルド済みギャラリーサイト（GitHub Pagesが main /docs から配信）
```

## ライセンス

[MIT](LICENSE)。DESIGN.md・コード・文章はこのライセンスで自由に利用できます。スター・ウォーズ固有の名称・設定に関する権利は Lucasfilm Ltd. に帰属し、本ライセンスの対象外です。

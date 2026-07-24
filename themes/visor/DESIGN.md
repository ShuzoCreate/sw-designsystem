---
version: alpha
name: Visor
description: >
  視界に重畳する光学HUDの様式。マクロバイノキュラー、ヘルメットバイザー、
  照準スコープ、ドロイドPOV。単色の光の膜が視界そのものを計器化する —
  見ることが即ち測ることである。スクリーンではなく「レンズ越しの世界」のUI。
colors:
  mask: "#050505"
  ir-red: "#E8352A"
  ir-red-deep: "#4A0805"
  night-green: "#3DDC97"
  night-blue: "#12233F"
  amber: "#B87333"
  amber-deep: "#5C3317"
  mono-pale: "#D8E4E8"
typography:
  readout:
    fontFamily: "'Share Tech Mono', 'JetBrains Mono', monospace"
    fontSize: 0.78rem
    fontWeight: 400
    letterSpacing: 0.12em
    lineHeight: 1.25
  aurebesh:
    fontFamily: "Aurebesh, 'Aurebesh AF', sans-serif"
    fontSize: 0.7rem
    fontWeight: 400
    letterSpacing: 0.1em
    lineHeight: 1.25
rounded:
  full: 999px
spacing:
  sm: 8px
  md: 14px
  lg: 24px
components:
  visor-mask:
    shape: horizontal-oval
    temple-notch: true
    edge: "{colors.mask}"
  sensor-mode:
    rule: one-duotone-per-view
    modes: [ir-red, night, amber, mono]
  reticle:
    style: concentric-crosshair
    stroke: 1.5px
  range-ring:
    style: tick-arc-dial
  hex-lock:
    shape: hexagon
    use: target-acquisition
  target-marker:
    shape: diamond-or-bracket
    label: true
  corner-readout:
    position: corners-and-bottom-band
    style: segment-digits
  grain:
    scanline: true
    noise: subtle
    flicker: micro
---

## Overview

Visorは、スクリーンを持たないUIの様式である。マクロバイノキュラー、パイロットのヘルメットバイザー、爆撃照準器、ドロイドの視覚 — 画面の代わりに**視界そのもの**があり、そこに光の膜が重畳する。

大原則は **「見ることが即ち測ることである」**。生の視界は単色フィルターに変換され（赤外の赤、暗視の緑、砂漠の琥珀）、レティクル・目盛り・数値がその同じ色で焼き付く。すべての描画が同一の発光色を持つのは、それらが**同一のセンサーの出力**だからだ。そして視界の縁には常にハードウェアの影 — バイザーの形をした黒いマスク — があり、これがレンズ越しであることを忘れさせない。

## Colors

パレットは「黒いマスク ＋ センサーモード別のデュオトーン」。**1視界1モード**（vectorscope/kuat-sienarの1画面1色相の光学版）。

- **mask (#050505):** バイザー枠の黒。視界の外周を囲む。純黒に近い。
- **ir-red (#E8352A) / ir-red-deep (#4A0805):** 赤外・照準モード。明部と暗部のデュオトーン。
- **night-green (#3DDC97) / night-blue (#12233F):** 暗視モード。緑の描画と青黒の視界。
- **amber (#B87333) / amber-deep (#5C3317):** 砂漠・望遠モード。琥珀のデュオトーン。
- **mono-pale (#D8E4E8):** モノクロ・グレイン モード。白黒の粒子の粗い視界。

モードを混ぜない。ターゲットマーカーも数値もレティクルも、そのモードの明部色一色で描く。第二色はデュオトーンの暗部（視界側の色）だけ。

## Typography

- **等幅・セグメント風の数値**が主役。座標、距離、速度のカウンタが刻々と更新される。
- オーレベッシュのグリフ列が数値に添う。ラベルは3〜4文字の略号まで。
- 文字は視界の**縁のゾーン**に置かれる（四隅、下端の帯）。視界の中心は空けておく — そこは見るための場所。
- すべてモードの発光色。文字専用色は存在しない。

## Layout

- **中心は空、縁に計器。** レティクルだけが中心を占有できる。数値・状態・スケールバーは四隅と上下端の帯に退避する。
- 左右対称。縦スケールバー（目盛＋三角ポインタ）が左右に対で立つことが多い。
- 密度は薄い。視界を遮るUIは本末転倒であり、要素は10個未満。

## Elevation & Depth

- 深度は「視界＝奥」「描画＝手前の膜」の2層だけ。描画層に内部の重なりはない。
- 発光は蛍光管的な滲み（ブルーム）＋ハレーション。輝度はノイズで微振動する。
- **走査線・フィルムグレイン・ノイズが常在**。クリーンな画面はこの様式に存在しない — 劣化こそがセンサーの実在感。
- ヴィネット（視界周辺の減光）でレンズの光学特性を再現する。

## Shapes

- **視界の形＝横長オーバル（俵型）、こめかみ側に鋭角のノッチ。** バイザーの物理形状が画面の輪郭を決める。双眼鏡型は真円、爆撃照準は全面＋円弧の縁飾り。
- レティクルは同心円＋クロスヘア。ロックオンは六角形。マーカーはダイヤモンドか括弧ブラケット。
- 距離環・角度ダイヤル: 縁に沿ったティック付き円弧。
- 収束するワイヤーフレーム照準線（爆撃照準）。
- 線は1〜2px。すべての図形は「刻まれた光」で、塗り面はない。

## Components

- **visor-mask:** 視界を囲む黒いマスク。横長オーバル＋こめかみノッチが標準形。UIはこの内側にのみ存在する。
- **sensor-mode:** デュオトーンのモード切替（ir-red / night / amber / mono）。ビューごとに1モード。
- **reticle:** 同心円＋クロスヘア照準。中心専用。
- **range-ring:** ティック付き円弧の距離環・角度ダイヤル。
- **hex-lock:** 六角形のロックオン枠。捕捉時に対象へ吸着する。
- **target-marker:** ダイヤモンド／ブラケットのマーカー＋短いラベル。
- **corner-readout:** 四隅・下端帯の数値カウンタ。等幅、常時更新。
- **grain:** 走査線＋粒状ノイズ＋微フリッカーのオーバーレイ。

## Do's and Don'ts

**Do:**

- 視界全体を1つのセンサーモード（デュオトーン）に統一する
- バイザーの物理形状で視界をマスクする
- 中心を空け、計器を縁に寄せる
- 走査線・グレイン・微フリッカーで「レンズ越し」を維持する
- 描画をすべて同一発光色にする — 同一システムの出力であること

**Don't:**

- モードを混色しない（赤外の視界に緑の文字、は存在しない）
- 視界の中心をUIで塞がない（レティクル以外）
- パネル・カード・塗り面を持ち込まない（ここにスクリーンはない）
- クリーンでノイズレスな描画にしない — 劣化の除去はこの様式の否定
- マスクなしの全面ブリードを標準にしない（例外は爆撃照準のみ）

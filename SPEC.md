# 256-hoshikake-ds ｜ ホシカケ DS

## 0. ドキュメント情報

- 仕様書名: ホシカケ DS
- 対象ゲーム: `256-hoshikake-ds`
- 作成日: 2026-09-23
- 更新日: 2026-09-23
- ステータス: 実装済み
- 参照ファイル: `index.html` `three.min.js` `hoshikake-ds.html`（旧入口。転送）

## 1. ゲーム概要

- ジャンル: 3Dアクション（二画面）
- 一言説明: 空の島で星を5つ集め、敵は踏みつけかスピンで倒す
- 想定プレイ時間: 1プレイ数分
- 想定プレイヤー: iPhone Safari 縦持ち（DS型の上下画面）
- クリア体験の要点: 上画面の島を動き、下画面と本体ボタンで操作して星を集める

## 2. 対象環境

### 必須
- 配信先: GitHub Pages
- 最優先端末: iPhone Safari
- 対応画面幅: 320px 以上（筐体は最大 480px）
- 実装方式: `index.html` + 同梱 `three.min.js`。上画面は WebGL、下画面は 2D Canvas

### 任意
- キーボード: WASD / 矢印、Space、J、Q / E、Enter
- フォントは Google Fonts の DotGothic16

### 未確定
- なし

## 3. ファイル構成

- `index.html` `three.min.js` `hoshikake-ds.html`（転送）

## 4. コアループ

- タイトル（Aで開始）→ 移動・ジャンプ・スピン → 星5つでクリア
- START でポーズ。START または A で再開
- ベストタイムは `hoshikake-best`。キー名は変えない

## 5. 画面構成と状態遷移

- `title -> play -> pause -> play`
- `play -> clear`

## 6. 操作仕様

### 必須
- 画面上の十字キー、A、B、L、R、START。Pointer Events と `setPointerCapture`
- 効果音は WebAudio
- viewport は `maximum-scale=1.0, user-scalable=no, viewport-fit=cover`

### 任意
- 常時ミュートボタンはこの版では未設置

### 未確定
- なし

## 7. ルールと勝敗条件

- 星を5つ集めるとクリア。タイムが短いほど良い

## 8. UI

- 折りたたみ機の見た目。上画面にプレイ、下に十字と A / B

## 9. 音声

- オシレーターの効果音

## 10. 保存

- `hoshikake-best`

## 11. 実装制約

- three.js は同梱ファイルを読む

## 12. テスト項目

- Aでプレイが始まる
- STARTで止まり、もう一度で戻る
- 上画面の Canvas が描画される

## 13. 未確定事項

- なし

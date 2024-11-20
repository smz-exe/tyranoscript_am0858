# AM8:58

## アップデート内容

### バージョン 1.1 (2024年11月21日 更新)

1. **ランキングシステムの追加**
   - ゲーム終了後、プレイヤー名を入力してスコアをランキングに登録可能。
   - ランキングページで上位プレイヤーのスコアを確認可能。

2. **バグ修正**
   - 問題数が30問出題されなかった問題を修正。
   - 入力エラー時のメッセージ表示の挙動を最適化。

---

## 概要

AM8:58は、**タイピングゲーム**形式で実験レポートを完成させるティラノスクリプトを用いたブラウザゲームです。このゲームでは、指定された単語をタイピングし、制限時間内にタスクを完了することでスコア、並びにレポートの評価を競います。

- [テストプレイ](https://smz-exe.github.io/tyranoscript_am0858/)

---

## ゲームの特徴

1. **タイピング練習**
   - 実験に関連する単語をタイピングすることで、レポートを書く速度の向上を図ります。

2. **スコアシステム**
   - 残り時間に応じたスコアと評価（S, A, B, C）を表示。
   - リアルタイムで入力をチェック
   - 複数のローマ字入力に対応

3. **ランキング機能(新機能)**
   - ゲーム終了後、プレイヤー名とスコアを入力してランキングに登録可能。
   - ランキングページで上位プレイヤーのスコアを確認できます。

4. **カスタマイズ可能**
   - 単語リストを自由に拡張可能。

---

## ゲームルール

1. **目的**
   - 制限時間内に30問のタイピング問題をクリアしてください。

2. **評価システム**
   - 残り時間に応じてレポートの評価が決定します。
      - S評価:51秒以上
      - A評価:31秒以上
      - B評価:11秒以上
      - C評価:11秒未満

3. **スコア計算**
   - 残り時間に200を掛けた値がスコアとして表示されます。

4. **単語の構成**
   - 固定された単語とランダムな単語が混在します。
   - タイピング内容が正しければ次の問題に進みます。

---

## ランキング機能

1. **ランキング登録**
   - ゲーム終了後、プレイヤー名を入力し、スコアを登録できます。

2. **ランキング表示**
   - ランキングページで上位プレイヤーのスコアを確認可能。
   - プレイヤー名、スコア、残り時間、評価が表示されます。

3. **データ管理**
   - ランキングデータはサーバーで管理され、リアルタイムで反映されます。

---

## 技術仕様

1. **フロントエンド**
   - ティラノスクリプトを使用してタイピングゲームのロジックとUIを構築。

2. **バックエンド**
   - Glitchを利用した`Fastify`ベースのサーバー。
   - SQLiteを使用したランキングデータの管理。

3. **ランキングエンドポイント**
   - **登録**: スコアとプレイヤー名をPOSTリクエストで送信。
   - **表示**: GETリクエストでランキングデータを取得。

---

## ライセンス

ここで作成されたスクリプト(`first.ks`)に関しては CC0。ティラノスクリプトについては[配布元](https://tyrano.jp/)のライセンスに従います。`docs/data/video/`以下にあるファイルは、「みりんの動画素材」からダウンロードしたものです。

- `concentration-line03-bk.mp4` by 動画素材：[みりんの動画素材](https://miirriin.com/)

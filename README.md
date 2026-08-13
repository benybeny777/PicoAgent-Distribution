# PicoAgent Distribution

PicoAgentは、キャラクターと会話しながらPC作業も手伝ってもらえるデスクトップペットです。付属の2Dキャラに加え、利用権を持つPNG／Live2Dモデルを追加できます。既定のローカルAIでは会話をPC内で処理します。

> [!WARNING]
> 現在公開しているものは**開発中のベータ版**です。不具合、仕様変更、設定の互換性変更が入る可能性があります。大切なデータはバックアップし、試用目的でお使いください。Windows版は未署名のためSmartScreen警告が表示される場合があります。

> [!NOTE]
> **ベータ期間中はPicoAgentの全機能を試用できます。** 正式リリース時はFree／Proの機能区分を有効にします。外部APIの利用料や、選択した追加コンポーネントの導入条件は別途適用されます。

## 動画プレビュー

| 2Dキャラクター | Live2D表示例 |
|---|---|
| ![PicoAgentの2Dキャラクター画面](assets/main-light.webp) | ![PicoAgentのLive2D画面](assets/live2d-motion.webp) |

Live2Dの「ひより」は動作例です。ほかのモデルは下の一覧でも比較できます。モデル素材はインストーラへ同梱していません。

### Live2D動作例

| ひより（通常／配信） | はる（通常／配信） | イプシロン（通常／配信） | まお（通常／配信） |
|---|---|---|---|
| ![ひより通常](assets/character-hiyori.webp)<br>![ひより配信](assets/character-hiyori-stream.webp) | ![はる通常](assets/character-haru.webp)<br>![はる配信](assets/character-haru-stream.webp) | ![イプシロン通常](assets/character-epsilon.webp)<br>![イプシロン配信](assets/character-epsilon-stream.webp) | ![まお通常](assets/character-mao.webp)<br>![まお配信](assets/character-mao-stream.webp) |

| レン（通常／配信） | ライス（通常／配信） | わんこ（通常／配信） |
|---|---|---|
| ![レン通常](assets/character-ren.webp)<br>![レン配信](assets/character-ren-stream.webp) | ![ライス通常](assets/character-rice.webp)<br>![ライス配信](assets/character-rice-stream.webp) | ![わんこ通常](assets/character-wanko.webp)<br>![わんこ配信](assets/character-wanko-stream.webp) |

各プレビューは標準のペット表示を480px・134フレーム／16fpsで撮影し、待機、まばたき、口パク、モデルモーションを含みます。ライスは元モデルに口パラメータがないため口パク非対応です。本作品のキャラクターには株式会社Live2Dの著作物が用いられています。利用前に[サンプルデータ利用条件](https://www.live2d.com/learn/sample/model-terms/)を確認してください。

## 付属キャラクター

| キャラクター | 通常表示 | 配信表示 |
|---|---|---|
| **むぎ** — 明るく寄り添う作業相棒 | ![むぎ通常](assets/character-mugi.webp) | ![むぎ配信](assets/character-mugi-stream.webp) |
| **りん** — 面倒見がいいツンデレ作業相棒 | ![りん通常](assets/character-rin.webp) | ![りん配信](assets/character-rin-stream.webp) |
| **まい** — 包容力のあるやさしいお姉さん | ![まい通常](assets/character-mai.webp) | ![まい配信](assets/character-mai-stream.webp) |
| **こはる** — 親しみやすい作業相棒 | ![こはる通常](assets/character-koharu.webp) | ![こはる配信](assets/character-koharu-stream.webp) |
| **セナ** — 凛とした歌姫系作業相棒 | ![セナ通常](assets/character-sena.webp) | ![セナ配信](assets/character-sena-stream.webp) |
| **ノア** — 上品な吸血姫風メイド | ![ノア通常](assets/character-noa.webp) | ![ノア配信](assets/character-noa-stream.webp) |
| **実写（試作）** — 実写調で制作した成人キャラクター | ![実写通常](assets/character-photoreal-prototype.webp) | ![実写配信](assets/character-photoreal-prototype-stream.webp) |

全7体が、まばたき、口パク、視線、喜び／悲しみ、待機モーションに対応します。さらに、利用権を持つ1枚絵から17キーポーズ・42フレームの2Dキャラを作る試験機能もあります。制作コンポーネントは必要時に別途導入し、入力絵や環境により仕上がりは変わります。

## 機能一覧

- テキスト／音声会話、読み上げ、口パク、まばたき、視線、表情
- 8つの表示形式、ドラッグ移動、キャラごとの位置・大きさ・背景保存
- 付属2Dキャラ、自作PNG、利用権を持つCubism 4／5 Live2Dモデルの追加
- 既定のローカルAIと、任意のクラウドAI／外部サービス連携
- 許可範囲を指定したファイル操作、予定、要約などの追加機能
- 設定、会話履歴、追加キャラ、取得済みモデルを維持する更新経路

## 動作スペック

| 項目 | ベータ版の目安 |
|---|---|
| OS | Windows 10／11 x64 |
| 必須ランタイム | Microsoft WebView2（通常はWindowsに導入済み） |
| 現在のインストーラ | 約393MiB。高精細な付属7キャラを含む |
| ローカルAI最小構成 | RAM 8GB、CPU動作可、モデル約3.1GB |
| 通常推奨 | RAM 16GB、VRAM 4GB、モデル約5.0GB |
| GPU | 必須ではありません。対応GPUではVulkan推論を利用できます |
| 通信 | 初回モデル・選択した追加機能・更新の取得時に必要 |

ローカルAIのモデルにより必要容量と速度は変わります。アプリはPCのVRAM／RAMを目安に候補を選びます。

## インストール

1. [Releases](https://github.com/benybeny777/PicoAgent-Distribution/releases)から最新の`PicoAgent_*_x64-setup.exe`をダウンロードします。
2. インストーラを実行します。SmartScreenが表示された場合は、発行元と取得元がこのリポジトリであることを確認してから進めます。
3. PicoAgentを起動し、初回画面で用途と必要な追加機能を選びます。
4. ローカルAIを使う場合は、初回だけモデル取得のためインターネット接続と数GBの空き容量が必要です。

現時点のベータ配布はWindows 10／11（64bit）のみです。macOS版はmacOS上でのビルドと実機確認が完了してから追加します。

## 簡単な使い方

- キャラクターまたはフキダシをクリックして会話を開き、文字を入力します。
- キャラクターをドラッグするとウィンドウを移動できます。
- 右クリックの「設定…」でキャラ、表示形式、位置・大きさ、音声、AIモデルを変更できます。
- ファイル操作や外部連携は、設定で許可した範囲だけを使います。
- 問題が起きた場合は[Issues](https://github.com/benybeny777/PicoAgent-Distribution/issues)へ、PicoAgentのバージョンと再現手順を添えて報告してください。APIキー、会話全文、個人ファイルは掲載しないでください。

最新版情報は`latest.json`、詳細な案内は[配布ページ](https://benybeny777.github.io/PicoAgent-Distribution/)を参照してください。

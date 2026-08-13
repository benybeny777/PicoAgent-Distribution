# PicoAgent Distribution

PicoAgentは、キャラクターと会話しながらPC作業も手伝ってもらえるデスクトップペットです。付属の2Dキャラに加え、利用権を持つPNG／Live2Dモデルを追加できます。既定のローカルAIでは会話をPC内で処理します。

> [!WARNING]
> 現在公開しているものは**開発中のベータ版**です。不具合、仕様変更、設定の互換性変更が入る可能性があります。大切なデータはバックアップし、試用目的でお使いください。Windows版は未署名のためSmartScreen警告が表示される場合があります。

## 動画プレビュー

| 2Dキャラクター | Live2D表示例 |
|---|---|
| ![PicoAgentの2Dキャラクター画面](assets/main-light.webp) | ![PicoAgentのLive2D画面](assets/live2d-motion.webp) |

Live2Dの「ひより」は動作例です。モデル素材はインストーラへ同梱していません。

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

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

各プレビューは通常表示と配信表示を960px・360フレーム／30fps（12秒）で撮影しています。通常版は実画面を2倍密度で描画し、配信版はネイティブ1920×1080のフルHD画面から縮小しており、旧480px動画の引き伸ばしではありません。音声同期の口パク→考え中→成功→悲しみ→左右視線→待機を間隔を空けて見せます。ライスは元モデルに口パラメータがないため口パク非対応です。本作品のキャラクターには株式会社Live2Dの著作物が用いられています。利用前に[サンプルデータ利用条件](https://www.live2d.com/learn/sample/model-terms/)を確認してください。

## 付属キャラクター

| キャラクター | 通常表示 | 配信表示 |
|---|---|---|
| **むぎ** — 明るく寄り添う作業相棒 | ![むぎ通常](assets/character-mugi.webp) | ![むぎ配信](assets/character-mugi-stream.webp) |
| **りん** — 面倒見がいいツンデレ作業相棒 | ![りん通常](assets/character-rin.webp) | ![りん配信](assets/character-rin-stream.webp) |
| **まい** — 包容力のあるやさしいお姉さん | ![まい通常](assets/character-mai.webp) | ![まい配信](assets/character-mai-stream.webp) |
| **こはる** — 親しみやすい作業相棒 | ![こはる通常](assets/character-koharu.webp) | ![こはる配信](assets/character-koharu-stream.webp) |
| **セナ** — 凛とした歌姫系作業相棒 | ![セナ通常](assets/character-sena.webp) | ![セナ配信](assets/character-sena-stream.webp) |
| **ノア** — 上品な吸血姫風メイド | ![ノア通常](assets/character-noa.webp) | ![ノア配信](assets/character-noa-stream.webp) |
| **実写2Dテスト** — 150フレームと目・口7段階を持つ成人キャラクター | ![実写通常](assets/character-photoreal-prototype.webp) | ![実写配信](assets/character-photoreal-prototype-stream.webp) |

全7体が、目7段階のまばたき、口7段階の口パク、視線、喜び／悲しみ、待機モーションに対応します。通常2Dは150フレームへ統一し、髪や服の動きも物理演算ではなく事前描画した連番で表現します。

低頭身2Dは上半身、長身・実写・Live2Dは胸全体がぎりぎり入る胸上、チャット／バーの小型アイコンは首上を初期構図にします。利用者が保存したキャラ別構図は初期値より優先します。

## 機能一覧

- テキスト／音声会話、読み上げ、口パク、まばたき、視線、表情、ふれあい、長期記憶
- 7つの表示形式（ペット／マスコット／LINE風チャット／バー／作業／配信／ウィジェット）、OBS風の直接配置、キャラやフキダシの位置・大きさ・背景保存
- 付属2Dキャラ、自作PNG、利用権を持つCubism 4／5 Live2Dモデルの追加
- 既定のローカルAIと、任意のクラウドAI／外部サービス連携
- 許可範囲を指定したファイル操作、予定、要約などの実務スキル70種
- 設定、会話履歴、追加キャラ、取得済みモデルを維持する更新経路

### できること（スキル70種）

| 分類 | 例 |
|---|---|
| 毎日の習慣 | 時刻、天気、目覚まし、リマインダー、集中タイマー、ToDo、今日のまとめ、ニュース、RSS、為替、株価 |
| ファイルと文書 | 読み書き、ファイル名／全文検索、作業フォルダ整理、PDF編集、Office文書、形式変換、画像確認・加工 |
| PC操作 | アプリ起動、ウィンドウ操作、クリップボード、コマンド実行、長時間ジョブ、予約実行（cron風）、コード実行 |
| Webと調べもの | Web検索、ページ取得、ブラウザ操作、調査レポート作成 |
| 連絡とタスク管理 | Gmail、Slack、Discord、GitHub、Notion、Jira、Linear、Trello、Todoist、Googleカレンダー／ドライブ／ドキュメント／スプレッドシート／ToDo、Microsoft Graph |
| SNS | X、Bluesky、Mastodon、Misskey、Reddit、LinkedIn |
| 音声と記録 | 会議の録音、ローカル文字起こし、議事録づくり |
| つくる | 画像生成、ComfyUI連携、制作ワークスペース |

スキルは会話の内容から自動で選ばれます。ファイル操作は許可した範囲だけを対象にし、削除に相当する操作は必ずOSのゴミ箱へ移します。外部サービスは、鍵やトークンを設定した分だけ有効になります。

### AIモデル

| 接続先 | 内容 |
|---|---|
| 同梱ローカルAI（既定） | 推論エンジンを同梱。初回だけモデルを取得し、以後はオフラインでも会話できます |
| Ollama | 既に導入済みのOllamaへ接続できます |
| クラウドAI（任意） | OpenAI、Anthropic（Claude）、Google Gemini、DeepSeek、xAI、Mistral、OpenAI互換API。各社の利用料が発生します |

APIキー等はWindowsのDPAPIで暗号化して保存し、同じWindowsユーザーだけが復号できます。

### 開発者向け（既定は無効）

- ローカルHTTP API: 127.0.0.1のみ・トークン認証つき。Ollama風の`/api/chat`とOpenAI互換の`/v1/chat/completions`に対応します。
- MCPサーバー: `/mcp`でPicoAgentのスキルをMCPツールとして公開できます。
- MCPクライアント: 外部のMCPサーバーを登録すると、そのツールがスキル一覧へ加わります。

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

## よくある質問

- **オフラインでも使えますか**: 初回にモデルを取得したあとは、ローカルAIとの会話をオフラインで続けられます。通信が必要なスキルだけが使えません。
- **データはどこに保存されますか**: 設定、会話履歴、長期記憶、関係性、実行履歴、追加キャラ、取得したモデルはすべてPC内に保存されます。
- **勝手にファイルを消しませんか**: 消しません。許可したフォルダの中だけを扱い、削除相当は必ずゴミ箱へ移します。物理削除コマンドはコマンド実行や予約実行の経路でも拒否します。
- **Live2Dモデルは付属しますか**: 付属しません。動作例は条件を確認したうえで表示している公式サンプルです。利用権を持つモデルを読み込んでお使いください。
- **アンインストールは**: Windowsの「アプリと機能」から削除できます。設定や会話履歴を残すか消すかを選べます。

最新版情報は`latest.json`、詳細な案内は[配布ページ](https://benybeny777.github.io/PicoAgent-Distribution/)を参照してください。

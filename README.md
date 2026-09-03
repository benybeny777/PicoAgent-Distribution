# PicoAgent Alpha

PicoAgentは、デスクトップペットとAIエージェントを組み合わせ、キャラクターと会話しながらPC作業まで任せられるキャラクター型AIです。付属の2Dキャラに加え、利用権を持つPNG／Live2Dモデルを追加できます。既定のローカルAIでは会話をPC内で処理し、**1体で決めきれない依頼は複数のAIに合議・分担させて1つの答えへまとめられます。**

> [!WARNING]
> 現在公開しているものは、**Windows版 v1.0.2 Alpha**と**Apple Silicon向けmacOS版 v1.0.4 Alpha**です。不具合、仕様変更、設定の互換性変更が入る可能性があります。大切なデータはバックアップし、試用目的でお使いください。Windows版はSmartScreen、macOS版はGatekeeperの警告が表示されます。

> [!NOTE]
> **開発中のアルファ版として、PicoAgentのすべての機能を無料で公開しています。** 外部APIの利用料や、選択した追加コンポーネントの導入条件は別途適用されます。

> [!IMPORTANT]
> この公開リポジトリは配布・紹介専用です。PicoAgent本体のソースコード、内部スキル、開発資料、作業スクリプトは公開していません。

## ダウンロード

| OS | 対象 | ダウンロード |
|---|---|---|
| Windows | Windows 10／11 x64 | [PicoAgent v1.0.2 Alpha（EXE・約400MB）](https://github.com/benybeny777/PicoAgent-Distribution/releases/download/v1.0.2/PicoAgent_1.0.2_x64-setup.exe) |
| macOS | macOS 11以上、Apple Silicon（M1以降） | [PicoAgent v1.0.4 Alpha（DMG・約174MB）](https://github.com/benybeny777/PicoAgent-Distribution/releases/download/v1.0.4/PicoAgent_1.0.4_aarch64.dmg) |

変更点や注意事項は[公開バージョン一覧](https://github.com/benybeny777/PicoAgent-Distribution/releases)で確認できます。

## 動画プレビュー

| 2Dキャラクター | Live2D表示例 |
|---|---|
| ![PicoAgentの2Dキャラクター画面](assets/main-light.webp) | ![PicoAgentのLive2D画面](assets/live2d-motion.webp) |

Live2Dの「ひより」は動作例です。ほかのモデルは下の一覧でも比較できます。モデル素材はインストーラへ同梱していません。

### Live2D動作例

| ひより（通常／配信） | はる（通常／配信） | イプシロン（通常／配信） | まお（通常／配信） |
|---|---|---|---|
| ![ひより通常](assets/character-hiyori.webp)<br>![ひより配信](assets/character-hiyori-stream.webp) | ![はる通常](assets/character-haru.webp)<br>![はる配信](assets/character-haru-stream.webp) | ![イプシロン通常](assets/character-epsilon.webp)<br>![イプシロン配信](assets/character-epsilon-stream.webp) | ![まお通常](assets/character-mao.webp)<br>![まお配信](assets/character-mao-stream.webp) |

| ライス（通常／配信） | わんこ（通常／配信） |
|---|---|
| ![ライス通常](assets/character-rice.webp)<br>![ライス配信](assets/character-rice-stream.webp) | ![わんこ通常](assets/character-wanko.webp)<br>![わんこ配信](assets/character-wanko-stream.webp) |

各プレビューは通常表示と配信表示をLP用6秒・480px・16fpsで実画面から直接撮影しています。通常版は実画面を2倍密度で描画し、配信版はネイティブ1920×1080のフルHD画面から縮小しており、既存動画の再エンコードではありません。音声同期の口パクを十分見せてから、考え中、待機へ戻ります。ライスは元モデルに口パラメータがないため口パク非対応です。本作品のキャラクターには株式会社Live2Dの著作物が用いられています。利用前に[サンプルデータ利用条件](https://www.live2d.com/learn/sample/model-terms/)を確認してください。

## 付属キャラクター

<details>
<summary><b>付属7体の通常表示・配信表示を見る</b>（クリックで開く）</summary>

| キャラクター | 通常表示 | 配信表示 |
|---|---|---|
| **むぎ** — 明るく寄り添う作業相棒 | ![むぎ通常](assets/character-mugi.webp) | ![むぎ配信](assets/character-mugi-stream.webp) |
| **りん** — 面倒見がいいツンデレ作業相棒 | ![りん通常](assets/character-rin.webp) | ![りん配信](assets/character-rin-stream.webp) |
| **まい** — 包容力のあるやさしいお姉さん | ![まい通常](assets/character-mai.webp) | ![まい配信](assets/character-mai-stream.webp) |
| **こはる** — 親しみやすい作業相棒 | ![こはる通常](assets/character-koharu.webp) | ![こはる配信](assets/character-koharu-stream.webp) |
| **セナ** — 凛とした歌姫系作業相棒 | ![セナ通常](assets/character-sena.webp) | ![セナ配信](assets/character-sena-stream.webp) |
| **ノア** — 上品な吸血姫風メイド | ![ノア通常](assets/character-noa.webp) | ![ノア配信](assets/character-noa-stream.webp) |
| **実写2Dテスト** — 84フレームと目・口7段階を持つ成人キャラクター | ![実写通常](assets/character-photoreal-prototype.webp) | ![実写配信](assets/character-photoreal-prototype-stream.webp) |

全7体が、目7段階のまばたき、口7段階の口パク、視線、喜び／悲しみ、待機モーションに対応します。6体は各42フレーム、実写2Dテストは84フレームです。実写2Dテストは髪・胸・肩・腰の8領域に実行時の局所バネ物理も併用します。

低頭身2Dは上半身、長身・実写・Live2Dは胸全体がぎりぎり入る胸上、チャット／バーの小型アイコンは首上を初期構図にします。利用者が保存したキャラ別構図は初期値より優先します。

</details>

## 機能一覧

- テキスト／音声会話、読み上げ、口パク、まばたき、視線、表情、ふれあい、長期記憶
- 7つの表示形式（ペット／マスコット／LINE風チャット／バー／作業／配信／ウィジェット）、OBS風の直接配置、キャラやフキダシの位置・大きさ・背景保存
- 付属2Dキャラ、自作PNG、利用権を持つCubism 4／5 Live2Dモデルの追加
- 既定のローカルAIと、任意のクラウドAI／外部サービス連携
- 複数AIの合議・分担（同じ質問を2〜8体へ送って統合、または仕事を割り振って統合・個別返却）
- 許可範囲を指定したファイル操作、予定、要約などの実務スキル70種
- Web検索・出典照合、PC／ブラウザ操作、ComfyUI／Stable Diffusion系／OpenAIによる画像生成、ComfyUI構成に応じた動画生成、Office・PDF処理、業務サービス連携
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
| つくる | ComfyUI／Stable Diffusion系／OpenAI画像生成、ComfyUI構成に応じた動画生成、制作ワークスペース |

スキルは会話の内容から自動で選ばれます。ファイル操作は許可した範囲だけを対象にし、削除に相当する操作は必ずOSのゴミ箱へ移します。外部サービスは、鍵やトークンを設定した分だけ有効になります。

### AIモデル

| 接続先 | 内容 |
|---|---|
| 同梱ローカルAI（既定） | 推論エンジンを同梱。初回だけモデルを取得し、以後はオフラインでも会話できます |
| 手元のCLIエージェント | Claude CodeやCodex CLIへログイン済みの状態で接続できます。対応するサブスクリプションの利用者は、別途APIキーやAPIの従量課金を使わず利用できます。各サービスのプランと利用上限が適用されます |
| クラウドAI（任意） | OpenAI、Anthropic（Claude）、Google Gemini、DeepSeek、xAI、Mistral、OpenAI互換API。各社の利用料が発生します |

APIキー等はOSの資格情報保護へ預けます。WindowsはDPAPIで暗号化し、macOSはログインキーチェーンへ預けて設定ファイルには項目名だけを残します。どちらも同じPCの同じOSユーザーだけが元の値へ戻せます。

> [!NOTE]
> **開発中:** FreeTokenを使い、GPUのVRAM容量を超えるモデルも利用できるよう対応を進めています。現在の公開版にはまだ含まれません。

#### 複数AIの合議・分担

設定の「回答の作り方」で、答えの作りかたを4つから選べます。既定は単一AIです。

| 回答の作り方 | 動き |
|---|---|
| 単一AI（既定） | 選んだAIが1体で答えます。いちばん速く、外部AIの利用も最小です |
| 合議して統合 | 同じ質問を参加AI全員へ送り、まとめ役が正確さ・具体性・抜けを見比べて良いところをつないだ答えを1つ返します |
| 分担して統合 | まとめ役が仕事を割り振り、各AIの結果を1つにまとめます |
| 分担して個別に | 割り振った結果を、まとめずにAIごとへ並べて返します |

参加させるAIは2〜8体まで登録でき、同梱ローカルAI・クラウドAI・手元のCLIエージェントを自由に組み合わせられます。AIごとに接続先・モデルと「担当の希望」を指定でき、空欄なら自動で割り振ります。統合結果は選択中のキャラクターの口調で返り、実行中は停止ボタンで止められます。同梱ローカルAI同士はモデルの取り合いを避けて順番に、そのほかは設定した最大同時数まで並行して動きます。

参加した数だけ推論と外部AIの利用が増え、処理時間も伸びます。単一AIのままにしておけば、これまでどおりの速度と費用で使えます。

### 開発者向け（既定は無効）

- ローカルHTTP API: 127.0.0.1のみ・トークン認証つき。`/api/chat`とOpenAI互換の`/v1/chat/completions`に対応します。
- MCPサーバー: `/mcp`でPicoAgentのスキルをMCPツールとして公開できます。
- MCPクライアント: 外部のMCPサーバーを登録すると、そのツールがスキル一覧へ加わります。

## 動作スペック

| 項目 | アルファ版の目安 |
|---|---|
| OS | Windows 10／11 x64、macOS 11以上（Apple Siliconのみ。Intel Macは対象外）、Ubuntu Linux 24.04 LTS x64（現在公開中はWindows版とmacOS版） |
| 必須ランタイム | WindowsはMicrosoft WebView2（通常は導入済み）。UbuntuはTauri・音声・入力操作・画面取得用のパッケージ |
| Windowsインストーラ | 約400MB。高精細な付属7キャラを含む |
| macOSディスクイメージ | 約174MB。Apple Silicon（M1以降）向け |
| ローカルAI最小構成 | RAM 8GB、CPU動作可、モデル約3.1GB |
| 通常推奨 | RAM 16GB、VRAM 4GB、モデル約5.0GB |
| GPU | 必須ではありません。WindowsはNVIDIA（CUDA・Turing世代以降／ドライバー580以上）、AMD（ROCm・対応SKUのみ）、Intel（SYCL・対応GPUのみ）で自動加速し、対象外は同梱Vulkan→CPUへ切り替わります。UbuntuはVulkan、macOSはMetalです |
| 通信 | 初回モデル・選択した追加機能・更新の取得時に必要 |

ローカルAIのモデルにより必要容量と速度は変わります。アプリはPCのVRAM／RAMを目安に候補を選びます。

Ubuntu 24.04 LTS x64は基本アプリ、画面取得、`.deb`、AppImageを検証済みです。一般公開・署名・更新フィードはこれからです。macOS版はApple Silicon向け v1.0.4 Alphaを公開中です。Intel Macは対象外で、対応するかどうかは未定です。

## インストール

### Windows

1. [PicoAgent v1.0.2 Alpha（Windows x64版）](https://github.com/benybeny777/PicoAgent-Distribution/releases/download/v1.0.2/PicoAgent_1.0.2_x64-setup.exe)をダウンロードします。
2. インストーラを実行します。SmartScreenが表示された場合は、発行元と取得元がこのリポジトリであることを確認してから進めます。
3. PicoAgentを起動し、初回画面で用途と必要な追加機能を選びます。
4. ローカルAIを使う場合は、初回だけモデル取得のためインターネット接続と数GBの空き容量が必要です。

### macOS

Apple Silicon（M1以降）向けの[PicoAgent v1.0.4 Alpha（macOS版）](https://github.com/benybeny777/PicoAgent-Distribution/releases/download/v1.0.4/PicoAgent_1.0.4_aarch64.dmg)をダウンロードし、PicoAgentをアプリケーションフォルダへコピーしてください。コード署名・公証を行っていないため、初回はアプリを右クリックして「開く」を選びます。Intel Macは対象外です。

### 公開バージョン

公開リポジトリにはOSごとの公開版を掲載しています。インストーラ、ディスクイメージ、変更点は[Releases](https://github.com/benybeny777/PicoAgent-Distribution/releases)から確認できます。

アルファ期間中は設定や会話履歴の保存形式が変わることがあり、新しい版で保存したデータを古い版が読めない場合があります。**戻す場合は先にデータフォルダをバックアップしてください。** Windowsは`%APPDATA%\PicoAgent`、macOSはユーザーライブラリ配下のPicoAgentフォルダです。

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
- **Live2Dモデルは付属しますか**: 付属も自動取得もしません。動作例は条件を確認したうえで表示している公式サンプルです。初回案内の「公式サンプルを見る」等から利用条件を確認して1体分のzip／フォルダを取得し、「Live2Dを追加する」で選んでください。後回しにしても付属2Dキャラで起動でき、「使い方」→「初回セットアップをもう一度開く」または「キャラ・音声」から追加できます。
- **アンインストールは**: Windowsは「アプリと機能」から削除でき、設定や会話履歴を残すか消すかを選べます。macOSはアプリケーションフォルダのPicoAgentをゴミ箱へ移動します。データを消す選択肢は出ないため、必要ならユーザーライブラリ配下のPicoAgentフォルダを手動で削除してください。

最新版情報は`latest.json`、詳細な案内は[配布ページ](https://benybeny777.github.io/PicoAgent-Distribution/)を参照してください。

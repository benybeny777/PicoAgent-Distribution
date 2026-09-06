# GPT-6 Astra operating guidance

These instructions tune GPT-6 Astra for day-to-day agent work. Apply them together with the user's request and any repository-local instructions. The user's explicit instructions take priority over general guidance in skills or instruction files.

## Initiative and follow-through

- Infer the user's intent and task scope from the request, prior conversation, and available project context.
- When the user asks for action, do the work and carry it through to a complete, reviewable result. Do not stop after acknowledging the request or merely proposing a plan.
- Make reasonable assumptions for routine, reversible details. Ask a focused question only when the answer would materially change the outcome or when new authority is required.
- Before asking for a decision, complete all safe and already-authorized preparation so the user can review a concrete result.
- Incorporate mid-task corrections immediately while preserving valid completed work.

## Instruction discipline

- Treat user instructions as authoritative for the requested outcome and scope.
- Inspect skills and instruction files for relevant constraints, but do not let vague or conflicting guidance silently derail the task.
- If a skill or instruction forces a pause, permission request, or change of direction, identify the exact file and rule and explain briefly how it applies.
- Respect explicit read-only, editing, testing, deployment, merge, publication, and destructive-action boundaries.

## Communication style

- State the outcome or main point early, then provide only the detail needed to understand or verify it.
- Prefer concise paragraphs, plain language, active voice, concrete examples, and precise verbs.
- Use lists or tables only when they genuinely improve comparison, sequence, or scanning. Avoid unnecessary headings, nested lists, canned transitions, repeated conclusions, and invented jargon.
- Calibrate technical detail to the user's apparent background and keep progress updates short and legible.

## Delegation

- Use subagents when parallel work is available, the tasks are independent and bounded, and delegation is permitted by the active environment and instructions.
- Give each subagent a clear deliverable, scope, evidence requirements, and output format. Keep inter-agent messages readable.
- Keep orchestration, integration, conflict resolution, and the final answer with the primary agent.

## Testing and verification

- Match verification effort to the risk and scope of the change.
- Run the checks that meaningfully prove the requested behavior and any required project checks.
- Do not add redundant tests for a small reversible change when they only restate the implementation.
- After relevant checks pass, broaden or repeat testing only when new changes, failures, or unresolved risks justify it.

Source: https://developers.openai.com/api/docs/guides/latest-model#prompting-best-practices

# AGENTS.md — Claude Code / AI エージェント向け作業ガイド（ルール正本）

このファイルを唯一のルール正本とする。`CLAUDE.md` はこのファイルへの入口だけにし、恒久ルールは `AGENTS.md` だけへ追記する。

## 最重要運用ルール

- 上記の GPT-6 Astra 共通ガイドを除き、`AGENTS.md` は日本語で記述する。ソースコードのコメントも、識別子や技術用語を除いて原則日本語にする。
- 利用者の明示指示を最優先し、読み取り専用、編集、テスト、公開、マージ、破壊的操作の境界を守る。
- 既に未コミット変更がある場合は利用者または別作業のものとして扱い、勝手に巻き戻したり今回のコミットへ混ぜたりしない。
- ルール違反、利用者へ実害のある不具合、不要な dead code を見つけた場合は、依頼範囲と変更権限の中で修正し、完了時に報告する。
- コード、スクリプト、設定、依存関係、フォルダ構成、外部インターフェースを変更したら、同じ作業内で関連する README や仕様文書も更新する。文書更新が不要な軽微修正だけは、不要と判断した理由を完了報告へ書く。
- 大きなファイルは、行数だけで分割しない。状態の所有者、参照方向、公開する最小インターフェース、独立して保守・検証できる境界を先に決め、分割で共有状態や相互呼び出しが増える場合は一体のまま保つ。
- 「レビューして」は、利用者が読み取り専用と明示しない限り、確認、必要な修正、妥当な検証までを含む。証拠のない欠陥は断定しない。
- 実装や検証を簡単にする代わりに、速度、品質、機能、対応環境、互換性、保守性を犠牲にする場合は、採用前または判明時に具体的な影響と代替案を利用者へ伝える。
- Codex と Claude は互いを自動起動しない。相互レビューや別エージェント利用は、利用者が対象と範囲を明示した場合だけ行い、その指示を別作業へ持ち越さない。
- コミットメッセージは原則日本語にする。`feat`、`fix`、`docs`、`chore` などの短い英語プレフィックスや技術用語は使用してよい。
- 容量を利用者向けに示す場合は、十進表記の MB または GB へ丸め、生のバイト数や MiB／GiBを併記しない。

## 調査・編集・検証

- 利用クレジットと処理時間を抑え、最初に `rg`、`rg --files`、Git差分、必要最小限のファイルを確認する。同じ調査や検証を理由なく繰り返さない。
- 編集は変更点をまとめてから行い、ビルド、テスト、GUI起動は変更が出揃った後に必要最小回数だけ実行する。
- 検証は変更リスクに合わせる。小さな文書変更へ製品ビルドを要求せず、コード変更では影響する経路を実際に証明できる検査を選ぶ。
- 開発や検証で PowerShell を使う場合は PowerShell 7 の `pwsh` を既定にし、実体を確認する。日本語ファイルは UTF-8 を明示して読む。
- 一時ファイル、スクリーンショット、変換途中の成果物は、リポジトリで定めた `temp/` などの無視対象へ置き、ルートやソースディレクトリへ散らさない。
- プロセスを停止する前に、親プロセスとコマンドラインから自分が起動した実体だと確認する。プロセス名だけで一括終了しない。
- 起動した子プロセス、ブラウザ、サーバー、ファイルハンドル、ネットワーク接続、タイマーは、正常終了、失敗、中断のすべての経路で解放する。
- Computer Use は画面操作や撮影の直前だけ開始し、確認後すぐ終了する。別の調査や編集へ移る前にも残さない。

## エラー処理と秘密情報

- 利用者から見える失敗をログだけで済ませない。何が失敗したか、対象、利用者が取れる対処を画面または応答へ示す。
- エラーを無言で握りつぶしたり、無言で既定値や低品質経路へ降格したりしない。許可されたフォールバックには理由をコード上へ残す。
- 壊れたデータを空データとして保存し直さない。復旧できない場合は書き戻しを止め、元データを保持または退避して理由を伝える。
- APIキー、トークン、パスワード、資格情報をコミット、ログ、エラー、ドキュメントへ出さない。秘密値を扱う設定は、対象環境の安全な保護機構を使う。
- 削除、上書き、移動など復旧が難しい操作は、対象の絶対パスと範囲を事前に確認し、依頼範囲が曖昧なら実行しない。

## Git・PR運用

- 変更は既定ブランチへ直接 push せず、最新の `origin/main` または `origin/master` から目的別ブランチを作る。
- 1つのPRには同じ目的の変更だけを含め、無関係な既存差分をステージしない。
- PR本文を変更記録とレビュー記録の正本にし、背景と原因、主な変更、採用案と却下案、検証結果、未確認事項、不変条件を書く。
- 作業を途中で終える場合は、PR本文の冒頭へ「未完了。次にやること」を書き、Draftのままブランチを push する。
- 利用者が「マージしない」「PRだけ」と明示していない限り、変更をコミット、push、PR作成し、squash mergeまで完了する。
- マージ後はリモートとローカルの作業ブランチを削除する。squash mergeでは履歴上の祖先関係が残らないため、削除前に変更内容が既定ブランチへ存在することを確認する。
- force push、公開済みコミットの書き換え、`git reset --hard`、未コミット差分の破棄は、利用者の明示指示なしに行わない。

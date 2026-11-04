# AI-Tools（日本語）

**一つのパネルで、AI ツールチェーン全体をまとめて管理。** AI-Tools は各 AI コーディングクライアントの設定ファイルに分散している MCP サーバーと Agent Skills を一つのデスクトップアプリに集約します。検索・インストール・編集・デバッグ・ロールバック・同期まで、JSON を手で触ることなく完了します。

<p align="center">
  <a href="https://www.ywhome.top">公式サイト</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/releases/latest">ダウンロード</a> ·
  <a href="https://www.ywhome.top/#product-ai-tools-pricing">ライセンスと価格</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/issues">不具合報告</a>
</p>

<p align="center">
  <a href="./README.md">English</a> ·
  <a href="./README.zh.md">简体中文</a> ·
  <a href="./README.ar.md">العربية</a> ·
  <a href="./README.de.md">Deutsch</a> ·
  <a href="./README.es.md">Español</a> ·
  <a href="./README.fr.md">Français</a> ·
  <a href="./README.it.md">Italiano</a> ·
  <strong>日本語</strong> ·
  <a href="./README.ru.md">Русский</a>
</p>

> **このリポジトリ**は AI-Tools の公式リリース配信先です（Windows / macOS / Linux のインストーラーと、アプリの自動更新が読むマニフェスト）。ソースコードは含まれません。
> **機能ガイドと対応クライアント：<https://www.ywhome.top>**

---

## 一言でいうと

**31 の MCP 設定エントリーと 19 の Skills 同期先を、一つの台帳として管理。** Cursor、VS Code、Claude Code、Gemini CLI、Codex CLI、Windsurf、Zed、TRAE（CN / SOLO / プラグイン）、Kiro、OpenCode、JetBrains 系、Antigravity、OpenClaw、CodeBuddy、WorkBuddy、Qoder、ZCode、Cline、Qwen Code、iFlow CLI、LM Studio、OpenHands、GitHub Copilot CLI、Warp、Kimi Code CLI、Kilo Code、Goose、およびクラウドストレージ。一覧は実機スキャンで確定し、未掲載のクライアントも設定パスとスキルディレクトリを指定すれば追加できます。

## 選ばれる理由

| よくある手間 | AI-Tools なら |
| --- | --- |
| 同じサーバーを 6 つの JSON、6 種類のキー名で管理 | **一度の編集で全クライアントに反映。** 選択したクライアントへ自動分配し、JSON / JSONC / TOML、`servers` と `mcpServers`、`working_directory` と `cwd`、`transport` と `type`、`context_servers`、`mcp_servers` の違いを吸収します。 |
| ストアの読み込み待ち | **初回表示は即時。** ディスクキャッシュ + SWR で画面を先に出し、更新は裏側で静かに（一覧 1 時間・詳細 24 時間）。必要なときは強制更新も一発です。 |
| 「この編集で壊れない？」 | **すべて元に戻せる。** インストール・削除・更新・同期・編集を自動バックアップし、任意のスナップショットと現状を Diff 表示、ワンクリックで復元。 |
| curl とエディタで MCP をデバッグ | **Inspector 内蔵。** stdio / streamable-http / sse の 3 転送に対応し、フォームから Tool を直接呼び出し、結果は JSON ハイライト、ログは伸縮パネルで確認できます。 |
| 買い替えのたびに再設定 | **クラウドは自分の手元に。** 自分の Git（SSH 鍵 / HTTPS トークン / 匿名）または SFTP（パスワード / 鍵）へ進捗つきタスクキューで同期し、送信前にローカルとリモートの差分を項目単位で確認します。 |
| 端末データが心配 | **ローカルファースト。** クラウド同期を設定するまで外部送信はゼロ。キャッシュは AES-256-GCM、認証情報は SecretStore の暗号参照としてのみ保存します。 |

## 主要機能

- **MCP ストア** — Smithery、npm レジストリ、Alibaba Bailian オフライン索引（251 件・通信不要）、ModelScope、公式レジストリスナップショットを切り替え可能。カテゴリ・総件数・サーバー側ページネーション対応。
- **Skills ストア** — `~/.agents/skills/` 規約に準拠。検索・カテゴリ（UI 言語に追従）・並び替え・ソース絞り込み・ページサイズ調整。インストール不可のクライアントでは理由を表示してボタンを無効化し、空のディレクトリを作りません。
- **ワンクリック配備** — 複数クライアント同時インストール、クライアント単位の削除・更新、手動編集のフラグ立てでストア更新からローカル調整を保護。
- **MCP Inspector** — コマンド・引数・環境変数・ヘッダーを自由に指定し、Tools / Resources / Prompts を列挙して実行。子プロセスは終了時に回収されます。
- **ライブラリ** — インストール済みの一括編集・一括同期・削除。Skills では SKILL.md のオンライン編集、同梱ファイル管理、`.zip` / `.skill` / フォルダー / GitHub リンク / ドラッグ&ドロップでの取り込み、複数まとめて zip 出力、クラウド衝突解決。
- **クラウド同期** — 起動時の自動取得と手動送信をタスクパネルで管理、失敗時はワンクリック再試行、整合性チェックで誤上書きを防止。
- **履歴とロールバック** — 日時・サイズ・対象クライアント・件数を表示、任意バージョンとの Diff、一発復元、全履歴の消去。
- **実行環境チェック** — Node.js・Python・Git の有無、バージョン、パスを自動検出し「入っているのに動かない」を切り分けます。
- **プラットフォームソースと API トークン** — 組み込み源と直結源を Base URL + トークンで一元管理。プラットフォーム実エンドポイントに基づく接続テスト、有効化・既定設定・エクスポート、スコープ付きトークンの発行 / 失効も可能。
- **外観と 9 言語** — ライト / ダーク / システム追従、および English・简体中文・العربية（RTL）・Deutsch・Español・Français・Italiano・日本語・Русский。言語パックは必要時に読み込み、切替は即時です。
- **セキュリティ** — AES-256-GCM キャッシュ、http/https のみの外部リンク、DNS-over-HTTPS、単一インスタンスロック、メイン / プリロード / レンダラーの完全分離と IPC 許可リスト。

## リリースの中身

| 成果物 | 対象 |
| --- | --- |
| `AI-Tools-Setup-<version>.exe` | Windows インストーラー（NSIS / x64） |
| `AI-Tools-<version>-portable.exe` | Windows ポータブル版 |
| `AI-Tools-<version>.dmg` / `-arm64.dmg` | macOS（Intel / Apple シリコン） |
| `AI-Tools-<version>-mac.zip` / `-arm64-mac.zip` | macOS アーカイブ |
| `AI-Tools-<version>.AppImage` / `-arm64.AppImage` | Linux AppImage |
| `ai-tools_<version>_amd64.deb` / `_arm64.deb` | Linux .deb |
| `latest.yml` / `portable.yml` / `latest-mac.yml` / `latest-linux.yml` / `latest-linux-arm64.yml` | 自動更新マニフェスト |
| `*.blockmap` | 差分ダウンロード用 |

添付ファイルはすべてトークン不要で匿名ダウンロードできます。アプリが読む更新フィードの例：

```
https://github.com/qingchuang12/ai-tools-releases/releases/latest/download/latest.yml
```

マニフェストには SHA-512 とファイルサイズが含まれ、更新器は検証を通ってから適用します。

## ダウンロードとインストール

最新の公開版：**1.1.1**（2026-11-02）— [Releases 最新](https://github.com/qingchuang12/ai-tools-releases/releases/latest)

- Windows — [AI-Tools-Setup-1.1.1.exe](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-Setup-1.1.1.exe) ／ [ポータブル版](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-portable.exe)
- macOS — [dmg (Intel)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.dmg) ／ [dmg (Apple シリコン)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-arm64.dmg)
- Linux — [AppImage (x64)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.AppImage) ／ [deb (amd64)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/ai-tools_1.1.1_amd64.deb)

公式サイトのダウンロードページ（[www.ywhome.top/#product-ai-tools-download](https://www.ywhome.top/#product-ai-tools-download)）は順次開放中です。ボタンが有効になるまではこのリポジトリが正規の入手先です。

現在のビルドは**未署名**です。Windows では SmartScreen の「詳細情報 → 実行」を選択、macOS で起動しない場合は `xattr -cr /Applications/AI-Tools.app`、AppImage は `chmod +x` を先に実行してください。

## アプリ内の自動更新

インストール済みアプリは本リポジトリを自前で確認し、その場で更新します。NSIS は `latest.yml`、ポータブル版は `portable.yml`、macOS は `latest-mac.yml`、Linux は `latest-linux.yml` / `latest-linux-arm64.yml` を参照します。

## プライバシーとデータ

ローカルファースト：アプリはこのマシンの設定ファイルのみを操作し、クラウド同期を設定するまで何も送信しません。データは `~/.ai-tools/`（macOS / Linux）、`%USERPROFILE%\.ai-tools\`（Windows）に保存され、キャッシュはマシン特徴から導出した鍵で AES-256-GCM 暗号化されます。利用規約：<https://www.ywhome.top/legal/terms.html> · プライバシー：<https://www.ywhome.top/legal/privacy.html>

## 使い方

1. インストールして起動。
2. **MCP ストア**（または **Skills** タブ）で検索。
3. **インストール**をクリックし、対象クライアントを選択。
4. そのクライアントでそのまま利用可能。
5. 不具合は **Inspector** で再現し、**履歴**から復元。
6. 複数端末なら **設定 → クラウド同期**で Git か SFTP を構成。

## サポート

- 製品情報・機能・対応クライアント：<https://www.ywhome.top>
- 報告・要望：[このリポジトリの Issues](https://github.com/qingchuang12/ai-tools-releases/issues) または **service@ywhome.top**

---

<p align="center">
  <sub>AI-Tools はプロプライエタリソフトウェアです · © 2026 AI-Tools Team · mcp-dock 由来部分は MIT ライセンスに従います（アプリ同梱の <code>THIRD_PARTY_LICENSES.md</code> を参照）。</sub><br>
  <sub><a href="https://www.ywhome.top">www.ywhome.top</a> · <a href="https://www.ywhome.top/legal/terms.html">利用規約</a> · <a href="https://www.ywhome.top/legal/privacy.html">プライバシー</a> · <a href="mailto:service@ywhome.top">service@ywhome.top</a></sub>
</p>

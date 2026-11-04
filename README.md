# AI-Tools

**One panel for your whole AI toolchain.** AI-Tools gathers the MCP servers and Agent Skills scattered across every AI coding client into a single desktop app — browse, install, edit, debug, back up, and sync them from one place.

<p align="center">
  <a href="https://www.ywhome.top">Official website</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/releases/latest">Download</a> ·
  <a href="https://www.ywhome.top/#product-ai-tools-pricing">Licence &amp; pricing</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/issues">Issue reports</a>
</p>

> **What this repository is.** It is the official **release-artifact feed** for AI-Tools: installers for Windows / macOS / Linux plus the update manifests the app reads for in-app auto-update. It holds no source code.
> **Product homepage, feature tour and licence purchase: <https://www.ywhome.top>**

**Languages:** English · [简体中文](#简体中文) · [العربية](#العربية) · [Deutsch](#deutsch) · [Español](#español) · [Français](#français) · [Italiano](#italiano) · [日本語](#日本語) · [Русский](#русский)

---

## English

### 1. What AI-Tools does

Every AI coding client keeps its MCP configuration in its own file, in its own format, in its own directory. Keeping those consistent by hand is error-prone busywork — and that is exactly what AI-Tools removes. It is a cross-platform Electron desktop app (Windows / macOS / Linux) that reads and writes the real config files of the clients you actually have installed, and adds a store, a debugger, a versioned history and an optional cloud sync on top.

AI-Tools is a proprietary derivative of the open-source **mcp-dock** project; the portions inherited from it remain under the original MIT licence, reproduced in the `THIRD_PARTY_LICENSES.md` that ships inside the app.

### 2. Feature overview

| Area | What you get |
| --- | --- |
| **MCP store** | Browse and search MCP servers across multiple sources (Smithery, npm registry, Alibaba Bailian offline index, ModelScope, the official MCP registry snapshot), with categories, real totals and server-side pagination. Disk-cached SWR lists: the first screen renders instantly, refreshes happen in the background. |
| **Skills store** | Discover and install Agent Skills, compatible with the `~/.agents/skills/` convention. Search, categories, sorting, source filters, pagination; the install button is disabled with a reason on clients that cannot take skills. |
| **One-click install, many clients** | Write one server or skill into several clients at once (e.g. Cursor + VS Code + Claude Code). Uninstall or update per client. Manual edits are flagged so a store update never overwrites your local tuning. |
| **MCP Inspector** | Built-in JSON-RPC debugger over **stdio / streamable-http / sse**. List Tools, Resources and Prompts, call any tool with arguments from a form, read the result with JSON highlighting, and watch the process log in a resizable panel. |
| **Library** | Everything you installed, in one list: edit command / args / env, batch-sync to many clients, uninstall. For skills: view and **edit SKILL.md online** (frontmatter and body), manage attached files, **import** from `.zip` / `.skill` / a folder / a pasted GitHub link / drag-and-drop, **export** several skills into one zip, and run conflict detection before any cloud push. |
| **Multi-client sync** | Client detection is fully probe-driven — only clients present on your machine are listed. Shared physical directories are de-duplicated so nothing is written twice. |
| **Cloud sync** | Push your MCP and Skills configuration to **your own** remote — Git (SSH key / HTTPS token / anonymous) or SFTP (password / key). Background task queue with live progress and retry, an explicit local-vs-remote consistency diff, and credentials stored only as encrypted SecretStore references. |
| **History & rollback** | Every install, uninstall, update, sync and edit is backed up. Diff any snapshot against the current state (added / removed / changed, colour-coded), restore any version in one click, or clear the history. |
| **Runtime probes** | Detects Node.js, Python and Git — presence, version, path — to explain "installed but it will not start". |
| **Look & language** | Light / dark / follow-system themes with native window chrome, and **9 UI languages**: English, 简体中文, العربية (RTL), Deutsch, Español, Français, Italiano, 日本語, Русский. Language packs load on demand and switching is instant. |
| **Security** | Local cache encrypted with AES-256-GCM (key derived from machine characteristics); external links restricted to http/https and opened in your browser; DNS-over-HTTPS to dodge polluted resolvers; single-instance lock; strict main / preload / renderer isolation behind an allow-list of IPC channels. |

### 3. Supported clients and config formats

**31 MCP configuration entries and 19 Skills targets**, counting the built-in clients plus the cloud-storage entry (27 distinct products). Detection is probed on your machine, and you can add a custom client by pointing at any MCP config path and skills directory.

Format differences are handled for you: VS Code uses `servers` rather than `mcpServers`, Warp uses `working_directory` rather than `cwd`, Kimi Code CLI uses `transport` rather than `type`, Zed uses `context_servers`, and Codex CLI writes a TOML `mcp_servers` section. Covered clients include Cursor, VS Code, Claude Code, Gemini CLI, Codex CLI, Windsurf, Zed, TRAE (and CN / SOLO / plugin), Kiro, OpenCode, JetBrains IDEs, Antigravity, OpenClaw, CodeBuddy, WorkBuddy, Qoder, ZCode, Cline, Qwen Code, iFlow CLI, LM Studio, OpenHands, GitHub Copilot CLI, Warp, Kimi Code CLI, Kilo Code and Goose.

### 4. What lives in this repository

Releases carry the built binaries and the update manifests; nothing else. For each version you will find:

| Artifact | Platform |
| --- | --- |
| `AI-Tools-Setup-<version>.exe` | Windows installer (NSIS, x64) |
| `AI-Tools-<version>-portable.exe` | Windows portable, no install |
| `AI-Tools-<version>.dmg` / `-arm64.dmg` | macOS disk image (Intel / Apple silicon) |
| `AI-Tools-<version>-mac.zip` / `-arm64-mac.zip` | macOS archives |
| `AI-Tools-<version>.AppImage` / `-arm64.AppImage` | Linux AppImage (x64 / arm64) |
| `ai-tools_<version>_amd64.deb` / `_arm64.deb` | Linux .deb |
| `latest.yml`, `portable.yml`, `latest-mac.yml`, `latest-linux.yml`, `latest-linux-arm64.yml` | Auto-update manifests |
| `*.blockmap` | Delta-download blocks |

Every asset is anonymously downloadable — no token, no sign-in. The auto-update feed the app reads is, for example:

```
https://github.com/qingchuang12/ai-tools-releases/releases/latest/download/latest.yml
```

Manifests carry SHA-512 digests and file sizes; the updater verifies them before installing anything.

### 5. Download and install

Grab the newest build from [Releases → latest](https://github.com/qingchuang12/ai-tools-releases/releases/latest) and pick the artifact for your platform in the table above. Direct links for the current release (**1.1.1**, published 2026-11-02):

- Windows installer — [AI-Tools-Setup-1.1.1.exe](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-Setup-1.1.1.exe)
- Windows portable — [AI-Tools-1.1.1-portable.exe](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-portable.exe)
- macOS Intel / Apple silicon — [AI-Tools-1.1.1.dmg](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.dmg) · [AI-Tools-1.1.1-arm64.dmg](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-arm64.dmg)
- Linux x64 / arm64 — [AI-Tools-1.1.1.AppImage](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.AppImage) · [ai-tools_1.1.1_amd64.deb](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/ai-tools_1.1.1_amd64.deb)

The official site's download page ([www.ywhome.top/#product-ai-tools-download](https://www.ywhome.top/#product-ai-tools-download)) is opening up platform by platform; until a button is live there, this repository is the working download channel.

Install notes:

- Builds are currently **not code-signed**. Windows SmartScreen: "More info → Run anyway".
- macOS Gatekeeper may report the app as damaged: `xattr -cr /Applications/AI-Tools.app`
- AppImage: `chmod +x AI-Tools-1.1.1.AppImage` first.

### 6. In-app auto-update

Installed builds check this repository on their own and update in place — no need to re-download. NSIS installs follow `latest.yml`, portable builds follow `portable.yml`, macOS follows `latest-mac.yml`, Linux follows `latest-linux.yml` / `latest-linux-arm64.yml`.

### 7. Licence, activation and ads

AI-Tools is **proprietary software** (all rights reserved) — the binaries here are licensed for installation and use as described in the end-user licence, not as open source; portions inherited from mcp-dock stay under its original MIT licence, reproduced in `THIRD_PARTY_LICENSES.md` shipped with the app.

Everything is usable without activation: store browsing, one-click install, the Inspector, library editing, history rollback and multi-client sync. **Only cloud sync is entitlement-gated** — a fresh install gets a trial period (60 days by default), after which cloud sync pauses until you activate; activation is a locally verified signed token, re-checked online periodically. Purchase and activation entry points are on the official site: <https://www.ywhome.top/#product-ai-tools-pricing>.

Some distribution builds show ads until you activate; other builds are compiled without any ads. This is a packaging variant, not a feature cut — store and library capabilities are identical.

### 8. Privacy and data

Local-first: AI-Tools reads and writes config files on your machine and does not upload anything unless you configure cloud sync yourself. Application data lives in `~/.ai-tools/` (macOS / Linux) or `%USERPROFILE%\.ai-tools\` (Windows); the local cache is AES-256-GCM encrypted with a machine-derived key. Remote credentials are never stored as plaintext. Terms: <https://www.ywhome.top/legal/terms.html> · Privacy: <https://www.ywhome.top/legal/privacy.html>

### 9. Quick start

1. Install and open AI-Tools.
2. Browse or search in the **MCP store** (or switch to the **Skills** tab).
3. Click **Install**, select one or more target clients.
4. Use the capability in that client — no JSON copy-pasting.
5. Something wrong? Debug it in **Inspector**, then roll back from **History**.
6. Multiple machines? Configure Git or SFTP in **Settings → Cloud sync**.

### 10. Support

- Product information, features, clients and pricing: <https://www.ywhome.top>
- Bug reports and requests: [open an issue in this repository](https://github.com/qingchuang12/ai-tools-releases/issues) or write to **service@ywhome.top**

---

## 简体中文

**AI-Tools 是一款面向 AI 开发者的跨平台桌面管理器（Electron，支持 Windows / macOS / Linux）**：把散落在各家 AI 客户端配置里的 MCP 服务器与 Agent Skills 收拢到同一块面板，统一管理、批量分发、云端同步。项目基于开源 **mcp-dock** 二次开发，继承部分仍遵循其原 MIT 条款（MIT 原文随应用分发，见安装目录内 `THIRD_PARTY_LICENSES.md`），其余为专有软件。

- **官网（产品介绍 / 功能 / 支持客户端 / 定价 / 法务）**：<https://www.ywhome.top>
- **下载与在线更新清单**：本仓 [Releases](https://github.com/qingchuang12/ai-tools-releases/releases/latest)，最新版本 **1.1.1**（2026-11-02 发布）
- **支持范围**：31 个 MCP 配置入口、19 个 Skills 目标（含云端存储入口），自动适配 JSON / JSONC / TOML 三种配置格式
- **核心能力**：MCP 商店与 Skills 商店（多数据源、磁盘缓存 + SWR 秒开）、一键多端安装/卸载/更新、内置 MCP Inspector（stdio / streamable-http / sse，Tools·Resources·Prompts 实调）、我的库（在线编辑 SKILL.md、导入 `.zip`/`.skill`/GitHub 链接、导出打包、冲突检测）、配置多端同步（探测驱动、共享目录去重）、云端同步（Git SSH/Token/匿名 + SFTP，后台任务队列与一致性比对）、历史备份与 Diff 回滚、运行时环境检测（Node.js / Python / Git）、浅色·暗色·跟随系统主题、9 种界面语言（含阿拉伯语 RTL）、AES-256-GCM 加密缓存与进程隔离
- **授权**：商店、安装、Inspector、库编辑、历史回滚、多端同步**全部无需激活即可使用**；仅**云端同步**受权益门禁，新装默认 60 天试用，到期后暂停云同步直至激活。购买与激活入口见 [官网定价页](https://www.ywhome.top/#product-ai-tools-pricing)。
- **安装提示**：当前构建未做代码签名。Windows 遇 SmartScreen 选「更多信息 → 仍要运行」；macOS 提示损坏时执行 `xattr -cr /Applications/AI-Tools.app`；AppImage 先 `chmod +x`。
- **数据位置**：`~/.ai-tools/`（macOS / Linux）、`%USERPROFILE%\.ai-tools\`（Windows）。本地优先，未配置云同步时不上传任何内容。
- **反馈**：在本仓 [Issues](https://github.com/qingchuang12/ai-tools-releases/issues) 提问，或写信至 **service@ywhome.top**。条款：<https://www.ywhome.top/legal/terms.html> · 隐私：<https://www.ywhome.top/legal/privacy.html>

---

## العربية

**AI-Tools** تطبيق سطح مكتب متعدد المنصات (Electron على أنظمة Windows وmacOS وLinux) يجمع خوادم MCP ومهارات Agent الموزّعة على إعدادات أدوات الذكاء الاصطناعي في لوحة واحدة: تصفّح، تثبيت، تحرير، تصحيح، نسخ احتياطي ومزامنة سحابية.

- **الموقع الرسمي**: <https://www.ywhome.top> — **التنزيلات**: [Releases](https://github.com/qingchuang12/ai-tools-releases/releases/latest) (أحدث إصدار **1.1.1**)
- يدعم 31 مدخل إعدادات MCP و19 وجهة للمهارات، بصيغ JSON / JSONC / TOML، مع 9 لغات واجهة تشمل العربية (تخطيط RTL).
- كل الميزات متاحة دون تفعيل؛ البوابة الوحيدة هي المزامنة السحابية (فترة تجربة 60 يومًا افتراضيًا). الشراء: <https://www.ywhome.top/#product-ai-tools-pricing>
- الملفات غير موقّعة حاليًا: على macOS نفّذ `xattr -cr /Applications/AI-Tools.app`.
- البيانات محفوظة محليًا في `~/.ai-tools/` ولا تُرفع أي بيانات قبل إعداد المزامنة السحابية بنفسك.
- الدعم: [Issues](https://github.com/qingchuang12/ai-tools-releases/issues) · **service@ywhome.top**

---

## Deutsch

**AI-Tools** ist eine plattformübergreifende Desktop-Anwendung (Electron für Windows / macOS / Linux), die MCP-Server und Agent Skills aus den Konfigurationsdateien aller KI-Coding-Clients in einer Oberfläche bündelt — durchsuchen, installieren, bearbeiten, debuggen, sichern und synchronisieren.

- **Website**: <https://www.ywhome.top> · **Downloads**: [Releases](https://github.com/qingchuang12/ai-tools-releases/releases/latest) (aktuell **1.1.1**)
- 31 MCP-Konfigurationseinträge und 19 Skill-Ziele, Formate JSON / JSONC / TOML, 9 Benutzeroberflächen-Sprachen.
- Alle Funktionen sind ohne Aktivierung nutzbar; nur die **Cloud-Synchronisation** ist an eine Lizenz gebunden (Standard-Testzeitraum 60 Tage). Kauf: <https://www.ywhome.top/#product-ai-tools-pricing>
- Builds sind derzeit nicht signiert — macOS: `xattr -cr /Applications/AI-Tools.app`
- Lokale Daten unter `~/.ai-tools/`; ohne eingerichtete Cloud-Synchronisation werden keine Daten hochgeladen.
- Support: [Issues](https://github.com/qingchuang12/ai-tools-releases/issues) · **service@ywhome.top**

---

## Español

**AI-Tools** es una aplicación de escritorio multiplataforma (Electron para Windows / macOS / Linux) que reúne los servidores MCP y las Agent Skills dispersos en la configuración de cada cliente de IA en un solo panel: explorar, instalar, editar, depurar, respaldar y sincronizar en la nube.

- **Sitio oficial**: <https://www.ywhome.top> · **Descargas**: [Releases](https://github.com/qingchuang12/ai-tools-releases/releases/latest) (versión actual **1.1.1**)
- 31 entradas de configuración MCP y 19 destinos de skills, con formatos JSON / JSONC / TOML y 9 idiomas de interfaz.
- Todo funciona sin activación; solo la **sincronización en la nube** requiere licencia (periodo de prueba de 60 días por defecto). Compra: <https://www.ywhome.top/#product-ai-tools-pricing>
- Las compilaciones aún no están firmadas — en macOS: `xattr -cr /Applications/AI-Tools.app`
- Datos locales en `~/.ai-tools/`; nada se sube hasta que configuras la sincronización.
- Soporte: [Issues](https://github.com/qingchuang12/ai-tools-releases/issues) · **service@ywhome.top**

---

## Français

**AI-Tools** est une application de bureau multiplateforme (Electron pour Windows / macOS / Linux) qui réunit, dans un seul panneau, les serveurs MCP et les Agent Skills dispersés dans la configuration de chaque client d'IA : parcourir, installer, éditer, déboguer, sauvegarder et synchroniser.

- **Site officiel** : <https://www.ywhome.top> · **Téléchargements** : [Releases](https://github.com/qingchuang12/ai-tools-releases/releases/latest) (version **1.1.1**)
- 31 entrées de configuration MCP et 19 cibles de skills, formats JSON / JSONC / TOML, 9 langues d'interface.
- Tout est utilisable sans activation ; seule la **synchronisation cloud** exige une licence (essai de 60 jours par défaut). Achat : <https://www.ywhome.top/#product-ai-tools-pricing>
- Les builds ne sont pas encore signés — macOS : `xattr -cr /Applications/AI-Tools.app`
- Données locales dans `~/.ai-tools/` ; rien n'est envoyé tant que la synchronisation n'est pas configurée.
- Assistance : [Issues](https://github.com/qingchuang12/ai-tools-releases/issues) · **service@ywhome.top**

---

## Italiano

**AI-Tools** è un'applicazione desktop multipiattaforma (Electron per Windows / macOS / Linux) che raccoglie in un unico pannello i server MCP e le Agent Skills sparsi nelle configurazioni dei vari client AI: sfogliare, installare, modificare, debuggare, fare backup e sincronizzare.

- **Sito ufficiale**: <https://www.ywhome.top> · **Download**: [Releases](https://github.com/qingchuang12/ai-tools-releases/releases/latest) (versione **1.1.1**)
- 31 voci di configurazione MCP e 19 destinazioni di skills, formati JSON / JSONC / TOML, 9 lingue dell'interfaccia.
- Tutto è utilizzabile senza attivazione; solo la **sincronizzazione cloud** richiede una licenza (periodo di prova di 60 giorni). Acquisto: <https://www.ywhome.top/#product-ai-tools-pricing>
- Le build non sono ancora firmate — macOS: `xattr -cr /Applications/AI-Tools.app`
- Dati locali in `~/.ai-tools/`; nulla viene caricato finché non configuri la sincronizzazione.
- Supporto: [Issues](https://github.com/qingchuang12/ai-tools-releases/issues) · **service@ywhome.top**

---

## 日本語

**AI-Tools** は AI コーディングクライアントの設定ファイルに分散している MCP サーバーと Agent Skills を一つの画面に集約する、クロスプラットフォームのデスクトップアプリ（Electron / Windows・macOS・Linux）です。検索・インストール・編集・デバッグ・バックアップ・クラウド同期をまとめて行えます。

- **公式サイト**: <https://www.ywhome.top> · **ダウンロード**: [Releases](https://github.com/qingchuang12/ai-tools-releases/releases/latest)（最新 **1.1.1**）
- 31 の MCP 設定エントリーと 19 の Skills 同期先に対応（JSON / JSONC / TOML 形式を自動吸収）、UI は 9 言語。
- 有効化なしで全機能を利用可能。ゲートされるのは**クラウド同期**のみで、既定の 60 日トライアル後に停止します。購入: <https://www.ywhome.top/#product-ai-tools-pricing>
- 現在のビルドは未署名です。macOS で起動しない場合: `xattr -cr /Applications/AI-Tools.app`
- データは `~/.ai-tools/` に保存されるローカルファースト。クラウド同期を設定しない限り送信されません。
- お問い合わせ: [Issues](https://github.com/qingchuang12/ai-tools-releases/issues) · **service@ywhome.top**

---

## Русский

**AI-Tools** — кроссплатформенное десктоп-приложение (Electron для Windows / macOS / Linux), которое собирает MCP-серверы и Agent Skills из конфигураций всех AI-клиентов в одну панель: поиск, установка, редактирование, отладка, резервные копии и облачная синхронизация.

- **Официальный сайт**: <https://www.ywhome.top> · **Загрузки**: [Releases](https://github.com/qingchuang12/ai-tools-releases/releases/latest) (текущая версия **1.1.1**)
- 31 конфигурационный вход MCP и 19 целей для скиллов, форматы JSON / JSONC / TOML, 9 языков интерфейса.
- Все функции доступны без активации; ограничена только **облачная синхронизация** (испытательный период по умолчанию 60 дней). Покупка: <https://www.ywhome.top/#product-ai-tools-pricing>
- Сборки пока не подписаны — на macOS выполните `xattr -cr /Applications/AI-Tools.app`
- Данные хранятся локально в `~/.ai-tools/`; без настроенной синхронизации ничего не отправляется.
- Поддержка: [Issues](https://github.com/qingchuang12/ai-tools-releases/issues) · **service@ywhome.top**

---

<p align="center">
  <sub>AI-Tools is proprietary software · © 2026 AI-Tools Team · Portions derived from the open-source mcp-dock project remain under its MIT License (see <code>THIRD_PARTY_LICENSES.md</code> shipped with the app).</sub><br>
  <sub><a href="https://www.ywhome.top">www.ywhome.top</a> · <a href="https://www.ywhome.top/legal/terms.html">Terms</a> · <a href="https://www.ywhome.top/legal/privacy.html">Privacy</a> · <a href="mailto:service@ywhome.top">service@ywhome.top</a></sub>
</p>

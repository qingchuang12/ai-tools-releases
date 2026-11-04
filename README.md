# AI-Tools

**One panel for your whole AI toolchain.** AI-Tools brings every MCP server and Agent Skill from every AI coding client you use into one desktop app — discover it, install it, edit it, debug it, roll it back and sync it, without hand-editing another config file.

<p align="center">
  <a href="https://www.ywhome.top">Official website</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/releases/latest">Download</a> ·
  <a href="https://www.ywhome.top/#product-ai-tools-pricing">Licence &amp; pricing</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/issues">Issue reports</a>
</p>

<p align="center">
  <strong>English</strong> ·
  <a href="./README.zh.md">简体中文</a> ·
  <a href="./README.ar.md">العربية</a> ·
  <a href="./README.de.md">Deutsch</a> ·
  <a href="./README.es.md">Español</a> ·
  <a href="./README.fr.md">Français</a> ·
  <a href="./README.it.md">Italiano</a> ·
  <a href="./README.ja.md">日本語</a> ·
  <a href="./README.ru.md">Русский</a>
</p>

> **This repository** is the official release-artifact feed for AI-Tools: installers for Windows / macOS / Linux plus the update manifests the app reads for in-app auto-update. It contains no source code.
> **Product tour and feature list: <https://www.ywhome.top>**

---

## The capability, in one line

**31 MCP configuration entries and 19 Skills targets managed as a single inventory** — Cursor, VS Code, Claude Code, Gemini CLI, Codex CLI, Windsurf, Zed, TRAE (CN / SOLO / plugin), Kiro, OpenCode, JetBrains IDEs, Antigravity, OpenClaw, CodeBuddy, WorkBuddy, Qoder, ZCode, Cline, Qwen Code, iFlow CLI, LM Studio, OpenHands, GitHub Copilot CLI, Warp, Kimi Code CLI, Kilo Code, Goose, plus the cloud-storage entry. Detection is probed on your machine, and any client not on the list can be added by pointing at its config path.

## Why it is worth your time

| The daily friction | What AI-Tools gives you |
| --- | --- |
| One MCP server, six JSON files, six different key names | **Write once, deploy to many.** A single click fans the config out to every client you select, each in its own dialect — JSON / JSONC / TOML, `servers` vs `mcpServers`, `working_directory` vs `cwd`, `transport` vs `type`, `context_servers`, `mcp_servers`. |
| Store pages that spin while you wait | **Instant first screen.** Disk-cached SWR lists render before the network answers and refresh silently in the background (list 1 h, detail 24 h), with a force-refresh whenever you ask. |
| "Did that edit just break my client?" | **Every change is reversible.** Installs, uninstalls, updates, syncs and edits are backed up automatically; diff any snapshot against live state (added / removed / changed, colour-coded) and restore in one click. |
| Debugging an MCP server with curl and a text editor | **Inspector built in.** Call Tools, Resources and Prompts over stdio / streamable-http / sse from a form, read highlighted JSON results, watch the process log in a resizable panel. |
| Rebuilding your whole setup on a new machine | **Your own cloud, one-click restore.** Push MCP and Skills config to Git (SSH key / HTTPS token / anonymous) or SFTP (password / key) through a background task queue with live progress and retry, guarded by an explicit local-vs-remote consistency diff. |
| Skills you can only touch from a terminal | **A real skills workflow.** Edit SKILL.md frontmatter and body in-app, manage attached files, import `.zip` / `.skill` / a folder / a pasted GitHub link / drag-and-drop, export several skills as one zip, with conflict detection before any cloud push. |
| A config manager that phones home | **Local-first by default.** Nothing leaves the machine until you configure cloud sync yourself; cache encrypted with AES-256-GCM, remote credentials kept only as encrypted SecretStore references, external links restricted to http/https. |

## Core features

**MCP store** — browse and search servers across Smithery, the npm registry, the Alibaba Bailian offline index (251 entries, no network needed), ModelScope and the official MCP registry snapshot. Categories, real totals, server-side pagination — the same behaviour as the upstream web.

**Skills store** — discover and install Agent Skills, compatible with the `~/.agents/skills/` convention. Search, category filters that follow the UI language, sorting, source facets, pagination and page-size control; install-status badges refresh themselves. On clients that cannot take skills the button is disabled *with a reason*, so no empty `.source.json` shells are ever produced.

**One-click deploy** — install to several clients at once, uninstall or update per client, and flag manual edits so a store update never overwrites your local tuning. Sources can be switched per request, and connections are managed in Settings with a real per-platform connectivity test.

**MCP Inspector** — an interactive JSON-RPC debugger: custom command, args, env and headers; Tools / Resources / Prompts discovery; direct tool invocation with typed arguments; child processes are reclaimed on exit so nothing lingers.

**Library** — everything installed, in one place: edit command / args / env, batch-select and sync to many clients, uninstall. The Skills tab adds online SKILL.md editing, attachment management, import from archive / folder / GitHub link / drag-and-drop, bulk zip export and cloud conflict resolution (overwrite or skip, per item).

**Cloud sync** — Git or SFTP to your own remote, automatic pull at startup, manual push, a task panel with progress and one-click retry, and a consistency check that shows both sides before anything is overwritten.

**History & rollback** — timestamped backups showing size, clients and entry counts; version-to-version diff; one-click restore; full history clear.

**Runtime probes** — Node.js, Python and Git detection (presence, version, path) to answer "installed but it will not start".

**Platform sources & API tokens** — built-in and platform-direct sources managed side by side (base URL + token), enable/disable, default, export, plus a token centre with scoped (`skills:read`, `skills:download`, `models:read`, `models:download`, `admin`) and expiring credentials.

**Look & language** — light / dark / follow-system themes with native window chrome, and **9 UI languages**: English, 简体中文, العربية (full RTL), Deutsch, Español, Français, Italiano, 日本語, Русский. Language packs load on demand; switching is instant.

**Security engineering** — AES-256-GCM encrypted cache keyed on machine characteristics, http/https-only external links opened in your browser, DNS-over-HTTPS against polluted resolvers, single-instance lock, and strict main / preload / renderer isolation behind an allow-listed IPC surface.

## What a release contains

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

## Download and install

Newest published build: **1.1.1** (2026-11-02) — [Releases → latest](https://github.com/qingchuang12/ai-tools-releases/releases/latest).

- Windows installer — [AI-Tools-Setup-1.1.1.exe](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-Setup-1.1.1.exe)
- Windows portable — [AI-Tools-1.1.1-portable.exe](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-portable.exe)
- macOS Intel / Apple silicon — [AI-Tools-1.1.1.dmg](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.dmg) · [AI-Tools-1.1.1-arm64.dmg](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-arm64.dmg)
- Linux x64 / arm64 — [AI-Tools-1.1.1.AppImage](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.AppImage) · [ai-tools_1.1.1_amd64.deb](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/ai-tools_1.1.1_amd64.deb)

The official site's download page ([www.ywhome.top/#product-ai-tools-download](https://www.ywhome.top/#product-ai-tools-download)) is opening up platform by platform; until a button is live there, this repository is the working download channel.

Builds are currently **not code-signed**: Windows SmartScreen → "More info → Run anyway"; macOS, if it reports the app as damaged, `xattr -cr /Applications/AI-Tools.app`; AppImage, `chmod +x` first.

## In-app auto-update

Installed builds check this repository on their own and update in place — no re-downloading. NSIS installs follow `latest.yml`, portable builds follow `portable.yml`, macOS follows `latest-mac.yml`, Linux follows `latest-linux.yml` / `latest-linux-arm64.yml`.

## Privacy and data

Local-first: AI-Tools reads and writes config files on your machine and uploads nothing unless you configure cloud sync yourself. Application data lives in `~/.ai-tools/` (macOS / Linux) or `%USERPROFILE%\.ai-tools\` (Windows); the local cache is AES-256-GCM encrypted with a machine-derived key. Terms: <https://www.ywhome.top/legal/terms.html> · Privacy: <https://www.ywhome.top/legal/privacy.html>

## Quick start

1. Install and open AI-Tools.
2. Browse or search the **MCP store** (or switch to the **Skills** tab).
3. Click **Install** and pick one or more target clients.
4. Use the capability in that client — no JSON copy-pasting.
5. Something wrong? Reproduce it in **Inspector**, then roll back from **History**.
6. Multiple machines? Configure Git or SFTP in **Settings → Cloud sync**.

## Support

- Product information, features and supported clients: <https://www.ywhome.top>
- Bug reports and feature requests: [open an issue here](https://github.com/qingchuang12/ai-tools-releases/issues) or write to **service@ywhome.top**

---

<p align="center">
  <sub>AI-Tools is proprietary software · © 2026 AI-Tools Team · Portions derived from the open-source mcp-dock project remain under its MIT License (see <code>THIRD_PARTY_LICENSES.md</code> shipped with the app).</sub><br>
  <sub><a href="https://www.ywhome.top">www.ywhome.top</a> · <a href="https://www.ywhome.top/legal/terms.html">Terms</a> · <a href="https://www.ywhome.top/legal/privacy.html">Privacy</a> · <a href="mailto:service@ywhome.top">service@ywhome.top</a></sub>
</p>

# AI-Tools（简体中文）

**一个面板，管住你的整条 AI 工具链。** AI-Tools 把你使用的每一款 AI 编程客户端里的 MCP 服务器与 Agent Skills 全部收进一个桌面应用：发现、安装、编辑、调试、回滚、同步，一步到位，从此不再手改配置文件。

<p align="center">
  <a href="https://www.ywhome.top">官方网站</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/releases/latest">下载</a> ·
  <a href="https://www.ywhome.top/#product-ai-tools-pricing">授权与定价</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/issues">问题反馈</a>
</p>

<p align="center">
  <a href="./README.md">English</a> ·
  <strong>简体中文</strong> ·
  <a href="./README.ar.md">العربية</a> ·
  <a href="./README.de.md">Deutsch</a> ·
  <a href="./README.es.md">Español</a> ·
  <a href="./README.fr.md">Français</a> ·
  <a href="./README.it.md">Italiano</a> ·
  <a href="./README.ja.md">日本語</a> ·
  <a href="./README.ru.md">Русский</a>
</p>

> **本仓库**是 AI-Tools 的官方发布产物仓：Windows / macOS / Linux 安装包，以及应用内在线更新所读取的更新清单。仓内不含源代码。
> **产品导览与功能明细：<https://www.ywhome.top>**

---

## 一句话能力

**把 31 个 MCP 配置入口、19 个 Skills 目标当成一份清单来管** —— Cursor、VS Code、Claude Code、Gemini CLI、Codex CLI、Windsurf、Zed、TRAE（CN / SOLO / 插件）、Kiro、OpenCode、JetBrains 系列、Antigravity、OpenClaw、CodeBuddy、WorkBuddy、Qoder、ZCode、Cline、Qwen Code、iFlow CLI、LM Studio、OpenHands、GitHub Copilot CLI、Warp、Kimi Code CLI、Kilo Code、Goose 以及云端存储入口。清单完全由本机探测得出；列表之外的客户端，只要指给它配置文件路径与 Skills 目录，即可纳入统一管理。

## 为什么值得用

| 你每天的麻烦 | AI-Tools 给你的 |
| --- | --- |
| 同一个 Server，六份 JSON，六种键名 | **一次写入，多端生效。** 一次点选即把配置分发到所选客户端，并自动说各家的方言：JSON / JSONC / TOML、`servers` 与 `mcpServers`、`working_directory` 与 `cwd`、`transport` 与 `type`、`context_servers`、`mcp_servers`。 |
| 商店列表一直在转圈 | **首屏秒开。** 磁盘缓存 + SWR，先出画面再等网络，后台静默刷新（列表 1 小时、详情 24 小时），要新数据时一键强制刷新。 |
| 「刚改的配置会不会把客户端搞坏？」 | **任何改动都能退。** 安装、卸载、更新、同步、编辑全部自动备份；任意历史版本与当前状态做 Diff（新增 / 移除 / 修改分色标注），一键恢复。 |
| 用 curl 和文本编辑器调 MCP | **内置 Inspector。** stdio / streamable-http / sse 三种传输，表单里直接调用 Tool 并传参，结果 JSON 高亮，日志面板可拖拽。 |
| 换台机器要重配一遍 | **云端在你手里，一键还原。** 配置推到你自己的 Git（SSH 私钥 / HTTPS Token / 匿名）或 SFTP（密码 / 私钥），后台任务队列带实时进度与重试，推送前先做本地与云端的逐条一致性比对。 |
| Skills 只能靠命令行摆弄 | **完整的技能工作流。** 应用内在线编辑 SKILL.md 的 frontmatter 与正文、管理附属文件；导入 `.zip` / `.skill` / 已解压目录 / 粘贴 GitHub 链接 / 拖拽；多个技能一键打包导出；上云前自动冲突检测，可逐条选择覆盖或跳过。 |
| 担心配置管理器偷偷上传 | **本地优先。** 不主动配置云同步就不上传任何东西；缓存 AES-256-GCM 加密，远端凭据只以加密引用（SecretStore）保存，外部链接仅允许 http/https。 |

## 核心功能

**MCP 商店** —— Smithery、npm Registry、阿里云百炼离线索引（251 条，无需联网）、ModelScope、官方注册表快照多源切换；分类筛选、真实总数、服务端分页，与上游 Web 行为一致。

**Skills 商店** —— 兼容 `~/.agents/skills/` 统一标准；关键词搜索、随界面语言切换的分类标签、排序、来源筛选、分页与每页条数，安装状态徽章自动刷新。不支持安装的平台会禁用按钮并说明原因，绝不产出只含 `.source.json` 的空壳目录。

**一键部署** —— 多客户端同时安装、按客户端单独卸载或更新；在「我的库」里改过的配置会被标记为手动安装，商店更新不会覆盖你的本地调整。

**MCP Inspector** —— 交互式 JSON-RPC 调试器：自定义启动命令、参数、环境变量与请求头；连接后浏览 Tools / Resources / Prompts；图形界面直接调用并传参；子进程随应用退出自动回收，不留残留。

**我的库** —— 已安装内容的集中台账：编辑命令 / 参数 / 环境变量，批量多选同步到多个客户端，卸载管理；Skills 页支持在线编辑、附属文件管理、导入导出与云同步冲突处理。

**云端同步** —— Git / SFTP 双通道，启动自动拉取与手动推送都进任务面板，失败一键重试；一致性检测逐条对比两端内容，确认后才动手，避免误覆盖。

**历史与回滚** —— 备份列表展示时间、大小、涉及客户端与条目数量；任意版本 Diff 对比；一键恢复；支持清空全部历史。

**运行时环境检测** —— 自动识别本机 Node.js、Python、Git 的安装状态、版本与路径，快速定位「装了却跑不起来」。

**平台源与 API 令牌** —— 内置源与平台直连源统一管理（Base URL + API Token），每个连接支持按平台真实端点探测的「测试连接」、启停、设为默认、删除与导出；令牌中心可创建 / 导入 / 撤销 / 恢复，并按作用域与到期时间精细管理。

**外观与语言** —— 浅色 / 暗色 / 跟随系统主题（含 macOS 与 Windows 原生窗口适配）；**9 种界面语言**：English、简体中文、العربية（完整 RTL）、Deutsch、Español、Français、Italiano、日本語、Русский；语言包按需加载，切换即时生效。

**安全工程** —— 缓存与本地数据 AES-256-GCM 加密（密钥按机器特征派生，无需弹窗）；外部链接仅允许 http/https 并交给系统浏览器；内置安全 DNS（DoH）规避污染；单实例锁；主进程 / 预加载 / 渲染进程三层隔离，渲染层只能走白名单 IPC 通道。

## 每个版本包含什么

| 产物 | 平台 |
| --- | --- |
| `AI-Tools-Setup-<版本>.exe` | Windows 安装包（NSIS，x64） |
| `AI-Tools-<版本>-portable.exe` | Windows 便携版，免安装 |
| `AI-Tools-<版本>.dmg` / `-arm64.dmg` | macOS 磁盘映像（Intel / Apple 芯片） |
| `AI-Tools-<版本>-mac.zip` / `-arm64-mac.zip` | macOS 压缩包 |
| `AI-Tools-<版本>.AppImage` / `-arm64.AppImage` | Linux AppImage（x64 / arm64） |
| `ai-tools_<版本>_amd64.deb` / `_arm64.deb` | Linux .deb |
| `latest.yml`、`portable.yml`、`latest-mac.yml`、`latest-linux.yml`、`latest-linux-arm64.yml` | 在线更新清单 |
| `*.blockmap` | 差分下载块 |

所有附件均可匿名下载，无需令牌与登录。应用读取的更新源形如：

```
https://github.com/qingchuang12/ai-tools-releases/releases/latest/download/latest.yml
```

清单内含 SHA-512 摘要与文件大小，更新器校验通过后才落盘安装。

## 下载与安装

当前已发布最新版本：**1.1.1**（2026-11-02）—— [Releases 最新页](https://github.com/qingchuang12/ai-tools-releases/releases/latest)。

- Windows 安装包 —— [AI-Tools-Setup-1.1.1.exe](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-Setup-1.1.1.exe)
- Windows 便携版 —— [AI-Tools-1.1.1-portable.exe](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-portable.exe)
- macOS Intel / Apple 芯片 —— [AI-Tools-1.1.1.dmg](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.dmg) · [AI-Tools-1.1.1-arm64.dmg](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-arm64.dmg)
- Linux x64 / arm64 —— [AI-Tools-1.1.1.AppImage](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.AppImage) · [ai-tools_1.1.1_amd64.deb](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/ai-tools_1.1.1_amd64.deb)

官网下载页（[www.ywhome.top/#product-ai-tools-download](https://www.ywhome.top/#product-ai-tools-download)）正在逐平台开放；在按钮开放之前，本仓就是可用的下载通道。

当前构建**未做代码签名**：Windows 遇 SmartScreen 选「更多信息 → 仍要运行」；macOS 若提示应用已损坏，执行 `xattr -cr /Applications/AI-Tools.app`；AppImage 先 `chmod +x`。

## 应用内在线更新

已安装的应用会自行检查本仓并就地更新，无需重新下载：NSIS 安装包读 `latest.yml`，便携版读 `portable.yml`，macOS 读 `latest-mac.yml`，Linux 读 `latest-linux.yml` / `latest-linux-arm64.yml`。

## 隐私与数据

本地优先：应用只读写你本机的配置文件，未自行配置云同步前不上传任何内容。数据位于 `~/.ai-tools/`（macOS / Linux）、`%USERPROFILE%\.ai-tools\`（Windows），本地缓存以机器特征派生密钥做 AES-256-GCM 加密。条款：<https://www.ywhome.top/legal/terms.html> · 隐私：<https://www.ywhome.top/legal/privacy.html>

## 快速上手

1. 安装并打开 AI-Tools。
2. 在「MCP 商店」浏览或搜索，或切到「Skills」标签。
3. 点「安装」，勾选一个或多个目标客户端。
4. 回到该客户端直接使用，无需复制粘贴 JSON。
5. 出问题先在「Inspector」里复现，再到「历史」一键回滚。
6. 多台设备去「设置 → 云同步」配置 Git 或 SFTP。

## 支持

- 产品信息、功能明细与支持客户端：<https://www.ywhome.top>
- 缺陷与需求反馈：在本仓 [Issues](https://github.com/qingchuang12/ai-tools-releases/issues) 提问，或写信至 **service@ywhome.top**

---

<p align="center">
  <sub>AI-Tools 为专有软件 · © 2026 AI-Tools Team · 源自开源项目 mcp-dock 的部分仍遵循其 MIT 条款（见应用内 <code>THIRD_PARTY_LICENSES.md</code>）。</sub><br>
  <sub><a href="https://www.ywhome.top">www.ywhome.top</a> · <a href="https://www.ywhome.top/legal/terms.html">服务条款</a> · <a href="https://www.ywhome.top/legal/privacy.html">隐私政策</a> · <a href="mailto:service@ywhome.top">service@ywhome.top</a></sub>
</p>

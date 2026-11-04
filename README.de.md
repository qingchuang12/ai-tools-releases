# AI-Tools (Deutsch)

**Ein Panel für Ihre gesamte AI-Toolchain.** AI-Tools sammelt die MCP-Server und Agent Skills aus den Konfigurationsdateien aller Ihrer AI-Coding-Clients in einer Desktop-Anwendung — finden, installieren, bearbeiten, debuggen, zurückrollen und synchronisieren, ohne je wieder von Hand JSON zu pflegen.

<p align="center">
  <a href="https://www.ywhome.top">Offizielle Website</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/releases/latest">Download</a> ·
  <a href="https://www.ywhome.top/#product-ai-tools-pricing">Lizenz &amp; Preise</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/issues">Fehlermeldungen</a>
</p>

<p align="center">
  <a href="./README.md">English</a> ·
  <a href="./README.zh.md">简体中文</a> ·
  <a href="./README.ar.md">العربية</a> ·
  <strong>Deutsch</strong> ·
  <a href="./README.es.md">Español</a> ·
  <a href="./README.fr.md">Français</a> ·
  <a href="./README.it.md">Italiano</a> ·
  <a href="./README.ja.md">日本語</a> ·
  <a href="./README.ru.md">Русский</a>
</p>

> **Dieses Repository** ist der offizielle Release-Speicher von AI-Tools: Installationspakete für Windows / macOS / Linux sowie die Update-Manifeste, aus denen sich die App automatisch aktualisiert. Es enthält kein Quellcode.
> **Funktionsüberblick und unterstützte Clients: <https://www.ywhome.top>**

---

## Die Kernfähigkeit

**31 MCP-Konfigurationseinträge und 19 Skill-Ziele als eine einzige Inventur** — Cursor, VS Code, Claude Code, Gemini CLI, Codex CLI, Windsurf, Zed, TRAE (CN / SOLO / Plugin), Kiro, OpenCode, JetBrains-IDEs, Antigravity, OpenClaw, CodeBuddy, WorkBuddy, Qoder, ZCode, Cline, Qwen Code, iFlow CLI, LM Studio, OpenHands, GitHub Copilot CLI, Warp, Kimi Code CLI, Kilo Code, Goose und der Cloud-Speicher. Die Liste entsteht durch Scan auf Ihrem System; weitere Clients fügen Sie über Konfigurationspfad und Skill-Verzeichnis hinzu.

## Warum es sich lohnt

| Ihr Alltagsaufwand | Was AI-Tools liefert |
| --- | --- |
| Ein Server, sechs JSON-Dateien, sechs Schlüsselnamen | **Einmal schreiben, überall wirksam.** Die Konfiguration geht an alle gewählten Clients — jeweils in deren Dialekt: JSON / JSONC / TOML, `servers` statt `mcpServers`, `working_directory` statt `cwd`, `transport` statt `type`, `context_servers`, `mcp_servers`. |
| Store-Listen, die erst mal laden | **Erster Screen sofort.** Scheiben-Cache + SWR: zuerst das Bild, die Aktualisierung läuft still im Hintergrund (Listen 1 h, Details 24 h), Zwangsupdates per Klick. |
| „Macht mein Edit gerade den Client kaputt?" | **Jede Änderung ist rückholbar.** Installation, Deinstallation, Update, Sync und Edit werden automatisch gesichert; beliebigen Stand mit dem Ist-Zustand vergleichen (neu / entfernt / geändert, farblich) und mit einem Klick wiederherstellen. |
| MCP-Debugging mit curl und Texteditor | **Inspector eingebaut.** stdio / streamable-http / sse, Tools / Resources / Prompts aufrufen, Parameter im Formular, Ergebnis mit JSON-Highlighting, Log in verschiebbarem Panel. |
| Neuer Rechner, neue Einrichtung | **Ihre eigene Cloud, ein Klick zur Wiederherstellung.** Push auf Ihr eigenes Git (SSH-Key / HTTPS-Token / anonym) oder SFTP (Passwort / Key) mit Aufgaben-Warteschlange, Fortschritt und Retry — und explizitem Lokal-vs-Remote-Abgleich vor dem Überschreiben. |
| Ein Config-Manager, der nach Hause telefoniert? | **Lokal zuerst.** Ohne eingerichtete Cloud-Synchronisation geht nichts nach draußen; Cache AES-256-GCM-verschlüsselt, Zugangsdaten nur als verschlüsselte SecretStore-Referenzen, externe Links auf http/https beschränkt. |

## Kernfunktionen

- **MCP-Store** — Smithery, npm-Registry, Alibabas Bailian-Offline-Index (251 Einträge, ohne Netz), ModelScope und der offizielle Registry-Snapshot; Kategorien, echte Gesamtzahlen, serverseitige Paginierung.
- **Skills-Store** — kompatibel zur `~/.agents/skills/`-Konvention; Suche, sprachabhängige Kategorien, Sortierung, Quellenfilter, Paginierung. Clients ohne Skill-Unterstützung zeigen den Grund statt leerer `.source.json`-Hüllen.
- **Ein Klick, viele Clients** — Sammelinstallation, Deinstallation/Update pro Client, manueller Edit wird markiert und bleibt bei Store-Updates erhalten.
- **MCP-Inspector** — eigene Befehle, Argumente, Umgebungsvariablen und Header; Tools / Resources / Prompts direkt aufrufen; Kindprozesse werden beim Beenden eingesammelt.
- **Bibliothek** — alles Installierte an einem Ort: Befehl/Argumente/Env bearbeiten, mehrfach auswählen und synchronisieren, deinstallieren. Im Skills-Bereich SKILL.md online bearbeiten, Anhänge verwalten, `.zip` / `.skill` / Ordner / GitHub-Link / Drag-&-Drop importieren, mehrere als Zip exportieren, Konflikte vor dem Push klären.
- **Cloud-Synchronisation** — Git oder SFTP, automatischer Pull beim Start, manueller Push, Aufgabenpanel mit Fortschritt und Retry, Konsistenzprüfung beider Seiten.
- **Historie & Rückrollen** — Zeitstempel, Größe, betroffene Clients und Eintragszahlen; Versionsvergleich; Ein-Klick-Wiederherstellung; Historie komplett leeren.
- **Laufzeit-Prüfung** — Node.js, Python und Git erkennen (Vorhandensein, Version, Pfad) und erklären „installiert, startet aber nicht".
- **Quellen & API-Tokens** — eingebaute und direkt angebundene Plattformen (Base URL + Token) gemeinsam verwalten, Verbindungstest gegen echte Plattform-Endpunkte, an/aus, Standard, Export; Token-Center mit Scopes und Ablaufdatum.
- **Optik & 9 Sprachen** — hell / dunkel / System; English, 简体中文, العربية (RTL), Deutsch, Español, Français, Italiano, 日本語, Русский; Sprachpakete werden bei Bedarf geladen, Umschalten sofort.
- **Sicherheit** — AES-256-GCM-Cache mit maschinenabhängigem Schlüssel, http/https-only-Links in Systembrowser, DNS-over-HTTPS, Einzelinstanz-Sperre, strikt getrennte Haupt-/Preload-/Renderer-Prozesse mit IPC-Allow-List.

## Was ein Release enthält

| Artefakt | Plattform |
| --- | --- |
| `AI-Tools-Setup-<version>.exe` | Windows-Installer (NSIS, x64) |
| `AI-Tools-<version>-portable.exe` | Windows, portabel ohne Installation |
| `AI-Tools-<version>.dmg` / `-arm64.dmg` | macOS (Intel / Apple Silicon) |
| `AI-Tools-<version>-mac.zip` / `-arm64-mac.zip` | macOS-Archive |
| `AI-Tools-<version>.AppImage` / `-arm64.AppImage` | Linux AppImage |
| `ai-tools_<version>_amd64.deb` / `_arm64.deb` | Linux .deb |
| `latest.yml`, `portable.yml`, `latest-mac.yml`, `latest-linux.yml`, `latest-linux-arm64.yml` | Update-Manifeste |
| `*.blockmap` | Delta-Download-Blöcke |

Alle Anhänge sind anonym ladbar — ohne Token, ohne Login. Der Update-Feed, den die App liest, lautet beispielsweise:

```
https://github.com/qingchuang12/ai-tools-releases/releases/latest/download/latest.yml
```

Die Manifeste enthalten SHA-512 und Dateigröße; der Updater prüft, bevor er installiert.

## Download und Installation

Aktuell veröffentlichte Version: **1.1.1** (2026-11-02) — [Releases → neueste](https://github.com/qingchuang12/ai-tools-releases/releases/latest)

- Windows — [AI-Tools-Setup-1.1.1.exe](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-Setup-1.1.1.exe) · [portabel](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-portable.exe)
- macOS — [dmg (Intel)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.dmg) · [dmg (Apple Silicon)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-arm64.dmg)
- Linux — [AppImage (x64)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.AppImage) · [deb (amd64)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/ai-tools_1.1.1_amd64.deb)

Die Download-Seite der offiziellen Website ([www.ywhome.top/#product-ai-tools-download](https://www.ywhome.top/#product-ai-tools-download)) wird gerade plattformweise freigeschaltet; bis dahin ist dieses Repository der offizielle Bezugsweg.

Die Builds sind derzeit **nicht signiert**: Windows SmartScreen → „Weitere Informationen → Trotzdem ausführen"; macOS bei damaged-Meldung `xattr -cr /Applications/AI-Tools.app`; AppImage zuerst `chmod +x`.

## Automatische Aktualisierung

Installierte Ausgaben prüfen dieses Repository selbst und aktualisieren vor Ort. NSIS-Installationen folgen `latest.yml`, portable Ausgaben `portable.yml`, macOS `latest-mac.yml`, Linux `latest-linux.yml` / `latest-linux-arm64.yml`.

## Datenschutz und Daten

Lokal zuerst: AI-Tools liest und schreibt Konfigurationsdateien auf Ihrem Rechner und lädt nichts hoch, solange Sie keine Cloud-Synchronisation einrichten. Anwendungsdaten liegen in `~/.ai-tools/` (macOS / Linux) bzw. `%USERPROFILE%\.ai-tools\` (Windows); der Cache ist AES-256-GCM-verschlüsselt. AGB: <https://www.ywhome.top/legal/terms.html> · Datenschutz: <https://www.ywhome.top/legal/privacy.html>

## Schnellstart

1. Installieren und öffnen.
2. Im **MCP-Store** suchen (oder in den **Skills**-Tab wechseln).
3. **Installieren** klicken und Ziel-Clients wählen.
4. Im Client sofort verwenden — ohne JSON-Kauerei.
5. Bei Problemen im **Inspector** nachstellen, dann über die **Historie** zurückrollen.
6. Mehrere Rechner? **Einstellungen → Cloud-Sync** mit Git oder SFTP einrichten.

## Support

- Produktinfo, Funktionen und Clients: <https://www.ywhome.top>
- Fehlermeldungen und Wünsche: [Issues in diesem Repository](https://github.com/qingchuang12/ai-tools-releases/issues) oder **service@ywhome.top**

---

<p align="center">
  <sub>AI-Tools ist proprietäre Software · © 2026 AI-Tools Team · Anteile aus mcp-dock stehen unter der MIT-Lizenz (siehe mitgelieferte <code>THIRD_PARTY_LICENSES.md</code>).</sub><br>
  <sub><a href="https://www.ywhome.top">www.ywhome.top</a> · <a href="https://www.ywhome.top/legal/terms.html">AGB</a> · <a href="https://www.ywhome.top/legal/privacy.html">Datenschutz</a> · <a href="mailto:service@ywhome.top">service@ywhome.top</a></sub>
</p>

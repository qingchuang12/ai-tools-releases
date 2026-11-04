# AI-Tools (Italiano)

**Un unico pannello per tutta la tua catena di strumenti IA.** AI-Tools raccoglie in una app desktop i server MCP e le Agent Skills sparsi nelle configurazioni di ogni client di programmazione IA: sfogliare, installare, modificare, debuggare, ripristinare e sincronizzare, senza più toccare un JSON a mano.

<p align="center">
  <a href="https://www.ywhome.top">Sito ufficiale</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/releases/latest">Download</a> ·
  <a href="https://www.ywhome.top/#product-ai-tools-pricing">Licenza e prezzi</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/issues">Segnalazioni</a>
</p>

<p align="center">
  <a href="./README.md">English</a> ·
  <a href="./README.zh.md">简体中文</a> ·
  <a href="./README.ar.md">العربية</a> ·
  <a href="./README.de.md">Deutsch</a> ·
  <a href="./README.es.md">Español</a> ·
  <a href="./README.fr.md">Français</a> ·
  <strong>Italiano</strong> ·
  <a href="./README.ja.md">日本語</a> ·
  <a href="./README.ru.md">Русский</a>
</p>

> **Questo repository** è il canale ufficiale dei rilasci di AI-Tools: installer per Windows / macOS / Linux e i manifesti che l'app legge per aggiornarsi da sola. Non contiene codice sorgente.
> **Guida alle funzioni e client supportati: <https://www.ywhome.top>**

---

## La capacità, in una riga

**31 voci di configurazione MCP e 19 destinazioni di skills gestite come un unico inventario** — Cursor, VS Code, Claude Code, Gemini CLI, Codex CLI, Windsurf, Zed, TRAE (CN / SOLO / plugin), Kiro, OpenCode, IDE JetBrains, Antigravity, OpenClaw, CodeBuddy, WorkBuddy, Qoder, ZCode, Cline, Qwen Code, iFlow CLI, LM Studio, OpenHands, GitHub Copilot CLI, Warp, Kimi Code CLI, Kilo Code, Goose e la voce di archiviazione cloud. L'elenco nasce dalla rilevazione dei client presenti sulla tua macchina; ogni client mancante si aggiunge indicando il percorso di configurazione e la cartella delle skills.

## Perché conviene

| L'attrito di ogni giorno | Cosa ti dà AI-Tools |
| --- | --- |
| Un server, sei JSON, sei nomi di chiave | **Scrivi una volta, distribuisci ovunque.** La configurazione parte ai client scelti nel dialetto di ciascuno: JSON / JSONC / TOML, `servers` invece di `mcpServers`, `working_directory` invece di `cwd`, `transport` invece di `type`, `context_servers`, `mcp_servers`. |
| Liste dello store che girano | **Prima schermata istantanea.** Cache su disco + SWR: prima si vede, poi si aggiorna in silenzio (liste 1 h, dettagli 24 h), con refresh forzato quando serve. |
| «La mia modifica ha rotto il client?» | **Tutto è reversibile.** Installazioni, disinstallazioni, aggiornamenti, sincronizzazioni e modifiche vengono salvati; confronta uno snapshot con lo stato attuale (aggiunto / rimosso / modificato, a colori) e ripristina con un clic. |
| Debuggare un server MCP con curl | **Inspector integrato.** stdio / streamable-http / sse, chiamata di Tools / Resources / Prompts da form, risultato con evidenziazione JSON e log in pannello ridimensionabile. |
| Rifare tutto su un'altra macchina | **Il tuo cloud, ripristino in un clic.** Push verso il tuo Git (chiave SSH / token HTTPS / anonimo) o il tuo SFTP (password / chiave), con coda di attività, progresso e retry, e confronto esplicito locale-contro-remoto prima della sovrascrittura. |
| Un gestore di configurazioni che telefona a casa | **Local-first.** Nulla esce dalla macchina finché non configuri la sincronizzazione; cache AES-256-GCM, credenziali solo come riferimenti cifrati SecretStore, link esterni limitati a http/https. |

## Funzioni principali

- **Store MCP** — Smithery, registro npm, indice offline di Alibaba Bailian (251 voci, senza rete), ModelScope e snapshot del registro ufficiale; categorie, totali reali e paginazione lato server.
- **Store Skills** — conforme alla convenzione `~/.agents/skills/`; ricerca, categorie che seguono la lingua dell'interfaccia, ordinamento, filtri per fonte e paginazione. Sui client che non accettano skills il pulsante è disabilitato *con il motivo*, mai con directory vuote `.source.json`.
- **Distribuzione con un clic** — installazione su più client insieme, disinstallazione o aggiornamento per client, e marcatura delle modifiche manuali perché un aggiornamento dello store non le sovrascriva.
- **MCP Inspector** — comando, argomenti, variabili d'ambiente e header personalizzabili; scoperta di Tools / Resources / Prompts; processi figli ripuliti alla chiusura.
- **Libreria** — tutto ciò che è installato in un unico elenco: modifica comando / argomenti / env, selezione multipla e sincronizzazione, disinstallazione. Lato skills: modifica online di SKILL.md, gestione dei file allegati, importazione da `.zip` / `.skill` / cartella / link GitHub / trascinamento, export in zip multiplo e risoluzione dei conflitti prima del push.
- **Sincronizzazione cloud** — Git o SFTP, pull automatico all'avvio, push manuale, pannello attività con progresso e retry, verifica di coerenza tra i due lati.
- **Cronologia e ripristino** — data, dimensione, client coinvolti e numero di voci; diff tra versioni; ripristino con un clic; azzeramento completo.
- **Sonde di runtime** — rilevamento di Node.js, Python e Git (presenza, versione, percorso) per spiegare «installato ma non parte».
- **Fonti e token API** — fonti integrate e connessioni dirette alle piattaforme (URL base + token) gestite insieme, test di connessione sugli endpoint reali, abilitazione, predefinita ed export; centro token con ambiti e scadenza.
- **Aspetto e 9 lingue** — chiaro / scuro / sistema; English, 简体中文, العربية (RTL), Deutsch, Español, Français, Italiano, 日本語, Русский; pacchetti caricati su richiesta e cambio istantaneo.
- **Sicurezza** — cache AES-256-GCM con chiave derivata dalla macchina, link esterni solo http/https aperti nel browser, DNS-over-HTTPS, lock a istanza singola e isolamento rigoroso main / preload / renderer con allow-list IPC.

## Cosa contiene un rilascio

| Artefatto | Piattaforma |
| --- | --- |
| `AI-Tools-Setup-<version>.exe` | Installer Windows (NSIS, x64) |
| `AI-Tools-<version>-portable.exe` | Windows portable, senza installazione |
| `AI-Tools-<version>.dmg` / `-arm64.dmg` | macOS (Intel / Apple silicon) |
| `AI-Tools-<version>-mac.zip` / `-arm64-mac.zip` | Archivi macOS |
| `AI-Tools-<version>.AppImage` / `-arm64.AppImage` | Linux AppImage |
| `ai-tools_<version>_amd64.deb` / `_arm64.deb` | Linux .deb |
| `latest.yml`, `portable.yml`, `latest-mac.yml`, `latest-linux.yml`, `latest-linux-arm64.yml` | Manifesti di aggiornamento |
| `*.blockmap` | Blocchi di download differenziale |

Tutti gli asset sono scaricabili in forma anonima, senza token né login. Il feed letto dall'app è, ad esempio:

```
https://github.com/qingchuang12/ai-tools-releases/releases/latest/download/latest.yml
```

I manifesti contengono SHA-512 e dimensione; l'updater verifica prima di installare.

## Download e installazione

Ultima versione pubblicata: **1.1.1** (2026-11-02) — [Releases → più recente](https://github.com/qingchuang12/ai-tools-releases/releases/latest)

- Windows — [AI-Tools-Setup-1.1.1.exe](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-Setup-1.1.1.exe) · [portable](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-portable.exe)
- macOS — [dmg (Intel)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.dmg) · [dmg (Apple silicon)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-arm64.dmg)
- Linux — [AppImage (x64)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.AppImage) · [deb (amd64)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/ai-tools_1.1.1_amd64.deb)

La pagina di download del sito ufficiale ([www.ywhome.top/#product-ai-tools-download](https://www.ywhome.top/#product-ai-tools-download)) si sta aprendo piattaforma per piattaforma; nel frattempo questo repository è il canale valido.

Le build non sono ancora **firmate**: su Windows SmartScreen → «Ulteriori informazioni → Esegui comunque»; su macOS, se l'app risulta danneggiata, `xattr -cr /Applications/AI-Tools.app`; su AppImage prima `chmod +x`.

## Aggiornamento automatico

Le installazioni verificano da sole questo repository e si aggiornano in loco. Le NSIS seguono `latest.yml`, le portable `portable.yml`, macOS `latest-mac.yml`, Linux `latest-linux.yml` / `latest-linux-arm64.yml`.

## Privacy e dati

Local-first: AI-Tools legge e scrive i file di configurazione sulla tua macchina e non carica nulla finché non configuri la sincronizzazione. I dati risiedono in `~/.ai-tools/` (macOS / Linux) o `%USERPROFILE%\.ai-tools\` (Windows), con cache cifrata AES-256-GCM. Termini: <https://www.ywhome.top/legal/terms.html> · Privacy: <https://www.ywhome.top/legal/privacy.html>

## Per iniziare

1. Installa e apri AI-Tools.
2. Cerca nello **store MCP** (o nella scheda **Skills**).
3. Clicca **Installa** e scegli i client di destinazione.
4. Usa la capacità nel client, senza copiare e incollare JSON.
5. Problemi? Riproduci nell'**Inspector** e ripristina dalla **Cronologia**.
6. Più macchine? Configura Git o SFTP in **Impostazioni → Sincronizzazione cloud**.

## Supporto

- Informazioni sul prodotto, funzioni, client e prezzi: <https://www.ywhome.top>
- Bug e richieste: [apri una issue qui](https://github.com/qingchuang12/ai-tools-releases/issues) o scrivi a **service@ywhome.top**

---

<p align="center">
  <sub>AI-Tools è software proprietario · © 2026 AI-Tools Team · Le parti derivate da mcp-dock restano sotto licenza MIT (vedi <code>THIRD_PARTY_LICENSES.md</code> incluso nell'app).</sub><br>
  <sub><a href="https://www.ywhome.top">www.ywhome.top</a> · <a href="https://www.ywhome.top/legal/terms.html">Termini</a> · <a href="https://www.ywhome.top/legal/privacy.html">Privacy</a> · <a href="mailto:service@ywhome.top">service@ywhome.top</a></sub>
</p>

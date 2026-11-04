# AI-Tools (Français)

**Un seul panneau pour toute votre chaîne d'outils IA.** AI-Tools réunit, dans une application de bureau, les serveurs MCP et les Agent Skills dispersés dans la configuration de chaque client de codage IA : parcourir, installer, éditer, déboguer, revenir en arrière et synchroniser — sans jamais retoucher un JSON à la main.

<p align="center">
  <a href="https://www.ywhome.top">Site officiel</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/releases/latest">Téléchargement</a> ·
  <a href="https://www.ywhome.top/#product-ai-tools-pricing">Licence &amp; tarifs</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/issues">Signaler un problème</a>
</p>

<p align="center">
  <a href="./README.md">English</a> ·
  <a href="./README.zh.md">简体中文</a> ·
  <a href="./README.ar.md">العربية</a> ·
  <a href="./README.de.md">Deutsch</a> ·
  <a href="./README.es.md">Español</a> ·
  <strong>Français</strong> ·
  <a href="./README.it.md">Italiano</a> ·
  <a href="./README.ja.md">日本語</a> ·
  <a href="./README.ru.md">Русский</a>
</p>

> **Ce dépôt** est la source officielle des livrables AI-Tools : installateurs Windows / macOS / Linux et manifestes de mise à jour lus par l'application. Il ne contient pas de code source.
> **Présentation des fonctions et clients pris en charge : <https://www.ywhome.top>**

---

## La capacité en un mot

**31 entrées de configuration MCP et 19 cibles de skills gérées comme un seul inventaire** — Cursor, VS Code, Claude Code, Gemini CLI, Codex CLI, Windsurf, Zed, TRAE (CN / SOLO / plugin), Kiro, OpenCode, les IDE JetBrains, Antigravity, OpenClaw, CodeBuddy, WorkBuddy, Qoder, ZCode, Cline, Qwen Code, iFlow CLI, LM Studio, OpenHands, GitHub Copilot CLI, Warp, Kimi Code CLI, Kilo Code, Goose et l'entrée cloud. La liste est issue de la détection sur votre machine ; tout client absent s'ajoute en indiquant son chemin de configuration et son dossier de skills.

## Pourquoi ça change la journée

| La friction quotidienne | Ce qu'AI-Tools apporte |
| --- | --- |
| Un serveur, six fichiers JSON, six noms de clés | **Écrire une fois, déployer partout.** La configuration part vers chaque client choisi, dans son propre dialecte : JSON / JSONC / TOML, `servers` plutôt que `mcpServers`, `working_directory` plutôt que `cwd`, `transport` plutôt que `type`, `context_servers`, `mcp_servers`. |
| Les listes du store qui tournent | **Premier écran instantané.** Cache disque + SWR : l'affichage arrive avant le réseau, l'actualisation se fait en silence (listes 1 h, détails 24 h), avec rafraîchissement forcé à la demande. |
| « Est-ce que mon édition vient de casser le client ? » | **Tout est réversible.** Installations, désinstallations, mises à jour, synchronisations et éditions sont sauvegardées ; comparez n'importe quel instantané à l'état courant (ajouté / supprimé / modifié, en couleurs) et restaurez en un clic. |
| Déboguer un serveur MCP à coups de curl | **Inspecteur intégré.** stdio / streamable-http / sse, appel des Tools / Resources / Prompts depuis un formulaire, résultat en JSON coloré, journal dans un panneau redimensionnable. |
| Tout reconstruire sur une nouvelle machine | **Votre propre cloud, restauration en un clic.** Push vers votre dépôt Git (clé SSH / jeton HTTPS / anonyme) ou votre SFTP (mot de passe / clé), avec file de tâches, progression et reprise, et comparaison explicite local-vers-remote avant écrasement. |
| Un gestionnaire de configuration qui téléphone ? | **Local d'abord.** Rien ne sort tant que vous n'avez pas configuré la synchronisation ; cache chiffré AES-256-GCM, identifiants conservés uniquement comme références chiffrées SecretStore, liens externes limités à http/https. |

## Fonctions clés

- **Store MCP** — Smithery, registre npm, index hors ligne Alibaba Bailian (251 entrées, sans réseau), ModelScope et instantané du registre officiel ; catégories, totaux réels, pagination côté serveur.
- **Store Skills** — conforme à la convention `~/.agents/skills/` ; recherche, catégories suivant la langue de l'interface, tri, filtres par source, pagination. Sur les clients qui ne peuvent pas recevoir de skills, le bouton est désactivé *avec la raison*, jamais de dossier coquille `.source.json`.
- **Déploiement en un clic** — installation multi-clients, désinstallation ou mise à jour par client, édition manuelle signalée pour ne pas être écrasée par une mise à jour du store.
- **Inspecteur MCP** — commande, arguments, variables d'environnement et en-têtes personnalisables ; découverte des Tools / Resources / Prompts ; sous-processus nettoyés à la fermeture.
- **Bibliothèque** — tout ce qui est installé au même endroit : édition commande/arguments/env, sélection multiple et synchronisation, désinstallation. Côté skills : édition en ligne du SKILL.md, gestion des fichiers joints, import `.zip` / `.skill` / dossier / lien GitHub / glisser-déposer, export groupé en zip, résolution des conflits avant push cloud.
- **Synchronisation cloud** — Git ou SFTP, tirage automatique au démarrage, push manuel, panneau de tâches avec progression et reprise, contrôle de cohérence des deux côtés.
- **Historique et retour en arrière** — horodatage, taille, clients concernés et nombre d'entrées ; diff entre versions ; restauration en un clic ; purge de l'historique.
- **Sondes d'exécution** — détection Node.js, Python et Git (présence, version, chemin) pour expliquer « installé mais ne démarre pas ».
- **Sources et jetons d'API** — sources intégrées et connexes directes gérées ensemble (URL de base + jeton), test de connexion sur les vrais endpoints de plateforme, activation, défaut, export ; centre de jetons avec portées et expiration.
- **Apparence et 9 langues** — clair / sombre / système ; English, 简体中文, العربية (RTL complet), Deutsch, Español, Français, Italiano, 日本語, Русский ; chargement à la demande, bascule immédiate.
- **Sécurité** — cache AES-256-GCM dérivé de la machine, liens externes http/https ouverts dans le navigateur, DNS-over-HTTPS, verrou mono-instance, isolation stricte main / preload / renderer avec liste blanche IPC.

## Ce qu'il y a dans une version

| Livrable | Plateforme |
| --- | --- |
| `AI-Tools-Setup-<version>.exe` | Installeur Windows (NSIS, x64) |
| `AI-Tools-<version>-portable.exe` | Windows portable, sans installation |
| `AI-Tools-<version>.dmg` / `-arm64.dmg` | macOS (Intel / Apple silicon) |
| `AI-Tools-<version>-mac.zip` / `-arm64-mac.zip` | Archives macOS |
| `AI-Tools-<version>.AppImage` / `-arm64.AppImage` | Linux AppImage |
| `ai-tools_<version>_amd64.deb` / `_arm64.deb` | Linux .deb |
| `latest.yml`, `portable.yml`, `latest-mac.yml`, `latest-linux.yml`, `latest-linux-arm64.yml` | Manifestes de mise à jour |
| `*.blockmap` | Blocs de téléchargement différentiel |

Tous les fichiers sont téléchargeables anonymement — sans jeton ni connexion. Le flux d'automatisme lu par l'application, par exemple :

```
https://github.com/qingchuang12/ai-tools-releases/releases/latest/download/latest.yml
```

Les manifestes portent le SHA-512 et la taille ; l'updater vérifie avant d'installer.

## Téléchargement et installation

Dernière version publiée : **1.1.1** (2026-11-02) — [Releases → dernière](https://github.com/qingchuang12/ai-tools-releases/releases/latest)

- Windows — [AI-Tools-Setup-1.1.1.exe](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-Setup-1.1.1.exe) · [portable](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-portable.exe)
- macOS — [dmg (Intel)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.dmg) · [dmg (Apple silicon)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-arm64.dmg)
- Linux — [AppImage (x64)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.AppImage) · [deb (amd64)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/ai-tools_1.1.1_amd64.deb)

La page de téléchargement du site officiel ([www.ywhome.top/#product-ai-tools-download](https://www.ywhome.top/#product-ai-tools-download)) s'ouvre plateforme par plateforme ; en attendant, ce dépôt reste le canal officiel.

Les builds ne sont **pas encore signés** : SmartScreen Windows → « Plus d'informations → Exécuter quand même » ; sur macOS si l'app est annoncée endommagée, `xattr -cr /Applications/AI-Tools.app` ; AppImage, faire `chmod +x` d'abord.

## Mise à jour automatique

Les installations vérifient ce dépôt seules et se mettent à jour en place. Les installs NSIS suivent `latest.yml`, les portables `portable.yml`, macOS `latest-mac.yml`, Linux `latest-linux.yml` / `latest-linux-arm64.yml`.

## Confidentialité et données

Local-first : AI-Tools lit et écrit les fichiers de configuration sur votre machine et ne téléverse rien tant que vous n'avez pas configuré la synchronisation. Les données vivent dans `~/.ai-tools/` (macOS / Linux) ou `%USERPROFILE%\.ai-tools\` (Windows) ; le cache est chiffré AES-256-GCM. Conditions : <https://www.ywhome.top/legal/terms.html> · Confidentialité : <https://www.ywhome.top/legal/privacy.html>

## Démarrage

1. Installez et ouvrez AI-Tools.
2. Cherchez dans le **store MCP** (ou l'onglet **Skills**).
3. Cliquez **Installer** et choisissez les clients cibles.
4. Utilisez la capacité dans le client — sans copier-coller de JSON.
5. Un souci ? Reproduisez-le dans l'**Inspecteur**, puis revenez en arrière via l'**Historique**.
6. Plusieurs machines ? Configurez Git ou SFTP dans **Paramètres → Synchronisation cloud**.

## Assistance

- Informations produit, fonctions et clients : <https://www.ywhome.top>
- Anomalies et demandes : [ouvrir une issue ici](https://github.com/qingchuang12/ai-tools-releases/issues) ou écrire à **service@ywhome.top**

---

<p align="center">
  <sub>AI-Tools est un logiciel propriétaire · © 2026 AI-Tools Team · Les parties issues de mcp-dock restent sous licence MIT (voir <code>THIRD_PARTY_LICENSES.md</code> livré avec l'application).</sub><br>
  <sub><a href="https://www.ywhome.top">www.ywhome.top</a> · <a href="https://www.ywhome.top/legal/terms.html">Conditions</a> · <a href="https://www.ywhome.top/legal/privacy.html">Confidentialité</a> · <a href="mailto:service@ywhome.top">service@ywhome.top</a></sub>
</p>

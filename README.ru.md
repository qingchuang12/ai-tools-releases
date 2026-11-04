# AI-Tools (Русский)

**Одна панель для всей вашей цепочки ИИ-инструментов.** AI-Tools собирает MCP-серверы и Agent Skills из конфигураций всех ИИ-редакторов в одно десктоп-приложение: поиск, установка, правка, отладка, откат и синхронизация — без ручной работы с JSON.

<p align="center">
  <a href="https://www.ywhome.top">Официальный сайт</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/releases/latest">Загрузки</a> ·
  <a href="https://www.ywhome.top/#product-ai-tools-pricing">Лицензия и цены</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/issues">Сообщения об ошибках</a>
</p>

<p align="center">
  <a href="./README.md">English</a> ·
  <a href="./README.zh.md">简体中文</a> ·
  <a href="./README.ar.md">العربية</a> ·
  <a href="./README.de.md">Deutsch</a> ·
  <a href="./README.es.md">Español</a> ·
  <a href="./README.fr.md">Français</a> ·
  <a href="./README.it.md">Italiano</a> ·
  <a href="./README.ja.md">日本語</a> ·
  <strong>Русский</strong>
</p>

> **Этот репозиторий** — официальный канал поставки AI-Tools: установщики для Windows / macOS / Linux и манифесты, из которых приложение обновляется само. Исходный код здесь не публикуется.
> **Обзор возможностей и список поддерживаемых клиентов: <https://www.ywhome.top>**

---

## Суть возможности

**31 конфигурационный вход MCP и 19 целей для скиллов ведутся как один реестр** — Cursor, VS Code, Claude Code, Gemini CLI, Codex CLI, Windsurf, Zed, TRAE (CN / SOLO / плагин), Kiro, OpenCode, IDE JetBrains, Antigravity, OpenClaw, CodeBuddy, WorkBuddy, Qoder, ZCode, Cline, Qwen Code, iFlow CLI, LM Studio, OpenHands, GitHub Copilot CLI, Warp, Kimi Code CLI, Kilo Code, Goose и облачное хранилище. Список строится по фактическому сканированию системы; отсутствующий клиент добавляется указанием пути к конфигурации и папки скиллов.

## Почему это удобно

| Повседневная рутина | Что даёт AI-Tools |
| --- | --- |
| Один сервер, шесть JSON, шесть имён ключей | **Одна правка — развёртывание везде.** Конфигурация расходится по выбранным клиентам на их собственном диалекте: JSON / JSONC / TOML, `servers` вместо `mcpServers`, `working_directory` вместо `cwd`, `transport` вместо `type`, `context_servers`, `mcp_servers`. |
| Магазин долго грузится | **Первый экран мгновенно.** Дисковый кэш + SWR: сначала интерфейс, обновление идёт в фоне (списки 1 ч, детали 24 ч), принудительное обновление — одной кнопкой. |
| «Не сломала ли правка клиент?» | **Всё обратимо.** Установки, удаления, обновления, синхронизации и правки сохраняются автоматически; сравнивайте любой снимок с текущим состоянием (добавлено / удалено / изменено, цветами) и возвращайте в один клик. |
| Отладка MCP через curl | **Встроенный Inspector.** stdio / streamable-http / sse, вызов Tools / Resources / Prompts из формы, подсвеченный JSON и логи в перетаскиваемой панели. |
| Настройка с нуля на новой машине | **Ваше собственное облако, восстановление в один клик.** Отправка в ваш Git (SSH-ключ / HTTPS-токен / анонимно) или SFTP (пароль / ключ) с очередью задач, прогрессом и повтором и явным сравнением локального и удалённого перед перезаписью. |
| Менеджер конфигов, который что-то отправляет? | **Локальный режим по умолчанию.** Пока синхронизация не настроена, ничего не уходит; кэш шифруется AES-256-GCM, учётные данные хранятся только как зашифрованные ссылки SecretStore, внешние ссылки ограничены http/https. |

## Ключевые функции

- **Магазин MCP** — Smithery, реестр npm, автономный индекс Alibaba Bailian (251 запись, без сети), ModelScope и снимок официального реестра; категории, реальные счётчики и серверная пагинация.
- **Магазин скиллов** — соответствие соглашению `~/.agents/skills/`; поиск, категории на языке интерфейса, сортировка, фильтры по источникам, пагинация. На клиентах без поддержки скиллов кнопка отключена *с пояснением*, пустых каталогов `.source.json` не создаётся.
- **Развёртывание в один клик** — установка сразу в несколько клиентов, удаление или обновление по каждому клиенту, пометка ручных правок, чтобы обновление магазина их не затирало.
- **MCP Inspector** — своя команда, аргументы, переменные окружения и заголовки; обнаружение Tools / Resources / Prompts; дочерние процессы убираются при закрытии.
- **Библиотека** — всё установленное в одном списке: правка команды / аргументов / окружения, пакетный выбор и синхронизация, удаление. Вкладка скиллов: онлайн-редактирование SKILL.md, управление вложенными файлами, импорт `.zip` / `.skill` / папки / ссылки GitHub / перетаскиванием, пакетный экспорт в zip и разрешение конфликтов перед отправкой.
- **Облачная синхронизация** — Git или SFTP, автозагрузка при запуске, ручная отправка, панель задач с прогрессом и повтором, проверка согласованности двух сторон.
- **История и откат** — время, размер, затронутые клиенты и число записей; сравнение версий; восстановление в один клик; полная очистка истории.
- **Проверка окружения** — определение Node.js, Python и Git (наличие, версия, путь) для ответа на «установлено, но не запускается».
- **Источники и API-токены** — встроенные источники и прямые подключения платформ (базовый URL + токен) в одном месте, проверка соединения по реальным эндпоинтам платформы, включение, по умолчанию и экспорт; центр токенов с областями и сроком действия.
- **Оформление и 9 языков** — светлая / тёмная / системная тема; English, 简体中文, العربية (RTL), Deutsch, Español, Français, Italiano, 日本語, Русский; языковые пакеты подгружаются по требованию, переключение мгновенное.
- **Безопасность** — кэш AES-256-GCM с ключом из характеристик машины, внешние ссылки только http/https в системном браузере, DNS-over-HTTPS, блокировка второго экземпляра и строгая изоляция main / preload / renderer со списком разрешённых IPC.

## Что входит в релиз

| Артефакт | Платформа |
| --- | --- |
| `AI-Tools-Setup-<version>.exe` | Установщик Windows (NSIS, x64) |
| `AI-Tools-<version>-portable.exe` | Portable-версия Windows без установки |
| `AI-Tools-<version>.dmg` / `-arm64.dmg` | macOS (Intel / Apple silicon) |
| `AI-Tools-<version>-mac.zip` / `-arm64-mac.zip` | Архивы macOS |
| `AI-Tools-<version>.AppImage` / `-arm64.AppImage` | Linux AppImage |
| `ai-tools_<version>_amd64.deb` / `_arm64.deb` | Linux .deb |
| `latest.yml`, `portable.yml`, `latest-mac.yml`, `latest-linux.yml`, `latest-linux-arm64.yml` | Манифесты обновления |
| `*.blockmap` | Блоки дифференциальной загрузки |

Все вложения доступны анонимно — без токена и входа. Лента обновлений, которую читает приложение, например:

```
https://github.com/qingchuang12/ai-tools-releases/releases/latest/download/latest.yml
```

Манифесты содержат SHA-512 и размер файла; установщик проверяет их перед установкой.

## Загрузка и установка

Последний опубликованный выпуск: **1.1.1** (2026-11-02) — [Releases → последний](https://github.com/qingchuang12/ai-tools-releases/releases/latest)

- Windows — [AI-Tools-Setup-1.1.1.exe](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-Setup-1.1.1.exe) · [portable](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-portable.exe)
- macOS — [dmg (Intel)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.dmg) · [dmg (Apple silicon)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-arm64.dmg)
- Linux — [AppImage (x64)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.AppImage) · [deb (amd64)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/ai-tools_1.1.1_amd64.deb)

Страница загрузок на официальном сайте ([www.ywhome.top/#product-ai-tools-download](https://www.ywhome.top/#product-ai-tools-download)) открывается платформа за платформой; до этого рабочие загрузки — здесь.

Сборки пока **без цифровой подписи**: в Windows на SmartScreen выберите «Подробнее → Выполнить в любом случае»; на macOS при сообщении о повреждении выполните `xattr -cr /Applications/AI-Tools.app`; для AppImage сначала `chmod +x`.

## Автоматическое обновление

Установленные версии сами проверяют этот репозиторий и обновляются на месте. NSIS-установки читают `latest.yml`, portable — `portable.yml`, macOS — `latest-mac.yml`, Linux — `latest-linux.yml` / `latest-linux-arm64.yml`.

## Конфиденциальность и данные

Локальный режим: AI-Tools читает и пишет файлы конфигурации на вашей машине и ничего не отправляет, пока вы не настроите синхронизацию. Данные лежат в `~/.ai-tools/` (macOS / Linux) или `%USERPROFILE%\.ai-tools\` (Windows), кэш зашифрован AES-256-GCM. Условия: <https://www.ywhome.top/legal/terms.html> · Конфиденциальность: <https://www.ywhome.top/legal/privacy.html>

## Быстрый старт

1. Установите и откройте AI-Tools.
2. Найдите нужное в **магазине MCP** (или на вкладке **Skills**).
3. Нажмите **Установить** и выберите клиентов.
4. Пользуйтесь возможностью в клиенте — без копирования JSON.
5. Проблема? Воспроизведите в **Inspector** и откатитесь через **Историю**.
6. Несколько машин? Настройте Git или SFTP в **Параметры → Облачная синхронизация**.

## Поддержка

- О продукте, функциях, клиентах и ценах: <https://www.ywhome.top>
- Об ошибках и пожеланиях: [создайте issue здесь](https://github.com/qingchuang12/ai-tools-releases/issues) или напишите на **service@ywhome.top**

---

<p align="center">
  <sub>AI-Tools — проприетарное ПО · © 2026 AI-Tools Team · части из mcp-dock остаются под лицензией MIT (см. <code>THIRD_PARTY_LICENSES.md</code> в составе приложения).</sub><br>
  <sub><a href="https://www.ywhome.top">www.ywhome.top</a> · <a href="https://www.ywhome.top/legal/terms.html">Условия</a> · <a href="https://www.ywhome.top/legal/privacy.html">Конфиденциальность</a> · <a href="mailto:service@ywhome.top">service@ywhome.top</a></sub>
</p>

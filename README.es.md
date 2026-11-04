# AI-Tools (Español)

**Un solo panel para toda tu cadena de herramientas de IA.** AI-Tools reúne en una aplicación de escritorio los servidores MCP y las Agent Skills repartidos por la configuración de cada cliente de programación con IA: explorar, instalar, editar, depurar, revertir y sincronizar, sin volver a tocar un JSON a mano.

<p align="center">
  <a href="https://www.ywhome.top">Sitio oficial</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/releases/latest">Descargas</a> ·
  <a href="https://www.ywhome.top/#product-ai-tools-pricing">Licencia y precios</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/issues">Avisos de errores</a>
</p>

<p align="center">
  <a href="./README.md">English</a> ·
  <a href="./README.zh.md">简体中文</a> ·
  <a href="./README.ar.md">العربية</a> ·
  <a href="./README.de.md">Deutsch</a> ·
  <strong>Español</strong> ·
  <a href="./README.fr.md">Français</a> ·
  <a href="./README.it.md">Italiano</a> ·
  <a href="./README.ja.md">日本語</a> ·
  <a href="./README.ru.md">Русский</a>
</p>

> **Este repositorio** es el canal oficial de publicación de AI-Tools: instaladores para Windows / macOS / Linux y los manifiestos que la aplicación lee para actualizarse sola. No contiene código fuente.
> **Recorrido de funciones y clientes compatibles: <https://www.ywhome.top>**

---

## La capacidad, en una frase

**31 entradas de configuración MCP y 19 destinos de skills gestionados como un único inventario** — Cursor, VS Code, Claude Code, Gemini CLI, Codex CLI, Windsurf, Zed, TRAE (CN / SOLO / plugin), Kiro, OpenCode, IDEs de JetBrains, Antigravity, OpenClaw, CodeBuddy, WorkBuddy, Qoder, ZCode, Cline, Qwen Code, iFlow CLI, LM Studio, OpenHands, GitHub Copilot CLI, Warp, Kimi Code CLI, Kilo Code, Goose y la entrada de almacenamiento en la nube. La lista sale de detectar lo que hay en tu máquina; cualquier cliente adicional se añade señalando su ruta de configuración y su carpeta de skills.

## Por qué merece la pena

| La fricción de cada día | Lo que te da AI-Tools |
| --- | --- |
| Un servidor, seis JSON, seis nombres de clave | **Escribe una vez, despliega en todas.** La configuración se reparte a los clientes elegidos hablando el dialecto de cada uno: JSON / JSONC / TOML, `servers` en vez de `mcpServers`, `working_directory` en vez de `cwd`, `transport` en vez de `type`, `context_servers`, `mcp_servers`. |
| Listas de la tienda que no cargan | **Primera pantalla instantánea.** Caché en disco + SWR: primero se ve, luego se refresca en silencio (listas 1 h, detalle 24 h), con refuerzo forzado cuando lo pidas. |
| «¿Mi último cambio rompió el cliente?» | **Todo es reversible.** Instalaciones, desinstalaciones, actualizaciones, sincronizaciones y ediciones se respaldan solas; compara cualquier versión con el estado actual (añadido / eliminado / modificado, en color) y restaura con un clic. |
| Depurar un servidor MCP con curl | **Inspector integrado.** stdio / streamable-http / sse, llamar Tools / Resources / Prompts desde un formulario, resultado con resaltado JSON y registro en panel redimensionable. |
| Rehacer toda la configuración en otra máquina | **Tu propia nube, restaurar en un clic.** Envía a tu repositorio Git (clave SSH / token HTTPS / anónimo) o a tu SFTP (contraseña / clave) con cola de tareas, progreso y reintento, y una comparación explícita local-contra-remoto antes de sobrescribir. |
| Un gestor de configuración que telefonea a casa | **Local por defecto.** Nada sale del equipo hasta que configuras la sincronización; caché cifrada AES-256-GCM, credenciales guardadas solo como referencias cifradas SecretStore y enlaces externos limitados a http/https. |

## Funciones principales

- **Tienda MCP** — Smithery, registro npm, índice sin conexión de Alibaba Bailian (251 entradas, sin red), ModelScope y la instantánea del registro oficial; categorías, totales reales y paginación en servidor.
- **Tienda de Skills** — compatible con la convención `~/.agents/skills/`; búsqueda, categorías que siguen el idioma de la interfaz, orden, filtros por fuente y paginación. En clientes que no admiten skills el botón aparece deshabilitado *con el motivo*, nunca con directorios vacíos `.source.json`.
- **Despliegue en un clic** — instalación simultánea en varios clientes, desinstalación o actualización por cliente y marcado de ediciones manuales para que una actualización de la tienda no las pise.
- **Inspector MCP** — comando, argumentos, variables de entorno y cabeceras a medida; descubrimiento de Tools / Resources / Prompts; procesos hijos recogidos al cerrar la aplicación.
- **Biblioteca** — todo lo instalado en un listado: editar comando / argumentos / entorno, selección múltiple y sincronización, desinstalar. En skills: edición en línea del SKILL.md, gestión de archivos adjuntos, importación de `.zip` / `.skill` / carpeta / enlace GitHub / arrastrar y soltar, exportación agrupada en zip y resolución de conflictos antes de subir.
- **Sincronización en la nube** — Git o SFTP, descarga automática al arrancar, push manual, panel de tareas con progreso y reintento, y comprobación de coherencia entre ambos lados.
- **Historial y reversión** — hora, tamaño, clientes implicados y número de entradas; diff entre versiones; restauración con un clic; borrado completo del historial.
- **Sondas de entorno** — detección de Node.js, Python y Git (presencia, versión, ruta) para responder a «instalado pero no arranca».
- **Fuentes y tokens de API** — fuentes integradas y conexiones directas a plataformas (URL base + token) gestionadas juntas, prueba de conexión contra endpoints reales, activación, predeterminado y exportación; centro de tokens con ámbitos y caducidad.
- **Apariencia y 9 idiomas** — claro / oscuro / sistema; English, 简体中文, العربية (RTL), Deutsch, Español, Français, Italiano, 日本語, Русский; paquetes de idioma cargados bajo demanda y cambio inmediato.
- **Seguridad** — caché AES-256-GCM con clave derivada de la máquina, enlaces externos solo http/https abiertos en tu navegador, DNS-over-HTTPS, bloqueo de instancia única y aislamiento estricto main / preload / renderer con lista blanca IPC.

## Qué trae cada versión

| Artefacto | Plataforma |
| --- | --- |
| `AI-Tools-Setup-<version>.exe` | Instalador de Windows (NSIS, x64) |
| `AI-Tools-<version>-portable.exe` | Windows portable, sin instalación |
| `AI-Tools-<version>.dmg` / `-arm64.dmg` | macOS (Intel / Apple silicon) |
| `AI-Tools-<version>-mac.zip` / `-arm64-mac.zip` | Archivos de macOS |
| `AI-Tools-<version>.AppImage` / `-arm64.AppImage` | Linux AppImage |
| `ai-tools_<version>_amd64.deb` / `_arm64.deb` | Linux .deb |
| `latest.yml`, `portable.yml`, `latest-mac.yml`, `latest-linux.yml`, `latest-linux-arm64.yml` | Manifiestos de actualización |
| `*.blockmap` | Bloques de descarga diferencial |

Todos los archivos se pueden descargar de forma anónima, sin token ni sesión. El feed que lee la aplicación es, por ejemplo:

```
https://github.com/qingchuang12/ai-tools-releases/releases/latest/download/latest.yml
```

Los manifiestos incluyen SHA-512 y tamaño; el actualizador verifica antes de instalar.

## Descarga e instalación

Última versión publicada: **1.1.1** (2026-11-02) — [Releases → más reciente](https://github.com/qingchuang12/ai-tools-releases/releases/latest)

- Windows — [AI-Tools-Setup-1.1.1.exe](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-Setup-1.1.1.exe) · [portable](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-portable.exe)
- macOS — [dmg (Intel)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.dmg) · [dmg (Apple silicon)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-arm64.dmg)
- Linux — [AppImage (x64)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.AppImage) · [deb (amd64)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/ai-tools_1.1.1_amd64.deb)

La página de descargas del sitio oficial ([www.ywhome.top/#product-ai-tools-download](https://www.ywhome.top/#product-ai-tools-download)) se está abriendo plataforma a plataforma; mientras tanto, este repositorio es el canal válido.

Las compilaciones aún **no están firmadas**: en Windows, SmartScreen → «Más información → Ejecutar de todas formas»; en macOS, si aparece como dañada, `xattr -cr /Applications/AI-Tools.app`; en AppImage, antes `chmod +x`.

## Actualización automática

Las instalaciones comprueban este repositorio por su cuenta y se actualizan en el sitio. Las NSIS siguen `latest.yml`, las portables `portable.yml`, macOS `latest-mac.yml` y Linux `latest-linux.yml` / `latest-linux-arm64.yml`.

## Privacidad y datos

Local-first: AI-Tools lee y escribe los ficheros de configuración de tu equipo y no sube nada hasta que configuras la sincronización. Los datos viven en `~/.ai-tools/` (macOS / Linux) o `%USERPROFILE%\.ai-tools\` (Windows), con caché cifrada AES-256-GCM. Términos: <https://www.ywhome.top/legal/terms.html> · Privacidad: <https://www.ywhome.top/legal/privacy.html>

## Primeros pasos

1. Instala y abre AI-Tools.
2. Busca en la **tienda MCP** (o en la pestaña **Skills**).
3. Pulsa **Instalar** y elige los clientes destino.
4. Úsalo en ese cliente, sin copiar y pegar JSON.
5. ¿Algo falla? Reprodúcelo en el **Inspector** y revierte desde el **Historial**.
6. ¿Varios equipos? Configura Git o SFTP en **Ajustes → Sincronización en la nube**.

## Soporte

- Información del producto, funciones, clientes y precios: <https://www.ywhome.top>
- Errores y peticiones: [abre una issue aquí](https://github.com/qingchuang12/ai-tools-releases/issues) o escribe a **service@ywhome.top**

---

<p align="center">
  <sub>AI-Tools es software propietario · © 2026 AI-Tools Team · Las partes derivadas de mcp-dock mantienen su licencia MIT (véase <code>THIRD_PARTY_LICENSES.md</code> incluido en la aplicación).</sub><br>
  <sub><a href="https://www.ywhome.top">www.ywhome.top</a> · <a href="https://www.ywhome.top/legal/terms.html">Términos</a> · <a href="https://www.ywhome.top/legal/privacy.html">Privacidad</a> · <a href="mailto:service@ywhome.top">service@ywhome.top</a></sub>
</p>

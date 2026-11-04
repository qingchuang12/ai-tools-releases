# AI-Tools (العربية)

**لوحة واحدة لكل سلسلة أدوات الذكاء الاصطناعي لديك.** يجمع AI-Tools خوادم MCP ومهارات Agent المبعثرة في إعدادات كل أداة برمجة بالذكاء الاصطناعي داخل تطبيق سطح مكتب واحد: تصفّح، تثبيت، تحرير، تصحيح، تراجع ومزامنة — دون تحرير ملف JSON يدويًا بعد اليوم.

<p align="center">
  <a href="https://www.ywhome.top">الموقع الرسمي</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/releases/latest">التنزيلات</a> ·
  <a href="https://www.ywhome.top/#product-ai-tools-pricing">التراخيص والأسعار</a> ·
  <a href="https://github.com/qingchuang12/ai-tools-releases/issues">الإبلاغ عن الأخطاء</a>
</p>

<p align="center">
  <a href="./README.md">English</a> ·
  <a href="./README.zh.md">简体中文</a> ·
  <strong>العربية</strong> ·
  <a href="./README.de.md">Deutsch</a> ·
  <a href="./README.es.md">Español</a> ·
  <a href="./README.fr.md">Français</a> ·
  <a href="./README.it.md">Italiano</a> ·
  <a href="./README.ja.md">日本語</a> ·
  <a href="./README.ru.md">Русский</a>
</p>

> **هذا المستودع** هو القناة الرسمية لإصدارات AI-Tools: حزم التثبيت لأنظمة Windows وmacOS وLinux، وملفات البيان التي تقرأها التطبيق للتحديث الذاتي. لا يحتوي على الشيفرة المصدرية.
> **جولة الميزات وقائمة العملاء المدعومين: <https://www.ywhome.top>**

---

## القدرة الأساسية

**إدارة 31 مدخل إعدادات MCP و19 وجهة للمهارات كقائمة واحدة** — Cursor وVS Code وClaude Code وGemini CLI وCodex CLI وWindsurf وZed وTRAE (CN / SOLO / الإضافة) وKiro وOpenCode وبيئات JetBrains وAntigravity وOpenClaw وCodeBuddy وWorkBuddy وQoder وZCode وCline وQwen Code وiFlow CLI وLM Studio وOpenHands وGitHub Copilot CLI وWarp وKimi Code CLI وKilo Code وGoose، إضافة إلى مدخل التخزين السحابي. تُبنى القائمة من فحص جهازك فعليًا، وأي عميل غير موجود يُضاف بتحديد مسار ملف إعداده ومجلد المهارات.

## لماذا يستحق وقتك

| العائق اليومي | ما يمنحك إياه AI-Tools |
| --- | --- |
| خادم واحد، ستة ملفات JSON، ستة أسماء مفاتيح | **اكتب مرة واحدة ووزّع على الجميع.** يصل الإعداد إلى كل عميل اخترته بلهجته الخاصة: JSON / JSONC / TOML، و`servers` بدل `mcpServers`، و`working_directory` بدل `cwd`， و`transport` بدل `type`، و`context_servers`، و`mcp_servers`. |
| متاجر تُطيل الانتظار للتحميل | **شاشة أولى فورية.** تخزين على القرص مع SWR: يظهر المحتوى قبل الشبكة، والتحديث يجري بصمت في الخلفية (القوائم ساعة， والتفاصيل 24 ساعة)， مع تحديث تجريبي بلمسة زر. |
| «هل أفسد تعديلي الأخير العميل؟» | **كل تغيير قابل للتراجع.** تُحفظ التثبيتات والإزالة والتحديثات والمزامنة والتعديلات تلقائيًا؛ قارن أي لقطة بالحالة الحالية (مُضاف / محذوف / مُعدّل بالألوان) واستعد بنقرة. |
| تصحيح خوادم MCP بـ curl | **مفتّش مدمج.** يدعم stdio / streamable-http / sse، ويستدعي الأدوات والموارد والأوامر الجاهزة من نموذج، مع إبراز JSON لسجلّ النتائج وسجلّ تشغيل في لوحة قابلة لتغيير الحجم. |
| إعادة البناء على جهاز جديد | **سحابتك الخاصة， واستعادة بنقرة.** أرسل إلى Git الخاص بك (مفتاح SSH / رمز HTTPS / مجهول) أو SFTP (كلمة مرور / مفتاح) عبر قائمة مهام مع تقدّم وإعادة محاولة， ومقارنة صريحة بين الطرفين قبل الاستبدال. |
| مدير إعدادات يتصل بالخارج؟ | **محلي بالأساس.** لا يخرج شيء من الجهاز قبل أن تفعّل المزامنة السحابية بنفسك؛ التخزين المؤقت مشفّر بـ AES-256-GCM， والبيانات الاعتمادية تُحفظ كمراجع مشفّرة فقط في SecretStore， والروابط الخارجية محصورة في http/https. |

## الميزات الجوهرية

- **متجر MCP** — Smithery وسجل npm والفهرس غير المتصل من Alibaba Bailian (251 مدخلًا دون إنترنت) وModelScope ولقطة السجل الرسمي؛ مع تصنيفات وإجماليات حقيقية وتقسيم صفحات من الخادم.
- **متجر المهارات** — متوافق مع العرف `~/.agents/skills/`؛ بحث وتصنيفات تتبع لغة الواجهة وفرز وتصفية حسب المصدر وتقسيم صفحات. في العملاء الذين لا يستقبلون مهارات يُعطى الزر *مع سبب واضح*， فلا تُنشأ مجلدات فارغة تحوي `.source.json` فحسب.
- **توزيع بنقرة** — تثبيت على عدة عملاء دفعة واحدة， وإزالة أو تحديث لكل عميل على حدة، ووسم التعديلات اليدوية فلا يطغى تحديث المتجر عليها.
- **مفتّش MCP** — أمر ووسائط ومتغيرات بيئة وترويسات مخصّصة， واستعراض الأدوات والموارد والأوامر الجاهزة， مع تنظيف العمليات التابعة عند الإغلاق.
- **المكتبة** — كل المثبّت في قائمة واحدة: تعديل الأمر / الوسائط / البيئة， وتحديد متعدد ومزامنة， وإزالة. وفي تبويب المهارات: تحرير SKILL.md داخل التطبيق， وإدارة الملفات المرفقة， والاستيراد من `.zip` / `.skill` / مجلد / رابط GitHub / السحب والإفلات， والتصدير كحزمة zip واحدة， وحلّ التعارضات قبل الرفع.
- **المزامنة السحابية** — Git أو SFTP， وسحب تلقائي عند الإقلاع， ودفع يدوي， ولوحة مهام بتقدّم وإعادة محاولة， وفحص اتساق بين الطرفين.
- **السجل والتراجع** — الوقت والحجم والعملاء المعنيون وعدد البنود؛ مقارنة بين الإصدارات； استعادة بنقرة； إفراغ السجل بالكامل.
- **فحص البيئة** — كشف Node.js وPython وGit (الوجود والإصدار والمسار) للإجابة عن «ثبّتُ لكنه لا يعمل».
- **المصادر ورموز API** — مصادر مدمجة واتصالات مباشرة بالمنصات (Base URL + رمز) تُدار معًا， واختبار اتصال على نقاط النهاية الحقيقية للمنصة， والتفعيل والتعيين كافتراضي والتصدير؛ ومركز رموز بنطاقات وتواريخ انتهاء.
- **المظهر و9 لغات** — فاتح / داكن / حسب النظام؛ English و简体中文 والعربية (تخطيط RTL كامل) وDeutsch وEspañol وFrançais وItaliano و日本語 وРусский؛ تُحمَل حزم اللغات عند الحاجة والتبديل فوري.
- **الأمان** — تخزين مشفّر AES-256-GCM بمفتاح مشتق من مواصفات الجهاز， وروابط خارجية http/https فقط تُفتح في متصفحك، وDNS-over-HTTPS، وقفل النسخة الواحدة، وعزل صارم بين main / preload / renderer بقائمة قنوات IPC المعتمدة.

## ما يحويه كل إصدار

| الملف | النظام |
| --- | --- |
| `AI-Tools-Setup-<version>.exe` | مثبّت Windows (NSIS، x64) |
| `AI-Tools-<version>-portable.exe` | نسخة محمولة بلا تثبيت |
| `AI-Tools-<version>.dmg` / `-arm64.dmg` | macOS (Intel / Apple silicon) |
| `AI-Tools-<version>-mac.zip` / `-arm64-mac.zip` | أرشيفات macOS |
| `AI-Tools-<version>.AppImage` / `-arm64.AppImage` | Linux AppImage |
| `ai-tools_<version>_amd64.deb` / `_arm64.deb` | Linux .deb |
| `latest.yml` و`portable.yml` و`latest-mac.yml` و`latest-linux.yml` و`latest-linux-arm64.yml` | ملفات بيان التحديث |
| `*.blockmap` | كتل التنزيل التفاضلي |

جميع الملفات قابلة للتنزيل دون تسجيل دخول أو رمز. مصدر التحديث الذي تقرأه التطبيق مثلاً:

```
https://github.com/qingchuang12/ai-tools-releases/releases/latest/download/latest.yml
```

تحمل ملفات البيان بصمة SHA-512 وحجم الملف， ويتحقق المُحدِّث منها قبل التثبيت.

## التنزيل والتثبيت

أحدث إصدار منشور: **1.1.1** (2026-11-02) — [Releases ← الأحدث](https://github.com/qingchuang12/ai-tools-releases/releases/latest)

- Windows — [AI-Tools-Setup-1.1.1.exe](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-Setup-1.1.1.exe) · [النسخة المحمولة](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-portable.exe)
- macOS — [dmg (Intel)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.dmg) · [dmg (Apple silicon)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1-arm64.dmg)
- Linux — [AppImage (x64)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/AI-Tools-1.1.1.AppImage) · [deb (amd64)](https://github.com/qingchuang12/ai-tools-releases/releases/download/1.1.1/ai-tools_1.1.1_amd64.deb)

صفحة التنزيل في الموقع الرسمي ([www.ywhome.top/#product-ai-tools-download](https://www.ywhome.top/#product-ai-tools-download)) تُفتَح منصة تلو الأخرى； وإلى ذلك الحين يبقى هذا المستودع القناة المعتمدة.

البناءات **غير موقّعة رقميًا** حاليًا: على Windows اختر «مزيد من المعلومات → تشغيل على أي حال» من SmartScreen； وعلى macOS نفّذ `xattr -cr /Applications/AI-Tools.app` إن ظهرت رسالة التلف； ولـ AppImage نفّذ `chmod +x` أولًا.

## التحديث الذاتي داخل التطبيق

تتحقق النسخ المثبّتة من هذا المستودع بنفسها وتُحدَّث في مكانها. تتبع حزم NSIS ملف `latest.yml`， والمحمولة `portable.yml`， وmacOS ملف `latest-mac.yml`， وLinux ملفي `latest-linux.yml` و`latest-linux-arm64.yml`.

## الخصوصية والبيانات

محلي بالأساس: يقرأ AI-Tools ويكتب ملفات الإعداد على جهازك فقط， ولا يرفع شيئًا قبل أن تعدّل المزامنة السحابية بنفسك. البيانات في `~/.ai-tools/` (macOS / Linux) أو `%USERPROFILE%\.ai-tools\` (Windows)， والتخزين المؤقت مشفّر بـ AES-256-GCM. الشروط: <https://www.ywhome.top/legal/terms.html> · الخصوصية: <https://www.ywhome.top/legal/privacy.html>

## البدء السريع

1. ثبّت التطبيق وافتحه.
2. ابحث في **متجر MCP** (أو تبويب **المهارات**).
3. اضغط **تثبيت** واختر العملاء المستهدفين.
4. استخدم القدرة داخل العميل مباشرة — بلا نسخ JSON.
5. عند الخلل: أعِد إنتاجه في **المفتّش** ثم تراجع من **السجل**.
6. عدة أجهزة؟ اضبط Git أو SFTP في **الإعدادات ← المزامنة السحابية**.

## الدعم

- معلومات المنتج والميزات والعملاء: <https://www.ywhome.top>
- الإبلاغ عن الأخطاء والطلبات: [افتح مسألة هنا](https://github.com/qingchuang12/ai-tools-releases/issues) أو راسلنا على **service@ywhome.top**

---

<p align="center">
  <sub>AI-Tools برنامج احتكاري · © 2026 AI-Tools Team · الأجزاء المأخوذة من mcp-dock تبقى تحت ترخيص MIT (انظر <code>THIRD_PARTY_LICENSES.md</code> المرفق مع التطبيق).</sub><br>
  <sub><a href="https://www.ywhome.top">www.ywhome.top</a> · <a href="https://www.ywhome.top/legal/terms.html">الشروط</a> · <a href="https://www.ywhome.top/legal/privacy.html">الخصوصية</a> · <a href="mailto:service@ywhome.top">service@ywhome.top</a></sub>
</p>

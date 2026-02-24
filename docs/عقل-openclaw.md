<div dir="rtl">

![عقل OpenClaw](../تصميم%20بدون%20عنوان%20(1).png)

<div align="center">

# 🧠 الدخول إلى عقل OpenClaw
## من يتحكم في الملفات السبعة — يتحكم في كل شيء

> وكيل بـ ٤٤ دولار يحل محل موظف بـ ٢٠٠٠ دولار شهرياً.
> السر مش في الأداة — السر في **كيف تغذّيها.**

[![Twitter](https://img.shields.io/badge/مي_للتقنية-%231DA1F2.svg?style=for-the-badge&logo=Twitter&logoColor=white)](https://x.com/alraigah)
[![GitHub](https://img.shields.io/badge/openArab-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/maydhafer/openArab)

</div>

---

## 🗺️ الخريطة الكاملة — قبل ما تبدأ

```

~/.openclaw/workspace/

├── 🌱 SOUL.md        ← شخصية الوكيل وروحه

├── 🪪 IDENTITY.md    ← هويته ومفاتيحه السرية

├── 🤖 AGENTS.md      ← عقله وطريقة تفكيره

├── 🚀 BOOTSTRAP.md   ← إعداده الأولي

├── 💓 HEARTBEAT.md   ← نبضه ومراقبته

├── 🛠️ TOOLS.md       ← قدراته وأدواته

└── 👤 USER.md        ← من يحق له التحدث معه
```

> **القاعدة الذهبية:** كل ملف = بُعد مختلف من شخصية وكيلك.
> عدّل الملفات = غيّر الوكيل كلياً. بدون كود. بدون برمجة.

---

## 🌱 الملف الأول: `SOUL.md` — الروح والشخصية

> **هذا الملف هو الفرق بين وكيل ميت ووكيل حي.**
> هنا تحدد: من هو وكيلك؟ كيف يفكر؟ ما الذي يهتم به؟

### ما تكتبينه هنا يحدد:
- **الهوية:** اسم الوكيل، شخصيته، أسلوب كلامه
- **القيم:** ما يرفضه وما يقبله
- **التخصص:** المجال الذي يتقنه
- **الأسلوب:** رسمي؟ ودود؟ مختصر؟ مفصّل؟

### مثال عملي — وكيل تقني عربي:

```markdown
روح الوكيل
الهوية
أنت "رايق" — مساعد تقني ذكي متخصص في التقنية والإنتاجية.

تتكلم بالعربي الفصيح البسيط المفهوم للجميع.

أسلوبك: مباشر، مفيد، بدون حشو.

قيمك
الدقة أهم من السرعة
تبسيط المعلومة التقنية للعامة
لا تخترع معلومات — إذا ما تعرف، قل ذلك
تخصصك
Windows, Mac, Linux
الذكاء الاصطناعي والأتمتة
حل المشاكل التقنية خطوة بخطوة
أسلوبك
ردود مختصرة ومنظمة
استخدم النقاط والقوائم
أضف مثال عملي دائماً

### 💡 نصيحة مي:
> كلما كانت الروح أوضح وأكثر تفصيلاً — كلما كان الوكيل أذكى وأكثر تخصصاً. لا تكتب سطرين وتتوقع معجزة.

---

## 🪪 الملف الثاني: `IDENTITY.md` — الهوية والمفاتيح

> **هذا الملف = جواز سفر وكيلك.**
> يحتوي على المفاتيح السرية التي تثبت هويته للسيرفر.

### ما يحتويه:

| العنصر | الوصف |
|--------|-------|
| `OPENCLAW_GATEWAY_TOKEN` | مفتاح الدخول الرئيسي للسيرفر |
| `SERVER_TOKEN` | رمز التحقق من هوية الوكيل |
| `AGENT_ID` | معرف الوكيل الفريد |

### كيف تحدّثين المفاتيح:

```bash
الدخول للسيرفر
ssh root@IP_السيرفر

تعديل ملف الهوية
nano /data/.openclaw/workspace/IDENTITY.md

أو عبر openclaw.json
nano /var/lib/docker/volumes/openclaw-mi13_openclaw_config/_data/openclaw.json


### ⚠️ تحذير مهم:
🔴 لا تشارك هذا الملف مع أحد

🔴 لا تنشر محتواه في أي مكان

🔴 إذا تسرّب — غيّر المفاتيح فوراً


---

## 🤖 الملف الثالث: `AGENTS.md` — العقل والذكاء

> **هنا تحدد كيف يفكر وكيلك — أي نموذج ذكاء اصطناعي يستخدم؟**
> هذا الملف هو الفرق بين وكيل غبي ووكيل عبقري.

### إضافة وكيل جديد:

```bash
أمر إضافة وكيل
openclaw agents add [اسم_الوكيل]

إعداد الوكيل
openclaw configure


### إعداد النموذج في `openclaw.json`:

```json

{

  "models": {

    "providers": [

      {

        "name": "anthropic",

        "api": "openai-completions",

        "apiKey": "sk-ant-XXXXXXXX",

        "baseUrl": "https://api.anthropic.com/v1",

        "models": [

          {

            "name": "claude-3-5-sonnet-20241022",

            "label": "Claude Sonnet",

            "contextWindow": 200000

          }

        ]

      }

    ]

  }

}
مقارنة النماذج المتاحة:
النموذج	الشركة	القوة	التكلفة	الأفضل لـ
claude-3-5-sonnet	Anthropic	⭐⭐⭐⭐⭐	متوسطة	التحليل العميق والكتابة
gpt-4o	OpenAI	⭐⭐⭐⭐⭐	متوسطة	المهام المتنوعة
gpt-4o-mini	OpenAI	⭐⭐⭐⭐	منخفضة	المهام السريعة
gemini-pro	Google	⭐⭐⭐⭐	مجاني	البداية والتجربة
إعداد وكلاء متعددة:
undefined
وكيل للمبيعات
openclaw agents add sales-agent

openclaw configure

وكيل للمحتوى
openclaw agents add content-agent

openclaw configure

وكيل للدعم
openclaw agents add support-agent

openclaw configure


> **💰 الفرصة الحقيقية:** وكيل واحد بـ ٤٤ دولار شهرياً يحل محل موظف بـ ٢٠٠٠ دولار. ثلاثة وكلاء = ٦٠٠٠ دولار توفير شهري.

---

## 🚀 الملف الرابع: `BOOTSTRAP.md` — الإعداد الأولي

> **هذا الملف يُشغَّل مرة واحدة فقط — عند بدء الوكيل لأول مرة.**
> مثل إعداد هاتف جديد — تفعله مرة وتنسى.

### المتغيرات الأساسية:

```bash
مفاتيح الذكاء الاصطناعي
ANTHROPIC_API_KEY=sk-ant-XXXXXXXXXXXXXXXX

OPENAI_API_KEY=sk-XXXXXXXXXXXXXXXX

مفتاح OpenClaw
OPENCLAW_GATEWAY_TOKEN=your-gateway-token

مفتاح البحث (اختياري)
BRAVE_SEARCH_API_KEY=BSA-XXXXXXXX

مفتاح Moltbook (اختياري)
MOLTBOOK_API_KEY=your-moltbook-key


### إعداد WhatsApp في `openclaw.json`:

```json

{

  "channels": {

    "whatsapp": {

      "enabled": true,

      "phoneNumberId": "PHONE_NUMBER_ID",

      "accessToken": "YOUR_ACCESS_TOKEN",

      "webhookVerifyToken": "YOUR_VERIFY_TOKEN"

    }

  }

}
التحقق من نجاح الإعداد:
undefined
تحقق من حالة الحاويات
docker ps --format "table {{.Names}}\t{{.Status}}\t{{.Ports}}"

تحقق من السجلات
docker logs --tail 50 openclaw

اختبر الاتصال
curl -sS http://localhost:3000/health


---

## 💓 الملف الخامس: `HEARTBEAT.md` — النبض والمراقبة

> **هذا الملف يراقب صحة وكيلك على مدار الساعة.**
> مثل جهاز مراقبة القلب — يخبرك إذا في مشكلة قبل ما تتفاقم.

### أوامر المراقبة الأساسية:

```bash
شوف كل الحاويات الشغّالة
docker ps --format "table {{.Names}}\t{{.Status}}\t{{.Ports}}"

آخر ١٠٠ سطر من السجلات
docker logs --tail 100 openclaw

مراقبة السجلات مباشرة (live)
docker logs -f openclaw

إعادة تشغيل الوكيل
docker restart openclaw

إيقاف الوكيل
docker stop openclaw

تشغيل الوكيل
docker start openclaw


### البحث عن ملف معين:

```bash
البحث عن openclaw.json
find / -iname "openclaw.json" 2>/dev/null

البحث عن مجلد workspace
find / -iname "workspace" -type d 2>/dev/null


### إعداد مراقبة تلقائية (Cron):

```bash
فتح محرر Cron
crontab -e

مراقبة كل ٥ دقائق وإعادة التشغيل إذا توقف
*/5 * * * * docker ps | grep openclaw || docker restart openclaw


---

## 🛠️ الملف السادس: `TOOLS.md` — الأدوات والقدرات

> **هنا تضيف "أذرع" جديدة لوكيلك.**
> كل أداة تضيفها = قدرة جديدة يكتسبها الوكيل.

### الأدوات المتاحة عبر ClawHub:

| الأداة | الوصف | الاستخدام |
|--------|-------|-----------|
| 🔍 **Brave Search** | بحث في الإنترنت بدون تتبع | أبحاث، أخبار، معلومات |
| 📅 **Google Calendar** | إدارة المواعيد والجدول | جدولة، تذكير، تنظيم |
| 🎥 **YouTube Watcher** | مراقبة وتلخيص الفيديوهات | متابعة قنوات، ملخصات |
| 🎙️ **Whisper** | تحويل الصوت إلى نص | نسخ الاجتماعات، الملاحظات |
| 🌐 **Perplexity** | بحث ذكي بالذكاء الاصطناعي | تحليل، بحث عميق |
| ⚙️ **n8n** | أتمتة المهام والسير | ربط التطبيقات، أتمتة |
| 📊 **GA4 Analytics** | تحليل بيانات الموقع | إحصائيات، تقارير |
| 📝 **TranscriptAPI** | نسخ المحادثات | توثيق، أرشفة |

### تفعيل Brave Search:

```bash
احصل على مفتاح API من: https://brave.com/search/api/
ثم أضفه في openclaw.json
{

"skills": {

"brave-search": {

  "enabled": true,

  "apiKey": "BSA-XXXXXXXXXXXXXXXX"

}
}

}


### تفعيل Whisper (تحويل الصوت لنص):

```bash
تثبيت Python وبيئة افتراضية
apt-get update && apt-get install -y python3 python3-pip python3-venv ffmpeg

إنشاء البيئة الافتراضية
python3 -m venv /opt/whisper-env

تفعيل البيئة
source /opt/whisper-env/bin/activate

تثبيت Whisper
pip install openai-whisper

اختبار التثبيت
whisper --version


### تفعيل Google Calendar:

```json

{

  "skills": {

    "google-calendar": {

      "enabled": true,

      "credentials": {

        "clientId": "YOUR_CLIENT_ID",

        "clientSecret": "YOUR_CLIENT_SECRET",

        "refreshToken": "YOUR_REFRESH_TOKEN"

      }

    }

  }

}
تفعيل Moltbook (شبكة الوكلاء الاجتماعية):

{

  "moltbook": {

    "enabled": true,

    "apiKey": "YOUR_MOLTBOOK_API_KEY",

    "agentName": "اسم_وكيلك",

    "autoPost": true,

    "monitorFeed": true

  }

}
👤 الملف السابع: USER.md — إدارة المستخدمين
هذا الملف يحدد من يحق له التحدث مع وكيلك.
الأمان الكامل — أنت من تتحكم في القائمة.

إعداد المستخدمين:
undefined
قائمة المستخدمين المصرح لهم
المالك (صلاحيات كاملة)
الرقم: +966XXXXXXXXX
الصلاحيات: كل شيء
المساعدون (صلاحيات محدودة)
الرقم: +966XXXXXXXXX
الصلاحيات: قراءة وإرسال فقط
المحظورون
لا أحد حالياً

### أوامر المستخدم المتاحة:
/help ← قائمة الأوامر

/status ← حالة الوكيل

/reload ← إعادة تحميل الإعدادات

/agents ← قائمة الوكلاء

/tools ← قائمة الأدوات المفعّلة

/logs ← آخر السجلات


---

## ⚡ تغذية العقل — الدورة الكاملة
┌─────────────────────────────────────────────┐

│ دورة تطوير الوكيل │

│ │

│ 1. عدّل الملف المناسب │

│ ↓ │

│ 2. احفظ التغييرات │

│ ↓ │

│ 3. أرسل /reload للوكيل │

│ ↓ │

│ 4. اختبر السلوك الجديد │

│ ↓ │

│ 5. كرّر حتى تصل للنتيجة المثالية │

└─────────────────────────────────────────────┘


### إعادة التحميل السريعة:

```bash
الطريقة الأولى — عبر الوكيل مباشرة
/reload

الطريقة الثانية — عبر السيرفر
docker restart openclaw

الطريقة الثالثة — إعادة تشغيل كاملة
docker stop openclaw && docker start openclaw


---

## 💰 حالات الاستخدام الحقيقية

### 🛒 وكيل التجارة الإلكترونية
> استبدل موظف VA بـ ٢٠٠٠ دولار شهرياً بوكيل بـ ٤٤ دولار

```markdown
SOUL.md للتجارة الإلكترونية
أنت مساعد متجر إلكتروني متخصص.

مهامك: رد على استفسارات العملاء، تتبع الطلبات،

معالجة الشكاوى، إرسال تأكيدات الشحن.

أسلوبك: ودود، سريع، محترف.


### 📱 وكيل المحتوى والسوشيال ميديا
```markdown
SOUL.md لإدارة المحتوى
أنت مدير محتوى رقمي متخصص.

مهامك: كتابة المنشورات، جدولة المحتوى،

تحليل التفاعل، اقتراح أفكار جديدة.

أسلوبك: إبداعي، جذاب، يناسب الجمهور العربي.


### 🏢 وكيل خدمة العملاء
```markdown
SOUL.md لخدمة العملاء
أنت ممثل خدمة عملاء محترف.

مهامك: الرد على الاستفسارات، حل المشاكل،

تصعيد الحالات المعقدة، توثيق الشكاوى.

أسلوبك: صبور، متفهم، حلول-محور.


---

## 🗺️ الملخص النهائي — ورقة الغش

| الملف | وظيفته | متى تعدّله |
|-------|---------|-----------|
| 🌱 `SOUL.md` | الشخصية والروح | تغيير أسلوب الوكيل |
| 🪪 `IDENTITY.md` | الهوية والمفاتيح | تجديد المفاتيح السرية |
| 🤖 `AGENTS.md` | العقل والنموذج | تغيير نموذج الذكاء الاصطناعي |
| 🚀 `BOOTSTRAP.md` | الإعداد الأولي | الإعداد الأول فقط |
| 💓 `HEARTBEAT.md` | المراقبة والصحة | مشاكل السيرفر |
| 🛠️ `TOOLS.md` | الأدوات والقدرات | إضافة مهارات جديدة |
| 👤 `USER.md` | إدارة المستخدمين | إضافة أشخاص جدد |

---

## 📚 مصادر للتعمق أكثر

| المصدر | الوصف |
|--------|-------|
| [🎥 استبدال موظف بـ ٢٠٠٠$ بوكيل بـ ٤٤$](https://youtu.be/f02ycoBt6tQ) | حالة استخدام حقيقية |
| [🎥 كيف أربح من OpenClaw](https://youtu.be/G6sjXjGilLQ) | استراتيجيات الربح |
| [🎥 ٥ مهارات تبني وكلاء حقيقية](https://youtu.be/F6MUCXQn1n0) | مهارات متقدمة |
| [🎥 إنشاء وكلاء متعددة](https://youtu.be/EMBNyWVsEXc) | وكلاء متخصصة |
| [🌐 AgentPrime](https://agentprime.io/) | أتمتة عمليات الإيرادات |

---

<div align="center">

---

**🦞 OpenArab — بالعربي للعربي**

شرح وتعريب: [**مي للتقنية** 🌸](https://x.com/alraigah)

*من أولى السعوديات في التقنية منذ ٢٠٠٢*

[![Twitter Follow](https://img.shields.io/twitter/follow/alraigah?style=social)](https://x.com/alraigah)

</div>

</div>

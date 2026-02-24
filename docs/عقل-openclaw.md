<div dir="rtl">

# 🧠 عقل OpenClaw — الدليل الكامل

> دليل تقني عميق لفهم وبناء وكلاء AI احترافيين باستخدام OpenClaw

---

## 📋 فهرس سريع

|
#
|
 الموضوع 
|
 الوصف 
|
|
---
|
---------
|
-------
|
|
[
١
](
#١-ما-هو-openclaw
)
|
 ما هو OpenClaw؟ 
|
 نظرة عامة على المنصة 
|
|
[
٢
](
#٢-الدخول-للعقل--ملفات-workspace
)
|
 الدخول للعقل 
|
 شرح ملفات Workspace السبعة 
|
|
[
٣
](
#٣-إنشاء-الوكلاء
)
|
 إنشاء الوكلاء 
|
 كيف تبني وكيلك خطوة بخطوة 
|
|
[
٤
](
#٤-الربح-من-الوكلاء
)
|
 الربح من الوكلاء 
|
 نماذج عمل حقيقية وأرقام 
|
|
[
٥
](
#٥-تنظيم-الوكلاء-وإدارتهم
)
|
 تنظيم الوكلاء 
|
 Docker، المراقبة، والصيانة 
|
|
[
٦
](
#٦-الأدوات-والتكاملات
)
|
 الأدوات والتكاملات 
|
 Brave، Calendar، Whisper وغيرها 
|

---

## ١. ما هو OpenClaw؟

OpenClaw منصة مفتوحة المصدر تشغّل وكلاء AI على سيرفرك الخاص.  
مش SaaS، مش اشتراك شهري لكل وكيل — أنت تملك البنية التحتية كاملة.

**الفرق الجوهري:**

| | OpenClaw | منصات SaaS |
|--|---------|------------|
| التحكم | كامل | محدود |
| التكلفة | ثابتة (سيرفر فقط) | تتضاعف مع كل وكيل |
| الخصوصية | بياناتك عندك | بيانات على سيرفرات الغير |
| التخصيص | لا حدود | محدود بالخطة |

---

## ٢. الدخول للعقل — ملفات Workspace

كل وكيل في OpenClaw يعيش في مجلد واحد:

```bash

~/.openclaw/workspace/

├── SOUL.md        # الشخصية والقيم

├── IDENTITY.md    # الهوية والتوكنات

├── AGENTS.md      # إعدادات النماذج

├── BOOTSTRAP.md   # إعداد البيئة الأولي

├── HEARTBEAT.md   # المراقبة والصيانة

├── TOOLS.md       # الأدوات والتكاملات

└── USER.md        # الصلاحيات والأوامر
📄 SOUL.md — روح الوكيل
هذا الملف يحدد شخصية الوكيل وقيمه الأساسية.
كل ما تكتبه هنا يصبح جزءاً من system prompt الوكيل.

مثال عملي:

undefined
SOUL
الشخصية
أنا مساعد تقني متخصص في دعم المطورين العرب.

أتحدث بوضوح وأبسّط المعلومة التقنية.

القيم الأساسية
الدقة أولاً: لا أخمّن، أبحث وأتأكد
الاحترام: أتعامل مع كل سؤال باهتمام حقيقي
الاستمرارية: أتذكر السياق وأبني عليه
أسلوب التواصل
عربي فصيح مبسّط
أمثلة عملية دائماً
لا مصطلحات معقدة بدون شرح

> 💡 **نصيحة:** SOUL.md هو الفرق بين وكيل "يجاوب" ووكيل "يفهم". استثمر فيه وقتك.

---

### 🪪 IDENTITY.md — هوية الوكيل

يحتوي على **التوكنات والمعرّفات الفريدة** للوكيل.

```markdown
IDENTITY
AGENT_ID: agent_arabic_support_v1

AGENT_NAME: مساعد مهندسك

VERSION: 1.0.0

CREATED: 2026-02-24

OWNER: maydhafer

API Keys
ANTHROPIC_KEY: sk-ant-...

OPENAI_KEY: sk-...

GEMINI_KEY: AIza...

Webhook
WEBHOOK_SECRET: your_secret_here

CALLBACK_URL: https://yourdomain.com/webhook


> ⚠️ **تحذير:** لا ترفع هذا الملف على GitHub أبداً. أضفه لـ `.gitignore` فوراً.

```bash

echo "IDENTITY.md" >> .gitignore
🤖 AGENTS.md — إعدادات النماذج
هنا تحدد أي نموذج AI يستخدم الوكيل وكيف يتصرف.


{

  "models": {

    "providers": [

      {

        "name": "anthropic",

        "api": "openai-completions",

        "apiKey": "sk-ant-...",

        "baseUrl": "https://api.anthropic.com/v1",

        "models": [

          {

            "id": "claude-3-5-sonnet-20241022",

            "name": "Claude 3.5 Sonnet",

            "contextLength": 200000,

            "maxTokens": 8192

          }

        ]

      },

      {

        "name": "openai",

        "api": "openai-completions",

        "apiKey": "sk-...",

        "baseUrl": "https://api.openai.com/v1",

        "models": [

          {

            "id": "gpt-4o",

            "name": "GPT-4o",

            "contextLength": 128000,

            "maxTokens": 4096

          }

        ]

      },

      {

        "name": "google",

        "api": "openai-completions",

        "apiKey": "AIza...",

        "baseUrl": "https://generativelanguage.googleapis.com/v1beta/openai",

        "models": [

          {

            "id": "gemini-2.0-flash",

            "name": "Gemini 2.0 Flash",

            "contextLength": 1000000,

            "maxTokens": 8192

          }

        ]

      }

    ]

  }

}
استراتيجية اختيار النموذج:

المهمة	النموذج الأنسب	السبب
تحليل معقد	Claude 3.5 Sonnet	أفضل في التفكير المنطقي
ردود سريعة	Gemini 2.0 Flash	سرعة + سعر منخفض
كتابة إبداعية	GPT-4o	متوازن في الإبداع
مهام اقتصادية	Gemini Flash	الأرخص بفارق كبير
🚀 BOOTSTRAP.md — الإعداد الأولي
يُشغَّل مرة واحدة فقط عند أول تشغيل للوكيل.
يحتوي على متغيرات البيئة والإعدادات الأساسية.

undefined
#!/bin/bash

BOOTSTRAP.md — يُنفَّذ عند أول تشغيل
متغيرات البيئة
export OPENCLAW_ENV=production

export OPENCLAW_PORT=3000

export OPENCLAW_LOG_LEVEL=info

export OPENCLAW_MEMORY_LIMIT=2048

إعداد قاعدة البيانات
export DB_HOST=localhost

export DB_PORT=5432

export DB_NAME=openclaw_db

إعداد WhatsApp (اختياري)
export WHATSAPP_ENABLED=true

export WHATSAPP_SESSION_PATH=~/.openclaw/sessions/whatsapp

تهيئة المجلدات
mkdir -p ~/.openclaw/logs

mkdir -p ~/.openclaw/sessions

mkdir -p ~/.openclaw/memory

echo "✅ Bootstrap completed successfully"


**تشغيل Bootstrap:**

```bash

chmod +x ~/.openclaw/workspace/BOOTSTRAP.md

bash ~/.openclaw/workspace/BOOTSTRAP.md
💓 HEARTBEAT.md — مراقبة الوكيل
يحتوي على أوامر المراقبة والصيانة اليومية.

أوامر Docker الأساسية:

undefined
عرض حالة كل الوكلاء
docker ps --format "table {{.Names}}\t{{.Status}}\t{{.Ports}}"

متابعة logs وكيل معين
docker logs -f openclaw-agent --tail=100

إعادة تشغيل وكيل
docker restart openclaw-agent

إيقاف وكيل
docker stop openclaw-agent

تشغيل وكيل
docker start openclaw-agent

عرض استهلاك الموارد
docker stats openclaw-agent --no-stream

حذف وكيل قديم
docker rm -f openclaw-agent-old


**سكريبت مراقبة تلقائي:**

```bash
#!/bin/bash

heartbeat_check.sh — شغّله كل 5 دقائق عبر cron
AGENT_NAME="openclaw-agent"

STATUS=$(docker inspect --format='{{.State.Status}}' $AGENT_NAME 2>/dev/null)

if [ "$STATUS" != "running" ]; then

echo "⚠️ الوكيل متوقف! جاري إعادة التشغيل..."

docker restart $AGENT_NAME

# أرسل إشعار (اختياري)

curl -X POST "https://api.telegram.org/bot$BOT_TOKEN/sendMessage" \

     -d "chat_id=$CHAT_ID&text=🔄 تم إعادة تشغيل $AGENT_NAME تلقائياً"
fi


**إضافة للـ cron:**

```bash
افتح crontab
crontab -e

أضف هذا السطر (كل 5 دقائق)
*/5 * * * * /bin/bash ~/.openclaw/workspace/heartbeat_check.sh


---

### 🛠️ TOOLS.md — الأدوات والتكاملات

يحدد **الأدوات الخارجية** التي يستطيع الوكيل استخدامها.

```yaml
TOOLS.md
tools:

البحث على الإنترنت
brave_search:

enabled: true

api_key: "BSA..."

max_results: 10

safe_search: moderate
تقويم Google
google_calendar:

enabled: true

credentials_path: ~/.openclaw/credentials/google.json

scopes:

  - https://www.googleapis.com/auth/calendar.readonly

  - https://www.googleapis.com/auth/calendar.events
تحويل الصوت لنص
whisper:

enabled: true

model: "whisper-1"

language: "ar"

api_key: "sk-..."
إدارة المهام
notion:

enabled: true

api_key: "secret_..."

database_id: "your_db_id"
إرسال الإيميل
email:

enabled: true

provider: smtp

host: smtp.gmail.com

port: 587

username: "your@gmail.com"

password: "app_password"

**كيف يستخدم الوكيل الأدوات:**

```python
مثال: الوكيل يبحث ثم يضيف للتقويم
agent.search("أفضل مطاعم الرياض 2026")

→ يستخدم Brave Search تلقائياً
agent.add_event("اجتماع مع العميل", "2026-02-25 10:00")

→ يضيف لـ Google Calendar تلقائياً

---

### 👤 USER.md — الصلاحيات والأوامر

يحدد **من يستطيع التحكم بالوكيل** وما هي الأوامر المتاحة.

```markdown
USER.md
المستخدمون المصرح لهم
ADMIN_USERS:

maydhafer@gmail.com

admin@yourdomain.com

REGULAR_USERS:

team@yourdomain.com
الأوامر المتاحة
أوامر الأدمن
/restart — إعادة تشغيل الوكيل

/status — عرض حالة الوكيل

/logs — عرض آخر 50 سطر من logs

/update — تحديث الوكيل

/config — عرض الإعدادات الحالية

أوامر المستخدم العادي
/help — عرض قائمة الأوامر

/reset — إعادة تعيين المحادثة

/memory — عرض ما يتذكره الوكيل عنك

/feedback — إرسال ملاحظة للمطور

حدود الاستخدام
MAX_MESSAGES_PER_HOUR: 100

MAX_TOKENS_PER_MESSAGE: 4000

RATE_LIMIT_WINDOW: 3600


---

## ٣. إنشاء الوكلاء

### الخطوات من الصفر

**الخطوة ١: تثبيت OpenClaw**

```bash
تثبيت عبر Docker
docker pull openclaw/openclaw:latest

أو تثبيت مباشر
git clone https://github.com/openclaw/openclaw.git

cd openclaw

npm install


**الخطوة ٢: إنشاء مجلد الوكيل**

```bash

mkdir -p ~/.openclaw/workspace/my-agent

cd ~/.openclaw/workspace/my-agent
إنشاء الملفات السبعة
touch SOUL.md IDENTITY.md AGENTS.md BOOTSTRAP.md HEARTBEAT.md TOOLS.md USER.md


**الخطوة ٣: إعداد openclaw.json**

```json

{

  "version": "1.0",

  "agent": {

    "name": "my-agent",

    "workspace": "~/.openclaw/workspace/my-agent",

    "port": 3000

  },

  "models": {

    "default": "claude-3-5-sonnet-20241022",

    "providers": [

      {

        "name": "anthropic",

        "api": "openai-completions",

        "apiKey": "sk-ant-...",

        "baseUrl": "https://api.anthropic.com/v1",

        "models": [

          {

            "id": "claude-3-5-sonnet-20241022",

            "name": "Claude 3.5 Sonnet",

            "contextLength": 200000,

            "maxTokens": 8192

          }

        ]

      }

    ]

  },

  "memory": {

    "enabled": true,

    "type": "local",

    "path": "~/.openclaw/memory"

  }

}
الخطوة ٤: تشغيل الوكيل

undefined
تشغيل مباشر
openclaw start --config openclaw.json

أو عبر Docker
docker run -d \

--name my-agent \

-p 3000:3000 \

-v ~/.openclaw:/root/.openclaw \

openclaw/openclaw:latest


**الخطوة ٥: اختبار الوكيل**

```bash
اختبار بسيط
curl -X POST http://localhost:3000/chat \

-H "Content-Type: application/json" \

-d '{"message": "مرحبا، كيف حالك؟"}'

الرد المتوقع
{"response": "مرحباً! أنا بخير وجاهز لمساعدتك 🙂"}

---

## ٤. الربح من الوكلاء

### نماذج العمل الحقيقية

**النموذج ١: خدمة دعم العملاء**
التكلفة الشهرية:

├── سيرفر VPS: $20/شهر

├── API (Claude/GPT): $30-50/شهر

└── المجموع: ~$50-70/شهر

الإيرادات:

├── 10 عملاء × $200/شهر = $2,000/شهر

└── صافي الربح: ~$1,930/شهر


**النموذج ٢: وكيل محتوى (كتابة + نشر)**
التكلفة:

├── سيرفر: $20/شهر

├── API: $40/شهر

└── المجموع: $60/شهر

الإيرادات:

├── 5 عملاء × $500/شهر = $2,500/شهر

└── صافي الربح: ~$2,440/شهر


**النموذج ٣: وكيل مبيعات (Lead Generation)**
التكلفة:

├── سيرفر: $30/شهر

├── API + أدوات: $70/شهر

└── المجموع: $100/شهر

الإيرادات:

├── عمولة 10% على صفقات = $3,000-10,000/شهر

└── صافي الربح: $2,900-9,900/شهر


### مقارنة: وكيل AI مقابل موظف بشري

| | وكيل AI | موظف بشري |
|--|---------|-----------|
| التكلفة الشهرية | $50-200 | $2,000-5,000 |
| ساعات العمل | 24/7 | 8 ساعات |
| وقت الاستجابة | ثوانٍ | دقائق-ساعات |
| التوسع | فوري | أشهر |
| الإجازات | لا يأخذ | نعم |

> 💰 **الحقيقة:** وكيل واحد بـ $100/شهر يعمل عمل 3 موظفين بـ $6,000/شهر.

### كيف تبدأ بالربح؟

**المرحلة ١ — ابنِ وكيلك الخاص (الشهر الأول)**
- حدد مشكلة واحدة تحلها
- ابنِ وكيلاً بسيطاً يحلها
- اختبره على نفسك أولاً

**المرحلة ٢ — أول عميل (الشهر الثاني)**
- قدّم الوكيل لشخص يعاني من نفس المشكلة
- ابدأ بسعر رمزي ($50-100) مقابل تجربة حقيقية
- اجمع الملاحظات وحسّن

**المرحلة ٣ — التوسع (الشهر الثالث+)**
- ارفع السعر بعد إثبات القيمة
- أضف عملاء جدد بنفس الوكيل
- كل عميل جديد = ربح شبه صافي

---

## ٥. تنظيم الوكلاء وإدارتهم

### إدارة عدة وكلاء بـ Docker Compose

```yaml
docker-compose.yml
version: '3.8'

services:

agent-support:

image: openclaw/openclaw:latest

container_name: agent-support

ports:

  - "3001:3000"

volumes:

  - ~/.openclaw/agents/support:/root/.openclaw/workspace

environment:

  - AGENT_NAME=support-agent

restart: unless-stopped
agent-content:

image: openclaw/openclaw:latest

container_name: agent-content

ports:

  - "3002:3000"

volumes:

  - ~/.openclaw/agents/content:/root/.openclaw/workspace

environment:

  - AGENT_NAME=content-agent

restart: unless-stopped
agent-sales:

image: openclaw/openclaw:latest

container_name: agent-sales

ports:

  - "3003:3000"

volumes:

  - ~/.openclaw/agents/sales:/root/.openclaw/workspace

environment:

  - AGENT_NAME=sales-agent

restart: unless-stopped

**تشغيل الكل دفعة واحدة:**

```bash

docker-compose up -d
عرض حالة الكل
docker-compose ps

إيقاف الكل
docker-compose down


### مراقبة مركزية

```bash
عرض logs كل الوكلاء في نفس الوقت
docker-compose logs -f

عرض استهلاك الموارد
docker stats --format "table {{.Name}}\t{{.CPUPerc}}\t{{.MemUsage}}"

النتيجة المتوقعة:
NAME CPU % MEM USAGE
agent-support 0.5% 256MiB / 2GiB
agent-content 0.3% 198MiB / 2GiB
agent-sales 0.8% 312MiB / 2GiB

### هيكل المجلدات المنظّم

```bash

~/.openclaw/

├── agents/

│   ├── support/          # وكيل الدعم

│   │   ├── SOUL.md

│   │   ├── IDENTITY.md

│   │   └── ...

│   ├── content/          # وكيل المحتوى

│   │   ├── SOUL.md

│   │   └── ...

│   └── sales/            # وكيل المبيعات

│       ├── SOUL.md

│       └── ...

├── shared/

│   ├── credentials/      # مفاتيح API مشتركة

│   └── memory/           # ذاكرة مشتركة

├── logs/                 # سجلات الأحداث

└── backups/              # نسخ احتياطية
٦. الأدوات والتكاملات
Brave Search — البحث الذكي
undefined
الحصول على API Key
https://api.search.brave.com/
اختبار مباشر
curl -H "Accept: application/json" \

 -H "Accept-Encoding: gzip" \

 -H "X-Subscription-Token: BSA..." \

 "https://api.search.brave.com/res/v1/web/search?q=OpenClaw+AI&count=5"

### Google Calendar — إدارة المواعيد

```bash
تثبيت المكتبة
pip install google-auth google-auth-oauthlib google-api-python-client

إعداد الاعتمادات
١. اذهب لـ Google Cloud Console
٢. أنشئ مشروع جديد
٣. فعّل Calendar API
٤. حمّل credentials.json
٥. ضعه في ~/.openclaw/credentials/

### Whisper — تحويل الصوت لنص

```python
مثال استخدام Whisper مع الوكيل
import openai

def transcribe_audio(audio_file_path):

client = openai.OpenAI(api_key="sk-...")



with open(audio_file_path, "rb") as audio_file:

    transcript = client.audio.transcriptions.create(

        model="whisper-1",

        file=audio_file,

        language="ar"  # عربي

    )



return transcript.text
الاستخدام
text = transcribe_audio("voice_message.ogg")

print(text) # "مرحبا، أريد حجز موعد غداً الساعة العاشرة"


---

## 📌 ورقة الغش السريعة

```bash
═══════════════════════════════════════
أوامر OpenClaw الأساسية
═══════════════════════════════════════
تشغيل وكيل
docker start [agent-name]

إيقاف وكيل
docker stop [agent-name]

إعادة تشغيل
docker restart [agent-name]

عرض الحالة
docker ps

عرض الـ logs
docker logs -f [agent-name] --tail=50

الدخول للوكيل
docker exec -it [agent-name] bash

تحديث الوكيل
docker pull openclaw/openclaw:latest

docker-compose up -d --force-recreate

نسخة احتياطية
tar -czf backup-$(date +%Y%m%d).tar.gz ~/.openclaw/


---

<div align="center">

**[@alraigah](https://x.com/alraigah)** | مي للتقنية

</div>

</div>

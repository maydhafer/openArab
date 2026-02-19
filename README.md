<div dir="rtl" align="right">
  <p align="center">
    <img src="https://raw.githubusercontent.com/maydhafer/openArab/main/openarab-logo-text.png.png" alt="OpenArab" width="100%">
  </p>
  <p align="center">
    <a href="https://github.com/openclaw/openclaw/actions/workflows/ci.yml?branch=main"><img src="https://img.shields.io/github/actions/workflow/status/openclaw/openclaw/ci.yml?branch=main&style=for-the-badge" alt="CI"></a>
    <a href="https://github.com/openclaw/openclaw/releases"><img src="https://img.shields.io/github/v/release/openclaw/openclaw?include_prereleases&style=for-the-badge" alt="Release"></a>
    <a href="https://discord.gg/clawd"><img src="https://img.shields.io/discord/1456350064065904867?label=Discord&logo=discord&logoColor=white&color=5865F2&style=for-the-badge" alt="Discord"></a>
    <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge" alt="MIT"></a>
  </p>

  <div align="right">
    <div dir="rtl" align="right">
      <p>
        <strong> لكل عربي يتمنى يوصل لأقوى أدوات الذكاء الاصطناعي بسهولة - شرح وتعريب <a href="https://x.com/alraigah"> مي للتقنية </a></strong>🌸
        <br>
      </p>
      <hr>
      <h2>🔗 روابط مفيدة</h2>
      <ul>
        <li>🌐 <a href="https://openclaw.ai">الموقع الرسمي</a></li>
        <li>📖 <a href="https://docs.openclaw.ai/install">دليل التثبيت الرسمي</a></li>
        <li>🛠️ <a href="https://docs.openclaw.ai/tools/skills">قائمة المهارات الكاملة</a></li>
        <li>📚 <a href="https://docs.openclaw.ai">الوثائق الكاملة</a></li>
        <li>💬 <a href="https://discord.gg/clawd">مجتمع Discord</a></li>
        <li>☁️ <a href="https://hostinger.ae?REFERRALCODE=MayDhafer">Hostinger — استضافة سحابية موصى بها</a></li>
      </ul>
      <hr>

      <h2>🚀 كيف تبدأ وتثبت OpenClaw (خطوة بخطوة)</h2>
      <p>تثبيت OpenClaw سهل إذا مشيت على الخطوات بالترتيب، البرنامج يحتاج بيئة تشغيل بسيطة على جهازك.</p>

      <h3>1️⃣ المتطلبات الأساسية</h3>
      <ul>
        <li>تحتاج تثبيت <strong>Node.js</strong> (إصدار 22 أو أحدث).</li>
        <li>إذا كنت تستخدم <strong>Windows</strong>، الأفضل والموصى به استخدامه عبر <strong>WSL2</strong>.</li>
        <li>إذا كنت على <strong>macOS</strong> أو <strong>Linux</strong>، فالأمور جاهزة مباشرة.</li>
      </ul>

      <h3>2️⃣ التثبيت عبر الأوامر (Terminal)</h3>
      <p>افتح نافذة الأوامر عندك وانسخ الأوامر التالية بالترتيب:</p>
      
      <pre dir="ltr" align="left" style="background: #f4f4f4; padding: 10px; border-radius: 5px; overflow-x: auto;">
# أولاً: تثبيت البرنامج عالمياً في جهازك
npm install -g openclaw@latest

# ثانياً: تشغيل معالج الإعداد الذكي (Wizard)
# هذا الأمر بيساعدك تربط كل شي خطوة بخطوة ويثبته كخدمة تعمل في الخلفية
openclaw onboard --install-daemon</pre>

      <h3>3️⃣ تشغيل البوابة (Gateway)</h3>
      <p>بعد الإعداد، ابدأ بتشغيل البوابة عشان تقدر تتحكم في كل شي من المتصفح:</p>
      <pre dir="ltr" align="left" style="background: #f4f4f4; padding: 10px; border-radius: 5px; overflow-x: auto;">
openclaw gateway --port 18789 --verbose</pre>

      <h3>4️⃣ تجربة إرسال رسالة</h3>
      <p>تقدر تختبر البرنامج مباشرة من الأوامر:</p>
      <pre dir="ltr" align="left" style="background: #f4f4f4; padding: 10px; border-radius: 5px; overflow-x: auto;">
openclaw message send --to +1234567890 --message "هلا والله من OpenClaw"</pre>

      <hr>

      <h2>🔗 ربط OpenClaw بالتطبيقات</h2>
      <table border="1" cellpadding="8" cellspacing="0" width="100%">
        <tr>
          <th>التطبيق</th>
          <th>طريقة الربط</th>
        </tr>
        <tr>
          <td>واتساب</td>
          <td>امسح QR Code من داخل الإعدادات</td>
        </tr>
        <tr>
          <td>تيليغرام</td>
          <td>أنشئ بوت عبر BotFather وأضف التوكن</td>
        </tr>
        <tr>
          <td>ديسكورد</td>
          <td>أنشئ بوت وأضف التوكن</td>
        </tr>
        <tr>
          <td>سلاك</td>
          <td>أضف التوكنات من إعدادات سلاك</td>
        </tr>
        <tr>
          <td>آي مسج</td>
          <td>عبر تطبيق BlueBubbles على ماك</td>
        </tr>
        <tr>
          <td>مايكروسوفت تيمز</td>
          <td>عبر Microsoft Bot Framework</td>
        </tr>
      </table>
      <hr>

      <h2>🛠️ المهارات — وش يقدر يسوي بالضبط؟</h2>
      <p>OpenClaw يدعم مهارات جاهزة تضيفها بضغطة زر، وتخدم الأفراد مثل ما تخدم الشركات.</p>
      👈 <strong><a href="https://docs.openclaw.ai/tools/skills">أستمتع بمهارات جبارة بتفيدك بكل شي تصفح هنا</a></strong>

      <h3>📢 التسويق الشخصي وصناعة المحتوى</h3>
      <ul>
        <li>كتابة إعلانات سناب / إنستقرام / تيك توك</li>
        <li>تحليل أداء منشوراتك</li>
        <li>اقتراح أفكار ريلز وفيديوهات</li>
        <li>تحسين البايو والوصف</li>
        <li>إعادة صياغة محتوى لزيادة التفاعل</li>
      </ul>

      <h3>📈 زيادة المبيعات للأفراد</h3>
      <ul>
        <li>تحليل متجر سلة أو زد</li>
        <li>اقتراح تحسينات لصفحة المنتج</li>
        <li>تحليل سلوك العملاء</li>
      </ul>

      <h3>💰 إدارة فلوسك الشخصية</h3>
      <ul>
        <li>تحليل مصاريفك الشهرية من CSV</li>
        <li>اقتراح خطة ادخار</li>
        <li>تتبع أهداف مالية</li>
      </ul>

      <h3>🤖 أتمتة يومك</h3>
      <ul>
        <li>الرد التلقائي على الرسائل</li>
        <li>جدولة مهامك</li>
        <li>تحويل الصوت إلى نص</li>
      </ul>
      <hr>

      <h2>💳 متى تدفع فلوس فعلًا؟</h2>
      <p>OpenClaw نفسه مجاني (مفتوح المصدر). لكن تدفع في الحالات التالية فقط:</p>
      <ul>
        <li>إذا استخدمت مفاتيح API مدفوعة (مثل OpenAI أو Anthropic).</li>
        <li>إذا استخدمت مهارة تتطلب خدمة خارجية بفلوس.</li>
        <li>إذا شغّلته على سيرفر (VPS) مدفوع.</li>
      </ul>
      <blockquote>
        البرنامج مجاني ✔ لكن "المفاتيح" والخدمات الخارجية هي اللي عليها تكلفة حسب استخدامك.
      </blockquote>

      <h2> مشاكل شائعة وحلولها❓</h2>
      <table border="1" cellpadding="8" cellspacing="0" width="100%">
        <tr>
          <th>المشكلة</th>
          <th>الحل</th>
        </tr>
        <tr>
          <td>npm: command not found</td>
          <td>تأكد إنك ثبّت Node.js وأعدت تشغيل الطرفية</td>
        </tr>
        <tr>
          <td>البوابة ما تفتح</td>
          <td>تأكد إنك شغّلت <code>openclaw gateway</code> أولاً</td>
        </tr>
        <tr>
          <td>خطأ في الصلاحيات على ويندوز</td>
          <td>شغّل PowerShell كمسؤول</td>
        </tr>
      </table>
      <hr>

      <h2>👋 تواصلي معي</h2>
      <table border="1" cellpadding="8" cellspacing="0" width="100%">
        <tr>
          <th>المنصة</th>
          <th>الرابط</th>
        </tr>
        <tr>
          <td>X (تويتر)</td>
          <td><a href="https://x.com/alraigah">@alraigah</a></td>
        </tr>
        <tr>
          <td>تيليغرام</td>
          <td><a href="https://t.me/alraigah_M">@alraigah_M</a></td>
        </tr>
        <tr>
          <td>يوتيوب</td>
          <td><a href="https://www.youtube.com/@usb_boot">@usb_boot</a></td>
        </tr>
      </table>
      <hr>
      <blockquote>
        هذا المشروع شرح وتعريب لـ <a href="https://github.com/openclaw/openclaw">OpenClaw</a> بترخيص MIT.<br>
        الهدف إن كل عربي يوصل لأقوى أدوات الذكاء الاصطناعي بسهولة — <strong>مي للتقنية</strong>
      </blockquote>
      <hr>
    </div>
  </div>
</div>

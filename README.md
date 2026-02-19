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

<hr>

<blockquote align="right">
شرح وتعريب بواسطة <strong><a href="https://x.com/alraigah">مي للتقنية</a></strong> — عشان كل عربي يوصل لأقوى أدوات الذكاء الاصطناعي بسهولة
</blockquote>

<hr>

<h2>🦞 وش هو OpenClaw؟</h2>

<p>
تخيل إنك عندك <strong>مساعد شخصي بالذكاء الاصطناعي</strong> — يشتغل على جهازك أنت، ما يحتاج اشتراك شهري، وتتحكم فيه بالكامل.
</p>

<ul>
<li>يرد عليك على <strong>واتساب، تيليغرام، ديسكورد، سلاك، آي مسج</strong> وغيرها — كلها في مكان واحد</li>
<li><strong>يسمع صوتك ويكلمك</strong> — مو بس نصوص</li>
<li><strong>يفتح المتصفح ويتصفح</strong> بدالك ويسوي مهام تلقائية</li>
<li><strong>يتذكر</strong> تفضيلاتك وأسلوبك ويتعلم منك مع الوقت</li>
<li>يشتغل <strong>24 ساعة</strong> بدون ما تفتح جهازك (لو حطيته على سيرفر)</li>
</ul>

<hr>

<h2>💰 وش الفايدة العملية؟ وكيف تربح منه؟</h2>

<p><strong>للأفراد:</strong></p>
<ul>
<li>رد تلقائي على رسائل واتساب وأنت نايم</li>
<li>مساعد يحجز مواعيدك ويذكّرك بمهامك</li>
<li>يبحث لك على الإنترنت ويلخص لك النتائج</li>
<li>يكتب لك محتوى سوشيال ميديا بأسلوبك</li>
</ul>

<p><strong>للأعمال والمشاريع:</strong></p>
<ul>
<li>بوت خدمة عملاء على واتساب يرد 24/7 بدون موظف</li>
<li>مساعد مبيعات يرد على استفسارات العملاء فوراً</li>
<li>أتمتة المهام المتكررة (إرسال تقارير، متابعة طلبات، إلخ)</li>
<li>توفير آلاف الريالات شهرياً بدل اشتراكات متعددة</li>
</ul>

<p>
<strong>والأهم: كل هذا مجاناً</strong> — البرنامج مفتوح المصدر، تدفع بس لنموذج الذكاء الاصطناعي اللي تختاره (Claude أو ChatGPT).
</p>

<hr>

<h2>🖥️ على أي جهاز يشتغل؟</h2>

<table align="right">
<tr>
<th>النظام</th>
<th>الدعم</th>
</tr>
<tr>
<td>ويندوز</td>
<td>✅ مدعوم</td>
</tr>
<tr>
<td>ماك</td>
<td>✅ مدعوم</td>
</tr>
<tr>
<td>لينكس</td>
<td>✅ مدعوم</td>
</tr>
<tr>
<td>سيرفر سحابي ☁️</td>
<td>✅ الأسهل والأسرع</td>
</tr>
</table>

<hr>

<h2>⚙️ المتطلب الوحيد — Node.js</h2>

<p>قبل ما تثبّت OpenClaw، تحتاج تثبّت <strong>Node.js</strong>.</p>

<h3>🪟 تثبيت Node.js على ويندوز</h3>

<p>
<a href="https://nodejs.org/dist/v20.11.0/node-v20.11.0-x64.msi">تحميل مباشر</a>
</p>

<pre><code>winget install OpenJS.NodeJS.LTS</code></pre>

<h3>🍎 تثبيت Node.js على ماك</h3>

<p>
<a href="https://nodejs.org/dist/v20.11.0/node-v20.11.0.pkg">تحميل مباشر</a>
</p>

<pre><code>brew install node@20</code></pre>

<h3>🐧 تثبيت Node.js على لينكس</h3>

<pre><code>curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -</code></pre>

<pre><code>sudo apt-get install -y nodejs</code></pre>

<hr>

<h2>🚀 تثبيت OpenClaw</h2>

<pre><code>npm install -g openclaw@latest</code></pre>

<pre><code>openclaw onboard --install-daemon</code></pre>

<pre><code>openclaw gateway</code></pre>

<pre><code>http://localhost:10000</code></pre>

<hr>

<h2>🔗 روابط مفيدة</h2>

<ul>
<li><a href="https://openclaw.ai">الموقع الرسمي</a></li>
<li><a href="https://docs.openclaw.ai/install">دليل التثبيت</a></li>
<li><a href="https://docs.openclaw.ai/tools/skills">المهارات</a></li>
<li><a href="https://discord.gg/clawd">Discord</a></li>
</ul>

<hr>

<p>
هذا المشروع شرح وتعريب لـ <a href="https://github.com/openclaw/openclaw">OpenClaw</a> بترخيص MIT — <strong>مي للتقنية</strong>
</p>

</div>

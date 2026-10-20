# 🚀 Discord Badge & Playtime Auto-Farm

سكربت تلقائي لأتمتة ساعات اللعب والمطالبة بشارات ديسكورد (Discord Badges).

> ⚠️ **إخلاء مسؤولية:** هذا المشروع لأغراض تعليمية فقط. استخدام السكربتات الخارجية على حسابك الشخصي قد يخالف شروط خدمة ديسكورد (ToS) وقد يعرّض حسابك للحظر. استخدمه على مسؤوليتك.
>
> 🔒 **تحذير أمني:** بعد انتهاء العملية **غيّر كلمة مرور حسابك** لإبطال التوكن القديم. ولا تشارك التوكن مع أي شخص أبداً.

---

## 📑 المحتويات
1. [الميزات](#-الميزات)
2. [الشروحات المرئية](#-الشروحات-المرئية)
3. [استخراج التوكن والكوكيز](#-استخراج-التوكن-token-والكوكيز-cookies)
4. [التشغيل على الكومبيوتر](#-التشغيل-على-الكومبيوتر-pc)
5. [التشغيل على الهاتف (Termux)](#-التشغيل-على-الهاتف-android--termux)

---

## 📌 الميزات
- رفع ساعات اللعب الوهمية (Game Playtime).
- تجميع شارات ديسكورد التفاعلية.
- يعمل على الكومبيوتر (PC) والأندرويد (عبر Termux).

---

## 🎥 الشروحات المرئية
| الشرح | الرابط |
|---|---|
| طريقة عمل السكربت وفهمه | [شاهد الفيديو](https://youtu.be/kYSL0avUPXU) |
| طريقة بديلة لجلب التوكن (Euiz) — يُنصح بتوكن عادي غير مشفر | [شاهد الشرح](https://youtu.be/8pSysgdXq8E) |

---

## 🛠️ استخراج التوكن (Token) والكوكيز (Cookies)

### 💻 على الكومبيوتر
1. افتح **Chrome** أو **Brave** ثم [Discord Web](https://discord.com/app) وسجّل الدخول.
2. اضغط `F12` أو `Ctrl + Shift + I` لفتح أدوات المطور.
3. **التوكن:** من تبويب **Console** الصق الكود التالي واضغط `Enter` (يُنسخ التوكن تلقائياً):
   ```javascript
   window.webpackChunkdiscord_app.push([[Math.random()],{},e=>{for(const c of Object.values(e.c))if(c?.exports?.default?.getToken!==void 0)copy(c.exports.default.getToken())}]);
   ```
4. **الكوكيز:** من تبويب **Application** ← **Cookies** ← `https://discord.com`، ثم انسخ قيمة `__dcfduid` أو `__sdcfduid`.

### 📱 على الأندرويد (Kiwi Browser)
1. حمّل **Kiwi Browser** من [GitHub Releases](https://github.com/kiwibrowser/src.next/releases).
2. افتح [Discord Web](https://discord.com/app) وسجّل دخولك.
3. من النقاط الثلاث `⋮` فعّل **Desktop Site**.
4. من `⋮` ← **Developer Tools** ← **Console** ونفّذ نفس كود التوكن أعلاه.
5. من **Application** ← **Cookies** انسخ القيم المطلوبة.

> 💡 إذا واجهتك صعوبة، استخدم الطريقة البديلة في فيديو Euiz.

---

## 💻 التشغيل على الكومبيوتر (PC)

**المتطلب:** [Python 3.x](https://www.python.org/downloads/)

افتح CMD أو PowerShell داخل مجلد السكربت ونفّذ:
```bash
pip install requests websocket-client && python main.py
```

---

## 📱 التشغيل على الهاتف (Android / Termux)

حمّل **Termux** من [F-Droid](https://f-droid.org/packages/com.termux/) (نسخة Play Store قديمة ولا تعمل جيداً).

### ✅ الأمر الموحّد (انسخه والصقه مرة واحدة)
```bash
pkg update -y && pkg upgrade -y && pkg install python git -y && pip install requests websocket-client && python main.py
```

> ⚠️ هذا الأمر يفترض أنك داخل مجلد السكربت. إن لم تكن، نزّل المشروع أولاً:
> ```bash
> git clone <رابط-المستودع> && cd <اسم-المجلد>
> ```

### 📖 شرح كل أمر

| الأمر | ماذا يفعل؟ |
|---|---|
| `pkg update -y` | يحدّث قائمة الحزم المتاحة (مثل "تحديث الفهرس"). الخيار `-y` يوافق تلقائياً على الأسئلة. |
| `pkg upgrade -y` | يرقّي الحزم المثبّتة في Termux إلى أحدث إصدار. |
| `pkg install python git -y` | يثبّت **Python** (لتشغيل السكربت) و**Git** (لتنزيل المشاريع من GitHub). |
| `pip install requests websocket-client` | يثبّت مكتبتين: `requests` للاتصال بالإنترنت، و`websocket-client` للاتصال الحي بديسكورد. |
| `python main.py` | يشغّل السكربت الرئيسي. |

**ما معنى `&&`؟** يربط الأوامر ببعض: كل أمر ينفّذ فقط إذا نجح الذي قبله. إذا فشل أحدها يتوقف الباقي.

### 🧩 أخطاء شائعة
- **`No such file: main.py`** ← لست داخل مجلد السكربت. استخدم `cd اسم-المجلد` أو `ls` لرؤية الملفات.
- **فشل `pkg update`** ← جرّب `termux-change-repo` واختر مرآة أخرى.
- **`pip` غير موجود** ← نفّذ `pkg install python-pip -y`.

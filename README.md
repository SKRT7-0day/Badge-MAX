# 🚀 Discord Badge & Playtime Auto-Farm

🌐 **Language / اللغة:** [العربية](#-العربية) | [English](#-english)

---

# 🇸🇦 العربية

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

---

# 🇬🇧 English

An automated script for farming playtime hours and claiming Discord badges.

> ⚠️ **Disclaimer:** This project is for educational purposes only. Using external automation scripts on your personal account may violate Discord's Terms of Service and could get your account banned. Use at your own risk.
>
> 🔒 **Security warning:** When you're completely done, **change your Discord password** to invalidate the old token. Never share your token with anyone.

---

## 📑 Table of Contents
1. [Features](#-features)
2. [Video Guides](#-video-guides)
3. [Getting Your Token and Cookies](#-getting-your-token-and-cookies)
4. [Running on PC](#-running-on-pc)
5. [Running on Android (Termux)](#-running-on-android-termux)

---

## 📌 Features
- Farm fake game playtime.
- Collect interactive Discord badges.
- Works on PC and Android (via Termux).

---

## 🎥 Video Guides
| Guide | Link |
|---|---|
| How the script works | [Watch](https://youtu.be/kYSL0avUPXU) |
| Alternative way to get the token (Euiz). A normal, unencrypted token is recommended. | [Watch](https://youtu.be/8pSysgdXq8E) |

---

## 🛠️ Getting Your Token and Cookies

### 💻 On PC
1. Open **Chrome** or **Brave**, go to [Discord Web](https://discord.com/app), and log in.
2. Press `F12` or `Ctrl + Shift + I` to open Developer Tools.
3. **Token:** In the **Console** tab, paste the code below and press `Enter`. The token is copied to your clipboard automatically.
   ```javascript
   window.webpackChunkdiscord_app.push([[Math.random()],{},e=>{for(const c of Object.values(e.c))if(c?.exports?.default?.getToken!==void 0)copy(c.exports.default.getToken())}]);
   ```
4. **Cookies:** Go to **Application** → **Cookies** → `https://discord.com`, then copy the value of `__dcfduid` or `__sdcfduid`.

### 📱 On Android (Kiwi Browser)
1. Download **Kiwi Browser** from [GitHub Releases](https://github.com/kiwibrowser/src.next/releases).
2. Open [Discord Web](https://discord.com/app) and log in.
3. Tap the three dots `⋮` and enable **Desktop Site**.
4. Tap `⋮` → **Developer Tools** → **Console**, then run the same token code shown above.
5. Go to **Application** → **Cookies** and copy the required values.

> 💡 If you have trouble, use the alternative method from the Euiz video.

---

## 💻 Running on PC

**Requirement:** [Python 3.x](https://www.python.org/downloads/)

Open CMD or PowerShell inside the script folder and run:
```bash
pip install requests websocket-client && python main.py
```

---

## 📱 Running on Android (Termux)

Install **Termux** from [F-Droid](https://f-droid.org/packages/com.termux/). The Play Store version is outdated and doesn't work well.

### ✅ Combined command (copy and paste it all at once)
```bash
pkg update -y && pkg upgrade -y && pkg install python git -y && pip install requests websocket-client && python main.py
```

> ⚠️ This assumes you're already inside the script's folder. If not, download the project first:
> ```bash
> git clone <repo-link> && cd <folder-name>
> ```

### 📖 What each command does

| Command | What it does |
|---|---|
| `pkg update -y` | Refreshes the list of available packages. `-y` auto-confirms prompts. |
| `pkg upgrade -y` | Upgrades installed Termux packages to their latest versions. |
| `pkg install python git -y` | Installs **Python** (to run the script) and **Git** (to download projects from GitHub). |
| `pip install requests websocket-client` | Installs two libraries: `requests` for web requests and `websocket-client` for the live connection to Discord. |
| `python main.py` | Runs the main script. |

**What does `&&` mean?** It chains commands together: each command runs only if the previous one succeeded. If one fails, the rest stop.

### 🧩 Common errors
- **`No such file: main.py`** → You're not in the script's folder. Use `cd folder-name`, or `ls` to list files.
- **`pkg update` fails** → Run `termux-change-repo` and choose a different mirror.
- **`pip` not found** → Run `pkg install python-pip -y`.

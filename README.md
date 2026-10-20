# 🚀 Discord Badge & Playtime Auto-Farm

🌐 [English](README_EN.md) | **العربية**

سكربت لأتمتة ساعات اللعب والمطالبة بشارات ديسكورد.

> ⚠️ **للأغراض التعليمية فقط.** قد يخالف شروط خدمة ديسكورد (ToS) ويعرّض حسابك للحظر. استخدمه على مسؤوليتك.
> 🔒 بعد الانتهاء **غيّر كلمة مرور حسابك** لإبطال التوكن القديم، ولا تشارك التوكن مع أحد.

---

## ⚡ التشغيل السريع

**📱 Termux (أندرويد)**
```bash
pkg update -y && pkg upgrade -y && pkg install python git -y && pip install requests websocket-client && python main.py
```

**💻 كمبيوتر (PC)**
```bash
pip install requests websocket-client && python main.py
```

---

## 🎥 الفيديوهات
- [طريقة عمل السكربت](https://youtu.be/kYSL0avUPXU)
- [طريقة بديلة لجلب التوكن (Euiz)](https://youtu.be/8pSysgdXq8E) — استخدم توكن عادي غير مشفر.

---

## 🛠️ استخراج التوكن والكوكيز
1. افتح [Discord Web](https://discord.com/app) في Chrome أو Brave، وسجّل الدخول.
   - على الأندرويد استخدم [Kiwi Browser](https://github.com/kiwibrowser/src.next/releases) وفعّل **Desktop Site**.
2. افتح أدوات المطور: `F12` أو `Ctrl + Shift + I` (على Kiwi: `⋮` ← Developer Tools).
3. **التوكن:** من تبويب **Console** الصق الكود واضغط `Enter` (يُنسخ تلقائياً):
   ```javascript
   window.webpackChunkdiscord_app.push([[Math.random()],{},e=>{for(const c of Object.values(e.c))if(c?.exports?.default?.getToken!==void 0)copy(c.exports.default.getToken())}]);
   ```
4. **الكوكيز:** من **Application ← Cookies ← discord.com** انسخ قيمة `__dcfduid` أو `__sdcfduid`.

---

## 💻 التشغيل على الكمبيوتر
المتطلب: [Python 3.x](https://www.python.org/downloads/)

افتح CMD أو PowerShell داخل مجلد السكربت ونفّذ أمر PC أعلاه.

---

## 📱 التشغيل على الهاتف (Termux)
حمّل Termux من [F-Droid](https://f-droid.org/packages/com.termux/) (نسخة Play Store قديمة).

إن لم تنزّل المشروع بعد:
```bash
git clone <رابط-المستودع> && cd <اسم-المجلد>
```

### 📖 شرح الأوامر
| الأمر | ماذا يفعل؟ |
|---|---|
| `pkg update -y` | يحدّث قائمة الحزم |
| `pkg upgrade -y` | يرقّي الحزم المثبتة |
| `pkg install python git -y` | يثبّت Python وGit |
| `pip install requests websocket-client` | يثبّت مكتبات الاتصال |
| `python main.py` | يشغّل السكربت |

- `&&` تربط الأوامر: كل أمر ينفّذ فقط إذا نجح السابق.
- `-y` يوافق تلقائياً على أسئلة التأكيد.

### 🧩 أخطاء شائعة
- `No such file: main.py` ← ادخل مجلد السكربت بـ `cd`.
- فشل `pkg update` ← نفّذ `termux-change-repo`.
- `pip` غير موجود ← `pkg install python-pip -y`.

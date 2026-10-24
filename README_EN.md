# 🚀 Discord Badge & Playtime Auto-Farm

🌐 **English** | [العربية](README.md)

A script to automate playtime hours and claim Discord badges.

> ⚠️ **For educational purposes only.** It may violate Discord's Terms of Service (ToS) and put your account at risk of a **ban**. Use it at your own risk.
> 🔒 When you're done, **change your account password** to invalidate the old token, and never share the token with anyone.

> ✅ **The script only needs the token.** No cookies required.

---

## ⚡ Quick Start

**📱 Termux (Android)**
```bash
pkg update -y && pkg upgrade -y && pkg install python git -y && pip install requests websocket-client && python main.py
```

**💻 Computer (PC)**
```bash
pip install requests websocket-client && python main.py
```

---

## 🎥 Videos
- [Alternative way to get the token (Euiz)](https://youtu.be/8pSysgdXq8E) — use a regular, unencrypted token.

---

## 🔑 What is the token?
A long string that works like your account password. Whoever has it can log into your account without a password. **Don't send it, don't publish it, and don't put it anywhere except the script.**

The code used to get the token (the same code in every method):
```javascript
window.webpackChunkdiscord_app.push([[Math.random()],{},e=>{for(const c of Object.values(e.c))if(c?.exports?.default?.getToken!==void 0)copy(c.exports.default.getToken())}]);
```

---

# 📱 Phone Guide (Android)

## 🟢 First: Running on Termux (download the repository)

Download Termux from [F-Droid](https://f-droid.org/packages/com.termux/) (the Play Store version is outdated), then download the repository and run the script.

**1) Install the requirements (one time only)**
```bash
pkg install python git -y && pip install requests websocket-client
```

**2) Download the repository**
```bash
git clone https://github.com/SKRT7-0day/Badge-MAX.git
```

**3) Run the script**
```bash
python script.py
```

**4) Enter the required data**
After launching, the script asks you for:
- **The token** (see the token extraction section above)
- **Number of hours** you want to log
- **Number of games** you want to run

Type the values and press `Enter`, and the script will start automatically.

| Command | What does it do? |
|---|---|
| `git clone <link>` | Downloads the whole repository to your device |
| `cd Badge-MAX && python script.py` | Enters the project folder, then runs the script |

> 🔒 Before you put your token into any script, open the code and make sure it doesn't send the token anywhere other than Discord.

## 🛠️ Second: Extracting the token (Kiwi Browser)

**1) Install the browser**
- Download the **Kiwi Browser** APK from [GitHub Releases](https://github.com/kiwibrowser/src.next/releases).
- During installation, allow your browser/files app to "install from unknown sources".

**2) Open Discord**
- Open Kiwi and go to [discord.com/app](https://discord.com/app).
- If an option to open the app appears, choose **Continue in browser**.
- Log in and wait for it to finish loading.

**3) Enable desktop site**
- Tap the three dots `⋮` at the top of the browser, then enable **Desktop site**. Without it, Discord tries to open the app and the tools don't work well.

**4) Open developer tools and extract the token**
1. Tap `⋮` then **Developer tools**.
2. Tap the **Console** tab.
3. Type `allow pasting` then `Enter` if pasting is blocked.
4. Paste the code above and press Enter. `undefined` will appear, which is normal, and the token is now in the clipboard.
5. Paste it into a notes app or directly into Termux (long-press the screen ← Paste).

### 🧩 Common errors in Termux
- `No such file: script.py` ← enter the script folder with `cd Badge-MAX`.
- `pkg update` fails ← run `termux-change-repo`.
- `pip` not found ← `pkg install python-pip -y`.

---

# 💻 PC Guide

## 🛠️ First: Extracting the token

**1) Open Discord in the browser**
- Open **Chrome** or **Brave**, and go to [discord.com/app](https://discord.com/app).
- Log in, and wait until the servers and chats fully appear (don't continue before loading completes).

**2) Open developer tools**
- Press `F12` (or `Ctrl + Shift + I`). On Mac: `Cmd + Option + I`.
- A panel appears on the side or bottom of the page, with tabs at the top such as Elements, Console, and Network.

**3) Extract the token**
1. Click the **Console** tab.
2. If the browser says pasting is blocked, type `allow pasting` then `Enter`, and then it will let you paste.
3. Paste the code above and press `Enter`.
4. The word `undefined` will usually appear. **This is normal** and doesn't mean the process failed. The token is now copied to the clipboard.
5. Paste it directly (`Ctrl + V`) into a notes app or wherever the script asks for it.
6. It looks like a long string of 3 parts separated by dots, like `xxxx.yyyy.zzzz`.

> ⚠️ Discord shows a red "Stop!" message in the console warning against pasting code. This is a general warning, and you should never paste into the console any code you don't understand or whose source you don't trust.

## 🖥️ Second: Running on the computer
Requirement: [Python 3.x](https://www.python.org/downloads/)

Open CMD or PowerShell inside the script folder and run the PC command above.

---

## 🧩 Common problems when extracting the token (phone and computer)
| Problem | Solution |
|---|---|
| The console refuses pasting | Type `allow pasting` then `Enter` |
| An error like `Cannot read properties` appears | Reload the page, wait for it to fully load, and try again |
| Nothing appears after pasting, or `undefined` appears | This is normal. Try `Ctrl + V` in a notes app to see if the token was copied |
| The token wasn't copied at all | Discord sometimes updates its site and breaks the code. Use the alternative method in the Euiz video above |

> 🔒 **Reminder:** After you finish using the script, change your account password, as this invalidates the old token.

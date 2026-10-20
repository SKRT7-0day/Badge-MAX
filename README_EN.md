# 🚀 Discord Badge & Playtime Auto-Farm

🌐 **English** | [العربية](README.md)

A script to automate playtime hours and claim Discord badges.

> ⚠️ **Educational use only.** It may violate Discord's Terms of Service and get your account banned. Use at your own risk.
> 🔒 When you're done, **change your Discord password** to invalidate the old token, and never share your token.

---

## ⚡ Quick Start

**📱 Termux (Android)**
```bash
pkg update -y && pkg upgrade -y && pkg install python git -y && pip install requests websocket-client && python main.py
```

**💻 PC**
```bash
pip install requests websocket-client && python main.py
```

---

## 🎥 Videos
- [How the script works](https://youtu.be/kYSL0avUPXU)
- [Alternative token method (Euiz)](https://youtu.be/8pSysgdXq8E) — use a normal, unencrypted token.

---

## 🛠️ Getting Your Token and Cookies

> 🔑 **What is a token?** A long string that works like your account password. Anyone who has it can access your account without your password. **Never send it, post it, or paste it anywhere except the script.**

The code used to grab the token (the same code for every method):
```javascript
window.webpackChunkdiscord_app.push([[Math.random()],{},e=>{for(const c of Object.values(e.c))if(c?.exports?.default?.getToken!==void 0)copy(c.exports.default.getToken())}]);
```

### 💻 Part 1: On PC

**1) Open Discord in the browser**
- Open **Chrome** or **Brave** and go to [discord.com/app](https://discord.com/app).
- Log in and wait until your servers and chats have fully loaded (don't continue before that).

**2) Open Developer Tools**
- Press `F12` (or `Ctrl + Shift + I`). On Mac: `Cmd + Option + I`.
- A panel opens at the side or bottom of the page, with tabs along the top such as Elements, Console, Network, and Application.

**3) Get the token**
1. Click the **Console** tab.
2. If the browser says pasting is blocked, type `allow pasting` and press `Enter`. After that you can paste.
3. Paste the code above and press `Enter`.
4. You will usually see `undefined`. **This is normal** and doesn't mean it failed. The token is now copied to your clipboard.
5. Paste it right away (`Ctrl + V`) into a notes app or wherever the script asks for it.
6. It looks like a long string in 3 parts separated by two dots, like `xxxx.yyyy.zzzz`.

> ⚠️ Discord shows a red "Stop!" warning in the console about pasting code. It's a general warning. Never paste code into the console that you don't understand or don't trust.

**4) Get the cookies**
1. In the same Developer Tools panel, click the **Application** tab. If you can't see it, click the `»` arrows to reveal more tabs.
2. In the left sidebar, expand **Cookies** and click `https://discord.com`.
3. In the table, look in the **Name** column for `__dcfduid` (if it's missing, look for `__sdcfduid`).
4. Double-click its cell in the **Value** column to select it, then press `Ctrl + C` to copy.

### 📱 Part 2: On Android (Kiwi Browser)

**1) Install the browser**
- Download the **Kiwi Browser** APK from [GitHub Releases](https://github.com/kiwibrowser/src.next/releases).
- When installing, allow "install from unknown sources" for your browser or file manager.

**2) Open Discord**
- Open Kiwi and go to [discord.com/app](https://discord.com/app).
- If it offers to open the app, choose **Continue in browser**.
- Log in and wait for everything to load.

**3) Enable Desktop site**
- Tap the three dots `⋮` at the top and turn on **Desktop site**. Without it, Discord keeps pushing the app and the tools don't work well.

**4) Open Developer Tools and get the token**
1. Tap `⋮` then **Developer tools**.
2. Tap the **Console** tab.
3. Type `allow pasting` and press Enter if pasting is blocked.
4. Paste the code above and press Enter. You'll see `undefined`, which is normal. The token is now in your clipboard.
5. Paste it into a notes app, or directly into Termux (long-press the screen → Paste).

**5) Get the cookies**
- In Developer Tools, tap **Application** → **Cookies** → `https://discord.com`, and copy the value of `__dcfduid` or `__sdcfduid`, same as the PC steps.

### 🧩 Common problems at this stage
| Problem | Fix |
|---|---|
| Console refuses to paste | Type `allow pasting` then `Enter` |
| Error like `Cannot read properties` | Reload the page, wait for it to fully load, and try again |
| Nothing shows or you see `undefined` | That's normal. Try `Ctrl + V` in a notes app to check the token was copied |
| The token never copies | Discord sometimes updates its site and breaks the code. Use the alternative method in the Euiz video above |
| Can't find `__dcfduid` | Look for `__sdcfduid`, or reload the page and reopen the Application tab |

> 🔒 **Reminder:** When you're done with the script, change your Discord password. That invalidates the old token.

---

## 💻 Running on PC
Requirement: [Python 3.x](https://www.python.org/downloads/)

Open CMD or PowerShell inside the script folder and run the PC command above.

---

## 📱 Running on Android (Termux)
Get Termux from [F-Droid](https://f-droid.org/packages/com.termux/) (the Play Store version is outdated).

If you haven't downloaded the project yet:
```bash
git clone <repo-link> && cd <folder-name>
```

### 📖 What each command does
| Command | What it does |
|---|---|
| `pkg update -y` | Refreshes the package list |
| `pkg upgrade -y` | Upgrades installed packages |
| `pkg install python git -y` | Installs Python and Git |
| `pip install requests websocket-client` | Installs the networking libraries |
| `python main.py` | Runs the script |

- `&&` chains commands: each runs only if the previous one succeeded.
- `-y` auto-confirms prompts.

### 🧩 Common errors
- `No such file: main.py` → `cd` into the script's folder.
- `pkg update` fails → run `termux-change-repo`.
- `pip` not found → `pkg install python-pip -y`.

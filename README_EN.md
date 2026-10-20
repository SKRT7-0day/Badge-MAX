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
1. Open [Discord Web](https://discord.com/app) in Chrome or Brave and log in.
   - On Android use [Kiwi Browser](https://github.com/kiwibrowser/src.next/releases) and enable **Desktop Site**.
2. Open Developer Tools: `F12` or `Ctrl + Shift + I` (on Kiwi: `⋮` → Developer Tools).
3. **Token:** In the **Console** tab, paste the code and press `Enter` (it's copied automatically):
   ```javascript
   window.webpackChunkdiscord_app.push([[Math.random()],{},e=>{for(const c of Object.values(e.c))if(c?.exports?.default?.getToken!==void 0)copy(c.exports.default.getToken())}]);
   ```
4. **Cookies:** Go to **Application → Cookies → discord.com** and copy `__dcfduid` or `__sdcfduid`.

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

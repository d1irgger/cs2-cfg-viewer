# CS2 Config Viewer

> A CS2 config viewer and translation tool: turn complex CS2 config files into readable, plain-language descriptions.

**English** | [简体中文](README.md)

A visual **CFG/VCFG viewer and parser** built for **Counter-Strike 2**, with English-to-Chinese translation for keybinds, console commands, and video settings — so you can understand your own (or someone else's) config at a glance.

[![Version](https://img.shields.io/badge/version-4.1.0-6aa0ff)](https://github.com/d1irgger/cs2-cfg-viewer)
[![Online](https://img.shields.io/badge/🌐_Live_Demo-d1irgger.github.io/cs2--cfg--viewer-a98bff)](https://d1irgger.github.io/cs2-cfg-viewer/)
[![License](https://img.shields.io/badge/license-MIT-lightgrey)](LICENSE)

---

## 🌐 Use Online (Recommended)

**No download, no installation — just open it in your browser:**

### 👉 **[https://d1irgger.github.io/cs2-cfg-viewer/](https://d1irgger.github.io/cs2-cfg-viewer/)**

Chrome/Edge is recommended. Once it loads, click **"📁 Select Steam / userdata directory"** or **"📄 Import autoexec.cfg"** to get started.

> 💡 **Tip**: Selecting the `Steam/userdata` directory is much faster than selecting the Steam root directory. The browser will ask for permission to read the directory you choose. All data is processed **locally** and **never uploaded to any server**.

---

## 📌 What Is This?

CS2 stores its configuration as plain text in the following locations:

- **Per-user config**: `Steam/userdata/<SteamID>/730/local/cfg/`
- **Global config**: `<Game install dir>/game/csgo/cfg/`
- **Common files**: `machine_convars.vcfg`, `user_convars.vcfg`, `user_keys.vcfg`, `video.txt`

Inside these files are large numbers of key-value pairs such as `bind "key" "+command"` and `setting.cl_crosshaircolor 1`. For anyone unfamiliar with CS2 commands, they read like gibberish.

**CS2 Config Viewer** bridges that gap by translating these “walls of text” into readable Chinese:

- `bind "kp_ins" "+jump"` → 「Numpad 0 → Jump」
- `cl_crosshaircolor 4` → 「Crosshair color → Cyan」
- `setting.r_low_latency 2` → 「Low latency mode → Ultra-low latency」

---

## ✨ Features

### Web Version (v4.2.0)

- **🧠 Translation enhanced by official descriptions**: Includes ~150 built-in Chinese descriptions for commonly used commands, displayed instantly. Remaining entries use the official CS2 English description as translation context, improving machine-translation accuracy.
- **📥 cvarlist.md import**: One-click import of a community-maintained CS2 command list, expanding the English description library to 4000+ entries.
- **📂 Three data sources**: Scan a Steam `userdata` directory / load `.vcfg` files manually / import `autoexec.cfg`.
- **👥 Multi-account support**: Automatically detects multiple accounts under the same Steam installation, switchable via a dropdown; the path bar reflects the currently selected account.
- **🔍 Real-time search**: Instantly filter by keybind, command, setting, or official English description.
- **🌐 Optional online translation**: Start / stop at any time, with visible progress and automatic retry for failed entries.
- **🪟 Liquid glass UI**: Official CS2 icon, lightweight, clean, and content-first.

### Desktop Version

- **🖥️ Native file dialogs**: Pick files like a local app.
- **🔍 Reads Steam path from registry**: Automatically locates the Steam installation directory.

---

## 🧠 Translation Engine

All three usage modes share the same translation pipeline:

1. **Local dictionary**: Built-in English-to-Chinese mappings for common keys, commands, and settings.
2. **Online translation**: Entries not found locally are sent to the [MyMemory Translation API](https://mymemory.translated.net/) for English-to-Chinese translation.
3. **Description enhancement** (web version only): Uses the official ConVar English description as translation context, improving machine-translation accuracy.

---

## 📚 Data Sources

Official English descriptions come from community-maintained CS2 ConVar lists:

- [SuGolYolLom/CS2-Cvars-Cmds](https://github.com/SuGolYolLom/CS2-Cvars-Cmds)
- [ArmynC/ArminC-CS2-Cvars](https://github.com/ArmynC/ArminC-CS2-Cvars)

> Valve has not published official Chinese documentation for CS2 ConVars, so the translation layer relies on a combination of the local dictionary, community data, and MyMemory.

---

## 🔒 Privacy

- All config parsing and translation lookups are done **locally in your browser**.
- Command names and description text are sent to the MyMemory API for translation **only when** you click **"🌐 Start online translation"**.
- Your config files, Steam ID, and any personal information are never uploaded.

---

## ⚠️ Known Limitations

- **Automatic Steam path detection**: Only supported in the Python-based desktop version; the web version requires manually selecting a directory.
- **MyMemory free quota**: Anonymous users get roughly 5,000 characters/day; requests beyond that are skipped.
- **Firefox directory selection**: Firefox does not support directory selection. On the web version, use **"Load config file manually"** or switch to Chrome/Edge.

---

## 🤝 Feedback & Contributing

- **Issues / PRs**: [GitHub Issues](https://github.com/d1irgger/cs2-cfg-viewer/issues)
- **Author**: [@d1irgger](https://github.com/d1irgger)
- **Telegram**: [@timharrys](https://t.me/timharrys)

If this tool saves you time sifting through configs, a ⭐ star is the biggest encouragement.

---

## 📄 License

MIT License

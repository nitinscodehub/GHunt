# 🔥 GHunt — Real-World Setup Guide (No Confusion Version by Nitin)

![Banner](assets/long_banner.png)

#### 🌐 GHunt Online version: [https://osint.industries](https://osint.industries)

#### 🐍 Python 3.13 Compatible

![Python minimum version](https://img.shields.io/badge/Python-3.10%2B-brightgreen)

---

# 😎 Description

GHunt (v2) is an offensive Google OSINT framework used for gathering intel from Google services.
Fast, async, modular — and now super easy to set up with this **tested setup guide**.

---

# ✔️ Requirements

* Python **>= 3.10**
* Works perfectly on **Kali Linux** (tested)

---

# ⚙️ Full Working Installation Guide (Tested by Me)

## ✅ Step 1 — Install Python & pip

Kali normally has Python preinstalled. Still, ensure compatibility:

```bash
sudo apt install python-is-python3 -y
sudo apt install python3-pip -y
```

## ✅ Step 2 — Install pipx (Recommended)

```bash
pip3 install pipx
pipx ensurepath
```

> If you see "externally-managed-environment" error, ignore — pipx still installs.

## ✅ Step 3 — Install GHunt

```bash
pipx install ghunt --force
```

After installation, confirm:

```bash
ghunt --version
```

---

# 🔑 Login Setup (100% Working Guide)

Run:

```bash
ghunt login
```

You’ll see menu options:

```
[1] (Companion) Put GHunt on listening mode
[2] (Companion) Paste base64 encoded cookies
[3] Enter oauth token manually
[4] Enter master token manually
```

### ✔ Choose: **Option 1** → Listener Mode

GHunt will say:

```
GHunt is listening on port 60067...
```

### ✔ Open GHunt Companion Extension

Install from:

* Firefox
* Chrome
* Edge
* Opera

Then extension automatically sends cookies.

You will see:

```
[+] Received cookies!
[+] Got OAuth2 token
[+] Master token generated and saved
```

All credentials saved here:

```
~/.malfrats/ghunt/creds.m
```

Your GHunt is now fully authenticated.

---

# 💃 Usage

## 📧 1. Scan an Email

```bash
ghunt email <email_here>
```

Shows:

* DP / cover pic status
* Active Google services
* Calendar events
* Maps contribution
* PlayGames info
* Gaia ID
* Much more…

## 🕸️ 2. Spider Mode (Most Powerful)

Use for Google URLs:

```bash
ghunt spider <google_link>
```

Works on:

* Maps profiles
* Photos share links
* People cards
* YouTube channels
* MyMaps

## 📁 3. Drive File Lookup

```bash
ghunt drive <file_or_folder_id>
```

## 🌍 4. WiFi BSSID Geolocation

```bash
ghunt geolocate <bssid>
```

## 📝 5. Export JSON

```bash
ghunt email <email> --json output.json
```

---

# 🧪 My Personal Tested Example (Working)

```
ghunt email your_email@gmail.com
```

Output included:

* Default profile pics
* Gaia ID
* Activated services (Maps, Photos, Meet)
* Public Google Calendar
* 81 events dumped
* Maps profile link

```
https://www.google.com/maps/contrib/<gaia_id>/reviews
```

Everything worked perfectly.

---

# 🧑‍💻 Developers

Docs: [https://github.com/mxrch/GHunt/wiki](https://github.com/mxrch/GHunt/wiki)

If you want to use GHunt as a library:

```bash
pip3 install ghunt
```

Then:

```python
import ghunt
```

---

# 📮 Disclaimers

* Educational purposes only.
* Respect the AGPL license.
* Use responsibly.

---

## Maintainer

**Nitin (@nitinscodehub)**
Cybersecurity & OSINT Enthusiast
GitHub: [https://github.com/nitinscodehub](https://github.com/nitinscodehub)

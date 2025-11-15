<h1>GHunt — Google OSINT Recon Tool</h1>
<img alt="GHunt banner" src="https://github.com/user-attachments/assets/4ef7125a-e307-4fe3-aa17-b5b6e5591476" style="max-width:100%;height:auto;" />

Modern, cross-platform fork of GHunt focused on cleaner docs, easier setup, and faster OSINT workflows.
GHunt helps you discover Google account footprints (emails, Drive/docs metadata, Maps contributions, photos, IDs, and more) using passive techniques — no Google login required.

Disclaimer: Use this tool responsibly. Only investigate accounts you are authorized to analyze. Misuse can violate laws and service terms.

Table of Contents

What is GHunt?

Key Features

Quick Start

Clone

Linux (recommended)

Windows

Setup (Cookies)

Usage

Examples

Project Structure

Why this fork?

Contributing

License

Maintainer

What is GHunt?

GHunt ek powerful OSINT tool hai jo public Google footprint data extract karta hai.
Is fork ka main focus hai:

Easy installation

Cross-platform compatibility

Clean Docs

Beginner-friendly flow

Updated structure

Use cases: cybersecurity learning, digital investigations, bug bounty reconnaissance, privacy research, DFIR.

Key Features

Google account metadata discovery

Photos / Picasa info extraction

Google Maps contribution lookup

Google Drive / Docs metadata recon

Token (cookie)-based Google session analyzer

CLI-based fast workflow

Runs on both Linux & Windows

Quick Start
<h3 id="clone">1. Clone the repository</h3>
git clone https://github.com/nitinscodehub/GHunt.git
cd GHunt

🐧 <h3 id="linux-recommended">2. Linux (Kali/Ubuntu/Parrot)</h3>
Install Python + venv
sudo apt update -y
sudo apt install python3 python3-pip python3-venv -y

Create environment
python3 -m venv venv
source venv/bin/activate

Install requirements
pip install -r requirements.txt

🪟 <h3 id="windows">3. Windows</h3>
Install Python 3.10+

From: https://www.python.org/downloads

(❗ Make sure “Add to PATH” is enabled)

Clone repo
git clone https://github.com/nitinscodehub/GHunt.git
cd GHunt

Create virtual environment
python -m venv venv
venv\Scripts\activate

Install dependencies
pip install -r requirements.txt

<h2 id="setup-cookies">Setup (Cookies)</h2>

Some GHunt features require a browser session cookie export from Chrome/Edge.

How to export cookies

Open Chrome → Press F12

Application → Cookies → https://google.com

Export as JSON

Save as:

cookies.json


Place file in project root.

⚠️ Security Note: Never commit or upload cookies.json.

<h2 id="usage">Usage</h2>
Email lookup
python3 ghunt email example@gmail.com

Google ID lookup
python3 ghunt id 12345678901234567890

Picasa / Photos scan
python3 ghunt picasa example@gmail.com

Help menu
python3 ghunt --help

<h2 id="examples">Examples</h2>
python3 ghunt email xyz@gmail.com
python3 ghunt id 104938475938475
python3 ghunt picasa example@gmail.com

<h2 id="project-structure">Project Structure</h2>
GHunt/
├── ghunt                 # Main CLI script
├── assets                # Banners / Images
├── examples              # Example data
├── main.py               # Entry point (if used)
├── pyproject.toml        # Dependencies
├── README.md             # This README
├── cookies.json          # User-provided file (ignored)
└── venv/                 # Optional Python environment

<h2 id="why-this-fork">Why this fork?</h2>

Cleaner, modern README

Better user flow

Updated for Linux/Windows

Simplified installation

Ready for teaching, OSINT labs, and cyber training

<h2 id="contributing">Contributing</h2>

Fork the repo

Create a branch

Submit a PR

Keep commits focused

Never commit cookies.json or secrets

<h2 id="license">License</h2>

MIT License — open-source & free to use.

<h2 id="maintainer">Maintainer</h2>

Nitin (@nitinscodehub)
Cybersecurity & OSINT Enthusiast
GitHub: https://github.com/nitinscodehub

⚠️ Ethical Use Disclaimer

This tool is strictly for:

Ethical Hacking

Cybersecurity Research

OSINT Learning

Digital Forensics (DFIR)

Auditing Your Own Accounts

❗ Misuse = Your responsibility
❗ Illegal use can lead to legal action
❗ Always take consents & respect privacy

🛡️ AEGIS COGNITION
Parental Control & Screen-Time Manager – Chrome Extension

Aegis Cognition is a powerful yet privacy-respecting Chrome extension that helps parents and individuals:

⏱️ limit daily screen-time

🚫 automatically block distracting / harmful sites

🔐 require password for overrides and settings

👶 enable kid-safe browsing mode

🛡️ filter adult content with keywords & domains

Built entirely using Chrome Manifest V3 with no external servers or data collection.

⭐ FEATURES
⏱️ Smart Time Tracking

tracks active time per domain

resets automatically every day

works across tabs & windows

data stored locally only

🚫 Screen-Time Limits

default = no limit (infinite)

parent can set daily limits

optional per-site limits

site is blocked when time finishes

🔐 Password-Protected Override

When a website is blocked:

user sees the blocked screen

password is required to continue

domain is temporarily whitelisted

🛡️ Adult Content Filtering

Block based on:

❌ domains (ex: pornhub.com)

❌ keywords (ex: xxx, nsfw)

editable lists

🔒 Secure Settings

Password required to:

change limits

edit blocked sites

edit blocked keywords

toggle kid mode

Settings can be viewed without password, but cannot be changed without password.

👶 Kid Mode

Optional:

prevents casual tampering

keeps override password protected

blocks sensitive sites

🛠️ TECHNOLOGY STACK

✅ JavaScript (ES6)

✅ Chrome Extensions API — Manifest V3

✅ Background Service Worker

✅ Content Scripts

✅ HTML / CSS

✅ Chrome Storage API

No backend. No frameworks. No telemetry.

📂 PROJECT STRUCTURE
aegis-cognition/
│
├── manifest.json
├── background.js
├── popup.html / popup.js
├── options.html / options.js
├── blocked.html / blocked.js
├── filter.js
└── icons/ (optional)

🚀 INSTALLATION
🔧 Local Developer Install

Download or clone this repo

Open Chrome and navigate to:

chrome://extensions


Enable Developer Mode

Click Load unpacked

Select the project folder

You will now see the extension in the toolbar 🎉

📘 USAGE GUIDE
🟢 Step 1 — Set Parent Password

Open popup → Settings → Set password

🔵 Step 2 — Configure Time Limits

set minutes per day

attempting to save will require password

🟣 Step 3 — Customize Blocked Sites

Domains example:

youtube.com
instagram.com
reddit.com


Keywords example:

porn
xxx
nsfw

🔴 Step 4 — When Time Runs Out

page is blocked

password required to continue

🔐 PRIVACY POLICY

Your data never leaves your browser.

❌ no remote servers

❌ no analytics

❌ no tracking

✔ stored locally using chrome.storage.local

Password is local (hashing planned in roadmap).

🧠 IMPLEMENTATION NOTES

This project demonstrates:

Manifest V3 architecture

async event-driven service workers

secure override design UX

per-domain time tracking

safe content interception

Chrome storage synchronization

This is excellent interview discussion material.

⚠️ KNOWN LIMITATIONS

password currently stored unhashed

cannot prevent uninstalling extension

not synced across devices (yet)

some adult content may evade keyword filters

🗺️ ROADMAP

🔑 hash + salt password

☁️ cloud sync across devices

📊 usage charts / analytics dashboard

🧒 full hard-lock kid mode

🌙 incognito support

🛍 publish on Chrome Web Store

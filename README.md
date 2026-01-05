🛡 Aegis Cognition – Parental Control & Screen-Time Manager (Chrome Extension)

Aegis Cognition is a Chrome extension that helps parents and individuals reduce distraction, limit social-media screen time, and block adult content safely.

It combines:

⏱ per-site time tracking

🚫 auto-blocking when time is exhausted

🔐 password-protected override

🧑‍👧‍👦 kid-safe mode

📝 customizable domain & keyword blocklists

Built with Manifest V3, vanilla JavaScript, and Chrome APIs — no external servers or tracking.

✨ Features
⏱ Intelligent Time Tracking

tracks active browsing time per domain

resets daily

works across tabs & windows

stored locally via chrome.storage.local

🚫 Screen-Time Limits

default = no limit (infinite)

parent can set daily limit (minutes)

optional per-site limits

automatic blocking when limit reached

🔐 Password-Protected Override

When blocked:

user sees safe “blocked” page

password required to continue

approved sites are temporarily whitelisted

🛡 Adult Content Filtering

configurable keyword blocklist

configurable domain blocklist

blocks automatically on detection

🔒 Secure Settings

Password required for:

changing time limits

editing blocklists

enabling kid-mode

Settings can be opened, but cannot be changed without parent password.

👶 Kid Mode

Optional “child mode”:

prevents casual tampering

keeps override password-protected

blocks sensitive pages

🏗️ Technology Used

JavaScript (ES6)

Chrome Extensions – Manifest V3

Background Service Worker

Content Scripts

HTML / CSS

Chrome Storage API

No backend. No framework. No user tracking.

🧩 Project Structure
aegis-cognition/
│
├── manifest.json
├── background.js          # time tracking & enforcement logic
├── popup.html / popup.js  # UI showing daily usage
├── options.html           # settings page (styled)
├── options.js             # password-protected settings logic
├── blocked.html           # time limit / adult content block page
├── blocked.js             # override password logic
├── filter.js              # content filtering logic
└── icons/ (optional)

🚀 Installation
Developer Mode (local install)

Clone or download this repository

Open Chrome and go to:

chrome://extensions


Enable Developer Mode

Click Load Unpacked

Select the project folder

Extension will appear in your toolbar.

🧭 Usage Guide
1️⃣ First time setup

open extension popup

click Settings

set a parent password

2️⃣ Set screen-time limits

enter daily minutes

save

password will be requested

3️⃣ Add blocked sites or keywords

Examples:

youtube.com
instagram.com
reddit.com


Keywords example:

porn
xxx
nsfw

4️⃣ When time is up

extension blocks the site

override requires password

🔐 Privacy & Data Policy

Your data stays on your device.

❌ no servers

❌ no analytics

❌ no tracking

✔ local storage only (chrome.storage.local)

✔ inspectable source code

Password is currently stored in plain text locally
(optional upgrade: hashing supported — see roadmap)

🛠️ Implementation Details

This project demonstrates:

manifest v3 lifecycle management

service workers vs background pages

Chrome storage event synchronization

dynamic content blocking architecture

secure override flows

UX constraints inside popup environment

Excellent talking points for technical interviews.

🧭 Known Limitations

password is stored unhashed locally

cannot prevent user from uninstalling extension

some adult sites rely on obfuscation

time tracking does not sync across devices (yet)

🗺️ Roadmap

🔑 hash & salt password before storage

🌐 Firebase / cloud sync for families

📊 weekly analytics dashboard

🧑‍👧‍👦 full “hard” kid-lock mode

🌙 incognito support

🛍 publish to Chrome Web Store

Pull requests welcome.

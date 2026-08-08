# VirusTotal Telegram Bot 🦠

A Telegram bot that scans URLs, files, hashes and IPs
using the VirusTotal API.

Breaking Bad themed. *I am the one who scans.*

> ⚠️ For personal and educational use only.

---

## What's Inside

```
vt-telegram-bot/
│
├── bot.py
├── .env.example
├── requirements.txt
├── README.md
├── LICENSE
└── .gitignore
```

---

## What It Can Scan

| Send this | Example |
|-----------|---------|
| URL | `https://example.com` |
| MD5 hash | `d41d8cd98f00b204e9800998ecf8427e` |
| SHA1 hash | `da39a3ee5e6b4b0d3255bfef95601890` |
| SHA256 hash | `e3b0c44298fc1c149afb...` |
| IP address | `1.2.3.4` |
| File | Upload any file up to 32MB |

---

## What You Get Back

```
🚨 Malicious:   3
⚠️  Suspicious:  1
✅ Harmless:    65
❓ Undetected:  4

💀 Risk Score: 🔴 [████░░░░░░] 72/100

🔍 Flagged by:
  🔴 Kaspersky: malware
  🔴 BitDefender: trojan
```

---

## Commands

```
/start      — Welcome screen
/help       — How to use the bot
/stats      — Your scan history stats
/history    — Last 5 scans
/report     — Your personal threat report
/watch      — Monitor a URL or IP daily
/watchlist  — See what you are watching
/unwatch    — Stop monitoring something
```

---

## Setup

### 1. Get your API keys

| Key | Where to get it |
|-----|----------------|
| `VT_API_KEY` | https://virustotal.com |
| `TELEGRAM_TOKEN` | @BotFather on Telegram |

### 2. Clone and install

```bash
git clone https://github.com/auguxt/vt-telegram-bot.git
cd vt-telegram-bot
pip install -r requirements.txt
```

### 3. Set up your keys

```bash
cp .env.example .env
nano .env
```

Fill in:
```
VT_API_KEY=your_key_here
TELEGRAM_TOKEN=your_token_here
```

### 4. Run

```bash
python bot.py
```

---

## Example Output

**Safe URL:**
```
✅ Yeah science, bitch! It's clean!
Risk Score: 🟢 [░░░░░░░░░░] 0/100
Zero out of 80 engines raised an alarm.
```

**Dangerous URL:**
```
☣️ I AM the danger. And THIS is the danger.
Risk Score: 🔴 [████████░░] 85/100
Flagged by: Kaspersky, BitDefender, ESET
```

---

## ⚠️ Important

- Free VirusTotal API = 4 requests per minute
- Never commit your `.env` file
- Never commit `.session` files — they contain your tokens
- Max file size = 32MB

---

## Requirements

- Python 3.8+
- VirusTotal API key (free)
- Telegram Bot token

---

## License

MIT — see [LICENSE](LICENSE)

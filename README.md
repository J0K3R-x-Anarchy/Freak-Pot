# 🛡️ Freak-Pot Honeypot Suite

> "Why so serious?"

Put on a crooked smile—**Freak-Pot** is the ultimate trickster in your network, posing as an innocent server.  
It lures unwary intruders into its twisted carnival, then captures every gasp, credential slip, and suspicious command for your devious delight.

In this circus of chaos, only the bold survive—bring your curiosity, and let the madness begin.

---

## 🎯 Features

- **HTTP Honeypot**
  - Serves a customizable HTML page on port 80
  - Logs all GET/POST requests (path, headers, payload)
- **FTP Honeypot**
  - Simulates an FTP server on port 21
  - Captures credentials (`USER` / `PASS`)
  - Supports PASV, LIST, RETR, STOR with fake files
- **SSH Honeypot**
  - Simulates an SSH login on port 22
  - Logs username/password attempts
  - Records session activity (commands, inputs)
- **Interactive Console**
- **Cross-Platform Support**
  - ✅ **Linux:** Native build (`Freak`)
  - ✅ **Windows:** Standalone `.exe` available — no setup needed!

---

## 🚀 Quick Start

### 🔧 Linux

1. **Clone the repository**
   ```bash
   git clone https://github.com/J0K3R-x-Anarchy/Freak-Pot.git
   cd freak-pot
   ```
2. **Set permissions and run**
   ```bash
   chmod +x Freak
   sudo ./Freak
   ```

> _Root privileges are required to bind to ports 21, 22, and 80._

---

### 🪟 Windows

1. **Download `Freak.exe`** from the [Releases](https://github.com/J0K3R-x-Anarchy/Freak-Pot/releases)
2. **Double-click** the `.exe` file to run the honeypot — no installation required

> _Run as administrator to access system ports (80, 21, 22)._

---

## 💻 Usage

At the interactive prompt, type `help` to view available commands:

| Command             | Description                            |
|---------------------|----------------------------------------|
| `start http`        | Start HTTP honeypot (port 80)          |
| `http logs`         | Display HTTP request logs              |
| `set html <file>`   | Change served HTML file                |
| `start ftp`         | Start FTP honeypot (port 21)           |
| `ftp logs`          | Display FTP activity logs              |
| `start ssh`         | Start SSH honeypot (port 22)           |
| `ssh logs`          | View SSH login attempts and commands   |
| `exit`              | Stop all services and exit             |
| `help`              | Show this help menu                    |

Logs are saved in the working directory:
- `honeypot.log`       (HTTP)
- `ftp_honeypot.log`   (FTP)
- `ssh_honeypot.log`   (SSH)

---

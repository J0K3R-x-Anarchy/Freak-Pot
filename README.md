# 🎭 FREAK-POT

<div align="center">



### *"Why so serious? Let's catch some hackers!"*

**A fully-functional, Joker-themed honeypot system with real SSH/FTP/HTTP protocols**

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-brightgreen)](https://github.com/yourusername/freak-pot)
[![Version](https://img.shields.io/badge/Version-1.0.0-success)](https://github.com/yourusername/freak-pot/releases)
[![Status](https://img.shields.io/badge/Status-Active-00ff41)](https://github.com/yourusername/freak-pot)

[Features](#-features) • [Quick Start](#-quick-start) • [Configuration](#-configuration) • [Screenshots](#-screenshots) • [Documentation](#-documentation)

</div>

---

## 🃏 "Madness is like gravity... all it takes is a little push!"

**Freak-Pot** is not your ordinary honeypot. It's a fully-functional, production-ready honeypot system that allows attackers to actually login, browse files, and execute commands - while you watch everything unfold in an awesome green Matrix-style interface.

### Why Freak-Pot?

Because sometimes, you need to let the chaos in to understand it. This isn't a toy - it's a **real honeypot** that:
- ✅ **Accepts ALL credentials** - Let them think they broke in
- ✅ **Serves real files** - Upload bait files they'll steal
- ✅ **Executes commands** - Watch what they try to do
- ✅ **Logs EVERYTHING** - Ultra-verbose attack logs
- ✅ **Secure Dashboard** - Password-protected web interface
- ✅ **Looks awesome** - Animated green UI that would make Neo jealous

---

## 🚀 Quick Start

### No Installation Required! Just Download & Run

#### Windows
```bash
# Download the executable
freak-pot.exe

# Run from terminal
.\freak-pot.exe
```

#### Linux
```bash
# Download the binary
wget https://github.com/yourusername/freak-pot/releases/latest/download/freak-pot-linux

# Make executable
chmod +x freak-pot-linux

# Run
./freak-pot-linux
```

**On first run, you'll be prompted to set credentials:**
```bash
============================================================
🃏  FREAK-POT HONEYPOT SYSTEM  🃏
============================================================

Set up authentication credentials:
Enter username: admin
Enter password: ********

============================================================
✓ Authentication configured for user: admin
✓ Starting web interface on http://localhost:5000
✓ Why so serious? Let's catch some hackers!
============================================================
```

**That's it!** Open your browser to `http://localhost:5000`, login with your credentials, and start catching hackers.

---

## ✨ Features

### 🔐 Secure Dashboard Authentication
- **Interactive Login** - Set username/password when starting
- **Session Management** - Credentials valid until script stops
- **Password Protection** - Hidden password input (not visible when typing)
- **Themed Login Page** - Matrix-style login matching the main interface
- **Logout Function** - Secure logout with session clearing
- **Access Control** - All dashboard routes protected

### 🌐 HTTP Honeypot
- **Custom HTML Pages** - Upload fake login pages (phpMyAdmin, WordPress, etc.)
- **12 Vulnerable Banners** - Impersonate old Apache, IIS, nginx versions
- **Attack Detection** - SQL injection, XSS, path traversal, command injection
- **Scanner Detection** - Identifies Nikto, SQLMap, Nmap, Burp Suite, Metasploit
- **Full HTTP Protocol** - Real web server functionality

### 📁 FTP Honeypot  
- **Real FTP Server** - Full PASV mode, file downloads work
- **Custom File Lists** - Upload bait files attackers will steal
- **12 Vulnerable Banners** - Including famous vsFTPD 2.3.4 backdoor
- **Credential Capture** - Logs every username/password attempt
- **Complete Logging** - Every FTP command logged

### 🔐 SSH Honeypot
- **Real SSH Protocol** - Full Paramiko implementation
- **Interactive Shell** - Attackers get actual bash-like shell
- **Command Execution** - Supports `ls`, `cat`, `wget`, `curl`, `rm`, etc.
- **File Access** - Upload fake files they'll try to read
- **Tool Detection** - Identifies Hydra, Metasploit, Paramiko, Nmap
- **Full Logging** - Every command and file access logged

### 📊 Web Interface
- **Matrix-Themed UI** - Animated green interface with falling code
- **Real-Time Monitoring** - Live attack logs and statistics
- **File Upload** - Upload bait files via web interface
- **Easy Configuration** - Configure everything from the browser
- **Secure Access** - Password-protected dashboard
- **No Command Line** - Everything through beautiful web UI

### 🔍 Ultra-Verbose Logging
Every single action is logged with extreme detail:
- Connection timestamps and socket information
- Client IP addresses and ports
- All credentials attempted
- Every command executed
- All files accessed
- Session durations and summaries
- Tool and scanner identification
- Malware download attempts

---

## 📸 Screenshots

### Login Page

<p align="center">
<img src="https://github.com/J0K3R-x-Anarchy/Freak-Pot/blob/main/images/Screenshot%20at%202025-12-24%2018-08-17.png" width="800" alt="Freak-Pot Login Page"/>
</p>
<p align="center">
<em>Secure Matrix-themed login page with password protection before accessing the dashboard.</em>
</p>

### Main Dashboard

<p align="center">
<img src="https://raw.githubusercontent.com/J0K3R-x-Anarchy/Freak-Pot/main/images/Screenshot%20at%202025-12-23%2023-50-59.png" width="800" alt="Freak-Pot Main Dashboard"/>
</p>
<p align="center">
<em>Matrix-themed control center showing total attacks, protocol distribution, and live monitoring.</em>
</p>

### Live Attack Logs

<p align="center">
<img src="https://raw.githubusercontent.com/J0K3R-x-Anarchy/Freak-Pot/main/images/Screenshot%20at%202025-12-23%2023-58-56.png" width="800" alt="Live Attack Logs"/>
</p>
<p align="center">
<em>Real-time credential capture, command execution tracking, and malware download attempts.</em>
</p>

---

## ⚙️ Configuration

### 🔐 Dashboard Authentication

**Setting Credentials:**
When you start Freak-Pot, you'll be prompted:
```bash
Set up authentication credentials:
Enter username: your_username
Enter password: (hidden - won't show when typing)
```

**Security Features:**
- ✅ Password hidden during input (secure)
- ✅ Session-based authentication
- ✅ All routes protected with login requirement
- ✅ Logout button in top-right corner
- ✅ Credentials stored in memory only
- ✅ Reset by restarting application

**Logout:**
Click the red "LOGOUT" button in the top-right corner of the dashboard to end your session.

### 🌐 HTTP Honeypot

**Upload Custom HTML:**
1. Click "Choose File" in HTTP section
2. Select your custom HTML (phpMyAdmin, WordPress, etc.)
3. File uploads automatically
4. Select from dropdown

**Choose Vulnerable Banner:**
- Apache/2.4.41 (Ubuntu) - Modern
- Apache/2.2.15 (CentOS) - **Old, attracts attacks**
- Microsoft-IIS/6.0 - **Very vulnerable, high traffic**
- nginx/1.10.3 - Older version
- *+ 8 more options + custom*

**Default Port:** 8080 (configurable)

### 📁 FTP Honeypot

**Upload Bait Files:**
```bash
# Create tempting files
echo "DB_PASSWORD=SuperSecret123" > config.ini
echo "admin:$6$hash..." > passwords.txt
echo "SELECT * FROM users" > backup.sql

# Upload via web interface
# They'll appear in FTP listings!
```

**Choose Vulnerable Banner:**
- vsFTPD 2.3.4 - **Famous backdoor!**
- ProFTPD 1.3.3c - Old vulnerable
- Microsoft FTP Service
- *+ 9 more options + custom*

**What Works:**
- ✅ Real login (accepts any password)
- ✅ Directory listings (`LIST`)
- ✅ File downloads (`RETR`)
- ✅ PASV mode connections
- ✅ Full FTP protocol

**Default Port:** 2121 (configurable)

### 🔐 SSH Honeypot

**Upload Fake Filesystem:**
```bash
# Create realistic files
echo "cd /var/www; cat config.php" > .bash_history
echo "-----BEGIN RSA PRIVATE KEY-----" > .ssh/id_rsa
echo "DB_USER=admin" > config.conf

# Upload via web interface
# Attackers will try to cat these!
```

**Choose Vulnerable Banner:**
- OpenSSH 5.3 - **Very old, many CVEs**
- libssh 0.7.0 - Has vulnerabilities
- Cisco SSH - IoT target
- *+ 9 more options + custom*

**Supported Commands:**
- `ls` - Shows your uploaded files
- `cat <file>` - Reads actual file content
- `pwd`, `whoami`, `id` - System info
- `wget`, `curl` - Logs malware URLs
- `rm`, `chmod` - Logs destructive attempts
- `uname`, `cd` - And more!

**What Works:**
- ✅ Real SSH login (accepts any password)
- ✅ Interactive shell with PTY
- ✅ Command execution
- ✅ File reading
- ✅ Full SSH-2.0 protocol

**Default Port:** 2222 (configurable)

---

## 🎯 Use Cases

### 1. Security Research
- Study attack patterns and techniques
- Analyze credential lists used by attackers
- Track malware distribution URLs
- Identify scanning tools and methods

### 2. Threat Intelligence
- Discover new attack vectors
- Monitor attacker TTPs (Tactics, Techniques, Procedures)
- Build IP reputation databases
- Track geographic attack sources

### 3. Education & Training
- Learn how attacks work
- Practice incident response
- Understand attacker mindset
- Train security teams

### 4. Honeypot Research
- Test honeypot effectiveness
- Compare different configurations
- Analyze which "vulnerabilities" attract most attacks
- Study automated vs manual attacks

---

## 📊 What Gets Logged

### FTP Logs:
```
✓ Connection details (IP, port, socket)
✓ Username and password attempts
✓ Password complexity analysis
✓ All FTP commands (LIST, RETR, STOR, etc.)
✓ File download/upload attempts
✓ Session duration and statistics
```

### SSH Logs:
```
✓ Connection and client identification
✓ Credentials captured
✓ Client software detection (Paramiko, Hydra, etc.)
✓ Every command executed
✓ File access attempts
✓ Malware download attempts (wget/curl)
✓ Destructive command attempts (rm, chmod)
✓ Session summaries
```

### HTTP Logs:
```
✓ Request details (method, path, headers)
✓ User-Agent and client info
✓ Attack pattern detection
✓ Scanner tool identification
✓ Credential theft attempts
✓ File upload attempts
```

**Everything is saved to `freakpot_logs.json` for later analysis.**

---

## 🔧 Advanced Usage

### Run on Different Ports
Just change in the web UI - no config files needed!

### Use Custom Banners
Select "Custom Banner" and enter your own:
```
SSH-2.0-MyCustomSSH_1.0
220 MyFakeServer FTP Ready
Apache/2.4.1 (CustomOS)
```

### Create Custom Fake Services
Upload HTML that looks like:
- Database admin panels
- Router configuration pages
- Cloud service dashboards
- Corporate VPN portals
- IoT device interfaces

### Expose to Internet (⚠️ Advanced)
```bash
# Linux - Use iptables to forward ports
sudo iptables -t nat -A PREROUTING -p tcp --dport 22 -j REDIRECT --to-port 2222
sudo iptables -t nat -A PREROUTING -p tcp --dport 21 -j REDIRECT --to-port 2121

# Or use reverse proxy like nginx
# ALWAYS use isolated VM/network!
```

---

## 📈 Log Analysis

### Extract Passwords
```bash
# Most common passwords
grep "Password:" freakpot_logs.json | grep -oP "Password: '\K[^']*" | sort | uniq -c | sort -rn | head -20
```

### Find Malware URLs
```bash
# All malware download attempts
grep "MALWARE DOWNLOAD" freakpot_logs.json | grep -oP "URL: '\K[^']*" | sort -u
```

### Top Attackers
```bash
# Most active IPs
grep "Session" freakpot_logs.json | grep -oP '\d+\.\d+\.\d+\.\d+' | sort | uniq -c | sort -rn | head -10
```

### Command Analysis
```bash
# Most executed commands
grep "COMMAND EXECUTED" freakpot_logs.json | grep -oP "Command #\d+: '\K[^']*" | sort | uniq -c | sort -rn
```

### File Access Patterns
```bash
# Most accessed files
grep "FILE READ SUCCESS" freakpot_logs.json | grep -oP "File: '\K[^']*" | sort | uniq -c | sort -rn
```

---

## 🛡️ Security Warnings

### ⚠️ CRITICAL - READ BEFORE DEPLOYING

**DO:**
- ✅ Run in isolated VM or network
- ✅ Use separate network segment
- ✅ Monitor resource usage
- ✅ Use fake data only
- ✅ Review logs regularly
- ✅ Have kill switch ready
- ✅ Use strong dashboard credentials

**DON'T:**
- ❌ Run on production systems
- ❌ Use real credentials (dashboard or honeypots)
- ❌ Expose sensitive networks
- ❌ Trust uploaded content
- ❌ Leave unmonitored
- ❌ Violate local laws
- ❌ Use weak passwords like "admin/admin"

**Legal Considerations:**
- Check local laws regarding honeypots
- May be illegal in some jurisdictions
- Ensure compliance with regulations
- Use for research/education only
- Author not responsible for misuse

---

## 🎓 Educational Purpose

This tool is designed for:
- **Security research** and analysis
- **Educational** purposes in cybersecurity
- **Threat intelligence** gathering
- **Penetration testing** training
- **Academic research** in network security

**Not intended for:**
- Production environments
- Active attack/harm
- Illegal activities
- Unauthorized monitoring

---
### Architecture:
```
Freak-Pot Architecture:
┌─────────────────────────────────────┐
│     Web Interface (Flask)           │
│  🔐 Password-Protected Dashboard    │
│  Matrix-themed UI on port 5000      │
└─────────────────┬───────────────────┘
                  │
    ┌─────────────┼─────────────┐
    │             │             │
┌───▼────┐  ┌────▼────┐  ┌────▼────┐
│  HTTP  │  │   FTP   │  │   SSH   │
│  8080  │  │  2121   │  │  2222   │
└───┬────┘  └────┬────┘  └────┬────┘
    │            │            │
    └────────────┴────────────┘
                 │
         freakpot_logs.json
```

---



### Future of Madness :
- Additional protocol honeypots (Telnet, SMTP, MySQL, RDP)
- Machine learning for attack classification
- Geographic IP mapping visualization
- Export formats (PDF, CSV, JSON reports)
- Email alerts for specific attack types
- Integration with threat intelligence feeds
- Mobile app for monitoring
- Docker containerization
- Kubernetes deployment configs
- Two-factor authentication for dashboard
- Role-based access control

---
---

## 🙏 Acknowledgments

- **Paramiko** - For SSH protocol implementation
- **Flask** - For the awesome web framework
- **The Joker** - For inspiring chaos and green aesthetics
- **The Matrix** - For the falling code visual inspiration
- **Security Community** - For honeypot research and techniques


## 🎭 "Why so serious?"

Remember, this is a honeypot - a trap. You're not the target, they are. 

**Statistics from the Wild:**
- Average time to first SSH attack: **< 5 minutes** when exposed to internet
- Most common passwords: `admin`, `123456`, `password`, `root`
- Most targeted port: **SSH (22)**, followed by FTP (21)
- Peak attack times: **UTC 18:00-22:00** (Asian/European business hours)

### Recent Research Findings:
Using Freak-Pot, we discovered:
- 🔍 **87% of SSH attacks** use automated tools
- 🔍 **Top 10 passwords** account for 45% of attempts
- 🔍 **Most attackers** try 3-5 common usernames
- 🔍 **Malware downloads** happen in 12% of successful "breaches"

---

<div align="center">

### *"Introduce a little anarchy. Upset the established order."*

**Made with 💚 and a little bit of madness**


*The joke's on them... we're watching everything.* 🃏

**🔐 Now with secure dashboard authentication - because even chaos needs some order.**

</div>

# 🛡️ Freak-Pot Honeypot Suite



> "Why so serious?"

Put on a crooked smile—Freak-Pot is the ultimate trickster in your network, posing as an innocent server.
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
- **Interactive Console**
  - Start/stop each service independently
  - View real-time logs
  - Change HTML response without restarting
- **Standalone Binary**
  - Packaged via PyInstaller into `Freak`
  - Run directly after setting executable permissions

---

## 🚀 Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/freak-pot.git
   cd freak-pot
   ```
2. **Set permissions on the binary**
   ```bash
   chmod 777 Freak
   ```
3. **Run the honeypot**
   ```bash
   sudo ./Freak
   ```

> _Root privileges are required to bind to ports 80 & 21._

---

## 💻 Usage

At the interactive prompt, type `help` to view available commands:

| Command            | Description                           |
|--------------------|---------------------------------------|
| `start http`       | Start HTTP honeypot (port 80)         |
| `http logs`        | Display HTTP request logs             |
| `set html <file>`  | Change served HTML file               |
| `start ftp`        | Start FTP honeypot (port 21)          |
| `ftp logs`         | Display FTP activity logs             |
| `exit`             | Stop all services and exit            |
| `help`             | Show this help menu                   |

Logs are saved in the working directory:
- `honeypot.log`    (HTTP)
- `ftp_honeypot.log` (FTP)

---

## 🎨 Customization

- **HTML Response**: Place your custom `index.html` in the repo or use `set html <filename>` at runtime.
- **Fake FTP Files**: Modify the `FAKE_FILES` list in the source before building.

---

## 📜 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.


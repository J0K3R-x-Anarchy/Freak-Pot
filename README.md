Freak-Pot Honeypot Suite

Features

HTTP Honeypot:

Serves a customizable HTML page on port 80

Logs all GET/POST requests (path, headers, payload)

FTP Honeypot:

Simulates an FTP server on port 21

Captures credentials (USER / PASS)

Supports PASV, LIST, RETR, STOR with fake files

Interactive Console:

View logs

Change served HTML file

Start/stop HTTP & FTP services independently

Quick Start

Clone the repo

git clone https://github.com/<your-username>/freak-pot.git
cd freak-pot

Set executable permissions on the binary

chmod 777 Freak

Run the honeypot

sudo ./Freak

Note: Root privileges are required to bind ports 80 & 21.

Console Commands

Once launched, use the interactive prompt:

[Freak] > help
+----------------------+------------------------------------------+
| Command              | Description                              |
+----------------------+------------------------------------------+
| start http           | Start HTTP honeypot (port 80)            |
| http logs            | View HTTP log entries                    |
| set html <file>      | Change HTML response file                |
| start ftp            | Start FTP honeypot (port 21)             |
| ftp logs             | View FTP log entries                     |
| exit                 | Stop honeypots & exit                    |
| help                 | Show this menu                           |
+----------------------+------------------------------------------+

http logs → prints honeypot.log

ftp logs  → prints ftp_honeypot.log

Logs appear in the working directory.

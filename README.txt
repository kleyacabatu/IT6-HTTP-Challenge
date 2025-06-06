# IT6 CTF:  3-Digit PIN Challenge

## 🔍 Objective
Guess the correct 3-digit numeric PIN (000–999) of a local web server by crafting raw HTTP requests using Python and sockets only.

## 📜 How It Works
- A local `.exe` web server runs on `127.0.0.1:8888`
- Script iterates through every possible 3-digit pin
- Sends a POST request like:

POST / HTTP/1.1
Host: 127.0.0.1:8888
Content-Type: application/x-www-form-urlencoded
Content-Length: 7

pin=042

- Checks response for a success message

## 🛠 Technical Details
- Language: Python 3
- Libraries used: `socket`, `time`
- Constraint: No external HTTP libraries (e.g., `requests`)

## 🧠 Lessons Learned
- Learned how to use `socket` to create HTTP requests manually
- Understood brute-force attack limitations and server constraints
- Practiced reverse engineering a server’s expected input and output

## 🛡️ Security Suggestions
- Rate-limit requests per IP
- Add CAPTCHA or 2FA
- Lock out users after X failed attempts

## 📹 Video Presentation
*(https://drive.google.com/file/d/1nv_jJ5Gkxk2jQMQMy6hMIDDCBxM_TmJL/view?usp=sharing)*

## 👨‍💻 Author
Kley Aroes – Integrative Programming and Technologies (IT6)

# 🛡️ Password Checker | مدقق كلمات المرور

A privacy-first password strength checker and breach-detection tool that runs entirely in the browser.

🔗 **Live:** https://taif-alkhodidi1.github.io/password-checker

## ✨ Features
- **Strength analysis** based on entropy (character pool × length)
- Live strength meter, estimated crack time, and a checklist (length, upper/lowercase, digit, symbol, common-password detection)
- **Breach check** via the Have I Been Pwned API using **k-anonymity** — only the first 5 characters of the SHA-1 hash are sent; the password itself never leaves the browser
- Bilingual: Arabic (RTL) / English (LTR)
- Zero frameworks — pure HTML, CSS & JavaScript

## 🔒 How the breach check stays private
1. The password is hashed locally with **SHA-1** using the Web Crypto API.
2. Only the first **5 characters** of the hash are sent to the API.
3. The API returns all hash suffixes starting with that prefix.
4. The match is found **locally** in the browser.

The server never sees the password or its full hash.

## 🛠️ Built With
`HTML5` `CSS3` `JavaScript` `Web Crypto API` `Have I Been Pwned API`

## 🚀 Run Locally
Open `index.html` in any modern browser. The breach check needs an internet connection.

---
© Taif Alkhodidi

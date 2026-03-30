# 🏁 MythX: EndGame PR0T0C0L — CTF Writeup

> A complete walkthrough of challenges from the MythX CTF, covering real-world inspired vulnerabilities across multiple security domains.  

## 🚀 Overview

This repository contains my full writeup for the **MythX: EndGame PR0T0C0L CTF**.

The challenges focused on identifying weak implementations, misconfigurations, and hidden data across different layers - from cryptography to web applications and digital forensics.  

## 🧠 Skills & Domains Covered

| Domain              | Concepts Explored |
|--------------------|------------------|
| 🔐 Cryptography     | ROT13, Caesar Cipher, XOR attacks, RSA Common Factor |
| 🌐 Web Exploitation | Headers, Redirect Chains, robots.txt, API behavior |
| 🧪 Forensics        | LSB Steganography, File Carving, Data Appending |
| 🕵️ OSINT           | Metadata Analysis, Timeline Reconstruction |
| ⚙️ Reverse Engg.    | JavaScript Deobfuscation, Source Maps |  

## 🧩 Challenge Highlights

### 🔹 Cryptography
- Broke RSA using shared prime factor (`gcd(n1, n2)`)
- Recovered XOR key via known-plaintext attack
- Decoded layered encodings (Base64 → Base32 → Hex → ROT13 → Reverse)

### 🔹 Web Exploitation
- Extracted flags from HTTP headers across redirect chains
- Bypassed hidden paths via `robots.txt` and `sitemap.xml`
- Manipulated API behavior using custom headers

### 🔹 Forensics
- Extracted hidden ZIP appended inside PNG files
- Recovered secret data using LSB audio steganography

### 🔹 Reverse Engineering
- Decompiled client-side JavaScript vault logic
- Extracted sensitive data from exposed source maps  

## 🛠️ Tools & Technologies

- CyberChef -> Encoding/Decoding  
- exiftool -> Metadata extraction  
- binwalk -> File carving  
- netcat (nc) -> Remote interaction  
- curl -> HTTP requests  
- Python -> Automation & scripting  
- Browser DevTools -> JS debugging & analysis  

## 📄 Full Writeup

📘 The complete detailed writeup is available here:

👉 [MythX_CTF_Writeup.pdf](./MythX_CTF_Writeup.pdf) 

## 📊 CTF Stats

- 🧮 Challenges Solved: 15  
- 🧩 Categories: Crypto, Web, Forensics, OSINT, RE  
- ⚙️ Difficulty: Beginner → Intermediate  
- 🕒 Approach: Manual + Script-assisted  

## 🎯 Key Takeaways

- ⚠️ Reused cryptographic parameters can completely break encryption  
- 🌐 HTTP headers and metadata often leak sensitive information  
- 🧠 Client-side security is fundamentally flawed  
- 📦 File formats can conceal data beyond visible boundaries  
- 🔁 Automation is crucial for multi-step transformations  

## 🔥 Notable Concepts

- RSA Common Factor Attack  
- XOR Key Recovery via Zero Plaintext  
- LSB Steganography (Audio)  
- HTTP Header Exploitation  
- Source Map Leakage  

## 📸 Proof of Work

Screenshots and evidence include:

- Tool usage (CyberChef, exiftool, binwalk)  
- Network interaction (nc, curl)  
- Decoding workflows  
- Extracted flags  

(All included inside the PDF writeup) 

## 🤝 Connect

- 📝 Medium Writeup: [MythX: An EndGame PR0T0C0L](https://medium.com/@aN0niMiTTy/mythx-an-endgame-pr0t0co0l-140f12a0f650)     

## ⭐ Final Note

This CTF provided practical exposure to real-world vulnerabilities and reinforced the importance of analyzing systems beyond surface-level behavior. 

> ⚡ If you found this useful, consider giving this repo a ⭐

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

```bash
CyberChef     # Encoding/Decoding
exiftool      # Metadata extraction
binwalk       # File carving
nc (netcat)   # Remote interaction
curl          # HTTP requests
Python        # Automation & scripting
DevTools      # JS debugging & analysis

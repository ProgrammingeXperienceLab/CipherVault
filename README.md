# CipherVault

CipherVault - A lightweight, client-side encryption tool with a retro-neon cyberpunk interface.  
CipherVault allows users to securely encrypt and decrypt messages entirely in the browser without sending any data to a server.

**Try it Online:** [https://programmingexperiencelab.github.io/CipherVault/](https://programmingexperiencelab.github.io/CipherVault/)


---

## Overview

CipherVault is developed by **PXL – Programming eXperience Lab**. Its main goal is to provide a secure, privacy-focused encryption experience for messages with a modern, retro-neon UI. It runs fully client-side using the browser's Web Crypto API.

**Platform:** Web (HTML, CSS, JavaScript, Web Crypto API)  
**Audience:** Privacy-conscious users, developers, and encryption enthusiasts.

---

## Features

### Message Encryption
- Type a message and password.
- Encrypts client-side using **AES-GCM 256-bit**.
- Generates a random salt (16 bytes) and IV (12 bytes) per message.
- Output is **Base64 encoded** for easy sharing.

### Message Decryption
- Requires the encrypted message and the same password.
- Decrypts using AES-GCM with derived key.
- Provides clear feedback if decryption fails (e.g., wrong password).

### Password Strength Enforcement
- Minimum 12 characters.
- Must include uppercase, lowercase, number, and special character.
- Alerts user if password is weak.

### Security-Oriented UX
- Automatically clears input and output fields after use.
- Optional “Matrix-style” animated background without performance impact.

### Responsive Design
- Works on desktop and mobile.
- Uses **backdrop-filter** and animated glitch effects for cyberpunk look.

---

## Architecture

### Frontend UI
- HTML5, CSS3, JavaScript
- Canvas-based matrix-style animation
- Input forms, buttons for encryption/decryption
- Auto-clearing output textarea

### Security Module
- **Key Derivation:** PBKDF2 with SHA-256, 500,000 iterations
- **Randomness:** Crypto API generates salt and IV
- **Encryption:** AES-GCM 256-bit
- **Encoding:** Base64
- **Memory Hygiene:** Sensitive fields cleared after use

### Event Handlers
- Async functions handle encryption/decryption
- Password strength validation
- Click events on buttons

---

## Security Design
- **AES-GCM:** Ensures confidentiality and integrity
- **PBKDF2 with SHA-256:** Resists brute-force attacks
- Unique salt & IV per message
- Input/output auto-clear for memory safety
- HTTPS recommended for transport security

---

## Comparison

| Feature | CipherVault | Typical Alternatives |
|---------|------------|--------------------|
| Encryption Standard | AES-GCM 256-bit | AES-CBC / JS XOR |
| Key Derivation | PBKDF2 500k iterations | Weak or static keys |
| Client-Side Only | Yes | Often uses cloud |
| Automatic Field Clearing | Yes | Often absent |
| Retro-Neon UI | Matrix-style animation | Minimalist / generic |
| Password Enforcement | Strong enforced | Optional or absent |
| Base64 Output | Easy copy/paste | Sometimes binary only |

---

## Limitations
- Dependent on modern browser Crypto API
- Password strength is critical
- Not optimized for very large files or messages

---

## Future Enhancements
- Multi-file encryption support
- Optional passphrase hints
- WebAssembly integration for speed
- Export/import encrypted messages as `.pxl` files

---

## Summary
CipherVault is a secure, client-side encryption tool combining AES-GCM, PBKDF2, strong password enforcement, memory hygiene, and a cyberpunk UI for a unique, privacy-focused experience.

---

## License & Usage
© 2025 **PXL – Programming eXperience Lab**. All rights reserved.  

You may use this software **for personal purposes only**.  
**Modification, redistribution, or commercial use is strictly prohibited.**

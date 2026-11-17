<div align="center">

<a href="https://blog.dei3c.com" target="_blank" rel="noopener noreferrer">
  <img src="https://github.com/user-attachments/assets/2830eb70-512c-4ddb-87ec-5213a6e465b1" alt="得翼科技 | LINE Digital Business Card System" height="70" />
</a>

<br /><br />

[繁體中文](../../README.md) · [简体中文](README_zh-CN.md) · **English**

# LINE Digital Business Card System

### Self-hosted business cards with QR Code, vCard and LINE Flex Message

[![Platform](https://img.shields.io/badge/Platform-Docker-blue?style=flat-square)](https://github.com/robert820/line-business-card)
[![License](https://img.shields.io/badge/License-Freeware-informational?style=flat-square)](../../LICENSE)
[![Status](https://img.shields.io/badge/Status-In%20Development-orange?style=flat-square)](#-current-status)

</div>

---

## 📖 Overview

Create many digital business cards from one admin console, each with its own public URL, layout and contact data. Visitors can scan the QR Code, download the vCard, copy contact details or share through LINE.

This is a **self-hosted** system, not a cloud SaaS: card data and images stay on the server or NAS you manage.

---

## 📌 Current status

> Currently validated on local Docker Desktop (amd64); real NAS, arm64 and HTTPS reverse-proxy environments are not yet validated.

---

## ✨ Features

### 1. 🗂️ Manage many cards in one place
- Add, edit, duplicate and search cards; manage draft, published and archived states (single administrator).

### 2. 🎨 Two layouts with live preview
- Classic Business and Modern Vertical layouts with colour choices, previewed live while editing.

### 3. 🔗 One public URL per card
- Visitors open `/c/:slug` without logging in, and can copy the URL, copy contact info or navigate on a map.

### 4. 📱 QR Code and vCard
- Scan the QR Code with a phone, or download the vCard to add the contact.

### 5. 💬 LINE sharing and Flex Message
- Share or send cards via LIFF, and view / download the Flex JSON to preview it in the official Flex Simulator.

### 6. 🔒 Admin login protection
- Server-side sessions and Argon2id password hashing; production needs a strong `SESSION_SECRET` and HTTPS.

---

## 💻 Scope & limitations

| Item | Requirement / status | Notes |
| :--- | :--- | :--- |
| Server | Docker and Compose | Deployable on a NAS or Linux host; the SQLite database and uploaded images live on a persistent volume |
| Public cards & LINE images | HTTPS domain recommended | Set `PUBLIC_BASE_URL`; images shown in LINE must be reachable over HTTPS |
| LIFF | Optional integration | Set `LIFF_ID` to enable the LINE share entry; public cards still work without it |
| Deployment validation | Local Docker Desktop amd64 | Real NAS, arm64 and HTTPS reverse-proxy environments are not yet validated |

---

## 🚀 Workflow

1. Prepare a NAS or server with Docker Compose, copy the example environment file and generate a dedicated `SESSION_SECRET`.
2. Create the administrator account, start the container and make sure the database and upload directory sit on a persistent volume.
3. Set up an HTTPS reverse proxy and the public URL, then log in to the admin console to create and publish cards.
4. Test the QR Code, vCard and image links on the public card page; configure LIFF only when you need LINE sharing.

---

## 📦 Download

No downloadable build has been released yet. Once released, it will be provided on the [Releases page](https://github.com/robert820/line-business-card/releases).

---

## 🖥️ Requirements

- **Deployment**: Docker and Docker Compose (NAS or Linux host)
- **Backend**: Rust, Axum, SQLite; **Frontend**: React, TypeScript, Vite
- **Production**: no Node.js runtime needed; Axum serves the compiled frontend directly

---

## ❓ FAQ

<details>
<summary><b>Is this a cloud SaaS service?</b></summary>

No. It is self-deployed; card data and images stay on the server or NAS you manage.

</details>

<details>
<summary><b>Do visitors need an app or a LINE login to view a card?</b></summary>

No. Public card URLs open in any browser; LIFF is an optional LINE integration entry.

</details>

---

## 💬 Feedback & support

- 🐛 **Bug reports & feature requests**: please use the [Issues page](https://github.com/robert820/line-business-card/issues).
- 🌐 **DEI Tech official website**: [https://blog.dei3c.com](https://blog.dei3c.com)
- 📧 **Support & business inquiries**: please contact us through the official website.

---

## 📄 License

This software is released under a Proprietary Freeware license. See the [LICENSE](../../LICENSE) file for the full terms and disclaimers.

- **Third-party components and trademarks**: this software uses open-source Rust / npm packages and, for the optional LINE integration, LY Corporation's LIFF (under the LINE Developers Agreement); see [THIRD_PARTY_NOTICES.md](../../THIRD_PARTY_NOTICES.md). This project is not affiliated with or endorsed by LY Corporation or LINE; "LINE" is a trademark of its respective owner.

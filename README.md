<div align="center">

<a href="https://blog.dei3c.com" target="_blank" rel="noopener noreferrer">
  <img src="https://github.com/user-attachments/assets/2830eb70-512c-4ddb-87ec-5213a6e465b1" alt="得翼科技 | LINE Digital Business Card System" height="70" />
</a>

<br /><br />

**繁體中文** · [简体中文](docs/readme/README_zh-CN.md) · [English](docs/readme/README_en.md)

# LINE 數位名片管理與分享系統

### 自架名片、QR Code、vCard 與 Flex Message

[![Platform](https://img.shields.io/badge/Platform-Docker-blue?style=flat-square)](https://github.com/robert820/line-business-card)
[![License](https://img.shields.io/badge/License-Freeware-informational?style=flat-square)](LICENSE)
[![Status](https://img.shields.io/badge/Status-In%20Development-orange?style=flat-square)](#-目前狀態)

</div>

---

## 📖 軟體簡介

用一個管理後台建立多張數位名片，為每位聯絡人維護獨立的公開網址、版型與聯絡資訊。訪客可掃描 QR Code、下載 vCard、複製聯絡方式或透過 LINE 分享。

這是**自行部署**的系統，不是雲端 SaaS：名片資料與圖片保存在您管理的伺服器或 NAS。

---

## 📌 目前狀態

> 目前於本機 Docker Desktop (amd64) 驗證；實際 NAS、arm64 與 HTTPS 反向代理環境尚未驗證。

---

## ✨ 功能介紹

### 1. 🗂️ 集中管理多張名片
- 新增、編輯、複製與搜尋名片，管理草稿、已發布與封存狀態（單一管理員）。

### 2. 🎨 兩款版型與即時預覽
- 經典商務與現代直式版型、可選配色，編輯時可即時預覽。

### 3. 🔗 每張名片一個公開網址
- 訪客無須登入即可開啟 `/c/:slug`，複製網址、聯絡資訊或使用地圖導航。

### 4. 📱 QR Code 與 vCard
- 手機掃描 QR Code，或下載 vCard 加入通訊錄。

### 5. 💬 LINE 分享與 Flex Message
- 可透過 LIFF 分享或傳送名片，並可檢視、下載 Flex JSON，方便在官方 Flex Simulator 預覽。

### 6. 🔒 管理登入保護
- 伺服器端 session、Argon2id 密碼雜湊；正式部署需設定強式 `SESSION_SECRET` 與 HTTPS。

---

## 💻 支援範圍與限制

| 項目 | 需求／狀態 | 說明 |
| :--- | :--- | :--- |
| 伺服器 | Docker 與 Compose | 可部署於 NAS 或 Linux 主機；SQLite 資料庫與上傳圖片保存於持久化 Volume |
| 公開名片與 LINE 圖片 | 建議 HTTPS 網域 | 設定 `PUBLIC_BASE_URL`；LINE 顯示圖片需可由外部以 HTTPS 讀取 |
| LIFF | 選用整合 | 設定 `LIFF_ID` 後啟用 LINE 分享入口；未設定時一般公開名片仍可瀏覽 |
| 部署驗證 | 本機 Docker Desktop amd64 | 實際 NAS、arm64 與 HTTPS 反向代理環境尚未驗證 |

---

## 🚀 使用流程

1. 準備支援 Docker Compose 的 NAS 或伺服器，複製環境設定範例並產生專用 `SESSION_SECRET`。
2. 建立管理員帳號、啟動容器，並確認資料庫與上傳目錄位於持久化 Volume。
3. 設定 HTTPS 反向代理及公開網址，再登入管理後台建立名片並發布。
4. 使用公開名片頁測試 QR Code、vCard 與圖片連結；需要 LINE 分享時再設定 LIFF。

---

## 📦 下載與使用說明

目前尚未發布可下載的執行檔；發布後將提供於本專案的 [Releases 頁面](https://github.com/robert820/line-business-card/releases)。

---

## 🖥️ 系統與環境需求

- **部署**：Docker 與 Docker Compose（NAS 或 Linux 主機）
- **後端**：Rust、Axum、SQLite；**前端**：React、TypeScript、Vite
- **正式環境**：不需要 Node.js，Axum 直接提供編譯後的前端

---

## ❓ 常見問題 (FAQ)

<details>
<summary><b>這是雲端 SaaS 服務嗎？</b></summary>

不是。這是自行部署的系統，名片資料與圖片保存在您管理的伺服器或 NAS。

</details>

<details>
<summary><b>訪客需要安裝 App 或登入 LINE 才能看名片嗎？</b></summary>

不需要。一般公開名片網址可直接用瀏覽器開啟；LIFF 是選用的 LINE 整合入口。

</details>

---

## 💬 問題反饋與支援

- 🐛 **錯誤回報與功能建議**：歡迎至本專案的 [Issues 頁面](https://github.com/robert820/line-business-card/issues) 提出。
- 🌐 **得翼科技官方網站**：[https://blog.dei3c.com](https://blog.dei3c.com)
- 📧 **技術支援與商務洽詢**：請透過官方網站聯繫我們。

---

## 📄 授權條款 (License)

本軟體採用專有免費軟體授權（Proprietary Freeware），完整授權規範、使用條款與免責聲明請參閱 [LICENSE](LICENSE) 檔案。

- **第三方元件與商標**：本軟體使用多個開源 Rust／npm 套件，並於選用的 LINE 整合中使用 LY Corporation 的 LIFF（依 LINE Developers Agreement），授權聲明請見 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。本專案與 LY Corporation 及 LINE 無隸屬或背書關係，「LINE」為其權利人之商標。

<div align="center">

<a href="https://blog.dei3c.com" target="_blank" rel="noopener noreferrer">
  <img src="https://github.com/user-attachments/assets/2830eb70-512c-4ddb-87ec-5213a6e465b1" alt="得翼科技 | LINE Digital Business Card System" height="70" />
</a>

<br /><br />

[繁体中文](../../README.md) · **简体中文** · [English](README_en.md)

# LINE 数字名片管理与分享系统

### 自架名片、QR Code、vCard 与 Flex Message

[![Platform](https://img.shields.io/badge/Platform-Docker-blue?style=flat-square)](https://github.com/robert820/line-business-card)
[![License](https://img.shields.io/badge/License-Freeware-informational?style=flat-square)](../../LICENSE)
[![Status](https://img.shields.io/badge/Status-In%20Development-orange?style=flat-square)](#-目前状态)

</div>

---

## 📖 软件简介

用一个管理后台创建多张数字名片，为每位联系人维护独立的公开网址、版型与联系信息。访客可扫描 QR Code、下载 vCard、拷贝联系方式或通过 LINE 分享。

这是**自行部署**的系统，不是云端 SaaS：名片数据与图片保存在您管理的服务器或 NAS。

---

## 📌 目前状态

> 目前于本机 Docker Desktop (amd64) 验证；实际 NAS、arm64 与 HTTPS 反向代理环境尚未验证。

---

## ✨ 功能介绍

### 1. 🗂️ 集中管理多张名片
- 添加、编辑、拷贝与搜索名片，管理草稿、已发布与封存状态（单一管理员）。

### 2. 🎨 两款版型与即时预览
- 经典商务与现代直式版型、可选配色，编辑时可即时预览。

### 3. 🔗 每张名片一个公开网址
- 访客无须登录即可打开 `/c/:slug`，拷贝网址、联系信息或使用地图导航。

### 4. 📱 QR Code 与 vCard
- 手机扫描 QR Code，或下载 vCard 加入通信录。

### 5. 💬 LINE 分享与 Flex Message
- 可通过 LIFF 分享或发送名片，并可查看、下载 Flex JSON，方便在官方 Flex Simulator 预览。

### 6. 🔒 管理登录保护
- 服务器端 session、Argon2id 密码哈希；正式部署需设置强式 `SESSION_SECRET` 与 HTTPS。

---

## 💻 支持范围与限制

| 项目 | 需求／状态 | 说明 |
| :--- | :--- | :--- |
| 服务器 | Docker 与 Compose | 可部署于 NAS 或 Linux 主机；SQLite 数据库与上传图片保存于持久化 Volume |
| 公开名片与 LINE 图片 | 建议 HTTPS 网域 | 设置 `PUBLIC_BASE_URL`；LINE 显示图片需可由外部以 HTTPS 读取 |
| LIFF | 选用集成 | 设置 `LIFF_ID` 后激活 LINE 分享入口；未设置时一般公开名片仍可浏览 |
| 部署验证 | 本机 Docker Desktop amd64 | 实际 NAS、arm64 与 HTTPS 反向代理环境尚未验证 |

---

## 🚀 使用流程

1. 准备支持 Docker Compose 的 NAS 或服务器，拷贝环境设置范例并产生专用 `SESSION_SECRET`。
2. 创建管理员帐号、启动容器，并确认数据库与上传目录位于持久化 Volume。
3. 设置 HTTPS 反向代理及公开网址，再登录管理后台创建名片并发布。
4. 使用公开名片页测试 QR Code、vCard 与图片链接；需要 LINE 分享时再设置 LIFF。

---

## 📦 下载与使用说明

目前尚未发布可下载的运行档；发布后将提供于本项目的 [Releases 页面](https://github.com/robert820/line-business-card/releases)。

---

## 🖥️ 系统与环境需求

- **部署**：Docker 与 Docker Compose（NAS 或 Linux 主机）
- **后端**：Rust、Axum、SQLite；**前端**：React、TypeScript、Vite
- **正式环境**：不需要 Node.js，Axum 直接提供编译后的前端

---

## ❓ 常见问题 (FAQ)

<details>
<summary><b>这是云端 SaaS 服务吗？</b></summary>

不是。这是自行部署的系统，名片数据与图片保存在您管理的服务器或 NAS。

</details>

<details>
<summary><b>访客需要安装 App 或登录 LINE 才能看名片吗？</b></summary>

不需要。一般公开名片网址可直接用浏览器打开；LIFF 是选用的 LINE 集成入口。

</details>

---

## 💬 问题反馈与支持

- 🐛 **错误回报与功能建议**：欢迎至本项目的 [Issues 页面](https://github.com/robert820/line-business-card/issues) 提出。
- 🌐 **得翼科技官方网站**：[https://blog.dei3c.com](https://blog.dei3c.com)
- 📧 **技术支持与商务洽询**：请通过官方网站联系我们。

---

## 📄 授权条款 (License)

本软件采用专有免费软件授权（Proprietary Freeware），完整授权规范、使用条款与免责声明请参阅 [LICENSE](../../LICENSE) 文件。

- **第三方组件与商标**：本软件使用多个开源 Rust／npm 软件包，并在可选的 LINE 集成中使用 LY Corporation 的 LIFF（依 LINE Developers Agreement），授权声明请见 [THIRD_PARTY_NOTICES.md](../../THIRD_PARTY_NOTICES.md)。本项目与 LY Corporation 及 LINE 无隶属或背书关系，“LINE”为其权利人之商标。

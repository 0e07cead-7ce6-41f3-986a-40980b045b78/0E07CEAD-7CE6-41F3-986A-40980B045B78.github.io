# Personal Blog & Security Lab

<!-- 個人部落格與資安實驗室 -->

[![Verified Commits](https://img.shields.io/badge/Commits-Verified-green?logo=github)](https://github.com/0e07cead-7ce6-41f3-986a-40980b045b78/0E07CEAD-7CE6-41F3-986A-40980B045B78.github.io)
[![Hugo](https://img.shields.io/badge/Built%20with-Hugo-FF4088?logo=hugo)](https://gohugo.io/)
[![PaperMod Theme](https://img.shields.io/badge/Theme-PaperMod-blue)](https://github.com/adityatelange/hugo-PaperMod)

A modern personal blog and security research lab built with Hugo and PaperMod theme, featuring cryptographic verification tools.

<!-- 使用 Hugo + PaperMod 主題建立的現代化個人部落格，包含加密驗證工具 -->

## 📋 Table of Contents

<!-- 目錄 -->

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Quick Start](#quick-start)
- [Project Structure](#project-structure)
- [Configuration](#configuration)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## ✨ Features

<!-- 功能特性 -->

- 📝 **Markdown Support** - Write articles in Markdown format
  <!-- Markdown 支援：使用 Markdown 撰寫文章 -->
- 🎨 **PaperMod Theme** - Clean and modern design
  <!-- PaperMod 主題：簡潔現代的設計 -->
- 🔐 **Signature Verification** - Ed25519 digital signature verification system
  <!-- 簽章驗證：Ed25519 數位簽章驗證系統 -->
- 🔍 **SHA-256 Hash Checker** - Real-time message integrity verification
  <!-- SHA-256 雜湊檢查：即時訊息完整性驗證 -->
- 📱 **Responsive Design** - Perfect adaptation for all devices
  <!-- 響應式設計：完美適配各種裝置 -->
- 🛠️ **Security Tools** - Base64, URL encoder, password strength meter, etc.
  <!-- 資安工具：Base64、URL 編碼器、密碼強度檢測等 -->
- 🔍 **Full-text Search** - Quick article search capability
  <!-- 全文搜尋：快速查找文章 -->
- 📊 **SEO Optimized** - Auto-generated Sitemap and RSS feed
  <!-- SEO 優化：自動生成 Sitemap 與 RSS -->
- 🌍 **Internationalization** - Multi-language support (including Traditional Chinese)
  <!-- 國際化：支援多語言（包含繁體中文）-->

## 🛠 Tech Stack

<!-- 技術棧 -->

- **Static Site Generator**: [Hugo Extended](https://gohugo.io/)
  <!-- 靜態網站生成器 -->
- **Theme**: [PaperMod](https://github.com/adityatelange/hugo-PaperMod)
  <!-- 主題 -->
- **Deployment**: GitHub Pages + GitHub Actions
  <!-- 部署方式 -->
- **Cryptography**: Ed25519, SHA-256, SHA-512
  <!-- 加密演算法 -->
- **Client-side Tools**: Web Crypto API, zxcvbn
  <!-- 客戶端工具 -->

## 🚀 Quick Start

<!-- 快速開始 -->

### Prerequisites

<!-- 前置要求 -->

- [Hugo Extended](https://gohugo.io/installation/) (v0.100+)
- Git
- Code Editor (VS Code recommended)
  <!-- 程式碼編輯器（推薦 VS Code）-->

### Local Development

<!-- 本地開發 -->

```bash
# Clone the repository
# 複製倉庫
git clone https://github.com/0e07cead-7ce6-41f3-986a-40980b045b78/0E07CEAD-7CE6-41F3-986A-40980B045B78.github.io.git
cd 0E07CEAD-7CE6-41F3-986A-40980B045B78.github.io

# Initialize submodules (theme)
# 初始化子模組（主題）
git submodule update --init --recursive

# Start local development server
# 啟動本地開發伺服器
hugo server -D

# Visit http://localhost:1313
# 訪問 http://localhost:1313
```

### Build for Production

<!-- 建置生產版本 -->

```bash
# Clean build with minification
# 清理並建置（含壓縮）
hugo --minify

# Generated files will be in public/ directory
# 生成的檔案會在 public/ 目錄中
```

## 📁 Project Structure

<!-- 專案結構 -->

```
.
├── .github/
│   └── workflows/          # GitHub Actions CI/CD
│                          # GitHub Actions 自動部署工作流程
├── archetypes/             # Article templates
│                          # 文章模板
├── content/                # Article content
│   ├── about.md           # About page (關於頁面)
│   ├── tools.md           # Security tools index (資安工具索引)
│   ├── verify.md          # Signature verification page (簽章驗證頁面)
│   └── ...
├── layouts/
│   ├── partials/          # Partial templates (部分模板)
│   │   └── extend_head.html    # Custom head extensions (自訂 head 擴充)
│   └── shortcodes/        # Custom shortcodes (自訂短代碼)
│       ├── base64.html         # Base64 encoder/decoder (Base64 編碼/解碼器)
│       ├── sha512.html         # SHA-512 generator (SHA-512 生成器)
│       ├── verify-tool.html    # Signature verifier (簽章驗證器)
│       └── ...
├── static/                 # Static assets (靜態資源)
│   └── robots.txt         # SEO configuration (SEO 配置)
├── themes/
│   └── PaperMod/          # PaperMod theme (Git submodule)
│                          # PaperMod 主題（Git 子模組）
├── .gitignore             # Git ignore rules (Git 忽略規則)
├── hugo.yml               # Hugo configuration (Hugo 配置檔)
└── README.md              # This file (本檔案)
```

## ⚙️ Configuration

<!-- 配置說明 -->

### Hugo Settings

<!-- Hugo 設定 -->

Edit `hugo.yml` to modify basic site settings:

<!-- 編輯 hugo.yml 修改網站基本設定 -->

```yaml
baseURL: "https://yourdomain.com"
title: "Your Site Title"
languageCode: "zh-tw"  # Language code (語言代碼)
theme: "PaperMod"
```

### Security Keys

<!-- 安全金鑰 -->

The site uses Ed25519 public key for signature verification:

<!-- 本站使用 Ed25519 公鑰進行簽章驗證 -->

```yaml
params:
  site_verify_key: "YOUR_BASE64_PUBLIC_KEY"
  site_verify_fingerprint: "YOUR_SHA256_FINGERPRINT"
```

> ⚠️ **Important**: Only put PUBLIC keys in the config. Never commit private keys.

<!-- 重要：配置檔中只能放公鑰，絕不要提交私鑰 -->

### Creating New Articles

<!-- 建立新文章 -->

```bash
# Create a new post
# 建立新文章
hugo new content/posts/my-first-post.md
```

Article template is located at `archetypes/default.md`.

<!-- 文章模板位於 archetypes/default.md -->

### Custom Pages

<!-- 自訂頁面 -->

Create new pages in `content/` directory with Front Matter:

<!-- 在 content/ 目錄下建立新頁面，使用 Front Matter 定義 -->

```markdown
---
title: "Page Title"
date: 2026-01-12
draft: false
---

Your content here...
```

## 🌐 Deployment

<!-- 部署 -->

### GitHub Pages (Automatic)

<!-- GitHub Pages（自動部署）-->

This repository is configured with GitHub Actions workflow (`.github/workflows/hugo.yml`). Every push to `main` branch automatically triggers build and deployment.

<!-- 本倉庫配置有 GitHub Actions 工作流程，每次推送到 main 分支時自動建置並部署 -->

**Workflow includes:**

<!-- 工作流程包含： -->

- Checkout code with submodules
  <!-- 檢出程式碼（含子模組）-->
- Setup Hugo Extended
  <!-- 設定 Hugo Extended -->
- Build site with minification
  <!-- 建置網站（含壓縮）-->
- Deploy to GitHub Pages
  <!-- 部署到 GitHub Pages -->

### Manual Deployment

<!-- 手動部署 -->

```bash
# Build the site
# 建置網站
hugo --minify

# Push to repository
# 推送到倉庫
git add .
git commit -m "build: update website"
git push origin main
```

## 🔐 Security Features

<!-- 安全功能 -->

### Ed25519 Signature Verification

<!-- Ed25519 簽章驗證 -->

The site includes a client-side signature verification tool:

<!-- 本站包含客戶端簽章驗證工具 -->

- Verifies message authenticity using Ed25519 algorithm
  <!-- 使用 Ed25519 演算法驗證訊息真實性 -->
- SHA-256 hash comparison for message integrity
  <!-- SHA-256 雜湊比對確保訊息完整性 -->
- Real-time verification with Web Crypto API
  <!-- 使用 Web Crypto API 即時驗證 -->

### GPG Key

<!-- GPG 金鑰 -->

All commits are signed with GPG for code integrity:

<!-- 所有提交都使用 GPG 簽署以確保程式碼完整性 -->

```bash
# Configure GPG signing
# 配置 GPG 簽署
git config --global user.signingkey YOUR_KEY_ID
git config --global commit.gpgsign true

# Commits will be automatically signed
# 提交時自動簽署
git commit -m "your message"
```

## 🛡️ Security Tools

<!-- 資安工具 -->

The site includes several security-focused tools:

<!-- 本站包含多個資安工具 -->

- **Base64 Encoder/Decoder** - Unicode-compatible Base64 conversion
  <!-- Base64 編碼/解碼器：支援 Unicode 的 Base64 轉換 -->
- **SHA-512 Generator** - Secure hash generation
  <!-- SHA-512 生成器：安全的雜湊生成 -->
- **URL Encoder/Decoder** - URL-safe string encoding
  <!-- URL 編碼/解碼器：URL 安全的字串編碼 -->
- **Password Strength Meter** - zxcvbn-based password analysis
  <!-- 密碼強度檢測器：基於 zxcvbn 的密碼分析 -->
- **Signature Verifier** - Ed25519 signature verification with hash comparison
  <!-- 簽章驗證器：Ed25519 簽章驗證與雜湊比對 -->

All tools run **client-side only** - your data never leaves your browser.

<!-- 所有工具都在客戶端運行，您的資料永遠不會離開瀏覽器 -->

## 🤝 Contributing

<!-- 貢獻 -->

Issues and Pull Requests are welcome!

<!-- 歡迎提交 Issue 與 Pull Request -->

### Development Workflow

<!-- 開發流程 -->

1. Fork the repository
   <!-- 分叉倉庫 -->
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
   <!-- 建立功能分支 -->
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
   <!-- 提交變更 -->
4. Push to the branch (`git push origin feature/amazing-feature`)
   <!-- 推送到分支 -->
5. Open a Pull Request
   <!-- 開啟 Pull Request -->

## 📄 License

<!-- 授權 -->

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

<!-- 本專案採用 MIT 授權 - 詳見 LICENSE 檔案 -->

## 🔗 Links

<!-- 連結 -->

- **Live Site**: [https://12587456.xyz](https://12587456.xyz)
- **Hugo Documentation**: [https://gohugo.io/documentation/](https://gohugo.io/documentation/)
- **PaperMod Theme**: [https://github.com/adityatelange/hugo-PaperMod](https://github.com/adityatelange/hugo-PaperMod)

---

**Created**: 2026-01-12  
**Last Updated**: 2026-01-12

---

<!-- 
========================================
以下為開發者中文備註（僅在原始碼中可見）
========================================

⚠️ 重要維護注意事項：

1. 主題管理
   - themes/PaperMod 是 Git Submodule，不要直接修改
   - 自訂功能放在 layouts/ 底下，會覆蓋主題原始檔案
   - 更新主題：git submodule update --remote themes/PaperMod

2. 安全性
   - 絕對不要將私鑰、API Token 提交到倉庫
   - .gitignore 已設定排除 *.key, *.pem 等敏感檔案
   - 公鑰可以公開在 hugo.yml 中（site_verify_key）

3. 開發測試
   - 本地測試：hugo server -D
   - 建置測試：hugo --minify
   - 檢查生成檔案：ls public/

4. Git 提交規範
   - feat: 新功能
   - fix: 修復 bug
   - docs: 文件更新
   - style: 格式調整
   - refactor: 重構程式碼
   - chore: 雜項更新

5. 部署流程
   - 推送到 main 分支會自動觸發 GitHub Actions
   - 建置時間約 1-2 分鐘
   - 部署完成後約 5 分鐘生效

6. 常見問題排解
   - 主題未載入：執行 git submodule update --init --recursive
   - 建置失敗：檢查 Hugo 版本是否為 Extended
   - 樣式跑版：清除瀏覽器快取後重新整理

7. 檔案架構說明
   - content/: 文章內容（Markdown）
   - layouts/shortcodes/: 自訂的 Hugo shortcode（工具元件）
   - layouts/partials/: 自訂的部分模板（如 extend_head.html）
   - static/: 靜態資源（圖片、CSS、JS）
   - public/: 建置後的輸出（不要手動修改，會被覆蓋）

8. Shortcode 使用方式
   {{< base64 >}}          # Base64 工具
   {{< sha512 >}}          # SHA-512 工具
   {{< verify-tool >}}     # 簽章驗證工具
   {{< signed-msg msg="..." sig="..." >}}  # 已簽署訊息區塊

========================================
-->
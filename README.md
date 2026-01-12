# 個人博客網站

[![Verified Commits](https://img.shields.io/badge/Commits-Verified-green?logo=github)](https://github.com/0e07cead-7ce6-41f3-986a-40980b045b78/0E07CEAD-7CE6-41F3-986A-40980B045B78.github.io)
[![Hugo](https://img.shields.io/badge/Built%20with-Hugo-FF4088?logo=hugo)](https://gohugo.io/)
[![PaperMod Theme](https://img.shields.io/badge/Theme-PaperMod-blue)](https://github.com/adityatelange/hugo-PaperMod)

一個基於 Hugo 和 PaperMod 主題的現代化個人博客網站，包含安全驗證功能。

## 📋 目錄

- [功能特性](#功能特性)
- [技術棧](#技術棧)
- [快速開始](#快速開始)
- [目錄結構](#目錄結構)
- [配置說明](#配置說明)
- [部署](#部署)
- [貢獻](#貢獻)
- [許可](#許可)

## ✨ 功能特性

- 📝 **Markdown 支持** - 使用 Markdown 編寫文章
- 🎨 **PaperMod 主題** - 簡潔現代的設計
- 🔐 **Hash 驗證** - 驗證文章是否與原文一致
- 📱 **響應式設計** - 完美適配各種設備
- 🔍 **全文搜索** - 快速查找文章
- 📊 **SEO 優化** - 自動生成 Sitemap 和 RSS
- 🌍 **國際化** - 支持多語言（包括繁體中文）

## 🛠 技術棧

- **靜態生成器**：[Hugo](https://gohugo.io/)
- **主題**：[PaperMod](https://github.com/adityatelange/hugo-PaperMod)
- **部署**：GitHub Pages
- **加密驗證**：GPG/Hash 簽名

## 🚀 快速開始

### 前置要求

- [Hugo Extended](https://gohugo.io/installation/) (v0.100+)
- Git
- 代碼編輯器（推薦 VS Code）

### 本地開發

```bash
# 克隆倉庫
git clone https://github.com/0e07cead-7ce6-41f3-986a-40980b045b78/0E07CEAD-7CE6-41F3-986A-40980B045B78.github.io.git
cd 0E07CEAD-7CE6-41F3-986A-40980B045B78.github.io

# 初始化子模組（主題）
git submodule update --init --recursive

# 運行本地服務器
hugo server

# 訪問 http://localhost:1313
```

### 構建生產版本

```bash
# 清理並構建
hugo --minify

# 生成文件在 public/ 目錄中
```

## 📁 目錄結構

```
.
├── archetypes/          # 文章模板
├── content/             # 文章內容
│   ├── about.md        # 關於頁面
│   ├── tools.md        # 工具頁面
│   └── ...
├── layouts/             # 自定義佈局
│   ├── partials/       # 部分模板
│   └── shortcodes/     # 短代碼
├── static/              # 靜態資源
├── themes/              # 主題
│   └── PaperMod/       # PaperMod 主題（子模組）
├── hugo.yml            # Hugo 配置文件
└── README.md           # 本文件
```

## ⚙️ 配置說明

### Hugo 配置

編輯 `hugo.yml` 修改網站基本設置：

```yaml
baseURL: "https://yourdomain.com"
title: "你的網站標題"
languageCode: "zh-tw"
```

### 新建文章

```bash
hugo new content/posts/my-first-post.md
```

文章模板位於 `archetypes/default.md`

### 自定義頁面

在 `content/` 目錄下新建頁面，使用 Front Matter 定義：

```markdown
---
title: "頁面標題"
date: 2026-01-12
draft: false
---

你的內容...
```

## 🌐 部署

### GitHub Pages 自動部署

本倉庫配置有 GitHub Actions 工作流程 (`.github/workflows/`)，每次推送到 `main` 分支時自動構建和部署。

### 手動部署

```bash
# 構建網站
hugo --minify

# 提交構建文件
git add public/
git commit -m "build: update website"
git push origin main
```

## 🔐 GPG 簽名提交

所有提交都使用 GPG 簽名驗證，確保代碼完整性：

```bash
# 配置 GPG 簽名
git config --global user.signingkey YOUR_KEY_ID
git config --global commit.gpgsign true

# 提交時自動簽名
git commit -m "commit message"
```

## 🤝 貢獻

歡迎提交 Issue 和 Pull Request！

## 📄 許可

此項目採用 MIT 許可證 - 詳見 [LICENSE](LICENSE) 文件

---

**建立日期**: 2026-01-12  
**最後更新**: 2026-01-12


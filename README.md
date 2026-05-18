# 📚 human-context

> A local-first workspace for understanding large markdown knowledge bases in AI workflows.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](./LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/zzgiabaozzbui/human-context/pulls)
[![No Build](https://img.shields.io/badge/build-none-lightgrey.svg)](https://github.com/zzgiabaozzbui/human-context)
[![Single File](https://img.shields.io/badge/size-1%20file-orange.svg)](./md-folder-viewer.html)
[![Last Commit](https://img.shields.io/github/last-commit/zzgiabaozzbui/human-context)](https://github.com/zzgiabaozzbui/human-context/commits/main)
[![Viewer Size](https://img.shields.io/github/size/zzgiabaozzbui/human-context/human-context/md-folder-viewer.html?label=viewer%20size&color=informational)](./md-folder-viewer.html)

---

[▶ Watch demo](./readme-files/demo.mp4)

> *File tree with token counts · Frontmatter as metadata cards · TOC with scroll spy · Dark mode*

![Screenshot](./readme-files/screenshot.png)

---

## Table of Contents

- [🧠 The Story](#-the-story)
- [⚡ Quick Start](#-quick-start)
- [🚫 This is not a docs generator](#-this-is-not-a-docs-generator)
- [🤔 Why not Obsidian / Notion / GitBook?](#-why-not-obsidian--notion--gitbook)
- [✨ Features](#-features)
- [🤝 Contributing](#-contributing)
- [🗺️ Roadmap](#️-roadmap)
- [🏗️ How It Works](#️-how-it-works)
- [🙏 Contributors](#-contributors)
- [📄 License](#-license)
- [🇻🇳 Tiếng Việt](#-tiếng-việt)
- [🇨🇳 中文](#-中文)

---

## 🧠 The Story

Context engineering is pulling developers in two directions at once.

One side says: keep everything in `.md` — plain text, version-controlled, AI-readable. No build system. No friction. Your `CLAUDE.md`, your `memory/` folder, your `docs/` live right there in the repo where they belong.

The other side says: humans need a real interface. Navigable. Searchable. With syntax highlighting and a table of contents. Not just squinting at raw markdown in VS Code.

Both are right. Both are incomplete. Most people pick a side.

Children pick a side. **Adults take both.**

Your AI already reads the `.md` files perfectly. What's missing is a way for your teammates — and your future self — to read them too, with actual eyes, in an actual browser, without migrating to Notion or setting up a whole documentation pipeline.

**human-context** is that missing piece. A single `.html` file you drop into any project. Open it in Chrome, point it at your folder, and instantly get a proper reading experience for every `.md` file — file tree, syntax highlighting, TOC, cross-file navigation, dark mode, and token counts so you know exactly what you're feeding your AI.

No server. No `npm install`. No build step. **One file.**

---

## ⚡ Quick Start

**Option A — one-liner (Mac/Linux):**

```bash
curl -O https://raw.githubusercontent.com/zzgiabaozzbui/human-context/main/human-context/md-folder-viewer.html
```

**Option B — manual:**

**1.** Download [`md-folder-viewer.html`](./md-folder-viewer.html)

**2.** Open it in Chrome or Edge (double-click the file)

**3.** Click **Open Folder** → select your project folder

That's it. Your folder becomes a navigable knowledge base.

> **Firefox users:** supported via file picker fallback, but folder memory won't persist between sessions (Firefox doesn't support the File System Access API).

---

> If this saved you time — [⭐ star it](https://github.com/zzgiabaozzbui/human-context). It helps others find it.

---

## 🚫 This is not a docs generator

**human-context is not Docusaurus. It is not MkDocs. It is not a site builder.**

It is a local-first workspace for understanding large markdown knowledge bases in AI workflows.

Use your existing markdown docs instantly. **No build. No install. No server.**

---

Docs generators work like this:

```text
write docs → build site → deploy → publish
```

human-context works like this:

```text
open folder → inspect context → select files → feed AI
```

---

Three things this tool has that they don't:

**Arbitrary folder opening** — No repo setup. No `mkdocs.yml`. No project structure required. Just: open folder → runs. A random folder of notes from 2019? Works. Someone else's repo you just cloned? Works. Your `~/Documents/`? Works.

**AI-native context awareness** — Docusaurus doesn't care about tokens, prompt budget, or AI context quality. human-context is built entirely around that. Every file shows token counts so you know exactly what you're feeding your AI — before you feed it.

**Zero friction** — Many devs won't install. Won't build. Won't set up. But they will double-click an HTML file. That's the only distribution that works without asking anything of the user.

---

## 🤔 Why not Obsidian / Notion / GitBook?

Wrong tool for the job.

Those tools are for **managing** a knowledge base — writing, organizing, linking, publishing.

human-context is for **reading** one. Specifically: reading whatever markdown folder you have open right now, with zero ceremony.

| | human-context | Obsidian | Notion | GitBook |
| --- | --- | --- | --- | --- |
| Open any folder instantly | ✅ | ❌ vault setup | ❌ import required | ❌ repo integration |
| No install | ✅ | ❌ | ❌ | ❌ |
| No account | ✅ | ✅ | ❌ | ❌ |
| Works offline | ✅ | ✅ | ❌ | ❌ |
| Token counting for AI | ✅ | ❌ | ❌ | ❌ |
| Files never leave your machine | ✅ | ✅ | ❌ | ❌ |

The difference in practice:

**Obsidian:** install → create vault → configure → open file
**human-context:** open file → click Open Folder → done

Obsidian is powerful. Use it for building a long-term personal knowledge base.
human-context is for when you just need to read a folder. Any folder. Right now.

---

## ✨ Features

- **🌲 File tree** — auto icons by filename and folder, collapsible
- **📊 Token and word counts** — per-file token / word / char / heading stats in the tree and content panel
- **🃏 Frontmatter cards** — YAML `---` blocks rendered as structured metadata, not raw text
- **🎨 Syntax highlighting** — via highlight.js, light and dark themes
- **📋 Table of contents** — auto-generated, scroll spy, smooth scroll
- **🔗 Cross-file navigation** — click `.md` links inside content to navigate between files
- **🗂️ Section cards** — H2 blocks wrapped in visual cards for easier scanning
- **🔍 Search** — filter the file tree in real time
- **🌙 Dark mode** — persisted in localStorage
- **💾 Folder memory** — IndexedDB remembers your last folder, reopens it automatically on next visit
- **📱 Responsive** — tree panel collapses on mobile with hamburger toggle
- **🌐 Multilingual UI** — switch between English, Tiếng Việt, and 中文

Also included: [`md-reader.html`](./md-reader.html) — the simpler single-file version (drag & drop one `.md` file, no folder needed).

---

## 🤝 Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for setup notes, coding style, and the PR checklist.

This is **one HTML file**. You can read the entire codebase in 30 minutes and understand every line. That's the point.

If you've ever wanted to contribute to open source but felt intimidated by monorepos, build pipelines, and 47-step setup guides — this is for you.

**Good first contributions:**

- Add a new file icon pattern in `getIcon()` — one line, instant result
- Add a new heading icon pattern in `HEADING_ICONS[]` — same
- Improve dark mode contrast or spacing — pure CSS, safe to experiment
- Add a new language to this README — no code required
- Fix a bug you found (the code is right there)
- Improve mobile layout

**How to contribute:**

1. Fork the repo
2. Open `md-folder-viewer.html` in a text editor
3. Make your change
4. Test it by opening the file in Chrome
5. Open a PR with a short description of what you changed and why

No tests to run. No CI to wait for. No environment to set up.

Browse [`good first issues`](https://github.com/zzgiabaozzbui/human-context/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22) to find something ready to pick up.

If you improve it — please push back. That's how this gets better for everyone.

---

## 🗺️ Roadmap

These are things not yet built. Any of them would make a great PR — [claim one in Issues](https://github.com/zzgiabaozzbui/human-context/issues):

- [x] **Keyboard navigation** (`j` / `k` to move between files) — make it feel like a real IDE
- [x] **Word count alongside token count** — more writing-friendly stats
- [ ] **Support `.txt`, `.rst`, `.mdx`** — extend beyond markdown
- [ ] **Export folder as a static site** — offline-ready HTML bundle, shareable without a server
- [ ] **Print / PDF mode** — formatted output for documentation handoff
- [ ] **Customizable icon sets** — bring your own emoji map per project
- [ ] **Inline image support** — render local `./images/*.png` inside content
- [ ] **Better mobile experience** — swipe gestures, full-screen reading mode

Have an idea not on this list? [Open an issue](https://github.com/zzgiabaozzbui/human-context/issues/new) or just build it.

---

## 🏗️ How It Works

```text
md-folder-viewer.html
│
├── File System Access API  → showDirectoryPicker() [Chrome/Edge]
├── webkitdirectory input   → fallback for Firefox
├── marked.js (CDN)         → markdown parsing
├── highlight.js (CDN)      → syntax highlighting
├── IndexedDB               → folder handle persistence across sessions
└── CSS custom properties   → full light/dark design system, no framework
```

Everything runs client-side. Nothing is sent anywhere. Your files never leave your machine.

---

## 🙏 Contributors

Thanks to everyone who has improved this project:

<!-- Add your name here when you open a PR -->

[![zzgiabaozzbui](https://avatars.githubusercontent.com/zzgiabaozzbui?s=64)](https://github.com/zzgiabaozzbui)

**[zzgiabaozzbui](https://github.com/zzgiabaozzbui)** — Original author

*Your name could be here. [See Contributing ↑](#-contributing)*

---

## 📄 License

MIT — do whatever you want, just keep the copyright notice. See [LICENSE](./LICENSE).

---

## 🇻🇳 Tiếng Việt

### Câu chuyện

Context engineering đang kéo developer theo hai hướng cùng lúc.

Một phía nói: giữ tất cả trong `.md` — AI đọc được, git-friendly, không phụ thuộc tool nào. Không cần build system. Không cần setup. `CLAUDE.md`, thư mục `memory/`, thư mục `docs/` nằm ngay trong repo, đúng chỗ.

Phía kia nói: con người cần giao diện thật. Điều hướng được. Tìm kiếm được. Có syntax highlighting và mục lục. Không phải nhìn chằm chằm vào markdown thô trong VS Code.

Cả hai đều đúng. Cả hai đều thiếu. Đa số người chọn một trong hai.

Trẻ con mới chọn một. **Người lớn chọn cả hai.**

AI của bạn đã đọc các file `.md` hoàn hảo rồi. Thứ còn thiếu là cách để đồng nghiệp — và chính bạn sau vài tuần — đọc chúng bằng mắt thật, trên trình duyệt thật, mà không phải migrate sang Notion hay dựng cả một pipeline documentation.

**human-context** là mảnh ghép còn thiếu đó. Một file `.html` duy nhất. Mở lên, chọn folder, đọc. Không cần server, không cần cài gì.

### Cách dùng nhanh

**Option A — một lệnh (Mac/Linux):**

```bash
curl -O https://raw.githubusercontent.com/zzgiabaozzbui/human-context/main/human-context/md-folder-viewer.html
```

**Option B — thủ công:**

**1.** Tải [`md-folder-viewer.html`](./md-folder-viewer.html)

**2.** Mở bằng Chrome hoặc Edge (double-click vào file)

**3.** Bấm **Open Folder** → chọn folder dự án

> **Firefox:** hỗ trợ qua file picker fallback, nhưng không nhớ folder giữa các session.

---

> Nếu tool này hữu ích — [⭐ star repo](https://github.com/zzgiabaozzbui/human-context) để người khác tìm thấy.

### Đây không phải docs generator

**human-context không phải Docusaurus. Không phải MkDocs. Không phải site builder.**

Đây là workspace local-first để hiểu và làm việc với markdown knowledge base trong AI workflow.

Dùng ngay docs markdown hiện có. **Không build. Không cài. Không server.**

---

Docs generator làm thế này:

```text
viết docs → build site → deploy → publish
```

human-context làm thế này:

```text
mở folder → xem context → chọn file → feed AI
```

---

Ba thứ tool này có mà chúng không có:

**Mở folder tùy ý** — không cần repo setup, không cần config, không cần cấu trúc project. Chỉ cần: mở folder → chạy. Folder notes cũ từ 2019? Được. Repo vừa clone của người khác? Được. Thư mục `~/Documents/`? Được.

**AI-native context awareness** — Docusaurus không quan tâm token là gì. human-context build toàn bộ quanh prompt budget: mỗi file hiện số token để bạn biết đang feed AI bao nhiêu — trước khi feed.

**Zero friction** — Nhiều dev sẽ không cài, không build, không setup. Nhưng họ sẽ double-click file HTML. Đó là cách duy nhất để phân phối mà không đòi hỏi gì từ user.

### Tại sao không dùng Obsidian / Notion / GitBook?

Sai tool cho công việc này.

Các tool đó để **quản lý** knowledge base — viết, tổ chức, link, xuất bản.

human-context để **đọc** — cụ thể là đọc bất kỳ folder markdown nào bạn đang có, không cần ceremony.

| | human-context | Obsidian | Notion | GitBook |
| --- | --- | --- | --- | --- |
| Mở folder tức thì | ✅ | ❌ cần vault setup | ❌ cần import | ❌ cần tích hợp repo |
| Không cài đặt | ✅ | ❌ | ❌ | ❌ |
| Không cần tài khoản | ✅ | ✅ | ❌ | ❌ |
| Làm việc offline | ✅ | ✅ | ❌ | ❌ |
| Đếm token cho AI | ✅ | ❌ | ❌ | ❌ |
| File không rời máy | ✅ | ✅ | ❌ | ❌ |

Sự khác biệt trong thực tế:

**Obsidian:** cài → tạo vault → cấu hình → mở file
**human-context:** mở file → click Open Folder → xong

Obsidian rất mạnh. Dùng nó nếu bạn đang xây dựng personal knowledge base lâu dài.
human-context dành cho khi bạn chỉ cần đọc một folder. Bất kỳ folder nào. Ngay bây giờ.

### Tính năng

- **🌲 Cây file** — icon tự động theo tên file/folder, có thể thu gọn
- **📊 Đếm token** — hiển thị token / từ / ký tự / heading trên từng file
- **🃏 Frontmatter card** — YAML `---` được render thành metadata card riêng biệt
- **🎨 Syntax highlighting** — qua highlight.js, hỗ trợ sáng/tối
- **📋 Mục lục** — tự tạo, scroll spy, smooth scroll
- **🔗 Điều hướng chéo** — click link `.md` trong nội dung để mở file khác
- **🗂️ Section cards** — các block H2 được đóng khung để dễ scan
- **🔍 Tìm kiếm** — lọc cây file theo tên trong thời gian thực
- **🌙 Dark mode** — lưu vào localStorage
- **💾 Nhớ folder** — IndexedDB ghi nhớ folder cuối, tự mở lại lần sau
- **📱 Responsive** — tree panel thu gọn trên mobile
- **🌐 Đa ngôn ngữ** — chuyển đổi giữa EN / Tiếng Việt / 中文

### Đóng góp

File này chỉ có **1 file HTML duy nhất**. Bạn có thể đọc hết code trong 30 phút. Đó là chủ ý.

Nếu bạn là người mới muốn contribute open source nhưng ngại monorepo, pipeline CI 47 bước — đây là dành cho bạn.

**Những gì dễ làm:**

- Thêm icon mới trong `getIcon()` — một dòng, kết quả ngay lập tức
- Thêm pattern heading icon trong `HEADING_ICONS[]` — tương tự
- Cải thiện dark mode hoặc spacing — chỉ là CSS
- Thêm ngôn ngữ mới vào README — không cần code
- Fix bug bạn tìm thấy

**Cách contribute:**

1. Fork repo
2. Mở `md-folder-viewer.html` trong text editor
3. Sửa
4. Test bằng cách mở file trong Chrome
5. Mở PR với mô tả ngắn gọn

Không cần test suite. Không cần CI. Không cần setup environment.

Xem [`good first issues`](https://github.com/zzgiabaozzbui/human-context/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22) để tìm việc cụ thể có thể nhận.

Nếu bạn cải thiện được — hãy push lên. Dự án này tốt hơn là nhờ mọi người cùng làm.

### Roadmap

Những thứ chưa có — PR welcome — [nhận issue tại đây](https://github.com/zzgiabaozzbui/human-context/issues):

- [x] **Điều hướng bằng phím** (`j` / `k`) — như IDE thật
- [x] **Word count bên cạnh token count** — thống kê thân thiện với người viết
- [ ] **Hỗ trợ `.txt`, `.rst`, `.mdx`** — mở rộng ngoài markdown
- [ ] **Export folder thành static site** — bundle HTML offline, share không cần server
- [ ] **Chế độ in / PDF** — output định dạng đẹp để handoff tài liệu
- [ ] **Icon set tùy chỉnh** — tự mang emoji map riêng cho từng project
- [ ] **Hiển thị ảnh local** — render `./images/*.png` ngay trong content
- [ ] **Layout mobile tốt hơn** — swipe gesture, chế độ đọc toàn màn hình

### Hoạt động như thế nào

```text
md-folder-viewer.html
│
├── File System Access API  → showDirectoryPicker() [Chrome/Edge]
├── webkitdirectory input   → fallback cho Firefox
├── marked.js (CDN)         → parse markdown
├── highlight.js (CDN)      → syntax highlighting
├── IndexedDB               → lưu folder handle giữa các session
└── CSS custom properties   → design system sáng/tối, không dùng framework
```

Mọi thứ chạy client-side. Không gửi gì ra ngoài. File của bạn không rời khỏi máy.

---

## 🇨🇳 中文

### 背景故事

Context Engineering 正在把开发者同时往两个方向拉。

一边说：把所有内容保存为 `.md` 文件 —— AI 可读、版本可控、零依赖。不需要构建系统，不需要配置。`CLAUDE.md`、`memory/` 目录、`docs/` 就放在 repo 里，就在它们应该在的地方。

另一边说：人类需要真正的界面。可导航。可搜索。有语法高亮和目录。而不是在 VS Code 里盯着原始 Markdown 看。

两者都对。两者都不完整。大多数人选其一。

小孩才做选择。**成熟的开发者两个都要。**

你的 AI 已经能完美读取这些 `.md` 文件了。缺少的是让你的队友——以及几周后的你自己——也能用真实的眼睛，在真实的浏览器里读它们的方式，而不用迁移到 Notion 或搭一整套文档流水线。

**human-context** 就是那块缺失的拼图。一个单独的 `.html` 文件。打开浏览器，选择文件夹，立即获得完整的阅读体验。无需服务器，无需 `npm install`，无需构建步骤。

### 快速开始

**方式 A — 一行命令（Mac/Linux）：**

```bash
curl -O https://raw.githubusercontent.com/zzgiabaozzbui/human-context/main/human-context/md-folder-viewer.html
```

**方式 B — 手动：**

**1.** 下载 [`md-folder-viewer.html`](./md-folder-viewer.html)

**2.** 用 Chrome 或 Edge 打开（双击文件即可）

**3.** 点击 **Open Folder** → 选择你的项目文件夹

> **Firefox 用户：** 通过文件选择器支持，但 session 之间不会记忆文件夹。

---

> 如果对你有帮助 —— [⭐ 给个 Star](https://github.com/zzgiabaozzbui/human-context)，让更多人发现它。

### 这不是文档生成器

**human-context 不是 Docusaurus，不是 MkDocs，不是站点构建器。**

它是一个本地优先的工作空间，用于在 AI 工作流中理解大型 Markdown 知识库。

直接使用你现有的 Markdown 文档。**无需构建。无需安装。无需服务器。**

---

文档生成器的工作方式：

```text
写文档 → 构建站点 → 部署 → 发布
```

human-context 的工作方式：

```text
打开文件夹 → 查看上下文 → 选择文件 → 喂给 AI
```

---

三个这个工具有而它们没有的东西：

**任意文件夹打开** — 不需要 repo 配置，不需要构建配置，不需要项目结构。只需：打开文件夹 → 运行。2019 年的旧笔记？可以。刚 clone 下来的别人的 repo？可以。你的 `~/Documents/`？可以。

**AI 原生上下文感知** — Docusaurus 不关心 token 是什么。human-context 围绕 prompt budget 构建：每个文件显示 token 数量，让你在喂给 AI 之前就知道要喂多少。

**零摩擦** — 很多开发者不会安装，不会构建，不会配置。但他们会双击一个 HTML 文件。这是唯一一种不向用户提出任何要求的分发方式。

### 为什么不用 Obsidian / Notion / GitBook？

工具用错了场景。

那些工具是用来**管理**知识库的 —— 写作、整理、链接、发布。

human-context 是用来**阅读**的 —— 具体来说，是阅读你现在手边的任何 Markdown 目录，零准备工作。

| | human-context | Obsidian | Notion | GitBook |
| --- | --- | --- | --- | --- |
| 即时打开任意文件夹 | ✅ | ❌ 需要 vault 配置 | ❌ 需要导入 | ❌ 需要 repo 集成 |
| 无需安装 | ✅ | ❌ | ❌ | ❌ |
| 无需账号 | ✅ | ✅ | ❌ | ❌ |
| 离线可用 | ✅ | ✅ | ❌ | ❌ |
| AI Token 计数 | ✅ | ❌ | ❌ | ❌ |
| 文件不离开本机 | ✅ | ✅ | ❌ | ❌ |

实际使用对比：

**Obsidian：** 安装 → 创建 vault → 配置 → 打开文件
**human-context：** 打开文件 → 点击 Open Folder → 完成

Obsidian 非常强大。如果你在构建长期的个人知识库，用它。
human-context 是当你只需要读一个目录时用的。任何目录。就是现在。

### 功能特性

- **🌲 文件树** — 按文件名/文件夹自动分配图标，可折叠
- **📊 Token 统计** — 每个文件显示 token 数 / 字数 / 字符数 / 标题数
- **🃏 Frontmatter 卡片** — YAML `---` 块渲染为结构化元数据卡片
- **🎨 语法高亮** — 基于 highlight.js，支持亮色/暗色主题
- **📋 目录导航** — 自动生成，滚动跟踪，平滑滚动
- **🔗 跨文件导航** — 点击内容中的 `.md` 链接跳转到对应文件
- **🗂️ Section 卡片** — H2 块包裹在视觉卡片中，便于扫描
- **🔍 搜索** — 实时按文件名过滤文件树
- **🌙 暗色模式** — 保存到 localStorage
- **💾 文件夹记忆** — IndexedDB 记住上次文件夹，下次自动打开
- **📱 响应式** — 移动端汉堡菜单切换文件树面板
- **🌐 多语言界面** — 可切换 EN / Tiếng Việt / 中文

### 参与贡献

这只是**一个 HTML 文件**。你可以在 30 分钟内读完全部代码。这是有意为之的。

**适合新手的贡献：**

- 在 `getIcon()` 中添加新的文件图标 —— 一行代码，即时生效
- 在 `HEADING_ICONS[]` 中添加新的标题图标规则 —— 同上
- 改善暗色模式对比度或间距 —— 只是 CSS
- 为 README 添加新语言翻译 —— 无需写代码
- 修复你发现的 Bug

**贡献方式：**

1. Fork 本仓库
2. 用文本编辑器打开 `md-folder-viewer.html`
3. 做出修改
4. 在 Chrome 中打开文件进行测试
5. 提交 PR，附上简短说明

无需运行测试。无需等待 CI。无需配置环境。

浏览 [`good first issues`](https://github.com/zzgiabaozzbui/human-context/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22) 找一个可以认领的任务。

### 路线图

尚未实现的功能 —— 欢迎提 PR —— [在 Issues 中认领](https://github.com/zzgiabaozzbui/human-context/issues)：

- [x] **键盘导航**（`j` / `k` 在文件间移动）—— 像真正的 IDE 一样
- [x] **在 Token 数旁显示字数统计** —— 对写作者更友好
- [ ] **支持 `.txt`、`.rst`、`.mdx`** —— 扩展到 Markdown 之外
- [ ] **将文件夹导出为静态网站** —— 离线可用的 HTML 包，无需服务器即可分享
- [ ] **打印 / PDF 模式** —— 格式化输出，用于文档交接
- [ ] **可自定义图标集** —— 为每个项目带上你自己的 emoji 映射
- [ ] **本地图片支持** —— 在内容中渲染 `./images/*.png`
- [ ] **更好的移动端体验** —— 滑动手势、全屏阅读模式

有新想法？[提一个 Issue](https://github.com/zzgiabaozzbui/human-context/issues/new) 或者直接动手做。

### 工作原理

```text
md-folder-viewer.html
│
├── File System Access API  → showDirectoryPicker() [Chrome/Edge]
├── webkitdirectory input   → Firefox 回退方案
├── marked.js (CDN)         → Markdown 解析
├── highlight.js (CDN)      → 语法高亮
├── IndexedDB               → 跨 session 保存文件夹句柄
└── CSS custom properties   → 亮/暗色设计系统，无需框架
```

所有处理均在客户端完成。不发送任何数据。你的文件不会离开你的设备。

---

Made by [chillchill](https://github.com/zzgiabaozzbui) · [⭐ Star if useful](https://github.com/zzgiabaozzbui/human-context) · [🐛 Report a bug](https://github.com/zzgiabaozzbui/human-context/issues/new)

---

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=zzgiabaozzbui/human-context&type=Date)](https://star-history.com/#zzgiabaozzbui/human-context&Date)

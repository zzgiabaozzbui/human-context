# 📚 human-context

> `.md` for AI. `.html` for humans. Why not both?

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](./LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/zzgiabaozzbui/human-context/pulls)
[![No Build](https://img.shields.io/badge/build-none-lightgrey.svg)](https://github.com/zzgiabaozzbui/human-context)
[![Single File](https://img.shields.io/badge/size-1%20file-orange.svg)](./md-folder-viewer.html)
[![Last Commit](https://img.shields.io/github/last-commit/zzgiabaozzbui/human-context)](https://github.com/zzgiabaozzbui/human-context/commits/main)
[![Viewer Size](https://img.shields.io/github/size/zzgiabaozzbui/human-context/human-context/md-folder-viewer.html?label=viewer%20size&color=informational)](./md-folder-viewer.html)

---

https://github.com/user-attachments/assets/34eefadc-edef-40b7-b56e-b54863e92087

> *File tree with token counts · Frontmatter as metadata cards · TOC with scroll spy · Dark mode*

---

## Table of Contents

- [🧠 The Story](#-the-story)
- [🤔 Why not Obsidian / Notion / GitBook?](#-why-not-obsidian--notion--gitbook)
- [⚡ Quick Start](#-quick-start)
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

Context engineering is splitting into two schools of thought.

**School A** says: everything should be `.md` — plain text, version-controlled, AI-readable, no fluff.
**School B** says: humans need a real UI — navigable, searchable, beautiful, with syntax highlighting and a table of contents.

Both are right. Both are incomplete. Most people pick a side. **Adults pick both.**

Your AI reads the `.md` files — your `CLAUDE.md`, your `memory/` folder, your `docs/`. But your teammates, your future self, your new hires — they need to *read* those files too, with actual eyes, in an actual browser, without squinting at raw markdown in VS Code.

**human-context** is the missing half. A single `.html` file you drop into any project. Open it in Chrome, point it at your folder, and instantly get a proper reading experience for every `.md` file in your codebase — file tree, syntax highlighting, TOC, cross-file navigation, dark mode, and token counts so you know exactly how much context you're feeding your AI.

No server. No `npm install`. No build step. **One file.**

---

## 🤔 Why not Obsidian / Notion / GitBook?

Because they require you to **move your files there**.

**human-context** reads the files **where they already are** — in your repo, next to your code, committed with your team. Open the `.html` file, pick the folder, read. Close it when you're done. Nothing moved, nothing synced, nothing uploaded.

| | human-context | Obsidian | Notion | GitBook |
| --- | --- | --- | --- | --- |
| Files stay in your repo | ✅ | ⚠️ vault | ❌ | ❌ |
| No account needed | ✅ | ✅ | ❌ | ❌ |
| No install / sync | ✅ | ❌ | ❌ | ❌ |
| Works offline | ✅ | ✅ | ❌ | ❌ |
| Token counting | ✅ | ❌ | ❌ | ❌ |
| One file, zero deps | ✅ | ❌ | ❌ | ❌ |

---

## ⚡ Quick Start

**1.** Download [`md-folder-viewer.html`](./md-folder-viewer.html)

**2.** Open it in Chrome or Edge (double-click the file)

**3.** Click **Open Folder** → select your project folder

That's it. Your folder becomes a navigable knowledge base.

> **Firefox users:** supported via file picker fallback, but folder memory won't persist between sessions (Firefox doesn't support the File System Access API).

---

> If this saved you time — [⭐ star it](https://github.com/zzgiabaozzbui/human-context). It helps others find it.

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
- [ ] **Support `.txt`, `.rst`, `.mdx`** — extend beyond markdown
- [ ] **Export folder as a static site** — offline-ready HTML bundle, shareable without a server
- [ ] **Print / PDF mode** — formatted output for documentation handoff
- [x] **Word count alongside token count** — more writing-friendly stats
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

### Tại sao repo này tồn tại

Context engineering đang chia làm 2 trường phái:

- **Phe `.md`**: tất cả nằm trong file markdown — AI đọc được, git-friendly, không phụ thuộc tool nào.
- **Phe `.html`**: con người cần giao diện thật — điều hướng được, tìm kiếm được, đẹp mắt.

Cả hai đều đúng. Cả hai đều thiếu. Đa số người chọn một trong hai. **Người lớn chọn cả hai.**

AI của bạn đọc file `.md` — `CLAUDE.md`, thư mục `memory/`, thư mục `docs/`. Nhưng đồng nghiệp, người mới vào nhóm, và chính bạn sau 3 tháng — cần đọc bằng mắt người thật, trong trình duyệt thật, không phải nhìn chằm chằm vào raw markdown.

**human-context** là nửa còn thiếu đó. Một file `.html` duy nhất. Mở lên, chọn folder, đọc. Không cần server, không cần cài gì.

### Tại sao không dùng Obsidian / Notion / GitBook?

Vì chúng yêu cầu bạn **chuyển file sang đó**.

**human-context** đọc file **ngay tại chỗ** — trong repo của bạn, bên cạnh code, được commit cùng team. Mở file `.html`, chọn folder, đọc. Đóng lại khi xong. Không có gì bị di chuyển, không sync, không upload.

### Cách dùng nhanh

**1.** Tải [`md-folder-viewer.html`](./md-folder-viewer.html)

**2.** Mở bằng Chrome hoặc Edge (double-click vào file)

**3.** Bấm **Open Folder** → chọn folder dự án

> **Firefox:** hỗ trợ qua file picker fallback, nhưng không nhớ folder giữa các session.

---

> Nếu tool này hữu ích — [⭐ star repo](https://github.com/zzgiabaozzbui/human-context) để người khác tìm thấy.

### Tính năng

- **🌲 Cây file** — icon tự động theo tên file/folder, có thể thu gọn
- **📊 Đếm token** — hiển thị token / ký tự / heading trên từng file
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

- [ ] **Điều hướng bằng phím** (`j` / `k`) — như IDE thật
- [ ] **Hỗ trợ `.txt`, `.rst`, `.mdx`** — mở rộng ngoài markdown
- [ ] **Export folder thành static site** — bundle HTML offline, share không cần server
- [ ] **Chế độ in / PDF** — output định dạng đẹp để handoff tài liệu
- [ ] **Word count bên cạnh token count** — thống kê thân thiện với người viết
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

### 为什么会有这个项目

上下文工程（Context Engineering）正在分裂成两个流派：

- **Markdown 派**：所有内容保存为 `.md` 文件 —— AI 可读、版本可控、零依赖。
- **HTML 派**：人类需要真正的界面 —— 可导航、可搜索、有语法高亮和目录。

两者都对。两者都不完整。大多数人选其一。**成熟的开发者两个都要。**

你的 AI 读 `.md` 文件 —— `CLAUDE.md`、`memory/` 目录、`docs/` 目录。但你的队友、新成员、三个月后的你自己——需要用真实的眼睛，在真实的浏览器里阅读这些文件。

**human-context** 就是缺失的那一半。一个单独的 `.html` 文件，放进任何项目。打开浏览器，选择文件夹，立即获得完整的阅读体验。无需服务器，无需 `npm install`，无需构建步骤。

### 为什么不用 Obsidian / Notion / GitBook？

因为它们要求你**把文件搬过去**。

**human-context** 读取文件**就在原处** —— 在你的仓库里，紧挨着代码，和团队一起提交。打开 `.html` 文件，选择文件夹，阅读。用完关掉。没有任何文件被移动、同步或上传。

### 快速开始

**1.** 下载 [`md-folder-viewer.html`](./md-folder-viewer.html)

**2.** 用 Chrome 或 Edge 打开（双击文件即可）

**3.** 点击 **Open Folder** → 选择你的项目文件夹

> **Firefox 用户：** 通过文件选择器支持，但 session 之间不会记忆文件夹。

---

> 如果对你有帮助 —— [⭐ 给个 Star](https://github.com/zzgiabaozzbui/human-context)，让更多人发现它。

### 功能特性

- **🌲 文件树** — 按文件名/文件夹自动分配图标，可折叠
- **📊 Token 统计** — 每个文件显示 token 数 / 字符数 / 标题数
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

如果你一直想为开源做贡献，但被复杂的 monorepo 和 CI 流程劝退 —— 这个项目就是为你准备的。

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

如果你改进了它 —— 请提交 PR。这个项目因大家的共同贡献而变得更好。

### 路线图

尚未实现的功能 —— 欢迎提 PR —— [在 Issues 中认领](https://github.com/zzgiabaozzbui/human-context/issues)：

- [ ] **键盘导航**（`j` / `k` 在文件间移动）—— 像真正的 IDE 一样
- [ ] **支持 `.txt`、`.rst`、`.mdx`** —— 扩展到 Markdown 之外
- [ ] **将文件夹导出为静态网站** —— 离线可用的 HTML 包，无需服务器即可分享
- [ ] **打印 / PDF 模式** —— 格式化输出，用于文档交接
- [ ] **在 Token 数旁显示字数统计** —— 对写作者更友好的统计
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

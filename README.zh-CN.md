# OpenResume

**你只需写好内容。** OpenResume 是一份简历模板，版式、PDF 导出和分享链接都由它自动完成——改两个文件、推送，即可得到可分享的 PDF 与链接。

**中文** | [**English**](README.md)

---

## 为什么用 OpenResume？

| 你来做 | 模板来做 |
|--------|----------|
| 在两个文件中编辑简历**内容** | 版式、字体与排版 |
| 推送到 GitHub | 在云端自动编译 PDF |
| 分享一个链接 | 托管 PDF 并生成固定链接 |

不用配 LaTeX、不用自己导出 PDF、不用研究怎么分享。专注写你的经历即可。

---

## 快速开始

### 1. 使用本模板

在本仓库页面点击绿色的 **Use this template** 按钮（或 Fork 本仓库），即可在你自己的账号下生成一份副本，结构完全一致。

### 2. 只改内容

| 简历 | 编辑文件 |
|------|----------|
| **英文** | `en/content.tex` |
| **中文** | `cn/content.tex` |

把占位内容换成你的姓名、教育、经历和技能。除非要改版式，否则**不要**修改 `resume.tex` 等模板文件。

### 3. 推送即构建、即分享

```bash
git add en/content.tex cn/content.tex
git commit -m "更新简历"
git push origin main
```

工作流跑完（约 1–2 分钟）后：

- **下载 PDF**：在 **Actions** 里打开最近一次运行 → 下载 `resume-pdfs` 产物。
- **分享链接**（将 `YOUR_USERNAME`、`YOUR_REPO` 换成你的 GitHub 用户名和仓库名）：
  - 英文：`https://github.com/YOUR_USERNAME/YOUR_REPO/raw/pdf/resume-en.pdf`
  - 中文：`https://github.com/YOUR_USERNAME/YOUR_REPO/raw/pdf/resume-cn.pdf`

可以把这些链接放在个人主页、LinkedIn 或直接发给招聘方。

---

## 仓库结构

```
openResume/
├── en/
│   ├── content.tex   ← 编辑：英文简历内容
│   └── resume.tex    ← 模板（除非改版式，否则勿动）
├── cn/
│   ├── content.tex   ← 编辑：中文简历内容
│   ├── resume.tex    ← 模板
│   ├── fonts/        ← 中文字体（保持不动）
│   └── images/       ← 可选：放 you.jpg 作为照片
└── .github/workflows/
    └── build-pdf.yml ← 推送时自动构建 PDF（无需修改）
```

---

## 本地编译（可选）

如需在本机编译 PDF：

- **英文**：在 `en/` 目录下执行 `pdflatex resume`（或用 `latexmk`）。
- **中文**：在 `cn/` 目录下执行 `xelatex resume`（或使用 XeLaTeX 的 `latexmk`）。

---

## 许可

模板与自动化脚本可自由使用。请将所有占位内容替换为你自己的信息；模板中不包含任何真实个人信息。

---

[**English**](README.md)

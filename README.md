# OpenResume

**OpenResume** is a public resume template repository. You focus only on **content**; layout, PDF export, and sharing are automated via GitHub Actions.

---

## Features / 特点

| English | 中文 |
|--------|------|
| **Content-only editing** — Edit only `en/content.tex` and `cn/content.tex`. No need to touch layout, fonts, or build scripts. | **只改内容** — 仅需编辑 `en/content.tex` 与 `cn/content.tex`，无需改版式、字体或构建脚本。 |
| **Auto build on push** — Push to `main` and PDFs are built in the cloud. | **推送即构建** — 推送到 `main` 后自动在云端编译 PDF。 |
| **Auto PDF hosting** — Built PDFs are published to the `pdf` branch for stable links. | **自动托管 PDF** — 编译后的 PDF 发布到 `pdf` 分支，提供固定链接。 |
| **Bilingual** — English (pdflatex) and Chinese (XeLaTeX) templates included. | **中英双语** — 内含英文（pdflatex）与中文（XeLaTeX）模板。 |

---

## Quick Start / 快速开始

### 1. Use this template / 使用本模板

Fork this repository or use GitHub’s “Use this template” to create your own repo. Replace all placeholder text in the content files with your information.

Fork 本仓库或使用 GitHub「Use this template」创建自己的仓库，将内容文件中的占位内容替换为您的信息。

### 2. Edit content only / 仅编辑内容

| Language | File to edit | 编辑文件 |
|----------|--------------|----------|
| English  | `en/content.tex` | 英文简历正文 |
| 中文     | `cn/content.tex` | 中文简历正文 |

Do not edit `resume.tex` or other template files unless you want to change layout.

除非要改版式，否则请勿修改 `resume.tex` 及其他模板文件。

### 3. Push to build / 推送即构建

```bash
git add en/content.tex cn/content.tex
git commit -m "Update resume content"
git push origin main
```

After the workflow runs:

- **Artifacts**: In the run’s summary, download the `resume-pdfs` artifact.
- **Stable links** (replace `YOUR_USERNAME` and `YOUR_REPO` with your GitHub username and repo name):
  - English: `https://github.com/YOUR_USERNAME/YOUR_REPO/raw/pdf/resume-en.pdf`
  - 中文: `https://github.com/YOUR_USERNAME/YOUR_REPO/raw/pdf/resume-cn.pdf`

工作流运行完成后：

- **产物**：在该次运行的摘要页下载 `resume-pdfs`。
- **固定链接**（将 `YOUR_USERNAME`、`YOUR_REPO` 换成你的 GitHub 用户名与仓库名）：
  - 英文：`https://github.com/YOUR_USERNAME/YOUR_REPO/raw/pdf/resume-en.pdf`
  - 中文：`https://github.com/YOUR_USERNAME/YOUR_REPO/raw/pdf/resume-cn.pdf`

---

## Repository structure / 仓库结构

```
openResume/
├── README.md
├── .gitignore
├── en/
│   ├── content.tex    ← Edit: English content only
│   └── resume.tex     ← Template (preamble + layout)
├── cn/
│   ├── content.tex    ← Edit: 中文内容
│   ├── resume.tex     ← 模板
│   ├── fonts/         ← Chinese fonts (do not remove)
│   └── images/        ← Optional: put you.jpg for photo
└── .github/workflows/
    └── build-pdf.yml  ← Build on push (no need to edit)
```

---

## Local build (optional) / 本地编译（可选）

- **English**: In the `en/` directory run `pdflatex resume` (or use latexmk).
- **中文**: In the `cn/` directory run `xelatex resume` (or latexmk with XeLaTeX).

---

## License / 许可

Template structure and automation are provided for reuse. Replace all placeholder content with your own; the template contains no real personal data.

模板结构与自动化脚本可自由使用。请将所有占位内容替换为您本人的信息；模板中不包含任何真实个人信息。

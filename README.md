# EasyResumeTex

**Build your resume with AI coding and Git tools.**

EasyResumeTex is a LaTeX resume template designed for a code-first workflow: your content lives in plain text, so you can edit with [Codex](https://openai.com/codex/), [GitHub Copilot](https://github.com/features/copilot), [Cursor](https://cursor.com), or any editor; version it with Git (e.g. on GitHub); and get PDFs and shareable links automatically on push. No local LaTeX setup, no manual export—just write, commit, and share.

[**中文说明**](README.zh-CN.md) | **English**

---

## Why this approach?

| You do | You get |
|--------|--------|
| Edit **content** in two files (`en/content.tex`, `cn/content.tex`) | Layout and PDFs handled by the template and CI |
| Use **AI coding tools** to polish wording, tailor bullets, fix grammar | Plain-text LaTeX works in any code editor and with any assistant |
| Use **Git** (branch, commit, diff, history) and host on GitHub/GitLab | Version control, cloud build via Actions, and one stable link to share |

No “final_v2_final.pdf” in a folder. No wrestling with Word or Google Docs. Your resume is a small codebase: AI helps you write it, Git helps you manage it.

---

## Quick Start

### 1. Use this template

On this repository page, click the green **Use this template** button (or fork the repo) to create your own copy.

### 2. Edit content only

| Resume | File to edit |
|--------|--------------|
| **English** | `en/content.tex` |
| **中文** | `cn/content.tex` |

Replace the placeholders with your info. Use AI assistants in your editor to refine wording. Do **not** edit `resume.tex` or other template files unless you want to change the layout.

### 3. Push to build and share

```bash
git add en/content.tex cn/content.tex
git commit -m "Update resume"
git push origin main
```

After the workflow runs (about 1–2 minutes):

- **Download PDFs**: **Actions** tab → latest run → download the `resume-pdfs` artifact.
- **Share links** (replace `YOUR_USERNAME` and `YOUR_REPO`):
  - English: `https://github.com/YOUR_USERNAME/YOUR_REPO/raw/pdf/resume-en.pdf`
  - 中文: `https://github.com/YOUR_USERNAME/YOUR_REPO/raw/pdf/resume-cn.pdf`
  - **Example PDFs** (this template): [resume-en.pdf](https://github.com/qbai99/EasyResumeTex/raw/pdf/resume-en.pdf) · [resume-cn.pdf](https://github.com/qbai99/EasyResumeTex/raw/pdf/resume-cn.pdf)

Use these links on your portfolio, LinkedIn, or with recruiters.

---

## Repository structure

```
EasyResumeTex/
├── en/
│   ├── content.tex   ← Edit: English resume content
│   └── resume.tex    ← Template (don’t edit unless changing layout)
├── cn/
│   ├── content.tex   ← Edit: 中文简历内容
│   ├── resume.tex    ← Template
│   ├── fonts/        ← Chinese fonts (keep as-is)
│   └── images/       ← Optional: add you.jpg for a photo
└── .github/workflows/
    └── build-pdf.yml ← Builds PDFs on push (no need to edit)
```

---

## Local build (optional)

- **English**: In `en/` run `pdflatex resume` (or `latexmk`).
- **中文**: In `cn/` run `xelatex resume` (or `latexmk` with XeLaTeX).

---

## License

Template and automation are free to use. Replace all placeholder content with your own; the template contains no real personal data.

---

[**中文说明**](README.zh-CN.md)

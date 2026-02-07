# OpenResume

**Focus on your content.** OpenResume is a resume template that handles layout, PDF export, and shareable links for you—edit two files, push, and you're done.

[**中文说明**](README.zh-CN.md) | **English**

---

## Why OpenResume?

| You do | We do |
|--------|--------|
| Edit your resume **content** in two simple files | Layout, typography, and formatting |
| Push to GitHub | Build PDFs in the cloud |
| Share one link | Host PDFs and provide stable URLs |

No LaTeX setup, no manual PDF export, no figuring out how to share. Just write your story.

---

## Quick Start

### 1. Use this template

On this repository page, click the green **Use this template** button (or fork the repo) to create your own copy. You’ll get a new repo under your account with the same structure.

### 2. Edit content only

| Resume | File to edit |
|--------|--------------|
| **English** | `en/content.tex` |
| **中文** | `cn/content.tex` |

Replace the placeholder text with your name, education, experience, and skills. Do **not** edit `resume.tex` or other template files unless you want to change the layout.

### 3. Push to build and share

```bash
git add en/content.tex cn/content.tex
git commit -m "Update resume"
git push origin main
```

After the workflow runs (about 1–2 minutes):

- **Download PDFs**: Open the latest run in the **Actions** tab → download the `resume-pdfs` artifact.
- **Share links** (replace `YOUR_USERNAME` and `YOUR_REPO` with your GitHub username and repo name):
  - English: `https://github.com/YOUR_USERNAME/YOUR_REPO/raw/pdf/resume-en.pdf`
  - 中文: `https://github.com/YOUR_USERNAME/YOUR_REPO/raw/pdf/resume-cn.pdf`

You can put these links on your portfolio, LinkedIn, or send them directly to recruiters.

---

## Repository structure

```
openResume/
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

If you want to compile PDFs on your machine:

- **English**: In the `en/` directory run `pdflatex resume` (or use `latexmk`).
- **中文**: In the `cn/` directory run `xelatex resume` (or `latexmk` with XeLaTeX).

---

## License

Template and automation are free to use. Replace all placeholder content with your own; the template contains no real personal data.

---

[**中文说明**](README.zh-CN.md)

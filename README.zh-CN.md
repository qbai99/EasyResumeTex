# EasyResumeTex

**用 AI 编程与 Git 工具来写简历。**

EasyResumeTex 是一份为「代码优先」流程设计的 LaTeX 简历模板：内容以纯文本存在，因此可以用 [Codex](https://openai.com/codex/)、[GitHub Copilot](https://github.com/features/copilot)、[Cursor](https://cursor.com) 或任意编辑器编辑；用 Git（如在 GitHub 上）做版本管理；推送后自动得到 PDF 和可分享链接。无需本地装 LaTeX、无需手动导出——写好、提交、分享即可。

**中文** | [**English**](README.md)

---

## 为什么用这种方式？

| 你来做 | 你能得到 |
|--------|----------|
| 只改两个文件里的**内容**（`en/content.tex`、`cn/content.tex`） | 版式和 PDF 由模板和 CI 自动处理 |
| 用 **AI 编程工具** 润色措辞、按岗位改经历、改语法 | 纯文本 LaTeX 可在任何代码编辑器里用任何助手编辑 |
| 用 **Git**（分支、提交、diff、历史）并托管在 GitHub/GitLab | 版本管理、云端自动构建、一条固定链接即可分享 |

不再在文件夹里堆「最终版_v2_真的最终.pdf」，也不用和 Word 或 Google Docs 较劲。简历就是一个小型代码库：AI 帮你写，Git 帮你管。

---

## 快速开始

### 1. 使用本模板

在本仓库页面点击绿色的 **Use this template** 按钮（或 Fork 本仓库），生成属于你自己的副本。

### 2. 只改内容

| 简历 | 编辑文件 |
|------|----------|
| **英文** | `en/content.tex` |
| **中文** | `cn/content.tex` |

把占位内容换成你的信息。在编辑器里用 AI 助手润色措辞。除非要改版式，否则**不要**改 `resume.tex` 等模板文件。

### 3. 推送即构建、即分享

```bash
git add en/content.tex cn/content.tex
git commit -m "更新简历"
git push origin main
```

工作流跑完（约 1–2 分钟）后：

- **下载 PDF**：打开 **Actions** → 最近一次运行 → 下载 `resume-pdfs` 产物。
- **分享链接**（将 `YOUR_USERNAME`、`YOUR_REPO` 换成你的用户名和仓库名）：
  - 英文：`https://github.com/YOUR_USERNAME/YOUR_REPO/raw/pdf/resume-en.pdf`
  - 中文：`https://github.com/YOUR_USERNAME/YOUR_REPO/raw/pdf/resume-cn.pdf`
  - **示例 PDF**（本模板产出）：[resume-en.pdf](https://github.com/qbai99/EasyResumeTex/raw/pdf/resume-en.pdf) · [resume-cn.pdf](https://github.com/qbai99/EasyResumeTex/raw/pdf/resume-cn.pdf)

可把链接放在个人主页、LinkedIn 或直接发给招聘方。

---

## 仓库结构

```
EasyResumeTex/
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

- **英文**：在 `en/` 下执行 `pdflatex resume`（或 `latexmk`）。
- **中文**：在 `cn/` 下执行 `xelatex resume`（或使用 XeLaTeX 的 `latexmk`）。

---

## 许可

模板与自动化脚本可自由使用。请将所有占位内容替换为你自己的信息；模板中不包含任何真实个人信息。

---

[**English**](README.md)

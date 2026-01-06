# modernnewspaper

**modernnewspaper** is a modern, Unicode-first LaTeX package for creating
newspaper-style documents. It is designed as a clean and extensible
alternative to the legacy `newspaper` package, with support for modern
typographic workflows and multilingual content.

This package is suitable for both **print** and **digital** newspapers,
newsletters, and bulletins.

---

## ✨ Features

- Unicode-first (XeLaTeX / LuaLaTeX)
- Clean newspaper masthead
- Native website URL support
- Volume, issue, and date metadata
- Multi-column layout
- Article system (headline, byline, body)
- Multilingual support (Myanmar, Arabic, Indic, CJK, etc.)
- Open-source and LPPL licensed

---

## 📦 Requirements

- **XeLaTeX** or **LuaLaTeX**
- `pdfLaTeX` is **not supported**

---

## 🔧 Installation

### Option 1: Local (recommended)

Copy `modernnewspaper.sty` into the same directory as your `.tex` file.

### Option 2: User installation

Install into your local `texmf` tree:

```
~/texmf/tex/latex/modernnewspaper/
```

---

## 🚀 Quick Start

```latex
\documentclass{article}
\usepackage{modernnewspaper}

\SetPaperName{Modern Newspaper}
\SetPaperSlogan{Informing the future}
\SetPaperLocation{Yangon, Myanmar}
\SetPaperWebsite{https://example.com}
\SetPaperVolume{1}
\SetPaperIssue{1}

\begin{document}

\MakePaperHeader

\BeginNewsColumns{2}

\begin{article}
\headline{Hello World}
\byline{Editor}

Unicode test:
မြန်မာစာ · العربية · हिन्दी · 中文 · English
\end{article}

\EndNewsColumns

\end{document}
```

Compile with:

```bash
xelatex example.tex
```

or

```bash
lualatex example.tex
```

---

## 📘 Documentation

- Full manual: `docs/manual.tex`
- Example file: `example/example.tex`

---

## 🗺 Roadmap

Planned features:

- Drop caps
- Image-wrapped articles
- RTL language support
- Theme system
- Accessibility improvements
- CTAN submission

---

## 🤝 Contributing

Contributions are welcome!

You can help by:
- Reporting bugs
- Suggesting features
- Improving documentation
- Submitting pull requests

Please keep changes compatible with **LPPL**.

---

## 📄 License

This project is licensed under the  
**LaTeX Project Public License (LPPL) v1.3c**.

See the `LICENSE` file or:
https://www.latex-project.org/lppl.txt

---

## 👤 Author

**Laithon**

GitHub: https://github.com/laithon

---

## ⭐ Status

This project is under active development.  
Current version: **v0.1.0**
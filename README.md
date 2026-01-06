# modernnewspaper

**modernnewspaper** is a modern, Unicode-first LaTeX package for creating
newspaper-style documents. It is designed as a clean, stable, and
extensible alternative to the legacy `newspaper` package, with first-class
support for multilingual content and modern typographic workflows.

This package is suitable for both **print** and **digital** newspapers,
newsletters, and bulletins.

---

## ✨ Features

- Unicode-first (XeLaTeX / LuaLaTeX)
- Clean front-page newspaper masthead
- Inner-page custom headers
- Volume, issue, date, and website metadata
- Multi-column layouts (2, 3, or more columns)
- Article system (headline, byline, dateline, body)
- Unicode-safe drop caps (works in columns)
- Column-safe images (no floating conflicts)
- Right-to-left (RTL) support for Arabic and similar scripts
- Multilingual support (Myanmar, Arabic, Hindi, Chinese, English, etc.)
- Open-source and LPPL licensed

---

## 📦 Requirements

- **XeLaTeX** or **LuaLaTeX**
- `pdfLaTeX` is **not supported**

### Fonts (important)

To display non-Latin scripts correctly, appropriate fonts must be installed.
Recommended free fonts include:

- Myanmar: **Noto Serif Myanmar**
- Arabic: **Amiri**
- Devanagari (Hindi): **Noto Serif Devanagari**
- Chinese: **Noto Serif CJK**

On Debian/Ubuntu:

```bash
sudo apt install fonts-noto fonts-noto-cjk fonts-amiri
```

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
\SetPaperIssue{5}
\SetPaperDate{\today}

\begin{document}

\MakePaperHeader

\BeginNewsColumns{3}

\begin{article}
\headline{Hello World}
\byline{Editor}

\DropCap{U}nicode text works across scripts:

မြန်မာစာ · العربية · हिन्दी · 中文 · English
\end{article}

\EndNewsColumns

\end{document}
```

Compile with:

```bash
xelatex example.tex
```

or:

```bash
lualatex example.tex
```

---

## 📰 Section Banners

Newspaper-style section banners can be created with rules above and below
centered text:

```latex
\SectionBanner{World News}
```

This produces:

```
--------------------
     World News
--------------------
```

---

## 📘 Documentation

- Full manual: `docs/manual.tex`
- Example file: `example/example.tex`

---

## 🗺 Roadmap

Planned improvements:

- Automatic font switching per script
- Running headers and page numbers
- Newspaper class file (`modernnewspaper.cls`)
- Theme presets
- CTAN submission

---

## 🤝 Contributing

Contributions are welcome!

You can help by:
- Reporting bugs
- Suggesting features
- Improving documentation
- Submitting pull requests

Please keep changes compatible with **LPPL** and focused on layout stability.

---

## 📄 License

This project is licensed under the  
**LaTeX Project Public License (LPPL) v1.3c**.

See the `LICENSE` file or:
https://www.latex-project.org/lppl.txt

---

## 👤 Author

**Laitei**

- GitHub: https://github.com/Laitei40  
- Facebook: https://www.facebook.com/laitei.fb  

---

## ⭐ Status

This project is under active development.  
Current version: **v0.2.1**

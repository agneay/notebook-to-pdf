# Notebook to PDF

Convert Jupyter notebooks (`.ipynb`) to PDF or standalone HTML right in your browser. Nothing is uploaded and there is nothing to install.

**Live site:** https://__OWNER__.github.io/notebook-to-pdf/

## Features

- Markdown cells with tables, images, cell attachments and LaTeX math (MathJax)
- Syntax-highlighted code cells with optional `In [n]` / `Out[n]` labels
- Outputs: stdout/stderr, plots (PNG/JPEG/SVG), pandas DataFrames and other HTML, error tracebacks
- Options to hide code or outputs, set a title header, choose A4 or US Letter, and add page numbers
- Styles: four document styles (Modern, Academic, Jupyter classic, Minimal), five code themes (Soft light, GitHub, Solarized light, Monokai, Black and white), three text sizes and three margin widths
- **Download HTML**: a single self-contained `.html` file with the same styling (math and images embedded). Printing it from your browser gives a PDF with selectable, searchable text
- Live preview before you download

## Usage

1. Open the live site (or `index.html` locally).
2. Choose or drag in a `.ipynb` file.
3. Adjust the options and style, then click **Download PDF** or **Download HTML**.

## How it works

It's a single static `index.html` with no build step. Libraries come from cdnjs:
[marked](https://github.com/markedjs/marked) for Markdown, [highlight.js](https://highlightjs.org/) for code,
[MathJax](https://www.mathjax.org/) for math, and [html2canvas](https://html2canvas.hertzen.com/) + [jsPDF](https://github.com/parallax/jsPDF) for the PDF.

The PDF is built one cell at a time, so long notebooks don't hit the browser's canvas size limit. Pages are images inside the PDF, so the text can't be selected; use **Download HTML** and print it if you need selectable text.

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deployment

Every push to `main` deploys to GitHub Pages through `.github/workflows/pages.yml`.

## License

MIT

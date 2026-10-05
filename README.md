# Notebook to PDF

Convert Jupyter notebooks (`.ipynb`) to PDF right in your browser. Nothing is uploaded and there is nothing to install.

**Live site:** https://__OWNER__.github.io/notebook-to-pdf/

## Features

- Markdown cells with tables, images, cell attachments and LaTeX math (MathJax)
- Syntax-highlighted code cells with optional `In [n]` / `Out[n]` labels
- Outputs: stdout/stderr, plots (PNG/JPEG/SVG), pandas DataFrames and other HTML, error tracebacks
- Options to hide code or outputs, set a title header, choose A4 or US Letter, and add page numbers
- Live preview before you download

## Usage

1. Open the live site (or `index.html` locally).
2. Choose or drag in a `.ipynb` file.
3. Adjust the options and click **Download PDF**.

## How it works

It's a single static `index.html` with no build step. Libraries come from cdnjs:
[marked](https://github.com/markedjs/marked) for Markdown, [highlight.js](https://highlightjs.org/) for code,
[MathJax](https://www.mathjax.org/) for math and [html2pdf.js](https://github.com/eKoopmans/html2pdf.js) for the PDF.

Pages are rendered as images inside the PDF, so the text can't be selected or searched.

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deployment

Every push to `main` deploys to GitHub Pages through `.github/workflows/pages.yml`.

## License

MIT

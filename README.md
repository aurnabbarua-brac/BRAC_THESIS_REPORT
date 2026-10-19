# BRAC University Thesis (LaTeX)

LaTeX source for a BRAC University thesis using the BRACU thesis template prepared by the Ayesha Abed Library. The project is organized into separate folders for chapters, preliminary pages, appendices, references, and figures.

## Project layout

- `main.tex` — document entry point, packages, thesis structure, and bibliography setup.
- `core/` — title page, declaration, approval, abstract, and other preliminary pages.
- `chapters/` — thesis chapter source files.
- `appendix/` — appendix source files.
- `bibliography/references.bib` — BibLaTeX bibliography database.
- `images/` — figures used by the thesis; keep referenced image files in this folder.

Keep files in their designated folders and update `main.tex` when adding or removing chapters, appendices, or other included material.

## Requirements

- Windows with [MiKTeX](https://miktex.org/download) installed and its executables available in `PATH`.
- Visual Studio Code with the [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) extension.
- The LaTeX packages used by the template, including `biblatex` with Biber, `nomencl`, and `makeindex`. MiKTeX can install missing packages when prompted; enable on-the-fly package installation if desired.

## View the thesis

[View the full thesis](main.pdf)

## Build

Open `main.tex` in VS Code and build it with LaTeX Workshop. The project uses `main.tex` as its root document.

For a command-line build with `latexmk`:

```powershell
latexmk -pdf -synctex=1 -interaction=nonstopmode main.tex
```

The build runs the needed LaTeX and Biber passes and writes `main.pdf` plus intermediate files in the project folder. The intermediate files and PDF output are excluded from Git by `.gitignore`; build again whenever you need a fresh PDF.

If `latexmk` is unavailable, install it through MiKTeX Console or build with the LaTeX Workshop extension after installing the required MiKTeX packages.

## Git sharing

Commit the `.tex` source files, `bibliography/references.bib`, and images referenced by the thesis. Do not commit generated build files, editor-specific settings, or machine-specific files. Review the staged files before publishing to make sure they contain only material you intend to share.


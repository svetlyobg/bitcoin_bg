# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Bulgarian translation of the Bitcoin whitepaper ("Биткойн: Директна електронна парична система") by Satoshi Nakamoto, typeset in LaTeX. The source document is `main.tex` and the reference original is `uk.pdf`.

## Build Commands

The document **must** be compiled with `xelatex` or `lualatex` (not `pdflatex`), because it uses `fontspec` and `polyglossia` for Bulgarian/Cyrillic support:

```bash
xelatex main.tex
```

The font `DejaVu Serif` (and `DejaVu Sans Mono` for monospace) must be installed on the system.

## Document Structure

Everything lives in a single file `main.tex`. The document uses:

- **polyglossia** with `\setmainlanguage{bulgarian}` for language support
- **tikz** and **forest** for diagrams (Merkle trees, block chains, privacy model)
- **amsmath** for mathematical formulas (Poisson probability calculations)
- **listings** for code snippets
- **hyperref** for PDF metadata and links

Custom `\forestset` styles (`blocklabel`, `headerlabel`, `container`, `headeritem`, `dashedbox`, `solidbox`) are defined in the preamble for block/Merkle tree diagrams.

## Language and Encoding

All content is in Bulgarian (Cyrillic). Commit messages are also in Bulgarian. When editing, preserve the Bulgarian language for all document text.

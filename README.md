# ASME Conference Paper Template

A LaTeX template for ASME conference papers using the `asmeconf` class. This template can be adapted to **any ASME conference** (IMECE, IDETC/CIE, SMASIS, etc.) by updating the conference-specific fields in `main.tex`.

## Adapting to Your Conference

The following fields in `main.tex` control the conference header and should be changed to match your target conference:

```latex
\ConfName{Proceedings of the ASME 20XX\linebreak Your Conference Full Name}
\ConfAcronym{CONFYEAR}          % e.g., IMECE2026, IDETC2026
\ConfDate{Month DD--DD, 20XX}   % e.g., November 8--12, 2026
\ConfCity{City, State/Province}  % e.g., Vancouver, BC, Canada
\PaperNo{CONF20XX-XXXXX}        % e.g., IMECE2026-XXXXX
```

## Conference Details (IMECE 2026)

The current configuration targets IMECE 2026:

- **Conference:** ASME 2026 International Mechanical Engineering Congress and Exposition (IMECE2026)
- **Venue:** Vancouver Convention Centre, Vancouver, British Columbia, Canada
- **Conference Dates:** November 8--12, 2026
- **Exhibition Dates:** November 9--11, 2026

## Origin

This template is based on the **asmeconf** LaTeX class (v1.46, dated 2026/01/10) from CTAN:

- **CTAN:** [ctan.org/pkg/asmeconf](https://ctan.org/pkg/asmeconf)
- **GitHub (issues):** [github.com/John02139/asmeconf](https://github.com/John02139/asmeconf)
- **ASME formatting guidelines:** [www.asme.org/publications-submissions/proceedings/formatting-the-paper](https://www.asme.org/publications-submissions/proceedings/formatting-the-paper)
- **Author:** John H. Lienhard V, Department of Mechanical Engineering, MIT
- **License:** MIT License

The `asmeconf` class provides:
- ASME-compliant fonts, margins, headings, captions, and reference formats
- Hyperlinks, PDF bookmarks, and metadata
- Inline or grid-style author blocks
- Line numbering for draft review
- Final column balancing
- PDF/A archival standard support
- BibTeX style (`asmeconf.bst`) matching current ASME reference formats with DOI/URL support

## Files

| File | Description |
|------|-------------|
| `main.tex` | Main document (single self-contained file) |
| `asmeconf.cls` | ASME conference class file (v1.46) |
| `asmeconf.bst` | BibTeX style for ASME reference formatting |
| `References.bib` | Bibliography file with sample entries |

## Usage

### Compile

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

### Class Options

| Option | Description |
|--------|-------------|
| `colorlinks` | Colored hyperlinks (remove before final ASME submission) |
| `balance` | Balance column heights on the last page |
| `lineno` | Line numbers for draft review (run twice) |
| `grid` | Traditional grid-style author block |
| `nofoot` | Omit ASME copyright footer |
| `nohead` | Omit conference headers |
| `upint` | Upright integral signs |

### Notes

- Remove `[colorlinks]` before final submission to ASME (all text must be black for print).
- `\DocumentMetadata{...}` requires LaTeX format 2022/06/01 or later. If your TeX Live is older, leave it commented out.
- The `asmeconf.cls` included here has minor patches for compatibility with TeX Live 2021.

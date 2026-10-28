# Changelog

## v1.1.0 — 2026-10-28

### Fixed
- `README.md`: `docs/Jumping_Robot.pdf` was labelled as the team's "written submission". It is actually the published IEEE RA-L paper under review (Chen et al., 2021). The README now labels it correctly and gives the full citation and DOI.

### Added
- `README.md`: a paper citation, team member names, a section-by-section summary of the presentation, an annotated repo tree, how to open each file, and a note that every quantitative result comes from the paper's simulations.
- `CHANGELOG.md` (this file).

### Notes
- There is no source code in this repository, so nothing was compiled or run. The files were checked for integrity: the `.pptx` archive passes `unzip -t` and loads in `python-pptx` (28 slides), the PDF opens and extracts with `pdftotext` (8 pages), and `figure.png` is a valid 2752×1536 PNG.
- The documents themselves were not changed.

## v1.0.0

- Initial upload: presentation, summary figure, and reference paper.

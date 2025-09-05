# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a personal resume/CV repository containing LaTeX source files for generating professional resume documents. The repository uses GitHub Pages hosting and maintains both LaTeX (.tex) and Markdown (.md) versions of the resume.

## Key Files

- `resume.tex` - Primary LaTeX source file containing resume content
- `resume.cls` - Custom LaTeX class file defining document structure and styling
- `resume.md` - Markdown version of the resume
- `resume.pdf` - Generated PDF output (built from LaTeX source)
- `resume.html` - HTML version for web display

## Build Commands

### PDF Generation
```bash
# Generate PDF from LaTeX source
pdflatex resume.tex

# Alternative using latexmk (handles dependencies automatically)
latexmk -pdf resume.tex

# Clean auxiliary files
latexmk -c resume.tex
```

### File Conversions
The repository maintains multiple formats of the same content. When updating the resume:

1. Edit the primary LaTeX source (`resume.tex`)
2. Generate PDF using `pdflatex resume.tex`
3. Update the Markdown version (`resume.md`) to match content changes
4. Commit all updated formats together

## LaTeX Environment

- Uses TinyTeX distribution located at `/Applications/TinyTeX/`
- Custom resume class (`resume.cls`) based on LaTeX Templates design
- Key packages: palatino (font), geometry (margins), hyperref (links), hyphenat (hyphenation control)
- Document uses 11pt font on letter paper with 0.5" margins

## Development Workflow

Since this is a documentation-focused repository:

1. Content changes should be made to `resume.tex` first
2. Rebuild PDF immediately after changes: `pdflatex resume.tex`
3. Verify PDF output before committing
4. Update corresponding Markdown version if needed
5. All auxiliary LaTeX files (`.aux`, `.log`, `.out`, etc.) are gitignored

## Content Structure

The resume follows a structured format with these sections:
- Profile (summary statement)
- Experience (chronological work history)
- Education
- Certifications & Accreditations
- Awards

Each section uses the custom `rSection` environment defined in `resume.cls`.
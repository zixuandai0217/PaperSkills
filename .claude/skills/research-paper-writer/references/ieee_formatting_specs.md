# IEEE Formatting Specifications

## Page Layout

### Paper Size
- **Size**: A4 (210mm × 297mm) or US Letter (8.5" × 11")
- **Orientation**: Portrait

### Margins
- **Top**: 19mm (0.75")
- **Bottom**: 43mm (1.69")
- **Left/Right**: 14.32mm (0.56")
- **Column separation**: 4.22mm (0.17")

### Columns
- **Layout**: Two-column
- **Column width**: Approximately 88mm (3.5")

## Typography

### Font
- **Primary**: Times New Roman throughout
- **Alternative**: Computer Modern (LaTeX default)

### Font Sizes

| Element | Size | Style |
|---------|------|-------|
| Title | 24pt | Bold |
| Author names | 11pt | Regular |
| Author affiliations | 10pt | Italic |
| Section headings | 10pt | Bold |
| Subsection headings | 10pt | Bold, Italic |
| Body text | 10pt | Regular |
| Figure/Table captions | 8pt | Regular |
| References | 9pt | Regular |
| Footnotes | 8pt | Regular |

### Line Spacing
- **Body text**: Single spacing
- **Between paragraphs**: 3pt spacing
- **Paragraph indentation**: None (block style)

## Section Numbering

### Format
- **Level 1**: 1., 2., 3. (bold, numbered)
- **Level 2**: 1.1, 1.2, 1.3 (bold, numbered)
- **Level 3**: 1.1.1, 1.1.2 (bold, italic, numbered)
- **Level 4+**: Run-in heading (bold, ends with period)

### Examples
```
1. Introduction

2. Related Work
  2.1. Traditional Methods
    2.1.1. Feature-based Approaches
  2.2. Deep Learning Methods

3. Methodology
  3.1. Architecture Overview
  3.2. Fusion Strategy
```

## Title and Author Information

### Title
- **Format**: Centered, 24pt bold
- **Position**: Top of first column
- **Length**: Concise, typically 10-15 words
- **Capitalization**: Title case (capitalize major words)

### Authors
- **Format**: Centered, 11pt
- **Order**: First name, middle initial, last name
- **Affiliation**: Below name, 10pt italic
- **Email**: Below affiliation, 10pt

### Example
```
Title of the Paper in Title Case

John A. Smith, Jane B. Doe, and Robert C. Johnson

Department of Computer Science, University Name, City, Country
{jsmith, jdoe, rjohnson}@university.edu
```

## Abstract and Keywords

### Abstract
- **Position**: Following author information
- **Heading**: "Abstract" - bold, 10pt
- **Format**: Single paragraph, 10pt
- **Length**: 150-250 words
- **Style**: Indented both sides (optional)

### Keywords
- **Position**: Following abstract
- **Heading**: "Index Terms" - bold, 10pt
- **Format**: 3-5 keywords, separated by commas
- **Style**: 10pt regular

### Example
```
Abstract—This paper proposes a novel approach to...
[150-250 words]

Index Terms—Keyword 1, keyword 2, keyword 3, keyword 4
```

## Figures and Tables

### Figures
- **Placement**: Top or bottom of column, or across both columns
- **Caption**: Below figure, 8pt
- **Format**: "Fig. X. Caption text."
- **Numbering**: Sequential (Fig. 1, Fig. 2, etc.)
- **Resolution**: Minimum 300 DPI for photographs, 600 DPI for line art

### Tables
- **Placement**: Top of column preferred
- **Caption**: Above table, 8pt
- **Format**: "TABLE I: Caption text"
- **Numbering**: Roman numerals (TABLE I, TABLE II)
- **Lines**: Horizontal lines only, no vertical lines
- **Alignment**: Centered within column

### Example Figure
```
[Figure centered in column]

Fig. 1. Architecture of the proposed fusion network.
```

### Example Table
```
TABLE I: Performance Comparison on Test Dataset

Method    | Accuracy | Precision | Recall
----------|----------|-----------|--------
Baseline  | 0.82     | 0.80      | 0.84
Proposed  | 0.91     | 0.89      | 0.92
```

## Equations

### Format
- **Numbering**: Right-aligned in parentheses
- **Style**: Centered, with 1-line spacing above and below
- **Reference**: "Equation (1)" or "(1)" in text

### Example
```
The loss function is defined as:

    L = αLcls + βLreg                    (1)

where Lcls is the classification loss and Lreg is the regression loss.
```

## Algorithms

### Format
- Use algorithm environment (algorithmic, algorithm2e packages)
- Numbered sequentially
- Caption above algorithm
- Reference as "Algorithm 1"

### Example
```
Algorithm 1: Fusion-Based Detection

Input: RGB image I_rgb, thermal image I_thermal
Output: Detection results D

1: Extract features: F_rgb ← CNN(I_rgb)
2: Extract features: F_thermal ← CNN(I_thermal)
3: Fuse features: F_fused ← Attention(F_rgb, F_thermal)
4: Detect objects: D ← Detector(F_fused)
5: return D
```

## References

### Format
- **Heading**: "References" - bold, 10pt, centered or left-aligned
- **Style**: 9pt, single spacing
- **Numbering**: Sequential [1], [2], [3]
- **Indentation**: Hanging indent (optional)

### IEEE Citation Style

**Journal Article:**
```
[1] A. Author and B. Author, "Title of article," Journal Name, vol. X, no. Y, pp. 123-456, Month Year.
```

**Conference Paper:**
```
[2] A. Author et al., "Title of paper," in Proc. Conference Name (Abbrev.), City, Country, Year, pp. 123-456.
```

**Book:**
```
[3] A. Author, Book Title, Xth ed. City, Country: Publisher, Year.
```

**Online/Website:**
```
[4] "Page Title," Website Name. [Online]. Available: URL
```

**Dataset:**
```
[5] A. Author, "Dataset name," Year. [Online]. Available: URL
```

## Page Numbers

- **First page**: No page number
- **Subsequent pages**: Bottom center, starting from page 2
- **Style**: Plain Arabic numerals (2, 3, 4...)

## Special Elements

### Footnotes
- **Marker**: Superscript Arabic numerals
- **Position**: Bottom of column
- **Size**: 8pt
- **Separator**: Short horizontal line above

### Acknowledgments
- **Heading**: "Acknowledgments" - bold, 10pt
- **Position**: Before references
- **Content**: Funding sources, contributions, thanks

### Author Biographies
- **Optional**: For journal papers
- **Format**: Photo (optional) + brief bio (50-100 words)
- **Content**: Education, current position, research interests

## LaTeX Template

### Basic Structure
```latex
\documentclass[10pt,conference]{IEEEtran}

\usepackage{cite}
\usepackage{amsmath}
\usepackage{graphicx}
\usepackage{algorithm}
\usepackage{algorithmic}

\begin{document}

\title{Title of Your Paper}

\author{
\IEEEauthorblockN{Author Name}
\IEEEauthorblockA{Institution\\
Email: author@institution.edu}
}

\maketitle

\begin{abstract}
Your abstract here...
\end{abstract}

\IEEEpeerreviewmaketitle

\section{Introduction}
...

\section{Related Work}
...

\section{Methodology}
...

\section{Experiments}
...

\section{Conclusion}
...

\bibliographystyle{IEEEtran}
\bibliography{references}

\end{document}
```

## Common Formatting Issues

### Avoid
- **Single-column format** (except for abstract)
- **Custom margins** or page sizes
- **Color figures** in print (use grayscale or ensure color is essential)
- **Footnotes in abstract or title**
- **Page numbers on first page**
- **Vertical lines in tables**

### Check
- [ ] All figures are high resolution
- [ ] Tables use horizontal lines only
- [ ] Equations are numbered and referenced
- [ ] References follow IEEE format
- [ ] No orphans or widows (single lines at page breaks)
- [ ] Consistent capitalization in titles and headings
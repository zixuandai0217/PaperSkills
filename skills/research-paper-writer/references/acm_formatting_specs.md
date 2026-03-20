# ACM Formatting Specifications

## Overview

ACM uses the ACM Primary Article Template for conference proceedings and journals. The format is similar to IEEE but has distinct differences in layout, metadata, and citation style.

## Document Class Options

### Standard Options
```latex
\documentclass[sigconf]{acmart}  % Conference proceedings
\documentclass[sigplan]{acmart}  % SIGPLAN conference
\documentclass[acmsmall]{acmart} % Small journal format
\documentclass[acmlarge]{acmart} % Large journal format
```

### Common Settings
```latex
\setcopyright{acmcopyright}  % or {rightsretained}, {acmlicensed}
\acmYear{2025}
\acmConference[Conference Abbrev]{Full Conference Name}{Month Day-Day, Year}{City, Country}
```

## Page Layout

### Paper Size
- **Size**: US Letter (8.5" × 11") or A4
- **Orientation**: Portrait

### Margins
- **Top/Bottom**: 1 inch (25.4mm)
- **Left/Right**: 0.75 inch (19mm)
- **Column separation**: 0.33 inch (8.5mm)

### Columns
- **Layout**: Two-column (main body), single-column (abstract)
- **Column width**: Approximately 3.33 inches (84.5mm)

## Typography

### Font
- **Primary**: Linux Libertine (serif), Biolinum (sans-serif)
- **Monospace**: Inconsolata
- **Math**: Libertine Math

### Font Sizes

| Element | Size | Style |
|---------|------|-------|
| Title | 18pt | Bold |
| Subtitle | 14pt | Regular |
| Author names | 12pt | Regular |
| Author affiliations | 10pt | Italic |
| Section headings | 12pt | Bold, Small Caps |
| Subsection headings | 11pt | Bold, Italic |
| Body text | 9pt | Regular |
| Figure/Table captions | 8pt | Regular |
| References | 8pt | Regular |
| Abstract | 9pt | Regular |

### Line Spacing
- **Body text**: Single spacing
- **Between paragraphs**: 6pt spacing
- **Paragraph indentation**: None (block style with spacing)

## Title and Author Information

### Title
- **Format**: Centered, 18pt bold
- **Capitalization**: Title case
- **Length**: Concise, typically 10-15 words
- **Special characters**: Avoid in running head

### Authors
- **Format**: Centered, grouped by affiliation
- **Style**: Name on one line, affiliation below
- **Email**: Grouped by institution

### Example
```
Title of the Paper: With Optional Subtitle

John A. Smith¹, Jane B. Doe², Robert C. Johnson¹

¹University Name, City, Country
{jsmith, rjohnson}@university.edu

²Another University, City, Country
jdoe@another.edu
```

## Abstract and Metadata

### Abstract
- **Position**: Single column at top of first page
- **Heading**: "Abstract" - bold, 12pt, small caps
- **Format**: One or two paragraphs, 9pt
- **Length**: 150-200 words
- **Style**: Block format, no indentation

### CCS Concepts
- **Position**: Below abstract
- **Heading**: "CCS Concepts" - bold
- **Format**: ACM Computing Classification System
- **Example**: 
  ```
  • Computing methodologies → Computer vision; Object detection
  • Information systems → Multimedia content creation
  ```

### Keywords
- **Position**: Below CCS Concepts
- **Heading**: "Keywords" - bold
- **Format**: 3-5 keywords, separated by semicolons
- **Example**: "multimodal fusion; object detection; thermal imaging; deep learning"

### ACM Reference Format
- **Position**: Bottom of first column (optional)
- **Format**: Standard ACM citation format for the paper itself
- **Example**:
  ```
  John A. Smith, Jane B. Doe, and Robert C. Johnson. 2025. Title of the Paper. 
  In Proceedings of Conference Name (Abbrev. '25). ACM, New York, NY, USA, 10 pages. 
  https://doi.org/xx.xxxx/xxxxxxx.xxxxxx
  ```

## Section Numbering

### Format
- **Level 1**: 1. INTRODUCTION (bold, small caps, numbered)
- **Level 2**: 1.1 Subsection Title (bold, numbered)
- **Level 3**: 1.1.1 Sub-subsection Title (bold, italic, numbered)
- **Level 4+**: Run-in heading (bold, ends with period)

### Examples
```
1. INTRODUCTION

2. RELATED WORK
  2.1. Traditional Approaches
    2.1.1. Feature-Based Methods
  2.2. Deep Learning Methods

3. METHODOLOGY
  3.1. System Architecture
```

## Figures and Tables

### Figures
- **Placement**: Top of column preferred, or across both columns
- **Caption**: Below figure, 8pt
- **Format**: "Figure X. Caption text." (note: spelled out, not abbreviated)
- **Numbering**: Sequential (Figure 1, Figure 2)
- **Width**: Single column (3.33") or full width (7")

### Tables
- **Placement**: Top of column preferred
- **Caption**: Above table, 8pt
- **Format**: "Table X. Caption text"
- **Numbering**: Sequential (Table 1, Table 2)
- **Lines**: Horizontal lines only, booktabs style
- **Width**: Column width or full width

### Example Figure
```
[Figure centered in column]

Figure 1. Architecture of the proposed fusion network.
```

### Example Table
```
Table 1. Performance Comparison on Test Dataset

Method    Accuracy   Precision   Recall
--------- ---------- ----------- --------
Baseline      0.82        0.80     0.84
Proposed      0.91        0.89     0.92
```

## Equations

### Format
- **Numbering**: Right-aligned in parentheses
- **Style**: Centered, with spacing above and below
- **Reference**: "Equation (1)" or "(1)" in text

### Example
```
The loss function is defined as:

    L = αLcls + βLreg                    (1)

where Lcls is the classification loss and Lreg is the regression loss.
```

## Algorithms

### Format
- Use algorithm environment
- Numbered sequentially
- Caption above algorithm
- Reference as "Algorithm 1"

### Example
```
Algorithm 1 Fusion-Based Detection

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
- **Heading**: "REFERENCES" - bold, small caps, centered
- **Style**: 8pt, single spacing
- **Numbering**: Sequential [1], [2], [3]

### ACM Citation Style

**Journal Article:**
```
[1] A. Author and B. Author. Year. Title of article. Journal Name X, Y (Month Year), 123-456. 
    https://doi.org/xx.xxxx/xxxxx
```

**Conference Paper:**
```
[2] A. Author, B. Author, and C. Author. Year. Title of paper. In Proceedings of Conference Name 
    (Abbrev. 'YY). ACM, New York, NY, USA, 123-456. https://doi.org/xx.xxxx/xxxxx
```

**Book:**
```
[3] A. Author. Year. Book Title, Xth ed. Publisher, City, Country.
```

**Online/Website:**
```
[4] A. Author. Year. Title of page. Retrieved Month Day, Year from URL
```

**Dataset:**
```
[5] A. Author. Year. Dataset name. Retrieved from URL
```

## Special Elements

### Footnotes
- **Marker**: Superscript symbols (*, †, ‡, §) or Arabic numerals
- **Position**: Bottom of page
- **Size**: 8pt
- **Separator**: Short horizontal rule

### Acknowledgments
- **Heading**: "Acknowledgments" - bold
- **Position**: Before references
- **Format**: Unnumbered section

### Author Biographies
- **Optional**: For some journals
- **Format**: Photo (optional) + brief bio
- **Position**: End of document

## LaTeX Template

### Basic Structure
```latex
\documentclass[sigconf]{acmart}

\setcopyright{acmcopyright}
\acmYear{2025}
\acmConference[CONF'25]{Conference Name}{Month Day-Day, 2025}{City, Country}

\usepackage{booktabs}
\usepackage{graphicx}

\begin{document}

\title{Title of Your Paper}
\subtitle{Optional Subtitle}

\author{John A. Smith}
\affiliation{
  \institution{University Name}
  \city{City}
  \country{Country}
}
\email{jsmith@university.edu}

\author{Jane B. Doe}
\affiliation{
  \institution{Another University}
  \city{City}
  \country{Country}
}
\email{jdoe@another.edu}

\begin{abstract}
Your abstract here...
\end{abstract}

\begin{CCSXML}
<ccs2012>
  <concept>
    <concept_id>10010147.10010178</concept_id>
    <concept_desc>Computing methodologies</concept_desc>
    <concept_significance>500</concept_significance>
  </concept>
</ccs2012>
\end{CCSXML}

\ccsdesc[500]{Computing methodologies~Computer vision}
\ccsdesc[300]{Computing methodologies~Object detection}

\keywords{multimodal fusion, object detection, thermal imaging}

\maketitle

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

\bibliographystyle{ACM-Reference-Format}
\bibliography{references}

\end{document}
```

## Key Differences from IEEE

| Feature | IEEE | ACM |
|---------|------|-----|
| Document class | `IEEEtran` | `acmart` |
| Title size | 24pt | 18pt |
| Section headings | Bold, numbered | Bold, small caps, numbered |
| Abstract position | Two-column | Single-column |
| CCS Concepts | Not required | Required |
| Keywords format | "Index Terms" | "Keywords" |
| Figure captions | "Fig. X" | "Figure X" |
| Table numbering | Roman numerals | Arabic numerals |
| Reference format | Different syntax | Different syntax |
| Copyright | Varies | ACM-specific options |

## Common Formatting Issues

### Avoid
- **Custom document classes** (use official ACM class)
- **Modified margins or fonts**
- **Missing CCS concepts**
- **Color figures** without checking print requirements
- **Page numbers on first page** (handled automatically)

### Check
- [ ] CCS concepts are complete and accurate
- [ ] Keywords are relevant and specific
- [ ] Copyright and conference information is correct
- [ ] All figures are high resolution
- [ ] Tables use booktabs style
- [ ] References follow ACM format
- [ ] DOIs are included where available
- [ ] No orphans or widows in text
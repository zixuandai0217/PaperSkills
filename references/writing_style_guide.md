# Academic Writing Style Guide

## Tone and Voice

### General Guidelines
- **Formal, objective, and precise language**: Avoid colloquialisms, contractions, and informal expressions
- **Third-person perspective**: Avoid "I" or "we" unless describing specific contributions (e.g., "We propose...", "Our approach...")
- **Tense usage**:
  - Present tense for established facts: "Deep learning achieves state-of-the-art results..."
  - Past tense for specific studies: "Smith et al. [1] demonstrated that..."
- **Clear, direct statements**: Avoid unnecessary complexity and wordiness

### Examples

**Poor:** "We think our method is pretty good and works better than others."
**Good:** "The proposed method outperforms existing approaches by 15% on the benchmark dataset."

**Poor:** "This is a very important problem that many people care about."
**Good:** "Accurate object detection in adverse weather conditions is critical for autonomous driving safety."

## Technical Precision

### Acronyms and Definitions
- **Define on first use**: "Context-Aware Systems (C-AS) enable..."
- **Consistent usage**: Use acronym after definition, don't mix forms
- **Common acronyms**: AI, ML, CNN, RNN, IoT (may not need definition in specialized papers)

### Quantification
- **Avoid vague terms** without data:
  - Poor: "significant improvement", "much better", "very fast"
  - Good: "15% accuracy improvement", "2x faster than baseline", "95% precision"
- **Use specific metrics**: accuracy, precision, recall, F1-score, mAP, latency, throughput

### Domain Terminology
- Use correct, consistent technical terms
- Follow field conventions for naming (e.g., "object detection" not "thing finder")
- Capitalize proper nouns: "Convolutional Neural Network (CNN)"

## Argumentation Structure

### Claim-Evidence Pattern
1. **State claim clearly**: "The proposed fusion strategy improves detection accuracy."
2. **Provide evidence**: "Experimental results show a 12% mAP improvement over the baseline."
3. **Explain mechanism**: "This improvement stems from the cross-modal attention mechanism..."

### Logical Progression
Follow this structure for clarity:
1. **Motivation**: Why is this problem important?
2. **Problem**: What specific challenge are you addressing?
3. **Solution**: What is your approach?
4. **Validation**: How do you know it works?

### Comparison with Related Work
- **Explicit comparison**: "Unlike [X] which focuses on Y, our approach addresses Z..."
- **Identify gaps**: "However, these approaches do not address..."
- **Position clearly**: "Our work complements [X] by..."

## Section-Specific Guidelines

### Abstract

**Structure (150-250 words):**
1. **Context** (1 sentence): Broad motivation
2. **Problem** (1-2 sentences): Specific gap or challenge
3. **Approach** (2-3 sentences): What you did
4. **Results** (2-3 sentences): Key findings with metrics
5. **Conclusion** (1 sentence): Significance

**Characteristics:**
- Self-contained (readable without full paper)
- No citations or references
- No undefined acronyms
- Specific numbers where possible

**Example:**
"Accurate object detection in adverse weather remains challenging due to degraded visibility. Existing methods rely solely on visible-light cameras, which fail in low-light or foggy conditions. This paper proposes a fusion-based detection framework that integrates thermal and visible imagery using a cross-modal attention mechanism. Experiments on the FLIR dataset demonstrate 15% higher mAP than RGB-only baselines, with particularly strong improvements at night (28% mAP gain). The approach achieves real-time performance at 30 FPS on edge devices. These results establish thermal-visible fusion as a practical solution for robust all-weather detection."

### Introduction

**Structure:**
1. **Hook** (1 paragraph): Compelling real-world problem or statistic
2. **Background** (1-2 paragraphs): Context and existing approaches
3. **Gap** (1 paragraph): What is missing or inadequate
4. **Contributions** (1 paragraph): Bullet list of 3-5 specific contributions
5. **Organization** (1 paragraph): Roadmap of paper sections

**Guidelines:**
- Build from general to specific (inverted pyramid)
- Use concrete examples, not abstractions
- Cite key related work to establish context
- Be specific about contributions (not "we make several contributions")

**Example Contribution List:**
"The main contributions of this paper are:
- A novel cross-modal fusion architecture that dynamically weights thermal and visible features based on environmental conditions.
- An attention mechanism specifically designed for small-object detection in fused imagery.
- Extensive evaluation on three benchmark datasets demonstrating state-of-the-art performance.
- Open-source implementation and pre-trained models for reproducibility."

### Related Work

**Organization:**
- Group by theme or approach (not chronological list)
- Typical categories: traditional methods, deep learning approaches, fusion strategies
- Use subsections for clarity in longer reviews

**Comparison Template:**
"[Author] et al. [X] proposed [method] for [problem]. Their approach [strengths]. However, [limitations]. In contrast, our method [differences]."

**Gap Identification:**
"While these approaches achieve [result], they do not address [specific challenge]. This paper focuses on [your focus]."

### Methodology

**Structure:**
1. **Overview**: High-level description and architecture diagram reference
2. **Components**: Detailed description of each module
3. **Algorithms**: Pseudocode for key procedures
4. **Design Rationale**: Why these choices were made

**Guidelines:**
- Use formal notation where appropriate (equations, sets, functions)
- Reference figures: "As shown in Figure 2..."
- Explain design decisions: "We use X rather than Y because..."
- Include complexity analysis if relevant

### Results

**Presentation:**
- **Tables**: For precise numerical comparison
- **Figures**: For trends, distributions, visualizations
- **Text**: Highlight key findings and guide interpretation

**Structure:**
1. **Setup**: Datasets, metrics, baselines, implementation details
2. **Main Results**: Quantitative comparison with tables
3. **Analysis**: Ablation studies, error analysis, qualitative examples
4. **Discussion**: Interpretation of findings

**Guidelines:**
- Present data objectively
- Acknowledge unexpected or negative results
- Compare with baselines quantitatively
- Statistical significance when applicable

### Conclusion

**Structure:**
1. **Summary**: Brief recap of contributions (1 paragraph)
2. **Impact**: Significance and implications (1 paragraph)
3. **Limitations**: Honest assessment (1 paragraph)
4. **Future Work**: Directions for continued research (1 paragraph)

**Guidelines:**
- Don't simply repeat abstract
- No new information or results
- Be honest about limitations
- Concrete future directions, not vague "more research needed"

## Common Mistakes to Avoid

### Language Issues
- **Contractions**: Use "do not" not "don't", "cannot" not "can't"
- **Informal expressions**: Avoid "pretty much", "kind of", "a lot"
- **Vague intensifiers**: "very", "quite", "rather", "fairly"
- **Absolute claims**: "always", "never", "all" (use "typically", "generally")

### Structural Issues
- **Missing context**: Jumping into technical details without motivation
- **Unclear contributions**: Vague statements about "improving performance"
- **Poor organization**: Sections that don't flow logically
- **Missing citations**: Claims without supporting references

### Technical Issues
- **Undefined terms**: Using acronyms or jargon without explanation
- **Inconsistent notation**: Changing symbols or terminology
- **Missing units**: Numbers without units or scales
- **Unverified claims**: Statements without evidence or citation

## Revision Checklist

Before finalizing, verify:

- [ ] Abstract is self-contained and 150-250 words
- [ ] Introduction has clear contribution list
- [ ] All acronyms defined on first use
- [ ] Figures and tables referenced in text
- [ ] Citations complete and properly formatted
- [ ] Results include quantitative comparisons
- [ ] Limitations honestly discussed
- [ ] No undefined technical terms
- [ ] Consistent tense throughout
- [ ] Logical flow between sections
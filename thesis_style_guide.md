# Thesis Style Guide

Source: department formatting instructions. LaTeX/Overleaf equivalents added
in brackets where the original refers to Word-specific features.

## 1. Title
Titles must state what was done, not just the topic.
- Weak: "Silicon microfluidics"
- Better: "Silicon microfluidic sensors"
- Good: "Fabrication and test of silicon microfluidic sensors"
- Strong: "Realisation and test of a novel microfluidic sensor"

Title page includes: writer's name, master program affiliation, time
period/date, institute, names of professor/assistants.
[LaTeX: populate \title, \author, \date in main.tex; add affiliation/
institute/advisor via \thanks{} or a custom title page.]

## 2. Summary with Project Description
- Open with the project description as originally formulated at the start.
- State purpose, methods used, results, main conclusions, recommendations.
- Stress novelty and impact.
- Not numbered.

## 3. Table of Contents
Chapters and sections (optionally subsections) with page numbers.
[LaTeX: \tableofcontents — generated and updated automatically on compile,
no manual update needed.]

## 4. Introduction
- Purpose, background, starting points, limitations, in more detail than the summary.
- Briefly explain approach and what is new.
- Explicitly separate your own contribution from prior/global work.
- Acknowledgements go here or in a separate Acknowledgements section before
  the Introduction.

## 5. Body of the Report
- Split into chapters as needed, but must read as one coherent argument —
  not a chronological log of what you did.
- Anything that doesn't fit the logical flow goes to an appendix, referenced
  from the text.
- Typical contents: theoretical background, design rationale, key design/
  layout, simulations/calculations, realisation details, measurement
  setup/method, discussion of results.

## 6. Conclusions
- All relevant conclusions, including negative results.
- Stress novelty and impact (scientific or industrial).
- New insights, outlook, recommendations for improvement go here.
- Do not introduce new results/concepts not already in the body.
- Keep it structured, not a loose list.

## 7. Symbol List
- Needed if there are many symbols. Alphabetic order (lowercase, uppercase,
  Greek). Meaning + units for each.
- Use standard symbols where they exist; never reuse one symbol for two
  meanings.
- Non-standard abbreviations go here too. Define each abbreviation at first
  use in the text, then use it consistently.
- Not numbered.

## Page Layout
[Original Word margin specs — not directly applicable in Overleaf, which
handles this via document class/geometry package. If a specific class or
margin spec is required by the department for LaTeX submissions, confirm
and set via \usepackage{geometry}.]

## Headers/Footers, Styles
[LaTeX equivalents: headers/footers via \usepackage{fancyhdr}; heading
levels via \section, \subsection, \subsubsection — no manual "style"
management needed, unlike Word.]

## Literature References
[Original uses Word endnotes. LaTeX equivalent: \usepackage{natbib} or
biblatex + references.bib, \cite{} in text, bibliography auto-numbered
and formatted by \bibliographystyle.]

## Chapters and Contents
- Start each chapter on a new page. [LaTeX: automatic with \chapter in the
  `report` class.]
- Place figures near the relevant text. Group information into paragraphs.

## Numbering
- **Chapters/sections**: decimal system (1, 1.1, 1.2, 2, 2.1, ...). Summary,
  appendices, literature list, symbol list are NOT numbered.
  [LaTeX: automatic via \section etc.; use \section*{} for the unnumbered
  ones like Summary.]
- **Formulas**: number essential/referenced formulas. Under ~20 formulas,
  simple sequential numbering is fine; otherwise use chapter-based
  numbering (3.1, 3.2, ...). [LaTeX: `equation` environment auto-numbers;
  chapter-based numbering via \numberwithin{equation}{chapter}.]
- **Tables**: Table 1, Table 2 or Table 3.1, Table 3.2.
  [LaTeX: `table` environment + \caption, auto-numbered.]
- **Figures**: Figure 1, Figure 2 or Fig. 3.1, Fig. 3.2. Captions must be
  self-explanatory — state what's shown: "Measured...", "Simulated...",
  "Theoretical...", "Comparison...". [LaTeX: `figure` environment +
  \caption, auto-numbered.]
- **Appendices**: group by type if there are many (e.g. "Graphs", "Mask
  layouts" as ToC entries, with individual items like "Graph A. First DC
  current measurement" inside).

## Language

**Sentence length**: average under 20 words/sentence; never exceed 35 in
the longest sentence. A sentence split by `;` or `:` counts as two.

**Avoid nested sub-clauses.** Bad example from the source doc:
"The differential equations, the solutions of which that must be solved
with eight constants, to be derived from the boundary conditions, are
known, have been derived." — don't write like this.

**Avoid overstressed constructions.** Prefer: "We borrowed lab equipment
from the IOA, but it was useless for our purpose." over "The lab equipment
that we borrowed from the IOA turned out to be useless for our purpose."

**Cut redundant words.** "We dry it slowly." beats "By slow and careful
evaporation of water we perform the needed dehydration until it is dry."

**Voice**: impersonal/passive is traditional in scientific writing, but
can obscure who did what. Active, personal voice ("I investigated...")
is acceptable and often clearer, especially in a thesis/lab-report
context. Prefer active over passive where it doesn't sound casual:
"Adding 3.6% wolfram doubled the pull strength" over "The pull strength
was doubled by the addition of 3.6% wolfram."

# Source — Notes in Modern Analysis (MATH S4061)

LaTeX source for the **class edition** of the lecture notes — Columbia University,
MATH S4061 (Introduction to Modern Analysis I), Summer 2026, based on the lectures
of Andre Carneiro. Student notes by Tyler Sotomayor.

Built PDFs are published at <https://tylersotomayor.github.io/real-anal/>.

## Build

Requires TeX Live or MacTeX (`pdflatex` + `makeindex`):

```sh
make            # complete notes (main-class.pdf) + each lecture PDF
make book       # just the complete notes
make lectures   # just the individual lecture PDFs
```

`main-class.tex` is the entry point for the complete notes (it loads `main.tex`).
Each `chapter-00.tex` / `lecture-NN.tex` also compiles on its own, e.g.
`pdflatex lecture-03.tex`. All house-style macros live in `analysisnotes.sty`.

## Contents

- `chapter-00.tex` — Foundations (logic, sets, functions, the craft of proof)
- `lecture-01.tex` … `lecture-07.tex` — the lectures
- `exercises-facts.tex`, `exercises-hw1.tex` … `exercises-hw3.tex` — problem sets with worked solutions
- `course-facts.tex` — the course list of facts
- `analysisnotes.sty` — shared house style

Exam material is not part of this public edition.

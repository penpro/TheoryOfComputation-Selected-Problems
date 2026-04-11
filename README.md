# Sum of Integers and Cubes

This repository contains a short mathematical presentation and supporting materials on two classic summation formulas:

- \(S(n) = 1 + 2 + \cdots + n = \frac{n(n+1)}{2}\)
- \(C(n) = 1^3 + 2^3 + \cdots + n^3 = \frac{1}{4}n^2(n+1)^2\)

The main goal is to prove these identities by induction and show the elegant result

\[
C(n) = S(n)^2.
\]

The project also includes historical context about Gauss and a brief note on why these summation formulas matter in calculus, especially when working with Riemann sums and integrals from first principles.

---

## Repository Contents

Place the files in this repository roughly like this:

```text
.
├── README.md
├── latex/
│   ├── sums_and_cubes.tex
│   └── sums_and_cubes.pdf
├── slideshow/
│   ├── sums_and_cubes_slides.pdf
│   └── sums_and_cubes_slides.pptx
└── media/
    └── youtube-link.txt
```

If your filenames differ, just update the links below.

---

## Included Materials

### LaTeX Source
- [LaTeX source file](./latex/sums_and_cubes.tex)

### Compiled PDF
- [PDF writeup](./latex/sums_and_cubes.pdf)

### Slideshow
- [Slide deck PDF](./slideshow/sums_and_cubes_slides.pdf)
- [Slide deck PowerPoint](./slideshow/sums_and_cubes_slides.pptx)

### Video Placeholder
- YouTube presentation link: **[PASTE YOUTUBE LINK HERE](https://www.youtube.com/)**

---

## Topic Summary

This project proves two well-known summation formulas using mathematical induction.

First, it shows that the sum of the first \(n\) natural numbers is

\[
S(n)=\frac{1}{2}n(n+1).
\]

Then it proves that the sum of the first \(n\) cubes is

\[
C(n)=\frac{1}{4}n^2(n+1)^2.
\]

Combining those results gives the striking identity

\[
1^3 + 2^3 + \cdots + n^3 = \left(1+2+\cdots+n\right)^2.
\]

In other words, the sum of the first \(n\) cubes is exactly the square of the sum of the first \(n\) integers.

---

## Historical Context

A famous story about Carl Friedrich Gauss says that as a child he was asked to add the integers from 1 to 100. Instead of adding them one at a time, he noticed that the numbers can be paired:

\[
1+100,\quad 2+99,\quad 3+98,\quad \dots
\]

Each pair has the same total, which leads quickly to the formula for

\[
1+2+\cdots+n.
\]

Whether the classroom story happened exactly as it is often told or not, the pairing idea is real and remains one of the cleanest ways to understand why the formula works.

---

## Connection to Calculus

These sums show up again in calculus when definite integrals are developed from Riemann sums. When an area is approximated by many narrow rectangles, the algebra often produces expressions involving

\[
1+2+\cdots+n, \qquad 1^2+2^2+\cdots+n^2, \qquad 1^3+2^3+\cdots+n^3.
\]

That makes these formulas more than just algebra patterns. They become part of the standard machinery used to move from finite sums to exact integrals.

---

## How to Compile the LaTeX File

From the repository root, a basic `pdflatex` workflow would look like this:

```bash
cd latex
pdflatex sums_and_cubes.tex
```

If you are using Overleaf, upload the `.tex` file and compile normally.

---

## Notes

- Update the file links if your folder names or filenames change.
- Replace the YouTube placeholder with the final video URL once the presentation is uploaded.
- Add any screenshots, diagrams, or presenter notes to the repository if needed.

---

## Author

Wesley Weaver

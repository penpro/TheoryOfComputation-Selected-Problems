# Theory of Computation — Selected Problems

This repository contains presentations and supporting materials for two sets of selected problems:

1. **Sums of Integers and Cubes** — induction proofs of two classic summation formulas.
2. **Sipser Chapter 1 — Exercises 1.19, 1.20(e–h), and 1.29(b)** — regular expressions, NFAs, and a pumping-lemma proof.

---

## Watch the Presentations

| # | Topic | Video |
|---|-------|-------|
| 1 | Sums of Integers and Cubes | **<https://youtu.be/2Oc9ijN37aA>** |
| 2 | Sipser 1.19, 1.20(e–h), 1.29(b) | **<https://youtu.be/_tsHJSzw73o>** |

---

## Files in This Repository

All files are stored directly in the root folder:

```text
.
├── 0.11 LaTeX.tex
├── 0.11 Slideshow.odp
├── 0.11 Slideshow.pptx
├── 0.11 Solution.pdf
├── Theory_of_Computation_1_19.tex
├── Theory_of_Computation_1_19.pdf
└── README.md
```

---

## File Descriptions

### Problem set 1 — Sums of Integers and Cubes

#### `0.11 LaTeX.tex`
The LaTeX source file for the written proof and supporting explanation.

#### `0.11 Solution.pdf`
The compiled PDF version of the writeup.

#### `0.11 Slideshow.odp`
The slideshow in OpenDocument Presentation format.

#### `0.11 Slideshow.pptx`
The slideshow in PowerPoint format.

### Problem set 2 — Sipser 1.19, 1.20(e–h), 1.29(b)

#### `Theory_of_Computation_1_19.tex`
The LaTeX source for the granular notes and solutions to Sipser's Exercises 1.19, 1.20(e–h), and Problem 1.29(b).

#### `Theory_of_Computation_1_19.pdf`
The compiled PDF version of the writeup, including TikZ diagrams of the NFAs.

### `README.md`
This file, which explains the contents and purpose of the repository.

---

## Topic Summary — Problem Set 1

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

### Historical Context

A famous story about Carl Friedrich Gauss says that as a child he was asked to add the integers from 1 to 100. Instead of adding them one at a time, he noticed that the numbers can be paired:

\[
1+100,\quad 2+99,\quad 3+98,\quad \dots
\]

Each pair has the same total, which leads quickly to the formula for

\[
1+2+\cdots+n.
\]

Whether the classroom story happened exactly as it is often told or not, the pairing idea is real and remains one of the cleanest ways to understand why the formula works.

### Connection to Calculus

These sums show up again in calculus when definite integrals are developed from Riemann sums. When an area is approximated by many narrow rectangles, the algebra often produces expressions involving

\[
1+2+\cdots+n, \qquad 1^2+2^2+\cdots+n^2, \qquad 1^3+2^3+\cdots+n^3.
\]

That makes these formulas more than just algebra patterns. They become part of the standard machinery used to move from finite sums to exact integrals.

---

## Topic Summary — Problem Set 2

This writeup walks through three exercises from Chapter 1 of Sipser's *Introduction to the Theory of Computation* (3rd ed.), with extra notation explanations so the symbols and conventions are clear before the problems are solved.

### Exercise 1.19 — Convert regular expressions to NFAs

For each regular expression, the language is translated into plain English, the automaton's required "memory" is identified, and a small NFA is presented both as a TikZ diagram and as a formal 5-tuple.

- **1.19(a)** \((0\cup 1)^*000(0\cup 1)^*\) — binary strings containing `000` as a substring.
- **1.19(b)** \((((00)^*(11))\cup 01)^*\) — strings made from blocks of either `(00)*11` or `01`.
- **1.19(c)** \(\varnothing^*\) — the language \(\{\varepsilon\}\), recognized by a single accepting state.

### Exercise 1.20(e–h) — Read regular expressions

Each expression is translated into English over the alphabet \(\Sigma=\{a,b\}\), then sample members and nonmembers are given to confirm the reading.

- **1.20(e)** \(\Sigma^*a\Sigma^*b\Sigma^*a\Sigma^*\) — strings with an `a`, then later a `b`, then later another `a`.
- **1.20(f)** \(aba \cup bab\) — exactly the two strings `aba` and `bab`.
- **1.20(g)** \((\varepsilon \cup a)b\) — exactly the strings `b` and `ab`.
- **1.20(h)** \((a \cup ba \cup bb)\Sigma^*\) — every string except \(\varepsilon\) and `b`.

### Problem 1.29(b) — Pumping-lemma proof

Shows that \(A_2 = \{www \mid w \in \{a,b\}^*\}\) is not regular by choosing the string \(s = (a^p b)(a^p b)(a^p b)\), forcing \(y = a^k\) with \(k \ge 1\), and pumping up to break the threefold-copy structure.

---

## How to Compile the LaTeX Files

From the repository root, a basic `pdflatex` workflow looks like this:

```bash
pdflatex "0.11 LaTeX.tex"
pdflatex Theory_of_Computation_1_19.tex
```

`Theory_of_Computation_1_19.tex` uses TikZ with the `automata`, `positioning`, and `arrows.meta` libraries, so a full TeX distribution (TeX Live or MiKTeX) is recommended.

If you are using Overleaf, upload the `.tex` file and compile normally.

---

## Author

Wesley Weaver

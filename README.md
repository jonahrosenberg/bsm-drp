# Classifying Constructability of Regular *n*-gons using Algebra

A short expository paper written for the **Budapest Semesters in Mathematics (BSM) Directed Reading Program**, Fall 2025.

**Author:** Jonah Rosenberg
**Teaching Assistant:** Balázs Attila Forman

## Overview

This paper proves the classical Gauss–Wantzel theorem characterizing which regular polygons can be constructed with a compass and straightedge. The main result:

> A regular *n*-gon is constructible if and only if
> $$n = 2^k p_1 p_2 \cdots p_t$$
> where $k \in \mathbb{N} \cup \{0\}$ and the $p_i$ are *distinct Fermat primes*.

## Outline of the argument

The proof translates the geometric question of constructibility into algebra and field theory:

1. **Constructible numbers form a field.** Starting from the points $0, 1 \in \mathbb{C}$, the set of points constructible with compass and straightedge is shown to be a subfield of $\mathbb{C}$, closed under addition, negation, multiplication, and division.
2. **Quadratic tower characterization.** Any new point obtained by intersecting lines and circles has coordinates lying in at most a quadratic extension of the current field. Hence every constructible point lives in a tower
   $$\mathbb{Q} = K_0 \subseteq K_1 \subseteq \cdots \subseteq K_m = \mathbb{Q}(\alpha), \qquad [K_{i+1}:K_i] = 2,$$
   so $[\mathbb{Q}(\alpha):\mathbb{Q}]$ is a power of two.
3. **Reduction to roots of unity.** A regular *n*-gon is constructible iff the primitive root of unity $\zeta_n$ is constructible.
4. **Cyclotomic degree.** Using $\mathbb{Q}$-embeddings, $[\mathbb{Q}(\zeta_n):\mathbb{Q}] = \varphi(n)$, where $\varphi$ is Euler's totient function.
5. **Galois-theoretic criterion.** $\zeta_n$ is constructible iff $\varphi(n) = 2^m$ for some $m$.
6. **Number-theoretic conclusion.** Analyzing when $\varphi(n)$ is a power of two yields exactly the Fermat-prime condition above.

## Repository contents

| File | Description |
|------|-------------|
| [main.tex](main.tex) | LaTeX source of the paper |
| [BSM_DRP.pdf](BSM_DRP.pdf) | Compiled PDF |

## Building

Compile the source with any standard LaTeX distribution (e.g. TeX Live, MiKTeX):

```bash
pdflatex main.tex
```

The document uses `amsmath`/`amsthm`, `tikz` (with `tikz-cd`), `hyperref`, and other common packages, all included in a full TeX installation.

## References

- David S. Dummit and Richard M. Foote, *Abstract Algebra*, 3rd ed., John Wiley & Sons, 2004.
- Ian N. Stewart, *Galois Theory*, 4th ed., Chapman & Hall/CRC, 2015.
- Martin Bishop, *Abstract Algebra III – Galois Theory*, Northwestern University, Spring 2025.

# Open statement (not a theorem)

Author: Benjamin Stanley Frohman (frohmanbenjamin@gmail.com)
Repository: https://github.com/BenFrohman/3n-plus-c-cycle-census

This file deposits the Collatz conjecture in the notation of this project.
It is **not proved** by Theorems 1–6, Corollary 4, the inverse-tree drawing, or the prefix census.

---

## Definition of the missing set

Let

$$
C_+(n)=
\begin{cases}
n/2 & n\text{ even},\\
3n+1 & n\text{ odd},
\end{cases}
$$

and let

$$
\operatorname{Pred}(1)=\{n\in\mathbb{Z}_{>0}:\exists k\ge 0\text{ with }C_+^k(n)=1\}.
$$

The missing set is

$$
\Delta \;:=\; \mathbb{Z}_{>0}\setminus\operatorname{Pred}(1).
$$

On the positive integers, a forward orbit that never hits \(1\) either enters a cycle that does not contain \(1\), or visits no integer twice and is unbounded. Hence the dichotomy

$$
\Delta=\Delta_{\mathrm{cyc}}\cup\Delta_{\mathrm{div}}.
$$

There is no third cell: a bounded non-cycling orbit in \(\mathbb{Z}_{>0}\) would repeat a value, hence cycle.

---

## Missing Lemma L (Collatz)

For every integer \(n>0\) there exists an integer \(k\ge 0\) such that

$$
C_+^k(n)=1.
$$

Equivalently, the forward orbit of \(n\) enters the cycle \(4\to 2\to 1\).

Equivalently,

$$
\operatorname{Pred}(1)=\mathbb{Z}_{>0}\qquad(\Delta=\emptyset).
$$

**Status: open.** This is the Collatz conjecture.

---

## Discharge conditions

Any one of the following, together with the dichotomy above, would prove L:

1. \(\Delta_{\mathrm{cyc}}=\emptyset\) and \(\Delta_{\mathrm{div}}=\emptyset\).
2. \(\operatorname{Pred}(1)=\mathbb{N}\).
3. A second-cycle obstruction that covers every residue class, together with a proof that no positive orbit diverges.

These three are equivalent to L. None of them is proved in this repository.

---

## What is already proved (does not discharge L)

- Theorem 1: one point of \(\operatorname{Pred}(1)\).
- Theorem 2: conjugacy \(C_{-c}(n)=-C_c(-n)\).
- Theorem 3 / Corollary 4: \(C_-\) has three positive cycles; the shared shape does not force a unique sink.
- Theorem 5: \(\operatorname{Pred}(1)\) is infinite.
- Theorem 6: under the geometric model, \(\mathbb{E}[\log M_a]=\log(a/4)\).

Barina empties \(\Delta\) on \(\{1,\ldots,2^{71}-1\}\). Steiner and Eliahou constrain \(\Delta_{\mathrm{cyc}}\). Terras and Tao constrain almost all orbits. None of those is L.

Do not deposit this file as a solution of the Collatz conjecture.

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

Write

- \(\Delta_{\mathrm{cyc}}\) for the set of \(n\) whose forward orbit eventually enters a cycle that does not contain \(1\),
- \(\Delta_{\mathrm{div}}\) for the set of \(n\) whose forward orbit visits no integer twice and is unbounded.

---

## Lemma D (dichotomy; proved)

$$
\Delta=\Delta_{\mathrm{cyc}}\cup\Delta_{\mathrm{div}}.
$$

*Proof.* Let \(n>0\) and suppose \(n\notin\operatorname{Pred}(1)\). The forward orbit never equals \(1\). If some value repeats, the orbit has entered a cycle; that cycle cannot contain \(1\), so \(n\in\Delta_{\mathrm{cyc}}\). If no value repeats, the orbit is an infinite injective sequence in \(\mathbb{Z}_{>0}\), hence unbounded, so \(n\in\Delta_{\mathrm{div}}\). There is no third cell: a bounded non-cycling orbit in \(\mathbb{Z}_{>0}\) would repeat a value by finiteness, hence cycle.

---

## Lemma 1 (no second cycle; OPEN)

$$
\Delta_{\mathrm{cyc}}=\emptyset.
$$

That is: \(C_+\) has no positive cycle other than \(4\to 2\to 1\).

Partial results, not a proof: Steiner rules out a nontrivial one-odd-term cycle; later work rules out many short cycle types; Eliahou constrains the length of any other cycle given a verification floor; Barina implies no other cycle intersects \(\{1,\ldots,2^{71}-1\}\).

**Status: open.**

---

## Lemma 2 (no divergent ray; OPEN)

$$
\Delta_{\mathrm{div}}=\emptyset.
$$

That is: no positive orbit of \(C_+\) is infinite, injective, and unbounded.

Partial results, not a proof: Terras, a density-one set of starts has finite stopping time; Tao, almost all orbits (logarithmic density) become almost bounded; Barina, no divergent ray starts in \(\{1,\ldots,2^{71}-1\}\).

**Status: open.**

---

## Lemma 3 / Missing Lemma L (Collatz; OPEN)

For every integer \(n>0\) there exists an integer \(k\ge 0\) such that

$$
C_+^k(n)=1.
$$

Equivalently, the forward orbit of \(n\) enters \(4\to 2\to 1\). Equivalently \(\operatorname{Pred}(1)=\mathbb{Z}_{>0}\).

---

## Conditional theorem (proved as an implication)

Lemma D + Lemma 1 + Lemma 2 imply Lemma L.

*Proof.* By D, \(\Delta=\Delta_{\mathrm{cyc}}\cup\Delta_{\mathrm{div}}\). Lemmas 1 and 2 empty both cells, so \(\Delta=\emptyset\), so every \(n>0\) lies in \(\operatorname{Pred}(1)\).

The implication is not a discharge of L. Lemmas 1 and 2 remain open. This repository does not prove Collatz.

---

## What is already proved (does not discharge L)

- Theorem 1: one point of \(\operatorname{Pred}(1)\).
- Theorem 2: conjugacy \(C_{-c}(n)=-C_c(-n)\).
- Theorem 3 / Corollary 4: \(C_-\) has three positive cycles; the shared shape does not force a unique sink.
- Theorem 5: \(\operatorname{Pred}(1)\) is infinite.
- Theorem 6: under the geometric model, \(\mathbb{E}[\log M_a]=\log(a/4)\).

Do not deposit this file as a solution of the Collatz conjecture.

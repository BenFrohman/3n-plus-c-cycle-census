# Lemma L — cycles and rays

**Status: OPEN.** This file is not a proof of the Collatz conjecture.

Author: Benjamin Stanley Frohman (frohmanbenjamin@gmail.com)

Lemma L needs both cells of \(\Delta\) emptied. Lemma D is the reason.

---

## Statement

**Lemma L.** For every integer \(n>0\) there exists \(k\ge 0\) with \(C_+^k(n)=1\).

Equivalently \(\operatorname{Pred}(1)=\mathbb{N}\). Equivalently \(\Delta=\emptyset\).

---

## Why both halves

Lemma D (proved): \(\Delta=\Delta_{\mathrm{cyc}}\cup\Delta_{\mathrm{div}}\), disjoint.

- Lemma 1 empties \(\Delta_{\mathrm{cyc}}\) (no extra cycle).
- Lemma 2 empties \(\Delta_{\mathrm{div}}\) (no divergent ray).
- Lemma 3: 1 and 2 together empty \(\Delta\), hence L.

Killing only cycles leaves possible rays. Killing only rays leaves possible extra cycles. Either leftover is a counterexample to L. There is no third cell and no fourth route that skips one of them.

---

## Cycles half (Lemma 1)

Toward, not a proof: Steiner / Proposition 1.1 (no 1-odd-term cycle); Simons (no 2-cycle); Hercher (no \(m\)-cycle for \(m\le 91\); Eliahou windows on length given a floor; Barina (no extra cycle meets \(\{1,\ldots,2^{71}-1\}\)).

Residual: an \(m\ge 92\) cycle above \(2^{71}\) with length in the Eliahou semigroup, or a shape not captured as an \(m\)-cycle of that kind.

---

## Rays half (Lemma 2)

Toward, not a proof: Terras (density-one finite stopping time); Everett; Korec; Tao 2019 (almost all orbits almost bounded); Barina (no ray starts below \(2^{71}\)).

CST (Terras coefficient stopping time) would kill extra *cycles* (smallest term of a cycle has infinite stopping time but finite coefficient stopping time). CST is not Lemma 2. Almost-all boundedness is not all-boundedness.

Naive Lyapunov functions \(V(n)=n\) and \(V(n)=\log n\) fail on \(v=1\) steps (\(27\to 41\)). See [`GRIND.md`](GRIND.md).

---

## Ace the world

The world-class result would be a proof of both halves, or a single argument that every vertex of \(G_+\) has a path to 1. That result is not in this repository. This file records the conjunction. It does not fire it.

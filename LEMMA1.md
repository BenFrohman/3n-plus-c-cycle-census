# Lemma 1 details

**Status: OPEN.** This file is not a proof that \(\Delta_{\mathrm{cyc}}=\emptyset\).

Author: Benjamin Stanley Frohman (frohmanbenjamin@gmail.com)  
Repository: https://github.com/BenFrohman/3n-plus-c-cycle-census

Lemma 1 is the no-second-cycle half of Collatz. Details below are constraints and equivalent forms, not a proof that the set is empty.

---

## Statement

**Lemma 1.** \(\Delta_{\mathrm{cyc}}=\emptyset\).

That is: the only cycle of \(C_+\) in \(\mathbb{Z}_{>0}\) is \(4\to 2\to 1\).

Equivalent forms, all open:

- \(C_+\) has a unique positive cycle;
- there is no tuple of odd positives \(n_0,\ldots,n_{K-1}\) with \(K\ge 1\), not equal to \(\{1\}\), closed under the Syracuse map \(S_3\);
- the only positive solution of the Steiner identity below is \(K=1\), \(L=2\), \(n_0=1\).

---

## The identity a cycle would have to solve

Let the odd terms be \(n_0,\ldots,n_{K-1}\) and \(v_i=v_2(3n_i+1)\ge 1\), \(L=\sum v_i\). Then

$$
n_{i+1}=\frac{3n_i+1}{2^{v_i}},\qquad n_K=n_0,
$$

which telescopes to

$$
(2^L-3^K)\,n_0=\sum_{i=0}^{K-1}3^{K-1-i}\,2^{s_i},
$$

with \(s_i\) the partial sums of the \(v\)'s. So \(2^L-3^K\) divides that sum, and

$$
\Bigl\lvert\frac{L}{K}-\log_2 3\Bigr\rvert
$$

is small. An extra cycle is a good rational approximation to \(\log_2 3\) with a positivity constraint on every \(n_i\). The trivial cycle is the solution \(K=1\), \(L=2\), \(n_0=1\).

---

## Circuit type (\(m\)-cycles)

An \(m\)-cycle, in the Simons–de Weger / Hercher sense, is a cycle assembled from \(m\) blocks of the form “a run of odd-to-odd rises, then a run of pure halvings.” Steiner is \(m=1\). Simons is \(m=2\). Hercher: no such block-decomposition with \(m\le 91\). That is not “no cycle of hailstone length \(\le 91\).” It is “no cycle of that block shape with \(m\le 91\).” If an extra cycle exists it is more tangled than those \(91\) block types, or it has \(m\ge 92\).

---

## What the verification floor does

Let \(X_0\) be a number such that every start in \(1,\ldots,X_0\) reaches \(1\). Currently \(X_0=2^{71}\) (Barina). Then:

- the smallest term of any extra cycle is \(>X_0\);
- Eliahou-type continued-fraction arguments turn that floor into a lower bound on \(K\), the number of odd terms;
- raising \(X_0\) raises the bound on \(K\), but never makes \(K=\infty\).

So Lemma 1 is not implied by any finite \(X_0\). The prefix fact

$$
\Delta_{\mathrm{cyc}}\cap\{1,\ldots,2^{71}-1\}=\emptyset
$$

is proved. The claim \(\Delta_{\mathrm{cyc}}=\emptyset\) is the same statement with \(2^{71}\) replaced by \(\infty\).

---

## Invariance and size if nonempty

If Lemma 1 fails, \(\Delta_{\mathrm{cyc}}\) is infinite: the extra cycle plus its entire inverse tree (always \(\times 2\), sometimes \((m-1)/3\)). It is forward- and backward-invariant, disjoint from \(\operatorname{Pred}(1)\), and lies entirely above \(X_0\).

---

## What does *not* prove Lemma 1

- The shape of the rule. \(C_-\) has three positive cycles.
- Model drift \(\log(3/4)<0\). Cycles have realized drift \(0\).
- Theorem 5 (infinite inverse tree of \(1\)). That tree can coexist with another tree.
- Lemma D or Lemma R. Those are about the partition of \(\Delta\), not about emptying one cell.
- Graph theory. The functional graph restates D; connectivity of \(G_+\) is L again.

---

## What a proof of Lemma 1 would have to do

Show that the Steiner identity has no other positive integer solution \((K,L,n_0,v_0,\ldots,v_{K-1})\), or that every such solution forces some \(n_i\le X_0\), contradicting Barina. That Diophantine statement is open.

Lemma 1 remains open. It is half of Lemma L. The other half is Lemma 2.

Do not deposit this file as a solution of the Collatz conjecture.

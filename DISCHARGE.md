# What would discharge Lemmas 1, 2, and L

Author: Benjamin Stanley Frohman (frohmanbenjamin@gmail.com)
Repository: https://github.com/BenFrohman/3n-plus-c-cycle-census

This file is a menu of sufficient conditions. None of them is proved here.
Graph theory licenses Lemma D and the language of components. Next discharges have to see the coefficient 3.

---

## What would discharge Lemma 1

Any one of these, with no gap:

1. **Steiner identity has only the trivial positive solution.**
   Show that
   $$
   (2^L-3^K)n_0=\sum_{i=0}^{K-1}3^{K-1-i}\,2^{s_i}
   $$
   has no solution in odd positives \(n_i\) except \(K=1\), \(L=2\), \(n_0=1\).

2. **Every extra solution forces a term \(\le X_0\).**
   Then Barina contradicts it. Eliahou-type bounds do this for short or structured cycles (\(m\le 91\)). They do not do it for every cycle shape.

3. **A complete \(m\)-cycle obstruction for all \(m\).**
   Hercher stops at \(91\). An argument that works for arbitrary \(m\) would finish Lemma 1.

Until one of those three exists, Lemma 1 stays open.

---

## What would discharge Lemma 2

Any one of these, with no gap:

1. **A Lyapunov function on all of \(\mathbb{Z}_{>0}\).**
   A function \(V\) with \(V(C_+(n))<V(n)\) outside a finite set (or outside \(\operatorname{Pred}(1)\)). Then no injective unbounded ray.

2. **Upgrade Terras / Tao from almost-all to all.**
   Density one and logarithmic density leave a possible zero-density set of rays. Closing that zero-density set is Lemma 2.

3. **Show that a divergent ray would violate the same Diophantine approximation that cycles do,** but in the other direction (\(L/K\) too far from \(\log_2 3\) for too long). Heuristic, not a theorem, until the error term is controlled uniformly.

The model mean \(\log(3/4)<0\) is the outline of (3). It is not (3).

---

## What would discharge L

Lemma D plus both of the above. Equivalently: a directed path in \(G_+\) from every vertex to \(1\). Equivalently: \(\operatorname{Pred}(1)=\mathbb{N}\).

There is no fourth route that skips 1 and 2. A spanning-tree construction is L under another name. A 2-adic connectedness theorem lives on \(\mathbb{Z}_2\), not on \(\mathbb{N}\). Conway-style undecidability for generalized maps is a warning that some nearby graphs are not decidable; it does not decide this one.

---

## What to write next

The only next deposit that would be new mathematics is an attack on the Steiner identity or a Lyapunov argument, with every inequality written out. The next deposit that is not new mathematics is another restatement of D, R, and the implication.

Neither this file nor LEMMA1.md nor LEMMA2.md discharges L.

# What would discharge Lemmas 1, 2, and L

**None of the items below is proved in this repository.**

Author: Benjamin Stanley Frohman (frohmanbenjamin@gmail.com)  
See also [`CONJECTURE.md`](CONJECTURE.md), [`LEMMA1.md`](LEMMA1.md), [`LEMMA2.md`](LEMMA2.md).

Graph theory is done. It gave Lemma D and the word component. Next discharges have to see the coefficient 3.

---

## What would discharge Lemma 1

Any one of these, with no gap:

1. **Steiner identity has only the trivial positive solution.**  
   Show that
   $$
   (2^L-3^K)n_0=\sum_{i=0}^{K-1}3^{K-1-i}\,2^{s_i}
   $$
   has no solution in odd positives `n_i` except `K=1`, `L=2`, `n_0=1`.

2. **Every extra solution forces a term `\le X_0`.**  
   Then Barina contradicts it. Eliahou-type bounds do this for short or structured cycles (`m\le 91`). They do not do it for every cycle shape.

3. **A complete `m`-cycle obstruction for all `m`.**  
   Hercher stops at 91. An argument that works for arbitrary `m` would finish Lemma 1.

Until one of those three exists, Lemma 1 stays open.

---

## What would discharge Lemma 2

Any one of these, with no gap:

1. **A Lyapunov function on all of `\u2124>0`.**  
   A function `V` with `V(C_+(n)) < V(n)` outside a finite set (or outside `Pred(1)`). Then no injective unbounded ray.

2. **Upgrade Terras / Tao from almost-all to all.**  
   Density one and logarithmic density leave a possible zero-density set of rays. Closing that zero-density set is Lemma 2.

3. **Uniform control of `L/K` versus `log_2 3` along every infinite orbit.**  
   Show that a divergent ray would keep `L/K` too far from `log_2 3` for too long. The model mean `log(3/4)<0` is the outline of this. It is not this.

---

## What would discharge L

Lemma D plus both of the above. Equivalently: a directed path in `G_+` from every vertex to 1. Equivalently: `Pred(1)=ℕ`.

There is no fourth route that skips 1 and 2. A spanning-tree construction is L under another name. A 2-adic connectedness theorem lives on `ℤ_2`, not on `ℕ`. Conway-style undecidability for generalized maps is a warning that some nearby graphs are not decidable; it does not decide this one.

---

## What is not a next discharge

- Raising the Barina prefix
- Another restatement of D, R, and the implication
- Another inverse-tree drawing
- Model drift without a uniform error bound
- Graph axioms that do not see the coefficient 3

The only next deposit that would be new mathematics is an attack on the Steiner identity or a Lyapunov argument, with every inequality written out.

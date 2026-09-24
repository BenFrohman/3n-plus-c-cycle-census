# Lemma 2 (open)

Author: Benjamin Stanley Frohman (frohmanbenjamin@gmail.com)
Repository: https://github.com/BenFrohman/3n-plus-c-cycle-census

**Lemma 2.** \(\Delta_{\mathrm{div}}=\emptyset\).

That is: no positive orbit of \(C_+\) is infinite, injective, and unbounded.

---

## Toward it, not a proof

- Terras (1976): a density-one set of starts has finite stopping time. Almost all, not all.
- Tao (2019): almost all orbits (logarithmic density) become smaller than any prescribed unbounded \(f(n)\). Almost all, not all; almost bounded, not reaches 1.
- Theorem 6: under the geometric model, \(\mathbb{E}[\log M_3]=\log(3/4)<0\). Model, not orbits.
- Barina: no divergent orbit starts below \(2^{71}\). Prefix, not \(\mathbb{N}\).

---

## If nonempty

\(\Delta_{\mathrm{div}}\) would be infinite (the ray plus its inverse tree), forward- and backward-invariant, disjoint from \(\operatorname{Pred}(1)\) and from \(\Delta_{\mathrm{cyc}}\), and would lie entirely above \(2^{71}\).

The sibling \(C_5\) is the map on which \(\Delta_{\mathrm{div}}\) *looks* nonempty (7, 9, 11, 588, \ldots still growing after 20,000 steps). That is a different coefficient. Escape of those starts is not a proved divergence, and it is not a fact about \(C_+\).

---

## What would discharge it

See DISCHARGE.md: a global Lyapunov function; Terras/Tao made pointwise; or a uniform Diophantine control on \(L/K\) along an infinite orbit.

Lemma 2 remains open. Together with Lemma 1 it is Lemma L.

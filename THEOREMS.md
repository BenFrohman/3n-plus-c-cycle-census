# Official theorems

Author: Benjamin Stanley Frohman (frohmanbenjamin@gmail.com)
Repository: https://github.com/BenFrohman/3n-plus-c-cycle-census

These are the statements that are actually theorems. Collatz is not among them.

## Definition

For an odd integer \(c\),

$$
C_c(n)=
\begin{cases}
n/2 & n\text{ even},\\
3n+c & n\text{ odd}.
\end{cases}
$$

Write \(C_+\) for \(C_{+1}\) and \(C_-\) for \(C_{-1}\). For an odd integer \(a\), the compressed (Syracuse) step on odd \(n\) is

$$
S_a(n)=\frac{an+1}{2^{v_2(an+1)}}.
$$

---

## Theorem 1 (instance)

$$
C_+^{1348}(989\,345\,275\,647)=1,
$$

with peak \(1\,219\,624\,271\,099\,764\). The SHA-256 of the trajectory, one decimal integer per line and no trailing newline after \(1\), is

`f406d4f31af4402276e39a48d0d68e4e587ca0a318913a0b196d5da68332ed87`.

*Proof.* Direct iteration in exact integers.

---

## Theorem 2 (conjugacy)

For every odd integer \(c\) and every \(n\in\mathbb{Z}\),

$$
C_{-c}(n)=-C_c(-n).
$$

*Proof.* If \(n\) is even, both sides equal \(n/2\). If \(n\) is odd,

$$
C_{-c}(n)=3n-c,\qquad -C_c(-n)=-(3(-n)+c)=3n-c.
$$

---

## Theorem 3 (three positive sinks for the minus cell)

\(C_-\) has at least three distinct positive cycles:

1. \(1\to 2\to 1\)
2. \(5\to 14\to 7\to 20\to 10\to 5\)
3. \(17\to 50\to 25\to 74\to 37\to 110\to 55\to 164\to 82\to 41\to 122\to 61\to 182\to 91\to 272\to 136\to 68\to 34\to 17\)

These three sets of terms are pairwise disjoint.

*Proof.* Apply \(C_-\) to each term; the next term of the list is obtained, and the last term returns to the first. Pairwise disjointness is inspection of the three finite sets.

---

## Corollary 4 (the shape does not force a unique sink)

It is false that every map of the form "halve if even, \(3n+\) an odd constant if odd" has a unique positive cycle. The map \(C_-\) is of that shape and has at least the three cycles of Theorem 3.

*Proof.* Immediate from Theorem 3.

---

## Theorem 5 (the inverse tree of 1 is infinite)

Let \(\operatorname{Pred}(1)\) be the set of all positive integers \(n\) for which some \(k\ge 0\) has \(C_+^k(n)=1\). Then \(\operatorname{Pred}(1)\) is infinite.

*Proof.* For every \(m\ge 1\), \(C_+(2m)=m\). Iterating from \(1\) gives

$$
C_+^k(2^k)=1\qquad(k=0,1,2,\ldots).
$$

So \(\{2^k:k\ge 0\}\subset\operatorname{Pred}(1)\). That set is infinite.

The other preimage is optional. If \(m\equiv 4\pmod{6}\), then \(k=(m-1)/3\) is a positive odd integer and \(C_+(k)=m\). That is how \(5\) appears:

$$
1\leftarrow 2\leftarrow 4\leftarrow 8\leftarrow 16\leftarrow 5.
$$

Those side branches still only produce numbers that already flow to \(1\).

**What Theorem 5 does not say.** Infinite is not exhaustive. Collatz is the claim \(\operatorname{Pred}(1)=\mathbb{N}\), which is open.

---

## Theorem 6 (model drift; not a theorem about orbits)

Let \(a\ge 3\) be an odd integer. On the probability space where a random valuation \(V\) satisfies

$$
\mathbb{P}(V=k)=2^{-k}\qquad(k=1,2,3,\ldots),
$$

define the model multiplier \(M_a = a\cdot 2^{-V}\). Then

$$
\mathbb{E}[\log M_a]=\log a-2\log 2=\log(a/4).
$$

In particular

$$
\mathbb{E}[\log M_3]=\log(3/4)<0,\qquad\mathbb{E}[\log M_5]=\log(5/4)>0.
$$

*Proof.* \(\mathbb{E}[V]=\sum_{k\ge 1}k\,2^{-k}=2\), so \(\mathbb{E}[\log M_a]=\log a-(\log 2)\mathbb{E}[V]=\log a-2\log 2\).

**What Theorem 6 does not say.** This is a statement about a geometric model of \(v_2(an+1)\), the same model used by Lagarias–Weiss and Kontorovich–Lagarias. It is not a theorem that every orbit of \(C_+\) falls, and it is not a theorem that the orbit of \(7\) under \(5n+1\) diverges.

---

## Not a theorem

That \(C_+\) itself has a unique positive sink — equivalently, that every positive integer reaches \(4\to 2\to 1\) — is the Collatz conjecture. Theorems 1–6 do not prove it, do not disprove it, and do not transfer uniqueness from one cell to the other.

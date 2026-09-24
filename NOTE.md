# A prefix census of 3n+c and 5n+1 cycles, with one verified Collatz instance

**Not a proof of the Collatz conjecture.**

Benjamin Stanley Frohman  
frohmanbenjamin@gmail.com  
ORCID 0009-0006-7068-3718  
https://github.com/BenFrohman/3n-plus-c-cycle-census  
24 September 2026

## 1. The problem

Let C_+(n) = n/2 if n even, else 3n+1.

The Collatz conjecture is: for every integer n > 0 there exists k with C_+^k(n) = 1.

That universal claim remains open (Terras 1976; Lagarias 1985, 2010; Tao 2022; Barina 2025). A single falling orbit is a proof of that orbit. It is not a proof of forall n, and it is not a disproof.

## 2. What is proved here

**Theorem 1 (instance).** Let n = 989345275647. Then C_+^{1348}(n) = 1, with peak 1219624271099764. Both n and the peak lie below 2^{53}-1.

Proof: direct iteration. SHA-256 of the 1349-term trajectory, one decimal integer per line:

f406d4f31af4402276e39a48d0d68e4e587ca0a318913a0b196d5da68332ed87

This n is the smallest integer of maximal total stopping time below 10^{12}. It is the longest complete orbit the companion 3n+1 machine can draw under JavaScript safe-integer limits.

**Theorem 2 (conjugacy).** For every odd integer c and every integer n,
C_{-c}(n) = -C_c(-n).

Proof: if n is even both sides equal n/2. If n is odd, C_{-c}(n) = 3n-c and -C_c(-n) = -(3(-n)+c) = 3n-c.

Corollary: the three known positive cycles of 3n-1 are the three known negative cycles of 3n+1 with every sign flipped. Written in full:

- 1 → 2 → 1
- 5 → 14 → 7 → 20 → 10 → 5
- 17 → 50 → 25 → 74 → 37 → 110 → 55 → 164 → 82 → 41 → 122 → 61 → 182 → 91 → 272 → 136 → 68 → 34 → 17

These are cycles of C_-, not of C_+. They do not lie in Δ_cyc(C_+). They are not renamed here.

## 3. Impact, stated without inflation

- Collatz is one cell of a family. Replacing +1 by an odd c changes the cycle portrait. Lagarias (1990) stated primitive-cycle existence and finiteness conjectures for T_d. Both remain open in general.
- Belaga and Mignotte (2000, 2006) tabulated 42,765 primitive cycles on 6,667 systems d <= 19,999. Primitive cycles for d != 1 are common. The rare object is a second positive cycle of d = +1.
- The sign of the Syracuse drift log(a/4) predicts the qualitative picture: a = 3 falls (heuristic), a = 5 grows (heuristic). A proof technique that cannot see that difference is too coarse to settle Collatz. That is a constraint on arguments, not a solution.
- Frohman observation. Call μ_F = log(3/4) the Frohman model mean (Tao: non-rigorous heuristic for C_+). On C_- the same large-n average is still log(3/4), and two extra cycles already exist. So μ_F < 0 does not mean one attractor. Odd-to-odd log-sum 0 on a cycle is the definition of a cycle, not a contradiction. Comparison orbit at 27: C_+ goes 27 → 82 → 41; C_- goes 27 → 80 → 40 → 20 → 10 → 5 into the 5-cycle. That start is classical. It is not a new periodic orbit.
- On starts 1..1000 under C_-, basins are 349 / 306 / 345 into the three known cycles. A basin count is not the C_- analogue of Collatz.
- Barina (2025) checked every n < 2^{71} under 3n+1. The present prefix N <= 10,000 is a readable toy of that check, written out in CATALOG.md.

## 4. Census rule

Map: C_c(n) = n/2 if even, else 3n+c.
Unique cycle: rotate so the term of least absolute value is first.
Search: starts 1..N. Cycles that never enter [1,N] are invisible.
Primitive: gcd of the terms is 1.

## 5-8. Catalog and 5n+1 unresolved counts

See CATALOG.md and docs/C_MINUS_CYCLES.md for every sequence. Summary:

- 3n+1: one cycle (1,4,2) at every bound through 10,000.
- 3n-1: three cycles after N >= 17, written above. Basins at N=1000: 349 / 306 / 345.
- 3n+5 at N=10,000: six cycles, zero unresolved. Odd cores (1); (5) scaled; (19,31,49); (23,37,29); two length-44 primitives first seen at 123 (min 187) and 171 (min 347).
- 5n+1: three cycles at N=100,200,500. Unresolved 60, then 139, then 389. Odd cores (1,3), (13,33,83), (17,43,27). Escape is not proved divergence.

## 9. Literature

Terras 1976; Lagarias 1985/1990/2010; Steiner 1977; Eliahou 1993; Belaga-Mignotte 1998/2000/2006; Holden 2011; Chamberland survey; Tao 2020 notes and 2019/2022; Barina 2025; Matthews-Watts; Crandall 1978; Metzger 1999; Conway 1972; Roosendaal; OEIS A006877, A006577, A003079, A003124.

## 10. What is not proved

The Collatz conjecture is open. The 3n-1 conjecture (every positive orbit of C_- reaches one of the three cycles above) is open. Divergence of any single 5n+1 orbit is open. This note is a verified catalog and a literature map. No cycle in this note is a newly discovered Frohman cycle.

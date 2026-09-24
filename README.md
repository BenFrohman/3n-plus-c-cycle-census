# 3n+c cycle census

**Not a proof of the Collatz conjecture.**

Author: Benjamin Stanley Frohman  
Email: frohmanbenjamin@gmail.com  
ORCID: [0009-0006-7068-3718](https://orcid.org/0009-0006-7068-3718)  
X: [@Investor0x](https://x.com/Investor0x)

This repository is a signed computational survey of the maps

```
C_c(n) = n/2 if n is even, else 3n+c
C_5(n) = n/2 if n is even, else 5n+1
```

together with one verified Collatz instance

```
T^{1348}(989345275647) = 1
peak = 1219624271099764
```

## What this work actually claims

1. **Instance theorem.** The delay-record start `989345275647` reaches 1 under ordinary Collatz in exactly 1348 hailstone steps. SHA-256 of the trajectory (one decimal integer per line) is `f406d4f31af4402276e39a48d0d68e4e587ca0a318913a0b196d5da68332ed87`.
2. **Conjugacy lemma.** `C_{-c}(n) = -C_c(-n)` for every integer n. In particular 3n-1 on the positives is 3n+1 on the negatives.
3. **Prefix census.** Every cycle listed in `CATALOG.md` was found by iterating starts in a stated bound. A search of 1..N cannot see a cycle that never intersects [1,N].
4. **Literature alignment.** The 3n-1 trio, the 5n+1 trio, and the six 3n+5 cycles (including the two length-44 primitives) match the classical / Belaga-Mignotte / Holden portrait. This is an independent recomputation, not a priority claim over those tables.

## What this work does not claim

- It does not prove that every positive integer reaches 1 under 3n+1.
- It does not disprove that claim.
- Extra cycles of 3n-1, 3n+5, or 5n+1 are facts about those maps. They are not counterexamples to Collatz.
- Primitive cycles for `c ≠ +1` are **not rare**. Belaga and Mignotte tabulated 42,765 primitive cycles across 6,667 values of d ≤ 19,999 coprime to 6. What is rare is a second *positive* cycle of `c = +1`.

## Files

- [`NOTE.md`](NOTE.md) — technical note (Zenodo-ready text; deposit it yourself).
- [`CATALOG.md`](CATALOG.md) — every unique cycle from the prefix search, written in full.
- [`verify.py`](verify.py) — recomputes the instance and the small catalog.
- [`CITATION.cff`](CITATION.cff)

Companion machine (separate license): [the-3n-plus-1-machine](https://github.com/BenFrohman/the-3n-plus-1-machine).

## Deposit

This text is ready to upload to Zenodo as a *technical note / data set*. Do not deposit it as a solution of the Collatz conjecture.

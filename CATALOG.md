# 3n+c family (odd c, positives)

Search of starts 1..N. Cycles above N are invisible. Not a proof of Collatz.

## Count table

| c | N=100 | 200 | 500 | 1000 | 10000 | portrait |
|---|---|---|---|---|---|---|
| +1 | 1 | 1 | 1 | 1 | 1 | only 1-4-2 |
| -1 | 3 | 3 | 3 | 3 | 3 | 1-cycle, 5-cycle, 17-cycle |
| +5 | 4 | 6 | 6 | 6 | 6 | two L=8, two L=44, plus 5x Collatz |
| -5 | 3 | 3 | 3 | 3 | 3 | 5x the three C_- cycles |
| +7 | 2 | 2 | 2 | 2 | 2 | (5,11) and 7x Collatz |
| -7 | 2 | 3 | 3 | 3 | 3 | 7x the three C_- cycles |
| +11 | 3 | 3 | 3 | 3 | 3 | (1,7), L=22, 11x Collatz |
| +13 | 4 | 8 | 10 | 10 | 10 | several L=13 + L=39 |
| +17 | 3 | 3 | 3 | 3 | 3 | (1,5), L=49, 17x Collatz |
| -23 | 1 | 2 | 3 | 3 | 11 | eight cycles only appear at N=10000 |

## Sequences already printed in prior replies

3n+1: 1-4-2-1
3n-1: 1-2-1 ; 5-14-7-20-10-5 ; 17-50-25-74-37-110-55-164-82-41-122-61-182-91-272-136-68-34-17
3n+5 L=44 first seen 123 and 171 (mins 187 and 347)
5n+1: 1-6-3-16-8-4-2-1 ; 13-66-33-166-83-416-208-104-52-26-13 ; 17-86-43-216-108-54-27-136-68-34-17

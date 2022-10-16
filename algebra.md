# Algebra

**方程就是有未知量的等式**。

A *universal algebra* is consisted of

* a carrier set A
* some operations mapping from A^n to A
* some equations about operations

A *free algebra* F(V) can be constructed from a universal algebra A and a variable set V.

1. if v is in V, then v is in F(V);
2. if n-ary operation op is in A, then [op; a1, ..., an] is in F(V), in which ai is in F(V).
3. repeat 1 and 2 until F(V) does not change, then pick equivalence classes based on equations in A.


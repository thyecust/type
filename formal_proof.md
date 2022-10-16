# Formal Proof

Formal proofs

1. represent arbitrary mathmematical concepts and proofs on a computer, and
2. enable a machine verification of the well-formedness of definitions and of the correctness of proofs.

Whitehead and Russell found a consistent foundation of mathematics in 1910.
Church published a typed lambda calculus based on a variant of Whitehead & Russell's system in 1940.
N.G. de Bruijn introduced dependent types to extend this system in 1970.

## Proof Assistants

| Proof Assistant |               Type Theory            |
| --------------  | ------------------------------------ |
| Isabelle        | LCF approach [2], [4]                |
| HOL4            | LCF approach [2], [3]                |
| Coq             | Calculus of inductive constructions [1]  |
| Nuprl           | Martin-Lof’s type theory             |
| Agda            | Martin-Lof’s type theory             |
| Lean            | Dependant type theory [5]            |

## Refs

1. Bertot & Casteran, 2004
2. Milner, 1972
3. Gordon, 2000
4. Nipkow et al., 2002
5. [Lean的前世今生](https://zhuanlan.zhihu.com/p/183902909)

## Related

[Lambda Cube](./lambda_cube.md)

## Note

1. There are many proof assistants (formal proof systems) not based on type theory. E.g. Mizar, Metamath. Read [不基于类型论的proof assistant还有发展空间吗？- mcwu](https://www.zhihu.com/question/414388834/answer/1412579377) for more.

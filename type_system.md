# Type System

Type systems are the most popular and best established lightweight formal methods.
Formal methods help eusure a system behaves correctly with respect to some specification of its desired behavior. [1]

> - heavyweight formal methods: Hoare Logic, algebraic specification languages, modal logics, denotational semantics.
> - lightweight formal methods: model checkers, runtime monitoring, type systems.

A type system can be regarded as calculating a kind of static approximation to the runtime behaviors of the terms in a program. [1]

## Sound, complete, consistent

alse known as soundness, completeness and termination.

Sound: well-typed terms do not go wrong. Also known as safety.

Complete: good terms are well-typed. Usually not true.

Consistent: term is either well-typed or bad-typed. Or, type-checking must terminate. Usually not true.

## Refs

1. TAPL 1.1

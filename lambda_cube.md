# Lambda Cube

![lambda cube](https://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Lambda_Cube_img.svg/253px-Lambda_Cube_img.svg.png)

- x-axis (lambda-P): types that can bind terms, corresponding to dependent types.
- y-axis (lambda-2): terms that can bind types, corresponding to polymorphism.
- z-axis (lambda-omega): types that can bind types, corresponding to (binding) type operators.

## Untyped lambda calculus

Syntax:

```
t := x
    | λx.t
    | t t

v := λx.t
```

Evaluation:

```
E-App1         t1 → t1'
              ---------
            t1 t2 → t1' t2

E-App2         t2 → t2'
              ---------
            v1 t2 → v1 t2'

E-AppAbs     (λx.t2) v2 → [x↦v2]t2
```

## Pure simply typed lambda calculus

Based on untyped lambda calculus.

Syntax:

```
t := x
    | λx:T.t
    | t t

v := λx:T.t

T := T → T

Γ := ∅
   | Γ, x:T
```

Evaluation:

```
E-App1         t1 → t1'
              ---------
            t1 t2 → t1' t2

E-App2         t2 → t2'
              ---------
            v1 t2 → v1 t2'

E-AppAbs     (λx:T11.t12) v2 → [x↦v2]t12
```

Typing:

```
T-Var           x:T ∈ Γ
               ----------
                Γ ⊦ x:T

T-Abs           Γ, x:T1 ⊦ t2:T2
               -----------------
                Γ ⊦ (λx:T1.t2): T1 → T2

T-App           Γ ⊦ t1:T1 → T2  Γ ⊦ t2:T1
               ---------------------------
                Γ ⊦ t1 t2 : T2
```

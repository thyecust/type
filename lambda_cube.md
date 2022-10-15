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

## System F, or lambda-2

Based on pure simply typed lambda-calculus.

Also known as polymorphic lambda-calculus.

Syntax:

```
t := x
    | λx:T.t
    | t t
    | λX.t
    | t [T]

v := λx:T.t
    | λX.t

T := X
    | T → T
    | ∀X.T

Γ := ∅
    | Γ, x:T
    | Γ, X
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

E-TApp       t1 → t1'
            -------------------
             t1 [T2] → t1' [T2]

E-TAppTAbs   (λX.t12) [T2] → [X↦T2] t12
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

T-TAbs          Γ, X ⊦ t2:T2
               -------------------
                Γ, λX.t2 ⊦ ∀X.T2

T-TApp          Γ ⊦ t1:∀X.T12
               -------------------
                Γ, t1 [T2] ⊦ [X↦T2] T12
```

## Type operators, or lambda-omega

Based on pure simply typed lambda calculus.

TAPL 29.

Syntax: TBD.

Evaluation: TBD.

Kinding: TBD.

Type equivalence: TBD.

Typing: TBD.

## Dependent type, or lambda-P

TAPL 30.5.


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

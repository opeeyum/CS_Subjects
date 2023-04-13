# Boolean Algebra

## Basic Laws
  1. 0 + 0 = 0
  2. 0 + 1 = 1
  3. 1 + 0 = 1
  4. 1 + 1 = 1
  5. 0 . 0 = 0
  6. 0 . 1 = 0
  7. 1 . 0 = 0
  8. 1 . 1 = 1
  9. $\overline 0$ = 1
  10. $\overline 1$ = 0

## AND Laws
  1. A . 0 = 0
  2. A . 1 = A
  3. A . A = A
  4. A . $\overline A$ = 0
## OR Laws
  1. A + 0 = A
  2. A + 1 = 1
  3. A + A = A
  4. A + $\overline A$ = 1

## NOT Laws
  1. If, A = 0, then $\overline A$ = 1
  2. If, A = 1, then $\overline A$ = 0
  1. $\overline{\overline A} = A$

## Commutative Law
  1. A + B = B + A
  2. A . B = B . A
  > All logic gates obey Commutative law.

## Associative Law
  1. (A + B) + C = A + (B + C)
  2. (A . B) . C = A . (B . C)
  3. (A ⊕ B) ⊕ C = A ⊕ (B ⊕ C)
  4. (A ⊙ B) ⊙ C = A ⊙ (B ⊙ C)
  > NAND and NOR does not obey Associative law.

## Distributive Law
  1. A (B + C) = AB + AC
  2. A + BC = (A + B)(A + C)

## Asorbtion Law
  1. A + AB = A
  2. A(A + B) = A
```
```
Question:

Minimize, $f = \overline AB + BC + AC$

Answer, $f = \overline AB + AC$

Solution,  

1. $f = \overline AB + 1 . BC + AC$
1. $f = \overline AB + (A + \overline A) . BC + AC$
1. $f = \overline AB + ABC + \overline ABC + AC$
1. $f = \overline AB + \overline ABC + ABC + AC$
1. $f = \overline AB (1 + C) + AC(1 + B)$
1. $f = \overline AB + AC$
```
```
## Consensus Theorem
  ![](/Images/consensus_theorem.jpg)

## Principle of Duality
- ### Steps to find dual of a function
  1. '.' <-> '+'
  2. '0' <-> '1'
  > Precaution:- Do not complement a variable.

  #### Example: 
  1. $f = A + BC$, finds its dual?
     - $f = A + B . C$
     - $f^D = A . B + C$
  2. $f = AB + CDE$
     - $f = A.B+C.D.E$
     - $f^D = (A+B).(C+D+E)$  

- ### Duality
  - If we have a valid boolean equation and if we apply dual on both the side then its dual equation will also be valid.
  - For eaxmple, 
    1. $A + BC = (A+B)(A+C)$
       - Applying dual both side
       - $A.(B+C) = (A.B) + (A.C)$
    2. $1 + \overline A = 1$
       - Applying dual both side
       - $0 . \overline A = 0$
- ### De-Morgans Theorem
1. $\overline{A.B} = \overline A + \overline B$
1. $\overline{A+B} = \overline A . \overline B$
- Applicable for any numeber of input variable.

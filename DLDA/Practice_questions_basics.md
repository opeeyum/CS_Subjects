Question: Design the following functions using minimum number of 2 input NAND gate.

1. f = $\overline A$
2. f = A . B
3. f = A + B
4. f = A . B + C . D
5. f = A + B . C
6. f = A + $\overline B$ . C
7. f = A . B + C . D + E . F
8. f = A . B + B . C + C . D + D . A 

Answers:

1. 1
2. 2
3. 3
4. 3
5. 3
6. 4
7. 6
8. 6

> First reduce the expression then design it with logic gates.
```
```
Question: Desing the following functions using minimum number of  input NOR gate.

1. f = $\overline A$
2. f = A . B
3. f = A + B
4. f = (A + B) . (C + D)
5. f = A . (B + C)
6. f = A . D + B . E + C . D + B . D + A . E + C . E
7. f = (A + B) . (C + D) . (E + F)
8. f = A . B + B . C + C . D + D . A 

Answers:

1. 1
2. 2
3. 3
4. 3
5. 3
6. 5
7. 6
```
```
Questions: [Gate 2009]

What is the mnimum number of gates required to implement the boolean function (AB + C), if we have to use only 2 input NOR gates?

Answer:

3

Solution: 
A . B + C = (A + C) . (B + C) 

```
```
Question: [Gate 1999]

Which of the following expression is not equivalent to $\overline X $?
1. $X$ NAND $X$
2. $X$ NOR $X$
3. $X$ NAND 1
4. $X$ NOR 1

Answer:

1, 2, 3

Solution:

1. $X$ NAND $X$ = $ \overline{X . X}$ = $\overline X$
2. $X$ NOR $X$ = $\overline {X + X}$ = $\overline X$
3. $X$ NAND 1 = $\overline {X . 1}$ = $\overline X$
4. $X$ NOR 1 = $\overline {X + 1}$ = $0$

```
```
Questions:
1. $A$ ⊕ $1$ = $\overline A$
2. $A$ ⊕ $0$ = $A$
3. $A$ ⊕ $A$ = $0$
4. $A$ ⊕ $\overline A $ = $1$

Solutions:
1.  $A$ ⊕ $1$ = $\overline{A}\ .\ 1$ + $A\ .\ \overline 1 $ = $\overline A$
2. $A$ ⊕ $0$ = $\overline{A}\ .\ 0$ + $A\ .\ \overline 0 $ = $A$
3. $A$ ⊕ $A$ = $\overline{A}\ .\ A$ + $A\ .\ \overline A $ = $0$
4. $A$ ⊕ $\overline A $ = $\overline{A}\ .\ \overline A$ + $A\ .\ A $ = $1$
```
```
Question:

If A ⊕ B = C, then solve A ⊕ C = ?

Answer:

B

Solution:

=> A ⊕ C = A ⊕ A ⊕ B; (A ⊕ B = C, given)

=> A ⊕ C = 0 ⊕ B;  (A ⊕ A = 0, following ineqality property)

=> A ⊕ C = B

Questions: [Gate 2014]

(1 ⊕ P) ⊕ (P ⊕ Q) ⊕ (P ⊕ Q) ⊕ (Q ⊕ 0)
1. $P + Q$
2. $\overline {P + Q}$
3. $P⊕Q$
4. $\overline{P⊕Q}$

Answer:

4

Solution:

=> $1 ⊕ P = \overline P$

=> $Q ⊕ 0 = Q$

=> let, $P ⊕ Q$ be $X$

=> then, $X ⊕ X = 0$ (as, XOR gate is inequality detector)

=> Now putting values in given equation

=> $\overline P ⊕ 0 ⊕ Q$

=> $\overline P ⊕ Q$

=> $P\ .\ Q\ +\ \overline{P\ .\ Q}$

=> $\overline{P ⊕Q}$
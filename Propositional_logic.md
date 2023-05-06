# 1. What is a Proposition?
Any declarative statement that is either true or false, but not both is termed as proposition.

[] Moon is made of cheese.

There are two laws regarding proposition as follows:
- ### Law of excluded middle
This law states that a proposition is required to be either true or false but not both.

- ### Law of contradiction
```
True = not False
False = not True
```

## 2. Types of proposition:

#### - Atomic Proposition
Any proposition which cannot be further divded is termed as atomic proposition.

#### - Compund Proposition
One or more atomic proposition combined to form a compound proposition using **connectors/operators** (i.e ~, ^, v, ->, <->).

**Note**:- `Both atomic and compund Proposition's are generally termed as Premises`.

## 3. What is Argument?
Collection of Premises on the basis of which we derive a conclusion is termed as Argument.

![](/Images/argurement_discrete.png)

## 3. Connectors / Operators

### a. Negation (~)
>It is a NOT of digital electronics.

![](Images/negation_discrete.png)

### b. Disjunction (v)
>It is a OR of digital electronics.

![](/Images/disjuction_discrete.png)

### c. Conjunction (^)
>It is AND of Digital Electronics

![](/Images/conjuction_discrete.png)

### d. Implication (->)
>It is also an binary operator. P -> Q, is read as **If P then Q**.

With truth table as follows:

![](/Images/implication_discrete.png)

P -> Q = ~p v Q ``If P then Q is equal to Not P OR Q``

### e. Bidirectional operator (<->)
- If sigifies if and only if (i.e iff)
- Work as Ex-NOR of digital electronics

## 5. Converse, Inverse & Contrapositive
![](/Images/cic_discrete.png)
![](/Images/cic_2_discrete.png)

## 6. Types of Propositions WRT their logical structure
#### - Tautology
A propositional function which is true in every possible case. A tautology is also termed as Valid statement.

#### - Contradiction
A propositional function which is false in every possible case.

#### - Contingency
A propositional function which is some time true and sometime false.

## 7. Satisfiability
A statement or a propsoition is said to be satisfiable if its truth table has **atleast one true value**, otherwise statement is unsatisfiable.

`Clearly, Tautology and Contingency are satisfiable whereas Contradiction is unsatisfiable.`

## 8. Precedence of Operators
![](/Images/precedence.jpg)

## 9. Quantifiers
First we have to understand the concept of **Predicates**. One of the downside of propositonal-logic is that we cannot restrict the domain of the subject, predicate's help us to do so.

**Predicate are wriitten as P(x)**, where P is the logic and x is the subject.

Predicates are used alongside quantifiers to express the extent to which a predicate is true over a range(domain) of elements. 

There are two types of quantifiers:
1. Universal Quantifier
2. Existential Quantifier

### Some Properties of Quantifiers
![](/Images/quantifiers_equivalence.jpg)
![](/Images/qunatifiers_equivalence2.jpg)
![](/Images/quantifiers_negation.jpg)

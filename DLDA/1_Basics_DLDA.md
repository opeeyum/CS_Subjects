# Logic Gates
Logic gates are the most basic building block of any digital system.

1. Basic Gates - AND, OR, NOT
2. Universal Gates - NAND, NOR
3. Special Purpose Gates - XOR & XNOR

## Basic Gates

1. ### AND Gate
   - Logic Symbol: 

     ![](/Images/and_gate_symbol.jpg)
   
   - Truth Table:
      |A|B|C|Y = A.B.C|
      |-|-|-|:-:|
      |0|0|0|0|
      |0|0|1|0|
      |0|1|0|0|
      |0|1|1|0|
      |1|0|0|0|
      |1|0|1|0|
      |1|1|0|0|
      |1|1|1|1|

> What is Truth Table? Truth table is a table which consists of all possible distinct input combination and their coressponding output for a given digital component.

2. ### OR Gate
   - Logic Symbol: 

     ![](/Images/or_gate_symbol.jpg)
   
   - Truth Table:
      |A|B|C|Y = A+B+C|
      |-|-|-|:-:|
      |0|0|0|0|
      |0|0|1|1|
      |0|1|0|1|
      |0|1|1|1|
      |1|0|0|1|
      |1|0|1|1|
      |1|1|0|1|
      |1|1|1|1|

3. ### NOT Gate
   - Logic Symbol: 

     ![](/Images/not_gate_symbol.jpg)
   
   - Truth Table:
      |A|Y = $\overline{A}$|
      |-|:-:|
      |0|1|
      |1|0|

## Universal Gate

1. ### NAND Gate
   - AND gate followed by NOT gate.

   - Logic Symbol: 

     ![](/Images/nand_gate_symbol.jpg)

   - Y = $\overline{A.B.C}$ = $\overline{A}+\overline{B}+\overline{C}$ (De-Morgan's Law)
   
   - Truth Table:
      |A|B|C|Y = ($\overline{A.B.C}$)|
      |-|-|-|:-:|
      |0|0|0|1|
      |0|0|1|1|
      |0|1|0|1|
      |0|1|1|1|
      |1|0|0|1|
      |1|0|1|1|
      |1|1|0|1|
      |1|1|1|0|

> AND, OR and NOT gate are called as basic gate as with their combination we can form a boolean function of any complexity.

- We can design the three basic gates using NAND gate, hence we can design all boolean function of any complexity with NAND gate that is why NAND gate is called universal gate.    

- #### NAND Gate as Universal Gate 
  1. NAND as NOT

     ![](/Images/nand_as_not_gate_symbol.jpg)
  2. NAND as AND

      ![](/Images/nand_as_and_gate_symbol.jpg)
  3. NAND as OR

      ![](/Images/nand_as_or_gate_symbol.jpg)

   

2. ### NOR Gate
   - OR gate followed by NOT gate.
   - Logic Symbol: 

     ![](/Images/nor_gate_symbol.jpg)
   - Y = $\overline{A+B+C}$ = $\overline{A}.\overline{B}.\overline{C}$ (De-Morgan's Law)
   - Truth Table:
      |A|B|C|Y = $\overline{A+B+C}$|
      |-|-|-|:-:|
      |0|0|0|1|
      |0|0|1|0|
      |0|1|0|0|
      |0|1|1|0|
      |1|0|0|0|
      |1|0|1|0|
      |1|1|0|0|
      |1|1|1|0|

   > NOR gate is also a universal gate, that is, all three basic gates AND, OR and NOT can be designed with NOR gate.

- #### NOR gate as Universal Gate
   1. NAND as NOT

      ![](/Images/nor_as_not_gate_symbol.jpg)

   2. NAND as AND
     - $A . B $ = $\overline {\overline {A. B}}$ = $ \overline {\overline A + \overline B}$
      ![](/Images/nor_as_and_gate_symbol.jpg)

   3. NAND as OR
      ![](/Images/nor_as_or_gate_symbol.jpg)

## Special Purpose Gate
1. ### EXOR, XOR (Exclusive OR gate)
   - Logic Symbol:
     ![](/Images/xor_gate_symbol.jpg)

   - Truth Table:
      | $A$ | $B$ | $\overline A$ | $\overline B$ | $\overline{A}B$ | $A\overline{B}$ | $\overline{A}B\ + \ A\overline{B}$ |
      |:-:|:-:|:-:|:-:|:-:|:-:|:-:|
      |0|0|1|1|0|0|0|
      |0|1|1|0|1|0|1|
      |1|0|0|1|0|1|1|
      |1|1|0|0|0|0|0|
   - XOR is called **Inequality Dectector**, as output is 1 for inequal inputs.
   -  E ODD R, ODD 1, we only focus on positive input. XOR gate is odd number of one detector.
   - Output of XOR gate can be swapped with either of the input.
   ![](/Images/xor_property_1.jpg)
   - Number of complemented input will result in number of complement in normal XOR output, that is
     - $\overline P ⊕ Q\ =\ \overline {P⊕Q}$
     - $\overline P ⊕ \overline Q\ =\ \overline{\overline{P⊕Q}}= P⊕Q$
     - $\overline P ⊕ Q ⊕ R = \overline{P⊕Q⊕R}$
     - $\overline P ⊕ \overline Q ⊕ \overline R = \overline{\overline{\overline{P⊕Q⊕R}}} = \overline{P⊕Q⊕R}$ 
2. ### XNOR, EXNOR
   - XOR gate followed by NOT gate.
   - Logic Symbol:

      ![](/Images/xnor_gate_symbol.jpg)

   - Truth Table:
      | A | B | A ⊙ B |
      |:-:|:-:|:-:|
      |0|0|1|
      |0|1|0|
      |1|0|0|
      |1|1|1|
   - Equality detector, as output is 1 from equal inputs.
   - XNOR is **even** 0 (zero) detector if number of input are **even** whereas XNOR is **odd** 0(Zero) detector if number of input are **odd**.
   - $A ⊙ B = \overline {A ⊕ B}$ (Even number of input)
   - $A ⊙ B ⊙ C = A ⊕ B ⊕ C  $ (Odd number of input)
   - $A ⊙ B ⊙ C ⊙ D = \overline {A ⊕ B ⊕ C ⊕ D}$ (Even number of input)
   - $A ⊙ B ⊙ C ⊙ D ⊙ E = A ⊕ B ⊕ C ⊕D⊕ E$ (Odd number of input)
   - Similar to XOR, with XNOR also we can exchange either of input with output.

     ![](/Images/xnor_property_1.jpg)
> For an logic gate if get output as Input then it also termed as buffer gate, all logic gates can acts as buffer gate.

- ### Minimum number of NAND, NOR gates for the following:
   || NAND | NOR |
   |:-:|:-:|:-:|
   |NOT|1|1|
   |AND|2|3|
   |OR|3|2|
   |XOR|4|5|
   |XNOR|5|4|

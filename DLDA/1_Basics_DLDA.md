# Logic Gates
Logic gates are the most basic building block of any digital system.

1. Basic Gates - AND, OR, NOT
2. Universal Gates - NAND, NOR
3. Special Purpose Gates - XOR & XNOR

## Basic Gates

1. ### AND Gate
   Logic Symbol: 

   ![](/Images/and_gate_symbol.jpg)
   
   Truth Table:
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
   Logic Symbol: 

   ![](/Images/or_gate_symbol.jpg)
   
   Truth Table:
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
   Logic Symbol: 

   ![](/Images/not_gate_symbol.jpg)
   
   Truth Table:
   |A|Y = $\overline{A}$|
   |-|:-:|
   |0|1|
   |1|0|

## Universal Gate

1. ### NAND Gate
   AND gate followed by NOT gate.

   Logic Symbol: 

   ![](/Images/nand_gate_symbol.jpg)

   Y = $\overline{A.B.C}$ = $\overline{A}+\overline{B}+\overline{C}$ (De-Morgan's Law)
   
   Truth Table:
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
   OR gate followed by NOT gate.

   Logic Symbol: 

   ![](/Images/nor_gate_symbol.jpg)

   Y = $\overline{A+B+C}$ = $\overline{A}.\overline{B}.\overline{C}$ (De-Morgan's Law)
   
   Truth Table:
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

## rubbish thing

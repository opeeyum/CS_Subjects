1. Question: [GATE 2014]

   Consider two processors P1 and P2 executing the same instruction set. Assume that under identical conditions, for the same input, a program running on P2 takes 25% less time but incurs 20% more CPI (clock cycles per instruction) as compared to program running on P1. If the clock frequency of P1 is 1GHz, then the clock frequency ofP2 (in GHz) is _____ ?

   Answer:

    1.6 Ghz

   Solution:
   |Parameters|P1|P2|
   |----|----|----|
   |no. of instructions|n|n|
   |execution time|t1|t2 = 0.75t1|
   |CPI|C1|C2 = 1.2C1|
   |Frequency (clock rate)| f1 = 1Ghz| f2 = ?|

   We know that, execution time for n instruction = n * CPI<sub>Avg</sub> * cycle time

   => cycle time = $1 \over clock-rate$

   => t1 = $n . C1 \over f1$

   => t2 = $n . C2 \over f2$ = $n*1.2*C1 \over f2$

   => since t2 = .75 x t1

   => $n*1.2*C1 \over f2$ = .75 x $n . C1 \over f1$

   On putting values will get, 1.6 Ghz
```
```
1. Question: [Gate 2005]

   A hardwired CPU uses 10 control signals S1 to S10, in various time steps T1 to T5, to implement 4 instructions I1 to I4 as shown below:

   || T1 | T2 | T3 | T4 | T5 |
   |-|-|-|-|-|-|
   |I1|S1, S2, S5|S2, S4, S6|S1, S7|S10|S3, S8|
   |I2|S1, S2, S5|S8, S9, S10|S5, S6, S7|S6|S10|
   |I3|S1, S2, S5|S7, S8, S10|S2, S6, S9|S10|S1, S3|
   |I4|S1, S2, S5|S2, S6, S7|S5, S10|S6, S9|S10|

   Which of the following pairs of expressions represent the circuit for generating control signals S5 and S10 respectively?
   1. S5 = T1 + I2. T3 and S10 = (I1 + I3) T4 + (I2 + I4) T5
   2. S5 = T1 + (I2 + I4) T3 and S10 = (I1 + I3) T4 + (I2 + I4) T5
   3. S5 = T1 + (I2 + I4) T3 and S10 = (I2 + I3 + I4) T2 + (I1 + I3) T4 + (I2 + I4) T5
   4. S5 = T1 + (I2 + I4) T3 and S10 = (I2 + I3) T2 + I4 . T3 + (I1 + I3) T4 + (I2 + I4) T5

   Answer:

   4.

   Solution:

   Check for all the row-column combination where S5 and S10 are enabled.
```
```
1. Question
   Answer
   Solution
```
```
1. Question
   Answer
   Solution
```
```
1. Question
   Answer
   Solution
```
```
1. Question
   Answer
   Solution
```
```
1. Question
   Answer
   Solution
```
```
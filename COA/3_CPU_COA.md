### CPU
Main component of computer system which performs operations and controls the system.

- **CPU Cycle Time**: Time in which CPU can perform 1 smallest operation i.e micro-operation.

 $$ clock\ Rate = {1 \over CPU\ Cycle\ Time} $$

- **CPI**: Cycle per instruction, Number of cpu cycles required to execute an instruction.

- **Execution Time**: 
  - For 1 instruction = CPI<sub>Avg</sub> x CPU Cycle Time
  - For n instructions = n x CPI<sub>Avg</sub> x CPU Cycle Time

- Consider computing the overall CPI for a machine A for which the following performance measures were recorder when executing a set of benchmark programs. Assume that the clock rate of the CPU is 200 Mhz

  |Instruction Category|Percentage of Occurence|No. of cycles per instruction|
  |-----|:-----:|:------:|
  |ALU|48|1|
  |Load & store|10|3|
  |Branch|39|4|
  |Other|3|5|

  Lets say there are 200 instructions then
  |No. of instruction|CPU Cycles|
  |----|----|
  |96|96|
  |20|60|
  |78|312|
  |6|30|

  Total CPU Cycles: 498

  CPI<sub>Avg</sub> = $498 \over 200$ = 2.49

  In general CPI<sub>Avg</sub> = $\sum_{n=1}^k\  n_i\  CPI_i\over \sum_{n=1}^k\  n_i$

  Where, $n_i$ = no. of instructions of type i.

  $CPI_i$ = CPI for instruction type i

  k = Different type of instructions

## MIPS (Million instructions Per Second)
CPU's performance is given by MIPS.

- Suppose a CPU takes t-seconds. to execute n no. of instructions.
- then, no. of instructions Executed in 1 sec. = $n (no.\ of\ instructions)\over t(total\ execution\ time)$ per sec
- MIPS = $n \over t\ 10^6$
- t (execution time for n instructions) = n * CPI<sub>Avg</sub> * 1 cycle time
- therefore, MIPS = $n \over n\ CPI_Avg\ CycleTime\ 10^6$ = $1 \over CPI_Avg\ CycleTime$
- MIPS may provide false result for comparison of 2 processors, beacuse it doesn't consider complexity of instruction.
- As type of instruction that computer dealt with may of different time complexity.
- To solve this problem we have FLOPS (Floating Point operations Per Second).

## Data Path
- Collection of functional units such as arithmetic logic units or multipliers.
- Perform data processing poerations

## Control Unit
- Control unit generates signals, sends those to components, components work accordingly.
- **Control Variable**: Name of the control signal.
- **Control Word**: collection of all control signals.

## Control Unit Organisation
- Hardwired Control Unit
- Microprogrammed Control Unit

### Harwired Control Unit
- Control Logic is implemented with Gates, flip-flops, decoders and other digital circuits.
- **Advantage**: Can be optimized to product a faster mode of operation.
- **Disadvnatage**: Rearrangeing the wires among various components is diffcult.


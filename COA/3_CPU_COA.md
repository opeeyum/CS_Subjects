### CPU
Main component of computer system which performs operations and controls the system.

- **CPU Cycle Time**: Time in which CPU can perform 1 smallest operation i.e micro-operation.
$$ clock\ Rate = Frequency = {1 \over CPU\ Cycle\ Time} $$

- **CPI**: Cycle per instruction, Number of CPU cycles required to execute an instruction.

- **Execution Time**: 
  - For 1 instruction = CPI<sub>Avg</sub> x CPU Cycle Time
  - For n instructions = n x CPI<sub>Avg</sub> x CPU Cycle Time

- Consider computing the overall CPI for a machine A for which the following performance measures were recorded when executing a set of benchmark programs. Assume that the clock rate of the CPU is 200 Mhz

  |Instruction Category|Percentage of Occurence|No. of cycles per instruction|
  |:-:|:-:|:-:|
  |ALU|48|1|
  |Load & Store|10|3|
  |Branch|39|4|
  |Other|3|5|

  Lets say there are 200 instructions then
  |No. of instruction|CPU Cycles|
  |:-:|:-:|
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
- therefore, MIPS = $n \over n\ CPI_Avg\ CycleTime\ 10^6$ = $1 \over CPI_Avg\ CycleTime\ 10^6$
- MIPS may provide false result for comparison of 2 processors, beacuse it doesn't consider complexity of instruction.
- As type of instruction that computer dealt with may of different time complexity.
- To solve this problem we have FLOPS (Floating Point operations Per Second).

## Data Path
- Collection of functional units such as arithmetic logic units or multipliers used to perform data processing operations.
- Data path diagram (*not a standard diagram)
  
  ![](/Images/data_path_diagram.jpg)
- Instruction Fetch simulation
  - IR <- M[PC], this operation is not fundamental, it will performed in multiple micro-operations.
    1. AR <- PC
    2. IR <- M[AR], PC <- PC + 1
  - In terms of data path
    1. PC OUT signal will be enabled, MUX-1 will set to transfer PC value to ALU, MUX-2 will set to transfer ALU value to Internal Data Bus and IN signal for Address register will be enabled, hence value be loaded to Address register from PC passing ALU and internal data bus.
    2. Now, OUT signal will be enabled for Address register to load Address Register value to Address bus, Memory Read Signal will be enabled to load value of the given address to data bus, MUX-2 will be set to forward Data bus value to Internal data bus, Instruction register IN signal will be enabled to store Internal Data Bus data and finally PC value will incremented.
  - This enable signals for all the components being PC, AR, MUX, and ALU etc is generated by Control Unit.
## Control Unit
- Control unit generates signals, sends those signals to components, and components work accordingly.
- **Control Variable**: Name of the control signal, that is READ, IN, OUT, and WIRTE etc. all are Control variables.
- **Control Word**: Collection of all control signals.
  | IR-IN | IR-OUT | AR-IN | AR-OUT | D1-IN | D1-OUT | D2-IN | D2-OUT | PC-IN | PC-OUT | PC-INC | MUX-1 | MUX-2 | ALU | Memory-READ | Memory-WRITE|
  |:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
  |0|0|1|0|0|0|0|0|0|1|0|1|1|10100|0|0|
  |1|0|0|1|0|0|0|0|0|0|1|0|0|00000|1|0|

- The two rows in the above table represent the control word for, AR <- PC and IR <- M[AR], PC <- PC + 1, respectively.

## Control Unit Organisation
- Hardwired Control Unit
- Microprogrammed Control Unit

### Harwired Control Unit
- Control Logic is implemented with Gates, flip-flops, decoders and other digital circuits.
- **Advantage**: Can be optimized to product a faster mode of operation.
- **Disadvnatage**: Rearranging the wires among various components is diffcult that is, it will be diffcult to update control logic.

![](/Images/hardwired_control_unit.jpg)

- How Control Unit generate control word?
  - Control word will be generated for each cpu cycle.
  - If an instruction takes n-cycles for execution then control unit needs to generate n-control words.
  - Timing of each control word will be decided by the timing generator integrated to control unit. 
  - After each instruction execution timing generator will be reset.
  - A intruction-Timing table is created having control-word for each timing signal for all instruction.
    ||I1|I2|I3|
    |-|-|-|-|
    |T1|...|...|...|
    |T2|...|...|...|
    |T3|...|...|...|

### Micro-Programmed Control unit
- Control logic is implemented with micro-programs.
- In other words, All possible control words are stored in a memory (control memory) and based on the requirements the specific control word is fetched from memory.
- Control memory resides inside CPU.
- For each instruction control words are stored in a sequence.
- **Advantages**: Updating the control logic is easy.
- **Disadvantages**: Slower than hardwired control unit.
- Execution Flow
  ![](/Images/control_word_sequencing.jpg )


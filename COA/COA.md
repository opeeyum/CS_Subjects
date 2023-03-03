# COA: Computer Organisation and Architecture

## Prerequisites
 - Number system
 - DLDA: Digital Logic, Design and Analysis.

## Architecture VS Organisation
 ### Architecture
  - Conceptual design & fundamental oprational structure.
    - What type of components (i.e CPU, RAM, ROM etc.) will be having in a system? 
    - Specifying functionality of each mentioned components.
    - Specifying CPU design i.e Block diagram of CPU, Pin diagram of cpu and working of CPU and most importantly Instructions that a cpu can take, Addressing Modes & Data format.
 ### Organisation
  (Organisation refers to implementation of computer Architecture)
  - Deals with physical devices and their interconnections.
    - I/O organisation
    - Memory organisation
  - With a perpective of the improving the performance.

 <table class = "table table-info table-sm table-bordered align-middle">
    <thead>
      <th>Architecture</th>
      <th>Organisation</th>
    </thead>
    <tbody>
      <tr>
        <td>CPU Design</td>
        <td>I/O organisation</td>
      </tr>
      <tr>
        <td>Instructions</td>
        <td>Memory organisation</td>
      </tr>
      <tr>
        <td>Addressing Modes</td>
        <td>Performance</td>
      </tr>
      <tr>
        <td>Data Format</td>
        <td></td>
      </tr>
    </tbody>
 </table>
 <hr>

 - #### Data Format
    (Representing the data in Binary)

    How the instruction and the data is going to be stored in the system?
    - We can store instruction and data either in **numbers** or second option is **characters**.
    - Numbers can have either **Fixed Point** OR **Floating Point** representation.
    - For characters we two code formats, 
        1. ASCII : Uses 8 bits, 7-bits for character + 1-bit for parity.
        2. EBCDIC (Extended Binary Coded Decimal Interchange Code): 8-bits per characters.
  
  ### Von Neumann's Architecture
   - Also known as **Stored Program Architecture**.
   - Also known as **Princeton Architecture**.
   - Suggests storing Instruction and Data both in a memory unit.

      <img src="../images/core_subjects/von_neumann_architecture.jpg" class="img-fluid mx-auto d-block" alt="" width="400"/>

        #### Bottleneck in Von Neumann Architecture
        - Since components are connected with Single set of Bus, hence CPU can't access Data and Instruction simultaneously.
        - Connecting more bus won't work as Memory can only handle one request at a time.
  ### Havard Architecture
   - Its a advancement to  Von Newmann's Architecture, suggests having two seperate memory unit for instruction and data, so that CPU can fetch instruction and data simultaneously.
   - Its not practically implemented.

```
Question:
 Which of the following is included in the architecture of computer?
 1. Addressing Modes, Design of CPU
 2. Instruction set, Data Format
 3. Secondary Memory, Operating System

Options:
 a) 1 & 2
 b) 2 & 3
 c) 1 & 3
 d) 1, 2, & 3

Answer:
 a.
```

## Components of Computer
 - ### CPU
   CPU consists of:
   - Control Unit (CU)
   - Arithmetic Logical Unit (ALU)

 - ### Memory
   Two types of memory are there
    - Primary Memory / Main Memory
    - Secondary Memory / Auxillary Memory

 - ### I/O Devices
   - Input Devices
   - Output Devices

 - ### Other Components
   - System Buses

     Connection lines between two devices within the Computer System, for comunication. There will muliple lines as one line transfers only one bit.
     
     Types of System Buses:
     - Address Bus: Address bus is **Uni-Directional**, From CPU to Memory/IO devices.
     - Data Bus: Data bus is purely **Bi-Directional**.
     - Control Bus: In Control bus every individual line is **Uni-Directional**.

       Memory generates, **Wait** and **Ready** signals for CPU.
       - Wait: Wait, working on some other instruction.
       - Ready: Ready to take new instruction.
       
       **Memory Cycle Time**: Time from accepting a request till memory gets ready again to perform next operation is known as Memory Cycle Time.

   - CPU Registers

     Small memory(storage) unit within the CPU.

     Types of CPU Registers:
     - General Purpose Registers (GPRs)
     - Special Purpose Registers
      1. **Accumulator** (AC): Used to store result of ALU and sometime to store one of the input of the ALU. 
      2. **Program Counter** (PC): Stores address of next instruction. 
      3. **Instruction Register** (IR): Used to store current instruction which CPU is executing.
      4. **Stack Pointer** (SP): Used to store address of the top element of the stack.
      5. **Flag Register**  / **Program Status Word** (PSW): It stores the status of ALU result. Status is stored to check the conditions.
      > In Some CPU's Status register is considered as PSW while in others combination of Accumulator and Status register is considered as PSW. 
      6. **Address Register** (AR) / **Memory Address Register** (MAR): It is used to send address to memory.
      7. **Data Register** (DR) / **Memory Data Register** (MDR) / **Memory Buffer Register** (MBR): It is used to send data to memory (memory write) & to recieve data from memory (memory read).

     Types of Architecture: Based on Input to ALU
      1. **Accumulator based**: One input of ALU comes from Accumulator, 2nd input can come from all other choices.
      2. **Register based Architecture**: Both the inputs of ALU taken from GPRs, result will be stored to Accumulator.
      3. **Register to Memory Architecture**: One operand(input) of ALU from Register and 2nd from Memory, result in Accumulator.
      4. **Complex-System architecture**: Both inputs can either come from Register or Memory(4 Combination possible), result will get stored in Accumulator.
      5. **Stack based architecture**: Both input comes from Stack based memory.

         > 32-bit and 64-bit in a system specifies the size of a single instruction.
```
Question:
 A CPU has 24-bits instruction. A program starts at address 300 (in decimal). Which of the following is a legal program counter value?

Options:
 a) 400
 b) 500
 c) 600
 d) 700

Answer:
 c.
```

```
Question:
 Consider the following program segment. Here R1 and R2 are the general purpose register. Assume that the content of memory location 2000 is 23. All numbers are in decimal. After the excution of this program the value of memory location 2000 is?

 Instructions         Operations

  MOV R1, #5          R1 <- #5
  MOV R2, (2000)      R2 <- M[2000]
  SUB R2, R1          R2 <- R2 - R1
  MOV (2000), R2      M[2000] <- R2
  HALT                Stop

Answer:
 18
```

```
Info:
 Consider the following program segment. Here R1, R2 and R3 are the general purpose register.

 Instructions         Operations            Instruction Size (in words)

 MOV R1, (3000)      R1 <- M[3000]          2
 LOOP: MOV R2, (R3)  R2 <- M[R3]            1
 ADD R2, R1          R2 <- R2 + R1          1
 MOV (R3), R2        M[R3] <- R2            1
 INC R3              R3 <- R3 + 1           1
 DEC R1              R1 <- R1 - 1           1
 BNZ LOOP            Branch on not Zero     2 
 HALT                Stop                   1

 Assume that the content of memory location 3000 is 10 and the content of the register R3 is 2000. The content of each of the memory locations from 2000 to 2010 is 100. The program is loaded from the memory location 1000. All the numbers are in decimal.

Questions:
 1. Assume that the memory is word addressable. The number of memory references for accessing the data in executing the program completely is: 
 a) 10
 b) 20
 c) 11
 d) 21

 2. Assume that the memory is word addressable. After the execution of this program the content of memory location 2010 is?
 a) 100
 b) 101
 c) 102
 d) 110

 3. Assume that the memory is byte addressable and teh word size is 32-bits. If the interrupt occurs during the execution of the instruction "INC R3", what return address is pushed onto the stack:
 a) 1005
 b) 1024
 c) 1020
 d) 1024

Answers:
1) d.
2) a.
3) c.

```

```
Info:
  In a simplified computer the instructions are:
  OP Ri, Rj  - Performs Rj Op Ri and stores the result in Ri
  OP m, Ri   - Performs val Op Ri and stores the result in Ri
              val denotes the content of memory location m
  MOV m, Ri   - Moves the content of memory location m to register Ri
  MOV Ri, m   - Moves the content of register Ri to memory location m

  The computer has only two registers and OP is either ADD or SUB. Consider the following basic block:

  t1 = a + b
  t2 = c + d
  t3 = e - t2
  t4 = t1 - t3

Question:
  Assume that all operands are initially in memory. The final value of  the computation should be in memory. What is the minimum number of MOV instructions in the code generated for this basic block?

Answer:
  3

Explaination:
  R1 <- a
  R2 <- b
  R1 = R1 + R2, t1
  M[X] <- R1, 1st MOV
  R1 <- c
  R2 <- d
  R1 = R1 + R2, t2
  R2 <- e
  R1 = R2 - R1, t3
  R2 <- M[X], 2nd MOV
  R1 = R2 - R1
  M[X] <- R1, 3rd MOV, Since final result should be in memory.
```
## Instruction
 A group of bits which instructs computer to perform some operation.

 Instruction consists of two parts:
 1. Operation Code (Opcode) -> What operation to perform.
 2. Operands information -> Address of operands, number of address stored can vary in the given instruction depending upon the implementation.

> ISA (Instruction set architecture): Collection of all instruction that a CPU supports.

### Types of Instructions
 Based on operation
 - Data Transfer:      MOV, LDI, LDA
 - Arithmetic & Logic: ADD, SUB, AND, OR
 - Machine Control:    EI, DI, PUSH, POP
 - Iterative:          LOOP, LOOPE, LOOPZ
 - Branch:             JMP, CALL, RET, JZ, JNZ

 Based on Operand Information
  - 4-Address Instruction

    Within each instruction **maximum** 4 address can be specified. 
    
    Computer having 4-Address instruction does not have Program Counter.

    Disadvantages:
     - Larger size Instruction.
     - Larger size program in memory.
     - Instruction fetch takes more time.
     - Relocation in not easy, as reolaction in 4-address type instruction requires to update each instruction because instructions have address of next instruction to be executed within them.
  - 3-Address Instruction

    Within each instruction **maximum** 3 address can be specified.

    Program counter is used to get address of next instruction.
  - 2-Address Instruction

    Within each instruction **maximum** 2 address can be specified.

    Program counter is used to get address of next instruction.

    One operand address in 2-address type instruction is used as SOurce and Destination both.

    Disadvantages:
    - More number of instruction for a program as compared to 3-address instruction format.
    - More memory for a program as number of instruction is larger.
  - 1-Address Instruction

    Within each instruction **maximum** 1 address can be specified.

    Accumulator is used as second operand implicitly, Accumulator based architecture.

    Program counter is used to get address of next instruction.
  - 0-Address Instruction

    Used in stack based architecture.
    
    No address is mentioned in the instructions, only opcode is specified. And, two oprands are implicitly taken from the stack.

## Addressing Mode
### Effective Address
- Address of operand in a computation-type instruction, i.e. ADD, SUB, MOV, AND
- OR, The target address in a branch-type instuctions.

### Instruction Cycle

### Addressing Mode
 - Its is used to specifiy how to access the operand whose address is mentioned in the instruction.

#### Index, Base Register + Displacement Mode

#### Scaled mode

#### PC-Relative Mode
- This Mode is used for branch type instruction.
- Consider following memory representation
  <table>
    <thead>
      <tr>
        <th>Memory Address</th>
        <th>Memory Content</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>...</td>
        <td>...</td>
      </tr>
      <tr>
        <td>500</td>
        <td>Instruction-2</td>
      </tr>
      <tr>
        <td>504</td>
        <td>Instruction-3</td>
      </tr>
      <tr>
        <td>508</td>
        <td>Instruction-4</td>
      </tr>
      <tr>
        <td>512</td>
        <td>Instruction-5</td>
      </tr>
      <tr>
        <td>516</td>
        <td>Instruction-6</td>
      </tr>
      <tr>
        <td>520</td>
        <td>Instruction-7</td>
      </tr>
      <tr>
        <td>524</td>
        <td>Instruction-8</td>
      </tr>
      <tr>
        <td>528</td>
        <td>Instruction-9</td>
      </tr>
      <tr>
        <td>...</td>
        <td>...</td>
      </tr>
    </tbody>
  </table>

  - A Program is stored from memory location 500 to 528.
  - Memory is WOrd addressable and 1 word = 4 Bytes.
  - Now,
  - Assume, CPU is executing Instruction-2, then PC (Program Counter) = 504.
  - In Decode CPU detects the INs-2 is a branch instruction(Conditional branch).
  - At Execution Phase CPU will check for the branch condition; True OR False.
  - If False (Branch Not Taken): **PC value will not get updated** and Next instruction in the sequence will be executed, I-3 in this case.
  - If True (Branch Taken): 
    - Lets say, 
    - I-2 is branching to I-6, 
    - that is, target instrcution is I-6, 
    - hence, target address = 516
    - PC will updated, PC = 504 + 12
  - Therefore, Effective address in PC-Relative mode = PC + addresss field value in instruction.
  - This mode is used for **Intra**-segment jump, that is target instruction is present same set on Instruction as branching Instruction.

#### Base Register Mode

- This mode is used for **Inter**-Segment jumps.
- Different to PC-relative mode, Value of address field from instruction, will be added to value of special purpose register Base-register.
- Hence, effective address = Base Register + Address Field Value.
- If program is relocated, nothing to update in Instruction, just update teh Base register value.

### Classification Of Addressing Modes
  <table>
    <thead>
      <tr>
        <th>Computable Addressing Modes</th>
        <th>Non-Computable Addressing Modes</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>An addressing mode which involves any arithmetic operation to compute effective address is classified as Computable Addressing modes.</td>
        <td>An addressing mode which does not involves any arithmetic operation to compute effective address is classified as Non-Computable Addressing modes.</td>
      </tr>
      <tr>
        <td>Auto Increment Mode</td>
        <td>Implied Mode</td>
      </tr>
      <tr>
        <td>Auto Decrement Mode</td>
        <td>Immediate Mode</td>
      </tr>
      <tr>
        <td>Indexed Mode</td>
        <td>Register Mode</td>
      </tr>
      <tr>
        <td>Index + Base Register Mode</td>
        <td>Register Indirect Mode</td>
      </tr>
      <tr>
        <td>Index + Base  + Displacement Register Mode</td>
        <td>Direct Mode</td>
      </tr>
      <tr>
        <td>Scaled mode</td>
        <td>Indirect Mode</td>
      </tr>
      <tr>
        <td>PC-Relative</td>
        <td></td>
      </tr>
      <tr>
        <td>Base Register</td>
        <td></td>
      </tr>
    </tbody>
  </table>

  > Pc-Relative and Base Register are used for Branch type instruction, some time all termed as Control mode instruction.

  > All other modes are used to fetch Operand.
1. Question:
    
    An instruction is stored at Location 300 with its address field at location 301. The address field has the value 250. A processor register contains the number 200. Evaluate the effective address, if addressing mode is:

    1. Direct

    2. Immediate

    3. Relative

    4. Register Indirect
    
    Answer:
    
    1. 250

    2. 301

    3. 551

    4. 200

    Solution:
```
```
2. Question:

    A relative branch mode type instruction is stored in memory at address 300. The branch is made to an address 450.

    a) What should be the value of relative address field of the instruction?

    b) Determine the value of PC before instruction fetch, after the fetch and after execution phase?
    
    Answer:
    
    a) 149

    b) Before: 300, After:301, After execution: 450
    
    Solution:
    
    In PC relatice mode target instruction address = PC value + address field from instruction (offset).

    => 450 = 301 + address field

    => address filed = 149
```
```
3. Question:
    
    A relative branch mode type instruction had taken branch to an address 750. The branch instruction is of 4 bytes and it has offset value 400. Then the starting address of the instruction in the memory is?
    
    Answer:
    
    346
    
    Solution:
    
    Target address = 750

    Address size = 4B

    Offset = displacement = 400

    Target Address = PC Value + offset

    => 750 = PC value + 400

    => PC Value = 350 (The address of branch instruction)

    => Starting address = 350 - 4 = 346
```
```
4. Question:
    
    An instruction is stored at Location X with its address field at location X + 1. The address field has the value Y. A processor register contains the number Z. Evaluate the effective address, if addressing mode is:

    1. Direct

    2. Immediate

    3. Relative

    4. Register Indirect
    
    Answer:
    
    Direct: Y

    Immediate: X + 1

    Relative: X + 2 + Y

    Register Indirect: Z
    
    Solution:
```
```
5. Question: [GATE - 15]
    
    For computers based on three-address instruction formats, each address field can be used to specify which of the following:

    S1: A memory operand

    S2: A processor register

    S3: An implied accumulator register

    Options:

    A. Either S1 or S2

    B. Either S2 or S3

    C. Only S2 and S3

    D. All of S1, S2 and S3
    
    Answer:
    
    A
    
    Solution:
    
    Remember, all the special purpose register are directly accesible by the CPU, no need for explict address, and accumulator register is a spcial purpose register.
```
```
6. Question: [GATE - 17]
    
    Consider a RISC machine where each instruction is exactly 4-bytes long. Conditional and unconditional branch instruction use PC-relative addressing mode with offset specified in bytes to the target location of the branch instruction. Further the offset is always with respect to the address of the next instruction in the program sequence. Consider the following instruction sequence.

    |Instr.| No Instruction|
    |----|-------|
    |i:   |     add R2, R3, R4|
    |i+1: |     sub R5, R6, R7|
    |i+2: |     cmp R1, R9, R10|
    |i+3: |     beq R1, offset|

    If the target of the branch instruction is i, then the decimal value of the offset is

    Answer:
    
    -16
    
    Solution:
    
    Target = PC value + offset

    => Assume ith instruction is at x address

    => Since each instruction is 4B long, hence i+3 instruction is at x + 16

    => putting values in the formula

    => x = x + 16 + offset

    => offset = -16

```
```
7. Question:

    Consider a system which supports 2-address, 1-address and 0-address instructions. The system has 'a' bits instructions and supports 2<sup>m</sup> bytes memory. If there are 't' 2-address instructions and 'w' 1-address and 'z' 0-address instructions then which of the following is correct?

    A. 2<sup>a</sup> = 2<sup>m</sup>. t + w + z

    B. 2<sup>a</sup> = 2<sup>2m</sup> . t + 2<sup>m</sup> . w + z

    C. 2<sup>a</sup> = 2<sup>3m</sup> . t + 2<sup>2m</sup> . w + 2<sup>2m</sup> . z

    D. 2<sup>a</sup> = 2<sup>2m</sup> . t + 2<sup>2m</sup> . w - z

    Answer:

    B
    
    Solution:
```
```
8. Question:

    An instruction is stored at location 500 with its address field at location 501. The address field has the value 690. A processor register contains the number 850. Evaluate the effective address, if addressing mode is:

    1. Direct

    2. Immediate

    3. Relative

    4. Register Indirect

    Answer:
    1. 690

    2. 501

    3. 1192, effective address = PC value + Value at current instruction's address field (offset)

    4. 850
    
    Solution:
```
```
9. Question:

    Consider a PC-relative mode typr branch instruction which takes branch on address 740 in memory. The instruction has offset value 160. What is the address of this instruction in  memory, if each instruction is stored in memory on 4 locations?

    A. 900

    B. 904

    C. 580

    D. 576

    Answer:

    D. 576

    Solution:
    Target address = PC-value + offset

    740 = x + 160

    x = 580

    Address of current instruction = 580 - 4 = 576
```
```
10. Question:

    An instruction is stored at location X its address field at location X + 1. The address field has the value Y. A processor register contains the number Z. Evaluate the effective address, if addressing mode is:

    1. Direct

    2. Immediate

    3. Relative

    4. Register Indirect
    
    Answer:

    1. Direct: Y

    2. Immediate: X + 1

    3. Relative: X + 2 + Y

    4. Register indirect: Z
   
    Solution:
```
```
11. Question:
    
    For the very first operand access among the table of the content in _____ addressing mode, the operand accessed in same as regiter indirect mode?

    A. Auto-increment mode

    B. Auto-Decrement mode

    C. Register mode

    D. Indexed Register Mode

    Answer:

    A. Auto-increment mode
    
    Solution:
    D. Indexed Register Mode: To get effective address we add two things value of index register and Value at register. since two values involved hence no.

    C. Register mode: Value stored at register is the operand value, hence no.

    B. Auto-decrement mode is similar to register indirect mode, but first value at register is decremented and then used to fetch operand, hence no.

```
```
12. Question:

    Consider a 6-words instruction, which is of the following type:

    | Opcode | Mode 1 | Mode 2 | Address 1 | Address 2 |

    The first operand (destination) uses register indirect mode and second operand uses indirect mode. Assume each operand is of size 2 words, each address is of 2 words and main memory takes 50ns for 1-word access.

    Total memory access time required in:

    1. Fetch cycle on instruction

    2. Execution cycle of instruction

    3. Instruction cycle of instruction
    
    Answer:

    1. 300 ns

    2. 400ns

    3. 700ns
    
    Solution:

    Fetch cycle includes only instruction fetch, instruction size 6-words, 6 * 50ns = 300ns.

    Execution cycle, it includes instruction decode, effective address calculation, operand fetch and result write back.

    => For address 1, one memory access for 2-words = 2 * 50ns

    => For address 2, two memory access for 2-words = 2 * 2 * 50ns

    => For result write back, since address 1 in destination, one memory access for 2-words = 2 * 50ns

    Total time = 100ns + 200ns + 100ns = 400ns

    Instruction cycle = Fetch cycle + Execution Cycle = 300ns + 400ns = 700ns

```
```
13. Question:
    
    Which of the following addressing mode(s) is/are used for accessing the array element from memory?

    A. Scaled Mode

    B. Indexed Mode

    C. PC-relative Mode

    D. Auto-decrement Mode

    Answer:
    
    A, B & D

    Solution:
```
```
14. Question:
    
    Which of the following can be the value(s) of PC immediately after the fetch of an instruction which is stored on a location 400?

    A. 400

    B. 399

    C. 401

    D. 402

    Answer:
    
    C & D

    Solution:

    Anything more than 400.
```
```
15. Question:
    
    The addressing modes used for source operand in the following instruction are respectively?

    1. R1 <- #5

    2. R1 <- M[5000]

    3. R1 <- M[R2]

    A. Implied, direct, register

    B. Implied, direct, register indirect

    C. Immediate, direct, register indirect

    D. Immediate, direct, register

    Answer:
    
    C.

    Solution:

    Instruction one direct operand value provided.
    
    Instruction two direct memory address provided.
    
    Instruction three register value as memory address.
```
```
16. Question: [MSQ]
    
    Consider the system where in fetch cycle complete instruction is fetched. Which of the following addressing mode do(es) not require memory access for operand after fetch cycle?

    A. Register Mode

    B. Register Indirect Mode

    C. Indirect Mode

    D. Indexed Mode

    Answer:
    
    A

    Solution:
```
```
17. Question: [MSQ]
    
    Consider a PC-relative branch mode type instruction stored in the memory at address 350. The relative address field of instruction constains value 110. Which of the following is/are the possible PC value immediately after execution phase of branch instruction execution?

    A. 350

    B. 351

    C. 460

    D. 461

    Answer:
    
    B & D

    Solution:

    Instruction can be of conditional branch type, hence if condition is true then,

    Target address = PC-value + offset

    => Target address = 350 + 1 + 110 (x is instruction size)

    => Target address = 460 + 1

    But, if condition is false, then Target address = PC-value = 351
```
```
18. Question:
    
    In which of the following addressing modes the location of operand is specified wihtin mnemonic itself?

    A. Immediate Mode

    B. Implied Mode

    C. Direct Mode

    D. Register Mode

    Answer:
    
    B

    Solution:

    Mnemonic means opcode in Assembly, hence, Implied Mode
```
```
19. Question:
    


    Answer:
    

    Solution:
```
```
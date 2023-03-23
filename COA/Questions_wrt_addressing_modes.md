1. Question:
    ```
    An instruction is stored at Location 300 with its address field at location 301. The  address field has the value 250. A processor register contains the number 200. Evaluate the effective address, if addressing mode is:
    1. Direct
    2. Immediate
    3. Relative
    4. Register Indirect
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
1. Question:
    ```
    A relative branch mode type instruction is stored in memory at address 300. The branch is made to an address 450.

    a) What should be the value of relative address field of the instruction?
    b) Determine the value of PC before instruction fetch, after the fetch and after execution phase?
    ```
    Answer:
    ```
    a) 149
    b) Before: 300, After:301, After execution: 450
    ```
    Solution:
    ```
    In PC relatice mode target instruction address = PC value + address field from instruction.
    => 450 = 301 + address field
    => address filed = 149
    ```
1. Question:
    ```
    A relative branch mode type instruction had taken branch to an address 750. The branch instruction is of 4 bytes and it has offset value 400. Then the starting address of the instruction in the memory is?
    ```
    Answer:
    ```
    346
    ```
    Solution:
    ```
    Target address = 750
    Address size = 4B
    Offset = displacement = 400

    Target Address = Pc Value + offset
    => 750 = PC value + 400
    => Pc Value = 350 (This address of next instruction)
    => Starting address = 350 - 4 = 346
    ```
1. Question:
    ```
    An instruction is stored at Location X with its address field at location X + 1. The address field has the value Y. A processor register contains the number Z. Evaluate the effective address, if addressing mode is:
    1. Direct
    2. Immediate
    3. Relative
    4. Register Indirect
    ```
    Answer:
    ```
    Direct: Y
    Immediate: X + 1
    Relative: X + 2 + Y
    Register Indirect: Z
    ```
    Solution:
    ```
    ```
1. Question: [GATE - 15]
    ```
    For computers based on three-address instruction formats, each address field can be used to specify which of the following:
    S1: A memory operand
    S2: A processor register
    S3: An implied accumulator register

    Options:
    A. Either S1 or S2
    B. Either S2 or S3
    C. Only S2 and S3
    D. All of S1, S2 and S3
    ```
    Answer:
    ```
    A
    ```
    Solution:
    ```
    Remember, all the special purpose register are directly accesible by the CPU, no need for explict address, and accumulator register is a spcial purpose register.
    ```
1. Question: [GATE - 17]
    ```
    Consider a RISC machine where each instruction is exactly 4-bytes long. Conditional and unconditional branch instruction use PC-relative addressing mode with offset specified in bytes to the target location of the branch instruction. Further the offset is always with respect to the address of the next instruction in the program sequence. Consider the following instruction sequence.
    Instr. No Instruction
    i:        add R2, R3, R4
    i+1:      sub R5, R6, R7
    i+2:      cmp R1, R9, R10
    i+3:      beq R1, offset

    If the target of the branch instruction is i, then the decimal value of the offset is
    ```
    Answer:
    ```
    -16
    ```
    Solution:
    ```
    Target = PC value + offset
    => Assume ith instruction is at x address
    => Since each instruction is 4B long, hence i+3 instruction is at x + 16
    => putting values in the formula
    => x = x + 16 + offset
    => offset = -16
    ```
1. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
1. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
1. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
1. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
1. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
1. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
1. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
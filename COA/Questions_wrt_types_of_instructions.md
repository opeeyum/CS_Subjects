1. Question:
    ```py
    Consider a digital computer which supports only 2-address instructions each with 16-bits. If address length is 6-bits then maximum and minimum how many instructions the system can support?
    ```
    Answer: 
    ```py
    Maximum = 16, Minimum = 1
    ```
    Explanation:
    ```py
    Instruction size = 16-bits
    Size of each address = 6-bits
    System supports 2-address instruction, therefore, bits of opcode = 16 - 2 * 6 = 4
    Maximun number of instruction 2^4 = 16

    Minimum will always be 1, as opcode is mandatory in eacg type of instruction.
    ```
2. Question:
    ```py
    Consider a digital computer which supports 32 2-address instructions. If address length is 8-bits then the length of the instruction is bits?
    ```
    Answer:
    ```
    21-bits
    ```
3. Question: [Gate 2016]
    ```py
    A processor has 40 distinct instructions and 24 general purpose registers. A 32-bit instruction word has an opcode, two register operands and an immediate operand. The number of bits available for the immediate operand field is ?
    ```
    Answer:
    ```py
    16-bits
    ```
    Solution:
    ```py
    No. of bits for instructions = 6-bits.
    Instruction size = 32-bits
    Since there are 24 registers, address size will be 5-bits
    Bits for immediate operand = 32 - 6 - 2 * 5 = 16-bits.
    ```
4. Question: [Gate 2016]
    ```py
    Consider a processor with 64 registers and an instruction set of size twelve. Each instruction has five distinct fields, namely, opcode, two source register identifiers, one destination register identifier, and a twelve-bit immediate value. Each instruction must be stored in memory in a byte-aligned fashion. If a program has 100 instructions, the amount of memory (in bytes) consumed by the program text is?
    ```
    Answer:
    ```
    ```
    Solution:
    ```py
    Address size = 6-bits, as 64 registers
    Opcode size = 4-bits
    Instruction design = opcode + 2 * address + 1 * address + 12-bits
    Instruction size = 4 + 2 * 6 + 6 + 12 = 34-bits = 4.25 B = 5 B
    Total instuction size = 100 * 5 = 500 B
    ```
> **Learning**: Calculate bit to byte conversion at instruction level, not at last level otherwise will get anwers as 425 Band its wrong.

5. Question:
    ```py
    Consider a system which supports 2-address instructions and 1-address instructions both. The system has 6-bit instructions and 2-bits addresses. If there are three 2-address instruction in the system then maximum and minimum how many 1-address instructions the system can support?
    ```
    Answer:
    ```
    ```
    Solution:
    ```py
    1. First get total opcode possible with instruction-type having minimum bits for opcode, in this case 2-address type, with 2 bits 4 opcode possible, sice only 3 are getting used, 1 combination remains unused.
    2. Now for 1 address type instruction total opcode = no. of unsed opcode from 2-address type * total opcode with 2-bits, 1 * 4 = 4
    3 For minimum answer will be 1 always. 
    ```
6. Question:
    ```py
    Consider a system which supports 3-address and 2-address instructions both. It has 30-bit instructions with 8-bit addresses. If there are 'x' 3-address instructions then maximum how many 2-address instructions can be formulated?
    ```
    Answer:
    ```
    ```
    Solution:
    ```py
    Instruction size = 30-bits
    Address size = 8-bits
    In 3-address total opcode bits = 30 - 3 * 8 = 6-bits
    In 2-address total opcode bits = 30 - 2 * 8 = 14-bits
    Since x instructions are there in 3-address, 
    therefore, total unused opcode combination = 2^6 - x
    hence total 2-address type = (2^6 - x) * 2 ^ 8.
    ```
7. Question:
    ```
    Consider a digital computer which supports only 3-address instructions. If size of instructions is 36-bits and the size of each address is 10-bits, then minimum and maximum number of instructions the computer can support?
    ```
    Answer:
    ```
    Max = 64
    Min = 1
    ```
    Solution:
    ```
    Instruction Size = 36-bits
    Address size = 10-bits
    opcode bits = 36 - 3 * 10 = 6 bits
    ```
7. Question:
    ```
    Consider a digital computer which supports 16 2-address instructions. If size of each address is 8-bits, then the size of instruction is bits?
    ```
    Answer:
    ```
    20-bits
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    In previous question if the instructions are stored in memory in byte-aligned fashion then space required in memory to store a program text of 200 instructions is bytes?
    ```
    Answer:
    ```
    600 B
    ```
    Solution:
    ```
    One instruction size = 20-bits = 20/8 B = 2.5 B ~ = 3 B
    Hence for 200 instructions size = 200 * 3 = 600 Byts
    ```
7. Question:
    ```
    Consider a digital computer which supports 32 3-address instructions. Size of each instruction is 38-bits. The system supports a word addressable memory, with word size of 32-bits, then the maximum allowable size of the memory is Kbytes?
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    Instruction Size = 38-bit
    Opcode bits = 5
    Address bits = (38 - 5) / 3 = 11 bits each.
    Total address possible = 2^11, and each address will have 32-bits(given)
    Total memory size = 2^11 * 32-bits = 8 KB
    ```
7. Question:
    ```
    Consider a digital computer which supports maximum of 32KB word addressable memory with word size 32-bits. The computer supports 40 distinct instructions each of which has 4 fields:
    1. Opcode
    2. Mode field to specify one of 7 addressing modes
    3. Register field to specify one of 24 processor registers
    4. Memory address field
    The size of instruction is bits?
    ```
    Answer:
    ```
    27-bits
    ```
    Solution:
    ```
    Opcode bits = 6-bits
    Mode bits = 3-bits
    Register Field = 5-bits
    Address filed = 13-bits, total words = 32KB/32bits
    ```
7. Question:
    ```
    Consider a digital computer which supports 32-bits instructions has instruction set of size 18, with each instruction has 4 fields:
    1. Opcode
    2. Mode field to specify one of 10 addressing modes
    3. Register field
    4. Memory address field of 14-bits
    The maximum number of general purpose registers possible in the CPU is?
    ```
    Answer:
    ```
    512 GPRs
    ```
    Solution:
    ```
    Instruction size = 32-bits
    Opcode bits = 5-bits
    Mode field = 4-bits
    Address = 14-bits
    Register Field = 32 - 5 - 4 - 14 = 9-bits
    ```
7. Question:
    ```
    Consider a system which supports 2-address instructions. If system has 24-bits instructions and 10-bits addresses then which of the following is/are possible number of instructions supported by system?
    a) 0
    b) 1
    c) 8
    d) 16
    ```
    Answer:
    ```
    Max it can support: 16
    And minimum will always be 1,
    Therefore, b, c, and d all three are possible.
    ```
    Solution:
    ```
    Instruction size = 24-bits
    Address size = 10-bits
    opcode bits = 24 - 2 * 10 = 4-bits
    ```
7. Question:
    ```
    Consider a hypothetical processor with largest instruction length being 32-bits and total 16 registers R0-R15. Processor supports following instructions:
        ADD   Ri, Rj
        SUB   Ri, Rj
        AND   Ri, Rj
        NOT   Ri
        MOV   Ri, Rj
        LOAD  Address //Loads with register RO
        Store Address // Stores the content of R1
        JUMP  Address
        JZ Address
    The maximum number of address lines on this processor is ?
    ```
    Answer:
    ```
    28
    ```
    Solution:
    ```
    Instruction size = 32-bits
    opcode bits = 4-bits, as 9 distinct addresses
    From Instruction 1, 2, 3, 5
    Address size = (32 - 4) / 2 = 14bits

    from Instruction 4, 6, 7, 8
    Address size = 32 - 4 = 28-bits
    ```
> 1. If there is fixed length instruction then OPCODE will be of variable length.

> 2. And, if instrcution size is variable then OPCODE will be of fixed length.

7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
7. Question:
    ```
    ```
    Answer:
    ```
    ```
    Solution:
    ```
    ```
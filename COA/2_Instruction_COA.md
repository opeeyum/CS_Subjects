## Instruction

A group of bits which instructs computer to perform some operation.

Instruction consists of two parts:

1.  Operation Code (Opcode): What operation to perform.
2.  Operands information: Address of operands, number of address stored can vary in the given instruction depending upon the implementation.

> ISA (Instruction Set Architecture): Collection of all instruction that a CPU supports.

### Types of Instructions

#### Based on operation

-   Data Transfer: `MOV, LDI(Load Immediate), LDA(Load Accumulator)`
-   Arithmetic & Logic: `ADD, SUB, AND, OR`
-   Machine Control: `EI(Enable Intrupt), DI(Disable Intrupt), PUSH, POP`
-   Iterative: `LOOP, LOOPE(Loop on Equal), LOOPZ(Loop on Zero)`
-   Branch: `JMP, CALL, RET(Return), JZ(Jump on Zero), JNZ(Jump on Non-Zero)`

#### Based on Operand Information

-   4-Address Instruction
    <table>
    <thead>
    <th>
    </th>
    <th>
    </th>
    <th>
    </th>
    <th>
    </th>
    <th>
    </th>
    </thead>
    <tbody>
    <tr>
    <td>
    Opcode
    </td>
    <td>
    Address 1
    </td>
    <td>
    Address 2
    </td>
    <td>
    Address 3
    </td>
    <td>
    Address 4
    </td>
    </tr>
    </tbody>
    <thead>
    <th>
    </th>
    <th>
    </th>
    <th>
    </th>
    <th>
    </th>
    <th>
    </th>
    </thead>
    </table>

    Within each instruction **maximum** 4 address can be specified.

    Two address fields are used to get the operands and third address field is used to store the result of the operation after instruction execution.

    Computer having 4-Address instruction does not have Program Counter, therefore last address in a instruction is address of next instruction to be executed.

    Disadvantages:

    -   Larger size Instruction.
    -   Larger size program in memory.
    -   Instruction fetch takes more time.
    -   Relocation in not easy, as relocation in 4-address type instruction requires to update each instruction because instructions have address of next instruction to be executed.

-   3-Address Instruction

    <table>
    <thead>
    <th>
    </th>
    <th>
    </th>
    <th>
    </th>
    <th>
    </th>
    </thead>
    <tbody>
    <tr>
    <td>
    Opcode
    </td>
    <td>
    Address 1
    </td>
    <td>
    Address 2
    </td>
    <td>
    Address 3
    </td>
    </tr>
    </tbody>
    <thead>
    <th>
    </th>
    <th>
    </th>
    <th>
    </th>
    <th>
    </th>
    </thead>
    </table>

    Within each instruction **maximum** 3 address can be specified.

    Two address fields are used to get the operands and third address field is used to store the result of the operation after instruction execution.

    All modern computer use 3-address instruction.

    Program counter is used to get address of next instruction.

-   2-Address Instruction

    <table>
      <thead>
      <th>
      </th>
      <th>
      </th>
      <th>
      </th>
      </thead>
      <tbody>
      <tr>
      <td>
      Opcode
      </td>
      <td>
      Address 1
      </td>
      <td>
      Address 2
      </td>
      </tr>
      </tbody>
      <thead>
      <th>
      </th>
      <th>
      </th>
      <th>
      </th>
      </thead>
      </table>

    Within each instruction **maximum** 2 address can be specified.

    Program counter is used to get address of next instruction.

    One address fields is used to get the operand and second address in 2-address type instruction is used as Source to get operand and Destination to store the result of the operation after instruction execution.

    Disadvantages:

    -   More number of instruction for a program as compared to 3-address instruction format.
    -   More memory for a program as more number of instruction.

-   1-Address Instruction
     <table>
      <thead>
      <th>
      </th>
      <th>
      </th>
      </thead>
      <tbody>
      <tr>
      <td>
      Opcode
      </td>
      <td>
      Address 1
      </td>
      </tr>
      </tbody>
      <thead>
      <th>
      </th>
      <th>
      </th>
      </thead>
      </table>

    Within each instruction **maximum** 1 address can be specified.

    Accumulator is used as second operand implicitly, Accumulator based architecture.

    Program counter is used to get address of next instruction.

-   0-Address Instruction

    <table>
      <thead>
      <th>
      </th>
      </thead>
      <tbody>
      <tr>
      <td>
      Opcode
      </td>
      </tr>
      </tbody>
      <thead>
      <th>
      </th>
      </thead>
      </table>

    Used in stack based architecture.

    No address is mentioned in the instructions, only opcode is specified.

    Two oprands are implicitly taken from the stack.

> If CPU supports 3-address instruction then it can support 2-Address, 1-Address, and 0-Address type instructions. This applicable to all instruction type 4, 3, 2, 1 and 0.

## Addressing Mode

### Effective Address

-   Address of operand in a computation-type instruction, i.e. ADD, SUB, MOV, AND
-   OR, The target address in a branch-type instuctions.
### Instruction Cycle

1. Instruction Fetch: Get Instruction from memory to CPU (Instruction Register). Program Counter Value is increased by Size of instruction loaded to instruction register.
2. Instruction Decode
3. Effective Address Calculation
4. Operand Fetch
5. Execution
6. Write Back - result

-   These instruction are classified into two cycles - Fetch Cycle and Execution Cycle.
<table>
    <thead>
      <th>
       Fetch Cycle
      </th>
    <th>
      Execution Cycle
    </th>
    </thead>
    <tbody>
    <tr>
    <td>
    Instruction Fetch
    </td>
    <td>
    Instruction Decode
    </td>
    </tr>
    <tr>
    <td>
    </td>
    <td>
    Effective Address Calculation
    </td>
    </tr>
    <tr>
    <td>
    </td>
    <td>
    Operand Fetch
    </td>
    </tr>
    <tr>
    <td>
    </td>
    <td>
    Instruction Execution
    </td>
    </tr>
    <tr>
    <td>
    </td>
    <td>
    Write Back Result
    </td>
    </tr>
    </tbody>
    </table>

### Addressing Mode

-   Its is used to specifiy how to access the operand whose address is mentioned in the instruction.

<table>
      <thead>
      <th>
      </th>
      <th>
      </th>
      <th>
      </th>
      </thead>
      <tbody>
      <tr>
      <td>
      Opcode
      </td>
      <td>
      Mode
      </td>
      <td>
      Address
      </td>
      </tr>
      </tbody>
      <thead>
      <th>
      </th>
      <th>
      </th>
      <th>
      </th>
      </thead>
      </table>

#### Implied Mode
Opcode definition specifies operand also.

Ex. INCA: Increment Accumulator

#### Immediate Mode
Address part in instruction is itself a operand value.
- Immediate addressing Mode is used to intialize register with constant value.

#### Direct Mode (Absolute Mode)
Address part in instruction is a memory address for operand i.e effective address.

#### Indirect Mode
Adddress part in instruction is a address for address of a instruction, that is address provided in a intruction is a address of effective address.

#### Register Mode
Address part in instruction specifies a reference to a register which holds the operand.

#### Register Indirect Mode
Address part in instruction specifies a reference to a reister which holds effective address i.e reference to meomry where operand in present.

- This addressing mode is used to shorten instruction length.

#### Auto Increment/Decrement Mode
- It is used to access table of content sequentially.
- It is a variant of register indirect mode.
- The content of register (effective address) is automatically incremented or decremented.
- Auto-increment will be the Post-Increment.
- While Auto-decrement mode will be the Pre-Decrement.
- Both Auto Increment/Decrement mode come with driver code i.e loop instructions to fetch operand multiple times.

#### Indexed Mode
- Used to access array element.
- Effective Address = Base Address + Index Value
- In the instruction Base address will be specified and Index value will be calculated from Index Register.
- The problem with Indexed addressing mode is that if, Os relocates the program then all instruction needs to be relocated as base address is specified in the instruction, which is not advisable.

#### Index, Base Register Mode
- Advancement to Indexed Mode, both index value and Base register is taken from special purpose register Index Register and Base Register respectively.

#### Index, Base Register + Displacement Mode
- This addressing mode is used to access array of records.
- Effective address = Base Register + Index Register + Address field value of instruction

#### Scaled mode

#### PC-Relative Mode

-   This Mode is used for branch type instruction.
-   Consider following memory representation
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

    -   A Program is stored from memory location 500 to 528.
    -   Memory is WOrd addressable and 1 word = 4 Bytes.
    -   Now,
    -   Assume, CPU is executing Instruction-2, then PC (Program Counter) = 504.
    -   In Decode CPU detects the INs-2 is a branch instruction(Conditional branch).
    -   At Execution Phase CPU will check for the branch condition; True OR False.
    -   If False (Branch Not Taken): **PC value will not get updated** and Next instruction in the sequence will be executed, I-3 in this case.
    -   If True (Branch Taken):
        -   Lets say,
        -   I-2 is branching to I-6,
        -   that is, target instrcution is I-6,
        -   hence, target address = 516
        -   PC will updated, PC = 504 + 12
    -   Therefore, Effective address in PC-Relative mode = PC + addresss field value in instruction.
    -   This mode is used for **Intra**-segment jump, that is target instruction is present same set on Instruction as branching Instruction.

#### Base Register Mode

-   This mode is used for **Inter**-Segment jumps.
-   Different to PC-relative mode, Value of address field from instruction, will be added to value of special purpose register Base-register.
-   Hence, effective address = Base Register + Address Field Value.
-   If program is relocated, nothing to update in Instruction, just update teh Base register value.

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

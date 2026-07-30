# 014 — Fetch, Decode, Execute

A CPU runs a program by repeatedly retrieving instructions, interpreting them, and carrying them out.

This repeating process is called the **fetch-decode-execute cycle**.

## 1. Fetch

The program counter holds the address of the next instruction.

A simplified fetch sequence is:

```text
Program counter provides address
        ↓
Memory returns instruction
        ↓
Instruction enters instruction register
        ↓
Program counter advances
```

At the end of fetch, the CPU has a binary instruction ready to examine.

## 2. Decode

The control unit interprets the instruction.

It determines things such as:

- what operation is requested;
- which registers are involved;
- whether memory must be accessed;
- where the result should go;
- whether the normal instruction order should change.

The instruction contains structured fields defined by the processor's instruction-set architecture.

The control unit converts those fields into control signals.

## 3. Execute

During execute, the CPU performs the required hardware actions.

This may involve:

- moving data between registers;
- sending values into the ALU;
- selecting an arithmetic or logical operation;
- reading or writing memory;
- updating flags;
- changing the program counter.

## Example: Adding Two Registers

Consider a simplified instruction:

```text
ADD A, B
```

The CPU may perform actions resembling:

1. Fetch the instruction from memory.
2. Place it in the instruction register.
3. Decode it as an addition involving registers A and B.
4. Send the register values toward the ALU.
5. Select the ALU's add operation.
6. Allow the result to settle.
7. Store the result in the chosen register at a clock edge.
8. Continue with the next instruction.

The exact sequence depends on the CPU design.

## One Instruction May Take Several Steps

A command that looks simple at the programming level may require several internal transfers and clock cycles.

For example, loading a value from memory can require:

```text
place address
request memory read
wait for data
capture returned value
store value in destination register
```

This is why one instruction should not be imagined as one transistor switching once.

It is a coordinated sequence involving many circuits.

## Jumps and Branches

Normally, the program counter advances to the next instruction.

A jump or branch changes that flow by loading a different address into the program counter.

A conditional branch may depend on a status flag:

```text
If zero flag = 1, jump to another address
Otherwise, continue normally
```

This ability creates loops, decisions, function calls, and program structure.

## Clocked Coordination

Between clock edges, signals move through the data path and logic circuits.

At selected edges, enabled registers capture new values.

The clock helps ensure that one stage's result becomes stable before the next state is committed.

Modern processors may overlap or reorganize parts of instruction processing, but the basic fetch-decode-execute model remains a useful foundation.

## The Full Chain So Far

```text
atoms and charge
        ↓
electricity and semiconductors
        ↓
transistors
        ↓
logic gates and Boolean logic
        ↓
binary representation
        ↓
adders and arithmetic circuits
        ↓
latches, flip-flops, registers, and clocks
        ↓
RAM and storage
        ↓
CPU components
        ↓
fetch, decode, execute
```

Complex software rests on this chain of simpler physical and logical layers.

## Connection to the Next Layer

The CPU can now fetch and carry out instructions, but we have not yet examined how instruction bit patterns are designed.

The next chapter will cover **instruction sets and machine code**.

## Knowledge Check

Which stage determines whether an instruction means add, load, store, compare, or jump?
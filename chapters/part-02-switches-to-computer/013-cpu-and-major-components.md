# 013 — The CPU and Its Major Components

A CPU is not one magical object that understands programs. It is an organized collection of circuits that move, store, transform, and control binary values.

## Registers

Registers are tiny, extremely fast storage locations inside the CPU.

They may hold:

- numbers being calculated;
- memory addresses;
- the current instruction;
- intermediate results;
- status information.

Different registers have different jobs.

## Arithmetic Logic Unit

The **arithmetic logic unit**, or ALU, performs operations such as:

```text
ADD
SUBTRACT
AND
OR
XOR
COMPARE
SHIFT
```

The ALU receives input values, performs the selected operation, and produces an output.

It does not choose the operation for itself. Control signals tell it what to do.

## Control Unit

The control unit coordinates the CPU.

It sends signals that determine:

- which register places data onto a path;
- which register accepts a value;
- which ALU operation is selected;
- whether memory is read or written;
- when stored state updates.

An instruction that looks like one command to a programmer may become several smaller control actions inside the processor.

## Buses and Internal Paths

A bus is a shared group of wires that carries several bits at once.

An 8-bit bus carries an 8-bit pattern. A wider bus carries more bits in parallel.

A simplified internal transfer might be:

```text
Register A → bus → Register B
```

Control signals select the source and destination.

Only one source should drive a shared bus at a time. Otherwise, different circuits may attempt to force conflicting electrical values onto the same wires.

## Program Counter

The **program counter** stores the address of the next instruction to fetch.

After a normal instruction, it usually advances to the following instruction.

A jump, branch, call, return, or interrupt can replace it with a different address.

The program counter gives instruction execution an order.

## Instruction Register

The **instruction register** holds the instruction currently being decoded or executed.

A simplified flow is:

```text
Memory → instruction register → control unit
```

The control unit examines the instruction's bit pattern and determines which hardware actions are required.

## Memory Address and Data Registers

A simplified CPU may also use registers dedicated to memory transfers:

- a memory address register holds the location being accessed;
- a memory data register holds data moving to or from memory.

Real CPU designs vary, but these concepts make the movement easier to understand.

## Status Flags

Operations may produce status information such as:

- result was zero;
- carry occurred;
- result was negative;
- arithmetic overflow occurred.

These flags can influence later instructions, especially conditional branches.

## The Clock

The clock helps coordinate state changes.

Between clock edges, values move through logic and settle. At an appropriate edge, enabled registers capture their next values.

The clock does not perform the work. It provides timing so the components update in an organized way.

## The CPU as a Data Path and Control System

A useful simplified model divides the CPU into two cooperating parts:

```text
Data path:
registers + buses + ALU

Control:
instruction decoding + control signals + timing
```

The data path performs transfers and operations. The control unit directs the sequence.

## Connection to the Next Layer

The CPU now has everything needed to carry out instructions, but we still need to follow the repeating process in order.

The next chapter connects the program counter, memory, instruction register, control unit, ALU, and registers through the **fetch-decode-execute cycle**.

## Knowledge Check

Why is the control unit necessary if the ALU already knows how to add, compare, and perform logical operations?
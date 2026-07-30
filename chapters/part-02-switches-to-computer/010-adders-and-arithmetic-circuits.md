# 010 — Adders and Arithmetic Circuits

Binary numbers become useful when circuits can perform operations on them.

The simplest important arithmetic circuit is an **adder**.

## Adding One Bit

Consider adding two single bits:

| A | B | Sum | Carry |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 1 |

The `Sum` column behaves like an XOR gate.

The `Carry` column behaves like an AND gate.

That gives us a **half adder**:

```text
Sum   = A XOR B
Carry = A AND B
```

## Why Carry Exists

In decimal, `9 + 1` produces `0` in the current position and carries `1` into the next position.

Binary works the same way:

```text
1 + 1 = 10
```

The current bit becomes `0`, and the next bit receives a carry of `1`.

## Full Adders

A half adder accepts two inputs. But when adding multi-bit numbers, each position may also receive a carry from the position before it.

A **full adder** accepts:

```text
A
B
Carry-in
```

and produces:

```text
Sum
Carry-out
```

Full adders can be chained together so that the carry from one bit position becomes the carry-in for the next.

## Adding Multiple Bits

Example:

```text
  0101   = 5
+ 0011   = 3
------
  1000   = 8
```

The circuit handles one column at a time. Carries move toward the higher-value bit positions.

A simple design is called a **ripple-carry adder** because each carry must ripple through the chain.

## Arithmetic Is Built From Logic

Addition may look mathematical at the surface, but the hardware is still using ordinary gates:

- XOR for differences between input bits;
- AND for carry conditions;
- OR for combining carry paths.

Larger arithmetic circuits can build on these ideas to perform:

- subtraction;
- incrementing;
- comparisons;
- shifts;
- multiplication.

## The ALU

The CPU groups arithmetic and logical operations inside the **arithmetic logic unit**, or ALU.

An ALU may be able to perform:

```text
ADD
SUBTRACT
AND
OR
XOR
COMPARE
SHIFT
```

Control signals tell the ALU which operation to produce.

The ALU does not decide what operation is needed. It performs the operation selected by the control unit.

## Speed and Timing

Real circuits need time for electrical changes to pass through their gates.

If many full adders are chained together, the final answer cannot be trusted until the carries have had time to settle.

This is one reason timing matters in computer design.

## Connection to the Next Layer

Arithmetic circuits can calculate a result, but without memory the result disappears as soon as the inputs change.

The next step is creating circuits that can **hold state** using feedback, latches, flip-flops, registers, and clocks.

## Knowledge Check

Why does a full adder need a carry-in input while a half adder does not?
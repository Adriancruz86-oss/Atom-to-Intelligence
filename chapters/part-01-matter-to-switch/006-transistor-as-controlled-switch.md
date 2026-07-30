# 006 — The Transistor as a Controlled Switch

A transistor allows one electrical signal to control another.

That makes it useful as a switch.

## The Basic Idea

A transistor has a control input and a path through which current may flow.

In a simplified digital model:

```text
control off  → current path blocked
control on   → current path allowed
```

The real physics is more detailed, but this model is enough to understand why transistors are useful in computers.

## From Voltage to Binary

Digital circuits treat voltage ranges as logical states:

```text
low voltage  → 0
high voltage → 1
```

A transistor can use one of those states to control whether another signal passes through the circuit.

## Why Transistors Matter

A single transistor is simple. Large groups of transistors can:

- invert a signal;
- compare signals;
- perform arithmetic;
- store state;
- control the movement of data.

Modern processors contain enormous numbers of transistors, but their complexity grows from combinations of this basic controlled-switch behavior.

## Connection to the Next Layer

One transistor does not perform a meaningful logical decision by itself. By connecting transistors together, we can create **logic gates**.

## Knowledge Check

What makes a transistor different from an ordinary switch operated by a person?
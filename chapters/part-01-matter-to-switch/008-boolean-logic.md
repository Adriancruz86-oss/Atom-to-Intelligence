# 008 — Boolean Logic

Boolean logic is a system for reasoning with two states, usually written as `0` and `1`, or false and true.

Logic gates physically implement these rules with voltage and transistors.

## Expressions Describe Circuits

A Boolean expression can describe what a circuit should output.

```text
A AND B
NOT A
A OR B
A XOR B
```

A truth table lists every possible input combination and the output produced by the rule.

## Combining Gates

Simple gates can be connected to make more useful decisions.

For example:

```text
(A AND B) OR C
```

The circuit first evaluates `A AND B`, then sends that result into an OR gate with `C`.

## Why This Scales

The gates do not understand numbers, instructions, or programs. They only react to electrical inputs according to their construction.

But combinations of Boolean rules can create:

- adders;
- selectors;
- comparison circuits;
- memory circuits;
- control circuits.

This is the bridge from switches to computation.

## Part I Takeaway

The dependency chain is now:

```text
atoms and charge
        ↓
electricity
        ↓
materials
        ↓
semiconductors and doping
        ↓
transistors
        ↓
logic gates
        ↓
Boolean circuits
```

## Connection to Part II

The next step is using gates to represent binary numbers and perform arithmetic. Later, feedback between gates allows circuits to store state using latches and flip-flops.

## Knowledge Check

Why can a circuit perform a complicated operation even though each individual gate follows only a simple rule?
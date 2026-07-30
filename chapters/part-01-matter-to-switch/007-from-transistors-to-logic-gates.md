# 007 — From Transistors to Logic Gates

Logic gates are small circuits built from transistors. They take binary inputs and produce a binary output.

## NOT

A NOT gate reverses its input.

```text
0 → 1
1 → 0
```

## AND

An AND gate outputs `1` only when both inputs are `1`.

```text
0 AND 0 → 0
0 AND 1 → 0
1 AND 0 → 0
1 AND 1 → 1
```

## OR

An OR gate outputs `1` when at least one input is `1`.

```text
0 OR 0 → 0
0 OR 1 → 1
1 OR 0 → 1
1 OR 1 → 1
```

## NAND and NOR

NAND is the opposite of AND. NOR is the opposite of OR.

These gates are especially important because complete digital systems can be built from repeated combinations of only NAND gates or only NOR gates.

## XOR

XOR outputs `1` when the two inputs are different.

```text
0 XOR 0 → 0
0 XOR 1 → 1
1 XOR 0 → 1
1 XOR 1 → 0
```

XOR becomes useful in adders, comparisons, and many cryptographic operations.

## Connection to the Next Layer

Logic gates give us physical circuits that follow rules. Boolean logic gives us a language for describing and combining those rules.

## Knowledge Check

Which gate outputs `1` only when its two inputs are different?
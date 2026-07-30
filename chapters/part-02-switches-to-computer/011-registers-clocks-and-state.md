# 011 — Registers, Clocks, and State

Logic gates can make decisions, and adders can calculate results. But a computer also needs to remember values.

That requires **state**.

## Feedback Creates Memory

A normal gate produces an output from its current inputs.

A memory circuit feeds part of its output back into the circuit:

```text
output → input path → output
```

Once the circuit settles into a stable condition, the feedback keeps reinforcing that condition.

This is the basic idea behind a **latch**.

## SR Latch

An SR latch has controls for setting and resetting one stored bit.

```text
S = Set
R = Reset
Q = stored output
Q̅ = opposite output
```

For a NOR-based SR latch:

| S | R | Result |
|---|---|---|
| 0 | 0 | Hold previous state |
| 1 | 0 | Set Q to 1 |
| 0 | 1 | Reset Q to 0 |
| 1 | 1 | Invalid or problematic state |

When the latch is holding a value, `Q` and `Q̅` keep each other in opposite states.

## Gated Latch

An enable input controls whether the latch is allowed to respond.

```text
Enable = 1 → input may change the stored bit
Enable = 0 → hold the current bit
```

The enable signal does not create the data. It grants permission for the data to affect the stored state.

## D Latch

A D latch simplifies the inputs.

```text
D = data to store
Enable = permission to change
Q = stored value
```

When enabled, `Q` follows `D`. When disabled, `Q` holds the last accepted value.

The circuit internally uses both `D` and `NOT D`, preventing the invalid SR-latch combination.

## Flip-Flops and Clock Edges

A latch can remain open for an interval. A flip-flop changes only at a specific clock edge.

```text
Before edge: inputs settle
At edge:     input is captured
After edge:  output holds
```

The clock acts like a repeated coordination signal.

A rising-edge-triggered flip-flop captures its input when the clock changes from low to high. A falling-edge-triggered design captures on the opposite transition.

## Registers

One flip-flop stores one bit.

A group of flip-flops stores several bits together.

```text
8 flip-flops = 8-bit register = 1 byte
```

At a clock edge, the enabled flip-flops capture their input bits together.

A load control determines whether the register accepts a new value:

```text
Load = 1 → capture new input at the clock edge
Load = 0 → keep the old value
```

## Why Timing Matters

Different circuits take small amounts of time to settle.

The clock gives the system a rhythm:

1. Values leave registers.
2. Logic or arithmetic circuits process them.
3. The result settles.
4. A clock edge stores the result in a destination register.

Not every component changes at every edge. Only enabled storage elements update.

## Connection to the Next Layer

Registers provide extremely fast storage inside the CPU, but programs and larger collections of data need much more space.

The next chapter explains RAM, addresses, and the difference between volatile and persistent storage.

## Knowledge Check

What is the main timing difference between a latch and an edge-triggered flip-flop?
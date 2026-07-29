# 003 — Voltage, Current, and Resistance

## Three Ideas That Describe a Circuit

To reason about electricity, we need to separate three related concepts:

- **Voltage** describes electrical potential difference.
- **Current** describes the rate at which charge flows.
- **Resistance** describes how strongly a material or component opposes that flow.

They are connected, but they are not interchangeable.

## Voltage: The Difference That Can Drive Change

Voltage is measured between two points. It describes a difference in electric potential.

A battery creates a voltage difference between its terminals. When those terminals are connected through a complete circuit, that difference can establish an electric field that drives charge through the circuit.

A common analogy compares voltage to pressure difference in a water system. The analogy helps, but voltage is not literally pressure. It is an electrical potential difference that can transfer energy to charges.

## Current: Charge Flow Over Time

Current measures how much electric charge passes a point per unit of time.

More moving charge per second means more current.

Current is not simply “electricity stored in a wire.” It describes motion. A circuit can have voltage across an open switch while no sustained current flows through the break.

This distinction matters later because digital circuits use voltage levels to represent states, while current flows as those states are created, changed, and maintained.

## Resistance: Opposition to Current

Resistance measures how strongly a component or material opposes current.

Resistance depends on factors such as:

- the material;
- the length and thickness of the path;
- temperature;
- and the component's design.

A resistor deliberately limits current. A wire usually has low resistance. An insulator has extremely high resistance under ordinary conditions.

## Ohm's Law

For many components under appropriate conditions, voltage, current, and resistance are related by:

```text
V = I × R
```

Where:

- `V` is voltage in volts;
- `I` is current in amperes;
- `R` is resistance in ohms.

The equation can be rearranged:

```text
I = V / R
R = V / I
```

This means that, for a fixed resistance, increasing voltage increases current. For a fixed voltage, increasing resistance decreases current.

Real electronic components are not always perfectly described by a constant resistance, but Ohm's law gives us a strong starting model.

## Power: How Fast Energy Is Transferred

Electrical power describes the rate at which energy is transferred or converted.

```text
P = V × I
```

A component that handles greater voltage and current may convert more electrical energy each second, often producing useful work and heat.

Heat matters in computing. Transistors switching billions of times, leakage current, and resistance all contribute to power consumption and heat. That is one reason processors require cooling and why energy efficiency limits computer design.

## Why These Ideas Matter for Computation

A digital circuit does not need to know what a number means. It needs stable physical ranges that can be distinguished reliably.

Engineers design circuits so that voltage ranges represent logical states. Components control how current can flow, while resistance, capacitance, timing, and noise affect whether those states remain dependable.

The computer's clean world of `0` and `1` is built on analog electrical behavior that must be carefully controlled.

## What Comes Next

Not every material responds to voltage in the same way. The next chapter compares conductors, insulators, and semiconductors—and explains why semiconductors made modern computing possible.

## Knowledge Check

1. Why is voltage always measured between two points?
2. How can voltage exist without sustained current?
3. Under a fixed voltage, what happens to current when resistance increases?
4. Why does electrical power matter to processor design?
5. Why is binary computation still dependent on analog physics?

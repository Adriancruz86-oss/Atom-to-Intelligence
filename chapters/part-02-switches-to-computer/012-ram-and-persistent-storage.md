# 012 — RAM and Persistent Storage

Registers are fast, but they are too small to hold an entire running program and all of its data.

A computer therefore uses several layers of storage.

## RAM

**Random-access memory**, or RAM, holds programs and data that the CPU is actively using.

RAM is called random access because the system can directly access a chosen memory location rather than reading every earlier location first.

Each location has an address.

```text
Address 1000 → stored value
Address 1001 → stored value
Address 1002 → stored value
```

The address identifies where data belongs. The stored bits are the data at that location.

## Reading and Writing Memory

A simplified memory operation uses three kinds of information:

- an address identifying the location;
- data being transferred;
- a control signal selecting read or write.

For a read:

```text
Choose address → request READ → receive stored data
```

For a write:

```text
Choose address → provide data → request WRITE
```

## Volatile Memory

Most system RAM is **volatile**.

That means it requires power to maintain its stored state. When power is removed, the stored working data disappears.

This is not a defect. RAM is designed for fast temporary access while the computer is running.

## Persistent Storage

Drives such as SSDs and hard drives are **persistent** or **nonvolatile** storage.

They retain information without continuous power.

Persistent storage holds:

- the operating system;
- installed programs;
- documents and media;
- saved settings;
- files that must survive shutdown.

## Loading a Program

A program stored on an SSD is not normally executed directly from the drive one instruction at a time.

A simplified flow is:

```text
Program stored on SSD
        ↓
Operating system loads needed parts into RAM
        ↓
CPU fetches instructions and data from memory
```

Registers then hold the small set of values the CPU is working with immediately.

## Storage Hierarchy

Computer storage is a tradeoff between speed, size, and cost.

```text
Registers → fastest and smallest
Cache     → very fast and small
RAM       → fast and larger
SSD/HDD   → slower and persistent
```

The layers work together so the CPU can access frequently needed information quickly while the system still has large, durable storage.

## Sleep and Hibernation

Sleep usually keeps system state in powered RAM while placing much of the computer into a low-power condition.

Hibernation saves the active state to persistent storage before powering down more completely. On restart, that saved state can be loaded back into RAM.

## Memory Is Organized Bits

Whether data is in a register, RAM, or an SSD, it is represented by physical states interpreted as bits.

The physical mechanism changes between technologies, but the abstraction remains:

```text
address or location → stored binary pattern
```

## Connection to the Next Layer

The system now has logic, arithmetic, state, registers, and larger memory.

The next step is assembling these parts into the major components of a CPU and explaining how data moves between them.

## Knowledge Check

Why must a program stored on persistent storage usually be loaded into RAM before the CPU actively runs it?
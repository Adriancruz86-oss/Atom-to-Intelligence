# 009 — Binary Numbers and Data Representation

A computer does not begin with numbers, letters, pictures, or instructions. At the physical level, it begins with electrical states.

A simplified digital circuit treats one voltage range as `0` and another as `1`.

Those two states are called **bits**.

## One Bit, Two Possibilities

A single bit can represent only two possibilities:

```text
0
1
```

Two bits can represent four patterns:

```text
00
01
10
11
```

Each added bit doubles the number of possible patterns.

```text
1 bit  = 2 patterns
2 bits = 4 patterns
3 bits = 8 patterns
8 bits = 256 patterns
```

Eight bits form one **byte**.

## Binary Numbers

Binary uses place values based on powers of two.

```text
128 64 32 16 8 4 2 1
```

For example:

```text
00000101
```

means:

```text
4 + 1 = 5
```

The circuit does not know that the pattern means five. People and software assign that interpretation.

## Patterns Need Meaning

The same binary pattern can mean different things depending on context.

```text
01000001
```

It might represent:

- the number `65`;
- the letter `A` in an encoding such as ASCII;
- part of a machine instruction;
- a color value;
- part of a memory address.

Bits provide patterns. A format or instruction tells the system how to interpret them.

## Signed Numbers

Computers also need negative numbers. A common method is **two's complement**.

In an 8-bit system:

```text
00000101 = 5
11111011 = -5
```

Two's complement is useful because the same adder circuitry can handle much of both positive and negative arithmetic.

## Text, Images, and Sound

Everything stored digitally is eventually represented by bit patterns.

- Text uses character encodings.
- Images use numbers for pixel colors and positions.
- Sound uses numerical samples of air-pressure changes.
- Programs use binary instructions and data.

This does not mean all information is naturally binary. It means computers encode information into binary so circuits can store and process it.

## Why This Matters

Logic gates operate on individual bits. To build a useful computer, those bits must be grouped and interpreted as larger values.

Binary representation creates the bridge from simple on/off electrical states to numbers and data.

## Connection to the Next Layer

Once a computer can represent numbers, it needs circuits that can operate on them.

The next step is combining logic gates into **adders and arithmetic circuits**.

## Knowledge Check

Why can the same 8-bit pattern represent a number, a letter, or part of an instruction?
# Number Systems

## Overview

A **Number System** is a method of representing numbers using a set of symbols (digits). Every digital system, including computers, microprocessors, FPGAs, and ASICs, stores and processes information using number systems.

Understanding number systems is the first step toward learning Digital Electronics, Computer Architecture, RTL Design, and Processor Design.

---

# Learning Objectives

After completing this chapter, you will be able to:

* Understand different number systems.
* Convert numbers between different bases.
* Perform binary arithmetic.
* Represent signed numbers.
* Understand complements and overflow.
* Apply these concepts in digital circuit design.

---

# Table of Contents

1. Introduction
2. Decimal Number System
3. Binary Number System
4. Octal Number System
5. Hexadecimal Number System
6. Number System Conversion
7. Binary Arithmetic
8. Signed Number Representation
9. One's Complement
10. Two's Complement
11. Overflow
12. Applications
13. Interview Questions
14. Practice Problems
15. References

---

# 1. Introduction

A number system is defined by its **base (radix)**.

The base determines:

* Number of symbols used
* Place value of each digit

General representation:

```
Number = Σ (Digit × Base^Position)
```

Example:

```
(1011)₂

= 1×2³ + 0×2² + 1×2¹ + 1×2⁰

= 8 + 0 + 2 + 1

= 11₁₀
```

---

# 2. Decimal Number System (Base-10)

Digits:

```
0 1 2 3 4 5 6 7 8 9
```

Example:

```
5827

=5×10³
+8×10²
+2×10¹
+7×10⁰

=5827
```

Used in everyday life.

---

# 3. Binary Number System (Base-2)

Digits:

```
0
1
```

Binary is the language of digital electronics.

Example:

```
110101₂

=53₁₀
```

Applications

* CPUs
* FPGA
* ASIC
* Memory
* Registers

---

# 4. Octal Number System (Base-8)

Digits

```
0–7
```

Example

```
735₈
```

Relationship

```
1 Octal Digit = 3 Binary Bits
```

Example

```
735₈

↓

111011101₂
```

Applications

* Legacy computer systems
* UNIX permissions

---

# 5. Hexadecimal Number System (Base-16)

Digits

```
0 1 2 3 4 5 6 7 8 9 A B C D E F
```

Example

```
2AF₁₆
```

Relationship

```
1 Hex Digit = 4 Binary Bits
```

Example

```
A3₁₆

↓

10100011₂
```

Applications

* Memory addresses
* Machine code
* Debugging
* Embedded Systems

---

# 6. Number System Conversion

## Decimal → Binary

Method

Repeated division by 2.

Example

```
25

↓

25/2 =12 R1

12/2 =6 R0

6/2 =3 R0

3/2 =1 R1

1/2 =0 R1

Answer

11001₂
```

---

## Binary → Decimal

Multiply each bit with powers of two.

Example

```
10110₂

=16+4+2

=22₁₀
```

---

## Binary → Octal

Group into 3 bits.

```
101110111

↓

101 110 111

↓

5 6 7

↓

567₈
```

---

## Binary → Hexadecimal

Group into 4 bits.

```
11010110

↓

1101 0110

↓

D6₁₆
```

---

## Hexadecimal → Binary

Replace every hex digit by four bits.

```
3F₁₆

↓

00111111₂
```

---

# 7. Binary Arithmetic

## Binary Addition

Rules

```
0+0=0

0+1=1

1+0=1

1+1=10

1+1+1=11
```

Example

```
1010

+

1101

------

10111
```

---

## Binary Subtraction

Rules

```
0−0=0

1−0=1

1−1=0

0−1=Borrow
```

---

## Binary Multiplication

Rules

```
0×0=0

0×1=0

1×0=0

1×1=1
```

---

# 8. Signed Number Representation

Positive numbers

```
MSB = 0
```

Negative numbers

```
MSB = 1
```

Common representations

* Sign Magnitude
* One's Complement
* Two's Complement

---

# 9. One's Complement

Invert every bit.

Example

```
10101010

↓

01010101
```

Disadvantage

Two representations of zero.

```
00000000

11111111
```

---

# 10. Two's Complement

Step 1

Invert bits.

Step 2

Add 1.

Example

```
25

00011001

↓

11100110

↓

11100111
```

Advantages

* Single zero
* Easy subtraction
* Used by modern processors

---

# 11. Overflow

Overflow occurs when the result cannot be represented using the available number of bits.

Example (4-bit)

```
1111

+

0001

------

10000
```

The fifth bit cannot be stored in a 4-bit register.

---

# Comparison

| Number System | Base | Digits   |
| ------------- | ---- | -------- |
| Binary        | 2    | 0–1      |
| Octal         | 8    | 0–7      |
| Decimal       | 10   | 0–9      |
| Hexadecimal   | 16   | 0–9, A–F |

---

# Applications

* Digital Electronics
* FPGA Design
* ASIC Design
* RTL Design
* Computer Architecture
* Embedded Systems
* Microprocessors
* Memory Addressing

---

# Interview Questions

1. Why do computers use binary?
2. What is radix?
3. Difference between octal and hexadecimal?
4. Why is hexadecimal preferred over binary?
5. Explain two's complement.
6. Why is one's complement rarely used?
7. What is overflow?
8. Difference between signed and unsigned numbers?
9. Convert 111101₂ to decimal.
10. Convert 255₁₀ to hexadecimal.

---

# Practice Problems

* Convert 75₁₀ to binary.
* Convert 101011₂ to decimal.
* Convert 7F₁₆ to binary.
* Convert 110101011₂ to hexadecimal.
* Find the two's complement of 10110100.
* Add 101101 + 110011.
* Subtract 11010 − 1011.
* Identify whether overflow occurs in 1111 + 0001.

---

# References

* Digital Design — M. Morris Mano
* Digital Fundamentals — Thomas L. Floyd
* Computer Organization and Design — Patterson & Hennessy
* CMOS VLSI Design — Weste & Harris

---

## Status

* [x] Decimal Number System
* [x] Binary Number System
* [x] Octal Number System
* [x] Hexadecimal Number System
* [x] Number System Conversion
* [x] Binary Arithmetic
* [x] Signed Number Representation
* [x] One's Complement
* [x] Two's Complement
* [x] Overflow

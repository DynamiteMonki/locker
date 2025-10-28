---
tags:
  - cs
  - cs50
from: YouTube
Date: 2025-10-23
---
---

- Computers represent data in 0's and 1's thats in binary notation

**Binary** is the number system where there are only two values that is 0 and 1 and a sequence of those make up a piece of data.

for example, 

A number `202` in binary can be :

```binary
11001010
```

in the above piece you can see that there is no continuous streams of zeros as we see in decimal system.

But in binary that values start from 1 -> 2 -> 4 -> 8 -> 16 -> 32 -> 64 - > 128 -> 256 and so on.

you just plugin the values from *right to left as in the above sequence of 0's and 1's with the binary sequence* you will surely get the number 202

Proff just put in `2+8+64+128` 

---

## **Binary Basics (Bits and Bytes)**

- **Bit**: The smallest unit of data (0 or 1)
- **Byte**: 8 bits grouped together (e.g., 01101001)
- These 0s and 1s correspond to electrical signals - typically low voltage (0) and high voltage (1)

## **How Different Data Types Are Represented**

### **Numbers**

- **Integers**: Stored in binary format
    - Example: The number 5 = 00000101 in binary
- **Negative numbers**: Often use "two's complement" representation
- **Decimals**: Use floating-point representation (sign, exponent, mantissa)

### **Text**

- **Characters**: Encoded using standards like:
    - ASCII (7-8 bits per character)
    - Unicode/UTF-8 (variable length, supports all languages)
    - Example: Letter 'A' = 01000001 in ASCII

### **Images**

- Stored as grids of **pixels**
- Each pixel has color values (RGB - Red, Green, Blue)
- Each color component typically uses 8 bits (0-255)

### **Audio**

- Sound waves are **sampled** at regular intervals
- Each sample is stored as a binary number
- Higher sample rates = better quality

### **Video**

- Sequence of images (frames) plus audio
- Often compressed to save space

## **Why Binary?**

- **Reliability**: Easy to distinguish between two states
- **Simple circuits**: Transistors work as on/off switches
- **Noise resistance**: Less prone to errors than multi-level systems

---

## **Two's Complement**

Two's complement is the most common method computers use to represent **signed integers** (positive and negative numbers) in binary. It's elegant because it allows the same circuitry to handle both addition and subtraction.

## **How It Works**

### **Key Rules:**

- The **leftmost bit** (MSB - Most Significant Bit) indicates the sign:
    - 0 = positive number
    - 1 = negative number
- Positive numbers are stored normally in binary
- Negative numbers use the two's complement conversion

## **Converting to Two's Complement (for negative numbers)**

**Two-step process:**

1. **Invert all bits** (0→1, 1→0) - this is called "one's complement"
2. **Add 1** to the result

### **Example: Representing -5 in 8-bit two's complement**

text

```
Start with +5:     00000101
Step 1 - Flip bits: 11111010  (one's complement)
Step 2 - Add 1:     11111011  (two's complement)

So -5 = 11111011
```

## **8-bit Two's Complement Range**

- **Positive**: 0 to 127 (00000000 to 01111111)
- **Negative**: -1 to -128 (11111111 to 10000000)
- Total range: -128 to +127

## **Why Two's Complement is Brilliant**

### **1. Addition Works Naturally**

text

```
Example: 5 + (-3)
   00000101  (+5)
 + 11111101  (-3 in two's complement)
 -----------
   00000010  (equals 2) ✓
```

The carry bit that overflows is simply discarded.

### **2. Single Zero Representation**

Unlike other methods, there's only one way to represent zero (00000000).

### **3. Simple Negation**

To negate any number (positive or negative), just apply two's complement again.

## **Quick Recognition Tips**

- **All 0s** = zero
- **Starts with 0** = positive
- **Starts with 1** = negative
- **All 1s** = -1
- **10000000** = most negative number (e.g., -128 in 8-bit)

This system is used in virtually all modern computers because it simplifies hardware design and arithmetic operations!
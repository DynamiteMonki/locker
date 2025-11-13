---
tags:
  - cs
from: AI
Date: 2025-11-01
---
---

- A data type is used to specify the type of data kept in an [[Variable]]

Some data types and what they hold:

### Primary Data Types in C

|Data Type|What it Stores|Example in Code|Common Size (Bytes)|
|---|---|---|---|
|**Integer Types (for whole numbers)**||||
|`int`|The "standard" whole number. Can be positive or negative.|`int score = 12500;`|4 bytes|
|`char`|A single character (letter, number, symbol) OR a very small integer.|`char grade = 'A';`|**Always 1 byte**|
|`short`|A whole number for when you know the value will be small. Saves memory.|`short temperature = -5;`|2 bytes|
|`long`|A whole number for when you need to store a very large value.|`long population = 7800000000L;`|4 or 8 bytes|
|`long long`|An even larger whole number for gigantic values.|`long long starsInGalaxy = 100000000000LL;`|8 bytes|
|**Floating-Point Types (for decimal numbers)**||||
|`float`|A number with a decimal point. Good for about 7 digits of precision.|`float price = 24.99f;`|4 bytes|
|`double`|A number with a decimal point that needs more precision. The "standard" decimal type.|`double pi = 3.1415926535;`|8 bytes|
|`long double`|An extra-large decimal number for maximum precision (rarely needed).|`long double veryPrecise = 3.1415...L;`|10, 12, or 16 bytes|
|**The "Nothing" Type**||||
|`void`|Represents the absence of a type. You can't declare a variable of this type.|`void printMessage(void);`|0 bytes|

---

### Modifiers: Changing the Behavior of Types

You can add keywords to the integer types to change their range. The most common one is `unsigned`.

|Modifier|What it Does|Example|Explanation|
|---|---|---|---|
|`unsigned`|Removes the negative range and adds it to the positive range.|`unsigned int age = 40;`|An `int` is normally about -2 billion to +2 billion. An `unsigned int` is **0 to +4 billion**. It can't be negative.|

Here's how `unsigned` affects the integer types:

| Data Type       | What it Stores                  | Common Size | Common Range         |
| --------------- | ------------------------------- | ----------- | -------------------- |
| `unsigned char` | A small positive whole number.  | 1 byte      | 0 to 255             |
| `unsigned int`  | A medium positive whole number. | 4 bytes     | 0 to ~4.2 billion    |
| `unsigned long` | A large positive whole number.  | 8 bytes     | 0 to ~18 quintillion |

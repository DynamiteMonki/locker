---
tags:
  - cs
  - cs50
from: AI
Date: 2025-10-31
---
---

# Escape sequence 

An **escape sequence** is a combination of characters that represents a special character or action **that cannot be typed directly** or has a non-printable meaning — like a newline, tab, or alert sound.

In C (and many other programming languages), escape sequences **start with a backslash (`\`)** followed by one or more characters.

They are used inside **character literals** (`' '`) and **string literals** (`" "`).

---

| Escape Sequence | Name              | What It Does / Represents                     |
| --------------- | ----------------- | --------------------------------------------- |
| `\n`            | Newline           | Moves cursor to next line                     |
| `\t`            | Horizontal tab    | Inserts a tab space                           |
| `\r`            | Carriage return   | Moves cursor to start of current line         |
| `\b`            | Backspace         | Moves cursor back one position                |
| `\f`            | Form feed         | Advances to next page (rarely used)           |
| `\\`            | Backslash         | Prints a literal `\`                          |
| `\"`            | Double quote      | Prints a literal `"` inside a string          |
| `\'`            | Single quote      | Prints a literal `'` inside a char            |
| `\?`            | Question mark     | Prints `?` (rarely needed)                    |
| `\a`            | Alert (bell)      | Makes a beep sound (if supported)             |
| `\v`            | Vertical tab      | Moves cursor down vertically (rare)           |
| `\0`            | Null character    | Represents end of string (ASCII 0)            |
| `\xhh`          | Hexadecimal value | Character from hex code (e.g. `\x41` = 'A')   |
| `\ooo`          | Octal value       | Character from octal code (e.g. `\101` = 'A') |

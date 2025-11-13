---
tags:
  - cs
  - cs50
from: AI
Date: 2025-10-31
---
---

- Strings are to me manipulated this is commonly done by using format specifiers in C along with the `printf` function.
- These act as a place holder.

An, example is:

```c
#include <stdio.h>

int main(void) {
	int x = 90;
	printf("Hello, %d\n", x);
	return 0;
	// output Hello, 90
}
```

---

# Some specifier

| Specifier   | Meaning                                    | Used for            | Example (`printf`)                            |
| ----------- | ------------------------------------------ | ------------------- | --------------------------------------------- |
| `%d`        | Signed decimal integer                     | `int`               | `printf("%d", 42);` → `42`                    |
| `%i`        | Same as `%d` (in `printf`)                 | `int`               |                                               |
| `%u`        | Unsigned decimal integer                   | `unsigned int`      | `printf("%u", -1);` → big number (wraparound) |
| `%f`        | Floating-point (decimal notation)          | `float`, `double`   | `printf("%f", 3.14);` → `3.140000`            |
| `%e` / `%E` | Scientific notation (lower/upper case 'e') | `float`, `double`   | `printf("%e", 123.456);` → `1.234560e+02`     |
| `%g` / `%G` | Auto-choose `%f` or `%e` (shorter)         | `float`, `double`   | `printf("%g", 123.456);` → `123.456`          |
| `%c`        | Single character                           | `char`              | `printf("%c", 'A');` → `A`                    |
| `%s`        | String                                     | `char[]` or `char*` | `printf("%s", "Hello");` → `Hello`            |
| `%p`        | Pointer address                            | pointer variables   | `printf("%p", &var);` → e.g. `0x7ffd42a`      |
| `%%`        | Literal percent sign                       | —                   | `printf("%%");` → `%`                         |

---

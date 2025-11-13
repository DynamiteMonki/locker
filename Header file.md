---
tags:
  - cs
  - headerfiles
from: AI
Date: 2025-10-31
---
# What is an header file ?

An header file is used to define some things, that may be functions, variables or constants. 

---

# How to make a header file ?

A header file should have a accompying `.c` file with the same name as it to implement the definations written in the `.h` file.

That is a foo.h will hold some definations that will be implemented in `foo.c` file 

---

# How to compile with your header files ?

You can pass the file which implements the header file's definations 

for example:

```bash
gcc src/main.c lib/main.c -o bin/main
```


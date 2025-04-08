## Hydro — A Simple C-Like Compiler
Hydro is a small, self-hosted compiler written in C++.
It compiles a simple C-like programming language to x86-64 NASM assembly targeting Linux (using the syscall ABI).

## Features
Lexer (Tokenizer)

Recursive Descent Parser

AST Generation

x86-64 Code Generation (NASM Syntax)

Supports:

Integer Arithmetic

Variables

If/Else

Exit Statements

Outputs .asm assembly file

Targets Linux x86-64 ABI (syscalls)


## PROJECT STRUCTURE
hydro/
├── src/
│   ├── main.cpp        # Entry point
│   ├── lexer.cpp       # Tokenizer
│   ├── parser.cpp      # Recursive descent parser
│   ├── codegen.cpp     # x86-64 NASM codegen
│   └── util.cpp        # Helpers (e.g., read_file)
├── include/            # Header files
├── test/               # Sample programs
├── Makefile
└── README.md


## Building

Requires `nasm` and `ld` on a Linux operating system.

```bash
git clone https://github.com/orosmatthew/hydrogen-cpp
cd 'CD-Assigment'
mkdir build
cd build
cmake ..
make
./hydro ../test.hy
nasm -f elf64 out.asm -o out.o
ld out.o -o out
./out
echo $?
```

Executable will be `hydro` in the `build/` directory.



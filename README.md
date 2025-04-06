

## Building

Requires `nasm` and `ld` on a Linux operating system.

```bash
git clone https://github.com/orosmatthew/hydrogen-cpp
cd compiler-design-assigment
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



# Shellcoding

## Creating Shellcode

1. Write assembly code \[[Linux syscall table](https://chromium.googlesource.com/chromiumos/docs/+/master/constants/syscalls.md)\].
2. Assemble: `nasm -f elf shellcode.asm`
3. Link: `ld -o shellcode shellcode.o`
4. Extract opcodes: `objdump -d shellcode`

## Relative Shellcoding

To make the shellcode more portable we don't want to rely on hardcoded values. To do so we want to hold a meaningful address in a register and work relative to it.

Here is an example of such a technique:

![](../.gitbook/assets/image%20%281%29.png)

We use `call` to push the next address to the stack and jump to our shellcode. That address is then put into `esi` and thus we can use `esi` for relative addressing. To get to `call` we place a `jmp` at the very start of the shellcode.


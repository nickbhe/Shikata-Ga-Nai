# Debuggers

## GDB

#### Load file into gdb

start gdb with the file

```text
gdb <FILE NAME>
```

or load it within gdb

```text
file <FILE NAME>
```

#### Quit

**q**. As simple as that.

### Info

**i** is an abbreviation for **info**.

#### List functions

```text
i functions
```

#### List breakpoints

```text
i b
```

#### List registers

```text
i registers
```

### Breakpoints

**b** is an abbreviation for **break**.

#### Break by address

```text
b *<ADDRESS>
```

instead of the address, a symbol can be used \[like functions name\]. 

#### Break by line number

```text
b <FILE NAME>:<LINENUM>
```

if filename is not specified the current one is used.

#### Break by offset

```text
b <+/-><OFFSET>
```

### Execution flow

#### Running

* Use **r** to run the binary.
* Use **c** to continue the execution.
* Use **finish** to continue until the current stack frame returns.

#### Stepping

* Use **s** \[abbreviation of step\] to execute a line of source code.
* Use **si** \[abbreviation of stepi\] to step into the next machine instruction.
* Use **ni** \[abbreviation of nexti\] to step into the next machine instruction \[step over function calls\].

### Examine Memory

**x** is an abbreviation for **examine**.

the command structure is **x/nfu &lt;ADDRESS&gt;**:

* **n** - Integer indicating how much memory to examine.
* **f** - Display format
* **u** - unit size 

**Example 1** - Examine 32 words in hexadecimal form, starting at EIP's value

```text
x/32xw $eip
```

**Example 2** - Examine the first 5 instructions of the function "func"

```text
x/5i *func
```


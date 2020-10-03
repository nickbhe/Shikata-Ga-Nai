# Examining Binaries

### What is this file?

run the `file` command!

Check what kind of security features are enabled

#### Checksec

Check the properties of a binary with [Checksec](https://github.com/slimm609/checksec.sh).

Output example from their repo:

![](../.gitbook/assets/image.png)

#### Hardening Check

Check binaries for security hardening features. I find it less reliable when it comes to RELRO.

Included in the **devscripts** package on debian-based distros.

#### gef - checksec

[gef](https://github.com/hugsy/gef) has a pretty neat `checksec` command.

### Let's dump stuff!

* `strings <FILE>` - look for any readable clue.
* `objdump -x <FILE> | less` - Information about the file, headers, sections and more. pipe for easy reading.
* `strace <FILE>` - examine syscalls in the binary.
* `ltrace <FILE>` - examine library calls in the binary.


# Linux Tricks

## Print by Hexadecimal Representation

### xxd

xxd is built-in Linux. create a file with hex representation. For example:

```text
 echo "00: 68 65 6c 6c 6f" > xxd_hex
```

convert to raw bites with xxd:

```text
xxd -r xxd_hex
```

### printf

```text
printf "\x68\x65\x6c\x6c\x6f"
```

### echo

```text
echo $'\x68\x65\x6c\x6c\x6f'
```

### python3

python3 \[or python\] may not exist on the machine.

```text
python3 -c "print('\x68\x65\x6c\x6c\x6f')"
```

If you don't want unreadable characters to be interpreted as UTF-8 with python3 use this instead:

```text
python3 -c "import sys; sys.stdout.buffer.write(b'\xca\xfe\xba\xbe\n')"
```

## Other

#### http server with python

```text
python3 -m http.server
```


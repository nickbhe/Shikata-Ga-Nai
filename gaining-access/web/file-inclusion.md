# File Inclusion

Local file inclusion \[LFI\] vulnerabilities allow the attacker to access files on the web-server. 

Remote file inclusion \[RFI\] vulnerabilities allow the attacker to access files on a remote machine through the web-server. This vulnerability is not as common as LFI, but easier to exploit.

If a file is writable and readable you can create yourself a web shell.  **log files** are a good target for this.

PHP comes with [built-in wrappers](https://www.php.net/manual/en/wrappers.php).


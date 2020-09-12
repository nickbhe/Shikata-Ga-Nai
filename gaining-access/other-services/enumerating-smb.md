# Enumerating SMB

The SMB \(Server Message Block\) had a poor security track over the years. It has services running on ports 445 or 139. Our initial **nmap** scan will probably find the SMB service.

## Tools

**nbtscan**  has the ability to scan entire subnets for SMB shares.

**smbclient** can interact with a SMB service. use "-L \\\\&lt;IP&gt;\\" for anonymous login.

**SMBMap** allows enumerating shares across an entire domain. Supposed to be easy to use with pentesting in mind.

**enum4linux** \[[cheatsheet](https://highon.coffee/blog/enum4linux-cheat-sheet/)\].

**metasploit** auxiliary/scanner/smb/smb\_version.


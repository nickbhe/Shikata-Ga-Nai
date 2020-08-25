# Nmap

My very best friend.

Nmap has many useful flags, it's best to know as many of them and use Nmap according to the environment. Find your balance between speed and intrusiveness.

After an initial scan it is recommended to run additional scans in the background. Scan for greater port range \[**-p-** for all ports\] or \[-sU\] for UDP ports.

## Templates

These are just examples! Combine them to gain the best results.

### \#1 - Ippsec's Default

used in HackTheBox by Ippsec and has proven itself to be pretty useful.

```text
nmap -sC -sV -oA <PathForResults> <IP>
```

> -Sc Performs a script scan using the default set of scripts... Some of the scripts in this category are considered intrusive and should not be run against a target network without permission.

> -sV Enables version detection.

> -oA Output in the three major formats at once. \[normal, XML, grepable\].

### \#2 - Manpage example 1

```text
nmap -A -T4 <IP>
```

> -A Enables additional advanced and aggressice options. Presently this enables OS detection \(**-O**\), version scanning \(**-sV**\), script scanning \(**-sC**\) and traceroute \(**--traceroute**\)... because script scanning with the default set is considered intrusive, you **should not use -A against target networks without permission**.

> -T Set a timing template.... The template names are **paranoid** \(**0**\), **sneaky** \(**1**\), **polite** \(**2**\), **normal** \(**3**\), **aggressive** \(**4**\), and **insane** \(**5**\)... If you are on a decent broadband or ethernet connection, I would recommend always using **-T4**.


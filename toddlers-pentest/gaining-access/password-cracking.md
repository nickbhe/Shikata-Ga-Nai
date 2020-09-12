# Password Cracking

Look for **default credentials** to the program you are trying to breach.

## Wordlist Generation

#### Cewl

A crawler that gathers words that can be used for password cracking. Example usage:

```text
cewl <URL> -m 8 -w <OUTPUT_FILE>
```

> **-m** Minimum word length, default 3.

## Crackers

### Hydra

> A very fast network logon cracker which supports many different services.

#### Cracking web-forms

```text
hydra -L <User List> -P <Password List> <IP> http-post-form "<Path to Page>:<Username Field>=^USER^&<Password Field>=^PASS^:<Failure Message>"
```

### Online Hash Crackers

* [CrackStation](https://crackstation.net/)




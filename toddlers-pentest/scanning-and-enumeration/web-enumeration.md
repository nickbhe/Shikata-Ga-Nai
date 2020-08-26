# Web Enumeration

## Vectors

Firstly interact with the website and ask yourself:

* What language is the app written in?
* what server software is the application running on?
* What does the application do?
* What is the technology stack?
* etc.

The browser's dev tools can help \[also, the [Wappalyzer](https://www.wappalyzer.com/) extension can help recognize technologies\].

Look for a sitemap like **robots.txt** and **sitemap.xml**.

Some sites ship with remote administration web applications, for example /manager/html \[Tomcat\] and /phpmyadmin \[MySQL\]. **Try to log in with default creds**.

## Tools

### Nikto

A good scanning tool for catching low hanging fruit. **Very noisy!**

### **Gobuster**

Directory \[and DNS\] busting. Rumored to be stabler and faster than **dirbuster** and **dirb**. Usage example:

```text
gobuster dir -u <URL> -w <wordlist> -c <cookies> -x <file extentions>
```


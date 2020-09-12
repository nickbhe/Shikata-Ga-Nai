# Privesc

## Manual Privesc

### Identify myself

* **whoami**
* Linux, **id**: will provide additional info about the user

### Find info about other users

* Linux, **cat /etc/passwd**

### Info about the host

* **hostname**
* Linux, **cat /etc/issue**, **cat /etc/release**, **release -a**

### Running processes

* Linux, **ps** &lt;Flag&gt; \[for example -xau: all processes, readble\]

### Networking Information

* Linux, **ip a**
* Linux, **/sbin/route** \[or **/sbin/routel**\]: display routing tables
* Linux, **netstat** \[or **ss**\] **-anp**: list connections

### Firewall status and rules

* Linux, try and peek the configuration. For example **grep -Hs iptables /etc/\***

...


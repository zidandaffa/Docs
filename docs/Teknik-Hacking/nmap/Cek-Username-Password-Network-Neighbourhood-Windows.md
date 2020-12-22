## Nmap: cek username password network neighbourhood windows
Lakukan
```
nmap --script smb-enum-users.nse -p445 <host>
sudo nmap -sU -sS --script smb-enum-users.nse -p U:137,T:139 <host>
```

## Referensi
http://nmap.org/nsedoc/scripts/smb-enum-users.html
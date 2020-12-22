# Nmap: Cek SQL Injection
Untuk mencek apakah sebuah situs dapat di serang menggunakan SQL Injection. Kita dapat menggunakan nmap
```
nmap -sV --script=http-sql-injection <target>
```

## Referensi
* http://nmap.org/nsedoc/scripts/http-sql-injection.html
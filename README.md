# Cheat sheet para pruebas de penetración
## Reconocimiento
### Nmap
```bash
nmap <IP> -sS -p- -sCV
```
### Go buster
#### Directorios
```bash
gobuster dir -u http://<IP> -w /usr/share/wordlists/SecLists/Discovery/Web-Content/directory-list-2.3-big.txt -x html,php,xml,json,txt,sh,git -r
```
#### Virtual host (subdominios)
```bash
gobuster vhost --apend-domain -u http://<Dominio> -w /home/kali/SecList/Discovery/DNS/subdomain-top1million-110000.txt -r <IP>
```
### Fuzzing
```bash
wfuzz -c -w /usr/share/wordlist/SecList/Dicovery/... 'http://<IP>/index.php?FUZZ=../../../../etc/passwd'
```
### SMB
##### Enumeración
```bash
enum4linux -a <IP>
```
##### Listado con sesión nula
```bash
smbclient -L //<IP>/ -N
```
##### SMBmap
```bash
smbmap -H <IP>
```
##### Acceso con credenciales
```bash
smbclient -L //<IP> -U <user>
```
##### Sesión nula
```bash
smbclient //<IP>/directorio -N 
```


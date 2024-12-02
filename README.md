# PTpoc
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

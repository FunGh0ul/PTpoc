# PTpoc
## Reconocimiento
### Nmap
```bash
nmap <IP> -sS -p- -sCV
```
### Go buster
```bash
gobuster dir -u http://<IP> -w /usr/share/wordlists/SecLists/Discovery/Web-Content/directory-list-2.3-big.txt -x html,php,xml,json,txt,sh,git -r
```

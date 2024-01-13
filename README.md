# top-sites-security.txt

1- Donwload top 1000000 domains from here https://radar.cloudflare.com/domains
2- Check `security.txt` and `.well-known/security.txt` for main domain

```
cat domains | httpx -path paths -mc 200 -cl -ct -o result1
```
```
cat domains | while read d; do echo "www.$d"; done | httpx -path paths -mc 200 -cl -ct -o result2 
```

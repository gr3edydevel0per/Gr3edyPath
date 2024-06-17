

## Fuzzing word lists 

-ic ignore comments from wordlists

**Apache Directory** 
- /home/greedydev/wordlists/SecLists/Discovery/Web-Content/apache.txt

**Api**
- /home/greedydev/wordlists/SecLists/Discovery/Web-Content/api/

**PHP files**
- /home/greedydev/wordlists/SecLists/Discovery/Web-Content/Common-PHP-Filenames.txt

**Directory List**
- /home/greedydev/wordlists/SecLists/Discovery/Web-Content/
- /home/greedydev/wordlists/SecLists/Discovery/Web-Content/raft-large-files

Extensions List
- /home/greedydev/wordlists/SecLists/Discovery/Web-Content/raft-large-extensions.txt
- Web extensions
	- /home/greedydev/wordlists/SecLists/Discovery/Web-Content/web-extensions.txt

Sub domains 

ffuf -u http://FUZZ.mydomain.com -c -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt -fs 0

For virtual host
- $ ffuf -u http://mydomain.com -c -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt -H 'Host: FUZZ.mydomain.com' -fs 0

`/usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt`

`/usr/share/seclists/Discovery/Web-Content/raft-medium-files-lowercase.txt`


ffuf -u http://FUZZ.creative.thm -c -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt  -fs 0

 ffuf -u http://creative.thm -c -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt -H 'Host: FUZZ.creative.thm'   -fs 0
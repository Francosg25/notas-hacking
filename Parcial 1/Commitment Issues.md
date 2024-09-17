## Objetivo

I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/139/challenge.zip)
## Solución
```
(kali㉿Franco)-:~$ ls
README.txt  challenge.zip
(kali㉿Franco)-:~$ unzip challenge.zip
...
(kali㉿Franco)-:~$ ls
README.txt  challenge.zip  drop-in
(kali㉿Franco)-:~$ cd drop-in/
(kali㉿Franco)-:~/drop-in$ ls -la
total 8
drwxr-xr-x 3 (kali㉿Franco)-   37 Mar 12  2024 .
drwxr-xr-x 5 (kali㉿Franco)- 4096 Sep 11 18:35 ..
drwxr-xr-x 8 (kali㉿Franco)- 166 Mar 12  2024 .git
-rw-r--r-- 1 (kali㉿Franco)-   11 Mar 12  2024 message.txt
(kali㉿Franco)-:~/drop-in$ cat message.txt 
TOP SECRET
(kali㉿Franco)-:~/drop-in$ git log
(kali㉿Franco)-~/drop-in$ git show 144fdc44b09058d7ea7f224121dfa5babadddbb9
commit 144fdc44b09058d7ea7f224121dfa5babadddbb9 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:25 2024 +0000

    remove sensitive info

diff --git a/message.txt b/message.txt
index 3a71673..d552d1e 100644
--- a/message.txt
+++ b/message.txt
@@ -1 +1 @@
-picoCTF{s@n1t1z3_be3dd3da}
+TOP SECRET
```

## Notas adicionales

## Referencias
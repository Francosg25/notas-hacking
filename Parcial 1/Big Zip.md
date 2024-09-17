## Objetivo
Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/504/big-zip-files.zip) 
## Solución
```
**┌──(kali㉿Franco)-[~]
└─$ cd hacking/PARCIAL\ 1/Big\ Zip/                     
                                                                             
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/Big Zip]
└─$ grep -r big-zip-files -e pico
                                                                             
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/Big Zip]
└─$ ls -la
total 3200
drwxrwx--- 1 root vboxsf    4096 Sep 15 21:26  .
drwxrwx--- 1 root vboxsf    4096 Sep 15 21:27  ..
drwxrwx--- 1 root vboxsf   81920 May  3  2020  big-zip-files
-rwxrwx--- 1 root vboxsf 3182988 Sep 11 12:31  big-zip-files.zip
-rwxrwx--- 1 root vboxsf       0 Sep 15 21:25 'Big Zip.md'
                                                                             
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/Big Zip]
└─$ cd big-zip-files/folder_       
cd: no such file or directory: big-zip-files/folder_
                                                                             
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/Big Zip]
└─$ cd big-zip-files        
                                                                             
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/Big Zip/big-zip-files]
└─$ grep -r pico       **

big-zip files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
```

## Notas adicionales

## Referencias
## Objetivo

Can you read files in the root file?

Additional details will be available after launching your challenge instance.

## Solución
```
┌──(kali㉿Franco)-[~]
└─$ cd hacking/PARCIAL\ 1            
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1]
└─$ ssh -p 50133 picoplayer@saturn.picoctf.net
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Tue Sep 17 05:01:23 2024 from 177.124.85.13
picoplayer@challenge:~$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1]
└─$ sudo vi test                              
[sudo] password for kali: 

ls: cannot access 'al': No such file or directory

shell returned 2

Press ENTER or type command to continue
ls: cannot access 'la': No such file or directory

shell returned 2
```
## Notas adicionales

## Referencias
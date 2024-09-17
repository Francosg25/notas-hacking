## Objetivo
Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/502/files.zip)

## Solución     
```
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1]
└─$ cd First\ Find 
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/First Find]
└─$ unzip files.zip    
Archive:  files.zip
   creating: files/
   creating: files/satisfactory_books/
   creating: files/satisfactory_books/more_books/
  inflating: files/satisfactory_books/more_books/37121.txt.utf-8  
  inflating: files/satisfactory_books/23765.txt.utf-8  
  inflating: files/satisfactory_books/16021.txt.utf-8  
  inflating: files/13771.txt.utf-8   
   creating: files/adequate_books/
   creating: files/adequate_books/more_books/
   creating: files/adequate_books/more_books/.secret/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
 extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt  
  inflating: files/adequate_books/more_books/1023.txt.utf-8  
  inflating: files/adequate_books/46804-0.txt  
  inflating: files/adequate_books/44578.txt.utf-8  
   creating: files/acceptable_books/
   creating: files/acceptable_books/more_books/
  inflating: files/acceptable_books/more_books/40723.txt.utf-8  
  inflating: files/acceptable_books/17880.txt.utf-8  
  inflating: files/acceptable_books/17879.txt.utf-8  
  inflating: files/14789.txt.utf-8   
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/First Find]
└─$ file files
files: directory
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/First Find]
└─$ ls
files  files.zip
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/First Find]
└─$ find files/ -name "uber-secret.txt"
files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/First Find]
└─$ cd files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
                                                                                                
┌──(kali㉿Franco)-[~/…/more_books/.secret/deeper_secrets/deepest_secrets]
└─$ ls
uber-secret.txt
                                                                                                
┌──(kali㉿Franco)-[~/…/more_books/.secret/deeper_secrets/deepest_secrets]
└─$ cat uber-secret.txt                                                       
picoCTF{f1nd_15_f457_ab443fd1}
```
## Notas adicionales

## Referencias
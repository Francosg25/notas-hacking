## Objetivo
You will find the flag after analysing this apk Download [here](https://artifacts.picoctf.net/c/449/timer.apk).
## Solución
```
┌──(kali㉿Franco)-[~/picoCTF/reversing/timer]
└─$ ls
timer.apk

┌──(kali㉿Franco)-[~/picoCTF/reversing/timer]
└─$ file timer.apk       
timer.apk: Android package (APK), with zipflinger virtual entry, with APK Signing Block

┌──(kali㉿Franco)-[~/picoCTF/reversing/timer]
└─$ exiftool timer.apk 
ExifTool Version Number         : 12.76
File Name                       : timer.apk
Directory                       : .
File Size                       : 4.7 MB
File Modification Date/Time     : 2023:03:15 21:16:09-06:00
File Access Date/Time           : 2024:10:30 10:36:27-06:00
File Inode Change Date/Time     : 2024:10:30 10:36:20-06:00
File Permissions                : -rw-rw-r--
File Type                       : ZIP
File Type Extension             : zip
MIME Type                       : application/zip
Zip Required Version            : 0
Zip Bit Flag                    : 0
Zip Compression                 : Deflated
Zip Modify Date                 : 1981:01:01 01:01:02
Zip CRC                         : 0xdfb66760
Zip Compressed Size             : 51
Zip Uncompressed Size           : 56
Zip File Name                   : META-INF/com/android/build/gradle/app-metadata.properties
Warning                         : [minor] Use the Duplicates option to extract tags for all 751 files
```

```
┌──(kali㉿Franco)-[~/picoCTF/reversing/timer]
└─$ unzip timer.apk                        
...    

┌──(kali㉿Franco)-[~/picoCTF/reversing/timer]
└─$ ls                                  
AndroidManifest.xml  META-INF  classes.dex  classes2.dex  classes3.dex  kotlin  res  resources.arsc  timer.apk

┌──(kali㉿Franco)-[~/picoCTF/reversing/timer]
└─$ grep -R picoCTF                     
grep: classes3.dex: binary file matches
```

```
┌──(kali㉿Franco)-[~/picoCTF/reversing/timer]
└─$ find . -name classes3.dex 
./classes3.dex

┌──(kali㉿Franco)-[~/picoCTF/reversing/timer]
└─$ strings classes3.dex | grep pico    
picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}
```
## Notas adicionales

## Referencias
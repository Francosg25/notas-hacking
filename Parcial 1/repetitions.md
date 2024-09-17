## Objetivo

Can you make sense of this file? Download the file [here](https://artifacts.picoctf.net/c/477/enc_flag).
## Solución
```
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/repetitions]
└─$ ls
enc_flag
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/repetitions]
└─$ cat enc_flag       
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbHBWV0VKVVZGWmFWMDVHV2tkYVNHUlZDazFyY0ZkVWJGWlhZVlpLU0dWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/repetitions]
└─$ base64 -d enc_flag
VjFSQ2EyTXlSblJUV0dSVllrWmFWRmx0TlZOalJtUlhZVVU1YVZKVVZuaFdWekZoWVZkR2NrNVVX
bUZTVmtwUVdWUkdibVZXVm5WUgpiSEJzWVRCd2VWVXhXbXBOUlRWSFdqTnNWZ3BYUjFKeVZGZHdW
MlZzVWxaVmJFNW9UVVJDTlZaWE1XRlpVWEJUVFZaV05GWkdaSGRVCk1rcFdUbFZXYVZKSGVFVlhi
bTkzVDFWT2JsQlVNRXNLCg==
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/repetitions]
└─$ base64 -d enc_flag | base64 -d
V1RCa2MyRnRTWGRVYkZaVFltNVNjRmRXYUU5aVJUVnhWVzFhYVdGck5UWmFSVkpQWVRGbmVWVnVR
bHBsYTBweVUxWmpNRTVHWjNsVgpXR1JyVFdwV2VsUlZVbE5oTURCNVZXMWFZUXBTTVZWNFZGZHdU
MkpWTlVWaVJHeEVXbm93T1VOblBUMEsK
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/repetitions]
└─$ base64 -d enc_flag | base64 -d | base64 -d
WTBkc2FtSXdUbFZTYm5ScFdWaE9iRTVxVW1aaWFrNTZaRVJPYTFneVVuQlpla0pyU1ZjME5GZ3lV
WGRrTWpWelRVUlNhMDB5VW1aYQpSMVV4VFdwT2JVNUViRGxEWnowOUNnPT0K
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/repetitions]
└─$ base64 -d enc_flag | base64 -d | base64 -d | base64 -d
Y0dsamIwTlVSbnRpWVhObE5qUmZiak56ZEROa1gyUnBZekJrSVc0NFgyUXdkMjVzTURSa00yUmZa
R1UxTWpObU5EbDlDZz09Cg==
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/repetitions]
└─$ base64 -d enc_flag | base64 -d | base64 -d | base64 -d | base64 -d
cGljb0NURntiYXNlNjRfbjNzdDNkX2RpYzBkIW44X2Qwd25sMDRkM2RfZGU1MjNmNDl9Cg==
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/repetitions]
└─$ base64 -d enc_flag | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_de523f49}
```                     
## Notas adicionales

## Referencias
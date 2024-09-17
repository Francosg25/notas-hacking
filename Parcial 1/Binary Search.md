## Objetivo
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/6/challenge.zip)

Additional details will be available after launching your challenge instance.
## Solución
```
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/Binary Search]
└─$ ssh -p 54800 ctf-player@atlas.picoctf.net   
The authenticity of host '[atlas.picoctf.net]:54800 ([18.217.83.136]:54800)' can't be established.
ED25519 key fingerprint is SHA256:M8hXanE8l/Yzfs8iuxNsuFL4vCzCKEIlM/3hpO13tfQ.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:54800' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 800
Higher! Try again.
Enter your guess: 900
Higher! Try again.
Enter your guess: 950
Higher! Try again.
Enter your guess: 999
Lower! Try again.
Enter your guess: 990
Lower! Try again.
Enter your guess: 970
Lower! Try again.
Enter your guess: 960
Lower! Try again.
Enter your guess: 955
Lower! Try again.
Enter your guess: 953
Lower! Try again.
Enter your guess: 952
Congratulations! You guessed the correct number: 952
Here's your flag: picoCTF{g00d_gu355_de9570b0}
Connection to atlas.picoctf.net closed.
```
## Notas adicionales

## Referencias
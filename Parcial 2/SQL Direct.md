## Objetivo
Connect to this PostgreSQL server and find the flag!

Additional details will be available after launching your challenge instance.
## Solución
```
┌──(kali㉿Franco)-[~/picoCTF/crypto2/miniRSA]
└─$ psql -h saturn.picoctf.net -p 52898 -U postgres pico  
Password for user postgres: 
psql (16.3 (Debian 16.3-1), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

```

## Notas adicionales

## Referencias
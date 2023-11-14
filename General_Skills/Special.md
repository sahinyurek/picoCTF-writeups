<img width="611" alt="Special_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/679e8d2b-3eb4-4a73-93d5-ff63ccb46f1f">

After a lot of trying I've found using four quotes before the command does work to run commands. Then I found a directory but couldn't cd to it so I used cat * to read everything.

```shell
┌──(xodzk㉿kali)-[~]
└─$ ssh -p 63887 ctf-player@saturn.picoctf.net

Special$ ""pwd
""pwd 
/home/ctf-player
Special$ """"ls
""""ls 
blargh
Special$ """"cd" "blargh        
""""cd" "blargh 
sh: 1: cd blargh: not found
Special$ """"cat *
""""cat * 
cat: blargh: Is a directory
Special$ """"cat blargh/*
""""cat blargh/* 
picoCTF{5p311ch3ck_15_7h3_w0r57_a60bdf40}
```



<img width="610" alt="Glitch_Cat_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/e2fec8da-1e48-4bc5-be28-9f0113213176">

We receive some characters as ASCII in python syntax so I just put it in print() function and got the flag.

```shell
┌──(xodzk㉿kali)-[~]
└─$ nc saturn.picoctf.net 52682
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'

┌──(xodzk㉿kali)-[~]
└─$ python3       
Python 3.11.4 (main, Jun  7 2023, 10:13:09) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print('picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}')
picoCTF{gl17ch_m3_n07_bda68f75}           
```

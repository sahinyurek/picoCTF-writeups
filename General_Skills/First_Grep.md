
<img width="616" alt="First_Grep_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/fa092729-f4f9-4077-9c7e-eb926670cd08">



Retrieve the file using wget.

```bash
┌──(xodzk㉿kali)-[~]
└─$ wget https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file
--2023-10-20 18:01:28--  https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14551 (14K) [application/octet-stream]
Saving to: ‘file’

file                                                       100%[========================================================================================================================================>]  14.21K  --.-KB/s    in 0s      

2023-10-20 18:01:30 (103 MB/s) - ‘file’ saved [14551/14551]
```

Check what it is.

```bash
┌──(xodzk㉿kali)-[~]
└─$ file file
file: ASCII text, with very long lines (4200)
```

Search for the flag using grep.

```bash
┌──(xodzk㉿kali)-[~]
└─$ grep picoCTF file
picoCTF{grep_is_good_to_find_things_5af9d829}
```

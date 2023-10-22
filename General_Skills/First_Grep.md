
<img width="616" alt="First_Grep_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/fa092729-f4f9-4077-9c7e-eb926670cd08">




Check what the file is.

```shell
┌──(xodzk㉿kali)-[~]
└─$ file file
file: ASCII text, with very long lines (4200)
```

Search for the flag using grep.

```shell
┌──(xodzk㉿kali)-[~]
└─$ grep picoCTF file
picoCTF{grep_is_good_to_find_things_5af9d829}
```

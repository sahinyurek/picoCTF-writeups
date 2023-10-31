

<img width="607" alt="fixme2 py_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/7606a372-034a-4b1f-9031-0e36905e629c">


Run it once to get the error message.

```shell
┌──(xodzk㉿kali)-[~]
└─$ python3 fixme2.py 
  File "/home/xodzk/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?

┌──(xodzk㉿kali)-[~]
└─$ nano fixme2.py
```

<img width="1239" alt="fixme2 py_1" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/7ff65d99-fdfe-4272-bf55-9561d28cc8c7">

Add one more equals sign after if to make it a comparison.

```shell
┌──(xodzk㉿kali)-[~]
└─$ python3 fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}
```

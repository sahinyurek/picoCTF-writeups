

<img width="610" alt="fixme1 py_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/3342bb58-30a3-4695-8cff-5bd483d27550">



Run it once to get the error message.

```shell
┌──(xodzk㉿kali)-[~]
└─$ python3 fixme1.py 
  File "/home/xodzk/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
```

nano fixme1.py to remove the indentation before print then save.

<img width="1198" alt="fixme_1" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/eedba36b-dd14-4f32-a489-bbd93d809ba3">


Run again to get the flag.

```shell
┌──(xodzk㉿kali)-[~]
└─$ python3 fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}
```

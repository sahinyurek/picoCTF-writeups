

<img width="609" alt="HashingJobApp_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/ac1b722d-f210-4b3b-9040-c8d2f72769d0">


I used md5sum in another shell. Reconnecting causes the string to change.

```shell
┌──(xodzk㉿kali)-[~]
└─$ nc saturn.picoctf.net 53638
Please md5 hash the text between quotes, excluding the quotes: 'UV rays'
Answer: 
fa572056bc7677e6104801f2773fcc76
fa572056bc7677e6104801f2773fcc76                                                                                    
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'a cheap motel'
Answer: 
d51908671c7603ec46c7379887509894
d51908671c7603ec46c7379887509894
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'homeless shelters'
Answer: 
ed96f5bcf2cb76f423a92190358b6881
ed96f5bcf2cb76f423a92190358b6881
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}

```

Using md5sum without arguments to give the input directly from the shell. Press Ctrl + D twice to mark the end of file.

```shell
┌──(xodzk㉿kali)-[~]
└─$ md5sum
UV raysfa572056bc7677e6104801f2773fcc76  -
                                                                                                                    
┌──(xodzk㉿kali)-[~]
└─$ md5sum
a cheap moteld51908671c7603ec46c7379887509894  -
                                                                                                                    
┌──(xodzk㉿kali)-[~]
└─$ md5sum
homeless sheltersed96f5bcf2cb76f423a92190358b6881  -
```

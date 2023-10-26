
<img width="610" alt="Python_Wrangling_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/dec7bd44-f05e-4897-a077-03f514ed591d">

We can see how to use the python script when we try to run it without any arguments. Then I figured -e is encryption and -d is decryption and got the flag using the given password and encrypted file.

```shell
┌──(xodzk㉿kali)-[~]
└─$ python3 ende.py        
Usage: ende.py (-e/-d) [file]

┌──(xodzk㉿kali)-[~]
└─$ cat pw.txt               
68f88f9368f88f9368f88f9368f88f93
                                                                                                                                                                                                                                    
┌──(xodzk㉿kali)-[~]
└─$ python3 ende.py -d flag.txt.en           
Please enter the password:68f88f9368f88f9368f88f9368f88f93
picoCTF{4p0110_1n_7h3_h0us3_68f88f93}
               
```

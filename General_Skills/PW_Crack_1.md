

<img width="606" alt="PW_Crack_1_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/0d4b2c92-2fd4-4482-adae-7aa74f34cc06">

The password checker asks for a password.

```shell
┌──(xodzk㉿kali)-[~]
└─$ python3 level1.py 
Please enter correct password for flag: 
```

We look at what is in python code to find out how the check is actually made.
We can see it is 691d here 
```python
if( user_pw == "691d"):
```

```shell
┌──(xodzk㉿kali)-[~]
└─$ cat level1.py
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################


flag_enc = open('level1.flag.txt.enc', 'rb').read()



def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "691d"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_1_pw_check()
                                                                                                                    
┌──(xodzk㉿kali)-[~]
└─$ python3 level1.py
Please enter correct password for flag: 691d
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_56891419}
```

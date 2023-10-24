<img width="619" alt="Wave_A_Flag_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/81d80922-b2a4-445b-8c0d-3a03e4e78259">


Check what the file is

```shell
┌──(xodzk㉿kali)-[~]
└─$ file warm                      
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=7b3da2efd83a2b9154697b6c7f6474042e1fd033, with debug_info, not stripped
```

Make it executable and run it

```shell
┌──(xodzk㉿kali)-[~]
└─$ chmod +x warm

┌──(xodzk㉿kali)-[~]
└─$ ./warm
Hello user! Pass me a -h to learn what I can do!
                                                                                                                                                                                                                                     
┌──(xodzk㉿kali)-[~]
└─$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}
```

# Unintended Solution

You can see the strings in a binary file using strings command. Use grep with pipe to grab the flag.

```shell                                                                                                                                                                                                                                     
┌──(xodzk㉿kali)-[~]
└─$ strings warm | grep picoCTF
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}
```

# Notes
You might not be able to execute the file if you are on an arm build.

See here: [Running x86 code on ARM devices](https://www.kali.org/docs/arm/x86-on-arm/)

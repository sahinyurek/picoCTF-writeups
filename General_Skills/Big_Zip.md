<img width="610" alt="Big_Zip_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/591d6e20-25d5-4c30-98c7-902132ee239f">


Unzip.

```shell

┌──(xodzk㉿kali)-[~]
└─$ unzip big-zip-files.zip 
Archive:  big-zip-files.zip
creating: big-zip-files/
...

```

Has many files so use grep -r to search everything.

```shell
┌──(xodzk㉿kali)-[~/big-zip-files]
└─$ grep -r pico
folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}

```

<img width="610" alt="Big_Zip_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/591d6e20-25d5-4c30-98c7-902132ee239f">


Retrieve the zip file and unzip.

```shell
┌──(xodzk㉿kali)-[~]
└─$ wget https://artifacts.picoctf.net/c/504/big-zip-files.zip
--2023-10-20 18:21:15--  https://artifacts.picoctf.net/c/504/big-zip-files.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.165.61.128, 18.165.61.93, 18.165.61.110, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.165.61.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3182988 (3.0M) [application/octet-stream]
Saving to: ‘big-zip-files.zip’

big-zip-files.zip                                          100%[======================================================================================================================================>]   3.04M  2.17MB/s    in 1.4s    

2023-10-20 18:21:19 (2.17 MB/s) - ‘big-zip-files.zip’ saved [3182988/3182988]

     
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


<img width="614" alt="Screenshot 2023-10-22 at 4 39 13 PM" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/213a59df-3125-4159-a0fd-47076738c6e6">



```shell
┌──(xodzk㉿kali)-[~]
└─$ wget https://artifacts.picoctf.net/c/164/disk.img.gz      
--2023-10-22 09:40:51--  https://artifacts.picoctf.net/c/164/disk.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.165.61.111, 18.165.61.128, 18.165.61.93, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.165.61.111|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29714372 (28M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz                                                100%[======================================================================================================================================>]  28.34M  4.54MB/s    in 7.0s    

2023-10-22 09:41:00 (4.03 MB/s) - ‘disk.img.gz’ saved [29714372/29714372]

┌──(xodzk㉿kali)-[~]
└─$ gunzip disk.img.gz

┌──(xodzk㉿kali)-[~]
└─$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)

┌──(xodzk㉿kali)-[~]
└─$ nc saturn.picoctf.net 64605     
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752
202752
Great work!
picoCTF{mm15_f7w!}      
```

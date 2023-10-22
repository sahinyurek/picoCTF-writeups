

<img width="607" alt="Disk_Disk_Sleuth_II_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/73148363-1867-4820-ad81-54c98f26de72">



```shell                                                                                                   
┌──(xodzk㉿kali)-[~]
└─$ wget https://mercury.picoctf.net/static/2e54f22211165e9f33a47bdb8a09268b/dds2-alpine.flag.img.gz
--2023-10-22 10:57:55--  https://mercury.picoctf.net/static/2e54f22211165e9f33a47bdb8a09268b/dds2-alpine.flag.img.gz
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29770549 (28M) [application/octet-stream]
Saving to: ‘dds2-alpine.flag.img.gz’

dds2-alpine.flag.img.gz                                    100%[======================================================================================================================================>]  28.39M  3.70MB/s    in 11s     

2023-10-22 10:58:08 (2.58 MB/s) - ‘dds2-alpine.flag.img.gz’ saved [29770549/29770549]
       
┌──(xodzk㉿kali)-[~]
└─$ gunzip dds2-alpine.flag.img.gz 
                                                                                                           
┌──(xodzk㉿kali)-[~]
└─$ mmls dds2-alpine.flag.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000262143   0000260096   Linux (0x83)
                                                                                                           
┌──(xodzk㉿kali)-[~]
└─$ fls -o 2048 dds2-alpine.flag.img 
d/d 26417:      home
d/d 11: lost+found
r/r 12: .dockerenv
d/d 20321:      bin
d/d 4065:       boot
d/d 6097:       dev
d/d 2033:       etc
d/d 8129:       lib
d/d 14225:      media
d/d 16257:      mnt
d/d 18289:      opt
d/d 16258:      proc
d/d 18290:      root
d/d 16259:      run
d/d 18292:      sbin
d/d 12222:      srv
d/d 16260:      sys
d/d 18369:      tmp
d/d 12223:      usr
d/d 14229:      var
V/V 32513:      $OrphanFiles

┌──(xodzk㉿kali)-[~]
└─$ fls -o 2048 dds2-alpine.flag.img 26417 
   
┌──(xodzk㉿kali)-[~]
└─$ fls -o 2048 dds2-alpine.flag.img 18290
r/r 18291:      down-at-the-bottom.txt
 
┌──(xodzk㉿kali)-[~]
└─$ icat -o 2048 dds2-alpine.flag.img 18291
   _     _     _     _     _     _     _     _     _     _     _     _     _  
  / \   / \   / \   / \   / \   / \   / \   / \   / \   / \   / \   / \   / \ 
 ( p ) ( i ) ( c ) ( o ) ( C ) ( T ) ( F ) ( { ) ( f ) ( 0 ) ( r ) ( 3 ) ( n )
  \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/ 
   _     _     _     _     _     _     _     _     _     _     _     _     _  
  / \   / \   / \   / \   / \   / \   / \   / \   / \   / \   / \   / \   / \ 
 ( s ) ( 1 ) ( c ) ( 4 ) ( t ) ( 0 ) ( r ) ( _ ) ( n ) ( 0 ) ( v ) ( 1 ) ( c )
  \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/ 
   _     _     _     _     _     _     _     _     _     _     _  
  / \   / \   / \   / \   / \   / \   / \   / \   / \   / \   / \ 
 ( 3 ) ( _ ) ( d ) ( b ) ( 5 ) ( 9 ) ( d ) ( a ) ( a ) ( 5 ) ( } )
  \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/ 
                                                                             
```


<img width="612" alt="Sleuthkit_Apprentice_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/e4309d4c-9814-4c28-97b4-c6c51978597f">



Retrieve the file with wget.

```shell
┌──(xodzk㉿kali)-[~]
└─$ wget https://artifacts.picoctf.net/c/138/disk.flag.img.gz
--2023-10-22 09:51:25--  https://artifacts.picoctf.net/c/138/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.165.61.110, 18.165.61.93, 18.165.61.111, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.165.61.110|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 47534528 (45M) [application/octet-stream]
Saving to: ‘disk.flag.img.gz’

disk.flag.img.gz                                           100%[======================================================================================================================================>]  45.33M  4.05MB/s    in 12s     

2023-10-22 09:51:40 (3.74 MB/s) - ‘disk.flag.img.gz’ saved [47534528/47534528]

```

unzip the image and see partitions with mmls

```shell
┌──(xodzk㉿kali)-[~]
└─$ gunzip disk.flag.img

┌──(xodzk㉿kali)-[~]
└─$ mmls disk.flag.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000360447   0000153600   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000360448   0000614399   0000253952   Linux (0x83)
                                                    
```


Look at file and directory names using fls -o imgoffset
There doesn't seem to be any useful file in the first partition

```shell
┌──(xodzk㉿kali)-[~]
└─$ fls -o 2048 disk.flag.img       
d/d 11: lost+found
r/r 12: ldlinux.sys
r/r 13: ldlinux.c32
r/r 15: config-virt
r/r 16: vmlinuz-virt
r/r 17: initramfs-virt
l/l 18: boot
r/r 20: libutil.c32
r/r 19: extlinux.conf
r/r 21: libcom32.c32
r/r 22: mboot.c32
r/r 23: menu.c32
r/r 14: System.map-virt
r/r 24: vesamenu.c32
V/V 25585:      $OrphanFiles
                                                                                                                                                                                                                                          
┌──(xodzk㉿kali)-[~]
└─$ fls -o 360448 disk.flag.img
d/d 451:        home
d/d 11: lost+found
d/d 12: boot
d/d 1985:       etc
d/d 1986:       proc
d/d 1987:       dev
d/d 1988:       tmp
d/d 1989:       lib
d/d 1990:       var
d/d 3969:       usr
d/d 3970:       bin
d/d 1991:       sbin
d/d 1992:       media
d/d 1993:       mnt
d/d 1994:       opt
d/d 1995:       root
d/d 1996:       run
d/d 1997:       srv
d/d 1998:       sys
d/d 2358:       swap
V/V 31745:      $OrphanFiles

```

Check home and root directories

```shell
┌──(xodzk㉿kali)-[~]
└─$ fls -o 360448 disk.flag.img 451
                                                                                                                                                                                                                                          
┌──(xodzk㉿kali)-[~]
└─$ fls -o 360448 disk.flag.img 1995
r/r 2363:       .ash_history
d/d 3981:       my_folder

```

find the flag in my_folder then output the contents with icat

```shell
┌──(xodzk㉿kali)-[~]
└─$ fls -o 360448 disk.flag.img 3981
r/r * 2082(realloc):    flag.txt
r/r 2371:       flag.uni.txt

┌──(xodzk㉿kali)-[~]
└─$ icat -o 360448 disk.flag.img 2371
picoCTF{by73_5urf3r_2f22df38}
                                                                      
```

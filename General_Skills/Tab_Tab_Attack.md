
<img width="612" alt="Tab_Tab_Attack_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/d4c4b27c-02a9-4d67-937f-7674d791642a">


Unzip the file then press tab after writing cd to autocomplete the folder name.

```shell
┌──(xodzk㉿kali)-[~]
└─$ unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
                   
┌──(xodzk㉿kali)-[~]
└─$ cd Addadshashanammu 
                                                                                                                                                                                                                                    
┌──(xodzk㉿kali)-[~/Addadshashanammu]
└─$ cd Almurbalarammi  
                                                                                                                                                                                                                                    
┌──(xodzk㉿kali)-[~/Addadshashanammu/Almurbalarammi]
└─$ cd Ashalmimilkala 
                                                                                                                                                                                                                                    
┌──(xodzk㉿kali)-[~/Addadshashanammu/Almurbalarammi/Ashalmimilkala]
└─$ cd Assurnabitashpi 
                                                                                                                                                                                                                                    
┌──(xodzk㉿kali)-[~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi]
└─$ cd Maelkashishi   
                                                                                                                                                                                                                                    
┌──(xodzk㉿kali)-[~/…/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi]
└─$ cd Onnissiralis 
                                                                                                                                                                                                                                    
┌──(xodzk㉿kali)-[~/…/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis]
└─$ cd Ularradallaku 
                                                                                                                                                                                                                                    
```

When there are no more folders you find a binary file run it and get the flag.

```shell
┌──(xodzk㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ls              
fang-of-haynekhtnamet

┌──(xodzk㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ file fang-of-haynekhtnamet 
fang-of-haynekhtnamet: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=47e898db922f38cb54ab4a08fb4e3def5a1cb6a1, not stripped
                                                                                                                                                                                                                                    
┌──(xodzk㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ./fang-of-haynekhtnamet  
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_a00cae70}


```

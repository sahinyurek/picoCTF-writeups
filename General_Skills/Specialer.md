<img width="604" alt="Specialer_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/c919e9fb-9aa8-4b45-a292-cde9d2d09e88">

Use tab completion here by pressing tab twice and it will list possible commands. We don't have cat so use echo"$(<flag.txt)" to read files.

```shell
┌──(xodzk㉿kali)-[~]
└─$ ssh -p 64383 ctf-player@saturn.picoctf.net

ctf-player@saturn.picoctf.net's password: 
Specialer$ 
!          bind       compopt    elif       fc         if         printf     shift      true       while
./         break      continue   else       fg         in         pushd      shopt      type       {
:          builtin    coproc     enable     fi         jobs       pwd        source     typeset    }
[          caller     declare    esac       for        kill       read       suspend    ulimit     
[[         case       dirs       eval       function   let        readarray  test       umask      
]]         cd         disown     exec       getopts    local      readonly   then       unalias    
alias      command    do         exit       hash       logout     return     time       unset      
bash       compgen    done       export     help       mapfile    select     times      until      
bg         complete   echo       false      history    popd       set        trap       wait
Specialer$ cd 
.hushlogin  .profile    abra/       ala/        sim/
Specialer$ cd ala/
Specialer$ echo "$(<kazam.txt)"
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_811ae7e9}
```



<img width="608" alt="plumbing_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/074f32ed-662c-48f4-810d-369875df60ae">


Read data with netcat then use grep with pipe to find the flag in the data.

```shell
┌──(xodzk㉿kali)-[~]
└─$ nc jupiter.challenges.picoctf.org 4427 | grep picoCTF
picoCTF{digital_plumb3r_5ea1fbd7}
```

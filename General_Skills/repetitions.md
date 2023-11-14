
<img width="604" alt="repetitions_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/06ef70c6-f418-466e-9ce0-ab03c983a839">

The encrypted flag is in base64 format so I decoded it repeatedly until I got the flag

```shell
┌──(xodzk㉿kali)-[~]
└─$ cat enc_flag                             
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbHBWV0VKVVZGWm9RMlZzV2tWUmJFNVNDbUpXV25wWmExSmhWMGRHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==

┌──(xodzk㉿kali)-[~]
└─$ cat enc_flag | base64 --decode | base64 --decode | base64 --decode | base64 --decode | base64 --decode | base64 --decode
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_dfe803c6}
```

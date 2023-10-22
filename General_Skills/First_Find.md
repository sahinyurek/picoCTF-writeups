
<img width="617" alt="First_Find_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/3a61497c-5570-495e-99ae-f08c94f4f37d">


                                                                                                           
Unzip file

```shell
┌──(xodzk㉿kali)-[~]
└─$ file files.zip
files.zip: Zip archive data, at least v1.0 to extract, compression method=store
┌──(xodzk㉿kali)-[~]
└─$ unzip files.zip 
Archive:  files.zip
   creating: files/
   creating: files/satisfactory_books/
   creating: files/satisfactory_books/more_books/
  inflating: files/satisfactory_books/more_books/37121.txt.utf-8  
  inflating: files/satisfactory_books/23765.txt.utf-8  
  inflating: files/satisfactory_books/16021.txt.utf-8  
  inflating: files/13771.txt.utf-8   
   creating: files/adequate_books/
   creating: files/adequate_books/more_books/
   creating: files/adequate_books/more_books/.secret/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
 extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt  
  inflating: files/adequate_books/more_books/1023.txt.utf-8  
  inflating: files/adequate_books/46804-0.txt  
  inflating: files/adequate_books/44578.txt.utf-8  
   creating: files/acceptable_books/
   creating: files/acceptable_books/more_books/
  inflating: files/acceptable_books/more_books/40723.txt.utf-8  
  inflating: files/acceptable_books/17880.txt.utf-8  
  inflating: files/acceptable_books/17879.txt.utf-8  
  inflating: files/14789.txt.utf-8   
```

Find the flag using find.

```shell
┌──(xodzk㉿kali)-[~]
└─$ cd files
┌──(xodzk㉿kali)-[~/files]
└─$ find . -name uber-secret.txt
./adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
┌──(xodzk㉿kali)-[~/files]
└─$ cat ./adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt

picoCTF{f1nd_15_f457_ab443fd1}

```


<img width="604" alt="nice_netcat_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/fb9ca1b1-0de4-4f7a-b408-33d6164f450a">

We receive ASCII values from netcat. We could convert them manually using an ASCII table. 

```shell
┌──(xodzk㉿kali)-[~]
└─$ nc mercury.picoctf.net 49039
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
51 
100 
56 
52 
101 
100 
99 
56 
125 
10 
```

I used this script written in python:

```python
def ascii_to_string(input_file):
    with open(input_file, 'r') as file:
        ascii_values = file.read().splitlines()

    try:
        string_result = ''.join(chr(int(ascii_value)) for ascii_value in ascii_values)
        return string_result
    except ValueError:
        return "Error: Invalid ASCII values in the input file."

if __name__ == "__main__":
    file_path = input("Enter the path to the file containing ASCII values: ")

    try:
        result = ascii_to_string(file_path)
        print("Converted string:")
        print(result)
    except FileNotFoundError:
        print("Error: File not found.")
```

Copy the ASCII values to a text file then run the script.

```shell
┌──(xodzk㉿kali)-[~]
└─$ python3 convertAscii.py 
Enter the path to the file containing ASCII values: ascii.txt
Converted string:
picoCTF{g00d_k1tty!_n1c3_k1tty!_3d84edc8}
```


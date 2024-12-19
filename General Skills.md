### PW Crack 1
Description \
Can you crack the password to get the flag? \
Download the password checker here and you'll need the encrypted flag in the same directory too

#### Hint:
1. To view the file in the webshell, do: $ nano level1.py
2. To exit nano, press Ctrl and x and follow the on-screen prompts.
3. The str_xor function does not need to be reverse engineered for this challenge.
```
def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "691d"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")
```
1. Run the 2 files in the same directory
2. Enter the user_pw as 691d

picoCTF{545h_r1ng1ng_56891419}


### PW Crack 2
Description \
Can you crack the password to get the flag? \
Download the password checker here and you'll need the encrypted flag in the same directory too.

#### Hint:
1. Does that encoding look familiar?
2. The str_xor function does not need to be reverse engineered for this challenge.
```
def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")
```
1. Run the 2 files in the same directory
2. user_pw == chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65): chr() indicates the ASCII codes.
3. By using the ASCII table, chr(0x33) == 3;  chr(0x39) == 9;  chr(0x63) == c;  chr(0x65) == e
4. Enter 39ce

picoCTF{tr45h_51ng1ng_502ec42e}

### ASCII Numbers
Description \
Convert the following string of ASCII numbers into a readable string:
0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x34 0x35 0x63 0x31 0x31 0x5f 0x6e 0x30 0x5f 0x71 0x75 0x33 0x35 0x37 0x31 0x30 0x6e 0x35 0x5f 0x31 0x6c 0x6c 0x5f 0x74 0x33 0x31 0x31 0x5f 0x79 0x33 0x5f 0x6e 0x30 0x5f 0x6c 0x31 0x33 0x35 0x5f 0x34 0x34 0x35 0x64 0x34 0x31 0x38 0x30 0x7d

1. https://codebeautify.org/ascii-to-text

picoCTF{45c11_n0_qu35710n5_1ll_t311_y3_n0_l135_445d4180}

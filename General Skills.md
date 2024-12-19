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

### Repetitions
Description \
Can you make sense of this file? \
Download the file here: \
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZrTTBKeldWaHdRMDB4V2tWU2JFNVdDbUpXV2tkVU1WcFhWVzFHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==

1. https://gchq.github.io/CyberChef/#input=Vm1wR1UxRXlSWGxVV0d4VFlteEtWVll3WkZOV2JHeHlWMjFHVjFKdGVEQlViRnBQWVd4S2RGVnNhRnBXVmxVeFdWWmFTMVpXV25WaApSbVJYWld0YWIxZFdXbXRTTWs1eVRsWldXQXBpVlZwVVZtMTBkMVZXWkZkVmEyUnBZbFphV0ZadE5WZFZaM0JwVTBWS2VsZFdVa05rCk1sWlhWbGhvV0dKWVFrOVZiRkpYVTBaa2NWUnVUbGRhTTBKWlZXcEdTMlZXV2tkYVNHUlhDazFzV25wV1YzaGhWbTFLUms1WE9WVlcKVmtwRVZHeGFZVmRGTVZoU2JGWnJUVEJLZWxkV2FIZFJNREI0VjJ0V1UySkZOVmREYlVwWFYydGtWVTFXY0ZoV1Z6RkhaRWRXUmxacwphR2tLWWxScmVsWkVSbGRVTWtwelVXeFdUbEpZVGt4RFp6MDlDZz09Cgo 

2. from Base64 6 times: 

1st Base64: \
VjFSQ2EyTXlSblJUV0dSVllrWmFWRmx0TlZOalJtUlhZVVU1YVZKVVZuaFdWekZoWVZkR2NrNVVX
bUZTVmtwUVdWUkdibVZXVm5WUgpiSEJzWVRCd2VWVXhXbXBOUlRWSFdqTnNWZ3BYUjFKeVZGZHdW
MlZzVWxaVmJFNW9UVVJDTlZaWE1XRlVkM0JzWVhwQ00xWkVSbE5WCmJWWkdUMVpXVW1GdGVFVlhi
bTkzVDFWT2JsQlVNRXNLCg== 

2nd Base64: \
V1RCa2MyRnRTWGRVYkZaVFltNVNjRmRXYUU5aVJUVnhWVzFhYVdGck5UWmFSVkpQWVRGbmVWVnVR
bHBsYTBweVUxWmpNRTVHWjNsVgpXR1JyVFdwV2VsUlZVbE5oTURCNVZXMWFUd3BsYXpCM1ZERlNV
bVZGT1ZWUmFteEVXbm93T1VOblBUMEsK 

3rd Base64: \
WTBkc2FtSXdUbFZTYm5ScFdWaE9iRTVxVW1aaWFrNTZaRVJPYTFneVVuQlpla0pyU1ZjME5GZ3lV
WGRrTWpWelRVUlNhMDB5VW1aTwplazB3VDFSUmVFOVVRamxEWnowOUNnPT0K 

4th Base64: \
Y0dsamIwTlVSbnRpWVhObE5qUmZiak56ZEROa1gyUnBZekJrSVc0NFgyUXdkMjVzTURSa00yUmZO
ek0wT1RReE9UQjlDZz09Cg== 

5th Base64: \
cGljb0NURntiYXNlNjRfbjNzdDNkX2RpYzBkIW44X2Qwd25sMDRkM2RfNzM0OTQxOTB9Cg== 

6th Base64: \
Get the CTF

picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_73494190}


### Runme.py
Description \
Run the runme.py script to get the flag. Download the script with your browser or with wget in the webshell. \
Download runme.py Python script: 
```
#!/usr/bin/python3
################################################################################
# Python script which just prints the flag
################################################################################

flag ='picoCTF{run_s4n1ty_run}'
print(flag)
```
#### Hint:
1. If you have Python on your computer, you can download the script normally and run it. Otherwise, use the wget command in the webshell.
2. To use wget in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
3. Type everything after the dollar sign in the webshell: $ wget , then paste the link after the space after wget and press enter. This will download the script for you in the webshell so you can run it!
4. Finally, to run the script, type everything after the dollar sign and then press enter: $ python3 runme.py You should have the flag now!

picoCTF{run_s4n1ty_run}


### Static Ain't Alwats Noise
Description \
Can you look at the data in this binary: static? This BASH script might help!

1. Download the files 
2. Open the static file in the text editor. I used the online Python Editor: https://www.online-python.com/
3. The CTF exists in the static file.
 
picoCTF{d15a5m_t34s3r_f5aeda17}


### Obedient Cat
Description \
This file has a flag in plain sight (aka "in-the-clear"). Download flag.
#### Hint:
1. Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.
2. To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag
3. $ man cat

1. Open the file in the text editor. I used the online Python Editor: https://www.online-python.com/
picoCTF{s4n1ty_v3r1f13d_1a94e0f9}


### 2Warm
Description \
Can you convert the number 42 (base 10) to binary (base 2)? 
#### Use this table to do the division, which is more clear 
https://www.rapidtables.com/convert/number/base-converter.html

picoCTF{101010}


### First Grep
Description
Can you find the flag in file? This would be really tedious to look through manually, something tells me there is a better way.

1. Open the file in the text editor. I used the online Python Editor: https://www.online-python.com/
2. The CTF is in teh file

picoCTF{grep_is_good_to_find_things_5af9d829}


### Warmed Up
Description \
What is 0x3D (base 16) in decimal (base 10)? \

Base 16 to decimal calculation:

1. D is 13
2. (0X3D)16 = (0 × 163) + (NaN × 162) + (3 × 161) + (13 × 160) = (61)10

picoCTF{61}

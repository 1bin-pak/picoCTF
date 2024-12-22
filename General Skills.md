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

### Strings it
Description\
Can you find the flag in file without running it? 

1. Open the file in the file in the online Python Editor: https://www.online-python.com/
2. The CTF is directly given as a string (not seperated substrings).

picoCTF{5tRIng5_1T_7f766a23}


### Bases
Description \
What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.

#### Need to Know:
https://www.microfocus.com/documentation/visual-cobol/vc80/CSWin/BKCJCJDEFNS009.html \
Base64 is a scheme for converting binary data to printable ASCII characters, namely the upper- and lower-case Roman alphabet characters (A–Z, a–z), the numerals (0–9), and the "+" and "/" symbols, with the "=" symbol as a special suffix code. The data's original length must be a multiple of eight bits.

1. Put the string into the Base 64 decoder
2. Decode it once and get: \
l3arn_th3_r0p35

picoCTF{l3arn_th3_r0p35}


### Lets Warm Up
Description \
If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

1. https://neapay.com/online-tools/hex-to-ascii-converter.html
2. Get: p

picoCTF{p}


### Convertme.py
Description
Run the Python script and convert the given number from decimal to binary to get the flag.
Download Python script

#### Hint:

1. Look up a decimal to binary number conversion app on the web or use your computer's calculator!
2. The str_xor function does not need to be reverse engineered for this challenge.
3. If you have Python on your computer, you can download the script normally and run it. Otherwise, use the wget command in the webshell.
4. To use wget in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
5. Type everything after the dollar sign in the webshell: $ wget , then paste the link after the space after wget and press enter. This will download the script for you in the webshell so you can run it!
6. Finally, to run the script, type everything after the dollar sign and then press enter: $ python3 convertme.py

Steps:

1. Run the code
2. Get:If 28 is in decimal base, what is it in binary base?
3. Convert 28 into binary, get: 11100
4. Enter 11100 and get the flag

picoCTF{4ll_y0ur_b4535_9c3b7d4d}


### Fixme1.py
Description \
Fix the syntax error in this Python script to print the flag. \
Download Python script

```
flag = str_xor(flag_enc, 'enkidu')
  print('That is correct! Here\'s your flag: ' + flag)
```
1. Fix the indentation of the print statement


picoCTF{1nd3nt1ty_cr1515_182342f7}


### Fixme2.py

Description \
Fix the syntax error in the Python script to print the flag. \
Download Python script
```
# Check that flag is not empty
if flag = "":
  print('String XOR encountered a problem, quitting.')
else:
  print('That is correct! Here\'s your flag: ' + flag)
```
```
# Check that flag is not empty
if flag == "":
  print('String XOR encountered a problem, quitting.')
else:
  print('That is correct! Here\'s your flag: ' + flag)
```

1. Change the '=' to '=='

picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}


### Codebook
Description \
Run the Python script code.py in the same directory as codebook.txt. \
Download code.py \
Download codebook.txt

1. Run the code file

picoCTF{c0d3b00k_455157_d9aa2df2}


### Wave A Flag
Description \
Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...

1. Open a text editor and find the flag

picoCTF{b1scu1ts_4nd_gr4vy_30e77291}

### Time Machine
Description \
What was I last working on? I remember writing a note to help me remember... \
You can download the challenge files here: \
challenge.zip
#### Hint:
1. The cat command will let you read a file, but that won't help you here!
2. Read the chapter on Git from the picoPrimer here.
https://primer.picoctf.org/#_git_version_control
3. When committing a file with git, a message can (and should) be included.
1. Upzip the zip file
2. Find the CTF in COMMIT_EDITMSG file, open it in the text editor

#### THIS QUESTION IS TESTING THE KNOWLDGE OF GIT, REDO IT
picoCTF{t1m3m@ch1n3_e8c98b3a}

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


### HashingJobApp 
Description
If you want to hash with the best, beat this test!
`$ nc saturn.picoctf.net 64337`

1. Go to the website: \
https://dencode.com/en/hash
```
momo1126-picoctf@webshell:~$ nc saturn.picoctf.net 53633
Please md5 hash the text between quotes, excluding the quotes: 'a full moon'
Answer: 
3dbbee596fa3666609f8bcff87bb3df4
3dbbee596fa3666609f8bcff87bb3df4
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Andy Warhol'
Answer: 
024e803352db3cd645a396423ac12c31
024e803352db3cd645a396423ac12c31
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Adolf Hitler'
Answer: 
540dea05a35b0fc9a050f36db954a484
540dea05a35b0fc9a050f36db954a484
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_674c1de2}
```
picoCTF{4ppl1c4710n_r3c31v3d_674c1de2}

### Glitch Cat (General Skills)
Description
Our flag printing service has started glitching! \
`$ nc saturn.picoctf.net 56585`
```
momo1126-picoctf@webshell:~$  nc saturn.picoctf.net 64530
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
```
```
remain = [chr(0x61), chr(0x34), chr(0x33), chr(0x39), chr(0x32), chr(0x64), chr(0x32), chr(0x65)]
res = []
for r in remain:
    res.append(r)
print('picoCTF{gl17ch_m3_n07_' + "".join(res) + '}')
```

picoCTF{gl17ch_m3_n07_a4392d2e}

### Magikarp Ground Mission 
Description \
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `a13b7f9d` 

Challenge Endpoints	\
`ssh ctf-player@venus.picoctf.net -p 59688`

```
momo1126-picoctf@webshell:~$ ssh ctf-player@venus.picoctf.net -p 59688
The authenticity of host '[venus.picoctf.net]:59688 ([3.131.124.143]:59688)' can't be established.
ED25519 key fingerprint is SHA256:P1f6h95BrSVnJbm2AKhphfHHGEyAeThib/rN/AwKs24.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[venus.picoctf.net]:59688' (ED25519) to the list of known hosts.
ctf-player@venus.picoctf.net's password: 
Welcome to Ubuntu 18.04.5 LTS (GNU/Linux 5.4.0-1041-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1of3.flag.txt 
picoCTF{xxsh_

ctf-player@pico-chall$ cat instructions-to-2of3.txt 
Next, go to the root of all things, more succinctly `/`

ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  bin  boot  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cat 2of3.flag.txt 
0ut_0f_\/\/4t3r_

ctf-player@pico-chall$ cat instructions-to-3of3.txt 
Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cd ~
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt 
71be5264}
```
picoCTF{xxsh_0ut_0f_\/\/4t3r_71be5264}

### What's A Net Cat? 
Description
Using netcat (nc) is going to be pretty important. \
Can you connect to jupiter.challenges.picoctf.org at port 41120 to get the flag?
```
momo1126-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 41120
You're on your way to becoming the net cat master
picoCTF{nEtCat_Mast3ry_3214be47}
```
picoCTF{nEtCat_Mast3ry_3214be47}

### Nice Netcat
Description \
There is a nice program that you can talk to by using this command in a shell: $ nc mercury.picoctf.net 22902, but it doesn't speak English...
```
momo1126-picoctf@webshell:~$ nc mercury.picoctf.net 22902
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
100 
51 
100 
102 
100 
54 
100 
102 
125 
10
```
```
st = "112 105 99 111 67 84 70 123 103 48 48 100 95 107 49 116 116 121 33 95 110 49 99 51 95 107 49 116 116 121 33 95 100 51 100 102 100 54 100 102 125 10"
s = st.replace(' ', ',')
# 112,105,99,111,67,84,70,123,103,48,48,100,95,107,49,116,116,121,33,95,110,49,99,51,95,107,49,116,116,121,33,95,100,51,100,102,100,54,100,102,125,10
lst = s.split(',')
# [112, 105,99,111, 67, 84, 70, 123, 103, 48, 48, 100, 95, 107, 49, 116, 116, 121, 33, 95, 110 ,49 ,99, 51, 95, 107, 49, 116, 116, 121, 33, 95, 100, 51 ,100 ,102 ,100 ,54 ,100, 102, 125, 10]

res = []
for r in lst:
    # res.append(chr(r))
    # TypeError: an integer is required (got type str)
    res.append(chr(int(r)))
print(''.join(res))
```
picoCTF{g00d_k1tty!_n1c3_k1tty!_d3dfd6df}

### Binhexa 
Description \
How well can you perfom basic binary operations? \
Start searching for the flag here `nc titan.picoctf.net 52483`
1. https://www.rapidtables.com/calc/math/binary-calculator.html
```
momo1126-picoctf@webshell:~$ nc titan.picoctf.net 60691

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 01000011
Binary Number 2: 10100010

Question 1/6:
Operation 1: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 01010001
Correct!

Question 2/6:
Operation 2: '&' AND
Perform the operation on Binary Number 1&2.
Enter the binary result: 00000010
Correct!

Question 3/6:
Operation 3: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 10000110
Correct!

Question 4/6:
Operation 4: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11100101
Correct!

Question 5/6:
Operation 5: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10101001100110
Correct!

Question 6/6:
Operation 6: '|' OR
Perform the operation on Binary Number 1&2.
Enter the binary result: 11100011
Correct!

Enter the results of the last operation in hexadecimal: E3
Correct answer!

The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_aeaf4b09}
```
picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_aeaf4b09}

### First Find 
Description \
Unzip this archive and find the file named 'uber-secret.txt'
Download zip file
1. https://zip.softgateon.net/?m=UnZip_Viewer
2. Open \
files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt

picoCTF{f1nd_15_f457_ab443fd1}

### Binary Search 
Description \
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses. \
Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools! \
You can download the challenge files here: \
challenge.zip
`ssh -p 53901 ctf-player@atlas.picoctf.net` \
Using the password `f3b61b38`. \
Accept the fingerprint with yes, and ls once connected to begin. Remember, in a shell, passwords are hidden!
1. Start from 500
2. Higher mean go higher numbers; Lower means choose lower numbers
3. guess = (most_recent_higher - most_recent_lower) // 2 + most_recent_lower
```
momo1126-picoctf@webshell:~$ ssh -p 65085 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500 
Higher! Try again.
Enter your guess: 750
Higher! Try again.
Enter your guess: 875
Lower! Try again.
Enter your guess: 812
Lower! Try again.
Enter your guess: 781
Lower! Try again.
Enter your guess: 765
Higher! Try again.
Enter your guess: 773
Higher! Try again.
Enter your guess: 777
Congratulations! You guessed the correct number: 777
Here's your flag: picoCTF{g00d_gu355_6dcfb67c}
Connection to atlas.picoctf.net closed.
```
picoCTF{g00d_gu355_6dcfb67c}

### Super SSH
Description \
Using a Secure Shell (SSH) is going to be pretty important. \
Can you ssh as ctf-player to titan.picoctf.net at port 57277 to get the flag? \
You'll also need the password 1db87a14. If asked, accept the fingerprint with yes. \
If your device doesn't have a shell, you can use: https://webshell.picoctf.org \
If you're not sure what a shell is, check out our Primer: https://primer.picoctf.com/#_the_shell
1. `ssh ctf-player@titan.picoctf.net -p 60295` \
Don't forget -p!!!!
2. -p port
Port to connect to on the remote host. This can be specified on a per-host basis in the configuration file.
```
momo1126-picoctf@webshell:~$ ssh ctf-player@titan.picoctf.net -p 60295
The authenticity of host '[titan.picoctf.net]:60295 ([3.139.174.234]:60295)' can't be established.
ED25519 key fingerprint is SHA256:4S9EbTSSRZm32I+cdM5TyzthpQryv5kudRP9PIKT7XQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[titan.picoctf.net]:60295' (ED25519) to the list of known hosts.
ctf-player@titan.picoctf.net's password: 
Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_45a48857}
Connection to titan.picoctf.net closed.
```
picoCTF{s3cur3_c0nn3ct10n_45a48857}

### Big Zip
Description
Unzip this archive and find the flag.
Download zip file https://artifacts.picoctf.net/c/505/big-zip-files.zip
```
┌──(kali㉿kali)-[~/code]
└─$ wget https://artifacts.picoctf.net/c/500/files.zip 

┌──(kali㉿kali)-[~/code]
└─$ grep -r "pico" files        
files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
```
#### Note:  UNDERSTAND $wget, $grep, REDO
https://hackmd.io/@nataliepjlin/SknjWeri3
https://www.whatismybrowser.com/developers/tools/wget-wizard/
picoCTF{gr3p_15_m4g1c_ef8790dc}

### Tab, Tab, Attack
Description \
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: Addadshashanammu.zip
#### Hint:
After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...
1. Upload the zip file into the Unzip viewer
2. Get the CTF from the content

picoCTF{l3v3l_up!_t4k3_4_r35t!_d32e018c}

### Python Wrangling 
Description \
Python scripts are invoked kind of like programs in the Terminal... Can you run this Python script using this password to get the flag? 
#### Hints:
1. Get the Python script accessible in your shell by entering the following command in the Terminal prompt: \
`$ wget https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/ende.py`
2. $ man python
```
momo1126-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/ende.py
--2024-12-29 08:43:17--  https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/ende.py
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1328 (1.3K) [application/octet-stream]
Saving to: 'ende.py.1'

ende.py.1                                   100%[===========================================================================================>]   1.30K  --.-KB/s    in 0s      

2024-12-29 08:43:17 (581 MB/s) - 'ende.py.1' saved [1328/1328]

momo1126-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/pw.txt
--2024-12-29 08:44:06--  https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/pw.txt
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 33 [application/octet-stream]
Saving to: 'pw.txt'

pw.txt                                      100%[===========================================================================================>]      33  --.-KB/s    in 0s      

2024-12-29 08:44:06 (13.5 MB/s) - 'pw.txt' saved [33/33]

momo1126-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/flag.txt.en
--2024-12-29 08:44:48--  https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/flag.txt.en
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 140 [application/octet-stream]
Saving to: 'flag.txt.en'

flag.txt.en                                 100%[===========================================================================================>]     140  --.-KB/s    in 0s      

2024-12-29 08:44:48 (59.9 MB/s) - 'flag.txt.en' saved [140/140]

momo1126-picoctf@webshell:~$ python3 ende.py 
Usage: ende.py (-e/-d) [file]
momo1126-picoctf@webshell:~$ python3 ende.py -d flag.txt.en
Please enter the password:dbd1bea4dbd1bea4dbd1bea4dbd1bea4
picoCTF{4p0110_1n_7h3_h0us3_dbd1bea4}
```
```
momo1126-picoctf@webshell:~$ cat pw.txt | python3 ende.py -d flag.txt.en
Please enter the password:picoCTF{4p0110_1n_7h3_h0us3_dbd1bea4}
momo1126-picoctf@webshell:~$ 
```
#### Reference:
https://ctftime.org/writeup/28917

picoCTF{4p0110_1n_7h3_h0us3_dbd1bea4}

### Permissions
Description \
Can you read files in the root file? \
The system admin has provisioned an account for you on the main server: \
`ssh -p 50965 picoplayer@saturn.picoctf.net` \
Password: UYiOazkqY2 \
Can you login and read the root file?
```
momo1126-picoctf@webshell:~$ ssh -p 50965 picoplayer@saturn.picoctf.net
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Mon Dec 30 04:33:21 2024 from 3.140.102.47
picoplayer@challenge:~$ ls /root
ls: cannot open directory '/root': Permission denied


picoplayer@challenge:~$ sudo -l
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi

    
picoplayer@challenge:~$ sudo vi /root
" ============================================================================
" Netrw Directory Listing                                        (netrw v165)
"   /root
"   Sorted by      name
"   Sort sequence: [\/]$,\<core\%(\.\d\+\)\=\>,\.h$,\.c$,\.cpp$,\~\=\*$,*,\.o$,\.obj$,\.info$,\.swp$,\.bak$,\~$
"   Quick Help: <F1>:help  -:go up dir  D:delete  R:rename  s:sort-by  x:special
" ==============================================================================
../
./
.vim/                                                                                                                                
.bashrc
.flag.txt
.profile
```
1. Go to .flag.txt, get the CTF
#### Note: UNDERSTAND & REDO
#### Reference
https://github.com/snwau/picoCTF-2023-Writeup/blob/main/General%20Skills/Permissions/Permissions.md

picoCTF{uS1ng_v1m_3dit0r_89e9cf1a}


### Serpentine  
Description
Find the flag in the Python script!
Download Python script
1. Run the py code and try to print the flag
```
Oops! I must have misplaced the print_flag function! Check my source code!
```
2. Call print_flag() to get the flag
```
import random
import sys

def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5c) + chr(0x01) + chr(0x57) + chr(0x2a) + chr(0x17) + chr(0x5e) + chr(0x5f) + chr(0x0d) + chr(0x3b) + chr(0x19) + chr(0x56) + chr(0x5b) + chr(0x5e) + chr(0x36) + chr(0x53) + chr(0x07) + chr(0x51) + chr(0x18) + chr(0x58) + chr(0x05) + chr(0x57) + chr(0x11) + chr(0x3a) + chr(0x0f) + chr(0x0e) + chr(0x59) + chr(0x06) + chr(0x4d) + chr(0x55) + chr(0x0c) + chr(0x0f) + chr(0x14)

def print_flag():
  flag = str_xor(flag_enc, 'enkidu')
  print(flag)

print_flag()
```
picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}

### Plumbing 
Description \
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? \
Connect to jupiter.challenges.picoctf.org 14291
#### Hint
What's a pipe? No not that kind of pipe... This kind
```
momo1126-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 14291 | grep pico
picoCTF{digital_plumb3r_ea8bfec7}
```
picoCTF{digital_plumb3r_ea8bfec7}


### Based 
Description \
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with nc jupiter.challenges.picoctf.org 29221
1. Use the converter to get the string of the following to get the flag:
01100011 01101000 01100001 01101001 01110010 Binary \
154 141 155 160 Octal \
736f636b6574 Hex
```
momo1126-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 29221
Let us see how data is stored
chair
Please give the 01100011 01101000 01100001 01101001 01110010 as a word.
...
you have 45 seconds.....

Input:
chair
Please give me the  154 141 155 160 as a word.
Input:
lamp
Please give me the 736f636b6574 as a word.
Input:
socket
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_00a975ff}
```

picoCTF{learning_about_converting_values_00a975ff}

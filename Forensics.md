### Secret of the Polyglot
Description \
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?
Download the suspicious file here.

1. Can find the 2nd part of the CTF directly by opening it as a PDF file
2. Open the file in Painter to see the 1st part of the file.

picoCTF{f1u3n7_1n_pn9_&_pdf_53b741d6}

### Scan Suprise
Description \
I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead? \
You can download the challenge files here: \
challenge.zip \
Additional details will be available after launching your challenge instance.
1. Download the zip file and find the image
2. https://zxing.org/w/decode.jspx \
Upload the QR Code image and get the CTF

picoCTF{p33k_@_b00_19eccd10}

### Information
Description \
Files can always be changed in a secret way. Can you find the flag? cat.jpg
1. Use the text editor to open the jpg file
2. Decode the resource string uisng Base64, get the CTF
```
<rdf:Description rdf:about=''
  xmlns:cc='http://creativecommons.org/ns#'>
  <cc:license rdf:resource='cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9'/>
 </rdf:Description>
```
picoCTF{the_m3tadata_1s_modified}

### Glory of The Garden
Description \
This garden contains more than it seems.
1. Open the file in the text editor to get the CTF

picoCTF{more_than_m33ts_the_3y3eBdBd2cc}


### Verify (Forensics)
Description \
People keep trying to trick my players with imitation flags. I want to make sure they get the real thing! I'm going to provide the SHA-256 hash and a decrypt script to help you know that my flags are legitimate. \
`ssh -p 50142 ctf-player@rhea.picoctf.net`\
Using the password f3b61b38. Accept the fingerprint with yes, and ls once connected to begin. Remember, in a shell, passwords are hidden! \
`Checksum: fba9f49bf22aa7188a155768ab0dfdc1f9b86c47976cd0f7c9003af2e20598f7` \
To decrypt the file once you've verified the hash, run `./decrypt.sh files/<file>.`

```
momo1126-picoctf@webshell:~$ ssh -p 58428 ctf-player@rhea.picoctf.net
ctf-player@rhea.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1016-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Sat Dec 28 07:18:45 2024 from 127.0.0.1
ctf-player@pico-chall$ ls
checksum.txt  decrypt.sh  files
ctf-player@pico-chall$ cat checksum.txt 
fba9f49bf22aa7188a155768ab0dfdc1f9b86c47976cd0f7c9003af2e20598f7
ctf-player@pico-chall$ sha256sum files/* | grep fba9f49bf22aa7188a155768ab0dfdc1f9b86c47976cd0f7c9003af2e20598f7
fba9f49bf22aa7188a155768ab0dfdc1f9b86c47976cd0f7c9003af2e20598f7  files/87590c24
ctf-player@pico-chall$ ./decrypt.sh
```
#### References: LEARN & REDO
https://github.com/noamgariani11/picoCTF-2024-Writeup/blob/main/Forensics/Verify.md \
"The sha256sum command can be used on a file to get the checksum. To get the checksum of all the files in the directory the sha256sum files/* command could be used. When paired with grep command with the known SHA256 checksum that needs to be found the correct file is displayed." \
https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix \
grep: a command used for searching and matching text patterns in files contained in the regular expressions.

picoCTF{trust_but_verify_87590c24}

### CanYouSee
Description \
How about some hide and seek? \
Download this file here.
1. Extract the png file from Zip \
https://extract.me/
2. Use photo forensics tools to extract string from the graph
https://29a.ch/photo-forensics/
```
JFIF
7http://ns.adobe.com/xap/1.0/
<?xpacket begin='
' id='W5M0MpCehiHzreSzNTczkc9d'?>
<x:xmpmeta xmlns:x='adobe:ns:meta/' x:xmptk='Image::ExifTool 11.88'>
<rdf:RDF xmlns:rdf='http://www.w3.org/1999/02/22-rdf-syntax-ns#'>
 <rdf:Description rdf:about=''
  xmlns:cc='http://creativecommons.org/ns#'>
  <cc:attributionURL rdf:resource='cGljb0NURntNRTc0RDQ3QV9ISUREM05fYTZkZjhkYjh9Cg=='/>
 </rdf:Description>
</rdf:RDF>
</x:xmpmeta>
```
3. Decode in Base64 to get the CTF \
`cGljb0NURntNRTc0RDQ3QV9ISUREM05fYTZkZjhkYjh9Cg==`

picoCTF{ME74D47A_HIDD3N_a6df8db8}

### WhitePages

1. Open the text file in Sublime, see a bunch of <0x2003> and white spaces -> indicates the Binary
2. Replace <0x2003> by 0, white space  by 1
3. Get
```
00001010000010010000100101110000011010010110001101101111010000110101010001000110000010100000101000001001000010010101001101000101010001010010000001010000010101010100001001001100010010010100001100100000010100100100010101000011010011110101001001000100010100110010000000100110001000000100001001000001010000110100101101000111010100100100111101010101010011100100010000100000010100100100010101010000010011110101001001010100000010100000100100001001001101010011000000110000001100000010000001000110011011110111001001100010011001010111001100100000010000010111011001100101001011000010000001010000011010010111010001110100011100110110001001110101011100100110011101101000001011000010000001010000010000010010000000110001001101010011001000110001001100110000101000001001000010010111000001101001011000110110111101000011010101000100011001111011011011100110111101110100010111110110000101101100011011000101111101110011011100000110000101100011011001010111001101011111011000010111001001100101010111110110001101110010011001010110000101110100011001010110010001011111011001010111000101110101011000010110110001011111001101110011000100110000001100000011100000110110001100000110001000110000011001100110000100110111001101110011100101100001001101010110001001100100001110000110001101100101001100100011100101100110001100100011010001100110001101010011100000110110011001000110001101111101000010100000100100001001
```
4. Convert the Binary string to string to get the flag
https://codebeautify.org/binary-string-converter
```
picoCTF

SEE PUBLIC RECORDS & BACKGROUND REPORT
5000 Forbes Ave, Pittsburgh, PA 15213
picoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}
```		

picoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}

### What Lies Within
Description \
There's something in the building. Can you retrieve the flag?
1. Use the online Steganography Decoder to find the CTF
https://stylesuxx.github.io/steganography/

picoCTF{h1d1ng_1n_th3_b1t5}

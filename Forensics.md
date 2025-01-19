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


### Verify
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

### So Meta
Description \
Find the flag in this picture.
1. Find the Metadata \
https://www.metadata2go.com/view-metadata

picoCTF{s0_m3ta_eb36bf44}

### Endianess-V2
Description \
Here's a file that was recovered from a 32-bits system that organized the bytes a weird way. We're not even sure what type of file it is. \
Download it here and see what you can get out of it
1. Use the MetaData Viewer to guess the file type --> JPEG
https://www.metadata2go.com/result#j=e162af02-1600-43da-9f3d-fe248fb79513
```
warning
Processing JPEG-like data after unknown 1-byte header
```
2. View the file in the Hex Editor
https://hexed.it/
JPEG first 4 is: ff d8 ff e0
However we got: e0 ff d8 ff (Reversed version of JPEG header)
3. Open the origional file in Cyberchef https://gchq.github.io/CyberChef/
4. Choose `Swap Endianess`
```
Data Format: Raw
Word Length (Bytes): 4
Pad incomplete words: checked
```
Reverse every 4 bytes of the whole file data
5. Download the file, should get a .jpg file
6. Open the file to see the CTF
#### References
https://www.youtube.com/watch?v=34QnIDFRsxI \
https://medium.com/@shreethaar/picoctf-2024-endianness-v2-8e41857f6adb \
https://medium.com/@0xVirtu4l/picoctf-2024-endianness-v2-challenge-solve-f9c93d6b8fa6

picoCTF{cert!f1Ed_iNd!4n_s0rrY_3nDian_004850bf}

### MSB 
Description \
This image passes LSB statistical analysis, but we can't help but think there must be something to the visual artifacts present in this image... \
Download the image here
1. Upload the png file to https://georgeom.net/StegOnline/upload
2. Choose `Extract Files / Data`
3. Check the MSB values `7` for R, G, B
4. Download Extracted Data -> Open in the txt editor to get the flag

picoCTF{15_y0ur_que57_qu1x071c_0r_h3r01c_ea7deb4c}

### St3g0    
Description \
Download this image and find the flag. \
Download image 
1. Upload the image to \
https://www.aperisolve.com/
2. Go to the `Zeteg` section to find the flag

picoCTF{7h3r3_15_n0_5p00n_a1062667}


### Hideme
Description \
Every file gets a flag. \
The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye here.
1. Download the file and upload to https://www.aperisolve.com/9fa5ca05a7c9e9930f27d577d7f9cbf1
2. Download the .7Z file from section `Foremost`
3. Upload the .7Z file to https://extract.me/
4. Doaload the 00000077.zip file in local download
5. Open `secret` folder -> Open flag.png to see the flag

picoCTF{Hiddinng_An_imag3_within_@n_ima9e_d55982e8}

### Lookey Here
Description \
Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it. \
Download the data here.
1. Download the file and use `grep` to find the flag
```
momo1126-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/124/anthem.flag.txt

momo1126-picoctf@webshell:~$ grep 'CTF' anthem.flag.txt 
      we think that the men of picoCTF{gr3p_15_@w3s0m3_4c479940}
```
picoCTF{gr3p_15_@w3s0m3_4c479940}

### Enhance!
Description \
Download this image file and find the flag. \
Download image file

1. Upload the `.svg` file to https://www.svgviewer.dev/ \
to get the flag
```
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<!-- Created with Inkscape (http://www.inkscape.org/) -->

<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="210mm"
   height="297mm"
   viewBox="0 0 210 297"
   version="1.1"
   id="svg8"
   inkscape:version="0.92.5 (2060ec1f9f, 2020-04-08)"
   sodipodi:docname="drawing.svg">
  <defs
     id="defs2" />
  <sodipodi:namedview
     id="base"
     pagecolor="#ffffff"
     bordercolor="#666666"
     borderopacity="1.0"
     inkscape:pageopacity="0.0"
     inkscape:pageshadow="2"
     inkscape:zoom="0.69833333"
     inkscape:cx="400"
     inkscape:cy="538.41159"
     inkscape:document-units="mm"
     inkscape:current-layer="layer1"
     showgrid="false"
     inkscape:window-width="1872"
     inkscape:window-height="1016"
     inkscape:window-x="48"
     inkscape:window-y="27"
     inkscape:window-maximized="1" />
  <metadata
     id="metadata5">
    <rdf:RDF>
      <cc:Work
         rdf:about="">
        <dc:format>image/svg+xml</dc:format>
        <dc:type
           rdf:resource="http://purl.org/dc/dcmitype/StillImage" />
        <dc:title></dc:title>
      </cc:Work>
    </rdf:RDF>
  </metadata>
  <g
     inkscape:label="Layer 1"
     inkscape:groupmode="layer"
     id="layer1">
    <ellipse
       id="path3713"
       cx="106.2122"
       cy="134.47203"
       rx="102.05357"
       ry="99.029755"
       style="stroke-width:0.26458332" />
    <circle
       style="fill:#ffffff;stroke-width:0.26458332"
       id="path3717"
       cx="107.59055"
       cy="132.30211"
       r="3.3341289" />
    <ellipse
       style="fill:#000000;stroke-width:0.26458332"
       id="path3719"
       cx="107.45217"
       cy="132.10078"
       rx="0.027842503"
       ry="0.031820003" />
    <text
       xml:space="preserve"
       style="font-style:normal;font-weight:normal;font-size:0.00352781px;line-height:1.25;font-family:sans-serif;letter-spacing:0px;word-spacing:0px;fill:#ffffff;fill-opacity:1;stroke:none;stroke-width:0.26458332;"
       x="107.43014"
       y="132.08501"
       id="text3723"><tspan
         sodipodi:role="line"
         x="107.43014"
         y="132.08501"
         style="font-size:0.00352781px;line-height:1.25;fill:#ffffff;stroke-width:0.26458332;"
         id="tspan3748">p </tspan><tspan
         sodipodi:role="line"
         x="107.43014"
         y="132.08942"
         style="font-size:0.00352781px;line-height:1.25;fill:#ffffff;stroke-width:0.26458332;"
         id="tspan3754">i </tspan><tspan
         sodipodi:role="line"
         x="107.43014"
         y="132.09383"
         style="font-size:0.00352781px;line-height:1.25;fill:#ffffff;stroke-width:0.26458332;"
         id="tspan3756">c </tspan><tspan
         sodipodi:role="line"
         x="107.43014"
         y="132.09824"
         style="font-size:0.00352781px;line-height:1.25;fill:#ffffff;stroke-width:0.26458332;"
         id="tspan3758">o </tspan><tspan
         sodipodi:role="line"
         x="107.43014"
         y="132.10265"
         style="font-size:0.00352781px;line-height:1.25;fill:#ffffff;stroke-width:0.26458332;"
         id="tspan3760">C </tspan><tspan
         sodipodi:role="line"
         x="107.43014"
         y="132.10706"
         style="font-size:0.00352781px;line-height:1.25;fill:#ffffff;stroke-width:0.26458332;"
         id="tspan3762">T </tspan><tspan
         sodipodi:role="line"
         x="107.43014"
         y="132.11147"
         style="font-size:0.00352781px;line-height:1.25;fill:#ffffff;stroke-width:0.26458332;"
         id="tspan3764">F { 3 n h 4 n </tspan><tspan
         sodipodi:role="line"
         x="107.43014"
         y="132.11588"
         style="font-size:0.00352781px;line-height:1.25;fill:#ffffff;stroke-width:0.26458332;"
         id="tspan3752">c 3 d _ 2 4 3 7 4 6 7 5 }</tspan></text>
  </g>
</svg>
```
#### Note
1. https://rohitchaudhary045.medium.com/picoctf-enhance-writeup-488fdce88803
2. https://ctftime.org/writeup/32917
`$ strings drawing.flag.svg`

picoCTF{3nh4nc3d_24374675}

#### Redaction Gone Wrong 
Description
Now you DON’T see me.
This report has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?
1. Select the text, copy and paste to the text editor to see the flag
* Or use the PDF text extract tool https://www.pdf2go.com/pdf-to-text
```
Financial Report for ABC Labs, Kigali, Rwanda for the year 2021.  
Breakdown - Just painted over in MS word.  
Cost Benefit Analysis 
Credit Debit 
This is not the flag, keep looking 
Expenses from the    
picoCTF{C4n_Y0u_S33_m3_fully} 
Redacted document.
```
picoCTF{C4n_Y0u_S33_m3_fully}

### Extensions 
Description \
This is a really weird text file TXT? Can you find the flag?
1. Open the `.txt` file in the Hex Editor -> see it's actually a `.png` file
2. Change its extension to `.png` to get the flag

picoCTF{now_you_know_about_extensions}

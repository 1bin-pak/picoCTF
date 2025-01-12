### Mod 26
Description
Cryptography can be easy, do you know what ROT13 is? cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_hyLicInt}
1. cryptii -> ROT13

picoCTF{next_time_I'll_try_2_rounds_of_rot13_ulYvpVag}

### The Numbers
Description
The numbers... what do they mean?
16 9 3 15 3 20 6 { 20 8 5 14 21 13 2 5 18 19 13 1 19 15 14}
1. cryptii -> a1z26-cipher

picoCTF{thenumbersmason}

A1Z26 cipher – Translate between letters and numbers
Converts alphabet characters into their corresponding alphabet order number (e.g. A=1, B=2, …, Z=26) while non-alphabet characters are being dropped.

### 13
Description
Cryptography can be easy, do you know what ROT13 is? cvpbPGS{abg_gbb_onq_bs_n_ceboyrz}
1. cryptii -> ROT13

picoCTF{not_too_bad_of_a_problem}

### interencdec
Description
Can you get the real meaning from this file.
Download the file here and open in the text editor:
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6ZzVNR3N5TXpjNWZRPT0nCg==

1. Base64 decode of:\
   YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6ZzVNR3N5TXpjNWZRPT0nCg== \
   get: \
   b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg5MGsyMzc5fQ=='
2. Base64 decode of: \
   d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg5MGsyMzc5fQ== \
   get: \
   wpjvJAM{jhlzhy_k3jy9wa3k_890k2379}
3. Caesar Cipher decode shift 19 of: \
   wpjvJAM{jhlzhy_k3jy9wa3k_890k2379}
   get: \
   picoCTF{caesar_d3cr9pt3d_890d2379}
   
### rotation
Description
You will find the flag after decrypting this file
Download the encrypted flag here:
xqkwKBN{z0bib1wv_l3kzgxb3l_949in1i1}

1. Caesar Cipher shift 18

picoCTF{r0tat1on_d3crypt3d_949af1a1}

### caesar
Description
Decrypt this message:
download the file and open it in the text editor: \
picoCTF{gvswwmrkxlivyfmgsrhnrisegl}
1. Caesar Cipher decode shift 4 and get 

picoCTF{crossingtherubicondjneoach}

### Vigenere
Description
Can you decrypt this message?
Decrypt this message using this key "CYLAB":
rgnoDVD{O0NU_WQ3_G1G3O3T3_A1AH3S_cc82272b}
1. cryptii -> Vigenere Cipher -> KEY: CYLAB

picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_ae82272q}

### substitution0
Description
A message has come in but it seems to be all scrambled. Luckily it seems to have the key at the beginning. Can you crack this substitution cipher? \
Download the message here: \
DECKFMYIQJRWTZPXGNABUSOLVH 

Ifnfuxpz Wfyndzk dnpaf, oqbi d yndsf dzk abdbfwv dqn, dzk enpuyib tf bif effbwf
mnpt d ywdaa cdaf qz oiqci qb oda fzcwpafk. Qb oda d efdubqmuw acdndedfua, dzk, db
bidb bqtf, uzrzpoz bp zdbundwqaba—pm cpunaf d ynfdb xnqhf qz d acqfzbqmqc xpqzb
pm sqfo. Bifnf ofnf bop npuzk ewdcr axpba zfdn pzf flbnftqbv pm bif edcr, dzk d
wpzy pzf zfdn bif pbifn. Bif acdwfa ofnf flcffkqzywv idnk dzk ywpaav, oqbi dww bif
dxxfdndzcf pm eunzqaifk ypwk. Bif ofqyib pm bif qzafcb oda sfnv nftdnrdewf, dzk,
bdrqzy dww biqzya qzbp cpzaqkfndbqpz, Q cpuwk idnkwv ewdtf Juxqbfn mpn iqa pxqzqpz
nfaxfcbqzy qb.

Bif mwdy qa: xqcpCBM{5UE5717U710Z_3S0WU710Z_59533D2F}

#### Hint: 
#### Try a frequency attack. An online tool might help 
1. https://www.guballa.de/substitution-solver

The flag is: picoCTF{5UB5717U710N_3V0LU710N_59533A2E}

### Rail Fence Cipher
Description
A type of transposition cipher is the rail fence cipher, which is described here. Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it? \
Download the message here: \
Ta _7N6D8Dhlg:W3D_H3C31N__387ef sHR053F38N43DFD i33___N6
Put the decoded message in the picoCTF flag format, picoCTF{decoded_message}.
1. https://www.boxentriq.com/code-breaking/rail-fence-cipher
2. Use the link above, DO NOT use Criptii since it's not accurate
3. Rails: 4, Offset:0

picoCTF{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_83F6D8D7}

### substitution1
Description
A second message has come in the mail, and it seems almost identical to the first one. Maybe the same thing will work again.
Download the message here:

ZWDg (gejfw djf zacwpfx wex dqar) afx a wscx jd zjicpwxf gxzpfbws zjicxwbwbjv. Zjvwxgwavwg afx cfxgxvwxm hbwe a gxw jd zeaqqxvrxg hebze wxgw wexbf zfxawbybws, wxzevbzaq (avm rjjrqbvr) gnbqqg, avm cfjtqxi-gjqybvr atbqbws. Zeaqqxvrxg pgpaqqs zjyxf a vpitxf jd zawxrjfbxg, avm hexv gjqyxm, xaze sbxqmg a gwfbvr (zaqqxm a dqar) hebze bg gptibwwxm wj av jvqbvx gzjfbvr gxfybzx. ZWDg afx a rfxaw has wj qxafv a hbmx affas jd zjicpwxf gxzpfbws gnbqqg bv a gadx, qxraq xvybfjvixvw, avm afx ejgwxm avm cqasxm ts iavs gxzpfbws rfjpcg afjpvm wex hjfqm djf dpv avm cfazwbzx. Djf webg cfjtqxi, wex dqar bg: cbzjZWD{DF3LP3VZS_4774ZN5_4F3_Z001_4871X6DT}

#### Hint:
#### 1. Try a frequency attack
#### 2. Do the punctuation and the individual words help you make any substitutions?
1. https://planetcalc.com/8047/
   
picoCTF{FR3XU3NCY_4774CK5_4R3_C001_4871E6FB}

### substitution1
Description A second message has come in the mail, and it seems almost identical to the first one. Maybe the same thing will work again. Download the message here:

ZWDg (gejfw djf zacwpfx wex dqar) afx a wscx jd zjicpwxf gxzpfbws zjicxwbwbjv. Zjvwxgwavwg afx cfxgxvwxm hbwe a gxw jd zeaqqxvrxg hebze wxgw wexbf zfxawbybws, wxzevbzaq (avm rjjrqbvr) gnbqqg, avm cfjtqxi-gjqybvr atbqbws. Zeaqqxvrxg pgpaqqs zjyxf a vpitxf jd zawxrjfbxg, avm hexv gjqyxm, xaze sbxqmg a gwfbvr (zaqqxm a dqar) hebze bg gptibwwxm wj av jvqbvx gzjfbvr gxfybzx. ZWDg afx a rfxaw has wj qxafv a hbmx affas jd zjicpwxf gxzpfbws gnbqqg bv a gadx, qxraq xvybfjvixvw, avm afx ejgwxm avm cqasxm ts iavs gxzpfbws rfjpcg afjpvm wex hjfqm djf dpv avm cfazwbzx. Djf webg cfjtqxi, wex dqar bg: cbzjZWD{DF3LP3VZS_4774ZN5_4F3_Z001_4871X6DT}

Hint:
1. Try a frequency attack
2. Do the punctuation and the individual words help you make any substitutions?
https://planetcalc.com/8047/

picoCTF{FR3XU3NCY_4774CK5_4R3_C001_4871E6FB}


### substitution2
Description
It seems that another encrypted message has been intercepted. The encryptor seems to have learned their lesson though and now there isn't any punctuation! Can you still crack the cipher?
Download the message here:

isnfnnpctitnznfmxhisnfwnxxntimjxctsnascdstushhxuhgqbinftnubfciruhgqnicichktckuxbackdurjnfqmifchimkabturjnfusmxxnkdnisntnuhgqnicichktehubtqfcgmfcxrhktrtingtmagckctifmichkebkamgnkimxtwscusmfnznfrbtnebxmkagmfonimjxntocxxtshwnznfwnjnxcnznisnqfhqnfqbfqhtnhemscdstushhxuhgqbinftnubfciruhgqnicichkctkhihkxrihinmuszmxbmjxntocxxtjbimxthihdnitibankitckinfntinackmkanpucinamjhbiuhgqbinftucnkunanenktcznuhgqnicichktmfnheinkxmjhfchbtmeemcftmkauhgnahwkihfbkkckdusnuoxctitmkanpnubickduhkecdtufcqitheenktnhkisnhisnfsmkactsnmzcxrehubtnahknpqxhfmichkmkacgqfhzctmichkmkaheinksmtnxngnkitheqxmrwnjnxcnznmuhgqnicichkihbusckdhkisnheenktcznnxngnkitheuhgqbinftnubfcirctisnfnehfnmjniinfznscuxnehfinusnzmkdnxctgihtibankitckmgnfcumkscdstushhxtebfisnfwnjnxcnznismimkbkanftimkackdheheenktczninuskcvbntctnttnkicmxehfghbkickdmkneenuicznanenktnmkaismiisnihhxtmkauhkecdbfmichkehubtnkuhbkinfnackanenktcznuhgqnicichktahntkhixnmatibankitihokhwisncfnkngrmtneenuicznxrmtinmusckdisngihmuicznxrisckoxconmkmiimuonfqcuhuiectmkheenktcznxrhfcnkinascdstushhxuhgqbinftnubfciruhgqnicichkismitnnotihdnknfminckinfntickuhgqbinftucnkunmghkdscdstushhxnftinmusckdisngnkhbdsmjhbiuhgqbinftnubfcirihqcvbnisncfubfchtcirghiczmickdisngihnpqxhfnhkisncfhwkmkankmjxckdisngihjniinfanenkaisncfgmusckntisnexmdctqcuhUIE{K6F4G_4K41R515_15_73A10B5_702E03EU}
Hint:
1. Try refining your frequency attack, maybe analyzing groups of letters would improve your results?
https://planetcalc.com/8047/

picoCTF{N6R4M_4N41Y515_15_73D10U5_702F03FC}

### basic-mod1
Description \
We found this weird message being passed around on the servers, we think we have a working decryption scheme. \
Download the message here.
Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore. \
Wrap your decrypted message in the picoCTF flag format (i.e. picoCTF{decrypted_message}): \
128 322 353 235 336 73 198 332 202 285 57 87 262 221 218 405 335 101 256 227 112 140 \
##### Source: 
https://github.com/noamgariani11/picoCTF-2022-Writeup/blob/main/Cryptography/basic-mod1/basic-mod1.md. 
#### Definitely needs more practice on the scripts
```
arr = [128,322,353,235,336,73,198,332,202,285,57,87,262,221,218,405,335,101,256,227,112,140 ]
characterSet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789_"
flag = "picoCTF{"

for i in range(len(arr)):
	arr[i] = arr[i] % 37
	flag += characterSet[arr[i]]

flag += "}"
print(flag)
```
picoCTF{R0UND_N_R0UND_79C18FB3}


### basic-mod2
Description
A new modular challenge!
Download the message here.
Take each number mod 41 and find the modular inverse for the result. Then map to the following character set: 1-26 are the alphabet, 27-36 are the decimal digits, and 37 is an underscore.
Wrap your decrypted message in the picoCTF flag format (i.e. picoCTF{decrypted_message}):
104 372 110 436 262 173 354 393 351 297 241 86 262 359 256 441 124 154 165 165 219 288 42

```
arr = [104,372,110,436,262,173,354,393,351,297,241,86,262,359,256,441,124,154,165,165,219,288 ,42]
characterSet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789_"
flag = "picoCTF{"

for i in range(len(arr)):
        arr[i] = pow(arr[i], -1, 41)
        flag += characterSet[arr[i]-1]

flag += "}"
print(flag)
```
picoCTF{1NV3R53LY_H4RD_DADAACAA}

### Morse-Code
Description
Morse code is well known. Can you decrypt this?
Download the file here.
Wrap your answer with picoCTF{}, put underscores in place of pauses, and use all lowercase.

1. Download the audio file
2. Upload to the website: \
   https://morsecode.world/international/decoder/audio-decoder-adaptive.html
   Get: \
   WH47 H47H 90D W20U9H7
3. Just remember, in case you get any gaps in the decoded message replace them with ‘_’, and wrap the flag with picoCTF{}
##### Source: https://h4krg33k.medium.com/picoctf-2022-cryptography-writeups-145a6f14ac6f
picoCTF{WH47_H47H_90D_W20U9H7}

### HideToSee 
Description \
How about some hide and seek heh? \
Look at this image here.
1. Go to the website:
https://futureboy.us/stegano/decinput.html \
Get the string: \
krxlXGU{zgyzhs_xizxp_05y2z65z}
2. Use AtBash Cipher decoder:
https://cryptii.com/pipes/atbash-cipher
krxlXGU{zgyzhs_xizxp_05y2z65z} -> picoCTF{atbash_crack_05b2a65a}

picoCTF{atbash_crack_05b2a65a}

### Easy1 
Description \
The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? We've given you the encrypted flag, key, and a table to help `UFJKXQZQUNB` with the key of  `SOLVECRYPTO`. Can you use this table to solve it?
1. The table indicates using Vigenère Cipher Decoder to get the Flag \
https://www.boxentriq.com/code-breaking/vigenere-cipher \
Ciphertext: UFJKXQZQUNB \
Key: SOLVECRYPTO \
Plaintext: CRYPTOISFUN

picoCTF{CRYPTOISFUN}

### La Cifra De 
Description \
I found this cipher in an old book. Can you figure out what it says? Connect with \
`nc jupiter.challenges.picoctf.org 32411`.
```
momo1126-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 32411
Encrypted message:
Ne iy nytkwpsznyg nth it mtsztcy vjzprj zfzjy rkhpibj nrkitt ltc tnnygy ysee itd tte cxjltk

Ifrosr tnj noawde uk siyyzre, yse Bnretèwp Cousex mls hjpn xjtnbjytki xatd eisjd

Iz bls lfwskqj azycihzeej yz Brftsk ip Volpnèxj ls oy hay tcimnyarqj dkxnrogpd os 1553 my Mnzvgs Mazytszf Merqlsu ny hox moup Wa inqrg ipl. Ynr. Gotgat Gltzndtg Gplrfdo 

Ltc tnj tmvqpmkseaznzn uk ehox nivmpr g ylbrj ts ltcmki my yqtdosr tnj wocjc hgqq ol fy oxitngwj arusahje fuw ln guaaxjytrd catizm tzxbkw zf vqlckx hizm ceyupcz yz tnj fpvjc hgqqpohzCZK{m311a50_0x_a1rn3x3_h1ah3x7g996649}

Ehk ktryy herq-ooizxetypd jjdcxnatoty ol f aordllvmlbkytc inahkw socjgex, bls sfoe gwzuti 1467 my Rjzn Hfetoxea Gqmexyt.

Tnj Gimjyèrk Htpnjc iy ysexjqoxj dosjeisjd cgqwej yse Gqmexyt Doxn ox Fwbkwei Inahkw.

Tn 1508, Ptsatsps Zwttnjxiax tnbjytki ehk xz-cgqwej ylbaql rkhea (g rltxni ol xsilypd gqahggpty) ysaz bzuri wazjc bk f nroytcgq nosuznkse ol yse Bnretèwp Cousex.

Gplrfdo’y xpcuso butvlky lpvjlrki tn 1555 gx l cuseitzltoty ol yse lncsz. Yse rthex mllbjd ol yse gqahggpty fce tth snnqtki cemzwaxqj, bay ehk fwpnfmezx lnj yse osoed qptzjcs gwp mocpd hd xegsd ol f xnkrznoh vee usrgxp, wnnnh ify bk itfljcety hizm paim noxwpsvtydkse.
```
1. Go to the website to get the CTF
https://www.guballa.de/vigenere-solver
```
It is interesting how in history people often receive credit for things they did not create

During the course of history, the Vigenère Cipher has been reinvented many times

It was falsely attributed to Blaise de Vigenère as it was originally described in 1553 by Giovan Battista Bellaso in his book La cifra del. Sig. Giovan Battista Bellaso 

For the implementation of this cipher a table is formed by sliding the lower half of an ordinary alphabet for an apparently random number of places with respect to the upper halfpicoCTF{b311a50_0r_v1gn3r3_c1ph3r7b996649}

The first well-documented description of a polyalphabetic cipher however, was made around 1467 by Leon Battista Alberti.
```

picoCTF{b311a50_0r_v1gn3r3_c1ph3r7b996649}

### Tapping
Description \
Theres tapping coming in from the wires. What's it saying \
`nc jupiter.challenges.picoctf.org 21610`
```
momo1126-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 21610
.--. .. -.-. --- -.-. - ..-. { -- ----- .-. ... ...-- -.-. ----- -.. ...-- .---- ... ..-. ..- -. ...-- ----. ----- ..--- ----- .---- ----. ..... .---- ----. } 
```
1. Use the Morse Code Decoder to get the CTF \
https://dencode.com/en/ 

picoCTF{M0RS3C0D31SFUN3902019519}

### Waves Over Lambda
Description \
We made a lot of substitutions to encrypt this. Can you decrypt it? Connect with `nc jupiter.challenges.picoctf.org 13758`.

```
momo1126-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 13758
-------------------------------------------------------------------------------
ancpifks xbib vs dnli jtfp - jibmlbcad_vs_a_nwbi_tfuzqf_qcwkjikfdl
-------------------------------------------------------------------------------
xfwvcp xfq snub kvub fk ud qvsonsft yxbc vc tncqnc, v xfq wvsvkbq kxb zivkvsx ulsblu, fcq ufqb sbfiax funcp kxb znnrs fcq ufos vc kxb tvzifid ibpfiqvcp kifcsdtwfcvf; vk xfq skilar ub kxfk snub jnibrcnytbqpb nj kxb anlckid anltq xfiqtd jfvt kn xfwb snub vuonikfcab vc qbftvcp yvkx f cnztbufc nj kxfk anlckid. v jvcq kxfk kxb qvskivak xb cfubq vs vc kxb bgkibub bfsk nj kxb anlckid, hlsk nc kxb zniqbis nj kxibb skfkbs, kifcsdtwfcvf, untqfwvf fcq zlrnwvcf, vc kxb uvqsk nj kxb afiofkxvfc unlckfvcs; ncb nj kxb yvtqbsk fcq tbfsk rcnyc onikvncs nj blinob. v yfs cnk fztb kn tvpxk nc fcd ufo ni ynir pvwvcp kxb bgfak tnaftvkd nj kxb afsktb qifaltf, fs kxbib fib cn ufos nj kxvs anlckid fs dbk kn anuofib yvkx nli nyc niqcfcab sliwbd ufos; zlk v jnlcq kxfk zvskivke, kxb onsk knyc cfubq zd anlck qifaltf, vs f jfvitd ybtt-rcnyc otfab. v sxftt bckbi xbib snub nj ud cnkbs, fs kxbd ufd ibjibsx ud ubunid yxbc v kftr nwbi ud kifwbts yvkx uvcf.
```
1. Use the Substitution Cipher Decoder to get the flag
https://planetcalc.com/8047/ 

```
-------------------------------------------------------------------------------
ancpifks xbib vs dnli jtfp - jibmlbcad_vs_a_nwbi_tfuzqf_qcwkjikfdl
-------------------------------------------------------------------------------
xfwvcp xfq snub kvub fk ud qvsonsft yxbc vc tncqnc, v xfq wvsvkbq kxb zivkvsx ulsblu, fcq ufqb sbfiax funcp kxb znnrs fcq ufos vc kxb tvzifid ibpfiqvcp kifcsdtwfcvf; vk xfq skilar ub kxfk snub jnibrcnytbqpb nj kxb anlckid anltq xfiqtd jfvt kn xfwb snub vuonikfcab vc qbftvcp yvkx f cnztbufc nj kxfk anlckid. v jvcq kxfk kxb qvskivak xb cfubq vs vc kxb bgkibub bfsk nj kxb anlckid, hlsk nc kxb zniqbis nj kxibb skfkbs, kifcsdtwfcvf, untqfwvf fcq zlrnwvcf, vc kxb uvqsk nj kxb afiofkxvfc unlckfvcs; ncb nj kxb yvtqbsk fcq tbfsk rcnyc onikvncs nj blinob. v yfs cnk fztb kn tvpxk nc fcd ufo ni ynir pvwvcp kxb bgfak tnaftvkd nj kxb afsktb qifaltf, fs kxbib fib cn ufos nj kxvs anlckid fs dbk kn anuofib yvkx nli nyc niqcfcab sliwbd ufos; zlk v jnlcq kxfk zvskivke, kxb onsk knyc cfubq zd anlck qifaltf, vs f jfvitd ybtt-rcnyc otfab. v sxftt bckbi xbib snub nj ud cnkbs, fs kxbd ufd ibjibsx ud ubunid yxbc v kftr nwbi ud kifwbts yvkx uvcf.

-------------------------------------------------------------------------------
CONGRATS HERE IS YOUR FLAG - FREQUENCY_IS_C_OVER_LAMBDA_DNVTFRTAYU
-------------------------------------------------------------------------------
HAVING HAD SOME TIME AT MY DISPOSAL WHEN IN LONDON, I HAD VISITED THE BRITISH MUSEUM, AND MADE SEARCH AMONG THE BOOKS AND MAPS IN THE LIBRARY REGARDING TRANSYLVANIA; IT HAD STRUCK ME THAT SOME FOREKNOWLEDGE OF THE COUNTRY COULD HARDLY FAIL TO HAVE SOME IMPORTANCE IN DEALING WITH A NOBLEMAN OF THAT COUNTRY. I FIND THAT THE DISTRICT HE NAMED IS IN THE EXTREME EAST OF THE COUNTRY, JUST ON THE BORDERS OF THREE STATES, TRANSYLVANIA, MOLDAVIA AND BUKOVINA, IN THE MIDST OF THE CARPATHIAN MOUNTAINS; ONE OF THE WILDEST AND LEAST KNOWN PORTIONS OF EUROPE. I WAS NOT ABLE TO LIGHT ON ANY MAP OR WORK GIVING THE EXACT LOCALITY OF THE CASTLE DRACULA, AS THERE ARE NO MAPS OF THIS COUNTRY AS YET TO COMPARE WITH OUR OWN ORDNANCE SURVEY MAPS; BUT I FOUND THAT BISTRITZ, THE POST TOWN NAMED BY COUNT DRACULA, IS A FAIRLY WELL-KNOWN PLACE. I SHALL ENTER HERE SOME OF MY NOTES, AS THEY MAY REFRESH MY MEMORY WHEN I TALK OVER MY TRAVELS WITH MINA.
```
#### Hint
1. Flag is not in the usual flag format
The flag is just `FREQUENCY_IS_C_OVER_LAMBDA_DNVTFRTAYU`, Don't add 'picoCTF'

FREQUENCY_IS_C_OVER_LAMBDA_DNVTFRTAYU


### John_Pollard
Description \
Sometimes RSA certificates are breakable
1. Download the certificate and input ALL the content to the Certificate Decoder
https://redkestrel.co.uk/tools/decoder
```
Certificate:
    Data:
        Version: 1 (0x0)
        Serial Number: 12345 (0x3039)
        Signature Algorithm: md2WithRSAEncryption
        Issuer: CN=PicoCTF
        Validity
            Not Before: Jul  8 07:21:18 2019 GMT
            Not After : Jun 26 17:34:38 2019 GMT
        Subject: OU=PicoCTF, O=PicoCTF, L=PicoCTF, ST=PicoCTF, C=US, CN=PicoCTF
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
                Public-Key: (53 bit)
                Modulus: 4966306421059967 (0x11a4d45212b17f)
                Exponent: 65537 (0x10001)
    Signature Algorithm: md2WithRSAEncryption
    Signature Value:
        07:6a:5d:61:32:c1:9e:05:bd:eb:77:f3:aa:fb:bb:83:82:eb:
        9e:a2:93:af:0c:2f:3a:e2:1a:e9:74:6b:9b:82:d8:ef:fe:1a:
        c8:b2:98:7b:16:dc:4c:d8:1e:2b:92:4c:80:78:85:7b:d3:cc:
        b7:d4:72:29:94:22:eb:bb:11:5d:b2:9a:af:7c:6b:cb:b0:2c:
        a7:91:87:ec:63:bd:22:e8:8f:dd:38:0e:a5:e1:0a:bf:35:d9:
        a4:3c:3c:7b:79:da:8e:4f:fc:ca:e2:38:67:45:a7:de:6e:a2:
        6e:71:71:47:f0:09:3e:1b:a0:12:35:15:a1:29:f1:59:25:35:
        a3:e4:2a:32:4c:c2:2e:b4:b5:3d:94:38:93:5e:78:37:ac:35:
        35:06:15:e0:d3:87:a2:d6:3b:c0:7f:45:2b:b6:97:8e:03:a8:
        d4:c9:e0:8b:68:a0:c5:45:ba:ce:9b:7e:71:23:bf:6b:db:cc:
        8e:f2:78:35:50:0c:d3:45:c9:6f:90:e4:6d:6f:c2:cc:c7:0e:
        de:fa:f7:48:9e:d0:46:a9:fe:d3:db:93:cb:9f:f3:32:70:63:
        cf:bc:d5:f2:22:c4:f3:be:f6:3f:31:75:c9:1e:70:2a:a4:8e:
        43:96:ac:33:6d:11:f3:ab:5e:bf:4b:55:8b:bf:38:38:3e:c1:
        25:9a:fd:5f


(Decoded using the following version of OpenSSL: OpenSSL 3.1.1 30 May 2023)
```
2. Factor the Modulus 4966306421059967 in the Integer Factorization Calculator
https://www.alpertron.com.ar/ECM.HTM
```
4966306421059967 = 67867967 × 73176001
```
3. One of the factors is p, and the other one is q
#### Hint:
1. The flag is in the format picoCTF{p,q}
2. Try swapping p and q if it does not work

picoCTF{73176001,67867967}

### ReadMyCert
Description \
How about we take you on an adventure on exploring certificate signing requests \
Take a look at this CSR file here.
1. Download and input all the contents of the certification to 
https://redkestrel.co.uk/tools/decoder

picoCTF{read_mycert_3aa80090}


### Transposition=Trial
Description \
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message. \
Download the corrupted message here. \
`heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V091B0AE}2`
1. heT -> The
1st -> 2nd; 2nd -> 3rd; 3rd -> 1st
```
flag = ''
message = "heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V091B0AE}2"
for i in range(0, len(message), 3):
		flag += message[i+2:i+3] + message[i:i+1] + message[i+1:i+2]

print(flag.split()[-1])
```
#### Reference Redo the script
https://github.com/noamgariani11/picoCTF-2022-Writeup/blob/main/Cryptography/transposition-trial/transposition-trial.md

picoCTF{7R4N5P051N6_15_3XP3N51V3_109AB02E}

### Rail-Fence
Description \
A type of transposition cipher is the rail fence cipher, which is described here. Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it? \
Download the message here. \
Put the decoded message in the picoCTF flag format, picoCTF{decoded_message}. \
`Ta _7N6D8Dhlg:W3D_H3C31N__387ef sHR053F38N43DFD i33___N6`
1. Use the Rail-Fence Decoder -> 4 rails \
https://planetcalc.com/6947/ \
`The flag is: WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_83F6D8D7`

picoCTF{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_83F6D8D7}


### Mr-Worldwide
Description \
A musician left us a message. What's it mean?
```
picoCTF{(35.028309, 135.753082)(46.469391, 30.740883)(39.758949, -84.191605)(41.015137, 28.979530)(24.466667, 54.366669)(3.140853, 101.693207)_(9.005401, 38.763611)(-3.989038, -79.203560)(52.377956, 4.897070)(41.085651, -73.858467)(57.790001, -152.407227)(31.205753, 29.924526)}
```
1. Use Reverse Geocoding to find the city names
https://developers.google.com/maps/documentation/javascript/examples/geocoding-reverse
```
35.028309, 135.753082: Kyoto
46.469391, 30.740883: Odesa
39.758949, -84.191605: Dayton
41.015137, 28.979530: Istanbul 
24.466667, 54.366669: Abu Dhabi
3.140853, 101.693207: Kuala Lumpur
_
9.005401, 38.763611: Addis Abada
-3.989038, -79.203560: Loja
52.377956, 4.897070: Amsterdam
41.085651, -73.858467: Sleepy Hollow
57.790001, -152.407227: Kodiak
31.205753, 29.924526: Alexandria
```
2. Pick the 1st letter of each city to get the flag
```
KODIAK_ALASKA
```
picoCTF{KODIAK_ALASKA}

### Flags
Description \
What do the flags mean?
1. Navy Signal Code \
https://www.dcode.fr/maritime-signals-code

PICOCTF{F1AG5AND5TUFF}

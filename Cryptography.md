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


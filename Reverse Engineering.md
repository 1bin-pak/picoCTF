### Transformation
Description
I wonder what this really is... enc \
灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸彥㜰㍢㐸㙽 \
''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])
1. Go to CyberChef -> Text Encoding Brute Force
2. UTF-16BE (1201) to get the flag
   
picoCTF{16_bits_inst34d_of_8_e703b486}

### Safe Opener
Description \
Can you open this safe? \
I forgot the key to my safe but this program is supposed to help me with retrieving the lost key. Can you help me unlock my safe? \
Put the password you recover into the picoCTF flag format like: \
picoCTF{password}
```
import java.io.*;
import java.util.*;  
public class SafeOpener {
    public static void main(String args[]) throws IOException {
        BufferedReader keyboard = new BufferedReader(new InputStreamReader(System.in));
        Base64.Encoder encoder = Base64.getEncoder();
        String encodedkey = "";
        String key = "";
        int i = 0;
        boolean isOpen;
        

        while (i < 3) {
            System.out.print("Enter password for the safe: ");
            key = keyboard.readLine();

            encodedkey = encoder.encodeToString(key.getBytes());
            System.out.println(encodedkey);
              
            isOpen = openSafe(encodedkey);
            if (!isOpen) {
                System.out.println("You have  " + (2 - i) + " attempt(s) left");
                i++;
                continue;
            }
            break;
        }
    }
    
    public static boolean openSafe(String password) {
        String encodedkey = "cGwzYXMzX2wzdF9tM18xbnQwX3RoM19zYWYz";
        
        if (password.equals(encodedkey)) {
            System.out.println("Sesame open");
            return true;
        }
        else {
            System.out.println("Password is incorrect\n");
            return false;
        }
    }
}
```
1. Use Base64 (mentioned in the code)
2. Decode the encodedkey string to get the CTF `cGwzYXMzX2wzdF9tM18xbnQwX3RoM19zYWYz`
pl3as3_l3t_m3_1nt0_th3_saf3

picoCTF{pl3as3_l3t_m3_1nt0_th3_saf3}

### Safe Opener 2
Description \
What can you do with this file? \
I forgot the key to my safe but this file is supposed to help me with retrieving the lost key.  Can you help me unlock my safe?
1. Download the file
2. Open with the text editor to get the flag

picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_7db9fb8c}

### Reverse 
Description \
Try reversing this file? Can ya? \
I forgot the password to this file. Please find it for me?
1. Download the file
2. Open it in a text editor to get the flag

picoCTF{3lf_r3v3r5ing_succe55ful_d7b14d43}

### Vault-Door-1 
Description \
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: VaultDoor1.java
1. Get the following part of the source code
```
// I came up with a more secure way to check the password without putting
    // the password itself in the source code. I think this is going to be
    // UNHACKABLE!! I hope Dr. Evil agrees...
    //
    // -Minion #8728
    public boolean checkPassword(String password) {
        return password.length() == 32 &&
               password.charAt(0)  == 'd' &&
               password.charAt(29) == '9' &&
               password.charAt(4)  == 'r' &&
               password.charAt(2)  == '5' &&
               password.charAt(23) == 'r' &&
               password.charAt(3)  == 'c' &&
               password.charAt(17) == '4' &&
               password.charAt(1)  == '3' &&
               password.charAt(7)  == 'b' &&
               password.charAt(10) == '_' &&
               password.charAt(5)  == '4' &&
               password.charAt(9)  == '3' &&
               password.charAt(11) == 't' &&
               password.charAt(15) == 'c' &&
               password.charAt(8)  == 'l' &&
               password.charAt(12) == 'H' &&
               password.charAt(20) == 'c' &&
               password.charAt(14) == '_' &&
               password.charAt(6)  == 'm' &&
               password.charAt(24) == '5' &&
               password.charAt(18) == 'r' &&
               password.charAt(13) == '3' &&
               password.charAt(19) == '4' &&
               password.charAt(21) == 'T' &&
               password.charAt(16) == 'H' &&
               password.charAt(27) == '5' &&
               password.charAt(30) == '2' &&
               password.charAt(25) == '_' &&
               password.charAt(22) == '3' &&
               password.charAt(28) == '0' &&
               password.charAt(26) == '7' &&
               password.charAt(31) == 'e';
    }
```
2. Sort by the index --> sort by charAt() in Java
```
password.charAt(0)  == 'd' &&
password.charAt(1)  == '3' &&
password.charAt(2)  == '5' &&
password.charAt(3)  == 'c' &&
password.charAt(4)  == 'r' &&
password.charAt(5)  == '4' &&
password.charAt(6)  == 'm' &&
password.charAt(7)  == 'b' &&
password.charAt(8)  == 'l' &&
password.charAt(9)  == '3' &&
password.charAt(10) == '_' &&
password.charAt(11) == 't' &&
password.charAt(12) == 'H' &&
password.charAt(13) == '3' &&
password.charAt(14) == '_' &&
password.charAt(15) == 'c' &&
password.charAt(16) == 'H' &&
password.charAt(17) == '4' &&
password.charAt(18) == 'r' &&
password.charAt(19) == '4' &&
password.charAt(20) == 'c' &&
password.charAt(21) == 'T' &&
password.charAt(22) == '3' &&
password.charAt(23) == 'r' &&
password.charAt(24) == '5' &&
password.charAt(25) == '_' &&
password.charAt(26) == '7' &&
password.charAt(27) == '5' &&
password.charAt(28) == '0' &&
password.charAt(29) == '9' &&
password.charAt(30) == '2' &&
password.charAt(31) == 'e'
```
3. Concatenate the characters to get the string to get the flag
`d35cr4mbl3_tH3_CH4r4cT3r5_75092e`

#### Hint:
1. Look up the charAt() method online.


picoCTF{d35cr4mbl3_tH3_CH4r4cT3r5_75092e}

### Valut-Door-3 
Description \
This vault uses for-loops and byte arrays. The source code for this vault is here: VaultDoor3.java
1. Understand the logic of the origional code
```
0 < i < 8: i
8 <= i < 16: 23 - i
16 <= i < 32 step 2: 46 - i
31 >= x > 16 step -2: i

"Step 3: Key Observations and Adjustments
Python For Loops vs. Java For Loops:
In Java, the condition i >= 17 allows the loop to include index 17. However, in Python, the range function excludes the endpoint. To replicate the behavior, I adjusted the range to go from 31 to 16 in steps of -2."
https://medium.com/@sobatistacyber/picoctf-writeups-vault-door-3-86f9d578f87e
```
```
// Our security monitoring team has noticed some intrusions on some of the
    // less secure doors. Dr. Evil has asked me specifically to build a stronger
    // vault door to protect his Doomsday plans. I just *know* this door will
    // keep all of those nosy agents out of our business. Mwa ha!
    //
    // -Minion #2671
    public boolean checkPassword(String password) {
        if (password.length() != 32) {
            return false;
        }
        char[] buffer = new char[32];
        int i;
        for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
        }
        for (; i<32; i+=2) {
            buffer[i] = password.charAt(46-i);
        }
        for (i=31; i>=17; i-=2) {
            buffer[i] = password.charAt(i);
        }
        String s = new String(buffer);
        return s.equals("jU5t_a_sna_3lpm18g947_u_4_m9r54f");
    }
```
2. Write the code to find the origional string
```
def checkPassword(password):
    if not len(password) == 32:
        return False
    buffer = [""] * 32

    for i in range(8):
        buffer[i] = password[i]

    for i in range(8, 16):
        buffer[i] = password[23 - i]
    
    for i in range(16, 32, 2):
        buffer[i] = password[46 - i]
    
    for i in range(31, 16, -2):
        buffer[i] = password[i]
    print(''.join(buffer))  # Combine and print the reconstructed password

checkPassword("jU5t_a_sna_3lpm18g947_u_4_m9r54f")
```
#### Reference
https://medium.com/@sobatistacyber/picoctf-writeups-vault-door-3-86f9d578f87e

picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_79958f}


### Vault-Door-4 
Description \
This vault uses ASCII encoding for the password. The source code for this vault is here: VaultDoor4.java
1. Understand the logic of the origional code
```
// I made myself dizzy converting all of these numbers into different bases,
    // so I just *know* that this vault will be impenetrable. This will make Dr.
    // Evil like me better than all of the other minions--especially Minion
    // #5620--I just know it!
    //
    //  .:::.   .:::.
    // :::::::.:::::::
    // :::::::::::::::
    // ':::::::::::::'
    //   ':::::::::'
    //     ':::::'
    //       ':'
    // -Minion #7781
    public boolean checkPassword(String password) {
        byte[] passBytes = password.getBytes();
        byte[] myBytes = {
            106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
            0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
            0142, 0131, 0164, 063 , 0163, 0137, 070 , 0146,
            '4' , 'a' , '6' , 'c' , 'b' , 'f' , '3' , 'b' ,
        };
        for (int i=0; i<32; i++) {
            if (passBytes[i] != myBytes[i]) {
                return false;
            }
        }
        return true;
    }
```
2. Write the code of the origional string
```
def checkPassword():
    password = ''
    # 0142, 0131, 0164, 063 , 0163, 0137, 070 , 0146 
    # An octal integer literal begins with the digit 0 and contains any of the digits 0 through 7
    # 0O octal-digit so use octal-digit instead, otherwise will cause a syntax error
    # Use: 0o142, 0o131, 0o164, 0o63 , 0o163, 0o137, 0o70 , 0o146
    num = [106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
            0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
            0o142, 0o131, 0o164, 0o63 , 0o163, 0o137, 0o70 , 0o146]
    for n in num:
        password += chr(n)
    char = ['4' , 'a' , '6' , 'c' , 'b' , 'f' , '3' , 'b']
    password = ''.join(password) # jU5t_4_bUnCh_0f_bYt3s_8f
    char = ''.join(char) # 4a6cbf3b
    print('picoCTF{' + password + char + '}')

checkPassword()
```
#### Note
1. An octal integer literal begins with the digit 0 and contains any of the digits 0 through 7
2. 0o octal-digit -> have to change all the octal literal to octal-digit \
eg change 0142 to 0o142 to avoid the SyntaxError
3. Hex: prefix: 0x \
Octal: prefix: 0
4. __The following literals all specify the same number__
```
int literal_octal_prefered          = 0o52;
int literal_octal_to_be_deprecated  = 052;
int literal_decimal                 = 42;
int literal_hex                     = 0x2A;
int literal_binary                  = 0b00101010;
```
#### Reference
https://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0085r0.html

picoCTF{jU5t_4_bUnCh_0f_bYt3s_8f4a6cbf3b}

### Vault-Door-5 
Description \
In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: VaultDoor5.java
1. Understand the logic of the origional code
```
// Minion #7781 used base 8 and base 16, but this is base 64, which is
    // like... eight times stronger, right? Riiigghtt? Well that's what my twin
    // brother Minion #2415 says, anyway.
    //
    // -Minion #2414
    public String base64Encode(byte[] input) {
        return Base64.getEncoder().encodeToString(input);
    }

    // URL encoding is meant for web pages, so any double agent spies who steal
    // our source code will think this is a web site or something, defintely not
    // vault door! Oh wait, should I have not said that in a source code
    // comment?
    //
    // -Minion #2415
    public String urlEncode(byte[] input) {
        StringBuffer buf = new StringBuffer();
        for (int i=0; i<input.length; i++) {
            buf.append(String.format("%%%2x", input[i]));
        }
        return buf.toString();
    }

    public boolean checkPassword(String password) {
        String urlEncoded = urlEncode(password.getBytes());
        String base64Encoded = base64Encode(urlEncoded.getBytes());
        String expected = "JTYzJTMwJTZlJTc2JTMzJTcyJTc0JTMxJTZlJTY3JTVm"
                        + "JTY2JTcyJTMwJTZkJTVmJTYyJTYxJTM1JTY1JTVmJTM2"
                        + "JTM0JTVmJTY1JTMzJTMxJTM1JTMyJTYyJTY2JTM0";
        return base64Encoded.equals(expected);
```
2. Write the code to get the origional string
new string: urlEncode -> base64Encode
old string: base64Decode -> urlDecode

Enter the new string into \
https://toolbox.googleapps.com/apps/encode_decode/ Base64 Decode of
```
JTYzJTMwJTZlJTc2JTMzJTcyJTc0JTMxJTZlJTY3JTVm
JTY2JTcyJTMwJTZkJTVmJTYyJTYxJTM1JTY1JTVmJTM2
JTM0JTVmJTY1JTMzJTMxJTM1JTMyJTYyJTY2JTM0
```
Get
```
%63%30%6e%76%33%72%74%31%6e%67%5f%66%72%30%6d%5f%62%61%35%65%5f%36%34%5f%65%33%31%35%32%62%66%34
```

Go to https://www.urldecoder.org/ \
URL Decode of
```
%63%30%6e%76%33%72%74%31%6e%67%5f%66%72%30%6d%5f%62%61%35%65%5f%36%34%5f%65%33%31%35%32%62%66%34
```
Get
```
c0nv3rt1ng_fr0m_ba5e_64_e3152bf4
```
picoCTF{c0nv3rt1ng_fr0m_ba5e_64_e3152bf4}

### Vault-Door-6 
Description \
This vault uses an XOR encryption scheme. The source code for this vault is here: VaultDoor6.java
1. Understand the logic of the origional code
```
// Dr. Evil gave me a book called Applied Cryptography by Bruce Schneier,
    // and I learned this really cool encryption system. This will be the
    // strongest vault door in Dr. Evil's entire evil volcano compound for sure!
    // Well, I didn't exactly read the *whole* book, but I'm sure there's
    // nothing important in the last 750 pages.
    //
    // -Minion #3091
    public boolean checkPassword(String password) {
        if (password.length() != 32) {
            return false;
        }
        byte[] passBytes = password.getBytes();
        byte[] myBytes = {
            0x3b, 0x65, 0x21, 0xa , 0x38, 0x0 , 0x36, 0x1d,
            0xa , 0x3d, 0x61, 0x27, 0x11, 0x66, 0x27, 0xa ,
            0x21, 0x1d, 0x61, 0x3b, 0xa , 0x2d, 0x65, 0x27,
            0xa , 0x6c, 0x61, 0x6d, 0x37, 0x6d, 0x6d, 0x6d,
        };
        for (int i=0; i<32; i++) {
            if (((passBytes[i] ^ 0x55) - myBytes[i]) != 0) {
                return false;
            }
        }
        return true;
    }
```
2. Write the code to get the origional string
```
def checkPassword():
    password = ''
    res = []
    num = [0x3b, 0x65, 0x21, 0xa , 0x38, 0x0 , 0x36, 0x1d,
            0xa , 0x3d, 0x61, 0x27, 0x11, 0x66, 0x27, 0xa ,
            0x21, 0x1d, 0x61, 0x3b, 0xa , 0x2d, 0x65, 0x27,
            0xa , 0x6c, 0x61, 0x6d, 0x37, 0x6d, 0x6d, 0x6d]
    for n in num:
        n ^= 0x55
        res.append(chr(n))
    print(''.join(res))

checkPassword()
```
picoCTF{n0t_mUcH_h4rD3r_tH4n_x0r_948b888}

### Vault-Door-7 (RE) ????
https://captainmich.github.io/programming_language/CTF/Challenge/picoCTF2019/reverse_engineering.html

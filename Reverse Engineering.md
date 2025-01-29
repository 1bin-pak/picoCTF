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


### Vault-Door-7 
Description \
This vault uses bit shifts to convert a password string into an array of integers. Hurry, agent, we are running out of time to stop Dr. Evil's nefarious plans! The source code for this vault is here: VaultDoor7.java
1. Understand the origional code
```
// Each character can be represented as a byte value using its
    // ASCII encoding. Each byte contains 8 bits, and an int contains
    // 32 bits, so we can "pack" 4 bytes into a single int. Here's an
    // example: if the hex string is "01ab", then those can be
    // represented as the bytes {0x30, 0x31, 0x61, 0x62}. When those
    // bytes are represented as binary, they are:
    //
    // 0x30: 00110000
    // 0x31: 00110001
    // 0x61: 01100001
    // 0x62: 01100010
    //
    // If we put those 4 binary numbers end to end, we end up with 32
    // bits that can be interpreted as an int.
    //
    // 00110000001100010110000101100010 -> 808542562
    //
    // Since 4 chars can be represented as 1 int, the 32 character password can
    // be represented as an array of 8 ints.
    //
    // - Minion #7816
    public int[] passwordToIntArray(String hex) {
        int[] x = new int[8];
        byte[] hexBytes = hex.getBytes();
        for (int i=0; i<8; i++) {
            x[i] = hexBytes[i*4]   << 24
                 | hexBytes[i*4+1] << 16
                 | hexBytes[i*4+2] << 8
                 | hexBytes[i*4+3];
        }
        return x;
    }

    public boolean checkPassword(String password) {
        if (password.length() != 32) {
            return false;
        }
        int[] x = passwordToIntArray(password);
        return x[0] == 1096770097
            && x[1] == 1952395366
            && x[2] == 1600270708
            && x[3] == 1601398833
            && x[4] == 1716808014
            && x[5] == 1734293296
            && x[6] == 842413104
            && x[7] == 1684157793;
    }
```
2. int -> hex (get rid of prefix)
```
int_num = [1096770097, 1952395366, 1600270708, 1601398833, 1716808014, 1734293296, 842413104
,1684157793]
for d in int_num:
    # Get rid of the prefix: [2:]
    hex_num = hex(d)[2:]
    print(hex_num)
```
Get
```
415f6231
745f3066
5f623174
5f736831
6654694e
675f3730
32363430
64623561
```
3. hex -> ASCII \
Go to https://www.rapidtables.com/convert/number/hex-to-ascii.html \
Get `A_b1t_0f_b1t_sh1fTiNg_702640db5a`

#### Hint
1. Use a decimal/hexadecimal converter such as this one: https://www.mathsisfun.com/binary-decimal-hexadecimal-converter.html
2. You will also need to consult an ASCII table such as this one: https://www.asciitable.com/

#### Reference
https://www.youtube.com/watch?v=0qQckH67gmw&t=148s

picoCTF{A_b1t_0f_b1t_sh1fTiNg_702640db5a}

### Vault-Door-8 
Description \
Apparently Dr. Evil's minions knew that our agency was making copies of their source code, because they intentionally sabotaged this source code in order to make it harder for our agents to analyze and crack into! The result is a quite mess, but I trust that my best special agent will find a way to solve it. The source code for this vault is here: VaultDoor8.java
1. Beautify the code
https://www.onlinegdb.com/online_java_compiler#
2. Understand the logic of the origional code
```
public char[] scramble(String password) {/* Scramble a password by transposing pairs of bits. */
		char[] a = password.toCharArray();
		for (int b=0; b<a.length; b++) {
			char c = a[b];
			c = switchBits(c,1,2);
			c = switchBits(c,0,3); /* c = switchBits(c,14,3); c = switchBits(c, 2, 0); */ 
			c = switchBits(c,5,6);
			c = switchBits(c,4,7);
			c = switchBits(c,0,1); /* d = switchBits(d, 4, 5); e = switchBits(e, 5, 6); */ 
			c = switchBits(c,3,4);
			c = switchBits(c,2,5);
			c = switchBits(c,6,7);
			a[b] = c;
		}
		return a;
	} public char switchBits(char c, int p1, int p2) {
		/* Move the bit in position p1 to position p2, and move the bit
		that was in position p2 to position p1. Precondition: p1 < p2 */ 
		char mask1 = (char)(1 << p1);
		char mask2 = (char)(1 << p2); /* char mask3 = (char)(1<<p1<<p2); mask1++; mask1--; */ 
		char bit1 = (char)(c & mask1);
		char bit2 = (char)(c & mask2); /* System.out.println("bit1 " + Integer.toBinaryString(bit1));
System.out.println("bit2 " + Integer.toBinaryString(bit2)); */ 
        char rest = (char)(c & ~(mask1 | mask2));
		char shift = (char)(p2 - p1);
		char result = (char)((bit1<<shift) | (bit2>>shift) | rest);
		return result;
		
	} public boolean checkPassword(String password) {
		char[] scrambled = scramble(password);
		char[] expected = {
			0xF4, 0xC0, 0x97, 0xF0, 0x77, 0x97, 0xC0, 0xE4, 0xF0, 0x77, 0xA4, 0xD0, 0xC5, 0x77, 0xF4, 0x86, 0xD0, 0xA5, 0x45, 0x96, 0x27, 0xB5, 0x77, 0xD2, 0xD0, 0xB4, 0xE1, 0xC1, 0xE0, 0xD0, 0xD0, 0xE0
		};
		return Arrays.equals(scrambled, expected);
	}
```
Python Version
```
class VaultDoor8:
    def main(self):
        password = input("Enter vault password: ")
        stripped_password = password[8:-1]
        if self.check_password(stripped_password):
            print("Access granted.")
        else:
            print("Access denied!")

    def scramble(self, password):
        a = list(password)
        for i in range(len(a)):
            c = a[i]
            c = self.switch_bits(c, 1, 2)
            c = self.switch_bits(c, 0, 3)
            c = self.switch_bits(c, 5, 6)
            c = self.switch_bits(c, 4, 7)
            c = self.switch_bits(c, 0, 1)
            c = self.switch_bits(c, 3, 4)
            c = self.switch_bits(c, 2, 5)
            c = self.switch_bits(c, 6, 7)
            a[i] = c
        return ''.join(a)

    def switch_bits(self, c, p1, p2):
        mask1 = 1 << p1
        mask2 = 1 << p2
        bit1 = ord(c) & mask1
        bit2 = ord(c) & mask2
        rest = ord(c) & ~(mask1 | mask2)
        shift = p2 - p1
        result = (bit1 << shift) | (bit2 >> shift) | rest
        return chr(result)

    def check_password(self, password):
        scrambled = self.scramble(password)
        expected = [
            0xF4, 0xC0, 0x97, 0xF0, 0x77, 0x97, 0xC0, 0xE4,
            0xF0, 0x77, 0xA4, 0xD0, 0xC5, 0x77, 0xF4, 0x86,
            0xD0, 0xA5, 0x45, 0x96, 0x27, 0xB5, 0x77, 0xD2,
            0xD0, 0xB4, 0xE1, 0xC1, 0xE0, 0xD0, 0xD0, 0xE0
        ]
        return list(map(ord, scrambled)) == expected

# Create an instance of VaultDoor8 and run the main method
vault = VaultDoor8()
vault.main()
```
3. Pay attention to the switchBits() of the code. Just reverse the orders to get the order that the question wants
```
class VaultDoor8:
    def main(self):
        user_input = "picoCTF{"
        user_input += self.unScramble()
        user_input += "}"

        print("Reverse Password: " + user_input)
        print("Enter vault password: " + user_input)
        input_password = user_input[len("picoCTF{"):-1]

        if self.check_password(input_password):
            print("Access granted.")
        else:
            print("Access denied!")

    def unScramble(self):
        expected = [0xF4, 0xC0, 0x97, 0xF0, 0x77, 0x97, 0xC0, 0xE4, 0xF0, 0x77, 0xA4, 0xD0, 0xC5, 0x77, 0xF4, 0x86, 0xD0, 0xA5, 0x45, 0x96, 0x27, 0xB5, 0x77, 0xD2, 0xD0, 0xB4, 0xE1, 0xC1, 0xE0, 0xD0, 0xD0, 0xE0]
        for i in range(len(expected)):
            c = expected[i]
            c = self.switch_bits(c, 6, 7)
            c = self.switch_bits(c, 2, 5)
            c = self.switch_bits(c, 3, 4)
            c = self.switch_bits(c, 0, 1)
            c = self.switch_bits(c, 4, 7)
            c = self.switch_bits(c, 5, 6)
            c = self.switch_bits(c, 0, 3)
            c = self.switch_bits(c, 1, 2)
            expected[i] = c
        return ''.join(chr(e) for e in expected)

    def scramble(self, password):
        a = list(password)
        for i in range(len(a)):
            c = ord(a[i])
            c = self.switch_bits(c, 6, 7)
            c = self.switch_bits(c, 2, 5)
            c = self.switch_bits(c, 3, 4)
            c = self.switch_bits(c, 0, 1)
            c = self.switch_bits(c, 4, 7)
            c = self.switch_bits(c, 5, 6)
            c = self.switch_bits(c, 0, 3)
            c = self.switch_bits(c, 1, 2)
            a[i] = chr(c)
        return ''.join(a)

    def switch_bits(self, c, p1, p2):
        mask1 = 1 << p1
        mask2 = 1 << p2
        bit1 = c & mask1
        bit2 = c & mask2
        rest = c & ~(mask1 | mask2)
        shift = p2 - p1
        result = (bit1 << shift) | (bit2 >> shift) | rest
        return result

    def check_password(self, password):
        scrambled = self.scramble(password)
        expected = [
            0xF4, 0xC0, 0x97, 0xF0, 
			0x77, 0x97, 0xC0, 0xE4, 
			0xF0, 0x77, 0xA4, 0xD0, 
			0xC5, 0x77, 0xF4, 0x86, 
			0xD0, 0xA5, 0x45, 0x96, 
			0x27, 0xB5, 0x77, 0xD2, 
			0xD0, 0xB4, 0xE1, 0xC1, 
			0xE0, 0xD0, 0xD0, 0xE0
        ]
        return list(map(ord, scrambled)) == expected


# Create an instance of VaultDoor8 and run the main method
vault = VaultDoor8()
vault.main()

"""
Reverse Password: picoCTF{s0m3_m0r3_b1t_sh1fTiNg_91c642112}
Enter vault password: picoCTF{s0m3_m0r3_b1t_sh1fTiNg_91c642112}
Access denied!
"""
```
#### Understand, REDO

#### Reference
https://johantannh.github.io/picoctf2019-writeup/reversing/
https://www.youtube.com/watch?v=KP83DLVbD2Y&t=280s

picoCTF{s0m3_m0r3_b1t_sh1fTiNg_91c642112}


### Unpackme.py 
Description \
Can you get the flag? \
Reverse engineer this `Python program`.
1. change `exec(plain.decode())` to `print(plain.decode())` to run it as a script instead of the exec file to get the flag
2. Use this website to run the `Cryptography` library online
https://onecompiler.com/python/3vj2haaqr
```
import base64
from cryptography.fernet import Fernet


payload = b'gAAAAABkzWGSzE6VQNTzvRXOXekQeW4CY6NiRkzeImo9LuYBHAYw_hagTJLJL0c-kmNsjY33IUbU2IWlqxA3Fpp9S7RxNkiwMDZgLmRlI9-lGAEW-_i72RSDvylNR3QkpJW2JxubjLUC5VwoVgH62wxDuYu1rRD5KadwTADdABqsx2MkY6fKNTMCYY09Se6yjtRBftfTJUL-LKz2bwgXNd6O-WpbfXEMvCv3gNQ7sW4pgUnb-gDVZvrLNrug_1YFaIe3yKr0Awo0HIN3XMdZYpSE1c9P4G0sMQ=='

key_str = 'correctstaplecorrectstaplecorrec'
key_base64 = base64.b64encode(key_str.encode())  base64.b64encode: then b64 encode it
f = Fernet(key_base64)
plain = f.decrypt(payload)
print(plain.decode()) 
# exec(plain.decode())
```
picoCTF{175_chr157m45_cd82f94c}

### Fresh Java   
Description \
Can you get the flag? \
Reverse engineer this Java program.
1. Download the `.class` file
2. Use the `decomplier` https://www.decompiler.com/ \
to see the `.java` file to get the flag
```
import java.util.Scanner;

public class KeygenMe {
   public static void main(String[] var0) {
      Scanner var1 = new Scanner(System.in);
      System.out.println("Enter key:");
      String var2 = var1.nextLine();
      if (var2.length() != 34) {
         System.out.println("Invalid key");
      } else if (var2.charAt(33) != '}') {
         System.out.println("Invalid key");
      } else if (var2.charAt(32) != 'e') {
         System.out.println("Invalid key");
      } else if (var2.charAt(31) != 'b') {
         System.out.println("Invalid key");
      } else if (var2.charAt(30) != '6') {
         System.out.println("Invalid key");
      } else if (var2.charAt(29) != 'a') {
         System.out.println("Invalid key");
      } else if (var2.charAt(28) != '2') {
         System.out.println("Invalid key");
      } else if (var2.charAt(27) != '3') {
         System.out.println("Invalid key");
      } else if (var2.charAt(26) != '3') {
         System.out.println("Invalid key");
      } else if (var2.charAt(25) != '9') {
         System.out.println("Invalid key");
      } else if (var2.charAt(24) != '_') {
         System.out.println("Invalid key");
      } else if (var2.charAt(23) != 'd') {
         System.out.println("Invalid key");
      } else if (var2.charAt(22) != '3') {
         System.out.println("Invalid key");
      } else if (var2.charAt(21) != 'r') {
         System.out.println("Invalid key");
      } else if (var2.charAt(20) != '1') {
         System.out.println("Invalid key");
      } else if (var2.charAt(19) != 'u') {
         System.out.println("Invalid key");
      } else if (var2.charAt(18) != 'q') {
         System.out.println("Invalid key");
      } else if (var2.charAt(17) != '3') {
         System.out.println("Invalid key");
      } else if (var2.charAt(16) != 'r') {
         System.out.println("Invalid key");
      } else if (var2.charAt(15) != '_') {
         System.out.println("Invalid key");
      } else if (var2.charAt(14) != 'g') {
         System.out.println("Invalid key");
      } else if (var2.charAt(13) != 'n') {
         System.out.println("Invalid key");
      } else if (var2.charAt(12) != '1') {
         System.out.println("Invalid key");
      } else if (var2.charAt(11) != 'l') {
         System.out.println("Invalid key");
      } else if (var2.charAt(10) != '0') {
         System.out.println("Invalid key");
      } else if (var2.charAt(9) != '0') {
         System.out.println("Invalid key");
      } else if (var2.charAt(8) != '7') {
         System.out.println("Invalid key");
      } else if (var2.charAt(7) != '{') {
         System.out.println("Invalid key");
      } else if (var2.charAt(6) != 'F') {
         System.out.println("Invalid key");
      } else if (var2.charAt(5) != 'T') {
         System.out.println("Invalid key");
      } else if (var2.charAt(4) != 'C') {
         System.out.println("Invalid key");
      } else if (var2.charAt(3) != 'o') {
         System.out.println("Invalid key");
      } else if (var2.charAt(2) != 'c') {
         System.out.println("Invalid key");
      } else if (var2.charAt(1) != 'i') {
         System.out.println("Invalid key");
      } else if (var2.charAt(0) != 'p') {
         System.out.println("Invalid key");
      } else {
         System.out.println("Valid key");
      }
   }
}
```
#### Hint
1. Use a decompiler for Java!

#### Note
1. A Java class file is a file containing Java bytecode and having .class extension that can be executed by JVM \
https://www.geeksforgeeks.org/java-class-file/
2. A decompiler is a computer program that converts an executable file into a high-level source code \
https://medium.com/@pnfsoftware/what-is-decompilation-26ce48f282bc

picoCTF{700l1ng_r3qu1r3d_9332a6be}

### File-Run1 
Description \
A program has been provided to you, what happens if you try to run it on the command line? \
Download the program here.
1. Download the file -> Change permission -> Run it
```
momo1126-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/218/run
--2025-01-18 05:52:07--  https://artifacts.picoctf.net/c/218/run
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.93, 3.160.5.42, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.93|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16736 (16K) [application/octet-stream]
Saving to: 'run'

run                                          100%[==============================================================================================>]  16.34K  --.-KB/s    in 0.004s  

2025-01-18 05:52:07 (3.80 MB/s) - 'run' saved [16736/16736]

momo1126-picoctf@webshell:~$ ls
README.txt  anthem.flag.txt  run
momo1126-picoctf@webshell:~$ ls -l
total 136
-rw-r--r-- 1 root             root               4443 Jan 18 05:51 README.txt
-rw-rw-r-- 1 momo1126-picoctf momo1126-picoctf 108668 Mar 16  2023 anthem.flag.txt
-rw-rw-r-- 1 momo1126-picoctf momo1126-picoctf  16736 Mar 16  2023 run
momo1126-picoctf@webshell:~$ chmod +x run
momo1126-picoctf@webshell:~$ ls -l
total 136
-rw-r--r-- 1 root             root               4443 Jan 18 05:51 README.txt
-rw-rw-r-- 1 momo1126-picoctf momo1126-picoctf 108668 Mar 16  2023 anthem.flag.txt
-rwxrwxr-x 1 momo1126-picoctf momo1126-picoctf  16736 Mar 16  2023 run
momo1126-picoctf@webshell:~$ ./run
The flag is: picoCTF{U51N6_Y0Ur_F1r57_F113_9bc52b6b}
```
#### Hint
1. To run the program at all, you must make it executable (i.e. $ chmod +x run)
2. Try running it by adding a '.' in front of the path to the file (i.e. $ ./run)

#### Note
https://askubuntu.com/questions/530198/how-to-open-bash-files-with-terminal

picoCTF{U51N6_Y0Ur_F1r57_F113_9bc52b6b}

### File-Run2 
Description \
Another program, but this time, it seems to want some input. What happens if you try to run it on the command line with input "Hello!"? \
Download the program here.
1. Download the file -> Change permissions -> Run it with the input "Hello!"
```
momo1126-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/155/run
--2025-01-18 06:10:37--  https://artifacts.picoctf.net/c/155/run
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.93, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16816 (16K) [application/octet-stream]
Saving to: 'run.1'

run.1                                       100%[=========================================================================================>]  16.42K  --.-KB/s    in 0s      

2025-01-18 06:10:37 (95.7 MB/s) - 'run.1' saved [16816/16816]

momo1126-picoctf@webshell:~$ ls
README.txt  anthem.flag.txt  run  run.1
momo1126-picoctf@webshell:~$ ls -l
total 156
-rw-r--r-- 1 root             root               4443 Jan 18 05:51 README.txt
-rw-rw-r-- 1 momo1126-picoctf momo1126-picoctf 108668 Mar 16  2023 anthem.flag.txt
-rwxrwxr-x 1 momo1126-picoctf momo1126-picoctf  16736 Mar 16  2023 run
-rw-rw-r-- 1 momo1126-picoctf momo1126-picoctf  16816 Mar 16  2023 run.1
momo1126-picoctf@webshell:~$ chmod +x run.1 
momo1126-picoctf@webshell:~$ ./run.1 
Run this file with only one argument.

momo1126-picoctf@webshell:~$ ./run.1 Sup
Won't you say 'Hello!' to me first?
momo1126-picoctf@webshell:~$ ./run.1 Hello
Won't you say 'Hello!' to me first?
momo1126-picoctf@webshell:~$ ./run.1 Hello!
The flag is: picoCTF{F1r57_4rgum3n7_be0714da}
```
#### Hint
1. Try running it and add the phrase "Hello!" with a space in front (i.e. "./run Hello!")

#### Note
1. There's no space between `./` and `run.1`
```
momo1126-picoctf@webshell:~$ "./ run.1 Sup"
-bash: ./ run.1 Sup: No such file or directory

momo1126-picoctf@webshell:~$ ./run.1 Sup
Won't you say 'Hello!' to me first?
```

picoCTF{F1r57_4rgum3n7_be0714da}

### Crackme-py 
Description \
`crackme.py`
1. Download and read the `.py` file, see it uses `ROT47` decode
2. Use the `ROT47` decoder to get the flag
https://dencode.com/en/cipher/rot47

picoCTF{1|\/|_4_p34|\|ut_a79b6c2d}


### Bit-O-Asm-1 
Description \
Can you figure out what is in the eax register? Put your answer in the picoCTF flag format: picoCTF{n}  where n is the contents of the eax register in the decimal number base. If the answer was 0x11 your flag would be picoCTF{17}. \
Download the assembly dump here.
1. Download the file and upload to the Online Assembler
https://www.jdoodle.com/compile-assembler-nasm-online
2. Find the `eax` line and the hex number after it
```
eax,0x30
```
3. Convert it to Decimal, get `48`

picoCTF{48}

### Bit-O-Asm-2 (RE)
Description \
Can you figure out what is in the eax register? Put your answer in the picoCTF flag format: picoCTF{n} where n is the contents of the eax register in the decimal number base. If the answer was 0x11 your flag would be picoCTF{17}. \
Download the assembly dump here.
1. `0x9fe1a` is `654874` in Decimal
### Line-by-Line Explanation
```
1. <+0>: endbr64
Purpose: Security instruction (Intel CET).
Details: Marks a valid branch target for indirect jumps/calls. Prevents control-flow hijacking attacks (e.g., ROP attacks). Modern compilers add this by default.

2. <+4>: push rbp
Purpose: Save the old base pointer.
Details: Pushes the value of rbp (base pointer) onto the stack. This preserves the caller’s stack frame, allowing us to restore it later.

3. <+5>: mov rbp, rsp
Purpose: Set up a new stack frame.
Details: Copies rsp (stack pointer) into rbp. Now, rbp points to the top of the stack (the start of the current function’s stack frame).

4. <+8>: mov DWORD PTR [rbp-0x14], edi
Purpose: Save the 1st argument (edi) to the stack.
Details:
edi holds the first 32-bit integer argument in x86-64 calling conventions (e.g., int argc in main).
Stores edi at memory address rbp - 0x14 (a 4-byte slot on the stack).

5. <+11>: mov QWORD PTR [rbp-0x20], rsi
Purpose: Save the 2nd argument (rsi) to the stack.
Details:
rsi holds the second 64-bit pointer argument (e.g., char* argv[] in main).
Stores rsi at memory address rbp - 0x20 (an 8-byte slot on the stack).

6. <+15>: mov DWORD PTR [rbp-0x4], 0x9fe1a
Purpose: Initialize a local variable.
Details:
Writes the 32-bit value 0x9fe1a (decimal: 655,642) to the stack at rbp - 0x4.
Likely a constant or temporary variable used in the function.

7. <+22>: mov eax, DWORD PTR [rbp-0x4]
Purpose: Prepare the return value.
Details:
Copies the 32-bit value from rbp - 0x4 (the constant 0x9fe1a) into eax.
In x86-64, eax holds the return value of a function.

8. <+25>: pop rbp
Purpose: Restore the old base pointer.
Details:
Pops the saved rbp value (from line 2) off the stack back into rbp.
Restores the caller’s stack frame.

9. <+26>: ret
Purpose: Return from the function.
Details:
Pops the return address from the stack and jumps to it.
Control returns to the caller (e.g., main or another function).
```
#### What Does This Function Do?
```
Input: Takes two arguments (a 32-bit integer edi and a 64-bit pointer rsi).
Action: Stores these arguments on the stack, initializes a local variable to 0x9fe1a, and returns that value via eax.
Behavior: Essentially returns the constant 0x9fe1a regardless of input.
```

#### Stack Layout Visualization
```
Higher Addresses
+------------------+
| ...              |
| Saved RBP        | <-- RBP after `push rbp` (line 2)
+------------------+
| [RBP - 0x4]      | 0x9fe1a (local variable)  ← EAX gets this value
+------------------+
| ...              |
+------------------+
| [RBP - 0x14]     | Value of EDI (1st argument)
+------------------+
| [RBP - 0x20]     | Value of RSI (2nd argument)
+------------------+
Lower Addresses
```
#### Key Takeaways
```
Stack Frames: rbp marks the base of the stack frame, while rsp marks the top.
Argument Storage: Arguments are stored on the stack for later use.
Return Values: Use eax (32-bit) or rax (64-bit) to return values.
Security: endbr64 is a modern security feature for control-flow integrity.
```
#### Reference
DeepSeek AI
https://hackmd.io/@cmonast/ryJLkBtHa

picoCTF{654874}

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

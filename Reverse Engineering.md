### Transformation
Description
I wonder what this really is... enc \
灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸彥㜰㍢㐸㙽 \
''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])
1. Go to CyberChef -> Text Encoding Brute Force
2. UTF-16BE (1201) to get the flag
   
picoCTF{16_bits_inst34d_of_8_e703b486}

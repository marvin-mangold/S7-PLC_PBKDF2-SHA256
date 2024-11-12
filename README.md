# S7-PLC_PBKDF2-SHA256
## PBKDF2-SHA256 FC for Siemens PLC S7-1200 and S7-1500 
In cryptography, PBKDF1 and PBKDF2 (Password-Based Key Derivation Function 1 and 2) are key derivation functions
with a sliding computational cost, used to reduce vulnerability to brute-force attacks.

PBKDF2 applies a pseudorandom function, such as hash-based message authentication code (HMAC),
to the input password or passphrase along with a salt value and repeats the process many times to produce a derived key, 
which can then be used as a cryptographic key in subsequent operations. 
The added computational work makes password cracking much more difficult, and is known as key stretching. 

depending on the input "inputmode" different inputformats are used
    
    -1 Password and Salt are used as Bytes
    -2 Password and Salt are used as String

depending on the input "outputmode" different outputformats are available

    -1 The derivedKeyBytes ouput is the final value as bytes (Array [0..31] of Byte)
    -2 The derivedKeyString output is the final hash value as a hexadecimal string (64 bytes string)
    -3 Both 1 and 2
 
![PBKDF2](https://github.com/user-attachments/assets/102a295e-fe4a-46dc-b8a3-cafc3fec2e3a)

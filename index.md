# S7-PLC_HMAC-SHA256
## HMAC-SHA256 FC for Siemens PLC S7-1200 and S7-1500
In cryptography, an HMAC (sometimes expanded as either keyed-hash message authentication code or hash-based message authentication code)
is a specific type of message authentication code (MAC) involving a cryptographic hash function and a secret cryptographic key.
HMAC can provide authentication using a shared secret instead of using digital signatures with asymmetric cryptography.
Any cryptographic hash function, such as SHA-2 or SHA-3, may be used in the calculation of an HMAC; 
the resulting MAC algorithm is termed HMAC-x, where x is the hash function used (e.g. HMAC-SHA256 or HMAC-SHA3-512).
HMAC does not encrypt the message. Instead, the message (encrypted or not) must be sent alongside the HMAC hash. 
Parties with the secret key will hash the message again themselves, and if it is authentic, the received and computed hashes will match. 

HMAC-SHA256 = SHA256( ( K XOR opad ) <concat> SHA256( ( K XOR ipad ) <concat> M ) )

depending on the input "inputmode" different inputformats are used

    -1 Message and Key are used as Bytes
    -2 Message and Key are used as String

depending on the input "outputmode" different outputformats are available

    -1 The digest ouput is the final value as bytes (Array [0..31] of Byte)
    -2 The hexdigest output is the final hash value as a hexadecimal string (64 bytes string)
    -3 Both 1 and 2
 
![HMAC-SHA256](https://github.com/user-attachments/assets/ae1047e6-189b-4f92-9a73-a58d6404cc68)

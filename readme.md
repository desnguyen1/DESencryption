# Des Encryption/Decryption 
Destiny Nguyen

Z#: 23397389

CIS5371: Practical Aspects of Modern Cryptography

Assignment - 02: DES Encryption/Decryption

## How to Run the Program

## What Each File Contains

main.cpp
> Contains the general code to run the program and functions such as: 
> * ASCII to Binary
> * Binary to ASCII
> * splitting plaintext/ciphertext into 64-bit Blocks for DES 
> * getting plaintext from user

des.cpp
> Contains all the code for DES encryption/decryption and tables needed; 
> key scheduling is in a separate file. In addition, contains all the operations needed
> such as: 
> * xor function
> * binary to decimal
> * decimal to binary

keyScheduling.cpp
> Contains the code to run key scheduling and generate all the subKeys for 
> encryption and decryption. In addition, contains all the tables needed with functions:
> * left shift
> * right shift
> * get key from user
> There are two functions, one specifically for encryption and the other for decryption

## Program Tracing

Encryption: 
> Input: a message (plaintext) and secret key in ASCII

> Output: encrypted plaintext (ciphertext) using key in binary

Decryption:
> Input: takes ciphertext that was generated from encryption

> Output: decrypted ciphertext (plaintext) in binary and ASCII

main.cpp
> Getting key and plaintext: 
> * get the plaintext from user
> * converts plaintext from ASCII to Binary
> * copies plaintext so the original plaintext remains untouched
> * get the secret key from user (from keyScheduling.cpp)
> * converts key from ASCII to Binary 

> DES Encryption: 
> * get subKeys (from keyScheduling.cpp)
> * splits plaintext into 64-bit Blocks
> * starts DES encryption (from des.cpp)
> * outputs ciphertext in Binary

> DES Decryption:
> * get subKeys in reverse (from keyScheduling.cpp)
> * get the previously generated ciphertext (output of encryption)
> * splits ciphertext into 64-bit blocks
> * starts DES decryption (from des.cpp)
> * outputs plaintext generated from ciphertext in binary and ASCII

### Some Notes:
The tables are from Wikipedia but was adjusted by 1 to fit in with the array format
by beginning at index 0 instead of 1 (except s-boxes table was left alone).
# Vigenere-cipher
A python solution for  Vigenère cipher which  uses a simple form of polyalphabetic substitution. A polyalphabetic cipher is any cipher based on substitution using multiple offset alphabets.

=================================================================================================================================================================
The program was broken down to the following functions:

def text_processor(plain):
This function takes in the supplied message and removes special characters and numbers and returns the plain text in upper case.

def key_generator(nplain,key):
This function accepts the processed plain text and the supplied key. It generates the key by repeating itself to make sure, the key matches the length of the message.

def vigenere_encrypt(nplain,pkey):
This fucntion takes in the auto generated key and the message and encrypts it by doing alphabetic substitution, then it returns the encrypted text.

def vigenere_decrypt(hashed,pkey):
Lastly, decryption is done by taking the auto generated key and the hashed text and returning it to its orginal state, this function returns deciphered text.



# Encryption Process
The encryption is done as follows:
Ci = (P i+ Kj) mod 26,
where Kj is the j-th letter of the key, 
Pi is і-th letter of the original message, and
Ci is the i-th letter of the ciphertext.

Pseudo-code:
 
m <-- length of key 
for index, character in plaintext:
    ciphertext[index] <-- (character + key[index % m]) % 26
 
return ciphertext

# Decryption Process
The decryption is done as follows:
Di = ((Ci-Kj)+26) mod 26,
where Kj is the j-th letter of the key, 
Ci is і-th letter of the cipher text, and
Di is the i-th letter of the deciphered text.

Pseudo-code:
 
m <-- length of key 
for index, character in cipherext:
    decipheredtext[index] <-- ((character - key[index % m])+26) % 26
 
return decipheredtext

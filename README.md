# Vigenere-cipher
A python solution for  Vigenère cipher which  uses a simple form of polyalphabetic substitution. A polyalphabetic cipher is any cipher based on substitution using multiple offset alphabets.

#Encryption Process
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

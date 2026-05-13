# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.
# NAME: D.BALA SUBRAMANYAM
# REG.NO: 212224040062
# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
~~~
#include <stdio.h>
#include <string.h>

void xor_encrypt_decrypt(char *input, char *key) {
    int input_len = strlen(input);
    int key_len = strlen(key);
    for (int i = 0; i < input_len; i++) {
        input[i] = input[i] ^ key[i % key_len];
    }
}

int main() {
    char url[] = "BALA";
    char key[] = "secretkey";
    
    printf("Original text: %s\n", url);
    xor_encrypt_decrypt(url, key);
    printf("Encrypted text: %s\n", url);
    xor_encrypt_decrypt(url, key);
    printf("Decrypted text: %s\n", url);

    return 0;
}
~~~
# OUTPUT:
<img width="1747" height="991" alt="Screenshot 2026-05-13 133536" src="https://github.com/user-attachments/assets/96a84085-5d8d-40b8-ac8b-b947fc55e947" />

# RESULT:
The code are executed successfully verified.


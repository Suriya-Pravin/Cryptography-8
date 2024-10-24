### Date: 19.09.2024
# Ex-8: Implement:The AES Encryption and Decrption
## Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

## ALGORITHM:
### Step1:
AES is based on a design principle known as a substitution–permutation.

### Step2:
AES does not use a Feistel network like DES, it uses variant of Rijndael.

### Step3:
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
### Step4:
AES operates on a 4 × 4 column-major order array of bytes, termed the state

## PROGRAM:
```
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
    char url[100];
    char key[100];

    // Taking user input for URL and key
    printf("Enter URL: ");
    scanf("%s", url);

    printf("Enter key: ");
    scanf("%s", key);

    printf("Original URL: %s\n", url);

    xor_encrypt_decrypt(url, key);
    printf("Encrypted URL: %s\n", url);

    xor_encrypt_decrypt(url, key);
    printf("Decrypted URL: %s\n", url);

    return 0;
}
```
## OUTPUT:
![8](https://github.com/user-attachments/assets/1be423b9-684d-46d4-be6e-6509b73e9041)



## RESULT:
Hence,to use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption is done successfully.

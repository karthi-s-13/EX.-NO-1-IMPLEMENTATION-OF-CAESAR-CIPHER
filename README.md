# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

|NAME   | KARTHIKEYAN S |
|-------|---------------|
|REG NO | 212224230116  |

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:

```c
#include <stdio.h>
#include <ctype.h>  // for isalpha, isupper, islower

// Caesar Cipher function
void caesar_cipher(char text[], int shift, char result[]) {
    int i = 0;
    while (text[i] != '\0') {
        char ch = text[i];
        if (isalpha(ch)) {
            char base = isupper(ch) ? 'A' : 'a';
            result[i] = (ch - base + shift) % 26 + base;
        } else {
            result[i] = ch;  // keep spaces or punctuation unchanged
        }
        i++;
    }
    result[i] = '\0';  // null-terminate the result string
}

int main() {
    char plaintext[] = "HELLO WORLD";
    int shift = 3;
    char ciphertext[100];  // buffer for result

    caesar_cipher(plaintext, shift, ciphertext);

    printf("Plaintext: %s\n", plaintext);
    printf("Shift: %d\n", shift);
    printf("Ciphertext: %s\n", ciphertext);

    return 0;
}

```
## OUTPUT:
<img width="325" height="116" alt="Screenshot 2025-10-18 191257" src="https://github.com/user-attachments/assets/85258bdd-88b1-42fc-aa3c-910366eb43e1" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.

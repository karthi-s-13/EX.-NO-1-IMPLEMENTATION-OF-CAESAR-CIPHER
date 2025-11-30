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

```python
def caesar_cipher(text, shift):
    result = ""

    for char in text:
        if char.isalpha():  
            base = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - base + shift) % 26 + base)
        else:
            result += char  
    return result

plaintext = "HELLO WORLD"
shift = 3
ciphertext = caesar_cipher(plaintext, shift)

print("Plaintext:", plaintext)
print("Shift:", shift)
print("Ciphertext:", ciphertext)
```
## OUTPUT:
<img width="325" height="116" alt="Screenshot 2025-10-18 191257" src="https://github.com/user-attachments/assets/85258bdd-88b1-42fc-aa3c-910366eb43e1" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.

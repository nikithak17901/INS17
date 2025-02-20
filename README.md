Caesar Cipher - Simple Encryption & Decryption

This project demonstrates the Caesar Cipher, a basic encryption technique where each letter in the text is shifted by a fixed number of positions in the alphabet.

🔹 Features
✅ Encrypts plaintext using a shift key

✅ Decrypts ciphertext back to original text

✅ Works with both uppercase and lowercase letters

✅ Keeps special characters unchanged

📌 How It Works

Each letter in the text is shifted forward (encryption) or backward (decryption) based on the key.
The shift wraps around within the 26 English letters (A-Z, a-z).
Non-alphabet characters remain unchanged.


📂 Files Included
📜 CaesarCipher.ipynb - Jupyter Notebook with the complete implementation

📜 encrypt() - Function to encrypt text

📜 decrypt() - Function to decrypt text

🚀 Quick Start Prerequisites

Python 3.x
Jupyter Notebook (or Google Colab)

Run the Code 
1️⃣ Clone the Repository

git clone https://github.com/your-username/Caesar-Cipher.git
cd Caesar-Cipher
2️⃣ Open Jupyter Notebook & Run
3️⃣ Input Text & Key
Enter the text to encrypt: hello
Enter the key: 3
Cipher text: khoor

4️⃣ Decrypt the Text
Enter the cipher text: khoor
Enter the key: 3
Plain text: hello

🎯 Examples
🔹 Encryption
Plaintext	Key	Ciphertext
hello	3	khoor
python	5	udymts
🔹 Decryption
Ciphertext	Key	Plaintext
khoor	3	hello
udymts	5	python







Hill Cipher Encryption in Python
This is a simple implementation of the Hill Cipher encryption algorithm using NumPy.

📌How It Works
The program encrypts a given plaintext using matrix multiplication.
It converts characters to numerical values (A=0, B=1, ..., Z=25).
If the plaintext length is not a multiple of the key matrix size, it is padded with X.
The encryption is performed using modular arithmetic with matrix multiplication.
The encrypted text is then converted back to letters.

Prerequisites
Make sure you have Python installed with the following package:
pip install numpy

Usage
Run the script and enter the plaintext to encrypt.

🎯Example

Input:  HELLO

Output: ZEBBWX

Notes
The key matrix should be invertible modulo 26 for decryption.
The script currently only supports encryption.
Ensure that the key matrix is square (n × n).



Monoalphabetic-Cipher
A simple and user-friendly implementation of the Monoalphabetic Cipher in Python for encryption and decryption of messages using a fixed substitution alphabet.
Introduction
The Monoalphabetic Cipher is a type of substitution cipher where each letter in the plaintext is replaced with a corresponding letter from a predefined mapping. This implementation provides an easy-to-use interface for encrypting and decrypting messages.

Features
✅ Encrypts plaintext messages using a predefined substitution alphabet.

✅ Decrypts ciphertext messages back to the original plaintext.

✅ Preserves non-alphabetic characters without modification.

✅ Simple and easy-to-use Python script.

📌How It Works
The script defines two mappings:

p = 'abcdefghijklmnopqrstuvwxyz' (Plaintext alphabet)

ch = 'QWERTYUIOPASDFGHJKLZXCVBNM' (Ciphertext alphabet)

Each letter from the input is replaced with its corresponding letter from the predefined mapping during encryption, and vice versa during decryption.


Playfair-Cipher

A Python implementation of the Playfair Cipher for encrypting and decrypting text using a key-based 5x5 matrix

Introduction
The Playfair Cipher is a digraph substitution cipher that encrypts pairs of letters in plaintext using a 5x5 key matrix. It replaces repeating letters and adjusts odd-length messages by adding filler characters.

Features
✅ Encrypts text using a Playfair matrix.

✅ Decrypts ciphertext back to its original plaintext.

✅ Handles odd-length plaintext by appending an 'X'.

✅ Ignores spaces and treats 'J' as 'I'.

✅ Simple Python implementation with easy-to-follow logic.

📌How It Works
Matrix Creation: A 5x5 matrix is generated using the key.
Position Finding: Each letter's position is determined in the matrix.
Encryption: Letters in the same row/column shift accordingly; otherwise, a rectangle swap is performed.
Decryption: Reverse of encryption logic 

🎯Example
$ python playfair_cipher.py

Enter the plain text: instruments

Enter the key: monarchy

Encrypted message: GATLMZCLRQXA

Enter the cipher text: gatlmzclrqxa

Enter the key: monarchy

Decrypted message: INSTRUMENTSX


Vigenère Cipher

The Vigenère cipher is a method of encrypting alphabetic text using a keyword. It employs a form of polygraphic substitution, shifting each letter in the plaintext based on the corresponding letter in the keyword. This makes it more secure than simple ciphers like the Caesar cipher.

📌How It Works
Keyword Selection: Choose a keyword.
Align Text: Repeat the keyword to match the length of the plaintext.

Encryption:
For each letter in the plaintext, shift it forward in the alphabet based on the position of the corresponding keyword letter (A=0, B=1, ..., Z=25).

Decryption: Shift backwards using the same keyword.

Features
✅Polygraphic Substitution: Uses multiple substitutions based on a keyword.

✅Increased Security: More secure than basic ciphers due to variable shifting.

✅Simplicity: Easy to implement and understand.

🎯Example
Plaintext: "HELLO"
Keyword: "KEY"

Align the Text:

Plaintext: H E L L O
Keyword: K E Y K E
Corresponding Shifts:

K = 10, E = 4, Y = 24
Encrypt the Text:

H + K = R
E + E = I
L + Y = J
L + K = V
O + E = S
Encrypted message: "RIJVS"

The Vigenère cipher demonstrates a fundamental cryptographic principle and serves as an excellent introduction to more advanced encryption techniques.


Introduction to Feistel Network 

The Feistel network is a structure designed for building symmetric key block ciphers. It divides input data into two halves and processes them through several rounds of transformation, where the same function is applied for both encryption and decryption.

 Features of Feistel Network

✅Simplicity: Uses the same function for both encryption and decryption, making the design efficient.

✅Divide and Conquer: The input data is split into two parts, facilitating easier manipulation and transformation.

✅Symmetric Operation: The same keys are used for both processes, which underscores its symmetric nature.

✅Reversible: The Feistel structure ensures that if you can encrypt, you can also decrypt, utilizing the same function with different key arrangements.

✅Security: It allows for a complex key schedule and multiple rounds, increasing the difficulty of cryptanalysis.

📌How It Works

Input Splitting: The plaintext (input data) is divided into two halves, typically called the left half (L) and the right half (R).

Rounds: The Feistel network operates through multiple rounds (typically 16 in DES):

In each round, a round function (using a subkey) is applied to one half (usually the right half).
The output of this round function is then combined with the other half (using XOR).
The halves are swapped after each round, except in the final round.

Output: After the last round, the two halves are combined to produce the ciphertext.

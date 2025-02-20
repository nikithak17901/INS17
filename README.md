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

How It Works
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

Example

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

How It Works
The script defines two mappings:

p = 'abcdefghijklmnopqrstuvwxyz' (Plaintext alphabet)

ch = 'QWERTYUIOPASDFGHJKLZXCVBNM' (Ciphertext alphabet)

Each letter from the input is replaced with its corresponding letter from the predefined mapping during encryption, and vice versa during decryption.

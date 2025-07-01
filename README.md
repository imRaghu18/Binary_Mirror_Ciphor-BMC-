<p align="center">
<img src="./hstu_correct_logo.png" alt="HSTU Logo" width="150">
</p>
<h2 align="center"><strong>HAJEE MOHAMMAD DANESH SCIENCE AND TECHNOLOGY UNIVERSITY</strong></h2>
<h3 align="center">DINAJPUR-5200</h3>


<h2 align="center" style="color:#16a085;"><strong> Course Information</strong></h2>

<p align="center">
  <strong>Course Title:</strong> Mathematical Analysis for Computer Science  
  <br>
  <strong>Course Code:</strong> CSE 361
</p>

---

<h2 align="center" style="color:#2980b9;"><strong> Algorithm Name</strong></h2>

<h1 align="center" style="color:#8e44ad;"><strong> Binary Mirror Cipher BMC </strong></h1>

---

<h2 align="center" style="color:#16a085;"><strong> Submitted By</strong></h2>

<p align="center">
  <strong>Name:</strong> Raghubir Chaudhary  
  <br>
  <strong>Student ID:</strong> 2102064  
  <br>
  <strong>Level:</strong> 3  
  <br>
  <strong>Semester:</strong> II  
  <br>
  <strong>Department:</strong> Computer Science and Engineering  
</p>

---
<h2 align="center" style="color:#16a085;"><strong>👨‍🏫 Submitted To</strong></h2>

<p align="center">
  <strong>Name:</strong> Pankaj Bhowmik  
  <br>
  <strong>Designation:</strong> Lecturer  
  <br>
  <strong>Department:</strong> Computer Science and Engineering  
</p>


---
##  Table of Contents

- [Overview](#-overview)
- [Introduction](#-introduction)
- [Features](#-features)
- [Encryption Process](#-encryption-process)
- [Decryption Process](#-decryption-process)
- [Encryption Algorithm](#-encryption-algorithm)
- [Decryption Algorithm](#-decryption-algorithm)
- [Flowcharts](#-flowchart)
- [Test Case](#-test-case)
- [Source Code](#-source-code)
- [Benefits](#-benefits)
- [Conclusion](#-conclusion)
- [Future Improvements](#-future-improvements)

---

##  Introduction

Every character on a computer is stored as an 8-bit binary number (e.g., `A` = `01000001`). In this cipher:

- Encryption = Reverse (mirror) the bits → Convert to character.
- Decryption = Repeat the process to recover the original message.

It's an intuitive, keyless method ideal for beginners.

---

##  Features

-  Symmetric: Same logic for encryption and decryption.
-  Simple: Great for understanding low-level data manipulation.
-  Fast: Lightweight with minimal computation.
-  No Key Required: The method is self-contained.
-  Educational: Perfect for students learning binary-level operations.

---

##  Encryption Process

1. Take plaintext message.
2. For each character:
   - Convert to 8-bit binary.
   - Reverse the bits.
   - Convert reversed binary to new character.
3. Join all new characters → Ciphertext.

---

##  Decryption Process

Same as encryption:
1. Take ciphertext.
2. For each character:
   - Convert to 8-bit binary.
   - Reverse the bits.
   - Convert reversed binary to original character.
3. Join all characters → Plaintext.

---

##  Encryption Algorithm
<pre>
Algorithm EncryptBinaryMirror(plaintext):
    Begin
        ciphertext ← ""
        for each character ch in plaintext do
            binary ← ConvertTo8BitBinary(ch)
            mirrored ← ReverseBits(binary)
            newChar ← BinaryToChar(mirrored)
            ciphertext ← ciphertext + newChar
        end for
        return ciphertext
    End


Algorithm DecryptBinaryMirror(ciphertext):
    Begin
        plaintext ← ""
        for each character ch in ciphertext do
            binary ← ConvertTo8BitBinary(ch)
            mirrored ← ReverseBits(binary)
            origChar ← BinaryToChar(mirrored)
            plaintext ← plaintext + origChar
        end for
        return plaintext
    End

</pre>

---

## Flowchart for Encryption Algorithm
<p align="center">
<img src="./Encryption flowchart.png" alt="Encryption flowchart">
</p>

---

## Flowchart for Decryption Algorithm
<p align="center">
<img src="./Decryption flowchart.png" alt="Encryption flowchart">
</p>



---

##  Test Case: "BANGLADESH"

###  Encryption Table

| Char | ASCII | Binary     | Mirrored  | Decimal | Encrypted | Hex Code |
|------|-------|------------|-----------|---------|-----------|----------|
| B    | 66    | 01000010   | 01000010  | 66      | B         | \x42     |
| A    | 65    | 01000001   | 10000010  | 130     | ‚         | \x82     |
| N    | 78    | 01001110   | 01110010  | 114     | r         | \x72     |
| G    | 71    | 01000111   | 11100010  | 226     | â         | \xE2     |
| L    | 76    | 01001100   | 00110010  | 50      | 2         | \x32     |
| A    | 65    | 01000001   | 10000010  | 130     | ‚         | \x82     |
| D    | 68    | 01000100   | 00100010  | 34      | "         | \x22     |
| E    | 69    | 01000101   | 10100010  | 162     | ¢         | \xA2     |
| S    | 83    | 01010011   | 11001010  | 202     | Ê         | \xCA     |
| H    | 72    | 01001000   | 00010010  | 18      | DC2       | \x12     |

---

###  Decryption Table

| Encrypted | ASCII | Binary     | Mirror     | Decimal | Decrypted |
|-----------|-------|------------|------------|---------|-----------|
| B         | 66    | 01000010   | 01000010   | 66      | B         |
| ‚         | 130   | 10000010   | 01000001   | 65      | A         |
| r         | 114   | 01110010   | 01001110   | 78      | N         |
| â         | 226   | 11100010   | 01000111   | 71      | G         |
| 2         | 50    | 00110010   | 01001100   | 76      | L         |
| ‚         | 130   | 10000010   | 01000001   | 65      | A         |
| "         | 34    | 00100010   | 01000100   | 68      | D         |
| ¢         | 162   | 10100010   | 01000101   | 69      | E         |
| Ê         | 202   | 11001010   | 01010011   | 83      | S         |
| DC2       | 18    | 00010010   | 01001000   | 72      | H         |

 Final Output:  
- Encrypted: B ‚ r â 2 ‚ " ¢ Ê DC2  
- Decrypted: **BANGLADESH**

---

## 💻 Source Code (C++)
<pre>

#include <iostream>
#include <bitset>
#include <string>
using namespace std;

string mirrorBits(const string& bits) {
    return string(bits.rbegin(), bits.rend());
}

string binaryMirrorCipher(const string& input) {
    string result = "";
    for (char ch : input) {
        bitset<8> bin(ch);
        string mirrored = mirrorBits(bin.to_string());
        bitset<8> newChar(mirrored);
        result += static_cast<char>(newChar.to_ulong());
    }
    return result;
}

int main() {
    string plaintext = "BANGLADESH";
    string encrypted = binaryMirrorCipher(plaintext);
    cout << "Encrypted: ";
    for (char c : encrypted)
        cout << "\\x" << hex << (int)(unsigned char)c;
    cout << endl;

    string decrypted = binaryMirrorCipher(encrypted);
    cout << "Decrypted: " << decrypted << endl;

    return 0;
}

</pre>

---

##  Benefits

-  Helps beginners understand binary encryption.
-  Encourages bit-level thinking and practice.
-  No key needed, making it simple and easy to use.
-  Very fast and lightweight – suitable for small projects.
-  Good for testing or obfuscating data.
-  Can be combined with other ciphers for added security.
-  Great for educational assignments and demos.

---

##  Conclusion

The Binary Mirror Cipher is a very simple and clever encryption method. It flips the binary bits of each character to create unreadable symbols. It’s easy to use, fast, and requires no key. Although it’s not secure for serious use, it’s perfect for learning how encryption works at a basic binary level. It can also be used as part of a more complex hybrid cipher system.

---

##  Future Improvements

-  Add a key to make bit reversal more secure.
-  Flip selected bits instead of full mirroring.
-  Combine with Caesar, XOR, or matrix ciphers.
-  Randomize bit order using a pattern or key.
-  Add support for emojis and Unicode characters.
-  Allow partial mirroring based on position or rules.

---



                    










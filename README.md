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

<h1 align="center" style="color:#8e44ad;"><strong>🔐 Binary Mirror Cipher BMC </strong></h1>

---

<h2 align="center" style="color:#16a085;"><strong>🧑‍💻 Submitted By</strong></h2>

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
## 📖 Table of Contents

- [Overview](#-overview)
- [Introduction](#-introduction)
- [Features](#-features)
- [Encryption Process](#-encryption-process)
- [Decryption Process](#-decryption-process)
- [Encryption Algorithm](#-encryption-algorithm)
- [Decryption Algorithm](#-decryption-algorithm)
-  [Flowcharts](#-flowchart)
- [Test Case](#-test-case)
- [Source Code](#-source-code)
- [Benefits](#-benefits)
- [Conclusion](#-conclusion)
- [Future Improvements](#-future-improvements)

---

## 🧠 Introduction

Every character on a computer is stored as an 8-bit binary number (e.g., `A` = `01000001`). In this cipher:

- Encryption = Reverse (mirror) the bits → Convert to character.
- Decryption = Repeat the process to recover the original message.

It's an intuitive, keyless method ideal for beginners.

---

## ✅ Features

- 🔁 Symmetric: Same logic for encryption and decryption.
- 🧠 Simple: Great for understanding low-level data manipulation.
- ⚡ Fast: Lightweight with minimal computation.
- 🗝️ No Key Required: The method is self-contained.
- 🎓 Educational: Perfect for students learning binary-level operations.

---

## 🔐 Encryption Process

1. Take plaintext message.
2. For each character:
   - Convert to 8-bit binary.
   - Reverse the bits.
   - Convert reversed binary to new character.
3. Join all new characters → Ciphertext.

---

## 🔓 Decryption Process

Same as encryption:
1. Take ciphertext.
2. For each character:
   - Convert to 8-bit binary.
   - Reverse the bits.
   - Convert reversed binary to original character.
3. Join all characters → Plaintext.

---

## 🧮 Encryption Algorithm

```pseudo
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



















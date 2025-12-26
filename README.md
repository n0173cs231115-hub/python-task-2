# python-task-2
🔐 CLI Password Manager (Python)
📌 Project Overview

This project is a secure command-line password manager built using Python.
It allows users to safely store, retrieve, list, and delete credentials using strong cryptographic techniques.

All sensitive data is encrypted using AES-256-GCM, and access is protected by a master password.

🎯 Features

🔑 Master password–based authentication

🔒 AES-256-GCM encryption (industry standard)

🧠 Secure key derivation using PBKDF2-HMAC

📂 Encrypted JSON vault storage

💻 Command-line interface (CLI)

👁️ Hidden password input

🛡️ Protection against wrong password & tampered data

🛠️ Technologies Used

Language: Python 3

Libraries:

cryptography

argparse

json

getpass

os, base64, sys

📁 Project Structure
password_manager.py
vault.json        (auto-generated)
README.md

⚙️ Installation & Setup
1️⃣ Install Python (if not installed)

Download from: https://www.python.org

✔ Make sure Python 3.9+ is installed.

2️⃣ Install Required Library
pip install cryptography

▶️ How to Run the Project
➕ Add New Credentials
python password_manager.py add

📄 List All Stored Websites
python password_manager.py list

🔍 Get Credentials
python password_manager.py get google.com

🗑️ Delete Credentials
python password_manager.py delete google.com

🔐 How Security Works
Master Password

User sets a master password

Never stored anywhere

Used only to derive encryption key

Key Derivation

PBKDF2-HMAC with SHA-256

480,000 iterations

Random salt for each vault

Encryption

AES-256-GCM (Authenticated Encryption)

Ensures:

Confidentiality

Integrity

Tamper detection

📦 Vault Storage (vault.json)

Stores only encrypted data

Contains:

Salt (Base64)

Encrypted credentials (nonce + ciphertext)

No plaintext passwords are ever saved

❗ Error Handling

Wrong master password → Access denied

Vault file missing → Safe exit

Tampered data → Decryption failure

Invalid command → Help message shown

📚 Learning Outcomes

CLI application design using argparse

Real-world cryptographic implementation

Secure data storage practices

Password protection and threat mitigation

Defensive programming

🚀 Future Enhancements

Master password change feature

Auto-lock after failed attempts

Clipboard-safe password copy

Password strength checker

Multi-vault support

👤 Author

Name: (Your Name)
Course: B.Tech
Subject: Python / Cyber Security / Software Engineering
Institution: (Your College Name)

# Day 3: Harvard CS50 (Cryptography & Encryption)

## The Basics of Cryptography
* **Encipher (Encrypt):** The process of converting readable plaintext into unreadable ciphertext.
* **Decipher (Decrypt):** The process of converting ciphertext back into readable plaintext.
* **Cryptanalysis:** The study of analyzing and breaking codes.

## Secret-Key Cryptography (Symmetric)
* Uses a single, shared key for both encrypting and decrypting the data.
* **Example (Shift Ciphers):** Shifting letters by a specific key value (e.g., Key = 1 shifts A -> B. Key = 13 shifts A -> N)[cite: 3]. 
* **Ciphertext Example:** OR FHER GB QEVAX LBHE BINYGVAR (ROT13 cipher).
* **Modern Standards:** AES and Triple DES are common algorithms used for secret-key cryptography.

## Public-Key Cryptography (Asymmetric)
* Uses a mathematical pair of keys: a **Public Key** (shared with everyone) and a **Private Key** (kept secret).
* **The Process:** The sender uses the receiver's Public Key to turn plaintext into ciphertext.The receiver then uses their Private Key to turn the ciphertext back into plaintext[cite: 3].
* **Common Algorithms:** Diffie-Hellman, MQV, and RSA.

### Core Mathematics (RSA & Key Exchange)
* **RSA:** Relies heavily on prime numbers (p and q) and modular arithmetic. 
* **Key Exchange (Diffie-Hellman):** Allows two parties to securely generate a shared secret over a public channel using modular arithmetic.

## Digital Signatures & Authentication
* Used to prove the authenticity and integrity of a message. 
* **Algorithms:** DSA, ECDSA, RSA.
* **How it Works (Signing):** A message is first converted into a hash.The sender then uses their Private Key to encrypt that hash, creating the signature.
* **Verification:** The receiver verifies the digital signature to ensure the message wasn't altered.
* **Passkeys & WebAuthn:** Modern authentication technology where a Private Key signs a cryptographic "challenge" to prove identity without a password.

## Data States & Storage Security
* **Encryption in Transit:** Encrypting data while it moves across a network (e.g., Alice <-> Eve <-> Bob). 
* **End-to-End Encryption:** Data is encrypted directly from the sender (Alice) to the final receiver (Bob), meaning no one in the middle can read it.
* **Encryption at Rest:** Protecting data while it is stored, typically through Full Disk Encryption.
* **Secure Deletion:** Ensuring deleted files are mathematically erased, not just hidden[.
* **Ransomware:** A malicious attack where adversaries use encryption against you, locking your data until a fee is paid.

## The Future Threat
* **Quantum Computing:** The development of Qbits (quantum bits) makes it possible for future quantum computers to break many of our current encryption standards.

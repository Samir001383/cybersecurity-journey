# Day 2: Harvard CS50 (Securing Data & Hashing)

## Core Concepts & Usability
* **The Balancing Act:** Security must always be balanced against usability[cite: 1]. Overly strict security forces users toward unsafe shortcuts[cite: 1].
* **Single Sign-On (SSO):** Authenticating across services using an existing, trusted identity provider (e.g., Google, Microsoft)[cite: 1].
* **Password Managers:** Tools such as Apple iCloud Keychain, Google Password Manager, and Microsoft Credential Manager that generate and store complex credentials securely[cite: 1].
* **Antivirus:** Defensive software that monitors, detects, and removes viruses, worms, and malicious software before they cause damage[cite: 1].
* **Modern Authentication Shifts:** Phasing out vulnerable biometric inputs (like voice passwords) in favor of cryptographic Passkeys[cite: 1].

---

## Securing Data: Hashing vs. Cryptography

### Cryptography (Two-Way)
* Cryptography uses algorithms and ciphers to break data into manageable pieces and protect it[cite: 1].
* **Encoding:** Converting plaintext into codetext/ciphertext[cite: 1].
* **Decoding:** Reversing ciphertext back into readable plaintext[cite: 1].

### Hashing (One-Way)
* Unlike cryptography, hashing is strictly a **one-way mathematical function** ($x \rightarrow f(x)$)[cite: 1].
* It takes an input of arbitrary length and outputs a fixed-length string (the hash value)[cite: 1].
* Common hash functions: SHA-224, SHA-256, CMAC, HMAC, KMAC[cite: 1].
* **The Insecure Password Reset Indicator:** If a website emails an existing plaintext password after clicking "Forgot Password," the system is storing credentials in plaintext rather than one-way hashes[cite: 1].

---

## Threat Models & Defenses

### 1. Dictionary & Brute-Force Attacks on Hashes
* **The Threat:** Attackers obtain stolen database hashes, then pass large wordlists or brute-force combinations through the same hash algorithm to find matching hash outputs[cite: 1].
* **How to Prevent:** Utilize modern, computationally expensive hash functions with large bit lengths (yielding quadrillions of possible combinations) to slow down offline cracking tools[cite: 1].

### 2. Rainbow Tables
* **The Threat:** Attackers use precomputed lookup tables pairing common passwords with their corresponding hash values to instantly reverse stolen hashes[cite: 1].
* **How to Prevent (Salting):** Append a unique, cryptographically random string (a "salt") to each password prior to hashing[cite: 1]. Even if multiple users choose identical passwords, their salted hashes remain completely distinct, nullifying precomputed tables[cite: 1]. The salt is stored alongside the hash in the database[cite: 1].

---

## Core NIST Password Guidelines (SP 800-63B)
*Guidelines established by the National Institute of Standards and Technology:*

1. **Compromised Credential Screening:** Compare user-submitted passwords against known breach corpuses.
2. **Length Over Complexity:** Enforce an 8-character minimum, support lengths up to at least 64 characters, and remove mandatory symbol/number rules that encourage predictable patterns.
3. **Eliminate Arbitrary Periodic Expirations:** Drop forced 90-day password resets unless there is evidence of an actual breach.
4. **Permit Paste Functionality:** Allow clipboard pasting in password fields to support password manager adoption.
5. **Rate-Limiting & Throttling:** Implement automated lockouts or exponential delays on consecutive failed login attempts to stop online brute-force attacks.

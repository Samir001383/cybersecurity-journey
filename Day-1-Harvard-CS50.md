# Day 1: Harvard CS50 (Cybersecurity Basics)

## Core Concepts
* **Authentication:** Proving *who* you are (using a username and password).
* **Authorization:** What you are allowed to access once you are logged in.
* **NIST:** National Institute of Standards and Technology (they provide security recommendations).
* **MFA / 2FA:** Multi-Factor Authentication. Proving who you are using a mix of: Knowledge (password), Possession (phone), or Inherence (fingerprint).

## Threats & Preventions

### 1. Brute-Force & Dictionary Attacks
* **The Threat:** Hackers use automated software to guess every possible password combination or use massive lists of common words to break in.
* **How to Prevent:** Mandate long passwords. A 4-digit PIN has only 10,000 possibilities (easily cracked), but an 8-character password has over 6 quadrillion possibilities.

### 2. Credential Stuffing
* **The Threat:** A hacker takes your leaked username and password from one website and tries it on dozens of other websites to see if you reused it.
* **How to Prevent:** Never reuse passwords across different sites. Always enforce MFA.

### 3. Keylogging
* **The Threat:** Malware that records every single keystroke you type and sends it to an adversary over the internet.
* **How to Prevent:** Use One-Time Passwords (OTP). Even if the hacker records you typing the OTP, it becomes useless the second you use it.

### 4. Social Engineering & Phishing
* **The Threat:** Hackers manipulating you into giving them your password or clicking a fake, malicious link.
* **How to Prevent:** Never trust anyone asking for your credentials. Always verify the URL before clicking.

### 5. SIM Swapping & Machine-in-the-Middle
* **The Threat:** A hacker hijacks your phone number so your security texts go to them, or they secretly intercept data between you and a website.
* **How to Prevent:** Avoid using SMS (text messages) for 2FA. Use Authenticator apps or hardware security keys instead.

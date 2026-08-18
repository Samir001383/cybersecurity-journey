# Day 4: Harvard CS50 (Web & Network Security)

## 1. Network Connections & Wireless Security
* **WiFi:** A wireless protocol for connecting devices. 
* **WPA (WiFi Protected Access):** A security standard for wireless computer networks. 

## 2. Web Protocols & Interception Threats
* **HTTP (HyperText Transfer Protocol):** The standard protocol for web communication. 
* **Packet Sniffing:** An attacker passively captures network traffic (packets) traveling across a network. 
* **Machine-in-the-Middle (MitM) Attack:** An attacker secretly intercepts and relays communications between two parties.

## 3. Web Tracking & Session Hijacking
* **Cookies:** Small pieces of data stored on your device by a server to identify you or maintain your session state.
* **Session Hijacking:** An attacker steals your active session cookie, often via packet sniffing on an unsecured network. 

## 4. Securing the Web (HTTPS & TLS)
* **HTTPS:** The secure, encrypted version of HTTP.
* **TLS:** The underlying cryptographic protocol that powers HTTPS to encrypt data in transit.
* **X.509 Certificates & Certificate Authorities (CA):** Websites use digital certificates (X.509) to mathematically prove their identity. A trusted Certificate Authority (CA) cryptographically signs the certificate to a hash. 

## 5. Advanced Downgrade Attacks & Prevention
* **SSL Stripping:** An attacker intercepts a user's initial HTTP request and prevents the server from upgrading the connection to HTTPS. 
* **HSTS:** A protocol forcing browsers to only interact with the site using HTTPS.

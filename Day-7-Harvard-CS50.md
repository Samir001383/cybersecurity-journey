# Day 7: Harvard CS50 (Software, Vulnerabilities & Privacy)

## 1. Software Analysis & Exploitation
* **Machine Code / Attack Code:** The lowest level of instructions executed by a computer's CPU. Attackers write malicious attack code at this level to bypass higher-level security[cite: 2]. 
* **Stack Overflow:** A specific type of buffer overflow where a program writes more data to the call stack than it can hold[cite: 2]. 
* **Cracking & Reverse Engineering:** Deconstructing software to understand its inner workings, often to bypass licensing (cracking) or find hidden flaws[cite: 2]. 
* **Malware Analysis:** The practice of safely dissecting malicious software to understand its behavior and build defenses[cite: 2].

## 2. Software Ecosystems & Vulnerability Management
* **Open Source vs. Closed-Source Software:** Open source allows anyone to inspect the code (e.g., Linux), while closed-source is proprietary and hidden (e.g., Microsoft Windows)[cite: 2].
* **App Stores & Package Managers:** Centralized distribution platforms (like Apple/Google App Stores or Linux package managers) that manage operating systems and securely update software[cite: 2].
* **Bug Bounty:** Programs where organizations pay ethical hackers to legally find and report security flaws[cite: 2].
* **CVE (Common Vulnerabilities and Exposures):** A standardized dictionary of publicly disclosed vulnerabilities[cite: 2]. 
* **CVSS & EPSS:** CVSS scores the technical severity of a vulnerability (0 to 10), while EPSS predicts the statistical likelihood it will actually be exploited in the wild[cite: 2].
* **KEV (Known Exploited Vulnerabilities Catalog):** A master list maintained by the government detailing vulnerabilities that attackers are actively using right now[cite: 2].

## 3. Preserving Privacy & Web Tracking
* **Web Browsing History & Logs:** Local and server-side records detailing every site visited and action taken[cite: 2].
* **HTTP Headers & Fingerprinting:** Data sent by your browser to a website. Trackers use this data—especially the **User-Agent** (which identifies your browser/OS)—to create a unique "fingerprint" of your device without needing cookies[cite: 2].
* **Cookies & Tracking:**
  * **Session Cookies:** Temporary cookies that keep you logged in during a single visit[cite: 2].
  * **Tracking & Third-Party Cookies:** Cookies placed by external domains (like ad networks) to track your behavior across multiple different websites[cite: 2].
  * **Super Cookies:** Highly persistent tracking data inserted at the network level, making them extremely difficult for users to delete[cite: 2].
  * **Tracking Parameters:** Data added to the end of a URL to track your clicks[cite: 2]. 
* **Private Browsing:** A browser mode that deletes your history and cookies locally after you close the window, though it does not hide your traffic from your ISP[cite: 2].

## 4. Network & Device Privacy
* **DNS Privacy (DNS over HTTPS / DNS over TLS):** Encrypts your Domain Name System requests so ISPs and network snoopers cannot see which website names you are looking up[cite: 2].
* **VPN:** Encrypts your network traffic and masks your IP address from local observers[cite: 2].
* **Device Controls:** Managing **Permissions** and **Location-based Services** on your operating system to restrict which apps are allowed to access your camera, microphone, or GPS[cite: 2].

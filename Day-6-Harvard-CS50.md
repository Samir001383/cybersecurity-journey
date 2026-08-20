# Day 6: Harvard CS50 (Web Application Security & Attacks)

## 1. Code Injection & Front-End Attacks
* **Concept:** Attackers inject malicious JS, CSS, or HTML code into a trusted website.
* **The Attack (How it works):** 
  * Attackers often abuse browser Developer Tools to manipulate forms and bypass weak client-side validations.
  * They inject attack code using special characters like `<` (less than), `>` (greater than), `&` (and symbol), `"` (double quote), and `'` (single quote) to break out of text fields and run scripts.
  * They can also manipulate HTTP Headers to alter the request and exploit the server.
* **The Solution (Defense):**
  * **Server-Side Validations:** Never trust client-side validations alone; always enforce strict checks on the server side.
  * **Character Escaping:** Strip or escape dangerous special characters so the browser treats them as plain text rather than executable code.

## 2. SQL & Command Injection
* **SQL Injection:** An attack that targets the database by inserting malicious SQL queries into user input fields.
  * **The Solution:** Use **Prepared Statements**. This forces the application to treat user input strictly as data, not as executable database commands.
* **Command Injection:** An attack where the attacker tricks the application into executing arbitrary system commands on the host server.
  * **The Attack:** Often occurs when developers unsafely use execution functions like `eval` to process user input.
  * **The Solution:** Avoid dangerous functions like `eval` and strictly sanitize all inputs.

## 3. Cross-Site Request Forgery (CSRF)
* **Concept:** A malicious exploit where unauthorized commands are transmitted from a user that the web application trusts (hijacking their active session).
* **The Attack (How it works):** 
  * Attackers trick the victim's browser into sending forged HTTP requests using the `GET` method or `POST` method without the user's consent or knowledge.
* **The Solution (Defense):** Require unique, unguessable anti-CSRF tokens for any state-changing request (like changing a password or transferring funds).

## 4. Memory Vulnerabilities & Execution
* **Buffer Overflow:** An anomaly where a program writes more data to a block of memory (the buffer) than it is allocated to hold, overwriting adjacent memory locations.
* **The Consequence:** This memory manipulation often leads directly to **Arbitrary Code Execution** or **Remote Code Executions** (RCE), allowing the attacker to run malicious code on the target machine from a remote location.

## 5. Industry Standards
* **OWASP:** The Open Worldwide Application Security Project (OWASP) is a globally recognized nonprofit organization that provides standard frameworks and lists for the most critical web application security risks.

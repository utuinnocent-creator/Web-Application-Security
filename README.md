# Reflected XSS Vulnerability Scanner

## ⚠️ Disclaimer & Ethical Use
**This tool is intended for authorized security testing and educational purposes only.**  
Always obtain explicit written permission from the website owner before scanning. Running automated scanners against websites you do not own or have authorization to test may violate computer misuse laws and terms of service. The authors are not liable for any misuse or damages caused by this software.

## Overview
This Python script is an application security tool designed to detect **Reflected Cross-Site Scripting (XSS)** vulnerabilities. Developed for **Orion Health Systems**, it automates the process of testing web endpoints (such as search forms) to determine if user input is improperly reflected in the HTTP response without proper sanitization.

Reflected XSS is a critical vulnerability (OWASP Top 10) that allows attackers to execute malicious scripts in the context of a victim's browser, potentially leading to session hijacking, credential theft, or malware distribution.

## Features
- **Automated Payload Testing:** Submits a predefined list of common XSS payloads (e.g., `<script>`, `img onerror`) to target endpoints.
- **Reflection Analysis:** Analyzes HTTP responses to detect if payloads are reflected in the page content.
- **Vulnerability Reporting:** Clearly reports whether the tested endpoint is **Vulnerable** or **Secure** based on reflection results.
- **Error Handling:** Gracefully handles network errors, timeouts, invalid URLs, and connection failures without crashing.
- **Safe Testing:** Designed to be non-destructive; it only reads responses and does not attempt to exploit the vulnerability beyond detection.
- **Compliance:** Aligns with OWASP A03:2021 (Injection) testing methodologies.

## Requirements
- **OS:** Linux (Kali, Parrot, Ubuntu), macOS, or Windows.
- **Python:** Python 3.6+
- **Dependencies:**
  - `requests` (For HTTP requests)
  - `beautifulsoup4` (Optional, for advanced HTML parsing if needed)

### Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-name>

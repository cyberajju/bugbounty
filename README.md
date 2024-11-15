# Bug Bounty Checklist for Web App @cyberajju (2025 Update)

> This checklist is designed to streamline your bug bounty methodology.  
Check items off as you progress. Happy hunting!  

## Table of Contents

* [Recon on Wildcard Domain](#Recon_on_wildcard_domain)
* [Single Domain](#Single_domain)
* [Information Gathering](#Information)
* [Configuration Management](#Configuration)
* [Secure Transmission](#Transmission)
* [Authentication](#Authentication)
* [Session Management](#Session)
* [Authorization](#Authorization)
* [Data Validation](#Validation)
* [Denial of Service](#Denial)
* [Business Logic](#Business)
* [Cryptography](#Cryptography)
* [Risky Functionality - File Uploads](#File)
* [Risky Functionality - Card Payment](#Card)
* [HTML 5](#HTML)


## <a name="Recon_on_wildcard_domain">Recon on Wildcard Domain</a>  

- [ ] Run **amass**, **subfinder**, and **assetfinder** for subdomain enumeration.  
- [ ] Use **dnsgen** for permutations.  
- [ ] Use **massdns** or **puredns** for resolution.  
- [ ] Run **httpx** or **httprobe** for active subdomains.  
- [ ] Use **aquatone** or **gowitness** for screenshots.  
- [ ] Incorporate **Naabu** for port scanning.  
- [ ] Use **subjack** or **tko-subs** for subdomain takeover checks.  


## <a name="Single_domain">Single Domain</a>  

### Scanning  

- [ ] Perform **Nmap** scans (Top Ports + Vulnerabilities).  
- [ ] Use **Burp Suite** crawler or **ZAP** for spidering.  
- [ ] Fuzz directories/files using **ffuf** or **dirsearch**.  
- [ ] Utilize **hakrawler**, **gau**, or **katana** for URLs and parameters.  
- [ ] Extract JS endpoints via **LinkFinder** or **SecretFinder**.  
- [ ] Analyze Android apps with tools like **jadx** or **APKTool** for additional URLs and endpoints.  

### Manual Checking  

- [ ] Explore **Shodan**, **Censys**, and **ZoomEye** for exposed services.  
- [ ] Perform OSINT on **Google Dorks**, **Pastebin**, and **Github** repositories.  
- [ ] Look for exposed credentials and sensitive data using **truffleHog**, **gitrob**, or **gitleaks**.  


### <a name="Information">Information Gathering</a>

- [ ] Analyze **robots.txt**, **sitemap.xml**, and other exposed files.  
- [ ] Explore potential content differences with **User-Agent Switcher** (mobile vs desktop).  
- [ ] Perform **WhatWeb**, **Wappalyzer**, or **builtwith** scans for tech fingerprinting.  
- [ ] Identify **application entry points**, **roles**, and **client-side scripts**.  
- [ ] Map out **third-party integrations** and **co-hosted apps**.  


### <a name="Configuration">Configuration Management</a>

- [ ] Search for sensitive endpoints or **admin panels** using **AdminFinder**.  
- [ ] Locate backups, dev files, and unreferenced content.  
- [ ] Enumerate HTTP methods via **curl** or **Burp Suite Repeater**.  
- [ ] Validate security headers with **securityheaders.com** or **burpsuite**:  
  - **CSP**, **HSTS**, **X-Frame-Options**, etc.  


### <a name="Transmission">Secure Transmission</a>

- [ ] Audit SSL/TLS configuration with **testssl.sh** or **SSL Labs**.  
- [ ] Confirm credentials and session tokens are only transmitted over HTTPS.  
- [ ] Check for HSTS headers and **HSTS Preload** lists.  


### <a name="Authentication">Authentication</a>

- [ ] Perform user enumeration on login and registration forms.  
- [ ] Test for **brute-force resistance** and **rate-limiting**.  
- [ ] Analyze password policy strength and bypass.  
- [ ] Inspect **MFA implementation** and potential bypasses.  
- [ ] Test **password reset flows** for leaks or reuse issues.  
- [ ] Review OAuth and SSO integrations for flaws (e.g., **IDOR in tokens**).  


### <a name="Session">Session Management</a>

- [ ] Ensure **httpOnly**, **Secure**, and **SameSite** cookie attributes.  
- [ ] Test session expiration, token renewal, and invalidation on logout.  
- [ ] Check for **CSRF** issues and anti-clickjacking protections.  


### <a name="Authorization">Authorization</a>

- [ ] Test vertical privilege escalation (e.g., user to admin).  
- [ ] Test horizontal privilege escalation (between users).  
- [ ] Explore endpoint access control via **Burp Intruder** or **Turbo Intruder**.  
- [ ] Check for improper or missing role validation on actions.  


### <a name="Validation">Data Validation</a>

- [ ] Fuzz inputs for **XSS** (Reflected, Stored, DOM-based).  
- [ ] Test for injection flaws: **SQLi**, **NoSQLi**, **XML/XPath**, **Command Injection**.  
- [ ] Check for **SSRF**, **LFI/RFI**, and **XXE**.  
- [ ] Test HTTP header-based vulnerabilities (**HTTP Smuggling**, etc.).  
- [ ] Audit redirects for open redirection.  
- [ ] Test for client/server-side input validation discrepancies.  


### <a name="Denial">Denial of Service</a>

- [ ] Verify account lockout policies and test for DoS due to weak configurations.  
- [ ] Simulate HTTP protocol abuse (e.g., slow POST attacks).  
- [ ] Check wildcard searches in SQL or Elasticsearch leading to resource exhaustion.  


### <a name="Business">Business Logic</a>

- [ ] Look for bypasses in workflow processes.  
- [ ] Simulate race conditions in critical operations.  
- [ ] Test for logical flaws in multi-step forms or payment flows.  


### <a name="Cryptography">Cryptography</a>

- [ ] Verify that sensitive data (e.g., passwords, PII) is encrypted in transit and at rest.  
- [ ] Review encryption algorithms and configurations for weaknesses (e.g., **AES**, **RSA**).  
- [ ] Ensure salting and hashing with secure algorithms (e.g., **bcrypt**, **Argon2**).  


### <a name="File">Risky Functionality - File Uploads</a>

- [ ] Whitelist file types and validate MIME types.  
- [ ] Scan uploaded files for malware or exploits.  
- [ ] Ensure file storage outside of web root with random paths/names.  
- [ ] Validate files for embedded malicious payloads (e.g., **polyglot files**).  


### <a name="Card">Risky Functionality - Card Payment</a>

- [ ] Verify PCI-DSS compliance.  
- [ ] Test payment forms for CSRF and input validation.  
- [ ] Validate payment workflows against common payment gateway flaws.  


### <a name="HTML">HTML 5</a>

- [ ] Test **Web Messaging** integrity (postMessage).  
- [ ] Check **CORS** configurations for misconfigurations.  
- [ ] Validate **Web Storage** to prevent data exposure and injection.  
- [ ] Inspect Offline App caching for data exposure.  

---

**Sources**:  
CYB3R T3CH AJJU's 2025 Updates.  

---  

Let me know if you need further customization!

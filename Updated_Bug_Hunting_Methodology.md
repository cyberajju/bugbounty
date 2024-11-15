# My Bug Hunting Methodology | CyberTechAjju

**Follow me for more updates and insights:**  
- **Twitter**: https://x.com/Ajaykumar3856/
- **LinkedIn**: https://in.linkedin.com/in/ajay-meena-6b432128a
- **Youtube**: https://youtube.com/@cybertechajju?si=He6rc1ajEstskg7P
## Introduction  

This methodology is designed for all levels of bug bounty hunters, from beginners to experts. It provides a step-by-step process for uncovering vulnerabilities in web applications.  

---  

## Table of Contents  

1. [Reconnaissance](#Recon)  
2. [Subdomain Takeover](#Subdomain_Takeover)  
3. [Collecting URLs and Parameters](#Collecting_URLs)  
4. [Scanning and Fuzzing](#Scanning_and_Fuzzing)  
5. [Authentication Testing](#Authentication_Testing)  
6. [Session Management](#Session_Management)  
7. [Authorization Testing](#Authorization_Testing)  
8. [Data Validation and Injection](#Data_Validation)  
9. [Denial of Service (DoS)](#Denial_of_Service)  
10. [Advanced Techniques](#Advanced_Techniques)  

---  

## 1. Reconnaissance <a name="Recon"></a>  

### Subdomain Enumeration  

1. **Subfinder**  
   ```bash  
   subfinder -dL domains.txt -o subfinder.txt  
   ```  

2. **Amass**  
   ```bash  
   amass enum -passive -norecursive -noalts -df domains.txt -o amass.txt  
   ```  

3. **crt.sh Finder** (Using Crtfinder)  
   ```bash  
   python3 crtfinder.py -u example.com  
   ```  

4. **Waymore**  
   Collect URLs from multiple sources.  
   ```bash  
   waymore -i example.com -mode U -oU urls.txt  
   ```  

**Combine results**:  
   ```bash  
   cat subfinder.txt amass.txt other_sources.txt | anew all-subs.txt  
   cat all-subs.txt | httpx -o live-subs.txt  
   ```  

### Port Scanning (Active Recon)  
Use **Naabu** for port scanning.  
   ```bash  
   naabu -iL live-subs.txt -p 80,443 -o ports.txt  
   ```  

---  

## 2. Subdomain Takeover <a name="Subdomain_Takeover"></a>  

1. **Nuclei**  
   ```bash  
   nuclei -t takeovers -l live-subs.txt  
   ```  

2. **Subzy**  
   ```bash  
   subzy run --targets live-subs.txt  
   ```  

---  

## 3. Collecting URLs and Parameters <a name="Collecting_URLs"></a>  

1. **Waymore** (Collect URLs and filter live ones)  
   ```bash  
   waymore -i example.com -oU collected-urls.txt  
   cat collected-urls.txt | httpx -mc 200 -o live-urls.txt  
   ```  

2. **Parameter Extraction**  
   ```bash  
   cat live-urls.txt | grep "=" > live-parameters.txt  
   ```  

---  

## 4. Scanning and Fuzzing <a name="Scanning_and_Fuzzing"></a>  

1. **Nmap**  
   ```bash  
   nmap -iL live-subs.txt -p 80,443 --script vuln -oN nmap-scan.txt  
   ```  

2. **FFUF (Directory/File Fuzzing)**  
   ```bash  
   ffuf -u https://example.com/FUZZ -w wordlist.txt -mc 200,403,301,302 -o output.txt  
   ```  

---  

## 5. Authentication Testing <a name="Authentication_Testing"></a>  

- Test login, registration, and password reset functionalities.  
- Tools: **Burp Suite**, **Hydra**, and **ZAP**.  

### Bruteforce using Hydra  
```bash  
hydra -L usernames.txt -P passwords.txt https://example.com/login -vV  
```  

---  

## 6. Session Management <a name="Session_Management"></a>  

- Verify cookie attributes: **httpOnly**, **Secure**, **SameSite**.  
- Tools: **Burp Suite** for session token analysis.  

---  

## 7. Authorization Testing <a name="Authorization_Testing"></a>  

- Test for privilege escalation: horizontal and vertical.  
- Use **Burp Intruder** to manipulate role IDs.  

---  

## 8. Data Validation and Injection <a name="Data_Validation"></a>  

1. **SQL Injection**  
   ```bash  
   sqlmap -u "https://example.com?id=1" --batch --dbs  
   ```  

2. **XSS Fuzzing with XSStrike**  
   ```bash  
   python3 xsstrike.py -u "https://example.com/search?q=test"  
   ```  

---  

## 9. Denial of Service (DoS) <a name="Denial_of_Service"></a>  

- Use **slowloris** or **hulk** for basic DoS testing.  
   ```bash  
   slowloris https://example.com  
   ```  

---  

## 10. Advanced Techniques <a name="Advanced_Techniques"></a>  

- **GraphQL Testing**:  
   ```bash  
   graphql-cop -t https://example.com/graphql  
   ```  

- **Race Condition Testing**:  
   ```bash  
   turbo-intruder race_condition_script.py  
   ```  

---  

### Closing Note  

Stay curious and ethical. Every step of testing adds to a secure cyberspace. Happy Hunting!  

---  

**Sources and Tools**  
- [OWASP WSTG](https://owasp.org/www-project-web-security-testing-guide/)  
- [CyberTechAjju Tools](https://github.com/cybertechajju)  


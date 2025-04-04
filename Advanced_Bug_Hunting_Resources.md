# Advanced Bug Hunting Resources

## 1. Recon Techniques & Resources

### Subdomain Discovery
- [Project Discovery](https://chaos.projectdiscovery.io/) - Aggregation of bounty targets
- [DNS Dumpster](https://dnsdumpster.com/) - DNS recon & research
- [Grayhatwarfare](https://buckets.grayhatwarfare.com/) - Search public buckets
- [Censys.io](https://censys.io/) - Search engine for Internet-connected devices
- [LeakIX](https://leakix.net/) - Search engine for internet leaks
- [Shodan](https://www.shodan.io/) - Search engine for Internet of Things
- [FullHunt](https://fullhunt.io/) - Attack surface management platform

### Wordlists
- [Assetnote Wordlists](https://wordlists.assetnote.io/) - Comprehensive discovery wordlists
- [FuzzDB](https://github.com/fuzzdb-project/fuzzdb) - Dictionary of attack patterns
- [PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings) - A list of useful payloads
- [SecLists](https://github.com/danielmiessler/SecLists) - Collection of security wordlists

### Reconnaissance Tools
- [ReconFTW](https://github.com/six2dez/reconftw) - Full recon automation
- [ProjectDiscovery Tools](https://github.com/projectdiscovery) - httpx, subfinder, nuclei
- [Sudomy](https://github.com/Screetsec/Sudomy) - Subdomain enumeration
- [PureDNS](https://github.com/d3mondev/puredns) - Fast domain resolver and subdomain bruteforcing
- [Axiom](https://github.com/pry0cc/axiom) - Dynamic infrastructure for offensive security

## 2. Vulnerability Testing & Exploitation

### Web App Vulnerabilities
- [OWASP Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/) - Comprehensive testing guide
- [HackTricks](https://book.hacktricks.xyz/) - Collection of hacking tricks
- [Awesome-Web-Security](https://github.com/qazbnm456/awesome-web-security) - Curated list of resources
- [Web Application Exploits and Defenses](https://google-gruyere.appspot.com/) - Google's codelab
- [OWASP Top Ten](https://owasp.org/www-project-top-ten/) - Most critical security risks

### API Security
- [API Security Checklist](https://github.com/shieldfy/API-Security-Checklist) - Checklist for API security
- [OWASP API Security Project](https://owasp.org/www-project-api-security/) - Top 10 API vulnerabilities
- [API Security Encyclopedia](https://apisecurity.io/encyclopedia/content/api-security-encyclopedia.htm) - Common API security issues
- [GraphQL Hacking](https://github.com/bkimminich/juice-shop) - OWASP Juice Shop GraphQL challenges
- [APIs Pentest Book](https://pentestbook.six2dez.com/enumeration/webservices/apis) - Six2dez API Pentest Book

### Modern Web App Testing
- [DOM Invader](https://portswigger.net/burp/documentation/desktop/tools/dom-invader) - Burp Suite DOM XSS finder
- [JWT_Tool](https://github.com/ticarpi/jwt_tool) - Testing, tweaking and cracking JWTs
- [OAuth 2.0 Threat Model](https://tools.ietf.org/html/rfc6819) - Security considerations for OAuth 2.0
- [SAML Raider](https://github.com/SAMLRaider/SAMLRaider) - SAML2 Burp Extension
- [Inql](https://github.com/doyensec/inql) - GraphQL security scanner

## 3. Mobile Security Resources

### Android
- [MOBSF](https://github.com/MobSF/Mobile-Security-Framework-MobSF) - Mobile Security Framework
- [Frida](https://frida.re/) - Dynamic instrumentation toolkit
- [QARK](https://github.com/linkedin/qark) - Quick Android Review Kit
- [APKLeaks](https://github.com/dwisiswant0/apkleaks) - Scanning APK for URIs, endpoints & secrets
- [Drozer](https://github.com/FSecureLABS/drozer) - Android security assessment framework

### iOS
- [Objection](https://github.com/sensepost/objection) - Runtime mobile exploration toolkit
- [iLEAPP](https://github.com/abrignoni/iLEAPP) - iOS Logs, Events, And Plist Parser
- [Needle](https://github.com/FSecureLABS/needle) - iOS Security Testing Framework
- [SSL Kill Switch](https://github.com/nabla-c0d3/ssl-kill-switch2) - Disable SSL certificate validation
- [Passionfruit](https://github.com/chaitin/passionfruit) - iOS app runtime manipulation

## 4. Cloud Security Resources

### AWS
- [S3Scanner](https://github.com/sa7mon/S3Scanner) - Find open S3 buckets
- [PACU](https://github.com/RhinoSecurityLabs/pacu) - AWS exploitation framework
- [CloudSploit](https://github.com/aquasecurity/cloudsploit) - Cloud security auditing
- [AWS Security Tools](https://github.com/toniblyx/my-arsenal-of-aws-security-tools) - Arsenal of AWS security tools
- [ScoutSuite](https://github.com/nccgroup/ScoutSuite) - Multi-cloud security auditing tool

### GCP & Azure
- [BlobHunter](https://github.com/cyberark/BlobHunter) - Find misconfigured Azure Blob
- [AzureHound](https://github.com/BloodHoundAD/AzureHound) - Azure attack path collection
- [GCPBucketBrute](https://github.com/RhinoSecurityLabs/GCPBucketBrute) - Enumerate Google Storage buckets
- [gcp-iam-collector](https://github.com/marcin-kolda/gcp-iam-collector) - Google Cloud IAM collector
- [Cartography](https://github.com/lyft/cartography) - Consolidate infrastructure assets in graph format

## 5. Automation & Bug Bounty Workflows

### Productivity Tools
- [Axiom](https://github.com/pry0cc/axiom) - Dynamic infrastructure framework
- [Interlace](https://github.com/codingo/Interlace) - Asynchronous command execution
- [Nuclei Templates](https://github.com/projectdiscovery/nuclei-templates) - Community templates for Nuclei
- [Notify](https://github.com/projectdiscovery/notify) - Stream results to multiple services
- [Slack Bugbot](https://github.com/Leoid/BugBot) - Slack bot for bug bounty automation

### CI/CD Security
- [Checkov](https://github.com/bridgecrewio/checkov) - Static analysis for IaC
- [KICS](https://github.com/Checkmarx/kics) - Find security vulnerabilities in IaC
- [GitLeaks](https://github.com/zricethezav/gitleaks) - Detect hardcoded secrets
- [Semgrep](https://github.com/returntocorp/semgrep) - Static analysis at ludicrous speed
- [TFSec](https://github.com/aquasecurity/tfsec) - Security scanner for Terraform code

## 6. Specialized Tools & Techniques

### Fuzzing & Scanning
- [Wfuzz](https://github.com/xmendez/wfuzz) - Web fuzzer
- [FuzzDB](https://github.com/fuzzdb-project/fuzzdb) - Attack patterns
- [AFL++](https://github.com/AFLplusplus/AFLplusplus) - Fuzzing framework
- [Domato](https://github.com/googleprojectzero/domato) - DOM fuzzer
- [TKO Subs](https://github.com/anshumanbh/tko-subs) - Detect and takeover subdomains

### Advanced Techniques
- [Blind SSRF Testing](https://portswigger.net/web-security/ssrf/blind) - PortSwigger guide
- [Request Smuggling](https://github.com/PortSwigger/http-request-smuggler) - HTTP request smuggling
- [Prototype Pollution](https://github.com/BlackFan/client-side-prototype-pollution) - Client-side prototype pollution
- [WAF Bypass Techniques](https://github.com/0xInfection/Awesome-WAF) - WAF bypass techniques
- [CSP Bypass](https://github.com/PortSwigger/csp-auditor) - Content Security Policy auditing

## 7. Bug Bounty Platforms and Programs

### Bug Bounty Platforms
- [HackerOne](https://www.hackerone.com/) - Vulnerability coordination platform
- [Bugcrowd](https://www.bugcrowd.com/) - Crowdsourced security platform
- [Intigriti](https://www.intigriti.com/) - European bug bounty platform
- [YesWeHack](https://www.yeswehack.com/) - Global bug bounty platform
- [Synack](https://www.synack.com/) - Private bug bounty platform

### Self-Hosted Programs
- [List of Programs](https://github.com/projectdiscovery/public-bugbounty-programs) - List of bug bounty programs
- [Vulnerability Disclosure Programs](https://github.com/disclose/diodb) - Public VDP directory
- [Bug Bounty Forum](https://bugbountyforum.com/) - Community-based forum
- [Bug Bounty Platforms](https://www.bugcrowd.com/bug-bounty-list/) - Bugcrowd's list
- [Open Bug Bounty](https://www.openbugbounty.org/) - Free bug bounty program

## 8. Real-World Exploits & Reference Materials

### Write-ups & Case Studies
- [HackerOne Hacktivity](https://hackerone.com/hacktivity) - Public vulnerability reports
- [Pentester Land](https://pentester.land/list-of-bug-bounty-writeups.html) - List of bug bounty writeups
- [InfoSec Write-ups](https://infosecwriteups.com/) - Medium collection of write-ups
- [Bug Bounty POCs](https://github.com/daffainfo/AllAboutBugBounty) - All about bug bounty references
- [Awesome CVE PoC](https://github.com/qazbnm456/awesome-cve-poc) - Curated list of CVE PoCs

### Historical Vulnerabilities
- [Log4Shell](https://github.com/YfryTchsGD/Log4jAttackSurface) - Log4j attack surface
- [ProxyLogon](https://github.com/sophoslabs/CVE-2021-26855) - Exchange Server vulnerability
- [Spectre & Meltdown](https://meltdownattack.com/) - CPU vulnerabilities
- [PrintNightmare](https://github.com/cube0x0/CVE-2021-1675) - Windows Print Spooler
- [SolarWinds Supply Chain](https://github.com/cisagov/SolarWinds-Sunburst-Guidance) - CISA guidance

## 9. Advanced Training & Education

### Cybersecurity Courses
- [eLearnSecurity](https://elearnsecurity.com/) - Practical penetration testing training
- [SANS](https://www.sans.org/) - Information security training
- [Pentester Academy](https://www.pentesteracademy.com/) - Penetration testing courses
- [Cybrary](https://www.cybrary.it/) - Free cybersecurity training
- [Hack The Box Academy](https://academy.hackthebox.com/) - Hands-on cybersecurity training

### CTF Platforms
- [CTFTime](https://ctftime.org/) - CTF event listing
- [PicoCTF](https://picoctf.org/) - Computer security education
- [VulnHub](https://www.vulnhub.com/) - Vulnerable machines
- [Damn Vulnerable Web Application](https://github.com/digininja/DVWA) - PHP/MySQL vulnerable app
- [OWASP WebGoat](https://github.com/WebGoat/WebGoat) - Deliberately insecure app

## 10. Emerging Threats & Research

### Supply Chain Security
- [DepChecker](https://github.com/jeremylong/DependencyCheck) - Check dependencies
- [dep-scan](https://github.com/AppThreat/dep-scan) - Dependency scanner
- [Snyk](https://snyk.io/) - Dependency vulnerability scanner
- [Dependency-Track](https://github.com/DependencyTrack/dependency-track) - SBOM vulnerability tracker
- [npm-audit](https://docs.npmjs.com/cli/v6/commands/npm-audit) - Audit npm packages

### Zero-Day Research
- [Project Zero](https://googleprojectzero.blogspot.com/) - Google's vulnerability research team
- [The Internet Bug Bounty](https://internetbugbounty.org/) - Critical open source vulnerabilities
- [Exploit Database](https://www.exploit-db.com/) - Archive of exploits
- [cve.mitre.org](https://cve.mitre.org/) - Common Vulnerabilities and Exposures
- [Common Weakness Enumeration](https://cwe.mitre.org/) - Common software weaknesses

### AI Security
- [GPT Prompt Injection](https://github.com/greshake/GPT-security) - AI prompt injection attacks
- [AI Red Team](https://github.com/austin-taylor/ai-redteam) - Red teaming AI systems
- [Machine Learning Security](https://github.com/ckane/machine-learning-for-security) - ML for security
- [Awesome LLM Security](https://github.com/corca-ai/awesome-llm-security) - LLM security resources
- [AI Risk Database](https://airisk.io/) - AI vulnerability database

## Acknowledgements

Many thanks to the security community for sharing their knowledge and tools. This resource compilation wouldn't be possible without the open-source community and security researchers around the world.

For more information, contributions, and updates please visit the main [repository](https://github.com/username/bugbounty).

---

<p align="center">
  <i>Remember: With great power comes great responsibility. Use these tools ethically.</i>
</p> 

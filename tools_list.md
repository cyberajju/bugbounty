# Bug Bounty Tools Collection

<p align="center">
  <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExcjAxanoxMXI3Z3Btc2kwdHdlcTl5emNmYzRweWx6anlndnhpcWw1eSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/YQitE4YNQNahy/giphy.gif" width="300">
</p>

<p align="center">
  <i>A comprehensive collection of tools for Bug Bounty Hunting and Web Application Security Testing</i>
</p>

## Table of Contents
- [Installation Tools](#installation-tools)
- [Reconnaissance](#reconnaissance)
  - [Subdomain Enumeration](#subdomain-enumeration)
  - [DNS Analysis](#dns-analysis)
  - [Network Scanning](#network-scanning)
  - [Web Crawling](#web-crawling)
  - [Visual Reconnaissance](#visual-reconnaissance)
- [Content Discovery](#content-discovery)
  - [Directory Brute Force](#directory-brute-force)
  - [Parameter Discovery](#parameter-discovery)
  - [JS Analysis](#js-analysis)
- [Vulnerability Scanning](#vulnerability-scanning)
  - [General Scanners](#general-scanners)
  - [CMS Scanners](#cms-scanners)
  - [API Testing](#api-testing)
  - [XSS Detection](#xss-detection)
  - [SQL Injection](#sql-injection)
  - [SSRF Tools](#ssrf-tools)
  - [Template Injection](#template-injection)
  - [Other Vulnerability Classes](#other-vulnerability-classes)
- [Exploitation](#exploitation)
- [Wordlists](#wordlists)
- [Utility Tools](#utility-tools)
- [New Tools (2023-2025)](#new-tools-2023-2025)
- [Installation Scripts](#installation-scripts)
- [Online Resources](#online-resources)

## Installation Tools

### All-in-One Installation Scripts

| Tool | Description | Link |
|------|-------------|------|
| bbht | Bug Bounty Hunting Tools installer | [https://github.com/nahamsec/bbht](https://github.com/nahamsec/bbht) |
| VPS-Bug-Bounty-Tools | Script for setting up VPS for bug bounty | [https://github.com/drak3hft7/VPS-Bug-Bounty-Tools](https://github.com/drak3hft7/VPS-Bug-Bounty-Tools) |
| BugBountyTools | Comprehensive bug bounty environment setup | [https://github.com/m4ll0k/BugBountyTools](https://github.com/m4ll0k/BugBountyTools) |
| LazyRecon | Reconnaissance automation script | [https://github.com/nahamsec/lazyrecon](https://github.com/nahamsec/lazyrecon) |
| pentestkit | Penetration testing and bug bounty kit | [https://github.com/Cipher-Daemon/pentestkit](https://github.com/Cipher-Daemon/pentestkit) |

## Reconnaissance

### Subdomain Enumeration

| Tool | Description | Link |
|------|-------------|------|
| Amass | In-depth Attack Surface Mapping and Asset Discovery | [https://github.com/OWASP/Amass](https://github.com/OWASP/Amass) |
| Subfinder | Fast passive subdomain enumeration tool | [https://github.com/projectdiscovery/subfinder](https://github.com/projectdiscovery/subfinder) |
| Sublist3r | Fast subdomains enumeration tool | [https://github.com/aboul3la/Sublist3r](https://github.com/aboul3la/Sublist3r) |
| Assetfinder | Find domains and subdomains | [https://github.com/tomnomnom/assetfinder](https://github.com/tomnomnom/assetfinder) |
| Knockpy | Subdomain enumeration | [https://github.com/guelfoweb/knock](https://github.com/guelfoweb/knock) |
| Github-subdomains | Find subdomains on GitHub | [https://github.com/gwen001/github-subdomains](https://github.com/gwen001/github-subdomains) |
| Gitlab-subdomains | Find subdomains on GitLab | [https://github.com/gwen001/gitlab-subdomains](https://github.com/gwen001/gitlab-subdomains) |
| Findomain | Cross-platform subdomain enumerator | [https://github.com/Findomain/Findomain](https://github.com/Findomain/Findomain) |
| Crobat | Rapid Subdomain Scanner | [https://github.com/Cgboal/SonarSearch](https://github.com/Cgboal/SonarSearch) |
| Sudomy | Subdomain enumeration tool | [https://github.com/Screetsec/Sudomy](https://github.com/Screetsec/Sudomy) |
| Crtndstry | Yet another subdomain finder | [https://github.com/nahamsec/crtndstry](https://github.com/nahamsec/crtndstry) |
| Puredns | Fast domain resolver and subdomain bruteforcing | [https://github.com/d3mondev/puredns](https://github.com/d3mondev/puredns) |

### DNS Analysis

| Tool | Description | Link |
|------|-------------|------|
| Dnsx | Fast DNS toolkit | [https://github.com/projectdiscovery/dnsx](https://github.com/projectdiscovery/dnsx) |
| MassDNS | High-performance DNS stub resolver | [https://github.com/blechschmidt/massdns](https://github.com/blechschmidt/massdns) |
| Dnsgen | DNS wordlist generator | [https://github.com/ProjectAnte/dnsgen](https://github.com/ProjectAnte/dnsgen) |
| AltDNS | Subdomain discovery through alterations | [https://github.com/infosec-au/altdns](https://github.com/infosec-au/altdns) |
| DNSValidator | DNS validation toolset | [https://github.com/vortexau/dnsvalidator](https://github.com/vortexau/dnsvalidator) |
| Dnsrecon | Advanced DNS enumeration | [https://github.com/darkoperator/dnsrecon](https://github.com/darkoperator/dnsrecon) |

### Network Scanning

| Tool | Description | Link |
|------|-------------|------|
| Nmap | Network discovery and security auditing | [https://nmap.org/](https://nmap.org/) |
| Masscan | Mass IP port scanner | [https://github.com/robertdavidgraham/masscan](https://github.com/robertdavidgraham/masscan) |
| Naabu | Fast port scanner | [https://github.com/projectdiscovery/naabu](https://github.com/projectdiscovery/naabu) |
| Smap | Alternative port scanner | [https://github.com/s0md3v/Smap](https://github.com/s0md3v/Smap) |
| RustScan | Modern port scanner | [https://github.com/RustScan/RustScan](https://github.com/RustScan/RustScan) |

### Web Crawling

| Tool | Description | Link |
|------|-------------|------|
| Katana | Next-generation crawling and spidering framework | [https://github.com/projectdiscovery/katana](https://github.com/projectdiscovery/katana) |
| Gospider | Fast web spider | [https://github.com/jaeles-project/gospider](https://github.com/jaeles-project/gospider) |
| Hakrawler | Simple, fast web crawler | [https://github.com/hakluke/hakrawler](https://github.com/hakluke/hakrawler) |
| Waybackurls | Fetch all URLs from Wayback Machine | [https://github.com/tomnomnom/waybackurls](https://github.com/tomnomnom/waybackurls) |
| Gau | Get All URLs | [https://github.com/lc/gau](https://github.com/lc/gau) |
| GauPlus | Enhanced version of gau | [https://github.com/bp0lr/gauplus](https://github.com/bp0lr/gauplus) |
| Feroxbuster | Fast content discovery tool | [https://github.com/epi052/feroxbuster](https://github.com/epi052/feroxbuster) |

### Visual Reconnaissance

| Tool | Description | Link |
|------|-------------|------|
| Aquatone | Visual inspection of websites | [https://github.com/michenriksen/aquatone](https://github.com/michenriksen/aquatone) |
| Gowitness | Web screenshot utility | [https://github.com/sensepost/gowitness](https://github.com/sensepost/gowitness) |
| Webscreenshot | Screenshot websites | [https://github.com/maaaaz/webscreenshot](https://github.com/maaaaz/webscreenshot) |
| EyeWitness | Website screenshot tool | [https://github.com/FortyNorthSecurity/EyeWitness](https://github.com/FortyNorthSecurity/EyeWitness) |

## Content Discovery

### Directory Brute Force

| Tool | Description | Link |
|------|-------------|------|
| Dirsearch | Web path discovery | [https://github.com/maurosoria/dirsearch](https://github.com/maurosoria/dirsearch) |
| Ffuf | Fast web fuzzer | [https://github.com/ffuf/ffuf](https://github.com/ffuf/ffuf) |
| Gobuster | Directory/file & DNS busting tool | [https://github.com/OJ/gobuster](https://github.com/OJ/gobuster) |
| Wfuzz | Web application fuzzer | [https://github.com/xmendez/wfuzz](https://github.com/xmendez/wfuzz) |
| Fuzzuli | Web fuzzer | [https://github.com/musana/fuzzuli](https://github.com/musana/fuzzuli) |
| Dirbuster | Directory bruteforcing tool | [https://gitlab.com/kalilinux/packages/dirbuster](https://gitlab.com/kalilinux/packages/dirbuster) |

### Parameter Discovery

| Tool | Description | Link |
|------|-------------|------|
| Arjun | HTTP parameter discovery suite | [https://github.com/s0md3v/Arjun](https://github.com/s0md3v/Arjun) |
| x8 | Hidden parameters discovery suite | [https://github.com/Sh1Yo/x8](https://github.com/Sh1Yo/x8) |
| ParamSpider | Parameter miner for web applications | [https://github.com/devanshbatham/ParamSpider](https://github.com/devanshbatham/ParamSpider) |
| Parameth | Parameter brute-forcing | [https://github.com/maK-/parameth](https://github.com/maK-/parameth) |

### JS Analysis

| Tool | Description | Link |
|------|-------------|------|
| LinkFinder | Discover endpoints in JavaScript | [https://github.com/GerbenJavado/LinkFinder](https://github.com/GerbenJavado/LinkFinder) |
| SecretFinder | Find sensitive data in JavaScript | [https://github.com/m4ll0k/SecretFinder](https://github.com/m4ll0k/SecretFinder) |
| JSParser | Extract endpoints from JS files | [https://github.com/nahamsec/JSParser](https://github.com/nahamsec/JSParser) |
| subjs | Get JavaScript files from URLs | [https://github.com/lc/subjs](https://github.com/lc/subjs) |
| xnLinkFinder | Enhanced endpoint discovery | [https://github.com/xnl-h4ck3r/xnLinkFinder](https://github.com/xnl-h4ck3r/xnLinkFinder) |
| JSScanner | Scan JS files for endpoints and secrets | [https://github.com/dark-warlord14/JSScanner](https://github.com/dark-warlord14/JSScanner) |

## Vulnerability Scanning

### General Scanners

| Tool | Description | Link |
|------|-------------|------|
| Nuclei | Fast template-based scanner | [https://github.com/projectdiscovery/nuclei](https://github.com/projectdiscovery/nuclei) |
| Jaeles | Automated Web Application Testing Framework | [https://github.com/jaeles-project/jaeles](https://github.com/jaeles-project/jaeles) |
| Nikto | Web server scanner | [https://github.com/sullo/nikto](https://github.com/sullo/nikto) |
| Wapiti | Web vulnerability scanner | [https://github.com/wapiti-scanner/wapiti](https://github.com/wapiti-scanner/wapiti) |
| Osmedeus | Fully automated offensive security tool | [https://github.com/j3ssie/osmedeus](https://github.com/j3ssie/osmedeus) |
| Cariddi | Take a list of domains and scan for endpoints, secrets, and more | [https://github.com/edoardottt/cariddi](https://github.com/edoardottt/cariddi) |

### CMS Scanners

| Tool | Description | Link |
|------|-------------|------|
| WPScan | WordPress security scanner | [https://github.com/wpscanteam/wpscan](https://github.com/wpscanteam/wpscan) |
| Droopescan | Scanner for Drupal, Silverstripe, and others | [https://github.com/droope/droopescan](https://github.com/droope/droopescan) |
| AEM-Hacker | Tools to identify and exploit Adobe Experience Manager | [https://github.com/0ang3el/aem-hacker](https://github.com/0ang3el/aem-hacker) |
| CMSeeK | CMS detection and exploitation | [https://github.com/Tuhinshubhra/CMSeeK](https://github.com/Tuhinshubhra/CMSeeK) |
| Joomscan | Joomla vulnerability scanner | [https://github.com/OWASP/joomscan](https://github.com/OWASP/joomscan) |

### API Testing

| Tool | Description | Link |
|------|-------------|------|
| Kiterunner | API discovery and scanning tool | [https://github.com/assetnote/kiterunner](https://github.com/assetnote/kiterunner) |
| MindAPI | API security testing checklist & toolset | [https://github.com/dsopas/MindAPI](https://github.com/dsopas/MindAPI) |
| APICheck | HTTP API testing toolkit | [https://github.com/BBVA/apicheck](https://github.com/BBVA/apicheck) |
| Astra | Automated Security Testing for REST APIs | [https://github.com/flipkart-incubator/Astra](https://github.com/flipkart-incubator/Astra) |
| APIFuzzer | API fuzzer | [https://github.com/KissPeter/APIFuzzer](https://github.com/KissPeter/APIFuzzer) |
| TnT-Fuzzer | API fuzzer | [https://github.com/Teebytes/TnT-Fuzzer](https://github.com/Teebytes/TnT-Fuzzer) |

### XSS Detection

| Tool | Description | Link |
|------|-------------|------|
| XSStrike | Advanced XSS scanner | [https://github.com/s0md3v/XSStrike](https://github.com/s0md3v/XSStrike) |
| Dalfox | Fast parameter analysis XSS scanner | [https://github.com/hahwul/dalfox](https://github.com/hahwul/dalfox) |
| XSS-Loader | XSS payload generator | [https://github.com/capture0x/XSS-LOADER](https://github.com/capture0x/XSS-LOADER) |
| Freq | Detect XSS with regex pattern testing | [https://github.com/takshal/freq](https://github.com/takshal/freq) |
| Gxss | Find XSS params | [https://github.com/KathanP19/Gxss](https://github.com/KathanP19/Gxss) |
| kxss | Contextual XSS scanner | [https://github.com/tomnomnom/hacks/tree/master/kxss](https://github.com/tomnomnom/hacks/tree/master/kxss) |
| XSSHunter | XSS discovery and exploitation | [https://github.com/mandatoryprogrammer/xsshunter](https://github.com/mandatoryprogrammer/xsshunter) |

### SQL Injection

| Tool | Description | Link |
|------|-------------|------|
| SQLMap | Automatic SQL injection tool | [https://github.com/sqlmapproject/sqlmap](https://github.com/sqlmapproject/sqlmap) |
| NoSQLMap | NoSQL injection tool | [https://github.com/codingo/NoSQLMap](https://github.com/codingo/NoSQLMap) |
| Jeeves | Advanced SQL injection tool | [https://github.com/ferreiraklet/Jeeves](https://github.com/ferreiraklet/Jeeves) |
| SQLiScanner | Automatic SQL injection | [https://github.com/0xbug/SQLiScanner](https://github.com/0xbug/SQLiScanner) |
| DSSS | Damn Small SQLi Scanner | [https://github.com/stamparm/DSSS](https://github.com/stamparm/DSSS) |
| SQLmate | SQL injection exploitation | [https://github.com/s0md3v/sqlmate](https://github.com/s0md3v/sqlmate) |

### SSRF Tools

| Tool | Description | Link |
|------|-------------|------|
| SSRFmap | Automatic SSRF fuzzer and exploitation tool | [https://github.com/swisskyrepo/SSRFmap](https://github.com/swisskyrepo/SSRFmap) |
| Gopherus | Generate gopher link for exploiting SSRF | [https://github.com/tarunkant/Gopherus](https://github.com/tarunkant/Gopherus) |
| Interactsh | OOB interaction gathering server and client | [https://github.com/projectdiscovery/interactsh](https://github.com/projectdiscovery/interactsh) |
| AutoSSRF | Automatic SSRF finder | [https://github.com/Th0h0/autossrf](https://github.com/Th0h0/autossrf) |
| SSRFire | Automated SSRF finder | [https://github.com/ksharinarayanan/SSRFire](https://github.com/ksharinarayanan/SSRFire) |

### Template Injection

| Tool | Description | Link |
|------|-------------|------|
| tplmap | Automatic Server-Side Template Injection | [https://github.com/epinna/tplmap](https://github.com/epinna/tplmap) |
| SSTImap | Automatic SSTI detection | [https://github.com/vladko312/SSTImap](https://github.com/vladko312/SSTImap) |
| Injecto | SSTI scanner and exploiter | [https://github.com/BountyStrike/Injecto](https://github.com/BountyStrike/Injecto) |

### Other Vulnerability Classes

| Tool | Description | Link |
|------|-------------|------|
| Dontgo403 | Bypass 403 forbidden | [https://github.com/devploit/dontgo403](https://github.com/devploit/dontgo403) |
| Corsy | CORS misconfiguration scanner | [https://github.com/s0md3v/Corsy](https://github.com/s0md3v/Corsy) |
| CORScanner | CORS scanner | [https://github.com/chenjj/CORScanner](https://github.com/chenjj/CORScanner) |
| LFISuite | LFI exploitation suite | [https://github.com/D35m0nd142/LFISuite](https://github.com/D35m0nd142/LFISuite) |
| ppfuzz | Prototype pollution fuzzer | [https://github.com/dwisiswant0/ppfuzz](https://github.com/dwisiswant0/ppfuzz) |
| ppmap | Prototype pollution finder | [https://github.com/kleiton0x00/ppmap](https://github.com/kleiton0x00/ppmap) |
| JWT_Tool | JWT testing, tampering, and cracking | [https://github.com/ticarpi/jwt_tool](https://github.com/ticarpi/jwt_tool) |
| Photon | Incredibly fast crawler | [https://github.com/s0md3v/Photon](https://github.com/s0md3v/Photon) |

## Exploitation

| Tool | Description | Link |
|------|-------------|------|
| teh_s3_bucketeers | Amazon S3 bucket finder | [https://github.com/tomdev/teh_s3_bucketeers](https://github.com/tomdev/teh_s3_bucketeers) |
| lazys3 | S3 bucket enumeration | [https://github.com/nahamsec/lazys3](https://github.com/nahamsec/lazys3) |
| virtual-host-discovery | Find virtual hosts on target servers | [https://github.com/jobertabma/virtual-host-discovery](https://github.com/jobertabma/virtual-host-discovery) |
| SubOver | Subdomain takeover scanner | [https://github.com/Ice3man543/SubOver](https://github.com/Ice3man543/SubOver) |
| TKO-Subs | Subdomain takeover scanner | [https://github.com/anshumanbh/tko-subs](https://github.com/anshumanbh/tko-subs) |
| Takeover | Subdomain takeover tool | [https://github.com/m4ll0k/takeover](https://github.com/m4ll0k/takeover) |
| GitHacker | Git source code leakage exploit | [https://github.com/WangYihang/GitHacker](https://github.com/WangYihang/GitHacker) |

## Wordlists

| Tool | Description | Link |
|------|-------------|------|
| SecLists | Collection of security wordlists | [https://github.com/danielmiessler/SecLists](https://github.com/danielmiessler/SecLists) |
| OneForAll | Comprehensive wordlists | [https://github.com/six2dez/OneListForAll](https://github.com/six2dez/OneListForAll) |
| Assetnote Wordlists | High quality wordlists | [https://wordlists.assetnote.io/](https://wordlists.assetnote.io/) |
| PayloadsAllTheThings | A list of useful payloads and bypasses | [https://github.com/swisskyrepo/PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings) |
| FuzzDB | Dictionary of attack patterns | [https://github.com/fuzzdb-project/fuzzdb](https://github.com/fuzzdb-project/fuzzdb) |
| IntruderPayloads | Collection of Burp Intruder payloads | [https://github.com/1N3/IntruderPayloads](https://github.com/1N3/IntruderPayloads) |
| RobotsDisallowed | Harvesting interesting robots.txt entries | [https://github.com/danielmiessler/RobotsDisallowed](https://github.com/danielmiessler/RobotsDisallowed) |
| Fuzz.txt | Potentially dangerous files | [https://github.com/Bo0oM/fuzz.txt](https://github.com/Bo0oM/fuzz.txt) |
| Leaky-Paths | List of paths that potentially leak sensitive info | [https://github.com/ayoubfathi/leaky-paths](https://github.com/ayoubfathi/leaky-paths) |

## Utility Tools

| Tool | Description | Link |
|------|-------------|------|
| Anew | Append lines from stdin to a file, but only if they don't already exist | [https://github.com/tomnomnom/anew](https://github.com/tomnomnom/anew) |
| Unew | Command line tool for keeping only unique entries from multiple sources | [https://github.com/dwisiswant0/unew](https://github.com/dwisiswant0/unew) |
| Gf | A wrapper around grep for convenient pattern matching | [https://github.com/tomnomnom/gf](https://github.com/tomnomnom/gf) |
| Httprobe | Take a list of domains and probe for working HTTP and HTTPS servers | [https://github.com/tomnomnom/httprobe](https://github.com/tomnomnom/httprobe) |
| Httpx | Fast HTTP toolkit for running multiple probes | [https://github.com/projectdiscovery/httpx](https://github.com/projectdiscovery/httpx) |
| Unfurl | Extract and analyze domains from URLs | [https://github.com/tomnomnom/unfurl](https://github.com/tomnomnom/unfurl) |
| Uro | URL optimization tool | [https://github.com/s0md3v/uro](https://github.com/s0md3v/uro) |
| Qsreplace | Replace all query string values with a user-supplied value | [https://github.com/tomnomnom/qsreplace](https://github.com/tomnomnom/qsreplace) |
| SocialHunter | Find broken social media links that can lead to account takeover | [https://github.com/utkusen/socialhunter](https://github.com/utkusen/socialhunter) |
| anti-burl | A wrapper around curl that extracts URLs | [https://github.com/tomnomnom/hacks/tree/master/anti-burl](https://github.com/tomnomnom/hacks/tree/master/anti-burl) |
| getallurls | Fetch known URLs from AlienVault's Open Threat Exchange | [https://github.com/lc/hacks/tree/master/getallurls](https://github.com/lc/hacks/tree/master/getallurls) |
| gron | Make JSON greppable | [https://github.com/tomnomnom/gron](https://github.com/tomnomnom/gron) |
| Interlace | Easily turn single-threaded command-line applications into fast, multi-threaded ones | [https://github.com/codingo/Interlace](https://github.com/codingo/Interlace) |
| jq | Lightweight and flexible command-line JSON processor | [https://github.com/stedolan/jq](https://github.com/stedolan/jq) |
| Tmux | Terminal multiplexer | [https://github.com/tmux/tmux](https://github.com/tmux/tmux) |
| Asnlookup | Bulk ASN lookup tool | [https://github.com/yassineaboukir/Asnlookup](https://github.com/yassineaboukir/Asnlookup) |
| Ripgrep | Recursively search directories for a regex pattern | [https://github.com/BurntSushi/ripgrep](https://github.com/BurntSushi/ripgrep) |
| Meg | Fetch many paths for many hosts | [https://github.com/tomnomnom/meg](https://github.com/tomnomnom/meg) |

## Git Tools

| Tool | Description | Link |
|------|-------------|------|
| GitDorker | Scan GitHub repos for sensitive data | [https://github.com/obheda12/GitDorker](https://github.com/obheda12/GitDorker) |
| gitGraber | Monitor GitHub to find sensitive data in real-time | [https://github.com/hisxo/gitGraber](https://github.com/hisxo/gitGraber) |
| GitHacker | Find sensitive information in Git repos | [https://github.com/WangYihang/GitHacker](https://github.com/WangYihang/GitHacker) |
| GitTools | Tools to download, extract, and search Git repos | [https://github.com/internetwache/GitTools](https://github.com/internetwache/GitTools) |
| gitrob | Reconnaissance tool for GitHub organizations | [https://github.com/michenriksen/gitrob](https://github.com/michenriksen/gitrob) |
| git-secrets | Prevents committing secrets to a git repo | [https://github.com/awslabs/git-secrets](https://github.com/awslabs/git-secrets) |
| gitleaks | Scan git repos for secrets | [https://github.com/zricethezav/gitleaks](https://github.com/zricethezav/gitleaks) |
| truffleHog | Find secrets in git repositories | [https://github.com/trufflesecurity/trufflehog](https://github.com/trufflesecurity/trufflehog) |

## Sensitive Data Finding

| Tool | Description | Link |
|------|-------------|------|
| DumpsterDiver | Find secrets in various file types | [https://github.com/securing/DumpsterDiver](https://github.com/securing/DumpsterDiver) |
| EarlyBird | Find sensitive data in code | [https://github.com/americanexpress/earlybird](https://github.com/americanexpress/earlybird) |
| TruffleHog | Find credentials in git repos | [https://github.com/trufflesecurity/trufflehog](https://github.com/trufflesecurity/trufflehog) |
| SpiderFoot | OSINT automation tool | [https://github.com/smicallef/spiderfoot](https://github.com/smicallef/spiderfoot) |
| retire.js | Scanner detecting the use of JavaScript libraries with known vulnerabilities | [https://github.com/RetireJS/retire.js](https://github.com/RetireJS/retire.js) |
| shhgit | Find secrets in real time across GitHub, GitLab and BitBucket | [https://github.com/eth0izzle/shhgit](https://github.com/eth0izzle/shhgit) |
| SecretFinder | Find sensitive data in JavaScript files | [https://github.com/m4ll0k/SecretFinder](https://github.com/m4ll0k/SecretFinder) |

## New Tools (2023-2025)

| Tool | Description | Link |
|------|-------------|------|
| Xterminator | AI-Powered XSS detection | [https://github.com/rectify-ai/xterminator](https://github.com/rectify-ai/xterminator) |
| Nuclei v3 | Advanced template-based vulnerability scanner | [https://github.com/projectdiscovery/nuclei](https://github.com/projectdiscovery/nuclei) |
| Katana v2 | Next-generation crawler | [https://github.com/projectdiscovery/katana](https://github.com/projectdiscovery/katana) |
| Notify | Streamlined notification delivery for scanning results | [https://github.com/projectdiscovery/notify](https://github.com/projectdiscovery/notify) |
| GF-Patterns | Collection of regex patterns for grep | [https://github.com/1ndianl33t/Gf-Patterns](https://github.com/1ndianl33t/Gf-Patterns) |
| WhoAPI | API driven domain infrastructure data | [https://whoapi.com/](https://whoapi.com/) |
| AutoRecon | Multi-threaded reconnaissance tool | [https://github.com/Tib3rius/AutoRecon](https://github.com/Tib3rius/AutoRecon) |
| Log4j-scan | A fully automated, accurate, and extensive scanner for Log4j RCE CVE-2021-44228 | [https://github.com/fullhunt/log4j-scan](https://github.com/fullhunt/log4j-scan) |
| h2cSmuggler | HTTP/2 cleartext smuggling tool | [https://github.com/BishopFox/h2cSmuggler](https://github.com/BishopFox/h2cSmuggler) |
| GraphQLMap | GraphQL endpoint exploitation | [https://github.com/swisskyrepo/GraphQLmap](https://github.com/swisskyrepo/GraphQLmap) |
| Inql | GraphQL security testing | [https://github.com/doyensec/inql](https://github.com/doyensec/inql) |
| AWSGoat | Vulnerable by design AWS infrastructure | [https://github.com/ine-labs/AWSGoat](https://github.com/ine-labs/AWSGoat) |
| CDNStrip | Bypass WAF by finding origin server | [https://github.com/j3ssie/cdnstrip](https://github.com/j3ssie/cdnstrip) |
| ACE | Automated, customizable exploiter | [https://github.com/aliasrobotics/RVD](https://github.com/aliasrobotics/RVD) |
| Metlo | API security testing platform | [https://github.com/metlo-labs/metlo](https://github.com/metlo-labs/metlo) |

## Installation Scripts

### BBHT - Nahamsec Bug Bounty Hunting Tools
```bash
git clone https://github.com/nahamsec/bbht.git
cd bbht
chmod +x install.sh
./install.sh
```

### VPS Bug Bounty Tools
```bash
cd /tmp && git clone https://github.com/drak3hft7/VPS-Bug-Bounty-Tools
cd VPS-Bug-Bounty-Tools
sudo ./Tools-BugBounty-installer.sh
```

### Project Discovery Tools Installer
```bash
go install -v github.com/projectdiscovery/nuclei/v2/cmd/nuclei@latest
go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest
go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest
go install -v github.com/projectdiscovery/naabu/v2/cmd/naabu@latest
go install -v github.com/projectdiscovery/dnsx/cmd/dnsx@latest
go install -v github.com/projectdiscovery/katana/cmd/katana@latest
go install -v github.com/projectdiscovery/notify/cmd/notify@latest
go install -v github.com/projectdiscovery/interactsh/cmd/interactsh-client@latest
```

### Quick Essential Tools
```bash
# Install Go (required for many tools)
wget https://go.dev/dl/go1.20.5.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.20.5.linux-amd64.tar.gz
export PATH=$PATH:/usr/local/go/bin

# Essential tools
go install -v github.com/tomnomnom/anew@latest
go install -v github.com/tomnomnom/gf@latest
go install -v github.com/tomnomnom/waybackurls@latest
go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest
go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest
go install -v github.com/projectdiscovery/nuclei/v2/cmd/nuclei@latest
go install -v github.com/lc/gau/v2/cmd/gau@latest
go install -v github.com/ffuf/ffuf@latest
```

## Online Resources

| Resource | Description | Link |
|----------|-------------|------|
| HackerOne | Bug bounty platform | [https://www.hackerone.com/](https://www.hackerone.com/) |
| Bugcrowd | Bug bounty platform | [https://www.bugcrowd.com/](https://www.bugcrowd.com/) |
| Intigriti | European bug bounty platform | [https://www.intigriti.com/](https://www.intigriti.com/) |
| YesWeHack | Bug bounty platform | [https://yeswehack.com/](https://yeswehack.com/) |
| Synack | Private bug bounty platform | [https://www.synack.com/](https://www.synack.com/) |
| OWASP Web Security Testing Guide | Comprehensive testing guide | [https://owasp.org/www-project-web-security-testing-guide/](https://owasp.org/www-project-web-security-testing-guide/) |
| HackTricks | Collection of hacking tricks | [https://book.hacktricks.xyz/](https://book.hacktricks.xyz/) |
| PortSwigger Web Academy | Web security learning platform | [https://portswigger.net/web-security](https://portswigger.net/web-security) |
| Web Application Exploits and Defenses | Google's codelab | [https://google-gruyere.appspot.com/](https://google-gruyere.appspot.com/) |
| OWASP Top Ten | Most critical security risks | [https://owasp.org/www-project-top-ten/](https://owasp.org/www-project-top-ten/) |
| HackerOne Hacktivity | Public vulnerability reports | [https://hackerone.com/hacktivity](https://hackerone.com/hacktivity) |
| Pentester Land | Collection of write-ups | [https://pentester.land/](https://pentester.land/) |
| InfoSec Write-ups | Medium publication for security | [https://infosecwriteups.com/](https://infosecwriteups.com/) |
| Bug Bounty Forum | Community forum | [https://bugbountyforum.com/](https://bugbountyforum.com/) |
| The Internet Bug Bounty | Critical open source vulnerabilities | [https://internetbugbounty.org/](https://internetbugbounty.org/) |
| cve.mitre.org | Common Vulnerabilities and Exposures | [https://cve.mitre.org/](https://cve.mitre.org/) |
| Exploit Database | Archive of exploits | [https://www.exploit-db.com/](https://www.exploit-db.com/) |

---

<p align="center">
  <i>Happy Bug Hunting! 🐞</i>
</p>

<p align="center">
  <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExd2c0aGVnbDdjYmYweHViamo5OXAxMWtnNmVwajJhM2xpdzliamdwYiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/UqGhZVzzgbPy0TQzMG/giphy.gif" width="300">
</p>
``` 

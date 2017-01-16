FuzzDB is the first comprehensive dictionary of attack patterns and payload primitives, predictable resource locations, web backdoors, regex patterns for analyzing server responses and PII, and documentation for software security testing.

Project home: https://github.com/fuzzdb-project/fuzzdb

Note: Some antivirus/antimalware software will alert on FuzzDB. To resolve, the filepath should be whitelisted. There is nothing in FuzzDB that can harm your computer as-is, however due to the risk of local file include attacks it's not recommended to store this repository on a server or other important system.  

# Using FuzzDB #
FuzzDB is like an application security scanner, without the scanner. 
Some ways to use FuzzDB:
  * Website and application service black-box penetration testing with 
   * [OWASP Zap](https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project) proxy's FuzzDB Zap Extension 
   * Burp Proxy's [intruder](http://portswigger.net/intruder/) tool and scanner
   * [PappyProxy](http://www.pappyproxy.com/), a console-based intercepting proxy
  * To identify interesting service responses using grep patterns for PII, credit card numbers, error messages, and more
  * Inside custom tools for testing software and application protocols
  * Crafting security test cases for GUI or command line software with standard test automation tools
  * Incorporating into other Open Source software or commercial products
  * In training materials and documentation
  * To learn about software exploitation techniques
  * To improve your security testing product or service

FuzzDB and its patterns are already included in whole and part in many security tools and projects such as:
  * OWASP Zap Proxy fuzzdb plugin https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project
  * SecLists https://github.com/danielmiessler/SecLists
  * TrustedSec Pentesters Framework https://github.com/trustedsec/ptf
  * Rapid7 Metasploit https://github.com/rapid7/metasploit-framework
  * Portswigger Burp Suite http://portswigger.net
  * Protofuzz https://github.com/trailofbits/protofuzz
  * BlackArch Linux https://www.blackarch.org/
  * ArchStrike Linux https://archstrike.org/
 
# What's in FuzzDB? #
**Attack Patterns -**
FuzzDB contains comprehensive lists of [attack payload](https://github.com/fuzzdb-project/fuzzdb/tree/master/attack) primitives for fault injection testing. 
These patterns, categorized by attack and where appropriate platform type, are known to cause issues like OS command injection, directory listings, directory traversals, source exposure, file upload bypass, authentication bypass, XSS, http header crlf injections, SQL injection, NoSQL injection, and more. For example, FuzzDB catalogs 56 patterns that can potentially be interpreted as a null byte and contains lists of [commonly used methods](https://github.com/fuzzdb-project/fuzzdb/blob/master/attack/business-logic/CommonMethodNames.txt) such as "get, put, test," and name-value pairs than [trigger debug modes](https://github.com/fuzzdb-project/fuzzdb/blob/master/attack/business-logic/CommonDebugParamNames.txt).<br>

**Discovery -**
The popularity of standard software packaging distribution formats and installers resulted in resources like [logfiles and administrative directories](http://www.owasp.org/index.php/Forced_browsing) frequently being located in a small number of [predictable locations](https://github.com/fuzzdb-project/fuzzdb/tree/master/discovery/predictable-filepaths).
FuzzDB contains a comprehensive dictionary, sorted by platform type, language, and application, making brute force testing less brutish.<br>
https://github.com/fuzzdb-project/fuzzdb/tree/master/discovery

**Response Analysis -**
Since interesting system responses often consist of [predictable strings](https://github.com/fuzzdb-project/fuzzdb/tree/master/regex), FuzzDB contains a set of regex pattern dictionaries that can be matched against server responses to help find software security defects and monitor server responses for regular expressions for regular expressions including credit cards, social security numbers, and more.<br>

**Other useful stuff -**
Webshells, common password and username lists, and some handy wordlists.

**Documentation -**
A collection of original [documentation and cheatsheets](https://github.com/fuzzdb-project/fuzzdb/tree/master/docs) and documentation collected from different sources. Additionally, many directories contain a README.md file with usage notes.<br>

# How-To #
https://github.com/fuzzdb-project/fuzzdb/wiki/usagehints

# Why FuzzDB exists #
FuzzDB's attack and discovery pattern dictionary allows security testers and researchers to repeatably exercise applications and uncover more vulnerabilities. 

To inform future testing, FuzzDB collects attack and discovery patterns that have caused software to malfunction in the past. While a small number of patterns could find many bugs, a more comprehensive set of variants allows for discovery of edge cases that bypass protection mechanisms, that result from interoperability issues, or are only discovered through knowlege of predictable resource names.  

Released under the dual New BSD and Creative Commons by Attribution licenses, FuzzDB can be used for any purpose by penetration testers and security researchers and leveraged to improve the test cases built into open source and commercial security testing software.

# How were the attack patterns collected? #
Lots of hours of research while performing penetration tests and research:
  * analysis of default app installs
  * analysis of system and application documentation
  * analysis of error messages
  * researching old web exploits for repeatable attack strings
  * scraping scanner payloads from  http logs
  * various books, articles, blog posts, mailing list threads
  * other open source fuzzers and pentest tools
and the input of contributors: https://github.com/fuzzdb-project/fuzzdb/graphs/contributors

# Download #
**Preferred method is to check out sources via git, new payloads are added frequently**

```
git clone https://github.com/fuzzdb-project/fuzzdb.git

```
While in the FuzzDB dir, you can update your local repo with the command
```
git pull
```
You can also browse the [FuzzDB github sources](https://github.com/fuzzdb-project/fuzzdb/) and there is always a [zip file](https://github.com/fuzzdb-project/fuzzdb/archive/master.zip)

# Who #
FuzzDB was created by Adam Muntner (amuntner @ gmail.com)
FuzzDB (c) Copyright Adam Muntner, 2010-2017
Portions copyrighted by others, as noted in commit comments and README.md files. 

The FuzzDB license is New BSD and Creative Commons by Attribution. The ultimate goal of this project is to make the patterns contained within obsolete. If you use this project in your work, research, or commercial product, you are required to cite it. That's it. I always enjoy hearing about how people are using it to find an interesting bug or in a tool, send me an email and let me know. 

Submissions are always welcome!

Official FuzzDB project page: [https://github.com/fuzzdb-project/fuzzdb/](https://github.com/fuzzdb-project/fuzzdb/)

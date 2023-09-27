
# Trabalho realizado nas Semanas #2 e #3

## Identification

- Three CVEs (CVE-2021-31207, CVE-2021-34523, and CVE-2021-34473) impact Microsoft Exchange Server, collectively posing a severe threat.
- These vulnerabilities enable an attacker to achieve Remote Code Execution (RCE) by circumventing authentication mechanisms.
- Affected Systems:
    - Microsoft Exchange Server 2013
    - Microsoft Exchange Server 2019 Cumulative Update 9
    - Microsoft Exchange Server 2016 Cumulative Update 20
    - Microsoft Exchange Server 2016 Cumulative Update 19
    - Microsoft Exchange Server 2019 Cumulative Update 8



## Cataloging

- These vulnerabilities were publicly reported in 2021. While there's no specific researcher identified, there are reports that Orange Tsai made discoveries related to these CVEs. They are categorized as critical due to their potential to compromise the security of Microsoft Exchange Server.
- CVSS Base Score: 9.8.
- CVSS Base Severity: Critical.
- item4

## Exploit

- Exploitation of these CVEs typically involves injecting malicious commands, allowing attackers to bypass authentication, impersonate users, and write arbitrary files. - 
- Given the gravity of these vulnerabilities, it is possible that automated exploitation tools exist.


## Ataques

- UNC2980, a threat group believed to operate from China, drew attention when it leveraged these vulnerabilities in a cyber-espionage operation targeting a U.S.-based university in August 2021. 
- This underscores the significant potential for these vulnerabilities to lead to successful attacks. If exploited, they can grant attackers full control over the vulnerable Microsoft Exchange Server, potentially causing extensive damage and unauthorized access to systems and data.

### Links
- https://www.cvedetails.com/cve/CVE-2021-34523/
- https://www.mandiant.com/resources/blog/pst-want-shell-proxyshell-exploiting-microsoft-exchange-servers
- https://www.fortiguard.com/threat-signal-report/4093/vulnerable-microsoft-exchange-servers-actively-scanned-for-proxyshell
- https://msrc.microsoft.com/update-guide/en-US/advisory/CVE-2021-34523

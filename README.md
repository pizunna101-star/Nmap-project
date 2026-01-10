# Nmap-project
This portfolio demonstrates my practical skills, analytical thinking, and communication ability as acybersecurity analyst. It is intentionally structured to serve two purposes.
 
* Recruiter‑facing portfolio: Clearly shows what I can do, how I think, and how I document security work.
* Beginner‑friendly guide: Helps new cybersecurity learners understand Nmap from the ground up without being overwhelmed.
The focus is not just on running commands, but on why they are used, what the results mean, and how they support security decisions.

### Tool Introduction: Nmap
Nmap (Network Mapper) is an open‑source tool used for: - Host discovery - Port scanning - Service and version detection - OS fingerprinting - Vulnerability discovery (via scripts)
It is commonly used by: - Security analysts - Penetration testers - Blue teams for network auditing


### Lab Environment
**Scanning Host**: Kali Linux
**Target Options**: - Metasploitable2 (local lab) - Windows/Linux VM - Authorized test network
All scans in this portfolio are conducted in a controlled and authorized environment. 

---

### Host Discovery

**Objective**
Identify live hosts on a network before deeper scanning. This reduces noise and improves efficiency.

**Command**
nmap-sn 192.168.56.0/24

**Explanation**
* -sn : Ping scan (no port scan)
* Discovers which IPs are alive

**Analyst Insight**
This step is critical in large networks to avoid scanning inactive systems and triggering unnecessary alerts.
<img width="568" height="227" alt="image" src="https://github.com/user-attachments/assets/7bfd22a0-b00d-4284-847c-69c568f29df4" />

---

### Phase 2: Basic Port Scanning
**Objective**
Identify open TCP ports on a target system.

**Command**
nmap 192.168.56.102

**Explanation**
* Default scan
* Scans the most common 1000 TCP ports

**Analyst Insight**
Open ports reveal potential attack surfaces. Even a single exposed service can become an entry point if
misconfigured.

<img width="529" height="398" alt="image" src="https://github.com/user-attachments/assets/55822b1b-175e-4fd5-bcd4-39457fdd34a0" />
---

### Phase 3: Full TCP Port Scan
**Objective**
Ensure no open ports are missed.

**Command**
nmap-p- 192.168.1.10

**Explanation**
* -p- : Scans all 65,535 TCP ports

**Analyst Insight**
Attackers often hide services on uncommon ports. A full scan removes blind spots during reconnaissance.

<img width="481" height="407" alt="image" src="https://github.com/user-attachments/assets/97a68f13-6d0c-4960-ab51-a9eeea1c094c" />
---

### Phase 4: Service and Version Detection
**Objective**
Identify what services are running and their versions.

**Command**
nmap-sV 192.168.56.102

**Explanation**
* -sV : Detects service versions

**Analyst Insight**
Knowing the exact version helps correlate services with known vulnerabilities (CVEs).

<img width="496" height="323" alt="image" src="https://github.com/user-attachments/assets/d3b4cd8c-7d4d-4ad0-b11d-bc69f4c28fa1" />

---

### Phase 5: OS Detection
**Objective**
Determine the operating system of the target.

**Command**
nmap-O 192.168.56.102

**Explanation**
* -O : OS fingerprinting

**Analyst Insight**
OS identification helps attackers and defenders tailor their strategies. Defenders use this to validate asset
inventories.

<img width="359" height="356" alt="image" src="https://github.com/user-attachments/assets/c21755d3-aaf4-431e-bc03-ef508e27a7b7" />

---

### Phase 6: Aggressive Scan (Combined Intelligence)
**Objective**
Gather maximum information in a single scan.

**Command**
nmap-h 192.168.56.102

**Explanation**
Includes: - OS detection - Version detection - Script scanning - Traceroute

**Analyst Insight**
While powerful, aggressive scans are noisy and should be used cautiously in production environments.

<img width="605" height="352" alt="image" src="https://github.com/user-attachments/assets/3f3a0a2b-0e84-463e-b3ab-98b82805e109" />
<img width="667" height="405" alt="image" src="https://github.com/user-attachments/assets/8e9c3a14-aa2f-4380-bd9e-aee2c06f84c0" />
<img width="661" height="380" alt="image" src="https://github.com/user-attachments/assets/2535479d-38d6-4b44-82a1-b73916ed1101" />
<img width="524" height="401" alt="image" src="https://github.com/user-attachments/assets/894c7ca4-46c2-46bc-9a72-66cfc4f0b4c8" />

---

### Phase 7: Nmap Scripting Engine (NSE)
**Objective**
Use scripts to detect vulnerabilities and misconfigurations.

**Command**
nmap--script=vuln 192.168.56.102

**Explanation** 
Runs vulnerability detection scripts

**Analyst Insight**
This bridges reconnaissance and vulnerability assessment, making Nmap more than just a scanner.

<img width="477" height="408" alt="image" src="https://github.com/user-attachments/assets/dd8e343b-451f-4bb2-877b-5a82e5cbf672" />
<img width="445" height="395" alt="image" src="https://github.com/user-attachments/assets/cff17876-43ee-4415-af52-daec29581b60" />
<img width="599" height="403" alt="image" src="https://github.com/user-attachments/assets/3a1527ab-587b-4f2a-8a76-bbc4b12a342b" />
<img width="592" height="405" alt="image" src="https://github.com/user-attachments/assets/2ebd1ff1-e9d2-4417-8891-9bb05086a21a" />

---

### Phase 8: Output Management
**Objective**
Save scan results for reporting and analysis.

**Commands**
nmap-oA initial_scan 192.168.56.102

**Creates** 
nmap (normal output) - 
xml (machine‑readable) - 

**Analyst Insight**
gnmap (grepable)
Proper documentation is essential for audits, reports, and collaboration.

<img width="434" height="338" alt="image" src="https://github.com/user-attachments/assets/ebcc8670-e5d6-4c16-a6c8-ae0fc5bbed47" />

---

**Common Beginner Mistakes**
 
* Scanning unauthorized systems
* Ignoring scan timing options
* Misinterpreting filtered ports
* Running aggressive scans blindly

---

**Key Skills Demonstrated**
* Network reconnaissance
* Attack surface analysis
* Tool proficiency (Nmap)
* Security documentation
* Technical communication
* These are core skills every cybersecurity professional must possess

### Conclusion

This Nmap portfolio demonstrates not only technical capability but also structured thinking and clarity in
communication. As complexity increases, future portfolio sections will expand into vulnerability exploitation,
detection engineering, and defensive monitoring.

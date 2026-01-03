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


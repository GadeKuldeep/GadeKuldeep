# KULDEEP GADE - Cybersecurity Operator Portfolio

**Status**: 🟢 Active | Open to SOC L1, VAPT, Threat Intelligence Roles  
**Location**: Pune, Maharashtra, India  
**Contact**: gadekuldeep25@gmail.com | +91 93093 81367  

---

## 🎯 Executive Summary

I'm a **final-year B.E. Computer Engineering (Cybersecurity) student** at JCOE Kuran, Pune with a **hands-on, lab-driven approach** to security operations, threat detection, and offensive security techniques.

My expertise spans:
- **SOC Operations**: Real-world SIEM monitoring (Wazuh), log analysis, incident investigation
- **Network Defense**: Snort IDS tuning, custom rule writing, traffic forensics
- **Offensive Security**: Web exploitation, reconnaissance, penetration testing
- **Threat Hunting**: Malware analysis, PCAP investigation, behavioral detection
- **Automation**: Python security tools, detection frameworks, custom integrations

**Philosophy**: *Understand the attack. Build the defense.*

---

## 📚 Education & Certifications

**Degree**: B.E. Computer Engineering (Cybersecurity Specialization)  
**University**: Savitribai Phule Pune University (SPPU)  
**Graduation**: July 2027 (Final Year - 2026-27)

### Certifications Earned
- ✅ **Cisco CyberOps Associate** - Network defense and SOC operations
- ✅ **Junior Cybersecurity Analyst** - Cisco Networking Academy
- ✅ **Introduction to Cybersecurity** - Cisco Networking Academy
- ✅ **NPTEL Computer Networks** - Advanced networking fundamentals
- ✅ **NPTEL Programming in Java** - Software development

---

## 🔧 Technical Skill Breakdown

### SIEM & Threat Detection
- **Wazuh**: Advanced architecture, custom rule writing, MITRE ATT&CK mapping, alert tuning
- **Snort IDS**: Complex rule syntax (PCRE, byte_test, stateful flow), threshold tuning, traffic analysis

### Network & Forensics
- **Wireshark**: Advanced packet inspection, malware PCAP analysis, TCP flow investigation
- **tcpdump**: Network traffic capture and filtering
- **Network Security**: DNS security, TLS/SSL analysis, port scanning, reconnaissance

### Penetration Testing & Exploitation
- **Burp Suite**: Web application security testing, automated scanning, manual exploitation
- **Metasploit**: Post-exploitation, payload generation, multi-stage attacks
- **Nmap**: Advanced scanning, service enumeration, OS fingerprinting
- **SQLmap**: SQL injection automation and database extraction
- **Nikto**: Web server vulnerability scanning

### Credential Testing & Simulation
- **Hydra**: Brute-force credential testing
- **John the Ripper**: Password cracking and hash analysis
- **GoPhish**: Phishing simulation and awareness testing

### Programming & Automation
- **Python**: Custom security tools, socket programming, threat detection automation
- **Bash**: System administration, log analysis, security scripting
- **JavaScript/Node.js**: Web security, security tools development
- **FastAPI**: REST API development for security platforms

### Operating Systems & Infrastructure
- **Linux/Ubuntu**: System hardening, log analysis, SIEM deployment
- **Kali Linux**: Penetration testing platform, tool mastery
- **Windows Security**: Event log analysis, PowerShell hardening, privilege escalation
- **VirtualBox/VMware**: Lab architecture, network segmentation

---

## 🚀 Core Projects (Production-Ready)

### 1. 🔴🔵 RED-BLUE-TEAM-LAB-SETUP
**GitHub**: https://github.com/GadeKuldeep/Red-Blue-Team-Lab-Setup

**Purpose**: Full-scale cybersecurity home lab simulating real SOC operations and attack scenarios.

**Architecture**:
- **Kali Linux VM (Red Team)**: Attacker machine with Metasploit, Nmap, SQLmap, Hydra, GoPhish
- **Ubuntu Server VM (Blue Team)**: SIEM + IDS monitoring with Wazuh Manager + Snort
- **Target Systems**: DVWA (web exploitation), vulnerable applications for testing
- **Threat Simulation**: GoPhish phishing engine integrated with Wazuh webhooks for alerting

**Key Achievements**:
- ✅ Wazuh-Snort integration with 10+ custom detection rules (IDs 80500-80511)
- ✅ Debugged multi-part integration failure (`-A console` vs `-A fast` flag conflict + file permissions)
- ✅ Custom Snort rule tuning with byte_test, PCRE regex, stateful flow analysis
- ✅ Structured incident response reports for every attack scenario
- ✅ MITRE ATT&CK technique mapping for all detection rules
- ✅ Real-time alert correlation and escalation workflows

**Technologies Used**:
- VirtualBox | Ubuntu | Kali Linux
- Wazuh Manager & Agent | Snort IDS
- GoPhish | DVWA
- Custom Bash automation scripts

**What I Learned**:
- Production-grade SIEM deployment and tuning
- Advanced IDS rule writing and optimization
- Integration challenges and debugging methodologies
- Incident response workflows and documentation
- Purple team operations (attack + defense balance)

---

### 2. 🌐 NETWORK-TRAFFIC-ANALYSIS-LAB
**GitHub**: https://github.com/GadeKuldeep/Network-Traffic-Analysis-Lab

**Purpose**: Deep network forensics and packet-level threat detection capability.

**Key Focus Areas**:
- **PCAP Analysis**: Malware traffic identification, command-and-control (C2) communication
- **TCP/IP Investigation**: Flow analysis, anomaly detection, protocol violations
- **Wireshark Mastery**: Custom filter creation, follow streams, dissector development
- **Network Troubleshooting**: Connectivity issues diagnosis, latency analysis
- **Forensic Timeline Reconstruction**: Building attack timelines from network data

**Practical Investigations**:
- ✅ Diagnosed Wazuh connectivity issues via packet capture (port 1514 unanswered SYN packets)
- ✅ Analyzed multi-stage attack chains using PCAP evidence
- ✅ Built Wireshark filter sets for common attack patterns (SQL injection, XSS, etc.)
- ✅ Documented forensic methodology and evidence collection procedures
- ✅ Created reusable packet analysis playbooks

**Technologies Used**:
- Wireshark | tcpdump
- Network packet analysis tools
- Protocol inspection (TCP, UDP, DNS, HTTP, HTTPS)
- Evidence documentation systems

**What I Learned**:
- Network protocol stack understanding
- Malware behavior patterns in network traffic
- Forensic evidence collection and preservation
- Network troubleshooting methodologies
- Real-world packet investigation scenarios

---

### 3. 🚩 PICO-CTF-WRITEUPS
**GitHub**: https://github.com/GadeKuldeep/PicoCTF

**Purpose**: Documented solutions to Capture The Flag security challenges with methodology.

**Challenge Categories Mastered**:
- **Cryptography**: Hash functions, symmetric/asymmetric encryption, key exchange protocols
- **Web Exploitation**: SQL injection, XSS (reflected/stored/DOM), IDOR, insecure deserialization, SSTI
- **Reverse Engineering**: Binary analysis, disassembly, obfuscation techniques, code flow analysis
- **Binary Exploitation**: Buffer overflows, ROP chains, ASLR bypasses, heap exploitation
- **Forensics**: Memory analysis, log file investigation, data carving, image analysis
- **General Skills**: Linux fundamentals, command-line operations, tool proficiency

**Documentation Approach**:
- ✅ Step-by-step challenge walkthroughs with explanations
- ✅ Tool usage examples (GDB, IDA Pro, Burp Suite, strings, objdump, etc.)
- ✅ Vulnerability explanation with real-world impact assessment
- ✅ Beginner-friendly reference material for learning
- ✅ Common pitfalls and troubleshooting tips

**What I Learned**:
- Structured problem-solving methodology
- Tool proficiency in offensive security
- Security vulnerability exploitation techniques
- Defensive mindset from attacker perspective
- Documentation and knowledge sharing skills

---

### 4. ⚙️ PYTHON-SECURITY-TOOLS
**GitHub**: https://github.com/GadeKuldeep

**Purpose**: Custom automation frameworks for security operations and threat detection.

**Key Tools Built**:
- **Log Analysis Framework**: Automated parsing and correlation of security logs
- **Threat Detection Automation**: Rule-based detection with custom scoring algorithms
- **Network Scanning Utilities**: Nmap-based reconnaissance automation
- **Credential Testing Tools**: Hydra integration for security assessment
- **SIEM Integration Scripts**: Custom connectors for data enrichment and alerting

**Capabilities**:
- ✅ Real-time log processing and analysis
- ✅ Multi-source data correlation
- ✅ Custom alert generation and escalation
- ✅ Automated report generation
- ✅ Integration with external security tools

**Technologies Used**:
- Python 3.8+ | FastAPI | Flask
- Socket programming | imaplib (email forensics)
- Data structures for threat modeling
- Automation frameworks and scheduling

**What I Learned**:
- Security tool development best practices
- API integration and data enrichment
- Automation workflow design
- Performance optimization for security tools
- Scalability considerations for production systems

---

## 💼 Professional Experience

### Data Analyst Internship
**Company**: Technogrowth Software Solutions Pvt. Ltd.  
**Duration**: December 2025 - February 2026  
**Location**: Pune, India

**Responsibilities**:
- Data cleaning and preprocessing for analytics pipelines
- Report generation and visualization
- Business metrics analysis and interpretation
- Database query optimization

---

## 🏆 Platform Engagement & Achievements

### TryHackMe
- **Rank**: 140,004 globally (**Top 6%** in competitive rankings)
- **Status**: Platinum League participant
- **Achievements**: 
  - Completed 50+ hands-on security labs
  - Hacker's Holiday event completion
  - Room mastery in Windows security, forensics, SIEM tools
  - Consistent learning and progression

**Profile**: https://tryhackme.com/p/gadekuldeep25

### GitHub Portfolio
- **Active Development**: Regular commits to cybersecurity projects
- **Portfolio Projects**: 10+ repositories with detailed documentation
- **Community Contribution**: Open-source security tools
- **Code Quality**: Well-documented, production-ready code

**Profile**: https://github.com/GadeKuldeep

### LinkedIn Professional Network
- **Network**: Active engagement with cybersecurity professionals
- **Content**: Lab achievements, security insights, threat hunting methodology
- **Endorsements**: Wazuh, Snort, Network Security, Python, Cybersecurity
- **Recommendations**: From instructors and security professionals

**Profile**: https://linkedin.com/in/kuldeep-gade-52598b2b0

---

## 📋 Advanced Study Areas

### SIEM & Threat Detection Mastery
- ✅ **NIST Cybersecurity Framework (CSF)** - All 5 functions (Identify, Protect, Detect, Respond, Recover)
- ✅ **Wazuh Architecture**: Agents, managers, API, integrations
- ✅ **Custom Detection Rules**: Writing complex correlation rules
- ✅ **MITRE ATT&CK Framework**: Technique mapping for detections
- ✅ **Alert Tuning**: False positive reduction, severity calibration
- ✅ **Log Collection**: Centralization, parsing, indexing strategies

### Snort IDS Advanced Topics
- ✅ **Rule Syntax Mastery**: From basics to advanced (PCRE, byte_test, stateful)
- ✅ **Threshold Tuning**: Alert generation optimization
- ✅ **Traffic Analysis**: Pattern recognition and anomaly detection
- ✅ **Pre-processor Configuration**: Advanced traffic monitoring
- ✅ **Custom Signatures**: Writing signatures for new threat patterns

### Web Application Security (OWASP)
- ✅ **SQL Injection**: Detection, exploitation, mitigation
- ✅ **Cross-Site Scripting (XSS)**: Reflected, stored, DOM-based
- ✅ **Insecure Direct Object References (IDOR)**: Authorization flaws
- ✅ **Security Misconfiguration**: Server and application hardening
- ✅ **Weak Authentication**: Password policies, session management
- ✅ **Server-Side Template Injection (SSTI)**: Jinja2, Mako, ERB exploitation
- ✅ **Juice Shop Assessment**: Complete penetration testing walkthrough

### Windows Security Deep Dive
- ✅ **Event Log Analysis**: Event IDs 4624, 4625, 4688, 4672, 7045, 4698
- ✅ **PowerShell Logging**: Script block logging, execution policy hardening
- ✅ **Registry Analysis**: Persistence mechanisms, configuration analysis
- ✅ **Privilege Escalation**: Common vectors and exploitation techniques
- ✅ **Group Policy**: Security baseline implementation

### Network & Forensics Expertise
- ✅ **Wireshark Advanced Filtering**: Complex filter syntax, stream following
- ✅ **TCP/IP Protocol Analysis**: Deep protocol understanding
- ✅ **Malware Traffic Identification**: Signature-based and behavioral detection
- ✅ **Network Timeline Reconstruction**: Building attack narratives from evidence
- ✅ **Incident Forensics**: Disk, memory, and network artifact analysis

---

## 🎯 Job Search & Career Strategy

### Target Roles
1. **SOC L1 Analyst**
   - Log monitoring and real-time alerting
   - Incident triage and initial investigation
   - Alert tuning and false positive reduction
   - Escalation to senior analysts

2. **VAPT (Penetration Tester)**
   - Web and network security assessment
   - Vulnerability identification and exploitation
   - Risk prioritization and remediation recommendations
   - Report generation for non-technical stakeholders

3. **Threat Intelligence Analyst**
   - Malware analysis and reverse engineering
   - Threat research and TTP investigation
   - Intelligence report creation
   - Indicator of Compromise (IOC) development

### Target Companies
- **Applied For**: Neumetric, Bureau Veritas, Veradigm, CyberXchange, Quick Heal
- **Cold Outreach**: Deloitte, Capgemini, IBM, Accenture, TCS, Infosys, Wipro
- **Platforms**: Internshala, LinkedIn, Naukri.com

### Application Strategy
- ✅ 20+ tailored resumes for different roles (SOC L1 vs VAPT vs Threat Intel)
- ✅ Role-specific cover letters highlighting relevant projects
- ✅ Portfolio-driven applications linking GitHub projects
- ✅ Cold outreach emails to security teams at major firms
- ✅ LinkedIn connection strategy with hiring managers

---

## 📊 Key Metrics & Statistics

| Metric | Value |
|--------|-------|
| **Active Projects** | 10+ repositories on GitHub |
| **Lab VMs** | 3-tier architecture (Attacker, Defender, Target) |
| **Custom Detection Rules** | 15+ (Wazuh + Snort combined) |
| **CTF Challenges Solved** | 50+ across multiple platforms |
| **TryHackMe Rank** | Top 6% globally (140,004) |
| **Years Cybersecurity Focus** | 2+ years continuous, self-directed learning |
| **Certifications** | 5 (Cisco + NPTEL) |
| **Programming Languages** | 4+ (Python, JavaScript, Bash, Java) |

---

## 🔗 Quick Links

| Platform | URL |
|----------|-----|
| **GitHub** | https://github.com/GadeKuldeep |
| **LinkedIn** | https://linkedin.com/in/kuldeep-gade-52598b2b0 |
| **TryHackMe** | https://tryhackme.com/p/gadekuldeep25 |
| **Email** | gadekuldeep25@gmail.com |
| **Phone** | +91 93093 81367 |
| **Portfolio (Live)** | See `index.html` file |

---

## 🚀 Next Goals & Milestones

### Short-term (Next 3 Months)
- ✅ Secure cybersecurity internship or entry-level role (SOC L1/VAPT)
- ✅ Deploy interactive portfolio website (GitHub Pages)
- ✅ Complete CompTIA A+ certification
- ✅ Begin Security+ exam preparation

### Medium-term (6-12 Months)
- SOC L1 → Detection Engineer career progression
- Advanced threat hunting certifications
- Security+ certification completion
- Active bug bounty program participation

### Long-term (1-2 Years)
- Purple Team Analyst specialization
- Advanced incident response expertise
- Security architecture understanding
- Leadership in security operations team

---

## 💡 Core Philosophy

> "Understand the attack. Build the defense."

My approach to cybersecurity is built on five core principles:

1. **Hands-On Practice**: Theory without lab work is incomplete. I build what I learn.
2. **Structured Documentation**: Every discovery, challenge, and solution is recorded for future reference.
3. **Continuous Evolution**: Security changes daily. I adapt, investigate, and stay current.
4. **Purple Team Mindset**: To defend effectively, I must understand attacks deeply.
5. **Knowledge Sharing**: The security community grows through shared learning and open-source contributions.

---

## 📝 Professional Summary

I bring **2+ years of focused, self-directed cybersecurity study** with emphasis on **practical lab work** and **real-world application**. My projects demonstrate:

- **Technical Depth**: Advanced SIEM/IDS configuration, custom detection rules, network forensics
- **Problem-Solving**: Debugging complex integrations, analyzing attack chains, optimizing alerts
- **Communication**: Clear documentation, structured incident reports, professional presentation
- **Continuous Learning**: Regular skill updates, certification pursuit, active community participation

I'm seeking a role where I can apply this knowledge **immediately** in a **dynamic security operations** environment.

---

## 📄 How to Use This Portfolio

### For Job Applications
1. **Reference in Cover Letter**: "My cybersecurity lab and projects are documented at [GitHub link]"
2. **Share Portfolio Link**: Include the `index.html` portfolio URL in your application
3. **Highlight Specific Projects**: Reference Red-Blue-Team-Lab for SOC roles, PicoCTF for VAPT roles
4. **Show Real Work**: Use project descriptions to answer behavioral interview questions

### For Interview Preparation
1. **Project Deep-Dives**: Be ready to explain architecture, challenges, and solutions
2. **Tool Mastery**: Demonstrate hands-on experience with Wazuh, Snort, Wireshark, Python
3. **Attack Scenarios**: Walk through a real attack scenario from your lab
4. **Decision-Making**: Explain your choices in tool selection, architecture, and detection rules

### For Continuous Learning
1. **Use as Reference**: Your projects are living documentation of what you've learned
2. **Build Upon**: Extend projects with new technologies and methodologies
3. **Share Knowledge**: Document and share your learning journey with the community

---

**Portfolio Created**: August 21, 2026  
**Status**: 🟢 Ready for Job Applications  
**Target Start Date**: Immediate (Internship or Full-Time Role)

---

*"The best way to predict the future is to build it."*

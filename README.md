<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background: #0a0e27;
    color: #00ff88;
    font-family: 'Courier New', monospace;
    line-height: 1.6;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 40px 20px;
}

/* GLITCH EFFECT */
.glitch {
    font-size: 4rem;
    font-weight: 900;
    letter-spacing: 8px;
    color: #00ff88;
    text-shadow: 
        -2px -2px 0 #ff006e,
        2px 2px 0 #00d4ff,
        0 0 30px #00ff88;
    position: relative;
    display: inline-block;
    animation: glitch 0.3s infinite;
}

.glitch::before {
    content: attr(data-text);
    position: absolute;
    left: -2px;
    top: -2px;
    color: #ff006e;
    z-index: -1;
    opacity: 0.8;
    animation: glitch-before 0.3s infinite;
    clip-path: polygon(0 0, 100% 0, 100% 45%, 0 58%);
}

.glitch::after {
    content: attr(data-text);
    position: absolute;
    left: 2px;
    top: 2px;
    color: #00d4ff;
    z-index: -1;
    opacity: 0.8;
    animation: glitch-after 0.3s infinite;
    clip-path: polygon(0 58%, 100% 45%, 100% 100%, 0 100%);
}

@keyframes glitch {
    0% { text-shadow: -2px -2px 0 #ff006e, 2px 2px 0 #00d4ff, 0 0 30px #00ff88; }
    50% { text-shadow: -3px -3px 0 #ff006e, 3px 3px 0 #00d4ff, 0 0 40px #00ff88; }
    100% { text-shadow: -2px -2px 0 #ff006e, 2px 2px 0 #00d4ff, 0 0 30px #00ff88; }
}

@keyframes glitch-before {
    0% { clip-path: polygon(0 0, 100% 0, 100% 45%, 0 58%); }
    20% { clip-path: polygon(0 10%, 100% 0, 100% 35%, 0 68%); }
    40% { clip-path: polygon(0 5%, 100% 10%, 100% 50%, 0 48%); }
    60% { clip-path: polygon(0 0, 100% 5%, 100% 40%, 0 65%); }
    100% { clip-path: polygon(0 0, 100% 0, 100% 45%, 0 58%); }
}

@keyframes glitch-after {
    0% { clip-path: polygon(0 58%, 100% 45%, 100% 100%, 0 100%); }
    20% { clip-path: polygon(0 68%, 100% 35%, 100% 90%, 0 100%); }
    40% { clip-path: polygon(0 48%, 100% 50%, 100% 95%, 0 50%); }
    60% { clip-path: polygon(0 65%, 100% 40%, 100% 100%, 0 55%); }
    100% { clip-path: polygon(0 58%, 100% 45%, 100% 100%, 0 100%); }
}

.header {
    text-align: center;
    margin-bottom: 60px;
    animation: slideDown 1s ease-out;
}

@keyframes slideDown {
    from { opacity: 0; transform: translateY(-30px); }
    to { opacity: 1; transform: translateY(0); }
}

.subtitle {
    font-size: 1.5rem;
    color: #00d4ff;
    margin-top: 20px;
    letter-spacing: 3px;
    text-shadow: 0 0 15px #00d4ff;
}

.status-line {
    margin-top: 20px;
    font-size: 14px;
    letter-spacing: 2px;
    color: #ff006e;
}

.status-dot {
    display: inline-block;
    width: 10px;
    height: 10px;
    background: #00ff88;
    border-radius: 50%;
    margin: 0 10px;
    animation: pulse 2s infinite;
    box-shadow: 0 0 15px #00ff88;
    vertical-align: middle;
}

@keyframes pulse {
    0%, 100% { 
        opacity: 1;
        box-shadow: 0 0 15px #00ff88;
    }
    50% { 
        opacity: 0.5;
        box-shadow: 0 0 30px #00ff88;
    }
}

.grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
    margin: 40px 0;
}

.card {
    background: rgba(10, 14, 39, 0.9);
    border: 2px solid #00ff88;
    padding: 25px;
    backdrop-filter: blur(10px);
    position: relative;
    overflow: hidden;
    transition: all 0.4s ease;
    box-shadow: 0 0 20px rgba(0, 255, 136, 0.3);
    animation: cardFadeIn 0.8s ease-out;
}

@keyframes cardFadeIn {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
}

.card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(90deg, transparent, rgba(0, 255, 136, 0.2), transparent);
    animation: scan 3s linear infinite;
}

@keyframes scan {
    0% { transform: translateY(-100%); }
    100% { transform: translateY(100%); }
}

.card:hover {
    border-color: #ff006e;
    transform: translateY(-10px);
    box-shadow: 
        0 15px 40px rgba(255, 0, 110, 0.5),
        0 0 30px #ff006e;
}

.card-title {
    font-size: 1.4rem;
    color: #00d4ff;
    margin-bottom: 15px;
    text-transform: uppercase;
    letter-spacing: 2px;
    text-shadow: 0 0 10px #00d4ff;
    border-bottom: 1px solid #00ff88;
    padding-bottom: 10px;
    position: relative;
    z-index: 2;
}

.card-content {
    position: relative;
    z-index: 2;
    font-size: 0.95rem;
    color: #a0ff88;
    line-height: 1.8;
}

.skill-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 15px;
}

.skill-tag {
    background: rgba(0, 255, 136, 0.15);
    border: 1px solid #00ff88;
    color: #00ff88;
    padding: 6px 12px;
    font-size: 0.8rem;
    letter-spacing: 1px;
    text-transform: uppercase;
    cursor: pointer;
    transition: all 0.3s ease;
    position: relative;
    z-index: 3;
}

.skill-tag:hover {
    border-color: #ff006e;
    color: #ff006e;
    box-shadow: 0 0 15px #00ff88;
    transform: scale(1.1);
}

.section-title {
    font-size: 2rem;
    color: #00ff88;
    text-shadow: 0 0 20px #00ff88;
    margin: 60px 0 40px 0;
    letter-spacing: 3px;
    text-transform: uppercase;
    border-left: 4px solid #ff006e;
    padding-left: 20px;
    position: relative;
}

.section-title::after {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 0;
    width: 80px;
    height: 2px;
    background: linear-gradient(90deg, #ff006e, transparent);
}

.project-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 25px;
    margin: 30px 0;
}

.project-card {
    background: rgba(15, 30, 60, 0.95);
    border: 2px solid #00d4ff;
    padding: 25px;
    cursor: pointer;
    transition: all 0.5s ease;
    overflow: hidden;
    position: relative;
}

.project-card:hover {
    border-color: #ff006e;
    transform: translateY(-15px);
    box-shadow: 
        0 30px 60px rgba(255, 0, 110, 0.4),
        0 0 40px rgba(0, 212, 255, 0.3);
}

.project-icon {
    font-size: 2.5rem;
    margin-bottom: 12px;
    filter: drop-shadow(0 0 10px #00d4ff);
    animation: float 3s ease-in-out infinite;
}

@keyframes float {
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(-10px); }
}

.project-title {
    font-size: 1.1rem;
    font-weight: bold;
    color: #ff006e;
    margin-bottom: 8px;
    letter-spacing: 1px;
    text-transform: uppercase;
    text-shadow: 0 0 10px #ff006e;
    position: relative;
    z-index: 2;
}

.project-desc {
    font-size: 0.9rem;
    color: #a0ff88;
    margin-bottom: 12px;
    position: relative;
    z-index: 2;
}

.tech-badge {
    display: inline-block;
    font-size: 0.75rem;
    background: rgba(255, 0, 110, 0.15);
    border: 1px solid #ff006e;
    color: #ff006e;
    padding: 3px 8px;
    margin: 4px 4px 4px 0;
    transition: all 0.3s ease;
    position: relative;
    z-index: 2;
}

.tech-badge:hover {
    background: rgba(255, 0, 110, 0.3);
    box-shadow: 0 0 10px #ff006e;
}

.divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, #00ff88, transparent);
    margin: 40px 0;
}

.footer {
    text-align: center;
    margin-top: 60px;
    padding-top: 30px;
    border-top: 2px solid rgba(0, 255, 136, 0.3);
}

.contact-links {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
    margin: 20px 0;
}

.contact-link {
    color: #00ff88;
    text-decoration: none;
    font-size: 0.95rem;
    letter-spacing: 1px;
    transition: all 0.3s ease;
    border: 1px solid rgba(0, 255, 136, 0.5);
    padding: 8px 16px;
}

.contact-link:hover {
    color: #ff006e;
    border-color: #ff006e;
    text-shadow: 0 0 10px #ff006e;
}

.footer-info {
    font-size: 0.9rem;
    color: #a0ff88;
    margin-top: 20px;
}

.footer-info strong {
    color: #00d4ff;
}

.scanner-line {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 2px;
    background: linear-gradient(90deg, transparent, #00ff88, #ff006e, transparent);
    animation: scan-full 4s linear infinite;
    box-shadow: 0 0 20px #00ff88;
    pointer-events: none;
    z-index: 100;
}

@keyframes scan-full {
    0% { transform: translateY(-100vh); }
    100% { transform: translateY(100vh); }
}

h1, h2, h3, h4, h5, h6 {
    color: #00ff88;
    text-shadow: 0 0 10px #00ff88;
    letter-spacing: 1px;
    margin-top: 30px;
    margin-bottom: 15px;
}

ul, ol {
    margin-left: 20px;
    color: #a0ff88;
}

li {
    margin: 8px 0;
    color: #a0ff88;
}

strong {
    color: #00ff88;
}

em {
    color: #00d4ff;
}

table {
    width: 100%;
    border-collapse: collapse;
    margin: 20px 0;
    border: 1px solid #00ff88;
}

th, td {
    border: 1px solid #00ff88;
    padding: 12px;
    text-align: left;
    color: #a0ff88;
}

th {
    background: rgba(0, 255, 136, 0.1);
    color: #00d4ff;
}

tr:hover {
    background: rgba(0, 255, 136, 0.05);
}

code {
    background: rgba(0, 255, 136, 0.1);
    color: #ff006e;
    padding: 2px 6px;
    border-radius: 3px;
    font-size: 0.9rem;
}

pre {
    background: rgba(0, 0, 0, 0.5);
    border: 1px solid #00ff88;
    padding: 15px;
    border-radius: 4px;
    overflow-x: auto;
    margin: 15px 0;
}

pre code {
    background: none;
    color: #00ff88;
    padding: 0;
}

blockquote {
    border-left: 4px solid #ff006e;
    padding-left: 15px;
    color: #00d4ff;
    font-style: italic;
    margin: 20px 0;
}

a {
    color: #00d4ff;
    text-decoration: none;
    transition: all 0.3s ease;
}

a:hover {
    color: #ff006e;
    text-shadow: 0 0 10px #ff006e;
}

@media (max-width: 768px) {
    .glitch {
        font-size: 2rem;
        letter-spacing: 2px;
    }
    
    .grid {
        grid-template-columns: 1fr;
    }
    
    .project-grid {
        grid-template-columns: 1fr;
    }
    
    .contact-links {
        gap: 10px;
    }
}
</style>
</head>
<body>

<div class="scanner-line"></div>

<div class="container">

<div class="header">
    <h1 class="glitch" data-text="KULDEEP GADE">KULDEEP GADE</h1>
    <div class="subtitle">[ CYBER SECURITY OPERATOR ]</div>
    <div class="status-line">
        <span class="status-dot"></span>
        SOC ANALYST | VAPT SPECIALIST | THREAT HUNTER
        <span class="status-dot"></span>
    </div>
</div>

---

## 🎯 Executive Summary

I'm a **final-year B.E. Computer Engineering (Cybersecurity) student** at JCOE Kuran, Pune with a hands-on, lab-driven approach to security operations, threat detection, and offensive security techniques.

### My Expertise Spans:

- **SOC Operations**: Real-world SIEM monitoring (Wazuh), log analysis, incident investigation
- **Network Defense**: Snort IDS tuning, custom rule writing, traffic forensics
- **Offensive Security**: Web exploitation, reconnaissance, penetration testing
- **Threat Hunting**: Malware analysis, PCAP investigation, behavioral detection
- **Automation**: Python security tools, detection frameworks, custom integrations

> **Philosophy**: *Understand the attack. Build the defense.*

<div class="divider"></div>

## 📚 Education & Certifications

<div class="grid">
    <div class="card">
        <div class="card-title">→ Degree</div>
        <div class="card-content">
            <strong>B.E. Computer Engineering</strong><br>
            Specialization: Cybersecurity<br>
            <strong>University:</strong> Savitribai Phule Pune University (SPPU)<br>
            <strong>Graduation:</strong> July 2027 (Final Year)
        </div>
    </div>
    
    <div class="card">
        <div class="card-title">→ Certifications</div>
        <div class="card-content">
            ✅ Cisco CyberOps Associate<br>
            ✅ Junior Cybersecurity Analyst<br>
            ✅ Introduction to Cybersecurity<br>
            ✅ NPTEL Computer Networks<br>
            ✅ NPTEL Programming in Java
        </div>
    </div>
</div>

<div class="divider"></div>

## 🔧 Technical Skills

<div class="grid">
    <div class="card">
        <div class="card-title">→ SIEM & Detection</div>
        <div class="card-content">
            <strong>Wazuh:</strong> Custom rules, MITRE mapping, alert tuning<br>
            <strong>Snort IDS:</strong> Rule syntax, PCRE, stateful analysis<br>
            <strong>Log Analysis:</strong> Correlation, anomaly detection<br>
        </div>
        <div class="skill-tags">
            <span class="skill-tag">Wazuh</span>
            <span class="skill-tag">Snort</span>
            <span class="skill-tag">Log Analysis</span>
            <span class="skill-tag">Detection</span>
        </div>
    </div>
    
    <div class="card">
        <div class="card-title">→ Network & Forensics</div>
        <div class="card-content">
            <strong>Wireshark:</strong> Packet analysis, malware PCAP<br>
            <strong>tcpdump:</strong> Network capture and filtering<br>
            <strong>Forensics:</strong> Evidence analysis, investigation<br>
        </div>
        <div class="skill-tags">
            <span class="skill-tag">Wireshark</span>
            <span class="skill-tag">tcpdump</span>
            <span class="skill-tag">Forensics</span>
            <span class="skill-tag">Protocols</span>
        </div>
    </div>
    
    <div class="card">
        <div class="card-title">→ Penetration Testing</div>
        <div class="card-content">
            <strong>Burp Suite:</strong> Web app security testing<br>
            <strong>Metasploit:</strong> Exploitation framework<br>
            <strong>Nmap:</strong> Network scanning<br>
        </div>
        <div class="skill-tags">
            <span class="skill-tag">Burp Suite</span>
            <span class="skill-tag">Metasploit</span>
            <span class="skill-tag">Nmap</span>
            <span class="skill-tag">VAPT</span>
        </div>
    </div>
    
    <div class="card">
        <div class="card-title">→ Programming</div>
        <div class="card-content">
            <strong>Python:</strong> Security automation tools<br>
            <strong>Bash:</strong> System scripting<br>
            <strong>JavaScript:</strong> Web security<br>
        </div>
        <div class="skill-tags">
            <span class="skill-tag">Python</span>
            <span class="skill-tag">Bash</span>
            <span class="skill-tag">JavaScript</span>
            <span class="skill-tag">FastAPI</span>
        </div>
    </div>
</div>

<div class="divider"></div>

<h2 class="section-title">>> ACTIVE PROJECTS</h2>

<div class="project-grid">
    <div class="project-card">
        <div class="project-icon">🔴🔵</div>
        <div class="project-title">RED-BLUE-TEAM-LAB</div>
        <div class="project-desc">
            Production-grade home lab: Wazuh SIEM + Snort IDS + DVWA + GoPhish. 10+ custom detection rules with MITRE ATT&CK mapping.
        </div>
        <div>
            <span class="tech-badge">VirtualBox</span>
            <span class="tech-badge">Ubuntu</span>
            <span class="tech-badge">Kali</span>
            <span class="tech-badge">Wazuh</span>
            <span class="tech-badge">Snort</span>
        </div>
    </div>

    <div class="project-card">
        <div class="project-icon">🌐</div>
        <div class="project-title">NETWORK-TRAFFIC-ANALYSIS</div>
        <div class="project-desc">
            Deep packet forensics: PCAP analysis, malware traffic ID, TCP/IP investigation, Wazuh debugging.
        </div>
        <div>
            <span class="tech-badge">Wireshark</span>
            <span class="tech-badge">tcpdump</span>
            <span class="tech-badge">Forensics</span>
            <span class="tech-badge">Analysis</span>
        </div>
    </div>

    <div class="project-card">
        <div class="project-icon">🚩</div>
        <div class="project-title">PICO-CTF-WRITEUPS</div>
        <div class="project-desc">
            Complete challenge solutions: Cryptography, Web, Reverse Engineering, Binary, Forensics.
        </div>
        <div>
            <span class="tech-badge">CTF</span>
            <span class="tech-badge">Security</span>
            <span class="tech-badge">Documentation</span>
            <span class="tech-badge">Solutions</span>
        </div>
    </div>

    <div class="project-card">
        <div class="project-icon">⚙️</div>
        <div class="project-title">PYTHON-SECURITY-TOOLS</div>
        <div class="project-desc">
            Custom automation: Log analysis, threat detection, network scanning, credential testing, SIEM integration.
        </div>
        <div>
            <span class="tech-badge">Python</span>
            <span class="tech-badge">FastAPI</span>
            <span class="tech-badge">Automation</span>
        </div>
    </div>
</div>

<div class="divider"></div>

## 💼 Professional Experience

**Data Analyst Internship**  
**Technogrowth Software Solutions Pvt. Ltd.** | Pune, India  
*December 2025 - February 2026*

- Data cleaning and preprocessing for analytics pipelines
- Report generation and visualization
- Business metrics analysis

<div class="divider"></div>

## 🏆 Platform Achievements

| Platform | Achievement |
|----------|-------------|
| **TryHackMe** | Rank 140,004 globally (Top 6%) · 50+ labs completed · Platinum League |
| **GitHub** | 10+ repositories · Production-ready code · Active contributions |
| **LinkedIn** | Cybersecurity network · Security insights · Professional endorsements |

<div class="divider"></div>

## 📊 Quick Stats

| Metric | Value |
|--------|-------|
| Active Projects | 10+ repositories |
| Lab VMs | 3-tier architecture |
| Custom Detection Rules | 15+ (Wazuh + Snort) |
| CTF Challenges Solved | 50+ |
| TryHackMe Rank | Top 6% globally |
| Years Cybersecurity Focus | 2+ continuous |
| Certifications | 5 (Cisco + NPTEL) |

<div class="divider"></div>

## 🎯 Job Search Focus

### Target Roles
- **SOC L1 Analyst**: Log monitoring, incident triage, alert tuning
- **VAPT Specialist**: Web/network testing, vulnerability assessment
- **Threat Intelligence Analyst**: Malware analysis, TTP investigation

### Target Companies
Neumetric, Bureau Veritas, Deloitte, Capgemini, IBM, Accenture, TCS, Quick Heal

<div class="divider"></div>

## 🔗 Connect With Me

<div class="footer">
    <div class="contact-links">
        <a href="https://github.com/GadeKuldeep" class="contact-link" target="_blank">GitHub</a>
        <a href="https://linkedin.com/in/kuldeep-gade-52598b2b0" class="contact-link" target="_blank">LinkedIn</a>
        <a href="https://tryhackme.com/p/gadekuldeep25" class="contact-link" target="_blank">TryHackMe</a>
        <a href="mailto:gadekuldeep25@gmail.com" class="contact-link">Email</a>
    </div>
    
    <div class="footer-info">
        <strong>📧 gadekuldeep25@gmail.com</strong><br>
        <strong>📱 +91 93093 81367</strong><br>
        <strong>📍 Pune, Maharashtra, India</strong><br>
        <strong style="color: #00ff88;">🟢 ACTIVE | OPEN TO OPPORTUNITIES</strong>
    </div>
</div>

---

</div>

<script>
    // Glitch text setup
    document.querySelectorAll('.glitch').forEach(el => {
        el.setAttribute('data-text', el.textContent);
    });
    
    // Scroll reveal animation
    const observerOptions = {
        threshold: 0.1,
        rootMargin: '0px 0px -100px 0px'
    };
    
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.style.opacity = '1';
                entry.target.style.transform = 'translateY(0)';
            }
        });
    }, observerOptions);
    
    document.querySelectorAll('.card, .project-card').forEach(el => {
        el.style.opacity = '0';
        el.style.transform = 'translateY(20px)';
        observer.observe(el);
    });
</script>

</body>
</html>

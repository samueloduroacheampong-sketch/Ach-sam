# Ach-sam
Incident Response/ Unauthorized SSH access 
# Incident Response Simulation: Unauthorized SSH Access Attempt

## Overview
This project demonstrates a simulated **incident response (IR) exercise** in a controlled lab environment. The goal was to **detect, analyze, contain, and report** a simulated unauthorized SSH access attempt on a Linux server.  

This project highlights skills relevant for an **Incident Responder / SOC Analyst** role.

---

## Objectives
- Apply the NIST Incident Response Lifecycle: Preparation → Detection & Analysis → Containment → Eradication & Recovery → Lessons Learned.
- Produce a professional incident report documenting findings, remediation, and recommendations.
- Develop detection rules for suspicious login activity.

---

## Tools & Technologies
- **SIEM / Log Analysis:** ELK Stack (Elasticsearch, Logstash, Kibana)  
- **Endpoint Monitoring:** Auditd (Linux), Sysmon (Windows)  
- **Forensics & Analysis:** Wireshark, Volatility, grep  
- **Scripting / Automation:** Python for log parsing and alert enrichment  

---

## Methodology
1. **Preparation:**  
   - Setup a lab with a Linux server and monitoring workstation.  
   - Configured logs for ingestion into SIEM.  

2. **Detection & Analysis:**  
   - Detected multiple failed SSH login attempts followed by a successful login from an unusual IP.  
   - Correlated logs and network captures to confirm the suspicious activity.  

3. **Containment:**  
   - Isolated affected VM.  
   - Disabled compromised credentials.  
   - Blocked malicious IP via firewall rules.  

4. **Eradication & Recovery:**  
   - Wiped and restored server from a clean snapshot.  
   - Applied security updates and SSH hardening (key-based login, disable root login).  

5. **Lessons Learned:**  
   - Developed a detection rule for brute-force + successful login scenarios.  
   - Created an IR playbook for faster future triage.  

---

## Key Deliverables
- **Incident Report (PDF):** Incident Report Draft Cybersecurity.docx   
- **SIEM Detection Rule:** `detection-rules/ssh_bruteforce_success.yml`  
- **Log Samples:** Sanitized SSH log snippets (`logs/`)  
- **Screenshots:** Dashboards and alert views (`screenshots/`)  

---

## Outcomes
- Successfully detected and contained the simulated intrusion.  
- Produced a professional incident report suitable for SOC review.  
- Improved readiness by implementing detection rules and playbooks.  

---

## Ethical Disclaimer
This project was conducted entirely in a **controlled lab environment** for educational purposes. No unauthorized systems or sensitive data were accessed.

---

## How to Reproduce
1. Clone the repository:  
```bash
git clone https://github.com/yourusername/incident-response.git


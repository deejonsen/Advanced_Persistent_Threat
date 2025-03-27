# APT34 Cyberattack Analysis Report  
**Datacom Internship Program | Cybersecurity Consultant Simulation**  

---

## Project Overview  
This repository documents the research and analysis conducted during the **Datacom Internship Program**, simulating the role of a cybersecurity consultant tasked with investigating a breach by the APT34 threat group. The goal is to evaluate the attack's impact on a client organization and provide actionable recommendations to strengthen its cybersecurity posture.  

---

## Objectives  
1. **Research APT34**: Analyze the group’s history, motives, TTPs, and nation-state affiliation using OSINT tools.  
2. **Impact Assessment**: Evaluate the breach’s effects on confidentiality, integrity, and availability (CIA triad).  
3. **Defense Strategy**: Use the MITRE ATT&CK Framework to develop countermeasures.  
4. **Leadership Report**: Communicate findings and recommendations effectively.  

---

## Research Methodology  

### 1. **OSINT Data Collection**  
- **Tools Used**:  
  - **Threat Intelligence Platforms**: Mandiant, CrowdStrike, Recorded Future, Symantec.  
  - **Government Resources**: CISA, US-CERT.  
  - **News Outlets**: CyberScoop, Dark Reading.  
- **Key Questions Addressed**:  
  1. **History**: APT34’s first observed activity (2014), aliases (OilRig, Helix Kitten), and campaigns (e.g., POWBAT malware).  
  2. **Nation-State Link**: Associated with **Iran** (CISA Alert AA20-006A).  
  3. **Target Industries**: Energy, finance, telecommunications, and government sectors.  
  4. **Motives**: Espionage, intellectual property theft, geopolitical influence.  
  5. **TTPs**: Spear-phishing, credential dumping, DNS tunneling (mapped to MITRE ATT&CK).  
  6. **Defense Measures**: Network segmentation, MFA, EDR deployment.  

### 2. **MITRE ATT&CK Framework Integration**  
- **Mapped TTPs**:  
  | **Tactic**         | **Technique**                     | **MITRE ID**       |  
  |---------------------|-----------------------------------|--------------------|  
  | Initial Access      | Spear-phishing (Malicious Link)   | T1566.002          |  
  | Credential Access   | LSASS Memory Dumping              | T1003.001          |  
  | Exfiltration        | DNS Tunneling                     | T1048.003          |  
- **Defensive Controls**:  
  - **Email Filtering**: Block phishing attempts (DMARC/DKIM).  
  - **LSASS Protection**: Enable Credential Guard.  
  - **DNS Monitoring**: Detect anomalous traffic patterns.  

---

## Key Findings  

### 1. **APT34 Profile**  
- **Aliases**: OilRig, Helix Kitten.  
- **Operational Since**: 2014.  
- **Sponsorship**: Iranian government.  
- **Signature Campaigns**:  
  - **BONDUPDATER**: Malware mimicking legitimate software updates.  
  - **Domain Spoofing**: Use of lookalike domains (e.g., “micros0ft[.]com”).  

### 2. **Breach Impact**  
- **Confidentiality**: Customer data and IP stolen.  
- **Integrity**: Risk of data manipulation in compromised systems.  
- **Availability**: Potential for destructive attacks (e.g., disk-wiping).  

### 3. **Vulnerabilities Exploited**  
- Unpatched Microsoft Exchange servers.  
- Weak email security configurations.  
- Lack of network segmentation.  

---

## Recommendations  
1. **Immediate Actions**:  
   - Patch critical vulnerabilities (e.g., CVE-2021-26855 for Exchange).  
   - Enforce MFA for all privileged accounts.  
2. **Long-Term Strategy**:  
   - Deploy EDR solutions (e.g., CrowdStrike Falcon).  
   - Conduct quarterly phishing simulations.  
   - Implement Zero Trust Architecture.  
3. **MITRE ATT&CK Alignment**:  
   - Use ATT&CK Navigator to visualize APT34 TTPs and defense gaps.  

---

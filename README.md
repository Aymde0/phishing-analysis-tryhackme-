
# 🛡️ Analyzing Phishing Threats: Tryhackme SOC Simulator Reports

## 🧠 Scenario Title  
**Introduction to Phishing - TryHackMe SOC Level 1 Simulator**

---

## 📌 1. Overview / Scenario Summary  
This scenario is part of the TryHackMe SOC Level 1 Simulator and focuses on phishing analysis in a simulated Security Operations Center (SOC) environment. The objective was to investigate multiple email alerts, distinguish between false positives and actual threats, and respond appropriately to the findings.

---

## 🔍 2. Skills & Tools Used  
- Phishing email analysis  
- Email header inspection  
- IOC (Indicators of Compromise) identification  
- PowerShell command interpretation  
- Threat intelligence validation  
- Decision-making in incident response  
- Tools like VirusTotal and MXToolbox

---

## 🧪 3. Step-by-Step Breakdown

### 1. Initial Alert  
The simulation presented several reported phishing emails for triage and investigation.

### 2. Analysis Performed  
Each email was inspected thoroughly, looking into:
- Sender domain
- URL links
- Email headers
- Content of attachments

I validated links and domains using tools like VirusTotal and header analyzers.

### 3. Findings  
- **Majority of emails**: Determined to be **false positives**, either due to safe links/domains or lack of malicious payload.
- **One true positive** stood out:  
  - A suspicious PowerShell command was embedded in the email.
  - Upon decoding, I discovered that it attempted to download and execute a **privilege escalation PowerShell script** named `PowerCastP1`.
  - This script then **connected to a Command & Control (C2) server**, indicating malicious activity and attacker control.

### 4. Actions Taken  
- Marked the PowerShell-related email as a **true positive**.
- Recommended **blocking** the C2 server’s IP/domain.
- Suggested **endpoint scanning** for affected users.
- Documented the attack chain and escalated the case internally.

---

## 🧠 4. What I Learned  
- Improved ability to distinguish between phishing false positives and actual threats.
- Gained experience interpreting obfuscated PowerShell commands.
- Developed faster threat triage habits using online tools.
- Strengthened judgment in incident escalation decisions.

---

## 📈 5. Challenges Faced  
- Initially, understanding which email artifacts were suspicious required repeated practice.
- The PowerShell command was heavily obfuscated, which took time and research to decode and understand.
- Determining the maliciousness of unknown domains took some effort and multiple cross-verification sources.

---

## 🚀 6. What’s Next?  
- Move on to more advanced phishing scenarios.
- Begin scenarios involving **malware sandboxing** and **host-based investigations**.
- Explore deeper analysis techniques like email spoofing detection and DMARC validation.

---

## 🖼️ 7. Screenshot Evidence 

![Image 09-04-2025 at 19 04](https://github.com/user-attachments/assets/253bb89d-427a-498f-92c8-6a2ec70270c1)

![Image 09-04-2025 at 19 04](https://github.com/user-attachments/assets/a8f9d0cd-06d7-4cd1-8999-594adcd032a7)

![Image 09-04-2025 at 19 03](https://github.com/user-attachments/assets/76428e3b-fd50-435d-867b-a87bf2a72098)

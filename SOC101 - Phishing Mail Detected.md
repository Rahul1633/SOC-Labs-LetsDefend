# 🚨 Phishing Mail Detected

## Overview

- **Alert ID**: SOC101 — Phishing Mail Detected  
- **Initial Action**: Took ownership of the incident and created a case to begin investigation.

---

## Investigation Steps

### 1. Parse Email

- **Date/Time**: Feb, 14, 2021, 03:00 AM 
- **Alert Description**: Phishing email detected.
![soc-101](https://github.com/user-attachments/assets/6a26e226-3fb7-459c-82f2-a6b768d50e0e)


**Email Details**:
- **From**: hahaha@ihackedyourcomputer.com 
- **To**: mark@letsdefend.io 
- **Subject**: I hacked your computer  
- **Action**: Blocked  

The email was parsed to collect sender, recipient, subject, and attachment details.

---

### 2. Analyze Attachments / Links

![soc-101 mail](https://github.com/user-attachments/assets/306daf23-9db8-4558-85ef-668a8f84184c)
There are no attachments or urls 

### 3. Check Email Delivery Status

- The **device action** shows **Blocked**, confirming the email was stopped by security controls and not delivered to the recipient’s mailbox.

---
## Artifacts / IOCs

- **Sender Email**: hahaha@ihackedyourcomputer.com 


## Case Disposition

- **Verdict**: TRUE POSITIVE  
- **Analysis Notes**:  
A scam phishing email was detected and blocked by email security controls. No attachments, user interaction, or endpoint impact were identified.

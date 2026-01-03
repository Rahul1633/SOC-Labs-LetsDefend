# 🚨 Phishing Alert – Deceptive Mail Detected

## Overview

- **Alert ID**: SOC282 — Phishing Alert – Deceptive Mail Detected  
- **Initial Action**: Took ownership of the incident and created a case to begin investigation.

---

## Investigation Steps

### 1. Parse Email

- **Date/Time**: May 13, 2024, 09:22 AM  
- **Alert Description**: Phishing email detected.

**Email Details**:
- **From**: free@coffeeshooop.com  
- **To**: Felix@letsdefend.io  
- **Subject**: Free Coffee Voucher  
- **Action**: Allowed  

The email was parsed to collect sender, recipient, subject, and attachment details.

---

### 2. Analyze Attachments / Links

- **Attachment Name**: `FreeCoffee.zip`  
- **Extracted File**: `Coffee.exe`  

The executable was uploaded to **VirusTotal** for analysis.  
Result: Detected as **malicious by multiple antivirus engines**.

---

### 3. Check Email Delivery Status

- The **device action** shows **Allowed**, confirming the email was successfully delivered to the recipient’s mailbox.

---

### 4. Delete Email from Recipient Mailbox

- Since the email contained a malicious attachment and was delivered, it was removed from the recipient’s mailbox to prevent further risk.

---

### 5. Check Execution of Malicious File

- SIEM/EDR logs were reviewed to determine user interaction.
- Using the recipient identity (**Felix**), endpoint activity was analyzed.

**Findings**:
- `Coffee.exe` was executed on the endpoint.
- Command history confirms execution of the malicious file.

---

### 6. Containment

- The affected endpoint (**Felix**) was isolated to prevent lateral movement or further compromise.
- Incident was escalated to the **Incident Response Team** for deeper investigation.

---

## Artifacts / IOCs

- **Sender Email**: free@coffeeshooop.com  
- **Recipient Email**: Felix@letsdefend.io  
- **Attachment**: Coffee.exe  
- **File Hash (SHA-256)**:  

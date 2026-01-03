# 🚨 Phishing Alert – Deceptive Mail Detected

## Overview

- **Alert ID**: SOC282 — Phishing Alert – Deceptive Mail Detected  
- **Initial Action**: Took ownership of the incident and created a case to begin investigation.

---

## Investigation Steps

### 1. Parse Email

- **Date/Time**: May 13, 2024, 09:22 AM  
- **Alert Description**: Phishing email detected.
<img width="1037" height="359" alt="Pasted image 20251125172106" src="https://github.com/user-attachments/assets/f5a06a1b-1445-40b5-9a67-1cfb686d315a" />

**Email Details**:
- **From**: free@coffeeshooop.com  
- **To**: Felix@letsdefend.io  
- **Subject**: Free Coffee Voucher  
- **Action**: Allowed  

The email was parsed to collect sender, recipient, subject, and attachment details.

---

### 2. Analyze Attachments / Links
<img width="394" height="182" alt="Pasted image 20251125171226" src="https://github.com/user-attachments/assets/43d077e6-1145-4b5e-a005-2b668f9be3db" />

- **Attachment Name**: `FreeCoffee.zip`  
- **Extracted File**: `Coffee.exe`  
<img width="1381" height="669" alt="Pasted image 20251125171921" src="https://github.com/user-attachments/assets/5efd2650-ee91-4066-82b7-50f790e547f1" />

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
<img width="611" height="309" alt="Pasted image 20251125173551" src="https://github.com/user-attachments/assets/3b8435fd-0f12-4639-8cac-bdf228c4e7db" />

- Command history confirms execution of the malicious file.

---

### 6. Containment

- The affected endpoint (**Felix**) was isolated to prevent lateral movement or further compromise.
<img width="1074" height="336" alt="Pasted image 20251125173713" src="https://github.com/user-attachments/assets/16827fd2-78da-4666-bf92-945b17b757c1" />


---

## Artifacts / IOCs

- **Sender Email**: free@coffeeshooop.com  
- **Recipient Email**: Felix@letsdefend.io  
- **Attachment**: Coffee.exe  
- **File Hash (SHA-256)**: cd903ad2211cf7d166646d75e57fb866000f4a3b870b5ec759929be2fd81d334


---

## Case Disposition

- **Verdict**: TRUE POSITIVE  
- **Analysis Notes**:  
Phishing email with malicious attachment detected. The attachment was executed on the recipient’s endpoint. Endpoint isolation performed and incident escalated for further response and monitoring.


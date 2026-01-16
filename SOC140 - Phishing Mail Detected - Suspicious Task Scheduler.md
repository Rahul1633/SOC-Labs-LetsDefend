# 🚨 Phishing Mail Detected - Suspicious Task Scheduler

## Overview

- **Alert ID**: SOC140 - Phishing Mail Detected - Suspicious Task Scheduler 
- **Initial Action**: Took ownership of the incident and created a case to begin investigation.

---

## Investigation Steps

### 1. Parse Email

- **Date/Time**: Mar, 21, 2021, 12:26 PM
- **Alert Description**: Phishing email detected.
<img width="1107" height="320" alt="image" src="https://github.com/user-attachments/assets/e21f9512-7b77-4b24-8ebf-f7789fc2b181" />

**Email Details**:
- **From**: aaronluo@cmail.carleton.ca 
- **To**: mark@letsdefend.io
- **Subject**: COVID19 Vaccine
- **Action**:Blocked 

The email was parsed to collect sender, recipient, subject, and attachment details.

---

### 2. Analyze Attachments / Links
<img width="491" height="166" alt="image" src="https://github.com/user-attachments/assets/02f4c80a-a00e-4349-a78e-7200a87761bb" />

- **Attachment Name**: `72c812cf21909a48eb9cceb9e04b865d.zip`  
- **Extracted File**: `Material.pdf`  
<img width="1705" height="825" alt="image" src="https://github.com/user-attachments/assets/3b644aa8-9071-4a37-88ec-29586e2e9a61" />

The executable was uploaded to **VirusTotal** for analysis.  
Result: Detected as **malicious by multiple antivirus engines**.

---

### 3. Check Email Delivery Status

- The **device action** shows **Blocked**, confirming the email was stopped by security controls and not delivered to the recipient’s mailbox.

---

## Artifacts / IOCs

- **Sender Email**: aaronluo@cmail.carleton.ca 
- **Recipient Email**:mark@letsdefend.io 
- **Attachment**: Material.pdf  
- **File Hash (SHA-256)**: 39fb927c32221134a423760c5d1f58bca4cbbcc87c891c79e390a22b63608eb4


---
## Case Disposition

- **Verdict**: TRUE POSITIVE  
- **Analysis Notes**:  
A phishing email containing one attachment was detected and blocked by email security controls. No user interaction or endpoint impact was observed.

# 🚨 Phishing Alert –  Malicious Attachment Detected 

## Overview

- **Alert ID**:  SOC114 - Malicious Attachment Detected - Phishing Alert
- **Initial Action**: Took ownership of the incident and created a case to begin investigation.

---
## Investigation Steps

### 1. Parse Email

- **Date/Time**: May 13, 2024, 09:22 AM  
- **Alert Description**: Malicious Attachment Detected.
<img width="1470" height="592" alt="image" src="https://github.com/user-attachments/assets/b481620a-e2ef-46e0-8f62-855c89cec20e" />

**Email Details**:
- **From**: accounting@cmail.carleton.ca 
- **To**: accounting@cmail.carleton.ca  
- **Subject**: Invoice 
- **Action**: Allowed  

The email was parsed to collect sender, recipient, subject, and attachment details.

---

### 2. Analyze Attachments / Links
<img width="955" height="233" alt="image" src="https://github.com/user-attachments/assets/122077ab-f9a2-4220-9f0c-8781e253bf0f" />


- **Attachment Name**: `c9ad9506bcccfaa987ff9fc11b91698d`  
- **Extracted File**: `44e65a641fb970031c5efed324676b5018803e0a768608d3e186152102615795.xlsx`  
<img width="1741" height="817" alt="image" src="https://github.com/user-attachments/assets/7d9178c9-7354-406e-ae71-e832824dc65a" />

The executable was uploaded to **VirusTotal** for analysis.  
Result: Detected as **malicious by multiple antivirus engines**.

---

### 3. Check Email Delivery Status

- The **device action** shows **Allowed**, confirming the email was successfully delivered to the recipient’s mailbox.

---

### 4. Delete Email from Recipient Mailbox

- Since the email contained a malicious attachment and was delivered, it was removed from the recipient’s mailbox to prevent further risk.

---




# 🚨 Phishing Alert – Deceptive Mail Detected

## Overview

- **Alert ID**: SOC120 - Phishing Mail Detected - Internal to Internal
- **Initial Action**: Took ownership of the incident and created a case to begin investigation.

---

## Investigation Steps

### 1. Parse Email

- **Date/Time**: Feb, 07, 2021, 04:24 AM
- **Alert Description**: Phishing email detected.
<img width="1111" height="367" alt="image" src="https://github.com/user-attachments/assets/e0ac4aa0-872e-4187-a18a-af658abc1c9d" />


**Email Details**:
- **From**: john@letsdefend.io
- **To**: susie@letsdefend.io
- **Subject**: Meeting 
- **Action**: Allowed  

The email was parsed to collect sender, recipient, subject, and attachment details.

---
### 2. Analyze Attachments / Links
 
There no malicious attachments/links.

---

### 3. Check Email Delivery Status

- The **device action** shows **Allowed**, confirming the email was successfully delivered to the recipient’s mailbox.

---

## Case Disposition

- **Verdict**: FALSE POSITIVE  
- **Analysis Notes**:  
The email was reviewed and no malicious content or indicators were identified. The message was determined to be benign, with no user impact or security risk observed.

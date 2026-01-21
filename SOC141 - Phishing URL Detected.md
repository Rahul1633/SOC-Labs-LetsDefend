# 🚨 Phishing Alert – Malicious URL Detected

## Overview

- **Alert ID**: SOC141 - Phishing URL Detected
- **Initial Action**: Took ownership of the incident and created a case to begin investigation.

---

## Investigation Steps

<img width="1461" height="462" alt="image" src="https://github.com/user-attachments/assets/d2a53b41-bb64-47ae-9120-f51105721df0" />

### 1. Log details

- **Date/Time**: Mar, 22, 2021, 09:23 PM 
- **Alert Description**: Phishing URL detected.
- **Type**: Proxy  
- **Detected URL**: http://mogagrocol.ru/wp-content/plugins/akismet/fv/index.php?email=ellie@letsdefend.io
- **Action**: Allowed
<img width="1377" height="373" alt="image" src="https://github.com/user-attachments/assets/1d15efa9-ea11-4f9a-a196-9b9b655ed435" />




### 2. Analyze Attachments / Links

<img width="1731" height="822" alt="image" src="https://github.com/user-attachments/assets/391435aa-8af6-46d1-a6c7-844c015c9757" />


**The extracted URL was analyzed using VirusTotal. The URL was flagged as suspicious, indicating potential phishing activity associated with the domain.**

### 6. Containment

- The affected endpoint (**EmilyComp**) was isolated to prevent lateral movement or further compromise.
<img width="1107" height="546" alt="image" src="https://github.com/user-attachments/assets/1c577938-7e21-4edf-8ccf-9fa99f936879" />

---






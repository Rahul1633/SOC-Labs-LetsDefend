# 🚨 Malware Detected

## Overview

- **Alert ID**: SOC119 – Proxy – Malicious Executable File Detected  
- **Initial Action**: Took ownership of the incident and created a case to begin investigation.

<img width="1465" height="571" alt="image" src="https://github.com/user-attachments/assets/7867e665-ff98-41c3-afef-aa5aa7050706" />







### 1. Analyze Attachments / Links



<img width="1626" height="786" alt="image" src="https://github.com/user-attachments/assets/72ad0629-643b-4ffc-8bd0-d74220cf91f1" />


**This File is obtained after analysing logs**
<img width="1763" height="825" alt="image" src="https://github.com/user-attachments/assets/7da0be16-268b-4e28-84e9-ca76a733539a" />


The executable was uploaded to **VirusTotal** and **URLSCAN** for analysis.  
Result: Detected as **Non-Malicious by multiple antivirus engines**.

---

### 2. Check C2 Communication

Log Management was reviewed using the affected endpoint’s source address to identify any outbound connections related to the suspected malicious activity.


<img width="1477" height="593" alt="image" src="https://github.com/user-attachments/assets/549735d7-8791-4442-8f97-80a821bdafee" />

<img width="1232" height="537" alt="image" src="https://github.com/user-attachments/assets/591c4a4c-5c59-498c-8185-7dc2b3c64197" />

Log analysis identified a single outbound process, which was verified as legitimate.

<img width="1626" height="786" alt="image" src="https://github.com/user-attachments/assets/72ad0629-643b-4ffc-8bd0-d74220cf91f1" />

<img width="1763" height="825" alt="image" src="https://github.com/user-attachments/assets/7da0be16-268b-4e28-84e9-ca76a733539a" />

 ## Artifacts / IOCs

- **Source Address**: 172.16.17.5
- **Source Address**: 51.195.68.163
- **File Hash (SHA-256)**: 9e1ec8b43a88e68767fd8fed2f38e7984357b3f4186d0f907e62f8b6c9ff56ad
- **File Hash**:  8b88ebbb05a0e56b7dcc708498c02b3e
- **Requested URL**:https://www.win-rar.com/postdownload.html?&L=0&Version=32bit
- **Process**: EXPLORER.EXE
---

## Case Disposition

- **Verdict**: FALSE POSITIVE  
- **Analysis Notes**:  
The alert was triggered by proxy-based detection. Log analysis confirmed the observed event was legitimate and not associated with malicious activity.




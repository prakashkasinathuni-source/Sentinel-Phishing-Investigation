# Microsoft Sentinel Phishing Investigation

This folder contains a SOC investigation of a phishing attack detected using Microsoft Sentinel SIEM.

---

## Overview

A phishing email was delivered to a user, leading to credential compromise after the user clicked a malicious link. Microsoft Sentinel detected abnormal login behavior and raised a high-severity incident.

---

## What was analyzed

- Microsoft 365 email logs
- Azure AD sign-in logs
- Endpoint activity (Defender for Endpoint)
- URL click tracking
- SIEM correlation graph

---

## Key Findings

- Phishing email delivered successfully
- User clicked malicious link
- Credentials likely submitted to attacker
- Suspicious login detected from external IP

---

## Skills Demonstrated

- Microsoft Sentinel SIEM analysis
- Email security investigation
- Identity compromise detection
- Cloud incident response
- Log correlation across Microsoft security stack
- MITRE ATT&CK mapping

---

## MITRE ATT&CK

- T1566 – Phishing  
- T1204 – User Execution  
- T1078 – Valid Accounts  

---

## Outcome

The incident was contained successfully by blocking the attacker, resetting credentials, and securing the user account.

---

## Disclaimer

All data used in this investigation is fictional and created for educational portfolio purposes only.

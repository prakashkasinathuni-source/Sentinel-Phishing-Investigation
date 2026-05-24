# Microsoft Sentinel Phishing Investigation

## Alert Description

Microsoft Sentinel generated a high-severity incident indicating suspicious email activity followed by abnormal user login behavior and potential credential compromise.

The alert was triggered after a user clicked a malicious link contained in a phishing email.

---

## Severity

High

---

## Detection Source

Microsoft Sentinel (SIEM)

---

## Investigation Steps

1. Reviewed Sentinel incident overview and entities involved.
2. Analyzed email logs from Microsoft 365 Defender.
3. Identified phishing email delivered to user inbox.
4. Checked click activity on malicious URL.
5. Investigated Azure AD sign-in logs for abnormal behavior.
6. Correlated endpoint activity using Defender for Endpoint.
7. Verified PowerShell execution and browser activity.
8. Assessed if credentials were used by attacker.

---

## Logs Reviewed

- Microsoft 365 Defender Email Logs
- Azure AD Sign-in Logs
- Microsoft Defender for Endpoint
- Sentinel Incident Graph
- Firewall Proxy Logs

---

## Attack Timeline

| Time | Activity |
|------|----------|
| 09:10 | Phishing email delivered |
| 09:12 | User clicked malicious link |
| 09:15 | Credential submission detected |
| 09:20 | Suspicious login attempt from external IP |

---

## Indicators of Compromise (IOCs)

- Email Subject: “Urgent Password Reset Required”
- Malicious URL: hxxp://secure-login-check[.]com
- IP Address: 185.XX.XX.45
- User Account: user@company.com

---

## MITRE ATT&CK Mapping

- T1566 – Phishing
- T1204 – User Execution
- T1078 – Valid Accounts

---

## Root Cause

The user was targeted by a phishing email impersonating a legitimate service. The user clicked a malicious link and entered credentials, leading to account compromise.

---

## Containment Actions

- Blocked malicious URL in Defender
- Reset user password
- Revoked active sessions
- Enabled MFA enforcement
- Blocked attacker IP address
- Removed phishing email from mailbox

---

## Final Conclusion

The phishing attack was successfully detected and contained before further exploitation occurred. No evidence of lateral movement or data exfiltration was found.

---

## Recommendations

- Improve email filtering policies
- Enable Safe Links and Safe Attachments
- Conduct phishing awareness training
- Enforce MFA for all users
- Monitor Sentinel incidents in real time

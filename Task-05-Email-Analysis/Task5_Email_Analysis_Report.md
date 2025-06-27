# 📧 Task 05 – Email Phishing Analysis

## 🎯 Objective

Analyze a potentially malicious email to identify phishing indicators, inspect email headers, review body content, and suggest mitigations for avoiding such attacks in real-world environments.

---

## 📨 Sample Email (Analyzed)

> Subject: **"Your Account Will Be Closed – Urgent Action Required"**  
> From: **"Apple Support" <support@apple.secure-fix.com>**  
> To: victim@example.com  
> Date: June 26, 2025  
> Attachment: `Account_Suspension_Form.pdf`  
> Link in Email: `https://apple-secure-login.com/login/verify`


---

## 🧠 Indicators of Phishing (Red Flags)

| Element | Finding | Reason |
|--------|---------|--------|
| **Sender** | `@apple.secure-fix.com` | Not an official Apple domain |
| **Reply-To** | Different from From | Common phishing trick |
| **Urgency** | “Account will be closed” | Fear-based social engineering |
| **Link** | `apple-secure-login.com` | Fake domain (not apple.com) |
| **Attachment** | PDF requesting info | Risk of malicious macro or phishing form |
| **Typos** | "Your acount is suspended" | Professional orgs don’t make such errors |


---

## 🔍 Header Analysis (Gmail or any client)

- **Return-Path**: `<spoofed-email@randomdomain.com>`
- **Received from**: IP address shows mismatch with claimed sender domain
- **SPF**: `Fail`  
- **DKIM**: `None`  
- **DMARC**: `Fail`

> These results indicate the email likely did **not** pass verification — red flag.

---

## 🛡️ Mitigations & Security Tips

| Threat | Mitigation |
|--------|------------|
| Phishing Emails | User awareness training, reporting suspicious emails |
| Domain Spoofing | Enforce SPF, DKIM, DMARC |
| Malicious Attachments | Sandbox/scan all attachments with AV or VirusTotal |
| Dangerous Links | Link rewriting, DNS filtering |
| Password Harvesting | MFA, password manager alerts for suspicious logins |

---

## ✅ Conclusion

This email is a **phishing attempt** using social engineering, urgency, domain spoofing, and malicious links to steal credentials. A well-trained user or proper security gateway could detect and prevent this attack.

---

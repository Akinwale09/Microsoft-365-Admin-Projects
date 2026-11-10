# Implementing Phishing Protection in Microsoft 365 Admin Center

## Problem Statement
A company is experiencing an increase in phishing emails, posing a significant security risk. The security team needs to implement protection mechanisms to reduce phishing risks in M365.

## Solution Overview
s
This solution utilizes Microsoft 365 (M365) security features to protect against phishing attacks. The implementation involves:

1. **Microsoft Defender for Office 365**: Configuring anti-phishing policies and settings to detect and block phishing emails. https://security.microsoft.com/
2. **Exchange Online Protection (EOP)**: Setting up anti-phishing rules and filters to further enhance email security. https://admin.cloud.microsoft/exchange#/mailboxes
3. **Entra ID (formerly Azure Active Directory)**: Implementing multi-factor authentication (MFA) and conditional access policies to reduce the risk of compromised accounts. https://entra.microsoft.com/

## Implementation Steps

## Step 1: Configuring Microsoft Defender for Office 365
* **_Setting up anti-phishing rules and settings_**

![antipolicy](./email_security/antipolicy1.png)

![antipolicy](./email_security/antipolicy2.png)

![antipolicy](./email_security/antipolicy3.png)

---

* **_Creat a safe link policy to protect users from malicious URLs**

![safelink](./email_security/safeattach1.png)
![safelink](./email_security/safelink2.png)
![safelink](./email_security/safelink3.png)

---

* **_Configured a safe attachment policy to protect users from malicious email attachments_**

![safeattachments](./email_security/safeattach1.png)
![safeattachments](./email_security/safeattach2.png)
![safeattachments](./email_security/safeattach3.png)

---

* **_Implementing of  Anti-Spam for Zero-hour Auto Purge (ZAP) by moving delivered messages in mailboxes to the Junk Email folder or quarantine if found to be spam, phishing, or contain malware_**

![antispam](./email_security/antispam1.png)
![antispam](./email_security/antispam2.png)
![antispam](./email_security/antispam3.png)
![antispam](./email_security/antispam4.png)
---

* **_Enabled Microsoft Defender Attack Simulation Training_**

![attacksimulation](./email_security/attacksim1.png)
![attacksimulation](./email_security/attacksim2.png)
![attacksimulation](./email_security/attacksim3.png)
![attacksimulation](./email_security/attacksim4.png)
![attacksimulation](./email_security/attacksim5.png)
---

## Step 2: Setting up Exchange Online Protection (EOP)
* **_Setting up external email warning to help users identify emails from outside the organization_**

![emailwarn](./email_security/emailwarn1.png)
![emailwarn](./email_security/emailwarn2.png)
![emailwarn](./email_security/emailwarn3.png)
![emailwarn](./email_security/emailwarn4.png)
![emailwarn](./email_security/emailwarn5.png)
---

## Step 3: Implementing Entra ID security features
* **_Enabling multi-factor authentication (MFA) for all users_**

![mfa](./email_security/mfa.png)
---

## Benefits
This solution provides the following benefits:

* Reduced risk of phishing attacks and compromised accounts.
* Improved email security and filtering capabilities.
* Enhanced user authentication and access controls.


# Skills
- Microsoft 365 Security and Compliance
- Microsoft Defender for Office 365
- Exchange Online Protection (EOP)
- Entra ID 
- Conditional Access 



## Summary of Actions Taken

Feature                              |           Configuration
:-----------------------------------:|:--------------------------------------------------------------:
Defender Anti-Phishing               |Protects against impersonation & phishing attacks
Safe Links                           |Scans & blocks malicious URLs
Safe Attachments                     |Scans email attachments before delivery
External Email Warning               |Alerts users about external emails
Attack Simulation Training           |Phishing simulation for employees
Multi-Factor Authentication (MFA)    |Protects user accounts from phishing



## Conclusion
By implementing this solution, the company can significantly reduce the risk of phishing attacks and improve overall email security in M365.

## Project Overview

### Scenario
A financial services company must retain emails for 7 years due to compliance requirements. 
This project focuses on configuring Microsoft 365 Retention Policies and Archiving to ensure compliance with financial regulations.

### Solution Overview
This solution uses Microsoft 365 to create a 
* Retention Tag,
* Retention Policy
* Configure Archiving
* Enable Auto-Expanding Archive
* Litigation Hold

## Implementation
### *_Configuring Archiving for all users using Powershell_*

Ensure to sign in with global admin account of exchange admin user account

1. Open Powershell
2. Installed Exchange Online
3. Imported Exchange Online Module
4. Connected to Exchange Online

![](./Email%20Retention%20&%20Archiving/archive1.jpeg)
---
5. Enabled Mailbox Archiving Using PowerShell (To automatically enable archive mailboxes for all users)

![](./Email%20Retention%20&%20Archiving/archive2.jpeg)
---
6. To check if archiving is enabled
![](./Email%20Retention%20&%20Archiving/archive3.jpeg)

7. Enabled Auto-Expanding Archive
![](./Email%20Retention%20&%20Archiving/retention1.jpeg)
---

### *_Creating Retention Tags and Policies_*
8. Created Retention Tags (to Move Emails to Archive After 7 Years)

![](./Email%20Retention%20&%20Archiving/retention2.jpeg)
---
9. Creating and Applying a Retention Policy (Creating a Retention Policy that includes the newly created tag)

![](./Email%20Retention%20&%20Archiving/retention3.jpeg)
---
10. Assigning the retention policy to all mailboxes


![](./Email%20Retention%20&%20Archiving/retention4.jpg)
---
11. Verifying the Retention Policy (Check if the retention policy is applied)
![](./Email%20Retention%20&%20Archiving/retention7.jpeg)

Verify from the Admin Portal 

![retention5](./Email%20Retention%20&%20Archiving/retention5.jpeg)
---
### *_Verifying Litigation Hold done to prevent email deletion_*
![](./Email%20Retention%20&%20Archiving/retention6.jpeg)

## Summary

✅ Enable archive mailboxes for all users

✅ Enable auto-expanding archives for large mailboxes

✅ Create & assign a retention policy (7 years, move to archive)

✅ Enable Litigation Hold to meet compliance requirements

## Expected Results

✔️ Emails older than 7 years will automatically move to In-Place Archive.

✔️ The 7-Year Retention Policy is assigned to all users.

✔️ The Litigation Hold on emails is enabled to avoid deletion of mails

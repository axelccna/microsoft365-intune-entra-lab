# Microsoft Intune & Entra ID Lab Portfolio

Hands-on configuration for helpdesk / junior Microsoft 365 support roles.

Practical lab work completed in a Microsoft 365 Business Premium trial tenant.  
Focus is on core, helpdesk-relevant skills: Intune device enrollment and compliance, configuration profiles, app deployment, and Entra Conditional Access with multifactor authentication — configured with Microsoft recommended practices in mind.

---

## 1. Device Enrollment

Enrolled a Windows 11 VM into Microsoft Intune using Entra join with MDM auto-enrollment enabled.  
The device appears as Corporate-owned, managed by Intune, and Compliant.

![Entra device enrollment](./screenshots/device%20entra%20joined%20MDM%20intune%20compliant%20yes%20(microsoft%20admin%20center).png)

![Intune device compliant](./screenshots/intune%20admin%20center,%20device%20compliant.png)

---

## 2. Device Compliance Policy

Created a Windows 11 compliance policy requiring BitLocker, Secure Boot, Code Integrity, Firewall, Antivirus, TPM, and a strong password baseline.  
Assigned to a dedicated device group and verified full compliance.

![Compliance policy settings](./screenshots/win%2011%20baseline%20compliance%20policy.png)

![Compliance policy details](./screenshots/further%20win11%20baseline%20compliance%20settings.png)

![Policy assignment](./screenshots/showing%20the%20policy%20is%20active%20on%20the%20intune%20test%20devices%20group.png)

![Compliance results](./screenshots/screenshot%20showing%20the%20device%20is%20compliant%20with%20the%20policy.png)

---

## 3. Configuration Profile

Deployed a Settings Catalog profile that disables Windows Widgets and turns off Windows Copilot.

![Configuration profile](./screenshots/win%2011%20configurations%20profile,%20disable%20windows%20widgets,%20copilot,%20lockscreen%20timeout.png)

---

## 4. Application Deployment

Added Company Portal from the Microsoft Store and assigned it as **Required** to the Intune Test Devices group.

![Company Portal deployment](./screenshots/windows%20apps,%20adding%20company%20portal%20and%20assigning%20it%20to%20intune%20test%20devices%20group.png)

---

## 5. Conditional Access – Require MFA

Created a custom Conditional Access policy requiring multifactor authentication for the scoped test group.  
Started in Report-only mode, validated via sign-in logs, then switched to On.

![Conditional Access policy](./screenshots/conditional%20access%20policy%20in%20entra%20id%20to%20require%20MFA.png)

![Policy assignment](./screenshots/setting%20up%20conditional%20access%20policy%20for%20intune%20test%20devices%20group.png)

![MFA Grant control](./screenshots/setting%20up%20conditional%20access%20policy%20for%20intune%20test%20devices%20group%20showing%20require%20multifactor%20access%20was%20checked.png)

![Policy matched](./screenshots/conditional%20access%20policy%20details%20showing%20grant%20controls%20satisfied.png)

![MFA prompt](./screenshots/install%20microsoft%20authenticator%20popup%20indicating%20the%20MFA%20policy%20was%20sucessful.png)

![Sign-in logs](./screenshots/activity%20details%20sign-ins,%20authentication%20details,%20previously%20satisfied,%20result%20detail%20mfa%20requirement.png)

---

## 6. Consistent Scoping

Every policy was deliberately assigned to a purpose-built security group (`Intune Test Devices`) rather than “All Devices” or “All Users”.

![Test group members](./screenshots/showing%20the%20test%20device%20and%20test%20user%20are%20in%20the%20require%20mfa%20conditonal%20access%20group.png)

---

## 7. SharePoint / Teams Permissions (bonus)

Tested group membership and folder-level permissions, including diagnosing a classic permission inheritance issue.

![SharePoint group membership](./screenshots/showing%20group%20membership%20of%20sharepoint%20group.png)

![SharePoint permission management](./screenshots/sharepoint%20document%20access%20management%20for%20users.png)

---

## Skills Demonstrated

- Microsoft Intune device enrollment (Entra join + MDM)
- Compliance policy design & verification
- Configuration profiles (Settings Catalog)
- Required app deployment (Company Portal)
- Entra Conditional Access with group-based targeting
- MFA enforcement using Report-only → On rollout
- Policy verification via sign-in logs and real end-user prompt
- SharePoint permission inheritance troubleshooting

**Lab environment:** Microsoft 365 Business Premium trial  
**Focus:** Practical, recruiter-ready configuration

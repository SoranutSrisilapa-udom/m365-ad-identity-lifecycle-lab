# Microsoft 365 & Active Directory Identity Lifecycle Lab

An independent home lab demonstrating Windows domain administration,
Microsoft 365 user support, access troubleshooting, and simulated
employee offboarding.

## Project Objective

Practice provisioning user accounts, assigning access, troubleshooting
sign-in problems, and removing access across separate Active Directory
and Microsoft 365 environments.

## Lab Environment

| Component | Configuration |
|---|---|
| Virtualization | Oracle VirtualBox |
| Domain controller | DC02 — Windows Server 2025 |
| Workstation | WIN11-01 — Windows 11 |
| AD domain | support.test |
| Network | 10.77.0.0/24 |
| Domain controller IP and DNS | 10.77.0.10 |
| Workstation IP | 10.77.0.20 |
| Cloud services | Microsoft 365, Entra ID, Outlook, SharePoint |

The AD and Microsoft 365 accounts were administered separately.
Directory synchronization was not configured.

## Work Completed

### Active Directory and Windows
- Installed and configured AD DS and DNS.
- Joined a Windows 11 workstation to the domain.
- Configured 3 test users, security groups, and organizational units.
- Applied a workstation baseline Group Policy.
- Practiced password resets and required password changes.
- Resolved Remote Desktop authorization through group membership.

### Microsoft 365 and Entra ID
- Provisioned and licensed a cloud test account.
- Verified access to Outlook.
- Registered Microsoft Authenticator and reviewed Security Defaults.
- Reviewed sign-in records and performed a cloud password reset.
- Tested SharePoint access before and after granting visitor permission.

### Simulated Offboarding
- Disabled the AD test account.
- Blocked cloud sign-in and submitted session revocation.
- Removed SharePoint visitor access.
- Captured rejected fresh sign-in attempts for the restricted accounts.

## Troubleshooting Examples

| Problem | Corrective action |
|---|---|
| Client DNS queries failed | Corrected a duplicate IP address and subnet mask, then verified internal DNS resolution |
| Remote Desktop login was denied | Added the domain access group to the workstation's Remote Desktop Users group |
| SharePoint testing used the wrong identity | Repeated the test using the intended standard-user browser session |

## Validation and Limitations

- Verified domain sign-in, DNS service discovery, and applied Group Policy.
- Captured successful access after permission changes and rejected sign-ins after account restrictions.
- Authenticator registration was verified; the inspected sign-in did not prove an MFA challenge.
- The inactivity policy was applied, but exact elapsed lock timing was not independently recorded.
- Offboarding covered specific account and access restrictions; complete license and group cleanup was not demonstrated.
- This was an educational lab, not a production deployment.

## Skills Demonstrated

Active Directory, DNS, Group Policy, Windows troubleshooting,
Microsoft 365 administration, Entra ID, access permissions,
identity lifecycle management, and technical documentation.

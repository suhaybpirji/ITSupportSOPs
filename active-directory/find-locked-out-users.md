# Find Locked-Out Users in Active Directory

## Purpose
To identify which user accounts are currently locked out and determine the cause of repeated lockouts.

## Steps

### 1. Use PowerShell (Recommended)
1. Open PowerShell as Administrator.
2. Run:
   Search-ADAccount -LockedOut

3. To show detailed info:
   Search-ADAccount -LockedOut | Select-Object Name, SamAccountName, LockedOut, LastLogonDate

### 2. Use Active Directory Users and Computers
1. Open ADUC.
2. Right-click the domain → Find.
3. Click the drop-down and select “Custom Search”.
4. Go to the Advanced tab.
5. Paste this LDAP query:
   (lockoutTime>=1)
6. Click Find.

### 3. Check Event Viewer for Lockout Source
1. On the domain controller, open Event Viewer.
2. Navigate to:
   Windows Logs → Security
3. Look for Event ID **4740**:
   - This shows which device caused the lockout.

### 4. Common Lockout Causes
- Mobile device using old password
- Outlook storing old credentials
- Mapped drives with saved passwords
- Background services running under the user’s account
- Remote Desktop sessions still active

## Verification
- User is no longer locked out.
- Lockout source identified and resolved.
- No repeated lockouts after password reset.

## Notes
If lockouts continue, consider enabling **Account Lockout Policy auditing** for deeper investigation.

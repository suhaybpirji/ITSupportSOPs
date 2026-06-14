# Disable a User Account (Offboarding)

## Purpose
To securely offboard a user who has left the organisation by disabling their account and removing access to all systems.

## Steps
1. Open Active Directory Users and Computers.
2. Locate the user account.
3. Right-click → Disable Account.
4. Move the account to the “Disabled Users” OU.
5. Reset the password to a random secure value.
6. Remove all group memberships except “Domain Users”.
7. Convert mailbox to a shared mailbox if required.
8. Revoke all active sign-in sessions in Azure AD.
9. Remove assigned Microsoft 365 licenses.

## Verification
- Confirm the account shows the disabled icon.
- Ensure mailbox access is removed.
- Check Intune/Endpoint Manager for device wipe if needed.

## Notes
Never delete accounts immediately — archive first according to company policy.

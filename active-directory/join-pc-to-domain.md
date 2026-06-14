# Join a Windows PC to the Domain

## Purpose
To join a Windows workstation to the Active Directory domain so the user can authenticate and access network resources.

## Steps
1. Open Settings → System → About.
2. Click “Rename this PC (advanced)” or “Domain or workgroup”.
3. Click “Change…”.
4. Select “Domain” and enter the domain name (e.g., company.local).
5. Enter domain admin credentials when prompted.
6. Restart the PC when asked.
7. Log in using a domain account.

## Verification
- Check the computer object appears in the correct OU in AD.
- Confirm the user can log in with their domain credentials.
- Test access to shared drives and printers.

## Notes
Ensure the PC has correct DNS settings pointing to the domain controller.

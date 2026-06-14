# Fix Microsoft Teams Login Issues

## Purpose
To resolve problems where users cannot sign in to Microsoft Teams on desktop, web, or mobile.

## Symptoms
- “We couldn’t sign you in”
- “Something went wrong”
- Teams stuck on loading screen
- Endless sign‑in loop
- MFA prompt not appearing
- Incorrect account showing
- Teams opens but shows blank screen

## Steps

### 1. Check Microsoft 365 Account Status
1. Go to https://admin.microsoft.com
2. Open **Users → Active users**
3. Confirm:
   - User is not blocked
   - License includes Teams (Business/Enterprise)
   - Sign‑in allowed

### 2. Clear Teams Cache (Most Common Fix)
1. Fully close Teams
2. Press Windows + R → type:
   %appdata%\Microsoft\Teams
3. Delete everything inside the folder
4. Restart Teams

### 3. Sign Out and Sign In Again
1. Click profile picture → Sign out
2. Close Teams completely
3. Reopen and sign in

### 4. Check for Multiple Accounts
Teams may get confused if:
- Work + personal accounts are mixed
- Cached credentials exist

Clear Windows credentials:
1. Open **Credential Manager**
2. Remove:
   - MicrosoftOffice
   - Teams
   - ADAL
   - MSAL

### 5. Check MFA / Conditional Access
If login fails after MFA:
- Reset MFA (see reset-mfa.md)
- Check Conditional Access policies
- Ensure device is compliant (Intune)

### 6. Check Teams Service Health
Go to:
https://admin.microsoft.com → **Health → Service health**

Look for:
- Teams login issues
- Authentication outages
- Microsoft Entra issues

### 7. Try Teams Web
Go to:
https://teams.microsoft.com

If web works but desktop doesn’t → desktop cache/profile issue.

### 8. Reinstall Teams
1. Uninstall Teams
2. Delete:
   %appdata%\Microsoft\Teams
   %localappdata%\Microsoft\Teams
3. Reinstall from:
   https://www.microsoft.com/en/microsoft-teams/download-app

### 9. Check Firewall / Proxy
Ensure these URLs are allowed:
- *.teams.microsoft.com
- *.office.com
- *.microsoftonline.com
- *.skype.com

### 10. Check Device Time & Date
Incorrect time breaks authentication.

Set to automatic:
Settings → Time & Language → Date & Time → Set time automatically

## Verification
- User signs in successfully
- Teams loads chats and channels
- No sign‑in loops
- MFA prompts work correctly

## Notes
If Teams still fails:
- Check for broken Windows profile
- Check for Intune compliance issues
- Review sign‑in logs in Entra ID

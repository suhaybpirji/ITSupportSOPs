# Fix Outlook Online (Outlook on the Web) Issues

## Purpose
To resolve problems where users cannot access Outlook Online, emails do not load, or features are missing in the web version of Outlook.

## Symptoms
- Outlook Online not loading
- Blank screen or spinning loader
- “Something went wrong”
- Emails not appearing
- Cannot send or receive emails
- Missing folders
- Attachments not opening
- Search not working

## Steps

### 1. Check Microsoft 365 Service Health
Go to:
https://admin.microsoft.com → **Health → Service health**

Look for issues with:
- Exchange Online
- Outlook on the web
- Microsoft Entra ID (authentication)

If there’s an outage → wait for Microsoft to resolve it.

### 2. Try a Private/Incognito Window
If Outlook works in private mode:
- Browser cache or cookies are corrupted

### 3. Clear Browser Cache & Cookies
For Chrome:
1. Settings → Privacy → Clear browsing data
2. Clear:
   - Cached images/files
   - Cookies

For Edge:
1. Settings → Privacy
2. Clear browsing data

### 4. Disable Browser Extensions
Extensions that commonly break Outlook:
- Ad blockers
- Script blockers
- Privacy extensions
- VPN browser plugins

Disable them and reload Outlook.

### 5. Check User License
In Microsoft 365 Admin Center:
1. Go to **Users → Active users**
2. Select the user
3. Ensure they have:
   - Exchange Online license
   - Outlook Web Access enabled

### 6. Check Mailbox Status in Exchange Admin Center
Go to:
https://admin.exchange.microsoft.com

Check:
- Mailbox exists
- Mailbox is not disabled
- Mailbox is not on hold or restricted
- No mailbox corruption alerts

### 7. Reset Outlook Web Settings
In Outlook Online:
1. Click **Settings**
2. Search for **Reset view**
3. Reset:
   - Folder pane
   - Reading pane
   - Message list

### 8. Check Browser Compatibility
Outlook Online works best with:
- Microsoft Edge
- Google Chrome

Safari and Firefox may have limited features.

### 9. Check Conditional Access Policies
If Outlook Online works on one device but not another:
- Device may be blocked by Conditional Access

Check:
https://entra.microsoft.com → **Protection → Conditional Access**

### 10. Check Authentication Issues
If login loops or fails:
- Reset MFA (see reset-mfa.md)
- Check sign‑in logs for blocked attempts

### 11. Check Mailbox Quota
If mailbox is full:
- User cannot send or receive emails

Check in Exchange Admin Center:
- Mailbox usage → Increase quota (if allowed)

## Verification
- Outlook Online loads normally
- Emails appear correctly
- User can send and receive messages
- No login loops or blank screens
- Search works

## Notes
If Outlook Online still fails:
- Try another browser
- Check for network/firewall restrictions
- Check if the mailbox is soft‑deleted or recently restored

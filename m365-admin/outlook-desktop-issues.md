# Fix Outlook Desktop Issues (Microsoft 365)

## Purpose
To resolve problems with the Outlook desktop app including loading issues, profile corruption, sync failures, and connection problems.

## Symptoms
- Outlook stuck on “Loading Profile”
- Outlook not opening
- Cannot connect to mailbox
- “Disconnected” or “Trying to connect…”
- Search not working
- Missing folders or emails
- Slow performance
- Send/Receive errors
- Outlook crashes or freezes

## Steps

### 1. Restart Outlook and the Device
Simple but effective:
- Fully close Outlook
- Restart the computer
- Reopen Outlook

### 2. Check Microsoft 365 Service Health
Go to:
https://admin.microsoft.com → **Health → Service health**

Look for issues with:
- Exchange Online
- Outlook
- Authentication

### 3. Check Internet and VPN
Outlook may fail if:
- VPN is blocking traffic
- Firewall is restricting ports
- Network is unstable

Try:
- Disconnect VPN
- Switch network
- Restart router (home users)

### 4. Run Outlook in Safe Mode
Press Windows + R → type:

outlook.exe /safe

If Outlook works in Safe Mode:
- Add‑ins are causing the issue

Disable add‑ins:
1. File → Options → Add‑ins
2. Manage COM Add‑ins → Go
3. Disable all
4. Re‑enable one by one

### 5. Repair the Outlook Profile
1. Go to **Control Panel → Mail**
2. Click **Email Accounts**
3. Select the account
4. Click **Repair**

### 6. Create a New Outlook Profile
1. Control Panel → Mail
2. Click **Show Profiles**
3. Add → create new profile
4. Set it as default

If Outlook works → old profile was corrupted.

### 7. Clear Outlook Cache
Close Outlook, then delete:

%localappdata%\Microsoft\Outlook  
%appdata%\Microsoft\Outlook  

Reopen Outlook.

### 8. Reset Outlook Search Index
1. Control Panel → Indexing Options
2. Click **Advanced**
3. Click **Rebuild**

### 9. Check Autodiscover
Autodiscover issues cause:
- Wrong mailbox
- Connection failures

Test using:
https://testconnectivity.microsoft.com

### 10. Repair Office Apps
1. Settings → Apps
2. Microsoft 365 Apps
3. Modify → **Quick Repair**
4. If still broken → **Online Repair**

### 11. Check Mailbox Size
Large mailboxes slow Outlook.

In Outlook:
File → Tools → Mailbox Cleanup

### 12. Reset Navigation Pane
Run:

outlook.exe /resetnavpane

Fixes:
- Missing folders
- Broken folder pane

### 13. Check OST File Corruption
Delete the OST file:
1. Close Outlook
2. Go to:
   %localappdata%\Microsoft\Outlook
3. Delete the .ost file
4. Outlook will recreate it

### 14. Check Conditional Access / MFA
If Outlook won’t authenticate:
- Reset MFA (see reset-mfa.md)
- Check Conditional Access policies
- Ensure device is compliant (Intune)

## Verification
- Outlook opens normally
- Mailbox connects without errors
- Emails sync correctly
- Search works
- No crashes or freezes
- Performance is normal

## Notes
If Outlook still fails:
- Check for Windows profile corruption
- Check for third‑party antivirus blocking Outlook
- Check for PST corruption (if using PST files)

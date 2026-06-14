# Fix Shared Mailbox Calendar Issues (Microsoft 365)

## Purpose
To configure, manage, and troubleshoot calendar access and permissions for shared mailboxes in Microsoft 365.

## Common Scenarios
- Users cannot view the shared mailbox calendar
- Calendar not appearing in Outlook
- Delegates not receiving meeting invites
- Cannot edit or create calendar events
- Calendar permissions missing or incorrect
- Shared mailbox calendar not syncing across devices

---

## 1. Access the Shared Mailbox Calendar

### Outlook Desktop
1. Open Outlook
2. Expand the shared mailbox (left pane)
3. Click **Calendar**
4. The shared calendar should appear automatically

### Outlook Online
1. Go to https://outlook.office.com
2. Click **Calendar**
3. Add calendar → **Add shared calendar**
4. Enter the shared mailbox name

---

## 2. Assign Calendar Permissions

### Using Outlook Online
1. Open the shared mailbox calendar
2. Click **Share**
3. Add the user
4. Choose permission level:
   - **Can view**
   - **Can edit**
   - **Delegate**

### Using PowerShell (Advanced)

Set-MailboxFolderPermission "shared@domain.com:\Calendar" -User user@domain.com -AccessRights Editor

---

## 3. Permission Levels Explained

### Reviewer
- Can view events only

### Editor
- Can create, edit, and delete events

### Delegate
- Can manage calendar fully
- Receives meeting invites on behalf of the mailbox

---

## 4. Troubleshooting Calendar Issues

### Issue: Calendar Not Appearing in Outlook
Try:
- Restart Outlook
- Remove and re-add Full Access permissions
- Add the calendar manually in Outlook Online
- Create a new Outlook profile

---

### Issue: Cannot Edit Calendar Events
Check:
- User has **Editor** or **Delegate** permissions
- Full Access is assigned to the shared mailbox
- No Conditional Access restrictions

---

### Issue: Delegate Not Receiving Meeting Invites
Fix:
1. Open Outlook Desktop
2. File → Account Settings → Delegate Access
3. Ensure:
   **Delegate receives meeting invites** is enabled

---

### Issue: Calendar Not Syncing Across Devices
Try:
- Remove and re-add the shared mailbox in Outlook
- Clear Outlook cache:
%appdata%\Microsoft\Outlook

- Check mobile device sync settings

---

### Issue: Calendar Permissions Not Applying
Fix:
- Remove permission
- Wait 5 minutes
- Re-add permission
- Check for hybrid environment (on‑prem AD)

---

### Issue: Shared Mailbox Calendar Missing in Teams
Check:
- Shared mailbox must be linked to a Microsoft 365 Group
- Teams license assigned to user
- Teams creation not restricted

---

## 5. Verification
- Calendar appears in Outlook and Outlook Online
- User can create/edit events
- Delegates receive meeting invites
- No permission or sync errors
- Calendar updates sync across all devices

---

## Notes
If issues persist:
- Check if shared mailbox is synced from on‑prem AD
- Check retention or litigation hold
- Check if mailbox was recently converted
- Microsoft Support can repair corrupted calendar folders




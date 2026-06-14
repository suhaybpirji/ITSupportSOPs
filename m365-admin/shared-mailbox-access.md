# Fix Shared Mailbox Access Issues (Microsoft 365)

## Purpose
To resolve issues where users cannot access a shared mailbox in Outlook or Outlook Online.

## Symptoms
- Shared mailbox not appearing in Outlook
- “Cannot expand the folder”
- “You do not have permission to access this mailbox”
- Shared mailbox missing from Outlook Online
- Send As / Send on Behalf not working

## Steps

### 1. Check Permissions in M365 Admin Center
1. Go to https://admin.microsoft.com
2. Navigate to:
   Teams & groups → Active teams & groups
3. Search for the shared mailbox
4. Open it → Click **Members**
5. Ensure the user is added as:
   - **Member** (for access)
   - **Mailbox delegate** (for Send As / Send on Behalf)

### 2. Assign Permissions in Exchange Admin Center
1. Go to https://admin.exchange.microsoft.com
2. Open **Recipients → Mailboxes**
3. Search for the shared mailbox
4. Open **Mailbox delegation**
5. Add the user to:
   - **Full Access**
   - **Send As**
   - **Send on Behalf** (if required)

### 3. Wait for Permission Propagation
- Full Access: usually 5–15 minutes
- Send As: can take up to 60 minutes

### 4. Restart Outlook
- Fully close Outlook
- Reopen it to reload mailbox permissions

### 5. Add the Shared Mailbox Manually (If Needed)
In Outlook:
1. File → Account Settings → Account Settings
2. Double‑click the user’s mailbox
3. Click **More Settings**
4. Go to **Advanced**
5. Click **Add**
6. Enter the shared mailbox name

### 6. Check Outlook Online
Go to:
https://outlook.office.com

On the left pane:
- Click the user’s name → **Open another mailbox**
- Enter the shared mailbox name

If it opens here but not in Outlook → Outlook profile issue.

### 7. Fix Send As Issues
If Send As fails:
- Ensure the user is added under **Mailbox delegation → Send As**
- Remove and re‑add the permission
- Wait 30–60 minutes
- Restart Outlook

### 8. Check Licensing (Important)
Shared mailboxes **do not require a license**, *unless*:
- Mailbox is over 50GB
- Litigation hold is enabled
- Archiving is enabled

## Verification
- Shared mailbox appears in Outlook
- User can read and send emails
- Send As / Send on Behalf works
- No permission errors

## Notes
If the mailbox still doesn’t appear:
- Recreate the user’s Outlook profile
- Check for Conditional Access restrictions
- Check if the mailbox is hidden from address lists

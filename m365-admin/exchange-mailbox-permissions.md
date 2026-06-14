# Manage Exchange Mailbox Permissions (Microsoft 365)

## Purpose
To assign, remove, or troubleshoot mailbox permissions such as Full Access, Send As, and Send on Behalf for user and shared mailboxes.

## Common Scenarios
- User cannot access another mailbox
- Send As not working
- Send on Behalf missing
- Permissions not applying
- Outlook shows “Cannot expand the folder”
- Delegates not receiving meeting invites

## Types of Permissions

### 1. Full Access
Allows a user to:
- Open the mailbox
- Read emails
- Manage folders
- View calendar

Does NOT allow sending as the mailbox.

### 2. Send As
Allows a user to send email **as** the mailbox.
Recipient sees the mailbox as the sender.

### 3. Send on Behalf
Allows a user to send email **on behalf of** the mailbox.
Recipient sees:
`User on behalf of Mailbox`

---

## Steps

### 1. Open Exchange Admin Center
https://admin.exchange.microsoft.com

### 2. Navigate to Mailboxes
1. Go to **Recipients → Mailboxes**
2. Search for the mailbox (user or shared)
3. Click the mailbox

### 3. Assign Full Access Permissions
1. Go to **Mailbox delegation**
2. Under **Full Access**, click **Add**
3. Select the user
4. Save

Propagation time: **5–15 minutes**

### 4. Assign Send As Permissions
1. In **Mailbox delegation**
2. Under **Send As**, click **Add**
3. Select the user
4. Save

Propagation time: **30–60 minutes**

### 5. Assign Send on Behalf Permissions
1. In **Mailbox delegation**
2. Under **Send on Behalf**, click **Add**
3. Select the user
4. Save

Propagation time: **Instant**

---

## Troubleshooting

### 1. Permission Not Applying
Try:
- Remove the permission
- Wait 5 minutes
- Add it again

### 2. Outlook Not Showing the Mailbox
- Restart Outlook
- Recreate Outlook profile
- Add mailbox manually (Advanced settings)

### 3. Send As Not Working
Check:
- User added under **Send As**
- Wait up to 60 minutes
- Remove and re‑add permission
- Restart Outlook

### 4. Delegate Not Receiving Meeting Invites
In Outlook:
1. File → Account Settings → Delegate Access  
2. Ensure “Delegate receives meeting invites” is enabled

### 5. Mailbox Hidden from Address List
If mailbox doesn’t appear:
1. In Exchange Admin Center
2. Open mailbox → **General**
3. Ensure **Hide from address lists** is OFF

### 6. Hybrid Environments
If permissions don’t apply:
- Mailbox may be synced from on‑prem AD
- Changes must be made on‑prem

---

## Verification
- User can open the mailbox
- Send As works
- Send on Behalf works
- No permission errors
- Outlook loads mailbox correctly

## Notes
If permissions still fail:
- Check Conditional Access
- Check if mailbox is soft‑deleted
- Check if user is in a restricted group
- Review audit logs for permission changes

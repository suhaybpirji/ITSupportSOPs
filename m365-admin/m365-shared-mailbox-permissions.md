# Manage Shared Mailbox Permissions (Microsoft 365)

## Purpose
To assign, remove, and troubleshoot permissions for shared mailboxes, including Full Access, Send As, and Send on Behalf.

## Common Scenarios
- User needs access to a shared mailbox
- Send As not working
- Shared mailbox not appearing in Outlook
- Delegate cannot send emails
- Permissions not applying after changes
- Shared mailbox access issues in Teams/Groups

---

## Types of Permissions

### 1. Full Access
Allows a user to:
- Open the shared mailbox
- Read and manage emails
- Create folders
- View calendar

Does NOT allow sending as the mailbox.

### 2. Send As
Allows a user to send emails **as** the shared mailbox.

Recipient sees:
`Shared Mailbox Name`

### 3. Send on Behalf
Allows a user to send emails **on behalf of** the shared mailbox.

Recipient sees:
`User Name on behalf of Shared Mailbox Name`

---

## Assign Permissions

### 1. Open Exchange Admin Center
https://admin.exchange.microsoft.com

### 2. Navigate to Shared Mailboxes
1. Go to **Recipients → Mailboxes**
2. Filter by **Shared**
3. Select the shared mailbox

### 3. Add Full Access
1. Go to **Mailbox delegation**
2. Under **Full Access**, click **Add**
3. Select the user
4. Save

Propagation time: **5–15 minutes**

### 4. Add Send As
1. Under **Send As**
2. Click **Add**
3. Select the user
4. Save

Propagation time: **30–60 minutes**

### 5. Add Send on Behalf
1. Under **Send on Behalf**
2. Click **Add**
3. Select the user
4. Save

Propagation time: **Instant**

---

## Outlook Configuration

### Auto‑mapping
Full Access automatically maps the mailbox in Outlook.

If it does NOT appear:
- Remove Full Access
- Wait 5 minutes
- Re‑add it
- Restart Outlook

### Manual Add (If Needed)
1. File → Account Settings
2. Select account → Change
3. More Settings → Advanced
4. Add shared mailbox manually

---

## Troubleshooting

### Issue: Send As Not Working
Check:
- Permission assigned under **Send As**
- Wait up to 60 minutes
- Remove and re‑add permission
- Restart Outlook

### Issue: Shared Mailbox Not Appearing
Try:
- Restart Outlook
- Create new Outlook profile
- Add mailbox manually
- Check if mailbox is hidden from address lists

### Issue: Cannot Open Shared Mailbox
Check:
- Full Access assigned
- User license includes Outlook/Exchange
- No Conditional Access blocks

### Issue: Delegate Not Receiving Calendar Invites
Fix:
- Enable “Delegate receives meeting invites”
- Remove and re‑add delegate
- Check Outlook rules

### Issue: Permissions Not Applying
- Remove permission
- Wait 5 minutes
- Add again
- Check for hybrid environment (on‑prem AD)

---

## Verification
- User can open the shared mailbox
- Send As works
- Send on Behalf works
- Calendar access works
- Mailbox appears in Outlook automatically

---

## Notes
If issues persist:
- Check if mailbox is synced from on‑prem AD
- Check retention or litigation hold
- Check if mailbox was recently converted
- Review audit logs for permission changes

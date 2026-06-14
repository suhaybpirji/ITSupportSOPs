# Mailbox Delegation (Microsoft 365)

## Purpose
To assign, manage, and troubleshoot mailbox delegation permissions such as Full Access, Send As, and Send on Behalf for user and shared mailboxes.

## Common Scenarios
- Manager wants assistant to manage their mailbox
- Delegate needs to send emails on behalf of someone
- Shared mailbox access required
- Calendar delegation issues
- Send As not working
- Delegate not receiving meeting invites

---

## Types of Delegation

### 1. Full Access
Allows the delegate to:
- Open the mailbox
- Read and manage emails
- Create folders
- View calendar

Does NOT allow sending as the mailbox.

### 2. Send As
Allows the delegate to send emails **as** the mailbox.

Recipient sees:
`Mailbox Name`

### 3. Send on Behalf
Allows the delegate to send emails **on behalf of** the mailbox.

Recipient sees:
`Delegate Name on behalf of Mailbox Name`

---

## Assign Delegation Permissions

### 1. Open Exchange Admin Center
https://admin.exchange.microsoft.com

### 2. Navigate to Mailboxes
1. Go to **Recipients → Mailboxes**
2. Select the mailbox
3. Click **Mailbox delegation**

---

## Add Full Access
1. Under **Full Access**
2. Click **Add**
3. Select the user
4. Save

Propagation time: **5–15 minutes**

---

## Add Send As
1. Under **Send As**
2. Click **Add**
3. Select the user
4. Save

Propagation time: **30–60 minutes**

---

## Add Send on Behalf
1. Under **Send on Behalf**
2. Click **Add**
3. Select the user
4. Save

Propagation time: **Instant**

---

## Delegate Calendar Access (Outlook)
In Outlook:
1. File → Account Settings → Delegate Access
2. Add delegate
3. Choose permissions:
   - Reviewer
   - Author
   - Editor
4. Enable:
   **Delegate receives meeting invites**

---

## Troubleshooting

### Issue: Send As Not Working
Check:
- Permission assigned under **Send As**
- Wait up to 60 minutes
- Remove and re‑add permission
- Restart Outlook

### Issue: Cannot Open Mailbox
Check:
- Full Access assigned
- Outlook profile corruption
- Mailbox hidden from address lists

### Issue: Delegate Not Receiving Meeting Invites
Fix:
- Enable “Delegate receives meeting invites”
- Remove and re‑add delegate
- Check Outlook rules

### Issue: Mailbox Not Appearing Automatically
Try:
- Restart Outlook
- Create new Outlook profile
- Add mailbox manually

### Issue: Hybrid Environment
If mailbox is synced from on‑prem:
- Delegation must be set on‑prem AD

---

## Verification
- Delegate can open the mailbox
- Send As works
- Send on Behalf works
- Calendar delegation works
- No permission errors

---

## Notes
If delegation still fails:
- Check Conditional Access restrictions
- Check if mailbox is soft‑deleted
- Check if user is in restricted admin groups
- Review audit logs for permission changes

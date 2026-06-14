# Fix Send As Issues for Shared Mailboxes (Microsoft 365)

## Purpose
To configure, verify, and troubleshoot **Send As** permissions for shared mailboxes in Microsoft 365.

## Common Scenarios
- User cannot send as a shared mailbox
- “You do not have permission to send to this recipient”
- Emails sent show the user instead of the shared mailbox
- Send As works in Outlook Online but not Desktop
- Send As takes too long to apply
- Delegates receiving NDR (bounce) messages

---

## 1. Assign Send As Permission

### Steps
1. Open **Exchange Admin Center**  
   https://admin.exchange.microsoft.com

2. Go to **Recipients → Mailboxes**

3. Filter by **Shared**

4. Select the shared mailbox

5. Open **Mailbox delegation**

6. Under **Send As**, click **Add**

7. Select the user → Save

### Propagation Time
- Send As can take **30–60 minutes** to apply
- Sometimes up to **2 hours** in large tenants

---

## 2. Verify Send As in Outlook

### Outlook Desktop
When composing a new email:
1. Click **From**
2. Select the shared mailbox
3. Send a test email

### Outlook Online
1. New message
2. Click **From**
3. Choose the shared mailbox

---

## 3. Troubleshooting Send As Issues

### Issue: “You do not have permission to send to this recipient”
Causes:
- Send As not applied yet
- Wrong mailbox selected in the From field
- Permission not saved correctly

Fix:
- Remove Send As → wait 5 minutes → re‑add
- Restart Outlook

---

### Issue: Send As Works in OWA but Not Desktop
This is common.

Fix:
- Restart Outlook
- Create a new Outlook profile
- Clear Outlook cache:
%appdata%\Microsoft\Outlook


---

### Issue: Emails Show “User on behalf of Shared Mailbox”
Cause:
- User has **Send on Behalf**, not **Send As**

Fix:
- Remove Send on Behalf
- Add Send As only

---

### Issue: Shared Mailbox Not Appearing in Outlook
Fix:
- Ensure **Full Access** is also assigned
- Restart Outlook
- Add mailbox manually if needed

---

### Issue: Send As Not Applying After 1 Hour
Try:
- Remove permission
- Wait 5 minutes
- Add again
- Check for hybrid environment (on‑prem AD)

---

### Issue: Send As Fails for External Recipients
Check:
- Anti‑spam outbound policy
- Transport rules blocking external senders
- DKIM/DMARC alignment issues (rare)

---

## 4. Verification
- User can send emails **as** the shared mailbox
- Recipients see the shared mailbox as the sender
- No NDR or permission errors
- Works in both Outlook Desktop and Outlook Online

---

## Notes
If Send As still fails:
- Check if mailbox is synced from on‑prem AD
- Check if user is in restricted admin groups
- Check audit logs for permission changes
- Microsoft Support can force a permission sync



# Configure Mailbox Forwarding (Microsoft 365)

## Purpose
To set up, remove, or troubleshoot email forwarding for user and shared mailboxes in Microsoft 365.

## Common Scenarios
- Forward emails to another user
- Forward emails to an external address
- Forward emails from a shared mailbox
- Disable unwanted forwarding
- Fix forwarding not working
- Auto‑forwarding blocked by security policies

---

## Steps

### 1. Open Exchange Admin Center
https://admin.exchange.microsoft.com

### 2. Navigate to Mailboxes
1. Go to **Recipients → Mailboxes**
2. Search for the mailbox
3. Click the mailbox

---

## Configure Forwarding

### 3. Set Up Forwarding
1. Open the mailbox
2. Go to **Mail flow**
3. Click **Manage email forwarding**
4. Enable **Forward all emails**
5. Enter the forwarding address
6. (Optional) Tick **Keep a copy of forwarded messages**

Click **Save**

---

## Remove Forwarding

### 4. Disable Forwarding
1. Open **Manage email forwarding**
2. Turn off forwarding
3. Save

---

## Forwarding to External Addresses

### 5. Allow External Forwarding (If Blocked)
If forwarding to Gmail/Outlook.com fails:
- Tenant may block external forwarding

Check:
1. Go to **Microsoft 365 Defender portal**
   https://security.microsoft.com
2. Open **Policies → Anti‑spam**
3. Edit **Outbound spam policy**
4. Enable:
   **Automatic external forwarding → On**

---

## Forwarding via Inbox Rules

### 6. Check Inbox Rules (User‑Created)
Sometimes forwarding is set by a rule.

In Outlook Online:
1. Settings → Mail → Rules
2. Look for:
   - Forward
   - Redirect
   - Move to folder rules

Delete unwanted rules.

---

## Troubleshooting

### 7. Forwarding Not Working
Check:
- Forwarding address is correct
- External forwarding allowed
- No conflicting transport rules
- No DLP policies blocking forwarding
- Mailbox not hidden from address lists
- Recipient mailbox not full

### 8. Check Transport Rules
A mail flow rule may override forwarding.

Go to:
**Mail flow → Rules**

Look for:
- Block forwarding
- Redirect overrides
- DLP restrictions

### 9. Check Message Trace
Run a message trace to confirm:
- Email was forwarded
- Email was blocked
- Email was quarantined

### 10. Check Shared Mailbox Forwarding
Shared mailboxes can forward too.

Steps are identical:
- Open shared mailbox
- Manage email forwarding

---

## Verification
- Emails forward successfully
- External forwarding works (if enabled)
- No bounce messages
- Message trace confirms forwarding
- User receives forwarded mail instantly

---

## Notes
If forwarding still fails:
- Check Conditional Access restrictions
- Check if forwarding is blocked by tenant security baseline
- Check if the mailbox is compromised (unexpected forwarding is a red flag)

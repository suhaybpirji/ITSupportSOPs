# Convert Mailboxes Between User and Shared (Microsoft 365)

## Purpose
To convert a mailbox from a **user mailbox → shared mailbox** or from a **shared mailbox → user mailbox**, and resolve issues that occur after conversion.

## Common Scenarios
- Employee has left → convert to shared mailbox
- Shared mailbox needs to become a user mailbox
- License removal required
- Access issues after conversion
- Mailbox not appearing in Outlook after conversion
- Send As / Full Access permissions missing

---

## 1. Convert User Mailbox → Shared Mailbox

### Steps
1. Go to **Microsoft 365 Admin Center**  
   https://admin.microsoft.com

2. Navigate to:  
   **Users → Active users**

3. Select the user mailbox

4. Click **Mail** tab

5. Scroll down to **More actions**

6. Click **Convert to shared mailbox**

### After Conversion
- Remove the user’s license (optional)
- Add members under:
  - **Mailbox delegation**
  - **Microsoft 365 Admin Center → Members**

### Important Notes
- Shared mailboxes **do not require a license** unless:
  - Over 50GB
  - Litigation hold enabled
  - Archiving enabled

---

## 2. Convert Shared Mailbox → User Mailbox

### Steps
1. Go to **Exchange Admin Center**  
   https://admin.exchange.microsoft.com

2. Navigate to:  
   **Recipients → Mailboxes**

3. Select the shared mailbox

4. Click **Convert to regular mailbox**

5. Go to **Microsoft 365 Admin Center**

6. Assign a valid license:
   - Exchange Online
   - Microsoft 365 Business / Enterprise

### After Conversion
- User must sign in with a valid password
- Outlook may require a new profile

---

## 3. Troubleshooting After Conversion

### Issue: Mailbox Not Appearing in Outlook
Fix:
- Restart Outlook
- Recreate Outlook profile
- Add mailbox manually

### Issue: Permissions Missing
After conversion, re‑add:
- Full Access
- Send As
- Send on Behalf

### Issue: Cannot Sign In
If converting shared → user:
- Reset password
- Ensure sign‑in is allowed
- Assign correct license

### Issue: Mailbox Still Shows as Shared
Propagation can take:
- 5–30 minutes

Force refresh:
- Remove license → wait → reassign

### Issue: Mailbox Hidden from Address Lists
Check:
1. Exchange Admin Center
2. Mailbox → **General**
3. Ensure **Hide from address lists** is OFF

---

## 4. Verification
- Mailbox type shows correctly (user or shared)
- Permissions work
- Mailbox appears in Outlook
- User can send/receive mail
- No license warnings

---

## Notes
If conversion still fails:
- Check if mailbox is synced from on‑prem AD (hybrid)
- Check for retention or litigation hold
- Check if mailbox is soft‑deleted or recently restored
- Microsoft Support can force a mailbox type repair

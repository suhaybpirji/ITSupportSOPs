# Recover a Mailbox in Microsoft 365

## Purpose
To restore a user mailbox that has been deleted, disabled, corrupted, or needs recovery after accidental removal or account deletion.

## Common Scenarios
- User account was deleted and restored
- Mailbox missing in Outlook or Outlook Online
- Mailbox converted to shared and needs reverting
- Mailbox corrupted or inaccessible
- Need to recover mailbox data for a departed employee
- Soft‑deleted mailbox needs restoration

---

## Steps

### 1. Check if the User Account Still Exists
Go to:
https://admin.microsoft.com → **Users → Active users**

If the user is missing:
- Check **Deleted users**
- Restore the user if found

Mailbox is retained for **30 days** after deletion.

---

### 2. Check for a Soft‑Deleted Mailbox
Go to:
https://admin.exchange.microsoft.com → **Recipients → Mailboxes**

Click **Soft‑deleted mailboxes**.

If the mailbox is listed:
- Select it
- Click **Restore**

This reconnects the mailbox to the user account.

---

### 3. Restore a Mailbox for a Deleted User
If the user was deleted and restored:
- Mailbox may take **15–30 minutes** to reattach
- If not, restore manually:

1. Go to **Exchange Admin Center**
2. Open **Soft‑deleted mailboxes**
3. Select the mailbox
4. Choose **Restore**
5. Link it to the restored user account

---

### 4. Convert Shared Mailbox Back to User Mailbox
If mailbox was accidentally converted:

1. Go to **Exchange Admin Center**
2. Open the mailbox
3. Click **Convert to regular mailbox**
4. Assign a license in Microsoft 365 Admin Center

Mailbox requires:
- Exchange Online license

---

### 5. Recover Deleted Items (Up to 30 Days)
In Outlook Online:
1. Open **Deleted Items**
2. Click **Recover items deleted from this folder**
3. Restore required emails

---

### 6. Recover Purged Items (Admin Only)
Admins can recover items beyond user recovery:

1. Go to **Compliance Center**
2. Open **Content search**
3. Search the mailbox
4. Export or restore items

Useful for:
- Legal investigations
- HR requests
- Security incidents

---

### 7. Restore Mailbox Using eDiscovery
For advanced recovery:
1. Go to **Microsoft Purview Compliance Portal**
2. Create a **Content Search**
3. Export mailbox data (PST)
4. Import back into the user’s mailbox

---

### 8. Check Litigation Hold / Retention Policies
If mailbox is on hold:
- Data is preserved even if deleted
- Restore via eDiscovery

Check:
https://admin.exchange.microsoft.com → **Mailbox → Compliance**

---

### 9. Check for Corrupted Mailbox
If mailbox loads but behaves incorrectly:
- Missing folders
- Search broken
- Sync issues

Run:
- Outlook profile repair
- OST rebuild
- Mailbox repair via Microsoft Support (admin‑only)

---

## Verification
- Mailbox appears in Outlook and Outlook Online
- Emails, folders, and calendar restored
- No sync or connection issues
- User can send/receive mail normally

---

## Notes
If mailbox cannot be restored:
- Check if retention period expired (30 days)
- Check if the user was hard‑deleted (permanent)
- Check if the mailbox was never provisioned
- Contact Microsoft Support for deep corruption cases

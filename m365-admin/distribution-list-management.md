# Manage Distribution Lists (Microsoft 365)

## Purpose
To manage membership, permissions, and delivery settings for distribution lists (DLs) in Microsoft 365.

## Common Tasks
- Add or remove members
- Allow external senders
- Manage send permissions
- Convert DL to Microsoft 365 Group
- Fix “You don’t have permission to send to this group”

## Steps

### 1. Open Microsoft 365 Admin Center
https://admin.microsoft.com

### 2. Navigate to Distribution Lists
1. Go to **Teams & groups**
2. Click **Active teams & groups**
3. Filter by **Distribution list**

### 3. Add or Remove Members
1. Select the distribution list
2. Click **Members**
3. Add or remove users as needed
4. Changes apply instantly

### 4. Allow External Senders
If external emails are bouncing:
1. Open the DL
2. Go to **Settings**
3. Enable:
   **Allow people outside the organisation to send email to this group**

### 5. Manage Send Permissions
To allow a user to send as the DL:
1. Go to **Exchange Admin Center**
   https://admin.exchange.microsoft.com
2. Navigate to **Recipients → Groups**
3. Select the DL
4. Go to **Settings → Send As**
5. Add the user

Propagation time:
- Send As: 30–60 minutes
- Membership: instant

### 6. Restrict Who Can Send to the DL
1. In Exchange Admin Center
2. Open the DL
3. Go to **Delivery management**
4. Choose:
   - Only senders inside the organisation
   - Only specific senders

### 7. Convert DL to Microsoft 365 Group (Optional)
Useful for:
- Shared mailbox features
- Teams integration
- Shared files and calendar

Steps:
1. In Microsoft 365 Admin Center
2. Select the DL
3. Click **Convert to Microsoft 365 Group**

### 8. Fix “You don’t have permission to send to this group”
Check:
- Delivery management restrictions
- Moderation settings
- Send As permissions
- External sender settings

### 9. Check Moderation Settings
If emails require approval:
1. In Exchange Admin Center
2. Open the DL
3. Go to **Moderation**
4. Disable or update moderators

## Verification
- Emails deliver successfully
- Members receive messages
- Send As works
- External senders can email (if enabled)

## Notes
If DL changes don’t apply:
- Wait for propagation (up to 60 minutes for Send As)
- Check if the DL is synced from on‑prem AD (hybrid environment)

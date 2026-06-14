# Manage Microsoft 365 Groups

## Purpose
To manage membership, permissions, settings, and troubleshooting for Microsoft 365 Groups used across Outlook, Teams, SharePoint, and Planner.

## Common Scenarios
- Add or remove group members
- Manage group owners
- Fix access issues to group resources
- Convert distribution list to M365 Group
- Restore deleted groups
- Manage shared mailbox + SharePoint site linked to the group

---

## Steps

### 1. Open Microsoft 365 Admin Center
https://admin.microsoft.com

### 2. Navigate to Microsoft 365 Groups
1. Go to **Teams & groups**
2. Click **Active teams & groups**
3. Filter by **Microsoft 365** group

---

## Membership Management

### 3. Add or Remove Members
1. Select the group
2. Click **Members**
3. Add or remove users

Changes apply instantly.

### 4. Add or Remove Group Owners
Owners can:
- Manage membership
- Manage group settings
- Approve join requests

Steps:
1. Open the group
2. Click **Owners**
3. Add or remove owners

---

## Group Settings

### 5. Manage Group Privacy
Groups can be:
- **Public** (anyone can join)
- **Private** (owner approval required)

Change privacy:
1. Open the group
2. Click **Settings**
3. Choose Public or Private

### 6. Allow External Senders
To allow external emails:
1. Open the group
2. Go to **Settings**
3. Enable:
   **Let people outside the organization email the group**

### 7. Manage Subscription Settings
Control whether members receive group emails in their inbox.

---

## Linked Resources

### 8. Access the Group’s SharePoint Site
Every M365 Group has a SharePoint site.

To open it:
1. Select the group
2. Click **Files**
3. Open the SharePoint site

### 9. Access the Group’s Shared Mailbox
1. Go to Outlook Online
2. Click your profile picture
3. Select **Open another mailbox**
4. Enter the group name

### 10. Access the Group’s Teams Workspace
If the group is connected to Teams:
- It will appear in the Teams app automatically

If not:
- Create a Team from the existing group

---

## Advanced Management

### 11. Convert a Distribution List to a Microsoft 365 Group
1. Go to **Exchange Admin Center**
2. Open **Recipients → Groups**
3. Select the DL
4. Click **Upgrade to Microsoft 365 Group**

Requirements:
- DL must not be dynamic
- DL must not be nested

### 12. Restore a Deleted Microsoft 365 Group
Deleted groups are retained for **30 days**.

Steps:
1. Go to **Teams & groups → Deleted groups**
2. Select the group
3. Click **Restore**

Restores:
- SharePoint site
- Shared mailbox
- Planner
- Teams workspace (if applicable)

### 13. Check Group Expiration Policies
If groups are auto‑expiring:
- Check Azure AD Group Expiration settings

---

## Troubleshooting

### 14. User Cannot Access Group Files
Check:
- Group membership
- SharePoint permissions
- Conditional Access policies

### 15. Group Not Appearing in Outlook
Check:
- Group privacy settings
- Outlook client version
- Cached mode issues

### 16. Group Not Appearing in Teams
Check:
- Whether the group is connected to a Team
- Teams license assigned
- Teams creation restrictions

---

## Verification
- Members can access group resources
- Owners can manage the group
- Shared mailbox and SharePoint site work
- Teams integration works (if applicable)
- No permission or access errors

---

## Notes
If group issues persist:
- Check if the group is synced from on‑prem AD (hybrid)
- Check retention or compliance policies
- Check if the group was recently restored

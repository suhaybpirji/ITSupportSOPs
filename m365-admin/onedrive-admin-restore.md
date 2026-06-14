# Restore OneDrive Files (Admin Guide)

## Purpose
To restore deleted, corrupted, or ransomware‑affected files in a user’s OneDrive using Microsoft 365 admin tools.

## Common Scenarios
- User accidentally deleted files
- Files overwritten or corrupted
- Ransomware encrypted files
- Sync conflict caused data loss
- Need to restore OneDrive to a previous point in time

## Steps

### 1. Open Microsoft 365 Admin Center
https://admin.microsoft.com

### 2. Navigate to the User
1. Go to **Users → Active users**
2. Search for the affected user
3. Open their profile

### 3. Open the User’s OneDrive Admin Panel
1. In the user’s profile, click **OneDrive**
2. Click **Create link to files**
3. Open the OneDrive admin page

### 4. Restore Deleted Files (Recycle Bin)
1. On the left, open **Recycle bin**
2. Select files or folders
3. Click **Restore**

If files are not there:
- Check **Second‑stage recycle bin**

### 5. Use “Restore Your OneDrive” (Full Rollback)
This is the most powerful recovery option.

1. In OneDrive, click **Settings → Restore your OneDrive**
2. Choose a restore point:
   - Last 24 hours
   - Last week
   - Last month
   - Custom date/time
3. Review file activity timeline
4. Click **Restore**

This rolls back the entire OneDrive to a previous state.

### 6. Recover Files from Version History
For individual files:
1. Right‑click the file
2. Select **Version history**
3. Restore the correct version

### 7. Check for Ransomware Alerts
If ransomware is detected:
- OneDrive automatically prompts for a restore
- Admins can force a restore from the OneDrive admin panel

### 8. Check Sharing Links (If Files Were Shared)
If users report missing access:
1. Select the file/folder
2. Click **Manage access**
3. Re‑add sharing links or permissions

### 9. Check Sync Issues
If files are missing locally but exist in the cloud:
- Reset OneDrive (see onedrive-sync-issues.md)
- Re‑sync the affected folders

## Verification
- Files are restored
- User confirms data is correct
- No sync conflicts
- No ransomware‑encrypted files remain

## Notes
If files cannot be restored:
- Check retention policies
- Check if the user was deleted (OneDrive is retained for 30 days)
- Check if the site is locked by compliance or legal hold

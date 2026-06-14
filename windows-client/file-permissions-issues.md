# Fix File Permission Issues on Windows

## Purpose
To resolve problems where users cannot open, modify, delete, or access files or folders due to incorrect NTFS permissions or ownership.

## Symptoms
- “Access Denied”
- Cannot delete files or folders
- Cannot save changes
- Missing security tab
- Files locked by another process
- User cannot access shared folders

## Steps

### 1. Check NTFS Permissions
1. Right‑click the file/folder → Properties.
2. Go to the Security tab.
3. Check if the user or their group has:
   - Read
   - Write
   - Modify
   - Full Control (if required)

If missing → add the correct permissions.

### 2. Take Ownership (If Needed)
1. Right‑click → Properties → Security → Advanced.
2. Click “Change” next to Owner.
3. Enter the username or group.
4. Tick “Replace owner on subcontainers and objects”.
5. Apply.

### 3. Reset Permissions Using ICACLS
Run Command Prompt as Administrator:

icacls "C:\path\to\folder" /reset /t /c

This resets permissions to default.

### 4. Grant Full Control (If Required)
Run:

icacls "C:\path\to\folder" /grant username:F /t

Replace *username* with the actual user.

### 5. Check File Locks
Files may be locked by:
- Word/Excel
- OneDrive
- Antivirus
- Background processes

Use Task Manager to close the locking app.

### 6. Check Inherited Permissions
1. Go to Security → Advanced.
2. Ensure “Enable inheritance” is ON.
3. If OFF, permissions may be broken.

### 7. Check Shared Folder Permissions (If Network Share)
- NTFS permissions
- Share permissions
- AD group membership

Both must allow access.

### 8. Check Encryption (EFS)
If the file is encrypted:
- Only the original user can open it.
- Check for green filenames (EFS indicator).

### 9. Check Disk Errors
Run:

chkdsk C: /f

Corrupted file systems can break permissions.

## Verification
- User can open, modify, and delete files as expected.
- No “Access Denied” errors.
- Permissions are correctly inherited.
- Shared folders work normally.

## Notes
If permissions are repeatedly breaking:
- Check for misconfigured GPOs
- Check for OneDrive sync conflicts
- Check for third‑party security tools

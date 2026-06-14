# Fix OneDrive Sync Issues

## Purpose
To resolve problems where OneDrive files are not syncing, stuck, missing, or showing error icons.

## Symptoms
- Files not syncing
- Red X or yellow warning icons
- “Processing changes” stuck
- “Sync paused”
- Missing files or folders
- OneDrive not starting

## Steps

### 1. Check OneDrive Status
- Ensure OneDrive is running.
- Click the OneDrive icon in the taskbar.
- Check for error messages.

### 2. Restart OneDrive
Run:
%localappdata%\Microsoft\OneDrive\OneDrive.exe /shutdown
Then start it again from Start Menu.

### 3. Check Internet Connection
- Ensure the device is online.
- Test with:
  ping 8.8.8.8

### 4. Check Storage Space
- Ensure there is enough space on the device.
- Ensure the user has OneDrive cloud storage available.

### 5. Sign Out and Sign In Again
1. Open OneDrive settings.
2. Go to Account.
3. Click “Unlink this PC”.
4. Sign in again.

### 6. Reset OneDrive (Full Reset)
Run:
%localappdata%\Microsoft\OneDrive\onedrive.exe /reset

Then restart OneDrive manually.

### 7. Check File Path Length
- Windows has a 260‑character path limit.
- Shorten folder names if needed.

### 8. Check for Invalid Characters
OneDrive does not allow:
- * : ? " < > |  
- Leading/trailing spaces

Rename files if required.

### 9. Check File Locks
- Files may be locked by Office apps.
- Close Word, Excel, Teams, or Outlook.

### 10. Check OneDrive Admin Policies (If Managed)
- Storage limits
- Blocked file types
- Conditional access policies

## Verification
- OneDrive shows “Up to date”
- No sync errors
- Files appear on both local device and cloud

## Notes
If OneDrive still fails:
- Reinstall OneDrive
- Check Event Viewer → Applications and Services Logs → OneDrive

# Fix a Corrupted Windows User Profile

## Purpose
To resolve issues where a Windows user profile becomes corrupted, causing login problems, missing settings, or broken applications.

## Symptoms
- “User profile cannot be loaded”
- Temporary profile is loaded
- Missing desktop icons or files
- Settings not saving
- Apps crashing or resetting
- Slow login or black screen after login

## Steps

### 1. Check if Windows Loaded a Temporary Profile
1. Press Windows + R → type: sysdm.cpl
2. Go to the Advanced tab → User Profiles → Settings
3. If you see “TEMP” or a temporary profile → corruption confirmed

### 2. Restart the Device
Sometimes Windows repairs the profile automatically after a reboot.

### 3. Check Event Viewer for Profile Errors
Navigate to:
Windows Logs → Application

Look for:
- Event ID 1511 (temporary profile)
- Event ID 1515 (profile cannot be loaded)
- Event ID 1500/1508 (corruption)

### 4. Rename the Corrupted Profile Folder
1. Go to:
   C:\Users\
2. Find the user’s folder.
3. Rename it to:
   username.old

### 5. Fix Registry Profile List Entry
1. Press Windows + R → regedit
2. Navigate to:
   HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList
3. Find the SID with `.bak` at the end.
4. Rename:
   - Remove `.bak` from the correct SID
   - Add `.bak` to the corrupted one (if needed)
5. Ensure `ProfileImagePath` points to the correct folder.

### 6. Log In to Generate a New Profile
- Log out and log back in.
- Windows will create a fresh profile folder.

### 7. Copy User Data from Old Profile
Copy from:
C:\Users\username.old\

To:
C:\Users\username\

Copy folders:
- Desktop  
- Documents  
- Downloads  
- Pictures  
- Favourites  
- AppData\Local (selectively)  
- AppData\Roaming (selectively)

### 8. Reconfigure Applications
- Outlook profile
- OneDrive sync
- Browser profiles
- Mapped drives
- Printers

### 9. Delete the Old Profile (Optional)
Once confirmed working:
- Delete the `.old` folder
- Remove old SID from ProfileList

## Verification
- User logs in normally
- No temporary profile
- Desktop and files restored
- Apps work correctly
- Settings save properly

## Notes
If corruption keeps happening:
- Check disk health (chkdsk)
- Check for roaming profile issues
- Check antivirus or backup tools

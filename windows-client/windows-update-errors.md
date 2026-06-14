# Fix Windows Update Errors

## Purpose
To diagnose and resolve issues preventing Windows from downloading or installing updates.

## Symptoms
- Updates stuck at 0% or 100%
- Error codes (0x80070002, 0x800f081f, 0x8024a105, etc.)
- “Something went wrong”
- “We couldn’t complete the updates”
- Endless reboot/update loop

## Steps

### 1. Run Windows Update Troubleshooter
1. Open Settings → System → Troubleshoot → Other troubleshooters.
2. Run “Windows Update”.
3. Apply any fixes it suggests.

### 2. Restart Windows Update Services
Run these commands in PowerShell (Admin):

net stop wuauserv  
net stop bits  
net stop cryptsvc  

Rename update folders:

ren C:\Windows\SoftwareDistribution SoftwareDistribution.old  
ren C:\Windows\System32\catroot2 catroot2.old  

Restart services:

net start wuauserv  
net start bits  
net start cryptsvc  

### 3. Check Disk Space
- Ensure at least 10GB free on C:
- Delete temp files if needed.

### 4. Run System File Checker
Run:

sfc /scannow

### 5. Run DISM to Repair Windows Image
Run:

DISM /Online /Cleanup-Image /RestoreHealth

### 6. Install Updates Manually
1. Go to https://www.catalog.update.microsoft.com
2. Search for the KB number.
3. Download and install the update manually.

### 7. Check Group Policy (If Managed Device)
Open gpedit.msc and check:

Computer Configuration → Administrative Templates → Windows Update

Ensure no restrictive policies are blocking updates.

### 8. Check Event Viewer
Navigate to:

Windows Logs → System  
Applications and Services Logs → WindowsUpdateClient

Look for update-related errors.

## Verification
- Windows Update completes successfully.
- No error codes appear.
- Device restarts normally.

## Notes
If updates still fail:
- Check for third‑party antivirus interference.
- Consider performing an in‑place upgrade using the Windows Media Creation Tool.

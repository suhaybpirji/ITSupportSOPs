# Fix a Slow Windows PC

## Purpose
To diagnose and resolve performance issues on a Windows workstation that is running slowly.

## Symptoms
- Slow startup
- Apps take long to open
- High CPU or memory usage
- Freezing or lagging
- Fan running loudly

## Steps

### 1. Check Task Manager
1. Press Ctrl + Shift + Esc.
2. Check:
   - CPU usage
   - Memory usage
   - Disk usage
3. Identify apps using high resources.

### 2. Disable Startup Programs
1. Open Task Manager → Startup tab.
2. Disable unnecessary apps:
   - Teams auto-start
   - OneDrive (if not used)
   - Adobe Updater
   - Spotify
   - Steam

### 3. Clear Temporary Files
1. Press Windows + R → type %temp%
2. Delete all files.
3. Repeat with:
   - temp
   - prefetch

### 4. Run Disk Cleanup
1. Press Windows + R → cleanmgr
2. Select C:
3. Tick temporary files, thumbnails, recycle bin.

### 5. Check for Windows Updates
1. Settings → Windows Update.
2. Install all pending updates.

### 6. Check Disk Health
Run:
chkdsk C: /f

### 7. Check for Malware
- Run Windows Defender full scan.
- Remove suspicious apps.

### 8. Update Drivers
1. Open Device Manager.
2. Update:
   - Display drivers
   - Network drivers
   - Chipset drivers

### 9. Check Storage Space
- Ensure at least 10–20% free space on C: drive.

### 10. Restart the PC
A fresh reboot clears memory and stuck processes.

## Verification
- PC boots faster.
- Apps open normally.
- CPU/memory usage stabilises.
- No freezing or lag.

## Notes
If the PC is still slow:
- Check for failing HDD (use CrystalDiskInfo)
- Consider upgrading to SSD
- Add more RAM

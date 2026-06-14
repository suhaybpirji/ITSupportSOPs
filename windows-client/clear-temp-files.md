# Clear Temporary Files on Windows

## Purpose
To free up disk space and improve system performance by removing temporary files, cache, and leftover application data.

## Steps

### 1. Use Windows Disk Cleanup
1. Press Windows + R.
2. Type: cleanmgr
3. Select the system drive (usually C:).
4. Tick:
   - Temporary files
   - Thumbnails
   - Recycle Bin
   - Delivery Optimization Files
5. Click OK → Delete Files.

### 2. Manually Clear Temp Folders
1. Press Windows + R.
2. Type: %temp%
3. Delete all files inside the folder.
4. Press Windows + R again.
5. Type: temp
6. Delete all files inside (skip files in use).

### 3. Clear Prefetch (Optional)
1. Press Windows + R.
2. Type: prefetch
3. Delete all files.

### 4. Clear Browser Cache (Optional)
- Chrome: Settings → Privacy → Clear browsing data
- Edge: Settings → Privacy → Clear browsing data
- Firefox: Settings → Privacy → Clear data

### 5. Restart the PC
This ensures all locked files are released and removed.

## Verification
- Disk space increases.
- System performance improves.
- No errors when opening applications.

## Notes
Do not delete system folders or Windows Update files unless instructed by IT policy.

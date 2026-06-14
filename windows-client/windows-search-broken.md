# Fix Windows Search Not Working

## Purpose
To resolve issues where the Windows search bar or Start menu search stops working, becomes unresponsive, or shows no results.

## Symptoms
- Search bar not responding
- Cannot type in the search box
- No results appear
- Search crashes or freezes
- Start menu search not opening
- Cortana/SearchUI errors

## Steps

### 1. Restart Windows Search Service
1. Press Windows + R → type: services.msc
2. Find “Windows Search”
3. Right‑click → Restart

If the service is disabled:
- Set Startup Type to “Automatic”
- Start the service

### 2. Restart Search Processes
Open Task Manager and restart:
- SearchHost.exe
- SearchApp.exe
- SearchUI.exe (older versions)

### 3. Rebuild the Search Index
1. Open Control Panel → Indexing Options
2. Click “Advanced”
3. Under Troubleshooting, click “Rebuild”
4. Wait for indexing to complete

### 4. Run Search Troubleshooter
1. Open Settings → System → Troubleshoot → Other troubleshooters
2. Run “Search and Indexing”
3. Select the symptoms and apply fixes

### 5. Reset Windows Search (PowerShell)
Run PowerShell as Administrator:

Get-AppxPackage -Name Microsoft.Windows.Search | Reset-AppxPackage

### 6. Check for Corrupted System Files
Run:

sfc /scannow  
DISM /Online /Cleanup-Image /RestoreHealth

### 7. Check Keyboard Input Services
Ensure these services are running:
- Touch Keyboard and Handwriting Panel Service
- Text Input Management Service

### 8. Check Group Policy (If Managed Device)
Open gpedit.msc:

User Configuration → Administrative Templates → Start Menu and Taskbar

Ensure no policies disable search.

### 9. Create a New User Profile (If Needed)
If search works on a new profile → original profile is corrupted.

## Verification
- Search bar responds instantly
- Results appear correctly
- No freezing or errors
- Start menu search works normally

## Notes
If search still fails:
- Perform an in‑place Windows repair
- Check for third‑party software blocking search

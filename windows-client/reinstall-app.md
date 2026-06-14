# Reinstall an Application on Windows

## Purpose
To fix issues caused by corrupted application files, failed updates, or missing components by performing a clean reinstall.

## Steps

### 1. Uninstall the Application
1. Open Settings → Apps → Installed Apps.
2. Search for the application.
3. Click Uninstall.
4. Follow the prompts to remove it completely.

### 2. Remove Leftover Files (If Needed)
1. Press Windows + R → type %appdata%
2. Delete the folder related to the app.
3. Press Windows + R → type %localappdata%
4. Delete the app folder there too.
5. Check:
   C:\Program Files\
   C:\Program Files (x86)\
   Remove any leftover folders.

### 3. Restart the PC
This clears locked files and resets the environment.

### 4. Download the Latest Installer
- Use the official vendor website.
- Avoid third‑party download sites.
- Ensure you download the correct version (32‑bit or 64‑bit).

### 5. Install the Application
1. Run the installer as Administrator.
2. Follow the setup wizard.
3. Sign in if required.

### 6. Apply Updates
- Check for updates inside the app.
- Install any required plugins or extensions.

## Verification
- App launches without errors.
- No missing DLL or runtime errors.
- User can perform required tasks.

## Notes
If the app still fails:
- Check Event Viewer → Application logs.
- Reinstall .NET, Visual C++ Redistributables, or Java (if required).

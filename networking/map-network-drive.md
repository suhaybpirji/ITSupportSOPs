# Map a Network Drive

## Purpose
To map a shared network folder to a drive letter so users can easily access shared files and resources.

## Steps

### 1. Using File Explorer
1. Open File Explorer.
2. Right-click “This PC”.
3. Select “Map network drive…”.
4. Choose a drive letter (e.g., H:).
5. Enter the network path:
   \\server\sharename
6. Tick “Reconnect at sign-in”.
7. Tick “Connect using different credentials” if needed.
8. Click Finish.

### 2. Using Command Line
Run:
net use H: \\server\sharename /persistent:yes

### 3. Using PowerShell
Run:
New-PSDrive -Name "H" -PSProvider FileSystem -Root "\\server\sharename" -Persist

### 4. Check Permissions
If access is denied:
- Confirm the user is in the correct AD security group.
- Check NTFS permissions on the folder.
- Check share permissions.

### 5. Troubleshoot Common Issues
- Ensure the server is reachable:
  ping servername
- Ensure DNS resolves the server:
  nslookup servername
- Ensure the user is logged into the domain.

## Verification
- Drive appears under “This PC”.
- User can open and modify files (if permitted).
- Drive reconnects after reboot.

## Notes
If multiple users need the same drive, deploy via Group Policy Preferences.

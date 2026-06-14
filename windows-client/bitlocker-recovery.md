# BitLocker Recovery Guide

## Purpose
To assist users who are prompted for a BitLocker recovery key and cannot access their device.

## Symptoms
- Device asks for BitLocker recovery key at startup
- User cannot log in
- TPM reset or hardware change triggered recovery
- BIOS/UEFI changes caused BitLocker to lock

## Steps

### 1. Check Azure AD / Entra ID for Recovery Key
If the device is Azure AD joined:
1. Go to https://entra.microsoft.com
2. Navigate to:
   Devices → All Devices
3. Select the device.
4. Click “BitLocker keys”.
5. Provide the recovery key to the user.

### 2. Check Microsoft Account (Personal Devices)
If the device uses a Microsoft account:
1. Go to https://account.microsoft.com/devices/recoverykey
2. Sign in with the user’s Microsoft account.
3. Locate the matching device name.
4. Provide the recovery key.

### 3. Check On‑Prem Active Directory
If the device is domain‑joined:
1. Open Active Directory Users and Computers.
2. Right‑click the computer → Properties.
3. Go to the “BitLocker Recovery” tab.
4. Copy the recovery key.

### 4. Enter the Recovery Key
1. At the BitLocker screen, enter the 48‑digit key.
2. Press Enter to unlock the drive.

### 5. Identify the Cause
Common triggers:
- BIOS/UEFI updates
- TPM reset
- Hardware changes (RAM, SSD)
- Secure Boot changes
- Boot order changes

### 6. Suspend and Re‑Enable BitLocker (Recommended)
After logging in:
1. Open PowerShell as Admin.
2. Run:
   Suspend-BitLocker -MountPoint "C:"
3. Restart the device.
4. Re‑enable:
   Resume-BitLocker -MountPoint "C:"

## Verification
- Device boots normally.
- No further BitLocker prompts.
- Recovery key is backed up in the correct location.

## Notes
If no recovery key exists anywhere:
- There is **no bypass**.
- The only option is to **wipe and reinstall Windows**.

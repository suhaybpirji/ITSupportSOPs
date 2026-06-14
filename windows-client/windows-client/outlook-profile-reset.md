# Reset an Outlook Profile

## Purpose
To fix issues caused by corrupted Outlook profiles, including sync problems, missing emails, search issues, and startup errors.

## Symptoms
- Outlook stuck on “Loading Profile”
- Emails not syncing
- Search not working
- Missing folders or mailboxes
- Frequent crashes
- “Something went wrong” errors

## Steps

### 1. Close Outlook Completely
- Ensure Outlook is not running in the background.
- Check Task Manager and end any Outlook.exe processes.

### 2. Open Outlook Profile Manager
1. Press Windows + R.
2. Type:
   control mlcfg32.cpl
3. Click “Show Profiles”.

### 3. Create a New Profile
1. Click “Add”.
2. Enter a name (e.g., “Outlook-New”).
3. Sign in with the user’s email account.
4. Complete the setup wizard.

### 4. Set the New Profile as Default
1. In the Profiles window, select:
   “Always use this profile”
2. Choose the new profile from the dropdown.
3. Click Apply → OK.

### 5. Start Outlook
- Outlook will rebuild the mailbox.
- This may take time depending on mailbox size.

### 6. Reconfigure Additional Mailboxes (If Needed)
- Shared mailboxes
- Additional accounts
- PST files
- Archive mailboxes

### 7. Rebuild Search Index (If Search Is Broken)
1. Go to:
   Control Panel → Indexing Options
2. Click “Advanced”.
3. Click “Rebuild”.

### 8. Clear Autocomplete Cache (Optional)
1. In Outlook:
   File → Options → Mail
2. Under “Send messages”, click:
   “Empty Auto-Complete List”

## Verification
- Outlook opens without errors.
- Emails sync correctly.
- Search works.
- No missing folders or mailboxes.

## Notes
If issues persist:
- Check for corrupted OST file
- Disable faulty add-ins
- Repair Office installation

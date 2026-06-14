# Fix SharePoint Access Issues

## Purpose
To resolve problems where users cannot access SharePoint sites, document libraries, or shared files.

## Symptoms
- “Access Denied”
- “You need permission to access this site”
- User cannot open shared files
- SharePoint site not loading
- Missing document libraries
- 404 or 403 errors
- Files open read‑only

## Steps

### 1. Confirm the User Has a Valid License
In Microsoft 365 Admin Center:
1. Go to **Users → Active users**
2. Select the user
3. Ensure they have a license that includes:
   - SharePoint Online
   - OneDrive
   - Office apps (optional)

### 2. Check SharePoint Site Permissions
1. Go to the SharePoint site
2. Click **Settings → Site permissions**
3. Check if the user is:
   - A site member
   - A site owner
   - In a SharePoint group with access

If missing → add them.

### 3. Check Document Library Permissions
Sometimes the site is accessible but a specific library is restricted:
1. Open the library
2. Click **Settings → Library settings**
3. Check **Permissions for this document library**
4. Ensure inheritance is enabled OR add the user manually

### 4. Check File/Folder Permissions
If only one file/folder is blocked:
1. Select the file/folder
2. Click **Manage access**
3. Add the user with:
   - View
   - Edit
   - Full control (if needed)

### 5. Check Sharing Settings
If the user is external:
1. Go to SharePoint Admin Center
2. Open **Policies → Sharing**
3. Ensure external sharing is allowed for:
   - The tenant
   - The specific site

### 6. Check Conditional Access Policies
If access works on one device but not another:
- Device may be blocked by Conditional Access
- Check Entra ID → **Protection → Conditional Access**

Common restrictions:
- Require compliant device
- Block legacy authentication
- Block unmanaged devices

### 7. Check if the Site Is a Private Microsoft 365 Group
If the site is linked to a private M365 Group:
- User must be added to the **Group**, not just SharePoint

Steps:
1. Go to **Teams & groups → Active teams & groups**
2. Find the group
3. Add the user as a **member**

### 8. Check for Deleted or Moved Files
If files are missing:
- Check **Recycle bin**
- Check **Second‑stage recycle bin**
- Check **Version history**

### 9. Check Sync Issues (If Using OneDrive Sync)
If the user is syncing the library:
- Reset OneDrive (see onedrive-sync-issues.md)
- Ensure they have permission to the library

### 10. Check Site Collection Admin Permissions
If you cannot change permissions:
- You may need to be a **Site Collection Administrator**
- Add yourself via SharePoint Admin Center

## Verification
- User can access the SharePoint site
- Files open normally
- No “Access Denied” errors
- Permissions are correct
- Sync works (if applicable)

## Notes
If access still fails:
- Check if the site is part of a retention policy
- Check if the user is blocked by DLP
- Check if the site is archived or locked

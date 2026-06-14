# Fix Microsoft 365 License Issues

## Purpose
To resolve problems where users cannot access Microsoft 365 apps or services due to missing, incorrect, or misconfigured licenses.

## Symptoms
- “You don’t have a license to use this product”
- Office apps show “Unlicensed product”
- Teams not available
- OneDrive not syncing
- SharePoint access denied
- Outlook not connecting
- User cannot sign in to Office apps

## Steps

### 1. Check the User’s License in Admin Center
1. Go to https://admin.microsoft.com
2. Navigate to **Users → Active users**
3. Select the affected user
4. Click **Licenses and apps**

Verify:
- A valid license is assigned (Business/Enterprise)
- Required services are enabled (Exchange, SharePoint, Teams, OneDrive)

### 2. Reassign or Fix the License
If the license is missing:
- Assign the correct license

If the wrong license is assigned:
- Remove the incorrect one
- Add the correct one

If services are disabled:
- Expand the license
- Enable required apps (Exchange, Teams, SharePoint, etc.)

### 3. Wait for License Propagation
Most changes apply within:
- 1–5 minutes for cloud apps
- 30 minutes for Exchange/Teams
- Up to 24 hours for full Office activation (rare)

### 4. Force Office to Refresh Licensing
On the user’s device:
1. Open any Office app
2. Go to **File → Account**
3. Click **Sign out**
4. Close the app
5. Reopen and sign in again

### 5. Check Sign‑In Logs (If License Looks Correct)
Go to:
https://entra.microsoft.com → **Users → Sign‑in logs**

Look for:
- Conditional Access blocks
- Device compliance issues
- Authentication failures

### 6. Check for Duplicate Accounts
Common issue:
- User has two accounts with similar usernames
- Signs into the wrong one

Confirm the user signs in with:
- Correct UPN (email address)
- Correct tenant

### 7. Check Subscription Status
In Admin Center:
1. Go to **Billing → Your products**
2. Ensure:
   - Subscription is active
   - No payment issues
   - No expired licenses

### 8. Check for Service Plan Conflicts
Some licenses conflict with each other.

Example:
- Assigning both Business Premium and E3 can cause issues

Fix:
- Remove one of the overlapping licenses

### 9. Check for Disabled Services in PowerShell (Advanced)
Run:

Get-MsolUser -UserPrincipalName user@domain.com | Select DisplayName,Licenses

Check if service plans are disabled.

### 10. Reinstall Office (If Apps Still Show Unlicensed)
1. Uninstall Office
2. Restart device
3. Reinstall from:
   https://portal.office.com

## Verification
- User can access all licensed apps
- Office activates successfully
- Teams, OneDrive, SharePoint work
- No “Unlicensed product” messages

## Notes
If licensing issues persist:
- Check if the user is synced from on‑prem AD (hybrid)
- Check if the account is soft‑deleted or restored
- Check if the user is in a restricted group or policy

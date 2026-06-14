# Reset MFA for a User (Microsoft 365 Admin)

## Purpose
To reset a user’s Multi‑Factor Authentication (MFA) settings when they lose access to their authenticator app, phone, or cannot complete MFA prompts.

## Symptoms
- User cannot sign in due to MFA prompt
- Lost or replaced phone
- Authenticator app not working
- Stuck on MFA setup loop
- “Approve sign‑in request” but no device available

## Steps

### 1. Go to Entra ID Admin Center
https://entra.microsoft.com

### 2. Navigate to the User
1. Go to **Users → All Users**
2. Search for the affected user
3. Click their name

### 3. Reset MFA
1. On the left menu, select **Authentication methods**
2. Click **Require re‑register MFA**
3. Confirm the reset

This forces the user to set up MFA again at next login.

### 4. Clear Old Authenticator App (Optional)
1. Go to **Authentication methods**
2. Remove:
   - Microsoft Authenticator
   - Phone numbers
   - Temporary access pass (if expired)

### 5. Provide Instructions to the User
Tell the user to:
1. Sign in at https://aka.ms/mfasetup
2. Add Microsoft Authenticator
3. Add backup phone number
4. Complete MFA registration

### 6. Use Temporary Access Pass (TAP) (If Needed)
If the user cannot complete MFA at all:
1. Go to **Authentication methods**
2. Click **Add authentication method**
3. Choose **Temporary Access Pass**
4. Set:
   - One‑time use or multi‑use
   - Expiry time
5. Give the TAP code to the user

They can now sign in without MFA and re‑register.

## Verification
- User signs in successfully
- MFA prompts work correctly
- Authenticator app is registered
- Backup methods are added

## Notes
If MFA keeps failing:
- Check Conditional Access policies
- Check if the user is blocked in Azure AD
- Check if the device is compliant (Intune)

# Reset a User's Password (Microsoft 365 Admin)

## Purpose
To reset a user’s password when they forget it, get locked out, or need a forced password change.

## Symptoms
- User cannot sign in
- “Incorrect password”
- Account locked due to failed attempts
- Password expired
- User forgot their password

## Steps

### 1. Go to Microsoft 365 Admin Center
https://admin.microsoft.com

### 2. Navigate to the User
1. Go to **Users → Active users**
2. Search for the affected user
3. Click their name

### 3. Reset the Password
1. Click **Reset password**
2. Choose:
   - Auto‑generate password  
   - Or enter a custom password
3. Tick **Require this user to change their password when they first sign in**
4. Click **Reset password**

### 4. Provide the New Password to the User
- Share it securely (Teams chat, phone call, or in person)
- Never send passwords over email

### 5. Check for Account Lockout
If the user still cannot sign in:
1. Go to **Account → Sign‑in logs**
2. Look for:
   - MFA failures
   - Conditional Access blocks
   - Location/device restrictions

### 6. Check if the Account Is Blocked
1. In the user’s profile, go to **Account**
2. Ensure **Block sign‑in** is set to **No**

### 7. Reset MFA (If Needed)
If the user is stuck on MFA:
- Perform an MFA reset (see reset‑mfa.md)

### 8. Check Password Policies
If the user keeps getting locked out:
- Check Azure AD Smart Lockout settings
- Check if the password is being autofilled incorrectly on a device

## Verification
- User signs in successfully
- MFA prompts work (if enabled)
- No lockouts or repeated failures
- Password change completes

## Notes
If password resets keep failing:
- Check Conditional Access policies
- Check if the account is compromised
- Review sign‑in logs for suspicious activity

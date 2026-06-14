# Reset a User’s Password (Microsoft 365 Admin)

## Purpose
To reset a user’s password, unlock their account, resolve sign‑in issues, and verify authentication settings in Microsoft 365.

## Common Scenarios
- User forgot their password
- User locked out after too many attempts
- MFA not working
- Password expired
- Admin needs to force a password change
- Compromised account recovery

---

## 1. Reset a User’s Password (Admin Center)

### Steps
1. Go to **Microsoft 365 Admin Center**  
   https://admin.microsoft.com

2. Navigate to:  
   **Users → Active users**

3. Select the user

4. Click **Reset password**

5. Choose:
   - Auto‑generate password  
   - Create your own password  

6. Choose whether the user must change password at next sign‑in

7. Click **Reset password**

---

## 2. Unlock a User Account

If the user is locked out:

1. Go to the user’s profile  
2. Click **Account**  
3. Look for **Sign‑in blocked**  
4. Toggle **Unblock sign‑in**

---

## 3. Reset MFA (Multi‑Factor Authentication)

If the user cannot complete MFA:

1. Go to **Entra Admin Center**  
   https://entra.microsoft.com

2. Navigate to:  
   **Users → All users**

3. Select the user

4. Click **Authentication methods**

5. Click **Require re‑register MFA**

This forces the user to set up MFA again.

---

## 4. Check Password Expiration

If the user’s password expired:

1. Go to the user’s profile  
2. Click **Account**  
3. Check **Password expiration**  
4. Optionally set:
   - Password never expires

---

## 5. Check Conditional Access Blocks

If the user still cannot sign in:

1. Go to **Entra → Protection → Conditional Access**  
2. Check:
   - Location restrictions  
   - Device compliance  
   - App restrictions  
   - Sign‑in risk policies  

---

## 6. Check Sign‑In Logs

Go to:
**Entra → Monitoring → Sign‑in logs**

Look for:
- Incorrect password
- MFA failure
- Conditional Access block
- Risky sign‑in
- Legacy authentication attempt

---

## 7. Compromised Account Recovery

If suspicious activity is detected:

1. Reset password  
2. Reset MFA  
3. Sign‑out everywhere:
   - Entra → User → **Revoke sessions**

4. Check:
   - Forwarding rules  
   - Inbox rules  
   - Delegation  
   - Sign‑in logs  

---

## Verification
- User can sign in successfully
- MFA works normally
- No Conditional Access blocks
- No lockouts or expired password errors
- Sign‑in logs show successful authentication

---

## Notes
If issues persist:
- Check if the user is blocked from signing in
- Check device compliance in Intune
- Check if the account is disabled
- Microsoft Support can review deep authentication logs

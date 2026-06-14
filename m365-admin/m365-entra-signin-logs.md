# Use Entra ID Sign‑In Logs (Microsoft 365)

## Purpose
To investigate authentication issues, failed logins, MFA problems, Conditional Access blocks, and suspicious sign‑ins using Entra ID (Azure AD) sign‑in logs.

## Common Scenarios
- User cannot sign in
- MFA keeps prompting or failing
- Conditional Access blocking access
- Sign‑in from unusual location
- Password spray or brute‑force attack
- Legacy authentication attempts
- App‑specific login failures

---

## 1. Open Entra ID Sign‑In Logs

Go to:
https://entra.microsoft.com

Then:
1. **Identity**
2. **Monitoring**
3. **Sign‑in logs**

You will see:
- Successful sign‑ins
- Failed sign‑ins
- Conditional Access results
- MFA details
- Device information
- IP address and location

---

## 2. Filter by User

At the top:
- Click **Add filter**
- Choose **User**
- Enter the username

Useful for:
- Login failures
- MFA issues
- Device compliance problems

---

## 3. Key Fields to Check

### **Status**
- Success
- Failure
- Interrupted

### **Failure Reason**
Examples:
- “Invalid username or password”
- “MFA required”
- “Conditional Access policy blocked access”
- “Device not compliant”
- “User password expired”

### **Client App**
Shows:
- Browser
- Mobile app
- Legacy protocol (IMAP/POP/SMTP)

### **Location**
Check for:
- Impossible travel
- Unknown countries
- VPN locations

### **IP Address**
Useful for:
- Security investigations
- Identifying compromised accounts

### **Conditional Access**
Shows:
- Which policy applied
- Whether access was blocked or granted

---

## 4. Investigating Common Issues

### Issue: User Cannot Sign In
Check:
- Failure reason
- Password expired
- Account locked
- Incorrect username
- Conditional Access block

### Issue: MFA Not Working
Look for:
- “MFA required”
- “Authentication failed”
- Device not registered
- Reset MFA (see reset‑mfa.md)

### Issue: Conditional Access Blocking Access
Check:
- Which policy applied
- Device compliance
- Location restrictions
- App restrictions

### Issue: Suspicious Sign‑Ins
Look for:
- Impossible travel
- Unknown IPs
- Legacy authentication attempts
- Multiple failures followed by success

### Issue: Legacy Authentication Attempts
If you see:
- IMAP
- POP
- SMTP
- ActiveSync

These should be disabled for security.

---

## 5. Export Logs (Advanced)
Admins can export logs to:
- CSV
- Log Analytics
- Sentinel
- Power BI

Useful for:
- Security investigations
- Audit reports
- Long‑term monitoring

---

## 6. Risky Sign‑Ins
Go to:
**Identity → Protection → Risky sign‑ins**

Shows:
- Compromised accounts
- Leaked credentials
- Unusual behaviour

---

## Verification
- User can sign in successfully
- MFA works normally
- No Conditional Access blocks
- No suspicious sign‑ins
- Logs show expected behaviour

---

## Notes
If sign‑in issues persist:
- Check device compliance in Intune
- Check password expiration policies
- Check if user is blocked from signing in
- Review risky user alerts
- Microsoft Support can analyse deep authentication logs

# Fix Data Loss Prevention (DLP) Issues in Microsoft 365

## Purpose
To troubleshoot and resolve issues where DLP policies block emails, files, or actions unexpectedly — or fail to trigger when they should.

## Common Scenarios
- Emails blocked due to sensitive info
- Attachments removed or quarantined
- Users cannot send external emails
- SharePoint/OneDrive file sharing blocked
- DLP policy not triggering
- False positives or false negatives
- DLP tips not showing in Outlook

---

## 1. Check DLP Policy Status

Go to:
https://compliance.microsoft.com → **Data loss prevention**

Check:
- Policy is enabled
- Correct locations selected:
  - Exchange
  - SharePoint
  - OneDrive
  - Teams
- No conflicting policies

---

## 2. Check Policy Conditions

Common triggers:
- Credit card numbers
- Passport numbers
- National ID
- Bank details
- Sensitive keywords
- Custom sensitive info types

If policy is too strict:
- Lower the sensitivity
- Add exclusions
- Modify thresholds

---

## 3. Check Policy Actions

DLP can:
- Block email
- Block sharing
- Encrypt email
- Restrict access
- Show policy tips
- Audit only

Verify the action matches the intended behaviour.

---

## 4. Check Policy Priority

Policies run **top to bottom**.

If a higher‑priority policy blocks something:
- Lower‑priority policies won’t apply

Reorder policies if needed.

---

## 5. Check User Notifications (Policy Tips)

If users don’t see DLP warnings:
- Ensure **Policy Tips** are enabled
- Check Outlook version (older versions may not support tips)
- Check if policy is set to “Test mode with notifications”

---

## 6. Check Exchange Transport Rules

Transport rules may override DLP.

Go to:
**Exchange Admin Center → Mail flow → Rules**

Look for:
- Block external emails
- Restrict attachments
- Encryption rules
- DLP override rules

---

## 7. Check SharePoint/OneDrive Sharing Settings

If file sharing is blocked:
- Check site‑level sharing settings
- Check tenant‑level sharing restrictions
- Check sensitivity labels applied to the file

---

## 8. Check Sensitivity Labels

Sensitivity labels can override DLP.

Examples:
- “Confidential” label blocks external sharing
- “Highly Confidential” blocks downloads

Check:
https://compliance.microsoft.com → **Information protection**

---

## 9. Check Activity Explorer

To see what DLP is blocking:
1. Go to **Compliance Center**
2. Open **Activity Explorer**
3. Filter by:
   - DLP events
   - Blocked actions
   - Policy matches

---

## 10. Troubleshooting False Positives

If DLP blocks harmless content:
- Add keyword exclusions
- Add domain exclusions
- Adjust confidence levels
- Modify sensitive info types

---

## 11. Troubleshooting False Negatives

If DLP fails to trigger:
- Ensure correct locations are selected
- Ensure policy is enabled
- Check if content is encrypted
- Check if content is in an unsupported format
- Increase confidence levels

---

## 12. Testing DLP Policies

Use test data:
- Fake credit card numbers (e.g., 4111 1111 1111 1111)
- Dummy national ID formats
- Custom keywords

Send test emails or upload test files.

---

## Verification
- DLP triggers correctly
- No unexpected blocks
- Policy tips show for users
- Emails/files behave as expected
- No false positives or negatives

---

## Notes
If DLP still behaves incorrectly:
- Check for policy sync delays (up to 30 minutes)
- Check for conflicting sensitivity labels
- Check for Conditional Access restrictions
- Microsoft Support can review DLP match logs

# Run a Message Trace (Microsoft 365)

## Purpose
To track the delivery status of an email, identify why it failed, and determine where it was routed within Microsoft 365.

## Common Uses
- Email not received
- Email stuck or delayed
- Email marked as spam
- Email quarantined
- Email bounced
- Need to confirm delivery

## Steps

### 1. Open Exchange Admin Center
https://admin.exchange.microsoft.com

### 2. Navigate to Message Trace
1. Go to **Mail flow**
2. Click **Message trace**

### 3. Choose the Time Range
Options:
- Last 24 hours (fastest)
- Last 48 hours
- Custom range (up to 10 days)

For older traces:
- Use **Downloadable reports** (up to 90 days)

### 4. Enter Search Criteria
You can search by:
- Sender email
- Recipient email
- Message ID
- Date/time range

### 5. Run the Trace
Click **Search**.

### 6. Review the Results
Common statuses:

- **Delivered**  
  Email reached the mailbox successfully.

- **Failed**  
  Email bounced. Check error details.

- **Quarantined**  
  Email flagged by security filters.

- **Filtered as spam**  
  Delivered to Junk folder.

- **Expanded**  
  Sent to a distribution list.

- **Pending**  
  Still processing.

### 7. Open Message Details
Click the message to view:
- Message events
- SMTP response codes
- Routing path
- Security actions (ATP, anti‑spam, anti‑malware)

### 8. Download the Full Report (Optional)
For deeper analysis:
- Click **Export**
- Choose CSV format
- Review detailed event logs

### 9. Check Quarantine (If Needed)
Go to:
https://security.microsoft.com/quarantine

Search for the message and release it if safe.

### 10. Check Transport Rules
If the message was blocked or redirected:
1. Go to **Mail flow → Rules**
2. Look for rules affecting the sender or recipient

## Verification
- Message status is identified
- Delivery path is understood
- Issue is resolved (delivered, released, or sender notified)

## Notes
If messages are consistently failing:
- Check SPF, DKIM, DMARC
- Check anti‑spam policies
- Check transport rules
- Review sender reputation

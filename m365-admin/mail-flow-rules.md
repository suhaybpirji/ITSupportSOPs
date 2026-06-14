# Manage Mail Flow Rules (Transport Rules) in Exchange Online

## Purpose
To create, modify, and troubleshoot mail flow rules (also known as transport rules) that control how emails are routed, filtered, or modified in Microsoft 365.

## Common Uses
- Block or allow specific senders
- Add disclaimers to emails
- Redirect emails to another mailbox
- Apply DLP or sensitivity rules
- Bypass spam filtering
- Auto‑forward emails
- Tag emails with headers
- Quarantine suspicious messages

## Steps

### 1. Open Exchange Admin Center
https://admin.exchange.microsoft.com

### 2. Navigate to Mail Flow Rules
1. Go to **Mail flow**
2. Click **Rules**

You will see all existing transport rules.

### 3. Create a New Rule
1. Click **Add a rule**
2. Choose a template (optional)
3. Configure:
   - **Conditions** (what triggers the rule)
   - **Actions** (what the rule does)
   - **Exceptions** (when not to apply it)

Examples:
- Block emails from a domain  
- Redirect emails to a shared mailbox  
- Add a disclaimer to all outbound mail  

### 4. Set Rule Priority
Rules run **top to bottom**.

To change priority:
- Select the rule
- Click **Move up** or **Move down**

Important:
- Higher priority = runs earlier
- Conflicting rules may override each other

### 5. Enable or Disable a Rule
Toggle the rule ON or OFF using the switch next to its name.

### 6. Test the Rule
Send a test email that matches the rule conditions.

Check:
- Message trace
- Headers
- Delivery status

### 7. Edit an Existing Rule
1. Select the rule
2. Click **Edit**
3. Modify conditions, actions, or exceptions

### 8. Common Rule Examples

#### Block a Sender or Domain
Condition:  
- Sender domain is: example.com  
Action:  
- Reject message with explanation

#### Redirect Emails
Condition:  
- Recipient is: user@domain.com  
Action:  
- Redirect to: sharedmailbox@domain.com

#### Add Disclaimer
Action:  
- Apply disclaimer  
- Insert text or HTML

#### Bypass Spam Filtering
Condition:  
- Sender IP or domain  
Action:  
- Set spam confidence level (SCL) to -1

#### Auto‑Forwarding Control
Block external forwarding:
- Condition: Recipient is outside the organization  
- Action: Block message

### 9. Troubleshooting Mail Flow Rules

#### Rule Not Applying
- Check rule priority
- Check conditions and exceptions
- Check if rule is enabled
- Check message trace for rule hits

#### Conflicting Rules
- A later rule may override an earlier one
- Reorder rules to fix

#### Rule Applies Incorrectly
- Add exceptions
- Narrow the conditions

### 10. Check Message Trace for Rule Hits
In message trace:
- Open the message
- Look for **Applied transport rules**
- Shows which rules triggered

## Verification
- Rule triggers correctly
- Emails route as expected
- No unintended side effects
- Message trace confirms rule hits

## Notes
If rules still don’t work:
- Check if the tenant uses **Exchange Hybrid**
- On‑prem rules may override cloud rules
- Check for DLP or security policies interfering

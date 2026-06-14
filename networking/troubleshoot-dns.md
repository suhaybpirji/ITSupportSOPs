# Troubleshoot DNS Issues

## Purpose
To diagnose and resolve DNS-related problems that prevent users or devices from accessing network resources or the internet.

## Symptoms
- Cannot access websites
- Cannot resolve domain names
- Slow logins
- Cannot join domain
- “DNS server not responding” errors

## Steps

### 1. Check IP and DNS Configuration
1. Open Command Prompt.
2. Run:
   ipconfig /all
3. Verify:
   - Correct IP address
   - DNS server points to domain controller (internal DNS)

### 2. Test DNS Resolution
Run:
nslookup google.com
nslookup domain.local

If nslookup fails → DNS server issue.

### 3. Flush and Reset DNS Cache
Run:
ipconfig /flushdns
ipconfig /registerdns
net stop dnscache
net start dnscache

### 4. Test Connectivity to DNS Server
Run:
ping <DNS server IP>
If no reply → network issue.

### 5. Check DNS Server Health
On the DNS server:
- Open DNS Manager
- Check Forward Lookup Zones
- Check Reverse Lookup Zones
- Ensure no red X or warning icons

### 6. Restart DNS Service (Server-side)
Run:
Restart-Service DNS

### 7. Check Event Viewer
Look for DNS-related errors under:
Applications and Services Logs → DNS Server

## Verification
- nslookup resolves internal and external names
- Websites load normally
- Domain services work correctly

## Notes
Most DNS issues come from:
- Wrong DNS server configured
- DNS service stopped
- Network connectivity problems

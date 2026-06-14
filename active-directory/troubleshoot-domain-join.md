# Troubleshoot Domain Join Issues

## Purpose
To diagnose and resolve issues preventing a Windows PC from joining the Active Directory domain.

## Common Causes
- Incorrect DNS settings
- Network connectivity issues
- Time/date mismatch
- Incorrect domain name
- Firewall blocking domain traffic
- Domain controller unreachable

## Steps

### 1. Check DNS Settings
1. Open Command Prompt.
2. Run: ipconfig /all
3. Ensure DNS points to the domain controller (e.g., 192.168.1.10).

### 2. Test Connectivity
1. Ping the domain controller:
   ping dc01.company.local
2. Ping the domain name:
   ping company.local

### 3. Check Time Sync
1. Ensure the PC time is within 5 minutes of the domain controller.
2. Run:
   w32tm /resync

### 4. Verify Domain Name
Ensure you are using the correct FQDN:
- company.local  
- not company.com (common mistake)

### 5. Check Firewall
Ensure ports required for domain join are open:
- TCP/UDP 88 (Kerberos)
- TCP/UDP 389 (LDAP)
- TCP 445 (SMB)

### 6. Try Joining Again
1. Go to System → About → Domain join.
2. Enter domain name.
3. Enter domain admin credentials.

## Verification
- PC appears in the correct OU.
- User can log in with domain credentials.
- No errors in Event Viewer → System.

## Notes
If the computer object already exists in AD, delete it before retrying the join.

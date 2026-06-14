# Check Active Directory Replication

## Purpose
To verify that domain controllers are replicating correctly and that no AD replication issues exist.

## Steps

### 1. Use Command Line Tools
1. Open Command Prompt as Administrator.
2. Run:
   repadmin /replsummary
   - Shows overall replication health.

3. Run:
   repadmin /showrepl
   - Shows inbound/outbound replication per DC.

4. Run:
   dcdiag /test:replications
   - Performs replication diagnostics.

### 2. Check Event Viewer
1. Open Event Viewer on each domain controller.
2. Navigate to:
   Applications and Services Logs → Directory Service
3. Look for replication-related warnings or errors:
   - Event ID 1311
   - Event ID 1865
   - Event ID 2042

### 3. Validate DNS Health
1. Run:
   dcdiag /test:dns
2. Ensure all DNS records exist:
   - _ldap._tcp
   - _kerberos._tcp
   - GC records (if applicable)

### 4. Force Replication (if needed)
1. Open Active Directory Sites and Services.
2. Expand Sites → Servers → NTDS Settings.
3. Right-click a connection → Replicate Now.

## Verification
- No errors in repadmin output.
- No replication-related errors in Event Viewer.
- Replication completes successfully when forced.

## Notes
Replication issues often come from:
- DNS misconfiguration
- Network connectivity problems
- Offline domain controllers

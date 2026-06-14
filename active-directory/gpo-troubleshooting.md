# Group Policy Troubleshooting

## Purpose
To diagnose and resolve issues where Group Policy Objects (GPOs) are not applying correctly to users or computers.

## Steps

### 1. Run GPResult
1. Open Command Prompt as Administrator.
2. Run:
   gpresult /r
   - Shows applied GPOs for the logged-in user and computer.

3. For a full HTML report:
   gpresult /h c:\gporeport.html

### 2. Check Event Viewer
1. Open Event Viewer.
2. Navigate to:
   Applications and Services Logs → Microsoft → Windows → GroupPolicy → Operational
3. Look for:
   - Permission issues
   - GPO not found
   - Slow link detection

### 3. Validate Network Connectivity
Ensure the PC can reach:
- Domain controllers
- SYSVOL share
- NETLOGON share

Test using:
- \\domain.local\SYSVOL
- \\domain.local\NETLOGON

### 4. Check GPO Scope
Verify:
- The GPO is linked to the correct OU.
- The user/computer is inside that OU.
- Security filtering includes the correct groups.
- WMI filters (if used) match the device.

### 5. Force Group Policy Update
Run:
gpupdate /force

Restart if prompted.

### 6. Check SYSVOL Replication
If GPOs differ between DCs:
- Check DFSR health
- Run:
  dfsrdiag replicationstate

## Verification
- gpresult shows the expected GPOs applied.
- No GPO errors in Event Viewer.
- Settings take effect on the machine.

## Notes
Most GPO issues come from:
- Wrong OU placement
- Missing permissions
- SYSVOL replication problems

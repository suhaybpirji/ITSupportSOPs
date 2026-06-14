# Troubleshoot VPN Connectivity Issues

## Purpose
To diagnose and resolve issues preventing users from connecting to the company VPN.

## Symptoms
- “Unable to connect”
- “Authentication failed”
- “No response from server”
- Connected but no access to internal resources
- Split tunneling not working

## Steps

### 1. Check Internet Connectivity
1. Ensure the user has a stable internet connection.
2. Run:
   ping 8.8.8.8
3. If no reply → fix internet first.

### 2. Verify VPN Credentials
- Ensure username/password are correct.
- Check if MFA is required.
- Confirm the account is not locked out.

### 3. Check VPN Server Reachability
Run:
ping <VPN server IP>
If unreachable → network or firewall issue.

### 4. Restart VPN Adapter
1. Open Network Connections.
2. Right-click the VPN adapter → Disable.
3. Enable it again.

### 5. Flush DNS
Run:
ipconfig /flushdns

### 6. Reset Network Stack
Run:
netsh winsock reset
netsh int ip reset
Restart PC.

### 7. Check Firewall or Antivirus
- Ensure VPN client is allowed.
- Some AV tools block VPN tunnels.

### 8. Check Routing (Split Tunnel)
Run:
route print
Ensure internal subnets route through VPN.

### 9. Reinstall VPN Client (if needed)
- Uninstall the VPN client.
- Reboot.
- Install the latest version.

## Verification
- User can connect to VPN.
- Internal resources (file shares, intranet) are accessible.
- No authentication errors.

## Notes
Frequent VPN issues come from:
- Incorrect DNS
- Outdated VPN client
- Firewall blocking ports
- Account lockouts

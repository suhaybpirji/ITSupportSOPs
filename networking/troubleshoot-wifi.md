# Troubleshoot Wi-Fi Connectivity Issues

## Purpose
To diagnose and resolve issues preventing users from connecting to Wi-Fi networks or experiencing unstable wireless connections.

## Symptoms
- Cannot connect to Wi-Fi
- “Connected, no internet”
- Frequent disconnections
- Slow speeds
- Limited connectivity

## Steps

### 1. Check Basic Connectivity
1. Ensure Wi-Fi is turned on.
2. Toggle Airplane Mode on/off.
3. Restart the device.

### 2. Forget and Reconnect to the Network
1. Open Wi-Fi settings.
2. Select the network → Forget.
3. Reconnect and enter the password again.

### 3. Check Signal Strength
- Move closer to the access point.
- Avoid walls, metal objects, or interference.

### 4. Test Internet Access
Run:
ping 8.8.8.8
ping google.com

If IP works but domain fails → DNS issue.

### 5. Reset Network Adapter
Run:
netsh winsock reset
netsh int ip reset
Restart PC.

### 6. Update Wireless Drivers
1. Open Device Manager.
2. Expand Network Adapters.
3. Right-click Wi-Fi adapter → Update driver.

### 7. Check Router/Access Point
- Ensure the SSID is broadcasting.
- Check if MAC filtering is enabled.
- Restart the router/AP.

### 8. Check DHCP
Run:
ipconfig /renew
If no IP is assigned → DHCP issue.

### 9. Check for Interference
Common sources:
- Microwave ovens
- Bluetooth devices
- Neighbouring Wi-Fi networks
- Cordless phones

## Verification
- Device connects to Wi-Fi successfully.
- Internet access is stable.
- No packet loss or dropouts.

## Notes
If multiple users are affected, escalate to network team to check access point or controller.

# Fix "Printer Offline" Issues

## Purpose
To resolve issues where a network or local printer shows as “Offline” and cannot print.

## Symptoms
- Printer shows “Offline”
- Jobs stuck in queue
- Users cannot print
- Printer unreachable over network

## Steps

### 1. Check Physical Printer Status
- Ensure the printer is powered on.
- Check display panel for errors (paper jam, low toner, etc.).
- Ensure network cable or Wi-Fi is connected.

### 2. Restart the Print Spooler
Run:
net stop spooler
net start spooler

Or via Services:
1. Open services.msc
2. Find “Print Spooler”
3. Restart it

### 3. Clear Print Queue
1. Open:
   C:\Windows\System32\spool\PRINTERS
2. Delete all files inside.
3. Restart the spooler again.

### 4. Ping the Printer
Run:
ping <printer IP>

If no reply → network issue.

### 5. Check Printer IP Address
- Ensure the printer’s IP hasn’t changed.
- If DHCP is used, set a reservation.

### 6. Reinstall the Printer
1. Remove the printer from Devices & Printers.
2. Add it again using:
   \\printserver\printername

### 7. Check Print Server
On the print server:
- Ensure the printer is online.
- Restart the printer queue.
- Check Event Viewer for print errors.

### 8. Update Printer Drivers
- Install the latest driver from the manufacturer.
- Avoid universal drivers unless required.

## Verification
- Printer shows “Ready”
- Test page prints successfully
- No jobs stuck in queue

## Notes
If multiple users report the same issue, the print server or printer hardware is likely the cause.

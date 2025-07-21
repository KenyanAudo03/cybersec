# Chapter 2: Windows Basics

## Commands Practiced

- `ipconfig` – Show IP address and network details  
- `tasklist` – List running processes  
- `net user` – View and manage user accounts  
- PowerShell – Ran basic commands and scripts  
- Event Viewer – Reviewed system/application logs  

## Practice Summary

### ✔️ Checked System Info and Network Settings
- Used `ipconfig` to get IP, gateway, and DNS info.
- Checked active interfaces and connection status.

### ✔️ Process and User Management
- Ran `tasklist` to view active processes.
- Used `net user` to view accounts and test creating a local user.

### ✔️ PowerShell Basics
- Ran simple PowerShell commands like `Get-Process` and `Get-Service`.
- Practiced filtering output and stopping services.

### ✔️ Log Inspection with Event Viewer
- Navigated to System and Application logs.
- Filtered events by type (Error, Warning) and time.

## Example Commands Used

```cmd
ipconfig /all
tasklist | findstr chrome
net user testuser /add
powershell Get-Service | Where-Object {$_.Status -eq "Running"}
```

## Notes

- `ipconfig /all` is quick and reliable for network info.
- Event Viewer takes a bit of practice but is very useful for troubleshooting.
- PowerShell is a solid tool for system tasks and scripting once you get comfortable with the syntax.

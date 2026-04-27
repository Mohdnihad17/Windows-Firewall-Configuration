
# Windows Firewall Configuration
## Objective
Configure Windows Firewall to block inbound traffic on Telnet (port 23), verify the block using PowerShell, and then disable the rule.

## Tools Used

- Operating System: Windows 11
- Firewall Tool: Windows Defender Firewall with Advanced Security (`wf.msc`)
- Testing Utility: PowerShell (`Test-NetConnection`)

## Steps, Commands, and Screenshots

| Step | Description | Command / Action | Screenshot |
|------|-------------|------------------|------------|
| 1 | Viewed existing inbound rules | Opened `wf.msc` and reviewed inbound rules | ![Step 1](screenshots/Screenshot%202025-05-30%20112626.png) |
| 2 | Created inbound rule to block TCP port 23 | Rule Name: `Block Telnet Port 23 (Task-4)` | ![Step 2](screenshots/Screenshot%202025-05-30%20112955.png) |
| 3 | Tested rule using PowerShell | `Test-NetConnection -ComputerName 127.0.0.1 -Port 23` | ![Step 3](screenshots/Screenshot%202025-05-30%20113227.png) |
| 4 | Disabled the firewall rule | Disabled the rule via firewall interface | ![Step 4](screenshots/Screenshot%202025-05-30%20113446.png) |

## PowerShell Test Result

| Property         | Value         |
|------------------|---------------|
| ComputerName     | 127.0.0.1     |
| RemoteAddress    | 127.0.0.1     |
| RemotePort       | 23            |
| InterfaceAlias   | Ethernet      |
| SourceAddress    | 127.0.0.1     |
| TcpTestSucceeded | False         |

> The above result confirms that the connection to Telnet (port 23) was successfully blocked by the firewall rule.

**Mohammed Nihad I**  
**Royal College of Engineering and Technology**

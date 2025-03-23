# Windows Server Project for Multi-Branch Company

## Project Overview

This project simulates the setup of a multi-branch company infrastructure using Windows Server 2022. The company, CLOUD.LOCAL, operates in four locations: Maadi (Main Branch), Qena, Alexandria, and Ismailia. The infrastructure involves configuring domain controllers, web/FTP servers, group policies, and remote desktop access.


## Company Overview
CLOUD.LOCAL company has 4 branches in Egypt:
- **Maadi** (Primary Domain Controller)
- **Qena** (Read Only Domain Controller)
- **Alexandria** (Web & FTP Server)
- **Ismailia** (Child Domain Controller)

## Project Configuration

### 1. **Maadi (Primary Domain Controller)**
- **Active Directory Domain Services Role:** Installed and configured.
- **Group Policy Configuration:** Created Organizational Units (OUs) and user accounts.
- **WDS Configuration:** Configured for deployment.

### 2. **Qena (RODC Domain Controller)**
- **Read-Only Domain Controller:** Configured and delegated access for a user (marco) who has no privileges to add or edit OUs or users.

### 3. **Alexandria (Web & FTP Server)**
- **Web Servers:** Published `web1` on HTTP and `web2` on HTTPS. 
- **FTP Server:** Configured FTP server and provided user `mohamed` with FTP access.

### 4. **Group Policies**
- **Finance Team:** Applied policy to restrict removable device connections.
- **HR & Sales Teams:** Set specific wallpaper as a policy.

### 5. **Ismailia (Child Domain Controller)**
- **Remote Access:** User `fady` can access the primary domain server remotely.
- **DNS and User Creation:** Secondary DNS configured and user `ola` can log in to any device.

## Conclusion
This project demonstrates the setup and management of a multi-branch infrastructure using Windows Server 2022, including domain controllers, web/FTP servers, and group policies.

## Requirements
- Windows Server 2022 
- Basic knowledge of Active Directory, DNS, and Group Policies

## Setup Instructions
1. Follow the steps in the configuration section to set up the server roles.
2. Use PowerShell or Server Manager to configure services like WDS, Active Directory, and Group Policies.
3. For more detailed configurations, refer to the setup guidelines in the respective sections.
   
## Download Windows Server 2022 ISO
You can download the Windows Server 2022 ISO from the official Microsoft website here:
[Windows Server 2022 ISO Download](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022)

## Thank You
For further questions or contributions, feel free to reach out.


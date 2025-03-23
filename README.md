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
- Install & Deployment Active Directory Domain Service Role and Basic configuration
![Maadi PDC 1](https://github.com/user-attachments/assets/cedfaa47-6be8-4030-8048-14948843fee2)
- Create OUs and Ueres
![creating OUs and users](https://github.com/user-attachments/assets/1c4e969e-3f90-4b8a-978d-03a63518d385)
- WDS configuration on Maadi server (Primary Domain Controller)
![WDS configuration ](https://github.com/user-attachments/assets/884888e0-9052-4b58-969f-79200cab1f72)

### 2. **Qena (RODC Domain Controller)**
- **Read-Only Domain Controller:** Configured and delegated access for a user (marco) who has no privileges to add or edit OUs or users.
- Configure Qena’s Server as a RODC and set user (marco) is a delegated user
![Qena is RODC Server](https://github.com/user-attachments/assets/55a03afd-488d-49f0-9653-f76160c1440b)
- marco have no privileges to add or edit any OUs or users
![marco is delegated user on RODC](https://github.com/user-attachments/assets/99a1f73f-dcf4-4f2d-a971-f861720b6ac0)

### 3. **Alexandria (Web & FTP Server)**
- **Web Servers:** Published `web1` on HTTP and `web2` on HTTPS. 
- **FTP Server:** Configured FTP server and provided user `mohamed` with FTP access.
- Publish web1 on HTTP
And web2 on HTTPS
![http website publishing and https on standalone server ](https://github.com/user-attachments/assets/e715a704-ea9c-4839-bab0-8417775a0c10)
- access http (web1) from any device in domain
![access http (web1) from any device in domain](https://github.com/user-attachments/assets/a8483c90-a53c-42a1-9aad-485188f25158)
- access https (web2) from any device in domain
![access https (web2) from any device in domain](https://github.com/user-attachments/assets/d0898819-daa1-4c71-926f-a2e230446364)
- FTP server publishing
![ftp server publishing ](https://github.com/user-attachments/assets/c0e6cbc9-4a56-451b-bea4-79b5688959af)
- give permission to user mohamed access ftp from file browser
![give permission to mina access ftp](https://github.com/user-attachments/assets/2f9927c4-1acb-472b-9082-ac019d7fcb6f)

### 4. **Group Policies**
- **Finance Team:** Applied policy to restrict removable device connections.
- **HR & Sales Teams:** Set specific wallpaper as a policy.
- Applying Group Policy on finance team to ristrict them of connect removable device
![Applying Group Policy on finance team to ristrict them of connect removable device](https://github.com/user-attachments/assets/5bacc3da-b483-4c57-b170-b308c03de9fe)
- testing the policy applied on finance team
![testing the policy applied on finance team](https://github.com/user-attachments/assets/aef55cd7-12b1-4427-8151-a1c5d8474e56)
- Applying Group Policy on HR team to set speceific wallpaper
![Applying Group Policy on HR team to select speceific wallpaper](https://github.com/user-attachments/assets/f3b96381-baf5-4034-a30e-890ea5243c42)
- Applying Group Policy on Sales team to set specific wallpaper
![Applying Group Policy on Sales team to select speceific wallpaper](https://github.com/user-attachments/assets/0b8075d6-d328-45f1-a679-3b442bd138fa)
- Add user fady to remote desktop users group
![add user fady to remote desktop users group](https://github.com/user-attachments/assets/5c7c24a5-4ce4-45a8-b227-7bf7a7040bc2)
- User fady have access the primary domain server remotly
![user fady have access the primary domain server remotly](https://github.com/user-attachments/assets/721c40c1-c793-4696-9056-49471fb6cbe3)

### 5. **Ismailia (Child Domain Controller)**
- **Remote Access:** User `fady` can access the primary domain server remotely.
- **DNS and User Creation:** Secondary DNS configured and user `ola` can log in to any device.
![Ismailia is Child domain controller](https://github.com/user-attachments/assets/357d0524-48b7-4673-97f9-ea7709d4a0fa)
- secondry DNS in ismailia branch
![secondry DNS in ismailia branch](https://github.com/user-attachments/assets/a1a6a365-303e-4744-bda0-a8ea06d4db82)
- User ola created on ismailia (child domain) can log into any device
![user ola created on ismailia (child domain) can log into any device ](https://github.com/user-attachments/assets/5b986925-0c66-4a02-8621-489cf18050ea)

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


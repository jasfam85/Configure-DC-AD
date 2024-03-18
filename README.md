<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 11 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Created Virtual Machines:
  - Windows 11
  - Windows 2022 
- Installed Server Roles:
  - Active Directory Domain Services
  - DNS Services
- Joined to Domain:
  - Added DC-1 to newly created domain
  - Added Windows 11 to newly created domain 
- Configured RDP
  - Added users to Remote Desktop Settings
    - Made sure both end users were able to log in thru RDP
- Powershell Script
  - Ran script to add random end users to "_Employees" OU in Active Directory  

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://github.com/jasfam85/Configure-DC-AD/assets/163485424/86340432-c4e0-4f8d-981b-ecf7ae3ef20e" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Log into Azure and created the DC-1 and Windows11DC Virtual Machines
</p>
<br />

<p>
<img src="https://github.com/jasfam85/Configure-DC-AD/assets/163485424/cd22fad5-0b96-4030-b787-412f9b622f03" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://github.com/jasfam85/Configure-DC-AD/assets/163485424/38533ee6-7dcb-4fc9-ba25-e21e01f19856" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
Under Server Manager, I installed the following roles: Active Directory Domain Services, and DNS services. 
</p>
<br />

<p>
<img src="https://github.com/jasfam85/Configure-DC-AD/assets/163485424/9cac5425-8b1b-400b-a6e1-6d2869592874" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Join DC to the newly promoted Domain
<p>

<p>
<img src="https://github.com/jasfam85/Configure-DC-AD/assets/163485424/65ee46a6-7feb-42bb-88c3-e7d727e1bc5b" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Created OU's under Active Directory Users and Computers
<p>

<p>
<img src="https://github.com/jasfam85/Configure-DC-AD/assets/163485424/61bb54c4-af0e-4fdf-a12f-4f4c4f242f80" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
While Windows11DC is restarting it is stored in the default Computers OU
</p>
<img src="https://github.com/jasfam85/Configure-DC-AD/assets/163485424/d3c284c0-af11-4031-9331-87ab3e6c59eb" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://github.com/jasfam85/Configure-DC-AD/assets/163485424/6b5b399a-1f07-4686-84e4-91f64a9b65e3" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
Moved Windows11DC to "_Endpoints" OU (CREATED BEFORE COMPUTER WAS RESTARTED). Windows11DC is Successfully Joined to SlothWorld.com
<p>

<p>
<img src="https://github.com/jasfam85/Configure-DC-AD/assets/163485424/d2046e25-8ad4-4cc8-86ff-37b46646a59a" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://github.com/jasfam85/Configure-DC-AD/assets/163485424/176d19ca-5645-4def-8647-4bf249556ebb" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://github.com/jasfam85/Configure-DC-AD/assets/163485424/dfdcbd18-949c-40ab-99d2-662ebb9cd8fd" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
Ran Powershell ISE. Added random endpoint users to "_Employees" OU. Made sure I was able to log into their accounts. After adding them to RDP under the client Remote Desktop Settings. 
<p>

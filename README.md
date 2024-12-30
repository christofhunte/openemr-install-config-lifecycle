<p align="center">
<img src="https://i.imgur.com/MWiItN1.png" height="50%" width="50%" alt="Microsoft Active Directory Logo"/>
</p>

<h1>EMR System Deployed and ran in the Cloud (Azure)</h1>
This project outlines the istallation, configuration and usage of the OpenEMR software within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (22H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Setup Domain Controller and Client-1 in Azure
- Install Active Directory
- Create a Domain Admin user within the domain
- Join Client-1 to your domain (mydomain.com)
- Setup Remote Desktop for non-administrative users on Client-1
- Create a bunch of additional users and attempt to log into client-1 with one of the users
- Dealing with Account Lockouts
- Enabling and Disabling Accounts
- Observing Logs


<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/Z6rVp93.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The first step I did was creating a Resource Group in Azure and titled it "Active-Directory-Lab".
</p>
<br />

<p>
<img src="https://i.imgur.com/cRjq0oK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The next step I did was creating a virtual network and subnet for the virtual machines to run on. I placed the virtual network in the the Resource Group I created.
</p>
<br />

<p>
<img src="https://i.imgur.com/R3cztcO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/7JuFful.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/UtjTLIv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I then created a virtual machine for the domain controller and titled it "dc-1". I set its operating system to Windows Server 2022 with the username "chlabuser". I also set it's size to 2 vcpus with a 16 GiB memory to be certain the server can handle all that I will be doing going forward.
</p>
<br />

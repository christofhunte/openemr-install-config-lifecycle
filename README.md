<p align="center">
<img src="https://i.imgur.com/MWiItN1.png" height="50%" width="50%" alt="Microsoft Active Directory Logo"/>
</p>

<h1>EMR System Deployed and ran in the Cloud (Azure)</h1>
This project outlines the istallation, configuration and usage of OpenEMR software within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop (Microsoft Remote Desktop)
- PowerShell
- OpenEMR

<h2>Operating Systems Used </h2>

- Windows 10 (22H2)

<h2>List of Prerequisites</h2>

- Apache
- XAMPP
- PHP
- MySQL
- OpenEMR Directory


<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/NTrh00g.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/MqftraI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/xNRhNlv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. First I created a Windows 10 Virtual Machine within Azure to deploy OpenEMR on. I placed it within a new Resource Group and also created a new Virtual Network.
</p>
<br />

<p>
<img src="https://i.imgur.com/fEY9Raw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/s6eeJd4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/PoOobZ3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
2. I copied the public IP Address from the Virtual Machine and pasted into Remote Desktop (Microsoft Remote Desktop). I then logged into the server with the username and password I created for the VM.
</p>
<br />

<p>
<img src="https://i.imgur.com/XmvGdgI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/jGN6kd4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3. I ran a ping in PowerShell using the private IP Address for the virtual machine just test the connectivity of the network.
</p>
<br />

<p>
<img src="https://i.imgur.com/YB5eCuZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/1wyTKny.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/hknoyOW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
4. I downloaded the prerequisites in order for the OpenEMR software to run. I downloaded XAMMP Installer from the Apache website as well as the OpenEMR archive. The XAMPP contains Apache, MySQL and PHP which will be needed OpenEMR to run.
</p>

<p>
<img src="https://i.imgur.com/ZuzI0Pr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/fq2qbdD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/4VRFvxW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
5. I then installed XAMMP software onto the server with the components of MySQL, PHP, and Apache as well as others not necassarily needed for this project but I installed anyway. 
</p>
<br />

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
2. I copied the public IP Address from the Virtual Machine and pasted it into Remote Desktop (Microsoft Remote Desktop). I then logged into the server with the username and password I created for the VM.
</p>
<br />

<p>
<img src="https://i.imgur.com/XmvGdgI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/jGN6kd4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3. I ran a ping in PowerShell using the private IP Address for the virtual machine just to test the connectivity of the network.
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

<p>
<img src="https://i.imgur.com/4KCCXAz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/1NqGMuB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
6. Windows Defender Firewall blocked me from running MySQL and Apache so I had to allow access for them to run. Once I did that Apache and MySQL started running in the server.
</p>
<br />

<p>
<img src="https://i.imgur.com/XFhWf89.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/XTFzqjT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Z32Lf3F.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/cCkjUp4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
7. I copied and pasted the recommended PHP script from OpenEMR's website and pasted it into the Apache PHP code on the XAMPP Control Panel.
</p>
<br />

<p>
<img src="https://i.imgur.com/x5HV1cZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/u2TPVil.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
8. I stopped and started back up Apache after saving the updated PHP script.
</p>
<br />

<p>
<img src="https://i.imgur.com/eIZFHh6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/BymB1bQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/vfEKcic.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
9. I extracted all of the contents from the "openemr-7.02" zip into the "htdocs" directory within the "XAMMP" folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/RucXfM7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/LbeZnrq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
10. I changed the name of the directory from "openemr-7.02" to just "openemr". (I actually had a bit of trouble at this point because I forgot to do this step. The webserver for OpenEMR gave me a 404 error so I started toubleshooting and eventually realized that I had to change the directory name. It was a great learning experience particularly for troubleshooting.)
</p>
<br />

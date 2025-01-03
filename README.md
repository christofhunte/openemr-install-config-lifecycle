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
<img src="https://i.imgur.com/s6eeJd4.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/PoOobZ3.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
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
<img src="https://i.imgur.com/YB5eCuZ.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/1wyTKny.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/hknoyOW.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
</p>
<p>
4. I downloaded the prerequisites in order for the OpenEMR software to run. I downloaded XAMMP Installer from the Apache website as well as the OpenEMR archive. The XAMPP contains Apache, MySQL and PHP which will be needed OpenEMR to run.
</p>

<p>
<img src="https://i.imgur.com/ZuzI0Pr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/fq2qbdD.png" height="35%" width="35%" alt="Disk Sanitization Steps"/>
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

<p>
<img src="https://i.imgur.com/li4aWfX.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/LL5TNb2.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/osXfbLR.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/fw907kA.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/dKdUtS0.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/fRabtKM.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/df0ILXA.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
11. I finished installation in the web-broswer. After going to the installation script "http://localhost/openemr", I ensured the file and directory permissions were correct. Then I proceeded to step 1 and selected to create a database in setup. Then on the next page I confirmed the MySQL Server Details and filled out the OpenEMR Initial User Details. After creating database and first user I configured PHP, and then configured the Apache web server. After selecting a dark theme, "OpenEMR" was successfully installed. 
</p>
<br />

<p>
<img src="https://i.imgur.com/W2p7m6H.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/KfOjGiE.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/G8cKsVI.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
12. Once "OpenEMR" was installed I started exploring the system. First logged in with the credentials I created in the preious step. Next I went to the "Facilities" tab and created the name "Hunte Healthcare Center".
</p>
<br />

<p>
<img src="https://i.imgur.com/swgcO5f.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/jTadUNp.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
13. I started browsing the User/Groups tab and examined the features and what I can edit. I used my own user account that was already created as reference. I kept my access control set to "Administrators".
</p>
<br />

<p>
<img src="https://i.imgur.com/YSB6J6k.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/tAJYIxT.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
14. I created new users. One named "Jane Doe" and the other named "John Doe". I set their acces control to both "Physicians". 
</p>
<br />

<p>
<img src="https://i.imgur.com/gdegTco.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/zpbwzBA.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/FoIe9l1.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/SjHBgPv.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
15. I navigated to the "Search or Add Patient" section and created a new patient titled "Karen Doe". I filled in relevant parameters such as "Provider" and "Care Team".
</p>
<br />

<p>
<img src="https://i.imgur.com/X3LbOWs.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/dDGtpet.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/3UPupf1.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
16. After the patient was created I added a "Medical Problem"  of "Dry Eye" to simulate updating a patients medical records. 
</p>
<br />

<p>
<img src="https://i.imgur.com/7Hn6rzz.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
17. I explored to the "Patient Finder" section and found "Karen Doe". This would be where Physicians would go to look up patients.
</p>
<br />

<p>
<img src="https://i.imgur.com/nRlFezg.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/MzSrFe3.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
18. I navigated to the "Messages, Reminders, Recalls" section to simulate setting a reminder to "Jane Dough" as "Christof Hunte" who is an administrator about an appointment for "Karen Doe's" test the next day. I also sent a regular message as well.
</p>
<br />

<p>
<img src="https://i.imgur.com/YhiovYB.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/B5OlJQy.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/FdQl8nN.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/3xOgMfO.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/EThIXKp.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
19. I just started browsing other tabs such as "Pharmacies", "Fees", "Procedures" etc.
</p>
<br />

<p>
<img src="https://i.imgur.com/X3LbOWs.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/dDGtpet.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/3UPupf1.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
20. Finally I logged into the "OpenEMR" as "Jane Doe" to view the layout as a Physician instead of an admin. I just explored different tabs such as the "Messages, Reminders, Recalls" etc. After this the project of deploying an EMR system in an Azure Virtual Machine was successful.
</p>
<br />


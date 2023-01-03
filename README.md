<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Install/Enable IIS in Windows
- Install Web Platform Installer
- Install osTicket
- Assign Permissions
- Install HeidiSQL

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/i95EjYV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The first step should be to enable IIS by going into your control panel, which can be accessed by tapping the Windows key then typing control panel, click programs, then programs and features, and finally click on "Turn Windows features on or off" and check off the box beside "Internet Information Services" then click "OK".
</p>
<br />

<p>
<img src="https://i.imgur.com/2g33bmq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
-Install "Web Platform Installer"

-Open after installation

-Add MySQL 5.5

-Add ALL simple versions of x86 PHP up until version 7.3
</p>
<br />

<p>
<img src="https://i.imgur.com/1oO5XV2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
-Download OsTicket from the web

-Extract and copy "upload" folder to C:\inetpup\wwwroot

-Within C:\inetpup\wwwroot, rename "upload" to OsTicket
</p>
<br />

<p>
<img src="https://i.imgur.com/Z4pMizH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Reload IIS (Open IIS, Stop and Start the server)

-Go to sites -> Default -> osTicket

-On the right, click “Browse *:80”

</p>
<br />

<p>
<img src="https://i.imgur.com/HpmM0Ay.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enable Extensions in IIS: Note that some extensions are not enabled
-Go back to IIS, sites -> Default -> osTicket
-Double-click PHP Manager
-Click “Enable or disable an extension”
  -Enable: php_imap.dll
  -Enable: php_intl.dll
  -Enable: php_opcache.dll

</p>
<br />

<p>
<img src="https://i.imgur.com/hZuzvUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Refresh the osTicket site in your browse, observe the changes

</p>
<br />

<p>
<img src="https://i.imgur.com/hZuzvUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Rename:
	From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

</p>
<br />

<p>
<img src="https://i.imgur.com/OxUSPtR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Assign Permissions: ost-config.php
  -Disable inheritance -> Remove All
  -New Permissions -> Everyone -> All

</p>
<br />

<p>
<img src="https://i.imgur.com/prYNXjd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continue Setting up osTicket in the browser (click Continue)
  -Name Helpdesk
  -Default email (receives email from customers)

</p>
<br />

<p>
<img src="https://i.imgur.com/paW91Ol.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and Install HeidiSQL (download from web)
  -Create a new session, root/Password1
  -Connect to the session
  -Create a database called “osTicket”

</p>
<br />

<p>
<img src="https://i.imgur.com/wppjKAx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continue Setting up OsTicket in the browser
  -MySQL Database: osTicket
  -MySQL Username: root
  -MySQL Password: Password1

</p>
<br />
!! Congratulations, if all steps were followed correctly you should have successfully installed and setup osTicket !!

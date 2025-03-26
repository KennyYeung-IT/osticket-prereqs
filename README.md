# osticket-prereqs
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


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a Windows 10 virtual machine with 4 virtual CPUs and connect to it via RDP (Remote Desktop Protocol). Once logged in enable IIS (Internet Information Service) through control panel and windows features. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, extract and download the necessary files for the osticketing system via https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD. Then locate and install the PHP manager first. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the (osTicket-installation-Files) install the Rewrite Module and create the directory C:\PHP.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Unzip the PHP 7.3.8 "php-7.3.8-nts-Win32-VC15-x86.zip" from the (OsTicket-Installation-Files) into the 'C:\PHP' folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the "osTicket-Installation-Files" folder install VC_redist.x86.exe and MySQL 5.5.62 (mysql-5.5.62-win32.msi) Launch Configuration Wizard after install and create a username and password. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS as an Admin and register PHP within IIS. Reload ISS 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install osTicket v1.15.8 from (osTicket-Installation-Files), unzip "osTicket-V1.15.8.zip" and copy the 'upload' folder into the web server "c:\inetpub\wwwroot" within wwwroot rename upload folder to osticket.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Return to IIS Manager and restart the server. Then enable PHP Manager extensions php_imap.dll, php_intl.dll, and  php_opcache.dll.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Rename ost-config-php from "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php" to "C:\inetpub\wwwroot\osTicket\include\ost-config.php" and assign permissions to ost-config-php through Disable inheritance -> Remove All and New Permissions -> Everyone -> All. 
</p>
<br />
Install HeidiSQL and create a new session with a username and passsword. connect to sesstion and create a database called "osticket"

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Complete installation by registering users and emails. The osTicket can now be reached by users on http://localhost/osTicket/scp/login.php and end users can be simulated through http://localhost/osTicket/. 
</p>
<br />

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

![image](https://github.com/user-attachments/assets/0bd979a1-440b-4917-9174-6754127f6911)
![image](https://github.com/user-attachments/assets/63b475a0-2844-4551-9c09-babc2c12ae30)

<p>
Create a Windows 10 virtual machine with 4 virtual CPUs and connect to it via RDP (Remote Desktop Protocol). Once logged in enable IIS (Internet Information Service) through control panel and windows features. 
</p>
<br />

![image](https://github.com/user-attachments/assets/8bfb0df7-b74b-4e85-a6a0-e23c5b1b3590)
![image](https://github.com/user-attachments/assets/cfc82166-329c-4add-a8e0-b8ece06b45ee)

<p>
Next, extract and download the necessary files for the osticketing system via https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD. Then locate and install the PHP manager first. 
</p>
<br />

![image](https://github.com/user-attachments/assets/16730c26-a42e-45b9-9a98-daea64cfcd2a)


<p>
Install and enable IIS in Windows with CGI through control panel, then uninstall or change a program, and turn Windows features on and off. 
</p>

![image](https://github.com/user-attachments/assets/ac193280-98bf-4782-a03d-271e6d389702)

<p>
Install PHP manager for the IIS from the (osTicket-Installation-Files).
</p>


![image](https://github.com/user-attachments/assets/8a2e733b-a305-4b68-a92e-5e21d71e1d8e)
![image](https://github.com/user-attachments/assets/5316bc8e-ebf9-413b-883f-f5d4498dcc17)


<p>
From the (osTicket-installation-Files) install the Rewrite Module and create the directory C:\PHP.
</p>
<br />

![image](https://github.com/user-attachments/assets/2ad5490d-f4fe-4a02-acae-b0b2dc223221)

<p>
Unzip the PHP 7.3.8 "php-7.3.8-nts-Win32-VC15-x86.zip" from the (OsTicket-Installation-Files) into the 'C:\PHP' folder.
</p>
<br />

![image](https://github.com/user-attachments/assets/a89082e8-fe8e-4f1b-8b18-c443f28bdc5f)
![image](https://github.com/user-attachments/assets/aaff3219-17a5-4ce1-a082-2529ce69f806)


<p>
From the "osTicket-Installation-Files" folder install VC_redist.x86.exe and MySQL 5.5.62 (mysql-5.5.62-win32.msi) Launch Configuration Wizard after install and create a username and password. 
</p>
<br />

![image](https://github.com/user-attachments/assets/b655f53a-d935-4bf5-a05c-382456718303)
![image](https://github.com/user-attachments/assets/9b5c8de1-03fd-405d-81e8-b69638091fe1)
![image](https://github.com/user-attachments/assets/74646add-39b7-4be3-a45f-782b70598d36)

<p>
Open IIS as an Admin and register PHP within IIS. Reload ISS 
</p>
<br />

![image](https://github.com/user-attachments/assets/1b734500-7c2a-43f4-8470-9a0495854ece)

<p>
Install osTicket v1.15.8 from (osTicket-Installation-Files), unzip "osTicket-V1.15.8.zip" and copy the 'upload' folder into the web server "c:\inetpub\wwwroot" within wwwroot rename upload folder to osticket.
</p>
<br />


![image](https://github.com/user-attachments/assets/74646add-39b7-4be3-a45f-782b70598d36)
![image](https://github.com/user-attachments/assets/21fd4ab8-7426-4f13-b5da-a010abe85717)
![image](https://github.com/user-attachments/assets/3045bd53-4f9b-4e26-a05b-61b9a60cd796)

<p>
Return to IIS Manager and restart the server. Then enable PHP Manager extensions php_imap.dll, php_intl.dll, and  php_opcache.dll.
</p>
<br />

![image](https://github.com/user-attachments/assets/109bfa9a-9282-4d55-b25a-84b93d236502)
![image](https://github.com/user-attachments/assets/e6a470fc-f3b3-42f4-9423-4735bb2d0085)
![image](https://github.com/user-attachments/assets/7747968d-97f3-489c-9ae0-bdb0b31fa2f7)


<p>
Rename ost-config-php from "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php" to "C:\inetpub\wwwroot\osTicket\include\ost-config.php" and assign permissions to ost-config-php through Disable inheritance -> Remove All and New Permissions -> Everyone -> All. 
</p>

![image](https://github.com/user-attachments/assets/494e3176-f689-48d6-9eb2-04699148b6b7)

<p>
Setup osTicket in browser.
</p>

![image](https://github.com/user-attachments/assets/a72dd44d-7550-44bc-94b7-6f0a305746ef)
![image](https://github.com/user-attachments/assets/454e042d-733f-427b-a8f7-0a0712f6c87d)
![image](https://github.com/user-attachments/assets/7c70361c-96cf-4fc5-ab95-6260ac13c009)

<br />
Install HeidiSQL and create a new session with the username and passsword. connect to sesstion and create a database called "osTicket" Log in with the admin account and the osTicket system should be running. 



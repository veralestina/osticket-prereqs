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

<h2>Installation Steps to create osTicket</h2>

- Create a Resource Group in Azure as RG.
- Create a Virtual Machine in Azure as VM-osTicket.
- Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs. Allow the VM to create a new Virtual Network, VNet.

<p>
<img src="https://github.com/veralestina/Images/blob/main/Github%20information/vmipaddress.png" height="50%" width="50%" alt="VM"/>
</p>


- Enable IIS in Windows with CGI

<p>
<img src="https://github.com/veralestina/Images/blob/main/Github%20information/iiscgi.png" height="30%" width="30%" alt="IIS with CGI"/>
</p>

- Download and install PHP Manager for IIS
- Download and install Rewrite Module
- Create the directoy C:\PHP
- Download and install PHP 7.3.8
- Download and install VC_redist.x86.exe.
- Download and install MySQL 5.5.62, click typical setup, then launch Configuration Wizar after successful install, click Standard Configuration, enter password.
- Open IIS as an Admin
- Register PHP from within IIS
- Reload IIS
- Go to sites, Default, oTicket and on the right, click Browse*.80
- On osTicket, will notice that some red X's on certain extensions. See image below.

<p>
<img src="https://github.com/veralestina/Images/blob/main/Github%20information/notcompleteosticket.png" height="40%" width="40%" alt="Notcompletleyworkingosticketsite"/>
</p>

- This means that not all extensions on site have been enabled, so go back to IIS, sites, Default, osTicket, double-click PHP Manager, clikc Enable or disable an etension; Enable: php_imap.dll, php_intl.dll, php_opcache.dll.
- Refresh the osTicket site to observe the newly enabled extensions.

<p>
<img src="https://github.com/veralestina/Images/blob/main/Github%20information/completeosticket.png" height="40%" width="40%" alt="workingosticketsite"/>
</p>

- Rename C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php
- For ost-config.php; Disable inheritance, Remove All. New Permissions, change to Everyone and All.
- Go back to osTicket in browser and name Helpdesk and set a default email - this email will receive the email from customers placing a ticket.
-Downlad and install HeidiSQL. Open HeidiSQL. Create a new session, use root as username and create a password. Connect to the session. Create a new database called osTicket.
- Back to osTicket in the browser; for MySQL Database: osTicket, MySQL Username: root, MYSQL Password: password. Click the Install Now button.
- Go to help desk login page https://localhost/osTicket/scp/login.php
- The end users osTicket url is http://localhost/osTicket/
- Delete: C:\inetpub\wwwroot\osTicket\setup
- Set Permissions to Read Only: only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

And the Prerequisites and Installations for the creation of OSTicket have been completed.



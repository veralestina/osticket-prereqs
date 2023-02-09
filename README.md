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

- Create a Virtual Machine in Azure - create a Resource Group first
- Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs. Allow the VM to create a new Virtual Network, VNet.
- Enable IIS in Windows with CGI
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
- Not all extensions on site are enabled so go back to IIS, sites, Default, osTicket, double-click PHP Manager, clikc Enable or disable an etension; Enable: php_imap.dll, php_intl.dll, php_opcache.dll.
- Refresh the osTicket site to observe the newly enabled extensions.
- Rename C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php
- For ost-config.php; Disable inheritance, Remove All. New Permissions, change to Everyone and All.
- Go back to osTicket in browser and name Helpdesk and set a default email - this email will receive the email from customers placing a ticket.
-Downlad and install HeidiSQL. Open HeidiSQL. Create a new session, use root as username and create a password. Connect to the session. Create a new database called osTicket.
- Back to osTicket in the browser; for MySQL Database: osTicket, MySQL Username: root, MYSQL Password: password. Click the Install Now button.
- Go to help desk login page https://localhost/osTicket/scp/login.php
- The end users osTicket url is http://localhost/osTicket/
- Delete: C:\inetpub\wwwroot\osTicket\setup
- Set Permissions to Read Only: only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

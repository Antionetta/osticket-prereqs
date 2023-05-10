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

- Create a resource group in Microsoft Azure.
- Create a Virtual Machines with Windows 10 OS( maken sure when creating the VM to allow the VM to creant a new Virtual Network)
- Download the following files: https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/ZnFXjkQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Under Control Panel -> Programs -> Turn Windows Features on or off ->
World Wide Web Services -> Application Development Features -> [X] CGI

</p>
<br />

 
<p>
<img src="https://i.imgur.com/R4BBwir.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
</p>
<br />
<h3> Create Directory C:PHP
<p>
<img src="https://i.imgur.com/UUROlKI.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the Installation Files, download and install VC_redist.x86.exe
</p>
<br />

<p>
<img src="https://i.imgur.com/1VT6cAf.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the Installation Files, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
- Typical Setup ->
- Launch Configuration Wizard (after install) ->
- Standard Configuration ->
- Password1
</p>
<br />


<p>
<img src="https://i.imgur.com/BzPdQBq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS as an Admin

Register PHP from within IIS

Reload IIS (Open IIS, Stop and Start the server)

</p>
<br />
<img src="https://i.imgur.com/NZ5DTNd.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install osTicket v1.15.8
- Download osTicket from the Installation Files Folder
- Extract and copy “upload” folder to c:\inetpub\wwwroot
- Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
- Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />
<p>
<img src="https://i.imgur.com/XhMiji8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to sites -> Default -> osTicket

- On the right, click “Browse *:80”

</p>
<br />
<p>
<img src="https://i.imgur.com/J5tfzVE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h3>Note that some extensions are not enabled</h3>

- Go back to IIS, sites -> Default -> osTicket
- Double-click PHP Manager
- Click “Enable or disable an extension”
- Enable: php_imap.dll
- Enable: php_intl.dll
- Enable: php_opcache.dll
- Refresh the osTicket site in your browse, observe the changes
</p>
<br />
<p>
<img src="https://i.imgur.com/bt787N2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Rename: ost-config.php

From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

To: C:\inetpub\wwwroot\osTicket\include\ost-config.php


</p>
<p>
<h3>Assign Permissions: ost-config.php</h3>
Disable inheritance -> Remove All
New Permissions -> Everyone -> All

<p>
<img src="https://i.imgur.com/7bn7hhb.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h3>From the Installation Files, download and install HeidiSQL.</h3>
- Open Heidi SQL
- Create a new session, root/Password1
- Connect to the session
- Create a database called “osTicket”
</p>
<p>
<img src="https://i.imgur.com/MyJ4hoo.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h3>Continue Setting up osTicket in the browser (click Continue)</h3>
Name Helpdesk
Default email (receives email from customers)
- MySQL Database: osTicket
- MySQL Username: root
- MySQL Password: Password1
- Click “Install Now!”

</p>
<br />
<p>
<img src="https://i.imgur.com/7bn7hhb.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>

<h3>From the Installation Files, download and install HeidiSQL.</h3>
- Open Heidi SQL
- Create a new session, root/Password1
- Connect to the session
- Create a database called “osTicket”
</p>
<h3>Congratulations</h3>
Hopefully it is installed with no errors!
Browse to your help desk login page: http://localhost/osTicket/scp/login.php
<br />

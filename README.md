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
- Downlaod the following files: https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6


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

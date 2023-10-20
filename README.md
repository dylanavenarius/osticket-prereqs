<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used</h2>

- Windows 10 (21H2)

<h2>Overview</h2>

- Setup a Virtual Machine in Azure
- Install osTicket requirements
- Install osTicket itself

<h2>Installation Steps</h2>

<p>
<a href="https://ibb.co/6vzjLk7"><img src="https://i.ibb.co/q0KTVv3/step-1-create-VM.png" alt="step-1-create-VM" border="0" /></a>
</p>
<p>
In this step, we are creating a Windows 10 Virtual Machine in Azure with 2-4 virtual CPUs. When creating the VM, allow it to create a new Virtual Network. Wait for the resources to be fully deployed before moving on to step two.
</p>
<br />

<p>
<a href="https://ibb.co/y09rFqL"><img src="https://i.ibb.co/fMgsdHm/Install-IIS-on-VM.png" alt="Install-IIS-on-VM" border="0" /></a>
</p>
<p>
Next, using its Public IP Address, remote desktop into your newly created Virtual Machine and navigate to Programs and Features within the Control Panel and click "Turn Windows features on or off". From here we are going to install/ enable IIS or Internet Information Services and its supporting features: CGI, Common HTTP Features, IIS Management Console. Click "OK" after everything is selected and wait for IIS to be installed. IIS is a web server that osTicket runs on. After installation you can test if the web server is up and running by going to a web browser and tpying in 127.0.0.1, which should load the default IIS website. 
</p>
<br />

<p>
<a href="https://ibb.co/rcxrBXP"><img src="https://i.ibb.co/3MpZxPX/Screen-Shot-2023-10-19-at-3-55-02-PM.png" alt="Screen-Shot-2023-10-19-at-3-55-02-PM" border="0" /></a>
</p>
<p>
Lastly, we will be downloading and installing the necessary prerequisite software to allow us to successfully install and run osTicket on our Virtual Machine.
  
  - PHP Manager for IIS
  - Rewrite Module
  - PHP 7.3.8 "unzip contents into C:\PHP"
  - Microsoft Visual C++ Redistributable
  - MySQL
  - HeidiSQL
  - os Ticket v1.15.8
    
We will need to open IIS as an Admin and register PHP and reload IIS. Finally, once osTicket has been installed we will need to enable the following extenstions before creating a database and setting up an Admin user.
  
  - Enable: php_imap.dll
  - Enable: php_intl.dll
  - Enable: php_opcache.dll
    
</p>
<p>
<a href="https://ibb.co/CVZQxDd"><img src="https://i.ibb.co/3SqctQX/Screen-Shot-2023-10-19-at-3-57-47-PM.png" alt="Screen-Shot-2023-10-19-at-3-57-47-PM" border="0" /></a>
</p>
<br />

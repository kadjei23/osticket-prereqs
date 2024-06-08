<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial goes over the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- PHP Manager
- Rewrite Module
- PHP 7.3.8
- VC redist x86.exe.
- MySQL 5.5.62
- HeidiSQL
- osTicket

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/3tr7UXW.png" height="80%" width="80%" alt="RG-VM Creation"/>
</p>
<p>
First you want to go ahead and create a resource group that way you can put your virtual machine inside that.
<br /> [YouTube: Resource group and Vm creation in Azure.](https://youtu.be/iqZ9Vl3GcKc). Now after creating this we are ready to install the Prerequisites required to get osTicket up and running.

<p>
<img src="https://i.imgur.com/b024LVS.png" height="80%" width="80%" alt="Installation Files"/>
</p>
<p>
Getting started now we are going to be using all the prereqruisites above to make sure things run smoothly. Now that you have these we then go ahead and go to the control panel and type in IIS (Internet Information Services). By clicking that it will refer us to programs, then under programs and features we click turn windows feature on and off. That is going to open up a file named windows features, with that we find and check Internet Information Services, expand that same folder and expand the world wide web services. Open up application and development features and make sure we check CGI, after that's checked collapse that and expand common HTTP features and make sure all the folders under that are checked and and hit the okay button.
 <img src="https://i.imgur.com/cqX5UaO.png" height="80%" width="80%" alt="Check CGI"/> 
 <img src="https://i.imgur.com/79xAete.png" height="80%" width="80%" alt="HTTPS"/> 
 
  
  Doing this will install the web server that osTicket runs on. To confirm this works you can search 127.0.0.0 and this will bring you to the main IIS default page down below.
<img src="https://i.imgur.com/5pxwUyZ.png" height="80%" width="80%" alt="Check CGI"/>
  
  Next step is to download and install PHP 7.3.8


  <img src="https://i.imgur.com/3tr7UXW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 

  <img src="https://i.imgur.com/3tr7UXW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 

  <img src="https://i.imgur.com/3tr7UXW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 

  <img src="https://i.imgur.com/3tr7UXW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

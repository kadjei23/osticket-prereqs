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
<img src="https://i.imgur.com/WWnBfqZ.png" height="80%" width="80%" alt="Windows feature off"/> 
 <img src="https://i.imgur.com/cqX5UaO.png" height="80%" width="80%" alt="Check CGI"/> 
 <img src="https://i.imgur.com/79xAete.png" height="80%" width="80%" alt="HTTPS"/> 
 
  
  Doing this will install the web server that osTicket runs on. To confirm this works you can search 127.0.0.0 and this will bring you to the main IIS default page down below.
<img src="https://i.imgur.com/5pxwUyZ.png" height="80%" width="80%" alt="Check CGI"/>
  
  Next step is to download and install the PHP Manager for IIS.
 <img src="https://i.imgur.com/4dCReVf.png" height="80%" width="80%" alt="PHP Manager"/> 
 
Followed by installing the Rewrite Module.
 <img src="https://i.imgur.com/FLlTLlO.png" height="80%" width="80%" alt="Rewrite Module"/> 

 After completion install PHP 7.3.8 and unzip file to the directory C:\PHP

  <img src="https://i.imgur.com/UuPlOt3.png" height="80%" width="80%" alt="PHP 7.3.8"/> 

  <img src="https://i.imgur.com/H7zcvjF.png" height="80%" width="80%" alt="Directory"/> 

After that download and install VC redist x86.exe. and the mySQL 5.5.62
  <img src="https://i.imgur.com/U4ltR1z.png" height="80%" width="80%" alt="Redist"/> 
  <img src="https://i.imgur.com/lobEYlf.png" height="80%" width="80%" alt="mySQL 5.5.62"/>
 <img src="https://i.imgur.com/hyN4WkB.png" height="80%" width="80%" alt="Next"/>


After hitting next on mySQL installation we want to hit Typical setup type and install
<img src="https://i.imgur.com/GlnXka3.png" height="80%" width="80%" alt="Typical"/>

Launch mySQL and setup credential. Standard configuration>Install as Windows Service>Modify Securtiy settings>enter root password(Make sure the password is something memorable)>execute.
 <img src="https://i.imgur.com/yPRTE7X.png" height="80%" width="80%" alt="Standard config"/>
 <img src="https://i.imgur.com/aNVQjlv.png" height="80%" width="80%" alt="root"/>
 <img src="https://i.imgur.com/mQBI8eL.png" height="80%" width="80%" alt="execute"/>
 
 
 Next open and run IIS as an administrator and register PHP within IIS. Double click PHP Manager and register new PHP version

 
 <img src="https://i.imgur.com/sScTk5m.png" height="80%" width="80%" alt="PHP Manager"/>
 <img src="https://i.imgur.com/Okr3iW3.png" height="80%" width="80%" alt="PHP Setup"/>


 click 3 buttons on the right go to the PHP directory that was created then click php-cgi and open. Proceed to reload/restart IIS 
 <img src="https://i.imgur.com/RpPdseT.png" height="80%" width="80%" alt="PHP-CGI"/>
 <img src="https://i.imgur.com/OHM41YO.png" height="80%" width="80%" alt="Restart IIS"/>

 Next downlod and install osTicket then extract and copy the upload folder to c:\inetpub\wwwroot, within that rename upload to osTicket. Then restart the server again.
 <img src="https://i.imgur.com/Apxev2r.png" height="80%" width="80%" alt="Folder Copy"/>
 <img src="https://i.imgur.com/JZw5XTp.png" height="80%" width="80%" alt="rename"/>

 Next go to sites>default web site> osTicket. On the right hand side click Bowse.80 which brings you into the osTicket Setup page.
 <img src="https://i.imgur.com/7Ca8obX.png" height="80%" width="80%" alt="Browse.80"/>
 <img src="https://i.imgur.com/B8VzkKN.png" height="80%" width="80%" alt="osTicket setup"/>

 Some features may be marked with a red X once u come on the install page but ypu can easily go back to IIS>Default>osTicket and double click PHP manager and go to enable or disable extension. Enable php_imap.dll, php_intl.dll, php_opache.dll. Refresh osTicket installer in the browser and some features marked with a red x will be a green check.
 <img src="https://i.imgur.com/2d8Qmmm.png" height="80%" width="80%" alt="Enable Ext"/>
 <img src="https://i.imgur.com/7Ca8obX.png" height="80%" width="80%" alt="Ext. Enabled"/>
 <img src="https://i.imgur.com/GDgyZUk.png" height="80%" width="80%" alt="Refresh"/>

 Go back to wwwroot folder inside inetpub, click on osTicket>include and rename ost-sampleconfig.php to ost-config.php. Following that right click on it and head to properties>security>advanced>disable inheritance>remove all permissions.
 <img src="https://i.imgur.com/EK7nR6m.png" height="80%" width="80%" alt="Include"/>
 <img src="https://i.imgur.com/0JzFXGR.png" height="80%" width="80%" alt="Rename"/>
 <img src="https://i.imgur.com/yWBwZgA.png" height="80%" width="80%" alt="Disable"/>
 <img src="https://i.imgur.com/1V3i1vx.png" height="80%" width="80%" alt="Everyone"/>

 Then add Permissions and give everyone full control
 <img src="https://i.imgur.com/S4Q48ui.png" height="80%" width="80%" alt="Full control"/>

 Continue in browser with osTicket installation choose whichever name and password for Help desk and admin user
 <img src="https://i.imgur.com/OfwXNXn.png" height="80%" width="80%" alt="Name-setup"/>

 Install last prereqruisite Heidi SQL
 <img src="https://i.imgur.com/vney3BU.png" height="80%" width="80%" alt="HeidiSQL"/>
 
 
 
 
 
 
 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

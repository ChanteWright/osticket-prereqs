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

- Install / Enable IIS in Windows WITH
CGI and Common HTTP Features & AND IIS Management Console
- PHP Manager for IIS
- Rewrite Module
- PHP 7.3.8 
- VC_redist.x86.exe.
- MySQL 5.5.62

<h2>Installation Steps</h2>

<p>

![image](https://github.com/ChanteWright/osticket-prereqs/assets/138072479/43d0bf01-773a-41e3-8e0f-435ece7ff034)


</p>
<p>
Install / Enable IIS in Windows WITH
CGI and Common HTTP Features
World Wide Web Services -> Application Development Features ->
[X] CGI
[X] Common HTTP Features
AND IIS Management Console
Internet Information Services -> Web Management Tools -> IIS Management Console
	[X] IIS Management Console

</p>
<br />

<p>
  
![image](https://github.com/ChanteWright/osticket-prereqs/assets/138072479/c0d65430-0cad-4160-8826-34353a0621b5)

</p>
<p>
From the Downloads page select the installation package that is appropriate for your target machine. Download and run the installer, which will install and register PHP Manager's binaries with IIS. Note that only IIS versions 7.0 and above are supported. After installation is complete, launch the IIS Manager and find the "PHP Manager" feature

When opened, the "PHP Manager" feature provides a configuration overview for the PHP installation that is registered with IIS and is currently active. If no PHP is registered with IIS, then the only action that can be performed is the registation of a new PHP version.  

To register a new PHP version with IIS, first you need to download the zip archive with PHP binaries from http://windows.php.net/ and then extract the files from it into a folder of your choice. Note that you can also install PHP by using Web Platform Installer or the Windows installer from http://windows.php.net/ - the PHP Manager can be used to manage those PHP installations as well.

Click on "Register new PHP version" task and then provide the full path to the location of the main php executable file: php-cgi.exe:

http://www.phpmanager.xyz/latest/_images/register.png

After clicking OK the new PHP version will be registered with IIS and will become active. This means that all the sites on this IIS server by default will use this PHP version.
</p>
<br />

<p>
  
![image](https://github.com/ChanteWright/osticket-prereqs/assets/138072479/5f2ede2d-5b7a-47b7-bf1e-e6f68755baef)

![image](https://github.com/ChanteWright/osticket-prereqs/assets/138072479/374a05e8-c852-46c5-8bd8-4de8e9bcb0be)


</p>
<p>
Extract the PHP files:

Open the downloaded ZIP file.
Extract the contents to a directory of your choice, for example, C:\php.
Configure PHP:

Rename the php.ini-development file to php.ini.
Open php.ini with a text editor.
Make any necessary configuration changes. For example, you might want to enable extensions or adjust memory limits. Most of the default settings should work fine for a basic installation.
Update Environment Variables:

Open the Start menu and search for "Environment Variables" and click on "Edit the system environment variables."
In the "System Properties" window, click on the "Environment Variables" button.
In the "System Variables" section, scroll down and find the "Path" variable. Select it and click on "Edit."
Click on "New" and enter the path to your PHP installation directory (e.g., C:\php). Click "OK" to save the changes.
</p>
<br />

<p>

  ![image](https://github.com/ChanteWright/osticket-prereqs/assets/138072479/d4a435bc-6146-4d52-afa0-601149619fe2)

</p>
<p>
Download the VC_redist.x86.exe file:

Visit the Microsoft Download Center website: https://www.microsoft.com/en-us/download/details.aspx?id=48145
Click on the "Download" button to download the VC_redist.x86.exe file.
Run the installer:

Locate the downloaded VC_redist.x86.exe file.
Double-click on the file to run the installer.
Follow the installation wizard:

The installer will open and display the Microsoft Visual C++ Redistributable Setup window.
Click on the "Next" button to proceed.
Read and accept the license terms:

Read the license terms carefully.
If you agree to the terms, select the checkbox labeled "I have read and accept the license terms."
Click on the "Next" button to continue.
Choose the installation location:

By default, the installer will install the redistributable package in the recommended installation location.
If you want to change the installation location, click on the "Browse" button and choose a different directory.
Click on the "Next" button to proceed.
Start the installation:

Click on the "Install" button to begin the installation process.
Wait for the installation to complete:

The installer will extract and install the necessary files on your system.
The progress bar will indicate the installation progress.
Finish the installation:

Once the installation is complete, a confirmation message will appear.
Click on the "Finish" button to exit the installer.


<p>
  
![image](https://github.com/ChanteWright/osticket-prereqs/assets/138072479/e9b0ceb5-867b-4d3e-9212-d499dbe09d0f)

</p>
<p>
Download MySQL Installer:

Visit the MySQL website: https://dev.mysql.com/downloads/installer/
Scroll down to find the "MySQL Installer" section.
Click on the "Download" button to download the MySQL Installer.
Run the MySQL Installer:

Locate the downloaded MySQL Installer file (e.g., mysql-installer-web-community-x.x.x.x.msi).
Double-click on the file to run the installer.
Choose the installation type:

The MySQL Installer will open and display the Setup Type page.
Select "Custom" installation to have more control over the components to be installed.
Click on the "Next" button to proceed.
Select MySQL Server version:

On the Product Selection page, scroll down and find "MySQL Server" in the list of available products.
Select "MySQL Server 5.5.62" (or the closest available version) by clicking on the checkbox.
Click on the "Next" button to continue.
Choose the installation options:

On the Installation page, select the installation options according to your preferences.
You can choose the installation directory, configure the server type, set the port number, etc.
Ensure that the "MySQL Server" option is selected.
Click on the "Next" button to proceed.
Configure MySQL Server:

On the Accounts and Roles page, set the root password for the MySQL Server.
You can also create additional user accounts and configure their privileges.
Click on the "Next" button to continue.
Choose the MySQL Server configuration:

On the Windows Service page, select the service name and configure the startup type.
You can choose to run MySQL Server as a Windows service or not.
Click on the "Next" button to proceed.
Perform the installation:

On the Ready to Install page, review the installation summary and ensure that the selected components and settings are correct.
Click on the "Execute" button to start the installation process.
Wait for the installation to complete:

The installer will extract and install the MySQL Server files.
The progress bar will indicate the installation progress.
Finish the installation:

Once the installation is complete, the installer will display the Installation Complete page.
Click on the "Next" button and then click on the "Finish" button to exit the installer.
</p>
<br />


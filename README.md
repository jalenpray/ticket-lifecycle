<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle: Intake Through Resolution</h1>
This tutorial outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system osTicket.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>My List of Prerequisites</h2>

- Using Azure, we will create our virtual machine
- 

<h2>Installation Stages</h2>
- To start our project, we must create a virtual machine in Azure with Windows 11 Pro and 4 VCPUS.
<img width="1920" height="1008" alt="create VM" src="https://github.com/user-attachments/assets/395b4b67-e45b-4392-990c-261dc14f2b30" />

- Next we will start the Remote Desktop App on windows and enter in our public IP Address
- <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7efdc5e6-de22-4ae0-a7e2-6b19e9853bd0" />

We will enter our credentials
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e50743cd-eb4f-4781-b4db-656ec1912f8f" />

- once we are in our virtual machine, open Microsoft Edge, copy and paste this link:https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD and install it
- <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c0e2bbd5-da3c-4123-a8f9-978d16c691d7" />

Once the file folder is downlaoded, unzip it to your desktop amd extract the files from within the folder
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f3ca2d1d-9fd4-4a8c-aab9-69a1dc6e0e70" />

Click the windows icon, type in control panel, click turn windows features on and off, then check the (IIS) Internet Information Services box
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/882191d8-2da8-4458-8661-c6a788ad8a53" />

Scroll down and open world wide web, open Application Development Features and the the check box labeled "CGI"
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/807f1cd8-e7ed-409e-9416-1cd56add10a8" />

from the "osTicket-Installation-Files" folder install the PHP Manager for IIS. Say yes to everything to install it
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/31201544-6baa-4f6d-880c-808dc7f43654" />

From the “osTicket-Installation-Files” folder do the same thing and install the Rewrite Module
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ba5753ba-ccf1-4037-b463-1ed0146d6625" />

Open another File Explorer, go to the C Drive and make another folder called PHP. This will be the directory
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/126e2138-aa49-4f60-b535-9fa7aec27b8f" />

From the “osTicket-Installation-Files” folder, extract the files from the PHP 7.3.8 to the PHP folder
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/bfc51886-a35d-4887-9eb1-d1f964eccec4" />

From the “osTicket-Installation-Files” folder, install the VC_redist.x86.exe. file
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d95b125a-aa1c-423a-a52e-f746290f642a" />

From the “osTicket-Installation-Files” folder, install MySQL 5.5.62/Click Typical Setup -> Launch Configuration->Standard Configuration->enter the username and password which are both root
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d953526d-6c2e-4f40-937e-a9601881b8ef" />

Open IIS as Admin
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6569d5cf-9adf-48e8-b97d-70ee47c27bc4" />

Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0f1d061d-546a-4920-be1e-6d7ca34eb7fd" />

Reload IIS (Open IIS, Stop and Start the server)
<img width="1066" height="617" alt="image" src="https://github.com/user-attachments/assets/118ad7a0-b7fc-4adf-bae4-9f81356e4e1f" />

From the osTicket-Installation-Files folder, extract the osTicket-v1.15.8 folder
<img width="1440" height="900" alt="image" src="https://github.com/user-attachments/assets/4be05ac9-35ae-41d1-bd28-15f6c3883aeb" />

copy the “upload” folder into “c:\inetpub\wwwroot”
<img width="1440" height="900" alt="image" src="https://github.com/user-attachments/assets/9a29f8e1-dc62-4ec4-9b3e-846c9d493fb1" />
<img width="1440" height="900" alt="image" src="https://github.com/user-attachments/assets/c9e511bc-4796-4df0-a184-014fa5de7efd" />

Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
<img width="1440" height="900" alt="image" src="https://github.com/user-attachments/assets/191edbf3-da1a-4c26-a6ea-a7e8ccf947a9" />

Reload IIS again and Stop and Start the server (Open IIS, Stop and Start the server)
<img width="1440" height="860" alt="image" src="https://github.com/user-attachments/assets/99a8e33a-97e6-4f50-bdd5-1da54d63b817" />

Go to sites -> Default -> osTicket. On the right, click “Browse *:80”
<img width="1440" height="860" alt="image" src="https://github.com/user-attachments/assets/f4a6eefc-7112-4f51-a907-b5b3969cd500" />

Go back to IIS, sites -> Default -> osTicket
<img width="1440" height="860" alt="image" src="https://github.com/user-attachments/assets/f0756f62-b1e2-4689-b033-87d52fa07df4" />

Double-click PHP Manager
Click “Enable or disable an extension”
<img width="1440" height="860" alt="image" src="https://github.com/user-attachments/assets/77e3fadc-5240-4554-af1d-1a4bf142ccc4" />

Enable: php_imap.dll, Enable: php_intl.dll Enable: php_opcache.dll and after you are finished refresh your broswer
<img width="1440" height="860" alt="image" src="https://github.com/user-attachments/assets/2d6f4f8d-d857-4b3d-b820-b430f3784fc2" />

Go to the C Drive->inetpub->wwwroot->osTicket->include and look for the file ost-sampleconfig.php and rename it to ost-config.php
<img width="867" height="566" alt="image" src="https://github.com/user-attachments/assets/becb5177-dd8f-4ea6-8abc-c33ecdaef4b7" /> 
<img width="867" height="566" alt="image" src="https://github.com/user-attachments/assets/2da3552f-b28d-4e5a-8cd4-d0c500b1f657" />

Right click on ost-config.php and click properties->Security->Advanced->Disable Inheritance->Remove all inherited permissions->Apply->Ok
<img width="767" height="520" alt="image" src="https://github.com/user-attachments/assets/8543117a-893c-4e35-ac28-3740f7420721" />

Then to add New Permissions, click Add->Select a Principal->Type in Everyone->Check names->Ok->Full Control->Apply->Ok
<img width="1440" height="860" alt="image" src="https://github.com/user-attachments/assets/112f1798-1788-4035-861c-d1b5e1b389ca" />

Set up osTicket profile in the browser
<img width="1440" height="860" alt="image" src="https://github.com/user-attachments/assets/65f75640-af79-4e63-a3dc-3d7a750cd0cd" />

From the “osTicket-Installation-Files” folder, install the HeidiSQL program
<img width="867" height="566" alt="image" src="https://github.com/user-attachments/assets/4f4c29f1-583e-4827-acbd-bcf7a5245aa7" />

Open Heidi SQL. Create a new session->enter both the username and password, bothing being root->Click open
<img width="936" height="593" alt="image" src="https://github.com/user-attachments/assets/531e1cbe-d114-4dd7-81b7-995c24bbc232" />

To connect to the session, right click o Unnamed->Create new-> Database-> enter "osTicket"
<img width="936" height="593" alt="image" src="https://github.com/user-attachments/assets/24d9cf7f-48b9-439d-a342-d641c96589e9" />

Continue Setting up osTicket in the browser-> MySQL Database: osTicket-> MySQL Username: root-> MySQL Password: root-> Click Install
<img width="828" height="420" alt="image" src="https://github.com/user-attachments/assets/4f204d81-2a1f-49dc-92ea-fdc154efd1f6" />

The osTicket is finally installed!
<img width="837" height="642" alt="image" src="https://github.com/user-attachments/assets/c5726b6c-1211-4da2-b232-30c9e117f0a8" />


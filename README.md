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

<h2>Installation Stages</h2>
- To start our project, we must create a virtual machine in Azure with Windows 11 Pro and 4 VCPUS.
<img width="1000" height="459" alt="image" src="https://github.com/user-attachments/assets/03e8182a-b403-49e9-ba67-89596acfd31c" />

- Next we will start the Remote Desktop App on windows and enter in our public IP Address
<img width="967" height="526" alt="image" src="https://github.com/user-attachments/assets/61cee04d-73ab-4a31-976e-8b6877f00248" />

- We will enter our credentials
<img width="989" height="450" alt="image" src="https://github.com/user-attachments/assets/7ccc8253-5626-4e14-91c9-62c254d00b5b" />

- Once in the virtual machine, open Microsoft Edge and go to: https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD and install the contents
<img width="977" height="191" alt="image" src="https://github.com/user-attachments/assets/efca141d-fce5-4826-bc1b-7e7cb0bea0c1" />

- Once the file folder is downloaded, unzip it to your desktop amd extract the files from within the folder
<img width="827" height="463" alt="image" src="https://github.com/user-attachments/assets/582e0b80-46ab-4919-b954-950ca756ae7e" />

- Click the windows icon and go to the control panel. Go to Programs and click turn Windows features on and off, and check the Internet Information Services(IIS) box
<img width="614" height="465" alt="image" src="https://github.com/user-attachments/assets/01a2dea9-fa65-4116-b8bd-1f98af363058" />

- Scroll down and open world wide web, open Application Development Features and click the check box labeled "CGI"
<img width="617" height="462" alt="image" src="https://github.com/user-attachments/assets/f7d9fe20-1164-4346-b468-a649a05f7b5f" />

- From the "osTicket-Installation-Files" folder install the PHP Manager for IIS
<img width="796" height="501" alt="image" src="https://github.com/user-attachments/assets/8d502101-284f-439a-b4b2-c4335f65a370" />

- From the “osTicket-Installation-Files” install the Rewrite Module
<img width="745" height="457" alt="image" src="https://github.com/user-attachments/assets/8f1ca287-950d-42c6-b3f6-4eb49ac9ac9f" />

- Within File Explorer, go to the C Drive and make another folder called PHP. This will act as the directory
<img width="715" height="457" alt="image" src="https://github.com/user-attachments/assets/e104f376-746a-4217-b1b0-c0cc3b677708" />

- From the “osTicket-Installation-Files” folder, extract the files from the PHP 7.3.8 to the PHP folder
<img width="713" height="485" alt="image" src="https://github.com/user-attachments/assets/4ed26c96-dc18-4424-b106-d9624dcc0abc" />

- From the “osTicket-Installation-Files” folder, install the VC_redist.x86.exe. file
<img width="720" height="465" alt="image" src="https://github.com/user-attachments/assets/a1b51a7c-4ca0-43bf-8b79-87d68188f159" />

- From the “osTicket-Installation-Files” folder, install MySQL 5.5.62/Click Typical Setup -> Launch Configuration->Standard Configuration->enter the username and password which are both root
<img width="713" height="462" alt="image" src="https://github.com/user-attachments/assets/85272f5d-26df-4693-a05d-78738744aeec" />

- Open IIS as Admin
<img width="610" height="438" alt="image" src="https://github.com/user-attachments/assets/acc7c878-121c-4fb5-ba36-450952bcb103" />

- Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
<img width="801" height="435" alt="image" src="https://github.com/user-attachments/assets/bf80bdde-d016-4a7a-921f-fa6a184a5e8e" />

- Reload IIS (Open IIS, Stop and Start the server)
<img width="1066" height="617" alt="image" src="https://github.com/user-attachments/assets/118ad7a0-b7fc-4adf-bae4-9f81356e4e1f" />

- From the osTicket-Installation-Files folder, extract the osTicket-v1.15.8 folder
<img width="628" height="373" alt="image" src="https://github.com/user-attachments/assets/0926c407-a62d-473a-8005-7d213ee10d3c" />

- Copy the “upload” folder into “c:\inetpub\wwwroot”
<img width="1440" height="900" alt="image" src="https://github.com/user-attachments/assets/9a29f8e1-dc62-4ec4-9b3e-846c9d493fb1" />
<img width="1440" height="900" alt="image" src="https://github.com/user-attachments/assets/c9e511bc-4796-4df0-a184-014fa5de7efd" />

- Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
<img width="1440" height="900" alt="image" src="https://github.com/user-attachments/assets/191edbf3-da1a-4c26-a6ea-a7e8ccf947a9" />

- Reload IIS again and Stop and Start the server (Open IIS, Stop and Start the server)
<img width="1440" height="860" alt="image" src="https://github.com/user-attachments/assets/99a8e33a-97e6-4f50-bdd5-1da54d63b817" />

- Go to sites -> Default -> osTicket. On the right, click “Browse *:80”
<img width="1440" height="860" alt="image" src="https://github.com/user-attachments/assets/f4a6eefc-7112-4f51-a907-b5b3969cd500" />

- Go back to IIS, sites -> Default -> osTicket
<img width="1440" height="860" alt="image" src="https://github.com/user-attachments/assets/f0756f62-b1e2-4689-b033-87d52fa07df4" />

- Double-click PHP Manager Click “Enable or disable an extension”
<img width="1440" height="860" alt="image" src="https://github.com/user-attachments/assets/77e3fadc-5240-4554-af1d-1a4bf142ccc4" />

- Enable: php_imap.dll, Enable: php_intl.dll Enable: php_opcache.dll and after you are finished refresh your broswer
<img width="1440" height="860" alt="image" src="https://github.com/user-attachments/assets/2d6f4f8d-d857-4b3d-b820-b430f3784fc2" />

- Go to the C Drive->inetpub->wwwroot->osTicket->include and look for the file ost-sampleconfig.php and rename it to ost-config.php
<img width="867" height="566" alt="image" src="https://github.com/user-attachments/assets/becb5177-dd8f-4ea6-8abc-c33ecdaef4b7" /> 
<img width="867" height="566" alt="image" src="https://github.com/user-attachments/assets/2da3552f-b28d-4e5a-8cd4-d0c500b1f657" />

- Right click on ost-config.php and click properties->Security->Advanced->Disable Inheritance->Remove all inherited permissions->Apply->Ok
<img width="767" height="520" alt="image" src="https://github.com/user-attachments/assets/8543117a-893c-4e35-ac28-3740f7420721" />

- Then to add New Permissions, click Add->Select a Principal->Type in Everyone->Check names->Ok->Full Control->Apply->Ok
<img width="1440" height="860" alt="image" src="https://github.com/user-attachments/assets/112f1798-1788-4035-861c-d1b5e1b389ca" />

- Set up osTicket profile in the browser
<img width="1440" height="860" alt="image" src="https://github.com/user-attachments/assets/65f75640-af79-4e63-a3dc-3d7a750cd0cd" />

- From the “osTicket-Installation-Files” folder, install the HeidiSQL program
<img width="867" height="566" alt="image" src="https://github.com/user-attachments/assets/4f4c29f1-583e-4827-acbd-bcf7a5245aa7" />

- Open Heidi SQL. Create a new session->enter both the username and password, bothing being root->Click open
<img width="936" height="593" alt="image" src="https://github.com/user-attachments/assets/531e1cbe-d114-4dd7-81b7-995c24bbc232" />

- To connect to the session, right click o Unnamed->Create new-> Database-> enter "osTicket"
<img width="936" height="593" alt="image" src="https://github.com/user-attachments/assets/24d9cf7f-48b9-439d-a342-d641c96589e9" />

- Continue Setting up osTicket in the browser-> MySQL Database: osTicket-> MySQL Username: root-> MySQL Password: root-> Click Install
<img width="828" height="420" alt="image" src="https://github.com/user-attachments/assets/4f204d81-2a1f-49dc-92ea-fdc154efd1f6" />

- The osTicket is finally installed!
<img width="837" height="642" alt="image" src="https://github.com/user-attachments/assets/c5726b6c-1211-4da2-b232-30c9e117f0a8" />


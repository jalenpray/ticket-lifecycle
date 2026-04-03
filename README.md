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


From the “osTicket-Installation-Files” folder, install MySQL 5.5.62/Click Typical Setup -> Launch COnfiguration->Standard Configuration->enter the username and password which are both root
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d953526d-6c2e-4f40-937e-a9601881b8ef" />

Open IIS as Admin
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6569d5cf-9adf-48e8-b97d-70ee47c27bc4" />

Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0f1d061d-546a-4920-be1e-6d7ca34eb7fd" />

Reload IIS (Open IIS, Stop and Start the server)

Go to sites -> Default -> osTicket. On the right, click “Browse *:80”










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

- Azure Virtual Machine
- osTicket Installation Files
- Heidi SQL

  
<h2>Installation Steps</h2>

![Screenshot 2025-04-28 092017](https://github.com/user-attachments/assets/deaa8482-1fe4-4eba-9e92-d9bc7af85a0e)

1.) First, we set up a resource group in Microsoft azure and name it osTicket. Next, we create a virtual machine (VM) within this group, using a Windows 10 image and ensuring it is configured with a minimum of 2 vCPUS.


![Screenshot 2025-04-28 092549](https://github.com/user-attachments/assets/8dfd6278-6e02-42d3-aa2c-e9fe054f7de7)

2.) We access the virtual machine using Remote Desktop Protocol (RDP) by entering its public IPv4 address, which can be found in the Azure portal."


![osticket install_LI](https://github.com/user-attachments/assets/4a23beff-a906-4ea8-8680-1eb6b4eab2d9)

3.) "After establishing a connection to the VM, we download the osTicket-Installation-Files.zip file and extract its contents to the desktop. The resulting folder, named os-Ticket-Installation-Files, contains the necessary files for installing osTicket."


![image](https://github.com/user-attachments/assets/e8c380f4-c0c2-4503-996c-1a796efd579e)

4.) "Next, we enable Internet Information Services (IIS) by going to the Control Panel and selecting 'Turn Windows features on or off.' We scroll down to locate IIS, check the box to enable it, and expand the selection. Under 'World Wide Web Services' > 'Application Development Features,' we ensure that 'CGI' is selected, then click OK to apply the changes."


![image](https://github.com/user-attachments/assets/aa044c4f-8a9e-412b-8be1-9952aa9206a3)




![image](https://github.com/user-attachments/assets/5cc14b6f-eefc-413e-876b-e129714d5d78)




![image](https://github.com/user-attachments/assets/7e16ac1a-8c82-4561-9bda-d8a80ebc1e3f)


![image](https://github.com/user-attachments/assets/51d0a6e2-44b3-4cc7-8885-dea720bbd317)

5.) Within the osTicket installation folder on the VM’s desktop, we find and run the PHP Manager installer (PHPManagerForIIS_V1.5.0.msi) to continue the setup process."



![image](https://github.com/user-attachments/assets/e51935a0-4a18-483f-95de-6f2152e7ae08)




![image](https://github.com/user-attachments/assets/2a4b0988-34bb-4a9e-9ec9-9eaa6c1a130b)

6.) Within the same folder, we install the Rewrite Module to continue configuring the environment.

![image](https://github.com/user-attachments/assets/1a2ff974-bb16-4dda-a098-f18435250279)




![image](https://github.com/user-attachments/assets/36d86ccb-d7bd-47f4-88b6-78f90ba833b2)

7.) "In the same directory, we install the Rewrite Module to proceed with configuring the environment."


![image](https://github.com/user-attachments/assets/0282a6ea-cb48-4714-8fd5-d86f8233d325)

8.) Next, we create a new directory at C:\PHP to store the PHP runtime. We then extract all the contents of the PHP 7.3.8 archive (php-7.3.8-nts-Win32-VC15-x86.zip) into this folder. This step is essential for configuring PHP with IIS, as it allows the server to locate and execute PHP scripts correctly. Once extracted, we verify that all necessary files, including php.ini, are present in the directory."


![image](https://github.com/user-attachments/assets/d3254e10-aaba-48aa-8daf-b0aea2334827)




![image](https://github.com/user-attachments/assets/40196994-a3da-463a-b3a9-8dbbc64f1307)

9.) Next, we install VC_redist.x86.exe from the osTicket installation folder to ensure the required Visual C++ Redistributable components are properly installed. This step is crucial for the correct functioning of PHP and other components that rely on these libraries. After installation, we restart the system to apply the changes, ensuring that all dependencies are correctly initialized for the setup process."


![image](https://github.com/user-attachments/assets/a21de9cc-a964-48c4-b924-3a8b0f486578)




![image](https://github.com/user-attachments/assets/b2551cb4-5ece-4f9a-99d0-2b9e61994803)




![image](https://github.com/user-attachments/assets/9bb77b7d-aa4b-4b29-aeab-ce3127e39468)

10.) Next, we install MySQL (mysql-5.5.62-win32.msi) from the osTicket installation folder to set up the MySQL database server. After installation, we run the configuration wizard and select the standard configuration option. When prompted for a username and password, we choose 'root' for both to keep the setup simple for this project. Finally, we complete the installation by clicking the 'Execute' button."


![image](https://github.com/user-attachments/assets/99ab420b-cc71-4c9d-8092-d9517dde9fa5)




![image](https://github.com/user-attachments/assets/af876cdd-7e53-408b-a913-6ff0a1d8ed56)




![image](https://github.com/user-attachments/assets/224bb61a-dda5-47c6-aad2-e5ba987aab87)




![image](https://github.com/user-attachments/assets/d97bf624-5efa-42ce-bcf9-ad7ea40d61a3)




![image](https://github.com/user-attachments/assets/1fbb5407-4161-4b21-ac4a-7287896ddaa5)




![image](https://github.com/user-attachments/assets/1e87b06a-f0c7-46fe-a084-42ee217130d9)




![image](https://github.com/user-attachments/assets/c5bc10ee-a9a0-48ad-8bf9-99b24cbd4092)




![image](https://github.com/user-attachments/assets/4d260dab-349d-45c6-a1a9-4e5c0752ff84)




![image](https://github.com/user-attachments/assets/f3826ffa-0bdc-41b3-a0bd-fd327147f390)




![image](https://github.com/user-attachments/assets/080edcf2-61be-4155-89d2-6d2f814f53fb)

11.) "Next, we open IIS Manager as an administrator. To ensure PHP is properly integrated, we register it within IIS by configuring the required settings for handling PHP scripts. Once the configuration is complete, we restart the server by selecting the 'Restart' option in IIS Manager. This step is necessary to apply the changes and ensure IIS is fully ready to process PHP requests. After the restart, we verify that PHP is working correctly by checking the IIS logs and running a test script."



![image](https://github.com/user-attachments/assets/a7518d9f-6c67-4ac7-8f0b-d92190353daf)




![image](https://github.com/user-attachments/assets/187ff762-3ebb-40f3-967f-91680f34e3d3)




![image](https://github.com/user-attachments/assets/f2047e44-8fb1-492b-9223-1885609e18af)



![image](https://github.com/user-attachments/assets/5a1be101-8911-4e53-9e8d-0c2bd8d36c20)

12.) We begin by extracting osTicket-v1.15.8.zip from the osTicket-Installation-Files folder. Next, we copy the upload directory into C:\inetpub\wwwroot, and then rename it to osTicket within that location.



![image](https://github.com/user-attachments/assets/c6c827b5-b8aa-439b-a0de-c3930d7c6dc7)

13.) Next, we return to IIS Manager and restart the server. To enable the required PHP extensions, we navigate to Sites > Default Web Site > osTicket, then double-click on PHP Manager. From there, we choose "Disable or enable an extension" and enable php_intl.dll, php_opcache.dll, and php_imap.dll. Finally, we refresh the osTicket web interface to confirm that the Intl Extension is now enabled.



![image](https://github.com/user-attachments/assets/366c01ec-20f4-451c-82b7-d6d4ec5a6dde)

14.) Next, we navigate to C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php and rename the file to ost-config.php within the same directory.



![image](https://github.com/user-attachments/assets/e1cbe3d9-4372-41bb-b4c9-d209687ebc90)

15.) We then configure the correct permissions for ost-config.php by right-clicking the file and selecting "Properties". Under the Security tab, we disable inheritance, remove all existing permission entries, and grant full access to Everyone.



![image](https://github.com/user-attachments/assets/58f9efd7-662e-41f2-9b42-1b8f6ac71ada)

16.) We continue the osTicket setup in the browser by clicking "Continue". Next, we choose a name for our helpdesk and specify a default email address to receive notifications for customer-submitted tickets.


![image](https://github.com/user-attachments/assets/1d6c9e71-a807-4859-8721-6d88dbe1e6fa)


![image](https://github.com/user-attachments/assets/eebd253c-c230-4207-b1a7-892d7dc26e59)


![image](https://github.com/user-attachments/assets/cbe7cfe4-ec64-4d64-b36e-8deb42c8b00c)


![image](https://github.com/user-attachments/assets/b37c6bb7-bc5c-407e-9be5-c8b61fef1af1)

17.) From the os-Ticket-Installation-Files folder, install HeidiSQL. Once installed, launch the application and create a new session using "root" for both the username and password. In the left-hand panel, right-click on "Unnamed" and create a new database named osTicket.




![image](https://github.com/user-attachments/assets/a039727e-787f-4079-9cc1-e55c886aa081)

18.) Last, we continue setting up osTicket in the web browser of the VM. Under MySQL Database we type in “osTicket”. For both MySQL Username and MySQL Password, we type in “root”. When we click on the “Install Now” button we have finished with the installation of osTicket to our virtual machine.




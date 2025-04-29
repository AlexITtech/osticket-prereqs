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




![image](https://github.com/user-attachments/assets/d3254e10-aaba-48aa-8daf-b0aea2334827)




![image](https://github.com/user-attachments/assets/40196994-a3da-463a-b3a9-8dbbc64f1307)




![image](https://github.com/user-attachments/assets/a21de9cc-a964-48c4-b924-3a8b0f486578)




![image](https://github.com/user-attachments/assets/b2551cb4-5ece-4f9a-99d0-2b9e61994803)




![image](https://github.com/user-attachments/assets/9bb77b7d-aa4b-4b29-aeab-ce3127e39468)




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




![image](https://github.com/user-attachments/assets/a7518d9f-6c67-4ac7-8f0b-d92190353daf)




![image](https://github.com/user-attachments/assets/187ff762-3ebb-40f3-967f-91680f34e3d3)




![image](https://github.com/user-attachments/assets/f2047e44-8fb1-492b-9223-1885609e18af)



# osticket-prereqs
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
- Files needed for installation (Installation Files): https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

- Azure Microsoft

- HeidiSQL

- PHP Manager

- osTicket-v1.15.8

- Internet Information Services (ISS)

- Rewrite Module

- VC Redist

<h2>Installation Steps</h2>

<p>
(1.) First step you want to take is creating a Windows 10 virtual machine with 4vCPUS so it can run at the most optimal speed . You also have to create a username and password and that can be whatever you choose. We are using Microsoft Azure.
  
<img src="Screenshot 2023-09-18 194753.png"></img>
</p>
<br />

(2.) Next step you want to take is using the public ip address of the virtual machine open remote desktop and connect to the ip address of the virtual machine. After that login with the username and password you created.

<img src="Screenshot 2023-09-21 120557.png"></img> <img src="Screenshot 2023-09-21 120643.png"></img>

(3.) Once you're able to connect to your virtual machine, go to your control panel and click on programs. When you open programs click on "Turn Windows feature on or off".
![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/a99d0fb8-69d8-43a8-9905-e0f50a8f66a4)
![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/2529247c-2ff1-431e-9f78-0dd41f54b9cd)

(4.) To continue you will need to enable ISS in Windows with CGI and Common HTTP Features
- World Wide Web Services -> Application Development Features-> [X] CGI [X] Common HTTP Features
![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/d966d278-dda6-457e-b641-72abe3896b0a)
![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/ad34f0c0-2dc6-4d35-943f-14801276e238)

Also need to enable ISS Management Console

![270256860-eae09ba3-0d33-4b08-ac49-a2b1ffcf017e](https://github.com/Jacobi990/osticket-preregs/assets/143012536/0a40ad91-e2da-430b-87ad-183d31ef6460)

 You want to make sure ISS is enabled and to make sure go to a search engine and search up 127.0.0.1. The screen should look similar to this 
 
 ![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/7e642e5b-38b7-4467-961b-76d18aa723f7)

 (5.) ISS is now enabled. Download and install PHP Manager (PHPManagerForIIS_V1.5.0.msi) for ISS from the Installation Files. Go through the process to install and finialize the install

 (6.) Download and install the Rewrite Module (rewrite_amd64_en-US.msi) from the Installation Files. 

 (7.) Go to your C Drive (Windows (C:)) and create a folder named "PHP" 

 (8.) From the Installation Files download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into "PHP". Go to downloads and find the php you downloaded and extract it into the "PHP" file.
 
 !!ATTENTION!! if this appears choose to "Keep" the file: 

 ![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/0c5d9e19-879a-41ce-b089-7142261df853)
 ![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/3df45d3d-56ef-4442-9a72-07ef485a68c2)

 (9.) Next after you downloaded and extracted the zip file into the "PHP" folder on the C-Drive, download and install VC_redist.x86.exe. Go through all the steps to download and install it.

 (10.) Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
-  Typical Setup->
-  Launch Configuration Wizard (after install)->
-  Standard Configuraton->
-  Password1

Make the password: Password1

  ![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/f5b45ee1-8c36-4058-87d9-9bc7aaca777e)

  Then excute the application
  
  ![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/dd56c184-1ce8-4b0b-988a-0782b8893e49)

  (11.) Now the everything is downloaded go to the windows' search bar and look up "ISS". Open ISS as an admin. This is what should show up.
  
  ![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/80652aa2-c87b-4973-8809-bc6528c83078)

  (12.) From within ISS you want to register PHP. Click on PHP 
  
  ![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/a9fef8f5-7ca1-4eb2-8fb9-cd9e554fc968)

  Once you click on it, you'll see register new PHP version and then click on that.
  
  ![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/d6da5ece-ab25-430a-9109-a6381245120e)

  After you click on it you want to create a path to the "PHP" file. Go to C-Drive-> PHP-> click on php-cgi file. 
  
  ![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/96ee3267-103d-4511-9309-0ed78d15d593)










 




















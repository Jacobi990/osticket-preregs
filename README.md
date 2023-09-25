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

  Restart the ISS server

  ![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/e1d0ae2f-53a5-4a4a-b324-b207d1d4f958)

  (13.) Download osTicket v1.15.8 and install from the Installation Files. Extract and copy “upload” folder to c:\inetpub\wwwroot and then within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
  
  Once you do that reload ISS again.

  (14.) Go back to IIS, sites -> Default -> osTicket- on the right, click "Browse *.80".
  
  ![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/23ec64de-36aa-4b3b-a048-604a46c3d5c3)

  It shouldn't work the first time you click as some extensions aren't installed yet on the osTicket browser
  
  ![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/c89d153d-ad57-42c3-98a7-6456e6bca846)

  To enable the extensions: -Go back to IIS, sites -> Default -> osTicket -Double click PHP manager -Click "Enable or disable an extension"
  
  ![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/fa8de3fe-b005-4c80-b3ec-c27c884c41b1) ![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/c50110af-e0b1-447d-93ea-e06b950b8b40)

Enable these extensions after you click on the extension
- Enable: php_imap.dll
- Enable: php_intl.dll
- Enable: php_opcache.dll
- 
![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/3080e321-6aaf-4d3b-925b-37eb887d9667)

(15.) Once we have all the extensions installed in ISS, we are going to want to rename one of the files in our osTicket folder. Go into the file explorer and search for C;\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

We are going to rename the ost-sampleconfig.php to ost-config.php

Now that we have renamed the files, right click on the file and go to properties. From there click security, click on advance, and disable the inheritance. We will select Remove all inherited permissions from this object.

Now we will add new permissions.

Click Add

![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/6a80ec92-5aab-4eee-9307-7dd83ddbfbfe)

Click on select the principal

![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/a52f6dfd-fa9d-4f2c-b70a-58e9b1ab2de4)

Type "Everyone" in the text box

![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/fb61afee-c322-4507-af7a-da9bf4bfa08b)

Make sure everything is checked out including Full Controll

![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/8c7225e3-5659-4a71-9173-1d66954bce01)

Lastly click "Apply" then "Ok"

![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/dbd82ca0-5170-4525-9ff1-cb2ada656ac7)

Now we added our permissions go back to osTicket in the browser to continue in setting it up. At the bottom of osTicket click "Continue". Fill out the page as needed except for the "Database Setting". We need download and install Heidi SQL from the Installation Files

![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/0d079112-45cf-48fd-83d1-888bf43dc8af)

Once the program finish downloading we are going to create a new session

![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/690a246b-be64-4e95-ac31-f0525093a0ea)

We are going keep the username as root and set the password as "Password1"

![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/58cf5c33-3da7-49b2-8769-0f1e7e6ef35c)

Now everything is downloaded go back to osTicket and under "Database Settings" the username will be root and password will be "Password1"

Once you finish that we'll be creating a database in Heidi SQL. In Heidi right click on the left side where is says "Unnamed", select "create new", and then select "database". Name the new database osTicket. Once we have the new database setup go back to the osTicket browser and under MySQL Database type in osTicket.

![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/6d4d16ca-bd8a-49b3-9272-8fc96b6b6b0f)

We will be deleting the "setup" folder as some cleanup.  -Delete: C:\inetpub\wwwroot\osTicket\setup. Only delete the setup folder and nothing else.
Then set permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/13cc3308-92e0-4809-9e13-08558e5e0cd7)
![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/117d2f4d-63dd-46b2-b70d-d68675886dca)

And now final step is logging into osTicket on the browser
http://localhost/osTicket/scp/login.php 

![image](https://github.com/Jacobi990/osticket-preregs/assets/143012536/d2ef5229-f5e9-415a-9637-b0ff118287f3)

Great Job! You successfully downloaded osTicket



















  



  











 




















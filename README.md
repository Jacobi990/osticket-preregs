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
Files needed for installation: https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
Azure Microsoft
HeidiSQL
PHP Manager  
osTicket-v1.15.8  
Internet Information Services (ISS)
Rewrite Module
VC Redist
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



















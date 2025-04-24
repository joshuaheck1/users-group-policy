<p align="center">
<img width="450" height="250" alt="Microsoft Active Directory Logo" src="https://github.com/user-attachments/assets/cd75c7f5-fba1-4682-a616-dc487e761fbc"
 alt="Microsoft Active Directory Logo"/>
</p>

<h1>Creating Users and Group Policy Objects for Active Directory</h1>
This tutorial outlines creating a User Database and Group Policy Objects for Active Directory within Azure Virtual Machines.<br />

<h2>Prerequisite</h2>

- [Create Active Directory Infrastructure in Azure](https://github.com/joshuaheck1/create-ad-infrastructure)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Wndows App (for MacOS)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Section 1: Create User Database
- Section 2: Group Policy Objects 

<h2>Deployment and Configuration Steps</h2>

<h3>Section 1: Create User Database</h3>
<p>
<img width="600" height="500" alt="CU1" src="https://github.com/user-attachments/assets/78ca0b79-47d2-4c1a-8c41-a143b8680c6d" />
</p>

<p>
- Login into DC-1 via Remote Desktop using the jane_admin account. (mydomain.com\jane_admin and password)
<p>- From the Start Menu, type PowerShell in the Search Bar, right-click Windows PowerShell ISE, and Run as Admin.</p>
<br />

<p>
<img width="750" alt="CU2" src="https://github.com/user-attachments/assets/ab10520f-6366-401e-bdd2-576e982c1efd" />
<br />

- Click here --> [SCRIPT](https://github.com/joshmadakor1/AD_PS/blob/master/Generate-Names-Create-Users.ps1) to copy the file we need for the User database as seen in Figure 2.

<p>- Select the icon next to Raw in the top right corner. Copy raw file and go back to PowerShell ISE.</p>
<br />

<p>
<img width="750" alt="CU3" src="https://github.com/user-attachments/assets/9dd1f6f1-366a-41fb-9293-069c852967d7" />
</p>

<p>- 1. Click the blank page to Create a new file.</p>
<p>- 2. Paste the Script .</p>
<p>- 3. Click the Play button to Run the Script.</p>
<br />

<p>
<img width="750" alt="CU4" src="https://github.com/user-attachments/assets/3a74ba58-8578-438a-80f9-7d68d63c1843" />
</p>

<p>- While the thousands of users are being created, take a quick note of the password in the 2nd line of the script. This password is for all the users we are adding. We will need this when we attempt to login as one of the new users.</p>
<br />

<p>
<img width="750" alt="CU5" src="https://github.com/user-attachments/assets/b87b5323-61dd-4174-af96-995018e43893" />
</p>

<p>- We should have enough users by now to attempt to login on Client-1 with their credentials.</p>
<p>- Let the script keep running and head to the Start Menu. From here, navigate to Avctive Directory Users and Computers.</p>
<p>- Click OK and select the _EMPLOYEES folder to check out all the users created so far.</p>
<br />

<p>
<img width="750" alt="CU6" src="https://github.com/user-attachments/assets/f2ffba9f-88ac-4ca6-b7ab-aa5003c059e5" />
</p>

<p>- Choose a random Username you like and let's use it to login to Client-1.</p>
<p>- I chose bat.raj because... Why not? 😂</p>
<br />

<p>
<img width="750" alt="CU7" src="https://github.com/user-attachments/assets/192c3116-8252-438c-903b-a4067a1cce80" />
</p>

<p>- Now we will attempt to login to Client-1 with the new user you chose.</p>
<p>- Do not forget to specify domain in username. </p>
<p>- mydomain.com\bat.raj -> Password1. (mydomain.com\username and Password1) </p>
<p>- Did it work? bat.raj had zero issues logging in. 😉 </p>
<br />

<h3>Section 2: Group Policy Objects</h3>










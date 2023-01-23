<h1>Part 2</h1>

[YouTube Demonstration by Kevtech IT Support](https://www.youtube.com/watch?v=cfeHXNaYWjU)

<h2>Description</h2>
This project is about installing Active Directory on a Windows Server 2019 using Azure VM and creating users using PowerShell.
<br />


<h2>Environments Used </h2>

- <b>Azure VM</b>
- <b>Windows Server 2019</b>
- <b>PowerShell</b>

<h2>Program walk-through:</h2>

<!-- <p align="center"> --!>
1 - First step is to login into your Azure portal. <br/>
2 - After logging in select "Home" from the left panel then select "Server 2019". <br/>
<img width="900" alt="Select Home" src="https://user-images.githubusercontent.com/103763124/212562143-40397be2-474b-432c-bf61-f0669e4f07b6.png">
<br />
3	- "Start" the Server 2019. <br/>
4 - You can then use the pervious RDP file you downloaded in Part 1 or download a new one and login in. <br/>
<img width="900" alt="Start Server 2019" src="https://user-images.githubusercontent.com/103763124/212562023-3d122a94-21ea-4dd7-9179-f479ae544602.png">
<br />
5	- When the Server Manager completes loading select "Manage" from the top right corner then "Add Roles and Features".  <br/>
<img width="900" alt="Select Add Roles and feature" src="https://user-images.githubusercontent.com/103763124/212563204-71d40776-fa50-406e-b877-74ad1c1ff551.png">
<br />
6 - Then select "Active Directory Users and Computers". <br/>
<img width="900" alt="Select ADUC" src="https://user-images.githubusercontent.com/103763124/212563320-fe32cd1e-72cf-4203-8ed1-1c736332a2ec.png">
<br />
7 - When it opens select "Next". <br/>
<img width="900" alt="Select Next" src="https://user-images.githubusercontent.com/103763124/212563839-966cb4c3-366b-44b4-8ba9-9b7fbddd88d4.png">
<br />
8 - Keep the default and select "Next". <br/>
<img width="900" alt="Next Role" src="https://user-images.githubusercontent.com/103763124/212563366-60faba38-9433-4272-8a69-ddaee935233a.png">
<br />
9 - Keep the default and select "Next". <br/>
<img width="900" alt="Review IP" src="https://user-images.githubusercontent.com/103763124/212566820-294e1e7e-83c6-4050-91a2-22b497ce80c5.png">
<br />
10 - Select "Active Directory Domain Services". <br/>
<img width="900" alt="Select ADDS" src="https://user-images.githubusercontent.com/103763124/212563479-4ce16ee2-744b-46e8-8650-234858c579bf.png">
<br />
11 - Now you can select "Next". <br/>
<img width="900" alt"Chose ADDS" src="https://user-images.githubusercontent.com/103763124/212563676-ebc73d78-6973-4b64-8cb8-da958f5ef0e0.png">
<br />
12 - Then select "Add Features" then select "Next". <br/>
<img width="900" alt="ADD ADDS" src="https://user-images.githubusercontent.com/103763124/212563598-9dafe9b0-1c2a-4dd4-b06e-623f27099155.png">
<br />
13 - Keep the default and select "Next". <br/>
<img width="900" alt="Next NET" src="https://user-images.githubusercontent.com/103763124/212566949-9b9b596e-da62-4d35-b167-d5e3f95456ad.png">
<br />
14 - Keep the default and select "Next". <br/>
<img width="900" alt="Next DNS" src="https://user-images.githubusercontent.com/103763124/212563940-427dc584-9c49-4d1e-9d01-e333a6cd0aa7.png">
<br />
15 - Select "Install" and let the installation complete. <br/>
<img width="900" alt="Install ADDS" src="https://user-images.githubusercontent.com/103763124/212564019-83ddc5a2-ca90-4e10-b667-8155b794c260.png">
<br />
16 - Here select "Promote this server to a domain controller" in the blue writing. <br/>
<img width="900" alt="Promote the AD" src="https://user-images.githubusercontent.com/103763124/212564129-b1221c4d-f681-4256-b292-d924ee7ee540.png">
<br />
17 - Select "Add a new forest". <br/>
18 - Give your domain a name then select "Next". <br/>
<img width="900" alt="create domain" src="https://user-images.githubusercontent.com/103763124/212564253-90820e82-0e27-4bdb-a720-b9879aaea2f7.png">
<br />
19 - Here enter a password to recover your domain controller. You can enter the same password for your Server 2019 helpdesk account and confirm it then select "Next". <br/>
<img width="900" alt="Root Pass" src="https://user-images.githubusercontent.com/103763124/212564331-253357f5-0ccc-4dda-9478-7bd7c947f7bf.png">
<br />
20 -  Once the NETBIOS domain name is generated, select "Next". <br/>
<img width="900" alt="Next BIOS" src="https://user-images.githubusercontent.com/103763124/212564427-ea5ff49f-db32-4505-b613-366f021cd770.png">
<br />
21 - Keep the default and select "Next". <br/>
<img width="900" alt="Next Folders" src="https://user-images.githubusercontent.com/103763124/212564486-4f541adc-2ed0-425c-a644-f690b061e839.png">
<br />
22 - We are going to contiune to install Active Directory through PowerShell so select "View scipt". <br/>
<img width="900" alt="Review" src="https://user-images.githubusercontent.com/103763124/212564538-fa68715f-b053-4b54-9376-aadfdeb51d22.png">
<br />
23 - Once the script opens copy it. <br/>
<img width="900" alt="Script" src="https://user-images.githubusercontent.com/103763124/212564606-d9d4f7b6-0abf-439b-b216-8813a334957e.png">
<br />
24 - You can now select "Cancel" the rest of the installation and then select "Yes". <br/> 
<img width="900" alt="yes to exit ADDS" src="https://user-images.githubusercontent.com/103763124/212567514-1d4a1650-8eaa-4dd9-a4d1-d1825ef96ea6.png">
<br />
25 - Search "PowerShell" at the search tab on the taskbar and run it as an administrator. <br/>
26 - Paste in the script that you just copied and hit "Enter". <br/>
<img width="900" alt="enter the script" src="https://user-images.githubusercontent.com/103763124/212564708-054a012d-07dd-4847-84b3-0f8bc5ddcfbc.png">
<br />
27 - Now enter the domain controller password we created earlier and confirm it.   <br/>
<img width="900" alt="enter pass for script" src="https://user-images.githubusercontent.com/103763124/212564792-39b10887-d6e0-4e9c-91ab-420c0c0c6969.png">
<br />
28 - Once the passwords are confirmed the script will start continue installing Active Directory. <br/>
<img width="900" alt="Installing script" src="https://user-images.githubusercontent.com/103763124/212564853-12080983-6c82-48a3-9b67-6278706b33c3.png">
<br />
29 - The server will restart and you will need to navigate to your RDP that you saved or download perviously and login. <br/>
30 - Once you login the installation will contiune to complete. <br/>
<img width="900" alt="Reset ADDC" src="https://user-images.githubusercontent.com/103763124/212565118-2b64aa6c-6d02-4d91-80c8-4af2e3346584.png">
<br />
31 - When the server starts up navigate to the start menu and select "Active Directory Administrative Center". <br/> 
<img width="900" alt="Navigate to ADAC" src="https://user-images.githubusercontent.com/103763124/212565257-18869c81-2fcc-4616-a862-8fcb8b02cd8d.png">
<br />
32 - Select your domain name from the left corner. <br/>
<img width="900" alt="Open ADAC" src="https://user-images.githubusercontent.com/103763124/212565320-b99470bd-ed82-4cca-acc7-d7adefe5f3f4.png">
<br />
33 - Select "Enable a Recycle Bin" from the right corner. <br/>
<img width="900" alt="Enable recycle bin" src="https://user-images.githubusercontent.com/103763124/212565371-c18bdee3-a4e8-4061-82c6-db14d57bec8f.png">
<br />
34 - Select "OK". <br/>
<img width="900" alt="Select Okay for Bin" src="https://user-images.githubusercontent.com/103763124/212565358-8657d7c4-0e47-4149-b966-b28eff416a3f.png">
<br />
35 - Select "OK". <br/>
<img width="900" alt="Okay enable bin" src="https://user-images.githubusercontent.com/103763124/212565545-34439dfc-fa3c-4c5d-9d60-1db9ddc52339.png">
<br />
36 - Open "Server Manager" then select "Tools" from the top right corner then "Active Directory Users and Computers".  <br/>
37 - Expand your "Domain" then select "Users" folder and just look at the different accounts available. <br/>
<img width="900" alt="Users then helpdesk" src="https://user-images.githubusercontent.com/103763124/212569138-b77041c5-e315-416b-abbc-2941ef7b12b0.png">
<br />
38 - Next select "View" from the menu bar then "Advanced Features" this will allow you see more folders with more resources. <br/>
<img width="900" alt="Dangerous" src="https://user-images.githubusercontent.com/103763124/212569521-72e81081-72e9-40cc-832e-b25f2379a41b.png">
<br />
39 - Search "PowerShell" at the search tab on the taskbar and run it as an administrator. <br/>
40 - Type "import-module activedirectory" and then hit "Enter". <br/>
<img width="900" alt="import module" src="https://user-images.githubusercontent.com/103763124/212569658-c2b188d7-8d06-4a81-a654-d7e7b2d845df.png">
<br />
41 - Then type "get-command new-aduser -syntax" and then hit "Enter". This gives you some commands you can use to create resources in Active Directory. <br/>
<img width="900" alt="Syntax" src="https://user-images.githubusercontent.com/103763124/212569712-b489953a-d3cb-4fe0-8996-acaa9cd98fc8.png">
<br />
42 - Now type "new-aduser Jimmy" and then hit "Enter".  <br/>
<img width="900" alt="Adding Jimmy" src="https://user-images.githubusercontent.com/103763124/212569833-499fbe02-0910-4c00-97fe-67bbb53d7968.png">
<br />
43 - Let's add another user by typing "new-aduser Jeff" and then hit "Enter".  <br/>
<img width="900" alt="Add Jeff" src="https://user-images.githubusercontent.com/103763124/212569873-bd116e49-0d5c-411d-ac20-7cd2cd23911f.png">
<br />
44 - Now go back to "Active Directory Users and Computers". Select the "Users" folder from the left side. "Right Click" on Jeff and select "Reset Password". <br/>
<img width="900" alt="Jeff reset pasword" src="https://user-images.githubusercontent.com/103763124/212570354-3d5ca0af-f84f-4d40-b088-313b3e3ea3d4.png">
<br />
45 - Create a password for Jeff and select "OK". <br/>
<img width="900" alt="Jeff Password" src="https://user-images.githubusercontent.com/103763124/212570030-f8e71f90-2fbb-4663-a779-884239a9625b.png">
<br />
46 - After creating the password "Right Click" on Jeff again and select "Enable Account". <br/>
<img width="900" alt="Jeff Added" src="https://user-images.githubusercontent.com/103763124/212570227-b557ce1a-d8c1-42a5-a9ec-2ba04dfe3cbf.png">
<br />
47 - This time "Right Click" on Jimmy and select "Reset Password". <br/>
48 - Create a password for Jimmy and select "OK". <br/>
49 - After creating the password "Right Click" on Jimmy again and select "Enable Account". <br/>
<img width="900" alt="Jimmy enabled" src="https://user-images.githubusercontent.com/103763124/212570413-7552e76a-d13b-499e-9598-a1e2adc05c6f.png">
<br />
50 - Go back to your Azure Portal and "Stop" Server 2019. <br/>
<img width="900" alt="Stop Server 2019" src="https://user-images.githubusercontent.com/103763124/212570460-ce1c6768-190c-49f6-9497-6d743aad13d8.png">
<br />
51 - Confirm to "Stop". <br/>
<img width="900" alt="Confirm to stop" src="https://user-images.githubusercontent.com/103763124/212570463-effa555c-bcd7-4116-b7ca-dbe81f09f941.png">
<br />
52 - Confirmation of the Server 2019 has been stopped. <br/>
<img width="900" alt="Verication of Stopped" src="https://user-images.githubusercontent.com/103763124/212570470-ed3d884a-1a4e-4898-aa90-cb4e7d2605d0.png">
<br />
</p>





<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

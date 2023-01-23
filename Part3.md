<h1>Part 3</h1>

[YouTube Demonstration by Kevtech IT Support](https://www.youtube.com/watch?v=nvaShp_XNh0)

<h2>Description</h2>
This project is about setting up a Static IP for the PC. Joining the Windows 10 PC to the domain. Creating a back up admin account and adding it to the Adminsistrators group.
Disabling the built-in account. Adding the user Jimmy to the Remote Mangement Users so we remote into his account. Changing some Group Policies. 
Remoting in as the domain admin helpdesk account. Mapping a folder and sharing it. Logging in as a user.
<br />


<h2>Environments Used </h2>

- <b>Azure VM</b>
- <b>Windows Server 2019</b>
- <b>Windows 10</b>

<h2>Program walk-through:</h2>

<!-- <p align="center"> --!>
1 - First step is to login into your Azure portal. <br/>
2 - Start both VMs. <br/>
3 - On the Server search CMD on the search bar and open it. <br/>
<img width="900" alt="7" src="https://user-images.githubusercontent.com/103763124/214089760-e0ccabf3-0d55-4408-aa6a-0d2289d5eea0.png">
<br />
4 - Type "ipconfig" to see the IP of the Server 2019. <br/>
<img width="900" alt="8" src="https://user-images.githubusercontent.com/103763124/214090266-28b446c2-e5d9-4862-8d03-7f93959747f4.png">
<br />
5 - On the Windows 10 PC open CMD and type "ping 10.0.0.4" (basically ping the Server 2019 IP). It will work. <br/>
<img width="984" alt="9" src="https://user-images.githubusercontent.com/103763124/214090823-59afb6cc-12f5-49e8-bb78-464fb6b2b80b.png">
<br />
6 - But if you try to ping the domain "adamslab.local" it will not be able to. <br/>
<img width="900" alt="10" src="https://user-images.githubusercontent.com/103763124/214095905-32b6effe-b4d3-4449-8713-db7dcfea9039.png">
<br />
7 - To solve this issue search "Control Panel" on the search tab and open it. <br/>
 <img width="900" alt="11" src="https://user-images.githubusercontent.com/103763124/214091569-628c6b8e-9ec3-4e57-8f9e-5cad9623ccb5.png">
<br />
8 - Click on "View network status and tasks". <br/>
<img width="900" alt="12" src="https://user-images.githubusercontent.com/103763124/214096634-d323e2c7-bfc0-465b-940d-b79b232646d6.png">
<br />
9 - Click on "Change adapter settings". <br/>
<img width="900" alt="13" src="https://user-images.githubusercontent.com/103763124/214097157-5fadc11b-b1bc-416f-a23a-4fc483b3130f.png">
<br />
10 - Double click on "Ethernet". <br/>
<img width="900" alt="14" src="https://user-images.githubusercontent.com/103763124/214097574-9a663d5d-5ac5-4fc4-bad7-5f36c794ed69.png">
<br />
11 - Click on "Properties". <br/>
<img width="900" alt="15" src="https://user-images.githubusercontent.com/103763124/214097876-180a41c5-91f3-46f7-b59d-143fa0255f85.png">
<br />
12 - Click on "Internet Protocol Version 4 (TCP/IPv4)". <br/>
<img width="900" alt="16" src="https://user-images.githubusercontent.com/103763124/214098324-2ca57328-5593-41c1-b261-fe7f690febf1.png">
<br />
13 - Select "Use the following IP address" and "Use the following DNS server addresses" and enter the following details. <br/>
14 - The "IP address" will be the Windows 10 PC IP and the "Preferred DNS server" will be the Server 2019 IP. <br/>
15 - Then select "OK". <br/>
<img width="900" alt="18" src="https://user-images.githubusercontent.com/103763124/214098901-6b11a4c0-b8b4-448b-9b95-f581a3890c6f.png">
<br />
16 - Select "OK". <br/>
17 - You might get kicked out of the VM thats normal. If not just restart the VM and login back in. <br/>
<img width="900" alt="19" src="https://user-images.githubusercontent.com/103763124/214101138-0c1a88d2-cc98-4a1f-80ae-db02fd92b52f.png">
<br />
18 - When the Windows 10 PC starts again open CMD and ping your domain. For example, "ping adamslab.local". Now it works. <br/>
<img width="900" alt="20" src="https://user-images.githubusercontent.com/103763124/214101984-23dab594-686b-4731-9906-fb2c38f69b02.png">
<br />
19 - Open explore folder. Right click on "This PC" then choose "Properties" <br/>
<img width="900" alt="23" src="https://user-images.githubusercontent.com/103763124/214103944-72382b66-a1a3-4084-b282-b2cdec637c77.png">
<br />
20 - Click on "Rename this PC (advanced)" from the right column. <br/>
<img width="900" alt="24" src="https://user-images.githubusercontent.com/103763124/214104465-5b8087b5-e39f-4653-8175-60fb8c0f2812.png">
<br />
21 - Select "Change". <br/>
<img width="900" alt="25" src="https://user-images.githubusercontent.com/103763124/214104674-a6e31c4d-bed2-44e9-8e49-21ab7d5b1eb8.png">
<br />
22 - On the Member of select "Domain". <br/>
23 - Then type in your domain name. Then click on "OK". <br/>
<img width="900" alt="26" src="https://user-images.githubusercontent.com/103763124/214105295-62e951cf-4064-43f3-b2c8-9fd9cf94d40a.png">
<br />
24 - When you get a pop up screen enter the username and password of the Server 2019 credentials. Then select "OK". <br/>
<img width="900" alt="27" src="https://user-images.githubusercontent.com/103763124/214105810-3f1e1cb8-c861-440f-899e-78fa921f9469.png">
<br />
25 - If successful this is the confirmation you will receive. Click on "OK". <br/>
<img width="900" alt="28" src="https://user-images.githubusercontent.com/103763124/214106199-48d07b7c-c3ce-4b0a-a245-3dc8072c5062.png">
<br />
26 - Click on "OK". <br/>
<img width="900" alt="29" src="https://user-images.githubusercontent.com/103763124/214106570-e13f228e-62af-4917-8913-9e32d425d861.png">
<br />
27 - Select "Restart Now". <br/>
<img width="900" alt="30" src="https://user-images.githubusercontent.com/103763124/214106584-20d1024d-a4a8-45b9-9caf-012656e3f946.png">
<br />
28 - When the Windows 10 PC restarts, sign out of the Windows 10 PC. Click on the "start menu" then "shut down or signout" then "sign out". <br/>
<img width="900" alt="32" src="https://user-images.githubusercontent.com/103763124/214123665-0bb8a4ac-3a7f-4524-8d57-93be039f4599.png">
<br />
29 - Now lets login on the Windows 10 PC with the Server 2019 admin credentials. <br/>
<img width="900" alt="Screenshot 2023-01-23 at 8 39 49 PM" src="https://user-images.githubusercontent.com/103763124/214122620-5af45d84-e172-4a4c-ac98-79e158510e45.png">
<br />
30 - When you login lets test out if we add a user. Open "Active Directory Users and Computers". <br/>
31 - Right click on the "Users" folder then select "New" then "User". <br/>
<img width="900" alt="35" src="https://user-images.githubusercontent.com/103763124/214124592-b6ea0871-27c0-4b50-9a5d-d8b99831c73f.png">
<br />
32 - Add the following "Test" account. Then select "Next". <br/>
<img width="900" alt="36" src="https://user-images.githubusercontent.com/103763124/214125045-7be060ab-af25-4c45-9faa-dfa3233ad6c0.png">
<br />
33 - Give it a password. Then select "Next". <br/>
<img width="900" alt="37" src="https://user-images.githubusercontent.com/103763124/214125257-d2a74a28-a009-411f-9f7a-438ef2197052.png">
<br />
34 - Finally select "Finish". This proves that your able to use Active Directory and manage company resources from the Windows PC VM. <br/>
<img width="900" alt="38" src="https://user-images.githubusercontent.com/103763124/214125545-981fc21e-4373-48ad-8c5a-0b179579ef0b.png">
<br />
35 - In the search tab search for "Computer Management" and open it. <br/>
<img width="900" alt="39" src="https://user-images.githubusercontent.com/103763124/214125938-8c4fd811-51cc-4054-ab5c-fd0c23e7db5d.png">
<br />
36 - Here we are going to create a local "Admin Account" just in case we get locked out. Expand "Local Users and Groups" from the left column.  <br/>
<img width="900" alt="40" src="https://user-images.githubusercontent.com/103763124/214126862-87c09f0b-22f9-4313-ad43-a37fb5ee35db.png">
<br />
37 - Right click on the empty white area and select "New User..". <br/>
<img width="900" alt="41" src="https://user-images.githubusercontent.com/103763124/214127140-5f2935ad-4553-47c8-baff-da2d43f129ce.png">
<br />
38 - For the username type in "Administrator" and give it a password. <br/>
39 - Select "Create" then "Close". <br/>
<img width="900" alt="42" src="https://user-images.githubusercontent.com/103763124/214127594-58eafbea-ca64-4aff-bc3e-f5c5ac617241.png">
<br />
40 - Now select the "Administrator" account.  <br/>
<img width="900" alt="44" src="https://user-images.githubusercontent.com/103763124/214128195-39daa4c0-ac96-4284-9b3c-e692df33d940.png">
<br />
41 - Select "Password never expires" and "User cannot change password. <br/>
42 - Then select "Apply". <br/>
<img width="900" alt="46" src="https://user-images.githubusercontent.com/103763124/214128427-cd39d1d8-7d1b-4342-8b8a-04680369c9b0.png">
<br />
43 - Then select from the top tab "Member Of". Then select "Add". <br/>
<img width="900" alt="47" src="https://user-images.githubusercontent.com/103763124/214128903-ea92f2b1-919a-4aa7-8450-b791000df7a3.png">
<br />
44 - Select "Advanced". <br/>
<img width="900" alt="48" src="https://user-images.githubusercontent.com/103763124/214129124-91f0a4b1-bab9-4f60-ba56-3ffe528510f8.png">
<br />
45 - Select "Find Now". <br/>
<img width="960" alt="49" src="https://user-images.githubusercontent.com/103763124/214129420-c5a4aef1-aa9a-4ca4-b064-c96f86cad642.png">
<br />
46 - Now select the "Administrators" group. <br/>
<img width="900" alt="50" src="https://user-images.githubusercontent.com/103763124/214129728-28a7d84e-a8fd-4811-a1b0-65606af41e0b.png">
<br />
47 - Select "OK". <br/>
<img width="900" alt="51" src="https://user-images.githubusercontent.com/103763124/214129939-6bfb5486-7520-4c32-bb97-f313f1fa1430.png">
<br />
48 - Select "Apply" then "OK". <br/>
<img width="900" alt="53" src="https://user-images.githubusercontent.com/103763124/214130310-89d20b18-b368-43c3-8341-c3ec6a7c3a9e.png">
<br />
49 - Select the "helpdesk" account. <br/>
<img width="900 alt="54" src="https://user-images.githubusercontent.com/103763124/214130570-cc26fd84-5434-46a7-bd21-01ceb0c536f0.png">
<br />
50 - Select "Disable account" and the "Apply" then "OK". <br/>
<img width="900" alt="55" src="https://user-images.githubusercontent.com/103763124/214130843-27f68abb-e63f-4be3-b728-b4589daaabb5.png">
<br />
51 - Now select the "Groups" tab from the left column. Double click on "Remote Manamgement". <br/>
<img width="900" alt="58" src="https://user-images.githubusercontent.com/103763124/214133357-5b1c58c4-9920-44cc-a97e-ecc81418e6cd.png">
<br />
52 - Select "Add". <br/>
<img width="900" alt="59" src="https://user-images.githubusercontent.com/103763124/214133553-4d229889-9dd0-4a64-848b-893b65f6f599.png">
<br />
53 - Write "Jimmy" in the box then select "Check Names". Then select "OK". <br/>
<img width="900" alt="60" src="https://user-images.githubusercontent.com/103763124/214133801-d339f92a-f332-4f5a-bae0-cc7b836ad11b.png">
<br />
54 - Click on "Apply" then "OK". <br/>
55 - Then "sign out" of the Windows 10 PC. <br/>
<img width="900" alt="62" src="https://user-images.githubusercontent.com/103763124/214134065-d1f7f482-6f83-4544-8e80-bd6f7f92b312.png">
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

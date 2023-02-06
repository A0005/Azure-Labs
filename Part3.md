<h1>Part 3</h1>

[YouTube Demonstration by Kevtech IT Support](https://www.youtube.com/watch?v=nvaShp_XNh0)

<h2>Description</h2>
This project is about setting up a Static IP for the PC. Joining the Windows 10 PC to the domain. Creating a back up admin account and adding it to the Adminsistrators group.
Disabling the built-in account. Adding the user Jimmy to the Remote Management Users so we remote into his account. Changing some Group Policies. 
Remoting in as the domain admin helpdesk account. Creating a shared folder and mapping it to a drive. Logging in as a user.
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
50 - Select "Disable account" and then "Apply" then "OK". <br/>
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
<img width="900" alt="62" src="https://user-images.githubusercontent.com/103763124/214134065-d1f7f482-6f83-4544-8e80-bd6f7f92b312.png">
<br />
55 - Then "sign out" of the Windows 10 PC. <br/>
<img width="900" alt="63" src="https://user-images.githubusercontent.com/103763124/215957196-87d88d0a-b6fd-4a44-a080-4b53314dfb49.png">
<br />
56 - Go to the Server 2019 VM and open Server Manager. <br/>
<img width="900" alt="64" src="https://user-images.githubusercontent.com/103763124/215957314-cfbe4bfa-543f-4956-a3a9-6fd2cc76653c.png">
<br />
57 - Click on "Tools" from the top left then select "Group Policy Management". <br/>
<img width="900" alt="65" src="https://user-images.githubusercontent.com/103763124/215957583-7e589fbe-121c-4514-a857-b504029c716e.png">
<br />
58 - Expand "Forest" > "Domains" > "your domain name" > "Group Policy Objects" and select "Default Domain Controller Policy" then choose "Setting". <br/>
59 - If a "Trusted Sites" error pops up just add it. <br/>
<img width="900" alt="66" src="https://user-images.githubusercontent.com/103763124/215957916-d7a0c614-9e90-4511-820a-2ba4b16e7577.png">
<br />
60 -  Right Click on "Default Domain Controller Policy" then choose "Edit...". <br/>
<img width="900" alt="67" src="https://user-images.githubusercontent.com/103763124/215958542-dbc4b25a-6052-4618-a168-cf02673e02cf.png">
<br />
61 - In the "Computer Configuration" drop down menu expand "Policies" > "Windows Settings" > "Security Settings". <br/>
<img width="900" alt="68" src="https://user-images.githubusercontent.com/103763124/215958937-1ca79133-334a-4cfb-816d-8280e7568a17.png">
<br />
62 - Select "Account Policies" then "Account Lockout Policy". <br/>
63 - Here we are going to change how many times you get locked out. <br/>
64 - Select "Account lockout duration Properties" and set it to "10" minutes. Click "Apply" then "OK". <br/>
<img width="900" alt="84" src="https://user-images.githubusercontent.com/103763124/215959663-408bc372-ec36-4e3d-94bb-56cd49c6ab0c.png">
<br />
65 - Select "OK" again. <br/>
<img width="900" alt="85" src="https://user-images.githubusercontent.com/103763124/215959729-39ba5ec2-476a-4670-a108-a07a7f095f0b.png">
<br />
66 -  Now select "Account lockout threshold" and set it to 4 vaild attempts. Select "Apply" then "OK" <br/>
<img width="900" alt="88" src="https://user-images.githubusercontent.com/103763124/215960332-a1894b5e-869a-4d3e-a4d6-916be9ce2d92.png">
<br />
67 - Select "OK" again. <br/>
<img width="900" alt="89" src="https://user-images.githubusercontent.com/103763124/215960749-43c336c9-b33f-419a-a9cb-8674d91b5aef.png">
<br />
68 - Select "Reset account lockout counter after" and set it to "30" minutes. Select "Apply" then "OK" and "OK" again. <br/>
<img width="900" alt="93" src="https://user-images.githubusercontent.com/103763124/215961082-7ca2a6da-c624-415f-bec4-2abace50c3be.png">
<br />
69 - If select "Default Domain Policy" from the left column then "Settings" and scroll down you will see the policies that you changed. <br/>
<img width="900" alt="95" src="https://user-images.githubusercontent.com/103763124/215961834-bf1358bc-0d8e-4b3b-8bb1-c751f91696d8.png">
<br />
70  - Now right click on "Default Domain Policy" and select "Enforced". <br/>
<img width="900" alt="96" src="https://user-images.githubusercontent.com/103763124/216993237-af4d0c10-f976-4c5b-bf14-2216a608179d.png">
<br />
71  - Open CMD. <br/>
<img width="900" alt="98" src="https://user-images.githubusercontent.com/103763124/216993429-0dadcb14-9de2-491d-8997-0da0eed14dc9.png">
<br />
72  - Type in "gpupdate /force" and hit enter. <br/>
<img width="900" alt="99" src="https://user-images.githubusercontent.com/103763124/216993450-dae17363-ae44-4cf8-8936-1d86b70d3b52.png">
<br />
73  - Then type in "gpresults" and hit enter. <br/>
<img width="900" alt="100" src="https://user-images.githubusercontent.com/103763124/216993468-57d4961d-a678-488d-a463-e0235dba91f8.png">
<br />
74  - Then type in "gpresults /h HPReport.html" and hit enter. This is a way to download a report for the changes we made. <br/>
<img width="900" alt="101" src="https://user-images.githubusercontent.com/103763124/216993479-2038198d-7bef-4730-86d5-9d5e32907983.png">
<br />
75  - Open file explorer then the C drive. <br/>
<img width="900" alt="102" src="https://user-images.githubusercontent.com/103763124/216993501-ad4805ec-c42f-4c51-9e48-483e98e0c053.png">
<br />
76  - Click on "Users". <br/>
<img width="900" alt="103" src="https://user-images.githubusercontent.com/103763124/216993518-a31a51f4-960a-497c-8bdf-f7c703d24561.png">
<br />
77  - Then "helpdesk". <br/>
<img width="900" alt="104" src="https://user-images.githubusercontent.com/103763124/216995746-40bd2d92-6be6-4223-847f-4d89e393deb0.png">
<br />
78  - Then open the HPReport HTML Document. <br/>
<img width="900" alt="105" src="https://user-images.githubusercontent.com/103763124/216996239-a27af8a2-8d27-4826-bf2e-fde6f26c79d6.png">
<br />
79  - Select "OK" <br/>
<img width="900" alt="106" src="https://user-images.githubusercontent.com/103763124/216996261-e7557688-5885-42df-94a1-997bc96a5db7.png">
<br />
80  - Here you can see a report of the changes you did to the domains group policy. <br/>
<img width="900" alt="107" src="https://user-images.githubusercontent.com/103763124/216996275-a1563a1e-2429-4f9b-98e0-a307ccc3d042.png">
<br />
81  - Open "Server Manager" then select "File and Storage Services". Here we are going to create a shared folder. <br/>
<img width="900" alt="109" src="https://user-images.githubusercontent.com/103763124/216996305-144ec5cd-9b71-47df-9b2c-21ac032c4e2d.png">
<br />
82  - Select "Shares" then right click on the empty area and select "New Share...". <br/>
<img width="900" alt="201" src="https://user-images.githubusercontent.com/103763124/217001670-2f0f68aa-b76f-4176-9ccb-771b9ff8ab1a.png">
<br />
83  - Select "Next". <br/>
<img width="900" alt="202" src="https://user-images.githubusercontent.com/103763124/217002541-774b3431-1947-468f-b802-e1361988dc4a.png">
<br />
84  - Select "Next" again. <br/>
<img width="900" alt="203" src="https://user-images.githubusercontent.com/103763124/217002560-772ddd02-bfa9-4dae-b697-99e08a50e375.png">
<br />
85  - Called it your domain name and hit "Next". <br/>
<img width="900" alt="204" src="https://user-images.githubusercontent.com/103763124/217002572-31b484cb-24a7-4cb5-831a-fa74f13c99b2.png">
<br />
86  - Select "Next". <br/>
<img width="900" alt="205" src="https://user-images.githubusercontent.com/103763124/217002593-f098a87a-9226-4414-8348-e0c697c09016.png">
<br />
87  - Select "Next" again. <br/>
<img width="900" alt="206" src="https://user-images.githubusercontent.com/103763124/217002626-e384f250-46f4-4b0f-858a-714aba27126c.png">
<br />
88  - Select "Create". <br/>
<img width="900" alt="207" src="https://user-images.githubusercontent.com/103763124/217002644-18ff3bfe-7a8c-4ec7-8779-6c3b88c1eee8.png">
<br />
89  - Then "Close". <br/>
<img width="900" alt="208" src="https://user-images.githubusercontent.com/103763124/217002669-21ac0742-e23b-4084-bac7-d14013b870ed.png">
<br />
90  - Now open file explore. Then the C drive. <br/>
<img width="900" alt="209" src="https://user-images.githubusercontent.com/103763124/217002683-becb5f78-1f8a-4393-b77a-b938462141ed.png">
<br />
91  - Select "Shares". <br/>
<img width="900" alt="210" src="https://user-images.githubusercontent.com/103763124/217002703-b29f1b71-93d7-4a65-b449-54f650c6e293.png">
<br />
92  - Then select "your domain folder". <br/>
<img width="900" alt="211" src="https://user-images.githubusercontent.com/103763124/217004999-b4036d62-977e-4722-8bdf-07217a70a8a2.png">
<br />
93  -  Here "right click" then select "New" then "Folder". <br/>
<img width="900" alt="214" src="https://user-images.githubusercontent.com/103763124/217005115-332ad79e-4cc3-46c2-adb1-2844b384aa81.png">
<br />
94  - Name it "Home". <br/>
<img width="900" alt="215" src="https://user-images.githubusercontent.com/103763124/217005155-4c856246-8b86-410b-b3e6-31d7c3fbb86e.png">
<br />
95  - Right click the "Home" folder and select "Properties". <br/>
<img width="900" alt="216" src="https://user-images.githubusercontent.com/103763124/217005200-1a15d66b-39bc-4e26-b0f3-5885cabc111d.png">
<br />
96  - Select the "Sharing" tab. <br/>
<img width="900" alt="217" src="https://user-images.githubusercontent.com/103763124/217007182-ea610e0c-4f16-4757-aa8a-30aa4afba935.png">
<br />
97  - Then select "Advanced Sharing...". <br/>
<img width="900" alt="218" src="https://user-images.githubusercontent.com/103763124/217007207-e9751d13-9191-4130-847f-3989cce1cad2.png">
<br />
98  - Then check the box that says "Share this folder". Then select "OK". Now select the "Security" tab. <br/>
<img width="900" alt="219" src="https://user-images.githubusercontent.com/103763124/217007225-c758e1b6-41e4-4eb8-affa-255fd79c1195.png">
<br />
99  -  Select "Advanced". <br/>
<img width="900" alt="220" src="https://user-images.githubusercontent.com/103763124/217007261-bf80415c-171d-42af-8afc-b165520a05de.png">
<br />
100  -  Select "Disable inheritance". <br/>
<img width="900" alt="221" src="https://user-images.githubusercontent.com/103763124/217007277-4108a7a5-dcfa-4d8f-b519-bf5067928f55.png">
<br />
101  - Then choose the first one that says "Convert...". <br/>
<img width="900" alt="222" src="https://user-images.githubusercontent.com/103763124/217007295-b431bafb-de61-41fe-8716-d7651c4750d1.png">
<br />
102  - Select on "Users" then "Remove". <br/>
<img width="900" alt="223" src="https://user-images.githubusercontent.com/103763124/217007312-6ce0ef6c-73b0-4046-9678-49a0002c1cdd.png">
<br />
103  - Now select "Add". <br/>
<img width="900" alt="224" src="https://user-images.githubusercontent.com/103763124/217007323-f4427212-3cd0-4ba9-9f66-98bc30d12c53.png">
<br />
104  - Choose "Select a principle". <br/>
<img width="900" alt="225" src="https://user-images.githubusercontent.com/103763124/217007354-aee16326-dd51-4aae-9c82-45a923f44204.png">
<br />
105  - Enter in "Jimmy" the hit "Check Names" then choose "OK". <br/>
<img width="900" alt="226" src="https://user-images.githubusercontent.com/103763124/217007369-474a41a3-74b9-40d8-82e2-d96cb1fc7c86.png">
<br />
106  - Check the box that says "Modify" then select "OK". <br/>
<img width="900" alt="227" src="https://user-images.githubusercontent.com/103763124/217007381-374b1924-7f19-49d1-b5cc-ae13e3c9f545.png">
<br />
107  - Select "Apply" then "OK". <br/>
<img width="900" alt="228" src="https://user-images.githubusercontent.com/103763124/217007398-b276f1f9-c533-4f67-84ae-f07585497ab9.png">
<br />
108  - Select the "Sharing" tab then "Share...". <br/>
<img width="900" alt="229" src="https://user-images.githubusercontent.com/103763124/217007418-301fcaff-a51b-4e88-8e79-5e86a98fb2b8.png">
<br />
109  - Select on the drop down arrow on Jimmy’s "Permission Level" and choose "Read/Write". <br/>
<img width="900" alt="230" src="https://user-images.githubusercontent.com/103763124/217008291-8a3f25a2-4bcd-4087-b41c-e33475e506f3.png">
<br />
110  - Then select "Share". <br/>
<img width="900" alt="231" src="https://user-images.githubusercontent.com/103763124/217014127-88919ff7-30b0-4e1b-9c41-f2b5e12bc378.png">
<br />
111  - Then select "Done". <br/>
<img width="900" alt="232" src="https://user-images.githubusercontent.com/103763124/217014183-3023ca4b-68d2-4dd1-abd5-5fd1c1148c10.png">
<br />
112  - Copy the "Network Path:". <br/>
<img width="900" alt="233" src="https://user-images.githubusercontent.com/103763124/217014200-80b5ffc7-699e-4f4f-b028-7a360ff8cfa5.png">
<br />
113  - Open "Active Directory Users and Computers".  <br/>
<img width="900" alt="234" src="https://user-images.githubusercontent.com/103763124/217014215-7fc001e5-1c83-4194-95f3-6078d65a7dcb.png">
<br />
114  - Select on "Users" then "Jimmy" and select the "Profile" tab. <br/>
<img width="900" alt="235" src="https://user-images.githubusercontent.com/103763124/217022989-de855727-0464-4e7c-824e-a97a76a5f449.png">
<br />
115  - For "Connect" choose the H drive and paste in the Network Path that you previously copied. <br/>
<img width="900" alt="238" src="https://user-images.githubusercontent.com/103763124/217014308-9c84e172-55dc-4e98-8f73-2314834089b3.png">
<br />
116  - Select "Apply" then "Yes" then "OK". <br/>
<img width="900" alt="239" src="https://user-images.githubusercontent.com/103763124/217014378-069c2719-fbbb-44f2-a2bd-23f28178d0da.png">
<br />
117  - Now remote in into the Windows 10 PC and log in with Jimmy’s credentials. <br/>
<img width="900" alt="241" src="https://user-images.githubusercontent.com/103763124/217024307-e27622ca-3755-433e-a9b6-c494fc51fcdd.png">
<br />
118  - Open the File Explore then select "This PC" and you will see the shared drive. Open the shared drive which is the H drive. <br/>
<img width="900" alt="242" src="https://user-images.githubusercontent.com/103763124/217024281-d15b907e-38c2-458c-ac60-a97d0a924b98.png">
<br />
119  - Right Click and select "New" then "Text Document". <br/>
<img width="900" alt="243" src="https://user-images.githubusercontent.com/103763124/217024300-73ff1812-9012-474b-bc66-08dae9aa892c.png">
<br />
120  - Name it "Test". <br/>
<img width="900" alt="244" src="https://user-images.githubusercontent.com/103763124/217024335-031c2a77-2793-4481-822a-5147143b308c.png">
<br />
121  - Now if you go back the server and open the shared folder that was called "Home" you will see the "Test" document also available. <br/>
<img width="900" alt="245" src="https://user-images.githubusercontent.com/103763124/217024367-032b6841-75e2-4b4c-bb55-870f8ec435ed.png">
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

<h1>Part 1</h1>

[YouTube Demonstration by Kevtech IT Support](https://www.youtube.com/watch?v=jXTQcp44Oqs)

<h2>Description</h2>
This project is about installing Windows Server 2019 and Windows 10 using Azure Virtual Machines.
<br />


<h2>Environments Used </h2>

- <b>Azure VM</b>
- <b>Windows Server 2019</b>
- <b>Windows 10</b>

<h2>Program walk-through:</h2>

<!-- <p align="center"> --!>
1 - First step is to create a free Azure account. <br/>
2 - After creating your Azure account you can select home on the left panel. <br/>
3 - Then select Virtual machines. <br/>
<img width="900" alt="Click Virtual Machines" src="https://user-images.githubusercontent.com/103763124/211358766-358348ea-e2fc-4e13-9ae8-3d1ff6030140.png">
<br />
4	- Select the Create drop down menu. <br/>
5 - Then select Create a virtual machine hosted by Azure. <br/>
<img width="900" alt="Azure Virtual Machine" src="https://user-images.githubusercontent.com/103763124/211360798-2389803e-a3c5-45e4-b87f-b4ec372b558a.png">
<br />
6	- Select Create new resources group and name it "HomeLab" and select OK.  <br/>
<img width="900" alt="Create resource group" src="https://user-images.githubusercontent.com/103763124/211361617-1f9645c1-c3cd-48d6-a46c-f87d0c8bd846.png">
<br />
7 - Name your virtual machine "Server2019". <br/>
8 - For image select "Windows Server 2019 Datacenter -x64 Gen2". <br/>
9 - Size keep default "Standard_D2s_v3 - 2vcpus, 8 GiB memory ($137.24/month)". <br/>
<img width="900" alt="Replace 4" src="https://user-images.githubusercontent.com/103763124/213251475-34a0bb9f-ff62-4d47-9e48-b2a1f8b0a78d.png">
<br />
10 - Create your Administrator account. Give it a username and password. <br/>
<img width="900" alt="Create account" src="https://user-images.githubusercontent.com/103763124/211364147-4a037090-eda0-43fe-beba-983a6cbf12d0.png"> 
<br />
11 - Select Review + create. <br/>
<img width="900" alt="Review and create" src="https://user-images.githubusercontent.com/103763124/211364931-fd870385-f333-463b-83b3-149aa617204e.png"> 
<br />
12 - As it continues to create the "Server2019" in the background, go back to Home on the left panel then select Virtual machines to create another virtual machine hosted by Azure. <br/>
<img width="900" alt="Create virtual machine again" src="https://user-images.githubusercontent.com/103763124/211366023-7982c292-7570-478f-ad04-868d3e723bad.png">
<br />
13 - Select your resource group "HomeLab". <br/>
14 - Name your virtual machine "Windows10". <br/>
15 - Change the region to "(US) East US 2". <br/>
16 - For the Image choose "Windows 10 Pro, version 21H2 -x64 Gen2". <br/>
<img width="900" alt="Windows 10" src="https://user-images.githubusercontent.com/103763124/211367515-6aa43809-a9c6-4068-9a87-0a06681ccb32.png">
<br />
17 - Create your Administrator account. Give it a username and password. <br/>
<img width="900" alt="Create windows account" src="https://user-images.githubusercontent.com/103763124/211368489-8c090662-c409-457b-8afc-ee1fffd8be7a.png">
<br />
18 - Remember to confirm the Licensing at the bottom before selecting Review + create. <br/>
<img width="900" alt="Remember to confrim and create" src="https://user-images.githubusercontent.com/103763124/211369044-bb6fa721-3c07-485a-9d13-ca1517a43fce.png">
<br />
19 - Then select Create. <br/>
<img width="900" alt="Create windows 10" src="https://user-images.githubusercontent.com/103763124/211369543-9e186acf-d434-4a8b-9c95-969992811924.png">
20 - Go back to Home on the left panel then select Virtual machines and select "Server2019". <br/>
<img width="900" alt="Home then Vitual machine select 2019" src="https://user-images.githubusercontent.com/103763124/211370314-56fd3b2a-2550-40d7-ad65-d1b0ca8d0cfa.png">
<br />
21 - Then click on the "Connect" drop down panel then select "RDP". <br/>
<img width="900" alt="Select connect then RDP" src="https://user-images.githubusercontent.com/103763124/211369760-d4e28806-0717-49fa-adf2-6a205c81137c.png">
<br />
22 - Select Download RDP File. <br/>
<img width="900" alt="Download RDP file" src="https://user-images.githubusercontent.com/103763124/211370954-8c7f3889-4a82-4eae-b9b6-003defbfe472.png">
23 - Next open the RDP file you just downloaded. <br/>
24 - This step is for those doing this lab on a MacOS you will need to download a Microsoft RDP app from the Apple Store so you can open this file. <br/>
<img width="900" alt="Open downloaded file" src="https://user-images.githubusercontent.com/103763124/211371454-32562ffa-7002-4d60-893e-d9168b88a915.png">
<br />
25 - This the screen you get after successfully entering your username and password for the adminstrator account you create for the "Server2019" virtual machine. <br/>
<img width="900" alt="After connecting" src="https://user-images.githubusercontent.com/103763124/211372328-ba322cad-1e6e-49f9-bb2c-ec904c447474.png">
<br />
26 - Search systems on the search tab then select About your PC. <br/>
<img width="900" alt="Search systems properties" src="https://user-images.githubusercontent.com/103763124/211372826-3d0b6491-ae99-4c1e-8b43-7b0eb3dfc36b.png">
27 - Select Rename this PC and rename it to whatever you want. After that you get a prompt to restart your PC now you can select it. <br/> 
<img width="900" alt="Click rename " src="https://user-images.githubusercontent.com/103763124/211373708-f5c2c5d5-caa7-4801-bd6e-983e7b0cfaf3.png">
<br />
28 - As the "Server2019" VM restarts. Go back to your Azure portal and select Home on the left panel then Select Virtual machines and choose "Windows10". <br/>
<img width="900" alt="Home then windows 10" src="https://user-images.githubusercontent.com/103763124/211374279-335004f6-202c-444b-a149-ab2e14c9dcdc.png">
<br />
29 - Then click on the "Connect" drop down panel then select "RDP". <br/>
<img width="900" alt="connect then rdp into it " src="https://user-images.githubusercontent.com/103763124/211374501-2ecea517-11b6-48e7-ba40-54ea629a8913.png">
<br />
30 - Select Download RDP File. <br/>
<img width="900" alt="download the file " src="https://user-images.githubusercontent.com/103763124/211375261-31c7741c-f237-4cd1-8ede-0d0a592753a5.png">
<br />
31 - After opening the file you just downloaded and entered the administrator acccount username and password for the "Windows10" VM deselect all options and click on accept at the bottom. <br/>
<img width="900" alt="Deselect and accept" src="https://user-images.githubusercontent.com/103763124/211375607-450128d6-b063-4b23-b5d7-17d95bf259c9.png">
<br />
32 - Once again search systems on the search tab and select About your PC. Then select Rename this PC and rename it as you want. After that restart the PC. <br/>
<img width="900" alt="Rename the computer" src="https://user-images.githubusercontent.com/103763124/211376182-18b86d9f-0e9f-4aa0-bb8c-00b9377e13c4.png">
<br />
33 - After the PC restarts lauch the Microsoft Edge Web Browser and search "Google.com". <br/>
<img width="900" alt="1" src="https://user-images.githubusercontent.com/103763124/213265990-8ff549a6-9f1c-4c35-898b-8f7238ce74b0.png">
<br />
34 - In the Google search bar type " rsat tools download windows 10" and hit "Enter". <br/>
<img width="900 alt="2" src="https://user-images.githubusercontent.com/103763124/213266340-724ce4fc-8d65-440c-9c62-51e239f9ca9f.png">
<br />
35 - Select the first search result you get. <br/>
<img width="900" alt="3" src="https://user-images.githubusercontent.com/103763124/213266522-3331d963-df57-4b25-a844-ac575e84bafa.png">
<br />
36 - Click "Download". <br/>
<img width="900" alt="4" src="https://user-images.githubusercontent.com/103763124/213266710-3263cc0c-07b3-4a6f-9834-fc0fc3f2952a.png">
<br />
37 - Select "WindowsTH-KB2693643-x64.msu" basically 64 bit version. Then click "Next". <br/>
<img width="900" alt="5" src="https://user-images.githubusercontent.com/103763124/213267204-3b97c38c-00bb-4566-96af-ed0f9ae08f8c.png">
<br />
38 - After the download completes. Navigate to your File Explore on the taskbar and open the Downloads folder. <br/>
<img width="900" alt="6" src="https://user-images.githubusercontent.com/103763124/213267502-875ded73-40e6-469a-b3e9-2eac2836ba39.png">
<br />
39 - Select the RSAT tool you just downloaded. <br/>
<img width="900" alt="7" src="https://user-images.githubusercontent.com/103763124/213267709-d671bfb4-0a90-429b-a0e7-f828d69aacb6.png">
<br />
40 - Click "Yes". <br/>
<img width="900" alt="8" src="https://user-images.githubusercontent.com/103763124/213267874-d536621e-d2b3-409c-8dc4-bbf772b0dd0b.png">
<br />
41 - Select " I Accept". <br/>
<img width="900" alt="9" src="https://user-images.githubusercontent.com/103763124/213268033-ce20309d-36d1-4448-a0b7-cd81dc0be467.png">
<br />
42 - Select "Close". <br/>
<img width="900" alt="10" src="https://user-images.githubusercontent.com/103763124/213268235-e8d4a1ac-95ce-47e1-af54-48b0f37c6913.png">
<br />
43 - Select the "Start Tab". Scroll down to a folder called "Windows Administrative Tools" and expand it too see if the RSAT Tools were actually installed. <br/>
<img width="900" alt="11" src="https://user-images.githubusercontent.com/103763124/213268588-d6adaa87-7091-4b50-ba44-e4e7daee19cf.png">
<br />
44 - Now this the most important step which is stopping the VMs. Go back to your Azure portal. Select Home from the left panel then Virtual machines. Then select both VMs. <br/>
<img width="900" alt="Home and virtual lab then select both" src="https://user-images.githubusercontent.com/103763124/211376605-24aed6be-dbb8-4b51-9e24-b78b8c1ea03a.png">
<br />
45 - Select "Stop" from the top navigation bar. Then select "Yes" to confirm. <br/>
<img width="900" alt="Select yes" src="https://user-images.githubusercontent.com/103763124/211376628-81056248-0e75-4be4-9246-daabfab8cf1f.png">
46 - This is the confirmation after stopping your VMs. Status says "Stopped (deallocated)". <br/>
<img width="900" alt="Confirmed stopped" src="https://user-images.githubusercontent.com/103763124/211376596-4da32410-6328-4750-b98d-04c7e612dc87.png">
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

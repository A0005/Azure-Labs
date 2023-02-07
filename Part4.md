<h1>Part 4</h>

[YouTube Demonstration by Kevtech IT Support](https://www.youtube.com/watch?v=RnJKaE26zHw)

<h2>Description</h2>
This project is about troubleshooting a users locked out account, disabled account, and expired account. Created a logon hours policy.
<br />


<h2>Environments Used </h2>

- <b>Azure VM</b>
- <b>Windows Server 2019</b>
- <b>Windows 10</b>

<h2>Program walk-through:</h2>

<!-- <p align="center"> --!>
1 - First step is to log in to your azure portal and start the Server 2019 VM and Windows 10 VM. <br/>
2 - Here is an error message after the user "Jimmy" entered multiple incorrect passwords trying to log on. <br/>
<img width="900" alt="1" src="https://user-images.githubusercontent.com/103763124/217299495-b97c5fc8-5fe9-4875-a556-92c513f2a8ca.png">
<br />
3	- Switch to the Server 2019 and open "Active Directory Users and Computers". Select "Users" folder and then "Jimmy" <br/>
<img width="900" alt="3" src="https://user-images.githubusercontent.com/103763124/217302322-1ca3d9d0-02ae-46c6-b74f-6b6511daeffb.png">
<br />
4	- Select the "Account" tab and uncheck the box that says "Unlock account. This account is currently locked out on this Active Directory Domain Controller". <br/>
5 - Then select "Apply" and "OK". <br/>
<img width="900" alt="4" src="https://user-images.githubusercontent.com/103763124/217299567-d2c7ff0d-0acf-4230-aeec-610b7afdfd2f.png">
<br />
6 - Now "Jimmy" is able to login. <br/>
<img width="900" alt="6" src="https://user-images.githubusercontent.com/103763124/217299606-8c6c93c6-3dd9-4544-8587-99cf03b3489f.png">
<br />
7 - Now lets disable his account. Right click on "Jimmy" name and select "Disable Account". <br/>
<img width="900" alt="7" src="https://user-images.githubusercontent.com/103763124/217299629-8c1a175d-cc63-44f7-beab-b4cfbb55f5d0.png">
<br />
8 - Confirmation that his account has been disabled. <br/>
<img width="900" alt="8" src="https://user-images.githubusercontent.com/103763124/217299648-a6fc53e5-fc09-42e1-93f4-85486854a46a.png">
<br />
9 - When "Jimmy" tries to log in he is unable to. <br/>
<img width="900" alt="9" src="https://user-images.githubusercontent.com/103763124/217299684-3dba7933-00a5-482c-a14c-7e9267ec56c1.png">
<br />
10 - To solve this issue on the Server right click on "Jimmy’s" name and select "Enable Account". <br/>
<img width="900" alt="10" src="https://user-images.githubusercontent.com/103763124/217299722-48ca3753-4268-4bb1-86d5-386fcd0eb686.png">
<br />
11 - Confirmation that "Jimmy's" account has been enabled. <br/>
<img width="900" alt="11" src="https://user-images.githubusercontent.com/103763124/217306202-f8ad8ab5-48cc-404a-9338-ae1f2846ace3.png">
<br />
12 - Now lets reset "Jimmy’s" password. Right click on "Jimmy" and select "Reset Password...". <br/>
<img width="900" alt="12" src="https://user-images.githubusercontent.com/103763124/217306221-1b8967fc-0786-46a3-a10a-9fbdbc1c84ab.png">
<br />
13 - Give "Jimmy" a need password and uncheck the box that says "User must change password at next logon" and select "OK". <br/>
<img width="900" alt="13" src="https://user-images.githubusercontent.com/103763124/217306246-2e2ffce4-3ef0-494e-a845-fd7e42e6d1bd.png">
<br />
14 - Confirmation that "Jimmy's" password has been changed. <br/>
<img width="900" alt="14" src="https://user-images.githubusercontent.com/103763124/217306280-4d8e1940-e29e-44f0-8b3e-5bc643b57d8a.png">
<br />
15 - When you give Jimmy his new password he is able to log on with it. <br/>
<img width="900" alt="15" src="https://user-images.githubusercontent.com/103763124/217306308-19ab0b70-79d5-4aeb-9012-c1a6eb747e61.png">
<img width="989" alt="18" src="https://user-images.githubusercontent.com/103763124/217318445-0a7b54e8-046f-4650-9dd9-1f5b5d446fab.png">
<br />
16 - Now lets expire "Jimmy's" account. On Jimmy’s properties select the "Account" tab at the bottom where it says "Account expires" check the box "End of:" and set it to 12/1/22. Then select "Apply" and "OK". <br/>
<img width="900" alt="20" src="https://user-images.githubusercontent.com/103763124/217318991-b21a09f1-ae00-4652-8914-4f9f77650066.png">
<br />
17 - Here is the error "Jimmy" gets because his account has expired. <br/>
<img width="900" alt="21" src="https://user-images.githubusercontent.com/103763124/217319007-56bc712d-ac6f-4301-9441-78b15ec966e3.png">
<br />
18 -  Now go back to "Jimmy's" properties and set the "Account expires" to "Never". Then select the option box that says "Logon Hours...". <br/>
<img width="900" alt="22" src="https://user-images.githubusercontent.com/103763124/217319018-8728829d-2970-45df-96b4-ec83c35cbda8.png">
<br />
19 - Here select the whole section of your current day that you are doing this lab and click on the button that says "Logon Denied". <br/>
<img width="900" alt="23" src="https://user-images.githubusercontent.com/103763124/217319040-064aff25-3812-4948-8c2d-dd27ea22b923.png">
<br />
20 - Select "Apply" and "OK". <br/> 
<img width="900" alt="24" src="https://user-images.githubusercontent.com/103763124/217319062-58a64cef-8dd9-45e3-a07f-cab28044003c.png">
<br />
21 - When "Jimmy" tries to logon on a certain day he is unable to and gets this error. <br/>
<img width="900" alt="25" src="https://user-images.githubusercontent.com/103763124/217319083-90ced0b9-3919-4e52-897d-18abe4cfa0ed.png">
<br />
22 - Make sure to go back and select the day that you previous denied "Jimmy" and this time click on the button that says "Logon Permitted". <br/>
23 - Select "Apply" and "OK". <br/>
<img width="900" alt="26" src="https://user-images.githubusercontent.com/103763124/217319119-160c4fdf-3cb8-43be-a23c-00c4013cb328.png">
<br />
30 - Finally when "Jimmy" tries to log back in he is able to. <br/>
<img width="900" alt="28" src="https://user-images.githubusercontent.com/103763124/217319153-14829a73-8a5d-4e92-b3e1-5eb258db9bc8.png">
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

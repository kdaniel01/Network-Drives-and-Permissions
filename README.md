<img src="https://i.imgur.com/yJVkMdW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />


<h2>Description</h2>

<b>In this project,I created network shared drive and folders in which I granted access according to the user's role.
</b>


<h2>Environments and Technologies Used</h2>

- <b> Oracle Virtual Box<br /> 
- <b> Virtual Machine (Windows Server 2022)<br /> 
- <b> Virtual Machine (Windows 10 Pro)<br />
- <b> Active Directory Domain Services<br />


<h2>Overview </h2>
- <b>Part 1- Creating 2 Groups with 2 users each in Active Directory<br />
- <b>Part 2- Creating Network shared drive and folders<br />
- <b>Part 3- Adding home folder for users and then testing access<br />
 
 
<h2>Part 1- Creating 2 Groups with 2 users each in Active Directory Users and Computers:</h2>

<p align="center">
I created 2 groups which will represent Departments in the Tunetech organization. The Finance Department and HR Department group was created with 2 users each.
Finance Department-(Ben Jones- Financial A
HR Department- (Jen White- HR Assistant, Sarah John- HR Manager)
<br />
<img src="https://i.imgur.com/6WAB1sj.png" height="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/DiKiXii.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/qdQH6Zt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/H8g73Ch.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/yPspilD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/dVNz4qb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/ZIhksYb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<h2>Part 2- Creating Network shared drive and folders:</h2>

<p align="center">
Created Tunetech folder on the C: drive of the DC-1 Server. Shared that folder with both groups and specified the drive letter for the connection as T: Drive.<br />
<img src="https://i.imgur.com/lLHs5Cb.png" height="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Cfk3yY1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/aTOOgON.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/xLcbaK9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/M2HCGF1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<p align="center">
Mapped Tunetech folder by right clicking Network > Map network drive.Then specified T: Drive and folder path \\dc-1\tunetech.<br/>
<img src="https://i.imgur.com/BTWziAZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/fc1dDK5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/zLwSthv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />


<p align="center">
The inheritted permissions that HR Dept to Finance folder was removed and vice versa for the Finance folde right clicking Finance folder > properties > security > advanced >select HR Dept > disable inheritence > convert inherited permissions into explicit permissions on this object > then remove HR group.<br/>
<img src="https://i.imgur.com/DO23iHj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/p6PKdG3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/HoGuRws.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/rWbplz2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/cWZBfrT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<p align="center">
Creating explicit permissions for users according to their role. As we can, Rick Henderson(Finance Manger) would have been able to access the Financial Assistant folder but access was configured to only grant Ben Jones(Financial Assistant) access which he only has read but no write access to this folder. This was done for all users and there respected folder. Mangers were granted full control of their folder which includes read and write functions.<br/>
<img src="https://i.imgur.com/cWZBfrT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/jGHF5wh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/9CZJucZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
<br />
<h2>Part 3- Adding home folder for users and then testing access:</h2>

<p align="center">
Added home folder path in AD for each user then tested their access levels.<br />
<img src="https://i.imgur.com/1JiL8Ii.png" height="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/61pFQjt.png" height="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<p align="center">
We can see Rick only sees Finance Dept Folder and not HR Dept. Rick only can see the FInance Manager folder and not the Financial Assistant folder. Rick also created a new folder in the Finance Manager Folder called Budget but is not able to outside of that folder.<br />
<img src="https://i.imgur.com/fxccNPh.png" height="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/fzEwmcL.png" height="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/L1uqlrJ.png" height="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<p align="center">
Jen the HR assistant only has read acces and is not able to edit or create folders or files..<br />
<img src="https://i.imgur.com/mKZIwSF.png" height="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/jpo3tRI.png" height="80%" alt="Disk Sanitization Steps"/>
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

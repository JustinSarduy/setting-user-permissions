<h1>Creating Netowrk Files and Setting Permissions for Users within Azure VM's</h1>
In this tutorial, we will be creating network files and setting permissions for users as Admin in our Direct Controller Virtual Machine. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory
  

<h2>Operating Systems Used </h2>

- Windows (Windows 10 Pro)
- Windows (Windows Server 2022 Datacenter Azure Edition)

<h2>High-Level Steps (Pt.1)</h2>

- Step 1: Use Remote Desktop.
- Step 2: Use Admin to log into Dc (Domain Controller) Virtual Machine.
- Step 3: On this VM, create four folders within the C:\ drive.
- Step 4: Name the four drives as the following: "read-access", "write-access", "no-access", "accounting".
- Step 5: Once created we will be creating permissions in each invidual file.
- Step 6: In the "read-access" file, right click the file and click on "Properties", once in Properties, open up "Sharing" then "Share".
- Step 7: In the search bar, type "domain users" and then click "Add", this should drop "Domain Users" down below.
- Step 8: On the right side of the "Domain Users" there will a "Read" and down arrow, click that and it will open to where you can choose differnt options.
- Step 9: Make sure to click "Read" then after click "Share" at the bottom and then you will be done with that folder.
- Step 10: The steps will be the same for the "write-access" folder excpet at the end where you select "Read/Write" permission instead of "Read".
- Step 11: Same steps apply for the "no-acccess" folder untill you get to the search bar, add "domain admins" instead of users. Once added set permissions to "Read/Write" and share.
- Step 12: Skip "accounting" folder for now.

  <h2>High-Level Steps (Pt.2)</h2>
- Step 1: Use Remote Desktop and open another VM.
- Step 2: This time we will login as a random user from our Active Directory (can be any random user)
- Step 3: Once logged in as the user, we will test to see if we can access the files that we created earlier.
- Step 4: Open file explorer and type in search bar "\\dc-1" since the other VM is called dc-1, it may be different for others. As long as the name is the same as the other VM where we created the files.
- Step 5: When searched, our folders that we created and other default folders, should be seen.
- Step 6: If you click on the "read-access" folder, you will see you can see and read in the folder, but if you try creating a text it will pop up saying you need permission.
- Step 7: In the the "write-access" folder, you will be able to read and write in that folder since we put the "read/write" permission as an Admin
- Step 8: Lastly, if you try to click on the "no-access" folder, it should prevent you from accessing the folder completely 


<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img width="474" height="177" alt="image" src="https://github.com/user-attachments/assets/572d6558-4bb4-485d-b743-1b5e31c291b1" />
<h1>Creating Network Files and Setting Permissions for Users within Azure VM's</h1>
In this tutorial, we will be creating network files and setting permissions for users as Admin in our Direct Controller Virtual Machine. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory
  

<h2>Operating Systems Used </h2>

- Windows (Windows 10 Pro)
- Windows (Windows Server 2022 Datacenter Azure Edition)

<h2> Steps and Observation (Pt.1)</h2>

- Step 1: Use Remote Desktop.
- Step 2: Use Admin to log into Dc (Domain Controller) Virtual Machine.
- Step 3: On this VM, create three folders within the C:\ drive.
- Step 4: Name the three drives as the following: "read-access", "write-access", "no-access", "accounting".
- Step 5: Once created we will be creating permissions in each invidual file.
- Step 6: In the "read-access" file, right click the file and click on "Properties", once in Properties, open up "Sharing" then "Share".
 
  <img width="349" height="356" alt="Screenshot 2025-08-20 163827" src="https://github.com/user-attachments/assets/53ae8b85-eaf6-48ea-b251-43fa06390fdc" />
</p>
<p> As shown in the image, once the "read-access" file has been created, you will see different tabs but at the bottom there will be "Properties". Properties is where you will be able to set permissions for users in the 
system.
<br />

  
- Step 7: In the search bar, type "domain users" and then click "Add", this should drop "Domain Users" down below.
- Step 8: On the right side of the "Domain Users" there will a "Read" and down arrow, click that and it will open to where you can choose differnt options.
  
  <img width="541" height="274" alt="Screenshot 2025-08-20 165303" src="https://github.com/user-attachments/assets/e7df53da-c595-441a-af9c-bf92da02c821" />
Once you click "Properties" the image above will be shown on your sceen. There will be different tabs to go through, but the one that we will go through is the "Share" tab. The reason why we share is for the people that are on our network and will be able to see the files we create.

- Step 9: Make sure to click "Read" then after click "Share" at the bottom and then you will be done with that folder.
- Step 10: The steps will be the same for the "write-access" folder except at the end where you select "Read/Write" instead of "Read".
  
  <img width="526" height="145" alt="Screenshot 2025-08-20 170330" src="https://github.com/user-attachments/assets/8559dc0b-5224-4b92-8c74-48def8b6cf55" />

- Step 11: Same steps apply for the "no-acccess" folder untill you get to the search bar, add "domain admins" instead of users. Once added set permissions to "Read/Write" and share.

  <h2>High-Level Steps (Pt.2)</h2>
- Step 1: Use Remote Desktop and open another VM.
- Step 2: This time we will login as a random user from our Active Directory (can be any random user).
- Step 3: Once logged in as the user, we will test to see if we can access the files that we created earlier.
- Step 4: Open file explorer and type in search bar "\\dc-1" since the other VM is called dc-1, it may be different for others. As long as the name is the same as the other VM where we created the files.
 <img width="1005" height="267" alt="Screenshot 2025-08-20 171312" src="https://github.com/user-attachments/assets/d5e1a71a-f048-4260-a9f5-408ffbe5f2e2" />

- Step 5: When searched, our folders that we created and other default folders, should be seen as below.

   <img width="774" height="202" alt="Screenshot 2025-08-20 171653" src="https://github.com/user-attachments/assets/08e65b8c-018a-4972-8050-83357e9d4815" />

- Step 6: If you click on the "read-access" folder, you will see you can see and read in the folder, but if you try creating a text it will pop up saying you need permission.

   <img width="438" height="216" alt="Screenshot 2025-08-20 172444" src="https://github.com/user-attachments/assets/38316ab8-72fe-4c4a-a7a4-c60dab5d1545" />

- Step 7: In the the "write-access" folder, you will be able to read and write in that folder since we put the "read/write" permission as an Admin.

   <img width="831" height="549" alt="Screenshot 2025-08-20 172433" src="https://github.com/user-attachments/assets/b52b9448-517b-4149-9b2e-10d87f0c555c" />

- Step 8: Lastly, if you try to click on the "no-access" folder, it should prevent you from accessing the folder completely

   <img width="474" height="175" alt="Screenshot 2025-08-20 173152" src="https://github.com/user-attachments/assets/844bcd8f-751f-4d67-8984-90e27eb190c2" />







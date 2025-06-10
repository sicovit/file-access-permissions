# file-access-permissions
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Configuring User File Access and Permissions in Active Directory</h1>
Basic Guide to Managing File Access with Active Directory Users and Groups.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure
- Remote Desktop
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Key Steps to Set Up File Access Control in AD</h2>

-  Create a Shared Folder
-  Set NTFS (File System) Permissions
-  Verify Access from a Domain-Joined Client
-  (Optional) Add Users to AD Security Groups

<h2>Configuration</h2>

<p>
<img src="https://github.com/user-attachments/assets/7a50b7fe-9786-4fe3-9b24-767974785ee0" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To set up file access for users in Active Directory, first connect to your Windows Server through Remote Desktop. Create or choose a folder you want to share, then right-click it, go to Properties, and turn on sharing in the Sharing tab.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/2fdaf052-672c-4630-8339-fbc214893164" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, go to the Security tab to set permissions—this controls what users can do with the folder, like view, edit, or delete files. It’s best to create a security group in Active Directory, add your users to that group, and then give the group the correct permissions on the folder instead of assigning them one by one. This makes managing access much easier, especially as more users are added.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/7781b2d1-0b6b-47b2-9343-cb24448e868c" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 You can also use Group Policy to map shared folders to users’ computers automatically when they log in, so they don’t have to search for the folder themselves. With this setup, file access is secure, organized, and easy to manage across your network.
</p>
<br />

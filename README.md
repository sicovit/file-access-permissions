# file-access-permissions
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Managing Shared Folder Permissions Using Active Directory</h1>
How to Set Up Network Shares and Permissions with Active Directory.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure
- Remote Desktop
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Key Steps for Network File Shares and Permissions in AD</h2>

-  Create a Shared Folder
-  Set NTFS (File System) Permissions
-  Verify Access from a Domain-Joined Client
-  (Optional) Add Users to AD Security Groups

<h2>Configuration</h2>

<p>
<img src="https://github.com/user-attachments/assets/7a50b7fe-9786-4fe3-9b24-767974785ee0" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Start by connecting to your Windows Server through Remote Desktop. Choose or create a folder you want to share over the network, then right-click it, go to Properties, and enable sharing under the Sharing tab by selecting Advanced Sharing. Give the shared folder a name and adjust the basic share permissions to allow users to read or change files.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/2fdaf052-672c-4630-8339-fbc214893164" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After that, go to the Security tab to configure NTFS permissions, which control more detailed access, like who can open, modify, or delete files. It's recommended to create an Active Directory security group, add your users to it, and assign permissions to that group instead of individual users. This makes permission management much easier and more scalable.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/7781b2d1-0b6b-47b2-9343-cb24448e868c" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Use Group Policy to automatically map the network share to users’ computers when they log in, so they can access it without having to manually browse the network. With this setup, users can securely access shared folders over the network with the correct level of permission.
</p>
<br />

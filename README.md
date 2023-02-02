
Configuring  Active Directory within Azure VMs
<h2>Creating Active Directory</h2>


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Microsoft configuration
- Various Network Protocols  (DNS, HTTP/S, ICMP)


<h2>Operating Systems Used </h2>

- Windows 2022 (Server)
- Windows 10 (Client)

<h2>High-Level Steps</h2>

- Step 1 Resource group/Network Interface 
- Step 2 Creation of Active Directory
- Step 3 DNS serivce
- Step 4 Client Integration

<h2>Actions and Observations</h2>

<h1>Static IP</h1>
<p>
<img src="https://i.imgur.com/BJnw61g.png" height="80%" width="80%" alt="Static IP configuration Steps"/>
</p>
<p>
After creating a Domain Controller (Server) and Windows 10(Client's) VM in azure under the same VNet, change the Controller's NIC Private
 IP Address from dynamic to Static.
</p>
<br />
<h1>Active Directory and Domain Service as a Role</h1>

<p>
<img src="https://i.imgur.com/TmGNTPE.png" height="80%" width="80%" alt="Adding Active Directory Feature Steps"/>
</p>
<p>[
](https://i.imgur.com/WQS0gJJ.png) After installing Active Directory, add features from Server Manager. 
</p>
<br />

<h1>Fully qualified Domain naming</h1>
<p>
<img src="https://i.imgur.com/GEIyFkb.png" height="80%" width="80%" alt="DNS Configuration Steps"/>
</p>
<p>
DNS Configuration
</p>Login to the Domain Controller (Remote Desktop) and verify Client shows up in Active Directory Users and Computers (ADUC) inside the “Computers” container on the root of the domain 


</p>
<h1>  Create Active Directory</h1> 
</p>
<img src="https://i.imgur.com/WQS0gJJ.png" height="80%" width="80%" alt="Active Directory Steps"/>
</p>
 Add Admins and users in Active Directory with respective privilages and restictions

</p>
<p>
<img src="https://i.imgur.com/UH3nkDz.png" height="80%" width="80%" alt="Client join domain Steps"/>
</p>
<p>
Make sure Client's computer joins the Domain server and can log in with the new credential.
</p>
<br />

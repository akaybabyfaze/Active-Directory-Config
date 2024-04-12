<img src="https://i.imgur.com/ZqQ5cAh.jpg" height="40%" width="70%" alt="Active Directory Configuration"/>
<h2>Description</h2>
The project is a walkthrough of Active Directory on premises set up. Active Directory provides a central location for managing and controlling network resources, such as user authentication, authorization, and access to resources. Identity and Access Management Analyst are able to define, manage, and apply policies, permissions, and security settings to network resources. The Project also involved the use of PowerShell to create new users on Active Directory.
<br />
<h2>Environment Used</h2>
<ul>
  <li>Microsoft Azure Virtual Machines</li>
  <li>Windows Server 2022</li>
  <li>Windows 10 Pro (22H2)</li>
</ul>
<h2>Technologies Used</h2>
<ul>
  <li>Active Directory Domain Services</li>
  <li>PowerShell</li>
</ul>   
<h2>Program walk-through:</h2>
<p>
<h4><b>"DOMAIN CONTROLLER VM & WINDOWS 10 CLIENT VM"</b></h4>
Domain Controller (DC) server will be installed on the Virtual Machine (VM) with Windows Server 2022. This would be used to manage Active Directory (AD) on-premises. A Windows 10 client workstation will be installed to show domain access to the machine with domain users. During the creation of both VMs, they need to be on the <b>same Virtual Network(VN)</b>. DC server VM's IP needs to be configured to be static.
<br/>
<img src="https://i.imgur.com/6bK99pD.png" height="60%" width="100%" alt="Domain Controller"/>
<img src="https://i.imgur.com/9pO4BeU.png" height="60%" width="100%" alt="Windows 10 VM"/>
<img src="https://i.imgur.com/FyOyJbO.png" height="40%" width="60%" alt="DC Virtual Network"/>
<img src="https://i.imgur.com/2ygG6dS.png" height="25%" width="50%" alt="Static IP config"/>
<br/>
<h4><b>"INSTALLATION OF DOMAIN CONTROLLER":</b></h4> A Domain Controller (DC) is a server in a Windows-based network that is responsible for managing security authentication requests, enforcing security policies, and organizing resources. DC is a central authority for network management within a Windows domain. After installation, the server needs to be promoted to a DC.
<br/>
<img src="https://i.imgur.com/kGmKQf7.png" height="40%" width="60%" alt="RDP to Windows Server"/>
<img src="https://i.imgur.com/9o3Qp44.png" height="40%" width="60%" alt="Windows Server"/>
<img src="https://i.imgur.com/qODK6GZ.png" height="40%" width="60%" alt="Domain Controller"/>
<img src="https://i.imgur.com/e608J9b.png" height="40%" width="60%" alt="Domain created"/>
<br/>
  <h4><b>"ACTIVE DIRECTORY (AD)"</b></h4>
  Active Directory (AD) is a database and set of services that connect users with network resources. Two additional <b>Organization Units (OU)</b> will be created: '_Admins' and '_employee". An Admin user will be created in this group while other domain users with any special privileges will be in _employee "OU"
<br/>
<img src="https://i.imgur.com/i5CjQIj.png" height="50%" width="80%" alt="Active Directory UI"/>
<img src="https://i.imgur.com/1sAAHDD.png" height="25%" width="50%" alt="Admin User created"/>
<br/>
  <b>"JOINING WORKSTATION TO THE DOMAIN"</b>
  Client 1 (Windows 10)'s <b>DNS server</b> needs to configured with DC network address. Then, Client 1 can be added to the domain with the <b>Admin user's credentials</b>. For the purpose of this project, Client 1 workstation will be configured to allow <b>domain users</b> login remotely. From AD UI, Client 1's computer has now been added to <b>Computers OU</b>
<br/>
<img src="https://i.imgur.com/VYtCxVM.png" height="25%" width="60%" alt="DNS server config"/>
<img src="https://i.imgur.com/H75L4la.png" height="25%" width="60%" alt="Client 1 joined to the domain"/>
<img src="https://i.imgur.com/y6hAs53.png" height="40%" width="80%" alt="Client 1 under Computer OU"/>
<br/>
  <b>"USING POWERSHELL TO CREATE DOMAIN USERS"</b>
PowerShell can be used to automate processes. Where there are several domain users to be created, a PowerShell script can be used to perform the task in seconds. The project showed five new AD user details were imported from a CSV file, and a PowerShell script was run to create the new users. User "Femi.Musa" was able to log in successfully to Client 1 as a new user from the PowerShell AD scripts.
<br/>
<img src="https://i.imgur.com/LxRwbKP.png" height="50%" width="80%" alt="PowerShell script"/>
<img src="https://i.imgur.com/WKOcrib.png" height="50%" width="80%" alt="PowerShell script"/>
<img src="https://i.imgur.com/2L6l6o9.png" height="50%" width="80%" alt="PowerShell script"/>
<img src="https://i.imgur.com/DRM9WTj.png" height="50%" width="80%" alt="Domain users created"/>
<img src="https://i.imgur.com/ADJIKtz.png" height="50%" width="80%" alt="Domain user logged in successfully"/>
<br/>
</p>

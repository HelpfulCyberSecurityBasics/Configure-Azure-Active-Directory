<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create a Resource Group: This foundational step involves setting up a container in Azure to hold all related resources for the Active Directory lab.
- Create a Virtual Network (VNet): A VNet is established to provide a private network in Azure, allowing the virtual machines to communicate securely.
- Deploy the Windows Server VM (DC1): A Windows Server 2022 virtual machine is deployed to serve as the domain controller, which will host Active Directory.
- Configure DC1's Private IP Address to Static: The network interface card (NIC) of the domain controller VM is configured to use a static private IP address for stability.
- Deploy and Configure Client VM (Client1): A Windows 10 Pro virtual machine is deployed to act as a client, and its DNS settings are configured to point to the DC1's private IP address.


<h2>Deployment and Configuration Steps</h2>

<p>
  1. Virtual Network (VNet) Setup: Create a virtual network to ensure secure and isolated communication between your virtual machines.
<img width="879" height="585" alt="image" src="https://github.com/user-attachments/assets/b58d882a-58b2-4c96-a448-be17ac0173a5" />


</p>
<p>
</p>
<br />

<p>
2. Domain Controller VM Deployment (DC1): Deploy a Windows Server 2022 virtual machine to function as the primary domain controller for Active Directory.
  <img width="860" height="570" alt="image" src="https://github.com/user-attachments/assets/1495b821-d813-4efe-9ced-85527cc260f2" />

</p>
<p>
</p>
<br />

<p>
3. Static IP Configuration for DC1: Adjust the domain controller's private IP address to be static, ensuring stable network connectivity.
<img width="1336" height="543" alt="image" src="https://github.com/user-attachments/assets/f7157dc6-e126-40a3-9191-f88888aacb06" />

</p>
<p>
</p>
<br />
4. Client VM Deployment (Client1) and DNS Configuration: Deploy a Windows 10 Pro client virtual machine and configure its DNS settings to point to the domain controller's private IP.
<img width="872" height="546" alt="image" src="https://github.com/user-attachments/assets/300c538f-f739-497b-82a4-8233e2c18cb1" />

<br />
5. Connectivity Test (Ping): Verify successful communication between the client and domain controller by performing a ping test to the DC's private IP address.
<img width="847" height="514" alt="image" src="https://github.com/user-attachments/assets/ad4fae7b-e579-47c3-8d40-d0fd74632058" />


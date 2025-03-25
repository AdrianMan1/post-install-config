<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles for Grouping Permissions 
- Configure Departments, Teams, and Agents
- Configure SLAs
- Configure Help Topics

<h2>Configuration Steps</h2>

<p>

<ins>Configure Roles</ins>

Under the "Agents" and "Roles" tabs within the Admin Panel of osTicket allows us to configure and create roles that are assigned to agents within the portal.

<img width="701" alt="Screenshot 2025-03-25 at 10 41 32 AM" src="https://github.com/user-attachments/assets/bee440ae-154f-4c3a-8fa1-5c6327a88065" />


<p>

  
Here we have created a new user with the title "Supreme User" which has been configured to have unlimited permissions. Other roles such as "View Only" would only be able to see tickets but not be able to change them, while roles such as "Limited Access" can view and change tickets but not be able to do other things like assign it to another agent. 

![image](https://github.com/user-attachments/assets/77a8ec7e-5616-4090-a6b1-ceb246d3b87c)
Permissions for all roles are configured within the roles tab of the admin portal, as seen above. 
  
  <p> 
  </p>


<ins>Configure Departments, Teams and Agents 
  ㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤ</ins>

Using a similar process to what we did before, we can create and configure new & existing Departments, Teams, and Agents respectively. 

![image](https://github.com/user-attachments/assets/6a2e6389-4396-4aff-804c-2cc23063298b)

<p>


Above we are creating a new agent "Jane Doe" who will have the "Supreme Admin" role, belong to an "Online Banking" team within the SysAdmins Department. 
The process of creating these entities is similar to creating roles.

Agents: Admin Panel > Agent Tab > Add New Agent > Create the agent & assign access, permissions & teams they belong to.

Teams: Admin Panel > Teams Tab > Add New Team > Create team name (ex. Online Banking) & assign members.

Departments: Admin Panel > Departments Tab > Add New Department > Create the Department (Ex. SysAdmins) and determine SLAs & who is a part of this departmemt. 

  
</p>
<br />

<ins>Configure SLAs
  ㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤ</ins>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

If you are not familiar with SLAs (Surface Level Agreements), they are an agreement between a service provider (in this case, a helpdesk within osTicket) and a user/customer that describes standards of service regarding quality, avaliability and responsibilities. In our ticketing system, we need to create SLAs to give our agents a framework for the service to provide a customer. 

Within the osTicket portal we are able to configure these SLAs by going to: 
Admin Panel > Manage > SLA

From there we can create the following:

  - Severity-A (Grace Period: 1 hour, Schedule: 24/7)

  - Severity-B (Grace Period: 4 hours, Schedule: 24/7)

  - Severity-C (Grace Period: 8 hours, Business Hours)

What these SLAs tell us is how severe a user's issue is (this is most of the time configured by a SysAdmin or Manager, not by a user), how long we have to respond to or resolve the issue, and at what times the agents work on them (ex. buisness hours, 24/5, 24/7, etc...)

After configuring SLAs, we can configure our help topics with said them so users using our ticketing system can have a plain-text way of describing their problem while the agents can get these tickets knowing when and how to respond. 




</p>
<br />

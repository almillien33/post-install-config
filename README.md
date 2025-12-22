<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial provides a detailed overview of the post-installation configuration process for the open-source help desk ticketing system, osTicket. In this phase, we will transition the system from its initial setup (Alpha) to a fully operational help desk system, ready to handle real-world support tickets.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Configuration Steps</h2>

Okay great! We have successfully configured osTicket from scratch. Now, we will perform some system administration tasks and complete the post-installation setup. The first thing is to acknowledge the admin panel, which is http://localhost/osTicket/scp/login.php, and the agent panel http://localhost/osTicket. Just paste them within the VM internet address bar whenever you want to access them. Now, log into the admin panel, and you have to configure Roles (for grouping permissions) by going to Admin Panel -> Agents -> Roles. We will create a Supreme Admin. Click on "Add new role," then enter supreme admin for the name of the new role. Then, within roles, select permissions, and under tickets, check all the boxes, and the same thing for tasks and the knowledge base. Then you should select Add Role. If you followed the steps correctly, your screen should look something like this. As you can see, we have successfully created the "Supreme Admin" role.

<p>
<img width="2559" height="1405" alt="image" src="https://github.com/user-attachments/assets/8c9c3f5f-bdfb-4e7e-9587-29728497cd0b" />
</p>
<p>
Next, we are going to configure departments, so select the "Departments" button in the agents tab. Here we will select create a new department. On the Settings tab, look for 'Parent' and set it to 'Support.' For the name, enter 'sysadmins.' Then hit create when you're all done. 
</p>
<br />

<p>
<img width="2556" height="1403" alt="image" src="https://github.com/user-attachments/assets/e46741d2-52da-48c5-97b0-aebfef044993" />
</p>
<p>
After configuring a new department, we will set up a new team. Now go to Admin Panel -> Agents -> Teams and click on Add New Teams. Then, for the name, put Online banking, and leave everything as is, and select create. 
</p>
<br />

<p>
<img width="2559" height="1400" alt="image" src="https://github.com/user-attachments/assets/8cc2b8cc-20d1-42e0-b784-f2e0e48542d1" />
</p>
<p>
Next, we will create a new setting that will allow anyone to create tickets, so go to Admin Panel -> Settings -> User -> Settings. Then make sure the box next to Require registration and login to create tickets is unchecked.
</p>
<br />

<p>
<img width="2560" height="1397" alt="image" src="https://github.com/user-attachments/assets/ca758547-d0ab-496c-8b9b-5d21282725c1" />
</p>
<p>
It is now time to create Agents. Agents are the employees of the helpdesk who actually work on solving tickets. Now go to Admin Panel -> Agents -> Add New and create two users which are Jane Doe and John Doe, and create a password and email for both. Plus, uncheck Require password change at next login when you create the password. After that, hit the access tab and within Primary Department, set Jane to the sysadmins department and supreme admin. For the teams tab, select online banking for Jane and select create. Next, for John, set him to the support department and view only, and then hit create.
</p>
<br />

<p>
<img width="2557" height="1394" alt="image" src="https://github.com/user-attachments/assets/e805ee56-6548-492b-8cce-a06fbe644fde" />
</p>
<p>
After creating some agents, we will create users. Users are customers who create tickets when they are having issues. A user is identified with their Email address. To create a user, follow this path: Agent Panel->Users->User Directory->Add new.
</p>
<br />

<p>
<img width="2555" height="1396" alt="image" src="https://github.com/user-attachments/assets/c9a2e0ee-d399-47a2-b73c-14f01e66610a" />
</p>
<p>
SLA plans provide a length of time in which the help desk is expected to take in order to solve a specific ticket. SLA Plans are created by going to Admin Panel->Manage-> SLA Plans. Then create Sev-A (Grace Period: 1 hour, Schedule: 24/7), Sev-B (Grace Period: 4 hours, Schedule: 24/7), and Sev-C (Grace Period: 8 hours, Business Hours). Each SLA has a schedule, and within that schedule, there is a grace period. In this example, SEV-A has a 24/7 service and a one-hour grace period.
</p>
<br />

<p>
<img width="2555" height="1397" alt="image" src="https://github.com/user-attachments/assets/8d0906b2-448b-46de-96fd-4b191f756846" />
</p>
<p>
Now, configure help topics (For when users create a ticket). Help topics help users categorize their tickets, so go to Admin Panel -> Manage -> Help Topics and create a couple like Personal Computer Issues, Equipment Request, Password Reset, and Other.
</p>
<br />

<p>
<img width="2558" height="1400" alt="image" src="https://github.com/user-attachments/assets/1465583e-367c-4476-8dd6-9755316de6a3" />
</p>
<p>






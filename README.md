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

<h2>Configuration Steps</h2>

Okay great! We have successfully configured osTicket from scratch. Now, we will perform some system administration tasks and complete the post-installation setup. The first thing is to acknowledge the admin panel, which is http://localhost/osTicket/scp/login.php, and the agent panel http://localhost/osTicket. Just paste them within the VM internet address bar whenever you want to access them. Now, log into the admin panel, and you have to configure Roles (for grouping permissions) by going to Admin Panel -> Agents -> Roles. We will create a Supreme Admin. Click on "Add new role," then enter supreme admin for the name of the new role. Then, within roles, select permissions, and under tickets, check all the boxes, and the same thing for tasks and the knowledge base. Then you should select Add Role. If you followed the steps correctly, your screen should look something like this. As you can see, we have successfully created the "Supreme Admin" role.

<p>
<img width="966" height="438" alt="image" src="https://github.com/user-attachments/assets/058d8977-869a-4630-998f-a07b26b9de69" />
</p>
<p>
Next, we are going to configure departments, so select the "Departments" button in the agents tab. Here we will select create a new department. On the Settings tab, look for 'Parent' and set it to 'Support.' For the name, enter 'sysadmins.' Then hit create when you're all done. 
</p>
<br />

<p>
<img width="865" height="418" alt="image" src="https://github.com/user-attachments/assets/cc95712c-0cd8-43b2-829e-aaf764c75687" />
</p>
<p>
After configuring a new department, we will set up a new team. Now go to Admin Panel -> Agents -> Teams and click on Add New Teams. Then, for the name, put Online banking, and leave everything as is, and select create. 
</p>
<br />

<p>
<img width="870" height="322" alt="image" src="https://github.com/user-attachments/assets/65613724-f5dd-41fd-a7cc-88f3f352f45b" />
</p>
<p>
Next, we will create a new setting that will allow anyone to create tickets, so go to Admin Panel -> Settings -> User -> Settings. Then make sure the box next to Require registration and login to create tickets is unchecked.
</p>
<br />

<p>
<img width="872" height="685" alt="image" src="https://github.com/user-attachments/assets/03850f83-0a0f-4dbd-af7d-3c661d1e7c92" />
</p>
<p>
It is now time to create Agents. Agents are the employees of the helpdesk who actually work on solving tickets. Now go to Admin Panel -> Agents -> Add New and create two users which are Jane Doe and John Doe, and create a password and email for both. Plus, uncheck Require password change at next login when you create the password. After that, hit the access tab and within Primary Department, set Jane to the sysadmins department and supreme admin. For the teams tab, select online banking for Jane and select create. Next, for John, set him to the support department and view only, and then hit create.
</p>
<br />

<p>
<img width="965" height="421" alt="image" src="https://github.com/user-attachments/assets/f5c45729-1022-45f3-8a3a-6d4b7be3878d" />
</p>
<p>
After creating some agents, we will create users. Users are customers who create tickets when they are having issues. A user is identified with their Email address. To create a user, follow this path: Agent Panel->Users->User Directory->Add new.
</p>
<br />

<p>
<img width="873" height="366" alt="image" src="https://github.com/user-attachments/assets/945493ef-d519-48f2-a689-76a55fa0e829" />
</p>
<p>
SLA plans provide a length of time in which the help desk is expected to take in order to solve a specific ticket. SLA Plans are created by going to Admin Panel->Manage-> SLA Plans. Then create Sev-A (Grace Period: 1 hour, Schedule: 24/7), Sev-B (Grace Period: 4 hours, Schedule: 24/7), and Sev-C (Grace Period: 8 hours, Business Hours). Each SLA has a schedule, and within that schedule, there is a grace period. In this example, SEV-A has a 24/7 service and a one-hour grace period.
</p>
<br />

<p>
<img width="873" height="408" alt="image" src="https://github.com/user-attachments/assets/cc8db6e3-cc16-4c55-a725-53230662fd5b" />
</p>
<p>
Now, configure help topics (For when users create a ticket). Help topics help users categorize their tickets, so go to Admin Panel -> Manage -> Help Topics and create a couple like Personal Computer Issues, Equipment Request, Password Reset, and Other.
</p>
<br />

<p>
<img width="868" height="562" alt="image" src="https://github.com/user-attachments/assets/3cf8adb7-e267-4a18-8151-d28ef63be081" />
</p>
<p>






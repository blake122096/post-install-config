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

- Windows 10 Pro</b> (22H2) at least 2vCPUs, 8GB RAM

<h2>Post-Install Configuration Objectives</h2>

- Configuring roles, departments and teams
- Configuring agents (workers) and users (customers)
- Configuring SLAs: <b>Sev-A</b> (grace period: 1hr, schedule: 24x7), <b>Sev-B</b> (grace period: 4hr, schedule: 24x7), <b>Sev-C</b> (grace period: 8hr, schedule: business hr)
- Configuring help topics

<h2>Configuration Steps</h2>

<p>
Access the staff control panel (http://localhost/osTicket/scp) and log in as the admin user. Navigate to Admin Panel > Agents > Roles.
</p>
<br />

<p>
<img src="https://i.imgur.com/lpCEmOc.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/d0xEC62.png" height="80%" width="80%" />
</p>
<p>
Agent roles define permission levels, from "View only" (limited to viewing tickets) to "All access" (unrestricted actions, including assigning, modifying, and deleting tickets).  To create a new department, navigate to 
Admin Panel > Agents > Departments > Add new department.
</p>
<br />

<p>
<img src="https://i.imgur.com/BrivLPw.png" height="80%" width="80%" />
</p>
<p>
The Departments section allows for creating and managing departments, configuring SLAs, assigning tickets, and setting up alerts and autoresponses.  To create a new team, navigate to Admin Panel > Agents > Teams > Add New Team.
</p>
<br />

<p>
  <img src="https://i.imgur.com/x3t46ev.png" height="80%" width="80%" />
</p>

<p>
Teams allow further categorization of agents within departments (e.g., an "Online Banking" team within the "SysAdmins" department). Members can be added to teams to handle tickets.  To allow unregistered users to create tickets, go to 
Settings > Users and uncheck "Require registration and login to create tickets."
<br />
<p>
  <img src="https://i.imgur.com/pGe7fEx.png" height="80%" width="80%" />
</p>

<p>
Now can create some agents to work our tickets. Click on Agents (big tab) -> Add New Agent.
</p>
<br />
<p>
  <img src="https://i.imgur.com/VB0TioR.png" height="80%" width="80%" />
</p>

<p>
Configure agent accounts with details like name, password, email, access level (which sets pre-configured permissions), and team assignment. For example, create "Jane Doe" with "All Access" in the "SysAdmins" department, and "John Doe" with "Expanded Access" in the "Support" department. Permissions can be fine-tuned as needed.
</p>
<br />
<p>
<img src="https://i.imgur.com/1S1guxh.png" height="80%" width="80%" />
<img src="https://i.imgur.com/jomxLlm.png" height="80%" width="80%" />

</p>

<p>
Assign agents to their respective teams (e.g., Jane Doe to "Online Banking," John Doe to "Support") to enable ticket assignments between teams.  To create users, navigate to Admin Panel > Users > Add User.  Create two users, "Karen" and "Ken."
</p>
<br />
<p>
  <img src="https://i.imgur.com/AGaSsDV.png" height="80%" width="80%" />
</p>

<p>
To ensure timely resolution of critical issues, osTicket allows you to define Service Level Agreements (SLAs).  SLAs help prioritize tickets based on their urgency and potential impact on the business. By assigning different SLA levels, you can ensure that agents address the most critical issues first.
</p>
<br />
<p>
  <img src="https://i.imgur.com/CUIRala.png" height="80%" width="80%" />
</p>

<p>
Create SLA plans to prioritize tickets based on severity (Sev-A being the most urgent). Configure Sev-A with a 1-hour grace period and 24x7 schedule, Sev-B with a 4-hour grace period and 24x7 schedule, and Sev-C with an 8-hour grace period and business hours schedule.  To create help topics for ticket categorization, navigate to 
Admin Panel > Manage > Add New Help Topic.
</p>
<br />

<p>
<img src="https://i.imgur.com/Cs71oCW.png" height="80%" width"80%" />
</p>
<p>
Create help topics with hierarchical categorization. For example, create a top-level topic like "Report a Problem" and then add subtopics like "Access Issue" for more specific categorization.
</p>
<br />

</p>

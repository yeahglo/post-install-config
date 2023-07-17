<img width="790" alt="Screen Shot 2023-07-05 at 12 01 33 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/c7e47b62-8276-47e5-8c1a-69944eee66b1">

<h1>osTicket - Post-Install Configuration</h1>
This walkthrough is a set up of the osTicket software 

<h2>Environments and Technologies Used</h2>

- Microsoft Azure Virtual Machine
- Microsoft Remote Desktop
- Internet Information Services (IIS)
- osTicket Software

<h2>Operating System</h2>

- Windows 10, version 22H2

<h2>List of Prerequisites</h2>

- Setup & Configuration: [osTicket: Prerequisites and Installation](https://github.com/yeahglo/osticket-prereqs)
- Agent Login Page: http://localhost/osTicket/scp
- osTicket Documentation: https://docs.osticket.com/

<h2>Post-Install Configuration Objectives</h2>

- Define Roles, Departments, Teams and set permissions
- Create Agents and Users
- Create SLAs and Help Topics

<br/>

<img width="1280" alt="Screen Shot 2023-07-10 at 8 28 57 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/393bec16-8e3e-41f7-8c36-7a2999077e63">

**_Start by logging into the Agent Login Page for osTicket._** 

<br/>

**Step 1: Create a Role** - Roles determine levels of access.
- Navigage to Admin panel > Agents > Roles > Add New Role
- Name the role "Supreme Admin"
- Checkmark all permissions under Tickets, Tasks, and Knowledgebase

<br/>

<img width="1153" alt="Screen Shot 2023-07-10 at 8 38 54 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/35da20c1-7601-4b94-9cae-7332de1fee43">

**_Create the Supreme Admin Role._**

<img width="1096" alt="Screen Shot 2023-07-10 at 8 38 24 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/f96fa232-d29c-42ce-b204-a94779417277">

**_Turn on all of these permissions. There are plenty of permissions under Tickets, Tasks, and Knowledgebase._**

<br/>

**Step 2: Create a Department** - Departments determine ticket routing.
- Navigage to Admin panel > Agents > Roles > Add New Department
- Name the department "System Administrators"
- Leave the defaults settings for now

<br/>

<img width="1200" alt="Screen Shot 2023-07-10 at 8 47 15 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/40d692b0-9e32-4a4a-8a5a-cbecf5ee427e">

**_Use the default settings for the Systems Administrators Department._**

<br/>

**Step 3: Create a Team** - Teams allow you to pull agents for specific use cases.
- Navigage to Admin panel > Agents > Roles > Add New Team
- Create a "Level II Support" _(Note: You already have a Level I as a default.)_

<br/>

<img width="1203" alt="Screen Shot 2023-07-10 at 8 51 26 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/0460bfed-4a5a-4f0f-a1b1-128fd2ecb792">

**_More settings can be configured at the Team level, including assigning a team lead or adding members as you set up the team._**

<br/>

**Step 4: Allow anonymous users to create tickets** - Doing this ensures users, aka "ticket owners", can create tickets easily.
- Admin Panel > Settings > User Settings > uncheck “Require registration and login to create tickets”

<br/>

<img width="1194" alt="Screen Shot 2023-07-10 at 8 54 48 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/c3957e06-b945-4543-8512-637c96341b00">

**_Review the setting to allow anonymous users to create tickets._**

<br/>

**Step 5: Create an Agent** - Agents are help desk professionals who work the tickets.
- Navigate to Admin Panel > Agents > Add New Agent
- Name the agent "Anthony Torres"
- Add Anthony's department as System Administrators
- Assign the Supreme Admin role for him
- Assign him to the Level II Support Team
- Add Support under the Extended Access so he can view/edit tickets

<br/>

<img width="1105" alt="Screen Shot 2023-07-10 at 8 58 23 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/4f007583-8104-4b34-96cc-7fff281ec850">

**_The agent profile has many options to set access and permissions._**

<br/>

<img width="1207" alt="Screen Shot 2023-07-10 at 8 59 04 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/b597218c-86e8-43f9-b19f-eafdfd86dbd5">

**_Under the agent profile, osTicket lets you set and change the password as long as you have the permissions to change this._**

<br/>

**Step 6: Create a User** - Users create support tickets to get assistance from agents.
- Navigate to Agent Panel > Users > Add User _(Note: You can also import users)_
- Name the User "Dylan Thompson" and add an email for them

<br/>

<img width="1201" alt="Screen Shot 2023-07-10 at 9 17 26 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/21612baa-a541-4fb7-98b9-decdbc8e05b8">

**_Users are the ticket owners. It's possible to create them one by one, but you can also import them in bulk._**

<br/>

**Step 7: Create an SLA** - Service Level Agreements (SLAs) define what kind of response time and priority level is warranted for each ticket.
- Navigate to Admin Panel > Manage > SLA > Add New SLA Plan
- Name the SLA Plan "SEV-A" and set it on a 24/7 schedule with a 1-hour grace period

<br/>

<img width="1208" alt="Screen Shot 2023-07-10 at 9 21 25 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/24720102-a884-4e04-bf8c-831ee9cf867d">

**_SLAs can be set up to define what kind of timeline each ticket has in order to remain compliant with the service contract._**

<br/>

**Step 8: Create a Help Topic** - Help Topics allow users to set a category for their ticket.
- Navigate to Admin Panel > Manage > Help Topics > Add New Help Topic
- Name the Help Topic "Personal Computer Issues"

<br/>

<img width="1243" alt="Screen Shot 2023-07-13 at 9 38 00 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/01c09ec5-eec5-4ec2-94b6-9601455c9f40">

**_Help Topics will be visible to users to assign to individual tickets. You can customize further under the "New Tickets options" and "Forms" tabs._**

<h2>Next Steps</h2>

Continue to the third part to create and work a ticket.
[Ticket Lifecycle](https://github.com/yeahglo/ticket-lifecycle)

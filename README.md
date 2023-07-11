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

</br>

<img width="1280" alt="Screen Shot 2023-07-10 at 8 28 57 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/393bec16-8e3e-41f7-8c36-7a2999077e63">

**_We start by logging into our Agent Login Page for osTicket._** 

</br>

**Step 1: Create a Role**
Roles determine levels of access.
- Navigage to Admin panel > Agents > Roles > Add New Role
- Name the role "Supreme Admin"
- Checkmark all permissions under Tickets, Tasks, and Knowledgebase

</br>

<img width="1153" alt="Screen Shot 2023-07-10 at 8 38 54 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/35da20c1-7601-4b94-9cae-7332de1fee43">

**_Create the Supreme Admin Role._**

<img width="1096" alt="Screen Shot 2023-07-10 at 8 38 24 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/f96fa232-d29c-42ce-b204-a94779417277">

**_The Supreme Admin Role should have all permissions checked under Tickets, Tasks and Knowledgebase._**

</br>

**Step 2: Create a Department**
Departments determine ticket routing and allow you to customize settings.
- Navigage to Admin panel > Agents > Roles > Add New Department
- Name the department "System Administrators"
- Leave the defaults settings and SLAs for now

</br>


<img width="1200" alt="Screen Shot 2023-07-10 at 8 47 15 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/40d692b0-9e32-4a4a-8a5a-cbecf5ee427e">

**_Create the System Administrators Department._**

</br>

**Step 3: Create a Team**
Teams allow you to pull agents for specific use cases, such as your SMEs.
- Navigage to Admin panel > Agents > Roles > Add New Team
- Create a "Level II Support" (we already have a Level I as a default)

<img width="1203" alt="Screen Shot 2023-07-10 at 8 51 26 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/0460bfed-4a5a-4f0f-a1b1-128fd2ecb792">

**_Add a Level II Support Team._**

</br>

**Step 4: Allow anonymous users to create tickets**
Doing this ensures that our users, aka "ticket owners", can create tickets easily.
- Admin Panel > Settings > User Settings > uncheck “Require registration and login to create tickets”

<img width="1194" alt="Screen Shot 2023-07-10 at 8 54 48 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/c3957e06-b945-4543-8512-637c96341b00">

**_Make sure the requirement for registration is unchecked._**

</br>

**Step 5: Create an Agent**
Agents are help desk professionals who work the tickets.
- Navigate to Admin Panel > Agents > Add New Agent
- Name the agent "Anthony Torres"
- Add Anthony's department as System Administrators
- Add her role as Supreme Admin
- Add her to SMEs team, Level II Support
- Add her Extended Access to Support so she can also work tickets

</br>

<img width="1105" alt="Screen Shot 2023-07-10 at 8 58 23 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/4f007583-8104-4b34-96cc-7fff281ec850">

**_Create an Agent profile._**

</br>

<img width="1207" alt="Screen Shot 2023-07-10 at 8 59 04 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/b597218c-86e8-43f9-b19f-eafdfd86dbd5">

**_To set a password for practice, make sure your screen looks like this (unchecked) and click "set"._**



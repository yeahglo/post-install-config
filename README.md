<!--<img width="790" alt="Screen Shot 2023-07-05 at 12 01 33 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/c7e47b62-8276-47e5-8c1a-69944eee66b1">

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

- [osTicket: Prerequisites and Installation](https://github.com/yeahglo/osticket-prereqs)

<h2>Post-Install Configuration Objectives</h2>

- Define Roles, Departments, Teams and set permissions
- Create Agents and Users
- Create SLAs and Help Topics

**Step 1: Create Roles:**
Roles determine levels of access.
- Navigage to Admin panel > Agents > Roles > Add new role
- Name the role "Supreme Admin"
- Checkmark all permissions under Tickets, Tasks, and Knowledgebase


**Step 2: Create Departments:**
Departments determine ticket routing and allow you to customize settings.
- Navigage to Admin panel > Agents > Roles > Add New Department
- Name the department "System Administrators"
- Leave the defaults settings and SLAs for now

**Step 3: Create Teams:**
Teams allow you to pull agents for specific use cases, or define SMEs.
- Navigage to Admin panel > Agents > Roles > Add New Team
- Create a "Level II Support team to add a second level to the existing default

**Step 4: Allow anonymous users to create tickets**
Doing this ensures that our users, aka "ticket owners", can create tickets easily.
- Admin Panel > Settings > User Settings > uncheck “Require registration and login to create tickets”

**Step 5: Create Agents**
Agents are help desk-->


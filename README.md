# Helpdesk-Labs
# Active Directory Lab (Users, Groups, & Password Resets)

To kick off this Active Directory lab, I started by downloading Windows Server 2025.

![Windows Server download](assets/Screenshot%202026-10-10%20073843.png)

Instead of using a physical device, I used a virtual machine (VMware Workstation) to install and run Windows Server.

![VMware setup 1](assets/Screenshot%202026-10-13%20123311.png)
![VMware setup 2](assets/Screenshot%202026-10-13%20124005.png)

Once Windows Server was up and running, I configured it as a domain controller. In the top right corner I went to Manage > Add Roles and Features > Role-based installation. Selecting Active Directory Domain Services in the Server Roles tab allows the server to run as a domain controller.

![Server roles 1](assets/Screenshot%202026-10-13%20130053.png)
![Server roles 2](assets/Screenshot%202026-10-13%20130232.png)

## Users, Groups, and Organizational Units

After the domain controller was set up, I began creating users. By navigating to the Tools tab and selecting "Active Directory Users and Computers," I could create sample users and place them into groups and organizational units (OUs).

<video src="assets/Screen%20Recording%202026-10-17%20021140.mp4" controls width="700"></video>

Users in different OUs can access the same storage share depending on organizational needs. This is demonstrated below: Russ West can access the engineering share even though he's not part of the Engineering OU.

<video src="assets/Screen%20Recording%202026-10-17%20032901.mp4" controls width="700"></video>

## Group Policy (GPO)

A GPO (Group Policy Object) is a set of configuration settings that can be applied to a sector or an entire organization. Standard user and computer configurations can be managed with this tool. I created a GPO for my sample IT sector. I could have set password rules or account lockout policies, but I opted for a simple wallpaper setting. Using a GPO, I can enforce this setting for every user in the IT organizational unit (as shown in the last screenshot).

![GPO 1](assets/Screenshot%202026-10-17%20175329.png)
![GPO 2](assets/Screenshot%202026-10-17%20175416.png)
![GPO 3](assets/Screenshot%202026-10-17%20180234.png)
![GPO 4](assets/Screenshot%202026-10-17%20180816.png)
![GPO 5](assets/Screenshot%202026-10-17%20181456.png)
![GPO 6](assets/Screenshot%202026-10-17%20181959.png)

## Joining a Second PC to the Domain

To simulate a normal work environment, I added another PC to the domain (DOM.local). After configuring the new PC, any of the users created in this lab can log in, as demonstrated in the video.

<video src="assets/Screen%20Recording%202026-11-07%20160619.mp4" controls width="700"></video>

## Password Reset

To wrap up this lab, I demonstrated a simple password reset. This is useful for users who are locked out of their accounts due to incorrect password attempts.

<video src="assets/Screen%20Recording%202026-10-17%20183908.mp4" controls width="700"></video>

<video src="assets/Screen%20Recording%202026-11-02%20183417.mp4" controls width="700"></video>

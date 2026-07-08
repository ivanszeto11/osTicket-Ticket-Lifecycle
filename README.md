<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo" />
</p>

# osTicket - Ticket Lifecycle

## Overview

### Environments and Technologies Used
- Microsoft Azure (Virtual Machines)
- Remote Desktop Connection
- Internet Information Services (IIS)
- osTicket

### Operating Systems Used
- Windows 11 Pro

### Skills Learned
- Understanding the different ticket lifecycle stages and how to work through them
- Understanding ticket properties and the layout of tickets in osTicket
- Maintaining a line of communication with users throughout the ticket resolution process

## Walk-through

### Ticket Lifecycle Stages
1. **Ticket Creation:** The initial step when an issue is identified and a ticket is created by the user or an agent 
2. **Triage and Prioritization:** The ticket's severity and impact are identified to assign it an appropriate priority level. Triage is typically done by level 1 support analysts, who determine if the ticket needs to be escalated to a higher level  
3. **Assignment and Investigation:** The ticket is assigned to an agent or team with the expertise to resolve the issue, and they investigate the issue to find the root cause
4. **Resolution:** The agent provides a solution to the user's issue or fulfills their request
5. **Ticket Closure:** The resolution of the ticket is confirmed with the user and the ticket can be closed

In this lab, we will explore the stages of the ticket lifecycle by working through two sample tickets. First, we will create a ticket as an end user and work it to completion as an agent. Then, we will create another ticket as a help desk agent and resolve it. 

### Creating a Ticket as the End-User

<p align="center">
  <img width="838" height="360" alt="osticket-support-1" src="https://github.com/user-attachments/assets/3b14ac5c-8ecb-4817-93d4-c3a23024b63a" />
</p>

The image above shows the user portal in osTicket. This is where users can create new tickets or check the status of their existing tickets. To create a new ticket, click **Open a New Ticket**.

<p align="center">
  <img width="831" height="892" alt="osticket-support-2" src="https://github.com/user-attachments/assets/e481db38-96b8-40dd-88c0-9a4cd780c528" />
</p>

In order to create a ticket, the user must provide their name and email address. The email address will be linked with the user account and used to contact the user. For the lab, we will use the name "Ken" along with a fake email address. There is also the option to provide a phone number, but we will leave that blank.  

Next, we have to select a Help Topic for the ticket. This identifies what type of issue the ticket is for and allows the ticket to be routed to the Department that handles that specific topic. Let's select "General Inquiry / Other" as the Help Topic.  

The Ticket Details section is where we will describe the issue. Let's say the problem is that nobody in our banking department can access the online banking system, meaning they are unable to do any work. In the Issue Summary, we will give a brief description of the problem; this is like the subject line of an email. In the body of the message, we will describe the issue in more detail. Once this information is provided, we will click **Create Ticket**. We have just finished the Ticket Creation stage of the ticket lifecycle.

<p align="center">
  <img width="955" height="374" alt="osticket-support-3" src="https://github.com/user-attachments/assets/8073b9c7-87c6-4f6a-8316-654b42790bdc" />
</p>

Now, we will log in as a help desk agent, John Doe. In our ticket queue, we can see the ticket that we have just created. The ticket queue shows the ticket number, the timestamp of the ticket's last update, the subject line, the user who the ticket belongs to, the priority level, and the agent assigned to the ticket. Note that the issue summary we previously submitted appears in the subject column and the ticket is from Ken. We can open the ticket by clicking on the ticket number or the subject.

<p align="center">
  <img width="953" height="616" alt="osticket-support-4" src="https://github.com/user-attachments/assets/416fe614-ed2c-4109-9451-77c5f79eed2e" />
</p>

When we open the ticket, we will see the ticket header, containing the ticket properties, at the top. Most of these properties, including Status, Priority, Department, Assignee, and SLA Plan, are automatically set according to the Help Topic's configurations. Notice that the ticket was sent to the Support department. We can see this ticket because our account (John Doe) is part of the Support department.  

Below that is the ticket thread. The ticket thread displays all of the replies between the user and the agents, internal notes, and updates to ticket properties. Currently, the only thing in the ticket thread is the original message sent when the user created the ticket. From the message, we understand that the entire banking department is unable to access the online banking portal.  
  
We are now in the Triage and Prioritization stage. This is where we perform an initial assessment of the ticket and gather information to determine the issue's severity and the appropriate person or team to resolve the issue.

<p align="center">
  <img width="939" height="613" alt="osticket-support-5" src="https://github.com/user-attachments/assets/9af14421-531b-4b59-9793-6a7b6fa44c31" />
</p>

At the bottom of the ticket is the reply box. This is where we can communicate with the user and provide updates on the progress of the ticket. When we post a reply, the user will receive an email, given we have selected them as a recipient.  

Since the issue affects the entire online banking system and is beyond our expertise, we will escalate the ticket to the SysAdmins department. Let's post a reply to the user acknowledging the issue and notifying them that the SysAdmin department will work on the issue and update them.

<p align="center">
  <img width="949" height="438" alt="osticket-support-6" src="https://github.com/user-attachments/assets/3d8b5da1-0db8-4968-8560-32782037d695" />
</p>

After posting the reply, we can see that the ticket is now assigned to us. In osTicket, the default setting is for an agent to automatically claim a ticket upon replying to it.  

We understand the issue and have decided to escalate the ticket, so we will update the ticket properties and ultimately change the Department. To change a ticket property, click on the specific property.

<p align="center">
  <img width="645" height="248" alt="osticket-support-7" src="https://github.com/user-attachments/assets/0c49b3b2-b036-46d2-b2c4-534397ea64cf" />
</p>

First, let's change the Help Topic. It is possible for users to select the wrong Help Topic when they create tickets. In this case, the Help Topic should be "Report a Problem / Business Critical Outage" because the issue is a system outage affecting all employees and preventing them from completing their work.

<p align="center">
  <img width="641" height="248" alt="osticket-support-8" src="https://github.com/user-attachments/assets/277c5f6e-5900-4dfe-b9f5-2e2219ea9220" />
</p>

Next is the Priority Level. The Priority Level signals to agents which tickets they should respond to first. Categorizing priority will often differ based on organizational policies, but is typically based on business impact. Since the issue affects a large number of people and blocks business operations, we will change the Priority Level to "Emergency". We can leave an optional note that we are changing the Priority Level because the issue is business critical.

<p align="center">
  <img width="641" height="248" alt="osticket-support-9" src="https://github.com/user-attachments/assets/520bea0b-4170-4a11-928e-16f2a0b10cc2" />
</p>

The SLA Plan usually goes hand in hand with the Priority Level. It also indicates the urgency with which the ticket should be handled and determines how much time is allowed to pass before the ticket is overdue. We will change the SLA Plan to Sev-A, the highest severity, and note that the update is being made because the issue is business critical.

<p align="center">
  <img width="643" height="287" alt="osticket-support-10" src="https://github.com/user-attachments/assets/6e2ee862-caa8-46cb-8c58-8c393479eeb9" />
</p>

Next, we will change the Assignee from ourselves to a member of the SysAdmins department, Jane Doe.

<p align="center">
  <img width="643" height="272" alt="osticket-support-11" src="https://github.com/user-attachments/assets/a96cf683-20ff-4e88-b3a0-07dfa4fa86fe" />
</p>

Lastly, we will change the Department to SysAdmins, giving access to agents that specialize in system outages. We can write a note to explain why the change is being made.  
  
**Note:** We change this property last because it will affect our access to the ticket.

<p align="center">
  <img width="954" height="381" alt="osticket-support-12" src="https://github.com/user-attachments/assets/c87be14c-211e-4da9-bacf-822b33b710bc" />
</p>

After we change the Department, we are sent back to our ticket queue with a notification saying "Access denied". We also no longer see the ticket in our ticket queue.

<p align="center">
  <img width="954" height="355" alt="osticket-support-13" src="https://github.com/user-attachments/assets/6f2c28d2-75ba-4133-831b-c0d8f1c9a28d" />
</p>

Let's sign out of the John Doe account and log in to Jane Doe's account. We will see Ken's ticket in the ticket queue since Jane is in the SysAdmins department.  

Now we will go through the Assignment and Investigation stage of the ticket lifecycle. We have been assigned the ticket as Jane, and we will look into the cause of the issue. Since the entire online banking system is down, we should check the server that hosts the website. Let's say we check the server and find that it is unresponsive. We should restart the server to clear the memory and terminate any hung processes, and see if that fixes the issue. 

<p align="center">
  <img width="933" height="613" alt="osticket-support-14" src="https://github.com/user-attachments/assets/c1b7010f-dc1d-4519-96fe-d70f1b16f76a" />
</p>

We will communicate to the ticket owner that we have 

<p align="center">
  <img width="643" height="221" alt="osticket-support-15" src="https://github.com/user-attachments/assets/96fe04e4-5a36-4dcc-a53e-b01882492161" />
</p>

### Creating a Ticket as an Agent 

<p align="center">
  <img width="954" height="341" alt="osticket-support-16" src="https://github.com/user-attachments/assets/89830e63-b6a2-42a8-9201-c737e03700ff" />
</p>

<p align="center">
  <img width="643" height="388" alt="osticket-support-17" src="https://github.com/user-attachments/assets/c7a35305-7ca1-4cba-b511-58e225c27b25" />
</p>

<p align="center">
  <img width="951" height="772" alt="osticket-support-18" src="https://github.com/user-attachments/assets/53f14840-d2a9-4d93-9b66-6c25e1d3898e" />
</p>

<p align="center">
  <img width="940" height="591" alt="osticket-support-19" src="https://github.com/user-attachments/assets/0d151397-3727-40b3-a94e-5b2ec25e1bf5" />
</p>

<p align="center">
  <img width="643" height="220" alt="osticket-support-20" src="https://github.com/user-attachments/assets/fa0630e3-f36a-41f0-9d6a-ff28f822ebf9" />
</p>

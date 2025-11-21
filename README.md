<img width="1654" height="450" alt="agent_tickets_ticket_ticketQueue" src="https://github.com/user-attachments/assets/ec2266b2-bb97-4134-adba-d95fa9412a0a" />


<h1>OSticket Ticket Lifecycle Walkthrough</h1>

This walkthrough demonstrates how tickets move through the osTicket system. It covers department preparation, ticket creation from the end user perspective, agent actions, SLA handling, and behavior changes when ticket severity escalates.

<h2>Video Demonstration</h2>

- ### [YouTube: OSticket Lifecycle](https://youtu.be/W35YbFnIiE4)
---

## Table of Contents
- [Accessing osTicket](#accessing-osticket)
- [Preparing Departments](#preparing-departments)
- [Scenario 1: Banking Outage](#scenario-1-banking-outage)
- [Scenario 2: Adobe Upgrade Issue](#scenario-2-adobe-upgrade-issue)
- [Scenario 3: CFO Laptop Failure](#scenario-3-cfo-laptop-failure)
- [Severity and Access Behavior](#severity-and-access-behavior)
- [Completing All Tickets](#completing-all-tickets)

---

## Accessing osTicket

<table>
  <tr>
    <td><img width="1920" height="1080" alt="Screenshot (217)" src="https://github.com/user-attachments/assets/9ed0c2ca-a014-4e8b-bfca-1e66466186d4"" /></td>
    <td><img width="1920" height="1080" alt="Screenshot (218)" src="https://github.com/user-attachments/assets/49d88795-111a-416b-819c-381c0ae960dc" /></td>
  </tr>
</table>

Begin by confirming access to the two main interfaces.

**Admin or Analyst Login:**  
`http://localhost/osTicket/scp/login.php`

**End User Portal:**  
`http://localhost/osTicket`

These links allow the lab participant to act as an end user and as a help desk agent.

---

## Preparing Departments
<img width="80%" height="80%" alt="Screenshot (234)" src="https://github.com/user-attachments/assets/17435827-f709-4411-b0d4-fcb710a49424" />

Before working with tickets, update the department structure.

Actions:
- Change **SysAdmins** to a top-level department  
- Delete the **Maintenance** department  

This ensures that the ticket routing aligns correctly with later scenarios.

---

## Scenario 1: Banking Outage
<img width="80%" height="80%" alt="Screenshot (235)" src="https://github.com/user-attachments/assets/a229dcb4-490d-4a27-828f-742cfca69a8d" />

This scenario focuses on a critical outage affecting online banking.

### As an End User
Create a ticket with the issue:  
**“Entire mobile or online banking system is down”**

### As Agent john
Observe the assigned ticket properties:
- Priority  
- Department  
- SLA  
- Assigned To  

Set updated properties:
- SLA: **Sev A** (1 hour, 24/7)  
- Department: **Online Banking**

Attempt to view or update again as john and note any changes in access.

### As Agent jane
Work the ticket to completion by responding, updating status, and resolving it.

---

## Scenario 2: Adobe Upgrade Issue
<img width="80%" height="80%" alt="Screenshot (236)" src="https://github.com/user-attachments/assets/16c1e0b7-668b-4a5b-80a4-e85b4f7540c4" />

This scenario simulates a medium-priority support request.

### As an End User
Create a ticket with the issue:  
**“Accounting department needs Adobe upgrade, broken”**

### As Agent john
Observe the initial properties, then update:
- SLA: **Sev B** (4 hours, 24/7)  
- Department: **Support**

Work the ticket to completion as john.

---

## Scenario 3: CFO Laptop Failure
<img width="80%" height="80%" alt="Screenshot (237)" src="https://github.com/user-attachments/assets/fd310ec3-011b-44fb-a226-577b79c854bd" />

This scenario represents an executive-level hardware issue.

### As an End User
Create a ticket with the issue:  
**“CFO’s laptop will no longer turn on”**

### As Agent john
Observe the ticket, then assign:
- SLA: **Sev B** (4 hours, 24/7)  
- Department: **Support**

Work the ticket to completion as john.

---

## Severity and Access Behavior
<img width="80%" height="80%" alt="Screenshot (238)" src="https://github.com/user-attachments/assets/b314cb42-6f33-4e11-b007-e499163b4e1d" />

This section illustrates how severe tickets affect visibility for agents.

Actions:
1. Update properties on all tickets  
2. Mark the **SysAdmins** ticket as **Sev A** last  
3. Observe that the ticket becomes inaccessible in the Agent Panel  
4. Switch to the **Admin Panel** and assign yourself *View Access* to SysAdmins  
5. Return to the Agent Panel  
6. Observe the escalated ticket  

You should be able to view it but not modify it due to restricted access.

---

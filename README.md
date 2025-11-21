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

Begin by confirming access to the two main interfaces.

**Admin or Analyst Login:**  
`http://localhost/osTicket/scp/login.php`

**End User Portal:**  
`http://localhost/osTicket`

These links allow the lab participant to act as an end user and as a help desk agent.

---

## Preparing Departments

Before working with tickets, update the department structure.

Actions:
- Change **SysAdmins** to a top-level department  
- Delete the **Maintenance** department  

This ensures that the ticket routing aligns correctly with later scenarios.

---

## Scenario 1: Banking Outage

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

## Completing All Tickets

Resolve all remaining tickets in the queue to finish the lab.

Note: Many ticketing systems including osTicket send emails for every update. End users can reply directly to those messages and the replies will be added to the ticket thread.

---

## Optional Screenshots Section

```html
<table>
  <tr>
    <td><img src="image1.png" width="300"></td>
    <td><img src="image2.png" width="300"></td>
  </tr>
  <tr>
    <td><img src="image3.png" width="300"></td>
    <td><img src="image4.png" width="300"></td>
  </tr>
</table>

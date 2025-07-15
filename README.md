## Employee Onboarding & Offboarding Automation Lab

Showcasing integration skills with Google Workspace, Slack, Airtable, and Asana for modern employee lifecycle management.

---

## Overview

This lab demonstrates how to automate onboarding and offboarding for employees using SaaS tools, focusing on user accounts, permissions, and integration best practices. All examples are based on real-world scenarios and implemented using no-code and low-code tools (Zapier/Make, native automations, APIs).

---

## Diagram

           ┌────────────────┐
           │    Airtable    │
           │  Employee Base │
           └───────┬────────┘
                   │  (new/updated record)
                   ▼
         ┌────────────────────┐
         │  Zapier/Make Flow  │
         └─┬───────┬────────┬─┘
           │       │        │
           ▼       ▼        ▼
   ┌─────────┐ ┌────────┐ ┌────────┐
   │ Google  │ │ Slack  │ │ Asana  │
   │Workspace│ │        │ │        │
   └─────────┘ └────────┘ └────────┘
           │       │        │
       (updates, tasks, messages)
                   │
                   ▼
           ┌───────────────┐
           │   Airtable    │
           │ (Status Log)  │
           └───────────────┘
           
---

## Tool Integrations

1. Airtable – Source of Truth
- Employee Directory base with fields: Name, Email, Role, Manager, Status (Onboarding/Active/Offboarding)
- Automation Trigger: When a row is added or status is updated

2. Google Workspace – Account Management
- Onboarding: Auto-create user accounts, assign roles/groups, set permissions (via Zapier or Google Apps Script)
- Offboarding: Suspend/delete accounts, transfer docs

3. Slack – Communication
- Onboarding: Auto-invite to workspace, add to default/team channels, send welcome DM
- Offboarding: Remove from channels, deactivate account

4. Asana – Task Management
- Onboarding: Create project/checklist for new hire (tasks: “Read Handbook”, “Set up 2FA”, “Meet Manager”)
- Offboarding: Reassign/close open tasks, archive user projects

---

## Automation Flow

## Onboarding

- I create an Employee Directory in Airtable with these fields: Name, Email, Role, Manager, Status (Onboarding/Active/Offboarding).
- When a new employee row is added and Status = 'Onboarding', automation is triggered.
- Automation Platform (Zapier or Make)
- The automation (Zap) starts when an Airtable record’s Status = 'Onboarding'.

Actions:

- Create a Google Workspace account with correct group/OU.
- Add the user to Slack, auto-join #general, #onboarding, and team channels.
- Create an onboarding task project in Asana, assign it to the new hire and their manager.
- Log all actions and account usernames back in Airtable.
- Send a personalized Slack DM to the new hire with their onboarding steps.

---

## Offboarding

- "When HR sets Status = 'Offboarding' in Airtable:"
- Suspend Google account, transfer files to manager.
- Deactivate Slack account.
- Close or reassign all Asana tasks/projects.
- Update Airtable record with offboarding date.

---

## Sample Zapier/Make Workflow Steps

Onboarding:
1. Trigger: Airtable “Status” = Onboarding
2. Action: Google Workspace – Create user, add to group
3. Action: Slack – Invite user, add to #onboarding, send DM
4. Action: Asana – Create onboarding task list, assign to user
5. Action: Airtable – Update “Workspace/Slack Username”, “Onboarding Complete” checkbox

Offboarding:
1. Trigger: Airtable “Status” = Offboarding
2. Action: Google Workspace – Suspend user, transfer ownership
3. Action: Slack – Deactivate user
4. Action: Asana – Reassign/close tasks
5. Action: Airtable – Update “Offboarding Complete”

---

## Permissions & Security

- Google Workspace: Role-based OUs/groups for granular permissions  
- Slack: Channel access by team/role  
- Airtable: Base access limited to HR/managers  
- Asana: Projects shared with relevant team only

---

## Screenshots

- Airtable Employee Directory sample  
- Example Zapier/Make workflow  
- Google Workspace Admin (user creation)  
- Slack Welcome Message sample  
- Asana Onboarding Project sample

---

## Why This Matters

- Security: Automated deprovisioning protects company data  
- Efficiency: Saves HR/IT time, reduces manual errors  
- Great Experience: Consistent, welcoming onboarding

---

Sebastian Silva C. - July, 2025 - Berlin, Germany

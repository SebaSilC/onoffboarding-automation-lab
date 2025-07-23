## Employee Onboarding & Offboarding Automation Lab

Showcasing integration skills with Google Workspace, Slack, Airtable, and Asana for modern employee lifecycle management.

---

## Table of Contents

- [Overview]
- [Real-World Risk]
- [What I Built]
- [Diagram]
- [Objectives]
- [Steps Performed]
  - [1. Employee Directory Setup in Airtable]
  - [2. Onboarding Project Creation in Asana]
  - [3. Google Workspace User Provisioning]
  - [4. Slack Access Management]
  - [5. Zapier Workflow Automation]
- [Screenshots]
- [Lessons Learned]
- [Permissions & Security]
- [Extra Capabilities]
- [References]

---

## Overview

This lab demonstrates how to automate onboarding and offboarding for employees using SaaS tools, focusing on user accounts, permissions, and integration best practices. All examples are based on real-world scenarios and implemented using no-code and low-code tools (Zapier/Make, native automations, APIs)

---

## Real-World Risk

Manual onboarding and offboarding can lead to security gaps (such as lingering access after offboarding or missed permissions for new hires), inconsistent experiences and lost productivity. Automating these workflows reduces human error, speeds up operations and helps ensure compliance.

---

## What I Built

- An end-to-end automated onboarding and offboarding workflow using Airtable, Google Workspace, Slack, Asana and Zapier.
- Automated creation, permissioning, and deactivation of accounts.
- Task assignment and tracking for HR/IT and new hires.
- Real-time logging of all actions for audit and compliance.

---

## Diagram

![Automation Flow Diagram](./diagram.png)

---

## Objectives

- Eliminate manual steps and potential errors in the onboarding/offboarding process.
- Ensure fast, secure provisioning and deprovisioning of user accounts and access.
- Centralize all onboarding data and status for easy management and auditing.
- Create a smooth, welcoming experience for new employees.

---

## Steps Performed

**1. Employee Directory Setup in Airtable**
   - Created an Airtable base with fields for employee Name, Email, Role, Manager and Status (Onboarding/Active/Offboarding), like the following table:
     
   | Name        | Email             | Role      | Manager   | Status        |
   |-------------|-------------------|-----------|-----------|---------------|
   | Jane Smith  | jane@company.com  | Engineer  | J. Brown  | Onboarding    |
   | ...         | ...               | ...       | ...       | ...           |

   - Set up automations to trigger onboarding/offboarding flows based on the Status field *(Screenshot: airtable-employee-directory.png)*

**2. Onboarding Project Creation in Asana**
   - Designed an onboarding project template in Asana with tasks for new hires (e.g., account setup, document review)
   - Linked Asana to the automation flow for task assignment *(Screenshot: asana-onboarding-project.png)*

**3. Google Workspace User Provisioning**
   - Automated creation of new Google Workspace user accounts with correct organizational units and permissions.
   - Ensured that offboarding disables accounts and transfers ownership of company data *(Screenshot: google-workspace-admin.png)*

**4. Slack Access Management**
   - Automated Slack invitations for new hires, adding them to relevant channels and sending a welcome message.
   - Offboarding process removes users from workspace and channels *(Screenshot: slack-welcome-message.png)*

**5. Zapier Workflow Automation**
   - Built a Zapier flow that connects Airtable with Google Workspace, Slack and Asana to orchestrate onboarding/offboarding tasks end-to-end.
   - Ensures all actions are tracked and status updates are logged *(Screenshot: zapier-onboarding-flow.png)*

---

## Screenshots

*All screenshots are included in the screenshots/ folder of this repository.*

| Order | File Name                        | What it Shows                                                                                                   |
|-------|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| 1     | airtable-employee-directory.png  | Airtable Employee Directory with fields for Name, Email, Role, Manager and Status, tracking onboarding status.  |
| 2     | asana-onboarding-project.png     | Asana onboarding project listing new hire tasks, assignees and due dates.                                       |
| 3     | google-workspace-admin.png       | Google Workspace Admin panel showing how to add a new user and assign organizational unit.                      |
| 4     | slack-welcome-message.png        | Example Slack direct message to a new hire with onboarding instructions and relevant channels.                  |
| 5     | zapier-onboarding-flow.png       | Zapier workflow (Zap) automating onboarding steps from Airtable to Google Workspace, Slack and Asana.           |

---

## Lessons Learned

- Integrating SaaS tools can dramatically improve HR and IT workflows.
- Clear process documentation and automation reduce risk and free up time.
- Centralized tracking (Airtable) helps prevent things from slipping through the cracks.
- Proactive offboarding is just as important as onboarding for security.
- Small touches—like welcome messages and task checklists—improve the employee experience.

---

## Permissions & Security

- Google Workspace: Role-based OUs/groups for granular permissions.  
- Slack: Channel access by team/role.  
- Airtable: Base access limited to HR/managers.  
- Asana: Projects shared with relevant team only.

---

## Extra Capabilities

- **Device Assignment:** Airtable tracks laptops/devices issued to employees; flagged on offboarding for collection.
- **Endpoint Security:** 2FA enabled on Google Workspace and Slack by default; access revoked immediately on offboarding.
- **IT Support:** #it-support Slack channel for day-to-day help; urgent tickets can trigger Asana task creation automatically.
- **Security Training:** Automated reminders for phishing/security awareness can be assigned via Asana.

---

## References

- [Zapier Help Center](https://help.zapier.com/)
- [Airtable Automations](https://support.airtable.com/docs/automations-overview)
- [Google Workspace Admin Help](https://support.google.com/a/)
- [Slack Help Center](https://slack.com/help/categories/200111606)
- [Asana Guide](https://asana.com/guide)

---

Sebastian Silva C. - July, 2025 - Berlin, Germany

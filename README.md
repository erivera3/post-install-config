<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo" width="300">
</p>

<h1 align="center">osTicket Help Desk Deployment & Service Configuration (Enterprise Simulation)</h1>
This project demonstrates the deployment and post-installation configuration of an osTicket help desk system, with a focus on structuring a functional support environment rather than completing a basic installation. The implementation emphasizes role-based access control, departmental segmentation, cross-functional team design, controlled user access, SLA enforcement, and structured ticket intake. The objective was to transform a default installation into an operational service desk that reflects how real IT support systems manage ownership, visibility, and response expectations.

---

## 🎯 Goals & Objectives

The goal of this project was to configure osTicket into a structured and operational help desk environment.

By the end of this lab, I aimed to:

- Establish separate access layers for administrators, agents, and end users  
- Implement role-based permissions to control administrative capabilities  
- Define departments to enforce ticket visibility boundaries  
- Configure teams to enable cross-department collaboration  
- Provision agents and users to simulate real support workflows  
- Apply SLA policies to enforce time-based response expectations  
- Structure ticket intake using help topics for consistent categorization  

---

## 📌 Overview

A local osTicket environment was deployed and configured to simulate a real-world IT help desk. The focus was on post-installation configuration, including access control, workflow structure, and service behavior. The system was designed to reflect how tickets are submitted, routed, managed, and resolved across different support roles.

---

## 🧰 Technologies Used

- osTicket  
- PHP  
- MySQL  
- Web server (localhost environment)  
- Browser-based administrative interface  
- Role-Based Access Control (RBAC)  
- SLA policy management  

---

## 💻 Environment

- **OS:** Localhost-based lab environment  
- **Application:** osTicket  
- **Admin/Analyst Login Page:** `http://localhost/osTicket/scp/login.php`  
- **End User Portal:** `http://localhost/osTicket`  
- **Key Areas Configured:**
  - Agents / Roles  
  - Agents / Departments  
  - Agents / Teams  
  - Settings / User Settings  
  - Manage / SLA  
  - Manage / Help Topics  

---

## ⚙️ Implementation

### 1. Access Layer Separation

Separate access points were validated for administrators and end users. The admin login page provides authenticated access to the control panel, while the user portal allows ticket submission and status tracking.

This separation ensures that system configuration and ticket operations are not exposed to external users.

<p align="center"><img src="images/admin_login.png" width="700"></p>

<p align="center"><img src="images/user_portal.png" width="700"></p>

---

### 2. Administrative vs Operational Interface

The system was divided into two primary interfaces:

- **Admin Panel** for configuration and system management  
- **Agent Panel** for ticket handling and user interaction  

This distinction ensures that administrative controls are isolated from operational workflows.

<p align="center"><img src="images/admin_panel_dashboard.png" width="700"></p>

<p align="center"><img src="images/agent_panel_dashboard.png" width="700"></p>

---

### 3. Role-Based Access Control

Roles were configured to define permission levels across the system. Default roles were reviewed and unnecessary roles were disabled, prioritizing a controlled access model using the **Supreme Admin** role.

This ensures that permissions are structured and not assigned arbitrarily.

<p align="center"><img src="images/roles_config.png" width="700"></p>

---

### 4. Department Segmentation

Departments were configured to define ticket visibility and ownership boundaries. The **SysAdmins** department was created alongside existing departments to separate support responsibilities.

This prevents all agents from having unrestricted access to all tickets.

<p align="center"><img src="images/departments_sysadmins.png" width="700"></p>

---

### 5. Cross-Functional Team Structure

Teams were configured to allow collaboration across departments. The **Online Banking** team represents a service-based grouping that can include agents from different departments.

This allows support to be organized around services rather than strictly departmental roles.

<p align="center"><img src="images/team_online_banking.png" width="700"></p>

---

### 6. User Access Control

User settings were configured to require authentication before ticket submission. Registration is open, but users must log in to create tickets.

This enforces accountability while maintaining accessibility.

<p align="center"><img src="images/user_settings_registration.png" width="700"></p>

---

### 7. Agent and User Provisioning

Agents were created and assigned to departments to simulate support staff:

- Jane — SysAdmins  
- John — Support  

Users were created to simulate ticket submission:

- Karen  
- Ken  

This establishes a functional interaction model between requesters and support staff.

<p align="center"><img src="images/agents_list.png" width="700"></p>

<p align="center"><img src="images/users_list.png" width="700"></p>

---

### 8. SLA Policy Configuration

SLA policies were implemented to define response expectations:

- **Sev-A:** 1 hour (24/7)  
- **Sev-B:** 4 hours (24/7)  
- **Sev-C:** 8 hours (Business Hours)  

This enforces time-based accountability for ticket resolution.

<p align="center"><img src="images/sla_policies.png" width="700"></p>

---

### 9. Ticket Intake Structuring

Help topics were configured to standardize ticket submission and improve routing:

- Business Critical Outage  
- Personal Computer Issues  
- Equipment Request  
- Password Reset  
- Other  

This ensures tickets are categorized consistently at intake.

<p align="center"><img src="images/help_topics.png" width="700"></p>

---

## 🔍 Troubleshooting

### Panel Confusion (Admin vs Agent)
- **Problem:** Configuration attempted in the wrong interface  
- **Cause:** Misunderstanding of panel separation  
- **Fix:** Verified context using navigation tabs and panel toggle  

---

### Incorrect Navigation (Roles vs Departments)
- **Problem:** Accessed Roles instead of Departments  
- **Cause:** Similar menu structure under Agents  
- **Fix:** Confirmed correct URL and section before capturing  

---

### Open vs Restricted Ticket Access
- **Problem:** Conflicting configuration for ticket submission policy  
- **Cause:** Misinterpretation of user settings  
- **Fix:** Enforced registration-required model for controlled access  

---

## 🧠 Design Decisions

- **Registration Required:** Ensures accountability and prevents anonymous ticket abuse  
- **Department Segmentation:** Limits ticket visibility and enforces ownership  
- **Team Structure:** Enables cross-functional collaboration without flattening hierarchy  
- **SLA Policies:** Introduces measurable response expectations  
- **Role Simplification:** Reduces unnecessary permission complexity  

---

## 🛡️ System Awareness

- Ticket visibility is controlled by departments, not roles  
- Roles define permissions, not data access scope  
- Teams provide cross-department collaboration without removing boundaries  
- SLA policies depend on time and schedule configuration  
- User access settings directly affect system exposure and intake control  
- Misconfiguration in any layer impacts system behavior and workflow  

---

## 🌍 Real-World Relevance

This project reflects how enterprise help desk systems are structured in real IT environments. It applies to:

- Internal IT support teams  
- Managed Service Providers (MSPs)  
- Security and operations support desks  
- Enterprise service management platforms  

The configuration decisions directly impact efficiency, accountability, and system reliability.

---

## 📌 Lessons Learned

- Installation alone does not create a functional system  
- Access control must be structured, not assumed  
- Departments and teams solve different organizational problems  
- SLA policies give meaning to ticket priority  
- Ticket intake design affects downstream workflow efficiency  
- System behavior is determined by configuration, not just software  

---

## 💭 Key Takeaways

This project reinforced that deploying a system is only the starting point. Real value comes from how the system is structured, controlled, and operated. I now understand how access, ownership, and response expectations define the effectiveness of a help desk environment.

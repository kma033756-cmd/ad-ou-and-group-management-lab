# Active Directory OU Infrastructure & Group Management Lab (`ETHA.com`)

## 📌 Project Overview
This repository documents the planning and implementation of Active Directory Organizational Units (OUs), security and distribution groups, IGDLA group nesting strategies, and user template automation using **Active Directory Users and Computers (ADUC)** and the **Active Directory Administrative Center (ADAC)** on Windows Server.

## 🏗️ Environment Architecture
* **Domain Controller:** `STO-DC1` (`ETHA.com`)
* **Core Tooling:** Active Directory Administrative Center (ADAC), ADUC, Windows PowerShell
* **Domain Functional Level:** Windows Server 2025

---

## ⚙️ Key Tasks & Technical Implementation

### 1. OU Infrastructure Planning & Creation
* Configured advanced Active Directory features and enabled the **AD Recycle Bin** with confirmation.
* Created top-level Organizational Units (OUs) to structure enterprise departments under `ETHA.com`:
  * `IT`
  * `Managers`
  * `Marketing`
  * `Research`
  * `Sales`

### 2. User & Group Management via ADAC
* Provisioned user accounts across departmental OUs (e.g., `Amr Zaki`, `April Reagan`, `Beth Burke`, `Brad Sutton`, `Allie Bellew`).
* Created **Security Global Groups** for each department to manage granular permissions.
* Created and managed **Distribution Groups** (e.g., `Research Mail`) and configured group managers.
* Converted group types between Distribution and Security scopes within ADAC.

### 3. IGDLA Group Nesting Strategy
* Implemented Microsoft’s **IGDLA** strategy (Accounts in **G**lobal groups, Global groups in **D**omain Local groups, applied to **A**ccess **L**ocal resources) to establish scalable, best-practice access control across the domain.

### 4. Automated User Provisioning Using Templates
* Created a standardized template account (`_ResearchTemplate`) with pre-configured organizational details, company name (`ETHA Corporation`), department assignments, and default profile settings.
* Copied and cloned new user accounts (e.g., `Research User`) rapidly from the template to ensure uniform configuration and compliance across branch office deployments.

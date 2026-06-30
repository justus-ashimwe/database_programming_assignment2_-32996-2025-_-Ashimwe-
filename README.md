Oracle Multitenant Architecture & Pluggable Database (PDB) Management Project

## 📋 Student & Repository Information
* **Full Name:** Ashimwe Bienaime Justus
* **Student ID:** 32996/2025
* **GitHub Repository:** [database_programming_assignment2_-32996-2025-_-Ashimwe-](https://github.com/justus-ashimwe/database_programming_assignment2_-32996-2025-_-Ashimwe-)
* **Created PDB Name:** `ja_pdb_32996`
* **Created Username:** `Ashimwe_plsqlauca_32996`
* **Issues Encountered:** Yes (Resolved)

---

## 🎯 Assignment Overview
This individual practical assignment demonstrates hands-on Oracle Database Administration skills. It focuses on the practical implementation of the Oracle Multitenant Architecture, Pluggable Database (PDB) lifecycle management, and user security configurations.

---

## 💻 Oracle Environment & Tools
* **Oracle Version:** Oracle Database 21c Express Edition (Version 21.3.0.0.0)
* **Operating System:** Microsoft Windows 10 (64-bit)
* **Tools Used:**
  * **SQL*Plus:** For executing administrative commands and SQL scripts.
  * **Oracle Enterprise Manager (OEM) Database Express:** For graphical database monitoring.
  * **Command Prompt:** For establishing local Oracle database connections.
  * **GitHub:** For version control and documentation tracking.

---

## 🛠️ Task Documentation

### Task 1: PDB Creation and User Configuration

#### 1. PDB Creation Process
A personal Pluggable Database (PDB) was successfully created inside the Oracle Container Database (CDB) following the requested naming conventions:
* Connect to the Oracle Container Database using `SYSDBA` privileges.
* Execute the PDB creation command to provision `ja_pdb_32996`.
* Alter the PDB state to **OPEN**.
* Verify status via administrative data dictionary views (`V$PDBS`).

#### 2. User Creation & Privileges
After initializing the PDB, a localized database user was provisioned within the pluggable environment:
* Switch the current container session to `ja_pdb_32996`.
* Create the user account `Ashimwe_plsqlauca_32996` with a secure password.
* Grant administrative and object-level roles/privileges required for database interaction.
* Verify user active status inside the target PDB.

---

### Task 2: Temporary PDB Creation and Deletion
To demonstrate complete mastery over PDB lifecycle actions, a temporary Pluggable Database was created and subsequently decommissioned:
1. **Creation:** Provisioned a temporary PDB using standard naming parameters.
2. **Verification:** Confirmed its existence within the container environment.
3. **Activation:** Opened the database to simulate an operational state.
4. **Deconstruction:** Properly closed and deleted the temporary PDB from physical storage.
5. **Final Check:** Verified that all associated database files were permanently erased.

---

### Task 3: Oracle Enterprise Manager (OEM) Configuration
Oracle Enterprise Manager Database Express was successfully integrated and utilized to monitor database health:
* Web browser connection established to the OEM port using `SYSDBA` credentials.
* **Monitored Dashboard Metrics:**
  * Database instance version and uptime status.
  * Host platform resource usage.
  * Storage allocations and pluggable architecture mapping details.

---

## ⚠️ Challenges Encountered & Solutions

### 1. ORA-01031: Insufficient Privileges
* **Problem:** The system blocked the execution of the PDB opening sequence due to inadequate session permissions.
* **Solution:** Re-established the terminal session utilizing explicit `AS SYSDBA` credentials and ensured commands were pointing to the root container.

### 2. ORA-00959: Tablespace Does Not Exist
* **Problem:** Attempting to assign space quotas failed because the target `USERS` tablespace did not exist inside the newly initialized PDB.
* **Solution:** Explicitly created the missing `USERS` tablespace within the PDB boundary before re-executing the user quota assignment script.

---

## 📝 Short Reflection & Lessons Learned
This assignment provided critical real-world experience in Oracle Database Administration. It bridged the gap between theory and practice regarding Oracle Multitenant Architectures. 

Through this practical execution, I gained skills in:
* Administering independent pluggable databases within a single container.
* Managing database user initialization, roles, and resource isolation via tablespaces.
* Resolving common Oracle system errors using troubleshooting methodologies.
* Documenting system architecture configurations cleanly via version control platforms.

---

## ⚖️ Integrity Statement
I declare that this assignment represents my own individual work. All database creations, user configurations, and documentation were performed personally in accordance with academic integrity guidelines.

I confirm that this assignment represents my own practical work, screenshots, and documentation. All external resources consulted have been properly acknowledged.

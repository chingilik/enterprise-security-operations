# Enterprise Security Operations

**Enterprise Defensive Security Lab: Active threat hunting, SIEM deployment, and Active Directory hardening within a Windows Server environment.**

## 📌 Project Overview
This repository documents the deployment and administration of an enterprise-grade Security Operations Center (SOC) home lab. The environment is designed to simulate real-world attacks, capture high-fidelity security telemetry, and implement strict network segmentation and defensive hardening.

## 🏗️ Lab Architecture
* **SIEM Server:** Ubuntu Server LTS (Secured via Ubuntu Pro ESM) hosting the Wazuh Manager, Indexer, and Dashboard.
* **Target Endpoint / Domain Controller:** Windows Server.
* **Privileged Access Workstation (PAW):** Kali Linux (Acting as the Purple Team Jump Box for secure administration and offensive testing).
* **Network:** Isolated VirtualBox NAT Network to simulate an internal enterprise LAN.

---

## 🚀 Deployment Phases & Milestones

### Phase 1: SIEM Infrastructure Deployment (Completed)
* Provisioned an Ubuntu LTS server with OpenSSH for secure remote management.
* Deployed the full Wazuh SIEM stack (Manager, Indexer, Dashboard).
* Successfully initialized the API and established the central log aggregation database.
* *Evidence:* ![Wazuh-dashboard](https://github.com/chingilik/enterprise-security-operations/blob/main/screenshots/Wazuh-dashboard.png)

### Phase 2: Administrative Segmentation & Jump Box (In Progress)
* *Pending:* Deploying a Kali Linux Jump Box to enforce Separation of Duties.
* *Pending:* Establishing secure SSH (CLI) and Web (GUI) management routes to the SIEM.
* *Pending:* Locking down the environment so administration is strictly handled via the dedicated Privileged Access Workstation.

### Phase 3: Endpoint Visibility & Live Fire Testing (Pending)
* *Pending:* Deploying the Wazuh Agent to the Windows Server using a custom PowerShell deployment script.
* *Pending:* Configuring the endpoint to forward Windows Event Logs to the SOC (Port 1514).
* *Pending:* **Live Fire Exercise:** Executing a simulated brute-force authentication attack against the Windows Server using offensive tools from the Kali Jump Box.
* *Pending:* Successfully catching and indexing Windows Event ID 4625 (Logon Failure) alerts in the Wazuh Dashboard in real-time.

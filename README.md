# Windows Server 2025 Active Directory Home Lab Infrastructure

## 🛠️ Project Overview
This project demonstrates the deployment of an isolated Active Directory Domain Services (AD DS) infrastructure environment inside an Oracle VM VirtualBox hypervisor sandbox. This lab implements robust static network addressing schemes and secure corporate identity user accounts.

## 📐 Environment Topology
* **Hypervisor Platform:** Oracle VM VirtualBox[span_0](start_span)[span_0](end_span)[span_1](start_span)[span_1](end_span)
* **Server Infrastructure Node:** Windows Server 2025 Standard Evaluation[span_2](start_span)[span_2](end_span)[span_3](start_span)[span_3](end_span)
* **Target Domain Architecture Forest:** `subin.local`[span_4](start_span)[span_4](end_span)[span_5](start_span)[span_5](end_span)
* **Private Network Subnet Scope:** `192.168.1.0/24`[span_6](start_span)[span_6](end_span)[span_7](start_span)[span_7](end_span)

---

## 💻 Technical Implementation Framework

### Step 1: Virtual Hypervisor Sandbox Isolation
* Migrated VirtualBox Guest network configuration from standard Wi-Fi Bridged access parameters down to an isolated **Host-only Adapter** mechanism[span_8](start_span)[span_8](end_span)[span_9](start_span)[span_9](end_span). This eliminates physical network overlap bugs and stops IP addressing conflicts (`169.254.x.x` APIPA errors)[span_10](start_span)[span_10](end_span)[span_11](start_span)[span_11](end_span).

### Step 2: Immutable Operating System Core IP Addressing
Configured static network infrastructure values inside the legacy Windows Control Panel adapter settings properties[span_12](start_span)[span_12](end_span)[span_13](start_span)[span_13](end_span):
* **Static Interface Target IP Address:** `192.168.1.10`[span_14](start_span)[span_14](end_span)[span_15](start_span)[span_15](end_span)
* **Subnet Private Class Mask:** `255.255.255.0`[span_16](start_span)[span_16](end_span)[span_17](start_span)[span_17](end_span)
* **Gateway Route Address Mapping:** `192.168.1.1`[span_18](start_span)[span_18](end_span)[span_19](start_span)[span_19](end_span)
* **Primary System DNS Namespace Resolution Loopback:** `192.168.1.10` *(Points Server locally to its own Active Directory Engine)*[span_20](start_span)[span_20](end_span)[span_21](start_span)[span_21](end_span)

### Step 3: Active Directory Domain Services Deployment
* Deployed the essential structural `AD DS` framework modules via Server Manager dashboard under **Role-Based Provisioning**[span_22](start_span)[span_22](end_span)[span_23](start_span)[span_23](end_span).
* Successfully initialized a root destination domain namespace tree specified as: `subin.local`[span_24](start_span)[span_24](end_span)[span_25](start_span)[span_25](end_span).
* Configured local Directory Services Restore Mode (`DSRM`) administrative backup authentication parameters[span_26](start_span)[span_26](end_span)[span_27](start_span)[span_27](end_span).

### Step 4: Schema Object & Operational Directory Provisioning
* Structured a dedicated organizational domain grouping target zone container via an **Organizational Unit (OU)** labeled `Employees`[span_28](start_span)[span_28](end_span)[span_29](start_span)[span_29](end_span).
* Populated the database directory with individual corporate system account access mappings[span_30](start_span)[span_30](end_span)[span_31](start_span)[span_31](end_span):
  1. `raj` (Subin Raj)[span_32](start_span)[span_32](end_span)[span_33](start_span)[span_33](end_span)
  2. `john` (John User)[span_34](start_span)[span_34](end_span)[span_35](start_span)[span_35](end_span)
  3. `testuser` (Test Account)[span_36](start_span)[span_36](end_span)[span_37](start_span)[span_37](end_span)

---

## 🔍 Validation Checkpoint
Deployment validation is confirmed when the `Active Directory Users and Computers` management console verified the uniform generation of the `Employees` Organizational Unit structure alongside its underlying core directory users[span_38](start_span)[span_38](end_span)[span_39](start_span)[span_39](end_span).


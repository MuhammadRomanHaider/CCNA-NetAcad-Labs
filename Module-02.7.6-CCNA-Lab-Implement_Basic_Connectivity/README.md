# CCNA Lab: 2.7.6 Packet Tracer - Implement Basic Connectivity

## 📌 Lab Overview
This repository documents the implementation and verification of basic network connectivity across Cisco switches and host end-devices. The lab demonstrates initial Cisco IOS device configuration, switch management interface (SVI) setup, host IP addressing, credential security hardening, and end-to-end ICMP connectivity testing.

---

## 📁 Deliverables
* ⚙️ **Packet Tracer Activity File:** `Implement_Basic_Connectivity.pka` 
* 🖼️ **Lab Screenshots & Verification Assets:** Embedded below in sequence.

---

## 🌐 Topology & Addressing Table

* [Topology Overview]

<img width="1920" height="1017" alt="pic2" src="https://github.com/user-attachments/assets/948ec987-636e-4404-b246-718e1a54c73f" />


| Device | Interface | IP Address | Subnet Mask |
| :--- | :--- | :--- | :--- |
| **S1** | VLAN 1 | `192.168.1.253` | `255.255.255.0` |
| **S2** | VLAN 1 | `192.168.1.254` | `255.255.255.0` |
| **PC1** | NIC | `192.168.1.1` | `255.255.255.0` |
| **PC2** | NIC | `192.168.1.2` | `255.255.255.0` |

---

## 🛠️ Configuration Workflow & Evidence

### Part 1: Basic Switch Configuration (S1 & S2)
* Configured hostnames (`S1` and `S2`).
* Configured line console password (`cisco`) and privileged EXEC mode secret (`class`).
* Applied legal warning banner (`banner motd`).
* Saved active configurations from RAM to NVRAM (`copy running-config startup-config`).
  
---

* [S1 Basic Password & Banner Configuration]


<img width="1917" height="1020" alt="pic3" src="https://github.com/user-attachments/assets/1a4da217-b4d2-4ddf-a663-d55395db9de5" />

*Figure 1: S1 privileged EXEC authentication and MOTD banner setup.*

* [S2 Configuration Verification & NVRAM Save]

<img width="1920" height="1020" alt="pic4" src="https://github.com/user-attachments/assets/d0e262fe-44c1-4933-af5e-2a563ddf233a" />

*Figure 2: S2 CLI line security verification and startup configuration commit.*

---

### Part 2: Host Interface IP Configuration
* Assigned static IPv4 addresses and subnet masks to `PC1` (`192.168.1.1/24`) and `PC2` (`192.168.1.2/24`).

* [PC2 IP Configuration]

<img width="1920" height="1020" alt="pic5" src="https://github.com/user-attachments/assets/c936c732-05d0-441b-a323-18734afdd128" />

*Figure 3: Static IPv4 configuration interface on PC2.*

---

### Part 3: Switch Management Interface (SVI) Setup & Initial Tests
* Tested initial connectivity prior to SVI configuration (expected failure).
* Configured IP addressing on `Vlan1` management interfaces for both `S1` and `S2`.
* Activated interfaces using `no shutdown`.

* [Initial Failed Ping Test]

<img width="1918" height="1022" alt="pic6" src="https://github.com/user-attachments/assets/b7e2d00b-dee6-4920-9bdf-b0f01e1ae920" />

*Figure 4: ICMP ping from PC1 to switch IP before SVI configuration (100% loss expected).*

* [S2 VLAN 1 SVI Address Configuration]

<img width="1920" height="1022" alt="pic7" src="https://github.com/user-attachments/assets/8dcb1650-7f5d-40d3-a0ee-689dec1875e7" />

*Figure 5: Assigning IP address to S2 interface Vlan1 and administrative enable (`no shutdown`).*

* [S2 Running Configuration Audit]

<img width="1920" height="1012" alt="pic8" src="https://github.com/user-attachments/assets/8c1c289f-78b3-4c69-8449-0001dba5ccad" />

*Figure 6: `show running-config` output confirming SVI parameters, MOTD, and VTY line configurations on S2.*

---

### Part 4: End-to-End Connectivity Verification
* Executed ICMP `ping` commands from `PC2` to verify end-to-end reachability across `PC1`, `S1`, and `S2`.

* [PC2 Ping Verification Output]

<img width="1920" height="1017" alt="pic9" src="https://github.com/user-attachments/assets/f6a7cd40-0a7c-464b-80ed-1e01dc37ccf0" />

*Figure 7: Successful ICMP ping tests confirming 100% reachability across all network nodes.*

---

## 📊 Completion & Assessment Verification

* [Packet Tracer Assessment Results]

<img width="1563" height="980" alt="pic10" src="https://github.com/user-attachments/assets/4c43ea89-3bb5-49d4-bac1-ebfb27df3156" />

*Figure 8: 100% Activity Completion status verifying all parameters (SVI status, IP addressing, passwords, hostnames, and NVRAM backups).*

---

## 🛠️ Core Skills Demonstrated
* **Cisco IOS CLI:** Device initialization, interface management, and security banner deployment.
* **Switch Management:** SVI (`Vlan1`) configuration and interface state control (`no shutdown`).
* **IPv4 Networking:** Subnet Mask application, host IP assignment, and interface status auditing.
* **Network Verification:** Diagnostics using `ping`, `show running-config`, and `show ip interface brief`.

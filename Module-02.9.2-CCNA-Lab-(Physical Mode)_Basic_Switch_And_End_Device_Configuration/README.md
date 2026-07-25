# 2.9.2 Lab - Basic Switch and End Device Configuration (Physical Mode)

## 📌 Lab Overview
In this Packet Tracer Physical Mode (PTPM) activity, network equipment including switches and PC hosts were selected from the shelf, placed in the rack and table workspace, and cabled according to physical port requirements. Basic Cisco IOS settings were configured on switches S1 and S2, IP parameters were assigned to end hosts, and full end-to-end connectivity was verified.

---

## 🌐 Network Topology & Addressing Table

<img width="1920" height="1026" alt="pic2" src="https://github.com/user-attachments/assets/dfadc685-b759-41a5-ab42-743e6b89d04d" />


| Device | Interface | IP Address | Subnet Mask |
| :--- | :--- | :--- | :--- |
| **S1** | VLAN 1 | 192.168.1.1 | 255.255.255.0 |
| **S2** | VLAN 1 | 192.168.1.2 | 255.255.255.0 |
| **PC-A** | NIC | 192.168.1.10 | 255.255.255.0 |
| **PC-B** | NIC | 192.168.1.11 | 255.255.255.0 |

---

## ⚙️ Configuration Workflow & Verification

### 1. Physical Topology Setup & Cabling
Mounted switches **S1** and **S2** in the rack, placed **PC-A** and **PC-B** on the workspace table, and cabled the devices using Ethernet copper straight-through cables according to the physical topology layout.

<img width="1920" height="1022" alt="pic3" src="https://github.com/user-attachments/assets/aa9f7d53-14ed-401d-a274-9cb534cff680" />


---

### 2. PC Host IP Configuration & Early Ping Test
Configured static IPv4 address parameters on **PC-A** (`192.168.1.10/24`) and tested connectivity prior to completing switch management interface setup.

<img width="1920" height="1020" alt="pic4" src="https://github.com/user-attachments/assets/1bc0d4d9-7afb-4e23-9265-c04dfbe41604" />


---

### 3. Switch Interface Status Verification
Connected console cabling from PC terminal software to examine operational status across active FastEthernet switch ports (`Fa0/1` trunk/inter-switch link and `Fa0/6` access link).

<img width="1920" height="1022" alt="pic5" src="https://github.com/user-attachments/assets/55c5eeaa-79a1-42c6-8afb-ac680b795dd2" />


---

### 4. Console Management & Full Physical Interconnect
Established console connections across all network components to perform basic switch security, banner configuration, and SVI management settings.

<img width="1920" height="1017" alt="pic6" src="https://github.com/user-attachments/assets/341e5c37-b71d-418b-8c93-e24be1707510" />


---

## 🧪 Verification & Completion

### End-to-End Connectivity Verification
Verified full network reachability by performing ICMP ping tests from **PC-B** to switch management SVIs (`S1: 192.168.1.1` and `S2: 192.168.1.2`).

<img width="1918" height="1026" alt="pic7" src="https://github.com/user-attachments/assets/068eec07-6b31-43bb-9946-c01397320624" />


### Completion Status
Activity completed successfully with a 100% assessment score across all physical location, cabling, security, and IP configuration parameters.

<img width="1913" height="982" alt="pic8" src="https://github.com/user-attachments/assets/151e0d95-a767-4f47-9350-e6bb97182f6c" />


# 2.9.1 Packet Tracer - Basic Switch and End Device Configuration

## 📌 Lab Overview
This activity serves as a capstone configuration exercise for basic LAN administration. As a LAN technician, initial device management configurations were performed on two Cisco Catalyst switches using Cisco IOS, host IP parameters were assigned to end devices, and end-to-end connectivity was verified across the network.

---

## 🌐 Topology & Addressing Table

<img width="1912" height="1027" alt="pic2" src="https://github.com/user-attachments/assets/1a69ef0b-04ac-4955-ad6f-85fcedce0d48" />


| Device | Interface | IP Address | Subnet Mask |
| :--- | :--- | :--- | :--- |
| **Class-A** | VLAN 1 | 128.107.20.10 | 255.255.255.0 |
| **Class-B** | VLAN 1 | 128.107.20.15 | 255.255.255.0 |
| **Student-1** | NIC | 128.107.20.25 | 255.255.255.0 |
| **Student-2** | NIC | 128.107.20.30 | 255.255.255.0 |

---

## ⚙️ Configuration Workflow & Verification

### 1. Initial Device Connections & Access
Established console connections from the host PCs to access the command-line interfaces of switches **Class-A** and **Class-B**.

<img width="1918" height="1018" alt="pic3" src="https://github.com/user-attachments/assets/2fbebf97-0290-4f5a-a2d3-a4e00ceb8feb" />


---

### 2. Device Naming & Basic IOS Security
Configured device hostnames, secured line access (console and VTY lines) with the execution password `8ubRu`, established privileged EXEC encrypted access using `C9WrE`, encrypted all clear-text passwords in the running configuration, and posted a Message of the Day (MOTD) banner.

```text
Class-A(config)# hostname Class-A
Class-A(config)# line console 0
Class-A(config-line)# password 8ubRu
Class-A(config-line)# login
Class-A(config)# line vty 0 15
Class-A(config-line)# password 8ubRu
Class-A(config-line)# login
Class-A(config)# enable secret C9WrE
Class-A(config)# service password-encryption
Class-A(config)# banner motd #Authorized access only! Any Attempt to get unauthorized access will result in the prosecution to full extent of the law.#
```

<img width="1920" height="1016" alt="pic5" src="https://github.com/user-attachments/assets/8756d4ac-3c8f-48fa-825f-5d0dcd02257e" />

---
<img width="1920" height="1021" alt="pic6" src="https://github.com/user-attachments/assets/10c32c7a-433f-420a-84ed-a43c4c94a9c2" />


---

### 3. SVI & Interface Configuration
Configured management interfaces (`VLAN 1`) with their designated IPv4 addresses and enabled the interfaces using the `no shutdown` command.

<img width="1920" height="1022" alt="pic7" src="https://github.com/user-attachments/assets/5867f2cc-330b-431a-b36b-3b4a82337877" />

---
<img width="1920" height="1021" alt="pic4" src="https://github.com/user-attachments/assets/f2e764bc-6c87-4fc5-a36d-cbd9fa895241" />


---

### 4. Saving Configurations & Host IP Assignment
Saved active running configurations to NVRAM (`startup-config`) across both switches and assigned static IPv4 parameters to **Student-1** and **Student-2**.

<img width="1920" height="1021" alt="pic6" src="https://github.com/user-attachments/assets/c145b42c-e3a3-4d28-84f4-9547e9abb186" />

---
<img width="1917" height="1015" alt="pic8" src="https://github.com/user-attachments/assets/6e50d841-259b-42cb-8e89-8ddab14e2ebf" />


---

## 🧪 Verification & Completion

### Ping Tests & Connectivity
Verified end-to-end connectivity across all hosts and switch management SVIs using ICMP ping requests from **Student-1**.

<img width="1920" height="1021" alt="pic9" src="https://github.com/user-attachments/assets/a03cd9a0-8362-4025-a5fb-50fd8059e47e" />


### Completion Status
Activity completed successfully with a 100% assessment score.

<img width="1568" height="972" alt="pic10" src="https://github.com/user-attachments/assets/9a794256-c596-4bf2-88b9-04016a12153d" />

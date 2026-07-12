# Cisco Packet Tracer: Configure Initial Switch Settings (Lab 2.5.5)

## 📌 Project Overview
This project documents the step-by-step configuration of baseline management and security parameters on Cisco Catalyst 2960 switches (`S1` and `S2`) using Cisco Packet Tracer. The lab covers establishing privileged management access control, protecting device execution environments with encrypted credentials, provisioning line access ports, applying operational warning banners, and ensuring long-term configuration durability across reboots.

---

## 🎯 Lab Objectives
* **Part 1:** Verify the Default Switch Configuration
* **Part 2:** Configure a Basic Switch Configuration
* **Part 3:** Configure a MOTD Banner
* **Part 4:** Save Configuration Files to NVRAM
* **Part 5:** Configure S2

---

## 💻 Technical Walkthrough & Step-by-Step Data

### Part 1: Verifying Default Switch Configurations
The lab initiated on `S1` inside the Cisco IOS unprivileged User EXEC mode interface. Initial hardware diagnostics were executed using privileged inspection parameters to examine default system profiles, interface properties, and factory-default configurations.

* **Image 1 Status:** Initial CLI prompt inspection showing unprivileged modes, entering privileged EXEC context via `enable`, and probing current startup properties.
<img width="1920" height="1020" alt="lab 2 5 5  png1" src="https://github.com/user-attachments/assets/fee66ded-4edc-45af-aed7-ae484ca59278" />


---

### Part 2: Building Out the Baseline System Configuration
To secure management access to `S1`, a series of core configurations were executed sequentially within the Global Configuration mode (`config t`):
1. **Device Hostname:** Assigned unique network identifier using `hostname S1`.
2. **Privileged EXEC Secret:** Configured a secure, MD5-hashed administrative entrance password (`enable secret`).
3. **Console Line Protection:** Secured out-of-band terminal console access with explicit login credentials (`line con 0`).

* **Image 2 Status:** Console session capturing hostname reassignment to `S1`, line access provisioning, password assignments, and terminal exit flows.
<img width="1920" height="1020" alt="lab 2 5 5  png2" src="https://github.com/user-attachments/assets/f87e5593-7606-4ebd-a8f0-910f58e5c1b8" />


---

### Part 3: Cleartext Password Obfuscation & Running Audits
By default, plain text passwords (like those assigned to terminal lines) reside exposed within the configuration profile. To mitigate risks, the global encryption engine was initialized.

* **Image 3 Status:** Executing `service password-encryption` to convert plaintext parameters into obfuscated Type-7 formats, followed by an active verification sweep.
<img width="1920" height="1021" alt="lab 2 5 5  png3" src="https://github.com/user-attachments/assets/54442d85-cb98-4034-93fb-945b491e2212" />


---

### Part 4: Provisioning Message of the Day (MOTD) Security Banners
A legal deterrent banner was declared using `banner motd` to issue clear unauthorized-access warnings during the initialization process of any incoming terminal session.

* **Image 4 Status:** Writing and declaring the explicit delimited text security banner string inside the global terminal environment.
<img width="1920" height="1018" alt="lab 2 5 5  png4" src="https://github.com/user-attachments/assets/08b4b7db-ccc5-4ef3-8beb-bfd0d76f5ccb" />



---

### Part 5: Synchronizing Volatile RAM Settings to Durable NVRAM
To prevent complete data loss upon a hardware power-cycle, the operational memory profile (`running-config`) was committed to the non-volatile system storage space (`startup-config`).

* **Image 5 Status:** Execution of the `copy running-config startup-config` backup syntax command and receiving the terminal validation confirmation log.
<img width="1920" height="1017" alt="lab 2 5 5  png5" src="https://github.com/user-attachments/assets/88d245f8-afc9-4c02-8bc5-e9083cd64144" />


---

### Part 6: Paralleled Security Deploys on Secondary Infrastructure (S2)
The exact same matching logical sequence of system identification, credential encryption parameters, lines protection, security banners, and storage synchronization records was mirror-deployed across the `S2` switch node.

* **Image 6 Status:** Completing configuration sweeps across the `S2` console terminal profile to align it with identical enterprise infrastructure baselines.
<img width="1920" height="1020" alt="lab 2 5 5  png6" src="https://github.com/user-attachments/assets/d07d7cde-2bd8-4581-9655-63e8cc201b3c" />


---

## ✅ Lab Completion Verification
The activity completion tracking engine was evaluated to verify strict compliance against all performance metrics, successfully validating a flawless implementation baseline.

* **Activity Progress Status:** Verified at 100% Total Completion Score.
<img width="1920" height="988" alt="lab 2 5 5  png7" src="https://github.com/user-attachments/assets/a4ba950a-420a-4eab-bcac-32b85923e8de" />


---

## 🛠️ Core Skills Demonstrated
* **System Hostname Control:** Applying deterministic network device identifiers within Cisco IOS.
* **Administrative Access Hardening:** Restricting privilege rings using strong hashed (`secret`) mechanisms and securing management lines.
* **Cleartext Data Mitigation:** Implementing standard global reversing services (`service password-encryption`) to prevent plain-text credential exposures.
* **Banner Message Provisioning:** Structuring compliant boundary notification systems using specific delimiter boundaries.
* **State Persistence Control:** Committing operational active memory metrics down into permanent system NVRAM registers.

---

## 📁 Source Simulation Files
* 📥 **Packet Tracer Lab File:** [Download the Complete `.pka` Simulation File](Configure_Initial_Switch_Settings.pka)

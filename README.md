# 🛡️ Cybersecurity Lab Setup and Network Traffic Analysis

A hands-on cybersecurity project involving virtual machine configuration, network connectivity testing, and Wireshark-based network traffic analysis.

📌 Table of Contents

1. Project Overview
2. Objectives
3. Tools and Technologies
4. Kali Linux Setup and Configuration
5. Android VM Setup and Configuration
6. Wireshark Network Traffic Analysis
7. Key Learnings
8. Security and Ethical Considerations
9. References
10. Author

📖 Project Overview

This project focuses on setting up a virtual cybersecurity lab using Oracle VirtualBox, configuring Kali Linux and Android virtual machines, and performing network connectivity tests.
The lab uses a NAT Network configured with the subnet "10.0.0.0/24". Kali Linux and Android are configured to communicate over this network, with Android assigned the static IP address "10.0.0.9".
The project also includes six practical Wireshark exercises covering IP address identification, TCP stream analysis, HTTP plain-text credentials, brute-force activity, and VoIP traffic.

🎯 Objectives

- Configure a virtual cybersecurity lab using Oracle VirtualBox.
- Install and configure Kali Linux.
- Configure a NAT Network using "10.0.0.0/24".
- Configure the Android VM with a static IP address.
- Test connectivity between Kali Linux and Android.
- Verify internet access using ping commands.
- Capture a virtual machine snapshot.
- Perform six Wireshark network traffic analysis exercises.

---

<h2>Part 1: Kali Linux Setup and Configuration </h2>

<b>Step 1. Install 7-Zip</b>

7-Zip was installed to extract the Kali Linux virtual-machine package, which may be distributed as a .7z archive.<br>
Tool: 7-Zip

<b>Step 2. Install VirtualBox</b>

VirtualBox was installed as the hypervisor.

<b>Step 3. Configure the NAT Network</b>

Created a NAT Network in Oracle VirtualBox using the subnet "10.0.0.0/24".<br>
This network provides the virtual network environment for communication between Kali Linux and Android.

Configuration:

- Network type: NAT Network
- Network address: "10.0.0.0/24"


<img width="1280" height="719" alt="Image" src="https://github.com/user-attachments/assets/69e94640-435a-4b7f-bad1-cd036aa5434f" />


<b>Step 4. Install and Configure Kali Linux</b>

Installed and configured the Kali Linux virtual machine in Oracle VirtualBox.<br>
The VM was configured to connect to the previously created NAT Network.


<img width="1280" height="669" alt="Image" src="https://github.com/user-attachments/assets/2fcc98b7-7aa9-481d-96dd-de273a5894a4" />


<b>Step 5. Configure Kali Linux IP Settings</b>

Configured the IP settings for Kali Linux to operate within the lab network.


<img width="1280" height="678" alt="Image" src="https://github.com/user-attachments/assets/fb736d10-96b2-4562-b082-5034d1a5f95c" />


<b>Step 6. Verify Network Connectivity</b>

Opened the web browser to verify network connectivity.<br>
Successfully searched for the entered query, confirming that the internet connection was working.


<img width="1280" height="686" alt="Image" src="https://github.com/user-attachments/assets/d25eb6f3-82c2-411f-845f-22d24c9d70cc" />


<b>Step 7. Capture a Virtual Machine Snapshot</b>

Captured a snapshot of the configured Kali Linux virtual machine.<br>
A snapshot provides a restoration point that can be used to return the VM to its saved state when needed.


<img width="1280" height="682" alt="Image" src="https://github.com/user-attachments/assets/e7cc23da-b2ab-4eaa-9424-4e7c4f5dc9ae" />




---
<h2>Part 2: Android VM Setup and Configuration</h2>

<b>Step 1: Create Virtual Machine</b>

Created "Android9-Lab" in VirtualBox.<br>
Allocated 2 GB RAM and a 10 GB dynamically allocated virtual disk.

<b>Step 2: Install Android</b>

Attached the Android-x86 ISO.<br>
Installed Android and configured the bootloader.

<img width="1280" height="673" alt="Image" src="https://github.com/user-attachments/assets/cb8a0fc5-f63f-49f3-b568-09224c54502a" />


<b>Step 3: Configure Network</b>

Connected Android to the same NAT Network as Kali Linux.<br>
Used the subnet "10.0.0.0/24".

<b>Step 4: Configure Static IP</b>

Set the Android IP address to "10.0.0.9".


<img width="1280" height="672" alt="Image" src="https://github.com/user-attachments/assets/c711d968-ad64-4ccc-a49a-18ca58732369" />



<b>Step 5: Verify Connectivity</b>

Tested Android-to-Kali connectivity using "ping 10.0.0.2" and Verified internet access using "ping 8.8.8.8".

<img width="1280" height="679" alt="Image" src="https://github.com/user-attachments/assets/c45aa84a-6727-40a5-a2bb-f1d4d42f76c8" />


Tested Kali-to-Android connectivity using "ping 10.0.0.9".

<img width="1280" height="675" alt="Image" src="https://github.com/user-attachments/assets/98223088-a1a5-4922-a825-e687617959d6" />



---

<h2>Part 3: Wireshark Network Traffic Analysis</h2>

Completed six practical Wireshark exercises to explore packet inspection, network protocols, and traffic investigation.

<b>Lab 1: Identify the Attacker's IP</b>

Objective:<br>
Identify the source IP address associated with suspicious activity in the provided packet capture.

<b>Lab 2: Follow TCP Stream</b>

Objective:<br>
Use Wireshark's Follow TCP Stream feature to reconstruct and inspect a TCP conversation.

<b>Lab 3: Follow TCP Stream, Part 2</b>

Objective:<br>
Continue TCP stream analysis using the capture associated with the second exercise.

<b>Lab 4: HTTP Plain-Text Credentials</b>

Objective:<br>
Investigate HTTP traffic to understand how unencrypted communication may expose sensitive information.

<b>Lab 5: Brute Force Catch</b>

Objective:<br>
Investigate captured traffic for patterns consistent with repeated authentication attempts.

<b>Lab 6: VoIP Call Replay</b>

Objective:<br>
Inspect captured VoIP traffic to understand the protocols and packet flow associated with voice communication.



<img width="1280" height="1280" alt="Image" src="https://github.com/user-attachments/assets/05b3310d-92c2-415e-9720-db5437b54cfe" />



<h2>Key Learnings</h2>

Through this project, I gained practical experience in:

- Virtual machine installation and configuration.
- NAT Network configuration and IP addressing.
- Kali Linux network interface configuration.
- Android static IP configuration.
- Bidirectional connectivity testing.
- Internet connectivity verification using ping.
- Virtual machine snapshot management.
- Wireshark packet inspection and TCP stream analysis.
- HTTP traffic security analysis.
- Investigation of suspicious authentication activity.
- VoIP traffic analysis.


---

<h2>Challenges Faced</h2>

<b>1. Kali Linux Internet Connectivity</b>

- Faced internet connectivity issues in the Kali Linux VM.
- Checked the NAT Network configuration and network settings.
- Used the following commands to troubleshoot connectivity:

sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0<br>
sudo nmcli connection down "Wired connection 1"<br>
sudo nmcli connection up "Wired connection 1"<br>

<b>2. Android Network Configuration</b>

- Configured the Android VM to use the same NAT Network as Kali Linux.
- Set the static IP address to "10.0.0.9".
- Tested connectivity between Android and Kali Linux.
- Verified internet connectivity using "ping 8.8.8.8".

<b>3. Kali-to-Android Connectivity</b>

- Configured the Kali Linux network interface using the following command:

  sudo ifconfig eth0 10.0.0.2 netmask 255.255.255.0 up

- Added the default gateway:

  sudo ip route add default via 10.0.0.1 dev eth0

- Tested connectivity to Android using:

  ping 10.0.0.9

---

<h2>Security and Ethical Considerations</h2>

This project is intended for educational purposes and authorised lab environments.

- Analyse only traffic you are authorised to inspect.
- Redact credentials and sensitive information from screenshots.
- Support technical conclusions with packet evidence.
- Document connectivity test results accurately.

---

<h2>References</h2>

- "Oracle VirtualBox" (https://www.virtualbox.org/)
- "Kali Linux" (https://www.kali.org/)
- "Android-x86" (https://www.android-x86.org/)
- "Wireshark" (https://www.wireshark.org/](https://networkwalks.com/wireshark/)

---

<h2>Author</h2>

Nida Khedekar

B.Sc. Information Technology | CCNA | Network Engineer

Interested in Network Engineering, Network Security, and Cybersecurity.

"Connect on LinkedIn" (https://www.linkedin.com/in/nida-khedekar-614252349/)

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

🧰 Tools and Technologies

Tool| Purpose
Oracle VirtualBox| Virtual machine management
Kali Linux| Linux environment and network testing
Android-x86 9| Android virtual machine
Wireshark| Network packet analysis
NAT Network| Virtual machine networking
Ping| Connectivity verification

---

<h2>Part 1: Kali Linux Setup and Configuration </h2>

<b>Step 1. Install 7-Zip</b>

7-Zip was installed to extract the Kali Linux virtual-machine package, which may be distributed as a .7z archive.<br>
Tool: 7-Zip

<b>Step 2. Install VirtualBox</b>

VirtualBox was installed as the hypervisor.

<b>Step 3. Configure the NAT Network</b>

Created a NAT Network in Oracle VirtualBox using the subnet "10.0.0.0/24".
This network provides the virtual network environment for communication between Kali Linux and Android.

Configuration:

- Network type: NAT Network
- Network address: "10.0.0.0/24"


<img width="1280" height="719" alt="Image" src="https://github.com/user-attachments/assets/69e94640-435a-4b7f-bad1-cd036aa5434f" />


<b>Step 4. Install and Configure Kali Linux</b>

Installed and configured the Kali Linux virtual machine in Oracle VirtualBox.
The VM was configured to connect to the previously created NAT Network.


<img width="1280" height="669" alt="Image" src="https://github.com/user-attachments/assets/2fcc98b7-7aa9-481d-96dd-de273a5894a4" />


<b>Step 5. Configure Kali Linux IP Settings</b>

Configured the IP settings for Kali Linux to operate within the lab network.


<img width="1280" height="678" alt="Image" src="https://github.com/user-attachments/assets/fb736d10-96b2-4562-b082-5034d1a5f95c" />


<b>Step 6. Verify Network Connectivity</b>

Opened the web browser to verify network connectivity.
Successfully searched for the entered query, confirming that the internet connection was working.


<img width="1280" height="686" alt="Image" src="https://github.com/user-attachments/assets/d25eb6f3-82c2-411f-845f-22d24c9d70cc" />


<b>Step 7. Capture a Virtual Machine Snapshot</b>

Captured a snapshot of the configured Kali Linux virtual machine.
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

<b>Step 5: Verify Connectivity</b>

Tested Android-to-Kali connectivity using "ping 10.0.0.2".


Verified internet access using "ping 8.8.8.8".


Tested Kali-to-Android connectivity using "ping 10.0.0.9", with partial packet loss.



---
Test| Configuration or Command| Result

Shared NAT Network| Same NAT Network as Kali Linux| Configured

Static IP address| "10.0.0.9"| Configured

Android-to-Kali| "ping 10.0.0.2"| Successful

Android internet connectivity| "ping 8.8.8.8"| Successful

Kali-to-Android| "ping 10.0.0.9"| Partial packet loss

---

🔍 Part 3: Wireshark Network Traffic Analysis

Completed six practical Wireshark exercises to explore packet inspection, network protocols, and traffic investigation.

Lab 1: Identify the Attacker's IP

Objective

Identify the source IP address associated with suspicious activity in the provided packet capture.

Procedure

1. Open the relevant capture file in Wireshark.
2. Inspect the source and destination IP addresses.
3. Investigate the traffic associated with the activity.
4. Identify the IP address supported by the packet evidence.

📸 Screenshot 11: Attacker IP identification

<!-- INSERT WIRESHARK LAB 1 SCREENSHOT HERE -->Lab 2: Follow TCP Stream

Objective

Use Wireshark's Follow TCP Stream feature to reconstruct and inspect a TCP conversation.

Procedure

1. Open the relevant packet capture.
2. Identify a TCP packet belonging to the communication.
3. Right-click the packet.
4. Select Follow → TCP Stream.
5. Inspect the reconstructed conversation.

📸 Screenshot 12: Follow TCP Stream

<!-- INSERT WIRESHARK LAB 2 SCREENSHOT HERE -->Lab 3: Follow TCP Stream, Part 2

Objective

Continue TCP stream analysis using the capture associated with the second exercise.

Procedure

1. Open the relevant capture.
2. Identify the TCP communication.
3. Select Follow → TCP Stream.
4. Examine the reconstructed conversation.
5. Record the relevant observations.

📸 Screenshot 13: Follow TCP Stream, Part 2

<!-- INSERT WIRESHARK LAB 3 SCREENSHOT HERE -->Lab 4: HTTP Plain-Text Credentials

Objective

Investigate HTTP traffic to understand how unencrypted communication may expose sensitive information.

Procedure

1. Open the relevant packet capture.
2. Identify HTTP requests and responses.
3. Inspect packet details.
4. Follow the associated TCP stream if appropriate.
5. Document the security implications.

📸 Screenshot 14: HTTP plain-text traffic analysis

<!-- INSERT WIRESHARK LAB 4 SCREENSHOT HERE -->Security note: Redact credentials and other sensitive information before publishing screenshots.

Lab 5: Brute Force Catch

Objective

Investigate captured traffic for patterns consistent with repeated authentication attempts.

Procedure

1. Open the relevant packet capture.
2. Identify traffic associated with the authentication service.
3. Examine repeated connection attempts or authentication requests.
4. Inspect relevant packet details.
5. Document the evidence.

📸 Screenshot 15: Brute-force traffic investigation

<!-- INSERT WIRESHARK LAB 5 SCREENSHOT HERE -->Lab 6: VoIP Call Replay

Objective

Inspect captured VoIP traffic to understand the protocols and packet flow associated with voice communication.

Procedure

1. Open the relevant packet capture.
2. Identify the VoIP-related packets.
3. Inspect packet details and communication flow.
4. Examine available call-analysis or stream features.
5. Document the observations.

📸 Screenshot 16: VoIP traffic analysis

<!-- INSERT WIRESHARK LAB 6 SCREENSHOT HERE -->---

📚 Key Learnings

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

🔐 Security and Ethical Considerations

This project is intended for educational purposes and authorised lab environments.

- Analyse only traffic you are authorised to inspect.
- Redact credentials and sensitive information from screenshots.
- Support technical conclusions with packet evidence.
- Document connectivity test results accurately.

---

🔗 References

- "Oracle VirtualBox" (https://www.virtualbox.org/)
- "Kali Linux" (https://www.kali.org/)
- "Android-x86" (https://www.android-x86.org/)
- "Wireshark" (https://www.wireshark.org/)

---

👩‍💻 Author

Nida Khedekar

B.Sc. Information Technology | CCNA Qualified

Interested in Network Engineering, Network Security, and Cybersecurity.

"Connect on LinkedIn" (https://www.linkedin.com/in/nida-khedekar-614252349/)

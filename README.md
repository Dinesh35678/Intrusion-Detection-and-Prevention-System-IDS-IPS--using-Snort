# IDS/IPS using Snort

Theoretical Demonstration

Intrusion Detection System (IDS)
Monitors network traffic and systems for suspicious activity and known threats. Generates alerts when such activities are detected.

Types of IDS
1.	Network-based IDS (NIDS): Monitors network traffic.
2.	Host-based IDS (HIDS): Monitors a single host or device.

Detection Methods
1.	Signature-based: Uses a database of known threat signatures.
2.	Anomaly-based: Identifies deviations from normal behaviour patterns.

Intrusion Prevention System (IPS)
Monitors network traffic and systems for suspicious activity and known threats. Actively takes action to block or prevent detected threats.

Types of IPS
1.	Network-based IPS (NIPS): Monitors and takes action on network traffic.
2.	Host-based IPS (HIPS): Monitors and takes action on a single host or device.

Detection Methods
1.	Signature-based: Uses a database of known threat signatures.
2.	Anomaly-based: Identifies deviations from normal behaviour patterns.

Difference between Host based IDS / IPS and Network based IDS / IPS 
![ids vs ips](https://github.com/user-attachments/assets/251798f5-1481-4e97-94ca-b711dc320a76)

What is Snort
Snort is an open-source IDS/IPS (Intrusion Detection System / Intrusion Prevention System) that monitors network traffic based on user-defined rules. It is widely used to detect and prevent a variety of network threats.

Features of Snort
1.	Packet Sniffing: In this mode, Snort captures and displays network packets in real-time.
2.	Packet Logging: This mode logs network packets to disk for later analysis.
3.	Network Intrusion Detection System (NIDS): In NIDS mode, Snort analyses network traffic against a set of predefined rules to detect suspicious activity.

Snort Rule Structure
![rules syntax](https://github.com/user-attachments/assets/b6ed54b4-4191-4539-82bf-49048f2d3358)

Types of Snort Rules
1.	Community Rules: Free, user-contributed rules available to anyone in the Snort community.
2.	Registered Rules: Official Snort rules available for free to registered users, updated on a delayed basis.
3.	Subscription Rules: Premium, up-to-date rules available to paying subscribers, offering the latest threat detection capabilities.

Snorpy tool
Snorpy is a web-based GUI that simplifies Snort rule creation and management, providing an intuitive interface for customizing rules, reducing syntax errors, and efficiently generating and exporting Snort-compatible rules.

Link - Snorpy 2.0 - Web Based Snort Rule Creator (cyb3rs3c.net)

Practical Demonstration

Pre-requisites Setup
1.	Snort tool.
2.	Ubuntu Machine.
3.	Kali Linux Machine.
4.	Metasploit Machine.
5.	Windows Machine.

Snort Installation
1. Install snort tool on the Ubuntu machine.
![snort_1](https://github.com/user-attachments/assets/f0499080-d71a-490c-a40b-e136a355fc87)

2. Verify the successful installation of snort by check the snort version. 
![snort_3](https://github.com/user-attachments/assets/f4b7811f-2490-449f-9bd8-74d952b6b112)

Snort Configuration
1. Specify the subnets IP address of the connected network in scope.
![snort_2](https://github.com/user-attachments/assets/5a994336-27fc-48fd-84f0-6161a3cce08d)

2. Open the snort configuration file.
![snort_4](https://github.com/user-attachments/assets/055083f7-ae0f-4e47-b54e-be8a24c10882)

3. Set the subnets IP address of the connected network in Network variables.
![snort_5](https://github.com/user-attachments/assets/2e54fdca-88e7-4b04-80dc-136915a28f9a)

4. Disable the Pre-defined Rules set using # symbol.
![snort_7](https://github.com/user-attachments/assets/1d6391ac-8728-4e7a-8994-eaf5335fe064)

5. Run the snort.conf file and check whether the snort tool working properly.
![snort_8](https://github.com/user-attachments/assets/9eb55c1f-7c40-4b48-97b7-7951fc9a08d5)

Implementation of Snort Custom Detection Rule
Open the “local.Rules” file to create a new custom detection rule. 
![rule file ope](https://github.com/user-attachments/assets/911810f0-bd3e-4168-8b19-8dd423a9a1f9)

Ping Alert Detection Rule
1. Create a ping detection rule. 
![ping alert](https://github.com/user-attachments/assets/c9202488-d15c-40d8-a963-18c808642923)

2. Check the IP address of the Metasploit machine [Victim].
![metasploit ip](https://github.com/user-attachments/assets/e48bf011-4d81-4bce-8634-9d0d7420a463)

3. Now try to ping the victim machine from kali Linux machine [Attacker Machine].
![ping attack](https://github.com/user-attachments/assets/e6f7a209-1898-407e-b61e-8e404ecc15bd)

4. We had successfully identified a ping detection on the local network.
![ping detect](https://github.com/user-attachments/assets/acb95bb6-6a50-42df-9ff3-439c424832fe)

SSH Authentication Detection Rule
1. Create a SSH authentication detection rule.
![ssh rule](https://github.com/user-attachments/assets/ccbb155c-4879-44b6-895c-6dd7365ad7d6)

2. Check the IP address of the Metasploit machine [Victim].
![metasploit ip](https://github.com/user-attachments/assets/81876619-110f-4854-97f2-66525a08f15b)

3. Now, connect the SSH service of the victim machine.
![ssh login](https://github.com/user-attachments/assets/818b01d8-786b-4be9-b884-5e13f61a0f9d)

4. We had successfully identified a SSH Authentication on the local network.
![ssh detect](https://github.com/user-attachments/assets/b0e63829-43a5-4f3c-9181-20d4b977d955)

FTP Authentication Detection Rule
1. Create a FTP authentication detection rule.
![FTP Rule](https://github.com/user-attachments/assets/03030d3f-b08b-4d39-b4e5-275f86236392)

2. Check the IP address of the Metasploit machine [Victim].
![metasploit ip](https://github.com/user-attachments/assets/1e1b6e8b-b05d-47d1-849d-2539087b672a)

3. Now, connect the FTP service of the victim machine.
![FTP attempt](https://github.com/user-attachments/assets/33a94fab-81ad-44d9-a65c-69c906125391)

4. We had successfully identified a SSH Authentication on the local network.
![FTP alert](https://github.com/user-attachments/assets/b9175f76-6a4f-4c55-9fa8-32e0e7bf07fd)

Eternal Blue Attack Detection Rule
1. Download the community rules for detection of latest attacks.
![community rules](https://github.com/user-attachments/assets/8bb8eafb-63d6-4970-85da-c0482a591d6c)
 
2. Create an Eternal Blue attack detection rule.
![eternal blue rule](https://github.com/user-attachments/assets/f34f224f-e889-4f08-a9b5-cbc22ecde3c6)

3. Check the IP address of the windows machine [Victim].
![windows ip](https://github.com/user-attachments/assets/21592e1c-9fcd-4396-a45a-e3ec2a448a3f)

4. Start the Msf console on the kali Linux Machine [Attacker].
5. Then, Check for eternal blue payloads.
![meta_1](https://github.com/user-attachments/assets/7c361a4f-0c28-4204-a5b9-65f5caaa6d52)

7. Use the eternal blue payload.
8. Set the victim Ip address.
9. Finally, exploit the target machine and got meterpreter shell.
![eternal blue attack](https://github.com/user-attachments/assets/48ec3c28-152e-4e4d-aedc-4d7267378f18)

11. Successfully detected eternal blue on the local network.
![smb remote code alert](https://github.com/user-attachments/assets/01096abf-28d8-442e-b0f0-54743102a896)

Conclusion

Implementing Snort as an IDS/IPS solution provides robust network security through its customizable, open-source, rule-based system. Combined with Snorpy, It becomes easier for users to manage rules, enhancing threat detection and response capabilities.

Disclaimer

Snort's creators are not responsible for any illegal or unethical use. It is intended solely for legitimate security purposes and must be used in compliance with all applicable laws and regulations.

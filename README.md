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


What is Snort
Snort is an open-source IDS/IPS (Intrusion Detection System / Intrusion Prevention System) that monitors network traffic based on user-defined rules. It is widely used to detect and prevent a variety of network threats.

Features of Snort
1.	Packet Sniffing: In this mode, Snort captures and displays network packets in real-time.
2.	Packet Logging: This mode logs network packets to disk for later analysis.
3.	Network Intrusion Detection System (NIDS): In NIDS mode, Snort analyses network traffic against a set of predefined rules to detect suspicious activity.

Snort Rule Structure
 
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
 
2. Verify the successful installation of snort by check the snort version. 


Snort Configuration
1. Specify the subnets IP address of the connected network in scope.
 
2. Open the snort configuration file.
 

3. Set the subnets IP address of the connected network in Network variables.
 
4. Disable the Pre-defined Rules set using # symbol.
 
5. Run the snort.conf file and check whether the snort tool working properly.
 
Implementation of Snort Custom Detection Rule
Open the “local.Rules” file to create a new custom detection rule. 
 
Ping Alert Detection Rule
1. Create a ping detection rule. 



2. Check the IP address of the Metasploit machine [Victim].
 
3. Now try to ping the victim machine from kali Linux machine [Attacker Machine].
 








4. We had successfully identified a ping detection on the local network.
 
SSH Authentication Detection Rule
1. Create a SSH authentication detection rule.
 




2. Check the IP address of the Metasploit machine [Victim].
 
3. Now, connect the SSH service of the victim machine.
 







4. We had successfully identified a SSH Authentication on the local network.
 
FTP Authentication Detection Rule
1. Create a FTP authentication detection rule.
 









2. Check the IP address of the Metasploit machine [Victim].
 
3. Now, connect the FTP service of the victim machine.
 
4. We had successfully identified a SSH Authentication on the local network.
 

Eternal Blue Attack Detection Rule
1. Download the community rules for detection of latest attacks.
 
2. Create an Eternal Blue attack detection rule.
 





3. Check the IP address of the windows machine [Victim].
 
4. Start the Msf console on the kali Linux Machine [Attacker].
5. Then, Check for eternal blue payloads.
 






6. Use the eternal blue payload.
7. Set the victim Ip address.
8. Finally, exploit the target machine and got meterpreter shell.
 
9. Successfully detected eternal blue on the local network.
 
Conclusion

Implementing Snort as an IDS/IPS solution provides robust network security through its customizable, open-source, rule-based system. Combined with Snorpy, It becomes easier for users to manage rules, enhancing threat detection and response capabilities.

Disclaimer

Snort's creators are not responsible for any illegal or unethical use. It is intended solely for legitimate security purposes and must be used in compliance with all applicable laws and regulations.

# Date :
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
(Insert screenshot of your Packet Tracer setup here)<br>

<img width="541" height="455" alt="Screenshot 2026-10-24 113315" src="https://github.com/user-attachments/assets/cf224008-b66a-48a4-954a-05be0e341668" />

________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)
•	Router CLI configuration<br>
•	IP configurations on PCs<br>
•	Successful ping between PC0 and PC1<br>

<img width="1916" height="1075" alt="Screenshot 2026-10-25 181519" src="https://github.com/user-attachments/assets/865a0668-facd-4127-8b78-44dfd64f1dd9" />

<img width="1908" height="1078" alt="Screenshot 2026-10-25 181532" src="https://github.com/user-attachments/assets/3b8bc1a0-81d6-47ed-bdec-b5e71ed9e44e" />

<img width="1917" height="1078" alt="Screenshot 2026-10-25 181544" src="https://github.com/user-attachments/assets/6a8662f9-96e1-4c0b-a163-6294b2ce4db6" />

<img width="1907" height="1067" alt="Screenshot 2026-10-27 154613" src="https://github.com/user-attachments/assets/d168302f-21f9-4a0f-b866-ceed704401ad" />

<img width="1890" height="1075" alt="Screenshot 2026-10-27 154815" src="https://github.com/user-attachments/assets/e3aa7964-25da-4785-94e5-09cf7cab7e39" />

____________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.


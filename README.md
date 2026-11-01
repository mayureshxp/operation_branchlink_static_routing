Operation BranchLink — Branch Office Network Connectivity Using Static Routing

1. Project Overview

Operation BranchLink is a Cisco Packet Tracer-based network simulation that establishes communication between a Head Office (HQ) and a Branch Office using static routing.

The project demonstrates how two separate IPv4 networks can communicate through two routers connected using a point-to-point link.

Project Title: Branch Office Network Connectivity Using Static Routing
Tool Used: Cisco Packet Tracer
Domain: Computer Networking
Status: Core configuration and connectivity testing completed

2. Project Objectives

- Design a network connecting a Head Office and a Branch Office.
- Configure router interfaces with IPv4 addresses.
- Assign static IP addresses and default gateways to end devices.
- Implement static routes on both routers.
- Establish communication between two different IP networks.
- Verify end-to-end connectivity using ICMP ping.

3. Network Topology

The simulated network consists of the following devices:

Component| Device
HQ Router| R1_HQ
HQ Switch| SW1_HQ
HQ PCs| PC_HR, PC_IT
Branch Router| R2_BRANCH
Branch Switch| SW2_HQ
Branch PCs| PC_FINANCE, PC_SALES

R1_HQ and R2_BRANCH are connected through a point-to-point router link.

4. IP Addressing Plan

Device| Interface| IP Address| Default Gateway
R1_HQ| LAN interface| 192.168.10.1/24| —
R1_HQ| Router link| 10.0.0.1/30| —
R2_BRANCH| Router link| 10.0.0.2/30| —
R2_BRANCH| LAN interface| 192.168.20.1/24| —
PC_HR| Network adapter| 192.168.10.10/24| 192.168.10.1
PC_IT| Network adapter| 192.168.10.11/24| 192.168.10.1
PC_FINANCE| Network adapter| 192.168.20.10/24| 192.168.20.1
PC_SALES| Network adapter| 192.168.20.11/24| 192.168.20.1

5. Configuration and Implementation

The following configuration steps were performed:

1. Configured router interfaces with IPv4 addresses.
2. Enabled the router interfaces.
3. Assigned static IP addresses and subnet masks to all four PCs.
4. Configured the default gateway on each PC.
5. Configured static routes on both routers.
6. Verified the router-to-router connection.
7. Inspected routing tables.
8. Tested end-to-end connectivity using the ping command.

Static Routing Configuration

On R1_HQ:

ip route 192.168.20.0 255.255.255.0 10.0.0.2

On R2_BRANCH:

ip route 192.168.10.0 255.255.255.0 10.0.0.1

These routes allow the HQ router and Branch router to forward packets to their respective remote LAN networks.

6. Testing and Results

The following connectivity tests were reported as successful:

- Router-to-router connectivity.
- PC_HR to PC_FINANCE.
- PC_FINANCE to PC_HR.
- PC_IT to PC_SALES.

The reported final PC-to-PC connectivity tests achieved 0% packet loss.

Result: Successful end-to-end communication was verified between the HQ and Branch networks using static routing.

7. Skills Practised

- IPv4 addressing and subnet masks
- Default gateway configuration
- Router interface configuration
- Static routing
- Routing table verification
- Network connectivity testing using ICMP ping
- Basic network troubleshooting
- Cisco Packet Tracer network simulation

8. Repository Structure

operation-branchlink-static-routing/
│
├── README.md
│
├── Project_Report.pdf
│
└── packet-tracer/
    │
    ├── Operation_BranchLink.pkt
    │
    └── screenshots/
        └── Project screenshots

9. Future Improvements

- Include a clearly labelled network topology diagram.
- Document routing tables and connectivity tests.
- Explore VLAN segmentation and access-control configurations in a future version.

10. Tools Used

- Cisco Packet Tracer
- Cisco IOS CLI
- ICMP Ping

11. Project Scope

This project is a simulated networking implementation developed in Cisco Packet Tracer. It demonstrates fundamental enterprise networking and static routing concepts in a controlled lab environment.

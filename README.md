# Project 02: Enterprise Network Lab

A hands-on network engineering lab built to demonstrate enterprise LAN/WAN design, FortiGate firewall integration, dynamic routing, high availability, access control, DHCP services, and end-to-end connectivity validation.

This repository documents the design and verification evidence for a multi-layer network environment using FortiGate, core switches, access switches, and a Linux server. The lab focuses on practical operations that are commonly used in real infrastructure: VLAN segmentation, inter-VLAN routing, NAT, OSPF, HSRP, EtherChannel, trunking, ACL enforcement, DHCP, and traffic verification.

## Repository

- GitHub: [chanathip-awc/network-lab](https://github.com/chanathip-awc/network-lab)
- Project type: Network infrastructure lab
- Focus areas: Enterprise switching, routing, firewall policy, NAT, segmentation, and validation

## Lab Objectives

- Design a segmented enterprise network topology.
- Configure VLANs and Layer 3 interfaces across core and access switching layers.
- Implement redundant gateway services with HSRP.
- Configure trunk links and EtherChannel for scalable switch connectivity.
- Integrate FortiGate firewall policies, NAT, routing, and OSPF adjacency.
- Provide DHCP services from a Client.
- Validate internet access and access-control behavior from client segments.

## High-Level Topology

![Network Topology](01-diagram/01-network-topology-v2.png)

![GNS3 Topology](01-diagram/02-gns3-topology.png)

The lab is organized around a layered network model. Access switches provide VLAN connectivity for endpoint networks, core switches handle Layer 3 switching, gateway redundancy, routing, and policy enforcement, and FortiGate provides firewall and NAT services toward the external network.

## Technology Scope

| Area | Implementation |
| --- | --- |
| Firewall | FortiGate interfaces, NAT policy, routing table, OSPF neighbor validation |
| Switching | VLANs, trunks, EtherChannel, spanning tree, HSRP, ACLs |
| Routing | OSPF between FortiGate and internal routing devices |
| Services | DHCP server for client addressing |
| Verification | Internet reachability and Debian access-control validation |

## FortiGate Configuration Evidence

### Interface Configuration

![FortiGate Interface](02-fortigate/01-interface.png)

### Firewall Policy and NAT

![FortiGate Firewall Policy NAT](02-fortigate/02-firewall-policy-nat.png)

### Routing Table

![FortiGate Routing Table](02-fortigate/03-routing-table.png)

### OSPF Neighbor

![FortiGate OSPF Neighbor](02-fortigate/04-ospf-neighbor.png)

## Core Switch Configuration Evidence

### VLAN Configuration

![Core Switch VLAN](03-core-switch/01-vlan.png)

### Layer 3 Interface Summary

![Core Switch IP Interface Brief](03-core-switch/02-ip-interface-brief.png)

### HSRP Gateway Redundancy

![Core Switch HSRP](03-core-switch/03-hsrp.png)

### Trunk Configuration

![Core Switch Trunk](03-core-switch/04-trunk.png)

### EtherChannel Configuration

![Core Switch EtherChannel](03-core-switch/05-etherchannel.png)

### Spanning Tree Verification

![Core Switch Spanning Tree](03-core-switch/06-spanning-tree.png)

### Access Control List

![Core Switch ACL](03-core-switch/07-acl.png)

### OSPF Configuration

![Core Switch OSPF](03-core-switch/08-ospf.png)

## Access Switch Configuration Evidence

### VLAN Configuration

![Access Switch VLAN](04-access-switch/01-vlan.png)

### Trunk Configuration

![Access Switch Trunk](04-access-switch/02-trunk.png)

## Server Configuration Evidence

### DHCP Server

![DHCP Server](05-server/01-dhcp-server.png)

The DHCP service provides IP addressing for client VLANs and supports the lab's end-to-end connectivity tests.

## Verification Results

### VLAN Internet Access

![VLAN Internet Access](06-verification/01-vlan-internet.png)

### Debian Access Control Validation

![Debian Access Control](06-verification/02-debian-access-control.png)

These verification screenshots confirm that the configured network can route traffic correctly while enforcing access-control requirements between selected hosts and network segments.

## Key Skills Demonstrated

- Enterprise network topology planning
- VLAN segmentation and Layer 3 switching
- FortiGate firewall interface, policy, NAT, and routing configuration
- OSPF routing and neighbor verification
- HSRP gateway redundancy
- Trunking and EtherChannel design
- Spanning Tree Protocol verification
- ACL-based traffic control
- DHCP server integration
- Practical network troubleshooting and validation

## Project Structure

```text
.
├── 01-diagram/
│   ├── 01-network-topology.png
│   └── 02-gns3-topology.png
├── 02-fortigate/
│   ├── 01-interface.png
│   ├── 02-firewall-policy-nat.png
│   ├── 03-routing-table.png
│   └── 04-ospf-neighbor.png
├── 03-core-switch/
│   ├── 01-vlan.png
│   ├── 02-ip-interface-brief.png
│   ├── 03-hsrp.png
│   ├── 04-trunk.png
│   ├── 05-etherchannel.png
│   ├── 06-spanning-tree.png
│   ├── 07-acl.png
│   └── 08-ospf.png
├── 04-access-switch/
│   ├── 01-vlan.png
│   └── 02-trunk.png
├── 05-server/
│   └── 01-dhcp-server.png
├── 06-verification/
│   ├── 01-vlan-internet.png
│   └── 02-debian-access-control.png
└── README.md
```

## Notes

This project is documented as a portfolio lab. The screenshots are included as implementation evidence and should be reviewed together with the topology diagrams to understand the full network flow.

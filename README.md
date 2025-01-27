# Inter-Branch Connectivity Project

## Overview
This project demonstrates the configuration and troubleshooting of inter-branch connectivity using routers, Layer 3 switches, and access switches. The design connects two branch offices and implements features like VLAN segmentation, OSPF routing, and trunk links.

## Topology
### Branch Office 1
- **Devices**: R1, R3 (Internet), Layer3_SW1, Layer3_SW2, SW1, SW2

### Branch Office 2
- **Devices**: R2, Layer3_SW3, Layer3_SW4, SW3, SW4

### Connection Between Branches
- OSPF routing via the Internet (R1 ↔ R3 ↔ R2).

## Technologies Used
- **Routing Protocol**: OSPF (Open Shortest Path First)
- **VLANs**: 
  - Finance (VLAN 10)
  - IT (VLAN 20)
  - Management (VLAN 30)
  - Wi-Fi (VLAN 40)
- **Switching**: 
  - Trunk links with 802.1Q encapsulation
  - Native VLAN configuration
- **IP Addressing**: 
  - Subnetting applied to efficiently allocate addresses across interfaces.

## Configuration Files
The repository contains configuration files for all devices:

- `R1.txt`: Configuration for Router 1.
- `R2.txt`: Configuration for Router 2.
- `R3.txt`: Configuration for the Internet router.
- `Layer3_SW1.txt`: Configuration for Layer 3 Switch 1.
- `Layer3_SW2.txt`: Configuration for Layer 3 Switch 2.
- `SW1.txt`: Configuration for Switch 1.
- `SW2.txt`: Configuration for Switch 2.
- `Layer3_SW3.txt`: Configuration for Layer 3 Switch 3.
- `Layer3_SW4.txt`: Configuration for Layer 3 Switch 4.
- `SW3.txt`: Configuration for Switch 3.
- `SW4.txt`: Configuration for Switch 4.

## Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/Caynaanshe/Inter-Branch.git
   ```
2. Review configurations and apply them to the respective devices in your simulation software (e.g., Cisco Packet Tracer, GNS3).
3. Verify connectivity between branches using `ping` or `traceroute`.

## Troubleshooting
- **Native VLAN mismatch**: Ensure all trunk links have consistent Native VLAN configurations.
- **VLAN interfaces down**: Verify active ports in each VLAN and check physical connectivity.
- **OSPF adjacency issues**: Confirm OSPF configurations and interface IP addresses.

## Credits
Designed and configured by **Mohamed Abdirahman Ali**.  
*CCNA & AWS SAA Certified*.

# pfSense-Firewall-Homelab
# introduction
The project is about the design and implementation of a virtual firewall environment using pfSense and Kali Linux in Oracle Virtualbox. This project is about getting hands-on experience with firewall administration, network configuration, access control and security testing.The main firewall device was pfSense, which managed communication between the external network (WAN) and the internal network (LAN). We used the Kali Linux test machine to verify connectivity, test firewall configuration, and perform security validation.

## 2. Project Objectives

The main objectives of this project were:

- To install and configure a pfSense firewall in a virtual environment.
- To configure WAN and LAN network interfaces.
- To create a secure internal LAN network.
- To enable and configure SSH remote administration.
- To create firewall rules for controlling network traffic.
- To test network communication between Kali Linux and pfSense.
- To perform basic security testing using Nmap.

## 3. Lab Environment

The project was developed using the following technologies:

- Oracle VirtualBox – Virtualization platform used to host virtual machines.
- pfSense Community Edition – Firewall and routing platform.
- Kali Linux – Security testing and administration machine.

#The virtual network consisted of two main components:
1. pfSense Firewall
2. Kali Linux Client Machine

---

## 4. Network Configuration
The pfSense firewall was configured with two network interfaces:

### WAN Interface

The WAN interface was connected to the VirtualBox NAT network to provide external connectivity.
Configuration:
- Connection Type: NAT
- IP Assignment: DHCP

  ### LAN Interface

The LAN interface was configured as an internal network for communication with Kali Linux.

Configuration:

- Network: 192.168.1.0/24
- pfSense LAN IP: 192.168.1.1
- DHCP: Enabled

### Kali Linux Configuration
Kali Linux was connected to the same internal network.
Configuration:
- IP Address: 192.168.1.100
- Subnet Mask: 255.255.255.0
- Gateway: 192.168.1.1
## 5. Firewall Configuration

After installing pfSense, firewall settings were configured to control traffic between the LAN network and the firewall.

The following configuration was completed:

- Configured LAN and WAN interfaces.
- Enabled DHCP services for LAN clients.
- Enabled SSH access for secure administration.
- Created firewall rules to allow required traffic.
- Verified that traffic was correctly controlled by pfSense.

---

## 6. SSH Configuration

Secure Shell (SSH) was enabled on pfSense to allow remote administration from Kali Linux.

The SSH configuration included:

- SSH Service: Enabled
- SSH Port: 22
- Source Network: LAN Network
- Destination: pfSense Firewall

A firewall rule was created:

- Action: Pass
- Interface: LAN
- Protocol: TCP
- Source: LAN net
- Destination: This Firewall
- Port: SSH (22)

## 7. Testing and Validation

The configuration was tested from Kali Linux using:

- "ip a" to verify the Kali IP address.
- "ping 192.168.1.1" to confirm communication with pfSense.
- "nmap -p 22 192.168.1.1" to verify SSH availability.
- "ssh admin@192.168.1.1" to confirm remote access.

All tests successfully verified connectivity and SSH functionality.


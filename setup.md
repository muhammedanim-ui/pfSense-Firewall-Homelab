# Lab Setup

## Environment

- Hypervisor: Oracle VirtualBox
- Firewall: pfSense Community Edition
- Client Machine: Kali Linux

## Network Configuration

### pfSense

Adapter 1 (WAN)
- Mode: NAT

Adapter 2 (LAN)
- Mode: Internal Network
- LAN IP: 192.168.1.1/24

### Kali Linux

Adapter 1
- Mode: Internal Network
- IP Address: 192.168.1.100/24
- Gateway: 192.168.1.1

## Installation Summary

1. Installed pfSense.
2. Assigned WAN and LAN interfaces.
3. Configured LAN IP address.
4. Enabled DHCP server.
5. Connected Kali Linux to the LAN.
6. Verified connectivity using `ping`.
7. Enabled SSH on pfSense.
8. Created firewall rule to allow SSH.

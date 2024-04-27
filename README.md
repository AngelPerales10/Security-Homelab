# Cybersecurity Homelab

![CyberNetworkTopology](https://github.com/AngelPerales10/Security-Homelab/assets/108242721/6b01b7e2-71c7-4fba-a8e4-568a6057ddc9)

## Summary
I developed this dynamic cybersecurity homelab to explore and understand various technologies, simulate attacker behaviors, and gain insight into defensive strategies from the blue team perspective.

This cybersecurity homelab provides a hands-on environment for exploring and understanding cybersecurity concepts, ranging from network configurations to log analysis and threat detection. As I continue to utilize and explore this lab, I aim to delve deeper into various attack scenarios and defensive strategies.

## Overview

### Components:
- The internet
- Home router
- My main machine with VMWare
- VMWare Virtual Machines:
  - pfSense
  - Security Onion
  - Kali Linux
  - Splunk
  - Domain Controller running Windows Server 2019:
    - Active Directory, DNS, and DHCP configured
    - Universal Forwarder configured to send events to Splunk VM
    - Linux and Windows machines active within the domain for testing events

### Connectivity:
- **pfSense**:
  - Acts as the main router and firewall
  - Utilizes NAT connection through VMWare
  - Connects segments through various VMNETs
    - VMNET 2
    - VMNET 3
    - VMNET 4
    - VMNET 5
    - VMNET 6
  - IP Address: `192.168.1.1`

- **Kali Linux**:
  - Connected to LAN on VMNET 2
  - IP Address: `192.168.1.10`

- **Domain Controller**:
  - Connected to VMNET 3
  - IP Address: `192.168.2.10`
  - Acts as the victim network

- **Security Onion**:
  - Connected to VMNET 4
  - IP Address: `192.168.3.10`

- **Span Port**:
  - Connected to VMNET 5
  - Mirrors traffic sent out on victim network to Security Onion

## Purpose

As this setup is relatively new, I've been currently primarily focused on:

- Learning Splunk
- Forwarding events from the Domain Controller using Universal Forwarder
- Understanding event visualization and querying in Splunk
- Analyzing different event logs within Splunk



# SOC Home Lab

## Project Overview

This project documents the design and implementation of a virtual Security Operations Center (SOC) laboratory.

The lab is being built to develop hands-on experience in security monitoring, log collection, threat detection, incident investigation, and SIEM administration.

## Lab Environment

| Component | Configuration |
|---|---|
| Hypervisor | VMware Workstation Pro 26H1 |
| SIEM Server | SIEM1 |
| Operating System | Windows Server 2022 Standard |
| IPv4 Address | 10.10.1.22/24 |
| Default Gateway | 10.10.1.1 |
| DNS Server | 8.8.8.8 |
| VMware Tools | Installed and Running |

---

## Phase 1 - SIEM1 Deployment and Configuration

The first phase of the SOC lab consisted of deploying and preparing the Windows Server that will support the SIEM environment.

### Tasks Completed

- Deployed the SIEM1 virtual machine
- Installed Windows Server 2022
- Configured a static IPv4 address
- Configured the default gateway and DNS server
- Installed VMware Tools
- Verified the VMware Tools service using PowerShell
- Prepared SIEM1 for the next phases of the SOC environment

### SIEM1 - Windows Server 2022

![SIEM1 Windows Server](images/siem1-windows-server.png)

SIEM1 is deployed as a Windows Server 2022 virtual machine running on VMware Workstation Pro.

### Network Configuration

![SIEM1 Network Configuration](images/siem1-network-config.png)

SIEM1 uses a static IPv4 configuration to provide a consistent network address for communication and future security log collection within the SOC lab.

**Network configuration:**

- IPv4: `10.10.1.22`
- Subnet mask: `255.255.255.0`
- Default gateway: `10.10.1.1`
- DNS: `8.8.8.8`

### VMware Tools Verification

![VMware Tools Verification](images/vmware-tools-verification.png)

VMware Tools was verified from PowerShell using:

`Get-Service VMTools`

The service returned a `Running` status, confirming that VMware Tools is operational.

---

## Current Status

**Phase 1 - SIEM1 Deployment and Initial Configuration: Completed**

The next phases will expand the lab with additional systems, centralized log collection, SIEM configuration, detection engineering, and security investigations.

## Skills Demonstrated

- VMware Workstation administration
- Windows Server deployment
- Static IPv4 configuration
- Virtual machine administration
- PowerShell service verification
- SOC lab architecture and documentation

---

## Phase 2 - Windows Server 2019 Deployment and Configuration

The second phase of the SOC lab consisted of deploying and configuring an additional Windows Server 2019 virtual machine.

This system will be used as part of the lab infrastructure for future security monitoring, log collection, and investigation activities.

### Tasks Completed

- Created the Windows Server 2019 virtual machine
- Installed Windows Server 2019
- Renamed the system to `Windows2019`
- Configured a static IPv4 address
- Configured the default gateway and DNS server
- Installed VMware Tools
- Verified the VMware Tools service using PowerShell
- Disabled automatic Server Manager launch at logon
- Installed available Windows updates
- Prepared the system for integration into the SOC lab

### Windows Server 2019 Deployment

![Windows Server 2019](images/windows2019-server.png)

The `Windows2019` virtual machine was successfully deployed using VMware Workstation Pro.

### Network Configuration

![Windows Server 2019 Network Configuration](images/windows2019-network-config.png)

A static IPv4 configuration was assigned to maintain consistent communication with the other systems in the SOC lab.

**Network configuration:**

- Hostname: `Windows2019`
- IPv4: `10.10.1.19`
- Subnet mask: `255.255.255.0`
- Default gateway: `10.10.1.1`
- DNS: `8.8.8.8`

### VMware Tools Verification

![Windows Server 2019 VMware Tools](images/windows2019-vmware-tools.png)

VMware Tools was verified using PowerShell:

`Get-Service VMTools`

The `Running` status confirms that the VMware Tools service is operational.

### Phase 2 Status

**Windows Server 2019 Deployment and Initial Configuration: Completed**

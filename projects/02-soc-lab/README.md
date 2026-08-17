# SOC Home Lab

## Project Overview

This project documents the design and implementation of a virtual Security Operations Center (SOC) laboratory.

The lab is being built to develop hands-on experience in security monitoring, log collection, threat detection, incident investigation, Windows administration, and SIEM operations.

The environment is deployed using VMware Workstation Pro and currently consists of four virtual machines connected to the same virtual network.

---

## Lab Environment

| System | Operating System | Role | IPv4 | Status |
|---|---|---|---|---|
| SIEM1 | Windows Server 2022 Standard | Primary SIEM Server | `10.10.1.22/24` | ✅ Configured |
| Windows2019 | Windows Server 2019 | Windows Lab Server | `10.10.1.19/24` | ✅ Configured |
| Windows11 | Windows 11 | Endpoint Workstation | `10.10.1.11/24` | ✅ Configured |
| SIEM2 | Windows 11 | Secondary SIEM Workstation | `10.10.1.18/24` | ✅ Configured |

**Virtualization platform:** VMware Workstation Pro 26H1  
**Network:** `10.10.1.0/24`  
**Default gateway:** `10.10.1.1`  
**DNS server:** `8.8.8.8`

---

## Current Lab Architecture

```text
                         SOC Home Lab
                              |
                     VMware Workstation Pro
                              |
                        10.10.1.0/24
             _________________|_________________
            /                 |                 |                 \
           /                  |                 |                  \
        SIEM1            Windows2019        Windows11            SIEM2
  Windows Server 2022  Windows Server 2019   Windows 11          Windows 11
   Primary SIEM Server   Lab Server           Endpoint       Secondary SIEM
      10.10.1.22         10.10.1.19         10.10.1.11        10.10.1.18
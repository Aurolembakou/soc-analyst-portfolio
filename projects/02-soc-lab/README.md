## Lab Environment

| System | Operating System | Role | IPv4 | Status |
|---|---|---|---|---|
| SIEM1 | Windows Server 2022 Standard | SIEM Server | `10.10.1.22/24` | ✅ Configured |
| Windows2019 | Windows Server 2019 | Windows Lab Server | `10.10.1.19/24` | ✅ Configured |

**Virtualization platform:** VMware Workstation Pro 26H1  
**Default gateway:** `10.10.1.1`  
**DNS server:** `8.8.8.8`

## Current Lab Architecture

```text
                  SOC Home Lab
                       |
              VMware Workstation Pro
                       |
                10.10.1.0/24
                 /           \
                /             \
        SIEM1                 Windows2019
  Windows Server 2022      Windows Server 2019
      10.10.1.22              10.10.1.19
          |                       |
     SIEM Platform          Monitored System
       (planned)              (planned)


**Important :** dans la partie architecture, les trois accents graves autour du diagramme doivent rester présents.

### 2. Améliorons le bas du README

Actuellement, `Current Status` et `Skills Demonstrated` se trouvent avant Phase 2. Ce serait plus logique de les avoir **tout à la fin**, car ils décrivent l'ensemble du projet.

Dans Notepad, supprime cette ancienne partie située après Phase 1 :

```markdown
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

## Lab Progress

| Phase | Description | Status |
|---|---|---|
| Phase 1 | SIEM1 - Windows Server 2022 deployment | ✅ Completed |
| Phase 2 | Windows Server 2019 deployment | ✅ Completed |
| Phase 3 | Next SOC lab component | ⏳ Upcoming |

## Skills Demonstrated

- VMware Workstation Pro administration
- Windows Server 2019 and 2022 deployment
- Virtual machine configuration
- Static IPv4 network configuration
- Windows Server administration
- VMware Tools installation and verification
- PowerShell service validation
- SOC lab infrastructure design
- Technical documentation with Git and GitHub

## Next Steps

The environment will be expanded progressively as the SOC lab develops. Planned activities include centralized log collection, SIEM integration, security monitoring, detection engineering, and incident investigation.

> This repository documents the lab as it is built. Screenshots and configurations are included as evidence of hands-on implementation.


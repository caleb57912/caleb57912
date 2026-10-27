<div align="center">

# 🧪 Caleb's Lab

**Homelab, security projects, and whatever I'm currently breaking and fixing.**

<a href="https://github.com/caleb57912/SOC-Homelab"><img src="https://img.shields.io/badge/SOC_Homelab-181717?style=for-the-badge&logo=github&logoColor=white"></a>
<a href="https://github.com/caleb57912/RMM-Homelab"><img src="https://img.shields.io/badge/RMM_Homelab-181717?style=for-the-badge&logo=github&logoColor=white"></a>
<a href="https://github.com/caleb57912/GRC-Homelab"><img src="https://img.shields.io/badge/GRC_Homelab-181717?style=for-the-badge&logo=github&logoColor=white"></a>
<a href="https://github.com/caleb57912/AWS-Migration-Design"><img src="https://img.shields.io/badge/AWS_Migration_Design-181717?style=for-the-badge&logo=github&logoColor=white"></a>

</div>

---

## 🏠 The lab

| | |
|---|---|
| 🖥️ **Compute** | Proxmox VE server running VMs, game servers, and dedicated security and management segments |
| 🌐 **Network** | Ubiquiti UDR at the edge with zone-based firewalling, Cisco Catalyst 3750-X for switching and traffic mirroring |
| 🛡️ **Security** | A SOC on its own VLAN watching the real home network |
| 🧭 **Management** | An RMM and a GRC platform on a separate management VLAN, monitored by the SOC |

---

## 🔬 Projects

I run my home network like a small organization: one program, split into three repos.

| Project | What it is | Status |
|---|---|---|
| [SOC-Homelab](https://github.com/caleb57912/SOC-Homelab) | **Detect and respond.** A Security Operations Center segment defending my home network: Splunk, Sysmon, Pi-hole, Wazuh, Zeek, Suricata, MISP, TheHive, Shuffle, Velociraptor | 🚧 Building · Phase 3 |
| [RMM-Homelab](https://github.com/caleb57912/RMM-Homelab) | **Manage and automate.** Self-hosted RMM for inventory, patching, scripting and remote access, run the way an MSP runs a client | 📐 Planned |
| [GRC-Homelab](https://github.com/caleb57912/GRC-Homelab) | **Govern.** Policies, a CIS Controls v8 assessment backed by real evidence, a risk register and compliance reporting | 📐 Planned |

```mermaid
flowchart LR
    RMM[RMM-Homelab<br/>manage + automate] -->|deploys agents| SOC[SOC-Homelab<br/>detect + respond]
    SOC -->|monitors| RMM
    RMM -->|inventory, patch status| GRC[GRC-Homelab<br/>govern]
    SOC -->|benchmark scores, logging coverage| GRC
```

### ☁️ Cloud

| Project | What it is | Status |
|---|---|---|
| [AWS-Migration-Design](https://github.com/caleb57912/AWS-Migration-Design) | **Design and migrate.** A HIPAA-aligned AWS migration for a fictional 8-clinic healthcare network: multi-AZ architecture, AWS HealthImaging for DICOM, Terraform for the full design, and a live deploy slice that's verified and then torn down | 🚧 Building · Phase 1 |

---

## 🔧 Currently working on

- Getting every log source into Splunk: firewall, switch, hypervisor, DNS and endpoint telemetry are in
- Endpoint onboarding as a single script: Sysmon, audit policy and a Splunk forwarder managed by a deployment server
- Planning the management VLAN that the RMM and GRC platforms will run on
- Designing an AWS migration for a healthcare clinic network, with a reason recorded for every architecture decision

---

## 🧰 In the lab

![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=flat-square&logo=proxmox&logoColor=white)
![Splunk](https://img.shields.io/badge/Splunk-000000?style=flat-square&logo=splunk&logoColor=white)
![Sysmon](https://img.shields.io/badge/Sysmon-0078D4?style=flat-square)
![Pi-hole](https://img.shields.io/badge/Pi--hole-96060C?style=flat-square&logo=pihole&logoColor=white)
![Ubiquiti](https://img.shields.io/badge/Ubiquiti-0559C9?style=flat-square&logo=ubiquiti&logoColor=white)
![Cisco](https://img.shields.io/badge/Cisco-1BA0D7?style=flat-square&logo=cisco&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

**Up next:**
![Wazuh](https://img.shields.io/badge/Wazuh-005571?style=flat-square)
![Suricata](https://img.shields.io/badge/Suricata-EF3B2D?style=flat-square)
![Zeek](https://img.shields.io/badge/Zeek-2B5797?style=flat-square)
![MISP](https://img.shields.io/badge/MISP-1F4E79?style=flat-square)
![Tactical RMM](https://img.shields.io/badge/Tactical_RMM-1F6FEB?style=flat-square)
![CISO Assistant](https://img.shields.io/badge/CISO_Assistant-6E40C9?style=flat-square)
![CIS Controls v8](https://img.shields.io/badge/CIS_Controls_v8-2EA043?style=flat-square)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![CloudFormation](https://img.shields.io/badge/CloudFormation-FF4F8B?style=flat-square)
![AWS CDK](https://img.shields.io/badge/AWS_CDK-FF9900?style=flat-square)

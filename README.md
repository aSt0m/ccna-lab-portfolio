<div align="center">

# 🌐 Cisco CCNA (200-301) — Lab Portfolio

[![Cisco](https://img.shields.io/badge/Cisco-CCNA%20200--301-blue?style=for-the-badge&logo=cisco&logoColor=white)](https://www.cisco.com/)
[![Packet Tracer](https://img.shields.io/badge/Simulator-Packet%20Tracer%208.x-brightgreen?style=for-the-badge)](https://www.netacad.com/)
[![GNS3](https://img.shields.io/badge/Emulator-GNS3%20Environment-orange?style=for-the-badge&logo=gns3&logoColor=white)](https://www.gns3.com/)
[![Wireshark](https://img.shields.io/badge/Analysis-Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white)](https://www.wireshark.org/)

<p align="center">
  Repositorio estructurado de laboratorios prácticos, diagramas de topología, esquemas de direccionamiento IP y configuraciones Cisco IOS para la preparación y dominio de la certificación <b>Cisco Certified Network Associate (CCNA 200-301)</b>.
</p>

</div>

---

## 📌 Acerca de este Repositorio

Este espacio reúne implementaciones prácticas que cubren los seis dominios oficiales del temario de certificación CCNA. Cada práctica incluye:
- **Diagrama de topología** en alta resolución.
- **Tabla de direccionamiento** completa (IPv4/IPv6, VLSM, VLANs).
- **Archivos de emulación/simulación** descargables (`.pkt` para Packet Tracer y proyectos portables para GNS3).
- **Configuraciones en texto plano** (`running-config` de switches y routers) para auditoría y control de versiones.
- **Evidencias de verificación** mediante salidas de comandos CLI y análisis de tráfico en Wireshark.

---

## 📂 Estructura del Proyecto

El repositorio está organizado de forma modular, separando la lógica de red por tecnología y dominio de estudio:

```text
ccna-lab-portfolio/
│
├── .gitignore                          # Exclusión de binarios volátiles e imágenes pesadas
├── README.md                           # Portada y documentación global del portafolio
│
├── 01-network-fundamentals/            # Modelos OSI/TCP-IP, IPv4, IPv6, Subnetting y VLSM
│   └── 01-ipv4-subnetting-vlsm/
│       ├── README.md
│       ├── topology.png
│       └── configs/
│
├── 02-network-access/                  # Switching L2/L3, VLANs, Trunking, EtherChannel, Spanning-Tree
│   ├── 01-vlan-trunking-802.1q/
│   │   ├── README.md
│   │   ├── topology.png
│   │   ├── vlan-trunking.pkt
│   │   └── configs/
│   │       ├── SW1-running.cfg
│   │       └── SW2-running.cfg
│   └── 02-spanning-tree-rstp/
│       ├── README.md
│       ├── topology.png
│       └── configs/
│
├── 03-ip-connectivity/                # Enrutamiento estático, OSPFv2 (Single & Multi-Area), Gateway Redundancy
│   ├── 01-ospfv2-single-area/
│   │   ├── README.md
│   │   ├── topology.png
│   │   ├── configs/
│   │   └── captures/                  # Capturas de paquetes relevantes (.pcapng)
│   └── 02-ospf-multi-area-gns3/
│       ├── README.md
│       ├── topology.png
│       ├── ospf-lab.gns3project
│       └── configs/
│
├── 04-ip-services/                     # NAT/PAT, DHCP Snooping, NTP, DNS, SNMP, Syslog
│   ├── 01-nat-pat-overload/
│   └── 02-first-hop-redundancy-hsrp/
│
├── 05-security-fundamentals/           # ACLs estándar y extendidas, Port Security, DAI, SSH
│   ├── 01-standard-extended-acls/
│   └── 02-layer2-security-mitigation/
│
└── 06-automation-programmability/      # Fundamentos de SDN, REST APIs, JSON, scripts de automatización
    └── 01-netmiko-config-backup/
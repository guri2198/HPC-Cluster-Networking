# HPC Cluster Deployment

## Overview

This repository documents the deployment and configuration of an HPC (High Performance Computing) cluster. It includes the physical network setup, Ruckus switch configuration, LACP (IEEE 802.3ad) implementation, network validation, and troubleshooting documentation.
<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/00eefff0-d7fc-4775-8417-8f5bfe3f282d" />

The goal is to provide a reproducible deployment guide and maintain a record of the cluster infrastructure.

---

## Features

* Physical HPC cluster setup
* Network topology documentation
* Ruckus switch configuration
* LACP (802.3ad) bonding configuration
* HPC network configuration
* Network validation and testing
* Troubleshooting guide
* Deployment scripts

---

## Infrastructure

### Hardware

* 4 × HPC Servers
* Ruckus ICX Switch
* Ethernet Cables
* Rack-mounted Infrastructure

### Software

* Linux
* NetworkManager (`nmcli`)
* LACP (IEEE 802.3ad)
* SSH

---

<img width="1014" height="1022" alt="WhatsApp Image 2026-06-05 at 17 23 31" src="https://github.com/user-attachments/assets/e719d4fd-e1dd-4974-a285-a912c695d00c" />


## Repository Structure

```text
hpc-cluster-deployment/
│
├── README.md
├── physical/
│   ├── rack-layout.md
│   ├── cabling.md
│   └── topology.drawio
│
├── switch/
│   ├── configs/
│   ├── backups/
│   └── show-commands.md
│
├── hpc/
│   ├── hpc1/
│   ├── hpc2/
│   ├── hpc3/
│   └── hpc4/
│
├── scripts/
│   ├── configure_lacp.sh
│   ├── verify_network.sh
│   └── collect_logs.sh
│
├── outputs/
│   ├── bond_status.txt
│   ├── ping_results.txt
│   └── switch_output.txt
│
├── diagrams/
│   └── topology.png
│
└── docs/
    ├── implementation.md
    ├── troubleshooting.md
    └── rollback.md
```

---

## Deployment Workflow

1. Install and rack the HPC servers.
2. Connect all servers to the Ruckus switch.
3. Configure switch ports and LACP.
4. Configure network bonding on each HPC node.
5. Verify LACP status and interface health.
6. Test connectivity and redundancy.
7. Document configuration and validation results.

---

## Validation Checklist

* [ ] All physical links are connected.
* [ ] Switch ports are operational.
* [ ] LACP bundle is established.
* [ ] Bond interface is active.
* [ ] All HPC nodes can communicate.
* [ ] Failover works correctly.
* [ ] Network performance is verified.

---

## Useful Commands

### Check interfaces

```bash
ip link
ip addr
```

### Verify bonding

```bash
cat /proc/net/bonding/bond0
```

### Check routes

```bash
ip route
```

### Test connectivity

```bash
ping <destination-ip>
```

### SSH

```bash
ssh user@<server-ip>
```

---

## Future Enhancements

* VLAN configuration
* Network automation
* Monitoring and alerting
* Performance benchmarking
* Configuration backup
* Ansible-based deployment

---

## Author

**Guri**

---

## License

This project is intended for internal infrastructure documentation and deployment.

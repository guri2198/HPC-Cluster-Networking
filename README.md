hpc-lacp-deployment/
│
├── README.md                     # Project overview
├── LICENSE
├── .gitignore
│
├── docs/
│   ├── architecture.md           # Overall network architecture
│   ├── topology.png              # Network diagram
│   ├── implementation.md         # Step-by-step implementation
│   ├── troubleshooting.md        # Common issues & fixes
│   ├── validation.md             # How to verify LACP
│   └── rollback.md               # Recovery procedure
│
├── configs/
│   ├── ruckus/
│   │   ├── switch-config.txt
│   │   └── lacp-port-channel.txt
│   │
│   ├── hpc1/
│   │   ├── bond.conf
│   │   ├── nmcli.sh
│   │   └── network.conf
│   │
│   ├── hpc2/
│   ├── hpc3/
│   └── hpc4/
│
├── scripts/
│   ├── configure_lacp.sh
│   ├── verify_lacp.sh
│   ├── network_check.sh
│   └── collect_logs.sh
│
├── diagrams/
│   ├── physical_topology.drawio
│   ├── physical_topology.png
│   └── logical_topology.png
│
├── outputs/
│   ├── ip_addr.txt
│   ├── ip_link.txt
│   ├── bond_status.txt
│   ├── switch_show_lacp.txt
│   └── ping_tests.txt
│
└── CHANGELOG.md

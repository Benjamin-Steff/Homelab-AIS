Internet
   │
Box FAI
   │
Réseau domestique 192.168.X.0/24
   │
Proxmox
   │
pfSense (VM 100)
   ├── WAN → 192.168.42.254
   └── LAN → 10.0.0.1/16
            ├── Windows Server (AD)
            ├── Windows Clients
            └── CrowdSec
